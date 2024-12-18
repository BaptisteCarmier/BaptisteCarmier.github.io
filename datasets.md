---
layout: page
title: WHO'S IN THE SPOTLIGHTS
subtitle: by Ecureuils Cosmiques 24
cover-img: /assets/img/header_ada.png

author: Carmier Baptiste, Léo Carron, Thomas Lepère, Adélaide Pinel, Etienne De Labarrière
---

- The [**CMU Movie Summary Corpus**](https://www.cs.cmu.edu/~ark/personas/) is a dataset focused on movies and character analysis. It includes 42,306 movie plot summaries sourced from Wikipedia. It also provides metadata for each movies Movie box office revenue, genre, release date, runtime, and language. The dataset also includes characters characteristic and so actors labels exists such as gender, estimated age at the time of the movie's release, actor date of birth, actor name and more.

- *name-dataset*: To address missing gender information,
we use the `names-dataset` Python library, sourced from a GitHub repository ([here](https://github.com/philipperemy/name-dataset)).
Based on a Facebook leak, it provides likely gender classifications for first names,
helping us infer actors' genders as male or female. Install it via: `pip install names-dataset`

- To analyze country-level gender representation in films,
we use demographic data from the [Our World in Data Population & Demography Explorer](https://ourworldindata.org/explorers/population-and-demography).
This dataset provides the male and female population for selected countries from 1950 to 2023,
enabling us to compare movie industry gender representation with actual demographic distributions. 
