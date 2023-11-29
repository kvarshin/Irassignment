# WILP_IR_Assignment

The assignment is on implementing the ranking techniques on semantic scholar dataset.

# Corpus 

The folder `s2` contains 3 files:

### `s2_doc.json`: All (8K) documents in the corpus. It is a corpus of research papers from the domain of Computer Science. Each research paper has 3 fields:

#### `docno`: A unique document id for each research paper
#### `title`: Title of the document
#### `paperAbstract`: Abstract of the research paper

### `s2_query.json`: All the 100 queries. Each query has 2 fields:

#### `qid`: The unique id of the query
#### `query`: The text of the query

### `s2.qrel`: The relevance values of research papers for each query. The columns are:
#### `qid`
#### `docno`
#### `relevance`: can take values between `4` (highest) to `0` (lowest)

# Running the code

-- The code has been tested with `Python 3.10`, so to ensure that you do not run into any problems related to versions, install and use `Python 3.10` for subsequent steps.

-- The top of the directory contains `main.py` and `requirements.txt`. Run the following command to first install all dependencies from there:
    
    `pip install -r requirements.txt`

-- Run `python main.py`. If everything goes well, you will see the following output:
    
```
Dictionary size: 73759
complete your code
```
    
This means your indexes were successfully created. 

-- Navigate to `s2/intermediate/` folder where the indexes are stored. `s2/intermediate/postings.tsv` is the inverted index file. This postings can be read in memory and used to construct vector representations.