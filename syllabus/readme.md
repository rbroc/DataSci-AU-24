# Syllabus: Data Science, Prediction, and Forecasting #

**NB: The information presented here has been taken from the [AU Course Catalogue](https://kursuskatalog.au.dk/en/course/122493/Data-Science-Prediction-and-Forecasting). It should be viewed as indicative, rather than definitive. In the case of errors, the official AU version is binding.**

## Overview ##

### Purpose:
The purpose of the course is to introduce students to advanced statistical and computational methods required for the analysis of large, complex, and naturalistic data sets. In particular, students are introduced to state-of-the-art methods for the analysis of time series. In this area, a particular focus is placed on prediction and forecasting. Examples of relevant data sets are publicly available unit sales time series from large multinational companies, financial market time series, behavioural time series from cognitive-scientific and neuroscientific experimental studies, social media network data, data from wearable technology, and data from interactive sensors. Students will also be able to recognise important ethical, social, and policy implications arising from the application of advanced statistical analysis to human data, and to reflect on the ethical choices that must be made when developing data processing and statistical analysis software.  

The course covers advanced tools in data science, time series analysis, prediction, and forecasting. The course relates these tools to experimental and lab methodology, and to theories of cognitive functions. The course also includes integrated discussion of the ethical, social, and policy implications of the use of data science.

The course equips students with the computational tools to model and investigate human cognition and behaviour both at the individual and at the collective level. The course prepares students for a wide range of data processing and analysis career paths.

### Academic Objectives ###

In the evaluation of the student’s performance, emphasis is placed on the extent to which the student is able to:

1. Knowledge:
    - describe and contrast different computational and statistical methods for analysing large and complex data sets, in particular time series.

2. Skills:
    - identify relevant data sources for specific research and applied questions, and integrate data sources as needed
    - prepare and pre-process complex data for analysis
    - create visualisation of time series and other complex data.

3. Competences:
    - clearly and effectively present the results of complex analyses, in a way that is understood by non-specialists
    - critically evaluate the appropriateness of a given method for a given data set
    - recognise and analyse ethical, social, and policy issues arising from the use of data science methods and technology.


## Course Assessment ##

The examination consists of a take-home assignment on a topic of the student’s choice and a related practical product.

The assignment can be written individually or in groups of up to 4 students. Group assignments must be written in such a way that the contribution of each student, except for the introduction, thesis statement and conclusion, can form the basis of individual assessment. The assignment should clearly state which student is responsible for which section.

- Length for one student: 10-12 standard pages
- Length for two students: 17-22 standard pages
- Length for three students: 24-32 standard pages
- Length for four students: 31-42 standard pages

The scope and nature of the product must be relevant in relation to the content of the course and is subject to the approval of the teacher. It must be possible to submit the product digitally in a documented form which can be accessed by the examiner and co-examiner.

The product must be accompanied by a take-home assignment on a topic of the student’s choice, in which the student explains the relevance and methodological and theoretical basis of the product.
The assignment and the product must be submitted for assessment in the Digital Exam system before the deadline set in the examination plan. Assessment is based on an overall assessment of the take-home assignment and the practical product.

## Schedule ##

Each course element (1-12) is a four hour session, consisting of a 2hr lecture and 2hrs coding session.
Below is the plan for the course. In the _Reading_ column, you will find a number of suggested readings, mostly drawn he textbook we will follow throughout the course (see _Textbook_ Section below)

| Week  | Session | Teacher |  Lecture | Classroom | Reading |
| :---: | :-----: | ------- | ----------| -------| ---|
|  6   |    1    | Roberta | Course Overview & Modeling Cultures  | Formulating a Predictive Modeling Problem (`pandas`, `matplotlib/seaborn`)  | _Chapter 1_, _Suggested Readings_ |
|  7   |    2    | Roberta | Regression Algorithms & Evaluation | Linear Regression & KNN Models (`sklearn`, `numpy`) | _Chapters 2,3,7_  |
|  8   |    3    | Roberta | Classification, Overfitting & Regularization | Lasso & Ridge Regression in `sklearn` | _Chapters 4,6,9_ |
|  9   |    4    | Roberta | Bias-Variance Trade-off & Decision Trees  | Bias & Variance Simulation | _Chapter 8.1_    |
|  10   |    5    | Roberta | Bagging & Boosting  |  Random Forests & XGBoost (`sklearn`, `xgboost`) | _Chapter 8.2-3_  |
|  11   |    6    | Mads | Data Science in Industry | Cover letter and CV | [MLOps and DevOps: Why Data Makes It Different](https://www.oreilly.com/radar/mlops-and-devops-why-data-makes-it-different/); <br> Breiman, L. (2001). Statistical Modeling: The Two Cultures (with comments and a rejoinder by the author). _Statist. Sci._, 199–231. [https://doi.org/10.1214/ss/1009213726](https://doi.org/10.1214/ss/1009213726)   |
|  12   |    7    | Mads | Causal Data Science I  | Estimating causal effects | Peters, J., Janzing, D., & Schölkopf, B. (2017). Elements of causal inference: Foundations and learning algorithms. The MIT press. Chapters 2-3, https://mitpress.mit.edu/books/elements-causal-inference <br> Sharma, A., & Kiciman, E. (2020). DoWhy: An End-to-End Library for Causal Inference. arXiv:2011.04216. http://arxiv.org/abs/2011.04216|
|  14   |    8    | Mads | Causal Data Science II  | Causal discovery |  Glymour, C., Zhang, K., & Spirtes, P. (2019). Review of Causal Discovery Methods Based on Graphical Models. Frontiers in Genetics, 10, 524. https://doi.org/10.3389/fgene.2019.00524|
|  15   |    9    | Mads | Modeling Time Series   | Time series modelling | [Forecasting: Principles and Practice](https://otexts.com/fpp3/) chapters: 3, 7, 9 |
|  16   |   10    | Roberta | Neural Networks | Image/Audio Classification with CNNs (`torch`, `timm`, `transformers`) | _Chapter 10_ |
|  17   |   11    | Roberta | Project Presentations    | Project Presentations      | N/A |
|  18   |   12    | Roberta | Project Hackathon*  | Project Hackathon | N/A  |
|  19   |   13    | Roberta | Project Hackathonn  | Project Hackathon | N/A  |

*Might reintroduce unsupervised learning (dimensionality reduction and clustering)

Lectures take place Tuesday 14:00 - 16:00 and classes Wednesday 08:00 - 10:00.


## Textbook ## 

Throughout the course, we will follow this textbook:
* James, G., Witten, D., Hastie, T., Tibshirani, R., & Taylor, J. (2023). An introduction to statistical learning: With applications in Python. Springer Nature.

The textbook is freely available, and can be downloaded at this link: https://www.statlearning.com/
The textbook comes with a number of very nicely structured exercises at the end of each chapter. These are implemented as Jupyter notebooks and can be found at: https://github.com/intro-stat-learning/ISLP_labs.
You can use these to further practice things discussed during lectures, or to complement the practical exercises you will be presented with during our classes.

In you are in for the math, you can complement these readings with a parallel textbook which covers the same topics, but with more advanced mathematical content:
* Hastie, T., Tibshirani, R., Friedman, J. H., & Friedman, J. H. (2009). The elements of statistical learning: data mining, inference, and prediction (Vol. 2, pp. 1-758). New York: springer.

This is available at: https://hastie.su.domains/Papers/ESLII.pdf


## Suggested Readings ##

These readings present arguments that are foundational to the philosophy of the course, and they help contextualize the prediction _versus_ explanation dichotomy (as we will see, this is not really a dichotomy) in the context of cognitive sciences. 
We will explicitly focus on these in the first lecture. Reading them will make it much easier to contextualize methods and topics discussed throughout the course, and I thus suggest you pick a few of them and read them.
The order I have sorted them in is a good proxy for relevance.

* Yarkoni T, & Westfall J (2017). Choosing Prediction Over Explanation in Psychology: Lessons From Machine Learning. _Perspectives on Psychological Science_, available [here](https://doi.org/10.1177/1745691617693393)
* Shmueli G (2010), To Explain or to Predict?, _Statistical Science_, available [here](https://projecteuclid.org/journals/statistical-science/volume-25/issue-3/To-Explain-or-to-Predict/10.1214/10-STS330.full)
* Rocca R, & Yarkoni T (2022), Putting Psychology to the Test: Rethinking Model Evaluation Through Benchmarking and Prediction. _Advances in Methods and Practices in Psychological Science_, available [here](https://journals.sagepub.com/doi/full/10.1177/25152459211026864)
* Lipton, Z. C. (2018). The mythos of model interpretability: In machine learning, the concept of interpretability is both important and slippery. _Queue_. Available [here](https://dl.acm.org/doi/pdf/10.1145/3236386.3241340).
* Breiman L (2001), Statistical Modeling: The Two Cultures, _Statistical Science_, available [here](https://doi.org/10.1214/ss/1009213726)
* Hasson, U., Nastase, S. A., & Goldstein, A. (2020). Direct fit to nature: an evolutionary perspective on biological and artificial neural networks. _Neuron_. Available [here](https://www.cell.com/neuron/pdf/S0896-6273(19)31044-X.pdf)

## Padlet on Brightspace ##

We will use Brightspace for class-related communication. Please ask (and answer) questions in the Padlet, which you can find under `General Information`. There is no such thing as a stupid or trivial question! If a classmates asks a question you know an answer to, try and answer. The padlet is not only for instructor-student interaction, it is for all students to share knowledge and resources, and to get answers as fast as possible. 

## Asking questions (on the Padlet, in class, and elsewhere) ##

1. Google It First! Google the error Python gives you. English language errors will have more solutions online.
2. Search existing online resources (Google, StackOverflow, etc.) and class discussion on the Padlet for answers. If the question has already been answered, you're done!
3. If it has already been asked but you're not satisfied with the answer, refine your question to get the answer you need, and add to the thread.
    * Document the questions you ask and the responses.
    * Give your question context from course concepts not course assignments
        * Good context: "I have a question on parameters for RandomForest classifiers in scikit-learn"
        * Bad context: "I have a question on the notebook from the fourth lecture"
    * Be precise in your description:
        * Good description: "I am getting the following error and I'm not sure how to resolve it - ```ImportError: No module named sklearn```"
        * Bad description: "Python is giving me errors."

## Disability Resources ##

Your experience in this class is important to me. If you have already established accommodations with Special Educational Support (SES), please communicate your approved accommodations to me at your earliest convenience so we can discuss your needs in this course. If you have not yet established services through SES, but have a temporary health condition or permanent disability that requires accommodations (conditions include but not limited to; mental health, attention-related, learning, vision, hearing, physical or health impacts), you are welcome to contact 8716 2720 (Monday & Thursday 9-12, Tuesday 13-15) or email sps@au.dk. SES offers resources and coordinates reasonable accommodations for students with disabilities and/or temporary health conditions. Reasonable accommodations are established through an interactive process between you, your instructor(s) and SES. It is the policy and practice of the Aarhus University to create inclusive and accessible learning environment and ensure that all students have the opportunity to educate themselves on equal terms even if they have a disability.