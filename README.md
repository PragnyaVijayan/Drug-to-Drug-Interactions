# Drug Interaction Database and Visualization

## Project Overview
This project aims to create a comprehensive database of drug interactions using web scraping techniques from Drugs.com. The goal was to develop a tool that provides insights into which drugs interact with each other, visualized through graphs and accessible via a simple user interface.

## Contributors
• Pragnya Vijayan
• Ena Nayak

# Implementation Details

## Web Scraping
We utilized web scraping to gather data from Drugs.com. The website structure involved selecting drug names alphabetically and parsing through individual drug interaction pages. We used BeautifulSoup for HTML parsing and wrote functions like extract_drug_link to handle various formats of interaction data.

## Data Preprocessing
• Each drug interaction was stored in JSON files categorized by letter pairs (e.g., "aa.json", "ab.json").
• We extracted relevant data and cleaned up extraneous information using regular expressions (get_drug_names) to simplify drug names for analysis.

## Database and Analysis
• We constructed a pandas dataframe from the cleaned data, focusing on drugs and their interactions.
• Interaction frequencies were analyzed and visualized using histograms to understand the distribution of interactions across drugs.

## Drug Clustering and Classification
• We attempted clustering using cosine similarity matrices and K-Means to group drugs based on interaction patterns. The elbow method helped determine optimal cluster numbers.

## Graph Visualization
• We employed Networkx to create interactive graphs displaying drug interactions. Users can input a drug name to visualize its interactions as a subgraph, enhancing usability and clarity.

# Results and Analysis
## Findings
• Over 3000 drugs were found to interact with varying numbers of other drugs, highlighting the complexity of drug interactions.
• Clustering revealed some identifiable groups, though refinements are needed for more precise classifications.
## Interactive Interface
• Users can input a drug name to retrieve its interactions and view a subgraph focused on relevant drug interactions.

# Issues and future plans

## Challenges
• Initially planned to scrape WebMD but faced a 403 error due to scraping restrictions.
• Varying formats of interaction pages required adaptation in scraping methods.
• Imperfect scraping led to irrelevant data inclusion, affecting graph clarity.

## Adaptations
• Changed approach from using the Apriori algorithm to visual graph outputs for better representation of drug interactions.

## Potential Enhancements
• Incorporate drug classification systems (e.g., ATC, USP) to provide deeper insights into drug interaction patterns.
• Refine clustering algorithms to better categorize drugs based on interaction behaviors.
• Address data precision issues in scraping to improve graph quality and accuracy.
