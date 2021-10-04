# coursera statistics standford
https://www.coursera.org/learn/stanford-statistics/lecture/3ita3/course-welcome
- course objective:
  - main tools for descriptive statistics which are essential for exploring data, with an emphasis on visualizing information
  - important ideas about sampling and conducting experiment
  - look over some **important rules of probability**
  - and discuss **normal approximation** and the **central limit theorem**
  - important concepts and pitfalls of **regression**
  - and how to do inference with **confidence intervals** and **tests hypotheses**
  - You will learn the key ideas about computer-intensive inference with the Monte Carlo method and the Bootstrap.
  - We will show you how to analyze **categorical data** and discuss one-way analysis of variance.
  - Finally, we will look at reproducibility, data snooping and the multiple testing fallacy and how to account for multiple comparisons.
  - These issues have become particularly important in the era of big data. 
- Broadly, there are three main reasons why statistical literacy is essential in data science.
  1. First, it provides the skills to assess whether the data are sufficient to answer the questions at hand.
  2. Second, it establishes a rigorous framework for quantifying uncertainty.
  3. And finally, it provides techniques for effectively communicating the findings of your analyses.


## week 1
This module provides an overview of the course and a review of the main tools used in descriptive statistics to visualize information. 
### Descriptive statistics and visualizing information
- summary - numerical summary -> graphical summary

### Numerical Summary Measure
- boxplot gives a 5 numbers summary of the data

## week 2
In this module, you will look at the main concepts for **sampling** and **designing experiments.**
You will learn about curious pitfalls and how to evaluate the effectiveness of such experiments.

### Learning Objectives
- Understanding the basics of statistical inference, sampling and designing experiments
- Getting familiar with the main pitfalls of sampling
- Ability to apply knowledge and understand real data sampling
- Ability to evaluate the effectiveness of designed experiments

### observational studies vs experiment, confounding, placebo effect <- GOLDEN
**observational study**: it measures outcomes of interest and this can be used to establish **association**
    - people who eat red meat have higher rates of certain cancers than people who don't
        - this means there is an association betweeen red meat consumption and cancer: there is a link between these two
        - but this **does not** mean that eating red meat causes cancer: people who don't eat red meat are known to exercise more and drink less alcohol
          - and it could be the latter two issues that causes the difference in cancer rates
- but **association is not causation**, because there maybe **confounding factors** such as exercise that are associated both with red meat consumption and cancer

**To establish causation, an experiment is required:**
> treatment is a technical term
- A **treatment**(e.g. eating red meat) is assigned to people in the **treatment group** but not to people in **control group**
- then the outcomes in the two groups are compared. to rule out confounders, both groups should be similar, apart from the treatment. to this end:
    - the subjects are assigned into treatment and control groups at random
    - when possible, subjects in the control group get a placebo: it resembles the treatment but is neutral. assigning a placebo makes sure that both groups are equally affected by the **placebo effect**: the idea of being treated may have an effect by itself
    - the experiment is **double-blind:** neither the subjects nor the evaluators know which subjects are assigned to treatment and which subjects are assigned to control
* the placebo effect is still not fully understood and is one of the most interesting phenomena in science
* Randomization makes sure that influences other than treatment influence both treatment and control group equally.
* mutual exclusive
