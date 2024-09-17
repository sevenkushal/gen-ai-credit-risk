**AI-Powered Credit Risk Assessment Summaries**

**Objective -** To create an agent that can provide end-users with a concise report about the rationale behind why a certain user has their loan_status as 0 (not likely to default) or 1 (likely to default).

**Steps -**
1) Create a logistic regression model trained on our labelled data to understand the coefficients for each of the variables
2) The coefficients are provided to the LLM as a prompt along with instructions on how we would want the agent to provide reports for each of the users
3) The fine-tuned model is generated based on training data. We have used 10 samples to train the LLM
4) An output in the form of a crisp 100-word paragraph is generated for end-users

**Sample Output -** 
For user_id = 105, the loan_status is 1, indicating a predicted default on 
the loan. Despite a decent income, the loan amount is significant compared 
to their income, with a loan_percent_income ratio of 59%, suggesting
potential financial strain. Additionally, the person is relatively young, 
has a short employment length of 1 year, and does not own their home, which
may indicate a less stable financial situation. These factors, along with a
moderate credit history, contribute to the model predicting a higher risk of
default for this user.
