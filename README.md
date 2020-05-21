# COVID-19 Infodemic Twitter Dataset: Modeling the Perspective of Journalists, Fact-Checkers, Social Media Platforms, Policy Makers, and the Society


This repository contains a dataset consisting of tweets annotated with fine-grained labels related to disinformation about COVID-19. The labels answer seven different questions that are of interests to journalists, fact-checkers, social media platforms, policymakers, and society as a whole. There are annotations for Arabic and English.

To label the dataset, we prepared comprehensive annotation guidelines [1], which can help similar tasks in different domains. Moreover, we launched an annotation platform to label tweets, where anyone can contribute and help increase the size of the dataset, which we will be updating here periodically.

## Help the community to label more data

We also invite you to join us to label tweets related to COVID-19 disinformation.

<!--Please click the links below to label some tweets. -->

To annotate we recommend you to [register](https://micromappers.qcri.org/account/register) to [micromapper](https://micromappers.qcri.org/) and then [login](https://micromappers.qcri.org/account/signin) for the annotation. However, one can annotate with any registration.

1.	Please go to any of the the following links
  * [English](https://micromappers.qcri.org/project/covid19-tweet-labelling/)
  * [Arabic](https://micromappers.qcri.org/project/covid19-arabic-tweet-labelling/) <br/>
Then, either click ***Start Contributing Now*** or ***Contribute***. This will lead to a page with annotation instructions. Please, scroll down and click ***Start contributing***.
2.	 You can now start annotating.


An example of the annotation page looks as follows:
![Example](etc/screenshot_example.png?raw=true "Annotation example")


## Questions with the Associated Labels
Below is the list of the questions and the possible labels (answers).
See the paper below or the above micromappers links for detailed definition of the annotation guidelines.

**1. Does the tweet contain a verifiable factual claim?** <br/>
*Labels:*
* *YES:* if it contains a verifiable factual claim;
* *NO:* if it does not contain a verifiable factual
claim;
* *Don’t know or can’t judge:* the content of the tweet does not have enough information to make a judgment. It is recommended to categorize the tweet using this label when the content of the tweet is not understandable at all. For example, it uses a language (i.e., non-English) or references that are difficult to understand;

**2. To what extent does the tweet appear to contain false information?** <br/>
*Labels:*
1. NO, definitely contains no false information
2. NO, probably contains no false information
3. Not sure
4. YES, probably contains false information
5. YES, definitely contains false information

**3. Will the tweet’s claim have an effect on or be of interest to the general public?** <br/>
*Labels:*
1. NO, definitely not of interest
2. NO, probably not of interest
3. Not sure
4. YES, probably of interest
5. YES, definitely of interest

**4. To what extent does the tweet appear to be harmful to society, person(s), company(s) or product(s)?** <br/>
*Labels:*
1. NO, definitely not harmful
2. NO, probably not harmful
3. Not sure
4. YES, probably harmful
5. YES, definitely harmful


**5. Do you think that a professional fact-checker should verify the claim in the tweet?** <br/>
*Labels:*
1. NO, no need to check
2. NO, too trivial to check
3. YES, not urgent
4. YES, very urgent
5. Not sure


**6. Is the tweet harmful for society and why?** <br/>
*Labels:*
<ol type="A">
<li>NO, not harmful</li>
<li>NO, joke or sarcasm</li>
<li>Not sure</li>
<li>YES, panic</li>
<li>YES, xenophobic, racist, prejudices, or hate-speech</li>
<li>YES, bad cure</li>
<li>YES, rumor or conspiracy</li>
<li>YES, other</li>
</ol>

**7. Do you think that this tweet should get the attention of a government entity?**  <br/>
*Labels:*
Q1. NO, not interesting
Q2. Not sure
<ol type="A">
<li>YES, categorized as in question 6</li>
<li>YES, other</li>
<li>YES, blame authorities</li>
<li>YES, contains advice</li>
<li>YES, calls for action</li>
<li>YES, discusses action taken</li>
<li>YES, discusses cure</li>
<li>YES, asks question</li>
</ol>

LIST OF VERSIONS
================
v1.0 [2020/05/01]: initial distribution of the annotated dataset
* English data: 504 tweets
* Arabic data: 218 tweets



CONTENTS OF THE DISTRIBUTION AND DATA FORMAT
===========================
The directory contains the following two sub-directories:
* Readme.txt this file

1. "English": This directory contains tab-separated values (i.e., TSV) file, and one JSON file. The TSV file stores ground-truth annotations for the aforementioned tasks. The data format of these files is described in detail below. Each line in the JSON file corresponds to data from a single tweet stored in JSON format (as downloaded from Twitter).  

2. "Arabic": Similarly to English, this directory contains one TSV file and one JSON file using the same format. 

Format of the TSV files under the "annotations" directory
---------------------------------------------------------
Each TSV file in this directory contains the following columns, separated by a tab:

* tweet_id: corresponds to the actual tweet id from Twitter.
* tweet_text: corresponds to the original text of a given tweet as downloaded from Twitter.
* q*_label (column 3-9): corresponds to the label for question 1 to 7.


Note that there are NA (i.e., null) entries in the TSV files that simply indicate "not applicable" cases. We label NA for question 2 to 5 when question 1 is labeled as NO. 

Examples
=========

**Please don't take hydroxychloroquine (Plaquenil) plus Azithromycin for #COVID19 UNLESS your doctor prescribes it. Both drugs affect the QT interval of your heart and can lead to arrhythmias and sudden death, especially if you are taking other meds or have a heart condition.** <br/>
Labels:
<ol type="A">
	<li>Q1: Yes;</li>
	<li>Q2: NO: probably contains no false info</li>
	<li>Q3: YES: definitely of interest</li>
	<li>Q4: NO: probably not harmful</li>
	<li>Q5: YES:very-urgent</li>
	<li>Q6: NO:not-harmful</li>
	<li>	NO: YES:discusses_cure</li>
</ol>


**BREAKING: @MBuhari’s Chief Of Staff, Abba Kyari, Reportedly Sick, Suspected Of Contracting #Coronavirus | Sahara Reporters A top government source told SR on Monday that Kyari has been seriously “down” since returning from a trip abroad. READ MORE: https://t.co/Acy5NcbMzQ https://t.co/kStp4cmFlr.**  <br/>
*Labels:*
<ol type="A">
	<li>Q1: Yes; </li>
	<li>Q2: NO: probably contains no false info</li>
	<li>Q3: YES: definitely of interest</li>
	<li>Q4: NO: definitely not harmful</li>
	<li>Q5: YES:not-urgent</li>
	<li>Q6: YES:rumor</li>
	<li>NO: YES:classified_as_in_question_6</li>
</ol>


STATISTICS
=========
Some statistics about the dataset

** Class label distribution of English tweets:
Q1	504
no	209
yes	295
	
Q2	295
1_no_definitely_contains_no_false_info	47
2_no_probably_contains_no_false_info	171
3_not_sure	40
4_yes_probably_contains_false_info	25
5_yes_definitely_contains_false_info	12

	
Q3	295
1_no_definitely_not_of_interest	9
2_no_probably_not_of_interest	44
3_not_sure	7
4_yes_probably_of_interest	177
5_yes_definitely_of_interest	58

	
Q4	295
1_no_definitely_not_harmful	106
2_no_probably_not_harmful	66
3_not_sure	2
4_yes_probably_harmful	67
5_yes_definitely_harmful	54

	
Q5	295
no_no_need_to_check	77
no_too_trivial_to_check	57
yes_not_urgent	112
yes_very_urgent	49
	
Q6	504
no_joke_or_sarcasm	62
no_not_harmful	333
not_sure	2
yes_bad_cure	3
yes_other	25
yes_panic	23
yes_rumor_conspiracy	42
yes_xenophobic_racist_prejudices_or_hate_speech	14
		
Q6	504
no_not_interesting	319
not_sure	6
yes_asks_question	2
yes_blame_authorities	81
yes_calls_for_action	8
yes_classified_as_in_question_6	34
yes_contains_advice	9
yes_discusses_action_taken	12
yes_discusses_cure	5
yes_other	28


** Class label distribution of Arabic tweets:
Q1	218
no	78
yes	140
	
Q2	140
1_no_definitely_contains_no_false_info	31
2_no_probably_contains_no_false_info	62
3_not_sure	5
4_yes_probably_contains_false_info	40
5_yes_definitely_contains_false_info	2

	
Q3	140
1_no_definitely_not_of_interest	1
2_no_probably_not_of_interest	5
3_not_sure	9
4_yes_probably_of_interest	76
5_yes_definitely_of_interest	49

	
Q4	140
1_no_definitely_not_harmful	68
2_no_probably_not_harmful	21
3_not_sure	3
4_yes_probably_harmful	46
5_yes_definitely_harmful	2

	
Q5	140
no_no_need_to_check	22
no_too_trivial_to_check	55
yes_not_urgent	48
yes_very_urgent	15
	
Q6	218
no_joke_or_sarcasm	2
no_not_harmful	159
yes_bad_cure	1
yes_other	5
yes_panic	12
yes_rumor_conspiracy	33
yes_xenophobic_racist_prejudices_or_hate_speech	6
	
	
Q7	218
no_not_interesting	163
yes_blame_authorities	13
yes_calls_for_action	1
yes_classified_as_in_question_6	30
yes_contains_advice	1
yes_discusses_cure	6
yes_other	4


## Download the dataset

To download the dataset, just fill up this [form](https://forms.gle/popezW4Lembnin637).


## Please cite the following paper if you are using the data or the annotation guidelines:

1. *Firoj Alam, Shaden Shaar, Alex Nikolov, Hamdy Mubarak, Giovanni Da San Martino, Ahmed Abdelali, Fahim Dalvi, Nadir Durrani, Hassan Sajjad, Kareem Darwish, Preslav Nakov, "Fighting the COVID-19 Infodemic: Modeling the Perspective of Journalists, Fact-Checkers, Social Media Platforms, Policy Makers, and the Society", arxiv, 2020 [download](https://arxiv.org/abs/2005.00033).*

```bib
@misc{alam2020fighting,
    title={Fighting the {COVID-19} Infodemic: Modeling the Perspective of Journalists, Fact-Checkers, Social Media Platforms, Policy Makers, and the Society},
    author={Firoj Alam and Shaden Shaar and Alex Nikolov and Hamdy Mubarak and Giovanni Da San Martino and Ahmed Abdelali and Fahim Dalvi and Nadir Durrani and Hassan Sajjad and Kareem Darwish and Preslav Nakov},
    year={2020},
    eprint={2005.00033},
    archivePrefix={arXiv},
    primaryClass={cs.CL}
}
```
LICENSE
=======
This dataset is freely available for general research use.

## CREDITS
* Firoj Alam, Qatar Computing Research Institute, HBKU
* Shaden Shaar, Qatar Computing Research Institute, HBKU
* Alex Nikolov, Sofia University
* Hamdy Mubarak, Qatar Computing Research Institute, HBKU
* Giovanni Da San Martino, Qatar Computing Research Institute, HBKU
* Ahmed Abdelali, Qatar Computing Research Institute, HBKU
* Fahim Dalvi, Qatar Computing Research Institute, HBKU
* Nadir Durrani, Qatar Computing Research Institute, HBKU
* Hassan Sajjad, Qatar Computing Research Institute, HBKU
* Kareem Darwish, Qatar Computing Research Institute, HBKU
* Preslav Nakov, Qatar Computing Research Institute, HBKU


## CONTACT
Please contact tanbih@qcri.org

## Acknowledgment
Thanks to the QCRI's [Crisis Computing](https://crisiscomputing.qcri.org/) team for facilitating us with [Micromappers](https://micromappers.qcri.org/).
