# ConTEXT-Explorer

**ConTEXT Explorer** is an open Web-based system for exploring and visualizing concepts (combinations of co-occurring words and phrases) over time in the text documents. **ConTEXT Explorer** is designed to lower the barriers to applying information retrieval and machine learning for text analysis, including:
- preprocessing text with sentencizer and tokenizer in a **Spacy pipline**;
- building **Gensim** word2vec model for discovering similar terms, which can be used to expand queries;
- indexing the cleaned text, and creating a search engine using **Whoosh**, which allows to rank sentences using the Okapi BM25F function;
- visualizing results across time in interactive plots using **Plotly**.

It is designed to be user-friendly, enabling researchers to make sense of their data without technical knowledge. Users may:

- upload (and save) their text corpus, and customize search fields;
- add terms to the query using input from the word2vec model, sentence ranking, or manually;
- check term frequencies across time;
- group terms with "ALL" or "ANY" operator, and compound the groups to form more complex queries;
- view results across time for each query (using raw counts or proportion of relevant documents);
- save and reload results for further analysis; 
- download a subset of a corpus filtered by specified terms.

More details can be found in the user manual below.

## How to install
### Get the app
Clone this repo to your local environment:

    git clone https://github.com/alicia-ziying-yang/conTEXT-explorer.git

### Install required dependencies    
ConTEXT Explorer is developed using Plotly Dash in **Python**. We are using `Python 3.7.5`, and all required packages are listed in `requirement.txt`. To install the packages in your local environment, you need to upgrade `pip` to the newest version and use:

    pip install -r requirements.txt; fi 

### Run the app
- If you want to run ConTEXT Explorer on an **ubuntu server**, use:

      python app.py

  The IP address with app access will be displayed in the output.
  
  If you have issues with the access, try running the code with `nohup`:

      nohup python app.py &
    
  

- If you want to run ConTEXT Explorer on your **local computer**, comment the code for ubuntu server, and uncomment the last line in `app.py`:

       # app.run_server(debug=False, host="0.0.0.0") # ubuntu server    
       app.run_server(debug=False, port="8010") # local test           

  You can then access the app through your browser: http://127.0.0.1:8010

## How to use

[Click here to view the paged PDF version](https://github.com/alicia-ziying-yang/conTEXT-explorer/blob/main/doc/conTEXT_explorer_ui_manual.pdf)

![alt text](https://github.com/alicia-ziying-yang/conTEXT-explorer/blob/1f330277415a54bff35e9dbd00025bb57fe6221d/doc/conTEXT_explorer_ui_manual.png?raw=true)
