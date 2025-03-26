# Premier League Match Outcome Prediction

## Project Overview
This project predicts the outcome of Premier League matches using machine learning, specifically XGBoost on AWS SageMaker. 
The dataset was collected from a football match API and processed to extract meaningful features before training the model.

## Dataset
The dataset was initially sourced through an API, which provided extensive match data from the Premier League. However, the raw dataset required significant processing. 
I had to clean and transform the data, which involved removing unnecessary features, handling missing values, and encoding categorical variables. 
I also reduced the dataset to ensure it was suitable for training machine learning models. 
Some key features included in the final dataset were team statistics (home/away win rates, average goals scored, etc.), match outcomes, and team-related information.
- Removing unnecessary columns
- Encoding categorical variables
- Creating new features from existing data
- Normalizing and transforming numerical data

## Model and Training
Initially, I tried using AWS SageMaker for model training and deployment. However, I encountered several issues:
- The data format was not in the required LIBSVM format for SageMaker.
- Faced difficulties with encoding issues for multi-class classification, particularly related to the match_outcome label.
- The training job failed multiple times due to configuration errors and incorrect data types.

After encountering these obstacles, I decided to run the model locally instead of continuing with SageMaker.

## Technologies Used
- **AWS SageMaker** for cloud-based training
- **AWS S3** for data storage
- **XGBoost** as the primary machine learning algorithm
- **Pandas & NumPy** for data preprocessing
- **Matplotlib & Seaborn** for exploratory data analysis
- **Git & GitHub** for version control

## Results
The model achieved 58% accuracy using XGBoost, and 64% accuracy using Logistic Regression. 
However, when transitioning to AWS SageMaker, adjustments were necessary and it didn't work out.
