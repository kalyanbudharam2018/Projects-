## Task 2 **Professional Aptitude**.

* Information Density Sentence Sorting. 
Implement a program in Python that sorts sentences in a given text by their information density.
The sentences should be sorted in descending order, with the most information-dense sentence appearing first.

**Difficulty: Medium**


Answer:


* To sort sentences in a given text by their information density, we can use the following approach:

First, we split the text into sentences using a sentence tokenizer.
Next, we calculate the information density of each sentence. This can be done by calculating the ratio of the number of unique words in the sentence to the total number of words in the sentence.
Finally, we sort the sentences based on their information density in descending order and return the sorted list.


* Python Code:

'''

import nltk

def information_density(text: str) -> List[str]:

    sentences = nltk.sent_tokenize(text)
    scores = []
    
    for sentence in sentences:
    
        words = nltk.word_tokenize(sentence.lower())
        
        unique_words = set(words)
        
        density = len(unique_words) / len(words)
        
        scores.append((sentence, density))
    
    scores.sort(key=lambda x: x[1], reverse=True)
    
    return [score[0] for score in scores]

'''
