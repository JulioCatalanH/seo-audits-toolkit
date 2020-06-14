# SEOToolkit

![](examples/example.png)

## Installation

You need **Python3**

```Bash
git clone https://github.com/StanGirard/SEOToolkit
cd SEOToolkit
```

Then install dependencies

```Bash
pip install -r requirements.txt
```

## Running Flask

```Bash
python3 flask_api
```

This will expose two endpoints:
- `localhost:5000/api/graph`
- `localhost:5000/api/headers`

### Parameters

#### Graphs

-  `/api/graph?url=https://primates.dev` will crawl the website and respond with the graph as html
-  `/api/graph?url=https://primates.dev&redo=True` will force the crawling. Doesn't crawl if less than 24 hours
-  `/api/graph?url=https://primates.dev&max=10` stops after visiting 10 pages. (Default=500)

#### Headers

- `/api/headers?url=https://primates.dev` returns all the headers of the page

```JSON
{
  "h1": {
    "count": 0, 
    "values": []
  }, 
  "h2": {
    "count": 15, 
    "values": [
      "Help fight diseases with your computer", 
      "A Twitter Crawler and News Indexer", 
      "Find every social account of a user", 
      "How to point a domain name to a server?", 
      "What is a Sitemap?", 
      "All you need to know about Corona", 
      "Find all URLs of a website in a few seconds - Python", 
      "Render games directly in your browser - BabylonJS", 
      "Brave says no to error 404", 
      "DDOS with a crapy computer - Slowloris Attack", 
      "Parsing an API XML Response Data - Python", 
      "What is a smart contract?", 
      "Twint - A Twitter scraper that rocks", 
      "A quick introduction to Elastic Stack - ELK", 
      "Sharding, Ethereum's solution to scaling up"
    ]
  }, 
  "h3": {
    "count": 4, 
    "values": [
      "Featured Posts", 
      "Sharding, Ethereum's solution to scaling up", 
      "10 Github Repositories you should check!", 
      "Brave - A Web Browser that pays its users and respects privacy"
    ]
  }, 
  "h4": {
    "count": 1, 
    "values": [
      "Sign Up To The Newsletter"
    ]
  }, 
  "h5": {
    "count": 2, 
    "values": [
      "Subscribe to Primates", 
      "Newsletter"
    ]
  }, 
  "h6": {
    "count": 0, 
    "values": []
  }
}
```

## TODO

- [ ] Not downloading images when they are linked
- [ ] Async requests
- [ ] Implement Scrapy for better perf

Have fun ! 
