# No Parameter Left Behind: How Distillation and Model Size Affect Zero-Shot Retrieval

This repository contains the code to reproduce the results presented in the paper [No Parameter Left Behind: How Distillation and Model Size Affect Zero-Shot Retrieval](https://arxiv.org/abs/2206.02873).

In this work, we show that increasing model size results in marginal gains on in-domain test sets, but much larger gains in new domains never seen during fine-tuning. Furthermore, we show that rerankers largely outperform dense ones of similar size in several tasks. Our largest reranker reaches the state of the art in 12 of the 18 datasets of the Benchmark-IR (BEIR).

![Ilustration of our results](src/results.PNG)

## Models

* [monoT5-small model](https://huggingface.co/castorini/monot5-small-msmarco-10k)
* [monoT5-base model](https://huggingface.co/castorini/monot5-base-msmarco-10k)
* [monoT5-3B model](https://huggingface.co/castorini/monot5-3b-msmarco-10k)
* [MiniLM](https://huggingface.co/cross-encoder/ms-marco-MiniLM-L-6-v2)

## How do I reproduce the results?

As our best model is a zero-shot one, we provide only the evaluation script.
- [All public datasets, except Robust04 and CQADupstack](BEIR.ipynb) 
- [Robust04 and CQADupstack](CQADupstack_&_Robust04.ipynb) 

To reproduce monoT5-3B results at least 25GB of RAM and a Tesla P100 GPU are required.


## How do I cite this work?

~~~ {.xml
 @article{Rosa_2022,
    title={No Parameter Left Behind: How Distillation and Model Size Affect Zero-Shot Retrieval},
    author={Rosa, Guilherme and Bonifacio, Luiz and Jeronymo, Vitor and Abonizio, Hugo and Fadaee, Marzieh and Lotufo, Roberto and Nogueira, Rodrigo},
    journal={https://arxiv.org/abs/2206.02873},
    year={2022}
}
