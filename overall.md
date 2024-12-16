---
layout: page
title: Exploring gender differences in cinema
subtitle: by ADAvengers2023
cover-img: /assets/img/eatpraylove.jpg
thumbnail-img: /assets/img/thumb.png
share-img: /assets/img/eatpraylove.jpg
tags: [books, test]
author: İrem Şekeroğlu, Ariane Augustoni, Caroline Vonmering, Heling Shi, Shu Yang
---

<div style="text-align: justify;">
Our project aims to critically examine the portrayal of female characters in cinema. Driven by the movies‘ profound cognitive influence, our objective is to see how women are represented in movies. First, we will look at how many women and men are present in the movies and if this varies by genre. We will also take a look at which character types men and women play most often. Next, we will dive deeper into the summaries of the movies and use natural language processing to answer questions such as: Are men and women described with different adjectives? What sentiments are associated with these adjectives? And, also related to the summary data: which jobs do men and women usually have in movies? With this analysis, we want to identify any existing biases or subtle forms of discrimination. We will also explore how the depiction of women in movies evolved over time, by looking at how often men and women appear in summaries over time, and how often they act as protagonists. This study is fueled by the increasing societal focus on gender representation in media. By scrutinizing historical and character-level data, we aim to reveal trends in the depiction of women in film, thereby mirroring broader societal shifts.
</div>

Our dataset comes from the CMU [Movie Summary Corpus](https://www.cs.cmu.edu/~ark/personas/)

# Some general observations

<div style="text-align: justify;">
It is a well known fact that there are differences between actors and actresses ages. We wanted to test if this is true. On the barplot we can observe it and a t-test was made to check if the difference was significative. A p-value inferior to 0.5 was found indicating that actresses are on average younger than actors.
</div>

{% include Age_and_gender.html %}

# Womens representation in different genres

Over all movies together, we can see that there are more male actors than female actresses. 

{% include Gender_proportion_pastel.html %}

<div style="text-align: justify;">
Next, we wanted to know if the genre has an impact on that. How are women represented in different genres? In order to answer this question, we took a look at the twenty biggest genres in our dataset, so the genres where we have most data on actors and actresses in general. Then, we calculated the percentage of women in these genres and the result is shocking: female actresses never make up more than 41.5%, not even in romcoms! And in action movies, the percentage of women falls below 25%. This difference in the amount of women in different genres is highly significant: We performed a chi-squared test and obtained a p-value of approximately zero. 
</div>

{% include Genres_Pink_2.html %}

# Women playing different character types

<div style="text-align: justify;">
We were further interested which character types women play most often in the movies. We can see that women are most prevalent in the character types "dumb blonde" and "brainless beauty". We can also see that there is a big disproportionality in the number of character types for men and for women. This can partly be explained by the surplus of data on men than on women. But it might also hint at the fact that there are fewer "boxes" for female characters to fit in, they are portrayed more stereotypically and there is less variety in how they are written. Either way, the effect of character types on gender is significant, we performed a chi-square test and got a p-value of approximately zero. It is however important to note that there is very little data on character types in general, so this result needs to be taken with a grain of salt.
</div>


{% include types_wholeplot.html %}


Do you want to know more about with which adjectives male and female characters are described, which sentiments are linked to them, and what jobs they usually have in movies? You can find all that and more [here](/Women_and_movies/summaries/).


