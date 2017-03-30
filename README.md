[![PyPI version](https://badge.fury.io/py/fedexdeliverymanager.svg)](https://badge.fury.io/py/fedexdeliverymanager)

# python-fedexdeliverymanager

Python 3 API for [Fedex Delivery Manager](https://www.fedex.com/us/delivery/), a way to track packages.

## Prerequisites

Sign up for Fedex Delivery Manager and verify your address.

## Install

`pip install fedexdeliverymanager`

## Usage

```python
import fedexdeliverymanager

# Establish a session.
# Use the login credentials you use to login to Fedex Delivery Manager via the web.
# A login failure raises a `FedexError`.
session = fedexdeliverymanager.get_session("username", "password")

# Get all packages that Fedex Delivery Manager knows about.
packages = fedexdeliverymanager.get_packages(session)
```

## Caching
Session cookies are cached by default in `./fedexdeliverymanager_cookies.pickle` and will be used if available instead of logging in. If the cookies expire, a new session will be established automatically.

## Development

### Lint

`tox`

### Release

`make release`

### Contributions

Contributions are welcome. Please submit a PR that passes `tox`.

## Disclaimer
Not affiliated with Fedex.
