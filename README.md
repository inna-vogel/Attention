# Implementing Udacity's Simple Attention Network

In this notebook, we look at how attention is implemented. We will focus on implementing attention in isolation from a larger model. That's because when implementing attention in a real-world model, a lot of the focus goes into piping the data and juggling the various vectors rather than the concepts of attention themselves.

We will implement attention scoring as well as calculating an attention context vector.

# How can a Attention Network be described? 

One important property of human perception is that one does not tend to process a whole scenein its entirety at once.  Instead humans focus attention selectively on parts of the visual space toacquire information when and where it is needed, and combine information from different fixations over time to build up an internal representation of the scene, guiding future eye movementsand decision making. 
- Recurrent Models of Visual Attention 2014

- Attention allows to look at small relevant parts of input as it generates the output. __But how does the decoder know which parts to focus on?__ The process is learned over time. At every time step, attention decoder pays attention to the appropriate part of the input sequence using context.    

Attention was initially designed in the context of Neural Machine Translation using Seq2Seq Models.

Attention takes 2 sentences and turns them into a matrix. The words of the first sentence for the columns, the words of the second sentence form the rows. Then it makes matches, identifying relevant context.


