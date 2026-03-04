# rag-for-ai-
Description
This project showcase the implementation of an advanced RAG system that uses Objectbox vectordatabse and Groq's LLAM3 model as an llm to retrieve information from different PDF documents.
Steps:

I have used the PyPdfDirectoryLoader from the langchain_community document loader to load the PDF documents from the us-census-data directory.
transformed each text into a chunk of 1000 using the RecursiveCharacterTextSplitter imported from the langchain.text_splitter
stored the vector embeddings which were made using the HuggingFaceBgeEmbeddings using the ObjectBox vector store.
setup the llm ChatGroq with the model name Llama3-8b-8192
Setup ChatPromptTemplate
Setup vector_embedding function to enbedd the documents and store them in the ObjectBox vectorstore
finally created the document_chain and retrieval_chain for chaining llm to prompt and retriever to document_chain respectively
#Libraries Used
langchain==0.1.20
langchain-community==0.0.38
langchain-core==0.1.52
langchain-groq==0.1.3
langchain-objectbox
python-dotenv==1.0.1
pypdf==4.2.0
Installation
#Prerequisites
Git
Command line familiarity
Clone the Repository: git clone https://github.com/NebeyouMusie/End-to-End-RAG-Project-using-ObjectBox-and-LangChain.git
Create and Activate Virtual Environment (Recommended)
python -m venv venv
source venv/bin/activate
Navigate to the projects directory cd ./End-to-End-RAG-Project-using-ObjectBox-and-LangChain using your terminal
Install Libraries: pip install -r requirements.txt
Navigate to the app directory cd ./app using your terminal
run streamlit run app.py
open the link displayed in the terminal on your preferred browser
As I have already embedded the documents you don't need to click on the Embedd Documents button/ But, if it's not working then you need to click on the Embedd Documents button and wait until the documnets are processed
Enter your question from the PDFs found in the us-census-data directory
