# Nestlé HR AI Assistant

This repository contains the code and resources for building an AI-powered HR assistant that responds to user inquiries using Nestlé's HR policy documents. The project leverages cutting-edge AI technology, including the LLaMA 3.1 model from Hugging Face and a user-friendly Gradio interface.

## Files

- **ags_nestle_genai.ipynb**: Jupyter Notebook containing the implementation of the HR Assistant.
- **nestle_hr_policy.pdf**: The Nestlé HR policy document used as the source for information.
- **Nestle_HR_Assistant_Code.docx**: Documentation with the complete code implementation.
- **AI_HR_Assistant_output.jpg**: Screenshot of the assistant in action.

## Installation

1. **Clone this repository:**
   ```bash
   git clone https://github.com/yourusername/Nestle-HR-AI-Assistant.git
   cd Nestle-HR-AI-Assistant
    ```
2. **Install the required dependencies:**
  ```python
  pip install -r requirements.txt
  ```
4. **Run the Jupyter Notebook:**
  ```bash
  jupyter notebook ags_nestle_genai.ipynb
  ```

## Usage

### Environment Setup
**Create a Virtual Environment:**
   ```bash
   python -m venv nestle_hr_venv
   source nestle_hr_venv/bin/activate  # On Windows, use `nestle_hr_venv\Scripts\activate`
   ```
### Hugging Face Setup
1. **Login to Hugging Face:**
You need to have access to the LLaMA 3.1 8B model on Hugging Face. Make sure you've been granted access to the repository.
* Log in to Hugging Face via the command line:
   ```bash
   huggingface-cli login
   ```
* Follow the prompts to log in using your Hugging Face credentials or token.

2. **Download the LLaMA 3.1 8B Model:**
After logging in, you can download and use the model directly in your Python code:
   ```python
   from transformers import LlamaForCausalLM, LlamaTokenizer

   model_name = "meta-llama/Meta-Llama-3.1-8B"
   
   # Load the tokenizer and model
   tokenizer = LlamaTokenizer.from_pretrained(model_name)
   model = LlamaForCausalLM.from_pretrained(model_name, torch_dtype=torch.float16).to("cuda")
   ```
### Running the Application
1. **Set Up the Code for Nestlé HR Assistant:**
* Ensure all files (e.g., nestle_hr_policy.pdf, the script, etc.) are in the appropriate directories.
* Use the provided Python script that integrates the model with Gradio and other components to create your HR assistant.

2. **Run the Application:**
Once everything is set up, run your Python script (e.g., main.py) to launch the HR assistant:
   ```bash
   python main.py
   ```
⚠️_Note: If you are using a Jupyter Notebook, run the cells as needed._

### Monitoring and Optimization
1. **Monitor GPU Usage:**
Use '_nvidia-smi_' to monitor GPU usage and ensure that the model is utilizing your GPU efficiently

2. **Optimization and Fine-Tuning:**
You can further optimize the model or integrate more features as per your project needs.

### Final Note
Final Notes
This setup will allow you to use the LLaMA 3.1 8B model for creating the Nestlé HR Assistant. Ensure you have sufficient GPU resources, as working with large models like LLaMA 8B can be resource-intensive.
