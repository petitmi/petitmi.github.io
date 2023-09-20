---
authors:
 - "Nyx"
title: "How Does a Large-scale Data Product work?"
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

After my birth, I transitioned to a **remote server**, moving from a **database** to a **data warehouse**. Then I participated in various **analyzes**, with plenty of activities of being extracted and transformed. Finally, my lagacy contributes to an **online recommendation product** running in production, which operates on terminal phones. The product facilitates the birth of more data pieces like me.

My community is diverse, comprising **structured data** that can be easily stored in tables, **unstructured data** such as audio and text documents, and even **semi-structured data** that combines elements of both, like email.

## Delivery
The data product can be an **analysis report, a visualization dashboard, or an automatic data model running in production**, depending on different business objectives and phases. However, regardless of the type of data product, substantial data analysis is required. Various methods, such as exploratory data analysis, machine learning, and deep learning, are typically applied and often combined to obtain results.

## Data Preperation
The tasks here primarily involve **data cleaning, wrangling, and transformation**, rendering the data in a format suitable for mathematical and computational operations. To illustrate this process with the early-stage Natural Language Processing (NLP) as an example, words are indexed based on their occurrence in the corpus, typically organized into 'bags of words'.

## Data Storage
We store various types of data in different formats and locations to serve different purposes. Massive computations occur during the early hours on mountains of high-volume remote servers. A 1TB hard drive can accommodate up to 200 billion words, while large internet companies often need to process PBs (1PB = 1024TB) of data per day. Therefore robust data processing streams and data warehousing stacks are needed.

**Data warehouses** typically consist of three layers: the operational data store (ODS), common data model (CDM), and application data service (ADS). The ODS primarily stores raw or lightly structured data. The CDM contains highly detailed factual data, public summary data, and dimension data. Data in the ADS layer is intended for direct use, such as metrics displayed on data dashboards.
 

## Data Collection
If we don't record the data, we won't have it. It might sound trivial, but it's a truth. If we miss how users react when watching the videos, we won't be able to analyze why people are leaving the video channel on our product, not to mention building personalized video recommendations for users.

Data logging is typically the responsibility of front-end and back-end engineers, but data scientists must clearly define the timing and format for **tracking events**. This also requires a scalable and long-term vision for the data products.