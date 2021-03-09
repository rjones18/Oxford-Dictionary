# Oxford-Dictionary
This code if run allows you to look up any word you want that is in the Oxford Dictionary. I did this by first importing the `requests`, `dotnev`,  and `os` librarys into my python code. 


```
import requests
import dotenv
import os
```

I obtained my weather API from [Oxford Dictionaries](https://developer.oxforddictionaries.com/documentation). This API is free to use if you select the `Prototype` option and all you have to do to obtain it is to make a account on the Oxford Dictionary website. From this website is where I obtained my API Key. For security purposes I have placed the key into a .env file and only have the varible names I have put for the keys in my code.

Below is the information that returns when the code is run:

![Dictionary](https://github.com/rjones18/Images/blob/main/Dictionary.png)
