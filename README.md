# Unsupervised-Machine-Learning

## Project Overview

In this project, I am working for the fictitious company Moosic, a start-up that specializes in curating playlists tailored to specific moods.

## Objectives

	1.	Assess whether Spotify’s audio features (such as tempo, energy, danceability, etc.) can effectively identify “similar songs” based on humanly detectable criteria.
	2.	Evaluate the effectiveness of K-Means clustering as a method for creating music playlists.
	3.	Provide a prototype of automated playlist creation that can be refined in collaboration with Moosic’s music experts.

## Data Overview

The dataset contains the following audio features ([Spotify Web API documentation](https://developer.spotify.com/documentation/web-api/reference/get-audio-features)):

- Acousticness
- Danceability
- Energy
- Instrumentalness
- Liveness
- Loudness
- Speechiness
- Tempo
- Valence
- Duration
- Key
- Mode
- Time Signature


## Data Preparation

- Feature Selection: The most relevant audio features that would contribute to the clustering process have been selected while the ones that do not contribute much have been dropped.
- Outliers:The outlier songs were handled separately because the scaler is sensitive to outliers. The outliers were then divided into their own playlists.
 - Standardization: The selected features were standardized to ensure consistency across the dataset and to improve the performance of the clustering algorithm.
-	Principal Component Analysis (PCA): To simplify the dataset while retaining most of the variance, PCA was applied. This step allowed us to reduce the dimensionality of the data, making it easier to cluster and visualize.

## Evaluation of the K-Means Clustering

- Effectiveness: The audio features provided by Spotify were moderately effective in identifying similar songs as defined by humanly detectable criteria. Some songs in the playlists fit together very well, while others were a mixed bag.
  
- Limitations: Music is very subjective, so whether the clustering was successful or not is naturally in the eye of the beholder. This clustering is also based on Spotify’s audio features, which often appear arbitrary.

## Next Steps 

Since the objective of this project was to evaluate how well K-Means clustering performs in reating suitable playlists, it is the only algorithm applied here. In future steps, other algorithms can also be tested for their clustering capabilities in this case. Algorithms such as DBSCAN or hierarchical clustering might offer better performance or be more suitable for this type of data.

