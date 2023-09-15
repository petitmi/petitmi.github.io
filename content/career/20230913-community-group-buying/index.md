---
authors:
 - "Nyx"
title: "Data Science In Community Group-Buying"
date: 2023-09-13
description: ""
tags: ["data science", "community group-buying"]
Categories: ["Article", "English"]
summary: "There are two dominant features in group-buying compared to the online retail model: the first is pre-sale with next-day delivery, and the other is community pickup."
---

As a novel online retail model, community group-buying transforms individuals' grocery habits, as well as the supply chain, logistics, and warehousing. This business model combines the Bulk Purchase Sorting with Pre-sale Model, allowing it to achieve wholesale prices, but customers don't need to purchase in wholesale quantities. The key factor to the success of this model lies in the optimization of the supply chain. A management and visualization system, constructed with various precise, efficient, and sophisticated data science techniques, makes this possible.

## Why do people change their daily grocery shopping habits?

No one could have imagined that a minor news report about unattributed lung inflammation in December would evolve into an unexpected black swan event that would profoundly influence the destiny of humankind. COVID-19 disrupted the forward march of nations and individuals, or perhaps it disrupted the mutual tug-of-war among nations and individuals in a state of standstill.

2019 the year was marked by the 70th anniversary of the founding of the People's Republic of China, the Hong Kong protests against the extradition bill, the intensification of the US-China trade war. And of course, there were other significant events in different regions, such as various wars in the Middle East and the devastating fire that consumed the Notre-Dame Cathedral in Paris, among many others. 

In 2019, the year was marked by the 70th anniversary of the founding of the People's Republic of China, the Hong Kong protests against the extradition bill, and the intensification of the US-China trade war. Of course, there were other significant events in different regions, such as various wars in the Middle East and the devastating fire that consumed the Notre-Dame Cathedral in Paris, among many others. The Covid-19 outbreak was not strongly correlated with these events, but its effects had a somewhat hidden yet obvious relationship.

In China, people were intermittently confined to their homes on a city-by-city basis for the next three years. People were only allowed to receive food deliveries rather than go outside to pick up food. However, the delivery system was also blocked, so those who delivered essentials to individuals could only do so on behalf of the community. This was the time when community group-buying became known throughout China, though it was not the time of its inception.

Working at a major online retail company and focusing on the community group-buying business allowed me to witness how community group-buying grew during the three years of Covid-19, when people were struggling with city lockdowns and economic devastation.

There are two dominant features in community group-buying compared to the online retail model: the first is **pre-sale with next-day delivery**, and the other is **community pickup**. Although this model is crucial during special situations like lockdown days, it also works well in normal daily life *if the prices are low enough, and the items are diverse and of high quality*.

## What is community group-buying?

Let's start with the giant Walmart. Walmart was founded in 1945, and it grew through chain stores and big box stores, eventually becoming an oligopoly in niche categories. Famous for its lowest prices, Walmart has succeeded in leveraging technology to transform its supply chain. On the demand side, what customers experience is a preference for coming to supermarkets like Walmart rather than convenience stores with higher prices. The reason behind this phenomenon is the automated equipment and systems introduced in multiple stages of the supply chain. This transformation has also resulted in numerous layoffs and career changes. 

Community group-buying is a retail business model where customers are accustomed to doing groceries online and will be able to pick them up the next day thanks to the **effective and efficient supply chain**. On this online platform, users can select all kinds of items, especially fresh produce, for tomorrow's pickup. Unlike the traditional big-box approach, products are not sorted and packaged for consumers all at once. Instead, they undergo distributed sorting through shared warehouses, central warehouses, grid warehouses, and community sites. Products are only categorized into individual portions once they reach the community sites. During the previous transportation processes, they are consolidated. Additionally, shipments and redistributions between different regions occur based on sales or demand predictions. 

*In a nutshell, the community group buying model combines the **Bulk Purchase Sorting** with **Pre-sale Model**, allowing it to achieve **wholesale prices**, but customers don't need to purchase in **wholesale quantities***.

## Tasks and Data Science Solutions in Community Group-Buying

### 1. Sales Prediction

When it comes to sales prediction, strategies and goals vary depending on different factors.

**Total sales prediction** primarily impacts macro-level decision-making and is often reflected on data dashboards. In this context, extreme precision is less critical, and our focus should be on identifying trends and achieving accuracy at a larger scale.

Nevertheless, when dealing with sales predictions at **hierarchical regional and categorical levels**, the goal of accuracy becomes more crucial. This level of accuracy directly influences immediate decision-making and specific actions, and any decrease in accuracy can result in significant cost increases. Therefore, the sales prediction in both niche regions and categories is usually the most important in this section.

Additionally, sales prediction tasks involve considerations of **time periods and granularity**. *Real-time and day-by-day forecasting* is essential. For longer timeframes, such as week-to-week or month-to-month predictions, aggregating the day-by-day results can provide solutions.

Given the complexity of sales prediction and the multitude of factors influencing sales, different strategies are required for different aspects. To gain a broader perspective and account for numerous factors, we may turn to *unexplainable models like deep learning models*. Input features are derived from various aspects of user activities and the supply chain, as well as external factors like weather. We also heavily rely on *correlation analysis, cluster analysis, and other explainably analytical methods* to obtain features. Finally, once the structure of the prediction model is complete, we need to add time series analysis into it.

### 2. Purchase Optimization 

This part is commonly used in various e-commerce analysis models. To attract more customers and enhance their purchasing experience, it is essential to conduct user analysis, marketing analysis, and implement a personalized recommendation system.

Understanding the **target customer base** and identifying **potential customers** is crucial. User segmentation based on factors such as occupation and consumption habits allows us to distinguish between existing customers and potential ones. Managing the user lifecycle can be achieved through the AARRR model, which stands for *Acquisition, Activation, Retention, Referral, and Revenue*. This model has been extensively researched and is a valuable tool. Additionally, specific *sub-analyses like Traffic Source Analysis, Conversion Rate Analysis, and Repeat Purchase Analysis* can be applied.

When it comes to implementing a personalized recommendation system, *Machine Learning Methods for prediction and ranking, as well as A/B Testing for evaluation*, have reached a high level of maturity.

### 3. Loss Management

This part is like doing accounting. We compare the ***initial quantity** and the **final quantity** at each stage and identify the factors contributing to significant losses. Once we have analyzed the results, we can employ additional management tools, such as real-time alerts, to intervene in the chain reaction caused by these losses.

Furthermore, it's crucial to proactively **forecast and manage risk**. Risks originate from both external and internal environments, such as weather, politics, and internal corruption, with varying degrees and impacts. During the COVID-19 pandemic, the highest risk factor was regional lockdowns, which could result in overstocking or excessive demand fluctuations.

Apart from these considerations, **route optimization**, including *geodata analysis*, and **inventory optimization**, including *dynamic programming*, should also be explored.

### 4. Quality Optimization

The community group-buying model offers lower prices and reasonable delivery times, which are its primary advantages. However, lower prices often coincide with lower product quality, which can deter regular customers.

To implement quality analysis, the first step is to establish an indicator that reflects the quality status. The most common indicator is the **refund rate**, which calculates the number of refunds for SKUs, orders, or users. It's caliber is *the number of SKUs/orders/users returned divided by the total number of sales/fulfillments on the date of sale/date of fulfillment*.

However, this indicator has a **latency** issue. Consider a scenario where you purchase a box of grapes, only to discover two days later that they are spoiled and need to be returned. Due to your schedule, it takes another day before you can return the item. This results in a three-day lag in the indicator. The indicator becomes accurate and stable only after the refund window has closed.

In this context, the second step involves **revising or predicting** this refund rate indicator to solve the latency issue. Initially, basic *time series analysis* can be employed for revision. However, as the business matures, more *advanced machine learning* and *causal inference methods* are required for prediction.

Basically, when predicting this indicator, we have already been engaged in the quality analysis. We analyzes **suppliers** and different **segments of the supply chain** to identify the key factors influencing product quality.

Of course, similar to predicting sales amounts, refund rates at hierarchical levels of **regions and product categories** must be considered differently. For example, a sudden decline in the quality of Shaanxi gala apples in Guangdong due to an unforeseen event may have a significant impact locally, but may not be reflected in the global caliber of the indicator.



