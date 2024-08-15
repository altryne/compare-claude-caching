# Compare Anthropic Claude 3.5 with and without caching

This project compares the performance of Anthropic Claude 3.5 with and without caching using Weights & Biases [Weave](http://wandb.me/weave?utm_source=thursdai&utm_medium=referral&utm_campaign=thursdai&utm_id=github). It analyzes long context scenarios using transcripts from the ThursdAI.news podcast.

<img width="1631" alt="image" src="https://gist.github.com/user-attachments/assets/630f2a17-131b-433c-9b4e-4601ee644e6b">


## Installation

To get started with this project, follow these steps:

1. **Create a virtual environment** (optional but recommended):
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

2. **Install the requirements**:
   ```bash
   pip install -q weave set-env-colab-kaggle-dotenv tqdm ipywidgets requests anthropic
   ```

3. **Set up environment variables**:
   Copy the `.env.example` file to a new file named `.env`:
   ```bash
   cp .env.example .env
   ```

   Then, open the `.env` file and add your API keys:
   - Add your Weights & Biases API key from https://wandb.ai/authorize to `WANDB_API_KEY`
   - Add your Anthropic API key from https://www.anthropic.com or https://console.anthropic.com to `ANTHROPIC_API_KEY`

   Your `.env` file should look something like this:
   ```
   WANDB_API_KEY=your_wandb_api_key_here
   ANTHROPIC_API_KEY=your_anthropic_api_key_here
   ```

   Note: Keep your `.env` file private and never commit it to version control.

4. **Run the Jupyter Notebook**:
   Open and run the `evaluate_claude_long_context_caching.ipynb` notebook to compare Claude 3.5 performance with and without caching.

## Project Structure

- `evaluate_claude_long_context_caching.ipynb`: Main Jupyter notebook for running the comparison
- `data/*.md`: Transcript files used for analysis (not included in this repository)
- `.env`: File for storing your API keys (create this from `.env.example`)
- `README.md`: This file, containing project information and setup instructions

## Note

This project requires access to the Anthropic API and Weights & Biases. Make sure you have the necessary permissions and API keys before running the notebook.