# Social Media Performance Analysis
## Project Objective
The objective of this project is to build a report that examines how platform, content category, post format, and posting time influence engagement performance, with the aim of providing actionable insights and recommendations for the Marketing team to implement content campaigns across various social media platforms.
## Business Context
As a data analyst for a global IT company, your role is to analyze content performance across multiple social media platforms. The Marketing Manager wants to launch content campaigns on various platforms and needs insights on how to maximize engagement rates on each platform. You will be provided with a dataset for 2024, recording detailed performance metrics at the post level, including platform information, content type, and geographic reach.
### Dataset Overview
The dataset, provided by Onyx. It includes metadata such as post type (video, carousel image, text), content category (product promotion, education, entertainment), posting time, and hashtags used. Additionally, the dataset tracks performance metrics such as engagement rate, views, impressions, clicks, CTR, and geographic reach across various countries and regions.

The dataset contains **5,600 rows** and **24 columns**, covering multiple social media platforms and content performance metrics such as engagement, views, likes, shares, comments, impressions, clicks, engagement rate, posting date, posting hour, and engagement level.
##### The platforms included are:
- Facebook
- Instagram
- TikTok
- X.com
- YouTube
- LinkedIn
##### A data quality check was conducted before analysis. The dataset had:
- No duplicate rows
- No missing values in the main analytical variables used for the study
- Missing values mainly in `Clicks` and `Click_Through_Rate`, so these were not the focus of the main analysis
## Methods Used
##### The analysis was conducted in **Python** using:
- `pandas` for data cleaning and manipulation
- `numpy` for numerical operations
- `matplotlib.pyplot` and `seaborn` for data visualization
##### Main analytical steps:
1. Data loading and quality checking
2. Selecting key variables for analysis: Platform, Content_Type, Content_Category, Post_Type, Engagement_Rate, Post_Date, Post_Hour, Engagement_Level
4. Feature engineering from posting date:
   - Day of week
   - Day name
   - Weekend indicator
5. Grouping and aggregating engagement rate by:
   - Platform
   - Content category
   - Post type
   - Posting day and hour
6. Visualization using boxplots, bar charts, and a heatmap

## Statistical Validation
A one-way ANOVA test was conducted to examine whether engagement rates differ across platforms. The results showed a statistically significant difference (F = 5.54, p < 0.001).

Post-hoc Tukey HSD analysis indicated that:
- **LinkedIn had significantly lower engagement rates** compared to Instagram, TikTok, X.com, and YouTube
- **Instagram performed significantly better than YouTube**
- Most other platform comparisons were not statistically significant

This suggests that the overall difference in engagement performance is **primarily driven by LinkedIn’s lower performance**, rather than consistent differences across all platforms.

## Key Findings
#### 1. Platform performance
Among all platforms, **Instagram** had the highest average engagement rate, followed closely by **TikTok**, **Facebook**, and **X.com**. **LinkedIn** showed the lowest average engagement rate.

#### 2. Best content categories
The content categories with the strongest engagement were: **Educational** and **Customer Story**. These categories consistently outperformed Product Promotion, Entertainment, and Event/Webinar content.

#### 3. Best content category by platform
- **Facebook:** Educational
- **Instagram:** Educational
- **LinkedIn:** Customer Story
- **TikTok:** Customer Story
- **X.com:** Customer Story
- **YouTube:** Customer Story

This suggests that informative and story-driven content performed better than purely promotional content across most platforms.

#### 4. Best post type by platform
- **Facebook:** Video
- **Instagram:** Image
- **LinkedIn:** Image
- **TikTok:** Video
- **X.com:** Text
- **YouTube:** Video

This indicates that each platform has its own preferred content format, and content strategy should be adapted accordingly.

#### 5. Best posting times
The heatmap analysis showed that the highest success rates for high-engagement posts appeared in:
- Monday at 18:00
- Tuesday at 14:00
- Tuesday at 13:00
- Wednesday at 14:00
- Thursday at 18:00
- Saturday at 19:00

In general, **midday (around lunch break)** and **early evening** tended to generate stronger engagement than early morning slots. This pattern is consistent with higher user activity during breaks and after working hours.
## Business Recommendations
#### Based on the findings, the following actions are recommended:
- Prioritize **Instagram** and **TikTok** when the objective is to maximize engagement.
- Increase the share of **Educational** and **Customer Story** content in the content calendar.
- Match post format to platform preference:
  - Use **videos** for TikTok, Facebook, and YouTube
  - Use **images** for Instagram and LinkedIn
  - Use **text posts** for X.com
- Focus posting activity on two key time windows: **midday (13:00–14:00)** and **early evening (18:00–19:00)**.
- Reduce the proportion of purely promotional content and reallocate more content toward higher-performing categories, particularly **Educational** and **Customer Story**.
## Limitations
- The analysis is descriptive and does not establish causal relationships.
- The dataset does not include conversion or revenue metrics, so recommendations are based on engagement performance only.
- Missing values in click-related variables limited deeper analysis of traffic-driving effectiveness.
- Findings are specific to this dataset and should be validated through live content testing.
## Conclusion
This analysis shows that social media performance is shaped not only by platform choice, but also by content category, post format, and posting time. The findings suggest that engagement can be improved through a more targeted content strategy that aligns platform selection, content format, and posting schedule with audience behaviour. Overall, the results provide practical guidance for making more effective and data-driven social media marketing decisions.
