---
permalink: /research/
title: "Research"
author_profile: true
---

## Research Overview

My main research area has been **software engineering** in Computer Science. My main research interests include ``software maintenance`` and ``empirical studies``. I have used ``statistics``, ``data mining``, and ``automated software analysis techniques`` to assess and improve the software design quality (e.g., ``maintainability``).

For over 10 years, I focused on making an evolvable software. The ``maintainability`` of software deteriorates over time, and it is very important to maintain the software resilient to accommodate changes. Much of the total software development cost is spent on maintenance costs such as adding new features, fixing errors, and improving performance to adapt to a rapidly changing markets. Therefore, it is important to improve ``maintainability`` to reduce the software development cost.

I studied to answer the following questions.  
* **Change-proneness prediction**    
  * ``Which parts of the software change frequently?``  


* **Refactoring candidate identification**
  * ``Where should be fixed to improve software quality and reduce maintenance costs?``  
  * ``Which parts need to be fixed first for effective improvement within limited budgets, resources and time?``
  * ``How can we evaluate refactoring candidates more efficiently for the large-scale software?``


## Research Projects

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
