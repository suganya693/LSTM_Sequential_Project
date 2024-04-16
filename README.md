# LSTM_Sequential_Project
Text Data Preparation:
-Define a sample text data containing the corpus of text from which the model will learn.
-Tokenize the text using the Tokenizer class from Keras. This assigns a unique integer to each word in the vocabulary.

Input Sequence Generation:
-Split the text data into input sequences of varying lengths. These sequences will be used to train the model.
-Pad the sequences to ensure uniform length using the pad_sequences function from Keras.

Model Construction:
-Build a Sequential model using Keras.
-Add an Embedding layer to map the words to dense vectors of fixed size.
-Add LSTM layers for sequence processing. Two LSTM layers are used in this case.
-Add a Dense layer with softmax activation for outputting the predicted word.

Model Compilation:
-Compile the model using the compile method of the Sequential model. Specify the loss function, optimizer, and evaluation metrics.

Model Training:
-Train the model using the fit method of the Sequential model. Provide the input sequences (X) and the labels (y).

Text Generation Function:
-Define a function generate_text to generate text based on a seed text and a specified number of words to generate.
-Tokenize the seed text, pad it to the required length, and use the trained model to predict the next word.
-Append the predicted word to the seed text and repeat the process until the desired number of words is generated.

Testing:
-Test the model by providing a seed text and generating a sequence of words using the generate_text function.
-Print the generated text to the console.
