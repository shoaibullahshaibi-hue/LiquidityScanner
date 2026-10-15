# Liquidity Scanner — Android MVP

A zero-cost starter Android app for Binance USD-M perpetual futures. It uses public, unauthenticated market-data WebSockets and does not place orders.

## Current features
- Live mark price for BTCUSDT, ETHUSDT, SOLUSDT, BNBUSDT, XRPUSDT
- Visible top-of-book liquidity levels from Binance `depth20@100ms`
- Simple 1-minute market-structure classification (higher highs/higher lows, lower highs/lower lows, or mixed)
- Rule-based illustrative entry, stop-loss, and 1R/2R take-profit levels after a simple candle-break trigger
- No API key, paid data feed, backend, or subscription required

## Build
1. Install Android Studio with JDK 17 support.
2. Open this folder as a project.
3. Let Gradle sync; use Android SDK 35.
4. Run on an Android device/emulator with internet access.

## Important limitations
- This is an MVP source project, not a verified release APK. Build it in Android Studio to produce an APK.
- Visible order-book depth is not a full liquidation heatmap, and displayed walls can move or be spoofed. It only represents the exchange feed and levels returned by the endpoint.
- The structure/entry logic is intentionally basic and not a validated trading strategy. It does not model fees, funding, slippage, leverage, liquidation price, position sizing, or exchange precision filters.
- The WebSocket is closed when the app exits; background service/reconnect handling is not included yet.
- No orders are submitted and no financial advice is provided.
