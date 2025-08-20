# 🎬 TMDB Movie Data & Job Market Analysis

This project combines **movie data extraction** from The Movie Database (TMDB) with a lightweight **job market exploration**, using web requests + HTML parsing to build a structured dataset for analysis.  
Developed for the **Foundations of Information** course (University of Arizona).

---

## 🎯 Objectives
- Collect **movie metadata** (title, rating, genres, cast) from TMDB.
- Demonstrate **web scraping techniques** (requests + BeautifulSoup) with respectful headers.
- Clean and merge multi-page results into a single dataset for analysis.
- Explore **job market trends** (separate notebook/report) as an applied information exercise.

---

## 🗂️ Project Structure
```
TMDB-movie-data-and-Job-Market-Analysis/
│── Foundation_of_Information_Project_1_Solution_tmdb_data.ipynb   # TMDB scraping walkthrough
│── Foundation of Information Part B.ipynb                          # Multi-page scrape + data merge
│── Foundation of Information - PART B.html                         # Rendered output of Part B
│── combined_movie_data.csv                                         # Consolidated movie dataset
│── page_1.csv ... page_5.csv                                       # Intermediate page exports
│── Job Market Analysis.pdf                                         # Separate report (job trends)
│── README.md                                                       # Project overview (this file)
```

---

## ⚙️ Tools & Libraries
- **Python**: `requests`, `BeautifulSoup`, `pandas`
- **Jupyter Notebook** (reproducible walkthroughs)
- **Outputs**: CSVs for analysis and an accompanying PDF for job market notes

---

## 🔍 Methods
1. **HTTP Requests** — send GET requests with a user-agent header to TMDB listings
2. **HTML Parsing** — parse page structure with **BeautifulSoup** to extract movie fields:
   - Title
   - Rating / vote average
   - Genres (list)
   - Cast (principal actors)
3. **Pagination & Merging** — collect multiple pages (e.g., `page_1.csv` … `page_5.csv`) and **concat** into `combined_movie_data.csv`
4. **Cleaning** — normalize data types (rating → numeric), standardize genre lists, strip HTML artifacts

---

## 📈 Example Schema (`combined_movie_data.csv`)
| Title | Rating | Genres | Cast |
|------|--------:|--------|------|
| Barbie | 74.0 | ['Comedy','Adventure','Fantasy'] | ['Margot Robbie','Ryan Gosling', ...] |
| Spider-Man: Across the Spider-Verse | 85.0 | ['Animation','Action','Adventure'] | ['Shameik Moore','Hailee Steinfeld', ...] |

> Current dataset includes sample titles such as **Elemental**, **Heart of Stone**, **Spider-Man: Across the Spider-Verse**, **Transformers: Rise of the Beasts**, and **Barbie**.

---

## 🚀 How to Run
1. Install dependencies:
   ```bash
   pip install requests beautifulsoup4 pandas
   ```
2. Open the notebooks in Jupyter and run cells to (re)create intermediate CSVs:
   - `Foundation_of_Information_Project_1_Solution_tmdb_data.ipynb`
   - `Foundation of Information Part B.ipynb`
3. Use `combined_movie_data.csv` for analysis or visualization in your tool of choice.

---

## 🧭 Notes on Ethics & Terms
- Use **polite headers** and **respect robots.txt** and site **Terms of Service**.
- Avoid high-frequency scraping; **cache** pages when possible.
- This dataset is for **educational purposes** only.

---

## 👩‍💻 Author
**Rohit Surya** — Data collection, HTML parsing, dataset curation, report development

---

## 📌 License
Academic use only (Foundations of Information, University of Arizona).
