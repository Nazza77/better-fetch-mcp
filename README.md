# 🕸️ Better Fetch MCP Server

![fetch mcp logo](./logo.jpg)

This MCP server provides functionality to fetch web content in various formats, including HTML, JSON, plain text, and Markdown. This improved version offers Windows compatibility and simplified installation.

## 🧰 Tools

The following tools are available for fetching and processing web content:

### **1. `fetch_html` 🖼️**
- **Purpose**: Fetches and returns raw HTML content from any URL.
- **Input**:
    - `url` (string, required): URL of the website to fetch
    - `headers` (object, optional): Custom headers for the request
- **Output**: Raw HTML content of the webpage.

### **2. `fetch_json` 📊**
- **Purpose**: Fetches and parses JSON data from any URL.
- **Input**:
    - `url` (string, required): URL of the JSON resource
    - `headers` (object, optional): Custom headers for the request
- **Output**: Parsed JSON object.

### **3. `fetch_txt` 📝**
- **Purpose**: Fetches and returns clean plain text content, removing HTML tags and scripts.
- **Input**:
    - `url` (string, required): URL of the website to fetch
    - `headers` (object, optional): Custom headers for the request
- **Output**: Plain text content of the webpage.

### **4. `fetch_markdown` ✍️**
- **Purpose**: Fetches content and converts it to well-formatted Markdown.
- **Input**:
    - `url` (string, required): URL of the website to fetch
    - `headers` (object, optional): Custom headers for the request
- **Output**: Markdown representation of the webpage content.

## 📥 Installation

### Option 1: Direct usage via pnpx (recommended)

```bash
# Use directly without installation
pnpx github:Nazza77/better-fetch-mcp
```

### Option 2: Direct usage via npx

```bash
# Use directly without installation
npx -y github:Nazza77/better-fetch-mcp
```

### Option 3: Local installation using pnpm

```bash
# Clone the repository
git clone https://github.com/Nazza77/better-fetch-mcp.git
cd better-fetch-mcp

# Install dependencies using pnpm
pnpm install

# Build the server using pnpm
pnpm build

# Run the server using pnpm
pnpm start
```

## 🚀 Usage with Claude Desktop or other MCP clients

Add this configuration to your configuration file:

### Using pnpx (recommended)

```json
{
  "mcpServers": {
    "better-fetch": {
      "command": "pnpx",
      "args": ["github:Nazza77/better-fetch-mcp"]
    }
  }
}
```

### Using npx

```json
{
  "mcpServers": {
    "better-fetch": {
      "command": "npx",
      "args": ["-y", "github:Nazza77/better-fetch-mcp"]
    }
  }
}
```

## ✨ Features

- Fetches web content using modern fetch API.
- Supports custom headers for requests.
- Provides content in multiple formats: HTML, JSON, plain text, and Markdown.
- Uses JSDOM for HTML parsing and text extraction.
- Uses TurndownService for HTML to Markdown conversion.
- **Windows compatible** (added shx for build scripts).
- **Directly executable** via pnpx or npx without prior installation.

## 👨‍💻 Development

- Run `pnpm dev` to start the TypeScript compiler in watch mode.
- Use `pnpm test` to run the test suite.

## 🔄 Changes in this version

- Added Windows compatibility.
- Added `bin` property for direct execution with pnpx/npx.
- Updated dependencies (including jsdom to version 26.0.0).
- Improved logging for easier debugging.

## 📄 License

This project is licensed under the MIT License.
