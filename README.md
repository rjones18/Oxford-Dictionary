# Oxford-Dictionary
This code if ran allows you to look up any word you want that is in the Oxford Dictionay. I did this by first importing the `requests`, `dotnev`,  and `os` librarys into my python code. 


```
import requests
import dotenv
import os
```

I obtained my weather API from [Oxford Dictionaries](https://developer.oxforddictionaries.com/documentation). This API is free to use if you select the `Prototype` option and all you have to do to obtain it is to make a account on the Oxford Dictionary website. From this website is where I obtained my API Key. For security purposes I have placed the key into a .env file and only have the varible names I have put for the keys in my code.

Below is my final code:

```
import requests
import dotenv
import os

dotenv.load_dotenv()


app_id = os.environ.get('OXFORD_DICT_ID')
app_key = os.environ.get('OXFORD_DICT_KEY')

word = 'word'

url = f"https://od-api.oxforddictionaries.com:443/api/v2/entries/en-us/{word.lower()}"

headers = {'app_id': app_id, 'app_key': app_key}
response = requests.get(url, headers = headers)

print(f"{word}:", response.json()['results'][0]['lexicalEntries'][0]['entries'][0]['senses'][0]['definitions'][0])

```
