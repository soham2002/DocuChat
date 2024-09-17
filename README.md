# DocuChat
### DocuChatv1
[Click Here](https://colab.research.google.com/drive/1cefEldBlukCTfm-x_Qpg3hgwompKm1qQ?usp=sharing) to view Google Colab based implimentation of a PDF Chat Bot where the Uploaded PDF is embedded into a VectorDB (here Pinecone) and proper search query to fetch desired answers from the uploaded PDF.

### DocuChatv2
[Click Here](https://docuchat-pdf.streamlit.app/) to view the deployed DocuChat Model with GeminiPro and FAISS VectorEmbedding.

## How to run DocuChatv1?
To use the DocuChatv1 in Google Colab,follow these steps:

 1. Visit the Google colab file by clicking [here](https://colab.research.google.com/drive/1cefEldBlukCTfm-x_Qpg3hgwompKm1qQ?usp=sharing)
 2. Create a copy of the Colab file on your drive
 
 3. Generate Pinecone API Key:
    1. Once logged in, navigate to the API Keys section in the Pinecone dashboard.
    2. Click on Create API Key and copy the generated key.
      
 5. Create a Pinecone Index:
    1. Click on Create Index.
    2. Choose an index name, set the dimension (e.g., 768 for BERT-based models), and specify the metric (e.g., cosine similarity).
    3. Click Create.
 
 6. Change the Index Name to your own Index Name
```bash
pc = Pinecone(api_key=PINECONE_API_KEY)
index_name = pc.Index('ragchat') #change it to your pinecone index name

from langchain.vectorstores import Pinecone as PC

os.environ['PINECONE_API_KEY']

docs_chunks = [t.page_content for t in docs]
pinecone_index = PC.from_texts(
    docs_chunks,
    embeddings,
    index_name='ragchat' #change it to your Pinecone Index

)
```

6. Set Up Hugging Face API
   1. Create a Hugging Face Account:
   2. Go to Hugging Face and sign up or log in.
      
7. Generate Hugging Face Acess Token:
    1. Navigate to the Settings section of your Hugging Face account.
    2. Under Access Tokens, create a new token and copy it.
       
8. Add the API Keys to Colab:
   1. Add all the API Keys to the Secrets section of your Colab File
9. Run all the cells of the Colab File

![Alt text](https://github.com/soham2002/DocuChat/blob/main/static/SCG.png)

## How to run DocuChatv2?
To use the DocuChatv2 in your local system,follow these steps:

1. Install the required Python packages:

    ```bash
    pip install requirements.txt
    ```
2. Create a .env file:
   ```bash
   GEMINI_API_KEY = "Enter your Gemini Api Key"
   ```
4. Run the DocuChatv2 by running the following code in the terminal:

      ```bash
      streamlit run app.py
      ```
5. You are good to go!
![Alt text](https://github.com/soham2002/DocuChat/blob/main/static/DocuChat_SC.png)
