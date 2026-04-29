## Netflix Content Strategy Analysis
This project analyzes Netflix's content catalog to uncover trends in content growth, genre distribution, geographical expansion, and viewing patterns. 

The objective is to derive insights that can support data-driven content strategy decisions, such as what type of content to produce, where to expand, and how to align with audience consumption behavior. 

## Problem Statement
With increasing competition in the streaming industry, understanding content trends is critical for strategic decision-making.

This project aims to answer:
 -  What type of content is Netflix focusing on over time?
 - How has content growth evolved over time?
 - Which genres and countries dominate the platform?
 - What content characteristics align with viewer consumption patterns?

These insights can help guide future content production and acquisition strategies.

## Dataset
- Source: Netflix Movies and TV Shows dataset (Kaggle)
- Records: ~8,800 titles
- Features include:
    - Type (Movie / TV Show)
    - Genre
    - Country
    - Release Year
    - Date Added
    - Duration

# Data Challenges
- Missing values (director, cast, country)
- Multi-value categorical columns (genres, cast)
- Mixed formats in duration (minutes vs seasons)
- Inconsistent date formats

## Data Cleaning & Preprocessing
Key steps performed:
- Handled missing values by imputing or labeling as 'Unknown'
- Converted ```date_added``` to datetime format
- Extracted new features:
    - ```year_added```
    - ```month_added```
    - ```primary_genre```
    - ```content_age```
- Standardized duration into numeric format (```duration_value```)
- Created bins for analyzing movie duration distribution

# Tools & Technologies
- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Power BI (Dashboard & Visualization)
- Jupyter Notebook

# Key Insights
 - Content additions surged significantly after 2016, peaking around 2019, followed by a decline. 
 - TV Shows have grown at a faster rate than Movies, indicating a shift toward binge-driven engagement.
 - Drama dominates the catalog, with strong contributions from Comedy and Action genres. 
 - The majority of movies fall within the 80-120 minute range, aligning with standard viewer attention spans. 
 - The United States leads content production, with emerging contributions from India and the UK. 

# Business Recommendations
 - Increase investment in TV Shows, especially in high-engagement genres like Crime and Thriller. 
 - Expand content production in emerging markets such as India. 
 - Maintain optimal movie durations (~90-110 minutes) to match viewer preferences. 
 - Focus on serialized content formats to improve user retention and platform engagement. 

# Dashboard Preview
![Dashboard](visuals/Dashboard.png)

# Project Structure
```
netflix-content-analysis/
├── data/
│ ├── raw/
│ ├── cleaned/
├── notebooks/
│ ├── 01_data_cleaning.ipynb
│ ├── 02_analysis.ipynb
├── powerbi/
│ ├── netflix_dashboard.pbix
├── screenshots/
│ ├── dashboard.png
├── README.md
├── requirements.txt
```