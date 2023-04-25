## Task 3 **Communication Abilities**

* Sentence Combination
Implement a program in Python that combines two sentences into one, retaining the information from both sentences. The combined sentence should preserve the meaning and context of both input sentences.
**Difficulty: Hard**

* Answer:

To combine two sentences into one, we can use the following approach:

First, we identify the subject and the verb in each sentence using a part-of-speech tagger.
Next, we join the subject of the first sentence with the verb of the second sentence and the subject of the second sentence with the remaining part of the first sentence to form the combined sentence.


* Python Code:

import nltk

''' 

def combine_sentences(sentence1: str, sentence2: str) -> str:

    sent1_tokens = nltk.word_tokenize(sentence1)
    sent2_tokens = nltk.word_tokenize(sentence2)
    sent1_pos = nltk.pos_tag(sent1_tokens)
    sent2_pos = nltk.pos_tag(sent2_tokens)
    
    for i, (word, pos) in enumerate(sent1_pos):
        if pos.startswith('VB'):
            verb_index = i
            break
    
    for i, (word, pos) in enumerate(sent2_pos):
        if pos.startswith('VB'):
            break
    
    combined_sentence = ' '.join(sent1_tokens[:verb_index]) + ' ' + ' '.join(sent2_tokens[i:])
    
    return combined_sentence

'''
