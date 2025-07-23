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

Reasoning Behind Each Weight:

team_experience	(0.15(weight))- A strong founding team with domain experience is crucial for execution and resilience. However, execution must be balanced with other growth signals, hence a moderate weight.

market_size_million_usd	(0.20)-Startups targeting a larger market have higher upside potential. Investors value Total Addressable Market (TAM), so this gets a high weight.

monthly_active_users	(0.20)-	Active user base reflects traction and engagement, which directly signals product-market fit. Startups with growing users are often seen as valuable.

monthly_burn_rate_inr(0.10)-	While burn rate is important for sustainability, a high burn is not always bad if matched with growth. So, it's included but given a lower weight.

funds_raised_inr(0.15)-Fundraising reflects investor confidence, but over-reliance can lead to poor capital efficiency. Hence, a balanced mid-level weight.

valuation_inr(0.20)-Valuation reflects market perception and future potential. It's weighted high, but care should be taken as inflated valuations may not always reflect fundamentals.

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

