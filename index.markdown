---
layout: page
title: ADALunatics
subtitle: MeToo Movement Resurrection. 
cover-img: /assets/img/metooimg.png
use-site-title: true
---

<center> <h1>How Long Should We Wait for People to TALK?
</h1> </center>

Usually human rights’ movements get resurrected after a traumatic event e.g: Black Lives Matter was founded in 2013 and was revived in 2020 after Floyd’s death. However, there are other benign (Non-traumatic) events that could be a catalyst for movements such as movies e.g: Bombshell movie was released in 2019 opened a conversation about workplace sexual harassment (#MeToo) that occured in 2015.
<img src="assets/img/turanaburke.png" class="center"/>
------------

**Is there a gender bias in the people who talk about sexual harasment/metoo ?**

Can we successfully separate quotes group linked to sexual harasment from the rest ?

Explain how we select the keywords

Start with selecting words linked to metoo, by extracting words linked to metoo

<img src="assets/plots/Chapter_1/Wordcloud.png" class="center"/>

Find a nice way to show which keywords we will use

<img src="assets/plots/Chapter_1/Keywords.png" class="center"/>



Show the results after manual extraction linked to keywords

<img src="assets/plots/Chapter_1/Sentence_cloud_1_shorter_copy.png" class="center"/>





Show the results after first LDA

<img src="assets/plots/Chapter_1/Sentence_cloud_2.png" class="center"/>

Show the results after second LDA<img src="assets/plots/Chapter_1/Good_cloud_9.png" class="center"/>



**How can we incorporate the twitter dataset in this ?**





Study the time distribution of these quotes



<img src="assets/img/timeline.png" class="center"/>






Study the gender distribution for these quotes

{% include plots/gender_distribution_metadata.html %}







<img src="assets/img/gender_150K.png" class="center"/>





Can we identify other biases (study the distribution of the metadata for the speakers)





Sentiment analysis with BERT

Done for 200K and 400K

{% include plots/PCA_200K.html %}



---------

**Which events are responsible for the growth of the metoo movement ?**

- Over the years the #metoo movement has been marked by a few key traumatic events which lead to a sharp increase in its popularity. 
  - Show a timeline of these events 
  - Show tweet timeline
  - Measure the impact of these events and explain how we do so
- However, other non-traumatic events have also greatly influenced the metoo movement
  - Show a second timeline
  - Show same timeline for tweets
  - Measure the impact of these events too
- Compare the impact of both traumatic and non-traumatic events



-------



**Investigating cancel culture**
  
With more than 2.4 million posts under the “#MeToo” hashtag on Instagram in 2020, the movement has a very prominent position in the media (Instagram, 2020). Whilst the movements prevalence in media promotes a supporting and positive environment for individuals or victims who choose to come out with their sexual violence stories , this reflection discusses how the #MeToo movement has inadvertently encouraged toxicity on social media in the form of cancel culture. This toxic public discourse, cancel culture, is shown in prominent cases in media such as the example of Johnny Depp versus Amber Heard sexual and domestic violence allegations (ABC News, 2019). In which Johnny Depp was accused of sexual and domestic violence in 2016, resulting in him being “cancelled”. This included being dropped from his role in the Pirates of the Caribbean. We wanted to be investigate this phenomemon using the Quotebank dataset.
  
We took three examples of convicted people in the last five years present in the quotes or as speakers in the Quotebank dataset : 
  
**Al Franken** : American comedian, politician, media personality, who served as a United States Senator from Minnesota from 2009 to 2018, resigned on January 2, 2018, after several allegations of sexual misconduct were made against him.

| Al Franken | Quotes he pronounced | Quotes mentionning him |
|:------:|:------:|:------:|
| <img align="right" src="assets/img/Franken.jpeg" width="100" class="center"/> | <img src="assets/img/quotes_pronounced_Franken.png " width="300" class="center"/> | <img src="assets/img/quotes_mentioning_Franken.png " width="300" class="center"/> |


**Eric Schneiderman** : American lawyer and politician who served as the 65th Attorney General of New York from 2011 until his resignation in May 2018 after The New Yorker reported that four women had accused him of physical abuse.

| Eric Schneiderman | Quotes he pronounced | Quotes mentionning him |
|:------:|:------:|:------:|
| <img align="right" src="assets/img/Schneiderman.jpeg" width="100" class="center"/> | <img src="assets/img/quotes_pronounced_Schneiderman.png " width="300" class="center"/> | <img src="assets/img/quotes_mentioning_Schneiderman.png " width="300" class="center"/> |


**Andrew Kreisberg** : American television writer, producer and comic book writer. Kreisberg was suspended nn November 10, 2017 from his role as showrunner on The Flash, Arrow, Legends of Tomorrow, and Supergirl, after fifteen women and four men accused him of sexual harassment. On November 29, 2017, he was fired from all Warner Bros. Television's projects.

| Andrew Kreisberg | Quotes he pronounced | Quotes mentionning him |
|:------:|:------:|:------:|
| <img align="right" src="assets/img/Kreisberg.jpeg" width="100" class="center"/> | <img src="assets/img/quotes_pronounced_Kreisberg.png " width="300" class="center"/> | <img src="assets/img/quotes_mentioning_Kreisberg.png " width="300" class="center"/> |


We can observe on this three examples that the three of them seems have been cancelled by the media as the number of quotes pronounced by them and the number of quotes mentioning them drastically decreased right after their conviction. 

**Statistical analysis**


This observation has still to be confirmed by statistical analysis using a t-test assessing the difference of means of the number of quotes between the periods before and after their conviction. 

This has been done while studying a set of 65 accused people, mostly americans in which figures in addition to Al Franken, Andrew Kreisberg and Eric Schneiderman : Asia Argento, Luc Besson, Sylvester Stallone, Louis C.K., Kevin Spacey, Bob Weinstein, Oliver Stone, Roman Polanski, Matt Lauer, Glenn Thrush, Corey Lewandowski and others.

First, a t-test has been assessed between the normalized means of the count of quotes pronounced by them between the periods before and after their conviction, for each 65 accused people. This resulted with a significant p-value (p = 0.00046 <0.05). This puts in relief that this people are probably rejected by the society, giving them less time to express them, shutting them off the media, radios.

Secondly, another t-test has been assessed between the normalized means of the count of quotes mentioning them, again between the periods before and after their conviction, for these same 65 accused people. This resulted with a non-significant p-value (p = 0.672 > 0.05). This means that we couldn’t show that the society talks less about these people after their conviction. 


  

----------

**Conclusion**

Something very "generalized" for example impact of non-traumatic events can show that culture can also push these kind of movements and we don't have to wait for something bad to happen to expect growth. 
