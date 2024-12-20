---
layout: page
title: WHO'S IN THE SPOTLIGHTS
subtitle: by Ecureuils Cosmiques 24
cover-img: /assets/img/header_ada.png

author: Carmier Baptiste, Léo Carron, Thomas Lepère, Adélaide Pinel, Etienne De Labarrière
---

# Abstract
<div style="text-align: justify;">
    Gender equality and representation has been a core issue since the 20th and 21th century. Those centuries are characterized by a lot of movement and progress towards women's rights, for example in France the legalization of abortion in 1975. Knowing that it is commonly said that <em>“cinema is not only an art form but also a mirror of society”</em>, the question of gender representation is directly linked to the movie industry and it reflects how we perceive the world. In the movie industry, a lot of norms exist and they could change from country to country because more are conservatives while the others are progressive. Therefore an analysis should be done to assess those norms and to understand to what extent they impact movie creation and what are their potential causes. Mentalities also evolve with time and analyzing those different standards of evolution is necessary.
</div>
<br>

##### Datasets

<div style="text-align: justify;">
  For this project we mainly used the <a href="https://www.cs.cmu.edu/~ark/personas/">CMU Movie Summary Corpus</a>, which contains 42,306 movie plot summaries, sourced from Wikipedia. It also provides metadata for each movie such as title, release years, box office revenue, etc. The dataset also includes characters' characteristics and actors' labels such as gender, age, ethnicity, etc.<br>
  
  In parallel, we also used the <code>names-dataset</code> Python library to reconstruct missing genres, as well as demographic data (<a href="https://ourworldindata.org/explorers/population-and-demography">Our World in Data Population & Demography Explorer</a>) to analyze country-level representation in films. We also scaled the box office according to the value of the dollars at the year of interest based on the <a href="https://fred.stlouisfed.org/series/CPIAUCNS#0">Consumers Price Index</a>.<br>

  For further details on each dataset please check the <a href="https://baptistecarmier.github.io/datasets/">datasets page</a>.
</div>

{: .box-note}
**Note:** Mosts graphs are interactive allowing you to explore details about it.

# Some first observations 

<div style="text-align: justify;">
    As already mentioned, gender representation in movies reflect societal norms and thus evolves across time, genres, and regions. By analyzing these categorical values, we may understand how cinema mirrors challenges of gender representation.
</div>

### Across time
<div style="text-align: justify;">
    Analyzing the proportion of male and female actors in movies over the years provides valuable insights into the evolution of gender representation in the film industry. This view highlights trends and potential imbalances, helping us track changes and assess progress in achieving gender diversity in casting. A first plot of the evolution of men and women proportion in movies over time gives a first intuition on our analysis : 
</div>

{% include gender_proportion_plot.html%} 

<div style="text-align: justify;">
    This plots clearly shows that representation of gender has evolved since 1900. Since 1910 women representation have deacresed until 1940. At this point, the proportions are more or less constant until the 90's where women representation in movies slightly increases. 
</div>

### Among movie genres
<div style="text-align: justify;">
    This first analysis open the door to a more clichéd analysis based on the genre of the movie, expecting more women in drama or romantic movies than in other genres. 
</div>

{% include bar_chart_movie_genre.html%}

<div style="text-align: justify;">
    There is a clear difference in representation depending on the movie genre. As we expected, this reveals that women are more likely to play in drama or romantic movie, or at least they are more present in those genres rather than in others. This plot also shows that women are way less represented than men regardeless of the movie genre. 
</div>

<div style="text-alogn: justify;">
    Talking of movie genres, the movie genres was clustered based on a K-means algorithm that cluster all the differents genres in 15 clusters. This was based on the 5 main genres provided in the dataset for each movies, and is more convenient for further analysis. However, the following heatmap shows how each cluster is characterized.
</div>

{% include heatmap_clusters.html%}

### Among geographical regions

<div style="text-align: justify;">
    This first plot shows the distribution of male and female actors by region, highlighting North America, Asia, and Western Europe as the most represented regions in the dataset. Other regions have significantly fewer entries, indicating a potential underrepresentation of those areas. This uneven data distribution could reflect disparities in global cinema production, with some countries (like the USA) having large movie markets. At first glance, there seem to be no significant regional differences in gender distribution. We'll go further in the analysis by looking at a temporal scale.
</div>

{% include bar_chart_region_actors.html%} 

<div style="text-align: justify;">
    A temporal analysis of the trends of the representation was made and the heatmap below reveals how the proportion of female actors varies across regions and 25-year generational periods. Here we observe that in some regions like East Europa, the female representation seems to have increased quite significantly over the past century. For North America and Western Europe, the regions with the most data, it shows a gradual rise in female representation, except for a surprisingly high representation in the 1900–1925 period.
</div>

{% include heatmap_female_actors.html%} 

<div style="text-align: justify;">
    The heatmap's maximum value of 0.40 highlights a significant gap from the equitable fifty-fifty representation, meaning that there’s still today an underrepresentation in the movies across the globe. 
    <br>
    By using the data from <a href="https://ourworldindata.org/explorers/population-and-demography">Our World in Data Population & Demography Explorer</a>, we were able to calculate the proportion of women in each country for the generations from 1950 to today. Then, a representativity index was calculated by dividing the proportion of women in movies by their proportion in the population minus 1. A value of 0 indicates fair representation, while positive and negative values show respectively over- and under-representation. The map illustrates this representativity index by country and generation, as well as the net evolution of this representativity between the first (1950-1975) and last (2000-2020) generation.
</div>

{% include women_representation_map.html%} 

<div style="text-align: justify;">
    No surprise here! All countries are shaded in red, indicating the persistent overrepresentation of male actors in movies over time. The only exception is Indonesia during the last generation, having an overrepresentation of female actors! However, it’s interesting to look at the net evolution as if we zoom in on Europe, most of the countries have evolved toward a more equal representation of the genders. In conclusion, all these green-shaded countries indicate that while women are still underrepresented in movies, it is less marked than it was fifty years ago.
</div>

# Biases 
<div style="text-align: justify;">
    The figure below analyzes the biases that may exist between genders for different features. It displays two boxplots for male and female actors across five key features: Release Date, Box Office (scaled), Runtime, Height (scaled), and Age.
</div>

{% include boxplot_bias.html%} 

<div style="text-align; justify;">
    For release date, scaled box office, and runtime, it seems like there is no significant gender biases. Both genders show similar distributions, indicating that over time, the opportunities and success in terms of release years and scaled box office performance are not strongly influenced by gender. Films of different runtime also appear equally distributed between male and female actors.
    <br>
    However, the height scaled to the mean height of the gender in the world population reveals an interesting bias, as female actors tend to be taller than their average height in the population, while male actors’ heights align more closely with the average for men. This suggests a possible preference for taller women in casting, maybe reflecting some societal beauty standards. For male actors, the median is also higher than in the population but it is not as pronounced.
    <br>
    The age demonstrates a clear gender bias, with male actors generally being older than female actors. The age IQR for male actors is larger than for females, with a skew towards older ages, which may reflect the industry's tendency to favor older male actors in leading roles, while 75% of female actors are below 40 years old.
    <br>
    Thus, the only biases found were on the age and the height, which are the only two features that we can associate with the physic of the actor, which could reflect some standard of the society that causes these biases.
</div>

# Analyzing with matching data
<div style="text-align: justify;">
    The analysis of gender representation can be pushed further by matching the data, this means removing as much biases as possible to compare two equal things so a men and women of same height, same generation, or regions and which played in the same movie genre.
</div>

#### Matching by actors

<div style="text-align: justify;">
    How could we compare men and women's representativeness?

    So now we would like to know how we could quantify the representativeness of one actor so as to be able to compare representativeness of men and women actors. The parameter that has been chosen was the number of movies an actor did, indeed the more you’re on the screen the more people watch you and you are represented.
    We have seen before that men are significantly more represented than women. Furthermore we also showed some biases like the actor's age that should be taken into account. So we decided to match men vs women actors by taking a sample of a thousand actors to see if there was a significant difference in the number of films played according to the gender by taking into account these famous biases. 
    And we can show you the difference before and after matching
</div>

{% include unmatchgender.html%}

{% include matchgender.html%}

<div style="text-align: justify;">
    By looking at the graph unmatch, men clearly play in more movies than women. And after matching this over-representation was attenuated by matching but still it clearly appears that men play in more movies than women.
    The question is still, even if men are more represented, is this significant or not?
    The answer is in the student's t-test! Indeed by doing a student's t-test between the number of movies made by  men and women after matching we would know that.

    The p-value is 0.0072, clearly less than 0.05, which allows us to conclude that over all the time period the men significantly play in more movies than women even after taking into account biases, so men are significantly more represented !
</div>

<div style="text-align: justify;">
    But is it valid for all periods of time and is there at least a positive evolution ?
    <br>
    To answer that we have done the same matching and student's t-test as before by generation by taking into account only 350 actors because the generation with the least actors contained only 359 of them. Only 4 generation were taken into account: generation 1: 1925-1950, generation 2: 1950-1975, generation 3: 1975-2000 and generation 4: after 2000. But different random sample give different answers that are not the same at all therefore our results are unconvincing and we can't get any satisfying conclusion. Thus, some deeper analysis with more explicit data should be conducted to allow to draw persuasive conclusions. 
</div>

#### Matching by movies

<div style="text-align: justify;">
    Why have unbalanced casts ? 
    Since we observed that the women are underrepresented in the movie industry, we want to analyze if there is an economic reason for this imbalance in the actor casts. To begin, we get an insight on whether movies with heterogeneous cast distribution perform better than balanced one by having a look to the plot of the distribution of the movies’ box office for these two groups : 
</div>

{% include before_matching_movies.html%}

<div style="text-align: justify;">
    The distribution appears more or less similar, with a slight tendency for higher box office revenues in movies with unbalanced casts. To better analyze the impact of gender balance in movie casts, we use propensity score matching to compare movies that are more “comparable” according to their characteristics. This method ensures that the two groups are comparable by creating a matched dataset where we can more accurately assess differences in outcomes, such as box office success, that may be influenced by the gender balance of the cast. The plot below shows the same distribution as before, but now with matched movies : 
</div>

{% include matching_movies.html%}

<div style="text-align: justify;">
    After matching, we can see that the tendency remains similar but now higher box office revenue is observed for the balanced gender movies. With this analysis, the results support the fact that balanced movie’s casts perform a bit better than unbalanced ones according to their box office. This analysis suggests that balanced gender representation in casts can perform as well as - if not better than - unbalanced ones, offering no economic disadvantage and potentially supporting diversity in casting choices. 
</div>

# Conclusion

<div style="text-align: justify;">
    In conclusion, our investigation into gender representation in cinema has revealed the complex relationship between societal norms and the portrayal of women in film. We have demonstrated that gendered roles and stereotypes continue to shape not only the types of characters women portray but also their visibility and prominence within narratives. Our analysis shows that, while some progress has been made, significant disparities remain, particularly in more conservative regions, where representation is more limited. These findings highlight the ongoing challenges within the movie industry, yet they also underscore cinema's potential as a catalyst for social change. Moving forward, it is essential to advocate for a more equitable representation in film that reflects the diverse and evolving understanding of gender. The responsibility to shape a more inclusive cinematic landscape lies in the hands of creators and audiences alike.
</div>


