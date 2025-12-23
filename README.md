Language Model Training and Usage Project:
Hello,
This file explains in detail how to run all the files in the project step by step (they have all
been tested on Google Colab with GPU).
Basic Requirements (one time only)
Open any notebook and then run the following cell in the first block:
!pip install -q transformers datasets accelerate torch

1.	fine_tuning.ipynb – Training distilgpt2 on 1000 jokes from Reddit
Goal: Turn distilgpt2 into a joke generator.
Steps:
Make sure the file all.json is in the same folder.
Run the cells from top to bottom.
Training will take about 8–10 minutes on a T4 GPU.
After completion, the model and tokenizer will be automatically saved in the folder
distilgpt2-finetuned
Testing the trained model:
The last two cells in the notebook show a comparison between the original and
trained model.
You can also try any prompt like "Tell me a joke about programmers:".

1.	text_generation.ipynb – Generating a Continuous Story Using the Original GPT-2
Objective: Generate a long creative text starting from an opening sentence that you
write.
Steps:
Run the first cell (loading GPT-2).
Run the second cell.
A field will appear for you to write the beginning of the story, for example:
“Once upon a time in a futuristic city”
Press Enter, and the model will generate about 250–300 words to continue the story.

1.	summarization_qa.ipynb – Article summarization + Q&A
Goal: Summarize an article about Gaza + extract a specific answer.
Requirements:
Make sure that the file article.txt is in the same folder.
Steps:
Run the single cell in the notebook.
After completion, a new file named output.txt will be created containing:
The full original text
The summary
The answer to the question "What is the main humanitarian issue in Gaza?"
