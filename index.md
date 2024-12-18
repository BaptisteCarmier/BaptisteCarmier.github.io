---
layout: page
title: WHO'S IN THE SPOTLIGHTS
subtitle: by Ecureuils Cosmiques 24
cover-img: /assets/img/header_ada.png

author: Carmier Baptiste, Léo Carron, Thomas Lepère, Adélaide Pinel, Etienne De Labarrière
---

Gender equality and representation has been a core issue since the 20th and 21th century. Those centuries are characterized by a lot of movement and progress towards women's rights, for example in France the legalization of abortion in 1975. Knowing that it is commonly said that _“cinema is not only an art form but also a mirror of society”_, the question of gender representation is directly linked to the movie industry and it reflects how we perceive the world. In the movie industry, a lot of norms exist and they could change from country to country because more are conservatives while the others are progressive. Therefore an analysis should be done to assess those norms and to understand to what extent they impact movie creation and what are their potential causes. Mentalities also evolve with time and analyzing those different standards of evolution is necessary.

##### Datasets
For this project we mainly used the [CMU Movie Summary Corpus](https://www.cs.cmu.edu/~ark/personas/), which contains 42,306 movie plot summaries, sourced from Wikipedia. It also provides metadata for each movies such as title, release years, box office revenue, etc. The dataset also includes characters characteristic and so actors labels exists such as gender, age, ethnicity, etc.
In parallel, we also used the `names-dataset` Python library to reconstruct missing genres, as well as demographis data ([Our World in Data Population & Demography Explorer](https://ourworldindata.org/explorers/population-and-demography)) to analyze country level representation in films.

For further details on each dataset please check the [datasets page](https://baptistecarmier.github.io/datasets/).


{: .box-note}
**Note:** Mosts graphs are interactive allowing you to explore details about it.

# Naive Analysis
## Un subtitle

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum nisl ex, tempor a ipsum et, porttitor eleifend odio. Aenean tincidunt faucibus nisl sed tempus. Integer sollicitudin feugiat risus non sodales. Etiam sit amet nulla euismod, fringilla erat vel, iaculis augue. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Nullam tempus, sapien ac elementum ullamcorper, orci eros dignissim eros, et pretium ipsum justo vel lectus. Sed vitae pharetra lorem. Sed malesuada leo vitae accumsan placerat. Donec malesuada sapien dui.

{: .box-note}
**Note:** Mosts graphs are interactive allowing you to explore details about it.


# Biases 

# Better Analysis

<div style="text-align: justify;">
Graph des régions (pas obligé)
</div>

{% include bar_chart_region_actors.html%} 

<div style="text-align: justify;">
Et on rajoute une heatmap, par définition elle est centrée
</div>

{% include heatmap_female_actors.html%} 

# Analysis by country

<div style="text-align: justify;">
Changer le titre et écrire les paragraphes... Map interactive, est-ce que ça marche?
</div>

{% include women_representation_map.html%} 

# Conclusion

