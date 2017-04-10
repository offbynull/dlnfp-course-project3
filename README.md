# Deep Learning Nanodegree Foundations -- Project 3

Generate your own Simpsons TV scripts using RNNs.

## Links mentioned in review

If you are still a little confused about RNNs/LSTMs/GRUs in general (they are very confusing), I would highly recommend this blog posting (http://colah.github.io/posts/2015-08-Understanding-LSTMs/)




Something else that you can try is GRU or a Gated Recurrent Cell. It might be interesting to compare the results with the LSTM. You can read more about the the GRU compared to the LSTM here (https://arxiv.org/pdf/1412.3555v1.pdf).

The tensorflow code to use a GRU cell is the following:

tf.contrib.rnn.GRUCell()
Have a look at the doc here (https://www.tensorflow.org/api_docs/python/tf/contrib/rnn/GRUCell)




Nice work with this embedding. This is by far the best blog that I have ever read about embedding (http://mccormickml.com/2016/04/19/word2vec-tutorial-the-skip-gram-model/) If you have any questions at all about it, I would suggest reading this.

Embedding is important in that it reduces the time needed to train a network. The high dimensionality of sentence vectors is reduced to embed_dim size using the process that you studied in the word2vec module.




Awesome job! A lot of this stuff is confusing. For example, why do you need to use tf.nn.dynamic_rnn? You can read more about this in the RNN tutorial by TensorFlow (https://www.tensorflow.org/tutorials/recurrent)

The motivation of MultiRNNCell is as follows: having multiple LSTMs/GRUs/RNNs is logistically complicated across different time steps. The classMultiRNNCell makes the implementation seamless. Having multiple layers of LSTMs give the model way more expressive power.