# compare-llama-providers
This is a quick test to see if all the new LLama 3.1 server providers are returning the same tokens, using Weights & Biases Weave Evaluations [https://wandb.me/weave](https://wandb.me/weave)

## Installation

To get started with this project, you need to install the required dependencies. Follow the steps below:

1. **Create a virtual environment** (optional but recommended):
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

2. **Install the requirements**:
   ```bash
   pip install -r requirements.txt
   ```


3. **Set up environment variables**:
   Copy the `.env.example` file to a new file named `.env`:
   ```bash
   cp .env.example .env
   ```

   Then, open the `.env` file and add your secrets:
   - Add your Weights & Biases API key from https://wandb.ai/authorize to `WANDB_API_KEY`
   - Add your OpenRouter API key from https://openrouter.ai to `OPENROUTER_API_KEY`
   - Add your Groq API key to `GROQ_API_KEY`
   - Add your Together API key to `TOGETHER_API_KEY`

   Your `.env` file should look something like this:
   ```
   WANDB_API_KEY=your_wandb_api_key_here
   OPENROUTER_API_KEY=your_openrouter_api_key_here
   GROQ_API_KEY=your_groq_api_key_here
   TOGETHER_API_KEY=your_together_api_key_here
   ```

   Note: Make sure to keep your `.env` file private and never commit it to version control.