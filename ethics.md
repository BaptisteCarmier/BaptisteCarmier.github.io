---
layout: page
title: Ethical Considerations
cover-img: /assets/img/ethics2.webp
subtitle:
---
<div style="text-align: justify;">
As working with data can potentially have negative impacts on people, societies and the environment, we think it is crucial to address ethical considerations regarding our project. In following, we will take a closer look into the ethical risks and mitigations of our project using the categories proposed in the <a href="https://docs.google.com/document/d/1lhGV_xJiiuC98it5RB2TiitIBgu0pjUK8qq-8y-wbPw/edit" target="_blank">Digital Ethics Canvas 2023</a>.
</div>

# Dataset 
<div style="text-align: justify;">
Our dataset comes from the CMU Movie Summary Corpus. It was collected by David Bamman, Brendan O'Connor, and Noah Smith at the Language Technologies Institute and Machine Learning Department at Carnegie Mellon University. It was created with the purpose of looking at latent Personas of Film Characters. The data was extracted from Wikipedia and aligned with Metadata extracted from Freebase. The research was supported in part by U.S. National Science Foundation grant IIS-0915187. The data was extracted from Wikipedia on November 2nd, 2012. It contains data on movies ranging from 1898 to 2010. The data was preprocessed by the original authors, who extracted data on character types through language processing. It was additionally preprocessed by us, mainly by removing duplicated and outliers (such as for instance ages of actors above 150 years old). There is some missing data, for instance there are not summaries available for every movie, but only for about half. However, as there were still a total of 42295 summaries available, we considered this to be a sufficient dataset for our analysis. There was only data on box office revenue available for about 10% of the movies, which is why we rejected a research question about that. There is also not a lot of data on character types available. We do include the character types data in our research because we considered them to be interesting, but we are transparent about the fact that this data is very limited. The movie data in general is accessible <a href="https://www.cs.cmu.edu/~ark/personas/" target="_blank">here</a>. The data used for our project is stored in the project Github repository under <a href="https://github.com/epfl-ada/ada-2023-project-adavengers2023/tree/main/data" target="_blank">data</a> and the preprocessing on the data that we did can be seen in <a href="https://github.com/epfl-ada/ada-2023-project-adavengers2023/blob/main/Milestone2.ipynb" target="_blank">Milestone 2</a>.
</div>

# Beneficence
<div style="text-align: justify;">
We expect our research to benefit anyone who is interested in movies and the representation of women in them. The benefits of our analysis are manifold. Our project aims to educate readers about the depiction of women in movies. We strive to promote awareness about subtle biases that might influence our worldviews through the media we consume. Furthermore, this project promotes paying attention to detail and watching movies where women are more represented and portrayed in a more interesting light. As the demands of the audience greatly influences producers, we hope that the producers of movies will also pay more attention to this highly relevant topic in the future. 
</div>
  
# Privacy
<div style="text-align: justify;">
We believe that our data does not contain especially sensible data regarding privacy, as it only includes publicly available data on movies and actors/actresses. However, even in this case it is important to ask ourselves if the actors/actresses or movie producers are harmed by the way we use the data. We mitigate this by not mentioning individual movies or people explicitly but only talking about movies overall (for instance, we mention actresses are generally younger than actors in movies, but do not mention the ages of individual people). Hence, no personal or sensitive information can be derived from our analysis. 
</div>

# Non-maleficence
<div style="text-align: justify;">
Our data contains unsafe data to a certain extend as the movie summaries might contain descriptions of violence or nudity. However, as we do not show entire summaries but only adjectives extracted from them, so we think this is not an issue. Errors in the data or analysis could impact the validity of our findings and give a wrong idea about the way women are described in movies. Finally, since we are analyzing a lot of stereotypes concerning women as well as men in our project, it is crucial to emphasize that these are stereotypes and not the truth. We try our best to convey this message throughout all of the project and we believe that being aware of stereotypes and biases helps to avoid actually believing them and acting upon them in everyday life.
</div>

# Fairness
<div style="text-align: justify;">
We would like to emphasize that our data is in no way representative of the real world, as it is about movies, which are mostly fictional. The data may be biased by the majority of movies being from the United States of America. Movies from other regions of the world might not be represented accurately. In future analysis, it might be interesting to see how our results vary in different regions. Other than that, there might be biases in the age of the movies, however we do take this into account when taking a look at the evolution of female characters in movies over time. 
</div>

# Sustainability
<div style="text-align: justify;">
We believe that the carbon footprint generated by the storage of our data is negligible, as we are handling relatively small amounts of data. There is no human manual labor involved apart from the work done by the group members. The data and analysis do not require updates per se, but it would be very interesting to extend our research with more recent movie data in the future. 
</div>

# Empowerment 
<div style="text-align: justify;">
The people involved in the dataset (the actors and actresses) have not been notified about our project, however as mentioned above we believe this is ethical since the data we use about them is already publicly available and, more importantly, since we do not mention them individually in our data story, as described in the Privacy section above. 
</div>



