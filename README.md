# Alpaca Starter

This repository contains notebooks that request Alpaca market data.

## Obtain API credentials

1. Go to [Alpaca Markets](https://alpaca.markets/).
2. Select **Sign Up**.
3. Create and verify an account.
4. Open the Alpaca dashboard.
5. Use a paper-trading account for this repository.
6. In the dashboard, open **API Keys**.
7. Select **Generate New Keys**.
8. Copy the API key ID and secret key when shown. The secret is not recoverable after the dialog is closed.

Paper credentials and live credentials are distinct. Do not use live credentials unless the code is intended to submit real orders.

## Configure this repository

Create a file named `.env` in the repository root.

```dotenv
API_KEY=your_alpaca_api_key_id
SECRET_KEY=your_alpaca_secret_key
```

The notebooks load these variables as follows:

```python
API_KEY = os.getenv("API_KEY")
SECRET_KEY = os.getenv("SECRET_KEY")
```

Install the required Python packages:

```powershell
python -m pip install alpaca-py pandas plotly python-dotenv ipykernel
```

Run `01_data_ingestion_eda.ipynb` or `02_momentum_strategy.ipynb` from the repository root.

## Credential handling

- Keep `.env` local.
- Do not commit `.env`.
- Do not paste credentials into notebooks, source files, issues, or pull requests.
- Regenerate a key pair immediately if either value is exposed.

## References

- [Alpaca Market Data API: getting started](https://docs.alpaca.markets/us/docs/getting-started-with-alpaca-market-data)
- [Alpaca paper trading](https://docs.alpaca.markets/us/docs/paper-trading)
