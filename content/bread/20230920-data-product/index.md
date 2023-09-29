---
authors:
 - "Nyx"
title: "How Does a Large-scale Data Product Work?"
date: 2023-09-20
description: ""
tags: ["data product", "data engineering"]
Categories: ["Article", "English"]
summary: "It's me - a piece of data, growing within the data flow."
---
<div id="google_translate_element"></div>

<script type="text/javascript">
function googleTranslateElementInit() {
  new google.translate.TranslateElement({pageLanguage: 'en'}, 'google_translate_element');
}
</script>

<script type="text/javascript" src="//translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"></script>

## How Data Flows
I was born when a fragment of **logging** code detected someone's click on an article, user's phone was my birthplace. I have timestamp, article ID, user ID, cookies and so many other organs that make up of me. 

It's me - a piece of data, growing within the **data flow**. 

After my birth, I transitioned to a **remote server**, moving from a **database** to a **data warehouse**. Then I participated in various **analyzes**, with plenty of activities of being extracted and transformed. Finally, the legacy of my community (and of course myself) contributed to an **online recommendation product** running in production, which operates on terminal phones. The product then facilitated the birth of more data pieces like me.

My community is diverse, comprising **structured data** that can be easily stored in tables, **unstructured data** such as audio and text documents, and even **semi-structured data** that combines elements of both, like email.

## Delivery
The data product can be an **analysis report, a visualization dashboard, or an automatic data model running in production**, depending on different business objectives and phases. However, regardless of the type of data product, substantial data analysis is required. Various methods, such as exploratory data analysis, machine learning, and deep learning, are typically applied and often combined to obtain results.

## Data Preperation
The tasks here primarily involve **data cleaning, wrangling, and transformation**, rendering the data in a format suitable for mathematical and computational operations. Illustrating this process with the early-stage Natural Language Processing (NLP), words are indexed based on their occurrence in the corpus, typically organized into 'bags of words'.

## Data Storage
We store various types of data in different formats and locations to serve different purposes. Massive computations occur during the early hours on mountains of high-volume remote servers. A 1TB hard drive can accommodate up to 200 billion words, while large internet companies often need to process PBs (1PB = 1024TB) of data per day. Therefore robust data processing streams and data warehousing stacks are needed.

**Data warehouses** typically consist of three layers: the operational data store (ODS), common data model (CDM), and application data service (ADS). The ODS primarily stores raw or lightly structured data such as detailed conditions for every user click. The CDM contains highly detailed factual data such as the details of every ordering process, public summary data such as per clicks of per users per day, and dimension data such as user labels. Data in the ADS layer is intended for direct use, such as metrics displayed on data dashboards.

Various data infrastructure may feature tailored layers, but they typically share similar concepts. 

## Data Collection
If we don't record the data, we won't have it. It might sound trivial, but it's a fundamental truth. It frequently occurs that we need to analyze something, only to discover suddenly that we lack even the raw data. For example, let's say we notice a decline in active users on our video channels and wish to uncover the reasons. We aim to examine the average total watch time for each user and delve into various categories. However, we overlooked collecting data on user activities during their video watching sessions, as well as the time and positions where they exit the videos. If we fail to do well in the analysis of user behaviors, not to mention to build personalized video recommendations for them.

Data logging is typically the responsibility of front-end and back-end engineers, but data scientists must clearly define the timing and format for **tracking events**. This also requires a scalable and long-term vision for the data products.