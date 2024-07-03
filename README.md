# Dialogue Summarization Using LLM's and ROUGE Score Analysis

# Objective :

To summarize dialogues using various generative AI models and analyze the results using ROUGE scores.

# Model Selection :

Amazon Titan Text Lite accessed through Amazon Bedrock

LangChain gpt-3.5-turbo using Chat Messages

LangChain gpt-3.5-turbo using Promp template

HuggingFace's Flan-T5

# Dataset : https://huggingface.co/datasets/knkarthick/dialogsum

# Evaluate Using ROUGE Scores : 
Compute ROUGE scores (ROUGE-1, ROUGE-2, ROUGE-L) for each model's summaries against the reference summaries.


ROUGE (Recall-Oriented Understudy for Gisting Evaluation) is a set of metrics used for evaluating the quality of automatic summaries by comparing them to a set of reference summaries (typically human-generated). Here's what each ROUGE metric measures:

1. **ROUGE-1 (unigram overlap):**
   - Measures the overlap of unigrams (individual words) between the generated summary and the reference summaries.
   - Example: If a reference summary contains "good morning" and the generated summary contains "morning is good", ROUGE-1 would count "morning" and "good" as overlapping unigrams.

2. **ROUGE-2 (bigram overlap):**
   - Measures the overlap of bigrams (sequences of two adjacent words) between the generated summary and the reference summaries.
   - Example: If a reference summary contains "good morning" and the generated summary contains "morning is good", ROUGE-2 would count "morning is" and "is good" as overlapping bigrams.

3. **ROUGE-L (longest common subsequence):**
   - Measures the longest common subsequence (LCS) between the generated summary and the reference summaries. LCS is the longest sequence that can be found in both the generated and reference summaries without reordering the words.
   - Example: If a reference summary is "The cat sat on the mat" and the generated summary is "A cat sat on a mat", ROUGE-L would find the longest common subsequence as "cat sat on mat".

4. **ROUGE-Lsum (average ROUGE-L):**
   - Measures the average of the ROUGE-L scores of the individual sentences in the generated summary against the reference summaries. This metric is useful for multi-sentence summaries.
   - Example: If a generated summary consists of multiple sentences, ROUGE-Lsum calculates the average ROUGE-L score across all sentences.

### Interpretation:

- **Higher Scores**: A higher ROUGE score (close to 1.0) indicates a better overlap or similarity between the generated summary and the reference summaries, suggesting better quality in terms of content overlap.
