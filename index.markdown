---
layout: page
title: Movement Resurrection
subtitle: What impacts a Human Rights Movement?
cover-img: /assets/img/cover.gif
use-site-title: true
---

<center> <h1>How Many People Should Suffer Before We TALK about it?</h1> </center>

Human Rights’ movements tend to experience surges in pupularity after emotionally intense, or traumatic, events. One such example is Black Lives Matter, which was founded in 2013 and was revived in 2020 after George Floyd’s death. Other benign (non-traumatic) events can also be catalysts for these movements: another example is the movie Bombshell, which was released in 2019 and reopened the conversation about workplace sexual harassment (#MeToo) that was first made famous in 2017.
<img src="assets/img/turanaburke.jpg" class="center"/>
---

This data story focuses on the MeToo movement and in general about the topic of sexual harassment. We probe the media discourse and public opinion to gain insights about events and biases that characterize this discussion.

<center> <h1>How to Tackle this Problem?</h1> </center>
<img src="assets/img/quotebank.png" alt="foursquare_logo" width="200" style="float:right"/> 
In order to explore the public perception of the MeToo movement and investigate the impact of traumatic/non-traumatic events we explore quotes in the Quotebank dataset from 2015 to 2020. 

<img src="assets/img/Leo-Twitter-1.gif" width="200" style="float:left"/>
In order to augment our data, we have fetched tweets related to #MeToo from the public twitter API and integrated them with previously extracted tweets on MeToo.

---
**GOAL :**

Here are some interesting questions which we’ll dive into:
1. Can we extract quotes related to MeToo movement or Sexual Harassment in the workplace from Quotebank 2015-2020?
2. Is there a gender bias in the speakers of quotes related to sexual harassment ?
3. What is the impact of the traumatic vs non-traumatic events on the MeToo movement, based on quotes and tweets involved in #MeToo?
4. Can we observe cancel culture as a ramification of the #MeToo movement?


-----------------


<center> <h1>Can we extract quotes related to MeToo movement or Sexual Harassment in the workplace from Quotebank 2015-2020?</h1> </center>

We investigated the quotes in Quotebank throughout the years from 2015 to 2020 and we found a total of **115,584,251** quotes.
<img src="assets/plots/Chapter_1/quotes_years.png" class="center"/>

From these quotes, we extracted the words most most frequently co-occurring with MeToo, shown in the word cloud below. We validated our results with a word cloud from a MeToo search on [Media Cloud](https://mediacloud.org/), a news gathering website, to confirm that our sample is representative of the movement.

| Our Quotes 😎| Media Cloud 📹|
|:------:|:------:|
|<img src="assets/plots/Chapter_1/Wordcloud.png" width="350" class="left"/> | <img src="assets/plots/Chapter_1/media_cloud.jpeg" width="350" height="350" class="left"/>|

<img src="assets/plots/Chapter_1/Keywords.png" width="800" height="500" class="center"/>

We then extracted all the quotes from quotebank which contained any of these keywords.
These are samples of the initially extracted quotes.
<img src="assets/plots/Chapter_1/Sentence_cloud_1_shorter_copy.png" class="center"/>

Some of them do not look quite right, as we included some general keywords in our selection. We set out to refine our sample: using Latent Dirichlet Allocation (LDA) we assigned a topic to each of the previously extracted quotes. 
The topics detected by the LDA were very insightful of the content of the quotes extracted so far.

<img src="assets/plots/Chapter_1/ldatopics.png" width="600" class="center"/>

We could interpret this topics as:
1. **Women Empowerment** 👩 
2. **Sexual Harassment** ❌
3. **Politics** 📰
4. **Christmassy** 🎄

The second topic seems to be more like our target. It was further investigated by adding another LDA layer to filter it more. Then, we applied a PCA to explore the clustering of the latest topics generated.
The plot below shows a subsample of the first 2 PCA dimensions of the extracted quotes before filtering them based on topic a second time.
(You can read the quote itself by hovering the datapoint on the plot!)

{% include plots/PCA_600K_good_size_no_colour.html %}

By labeling the quotes with the latest topics of the final LDA we could see the clusters of different topics that are overlapping.

The clusters could be interpreted as
1. **US Politics** 🔥
2. **Sports** ⚽
3. **Sexual Harassment** ❌
4. **Global Politics** 📰

{% include plots/PCA_600K_good_size.html %}

By taking a closer look we notice that the quotes linked to the third topic, in green, do indeed refer to sexual harassment. 
Now that we have succesfully isolated these quotes we can start our analysis!

(As a sidenote: notice how the outermost post at the top refers to a quote by Bill Clinton: "I did not have sexual relations with that page", was correctly labeled as a quote on politics and not sexual harasment even though the LDA algorithm did not have access to any information related to the speaker!)

The timeline of the counts of these quotes can be firstly observed on a monthly resolution to get an idea of the trends. It is evident that apart from a few early dips due to missing data the baseline increased significantly at the end of 2017, when the MeToo movement first became well known, sparking an increased conversation about sexual harassment. We can already see some sharp increases over the overall trend, which will be investigated further while examining events' impacts.

<img src="assets/img/timeline_cropped.png" class="center"/>

-----------------

<center> <h1>Is there a gender bias in the speakers of quotes related to sexual harassment?</h1> </center>
 
Given the inherently gendered nature of sexual harassment, we were interested in the gender ratio of the quoted people in Quotebank 2015-2020 and in the dataset of #MeToo quotes. We hypothesised, due to the gender gap in leadership positions in many public fields, that there would be more quotes from males than females (and others) in Quotebank, and we wondered whether this feature would remain in the #MeToo quotes dataset we isolated. 

| Distribution in Quotebank [6M quotes] | Distribution in #MeToo [200k quotes] |
|:------:|:------:|
| <img src="assets/img/Gender_6M.png" width="300" > | <img src="assets/img/Gender_200K_white.png" width="300" > |

We can observe that there is indeed a gender bias in the Quotebank dataset. It is also clear that this ratio is reversed when dealing with the filtered data, which highlights how women have been the driving force behind the #MeToo rise. 
This fact even lead to the creation of a countermovement, #HimToo, a hashtag first focused on harassment on men but then redirected towards the apparent ease with which men could suffer negative consequences after being falsely accused (Boyle, Rathnayake, 2019). The time required for the legal process to actually settle the truth of accusations is most of the times too long and the career of the accused men, even if acquitted, can suffer. The Quotebank dataset gave us the means to find out how people were silenced, or cancelled, after an accusation.

Boyle, K. and Rathnayake, C., 2019. #HimToo and the networking of misogyny in the age of #MeToo. Feminist Media Studies, 20(8), pp.1259-1277.


-----------------

<center> <h1>Which events are responsible for the growth of the MeToo movement ?</h1> </center>

|<img src="assets/img/accused_people.gif" class="center"/>|
|:--:| 
| *Names of Celebrities, Politicians and CEOs accused of Sexual Misconduct* |

<img src="assets/img/webscraping.gif" alt="foursquare_logo" width="150" style="float:left"/>
Over the years the #MeToo movement has been marked by a few key traumatic events which lead to a sharp increase in its popularity. We were interested in the impact of some events on the MeToo movement. In other words, whether trends in the #MeToo timeline were temporally linked to some events. 
Thus, we gathered a dataset of traumatic events, itemising events related to the core issue of sexual harassment: the allegations by victims. The main source is a [Vox article](https://www.vox.com/a/sexual-harassment-assault-allegations-list/asia-argento) listing more than 250 public figures which were accused of sexual harassment between 2017 and 2019. Accordingly, we scraped this website to compile the needed data.

<img src="assets/img/untouchable.jpg" alt="foursquare_logo" width="100" style="float:right"/>
In parallel, we manually assembled a dataset of non-traumatic events found by original research. We chose events which are not related to the core issue of sexual harassment and consequences, such as movie releases, publications, demonstrations, and others related to MeToo in the same time period as above. 
We assume the number of quotes related to MeToo each day to be a proxy of the attention to the topic. 


<img src="assets/img/increase_impact.jpeg" alt="foursquare_logo" width="100" style="float:right"/>
**Quantify the impact** : We plan to measure the impact of each event as the before-after difference in public attention, and use this measure to investigate and compare traumatic vs non traumatic events. This in practice is done by taking the average of the number of quotes 2 weeks before and after the date of the event, in order to identify the trend to which the event belongs.


**What is the impact of traumatic events ?**

<img src="assets/plots/Traumatic_events_timeline.png" class="center"/>
This plot displays the timeline of extracted quotes involved with the #MeToo movement and the timing of the allegations/accusations. We can already observe two huge waves of accusations in the middle of 2017 and early 2018.

Now that we have our traumatic events we can measure their impact on the number of quotes related to sexual harassment.

| Distribution of traumatic events impacts | Top 10 most impactful events 💥|
|:------:|:------:|
|<img src="assets/img/Impact_traumatic.png" width = "400px" class="center"/>| <img src="assets/img/top10.png" width = "400" >|

When studying the 10 most impactful events we notice that these belong to the 2 main waves of accusations, indicating that these waves of accusations are indeed related to an incease in quotes related to sexual harassment. (Dear reader, you can check who was convicted at which moment directly on the timeline!) 

Upon further investigation we notice that the first wave in October 2017 corresponds to the moment in which the #MeToo went viral for the first time. 
Interstingly the second wave is not only linked to events directly linked to MeToo but happened at the same time as the birth of many other social movements inspired by MeToo: #SilenceIsNotSpiritual, MeTooK12 and the discussion of the ME TOO bill in U.S. Congress. 

{% include plots/cropped_traumatic_final.html %}


**What is the impact of non-traumatic events ?**

Now lets take a look at the non-traumatic events!
<img src="assets/plots/Non_Traumatic_events_timeline.png" class="center"/>

This plot displays the timeline of #MeToo quotes and the top 10 most impactful non-traumatic events. 

It is clear that our impact measure detected two main waves in the public attention. The first which rises above the baseline is in October 2017, which is the moment in which the hashtag went viral for the first time  
After a dip during Christmas due to the reduction of people releasing quotes, we can witness another large wave in January 2018. 

| Distribution of non-traumatic events impacts | Top10 most impactful events |
|:------:|:------:|
|<img src="assets/img/Impact_non_traumatic.png" width = "400" > | <img src="assets/img/nontraumatic.png" width = "400" >|


**Are we able to compare impacts from traumatic VS non-traumatic events ?**

The impact measure we obtained is higher for the traumatic events that happened to be before the aforementioned waves. It appears then that the movement was fueled by clusters of accusations. These probably also influenced one another by providing the motivation to come forward to the victims. 
Non traumatic events are more scattered and therefore had less impact on the timeline we analysed.

{% include plots/cropped_non_traumatic_final.html %}

**How does the tweet dataset confirm our results?**

The tweets dataset related to MeToo were processed in a similar way to obtain a timeline. Unfortunately the time covered ranges only from October 2018 to February 2019. We therefore restricted our analysis to the events around this time period.

<img src="assets/img/tweet_timeline_milo.png" width = "600" class="center"/>

None of the events analysed seem to directly impact the subsequent wave: by closely examining them one stands out. It is widely believed (Darwish, 2019) that the revival of #MeToo in september and october 2018 was due to the accusations levelled towards Brett Kavanagh, made public on Sep. 16, which sparked an FBI investigation after widely covered hearings with the judiciary committee. On October 6th Kavanagh would go on to be confirmed by the senate in a polarized debate. The entire story lasted for weeks, becoming the main topic in the news and the subsequent online conversation on #MeToo would then peak and slowly return to baseline levels.

*Darwish, K. (2019). Quantifying Polarization on Twitter: The Kavanaugh Nomination. ArXiv, abs/2001.02125.*

-----------------

<center> <h1>Can we observe cancel culture as a ramification of the #MeToo movement?</h1> </center>

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

This observation has still to be confirmed by statistical analysis using a t-test assessing the difference of means of the number of quotes between the periods before and after their conviction. This has been done while studying a set of 65 accused people, mostly americans.

First, a t-test has been assessed between the normalized means of the count of quotes pronounced by them between the periods before and after their conviction, for each 65 accused people. **This resulted with a significant p-value (p = 0.00046 <0.05). This puts in relief that this people are probably rejected by the society, giving them less time to express them, shutting them off the media, radios.** Secondly, another t-test has been assessed between the normalized means of the count of quotes mentioning them, again between the periods before and after their conviction, for these same 65 accused people. This resulted with a non-significant p-value (p = 0.672 > 0.05). This means that we couldn’t show that the society talks less about these people after their conviction.

-----------------


<center> <h1>Conclusion </h1> </center>

<img src="assets/img/metooimg.png" alt="foursquare_logo" width="210" style="float:right"/>
Based on the analysis performed, we strongly believe that non-traumatic events have observable impact on reviving the MeToo movement, which proves that we don’t need to wait for people to suffer or struggle in order to educate others and raise awareness. Media has an important role in impacting and shifting optics since it is related to most non-traumatic events. This analysis is a minor version of a potential extended and detailed project that could scrape all newspapers’ websites, social media interactions,...etc to get a much deeper understanding of the main factors affecting any human rights movement. Nonetheless, the Quotebank dataset is a powerful proxy of public discussion and is uniquely suited to analyse for example how much people are able to reach the wider public or not, as we did with cancel culture.

<img src="assets/img/ezgif.com-gif-maker (1).gif" class="center"/>

