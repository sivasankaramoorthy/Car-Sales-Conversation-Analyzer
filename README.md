# Car-Sales-Conversation-Analyzer
Car Sales Conversation Analyzer
This project is a Streamlit web application designed to analyze car sales conversations between customers and salespersons. The application extracts relevant customer requirements, discussed company policies, and customer objections, and provides sentiment analysis on the conversations. The application uses the LLaMA 2 model for natural language processing and is integrated with Hugging Face for model management.

Features
Extract Customer Requirements: 
                  Identify the car brand, type, fuel type, color, distance traveled, make year, and transmission type from conversation transcripts.
Company Policies Extraction:
                  Detect discussions about company policies such as free RC transfer, money-back guarantees, free RSA, and return policies.
Customer Objections Identification: 
                  Recognize customer objections related to refurbishment quality, car issues, pricing, and customer experience.
Sentiment Analysis: 
                  Analyze the sentiment of the conversation (positive, negative, or neutral) using the VADER sentiment analysis tool.
Visualization:
                  Provides bar charts summarizing extracted information like car types, colors, and objections.
Support for Multiple File Types: 
                  Upload and process conversation transcripts in both text and PDF formats.
Downloadable JSON: 
                  Extracted information can be downloaded as JSON files.
Installation Requirements
>Python 3.x
>Google Colab (for running the notebook)

The following Python packages are required:
>transformers
>torch
>streamlit
>langchain
>PyMuPDF
>nltk
>matplotlib
>pandas
>pyngrok

Setup Instructions
Clone the repository:
Code:
git clone https://github.com/sivasankaramoorthy/Car-Sales-Conversation-Analyzer.git
cd Car-Sales-Conversation-Analyzer

Install dependencies:
Code:
pip install transformers torch streamlit langchain PyMuPDF nltk matplotlib pandas pyngrok
Login to Hugging Face: Ensure that you have a Hugging Face account and use your token to authenticate.

Code:
from huggingface_hub import login
login(token="your_huggingface_token")

Run the Streamlit Application:

Code:
streamlit run app.py
Set Up Ngrok for Public Access:

Code:
ngrok authtoken your_ngrok_authtoken
ngrok connect 8501
Access the Application: After setting up Ngrok, the application will be available at a public URL provided by Ngrok.

Usage
Upload Transcripts:
              Upload conversation transcripts in .txt or .pdf format.
Extract Information:
              Click on the button corresponding to each file to extract customer requirements, policies discussed, and objections.
Sentiment Analysis:
              The sentiment of the conversation will be automatically analyzed and displayed.
Visualizations:
              View aggregated data in the form of bar charts.
Download Results:
              Download the extracted information as JSON files.
Example
Here’s an example of how to use the application:

Upload a file: Select a .txt or .pdf file containing the conversation transcript.
View Transcript: The conversation will be displayed in a text area.
Extract Information: Click the "Extract Information" button.
View Results: The extracted data will be displayed in JSON format and can be downloaded.
Visualizations: View charts summarizing the extracted information.

Development
Model Loading and Usage
The application loads the meta-llama/Llama-2-7b-chat-hf model from Hugging Face to generate and analyze text.

Key Functions
get_prompt(): Creates a structured prompt for the model.
generate(): Generates responses from the model.
extract_information(): Extracts JSON-formatted information from the conversation text.
analyze_sentiment(): Analyzes the sentiment of the conversation text.
aggregate_data(): Aggregates extracted data for visualization.
extract_text_from_pdf(): Extracts text from PDF files.
create_bar_chart(): Creates bar charts for visualization.


License
This project is licensed under the MIT License. See the LICENSE file for more details.

Acknowledgements
Hugging Face for providing the LLaMA 2 model.
Ngrok for providing public URLs for local applications.
Streamlit for the interactive web application framework.
NLTK for sentiment analysis tools.
