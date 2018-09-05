---
permalink: /datascience/
title: "Data Science"
author_profile: true
---

## Reason to Become a Data Scientist

### Software engineering and Data Science

My main research area has been **software engineering** in computer science.
Software engineering provides systematic methods, automated tools, techniques, processes to assist developers for software development. Using various data, the researchers in software engineering have solved the problems such as `defect prediction` and `software failure estimation`. Data science and software engineering are very similar in that they are both data-driven activities.


### Reason to become a data scientist and to transit from academia to industry

Data scientists are becoming more popular these days, and I want to become a data scientist in high tech software companies.

First, I have been working on evaluating and improving software design quality using statistical, data mining and automated software analysis techniques. Building a career path as a data scientist is a way to continue to use my research background.

Second, I would like to have a chance to work on analyzing the large-scale data set for solving real-world problems.
I want to expand my work from the software to users and find new insights into systems and business by leveraging big data intelligence.

Third, I want to feel excited about working in leading tech companies. I am fast to learn new technologies and enjoy working in a dynamically changing environment.
As my major is computer science and software engineering, I can quickly learn the newest innovations in deep learning and machine learning techniques, which can help me to become an advanced data scientist and machine learning engineer.


## Data Science Related Projects

### [Improvement of change-proneness prediction](/portfolio/research_project1/)  
*Type: Ph.D. research project*

Software changed either to add new functionalities or to fix bugs. Some part of the software may be more prone to be changed than others. Finding software parts that are more likely to change can be useful because we can decide how to effectively invest the software maintenance efforts. In previous studies, most of the metrics used to build a change-proneness predictive model are based on the structural complexity of software programs.

To improve the accuracy of the change-proneness prediction, I propose the new behavioral dependency metric that captures the aspects of the dynamic behavior program.


### [Efficient refactoring candidate identification](/portfolio/research_project2/)  
*Type: Ph.D. research project*

Recent research was focused on defining the cost-effective software refactoring process by suggesting the refactoring candidates that can maximize improvement in software design quality (e.g., maintainability). As the software is getting larger and more complex, it is harder to find the refactoring candidates because of the lack of resources in computing power and time. Therefore, we need a method to efficiently identify refactoring candidates for the large-scale software.

In this project, I propose the several new methods to improve the efficiency of the refactoring identification process.  

* [**Dynamic profiling-based refactoring identification**](/portfolio/research_project2/#dynamic)   
To identify the candidates in classes where real changes have occurred, I provided the method to use the ``dynamic profiling technique`` for finding the ``most frequently used functions`` based on the several scenarios of user behavior. Then, refactoring candidates are extracted to ``reduce the dependencies among the entities used in the most frequently used functions``.  

* [**Multiple and independent refactoring identification**](/portfolio/research_project2/#multiple)     
To find a sequence of cost-effective refactorings, I proposed the method for selecting ``multiple refactorings that have no dependencies each other and can be applied simultaneously`` based on the concept of ``maximal independent set (MIS)``.  

* [**Two-phased search-based refactoring identification**](/portfolio/research_project2/#twophase)   
``To reduce the search space of candidates to be examined``, I suggested using the ``two-phase approach``. In the first phase, the refactoring candidates that are more likely to improve maintainability are chosen using the [``Delta Table``](/portfolio/research_project3/), lightweight and fast candidate assessment. In the second phase, only the chosen refactoring candidates are evaluated using a more complex and precise fitness function.


### [Fast refactoring candidate assessment metric](/portfolio/research_project3/)  
*Type: Ph.D. research project*

The cost for assessing refactoring candidates is computation-intensive. For automating refactoring identification, previous studies have limitations for assessing the impact of a large number of refactoring candidates.

In this project, I propose a fast refactoring candidate assessment metric, `Delta Table`. This metric is an efficient method for assessing the impact of refactoring candidates on maintainability based on matrix computation, which is approximate but fast. This metric helps to select the efficient refactoring candidates for the large-scale software.

### [Supporting airline ticket purchase: Buy now or wait?](/portfolio/airlineticketPrediction/)  
*Type: Side project*

Airplane ticket prices fluctuate according to various conditions, and airlines do not disclose pricing policies, so it is difficult to forecast prices. Therefore, even if you board the same plane, the amount of money you pay for a seat varies greatly. Smart buyers want to pay the least amount of money to buy a plane ticket, but it is very difficult to decide when to buy a plane ticket. Online travel companies, such as Priceline, offer low fare alert services to help customers purchase airline tickets. When customers are interested in flights, they will be notified by email if the price have reached the one specified in advance. However, since these services are based on what has already happened, there is a disadvantage that if the prices continue to rise, they may miss the right time to buy an appropriate ticket.

To help customers buy airline tickets, I analyzed the data affecting airplane ticket prices and used data mining techniques to find patterns. Data on ``airplane fares`` and the ``factors affecting ticket prices`` (e.g., ``season``, ``week``, ``time``, and the ``number of stops``) are directly collected from ``Priceline`` and ``Kayak``. I also collected ``external factors`` (e.g., ``oil prices``) that can affect ticket prices. Based on the prediction that the airplane ticket will rise or fall tomorrow, I can assist customers to make the decision whether it is good to ``buy an airplane ticket now (Buy)`` or ``better to wait (Wait)``.


### [Model for Asia Countries using Global Competitiveness Index (GCI) Data](/portfolio/asiaModel/)  
*Type: Coursework project*

The World Economic Forum annually publishes the Global Competitiveness Index (GCI) data from around the world. We obtained the GCI data from 43 countries for a total of six years from 2002 to 2007. When considering countries with high ranked countries are advanced countries, I can find valuable insights of the advanced countries. This can be used as a model to suggest a direction for developing countries to become advanced countries. In this analysis, I focus on Asia countries.
