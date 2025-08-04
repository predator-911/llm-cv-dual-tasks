 🧠🖼️ Dual AI Tasks: Image Classification + Time Parser LLM

This repository contains two complete and optimized AI pipelines:
1. **Task 1: Image Classification**
2. **Task 2: LLM Fine-Tuning for Datetime Extraction**

---

## 📂 Folder Overview

### `task1_image_classification/`
🎯 Train and benchmark 3 image classification models using the **Oxford Flowers 102** dataset:
- ✅ MobileNetV2 (Keras + TFLite)
- ✅ ResNet50 (Keras + TFLite)
- ✅ YOLOv8 Classification (Ultralytics + ONNX)

📌 Includes:
- Dataset download and preprocessing
- Training + quantization
- Inference time benchmarks on CPU

> ✅ **Achieved < 20ms inference time** using YOLOv8 and MobileNet (TFLite)

---

### `task2_time_parser_llm/`
🎯 Fine-tune an LLM (TinyLlama-1.1B-Chat) to extract structured **datetime** ranges from **fuzzy human queries**.

Example:
```text
Input: "last night around 8"
Output: { "start": "2025-08-01T20:00:00", "end": null }
📌 Includes:

TinyLlama + LoRA training

Inference using Hugging Face pipeline

Output validation using regex and datetime parser

✅ JSON-formatted output confirmed + parseable with Python

✅ How to Use
Clone the repo and open each notebook in Colab or Jupyter:

bash
Copy
Edit
git clone https://github.com/predator-911/llm-cv-dual-tasks.git
Then open:

task1_image_classification/image_classification_models.ipynb

task2_time_parser_llm/llm_time_extraction_finetune.ipynb

🛠️ Tech Stack
Task	Tools & Libraries
Task 1	TensorFlow, Keras, TFLite, YOLOv8, ONNX
Task 2	Transformers, PEFT (LoRA), Datasets, TRL, TinyLlama

📈 Results Summary
Model / Task	Format	Inference Time	Output
YOLOv8	ONNX	9.2 ms	✅
MobileNetV2	TFLite	11.4 ms	✅
ResNet50	TFLite	101 ms	⚠️
LLM	JSON	~1s	✅ {"start": ..., "end": ...}

📎 Author
Lakshya Kumar
https://github.com/predator-911/llm-cv-dual-tasks


✉️ sharmalakshay0911@gmail.com

🏁 Status
✅ Both tasks complete, benchmarked, validated and submission-ready.

