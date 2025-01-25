# Gemma 2 Spanish Language Adaptation 🌍

Fine-tuning implementation of Google's Gemma 2 model for Spanish language translation, submitted for the Kaggle "Unlock Global Communication with Gemma" competition.

## Overview
- Fine-tuned Gemma 2 using LoRA for English-Spanish translation
- Dataset: 1000 curated translation pairs
- Achieved 79.09% accuracy on training data
- Optimized for Kaggle A100 GPU environment

## Implementation Details
- Model: Gemma 2B base model
- Adaptation: LoRA (rank=4)
- Learning rate: 1e-5
- Batch size: 1
- Epochs: 5

## Results
- Basic phrase translations
- Conversational expressions
- Common greetings
- Short sentences

## Usage
```python
# Load model
gemma_lm = keras_nlp.models.GemmaCausalLM.from_preset("gemma2_2b_en")

# Generate translation
prompt = template.format(
   instruction="Translate to Spanish: hello",
   response=""
)
print(gemma_lm.generate(prompt, max_length=256))