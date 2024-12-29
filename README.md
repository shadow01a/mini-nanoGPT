[中文](README.zh.md)

# Mini NanoGPT 🚀

#### Is Training a GPT Really This Simple?

> Make GPT model training simple and fun! A visual training platform based on [karpathy/nanoGPT](https://github.com/karpathy/nanoGPT).

## 📖 What Is This?

Mini-NanoGPT is a tool that helps you easily get started with GPT models. Whether you are:
- 🎓 A deep learning beginner
- 👨‍🔬 A researcher
- 🛠️ A developer

Or just someone interested in experiencing the charm of large models,

You can train models through a simple graphical interface!

## ✨ Key Features

### 1. Simple and Easy to Use
- 📱 **Visual Interface**: Say goodbye to the command line and complete training with just a few clicks.
- 🌍 **Bilingual (Chinese and English)**: Full support for both Chinese and English interfaces.
- 🎯 **One-Click Operations**: Data processing, training, and text generation can all be done with a single click.

### 2. Powerful Functionality
- 🔤 **Flexible Tokenization**: Supports character-level and GPT-2 tokenizers (better support for English).
- 🚄 **Efficient Training**: Supports multi-processing acceleration and distributed training.
- 📊 **Real-Time Feedback**: Displays training progress and results in real time.
- ⚙️ **Parameter Visualization**: All training parameters can be directly adjusted in the interface.

## 🚀 Quick Start

### 1. Set Up the Environment
```bash
# Clone the repository
git clone https://github.com/yourname/mini-nanogpt.git
cd mini-nanogpt

# Install dependencies (Python 3.7+)
pip install -r requirements.txt
```

### 2. Launch the Project
```bash
python main.py
```
Open your browser and visit the displayed link to see the training interface! (Usually http://localhost:7860)

## 🎮 User Guide

### Step 1: Prepare Data
- Open the "Data Processing" page, select or paste your training text, and choose the tokenization method. For English text, using the GPT-2 tokenizer can yield better results. For Chinese, you can keep the default.
- If you do not want to use a validation set for now, you can check "Do not use a validation set."
- After completion, click "Start Processing."
  
  Here's an example using a small piece of text:
  
  ![image](https://github.com/user-attachments/assets/ec8db0d6-5673-43ae-a4cb-ac064f7209ae)

### Step 2: Train the Model
- Switch to the "Training" page and adjust the parameters as needed (if you just want to experience it, you can keep the default values).
- The program supports real-time display of loss curves for the training set and validation set. If you generated a validation set in Step 1, there should theoretically be two curves below: the blue one for the training set loss and the orange one for the validation set loss.
- If only one curve is displayed, please check the terminal output. If you see output similar to:
  ```
  Error while evaluating val loss: Dataset too small: minimum dataset(val) size is 147, but block size is 512. Either reduce block size or add more data.
  ```
  It means that the block size you set is larger than your validation set. Please reduce its size, for example, to 128.
- This way, you should be able to see two dynamically changing curves normally.
- Click "Start Training" and wait for the model training to complete.
  
  ![image](https://github.com/user-attachments/assets/75e53570-393b-48db-aac3-f9b6822d05b1)

#### Evaluation-Only Mode?
- This mode allows you to evaluate the model's loss on the validation set. Set the `Number of Evaluation Seeds` to any value greater than 0 to enable evaluation-only mode. You can see the model's loss with different seeds.

### Step 3: Generate Text
1. Go to the "Inference" page
2. Enter an opening text
3. Click "Generate" to see what the model writes!

![image](https://github.com/user-attachments/assets/5f985e89-d7c2-4f3a-9500-5713497148cd)

## 📁 Project Structure
```
mini-nanogpt/
├── main.py          # Launch program
├── config/          # Configuration files
├── data/            # Data processing and storage
├── models/          # Model definitions
├── trainer/         # Training-related
├── inference/       # Inference generation
└── app/             # Interface-related
```

## ❓ Frequently Asked Questions

### What if it's running too slowly?
- 💡 Reduce the `batch_size` or model size.
- 💡 Using a GPU will significantly speed up the process.
- 💡 Increase the evaluation interval.

### The generated text isn't good enough?
- 💡 Try increasing the amount of training data.
- 💡 Adjust the model parameters appropriately.
- 💡 Change the temperature parameter during generation.

### Want to continue previous training?
- 💡 On the "Training" page, select "resume" in the "Initialization Method."
- 💡 Specify the previous output directory.

## 🤝 Contributing
Suggestions and improvements are welcome! You can contribute in the following ways:
- Submit an Issue
- Submit a Pull Request
- Share your usage experience

## 📝 License
This project is open-sourced under the [MIT License](LICENSE).

---

🎉 **Start Your GPT Journey Now!**
