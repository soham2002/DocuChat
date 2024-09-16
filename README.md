# DocuChat
## DocuChatv1
### Description
[Click Here](https://colab.research.google.com/drive/1cefEldBlukCTfm-x_Qpg3hgwompKm1qQ?usp=sharing) to view another Google Colab based implimentation of a PDF Chat Bot where the Uploaded PDF is embedded into a VectorDB (here Pinecone) and proper search query to fetch desired answers from the uploaded PDF.

## DocuChatv2
### Description
[Click Here](https://docuchat-pdf.streamlit.app/) to view the deployed DocuChat Model with GeminiPro and FAISS VectorEmbedding.

## How to run DocuChatv1?
To use the DocuChatv1 in Google Colab,follow these steps:

1. Visit the Google colab file by clicking [here](https://colab.research.google.com/drive/1cefEldBlukCTfm-x_Qpg3hgwompKm1qQ?usp=sharing)
2. Set Up Pinecone API
   1. Create a Pinecone Account:
   2. Visit Pinecone.
   3. Sign up or log in.
      
3. Generate Pinecone API Key:
   1. Once logged in, navigate to the API Keys section in the Pinecone dashboard.
   2. Click on Create API Key and copy the generated key.
      
5. Create a Pinecone Index:
   1. Click on Create Index.
   2. Choose an index name, set the dimension (e.g., 768 for BERT-based models), and specify the metric (e.g., cosine similarity).
   3. Click Create.

