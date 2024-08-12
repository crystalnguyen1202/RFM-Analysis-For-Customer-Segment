# RFM-Analysis-For-Customer-Segment
I used the RFM model and Python to group customers, thus providing the right solutions and suggestions to develop the right customer development strategy.
# Situation
A global retail company have a lot of customers. At the end of the year, the marketing department wants to run marketing campaigns to thank customers who have supported the company over the years. As well as exploiting potential customers to become loyal customers. However, the marketing department has not been able to group each customer this year because the data set is so large that it cannot be hand-processed as in previous years, so use the data analysis department to support the implementation of a segment classification of each customer to implement each marketing program to suit each customer group.
# Task
I grouped clients using the RFM model, which allowed me to offer the appropriate solutions and recommendations for creating the best customer development plan.
When I completed my project, I made use of the following resources and methods:
NumPy and Pandas libraries for Python data manipulation
For data visualization, use the Seaborn and Matplotlib libraries.
# Action
Overview
RFM analysis is a customer segmentation technique used in marketing to analyze and understand customer behavior. RFM stands for:

R – Recency: How recently a customer has made a purchase.

F – Frequency: How often a customer makes purchases.

M – Monetary Value: The total monetary value of a customer’s purchases.

The key idea behind RFM analysis is that customers who have recently made large, frequent purchases are more valuable than those who haven’t. By analyzing these three metrics, businesses can segment their customer base and develop targeted marketing strategies.

RFM analysis is a powerful tool for understanding and leveraging customer behavior, as it allows businesses to identify their most valuable customers and develop more effective marketing campaigns.
Analysis

![Screenshot 2024-08-12 134600](https://github.com/user-attachments/assets/96e39cbc-a189-449a-98f8-5a34c2cefb55)

Let’s take a look at the general information of the dataset:

![Screenshot 2024-08-12 134828](https://github.com/user-attachments/assets/8e57e8cf-3e50-4452-96eb-a73f2d936bf7)

After having an overview of the dataset, I noticed that the customerID is having the wrong data type and the UnitPrice has a minimum value that is negative. Therefore, I have filtered the data as follows:

![Screenshot 2024-08-12 134912](https://github.com/user-attachments/assets/eb0806bc-797f-42f4-a575-53b7ec14ba29)

Next, I calculated the RFM metrics. Based on the date information in the dataset, I have chosen the current date to be calculated as 31/12/2011.

![Screenshot 2024-08-12 135059](https://github.com/user-attachments/assets/d48f6964-7839-44bc-8e78-114679f21d8c)

Then I assigned quintiles for each RFM score. It is preferable for both frequency and monetary value if the value is high. A low recency value is seen as preferable.

![Screenshot 2024-08-12 135139](https://github.com/user-attachments/assets/34d345f2-9387-445d-a2bb-bad3ef6d60e8)

Based on the RFM score value, I divided the client base into a smaller number of identified parts.

![Screenshot 2024-08-12 135218](https://github.com/user-attachments/assets/c2a1f2b5-74cd-4bef-90aa-49299faa1848)

I have combined the 2 tables RFM and segment_score together to produce the final result that displays the segment corresponding to the RFM score.

![Screenshot 2024-08-12 135309](https://github.com/user-attachments/assets/63ca010a-cc34-401f-84dc-17bf018f4795)

![Screenshot 2024-08-12 135340](https://github.com/user-attachments/assets/378a453f-ac30-4cb2-aedf-ab9d26cba127)

In the segment file, based on the RFM scores, the customers are divided into 11 groups: Champions, Loyal, Potential Loyalist, New Customers, Promising, Need Attention, About To Sleep, At Risk, Cannot Lose Them, Hibernating Customers and Lost Customers.

Champions – Highly engaged and valuable customers with the highest RFM scores.

Loyal – Regular, high-spending customers with strong loyalty.

Potential Loyalist – Engaged customers with potential to become more valuable.

New Customers – Recent first-time buyers with room to grow.

Promising – Moderately engaged customers with potential.

Need Attention – Inactive customers who require re-engagement efforts.

About To Sleep – At risk of becoming inactive, need reactivation.

At Risk – Highly disengaged and likely to become lost customers.

Cannot Lose Them – Valuable but currently inactive customers.

Hibernating – Past high-value customers who could be reactivated.

Lost Customers – Completely disengaged, will require significant effort to win back.

To know more information, I calculated the number of customers in each segment.

![Screenshot 2024-08-12 135552](https://github.com/user-attachments/assets/8c6cd5c6-ee56-4134-8362-7f80c7c727ef)

I created the “RFM Customer Segments by Value” chart to get an overall view of the quantities of each customer segment.

![Screenshot 2024-08-12 135647](https://github.com/user-attachments/assets/7b5acf8b-00bb-40fa-ab2a-93fc8a7fec75)

Champions, are the most valuable and engaged customers. They have the highest Recency, Frequency, and Monetary (RFM) scores, indicating they make frequent purchases, have a high total spend, and have made a purchase very recently. These customers should be prioritized and provided with exceptional service to maintain their loyalty. I have noticed that the Champions customers account for around 18%, which is a relatively high number.

![Screenshot 2024-08-12 135733](https://github.com/user-attachments/assets/b9bc2727-d994-4add-83ad-6e961b03164f)

To visualize the correlation matrix of the RFM (Recency, Frequency, Monetary) values within the Champions segment of customers, I created a heatmap:

![Screenshot 2024-08-12 135815](https://github.com/user-attachments/assets/58b6887d-3389-4267-ae9c-c380e91775b4)

From this heatmap, we can see that: the r_score (Recency) has a strong positive correlation with the f_score (Frequency) and m_score (Monetary), the f_score and m_score also have a fairly strong positive correlation with each other.

# Result
Since this is a simulated project, there will be no actual results. Therefore, I have documented my suggestions in the “Result” section:

1. Based on the insights from the chart, the key RFM components that the business should focus on to drive the development of the Champions customer segment are:

– Recency (r_score): The Recency score has a strong positive correlation with both Frequency and Monetary. This indicates that maintaining and improving Recency (i.e., keeping customers actively engaged) will have a positive impact on both Frequency and Monetary.

– Frequency (f_score): The Frequency score also has a tight connection with Monetary. Therefore, the business should focus on increasing the transaction frequency of the Champions customers, as this will contribute to enhancing the Monetary value (revenue) from this key customer segment.

=> Prioritizing the enhancement of Recency and Frequency are the critical steps to develop the Champions customer segment, given the positive influence of these two factors on the Monetary value as well.

2. The customer segment that the business should focus on developing further is the “Potential Loyalist” segment. The reasons are:

– Developing the Potential Loyalist segment aligns well with the overall objective of growing the most valuable customer base. By nurturing these customers and turning them into loyal, high-value patrons, the business can strengthen its customer relationships and improve overall profitability.

– The Potential Loyalist segment represents customers with high value and growth potential. They are not yet fully loyal, but have the characteristics to become loyal and high-value customers for the business.

– Compared to the “Promising” segment which is low-value (130 customers), the Potential Loyalist segment (422 customers) has more room for further development and growth. Investing in this segment can yield better returns in the long run.











