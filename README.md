# PhishGuard ML: Detecting Malicious Links with Data Science

This project is a deep dive into how we can use Machine Learning to identify phishing links and spam before they reach a user's inbox. I built this to understand the intersection of Cybersecurity and Data Science.

## 🔍 The Workflow

### 1. Data Exploration & Cleaning
I started with a raw dataset of over 10,000 URLs. Using **Pandas**, I performed an initial "Health Check" on the data:
- **Exploration:** Used `df.info()` and `df.describe()` to understand the features (like URL length, number of dots, and special symbols).
- **Cleaning:** Handled missing values (NaN) and ensured the data was consistent for the model.
- **Visualization:** Used **Matplotlib** and **Seaborn** to create scatter plots and histograms to see how "Path Length" and "Subdomain Levels" correlate with malicious links.

### 2. The Machine Learning Model
Once the data was clean, I moved to the detection phase:
- **Vectorization:** Used `TfidfVectorizer` to convert text-based URLs into a numerical format the computer can understand.
- **The Brain:** I implemented the **Multinomial Naive Bayes (MultinomialNB)** algorithm from **Scikit-Learn**. 
- **The Result:** The model achieved an impressive **96.6% accuracy** in distinguishing between "Ham" (safe) and "Spam" (malicious) messages.

## 📊 Visualizing the Results
I believe data should be easy to read. I used **Matplotlib** to generate:
- **Dataset Distribution:** A pie chart showing the split between safe and malicious samples.
- **Confidence Metrics:** Bar graphs to visualize how certain the model is about its predictions.

## 💡 Key Learning
This project taught me that "Clean Data > Fancy Models." Spending time in the cleaning phase (the first 4 photos of my process) was what allowed the model to reach such high accuracy.

---
*Developed as part of my focus on applying AI/ML to modern cybersecurity challenges.*
