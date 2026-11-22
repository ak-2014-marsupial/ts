# About Trade Screener

Trade Screener is a professional Progressive Web App (PWA) designed for crypto traders, built using Feature-Sliced Design (FSD) architecture.

## Core Purpose
The application provides:
1. **Trading Dashboard**: Real-time bot portfolio monitoring, margin usage, active positions with Breakeven Price calculation (including fees), risk in USDT, and grid limit orders.
2. **Bybit Market Screener**: Linear futures and spot market screening with advanced filters (turnover, volatility, spread) and Open Interest (OI) Delta scanning.
3. **Request Orchestrator**: Safe public API queue with constant interval T and `AbortController` cancellation.
4. **Secure Architecture**: Dual-API model (`bybitPublicClient` + `botPrivateClient`) with encrypted token storage.
