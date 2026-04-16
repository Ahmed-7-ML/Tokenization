# 🧠 Arabic Medical Tokenization Using BPE

## 📌 Overview
This project demonstrates the significant impact of using **Domain-Specific Tokenization** on the efficiency of Large Language Models (LLMs).
We trained a **Domain-Specific Tokenizer** using Byte Pair Encoding (BPE)** on an Arabic medical dataset to improve the model's understanding of complex medical terminology.

---
## 🎯 Project Objectives
- Improve the representation of Arabic medical texts
- Reduce the number of tokens per sentence
- Maintain semantic integrity during segmentation
- Compare performance with general tokenizers

---
## ⚙️ Technologies Used
- Python
- Hugging Face tokenizers
- BPE (Byte Pair Encoding) Algorithm

---
## 🧪 How it Works

1. Develop a medical corpus in Arabic
2. Train the tokenizer using BPE
3. Test performance on complex medical sentences
4. Compare results with a general tokenizer

---
## 📊 Key Insights

### 🔹 1. Reduced Token Count
The specialized tokenizer produced fewer tokens per sentence, especially for complex medical terminology.

➡️ Result:
- Reduced Computational Cost
- Increased Effective Context Window

---
### 🔹 2. Preserving Semantic Integrity
Unlike generic tokenizers that break down Arabic words into incomprehensible fragments:

✔️ The Special Model:
- Preserves meaningful linguistic units
- Understands the morphological structure of medical terms

📌 Example:
- Words like "inflammation" and "sclerosis" are treated as logical units or quasi-units

---
### 🔹 3. Data-Centric Optimization
The results confirm that:

> **Data Preparation**, especially tokenization, is just as important as the model design itself.

✔️ Tokenizer optimization leads directly to:
- Better performance
- More accurate understanding
- More efficient training

---
## 🚀 Usage

### Tokenizer training:
```python
from tokenizers import Tokenizer
from tokenizers. models import BPE
from tokenizers.trainers import BpeTrainer
from tokenizers.pre_tokenizers import Whitespace

tokenizer = Tokenizer(BPE(unk_token="[UNK]"))
tokenizer.pre_tokenizer = Whitespace()

trainer = BpeTrainer( 
vocab_size=5000, 
special_tokens=["[UNK]", "[CLS]", "[SEP]", "[PAD]", "[MASK]"]
)

tokenizer.train(["medical_data.txt"], trainer)
tokenizer.save("medical_tokenizer.json")

````

---
### Tokenizer Testing:

```python
output = tokenizer.encode("Rheumatoid Arthritis")

print(output.tokens)
print(output.ids)
```

---
## 📌 Conclusion

This project proves that:

> **Domain-specific tokenization is a fundamental step in building robust and specialized AI systems.**

Especially in Arabic and technical fields like medicine, where the form of a word and its meaning are closely linked.

---
## 🔮 Future Work

* Expanding the corpus to include thousands/millions of sentences
* Experimenting with other algorithms such as Unigram LM
* Integrating the tokenizer with the Transformer model
* Applying it to tasks such as:

* Classifying medical texts

* Extracting Entity Nodes (NERs)

* Answering medical questions

---
## 👨‍💻 Developer

Ahmed Akram Amer | The Triple AI
