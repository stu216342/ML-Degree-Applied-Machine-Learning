# Literature Review

Approaches or solutions that have been tried before on similar projects.

**Summary of Each Work**:

- **Source 1**: TensorFlow Lite (LiteRT) On-Device Translation

  - **[PyTorch Seq2Seq Translation Tutorial](https://docs.pytorch.org/tutorials/intermediate/seq2seq_translation_tutorial.html)**
  - **Objective**: Tutorial to teach the fundamentals of Neural Machine Translation (NMT) by building a translation system without using high-level libraries like Hugging Face.
  - **Methods**: It uses a Gated Recurrent Unit (GRU) based Encoder-Decoder architecture with an Attention mechanism. It covers data preprocessing (cleaning, tokenizing), teacher forcing and manual evaluation. **Encoder**: The sentence (one-hot, language 1) goes into an Embedder word by word, which produces a dense vector, which is fed into the GRU together with the previous hidden state. This produces an output and the new hidden state (context). This solves the short memory problem of RNNs. The context of the (original english) sentence then goes to the decoder as hidden state. **Decoder**: The decoder takes the hidden state (context of the sentence) and the previous output of the decoder (the first one will be a Start Token). This output is again embedded, fed into the Decoder GRU, which again produces an output and a new hidden state. But **Bottleneck problem**: Full context of input sentence is in one vector after the Encoder. Solution: Attention. The Decoder has access to every hidden state that the Encoder produced.
  - **Outcomes**: A functional model that can translate short sentences. Because it is an RNN-based model, it is naturally very small and comp. efficient for mobile CPUs compared to large Transformers.
  - **Relation to the Project**: This is a learning baseline. We could use this structure to experiment with Hyperparameter Search (e.g. hidden layer sizes, learning rates or the number of GRU layers). The Tutorial shows the example French to English. We could compare that to Portugueese to English. It is interesting to see how well a model without a transformer will perform (allthough RNNs are probably outdated nowadays)

- **Source 2**: [Title of Source 2]

  - **[Link]()**
  - **Objective**:
  - **Methods**:
  - **Outcomes**:
  - **Relation to the Project**:

- **Source 3**: [Title of Source 3]

  - **[Link]()**
  - **Objective**:
  - **Methods**:
  - **Outcomes**:
  - **Relation to the Project**:
