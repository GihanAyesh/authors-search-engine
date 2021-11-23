# AUTHORS SEARCH ENGINE

## Contents

- Start the engine
- Software Stack
- Preprocessing
- Advanced features
- File Structure

---

## Start the Engine

npm is required to start the authors engine.
Run the following commands.

```bash
# Installing node modules
npm install

# Run this to start your application 
npm start
# Local:            http://localhost:3000
# On Your Network:  http://192.168.1.101:3000
```

## Software Stack

- Scraping - BeautifulSoup
- Search Engine - elasticsearch
- Frontend - react.js
- UI template - search.ui library
- Backend - node.js

## Preprocessing

The task of the preprocessing is to collect documents related to authors. 

The source used for scraping is [British Council](https://literature.britishcouncil.org)

The following fields are scrapped.
- name
- image (thumbnail)
- birthplace
- genres (writing categories)
- awards 
- work (written books)
- publishers 
- bio (long text field)
- critical perspective (long text field)

A total of 353 documents is collected. The documents are stemmed, tokenized and indexed using elasticsearch.

## Advanced Features

1. Filtering can be done using the following fields.
- genres 
- publishers

2. Sorting can be done using the following fields.
- genres 

## File Structure

- documents - The corpus of 353 authors is saved here in csv format
- public - favicon and web page name is defined
- src - config - config helper.js - controllers are defined, engine.json - configuration file
- App.js - The React app is defined
- package.json - The installed packages
- writer_scraper.ipynb - The scrapping script