# Assessing Wine Excellence: Exploring, Predicting, and Deployment 

Although I'm not well-versed in wine tasting, I am genuinely intrigued by the process of wine scoring. Over time, I've come to realize that certain wines are more enjoyable to me than others. Interestingly, my perception of a good wine seems to have little correlation with its price, brand, or country of origin. Even with some wines that bear impressive price tags, I've found them less than palatable. This sentiment holds true for wines from prestigious brands and those originating from regions like France or Argentina.

In an effort to avoid the disappointment of unfinished wine bottles at dinners or gatherings, I've adopted a strategy of purchasing wines based on their scores. I'm aware that these scores are highly subjective in nature. A wine rating is essentially a judgment assigned by wine critics after evaluating a wine, encapsulating their overall impression of the wine. It's a personal assessment, often conveyed through a numerical rating.

Although it's a bit subjective, I have to admit that choosing wines with high scores has worked well for me. But, I've noticed a downside: it means I'm only considering wines that have been scored. This limitation makes me wish I could find great wines from places that aren't reviewed by fancy critics, who can be pretty expensive.

This brings me to an intriguing question: Is there a systematic way to score wines? Could there potentially be an automated method for wine scoring?


**Dataset and Features**

The dataset employed in this research was sourced from the UCI Machine Learning Repository [link](https://archive.ics.uci.edu/dataset/186/wine+quality). The dataset encompasses wines originating from Minho, Portugal, specifically focusing on two distinct variants: red and white "Vinho Verde" wines. The dataset comprises two subsets, each pertaining to one of the variants. Within these subsets, there are eleven variables encompassing both physicochemical attributes (outlined in the table below) and a sensory quality score, which is rated on a scale from 0 to 10. Notably, the dataset does not encompass information about grape types, wine brands, or wine selling prices.

In the scope of this investigation, I merged the two datasets to facilitate the exploration of binary classification. The objective was to ascertain the optimal set of attributes that would yield the most effective outcomes in predicting whether a given sample corresponds to red or white wine.

<table style="font-family: Arial, sans-serif; font-size: 13px;">
  <tr>
    <th><b>Attribute</b></th>
    <th><b>Description</b></th>
  </tr>
  <tr>
    <td><b>Fixed Acidity</b></td>
    <td>This attribute represents the presence of fixed acids in the wine, such as tartaric and malic acid, contributing to taste and preservation.</td>
  </tr>
  <tr>
    <td><b>Volatile Acidity</b></td>
    <td>This attribute quantifies the volatile acids, including acetic acid, which can impart undesirable taste and odor to the wine.</td>
  </tr>
  <tr>
    <td><b>Citric Acid</b></td>
    <td>Citric acid, found in citrus fruits, adds a tangy flavor to the wine.</td>
  </tr>
  <tr>
    <td><b>Residual Sugar</b></td>
    <td>This attribute measures unfermented sugar content, influencing the wine's sweetness and taste.</td>
  </tr>
  <tr>
    <td><b>Chlorides</b></td>
    <td>Chlorides signify salt content in the wine, impacting its flavor profile.</td>
  </tr>
  <tr>
    <td><b>Free Sulfur Dioxide</b></td>
    <td>This attribute denotes sulfur dioxide that remains unreacted in the wine.</td>
  </tr>
  <tr>
    <td><b>Total Sulfur Dioxide</b></td>
    <td>Total sulfur dioxide includes both free and bound forms of sulfur dioxide.</td>
  </tr>
  <tr>
    <td><b>Density</b></td>
    <td>Density reflects the connection between alcohol content and grape variety in the wine.</td>
  </tr>
  <tr>
    <td><b>pH</b></td>
    <td>pH serves as a measure of the wine's acidity or basicity.</td>
  </tr>
  <tr>
    <td><b>Sulfates</b></td>
    <td>Sulfates, a type of preservative, influence both preservation and flavor of the wine.</td>
  </tr>
  <tr>
    <td><b>Alcohol</b></td>
    <td>Alcohol percentage impacts the wine's body and flavor characteristics.</td>
  </tr>
  <tr>
    <td><b>Quality</b></td>
    <td>Target variable, assessed on a scale of 0 to 10.</td>
  </tr>
</table>

Broadly speaking, the Random Forest Classifier and Support Vector Classifier stand out for achieving an impressive binary accuracy of 99.6%. Additionally, the Gradient Boosting Classifier, K-Nearest Neighbors, and Logistic Regression exhibit commendable binary accuracy performances.

It's apparent that the models fall short of being optimal, particularly when dealing with multiclass classification tasks. Nevertheless, these results should not constrain our potential. Possibilities for enhancement remain accessible through meticulous refinement, with special attention directed towards the refinement of the Deep Neural Network model.

The value of data-driven methodologies in the context of wine assessment becomes apparent. By synergizing data exploration, feature engineering, and advanced modeling techniques, we can uncover latent patterns and trends within the data. This journey doesn't conclude here; the continuous fine-tuning of models and exploration of novel data sources have the potential to further enhance the precision and relevance of our predictions.

The models are deployed on huggingface. You may refer below links for your reference.
* [wine_type_predictor_app](https://huggingface.co/spaces/sedeba19/Binary_Classification_Wine)
* [wine_quality_predictor_app](https://huggingface.co/spaces/sedeba19/wine_prediction_streamlit)

The article can be found here: 
