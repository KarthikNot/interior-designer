# <center> AI Interior Designer <center>

# 📜 Please read the license and use this project responsibly.

### 🌟 Model Description 🤖

- **Developed by:** Stability AI
- **Model Type:** Diffusion-based text-to-image generative model
- **License:** [CreativeML Open RAIL++-M License](https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0/blob/main/LICENSE.md)
- **Overview:** This innovative model allows users to generate and modify stunning images based on descriptive text prompts. It is a [Latent Diffusion Model](https://arxiv.org/abs/2112.10752) that leverages two fixed, pretrained text encoders: [OpenCLIP-ViT/G](https://github.com/mlfoundations/open_clip) and [CLIP-ViT/L](https://github.com/openai/CLIP/tree/main).
- **Further Resources:** For more information, explore our [GitHub Repository](https://github.com/Stability-AI/generative-models) and the SDXL report available on arXiv.

### 📚 Model Sources

For research purposes, we highly recommend our generative-models [GitHub repository](https://github.com/Stability-AI/generative-models), which implements the most popular diffusion frameworks for both training and inference. New functionalities, such as distillation, will be added over time. Additionally, Clipdrop provides free SDXL inference.

- **Repository:** [Generative Models Repository](https://github.com/Stability-AI/generative-models)
- **Demo:** [Clipdrop Demo](https://clipdrop.co/stable-diffusion)

SDXL utilizes an ensemble of expert pipelines for latent diffusion. Initially, the base model generates (noisy) latents, which are then refined using a specialized model (available [here](https://huggingface.co/stabilityai/stable-diffusion-xl-refiner-1.0/)) designed for final denoising steps. The base model can also function as a standalone module.

Alternatively, a two-stage pipeline can be employed: First, the base model generates latents of the desired output size. In the second step, a specialized high-resolution model applies a technique called SDEdit (also known as "img2img") to the latents generated in the first step, using the same prompt. This technique is slightly slower, as it requires more function evaluations.

**Source code** is available at [Source Code GitHub](https://github.com/Stability-AI/generative-models).

<img src='https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0/resolve/main/pipeline.png' alt='Pipeline Diagram'>

### 📊 Model Evaluation

<img src='https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0/resolve/main/comparison.png' alt='Model Comparison'>

The chart above illustrates user preferences for SDXL (with and without refinement) compared to SDXL 0.9 and Stable Diffusion versions 1.5 and 2.1. The SDXL base model significantly outperforms previous variants, and when combined with the refinement module, it achieves the best overall performance.

## 🛠️ How to Set Up This Project

This guide will help you set up the project's environment seamlessly.

**<u>1. Install Python</u> 🐍**

If you haven't installed Python yet, visit the official download page: [Python Download Guide](https://wiki.python.org/moin/BeginnersGuide/Download) and follow the instructions for your operating system (Windows, macOS, or Linux).

**<u>2. Create a Virtual Environment</u>**

1. Creating a virtual environment:

   - In the terminal, run this command:

   ```bash
   python -m venv venv
   ```

2. Activate the virtual environment:

   - To activate the virtual environment, use:

   ```bash
   .\venv\Scripts\activate
   ```

**3. Clone the Repository 📥**

1. Open your Git client or terminal.
2. Navigate to the directory where you want to clone the repository.
3. Run the following command, replacing `<repository_url>` with the actual URL of the project's repository:

```bash
git clone <repository_url>
```

**3. Install required Dependencies 📦**

1. Open terminal/cmd.
2. Navigate to repo directory
3. Run the following command to install dependencies from requirements.txt:

```bash
pip install -r requirements.txt
```

**4. Add the Together.ai API KEY 📦**

1. Create a .env file.
2. add a env variable "TOGETHER_API_KEY" in the .env file.  
   Example of a sample API KEY

```bash
TOGETHER_API_KEY = "<API_KEY>"
```

**4. Host the project Locally 🌐**

- After installing the required dependencies, run the following command to start the project locally:

```bash
streamlit run ./src/server.py
```
