# AigenKuest
## Stage 1: Markov Chain Text Generator

### 1. About the Project

AigenKuest is a project focused on exploring the mathematical foundations of information retrieval and understanding how search engines work through practical implementation.

This is the first stage of the project. It focuses on building a simple text generator using Python and Markov Chains.

The goal was to understand how a computer can learn patterns in text, calculate probabilities of word transitions, and generate sentences based on previously observed sequences.

Rather than treating this as just a programming exercise, I wanted to understand the mathematics behind the process.

### 2. Mathematical Concepts Explored

- Markov Chains
- Conditional Probability
- Transition Probabilities
- Transition Matrices
- Stationary Distributions
- Long-run Behaviour of Markov Chains

### 3. How It Works

The model follows these basic steps:

1. **Text Extraction:** Extracts text from an uploaded PDF document.
2. **Text Processing:** Converts text to lowercase and removes punctuation.
3. **Word Counting:** Determines the frequency of words in the document.
4. **Transition Mapping:** Identifies which words follow other words and counts these transitions.
5. **Probability Calculation:** Converts transition frequencies into probabilities.
6. **Text Generation:** Uses the calculated transition probabilities to generate sentences from a starting word.

The model learns from the text supplied to it. It does not understand the meaning of sentences; it generates text based on patterns and probabilities observed in the document.

### 4. Dataset and Source

For this implementation, I used a book obtained from **Project Gutenberg**, an online library that provides access to free electronic books.

I selected an openly accessible book and converted its original format into PDF for use in the project.

The PDF served as the text source from which the model learned word transitions.

Project Gutenberg: https://www.gutenberg.org/

*Note: The copyright and usage conditions of individual books may differ. Check the relevant terms before redistributing a book or its contents.*

### 5. How to Use the Notebook

The notebook is designed to run on Google Colab.

#### A. Upload Your Own Document

The project uses Google Colab's file upload functionality and the `pypdf` library to extract text from PDF documents.

To use your own book or document:

1. Open the notebook in Google Colab.
2. Locate and run the file upload cell.
3. Select a PDF document from your device.
4. Wait for the upload to complete.
5. Run the remaining cells.

The notebook automatically detects the uploaded filename, so you do not need to rename your document or manually change the filename in the code.

**Supported format:**
- PDF (`.pdf`)

Other formats, such as `.txt` and `.docx`, require different text-reading methods before their contents can be processed by the model.

**Important:** Use a PDF containing selectable text. Scanned PDFs may require OCR (Optical Character Recognition) before their contents can be extracted.

#### B. Test Different Words

The notebook allows you to investigate the possible next words following a particular word in your uploaded document.

For demonstration, the word `law` was used.

To test another word, locate the testing section and change:

`test_word = "law"`

to your preferred word.

For example:

`test_word = "love"`

The model will display:
- The words that follow the selected word.
- The frequency of each observed transition.
- The probability of each possible next word.

**Understanding the probability**

The transition probability is calculated as:

P(Next word | Current word) = Frequency of the transition / Total outgoing transitions from the current word.

For example, if `law` is followed by `of` in every recorded transition, the probability of moving from `law` to `of` is 1.0.

**Note:** The selected word must have at least one recorded outgoing transition in the processed text. Otherwise, the notebook will indicate that no recorded transitions are available.

### 6. Tools and Technologies

- Python
- Google Colab
- pypdf
- Markov Chain modelling

### 7. What I Learned

This stage helped me connect programming with mathematical concepts, particularly probability and Markov Chains.

One important insight was understanding the difference between word frequency and a stationary distribution.

Word frequency tells us how often a word occurs, while a stationary distribution describes the long-run behaviour of a Markov process.

It was also an opportunity to practise text processing, dictionaries, nested data structures, loops and probability calculations in Python.

### 8. Project Progress

**Stage 1: Markov Chain Text Generator — Completed.**

**Next Stage: PageRank**

The next stage will explore how Markov Chains, transition matrices, eigenvalues and eigenvectors can be applied to ranking web pages.

The broader goal is to gradually build an understanding of how search engines work, starting from their mathematical foundations.

---

*AigenKuest — Exploring the mathematics behind search engines, one stage at a time.*
