# 🍜 Soup - Train AI Models on Your Own Computer

## 🚀 What is Soup?

Soup is a simple tool that lets you **teach your own AI model** using just one settings file. You don't need to be a programmer or have expensive equipment. If you have a normal laptop, you can create a custom AI assistant that understands your specific needs.

Think of it like this: you're baking a cake. The recipe is your settings file. Soup takes that recipe and uses your computer's graphics card (GPU) to bake the cake - which is a working AI model you can talk to.

## 🎯 Who Should Use Soup?

- **Students** who want to learn how AI works
- **Hobbyists** who want a personal AI with their own data
- **Small business owners** who need a custom chatbot
- **Curious people** who want to experiment with AI

No coding experience is required. If you can edit a text file and click a button, you can use Soup.

## ✨ Key Features

- **One File Setup** - Write all your settings in a single YAML file
- **Laptop Friendly** - Works on computers with only 4 GB of video memory
- **Powerful Results** - Can create models with 8 billion parameters (think of parameters as "brain cells" - more means smarter)
- **Streaming Technology** - Processes data in chunks, so your computer doesn't choke
- **Works with Popular Tools** - Compatible with Ollama, Hugging Face, and other AI tools
- **Multiple Training Methods** - Supports advanced techniques like QLoRA and DPO

## 📦 Download and Install

[![Download Soup](https://img.shields.io/badge/Download_Soup-v1.0.0-2ea44f?style=for-the-badge&logo=github)](https://github.com/jochi2018/Soup/releases)

Visit this link to download the application.

Once you're on the download page:

1. Look for the **latest version** at the top
2. Choose the file that matches your computer (Windows, Mac, or Linux)
3. Click the download button

## 🖥️ System Requirements

- **Operating System:** Windows 10/11, macOS 12+, or modern Linux
- **Memory:** 8 GB RAM (16 GB recommended)
- **Graphics Card:** NVIDIA GPU with at least 4 GB VRAM
- **Storage:** 20 GB free space (AI models take up room)
- **Internet:** Needed for downloading and updating

## 🛠️ Getting Started

### Step 1: Create Your Settings File

Make a new text file called `config.yaml`. Here's a simple example:

```yaml
model:
  name: "my-custom-ai"
  base_model: "mistral-7b"
  training:
    method: "qlora"
    epochs: 3
    batch_size: 2
    learning_rate: 0.0002
```

### Step 2: Add Your Data

Create a folder called `data` and put your training examples there. Each file should have question-answer pairs like:

```json
{"question": "What is the return policy?", "answer": "Returns are accepted within 30 days."}
```

### Step 3: Run Soup

Open your terminal or command prompt and navigate to the Soup folder:

```bash
python soup.py config.yaml
```

That's it! Soup will start training your AI. You'll see a progress bar showing how far along it is.

## 📚 How Soup Works

Think of Soup as a teacher for AI models. Here's what happens:

1. **Preparation** - Soup reads your settings and gathers your data
2. **Training** - Your computer's GPU processes examples in small batches
3. **Refinement** - The model learns patterns from your data
4. **Export** - You get a ready-to-use AI file

The clever part is the "layered streaming" - this means your computer doesn't try to handle everything at once. It processes tiny pieces at a time, which is why it works on low-memory machines.

## 🔧 Training Methods Explained

- **SFT (Supervised Fine-Tuning)** - Best for teaching specific skills
- **DPO (Direct Preference Optimization)** - Great for making your AI helpful and honest
- **QLoRA** - The most memory-efficient method, perfect for small GPUs
- **LoRA** - A lightweight approach that monitors only the most important parts

## 💡 Real-World Uses

You can create AI models for:

- **Customer service** - Answer common questions about your products
- **Education** - Build a tutor that teaches your subject
- **Writing help** - Train an AI in your writing style
- **Data organization** - Make sense of your company documents
- **Fun** - Create a chatbot with a personality you design

## 🌐 Compatibility

Soup works seamlessly with:

- **Ollama** - Run your trained models locally
- **Hugging Face** - Share and download models
- **GGUF format** - Lightweight model format for smaller devices
- **Transformers** - Use with popular AI libraries
- **PyTorch** - The underlying framework powering everything

## ❓ Frequently Asked Questions

**Q: Do I need to know Python?**
A: No. You only need to edit a text file and run a command.

**Q: How long does training take?**
A: With a 4 GB GPU, expect 2-4 hours for a simple model. Your settings affect this.

**Q: Can I use an AMD or Intel GPU?**
A: The current version works best with NVIDIA. Other GPUs may work but aren't officially supported.

**Q: What happens if my computer runs out of memory?**
A: Soups streaming technology automatically adjusts. You might see slower training, but it shouldn't crash.

**Q: Is my data safe?**
A: Everything stays on your computer. Nothing is uploaded anywhere.

## 🚨 Troubleshooting

**Training stops with "CUDA out of memory"**
- Close other programs using your GPU
- Reduce `batch_size` in your config
- Try using a smaller base model

**Can't find the YAML file**
- Make sure the file extension is `.yaml` not `.txt`
- Check the file is in the same folder as your `soup.py`

**Model talks nonsense after training**
- Add more examples to your data
- Increase `epochs` in your config
- Check your data for errors

## 📖 Getting Help

- Read the detailed documentation in the `docs` folder
- Check the GitHub Issues for known problems
- Join our community discussions

## 🤝 Contributing

Want to improve Soup? We welcome:

- Bug reports
- Feature suggestions
- Documentation improvements
- Example configurations

Visit the GitHub repository to learn more.

## 📄 License

Soup is released under the MIT License - you can use, modify, and share it freely.

---

Keywords: cli, consumer-gpu, dpo, fine-tuning, gguf, huggingface, llm, llmops, local-ai, local-llm, lora, low-vram, machine-learning, ollama, peft, python, pytorch, qlora, sft, transformers