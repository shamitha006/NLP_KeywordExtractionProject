# NLP_KeywordExtractionProject
An NLP-based approach for test validation. 

Problem statement: Test validation is verifying the specific requirements by writing the test case. 
Test case needs to be  automated for ease of execution and identifying the issues. But to write the test case it may take time to identify keywords and write the case. Our approach will solve this problem where writing test cases will be easier.

This AI-based approach helps the user to Create a test case provided with an input template.
Multiple approaches have been studied and the best has been concluded based on results obtained. 

Keyword Extraction: Keyword extraction is one of the most required text mining tasks: Given a document, the extraction algorithm should identify a set of terms that best describe its argument.
The two techniques used are:
a) TF-IDF (Term Frequency Inverse-Document Frequency):
TF-IDF is a weighing statistic to measure if a word is important in a corpus or not. 
A keyword is supposed to have a high TF_IDF score which means a high term frequency(frequency in a row) and low document frequency(high IDF- not very frequent in the entire corpus). 
b) KeyBERT:
BERT is a bi-directional transformer model that allows us to transform phrases and documents into vectors that capture their meaning
Leverages BERT-embeddings and simple cosine similarity to find the sub-phrases in a document that are the most similar to the document itself.

This process also calls for string matching in order to choose the best match for the given instruction out of those which the system is already trained, it is performed using FuzzyWuzzy. 
FuzzyWuzzy is a Python library that provides tools for string matching. It uses the Levenshtein Distance algorithm to calculate the similarity between two strings.
The main functionality provided by FuzzyWuzzy is the fuzz module, which contains various functions for string matching and comparison.
fuzz.ratio: Calculates the similarity ratio between two strings based on the Levenshtein Distance. The ratio is a number between 0 and 100, where a higher value indicates a closer match.
The process module, on the other hand, provides a high-level API for various common string matching scenarios. It simplifies the process of finding the best match for a target string within a list of choices.
process.extract: This function takes a target string and a list of choices and returns a list of the best matches sorted by similarity score. It uses the fuzz.ratio function to calculate the similarity between the target string and each choice.

The evaluation metric employed is BERTScore:
BERTScore is an automatic evaluation metric used for testing the goodness of text generation systems
Gives the precision, recall and F1-scores computed between the ground-truth and the generated text
