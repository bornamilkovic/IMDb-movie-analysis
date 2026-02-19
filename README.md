# IMDB-movie-analysis
Exploratory data analysis (EDA) of an IMDb movie dataset, focusing on factors associated with IMDb score and simple predictive modeling.

## Summary
- Dataset: 5043 movies with 28 variables (latest entries up to 2016).
- Cleaning: converted empty strings to missing values, inspected missingness (most missing: `gross`, `budget`, `aspect_ratio`), and removed duplicate movie titles.
- Ratings: IMDb scores range roughly 1.6–9.5 with a median around 6.6.
- Budget & rating: very weak relationship between budget and IMDb score (near-zero correlation).
- Gross & rating: still weak, but higher than budget (small positive correlation).
- Budget & gross: clear positive association after log transform; a simple linear model explains about ~35% of variance in log(gross).
- Popularity: number of user votes correlates moderately with rating, and the relationship strengthens for frequently-rated movies (>100k votes).
- Time trend: median ratings trend lower for newer releases.
- Genres: documentaries/biographies/history/war tend to have higher average scores; horror tends to be associated with lower scores.
- Modeling: a multiple linear regression achieves ~0.57 adjusted R²; multicollinearity checks show no major issues (VIF values low) and residual diagnostics are acceptable.

## Report
- 📄 Full report (Croatian): [IMDb_filmovi.pdf](IMDb_filmovi.pdf)
- 📓 R Markdown: [Rmd/IMDb_filmovi.rmd](Rmd/IMDb_filmovi.rmd)

## Reproduce
1. Open `Rmd/IMDb_filmovi.rmd` in RStudio
2. Install required packages (if missing)
3. Knit to PDF/HTML

## Project structure
- `Rmd/` – analysis source (R Markdown)
- `IMDb_filmovi.pdf` – rendered report
- `figures/` – exported plots for embedding in README

---

## 📜 Disclaimer
Created as part of the course **Statistical Programming Fundamentals** at the Faculty of Electrical Engineering and Computing (FER), University of Zagreb (2026).  
Code is intended for educational purposes.

## 📄 License
MIT License.
