# cs221-project

Our team has implemented a bidirectional LSTM model to learn the mapping of an English-spelled name to its corresponding International Phonetics Alphabet (IPA). Each letter of the name was first encoded into its vectorized tensor, and this tensor was given as an input to the bidirectional LSTM model. In inference, the model would decode the output to produce the IPA of the english spelled name. 

- Dataset: We have scraped wikipedia for famous people's names and their corresponding IPA. we were  able to access a relevant data set known as CSLU: Spelled and Spoken Words", which was provided by the University of Pennsylvania's Linguistic Data Consortium. Published in 2006, the data set consists of recorded phone interviews of 3647 people.

- Model: Bidirection LSTM model, Encoder-Decoder Schema, and 2-letter bigram encoding

- Result: 

![results](https://github.com/jangj8523/cs221-project/blob/master/ipa%20translation%20result.png)
