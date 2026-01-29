# Installation

## Requirements

- Python 3.12 or higher
- An API key from [Financial Modeling Prep](https://financialmodelingprep.com/developer/docs/)

## Install from PyPI

Using pip:

```bash
pip install fmp-client
```

Using uv:

```bash
uv add fmp-client
```

Using poetry:

```bash
poetry add fmp-client
```

## Install from Source

Clone the repository and install in development mode:

```bash
git clone https://github.com/cbian/fmp-client.git
cd fmp-client
uv sync
```

## Dependencies

The package has minimal dependencies:

- `httpx>=0.27` - Async HTTP client

## Verify Installation

```python
import fmp_client

print(fmp_client.__all__)
# ['AsyncFMPClient', 'FMPAPIError', 'FMPAuthenticationError', ...]
```

## Getting an API Key

1. Sign up at [Financial Modeling Prep](https://financialmodelingprep.com/)
2. Navigate to your dashboard to get your API key
3. Keep your API key secure and never commit it to version control

!!! tip "Environment Variables"
    Store your API key in an environment variable:

    ```bash
    export FMP_API_KEY="your-api-key"
    ```

    Then in Python:

    ```python
    import os
    from fmp_client import AsyncFMPClient

    client = AsyncFMPClient(os.environ["FMP_API_KEY"])
    ```
