# Datasheet Template

## Motivation

This dataset was collected to analyze public sentiment towards the Guatemalan radio program "Por Favor No Se Enoje" expressed in YouTube comments associated with the program's videos. The purpose is to gain insights into audience reactions and opinions regarding the program's content and discussions on Guatemalan and regional politics. This dataset supports a Machine Learning and Artificial Intelligence capstone project for Imperial College's Professional Certificate in Machine Learning and Artificial Intelligence.

 
## Composition

The dataset comprises YouTube comments and associated video information collected using the YouTube Data API.

Features:

- text: The raw text of the YouTube comment.
- processed_comment: Text cleaned, lowercased, and with punctuation, numbers and extra spaces removed. Spanish stopwords from NLTK's stopwords module have been removed.
- video title: The title of the YouTube video to which the comment belongs.
- video published_date: The date the video was published on YouTube. Format: YYYY-MM-DD. Timezone: Etc/GMT+6.
- video view_count: The number of times the video was viewed.
- video like_count: The number of 'likes' the video received.
- updated_at: The timestamp of the comment collection, converted to Etc/GMT+6.
- vader_sentiment: A sentiment classification based on the Vader SentimentIntensityAnalyzer applied to the processed_comment. Values: "positive," "negative," or "neutral."
- human_sentiment: Manually labeled sentiment by human reviewers. Values: "positive," "negative," or "neutral." This was labeled using a subset of the dataset.
- topic: A topic assignment for the comment based on BERTopic model analysis. Topic numbers will vary based on model run. Negative topic number "-1" corresponds to outliers.

## Collection process

Comments were collected using the YouTube Data API v3 using the commentThreads endpoint for videos associated with the program "Por Favor No Se Enoje."

## Preprocessing/cleaning/labelling

The preprocessing steps include:

- Text Cleaning: Removal of punctuation, numbers, and extra spaces from the comment text using string manipulation functions.
- Lowercasing: Converting the comment text to lowercase for normalization.
- Stop Word Removal: Elimination of Spanish stop words from the comment text using NLTK's stopwords module. This removes common and irrelevant words that do not contribute to sentiment analysis or topic modeling.
 
## Uses

This dataset is intended for use in sentiment analysis, topic modeling, and social media monitoring studies. It enables analysis of public opinion towards "Por Favor No Se Enoje," facilitating insights for content creators, media analysts, and researchers interested in political discussion and public sentiment in Guatemala and surrounding countries.

## Distribution

This dataset is stored in a Google Drive folder located at: '/content/drive/MyDrive/Imperial College/Capstone Project/'. Access and distribution permissions are subject to control by the data owners. 

## Maintenance

There are no documented protocols or plans for maintaining and updating the dataset within the notebook. Information on how data could be appended with new comments as they are published on YouTube would strengthen the datasheet.

## Caveats

- Bias and Subjectivity: The comments express the opinions of YouTube users, and can be influenced by biases related to age, gender, location, political affiliation and culture.
- Offensive or Inappropriate Content: YouTube comments might contain offensive or inappropriate language. Some content has been filtered with manual labeling and data processing, but this might not have removed all instances.
- Misrepresentation of Public Opinion: The dataset reflects the views expressed by users who actively comment on YouTube, which might not be representative of the broader public's opinion.
- Human labeling subjectivity Subset of data was manually labeled for "human sentiment" introducing subjectivity as reviewers might have differing perceptions of comment sentiments.

