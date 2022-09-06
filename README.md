# Punctuation Capitalisation Restoration

## What’s the point?

he service receives an audio file and uses it as an input for trained model.

## Model details:

The service receives an English-language text file and uses it as an input to the Bert based model, based on a neural network trained in a mixture of natural and synthetic data, and outputs the result of the text sample recognition in form of a text. The model runs on a GPU equipped with tensor cores to provide greater service bandwidth. The input text file, in practice the optimal duration of the processed text samples should be no more than 3000 symbols for english language text.

## How does it work?

The user must provide the following inputs in order to start the service and get a response:

Inputs:

 -   `endpoint`: ?
 -   `method`: t2t
 -   `input_path`: Path to '\*.txt' file containing JSON representation of input argument 'file@data' and its value - path to '\*.txt' input text file.

Example of input file content:

```
{"file@data": "samples/sample.txt"}
```

## What to expect from this service?

Input text: samples/sample.txt - `hello my name is grace i love cake`

Response: 
- `text: Hello, my name is Grace. I love cake.`
