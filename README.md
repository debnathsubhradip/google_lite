# TinyGoogle

TinyGoogle built with Flask + Bootstrap + Google CSE

> Note: the demo may need some spin up time if nobody has accessed it for a certain period.

## Features

* Search content by Google Custom Search API
* Ignore [GFW](https://en.wikipedia.org/wiki/Great_Firewall) to use google search

## Search Times

There are 4 engines in this demo. Each engine can search 100 times/day.

If the demo run out of search times when you use, please try just another day.

## Requirements

* python 3.5
* flask 0.11.1
* gunicorn 19.6.0
* requests 2.12.1
* flask-bootstrap 3.3.7.0

## Build Setup

1. install requirements

  ```bash
  pip install -r requirements.txt
  ```
2. run

  ```bash
  gunicorn app:app  
  ```

## Config

1. in `data/engine.json`, you can change&add the engine's `key` and `cx` values:

  ```
    {
      "YOUR_ENGINE":{
        "name":"YOUR_NAME",
        "key":"YOUR_API_KEY",
        "cx":"YOUR_ENGINE_ID"
      }
    },
  ```
2. where to get CSE ID and Google API key :

  [Google CSE](https://cse.google.com/) & [Google API Console](https://console.developers.google.com/)
