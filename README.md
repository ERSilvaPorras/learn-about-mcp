# Learn About MCP

A comprehensive learning project exploring the **Model Context Protocol (MCP)** - a framework for building AI applications with standardized interfaces for tools, resources, and prompts.

## Overview

This project demonstrates practical implementation of MCP servers and clients using the Python SDK. Learn how to:
- Build MCP servers that expose resources, tools, and prompts
- Create MCP clients that consume server capabilities
- Manage documents, resources, and prompts effectively
- Integrate MCP with LLMs like Claude for enhanced AI interactions

## Project Structure

```
learn-about-mcp/
├── src/
│   ├── client/          # MCP client implementation
│   ├── server/          # MCP server implementation
│   ├── docs/            # Documentation and examples
│   └── tests/           # Unit and integration tests
├── main.py              # Entry point for the project
├── pyproject.toml       # Project configuration and dependencies
└── README.md            # This file
```

## Prerequisites

- Python 3.14 or higher
- uv (recommended) or pip (Python package manager) `curl -LsSf https://astral.sh/uv/install.sh | sh`

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd learn-about-mcp
```

2. Install dependencies using uv (recommended):
```bash
uv sync
```

Or using pip:
```bash
pip install -e .
```

3. Configure environment variables (if needed):
```bash
cp .env.example .env
# Edit .env with your configuration
```

## Dependencies

The project uses:
- **anthropic** (>=0.88.0) - Anthropic SDK for Claude interactions
- **mcp** (>=1.27.0) - Model Context Protocol SDK
- **python-dotenv** (>=1.2.2) - Environment variable management

## Quick Start

Run the main application:
```bash
python main.py
```

## Getting Started

### Building an MCP Server

Create a server in `src/server/` that exposes:
- **Resources** - Shared data structures (documents, configs)
- **Tools** - Functions that the client can invoke
- **Prompts** - Pre-defined prompts for AI interactions

### Building an MCP Client

Implement a client in `src/client/` that:
- Connects to MCP servers
- Discovers available resources, tools, and prompts
- Makes requests to execute tools or retrieve resources

## Usage Examples

### Example 1: Server Setup
```python
# src/server/server.py
from mcp.server import Server

server = Server("my-mcp-server")

# Add resources, tools, and prompts here

server.run()
```

### Example 2: Client Connection
```python
# src/client/client.py
from mcp.client import Client

client = Client()
client.connect("my-mcp-server")
```

## Testing

Run tests with:
```bash
pytest src/tests/
```

## Documentation

Additional documentation and examples are available in `src/docs/`.

## Resources

- [MCP Specification](https://modelcontextprotocol.io/)
- [Anthropic Documentation](https://docs.anthropic.com/)
- [Python MCP SDK](https://github.com/modelcontextprotocol/python-sdk)

## Learning Path

1. **Fundamentals** - Understand MCP core concepts
2. **Server Development** - Build your first MCP server
3. **Client Development** - Create an MCP client
4. **Integration** - Connect servers and clients
5. **Advanced** - Add resources, tools, and prompts

## Contributing

Contributions are welcome! Please:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see LICENSE file for details.

## Authors

- ERSilvaPorras
