# Stage 1: Markov Chain Text Generator

## About This Stage

This is the first stage of **AigenKuest**, a project focused on exploring the mathematical foundations of information retrieval and understanding how search engines work through practical implementation.

In this stage, I built a simple text generator using Python and Markov Chains. The aim was to understand how a computer can learn patterns in text, calculate the probability of word transitions, and generate sentences based on previously observed sequences.

Rather than treating this as just a programming exercise, I wanted to understand the mathematics behind the process.

## Mathematical Concepts Explored

- Markov Chains
- Conditional Probability
- Transition Probabilities
- Transition Matrices
- Stationary Distributions
- Long-run behaviour of Markov Chains

## How It Works

The model follows these basic steps:

1. **Text Processing:** The input text is cleaned by converting words to lowercase and removing punctuation.
2. **Word Counting:** The frequency of words and their occurrences is determined.
3. **Transition Mapping:** The model identifies which words follow other words and counts these transitions.
4. **Probability Calculation:** Transition frequencies are converted into probabilities.
5. **Text Generation:** Given a starting word, the model selects subsequent words based on their transition probabilities to generate a sentence.

The model learns from the text supplied to it. It does not generate sentences by understanding their meaning but by using patterns and probabilities observed in the input.

## Dataset and Source

For this implementation, I used a book obtained from **Project Gutenberg**, an online library providing access to free electronic books.

I selected an openly accessible book and converted its original format into PDF for use in the project.

The PDF served as the text source from which the model learned word transitions.

Project Gutenberg: https://www.gutenberg.org/

*Note: The availability and copyright status of individual books may differ. Check the book's usage conditions before redistributing its contents.*

## How to Use the Notebook

You can run this notebook using Google Colab.

### 1. Open the Notebook

Open the notebook provided in this folder using Google Colab.

### 2. Upload Your Own Document

You can replace the original book with your own text document.

In Google Colab:

1. Locate the file upload section in the notebook.
2. Upload your document from your device.
3. Ensure that the filename in your code matches the uploaded file's name.

For example, if your uploaded file is called `my_book.pdf`, use that filename wherever the original PDF filename is referenced.

**Supported document formats:**

- PDF (`.pdf`)
- Plain text (`.txt`)

Other formats, such as Word documents (`.docx`), may also be used, but you will need an appropriate text extraction method before passing the extracted text into the model.

For example, PDFs can be processed using a PDF text extraction library, while plain text files can be read directly in Python.

### 3. Change the Word Used for Testing

The notebook allows you to investigate the possible next words following a particular word.

For example, you may have used:

`love`

To investigate another word, simply replace `love` with your preferred word in the relevant code cell.

For example:

`transitions["love"]`

can be changed to:

`transitions["mathematics"]`

This allows you to examine the transitions and probabilities associated with different words in your document.

**Important:** The word you choose must exist in the processed text and have at least one observed word transition. Otherwise, the model may return an empty result or encounter a key error, depending on the code used.

### 4. Generate Text

You can also experiment with different starting words when generating sentences.

Change the starting word in the text-generation section of the notebook to explore how different starting points produce different sentences.

## Tools and Technologies

- Python
- Google Colab
- NumPy (where applicable)
- PDF text extraction
- Markov Chain modelling

## What I Learned

This stage helped me connect programming with mathematical concepts, particularly probability and Markov Chains.

One important insight was understanding the difference between word frequency and a stationary distribution. Word frequency tells us how often a word occurs, while a stationary distribution describes the long-run behaviour of a Markov process.

It was also an opportunity to practise text processing, dictionaries, nested data structures, loops and probability calculations in Python.

## Project Progress

**Stage 1: Markov Chain Text Generator — Completed.**

**Next Stage: PageRank**

The next stage will explore how Markov Chains, transition matrices, eigenvalues and eigenvectors can be applied to ranking web pages.

The broader goal is to gradually build an understanding of how search engines work, starting from their mathematical foundations.
