Project Overview
 -This project fine-tunes the mBART50 multilingual machine translation model for low-resource South African languages, specifically:
  >English → isiZulu
  >English → isiXhosa
 
Dataset: Language Pairs
 >English–isiZulu (25,200)
 >English–isiXhosa (26,000)
The dataset consists of parallel sentence pairs collected from publicly available Autshumato dataset.

Preprocessing Steps
-Data cleaning (removal of noisy or misaligned sentences)
-Text normalization
-Sentence alignment verification
-Tokenization using the mBART50TokenizerFast tokenizer
-Data Split (train:test - 80:20)

Training Process
-Model Pretrained: mBART50
-Fine-tuned using HuggingFace Transformers
-Training Configuration
  Optimizer: AdamW
  Learning rate: 3e-5
  Batch size: 8
  Epochs: 5
  Evaluation strategy: Per epoch
  
Monitoring
-Training Loss
-Validation Loss
-BLEU score per epoch
The model demonstrated steady convergence across epochs, with decreasing training and validation loss.

Evaluation Metrics:
-BLEU Score (primary quantitative metric)
-Validation loss

Results in BLEU Scores
English–isiZulu	19.29
English–isiXhosa	25.77
