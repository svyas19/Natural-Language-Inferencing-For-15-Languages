# Natural-Language-Inferencing-For-15-Languages

1.   Introduction</br></br>
Natural language processing (NLP) has grown increasingly elaborate over the past few years. Machine learning models tackle question answering, text extraction, sentence generation, and many other complex tasks. But, can machines determine the relationships between sentences, or is that still left to humans? If NLP can be applied between sentences, this could have profound implications for fact-checking, identifying fake news, analyzing text, and much more.</br>
If you have two sentences, there are three ways they could be related: one could entail the other, one could contradict the other, or they could be unrelated. Natural Language Inferencing (NLI) is a popular NLP problem that involves determining how pairs of sentences (consisting of a premise and a hypothesis) are related.
The main task is to create an NLI model that assigns labels of 0, 1, or 2 (corresponding to entailment, neutral, and contradiction) to pairs of premises and hypotheses.</br></br>

2.   Goal</br></br>
The main goal of this project is to determine the relationship between different sentences by classifying the relation between the sentences according to their respective labels and train the model to obtain good accuracy. The assigned labels are  0, 1, or 2 (corresponding to entailment, neutral, and contradiction) respectively.</br></br>

3. Data Analysis</br></br>
Language Distribution</br>

![Language Distribution](https://github.com/svyas19/Natural-Language-Inferencing-For-15-Languages/blob/main/Language%20distribution.png)


4. Word Cloud </br></br>
The most frequent Words</br></br>
![Word Cloud](https://github.com/svyas19/Natural-Language-Inferencing-For-15-Languages/blob/main/word%20cloud.png)</br>


5. Translation</br>
The premise-hypothesis sentence pairs were translated using the google translate API, but it was found that the API is inconsistent and fails to translate some sentences. This is especially a problem when one part of a sentence pair is translated to English and the other is not. In this case, it might just be easier to keep sentences in their original language than to use a pair that uses sentences in two different languages.</br></br>

6. Combining datasets</br>
Both the datasets were combined to create a larger corpus. The majority of this corpus will be in English since the multilingual pairs were already a minority part of the original dataset 1. This combined dataset was used on some of the models that were tested. It was not used with all models because the effects of the non-English sentence pair on classification accuracy are unknown. So the combined dataset was only tested on models that returned consistent prediction accuracy during training.</br></br>

7. Tokenization</br>
Tokenization is the process of creating a dictionary of words from the dataset in order to represent word-based sentences in coordinate-based vector representation. These token-based arrays then can be vectorized and a model can be then trained to classify those vectors.</br></br>
There are a few ways of performing tokenization. In this project, tokenization was performed using the 'Tokenizer' function from the TensorFlow library. The most common usage of tokenization involves tokenizing only train set. This allows us to get an idea of well the neural network can generalize when testing over the validation or test sets. This method of implementing tokenizer was implemented in the majority of the models trained. However, to see how much effect this can have a second method of tokenization was implemented in a few models which involves tokenizing the entire dataset.

8. Model Evaluation Results
![Evaluation Results](https://github.com/svyas19/Natural-Language-Inferencing-For-15-Languages/blob/main/Evaluation%20Results%20.png)




