# Lightweight Fine-Tuning with QLoRA on BERT

This project demonstrates parameter-efficient fine-tuning (PEFT) using QLoRA on a BERT model for the MRPC task from the GLUE benchmark. It is part of the Bertelsmann Next Gen Generative AI Nanodegree.

## Project Overview
- **PEFT Technique:** QLoRA (Quantized Low-Rank Adapter)
- **Base Model:** BERT (bert-base-cased and bert-base-uncased)
- **Dataset:** [GLUE MRPC](https://huggingface.co/datasets/nyu-mll/glue) (Microsoft Research Paraphrase Corpus)
- **Evaluation:** Model performance is evaluated before and after fine-tuning using the validation split.

## Workflow
1. **Load and Evaluate Base Model:**
   - Load a pre-trained BERT model and tokenizer.
   - Evaluate on the MRPC validation set to establish a baseline.
2. **Apply QLoRA PEFT:**
   - Configure and apply LoRA adapters to the model.
   - Fine-tune on the MRPC training set.
3. **Save and Reload PEFT Model:**
   - Save the fine-tuned LoRA adapter weights.
   - Reload the PEFT model and evaluate on the validation set.
4. **Compare Results:**
   - Compare evaluation metrics before and after fine-tuning.

## Repository Structure
- `LightweightFineTuning.ipynb`: Main notebook with all code and explanations.
- `bert_lora_model/`: Directory containing saved LoRA adapter weights and tokenizer files.
- `README.md`: Project documentation (this file).

## Requirements
- Python 3.8+
- Install dependencies with:
```bash
pip install -r requirements.txt
```

## Usage
Open and run the cells in `LightweightFineTuning.ipynb` to reproduce the workflow:
- Evaluate the base model
- Fine-tune with QLoRA
- Save and reload the PEFT model
- Compare evaluation results

## Results
The notebook prints evaluation metrics for both the base and fine-tuned models, allowing for direct comparison of performance improvements from PEFT.

## References
- [Hugging Face Transformers](https://huggingface.co/docs/transformers/index)
- [PEFT Library](https://github.com/huggingface/peft)
- [GLUE Benchmark](https://gluebenchmark.com/)

## License
See [`LICENSE`](./LICENSE) for details.
