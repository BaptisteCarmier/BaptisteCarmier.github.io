---
layout: page
title: WHO'S IN THE SPOTLIGHTS
subtitle: by Ecureuils Cosmiques 24
cover-img: /assets/img/header_ada.png

author: Carmier Baptiste, Léo Carron, Thomas Lepère, Adélaide Pinel, Etienne De Labarrière
---
# Datasets Description

<ul>
  <li>
    <div style="text-align: justify;">
      The <a href="https://www.cs.cmu.edu/~ark/personas/">CMU Movie Summary Corpus</a> is a dataset focused on movies and character analysis. It includes 42,306 movie plot summaries sourced from Wikipedia. It also provides metadata for each movie: box office revenue, genre, release date, runtime, and language. The dataset also includes characters' characteristics, and actors' labels such as gender, estimated age at the time of the movie's release, actor date of birth, actor name, and more.
    </div>
    <br>
  </li>
  <li>
    <div style="text-align: justify;">
      <em>name-dataset</em>: To address missing gender information, we use the <code>names-dataset</code> Python library, sourced from a GitHub repository (<a href="https://github.com/philipperemy/name-dataset">here</a>). Based on a Facebook leak, it provides likely gender classifications for first names, helping us infer actors' genders as male or female. Install it via: <code>pip install names-dataset</code>.
    </div>
    <br>
  </li>
  <li>
    <div style="text-align: justify;">
      To analyze country-level gender representation in films, we use demographic data from the <a href="https://ourworldindata.org/explorers/population-and-demography">Our World in Data Population & Demography Explorer</a>. This dataset provides the male and female population for selected countries from 1950 to 2023, enabling us to compare movie industry gender representation with actual demographic distributions.
    </div>
    <br>
  </li>
  <li>
    <div style="text-align: justify;">
      We used the <code>CPI.csv</code> dataset, as the price of the box office needed to be rescaled according to the value of the dollar at the year of interest. It is sourced from <a href="https://fred.stlouisfed.org/series/CPIAUCNS#0">Consumer Price Index for All Urban Consumers: All Items in U.S. City Average (CPIAUCNS) - FRED - St. Louis Fed</a>, which sources data from the US Bureau of Labor Statistics. This dataset contains the Consumer Price Index for the years between 1913 and 2024, adjusted to 1982-1984 as the base years.
    </div>
    <br>
  </li>
</ul>
