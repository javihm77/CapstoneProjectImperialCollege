# Model Card

## Model Description

- Model Name: Fine-tuned BERT for Sentiment Analysis of "Por Favor No Se Enoje" YouTube Comments
- Model Type: Sequence Classification
- Version: 1.0
- Developed By: Javier Hernandez
Date: November, 2024
Programming Language: Python
Libraries: transformers, torch, sklearn, etc. 

## Intended Use

This model is designed to classify the sentiment expressed in YouTube comments related to the Guatemalan radio program "Por Favor No Se Enoje." Its primary purpose is to automate the process of identifying the sentiment (positive, negative, or neutral) behind viewers' comments regarding the program's political discussions and content.

## Target Audience

The target audience includes content creators, media analysts, social scientists, and researchers interested in public opinion, political discourse, and sentiment analysis in Guatemala and neighboring countries.

## Factors Influencing Model Performance

- Text Length and Complexity: The length and complexity of comments can impact the model's ability to accurately predict sentiment. Shorter or more straightforward comments may be easier to classify.
- Vocabulary: Comments containing slang, colloquialisms, or specialized vocabulary related to Guatemalan politics might be harder to interpret.
- Emotional Expression: Implicit or nuanced expressions of sentiment might be more challenging for the model to detect accurately.
- Data Distribution: The model's performance is influenced by the distribution of sentiment classes in the training data. Imbalanced datasets can lead to biased predictions.
Metrics

## Model performance was evaluated using the following metrics:

- Accuracy: The proportion of correctly classified comments.
- Precision: The proportion of correctly predicted positive comments among all comments predicted as positive.
- Recall: The proportion of correctly predicted positive comments among all actual positive comments.
- F1-score: A balanced measure of precision and recall.
- Confusion Matrix: A table visualizing the model's performance across different sentiment classes, including true positives, true negatives, false positives, and false negatives.

## Evaluation Data

The model was evaluated on a manually labeled dataset of YouTube comments related to "Por Favor No Se Enoje" videos. This labeled dataset was split into training and test sets for fine-tuning the BERT model and evaluating its performance. The data used for evaluation contained comments in Spanish, covering various topics discussed on the program.

## Ethical Considerations

- Potential for Bias: The model might reflect biases present in the training data. Due to the limited dataset size, there could be skewed representation for some opinions and specific terminology from the program's users. This might lead to misclassifying sentiment for certain comments.
- Misinterpretation: Predictions are probabilities, and the model can still make mistakes. It's important to interpret the output with caution, particularly for sensitive topics.
- Transparency and Explainability: As a fine-tuned BERT model, its decision-making process can be opaque, posing challenges for understanding why certain sentiment predictions are made.

## Caveats and Recommendations

- Limited Dataset: The model was trained on a relatively small dataset of manually labeled comments which could limit generalizability. Expanding the training data with more diverse examples can further enhance model performance.
- Domain Specificity: The model is tailored to sentiment analysis within the context of "Por Favor No Se Enoje" YouTube comments. Its performance on comments from other YouTube channels or social media platforms might vary.
- Interpretability: Due to the complex nature of BERT models, interpretating specific word/feature influence on the model’s sentiment predictions can be challenging. While we leveraged SHAP analysis, these outputs should be interpreted cautiously, and further analysis is necessary.
- Human Review: The model should be seen as a tool to assist human analysis rather than fully replacing it. Especially when accuracy is critical, results should be reviewed by human reviewers.
- Continuous Monitoring: Continuously monitor the model's performance using updated datasets or data from newer Youtube videos. Re-evaluate the model for changing trends in YouTube comments for "Por Favor No Se Enoje".
