<!-- README.md rendered as HTML markup (safe to paste into Medium/Substack as an HTML block) -->

<h1>RAG Regulatory AI</h1>

<p>
  A step-by-step example of building a <strong>Retrieval Augmented Generation (RAG)</strong> system using
  <strong>Google Gemini</strong> and <strong>vector search</strong> to analyze regulatory documents.
</p>

<p>
  This project demonstrates how to create an AI assistant that answers questions about
  <strong>Maryland cannabis regulations</strong> using real document retrieval rather than relying on model memory.
</p>

<p>
  This repository accompanies the tutorial series:
  <br />
  <strong>"Building a Regulatory AI Assistant: A RAG System for Cannabis Law Using Gemini"</strong>
</p>

<hr />

<h2>What This Project Demonstrates</h2>

<p>This tutorial walks through the core components of a RAG pipeline:</p>

<ul>
  <li>document ingestion</li>
  <li>text chunking</li>
  <li>embedding generation</li>
  <li>vector similarity search</li>
  <li>grounded LLM responses</li>
</ul>

<p>
  The system retrieves relevant regulatory sections and uses them as context for
  <strong>Gemini</strong> to generate accurate answers.
</p>

<hr />

<h2>Example Question</h2>

<p>Example query:</p>

<pre><code>Can a dispensary advertise cannabis products on social media in Maryland?</code></pre>

<p>
  Instead of hallucinating, the system retrieves the relevant regulatory text and generates an answer
  grounded in the document.
</p>

<hr />

<h2>Project Structure</h2>

<pre><code>rag-regulatory-ai
│
├── vectordb.ipynb
├── maryland_cannabis_regulations.md
├── requirements.txt</code></pre>

<hr />

<h2>Setup</h2>

<h3>1. Clone the repository</h3>

<pre><code>git clone https://github.com/jasmineeea/rag-regulatory-ai.git
cd rag-regulatory-ai</code></pre>

<h3>2. Create virtual environment</h3>

<pre><code>python -m venv .venv
source .venv/bin/activate</code></pre>

<h3>3. Install dependencies</h3>

<pre><code>pip install -r requirements.txt</code></pre>

<hr />

<h2>Google Cloud Setup</h2>

<p>
  This tutorial uses <strong>Google Vertex AI</strong> and <strong>Gemini</strong>.
</p>

<p>Create a service account with the role:</p>

<pre><code>Vertex AI User</code></pre>

<p>Download the JSON key and place it in the project folder.</p>

<p>Example:</p>

<pre><code>policy-rag-dev-key.json</code></pre>

<p>Then initialize the Gemini client in the notebook using:</p>

<pre><code class="language-python">from google.oauth2 import service_account
from google import genai</code></pre>

<hr />

<h2>Running the Notebook</h2>

<p>Open the notebook:</p>

<pre><code>vectordb.ipynb</code></pre>

<p>Run the cells sequentially to:</p>

<ol>
  <li>load the regulatory dataset</li>
  <li>generate embeddings</li>
  <li>build a vector index</li>
  <li>retrieve relevant document chunks</li>
  <li>generate grounded answers with Gemini</li>
</ol>

<hr />

<h2>Dataset</h2>

<p>
  The dataset used in this example contains simplified sections of
  <strong>Maryland cannabis regulations</strong>, including:
</p>

<ul>
  <li>licensing requirements</li>
  <li>marketing restrictions</li>
  <li>packaging and labeling rules</li>
  <li>product testing requirements</li>
  <li>compliance audits</li>
</ul>

<p>This dataset is used purely for demonstration purposes.</p>

<hr />

<h2>Next Steps</h2>

<p>
  This repository is part of a larger series exploring advanced RAG techniques.
</p>

<p>Upcoming topics include:</p>

<ul>
  <li>BM25 lexical search</li>
  <li>hybrid retrieval pipelines</li>
  <li>result reranking</li>
  <li>contextual retrieval</li>
</ul>

<p>
  These techniques improve retrieval accuracy and are commonly used in production AI systems.
</p>

<hr />

<h2>Author</h2>

<p>
  <strong>Jasmine Anderson</strong>
</p>

<p>
  Building AI systems for regulatory intelligence and data-driven policy analysis.
</p>
