# MSoneAPI
Unofficial API for [malayalamsubtitles.org](https://malayalamsubtitles.org) powered by [FastAPI](https://fastapi.tiangolo.com/)

## API

### End points

For normal query
````
https://msoneapi.up.railway.app/{query}
````

To fetch the synopsis
````
https://msoneapi.up.railway.app/synopi/{msone_release_number}
````
Test the API [here](https://msoneapi.up.railway.app/test/search)

### Example for Python

``` python
import requests

headers = {'User-Agent': 'Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/108.0.0.0 Safari/537.36',
           'accept': 'application/json',
           }

s = requests.Session()
s.headers.update(headers)

def get_results(query):
    response = s.get(f'https://msoneapi.up.railway.app/{query}', headers=headers)
    results = response.json()
    return results
        
def get_synopsis(query):
    response = s.get(f'https://msoneapi.up.railway.app/synopi/{query}', headers=headers)
    results = response.json()
    return results
```
## Telegram Bot

#### Test the live bot  <a href="https://t.me/msonesubsbot" ><img src="https://img.shields.io/badge/Test%20Here-MSone%20Bot-blue.svg?logo=telegram" /> </a>

#### For example code, visit [MSone Bot](https://github.com/anzilr/MSoneBot)
