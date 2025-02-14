# 🎬 Movie Recommendation System  

## 📌 Overview  
This project implements a **movie recommendation system** using **collaborative filtering** and the **K-Nearest Neighbors (KNN) algorithm**. It analyzes user ratings to suggest similar movies based on preferences.  

**Collaborative Filtering** is used to recommend items by analyzing past interactions (ratings) between users and items (movies). Instead of relying on content-based features like genre or director, it finds patterns in user behavior to suggest similar movies.  

---

## 📂 Dataset  
The project uses the **MovieLens dataset**, which contains two main files:  

1. **movies.csv** – Contains metadata about movies, including:  
   - `movieId`: Unique identifier for each movie.  
   - `title`: Movie title.  
   - `genres`: List of movie genres.  

2. **ratings.csv** – Contains user ratings for movies, including:  
   - `userId`: Unique user identifier.  
   - `movieId`: Movie rated by the user.  
   - `rating`: Rating given by the user (1–5).  
   - `timestamp`: When the rating was given.  

---

## 🛠️ Technologies Used  
| **Technology** | **Usage** |  
|--------------|----------|  
| Python | Core programming language |  
| Pandas | Data manipulation and cleaning |  
| NumPy | Numerical operations |  
| Matplotlib, Seaborn | Data visualization |  
| Scipy (csr_matrix) | Sparse matrix representation |  
| Scikit-learn (KNN) | K-Nearest Neighbors algorithm for recommendations |  

---

## 🚀 Features  
✅ **Loads and processes movie and rating datasets**  
✅ **Handles missing values and cleans data**  
✅ **Uses a sparse matrix for efficient memory usage**  
✅ **Applies the KNN algorithm to find similar movies**  
✅ **Provides personalized recommendations based on user preferences**  
✅ **Visualizes user ratings and similarity scores**  

---

## 📌 Setup & Installation  

### 1️⃣ Install Dependencies  
Ensure you have Python installed. Then, install the required libraries using:  
```bash
pip install pandas numpy scipy scikit-learn matplotlib seaborn
```

### 2️⃣ Clone the Repository  
```bash
git clone https://github.com/rajatgupta3121/Movie_recommendation_system.git
cd Movie_recommendation_system
```

### 3️⃣ Run the Jupyter Notebook  
If you are using Jupyter Notebook:  
```bash
jupyter notebook
```
Then open `Movie_recommendation_system.ipynb` and run the cells step by step.

---

## 🏗️ How It Works  

### **Step 1: Load the Data**  
- Import the datasets (`movies.csv` and `ratings.csv`).  
- Merge both datasets to link movie titles with ratings.  

### **Step 2: Data Preprocessing**  
- Remove unnecessary columns (`timestamp`).  
- Convert the data into a structured format.  
- Handle missing values, if any.  
- Convert user ratings into a **pivot table**.  

### **Step 3: Create a Sparse Matrix**  
- Convert the dataset into a **sparse matrix** using `csr_matrix` from **SciPy**.  
- A sparse matrix optimizes memory usage for large datasets.  

### **Step 4: Apply the KNN Algorithm**  
- Use `NearestNeighbors` from **scikit-learn** to find similar movies.  
- Compute similarity based on the **Euclidean distance**.  

### **Step 5: Generate Movie Recommendations**  
- Pick a target movie.  
- Find its **nearest neighbors** based on user ratings.  
- Recommend movies that are highly rated and similar to the selected movie.  

---

## 📊 Data Visualization  

The project includes **various visualizations** to analyze the dataset:  

📌 **Distribution of Ratings** – Shows how user ratings are distributed.  
📌 **Heatmap of User-Movie Interactions** – Visualizes rating density.  
📌 **Top Movies by Popularity** – Displays the most-rated movies.  

---

## 🎯 Example Usage  

#### **Finding Similar Movies**  
If you want to find similar movies to *"Toy Story (1995)"*, the system will return:  

| **Recommended Movie** | **Similarity Score** |  
|---------------------|------------------|  
| A Bug's Life (1998) | 0.98 |  
| Aladdin (1992) | 0.96 |  
| Monsters, Inc. (2001) | 0.95 |  
| Finding Nemo (2003) | 0.94 |  
| The Lion King (1994) | 0.93 |  

---

## 💡 Future Improvements  

🔹 **Hybrid Recommendation** – Combine collaborative filtering with content-based filtering.  
🔹 **Deep Learning Models** – Implement recommendation using **Neural Networks**.  
🔹 **Real-Time Recommendations** – Deploy the model as a **Flask API**.  
🔹 **User-based Filtering** – Recommend movies based on similar users.  

---

## 🏆 Results & Conclusion  

✔ The recommendation system efficiently finds similar movies using user rating data.  
✔ The KNN algorithm provides accurate recommendations without needing extensive feature engineering.  
✔ The model can be extended for **personalized recommendations** in streaming platforms.  

---

## 📜 License  
This project is open-source and available under the **MIT License**.  

