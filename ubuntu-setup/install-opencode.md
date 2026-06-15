# Install OpenCode on Ubuntu

## Install Script (Recommended)

```bash
curl -fsSL https://opencode.ai/install | bash
```

## Alternative Methods

### npm

```bash
npm install -g opencode-ai
```

### Bun

```bash
bun install -g opencode-ai
```

### Homebrew

```bash
brew install anomalyco/tap/opencode
```

### Docker

```bash
docker run -it --rm ghcr.io/anomalyco/opencode
```

## Usage

Navigate to a project and run:

```bash
opencode
```

Run `/init` inside the TUI to have OpenCode analyze your project and create an `AGENTS.md` file.
