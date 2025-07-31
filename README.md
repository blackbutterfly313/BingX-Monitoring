---
title: bingx-monitoring
emoji: 📊
colorFrom: pink
colorTo: green
sdk: gradio
pinned: false
tags:
- trading
- dashboard
- bingx
- classifier
- gradio
sdk_version: 5.39.0
---

# BingX Monitoring Dashboard

Welcome to the **Nakhoda4X Pro** dashboard, a Gradio-based application for monitoring your BingX trading portfolio and classifying images (e.g., hotdog detection). This Space provides real-time insights into your trading activity and a fun image classification feature.

## Features
- **Trading Dashboard**: Displays total balance, open trades, today's profit, and risk exposure using BingX API data.
- **Portfolio Allocation**: Visualizes your portfolio distribution with a doughnut chart.
- **Monthly Performance**: Tracks profit/loss trends over time with a line chart.
- **Trading Activity**: Lists open and recent closed trades in a table.
- **API Management**: Securely manage your BingX API credentials within the app.
- **Hot Dog Classifier**: Classify uploaded images as "hot dog" or "not hot dog" using a pre-trained model.

## Prerequisites
- A BingX account with API key and secret (ensure permissions include Spot Trading, Perpetual Futures Trading, and Read access).
- Stable internet connection to fetch data from BingX API.

## Setup Instructions
1. **Access the Space**: Visit [https://huggingface.co/spaces/EricSam/bingx-monitoring](https://huggingface.co/spaces/EricSam/bingx-monitoring).
2. **Enter Credentials**: Click "Manage API Credentials" in the Trading Dashboard, input your BingX API key and secret, and save them.
3. **Sync Data**: Use the "Sync Now" or "Refresh" button to fetch and display your trading data.
4. **Explore Classifier**: Switch to the "Hot Dog Classifier" tab, upload an image, and classify it.

## Troubleshooting
- **Error: "Failed to sync with BingX API"**: Ensure your API credentials are valid, permissions are correct, and your network allows API requests. Check the browser console (F12) or Space logs for details. Refer to [BingX API Documentation](https://bingx-api.github.io/docs/) for support.
- **Invalid JSON Response**: If you see "Unexpected token 'E', 'Entry not found'", verify credentials, permissions, or contact BingX support (broker@bingx.com) with your API key ID.
- **Classifier Not Working**: If the hotdog classifier fails with a "RuntimeError" about missing frameworks, ensure `torch` is installed. Update `requirements.txt` to include `torch==2.3.0` and redeploy the Space.
- **Chart Issues**: Ensure Gradio SDK version 5.39.0 is compatible; update if necessary.

## Configuration
- **SDK**: Gradio 5.39.0
- **Dependencies**: Managed via `requirements.txt` (gradio==5.39.0, transformers==4.35.2, requests==2.28.1, torch==2.3.0)
- **Last Updated**: 09:43 PM +08, Thursday, July 31, 2025

## Notes
- API credentials are stored in memory for the session only and reset on page refresh.
- The "New Trade" button is a placeholder and requires additional implementation for full functionality.
- For configuration reference, see [Hugging Face Spaces Config](https://huggingface.co/docs/hub/spaces-config-reference).

## Contributions
Feel free to fork this Space, submit issues, or suggest enhancements on the [GitHub repository](https://huggingface.co/spaces/EricSam/bingx-monitoring) or via email.
