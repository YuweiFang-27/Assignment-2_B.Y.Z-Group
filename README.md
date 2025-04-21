  # Assignment-2_B.Y.Z-Group
NLP categorisation project for Stack Overflow posts

Group members: 
1. Beining Wang  a1952223
2. Yuwei Fang    a1948355
3. Zheng Wu      a1948878

Dataset Descriptions
This repository contains multiple datasets that were created during different stages of data collection, preprocessing, and classification. Below is a description of each file:

so_raw_posts.zip
Description: This ZIP archive contains the full raw question dataset fetched from Stack Overflow using the Stack Exchange API.
Format: Original questions with fields such as question_id, title, body, tags, and accepted_answer_id.
Reason for ZIP: The raw .csv exceeded GitHub’s upload size limit, so it is compressed.

raw_data.csv
Description: A structured version of the raw data with only relevant columns.
Fields: title, description (body), tags, accepted_answer.
Use: This dataset was used as input to the preprocessing pipeline.

clean_data.csv
Description: A preprocessed version of the raw dataset where HTML tags, punctuation, and stopwords were removed.
Use: This dataset serves as the input for classification models.

auto_categorised_posts.csv
Description: Categorization results based purely on rule-based keyword matching.
Use: Used as a baseline to compare against other classification approach.

final_categorised_posts.csv
Description: The final categorization results after combining rule-based annotations (first 300 rows) with BERT + Logistic Regression predictions for the remaining data.
 Use: evaluate the performance of the hybrid classification approach.

bert_balanced_pred.csv
Description: Predictions from a BERT model fine-tuned on a balanced, rule-labeled subset (max 50 per category).
Use: evaluate the performance of a purely BERT-based classification approach.
