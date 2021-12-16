---
layout: page
title: ADALunatics
subtitle: Deconstructing the metoo movement into impactful events. 
cover-img: /assets/img/metooimg.jpg
use-site-title: true
---

**Skeleton of the report**

Short introduction on harassments then zooming in on the metoo movement and then with one sentence explain what we'll be studying.

Introduce the data used again using an image

The goal of our research (this should be written at the end of our report (similar to an abstract in a paper))

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
- **Al Franken** : American comedian, politician, media personality,  who served as a United States Senator from Minnesota from 2009 to 2018, resigned on January 2, 2018, after several allegations of sexual misconduct were made against him;
- **Eric Schneiderman** : American lawyer and politician who served as the 65th Attorney General of New York from 2011 until his resignation in May 2018 after The New Yorker reported that four women had accused him of physical abuse.
- **Andrew Kreisberg** : American television writer, producer and comic book writer. Kreisberg was suspended nn November 10, 2017 from his role as showrunner on The Flash, Arrow, Legends of Tomorrow, and Supergirl, after fifteen women and four men accused him of sexual harassment. On November 29, 2017, he was fired from all Warner Bros. Television's projects.
  

- Show their quotes over time and do a case study explaining whether these people simply didn't find jobs or wether their jobs were silenced. (look at the wikipedia page)


| Quotes pronounced by Al Franken | Quotes mentionning  Al Franken |
|:------:|:------:|
|img {% include plots/timeline_quotes_fromAlFranken.html %} |img {% include plots/timeline_quotes_mentioningAlFranken.html %} |


{% include plots/timeline_quotes_fromEricSchneiderman.html %}

{% include plots/timeline_quotes_mentioningEricSchneiderman.html %}

{% include plots/timeline_quotes_fromAndrewKreisberg.html %}

{% include plots/timeline_quotes_mentioningAndrewKreisberg.html %}

  

- Add a horizontal line which shows the average number of quotes before got accused

  

----------

**Conclusion**

Something very "generalized" for example impact of non-traumatic events can show that culture can also push these kind of movements and we don't have to wait for something bad to happen to expect growth. 
