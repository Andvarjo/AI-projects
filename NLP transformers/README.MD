# NLP with Transformers 🤖

This notebook will walk you through a simple way to apply architectures like LSTM and Transformers for natural language processing. The objective of the exercise is to classify a series of sentences into a category belonging to a feeling "sentiment analysis".
The purpose of this work is to develop models using NLP, capable to classify text input into emotion class based on LSTM and Transformers Architectures to compare its performance on both scenario. The dataset used to test this models contains 20K phrase labeled by emotion:Joy, Anger, Sadness, Fear, Love and suprise.

Our first Task consist in data pre-processing accessing each sentence removing duplicated data and special characters (data cleaning). Once our data is ready to work with, we can proceed with the tokenizing and sequence task in order to convert all the data to numerical representation, which can be feeded to our models for training and testing purposes.

Our first approach is going to be made building an LSTM network, and then two Transformers architecture to test performance

## Conclusions
* Pre-processing data stage it's crucial for NLP purpose, because cleaning data before embedding will allow us to perform coding text to its purest form of representation, using NLTK stop words and dropping special characters will do the task for this exercise, but if you are going to work with another kind of dataset which uses special characters for context (like tweets or mentions in social media) can change the way that the machine interpreatates the sentences. Analyze the purpose of your specific task to take this kind of decissions.

* LSTM network led us to abetter result in terms of accuracy and loss, but it has more computational cost compared with transformer architecture for this specific solution. It is imperative to know the nature of the data, because LSTM in such point will lead to gradient vanishing for very long sentences or corpus, but this was not the case, each sentence had a maximun of 40 words which is suitable for NLP with LSTM

* Transformers based architectures can perfom better in this scenario in terms of time and computational cost, making things easier for fine tunning or for architecture fixing, because it needs less training time you can edit the network while you are looking for your desired outcome. for this case with the same or more number of epochs in less time we get a way looking similar performance in terms of loss and accuracy.Exploring the way we tuned the network and the architecture itself its proven that it can be adjusted for better performance.

* With the second transformer architecture which incorporates spatial embedding and the way that its layer are connected togheter we can achieve better performance than the other architectures, for future works we can explore if increasing atention heads, changing embedding dimenssion or even more transformer blocks we can improve the performarce or even fine tunning parameters.
