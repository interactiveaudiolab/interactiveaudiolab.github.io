---
layout: default
title: "Publications"
permalink: /publications/
---


{% include title.html%}

{% assign array = "2018,2017,2016,2015,2014,2013,2012,2011,2010,2009,2008,2007,2006" | split: "," %}

{:.bibtitle}
## 2018
{% bibliography --query @*[year=2018] %}

{:.bibtitle}
## 2017
{% bibliography --query @*[year=2017] %}

{:.bibtitle}
## 2016
{% bibliography --query @*[year=2016] %}  

{:.bibtitle}
## 2015
{% bibliography --query @*[year=2015] %}

{:.bibtitle}
## 2014
{% bibliography --query @*[year=2014] %}

{:.bibtitle}
## 2013
{% bibliography --query @*[year=2013] %}

{:.bibtitle}
## 2012
{% bibliography --query @*[year=2012] %}

{:.bibtitle}
## 2011
{% bibliography --query @*[year=2011] %}

{:.bibtitle}
## 2010
{% bibliography --query @*[year=2010] %}

{:.bibtitle}
## 2009
{% bibliography --query @*[year=2009] %}

{:.bibtitle}
## 2008
{% bibliography --query @*[year=2008] %}

{:.bibtitle}
## 2007
{% bibliography --query @*[year=2007] %}

{:.bibtitle}
## 2006
{% bibliography --query @*[year=2006] %}


