
# 🎬 Movie Recommender System

A **content-based movie recommender system** built with **Streamlit** and powered by **The Movie Database (TMDb) API**. It recommends similar movies based on a selected movie, displaying both the movie titles and their posters.

---

## 📌 Features

- Recommends **5 movies** similar to the one selected.
- Uses **cosine similarity** for recommendation logic.
- Fetches **movie posters** via the TMDb API.
- Built with an interactive **Streamlit UI**.
- Uses **pickled data** for fast loading (`movies.pkl`, `similarity.pkl`).

---

## 🛠️ Tech Stack

- **Python 3**
- **Streamlit** for front-end
- **Pandas** for data manipulation
- **scikit-learn** for similarity matrix
- **Pickle** for serialized model/data
- **TMDb API** for movie posters

---

## 🚀 How to Run the App

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/movie-recommender
   cd movie-recommender
   ```

2. **Install Dependencies**
   Make sure you have Python 3 and install required packages:
   ```bash
   pip install -r requirements.txt
   ```

   Example `requirements.txt`:
   ```
   streamlit
   pandas
   scikit-learn
   requests
   ```

3. **Place the Required Files**
   - `movies.pkl`: Preprocessed movie metadata (title, movie_id)
   - `similarity.pkl`: Cosine similarity matrix
   - `app.py`: Streamlit application file

4. **Run the App**
   ```bash
   streamlit run app.py
   ```

---

## 🧠 How It Works

- A movie is selected from a dropdown menu.
- The app retrieves its index in the dataset.
- It uses the cosine similarity matrix to find the top 5 most similar movies.
- Movie posters are fetched from the **TMDb API** using the corresponding `movie_id`.

---

## 📦 File Structure

```
├── app.py                # Main Streamlit app
├── movies.pkl            # Movie metadata
├── similarity.pkl        # Similarity matrix
├── Movie_Recommender.ipynb  # Notebook for preprocessing/training
├── README.md             # Project documentation
```

---

## 🔐 API Key

This app uses the **TMDb API** to fetch posters. Make sure to replace the `api_key` in `fetch_poster()` with your own key:
```python
url = f"https://api.themoviedb.org/3/movie/{{movie_id}}?api_key=YOUR_API_KEY&language=en-US"
```

---

## ✨ Sample Output

When you select a movie, you will see 5 recommended movies with their posters displayed in columns side-by-side.

---

## 🙌 Acknowledgements

- [The Movie Database (TMDb)](https://www.themoviedb.org/)
- [Streamlit](https://streamlit.io/)
- [scikit-learn](https://scikit-learn.org/)
