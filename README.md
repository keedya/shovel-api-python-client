# shovel-api-python-client

## Requirements.
Python 2.7 and later.

## Setuptools
You can install the bindings via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install
```

Or you can install from Github via pip:

```sh
pip install git+https://github.com/keedya/shovel-api-python-client.git
```

To use the bindings, import the pacakge:

```python
import python_shovel
```

## Description

API Client Library for [Shovel](https://github.com/keedya/Shovel)(RackHD/OpenStack Coordinator)

## Example

```python
from python_shovel import Configuration
from python_shovel import ApiClient
from python_shovel import GETApi as get_api

def get_config():
    config = Configuration()
    config.host = 'http://localhost:9005/api/1.1'
    config.verify_ssl = False
    config.api_client = ApiClient(host=config.host)
    config.debug = False
    get_api().configget()
    print config.api_client.last_response.data
```


