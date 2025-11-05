# match_maker

# 💘 OKCupid Smart Match Finder

A data analysis and machine learning project that finds **the most similar matches between male and female profiles** based on features like age, height, income, and job.

---

## 🧠 Project Idea
The goal of this project is to build a simple system that finds **the best matches** between male and female users from the OKCupid dataset, using numerical and categorical profile attributes.

Using feature encoding and cosine similarity, the model identifies pairs with the highest similarity scores.

---

## ⚙️ Technologies Used
- **Python 3.10+**
- **Pandas** – data processing  
- **NumPy** – numerical operations  
- **Matplotlib** – visualization  
- **scikit-learn** – preprocessing and similarity computation  
- **PyTorch** – GPU support and future deep learning extensions  

---

## 🧩 Main Steps

1. **Data Cleaning**
   - Fill missing numeric values with median.
   - Replace missing categorical values with `"Unknown"`.
   - Combine all essay columns into one column (`essay_text`).

2. **Feature Engineering**
   - Frequency encoding for high-cardinality categorical features (e.g., job, religion, ethnicity).
   - One-hot encoding for low-cardinality features.
   - Standard scaling for numeric features: `age`, `height`, `income`.

3. **Similarity Computation**
   - Split data into `df_male` and `df_female` based on gender.
   - Compute a cosine similarity matrix between male and female profiles.
   - For each man, retrieve the top-K most similar women.

4. **Result Display**
   - Custom function `show_matches_for_man(man_id, top_k)` prints:
     - Man’s real attributes (age, job)
     - Top K most similar women with similarity scores

---

## 🧮 Example Output

👨‍🦱 Man 0 | Age: 32 | Job: transportation

❤️ Woman 4394 | Age: 29 | Job: clerical / administrative | Similarity: 0.994

❤️ Woman 56095 | Age: 27 | Job: student | Similarity: 0.993

❤️ Woman 25852 | Age: 30 | Job: medicine / health | Similarity: 0.993

⚠️ Note:
This project uses the OKCupid dataset
 for research and educational purposes only.
The dataset itself is not included in this repository for privacy reasons.
