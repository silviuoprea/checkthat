# CLEF2021--CheckThat-Lab
This repository contains the _dataset_, _format checker, scorer and baselines_ for the [CLEF2021-CheckThat! Lab](https://sites.google.com/view/clef2021-checkthat). 
The shared task focuses on detecting check-worthy claims, previously fact-checked claims, and fake news. 
The CLEF2021-CheckThat! Lab has three main tasks: 
  - [Task 1: Check-Worthiness Estimation]
  - [Task 2: Detecting Previously Fact-Checked Claims]
  - [Task 3: Fake News Detection]
  
This file contains the basic information regarding the CLEF2021-CheckThat! Lab. 

__Table of contents:__

- [Tasks Description](#tasks-description)
	- [Task 1: Check-Worthiness Estimation](#Task-1-Check-Worthiness-Estimation)
		- [Subtask 1A: Check-Worthiness of Tweets](#subtask-1a-check-worthiness-of-tweets)
		- [Subtask 1B: Check-Worthiness of Debates/Speeches](#-Subtask-1B-Check-Worthiness-of-DebatesSpeeches)
		- [Data, Data Format and Scripts for Task 1](#Data-Data-Format-and-Scripts-for-Task-1)
	- [Task 2: Detecting Previously Fact-Checked Claims](#Task-2-Detecting-Previously-Fact-Checked-Claims)
		- [Subtask 2A: Detect Previously Fact-Checked Claims in Tweets](#Subtask-2A-Detect-Previously-Fact-Checked-Claims-in-Tweets)
		- [Subtask 2B: Detect Previously Fact-Checked Claims in Political Debates/Speeches](#Subtask-2B-Detect-Previously-Fact-Checked-Claims-in-Political-DebatesSpeeches)
		- [Data, Data Format and Scripts for Task 2](#Data-Data-Format-and-Scripts-for-Task-2)
	- [Task 3: Fake News Detection](#Task-3-Fake-News-Detection)
		- [Subtask 3A: Multi-Class Fake News Detection of News Articles](#Subtask-3A-Multi-class-fake-news-detection-of-news-articles)
		- [Subtask 3B: Topical Domain Classification of News Articles](#Subtask-3B-Topical-Domain-Classification-of-News-Articles)
		- [Data, Data Format and Scripts for Task 3](#Data-Data-Format-and-Scripts-for-Task-3)
- [Licensing](#licensing)
- [Credits](#credits)
- [Citation](#citation)


# Tasks Description

CheckThat! Lab at CLEF 2021 is the fourth edition of the lab. 
The 2018 edition of CheckThat! Lab focused on the identification and verification of claims in political debates. 
The 2019 edition featured political debates and isolated claims, in conjunction with a closed set of Web documents to retrieve evidence from.
In 2020, the focus was on social media ---in particular on *Twitter*--- as information posted on this platform is not checked by an authoritative entity before publication and such information tends to disseminate very quickly. Moreover, social media posts lack context due to their short length and conversational nature; thus, identifying a claim's context is sometimes key for enabling effective fact-checking.

In the new 2021 edition of the CheckThat! Lab, we feature three tasks: 1. *check-worthiness estimation*,  2. *detecting previously fact-checked claims*, and 3. *predicting the veracity of news articles and their domain*.
In these tasks, we focus on (*i*) *tweets*, (_ii_) *political debates and speeches*, and (_iii_) *news articles*. Moreover, besides **English** and **Arabic**, we extend our language coverage to **Spanish** and **Bulgarian**.
We further add a new task on multi-class fake news detection for news articles and domain classification, which can help direct the article to the right fact-checking expert.


## Task 1: Check-Worthiness Estimation
Given a piece of text (e.g., a tweet or a sentence in a debate), detect whether it is worth fact-checking. In order to determine what is worth fact-checking, we either resort to the judgments of professional fact-checkers or we ask human annotators to answer several auxiliary questions, such as ``does it contain a verifiable factual claim?``, ``is it harmful?`` and ``is it of general interest?``, before deciding on the check-worthiness label.


### Subtask 1A: Check-Worthiness of Tweets 
Given a tweet, predict whether it is worth fact-checking. This is a classification task, focusing on COVID-19 (and some other topics), and it is offered in **Arabic**, **Bulgarian**, **English**, and **Spanish**. The participants are free to work on any language(s) of their interest, and they can also use multilingual approaches that make use of all datasets for training.


### Subtask 1B: Check-Worthiness of Debates/Speeches
Given a political debate/speech, produce a ranked list of its sentences, ordered by their check-worthiness. This is a ranking task, and it is only offered in **English**.


### Data, Data Format and Scripts for Task 1

You can find all the information on the data format and evaluation metrics in directory [Task 1](task1)

- [Evaluation Results](task1#evaluation-results)
- [List of Versions](task1#list-of-versions)
- [Contents of the Task 1 Directory](task1#contents-of-the-repository)
- [Input Data Format](task1#input-data-format)
	- [Subtask 1A: Check-Worthiness of Tweets](task1#subtask-1a-check-worthiness-of-tweets)
	- [Subtask 1B: Check-Worthiness of Debates/Speeches](task1#subtask-1b-check-worthiness-of-debatesspeeches)
- [Output Data Format](task1#output-data-format)
	- [Subtask 1A: Check-Worthiness of Tweets](task1#subtask-1a-check-worthiness-of-tweets-1)
	- [Subtask 1B: Check-Worthiness of Debates/Speeches](task1#subtask-1b-check-worthiness-of-debatesspeeches-1)
- [Format Checkers](task1#format-checkers)
	- [Subtask 1A: Check-Worthiness of Tweets](task1#subtask-1a-check-worthiness-of-tweets-2)
	- [Subtask 1B: Check-Worthiness of Debates/Speeches](task1#subtask-1b-check-worthiness-of-debatesspeeches-2)
- [Scorers](task1#scorers)
	- [Subtask 1A: Check-Worthiness of Tweets](task1#subtask-1a-check-worthiness-of-tweets-3)
	- [Subtask 1B: Check-Worthiness of Debates/Speeches](task1#subtask-1b-check-worthiness-of-debatesspeeches-3)
- [Evaluation Metrics](task1#evaluation-metrics)
- [Baselines](task1#baselines)
	- [Subtask 1A: Check-Worthiness of Tweets](task1#subtask-1a-check-worthiness-of-tweets-4)
	- [Subtask 1B: Check-Worthiness of Debates/Speeches](task1#subtask-1b-check-worthiness-of-debatesspeeches-4)
- [Credits](task1#credits)


## Task 2: Detecting Previously Fact-Checked Claims
Given a check-worthy claim in the form of a tweet, and a set of previously fact-checked claims, rank the previously fact-checked claims in order of usefulness to fact-check the input claim.

### Subtask 2A: Detect Previously Fact-Checked Claims in Tweets
Given a tweet, detect whether the claim the tweet makes was previously fact-checked with respect to a collection of fact-checked claims. The task is offered in **Arabic** and **English**. This is a ranking task, where the systems are asked to produce a list of top-n candidates.


### Subtask 2B: Detect Previously Fact-Checked Claims in Political Debates/Speeches
Given a claim in a political debate or a speech, detect whether the claim has been previously fact-checked with respect to a collection of previously fact-checked claims. This is a ranking task, and it is offered in **English** only.

### Data, Data Format and Scripts for Task 2

You can find all the information on the data format and evaluation metrics in directory [Task 2](task2)

__Table of contents:__
- [Evaluation Results](task2#evaluation-results)
- [List of Versions](task2#list-of-versions)
- [Contents of the Task 2 Directory](task2#Contents-of-the-Task-2-Directory)
- [Input Data Format](task2#input-data-format)
	- [Subtask 2A: Detect Previously Fact-Checked Claims in Tweets](task2#Subtask-2A-Detect-Previously-Fact-Checked-Claims-in-Tweets)
	- [Subtask 2B: Detect Previously Fact-Checked Claims in Political Debates/Speeches](task2#Subtask-2B-Detect-Previously-Fact-Checked-Claims-in-Political-DebatesSpeeches)
- [Output Data Format](task2#output-data-format)
	- [Subtask 2A: Detect Previously Fact-Checked Claims in Tweets](task2#Subtask-2A-Detect-Previously-Fact-Checked-Claims-in-Tweets-1)
	- [Subtask 2B: Detect Previously Fact-Checked Claims in Political Debates/Speeches](task2#Subtask-2B-Detect-Previously-Fact-Checked-Claims-in-Political-DebatesSpeeches-1)
- [Format Checkers](task2#format-checkers)
	- [Subtask 2A: Detect Previously Fact-Checked Claims in Tweets](task2#Subtask-2A-Detect-Previously-Fact-Checked-Claims-in-Tweets-2)
	- [Subtask 2B: Detect Previously Fact-Checked Claims in Political Debates/Speeches](task2#Subtask-2B-Detect-Previously-Fact-Checked-Claims-in-Political-DebatesSpeeches-2)
- [Scorers](task2#scorers)
	- [Subtask 2A: Detect Previously Fact-Checked Claims in Tweets](task2#Subtask-2A-Detect-Previously-Fact-Checked-Claims-in-Tweets-3)
	- [Subtask 2B: Detect Previously Fact-Checked Claims in Political Debates/Speeches](task2#Subtask-2B-Detect-Previously-Fact-Checked-Claims-in-Political-DebatesSpeeches-3)
- [Evaluation Metrics](task2#evaluation-metrics)
- [Baselines](task2#baselines)
	- [Subtask 2A: Detect Previously Fact-Checked Claims in Tweets](task2#Subtask-2A-Detect-Previously-Fact-Checked-Claims-in-Tweets-4)
	- [Subtask 2B: Detect Previously Fact-Checked Claims in Political Debates/Speeches](task2#Subtask-2B-Detect-Previously-Fact-Checked-Claims-in-Political-DebatesSpeeches-4)
- [Credits](task2#credits)


## Task 3: Fake News Detection
Given the text of a news article, determine whether the claims made in the article are true, partially true, false or other (e.g., claims in dispute or unchecked) and also detect the topical domain of the article.


### Subtask 3A: Multi-Class Fake News Detection of News Articles
This task is a four-class classification problem, offered in **English**. Given the text of a news article, determine whether the claims made in the article are *true*, *partially true*, *false*, or *other*.

### Subtask 3B: Topical Domain Classification of News Articles
Given the text of a news article, determine the topical domain of the article. This is a classification task to determine the topic of a news article, and it is offered in **English**.

### Data, Data Format and Scripts for Task 3

You can find all the information on the data format and evaluation metrics in directory [Task 3](task3)

- [Evaluation Results](task3#evaluation-results)
- [List of Versions](task3#list-of-versions)
- [Contents of the Task 3 Directory](task3#contents-of-the-repository)
- [Input Data Format](task3#input-data-format)
	- [Subtask 3A: Multi-Class Fake News Detection of News Articles](task3#Subtask-3A-Multi-Class-Fake-News-Detection-of-News-Articles)
	- [Subtask 3B: Topical Domain Classification of News Articles](task3#Subtask-3B-Topical-Domain-Classification-of-News-Articles)
- [Output Data Format](task3#output-data-format)
	- [Subtask 3A: Multi-Class Fake News Detection of News Articles](task3#Subtask-3A-Multi-Class-Fake-News-Detection-of-News-Articles-1)
	- [Subtask 3B: Topical Domain Classification of News Articles](task3#Subtask-3B-Topical-Domain-Classification-of-News-Articles-1)
- [Format Checkers](task3#format-checkers)
	- [Subtask 3A: Multi-Class Fake News Detection of News Articles](task3#Subtask-3A-Multi-Class-Fake-News-Detection-of-News-Articles-2)
	- [Subtask 3B: Topical Domain Classification of News Articles](task3#Subtask-3B-Topical-Domain-Classification-of-News-Articles-2)
- [Scorers](task3#scorers)
	- [Subtask 3A: Multi-Class Fake News Detection of News Articles](task3#Subtask-3A-Multi-Class-Fake-News-Detection-of-News-Articles-3)
	- [Subtask 3B: Topical Domain Classification of News Articles](task3#Subtask-3B-Topical-Domain-Classification-of-News-Articles-3)
- [Evaluation Metrics](task3#evaluation-metrics)
- [Baselines](task3#baselines)
	- [Subtask 3A: Multi-Class Fake News Detection of News Articles](task3#Subtask-3A-Multi-Class-Fake-News-Detection-of-News-Articles-4)
	- [Subtask 3B: Topical Domain Classification of News Articles](task3#Subtask-3B-Topical-Domain-Classification-of-News-Articles-4)
- [Credits](task3#credits)




# Licensing

These datasets are free for general research use.

# Credits

Lab Organizers:

Task website: https://sites.google.com/view/clef2021-checkthat

Contact:   clef-factcheck@googlegroups.com

# Citation

You can find the overview paper on the CLEF2021-CheckThat! Lab in the paper, "The CLEF-2021 CheckThat! Lab on Detecting Check-Worthy Claims, Previously Fact-Checked Claims, and Fake News" (see citation bellow) in this [link]().

```


```
