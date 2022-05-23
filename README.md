# machine-learning-project
### Selected topic
We will analyze a large dataset about purchases that result rejected, with the objective to predict and visualize the patterns that have the clients that get a chargeback or claim, using a machine learning model.

### Reason they selected the topic

Nowadays, the company Magenta gets more chargeback and claims, so for its economy, it's necessary to have more knowledge of what kind of purchase could be. And to make a decision when it shows the alerts. So, we want to predict if a buyer will do a fraudulent purchase. Also, we have enough data to analyze and work with it. 

### Description of the source of data
- **date_created:** The date and hour when the chargeback and claim were created.  
- **date_approved:** The date and hour when the purchase was approved.
- **email:** Consecutive numbers that correspond to a client's email.
- **external_reference:** It's a number that uses Magenta to reference the client's purchase with Mercado Libre.
- **operation_id:** The number that use Mercado Libre to identify a purchase.
- **status:** The status of the buy.
- **status_detail:** The status of the operation, claim or chargeback.
- **transaction_amount:** The total of the purchase.
- **installments:** How many periods it will pay the transaction_amount.
- **payment_type:** The different ways to pay the purchase.
- **billing_address:** The complete address the payment_type require.
- **shipping_address:** The complete address for deliver
- **ship_carrier:** The company which will deliver the purchase.
- **shipping_and_handling:** If the ship_carrier requires an extra amount for delivery.

### Questions we hope to answer with the data

- Is it a safe operation?
- What variables are related to the fraudulent buyer?
- What are the big patterns the purchase shows?
- What range of charges is most likely to be fraudulent?
- What is the fraudulent buyer likely to buy?
- Are fraud operations made from a specific region?


### Provisional machine learning model

* Which model did you choose and why? Supervised Machine Learning will be used for this project, mainly because our data covers operations that we already know that are fraud, this means labeled data. When we dig a little bit more into Supervised Machine learning we know that the classification model will help us in this Fraud detection project.

* How are you training your model? We have one year of operations, fraud operations named as (chargebacks and claims) and approved operations. We'll split data into 75% training set and 25% testing set.

* What is the model's accuracy? 
We ran a logistic regression and RandomOversampler model and we obtained 0.5 of accuracy, there was a lot of data that we had to remove so the model could be ran properly. Definitely there's a lot to improve and consider, maybe some restrictions on the data. We'll have to go deeper as well as run different models so we can determine which one is the best fit for this case.

<img width="459" alt="randomsampler_performance" src="https://user-images.githubusercontent.com/31755703/169733620-a2bf7e2c-a703-4e60-9d44-35a914e2ac16.PNG">


* How does this model work? This is the current performance:

<img width="563" alt="randomsampler_results" src="https://user-images.githubusercontent.com/31755703/169733646-11a03659-ba1a-41c2-9799-45c997b1f392.PNG">

We need to remember that Random Sampler,instances of the minority class are randomly selected and added to the training set until the majority and minority classes are balanced.


