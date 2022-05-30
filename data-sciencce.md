# data sciencce

- [research](research)
- currently https://gft.udemy.com/course/chatbot/learn/lecture/8778732#overview
- https://www.tfcertification.com/pages/deep-learning-chatbot
- how to build gpt3 chatbot with python : https://www.youtube.com/watch?v=C-8sF81k7cY

---

```
-> current target: NLP
```

- `pd.columns`
- **features**: columns sent into our model (and later used to make predictions)
- The steps to building and using a model:
  - define
  - fit
  - predict
  - evaluate
- We can use a for-loop to compare the accuracy of models built with different values for max_leaf_nodes.
- As mentioned above, some of the features will throw an error if you try to use them to train your model
- https://www.kaggle.com/code/alexisbcook/missing-values deal with missing values - As is common, imputing missing values (in Approach 2 and Approach 3) yielded better results, relative to when we simply dropped columns with missing values (in Approach 1).

- supervised learning - regression problem: predict continuous(concrete) valued output - classification problem: predict discrete valued output

- Supervised Learning - In supervised learning, we are given a data set and already know what our correct output should look like, having the idea that there is a relationship between the input and the output. - Supervised learning problems are categorized into "regression" and "classification" problems. - In a **regression** problem, we are trying to predict results within a **continuous** output, meaning that we are trying to map input variables to some continuous function. - In a **classification** problem, we are instead trying to predict results in a **discrete** output. In other words, we are trying to map input variables into discrete categories.
- Squaring a feature, in other words, gave the linear model the ability to fit squared features.

- https://towardsdatascience.com/how-to-build-your-own-chatbot-using-deep-learning-bb41f970e281
-
- https://towardsdatascience.com/building-an-ai-chat-bot-e3a05aa3e75f
- good tutorial -> a simple chatbot in python with deep learning https://towardsdatascience.com/a-simple-chatbot-in-python-with-deep-learning-3e8669997758
- keyword: Natural Language Processing with Python -> book - https://www.youtube.com/watch?v=xvqsFTUsOmc - sumamry at 1:47:50 https://youtu.be/xvqsFTUsOmc?t=6470 - libraries at 1:48:10 https://youtu.be/xvqsFTUsOmc?t=6470
- find some good jupyter notebook, there's explanation what people do in it
- projects - https://www.dataiku.com/learn/samples/
- https://www.youtube.com/watch?v=Rt6eb9VOFII&t=942s

- In order to create our training data, there is first some things we must do to our data. Here is the list:

  Create a vocabulary of all of the words used in the patterns (recall the patterns are the queries posed by the user)
  Create a list of the classes — This is simply the tags of each intent
  Create a list of all the patterns within the intents file
  Create a list of all the associated tags to go with each pattern in the intents file
