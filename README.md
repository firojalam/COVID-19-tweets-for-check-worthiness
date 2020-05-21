# COVID-19 Infodemic Dataset: Modeling the Perspective of Journalists, Fact-Checkers, Social Media Platforms, Policy Makers, and the Society


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
<ol type="A">
<li>NO, not interesting</li>
<li>Not sure</li>
<li>YES, categorized as in question 6</li>
<li>YES, other</li>
<li>YES, blame authorities</li>
<li>YES, contains advice</li>
<li>YES, calls for action</li>
<li>YES, discusses action taken</li>
<li>YES, discusses cure</li>
<li>YES, asks question</li>
</ol>

## Download the dataset

To download the dataset, just fill up this [form](https://forms.gle/popezW4Lembnin637).


## Please cite the following paper if you are using the data or the annotation guidelines:

1. *Firoj Alam, Shaden Shaar, Alex Nikolov, Hamdy Mubarak, Giovanni Da San Martino, Ahmed Abdelali, Fahim Dalvi, Nadir Durrani, Hassan Sajjad, Kareem Darwish, Preslav Nakov, "Fighting the COVID-19 Infodemic: Modeling the Perspective of Journalists, Fact-Checkers, Social Media Platforms, Policy Makers, and the Society", arxiv, 2020 [download](https://arxiv.org/pdf/2005.00033.pdf).*

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
