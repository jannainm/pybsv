# pybsv
  
[![PyPI version](https://badge.fury.io/py/pybsv.svg)](https://badge.fury.io/py/pybsv)

Wrapping `bitsv` - https://github.com/AustEcon/bitsv

**Description:** An easy to use Python BSV library.

**Install:**

```bash
pip install pybsv
```

**Usage**:

```python
from pybsv import PyBSVClient
# SUPPORTED_NETWORKS = [MAIN_NETWORK_TYPE, SCALING_NETWORK_TYPE, TEST_NETWORK_TYPE]
client = PyBSVClient('Your WIF Private Key Here', network=pybsv.TEST_NETWORK_TYPE)
# SUPPORTED_CURRENCIES = [BSV_CURRENCY_KEY, USD_CURRENCY_KEY]
client.get_balance(pybsv.BSV_CURRENCY_KEY)

from pybsv import PyBSVClient, BSV_CURRENCY_KEY, USD_CURRENCY_KEY, TEST_NETWORK_TYPE
# SUPPORTED_NETWORKS = [MAIN_NETWORK_TYPE, SCALING_NETWORK_TYPE, TEST_NETWORK_TYPE]
client = PyBSVClient('Your WIF Private Key Here', network=TEST_NETWORK_TYPE)
# SUPPORTED_CURRENCIES = [BSV_CURRENCY_KEY, USD_CURRENCY_KEY]
print(client.get_balance(BSV_CURRENCY_KEY))
print(client.get_address())
trans_id = client.send_bsv('Destination Wallet Address Here', 0.10, USD_CURRENCY_KEY) # Send $0.10 worth of BSV
print(trans_id)
```

**Upload to PyPi:**

```bash
python setup.py sdist
python setup.py bdist_wheel
twine upload dist/*whl dist/*gz
```

*Do this from the root of this project.
