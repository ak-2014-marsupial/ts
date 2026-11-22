# Trade Screener: Hybrid PWA Architecture (v2.0)

Trade Screener is a professional Progressive Web App (PWA) built for crypto traders using Feature-Sliced Design (FSD) architecture. It combines real-time public market screening (Bybit Public API via Request Orchestrator) with a secure private client for managing bot portfolios, risk metrics, and grid limit orders.

## 🚀 Core Features

*   **Trading Dashboard**: Real-time portfolio monitoring (Equity, Wallet Balance, Available Margin, Margin Usage), active positions with Breakeven Price calculation (including Maker/Taker fees), risk in USDT, and grid limit orders.
*   **Bybit Market Screener**: Linear futures and spot tickers screening with filters (turnover, 24h price change, spread) and 5-minute Open Interest (OI) Delta scanner.
*   **Request Orchestrator (`PublicRequestQueue`)**: Constant interval queue with `AbortController` support to prevent API rate limits and CloudFlare blocks.
*   **Secure Session Architecture**: Bot auth token storage in IndexedDB encrypted with a PIN via Web Crypto API.
*   **Observer State Management**: Reactive stores (`PortfolioStore` and `ScreenerStore`) without Redux or Zustand bloat.
*   **Dynamic Theming**: Highly customizable UI with dark mode and generative color systems.

## 🛠 Tech Stack

*   **Framework**: React + Vite + TypeScript.
*   **Architecture**: Feature-Sliced Design (FSD).
*   **State Management**: Observer Pattern.
*   **Styling**: Vanilla CSS with CSS custom properties.
*   **APIs**: Dual-API model (`bybitPublicClient` + `botPrivateClient`).

## 📦 Getting Started

### Prerequisites
*   Node.js (v20+)
*   npm or npm-compatible package manager

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/[your-username]/TradeScreener.git
   cd TradeScreener/client
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Run development server:**
   ```bash
   npm run dev
   ```

---
*Built as a professional hybrid trading screener and portfolio management PWA.*
