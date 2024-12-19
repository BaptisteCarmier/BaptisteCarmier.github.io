---
layout: page
title: WHO'S IN THE SPOTLIGHTS
subtitle: by Ecureuils Cosmiques 24
cover-img: /assets/img/header_ada.png

author: Carmier Baptiste, Léo Carron, Thomas Lepère, Adélaide Pinel, Etienne De Labarrière
---

<div style="text-align: justify;">
    Gender equality and representation has been a core issue since the 20th and 21th century. Those centuries are characterized by a lot of movement and progress towards women's rights, for example in France the legalization of abortion in 1975. Knowing that it is commonly said that <em>“cinema is not only an art form but also a mirror of society”</em>, the question of gender representation is directly linked to the movie industry and it reflects how we perceive the world. In the movie industry, a lot of norms exist and they could change from country to country because more are conservatives while the others are progressive. Therefore an analysis should be done to assess those norms and to understand to what extent they impact movie creation and what are their potential causes. Mentalities also evolve with time and analyzing those different standards of evolution is necessary.
</div>

##### Datasets

<div style="text-align: justify;">
  For this project we mainly used the <a href="https://www.cs.cmu.edu/~ark/personas/">CMU Movie Summary Corpus</a>, which contains 42,306 movie plot summaries, sourced from Wikipedia. It also provides metadata for each movie such as title, release years, box office revenue, etc. The dataset also includes characters' characteristics and actors' labels such as gender, age, ethnicity, etc.<br>
  
  In parallel, we also used the <code>names-dataset</code> Python library to reconstruct missing genres, as well as demographic data (<a href="https://ourworldindata.org/explorers/population-and-demography">Our World in Data Population & Demography Explorer</a>) to analyze country-level representation in films. We also scaled the box office according to the value of the dollars at the year of interest based on the <a href="https://fred.stlouisfed.org/series/CPIAUCNS#0">Consumers Price Index</a>.<br>

  For further details on each dataset please check the <a href="https://baptistecarmier.github.io/datasets/">datasets page</a>.
</div>


{: .box-note}
**Note:** Mosts graphs are interactive allowing you to explore details about it.

# A First observation 

<div style="text-align: justify;">
    Analyzing the proportion of male and female actors in movies over the years provides valuable insights into the evolution of gender representation in the film industry. This view highlights trends and potential imbalances, helping us track changes and assess progress in achieving gender diversity in casting. A first plot of the evolution of the women proportion in movies over time gives a first intuition on our analysis : 
</div>

{% include gender_proportion_plot.html%} 

# Naive Analysis

# Spatial Analysis

{% include bar_chart_region_actors.html%} 

{% include heatmap_female_actors.html%} 

{% include women_representation_map.html%} 

# Biases 

{% include boxplot_bias.html%} 

# Better Analysis

## Matching the data 

<div style="text-align: justify;">
    Why have unbalanced casts ? 
    Since we observed that the women are underrepresented in the movie industry, we want to analyze if there is an economic reason for this imbalance in the actor casts. To begin, we get an insight on whether movies with heterogeneous cast distribution perform better than balanced one by having a look to the plot of the distribution of the movies’ box office for these two groups : 
</div>

{% include before_matching_movies.html%}

<div style="text-align: justify;">
    The distribution appears more or less similar, with a slight tendency for higher box office revenues in movies with unbalanced casts. To better analyze the impact of gender balance in movie casts, we use propensity score matching to compare movies that are more “comparable” according to their characteristics. This method ensures that the two groups are comparable by creating a matched dataset where we can more accurately assess differences in outcomes, such as box office success, that may be influenced by the gender balance of the cast. The plot below shows the same distribution but now with matched movies : 
</div>


# Conclusion

