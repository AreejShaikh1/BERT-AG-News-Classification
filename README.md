# BERT-AG-News-Classification


This project fine-tunes **BERT (bert-base-uncased)** for **text classification** on the **AG News dataset**.
The dataset consists of 4 news categories: **World, Sports, Business, and Sci/Tech**.

---

##  Project Structure

```
bert-ag-news/
│── config.json          # Model configuration
│── vocab.txt            # BERT vocabulary
│── pytorch_model.bin    # Pretrained weights
│── train.py             # Training script
│── inference.py         # Inference script
│── requirements.txt     # Dependencies
│── README.md            # Project documentation
```

---

##  Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/your-username/bert-ag-news.git
cd bert-ag-news
```

### 2. Create a virtual environment (recommended)

```bash
python -m venv venv
source venv/bin/activate   # On Linux/Mac
venv\Scripts\activate      # On Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

##  Training the Model

Run the training script:

```bash
python train.py
```

This will:

* Load the AG News dataset
* Tokenize with BERT tokenizer
* Fine-tune the model on training data
* Save results in `./results`

---

##  Inference / Prediction

Once trained, run predictions with:

```bash
python inference.py --text "The stock market saw record growth today."
```

Output:

```
Predicted Label: Business
```

---

##  Requirements

* Python 3.8+
* PyTorch
* Transformers (HuggingFace)
* Datasets (HuggingFace)

Install all via:

```bash
pip install torch transformers datasets
```

---

##  Results

* Base Model: **bert-base-uncased**
* Dataset: **AG News**
* Accuracy (on test subset): \~92% (after fine-tuning)

---

##  Acknowledgements

* [Hugging Face Transformers](https://huggingface.co/transformers/)
* [AG News Dataset](https://huggingface.co/datasets/ag_news)
