# Hello World Chrome Extension

This directory hosts the hello-world-extension.crx Chrome extension and its update manifest.

## Files

- `update.xml` - Chrome extension update manifest file
- `hello-world-extension.crx` - Chrome extension file (to be added later)

## Extension Details

- **Extension ID**: `agelionmihjmbckamodklaakoknmndga`
- **Version**: `1.0`

## Configuration

### HTTPS Setup

**Important**: Chrome requires HTTPS for hosting extension update manifests and CRX files.

To enable HTTPS for this server:

1. **For Local Development**:
   - Use a tool like [mkcert](https://github.com/FiloSottile/mkcert) to create local SSL certificates
   - Update the server configuration to use HTTPS

2. **For Production Deployment**:
   - Deploy to a platform that provides HTTPS by default (e.g., Azure Static Web Apps, Netlify, Vercel)
   - Or configure your web server (nginx, Apache) with an SSL certificate from Let's Encrypt

3. **Update the update.xml file**:
   - Replace `YOUR_SERVER_DOMAIN` with your actual HTTPS domain
   - Example: `https://example.com/hello-world-extension/hello-world-extension.crx`

### Using the Extension

1. Place the `hello-world-extension.crx` file in this directory
2. Configure your Chrome extension to point to the update manifest URL:
   - Update manifest URL: `https://YOUR_SERVER_DOMAIN/hello-world-extension/update.xml`
3. Chrome will automatically check this URL for updates based on the manifest

## Testing

To test locally with HTTPS:
```bash
# Install sirv-cli with HTTPS support
npm install -g sirv-cli

# Generate local certificates with mkcert (if not already installed)
# mkcert -install
# mkcert localhost

# Run with HTTPS (requires certificate files)
sirv ./src --cors --single --port 8000 --ssl --cert localhost.pem --key localhost-key.pem
```
