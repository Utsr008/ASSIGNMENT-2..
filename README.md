Assignment – 2: Encoder-Decoder Models using RNN and LSTM
Part-I: Theoretical Understanding of RNN, LSTM, and Encoder-Decoder

Answer the following questions in 2–4 sentences each:
 1. What is the difference between RNN and LSTM?

Ans. RNN is used to handle sequential data like time series while LSTM is used to handle
Long term patterns which introduces gates such as input, output, forget gate for the regulation of flow of information.

2. What is the vanishing gradient problem, and how does LSTM solve it?

Ans. The vanishing gradient problem occurs when gradients become too small during backpropagation through time, preventing RNNs from learning long-range dependencies. LSTMs fix this using a cell state that acts like a memory highway, plus gating mechanisms (input, forget, output) that regulate the flow of information and preserve gradient strength.

3. Explain the purpose of the Encoder-Decoder architecture.

Ans. Encoder-Decoder architecture is designed for tasks involving input and output sequences of different lengths like transcription. Encoder processes input sentence and convert it into numeric vector and then process it in decoder it generate output sentence, one word at a time.

4. In a sequence-to-sequence model, what are the roles of the encoder and decoder?

Ans. Encoder processes input sentence and convert it into numeric vector and then process it in decoder it predicts output sentence, one word at a time.
Example.. “Good”,  “Night” as input in encoder and <sos>, “Guten”, “Nicht” ,<eos> as output in decoder….in german..

5. How is attention different from a basic encoder-decoder model?

Ans. Encoder processes input sentence and convert it into numeric vector and then process it in decoder it predicts output sentence, but this can lead to information loss, like in long inputs where the attention mechanism improves it by allowing the decoder to focus on various parts of input sentence at each output  step, this will help in improving the accuracy of model.


Task 2: Sequence-to-Sequence Data Flow Draw or describe the data flow in an encoder-decoder model using RNN/LSTM. Clearly label: 
INPUT SEQUENCE
HIDDEN STATE
CONTEXT VECTOR
OUTPUT SEQUENCE

Ans.
Input seq passes the word-by-word into the encoder, where each word generates a hidden state through rnn/lstm. 
The final hidden state is termed as context vector, which summarizes the entire input. 
Now this context vector is passed to the decoder, which generates the output sequence, one word at a time.
EXAMPLE.. “Good”,  “Night” as input in encoder 
h1, h2 from encoder as hidden state and h1 termed as vector whereas h2 is d2 and rem is context….
h2 is the final hidden state passed to decoder and words generated step by step “Guten”, “Nicht” ,<eos> as output in decoder….in german…..
