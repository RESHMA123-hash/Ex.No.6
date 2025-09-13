# Ex.No.6 Development of Python Code Compatible with Multiple AI Tools
# NAME : K.Reshma
# Date:13.09.2025
# Register no: 212223090020
# Aim: Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools

#AI Tools Required:

# Explanation:
Experiment the persona pattern as a programmer for any specific applications related with your interesting area. 
Generate the outoput using more than one AI tool and based on the code generation analyse and discussing that. 
### Output
* A reusable `AIClient` protocol and `MultiAIOperator` orchestrator that:

  * Sends a prompt to each client,
  * Extracts keywords, token usage, and a simple sentiment score,
  * Computes pairwise Jaccard similarity across model outputs,
  * Detects outlier/divergent models,
  * Produces heuristic actionable insights,
  * Saves a JSON report and a CSV of model responses.
* A live run using four mocked models with:

  * Output DataFrame shown to you,
  * Actionable insights printed,
  * Files saved to `/mnt/data/multi_ai_report/report.json` and `/mnt/data/multi_ai_report/responses.csv`.

How to adapt the script to real AI providers

1. Replace `MockClient` with real wrapper classes that implement `generate(prompt, **kwargs)` and return at least `{"model": name, "text": "...", "tokens_used": ...}`. For example:

   * OpenAI: call `client.responses.create(...)` or `openai.ChatCompletion.create(...)` and return text/tokens.
   * Cohere/Anthropic: call their SDKs similarly.
2. Keep the analysis utilities (`extract_keywords`, `simple_sentiment_score`, `jaccard_similarity`) or swap in stronger NLP tools (spaCy, transformers, or semantic embeddings for similarity).
3. For robust similarity, use embeddings (cosine similarity) from a single provider or a neutral encoder.
4. Enhance "insights" by adding:

   * Confidence scoring from models (if provided),
   * Cross-model voting/aggregation,
   * Cost estimates (based on tokens and model pricing).

Files produced (paths):

* `/mnt/data/multi_ai_report/report.json`
* `/mnt/data/multi_ai_report/responses.csv`

If you'd like, next steps I can perform right now (pick any, I will run them immediately):

* Replace the `MockClient` with a real OpenAI client using your API key (you'd paste the key or set `OPENAI_API_KEY` in env) and run live comparisons.
* Add embeddings-based similarity (requires an embedding API or local encoder).
* Improve keyword extraction (use spaCy/YAKE/RAKE).
* Produce a nicely formatted PDF report or PowerPoint summarizing comparisons and recommended actions.
* Add automated tests and CI-friendly structure
  
# Result: The prompt for the above said problem executed successfully

