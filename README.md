# Financial-Reasoning-Extraction-with-Chain-of-Thought-CoT-

This project builds a reasoning-aligned large language model that converts unstructured earnings call transcripts into structured, quantitative trading signals.

## Motivation
- Quantitative finance requires numeric signals, but most financial information is unstructured text.
- Modern LLMs hallucinate and lack reasoning transparency.

This project enforces **explicit Chain-of-Thought reasoning** and **strict JSON schemas** to bridge that gap.

## Methodology
1. Generate synthetic reasoning datasets using GPT-4
2. Fine-tune Llama-3-8B with LoRA (Unsloth) to enforce structured reasoning
3. Extract sentiment signals from earnings transcripts
4. Validate signals using next-day equity returns (Information Coefficient)

## Key Results
- Reasoning-consistent structured outputs
- Reduced hallucinations via schema enforcement
- Positive IC with T+1 returns

## Tech Stack
Python, PyTorch, Hugging Face, Unsloth, Llama-3, Financial Time-Series Analysis

## Future Work
- Self-consistency decoding
- Multi-quarter reasoning
- Factor-neutral backtesting
