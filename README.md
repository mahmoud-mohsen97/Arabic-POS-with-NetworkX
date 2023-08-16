# Arabic-POS-with-NetworkX

## Introduction:
In this project, the goal is to build a pipeline for part-of-speech tagging and then represent the POS by network graphs for the Arabic language. Part-of-speech tagging is the process of assigning a grammatical category (such as noun, verb, adjective, etc.) to each word in a given text. We will represent the text as a network graph to visualize and analyze the relationships between words based on their parts of speech. 
## Data Description:
- I used in LSTM training Arabic PUD github Taken from Universal Dependencies
- Uses articles from Wikipedia(W) and the news(N)
- Data is sequential (sequence of words) therefore using a sequence-labeling model is preferred
- It contains 998 sentences and 16 Tags 
## Experiments:
- Approach 1:  Stanza – A Python NLP Package for Many Human Languages
  
  Stanza is a collection of accurate and efficient tools for the linguistic analysis of many human languages. Starting from raw text to syntactic     analysis and entity recognition, Stanza brings state-of-the-art NLP models to languages of your choosing.
  So I used it where it prepared library and that will give me a fast output but there was some wrong prediction and that lead me to search for a     more robust approach

- Approach 2: Bi-directional LSTM model (Bi-LSTM)
  
  Through searching I found the stat-of-art for this task is Meta BiLSTM (Bohnet et al., 2018) with an accuracy of 97.96 so I built a Bidirectional   LSTM which is a sequential labeling classifier and will get the sequential information into consideration 
## Results: 
By evaluating the two models on the PUD Dataset I get : 
- Stanza Accuracy: 41.55%
- Bidirectional LSTM  Loss: 0.1901 and an Accuracy: 0.9424 
## Conclusion:
Using the Stanza library was so fast and optimized but the Bidirectional LSTM was accurate and building the Network is very relative and depending on the case and what information and insights you want to get.
## Tools and Resources:
- Overview - Stanza (stanfordnlp.github.io)
- Usefull tutorial with github page for reading and parsing dataset
- Medium article for Processing input data
- The aravec for the word embedding 
- NetworkX for creating a network graph of the POS tags
- Matplotlib, arabic-reshaper, and python-bidi for visualizing the network graph
- Keras and sklearn for building and evaluating the model 
## Challenges Faced and Learning from the Project:
The biggest challenge in this project might be dealing with the complexity of the Arabic language and the lack of readily available datasets and tools for Arabic NLP tasks. From this project, one can learn how to use various Python libraries for NLP tasks and how process and use wording embedding for Arabic,The project also demonstrates how to visualize the resulting data using NetworkX and matplotlib especially for Arabic.
