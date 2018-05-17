# TextGenerator
### Standing on the shoulders of giants: 
- [Siraj's live tutorial](https://www.youtube.com/watch?v=ZGU5kIG7b2I&index=21&list=PL2-dafEMk2A7mfQDsEcmxxtxgFEZg0bW-) for generating text character by character   
- An excellent [blog](http://colah.github.io/posts/2015-08-Understanding-LSTMs/) explaining LSTM
- [Open course](https://www.youtube.com/watch?v=Keqep_PKrY8) of Stanford University about RNN and LSTM

This is an exercise on LSTM, using TensorFlow to build a two-layer-many-to-one-LSTM network from scratch (no Keras, no tensorflow.contrib.rnn, etc.).
Instead of generating text character by character like what Siraj has done in his tutorial, I did it word by word. 
For the word2vect part, I used the gensim package. 
The training text fed into the network was The Lord Of The Rings I.

#### Attention:
I did not pay much attention to the hyperparameter tuning, the idea was to get my hands dirty on building a LSTM network.
In order to get a reasonable generated text, I will need to train the model over night with a total epochs number of order 1000 
or even more and feed it with more training text, say the whole series of The Lord Of The Rings. 
For further improvement, I may add a dropout layer or use GRU cells instead of LSTM cells.


#### NEW:
I added an other version of text generator using 2 layers of GRU cells and dropout layers, indeed this make the computation 
faster and achieve a better result even the model was not sufficiently trained. However in this new version I used the tensorflow.contrib.rnn library to do the work.
