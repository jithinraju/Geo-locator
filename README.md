# GEO-locator

In this Python script you can input the Domain name and the result will be the IP and the country code from which the domain loads.

IP details are fetching from "ipstack.com". First We need to get a free API key from IPstack by entering your info and use the API key to fetch the details from "ipstack.com".

## Modules user

- socket
- requests

### Code

```python

import requests
import socket
url = input('Enter your domain : ')

try:
    ip = socket.gethostbyname(url)

    checkurl = f'http://api.ipstack.com/{ip}?{API-access_key}
    response = requests.get(checkurl)
    geodata = response.json()
    countryname = geodata['country_name']
    print(f'{url}\n{ip} from {countryname}')
    
except:
    print('Domain is not active')

```


### Result

```bash

Enter your domain : www.google.com
www.google.com
172.217.6.100 from United States

```
