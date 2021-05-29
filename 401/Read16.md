## What makes machine learning so special?
- Machine learning is the practice of teaching computers how to learn patterns from data, often for making decisions or predictions.

### Key Terminology

| **Term** | **Meaning** |
|------------|-------------------|
|Model|a set of patterns learned from data|
|Algorithm|a specific ML process used to train a model|
|Training data|the dataset from which the algorithm learns the model|
|Test data|a new dataset for reliably evaluating model performance|
|Features|Variables (columns) in the dataset used to train the model|
|Target variable|A specific variable you're trying to predict|
|Observations|Data points (rows) in the dataset|

## Machine Learning Tasks

- A task is a specific objective for your algorithms.
- Algorithms can be swapped in and out, as long as you pick the right task.
- you should always try multiple algorithms because you most likely won't know which one will perform best for your dataset.

### Supervised Learning

Supervised learning includes tasks for "labeled" data (i.e. you have a target variable).

- In practice, it's often used as an advanced form of predictive modeling.
- Each observation must be labeled with a "correct answer."
- Only then can you build a predictive model because you must tell the algorithm what's "correct" while training it (hence, "supervising" it).
- **Regression** is the task for modeling continuous target variables.
- **Classification** is the task for modeling categorical (a.k.a. "class") target variables.

### Unsupervised Learning

Unsupervised learning includes tasks for "unlabeled" data (i.e. you do not have a target variable).

- In practice, it's often used either as a form of automated data analysis or automated signal extraction.
- Unlabeled data has no predetermined "correct answer."
- You'll allow the algorithm to directly learn patterns from the data (without "supervision").
- **Clustering** is the most common unsupervised learning task, and it's for finding groups within your data.

## The 3 Elements of Great Machine Learning

- 1: A skilled chef (human guidance)
  - As you'll see, you'll need to make dozens of decisions along the way.
  - In fact, the very first major decision is how to road-map your project for guaranteed success.

- 2: Fresh ingredients (clean, relevant data)
  - Garbage In = Garbage Out, no matter which algorithms you use.
  - Professional data scientists spend most their time understanding the data, cleaning it, and engineering new features.

- 3: Don't overcook it (avoid over fitting)
  - An over fit model within a hedge fund can cost millions of dollars in losses.
  - An over fit model within a hospital can costs thousands of lives.
  - For most applications, the stakes won't be quite that high, but over fitting is still the single largest mistake you must avoid.

## What are Hyperparameter
- When we talk of tuning models, we specifically mean tuning hyperparameter.

There are two types of parameters in machine learning algorithms.

The key distinction is that model parameters can be learned directly from the training data while hyperparameter cannot.
