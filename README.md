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


#### Morphology
**Morpheme** - Small meaningful units that makes up a word.  
*Stems* - Core Units.  
*affixes* - pieces that adheres to stem  
**Example** - In the word '*Affixes*' ,  'Affix' is a stem while 'es' is a affix.  

#### Stemming
Converting the words into the stem i.e removing the affixes.  
*For Example* - *automates* , *automatic* and *automatic* should all be converted to *automate*.  


#### Porter's Algorithm for Stemming (Idea)
![Porter's Algorithm](https://raw.githubusercontent.com/prrateekk/NLP_summary/master/image/porter_algo.jpeg)
