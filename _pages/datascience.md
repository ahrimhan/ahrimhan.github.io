---
permalink: /datascience/
title: "Data Science"
author_profile: true
---

[1. Why do I want to become a data scientist? Why do I want to transit from academia to industry?](#reasondatascientist)  
[2. What areas am I interested? What project will I do in Insight?](#projecttoperform)  
[3. Why do I choose Insight Data Science Fellows Program?](#reasoninsight)
[4. Data Science Related Projects](#datascienceproject)


## 1. Ph.D Research

My main research area has been software engineering in Computer Science. My main research interests include software maintenance and empirical studies. I have used statistics, data mining, and automated software analysis techniques to assess and improve the software design quality of maintainability.

In research on change-proneness prediction, I proposed the new behavioral dependency metric that captures the aspects of the dynamic behavior program, and these metrics in conjunction with existing structural metrics help to make a more accurate prediction change-proneness model. (https://ahrimhan.github.io/portfolio/research_project1/)


In research on refactoring candidate identification for the large-scale software, I proposed several new methods to find the cost-effective refactorings that can efficiently improve maintainability using dynamic information, multiple refactorings, and a two-step approach. (https://ahrimhan.github.io/portfolio/research_project2/) For the scalable computing, I also provided a fast refactoring candidate assessment metric, which can evaluate candidates quickly using the matrix computation. (https://ahrimhan.github.io/portfolio/research_project3/)

More information about my research and published papers can be found in the following links: [research](https://ahrimhan.github.io/research/) and [publications](https://ahrimhan.github.io/publications/).


## 2. Skills and tools



## 3. Side Project / Ongoing Project (from kaggle, not academic)

flight ticket prediction
오빠랑 돌려본것 (금) - wisconsin breast cancer
Yelp reviews

## 4. Course work

developing countries

## 5. Why data scientist? <a name="mg"></a>

===

## 1. Reason to become a data scientist

### Software engineering and Data Science

My main research area has been **software engineering** in Computer Science.
Software engineering provides systematic methods, automated tools, techniques, processes to assist developers for software development. Using various data, the researchers in software engineering have solved the problems such as `defect prediction` and `software failure estimation`. Data science and software engineering are very similar in that they are both data-driven activities.


### Reason to become a data scientis and to transit from academia to industry

Data scientists are becoming more popular these days, and I want to become a data scientist in high tech software companies.

First, I have been studying on assessing and improving software design quality using statistics, data mining, and automated software analysis techniques. Building a career path as a data scientist is a way to continue to use my research background.

Second, I would like to have a chance to work on analyzing the large-scale data set for solving real-world problems. I want to expand my work from the software to users and find business insights such as predicting user behavior patterns by analyzing various kinds of data sets (e.g., behavioral traces of user interactions with online systems).

Third, I want to feel excited by working in leading tech companies. I am fast to learn new technologies and enjoy working in a dynamically changing environment. As my major is computer science and software engineering, I can quickly learn the newest innovations in deep learning and machine learning techniques, which can help me to become an advanced data scientist.

## 2. Project Plan in Insight

I would like to analyze the data of online consumer reviews and find business insights. The rich data of consumer reviews (e.g., reviews at Yelp or Amazon) or reactions (e.g., likes at Facebook) is the valuable source of finding business insights and patterns. Yelp has opened the dataset and I am planning to use this data to answer the following questions.

* What are the characteristics of fake reviews?
* What reviews do not customers trust? (e.g., reviews full of compliments, highly rating scores with a few reviews, short comments written for the free food, etc.)
* What reviews do customers trust? (e.g., highly ranked in the search, rating scores over 4, many well-organized menu photos, many high-resolution food photos, many reviews from elite members, etc.)

I am also interested in software defect prediction, fraud news detection, and challenges using Kaggle data set. I will keep in finding more interesting projects and choose the final project after receiving comments from mentors during the program.


## 3. Reason for the Insight Data Science Fellows Program

아카데미아에서 회사로
분야도 바꾸어서
나라도 바꾸어서
이런 나에게 기회를 주는 프로그램. 너무 감사하고 이런 프로그램을 알게 되어서 너무 럭키하고.

지금 나는 아카데미아에서 회사로써의 트랜지션이라는 큰 도전을 페이싱 하고 있는데
내가 관심이 많고 잘 할수 있을 것 같은 직업인 데이터 사이언스로서 앞으로 커리어를 쌓고 성장하고 싶다.



<cover letter>
I am eager to have an opportunity to participate in the Insight Data Science Fellows Program. If I get an offer, I will do my best to show all my potentials in the project. I strongly believe I can successfully transit the career from a researcher in software engineering to a data scientist in industry.

I am now currently want to work in Orange County, but I am available to move to Silicon Valley or Seattle areas next summer.

## 4. Data Science Related Projects

### [Improvement of change-proneness prediction](/portfolio/research_project1/)

Software changed either to add new functionalities or to fix bugs. Some part of the software may be more prone to be changed than others. Finding software parts that are more likely to change can be useful because we can decide how to effectively invest the software maintenance efforts. In previous studies, most of the metrics used to build a change-proneness predictive model are based on the structural complexity of software programs.

To improve the accuracy of the change-proneness prediction, I propose the new behavioral dependency metric that captures the aspects of the dynamic behavior program.


### [Efficient refactoring candidate identification](/portfolio/research_project2/)

Recent research was focused on defining the cost-effective software refactoring process by suggesting the refactoring candidates that can maximize improvement in software design quality (e.g., maintainability). As the software is getting larger and more complex, it is harder to find the refactoring candidates because of the lack of resources in computing power and time. Therefore, we need a method to efficiently identify refactoring candidates for the large-scale software.

In this project, I propose the several new methods to improve the efficiency of the refactoring identification process.  

**Dynamic profiling-based refactoring identification**  
To identify the candidates in classes where real changes have occurred, I provided the method to use the ``dynamic profiling technique`` for finding the ``most frequently used functions`` based on the several scenarios of user behavior. Then, refactoring candidates are extracted to ``reduce the dependencies among the entities used in the most frequently used functions``.  

**Multiple and independent refactoring identification**  
To find a sequence of cost-effective refactorings, I proposed the method for selecting ``multiple refactorings that have no dependencies each other and can be applied simultaneously`` based on the concept of ``maximal independent set (MIS)``.  

**Two-phased search-based refactoring identification**  
``To reduce the search space of candidates to be examined``, I suggested using the ``two-phase approach``. In the first phase, the refactoring candidates that are more likely to improve maintainability are chosen using the [``Delta Table``](/portfolio/research_project3/), lightweight and fast candidate assessment. In the second phase, only the chosen refactoring candidates are evaluated using a more complex and precise fitness function.


### [Fast refactoring candidate assessment metric](/portfolio/research_project3/)

The cost for assessing refactoring candidates is computation-intensive. For automating refactoring identification, previous studies have limitations for assessing the impact of a large number of refactoring candidates.

In this project, I propose a fast refactoring candidate assessment metric, `Delta Table`. This metric is an efficient method for assessing the impact of refactoring candidates on maintainability based on matrix computation, which is approximate but fast. This metric helps to select the efficient refactoring candidates for the large-scale software.
