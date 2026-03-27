
# Natural Language Processing with Transformers- Building AI Applications with Hugging face by Lewis Tunstall, Leandro von Werra, and Thomas Wolf


## Index
- [Chapter 1: Hello Transformers](#chapter-1-hello-transformers)



## Chapter 1: Hello Transformers:
1. Transformers architecture introduced in 2017, outperformed state of the arm neural networks along with an effective transfer learning method for NLP Neural Networks ULMFiT based on LSTM boosted the AI for NLP race because of their pervasiveness.
2. 2 Major Types of Transformers: (GPT) Generative Pre Trained Transformer and Bidirectional Encoder Representations (BERT). 
3. Transfer Learning is the idea of splitting the model into a body and a head, where the head is a task-specific network. During training, the weights of the body are frozen and these weights are used to initialize a new model for the new task. Hence a new model can be trained with much less data. 
4. GPT uses only the decoder part of the transformer, while BERT uses only the encoder part of the transformer. BERT is trained using masked language modelling. The objective is you mask the words of a sentence randomly and train the model to predict these words. 
5. Hugging Face Transformers helps you to: Implement the model architecture in code using PyTorch or TensorFlow, load pretrained weights from a server, preprocess inputs, pass them through the model with task-specific postprocessing, and implement dataloaders while defining loss functions and optimizers to train the model.
6. We can instantiate a pipeline by calling the `pipeline` function.  The second time you instantiate the pipeline, the library will notice that the weights and model has been downloaded and will used the cached function. 
	Ex) `classifier_pipeline = pipeline("text-classification`
7. In NLP, real-world objects like products and places and people are called named entities, and extracting them from text is called Named Entity Recognition. One can apply NER with hugging face transformers with: `ner_pipeline = pipeline("ner", aggregation_strategy="simple")`
8. A question answering pipeline can created with `eader = pipeline("question-answering")`. Giving the model a paragraph and asking the model a question and the model answers directly using the text in the passage is called extractive question answering. 
9. Summarization and question answering are slightly complicated tasks as they involve text generation. A summarization pipeline can initialized by: Ex) `summarizer = pipeline("summarization"`
10. The Hugging Face ecosystem has the hugging face hub, which holds all the models, datasets, etc. The models can also be played or tested with in the hugging face hub itself. The hugging face library has 4 major modules: Tokenizers, Transformers, Datasets and Accelerate, effectively covering every aspect of an NLP task pipeline. 
11. Main Challenges with working with transformers are: Language i.e it is dominated by the English language , data availability, working with long documents becomes expensive, Opacity i.e transformers to a large extent act like a blackbox and Bias. Bias is induced in the model due to bias in the data. 
