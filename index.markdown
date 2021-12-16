---
layout: page
title: ADALunatics
subtitle: MeToo Movement Resurrection.
cover-img: /assets/img/metooimg.png
use-site-title: true
---

<center> <h1>How Long Should We Wait for People to TALK?</h1> </center>

Human rights’ movements tend to get resurrected after a traumatic event. One such example is the Black Lives Matter movement which was founded in 2013 and was revived in 2020 after George Floyd’s death. However, other benign (non-traumatic) events can also be a catalyst for these movements, for instance the movie Bombshell was released in 2019 and reopened a conversation about workplace sexual harassment (#MeToo) that was first made famous in 2017.
<img src="assets/img/turanaburke.jpg" class="center"/>
---

<center> <h1>How to Tackle this Problem?</h1> </center>
<img src="assets/img/quotebank.png" alt="foursquare_logo" width="210" style="float:right"/>
We have used the Quotebank dataset from 2015 to 2020 to investigate the impact of traumatic/non-traumatic events on public opinion. Also, we have fetched tweets related to #MeToo to augment our data.

<img src="assets/img/Leo-Twitter-1.gif" class="center"/>

**GOAL :**

Here are some interesting questions which we’ll dive into:

1. Can we extract quotes related to MeToo movement or Sexual Harassment in the workplace from Quotebank 2015-2020?
2. Is there a gender bias in the speakers of quotes related to sexual harassment ?
3. What is the impact of the traumatic vs non-traumatic events on the MeToo movement, based on quotes and tweets involved in #MeToo?
4. Can we observe a cancel culture as a ramification of #MeToo movement?

<center> <h1>Can we extract quotes related to MeToo movement or Sexual Harassment in the workplace from Quotebank 2015-2020?</h1> </center>

We investigated the quotes in Quotebank throughout the years from 2015 to 2020 and we found a total of **115,584,251** quotes.
<img src="assets/plots/Chapter_1/quotes_years.png" class="center"/>

From the extracted quotes, we got the most frequent words co-occurring with MeToo, shown in the word cloud below. We validated our results with a word cloud from a MeToo search on [Media Cloud](https://mediacloud.org/), a news gathering website, to confirm that our sample is representative of the movement.

| Our Quotes 😎| Media Cloud 📹|
|:------:|:------:|
|<img src="assets/plots/Chapter_1/Wordcloud.png" width="350" class="left"/> | <img src="assets/plots/Chapter_1/media_cloud.jpeg" width="350" height="350" class="left"/>|

<img src="assets/plots/Chapter_1/Keywords.png" width="800" height="500" class="center"/>

The topics detected by the LDA were very insightful of the content in the quotes extracted sofar.

We could interpret them as  
1. **Women Empowerment** 👩 
2. **Sexual Harassment** ❌
3. **Politics** 📰
4. **Christmassy** 🎄
<img src="assets/plots/Chapter_1/ldatopics.png" class="center"/>

Applying PCA on the second LDA layer.

{% include plots/PCA_600K_good_size.html %}

Showing how the second LDA classified the quotes

{% include plots/PCA_600K_good_size_no_colour.html %}

**Is there a gender bias in the people who talk about sexual harassment/metoo ?**

Can we successfully separate quotes group linked to sexual harassment from the rest ?


Find a nice way to show which keywords we will use



Show the results after manual extraction linked to keywords

<img src="assets/plots/Chapter_1/Sentence_cloud_1_shorter_copy.png" class="center"/>


**How can we incorporate the twitter dataset in this ?**





Study the time distribution of these quotes



<img src="assets/img/timeline.png" class="center"/>





 <center> <h1>Is there a gender bias in the speakers of quotes related to sexual harassment ? </h1> </center>



Study the gender distribution for these quotes





<img src="assets/img/Gender_6M.png" class="center"/>




<img src="assets/img/Gender_200K.png" class="center"/>





Can we identify other biases (study the distribution of the metadata for the speakers)

Sentiment analysis with BERT

Done for 200K and 400K

{% include plots/PCA_600K_good_size.html %}



{% include plots/PCA_600K_good_size_no_colour.html %}



---------
<center> <h1>Which events are responsible for the growth of the metoo movement ?</h1> </center>

<img src="assets/img/accused_people.gif" class="center"/>

Over the years the #metoo movement has been marked by a few key traumatic events which lead to a sharp increase in its popularity. We were interested in the impact of some events on the metoo movement. In other words, whether trends in the #metoo timeline were temporally linked to some events. 
Thus, we gathered a dataset of traumatic events, itemising events related to the core issue of sexual harassment: the allegations by victims. The main source is a Vox article listing more than 250 public figures which were accused of sexual harassment between 2017 and 2019.

<img src="assets/img/untouchable.jpg" alt="foursquare_logo" width="150" style="float:right"/>
In parallel, we manually fabricated a dataset of non-traumatic events found by original research. We chose events which are not related to the core issue of sexual harassment and consequences, such as movie releases, publications, demonstrations, and others related to MeToo in the same time period as above. 
We assume the number of quotes related to MeToo each day to be a proxy of the attention to the topic. We plan to measure the impact of each event as the before-after difference in public attention, and use this measure to investigate and compare traumatic vs non traumatic events.

**What is the impact of traumatic events ?**
<img src="assets/plots/Traumatic_events_timeline.png" class="center"/>
This plot displays the timeline of extracted quotes involved with the #metoo movement and shows the allegations/accusations. We can already observe a huge wave of accusations since mid-2017 to early 2018. 
Talk about the 2week smoothing to reduce noise and the weekly trend

**What is the impact of non-traumatic events ?**
<img src="assets/plots/Non_Traumatic_events_timeline.png" class="center"/>
This plot displays the timeline of #metoo quotes and the top 15 most impactful traumatic events (dear reader, you can check who was convicted at which moment directly on the timeline!)
It is clear that our impact measure detected two main waves in the public attention. The first which rises above the baseline is in October 2017, which is the moment in which the hashtag went viral for the first time  
After a dip during Christmas due to the reduction of people releasing quotes, we can witness another large wave in January 2018. 

**Are we able to compare impacts from traumatic VS non-traumatic events ?**

<img src="assets/img/increase_impact.jpeg" alt="foursquare_logo" width="150" style="float:right"/>
Quantify the impact of a certain event was calculated based on the difference of number of #metoo quotes before and after the event date, on a window of 7 days. 

<center> <h1> to do</h1> </center>
Show tweet timeline
Measure the impact of these events and explain how we do so
{% include plots/cropped_1_titles.html %}
However, other non-traumatic events have also greatly influenced the metoo movement
Show a second timeline
Show same timeline for tweets
Measure the impact of these events too
{% include plots/cropped_2_titles.html %}
Compare the impact of both traumatic and non-traumatic events

Timeline and table 
Compare traumatic || non-traumatic events




-------



<center> <h1>Can we observe a cancel culture as a ramification of #MeToo movement?</h1> </center>

With more than 2.4 million posts under the “#MeToo” hashtag on Instagram in 2020, the movement has a very prominent position in the media (Instagram, 2020). Whilst the movements prevalence in media promotes a supporting and positive environment for individuals or victims who choose to come out with their sexual violence stories , this reflection discusses how the #MeToo movement has inadvertently encouraged toxicity on social media in the form of cancel culture. This toxic public discourse, cancel culture, is shown in prominent cases in media such as the example of Johnny Depp versus Amber Heard sexual and domestic violence allegations (ABC News, 2019). In which Johnny Depp was accused of sexual and domestic violence in 2016, resulting in him being “cancelled”. This included being dropped from his role in the Pirates of the Caribbean. We wanted to be investigate this phenomenon using the Quotebank dataset.

We took three examples of convicted people in the last five years present in the quotes or as speakers in the Quotebank dataset :

**Al Franken** : American comedian, politician, media personality, who served as a United States Senator from Minnesota from 2009 to 2018, resigned on January 2, 2018, after several allegations of sexual misconduct were made against him.

| Al Franken | Quotes he pronounced | Quotes mentioning him |
|:------:|:------:|:------:|
| <img align="right" src="assets/img/Franken.jpeg" width="100" class="center"/> | <img src="assets/img/quotes_pronounced_Franken.png " width="300" class="center"/> | <img src="assets/img/quotes_mentioning_Franken.png " width="300" class="center"/> |


**Eric Schneiderman** : American lawyer and politician who served as the 65th Attorney General of New York from 2011 until his resignation in May 2018 after The New Yorker reported that four women had accused him of physical abuse.

| Eric Schneiderman | Quotes he pronounced | Quotes mentioning him |
|:------:|:------:|:------:|
| <img align="right" src="assets/img/Schneiderman.jpeg" width="100" class="center"/> | <img src="assets/img/quotes_pronounced_Schneiderman.png " width="300" class="center"/> | <img src="assets/img/quotes_mentioning_Schneiderman.png " width="300" class="center"/> |


**Andrew Kreisberg** : American television writer, producer and comic book writer. Kreisberg was suspended nn November 10, 2017 from his role as showrunner on The Flash, Arrow, Legends of Tomorrow, and Supergirl, after fifteen women and four men accused him of sexual harassment. On November 29, 2017, he was fired from all Warner Bros. Television's projects.

| Andrew Kreisberg | Quotes he pronounced | Quotes mentioning him |
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
