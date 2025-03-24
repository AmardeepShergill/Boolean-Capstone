# Boolean-Capstone
A project using SQL and Tableau to analyse a given data set

Behind the Look: Decoding Sales, Customers, and Inventory
Executive Summary
Welcome to a comprehensive analysis of sales performance, customer demographics, product
performance, and inventory management for our e-commerce business. This report distills the
key insights and metrics that will guide the company toward optimizing its operations. Our
analysis uncovers critical data points, highlighting opportunities for growth and improvement,
particularly in inventory management and targeted marketing. We aim to shift the company’s
focus from simply asking “what is happening?” to understanding “why” these trends are
emerging and how they can be leveraged for future success.

Assumptions and Key Questions
The analysis was conducted under the following assumptions, which shaped our exploration:

# Sales and Website Activity
- Which parts of the website attract the most visitors, and where is the traffic originating from (email, direct, organic)?
- How does traffic correlate with sales, and which sources drive higher conversion rates?
  
# Customer Demographics and Behavior
- What are the key demographic profiles (age, gender, location) of our customers?
- Are there loyalty patterns tied to specific demographics or purchase frequency?
  
# Product Performance
- What is the relationship between category pricing, profit margins, and overall sales?
- Which categories have the highest repeat purchase rates, and what patterns emerge in customer loyalty?
  
# Inventory and Distribution
- Are stock shortages impacting sales? How do inventory levels at European distribution centers affect product availability?
- Are certain distribution centers facing challenges leading to delays or missed sales?

Methodology
- Data Collection: Data was extracted from the BigQuery dataset ‘thelook_ecommerce’,focusing on tables like events, users, products, orders, order_items, inventory_items, and distribution_centres.
- Data Cleaning: Missing values were handled, duplicates removed, and key variables such as dates, prices, and product identifiers were standardized for analysis.
- Tools Used: We utilized SQL for querying, Python for data manipulation, and Tableau for visualizations to drive interactive insights.

# Key Insights and Results
Website Activity
- Analysis Method: We focused on the events table, grouping by event type and traffic source. This allowed us to understand which traffic channels contributed the most to driving customers toward making purchases.
- Cart Events: Cart events were a critical focus of our analysis, as these reflect a strong intent to purchase. We grouped cart events by traffic source (organic, email, direct) to gauge how different channels influence purchase behavior.
- Effectiveness of Channels: To determine how effective each channel was in guiding users toward purchase, we divided the number of cart events by the total number of events from each traffic source. This gave us a percentage indicating the channel's effectiveness.
  - Metric: Organic traffic had the highest conversion rate, while email traffic contributed more volume but converted at a lower rate.

Recommendation: Although organic traffic represents the lowest volume, it converts at a much higher rate. To capitalize on this, we recommend collaborating with influencers on platforms like YouTube to create authentic, recommendation-based content that drives traffic organically.

# Customer Demographics and Behavior
- Age & Gender Distribution: Our analysis shows that the average customer age is 49.4 years, with a nearly even split between male and female customers (50.1% female, 49.9% male).
- Geographic Distribution: Customers come from 16 countries, with the highest concentrations in the US, China, and European nations. This reflects a global customer base but indicates that region-specific marketing may unlock further potential.

High-Value Segments: 
Middle-aged customers (40-49 years old) represent the largest segment with the highest purchasing power and loyalty. This segment should be a prime target for marketing campaigns.

Recommendation: Implement personalized marketing strategies targeting middle-aged customers, emphasizing their loyalty and purchasing power. Also, expand marketing efforts in growth regions like China and Brazil, where sales show potential for growth.

#  Product Performance
1. Top-Performing Product Categories (Regional data)
Outerwear & Coats and Jeans are the top-performing categories across both total sales and revenue. These categories dominate particularly in China and the United States.

Revenue from China:
- Outerwear & Coats generated $449,517 from 3,081 sales.
- Jeans generated $435,888 from 4,460 sales.
 Revenue from U.S.:
- Outerwear & Coats ranks third in the U.S., generating $291,008 in revenue.
Sweaters (China) also performed strongly, generating $286,384 from 3,875 sales.

Implications:
- Outerwear & Coats and Jeans should be prioritized for inventory management and marketing efforts, especially in China and the U.S.
- Sweaters in China also represent a significant market and can be further promoted to drive revenue.
  
2. Top Categories by Region (Regional data)
- China: Prefers Outerwear & Coats, Jeans, and Sweaters.
- United States: While Outerwear & Coats and Jeans remain strong, categories like Plus Size and Activewear are growing in demand.
Implications:
Marketing strategies should be tailored to regional preferences. For example, Outerwear & Coats can be promoted more aggressively in the U.S. and China, while Plus Size products should be more targeted toward U.S. customers.

3. Categories with the Highest Revenue Growth
- Plus Size (U.S.) saw an 83.16% revenue growth in May 2020.
- Leggings (France) experienced 73.78% growth in January 2024.
- Activewear (South Korea) achieved 63.76% growth in October 2020.
- Intimates (Germany) saw a 63.69% increase in December 2021.
 
Implications:
Plus Size and Leggings are key growth categories in their respective regions, suggesting opportunities for product expansion and targeted marketing campaigns.
Activewear and Intimates are growing categories that should be monitored closely for future promotion expansions.

4. Underperforming Categories
- Clothing Sets: Generated the lowest revenue of $17,576 from 213 sales.
- Jumpsuits & Rompers: Earned $39,774 from 934 sales.
- Suits: Despite $117,377 in revenue, this category underperformed with only 1,024 sales.
-Skirts and Leggings: Generated $115,618 and $84,396 in revenue, respectively, despite higher sales volumes.

Implications:
- Clothing Sets and Jumpsuits & Rompers may need reevaluation or stronger marketing efforts to boost sales.
- Suits may require adjustments in pricing or product offerings to become more competitive.
- Although Leggings have higher sales volume, revenue remains low. A potential price increase or introduction of premium products could improve profitability.

5. Gender-Based Insights
- Intimates and Leggings is a clear favorite for female customers, while categories like Suits and Outerwear see higher male customer engagement.
Implications:
- Tailored marketing strategies based on gender-specific preferences could increase sales and loyalty.
- Targeted promotions for female customers in Intimates and Leggings, and for male customers in Suits and Outerwear, could drive improved sales performance.

6. Seasonality and Trends
Certain categories display strong seasonality trends these include:
- Plus Size (U.S.) with 83.16% and Activewear (South Korea) with 63.76%, showed significant growth during peak months respectively in May and October 2020.
- Leggings (France) performed well in January 2024, indicating fitness-related products might peak early in the year with a 73.78% increase in revenue.

Implications:
- Inventory and marketing campaigns should be adjusted to account for seasonal demand spikes. Stock levels should be increased ahead of peak months, like January for fitness products and May for Plus Size apparel.

Inventory and Distribution
Low Stock Items:
- Product ID 755 (Intimates) had 50% of its stock sold within 48 hours
- Product IDs 9482 (Socks & Hosiery), 11668 (Intimates), and 15723 (Plus-size) were down to only 4 items in stock. #

Implications:
These stock levels indicate strong demand for these products. These shortages could negatively affect sales, especially as
they are concentrated in the Houston, TX distribution center, raising concerns about whether this is a location-specific issue or if the items ordered from this location are consistently popular.

Cancellations: 
The average cancellation rate across all items was 13.8%, which is significantly lower than the industry average of 36.34%. This suggests strong customer satisfaction. Additionally, Product ID 9464 was canceled 100% of the time, but since thisrefers to just one order, the sample size is too small to draw further insights.

Returns:
The return rate was 11.80%, with 59 out of 500 orders being returned. This compares favorably to the industry average of 17.6% for 2023, showing that our return rate is below the market average. Combined with cancellations, the total rate of returned or canceled orders stands at 25.6%, still below the industry standard.

Delivery Times: The data reflects delivery times of 1 day per item, though it’s likely that this doesn’t align with real-world conditions due to potential data inaccuracies.

# References:
Jingyi Ye, 2021, University of California, USA. "Industry Average Cancellations: 36.34%".
National Retail Federation, 2023. "Industry Average Returns: 17.6%".

Recommendation: 
Implement real-time inventory tracking, particularly in the Houston center, to better anticipate demand and avoid stockouts. Additionally, improve the distribution process to ensure that popular items are more evenly distributed across
regions, reducing the likelihood of bottlenecks in one location.

# Conclusion & Recommendations
Obstacles:
 Data Gaps: One of the key obstacles we encountered was related to the fact that the  data used in this analysis was generated and did not reflect real-world conditions. This particularly impacted pricing data, which may not align with actual market conditions.

Predictive Analysis Issues: As mentioned, our predictive model did not yield reliable results due to a combination of missing data, lack of optimal parameter testing, and no validation process. This issue should be revisited if more reliable, real-world data becomes available.

Inventory Optimization

Address stock shortages, particularly in European distribution centers, by implementing real-time inventory tracking and predictive restocking models to avoid missed sales opportunities.

Marketing Strategy
Tailor marketing efforts to high-performing categories like Outerwear & Coats, Jeans, and Plus Size, focusing on key regions like China and the U.S. Consider gender and regional preferences when crafting campaigns.

Traffic Optimization
Leverage organic traffic through influencer collaborations, particularly on platforms like YouTube, to amplify conversion rates by mimicking the authenticity of human recommendations. 

Product Strategy
Focus product expansion efforts on categories showing the highest revenue growth, such as Plus Size, Leggings, Activewear, and Intimates. Address underperforming categories like Clothing Sets and Suits by either improving marketing efforts or considering productadjustments.

Team Involvement
This project was completed by the following team members:
Amardeep 
Bartholomew 
Rebecca 
Sabona



Conclusion
This report highlights the key areas where the company can improve its operations based on a  thorough analysis of sales, customer demographics, product performance, and inventory management. By implementing the recommendations provided, the company can capitalize on growth opportunities, optimize its product offerings, and ensure smoother inventory management across its distribution centers.
