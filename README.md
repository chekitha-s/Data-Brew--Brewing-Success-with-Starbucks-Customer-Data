# Data Brew: Brewing Success with Starbucks Customer Data
## Proposal: 
The Starbucks Customer Dataset simulates interactions and transactions to optimize promotional strategies. It includes diverse offers sent through different channels to 17,000 customers with demographic details. Events capture customer responses and transactions, enabling analysis of offer effectiveness and customer behavior.

Our project aims to determine optimal promotion channels, tailor offers based on customer attributes and actions, and elevate the overall efficiency and effectiveness of Starbucks' marketing efforts. This initiative seeks to maximize customer engagement, elevate customer satisfaction, and drive the success of Starbucks' marketing strategies.

The data is contained in three files:
- portfolio.csv - data about offers sent to customers (10 offers x 6 columns)
- profile.csv - demographic data of customers (17,000 customers x 5 columns)
- transcript.csv - customer response to offers and transactions made (306,648 events x 4 columns)

Here is the schema and explanation of each variable in the files:

### profile.json
- age (int) - age of the customer
- became_member_on (int) - date when customer created an app account
- gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
- id (str) - customer id
- income (float) - customer's income
### portfolio.json
- id (string) - offer id
- offer_type (string) - type of offer ie BOGO, discount, informational
- difficulty (int) - minimum required spend to complete an offer
- reward (int) - reward given for completing an offer
- duration (int) - time for offer to be open, in days
- channels (list of strings)
### transcript.json
- event (str) - record description (ie transaction, offer received, offer viewed, etc.)
- person (str) - customer id
- time (int) - time in hours since start of test. The data begins at time t=0
- value - (dict of strings) - either an offer id or transaction amount depending on the record
- 
### SMART Questions - MIDTERM: 
1. How do different promotional events (received, viewed, completed) affect customer retention and repeat business with Starbucks over time?             
2. What is the profile of the customer base, including their gender distribution, age distribution, and income range, and how do these factors relate to each other?
3. What are the most popular offers and the influential factors driving the View rates of the Offers?
4. Which age groups are more likely to accept offers than others? Do these preferences also differ based on gender?

### SMART Questions - FINAL:
1. How can we design a precise predictive model to classify customer responses to offers as successful or not?
2. Can we predict which customer segment a new customer is likely to belong to based on their demographics?

### Conclusion
Our analysis of Starbucks’ customer, offer, and transaction data shows that both channel mix and offer type strongly influence offer completion. Multi-channel delivery (particularly mobile + web) consistently increases the likelihood of success compared to single-channel campaigns. BOGO offers appeal more to high-engagement customers, while discount offers are more effective for price-sensitive segments. Informational offers, while rarely completed, play a role in boosting awareness and future engagement.

Customer segmentation revealed distinct clusters that respond differently to channel strategies and offer designs, reinforcing the need for targeted marketing rather than a one-size-fits-all approach. Predictive models (GLM, SVM) demonstrated strong performance, with interpretable baselines and more flexible nonlinear classifiers both adding value.

Overall takeaway: Starbucks can improve campaign efficiency and customer satisfaction by tailoring offers to segment needs, leveraging the right channel combinations, and applying predictive modeling to guide targeting decisions.


