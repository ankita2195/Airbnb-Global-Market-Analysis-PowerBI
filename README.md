# Airbnb Global Market Analysis | Power BI

**What does Airbnb's global marketplace look like across 10 major cities, and what do listing, pricing, rating and review patterns reveal about it?**

This project explores Airbnb's marketplace across 10 major cities, examining how listings are distributed, where supply is concentrated, how properties are priced, and what review activity and host profiles reveal about the platform.

The analysis covers **279,712 listings, 182,024 hosts and over 1 million review records**, bringing together marketplace, customer experience and host-related insights in a three-page Power BI dashboard.

## 👉 **Live Dashboard:** [View Power BI Dashboard](https://app.fabric.microsoft.com/view?r=eyJrIjoiNTliOGMwZTYtNjE0ZC00MTM5LWJiNjMtOTkwYTM4ODhjYTQ4IiwidCI6ImE1ZmI3ZjgwLTIwNTEtNGE5Ny05YjEyLTZhYjIyMmQyYmQ1NSJ9)


## The Analysis

Rather than looking at listing counts separately, this project examines the marketplace through three perspectives:

- **Global Market Overview:** Listing trends over time, city-level distribution and the contribution of different property types.
- **Market Share & Customer Experience:** City-wise market concentration, room-type pricing and customer ratings across key service dimensions.
- **Review Behaviour & Host Credibility:** Review frequency, monthly review patterns, and the relationship between host profile pictures and identity verification.

## Key Findings

- **Growth trend:** Airbnb's growth peaked around 2015, followed by a slowdown. The trend shows a recovery during 2018-19 before a sharp decline in 2019-20, coinciding with the disruption caused by COVID-19. Increased regulations may have contributed to the earlier slowdown, although the dataset does not establish this as the cause.
- **Market concentration:** Paris, New York and Sydney together account for approximately **48.4% of listings** across the 10 cities analysed.
- **Property preference:** Entire-place listings make up around **65% of the total supply**, making them the dominant accommodation type in this dataset.
- **Customer experience:** The overall average listing rating is **93.41/100**. Accuracy and communication score relatively well, while cleanliness and value have more room for improvement.
- **Review behaviour:** Approximately **99% of reviewers have submitted three or fewer reviews**. One reviewer with 283 reviews stands out as an extreme observation.
- **Seasonal patterns:** Paris and Rome account for a substantial share of review activity during the April-August period, while New York shows a stronger share in November and December.

## Data & Methodology

The analysis uses two datasets:

| Dataset | Records | Fields |
|---|---:|---:|
| Listings | 279,712 | 33 |
| Reviews | 1,048,575 | 4 |
| **Total** | **1,328,287** | **37** |

<img width="1535" height="777" alt="Airbnb Data Model" src="https://github.com/user-attachments/assets/e7ec801a-8ea1-4b0f-ae19-8ad49721ba47" />

The datasets were connected using `listing_id` through a **many-to-one relationship**, with Listings on the one side and Reviews on the many side. Bidirectional cross-filtering was used to support interaction between listing attributes and review activity.

The analytical work included:
- DAX measures for listing counts, city rankings, cumulative market share, average pricing and ratings.
- Reviewer-level review frequency calculations to understand how often customers leave reviews.
- Cumulative distribution analysis to identify how review activity is concentrated.
- Interactive filtering across cities and other marketplace attributes.

## Tools Used

**Power BI, DAX, Data Modelling, Business Analysis**

## Important Data Considerations

- The available `host_since` field records when a host joined Airbnb, not when an individual listing was created. It is therefore treated as a host-tenure proxy rather than an exact listing creation date.
- Prices are recorded in local currencies. Direct price comparisons across countries should therefore be interpreted with caution.
- Review scores represent listing-level averages; the dataset does not contain individual review text or individual review scores.

## Dashboard

The Power BI dashboard is organised into three pages, moving from the global marketplace overview to customer experience and review behaviour.

#### Page 1: Overview
<img width="856" height="732" alt="image" src="https://github.com/user-attachments/assets/9f577c5e-20b8-473e-93d5-7f2dddd292ac" />

#### Page 2: Ratings
<img width="856" height="732" alt="image" src="https://github.com/user-attachments/assets/68653a31-e5ee-4fb3-813e-dc64c16a6ae1" />

#### Page 3: Reviews
<img width="856" height="732" alt="image" src="https://github.com/user-attachments/assets/4d94b4b5-5a28-44d2-8ee8-d0267f4b0abd" />
