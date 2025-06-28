# Victoria Important Dates MCP

A Model Context Protocol (MCP) server that provides access to Victoria, Australia's important dates and holidays API.

## Features

- Access to Victoria, Australia public holidays and important dates
- MCP-compatible server implementation
- Easy integration with MCP clients
- RESTful API wrapper for Victoria government data

## Installation

```bash
pip install vic-au-important-dates-mcp
```

## Usage

### As an MCP Server

```python
from vic_au_important_dates_mcp import VictoriaImportantDatesMCPServer

# Initialize the server
server = VictoriaImportantDatesMCPServer()

# Start the server
server.run()
```

### Direct API Usage

```python
from vic_au_important_dates_mcp.client import VictoriaImportantDatesClient

# Create a client instance
client = VictoriaImportantDatesClient()

# Get holidays for a specific year
holidays = client.get_holidays(2024)

# Get holidays for a specific date range
holidays = client.get_holidays_range("2024-01-01", "2024-12-31")
```

## Configuration

The package uses environment variables for configuration:

- `VICTORIA_API_BASE_URL`: Base URL for the Victoria API (optional, has defaults)
- `VICTORIA_API_KEY`: API key if required (optional)

## Development

### Setup

1. Clone the repository
2. Install dependencies: `pip install -e .`
3. Set up environment variables if needed

### Running Tests

```bash
python -m pytest
```

## License

MIT License - see LICENSE file for details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Support

For issues and questions, please use the GitHub issues page.
