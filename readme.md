# Extension Test Server

This server hosts Chrome extensions and their update manifests for testing purposes.

## Features

- Hosts Chrome extension (.crx) files
- Provides Chrome extension update manifests (update.xml)
- Configured for HTTPS support (required by Chrome for extension hosting)

## Hosted Extensions

### Hello World Extension
- **Directory**: `src/hello-world-extension/`
- **Extension ID**: `agelionmihjmbckamodklaakoknmndga`
- **Version**: `1.0`
- **Update Manifest**: `/hello-world-extension/update.xml`

See [src/hello-world-extension/README.md](src/hello-world-extension/README.md) for detailed configuration instructions.

## Running the Server

```bash
npm start
```

This will start the server on port 8000 with CORS enabled.

## HTTPS Configuration

Chrome requires HTTPS for extension update manifests and CRX file hosting. See the extension-specific README files for HTTPS setup instructions.

## Dev Container

This repo has a dev container. This means if you open it inside a [GitHub Codespace](https://github.com/features/codespaces), or using [VS Code with the remote containers extension](https://code.visualstudio.com/docs/remote/containers), it will be opened inside a container with all the dependencies already installed.