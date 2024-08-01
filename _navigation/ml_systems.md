### Interview prep
1. Open ended questions

2. Always start with data cleaning, data preparation: look for which features are useful, logging, evaluation metrics, scalable inference, feature stores: recommenders/rankers

3. Can we break a vague problem into small tiny set of sub-challenges, can we know which are solved with machine learning and which are not

4. Can we define a problem clearly, identify relevant metrics, ideate on data sources and possible important features, understands deeply what machine learning can do
Methods change over-time, however solving problems stays the same.


5. In Research: We care about training, whereas in production we care about serving. Candidate who have only learned about ML but haven't deployed a system in real world
often make the mistake of focusing entirely on training

Performane requirements:

In ML, there's an obsession with SOTA results. To edge out a small increase in performance, researchers often resort to techniques that make models too complex to be useful.

Ensembling different algorithms may not have good value in production environments: Cost to train, might lead to a complex system.


### Interview has very strong focus on production



### Design a machine learning system

1. Setup- project
2. Data Pipeline
3. Modelling and training
4. Serving

### Project Setup
1. What are goals of our project: What do I want to achieve with problem, For example, if you're asked to create a system to rank what 
activities to show first in one's newsfeed on Facebook, some of the possible goals are: minimize spread of  misinformation, maximize revenue from
sponsored content, or to maximize user's engagement

Goals of task: 1 newsfeed: goals 1. maximize revenue, minimize spread of misinfo, maximize revenue from sponsored content
Convert business goal to mathematical goal

User experience: ask interviewer how step by step, how end users are supposed to use the system. If you're asked to predict what app a phone user wants to use next,
then I want to know when and how the predictions are used. Do you only show predictions only when a user unlocks their phone or during time and cost of such things

Performance constraints: Latency and prediction accuracy, precision or recall, cost: false negative or positive, if 

Precision= Out of total predicted as yes, how many are actually yes
Recall = Out of all actual yes, how many were predicted yes

Increasing precision decreases recall, and vice versa. Recall is a good metric than precision
F1 score: harmonic mean of precision and recall. error tolerance

3. Evaluation: How would you evaluate performance of the system, different metrics to evaluate performance 
4. training performance vs inference performance: identifying a differentiable metric so that we can update
Evaluation function helps in 

5. Personalization: One model for all users, for a group of users, or each user. Can we train a base model and finetune a model
6. Project Constraints: Compute and time budgets


### Data pipeline

1. What kind of data is available, how much data is already we have
2. Is it annotated, how good and accurate is annotated
3. How expensive is to get things annotated
4. Data budget
5. How to annotate data: supervised/unsupervised
6. User data: what data needed, how to collect