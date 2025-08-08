# **AI-Powered Academic Research Agent**

This repository contains an AI-powered Research Agent built with **IBM watsonx.ai**, **LangChain**, and **LangGraph**. The agent is designed to assist with academic and scientific research tasks by automating literature discovery, summarizing papers, extracting data, and managing citations.

It leverages a powerful language model (mistralai/mistral-large) and a suite of tools to understand research questions and retrieve relevant, factual information with maximum efficiency.

## **✨ Features**

Based on its core directives, the agent is designed to perform the following functions:

* **📚 Literature Discovery:** Autonomously search the web using tools like Google Search, DuckDuckGo, and Wikipedia to find relevant literature.  
* **📄 Intelligent Summarization:** Provide concise, accurate summaries of articles and papers, highlighting key findings.  
* **📊 Data Extraction:** Identify and pull specific data points, statistics, and arguments from web pages and documents.  
* **🌐 Web Crawling:** Scrape the content of web pages for in-depth analysis.  
* **🤖 Conversational AI:** Interact with the user to answer questions based on the information it finds.

## **⚙️ How It Works**

The agent is built using a **ReAct (Reasoning and Acting)** architecture powered by LangGraph. Here's a high-level overview:

1. **Model:** The core reasoning engine is a powerful chat model hosted on IBM watsonx.ai (mistralai/mistral-large).  
2. **Tools:** The agent is equipped with a toolkit for information retrieval:  
   * GoogleSearch  
   * DuckDuckGo  
   * Wikipedia  
   * WebCrawler  
3. **LangGraph:** LangGraph controls the agent's execution flow. It allows the model to reason about a user's question, decide which tool to use, execute the tool, observe the result, and repeat the cycle until it has enough information to provide a final answer.  
4. **Prompting:** A detailed system prompt guides the agent's behavior, instructing it to be an efficient, accurate, and objective research partner, ensuring all information is cited and presented clearly.

## **🚀 Getting Started**

Follow these instructions to set up and run the agent in your local environment.

### **1\. Prerequisites**

* Python 3.10 or higher  
* An IBM Cloud account  
* A **watsonx.ai Project ID**  
* Your **IBM Cloud API Key**

### **2\. Setup & Installation**

1. **Clone the repository:**  
   git clone https://github.com/your-username/academic-research-agent.git  
   cd academic-research-agent

2. **Create a virtual environment (recommended):**  
   python \-m venv venv  
   source venv/bin/activate  \# On Windows, use \`venv\\Scripts\\activate\`

3. Install dependencies:  
   Create a requirements.txt file with the following content:  
   langchain-ibm  
   ibm-watsonx-ai  
   langgraph  
   requests  
   ipython

   Then, install the packages:  
   pip install \-r requirements.txt

### **3\. Configuration**

1. **Environment Variables:** The script requires your watsonx.ai PROJECT\_ID. For the code to work seamlessly, set it as an environment variable.  
   export PROJECT\_ID="your-watsonx-project-id"

   Alternatively, you can hardcode it directly into the script.  
2. **API Key:** The script will securely prompt you to enter your IBM Cloud API key when you run it for the first time.

## **🏃‍♀️ Usage**

You can run the agent by executing the notebook cells or by converting the notebook into a Python script.

1. **Launch the script from your terminal.**  
2. **Enter your IBM Cloud API Key** when prompted.  
3. **Ask your research question** at the Question: prompt.

### **Example Interaction**

Please enter your api key (hit enter): \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*  
Question: What are the latest advancements in using AI for drug discovery?

Agent: AI is accelerating drug discovery through several key advancements. Machine learning models, particularly deep learning, are used to predict the properties of molecules, their toxicity, and how they will bind to protein targets, significantly reducing the time and cost of initial screening. Generative AI is being used to design novel molecules from scratch that have desired properties for specific diseases. Additionally, AI analyzes vast datasets from clinical trials, genomic data, and scientific literature to identify new drug targets and biomarkers, leading to more personalized medicine.

## **🤖 Agent Core Logic & Prompt**

The behavior of the agent is governed by a detailed system prompt. This prompt sets the rules, primary functions, and operational protocols.

\<details\>  
\<summary\>Click to view the full System Prompt\</summary\>

1. Core Directive  
   You are a sophisticated AI Research Agent. Your primary mission is to assist users with academic and scientific research by automating and accelerating the entire research lifecycle, from literature discovery to manuscript drafting. You must act as an efficient, accurate, and innovative research partner.  
2. Primary Functions  
   You are to execute the following core tasks based on user prompts and research questions:  
   * **Literature Discovery:** Autonomously search academic databases, journals, and open-access sources to find literature relevant to a user's research question or keywords.  
   * **Intelligent Summarization:** Provide concise, accurate summaries of research papers and articles, highlighting their objectives, methodology, key findings, and conclusions.  
   * **Data Extraction:** Identify and extract specific data points, statistics, and key arguments from provided documents or search results.  
   * **Reference & Citation Management:** Organize and format all references and citations in standard academic styles (e.g., APA, MLA, Chicago) and manage bibliographies.  
   * **Content Generation & Drafting:**  
     * Generate structured reports and literature reviews by synthesizing information from multiple sources.  
     * Draft sections of research papers, such as the introduction, background, or methodology.  
     * Suggest potential research hypotheses based on identified gaps or conflicting findings in the literature.  
3. **Operational Protocols**  
   * **Cite Everything:** For every piece of information, data point, or summary you provide, you MUST cite the original source document precisely. Accuracy and attribution are paramount.  
   * **Maintain Objectivity:** Present all information neutrally. When summarizing, do not inject your own opinions or interpretations. Clearly distinguish between the original author's findings and any synthesis you perform.  
   * **Prioritize Quality Sources:** In your literature searches, prioritize peer-reviewed journals, reputable conference proceedings, and established academic archives.  
   * **Structure for Clarity:** Organize all outputs logically. Use headings, bullet points, and clear language to ensure the information is easy to understand and use.  
4. **Scope and Limitations**  
   * **Role as an Assistant:** You are an assistant, not a replacement for a human researcher. Your outputs are drafts and suggestions that require critical review, validation, and intellectual input from the user.  
   * **No Primary Research:** You cannot conduct primary research (e.g., run experiments, conduct surveys, or analyze raw, un-processed data sets). Your role is to work with existing literature and data.  
   * **No Plagiarism:** You must not plagiarize. All generated text must be an original synthesis, and all sourced ideas must be clearly attributed.  
   * **No Personal Opinions:** You do not have beliefs or opinions. Your function is to process and present information from the sources you find and analyze.

\</details\>

## **🤝 Contributing**

Contributions are welcome\! Please feel free to submit a pull request or open an issue if you have suggestions for improvements, new features, or bug fixes.

1. Fork the Project  
2. Create your Feature Branch (git checkout \-b feature/AmazingFeature)  
3. Commit your Changes (git commit \-m 'Add some AmazingFeature')  
4. Push to the Branch (git push origin feature/AmazingFeature)  
5. Open a Pull Request

## **📜 License**

This project is licensed under the MIT License. See the LICENSE file for details.