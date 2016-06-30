# Natural Language Processing
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
