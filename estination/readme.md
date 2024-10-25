# Quick Start
The lab website is organized so that edits are made on the `source` branch, then
compiled via Jekyll. The compiled files make up the `master` branch. Thus, the
first step is to clone _both_ the `source` and `master` branches.

```
git clone -b source git@github.com:interactiveaudiolab/interactiveaudiolab.github.io.git interactiveaudiolab.github.io-source
git clone git@github.com:interactiveaudiolab/interactiveaudiolab.github.io.git
```

If you prefer HTTPS then do it this way.
```
git clone -b source https://github.com/interactiveaudiolab/interactiveaudiolab.github.io.git interactiveaudiolab.github.io-source
git clone https://github.com/interactiveaudiolab/interactiveaudiolab.github.io.git
```

Then, open the directory containing the `source` branch. Where you perform edits depends on
what edits you are making.
- If you want to add a course, dataset, person, or project, find the `collections` directory.
- If you want to add a paper, first find the `_data` directory and enter its bibtex into the `references.bib` file (please put it in the right place chronologically). Then you need to add the pdf of the paper in the `assets` directory.
- If you want to add an image or the pdf of a paper, find the `assets` directory.
- If you want to edit any of the other site text, find the `pages` directory.

**Note**: Any edits to the readme.md file must be performed in both branches.


Once you have finished your edits, you will need to do the following.

1. Compile the website using Jekyll _into_ the `master` branch
2. Push both the `source` and `master` branch to GitHub.


### Making sure you're ready to compile the website
Compilation of the website depends on Jekyll, which is a part of the Ruby ecosystem. Verify you have both Ruby  and the gem package manager by running the following.

```
gem --version
```

**Note** I (Bryan) had success with ruby 2.4.0. and 2.7.2 Consider installing `rbenv` as a ruby environment manager so that you can select the ruby version you use. Also, you will need a version of gem that is 2.7.0 or later to install Jekyll. Once you have gotten that version...

Run the following to install `jekyll` as well as a package management tool called `bundler`.

```
gem install jekyll
gem install bundler -v 2.1.4
```

**Note**: If you are using macOS High Sierra (10.13) or Mojave (10.14) or Catalina (10.15) you might experience
difficulties installing Jekyll by only running the above command.
If you receive the following error message, you may find [this post](https://github.com/jekyll/jekyll/issues/7274#issuecomment-445499110) helpful in resolving the issue.

```
ERROR:  Error installing jekyll:
ERROR: Failed to build gem native extension.
```

Then, navigate to the directory containing the source branch (it should have a file
called `Gemfile`) and run the following.

```
bundler install
```

This installs the rest of the RubyGems (packages) we need.

### Compiling the website
We can now compile the website to the directory containing the master branch.
Navigate to the directory containing the source branch and execute the following command.
```
jekyll serve --destination <master-branch-directory>
```
**Note**: If you receive an error, you may need to prefix the previous command with `bundle exec`. This will let ruby know which gems to use to make this go.
```
bundle exec jekyll serve --destination <master-branch-directory>
```
If this is the first time you're running this bundle, you may need to run `bundle install` to install missing gems.
```
bundle install
```
**Note**: Windows users may encounter a `Liquid Exception` complaining about Unicode
Normalization. Fix this by running `chcp 65001` in your terminal.


If compilation succeeded, the `<master-branch-directory>` directory should now be populated with the
newly-compiled site and your webpage will be locally visible at `http://localhost:4000`.


### Deployment
Website deployment is handled via GitHub. You now need to take 3 steps to deploy: Add any new files you've created to git control. Then commit the changes to them. Then push to github. You need to do this for **both** the source and master branches.

```
cd <your-local-branch-directory>

git add .

git commit -m "<your commit message goes here>"

git push origin <your branch name>
```
Remember do this for **both** source and master.

GitHub will render the `master` branch to `https://interactiveaudiolab.github.io`.


# Dependencies
- [Jekyll-Scholar](https://github.com/inukshuk/jekyll-scholar)
- [Bootstrap 4.0](https://getbootstrap.com/docs/4.0/getting-started/introduction/)
- [Jekyll](https://jekyllrb.com) (which uses Liquid markup)
- Markdown (jekyll specifically uses Kramdown)


# File structure / explanation
```
+--- _data: information on the navigation structure and BibTeX file.
+--- _includes: reusable templates used within layouts
+--- _layouts: HTML files for page rendering, referenced by markdown pages to generate layouts
+--- _plugins: for jekyll-scholar
+--- _site: autogenerated site -- this is what needs to get copied over to master
+--- assets
|   +--- bibliography: includes IEEE template for generating the publications page
|   +--- css: contains SASS files for customized bootstrap
|   +--- images
+--- Collections: markdown files, essentially the content of the site, sorted by category.
|   +--- _courses: teaching materials for courses
|   +--- _datasets
|   +--- _people-alumni
|   +--- _people-collaborators
|   +--- _people-current
|   +--- _posts: Posts is a category that is default to Jekyll, but this site will use it for news items
|   +--- _projects
+--- Old-demos: the content of the original site before the uplift
+--- Pages: other markdown pages of the site that do not fall under collections.

```

# Site structure
- Index
  - Projects, with individual pages for each project.
  - Publications
    - Publications-full: an alternate list of all publications as a static view
  - Resources
    - Datasets, with individual pages for each dataset.
    - Teaching, with individual pages for each course.
  - People (one page with the following anchor links)
    - Current
    - Collaborators
    - Alumni


# Explanation of collections

Collections are Jekyll's way of grouping related content. The pages have a YAML front matter block to set variables relevant to the page. The rest of the page is markdown content.

## Example front matter for each collection

### Courses

```
name: Machine Perception of Music and Audio
university: Northwestern University
course-number: CS 352
quarter-held: Winter 2019
navigation: resources
```

### Datasets

```
name: Dataset Sample
creators: [Demo Jones, Example Brown]
external-url: http://tunebot.cs.northwestern.edu/
external-url-text: Tunebot
image: https://via.placeholder.com/150
altdescription: placeholder text for the placeholder image
navigation: resources
```

### People (same for alumni, collaborators, and current)

```
name: E. G. Huang
position: Associate Professor
email: eg-huang@example.edu
website: google.com
image: https://via.placeholder.com/700
altdescription: 700 pixel square placeholder image
navigation: people
```
### Posts (news items)

```
title:  "Another News Post!"
date:   2018-12-28 10:55:02 -0600
categories: (this one is optional)
```

### Projects

```
name: Project Sample
creators: [Demo Jones, Sample Smith]
external-url: http://tunebot.cs.northwestern.edu/
external-url-text: Tunebot
image: https://via.placeholder.com/150
altdescription: Placeholder image #alt description of image for screen readers
funding: NSF
collection: projects
```

These variables can be utilized within the markdown content with the syntax ``{{ page.variable }}``

## Creating new items in a collection
1. Create a new markdown file in the appropriate directory
    a. Ex. A new member in the lab would be created in collections/_people-current
    b. The name of the file will be used to generate the URL for the individual page for that item, so make sure it's appropriately descriptive. (JohnSmith.md is better than John.md)
2. Add the YAML variables relevant to the item's collection category
    a. See the previous section for what variables are needed.
3. Under the dashed line, add the content of the entry, styled with Markdown. Jekyll specifically uses Kramdown. A guide/cheat sheet to markdown can be found [here](https://guides.github.com/features/mastering-markdown/).
    a. Most of the index pages for these collections utilize excerpts. This is a feature built into Jekyll that pulls, by default, the first paragraph of content as a preview to the full entry.
4. The exception to this process is Publications, which pulls information directly from a BibTeX bibliography with the help of jekyll-scholar. This file is located in _data/references.bib
    please note-- url's in the .bib file are intended to  point to an external link of the paper itself.
    Another important note: the publications page queries years from an array of `publication_years` located in the `config.yaml` file. Unfortunately this will need to be updated for every year there are publications to show.

# Writing content for accessibility

A huge component of making a site accessible to all users is ensuring that the content of the site is formatted in a way that makes it easier to be read by assistive technology. The main goal is to ensure there is more than one way to consume that content.

Some helpful tips for this as you add content to this site:

## Images
- Include alt text on all images! Good alt text describes the image in a way that explains both what the image actually depicts, but also indicates why it is there. If the point of the image is to evoke a feeling, for example, the alt text should try to do that too.
- If an image is purely decorative (like to divide content), use a blank alt tag so screen readers skip over it.
- In the same vein, putting text within an image is bad practice -- those who rely on screen readers, or can't load images, can't access that text to read it.

## Links
- The text of a link should describe where the link will take the user. A link that says "Read More" can be confusing for a user skipping to the link with tab navigation. Part of the philosoplhy of creating accessible websites is creating sites that act predictably.
- external links should have some indication that they take the user away from your site. It is sufficient to add within the writing that the link will open in a new window, but the follow code snippet can be used to construct a link that includes an image indicating it will open in a new window, and text saying as much for screen readers. This will work when added to Markdown as well:

```
<a class="external-link" target="_blank" title="description of link with context" href="#">Description of link
<span class="fas fa-external-link-alt" title="link opens in a new window"></span>
<span class="sr-only">opens in a new window</span>
</a>
```

## Headings
- Maintain the hierarchy of header tags -- Don't skip from h2 to h5. This can throw off screen readers that use this structure to create an outline for previewing content.
- On a similar note, when you are writing content you should start with h2, as h1 is set up on this site to display the title of the page.

## Lists
- If a piece of text is a list of items, or a table, use the semantic HTML markup for these formats. Things that look like a list that don't use the HTML syntax is difficult for a screen reader to navigate

# Deployment
Deployment is admittedly a bit hacky at the moment given the already-existing history in this repo, and the limitations that GitHub has on plugins that can be used on their site.
1. Once you're finished making changes in development, be sure to run ``jekyll serve`` to re-render the site. If you don't none of your changes will appear on the site.
2. merge any changes you've made into the ``source`` branch. This is, for our purposes, the master repo, as the ``master`` branch is just for the rendered site. Deal with conflicts that arise.
3. Checkout the master branch in a separate directory from the source branch you have been working on.
4. Copy the content of `_site` from the source branch directory into the new directory, replacing any previous files in master with the newly generated build files.
5. In your directory containing the master branch, add the new files to git with ``git add .``.
6. Commit your changes with ``git commit -m "merging source into master``.
7. Upload your changes to GitHub with ``git push``. This will trigger a re-render of the webpage.

The site may take a minute to re-render and publish.
