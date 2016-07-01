# Natural Language Processing - [Stanford University](https://class.coursera.org/nlp/lecture)
---
#### Word Tokenization
Converting a large text into a list of words/tokens. It can be done by converting all the alphanumeric characters into linebreaks.

##### Normalization
**Example** U.S.A and USA are the same.

##### Lemmatization

Reduce variants form to base form.  
**for example** - are,am,is --> be  
car,cars,cars' --> car

##### Morphology
**Morpheme** - Small meaningful units that makes up a word.  
*Stems* - Core Units.  
*affixes* - pieces that adheres to stem  
**Example** - In the word '*Affixes*' ,  'Affix' is a stem while 'es' is a affix.  

##### Stemming
Converting the words into the stem i.e removing the affixes.  
*For Example* - *automates* , *automatic* and *automatic* should all be converted to *automate*.  


#### Porter's Algorithm for Stemming (Idea)  

![Porter's Algorithm](https://raw.githubusercontent.com/prrateekk/NLP_summary/master/image/porter_algo.jpeg)

#### Sentence Segmentation

*Period* ('.') is ambiguous.  
It can be used as a abbreviations(Dr.) as well as sentence termination,Decimal numbers etc

#### A decision tree could be used

*A Decision Tree is simply an if-else statement.*

![Sentence Segmentation using decision tree](https://raw.githubusercontent.com/prrateekk/NLP_summary/master/image/sentence_segmentation.jpeg)

**NOTE-** *E.O.S* - End Of Sentence.  
*Ideas to be formulated by the programmer. Lots of modifications can be made to make a more sophisticated decision tree.*  
*Some numeric features can be used.*    
*For Example - Probability of getting 'the' after a period is very high.*

### Similarity between 2 Strings ###

##### Given by Minimum Edit Distance #####
**Definition** - Minimum number of insertion,deletion and substitution required to convert a string to another.
*Used in computational Biology*

**CAN BE SOLVED USING DYNAMIC PROGRAMMING**  
*Substitution is given twice the weight of insertion and deletion*  
*Weights are added to each insertion and deletion operation as well.  
For example - 'e' and 'i' are likely to be used mistaken in a word. So, substitution cost for them is taken lesser.*  
**It is also important to know the proper alignment of the 2 strings for which minimum edit distance is found .**  
*Both time and space complexity is O(nm), where 'n' and 'm' are the lengths of the two strings respectively.*  

### Probabilistic Language Model (Grammar)
**Goal** is to find the *Probability of a sentence or a sequence of a sentence*  
*P(W) - P(w1,w2,....wn)*  
*P(wn|w1,w2...wn-1) is the probability of wn appearing when w1,w2...wn-1 has already appeared.*  
##### Chain Rule
*P(w1,w2,.....wn) = P(w1).P(w2|w1).P(w3|w1,w2).P(w4|w1,w2,w3)....P(wn|w1,w2...wn-1)*  
But this model is practically impossible as there are infinite amount of sentences.  
So we use the **Markov Assumption** and use the concept of *N-Gram*.  
Instead of using entire prefix in the formula, we use previous 'N' words.  
So in a *unigram* model, the formula would be -  
*P(w1,w2,w3...wn) = P(w1).P(w2)...P(wn)*  
Simliarly, a bigram model would look like -   
*P(w1,w2..wn) = P(w1).P(w2|w1).P(w3|w2).P(w4|w3)....P(wn|wn-1)*  

**Note that the final result may cause underflow since the sentences may be large.**  
*To deal with this problem we take the log.*.So the formula becomes-  
*log[P(w1,w2,....wn)] = log[P(w1)]+log[P(w2|w1)].....*
