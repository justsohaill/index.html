# Prospect Research Tool

AI-powered B2B prospect research tool that generates comprehensive sales briefs using Claude. Paste a LinkedIn profile and company website URL to get talking points, pain points, tech stack analysis, fit scores, and personalized outreach templates.

## Features

- Fetches and analyzes company websites for tech stack detection
- Parses LinkedIn profile data for prospect insights
- Generates fit scores (ICP fit, buying urgency, accessibility)
- Creates personalized outreach hooks and email templates
- Identifies role-specific pain points and talking points
- Exports briefs as Markdown files
- Dark mode support
- Editable brief fields — customize before sharing

## Setup

### 1. Get an Anthropic API Key

1. Go to [console.anthropic.com](https://console.anthropic.com/)
2. Sign up or log in
3. Navigate to **API Keys** in the sidebar
4. Click **Create Key** and copy it (starts with `sk-ant-`)

### 2. Clone the Repo

```bash
git clone https://github.com/justsohaill/index.html.git prospect-research-tool
cd prospect-research-tool
```

### 3. Add Your API Key

Create a `.env` file in the project folder:

```bash
echo "ANTHROPIC_API_KEY=sk-ant-your-key-here" > .env
```

Replace `sk-ant-your-key-here` with the key you copied from step 1.

### 4. Install Dependencies

```bash
npm install
```

### 5. Start the Server

```bash
npm start
```

### 6. Open the Tool

Go to [http://localhost:3000](http://localhost:3000) in your browser.

## Usage

1. Enter a **company website URL** (e.g. `https://acme.com`)
2. Optionally paste **LinkedIn profile text** — go to the prospect's LinkedIn profile, select all (Cmd+A), copy, and paste
3. Optionally add their **LinkedIn profile URL**
4. Click **Generate Research Brief**
5. Review, edit, print, copy, or save as Markdown

## Project Structure

```
├── server.js        # Express server (proxies website fetches + Claude API calls)
├── index.html       # Frontend UI
├── package.json     # Dependencies
├── .env             # Your Anthropic API key (not committed)
└── .gitignore       # Ignores node_modules and .env
```

## Configuration

Under **Settings** in the UI, you can choose between:

- **Sonnet 4.6** — higher quality analysis (default)
- **Haiku 4.5** — faster, lower cost

## License

MIT
