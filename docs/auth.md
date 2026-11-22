# Authentication & Security

Trade Screener employs a secure dual-API security model:

1. **Bybit Public API**: Direct read-only requests for market tickers and open interest using `bybitPublicClient` through `PublicRequestQueue`. No private API keys or secrets are ever exposed in the browser.
2. **Bot Private API (`botPrivateClient`)**: Secure connection to your Node.js bot backend.
3. **Session Security**: Bot auth tokens are stored securely in IndexedDB and encrypted using a 4-digit PIN via the Web Crypto API.
