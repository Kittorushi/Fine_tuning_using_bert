# Fine_tuning_using_bert


# The code above is for a Question Answering chatbot based on a fine-tuned BERT model using the CoQA dataset.

First, the necessary libraries are imported including Pandas, Numpy, Matplotlib, Seaborn, Torch, Transformers, and BertForQuestionAnswering and BertTokenizer from Transformers.

Next, the CoQA dataset is loaded into a Pandas dataframe and cleaned by removing a column and then reformatting the data into a new dataframe with the columns "text", "question", and "answer". This new dataframe is saved as a csv file for future use.

The chatbot is built using the BertForQuestionAnswering and BertTokenizer libraries from Transformers. A random question and answer from the CoQA dataset are selected and printed along with the associated text. The question and text are then converted into token ids using the tokenizer. The index of the [SEP] token is found, and the number of tokens in segment A (question) and segment B (text) are determined. The segment ids are created to distinguish between segment A and segment B.

Finally, the segment ids and input ids are used to create a tensor, which is input into the BertForQuestionAnswering model to generate an answer to the question.
