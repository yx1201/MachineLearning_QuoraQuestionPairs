# MachineLearning_QuoraQuestionPairs

## Abstract
As large text data are generated and recorded in today’s world, our ability to detect semantic similarity and equivalence in sentences become more and more important. This technique can be applied in many fields, including social media and research. Detecting similarity can be done in many ways. The simplest is to match the word occurred in the two sentences. However, this approach may not be able to capture the dynamic and subtlety nature of language. In this paper, we took the Quora question pair dataset and developed an empirical model using machine learning methods to estimate whether two questions are equivalent to not. We used Gloves and TF-IDF for word embedding and examined the similarity of questions by KNN, Random Forest and XGBoost. The objective of modeling was to minimize the log-loss of predictions on duplicacy in the testing dataset. Finally, we achieved significant lift against the baseline mode.

## 1. Introduction
In this digital world, the number of new documents and information are increasing exponentially. New research findings and reports are released. Hundreds of news articles, stories and tweets are generated every day. Thousands of facebook posts and events every day. Numerous new questions being posted on platforms like Quora and StackOverflow. The information explosion does have its own good. New ideas are more likely to come across one’s mind when one is immersed in an environment with diverse information. However, for people who are looking for an answer for a specific question, the huge amount of information can be a barrier. For example, when people are searching on StackOverflow looking for help with their code, they might find multiple opened questions related to their bug. It would be time consuming to go over all posted questions to find the best solution. People might also distracted  unrelated information when the they need to go over all related question to search for an answer.

This is a bad user experience for both writers and seekers, as the answers get fragmented across different versions of the same question. For the real-world problem out there, we hope AI could solve it.

### 1.1 Business Problem and Motivation
As the amount of available data grows in the digital age, the problem of managing the information becomes more difficult. The information explosion will likely lead to information overload. People might not be able to efficiently allocate their time in making the right decision on an issue or finding the answer to their question when they have too much information about the issue. To solve this problem, we can have a similarity detection system to test across all posted contents and detect the ones that are duplicates in their meaning.

This mechanism can be used in many scenarios. For example, models for detecting similarity sentences could be used to better organize and consolidate the questions or answers for platform such as Yahoo or Quora. It would be easier for the users to find high quality answers to questions.Such model could also be applied to improve the performance of smart speakers such as siri and Amazon Echo Dot. Moreover, A similarity detection system would be crucial for detecting the plagiarism or duplicated ideas in the research field. In those scenarios, a mature product should be an information system that automatically filters, merges or flag the publication that are very similar in the content.

In this paper, we are trying to build a model that could recognize not only common pattern in two questions, but when two questions use different words and phrases with the same semantic meaning. Our model tries to learn these patterns to achieve better prediction.

### 1.2 Previous Works
As sentence similarity detection widely used in some applications such as plagiarism detection or Question-Answer platform, there is extensive literature on measuring texts similarity. There are some other techniques that are related to our work. Some early approach for detecting sentence similarity uses word overlaps or surface-matching method. As Devrim Akca introduced the idea of word overlaps and surface-machining in his paper, this method is based on the number of words occurrence in both text segments(1). This technique relies on the assumption that if two texts are similar then they shares more
duplicate words. In 2006, Landauer proposed a corpus-based methods(2). The term co-occurrences in a corpus are operated by a singular value decomposition (SVD) for dimension deduction and generate a matrix T representing the corpus. Then, Vector similarity is then used to identify documents that are most related to the query. For now, more and more nature language process techniques are used on this problem to include semantic meaning in the sentences such as gloves, word2vec.

In this paper, we are going to combine semantic embedding, vector similarity and machine learning modeling together to predict the Quora question similarity.

### 1.3 Problem Formulation
In this paper, we would like classify whether question pairs are duplicates or not by applying advanced machine learning techniques. More specifically, our problem is a binary classification problem in which we take two natural language questions and return a binary result duplicate/different.

More specifically, given a training dataset, we would like to derive a model that could minimize the log-loss on the test dataset. Details on our training dataset, which contains the features X, input information related to the two questions of interest and our label are explained in the section below.

#### Detailed work description was in the pdf: [Quora Question Pairs Final Report](https://github.com/yx1201/MachineLearning_QuoraQuestionPairs/blob/master/1003_FinalProjectReport.pdf)
#### Contribution: Preprocessing and XGboost Modeling
