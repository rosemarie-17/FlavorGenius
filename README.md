# FlavorGenius: Unleashing AI's Mastery in Flavor Discovery
## Project Overview
This project leverages natural language processing (NLP) techniques and Amazon's 2023 Grocery and Gourmet Food reviews dataset to uncover emerging trends in healthy snacks, particularly for aging demographics. By combining review and metadata, we aim to support research and development (R&D) in identifying popular flavors, concepts, and market opportunities in the healthy snack industry.

## Objectives and Goals
* Analyze customer reviews to identify key themes and preferences.
* Use topic modeling to discover potential popular trends for aging demographics.
* Support R&D by providing data-driven insights into consumer preferences.

## Methodology
1. **Data Preparation:**
   * Merged review and metadata datasets using 'parent_asin' as the key.
   * Cleaned and preprocessed text data by removing stopwords and tokenizing.
2. **Topic Modeling:**
   * Applied Latent Dirichlet Allocation (LDA) to extract latent topics and themes from the text data.
3. **Evaluation:**
   * Analyzed the extracted topics to align them with potential consumer trends.
   * Generated word clouds with popular terms for each topic

## Results
* Identified major themes in the healthy snacks category, including keywords related to low-carb snacks, sugar-free options, and protein-rich products.
* Discovered significant trends in flavor preferences, such as "salty," "chocolate," "fruity," and "nut blends."
* Provided insights for the R&D team to focus on specific flavors and dietary preferences.

## Visualizations
These are some sample word clouds our project produced:
![wordcloud 1](https://github.com/user-attachments/assets/399f3b34-4eb5-41ed-8b67-406a9dd87705)
---
![wordcloud 2](https://github.com/user-attachments/assets/5a516916-58d8-4937-a0a5-8872788db0b2)

## Next Steps
* Extend topic modeling to include additional categories from the Amazon Reviews dataset, including 'Health and Personal Care' and 'Home and Kitchen.'
* Further develop topic detection algorithms to understand trends and topics for high and low-rating reviews and products.

## Individual Contributions
Each team member individually processed the data using different keywords.
* <ins>Rosemarie:</ins> snacks, low-carb
* <ins>Tamia:</ins> protein, vegetable
* <ins>Nasrin:</ins> fruits, vitamins
* <ins>Michelle:</ins> collagen, sugar-free

## How to Run
1. **Clone the Repository:**
   Clone this repository to your local machine:
   ```
   git clone <repository_url>
   cd <repository_directory>
   ```
2. **Install Dependencies:**
   Make sure you have Python 3.8 or later installed. Install the required libraries:
   ```
   pip install -r requirements.txt
   ```
3. **Download the Dataset:**
   The dataset used for this project can be accessed from [Amazon Reviews Dataset 2023](https://huggingface.co/datasets/McAuley-Lab/Amazon-Reviews-2023)
   * To install user reviews:
     Run the following code to download the user reviews:
     ```
     from datasets import load_dataset
     
     dataset = load_dataset("McAuley-Lab/Amazon-Reviews-2023", "raw_review_Grocery_and_Gourmet_Food", trust_remote_code=True)
     print(dataset["full"][0])
     ```
   * To install item metadata:
     Run the following code to download the user reviews:
     ```
     from datasets import load_dataset
     
     dataset = load_dataset("McAuley-Lab/Amazon-Reviews-2023", "raw_meta_Grocery_and_Gourmet_Food", trust_remote_code=True)
     print(dataset["full"][0])
     ```
