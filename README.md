# Steam Games Analysis with PySpark 🎮

This is a small project I made to play around with the Steam Web API and practice working with PySpark. The idea was to fetch real-time data from Steam, do some light data cleaning, and explore correlations between things like playtime, price, review scores, and more.

Everything runs in a Colab notebook and pulls fresh data each time. I used PySpark for the main processing, and then visualized the results using Seaborn and Matplotlib.

---

## What it does

- Connects to the Steam API and grabs the top 100 most played games
- Pulls info like price, discounts, review stats, and player numbers
- Cleans and joins the data using PySpark
- Analyzes relationships between different variables (e.g. does a higher price mean better reviews?)
- Creates a few visualizations to highlight interesting patterns

---

## Tools used

- **PySpark** – for handling the data
- **Seaborn / Matplotlib** – for plots
- **Steam Web API** – real-time data source
- **Google Colab** – everything runs in the cloud

---

## Visuals

### 🔥 Correlation Heatmap
<img width="938" height="790" alt="image" src="https://github.com/user-attachments/assets/57fbb976-d9c5-4e6b-baaf-3eaaa7a7224b" />


Shows how things like playtime, price, and review scores relate to each other.

---

### ⭐ Review Score vs Price
<img width="846" height="547" alt="image" src="https://github.com/user-attachments/assets/7bd30ba9-a762-46ad-8a76-7ca916de2b04" />



Scatterplot showing whether expensive games are better reviewed. (Short answer: kind of.)

---

### 📅 Positivity Ratio Over Time for Free Games vs Paid
<img width="1189" height="584" alt="image" src="https://github.com/user-attachments/assets/ff461721-7704-4a2e-aff5-55d855e75d36" />
<img width="1190" height="576" alt="image" src="https://github.com/user-attachments/assets/8d5114b8-5134-4b5c-bdea-4bdbf645b0c6" />


Tracks how user sentiment (positivity ratio) changes over time for the top 5 free games and paid games. 
Interesting to see which games maintain good reviews over time — and which ones don’t.

---

### 📊 Review & Sentiment Change for Paid Games
<img width="1389" height="590" alt="image" src="https://github.com/user-attachments/assets/62e34e78-765e-4484-9063-fee46ab26337" />


These histograms show how much review volume (ReviewDelta) and sentiment (SentimentDelta) change over time for paid games.
Helpful to spot spikes, drops, or consistent performance in how games are being received post-launch or after updates.

---

## How to run it

This notebook was built for Google Colab. To run it:

1. Add your Steam API key using the 🔒 **"Secrets"** tab on the left sidebar in Colab
2. Run the cells
3. That's it — it fetches fresh data and runs everything from scratch

There are no API keys stored in the notebook — everything is kept secure using Colab’s built-in secrets manager.

---

## Notes

- The data changes all the time since it’s live from Steam, so your results may vary depending on when you run it
- I limited the dataset to ~100 games to keep it quick and API-friendly
- This project was just for fun and learning — nothing commercial here

---

## Stuff I might add later

- Clustering games by review vs price vs playtime
- Genre-based analysis
- Build a little dashboard (maybe with Streamlit or something else)

---

Let me know if you have any feedback or ideas — happy to improve it! 🎮
