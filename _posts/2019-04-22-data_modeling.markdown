---
layout: post
title:      "Data Modeling"
date:       2019-04-22 20:30:21 -0400
permalink:  data_modeling
---


![](https://images.unsplash.com/photo-1531492898132-a3dfbc4dbac1?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=900&q=80)

**What is it?**

Data is everywhere. There are objects in front of you right now, both physical and digital, with attributes of their own. You computer has a brand, a color, a release year, an OS, and more. Your desk was made with a specific material, in a country, by a specific company. With so much information in the world, it is helpful to standardize it into a consistent, shareable, and scalable format. That is where data modeling comes in. 

Data models create frameworks that standardize the storage and organization of data. By creating a model we can avoid some common pitfalls when working with large amounts of data, say in a spreadsheet. Structuring data into a model allows for consistent data formatting and gives us insight in to the relationships of various objects.

Below is a basic example of a data model in the Physical stage. You can see the chart shows three entities, each with their own attributes and connected by specific relationships. More on this later. 

![](https://d3n817fwly711g.cloudfront.net/blog/wp-content/uploads/2012/06/relational-database-model1.png)


**When to use it?**

Data Modelling is helpful in any project that requires standard, searchable, consistent data as a resource. Largely models are helpful in giving individuals that aren't in the trenches with data everyday a better understanding of how the information they are generating is stored and accessed. Simply, they allow analysts, programmers, testers, manual writers, and others better understand the organizations data resource structure. Models are meant to be living, breathing formats that are scalable and change with the business and architectural needs. 

**Stages of Data Modelling?**

There are three main stages of data modelling that differ in specificity and relatedly, readability. Each is outlined below:

1. Conceptual Stage

In this stage the entities are represented with simplistic boxes representing each entitiy and lines connecting those boxes representing relationships. This stage is meant to keep information highly abstract and easy to understand. This is a great version to share with clients or other non-technical organization members to help them better understand the data structure.

2. Logical Stage

Information gets a bit more specific in this stage. Here we add important attributes to each entity helping to describe what they are composed of. In addition, we label what attributes are key and non key based. This means we label when an attribute is referencing the key of another entity. If an attribute is simply an aspect of an object it is a non key. 

3. Physical Stage

This stage is where we get ready for implementation and take specific actions toward that end. We now reference entities as "tables" and look at attributes as "columns." This is how our database will be thinking about this information so it is important we begin to as well. In addition, the table names and attribute names become less friendly in this stage as we adhere to specific database naming conventions. These names must align with the database framework we intend to use. 
