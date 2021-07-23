# Quantizing Transformer-Based Models

**Solution by**: ![MIL Team](https://machine-intelligence.ru/en/about)

**Date**: July 2021

![Scheme](https://github.com/ml-patterns/ml-patterns/blob/main/library/images/Quantizing_Transformer-Based_Models.jpeg)

### Challenge

When porting neural network models to devices (watches, speakers, cameras, refrigerators, etc.), it’s necessary to simplify the network architecture in order to reduce the size of the model, and thus speed up its operation. The restrictions on a neural network can be more significant, for example, if it’s supposed to calculate the model on a low-bit precision processor. In this case, it’s necessary to quantize the model. Despite the fact that quantization is an actively-developing area, there are a few projects devoted to the quantization of neural network models based on the architecture of transformers. The challenge was to propose a practical method of low-bit quantization of the SOTA architecture of a transformer, without significant loss of quality of the final model.

### Solution

We took the SOTA implementation of the transformer-based model architecture and quantized its layers and operations. For successful and fair quantization, it was necessary to implement quantized versions for all modules used inside the PyTorch model. A handy tool was also made to replace the original PyTorch modules with quantized ones. The algorithm for the best quantization strategy was implemented in a large number of experiments. As a result, the quality loss during the 2-bit quantization of models was reduced from 60% to just 3%.
We used the ASR transformer architecture implemented in the Fairseq open repository, presented in the article ![Transformers with convolutional context for ASR](https://arxiv.org/abs/1904.11660), a [LibriSpeech dataset](http://www.openslr.org/12/) for training speech recognition models, and a framework for quantizing models with complex architectures written for PyTorch by the MIL Team.

### Technologies

Python, PyTorch, torchaudio, Fairseq, SentencePiece.
