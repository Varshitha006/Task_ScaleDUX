# Task_ScaleDUX
Startup Scoring and Clustering:(https://startupscorecaluculator-3igezacnwdpaxf2v7fkas3.streamlit.app/)

This project evaluates and clusters startups based on multiple performance indicators using a custom scoring system and unsupervised machine learning (KMeans). The goal is to assist incubators or investors in identifying and categorizing startups for funding or mentorship.

📊 Dataset
The dataset includes the following columns:

team_experience

market_size_million_usd

monthly_active_users

monthly_burn_rate_inr

funds_raised_inr

valuation_inr

🧮 Scoring Logic:

Each startup is given a Startup Score (0–100) based on the weighted contribution of six metrics.

🔢 Feature Weights

Feature	Weight

Team Experience	15%

Market Size	20%

Monthly Active Users	20%

Monthly Burn Rate (lower is better)	10%

Funds Raised	15%

Valuation	20%

Note: The monthly_burn_rate_inr was negated to reward startups with lower burn.

🤖 Clustering with KMeans:

We used KMeans Clustering (unsupervised learning) to group startups into 4 meaningful segments based on:

Normalized performance features

Startup score


🧠 Cluster Interpretation
Based on the cluster centroids, we manually assigned meaningful labels to the clusters:


0	(Cluster ID) - High traction, well-funded startups(Label)

1 -	Early stage, low burn

2	-Rapid growth but high burn

3	-Low funding, low valuation niche startups

