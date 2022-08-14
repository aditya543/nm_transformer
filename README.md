# Introduction
This is an advanced sequence-to-sequence model for machine translation based on the latest and the greatest Transformer architecture.
This is powered by a Byte Level BPE Tokenize to achieve even amazing results.
This Repo is inspired by the amazing nmt-chatbot project by Daniel-Kukiela and Sentdex.
It can be used to translate between languages and achieve state-of-the-art results and also it may be used as a chatbot. This Repo comes with a 
pre-trained model which is trained off Reddit Chat Data. You can immediately start interacting with it by running inference.py

# Setup
Clone the repository and cd into it.
Install all the required packages from the requiremenst.txt file, Python version 3.7 is also required.
After getting all the pre-requisites, just run inference.py to start conversing with the pre-trained chatbot.
If you want to further train the chatbot, run train.py and it should start training.
Note that the pre-trined model that comes with this Repo is not a massive model, It's just a baby model with 57 million parameters and it was trained
only on 2.8 million comment-reply pairs from Reddit. The pre-trained model was trained just for 6 hours on one single machine with GeForce RTX 3060.
Do not expect this model to achieve some state-of-the-art results.

# Hyper-parameters
You can tweak all the neccesary hyper-parameters in setup/settings.py, the most important of them all is "max_vocab". The pre-trained model
has the vocab of just 32,000. Ideally you would want to have as much vocab as possible, a good start would be 50,000. The next most important
hyper-parameter is "num_encoder_layers" and "num_decoder_layers". The pre-trained model has only 2 for both but ideally you would want to have 6
as described in the 'Attention is all you need' paper. You can tinker with all the other hyper-parameters and see the results for yourself.

# Add your own Training Data.
This is yet another extremely simple task of this Repo, just get your source and target data, put it in train.from and train.to files and put them in
new_data directory, and just start running train.py
For example, let us suppose that you want to create a model that translates from English to Hindi, then you will create a file named train.from containing
all the English sentences and another file train.to containing all the Hindi sentences which translate to the English ones. Make sure that both from and to
files have equal number of lines.




