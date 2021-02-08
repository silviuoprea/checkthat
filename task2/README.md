# Task 3: Fake News Detection

This repository contains the _dataset_, _format checker, scorer and baselines_ for the [CLEF2021-CheckThat! Task 2](https://sites.google.com/view/clef2021-checkthat/tasks/task-2-claim-retrieval). 
Given a check-worthy claim in the form of a tweet, and a set of previously fact-checked claims, rank the previously fact-checked claims in order of usefulness to fact-check the input claim.


````
TBA
````

This file contains the basic information regarding the CLEF2021-CheckThat! Task 2
on check-worthiness on tweets provided for the CLEF2021-CheckThat! Lab
on "Automatic Detecting Check-Worthy Claims, Previously Fact-Checked Claims, and Fake News".
The current version are listed bellow corresponds to the release of the training and dev data sets.

__Table of contents:__
- [Evaluation Results](#evaluation-results)
- [List of Versions](#list-of-versions)
- [Contents of the Task 2 Directory](#Contents-of-the-Task-2-Directory)
- [Input Data Format](#input-data-format)
	- [Subtask 2A: Detect Previously Fact-Checked Claims in Tweets](#Subtask-2A-Detect-Previously-Fact-Checked-Claims-in-Tweets)
	- [Subtask 2B: Detect Previously Fact-Checked Claims in Political Debates/Speeches](#Subtask-2B-Detect-Previously-Fact-Checked-Claims-in-Political-DebatesSpeeches)
- [Output Data Format](#output-data-format)
	- [Subtask 2A: Detect Previously Fact-Checked Claims in Tweets](#Subtask-2A-Detect-Previously-Fact-Checked-Claims-in-Tweets-1)
	- [Subtask 2B: Detect Previously Fact-Checked Claims in Political Debates/Speeches](#Subtask-2B-Detect-Previously-Fact-Checked-Claims-in-Political-DebatesSpeeches-1)
- [Format Checkers](#format-checkers)
	- [Subtask 2A: Detect Previously Fact-Checked Claims in Tweets](#Subtask-2A-Detect-Previously-Fact-Checked-Claims-in-Tweets-2)
	- [Subtask 2B: Detect Previously Fact-Checked Claims in Political Debates/Speeches](#Subtask-2B-Detect-Previously-Fact-Checked-Claims-in-Political-DebatesSpeeches-2)
- [Scorers](#scorers)
	- [Subtask 2A: Detect Previously Fact-Checked Claims in Tweets](#Subtask-2A-Detect-Previously-Fact-Checked-Claims-in-Tweets-3)
	- [Subtask 2B: Detect Previously Fact-Checked Claims in Political Debates/Speeches](#Subtask-2B-Detect-Previously-Fact-Checked-Claims-in-Political-DebatesSpeeches-3)
- [Evaluation Metrics](#evaluation-metrics)
- [Baselines](#baselines)
	- [Subtask 2A: Detect Previously Fact-Checked Claims in Tweets](#Subtask-2A-Detect-Previously-Fact-Checked-Claims-in-Tweets-4)
	- [Subtask 2B: Detect Previously Fact-Checked Claims in Political Debates/Speeches](#Subtask-2B-Detect-Previously-Fact-Checked-Claims-in-Political-DebatesSpeeches-4)
- [Credits](#credits)

## Evaluation Results

TBA

## List of Versions


## Contents of the Task 2 Directory
We provide the following files:

* Main folder: [data](./data)
  * Subfolder: [subtask-2A--english](./data/subtask-2a--english)
  * Subfolder: [subtask-2A--arabic](./data/subtask-2a--arabic)
  * Subfolder: [subtask-2B--english](./data/subtask-2b--english)
* Main folder: [baselines](./baselines)<br/>
	Contains scripts provided for baseline models of the tasks
* Main folder: [formet_checker](./format_checker)<br/>
	Contains scripts provided to check format of the submission file
* Main folder: [scorer](./scorer)<br/>
	Contains scripts provided to score output of the model when provided with label (i.e., dev set).

* [README.md](./README.md) <br/>
	This file!



## Input Data Format

The format used in the task is inspired from [Text REtrieval Conference (TREC)](https://trec.nist.gov/)'s campaigns for information retrieval (a description of the TREC format can be found [here](https://github.com/joaopalotti/trectools#file-formats)).

Both subtasks share the same file formats with minor differences. There are ## file types:
- [Verified Claims (**Subtask-2A** and **Subtask-2B**)](#Verified-Claims-Subtask-2A-and-Subtask-2B)
- [Queries File (**Subtask-2A** and **Subtask-2B**)](#Queries-File-Subtask-2A-and-Subtask-2B)
- [Qrels File (**Subtask-2A** and **Subtask-2B**)](#Qrels-File-Subtask-2A-and-Subtask-2B)
- [Tweet Objects (**Subtask-2A** Only)](#Tweet-Objects-Subtask-2A-only)
- [Deabte/Speeches Transcripts (**Subtask-2B** Only)](#DeabteSpeeches-Transcripts-Subtask-2B-only)

### Verified Claims (Subtask-2A and Subtask-2B)

All the verified claims that will be used for both training and test are found in file (data/subtask-2a--english/v1/verified_claims.qrels.json), (data/subtask-2a--arabic/v1/verified_claims.qrels.json) and (data/subtask-2b--english/v1/verified_claims.qrels.json).

The file has the following format:

> vclaim_id <TAB> vclaim <TAB> title

where <br>

* vclaim_id: unique ID of the verified claim <br/>
* vclaim: text of the verified claim <br/>
* title: title of the document fact checking the verified claim <br/>

Example:

| vclaim_id | vclaim | title |
| --- | --- | --- |
| 2 | "A ""law to separate families"" was enacted prior to April 2018, and the federal government is powerless not to enforce it." | Was the ‘Law to Separate Families’ Passed in 1997 or ‘by Democrats’? |
| 222 | Former U.S. Vice President Joe Biden owns the largest mansion in his state. | Does Joe Biden Own the Largest Mansion in His State? |
| 503 | "U.S. Sen. Bernie Sanders compared Baltimore to a ""third world country."""  | Did U.S. Sen. Bernie Sanders Say Baltimore Was Like a ‘Third World Country’? |
| ... |

__Note__: Not all verified claims in the file have a corresponding tweet.


### Queries File (Subtask-2A and Subtask-2B)

### Qrels File (Subtask-2A and Subtask-2B)

### Tweet Objects (Subtask-2A Only)

### Deabte/Speeches Transcripts (Subtask-2B Only)


## Output Data Format

### Subtask 2A: Detect Previously Fact-Checked Claims in Tweets

TBA

### Subtask 2B: Detect Previously Fact-Checked Claims in Political Debates/Speeches

TBA


## Format Checkers

#### Subtask 2A: Detect Previously Fact-Checked Claims in Tweets

TBA

#### Subtask 2B: Detect Previously Fact-Checked Claims in Political Debates/Speeches

TBA

## Scorers

### Subtask 2A: Detect Previously Fact-Checked Claims in Tweets

TBA

### Subtask 2B: Detect Previously Fact-Checked Claims in Political Debates/Speeches

TBA

## Evaluation Metrics
This task is evaluated as a classification task. We will use accuracy, and F1 measure.


## Baselines

### Subtask 2A: Detect Previously Fact-Checked Claims in Tweets

TBA

### Subtask 2B: Detect Previously Fact-Checked Claims in Political Debates/Speeches

TBA


## Credits

Task 3 Organizers: TBA

Task website: https://sites.google.com/view/clef2021-checkthat/tasks/task-3-fake-news-detection

Contact:   clef-factcheck@googlegroups.com
