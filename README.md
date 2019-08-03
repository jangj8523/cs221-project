# cs221-project

Our team has implemented a bidirectional LSTM model to learn the mapping of an English-spelled name to its corresponding International Phonetics Alphabet (IPA). Each letter of the name was first encoded into its vectorized tensor, and this tensor was given as an input to the bidirectional LSTM model. In inference, the model would decode the output to produce the IPA of the english spelled name. 

- Dataset: We have scraped wikipedia for famous people's names and their corresponding IPA. we were  able to access a relevant data set known as CSLU: Spelled and Spoken Words", which was provided by the University of Pennsylvania's Linguistic Data Consortium. Published in 2006, the data set consists of recorded phone interviews of 3647 people.

- Model: Bidirection LSTM model, Encoder-Decoder Schema, and 2-letter bigram encoding

- Result: 

![results](https://github.com/jangj8523/cs221-project/blob/master/ipa%20translation%20result.png)

Due to the encoder-decoder architecture, our model does not map letters to Worldbet symbols one-to-one. As can be seen in Figure 5, our unidirectional model was generally able to correctly predict the pronunciation of the first consonant in the name. However, the model was not as successful in predicting subsequent letters, and instead tended to default to pronunciation combinations that existed in the data set, completely disregarding the actual letters in the input name. Of the outputs in Figure 5, "neil" (output of "nahe"), "baker" (output of "baxter"), and "steve" (output of "stevie") were all names that are present in their exact form in the data.
This sub-optimal performance was the primary motivation behind our introduction of the bidirectional model. The qualitative performance of our model noticeably improved with the introduction of the bidirectional model. For one, the model becomes much better at at least guessing the pronunciations of the consonants in the names. This seems to confirm our assumption that the pronunciation of a letter depends on both the letters that precede it and those that follow it. However, for names that are similar to those found in the data set (i.e. "baxter", "stevie"), the model still shows the tendency to "default"
