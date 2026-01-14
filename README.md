# n8n URL Shortener

This project is a backend automation system built using n8n that converts long URLs into shortened URLs.

The system exposes a webhook endpoint that accepts a long URL, processes it through an automation workflow, and returns a shortened URL using a URL shortening service.

---

## Project Overview

The goal of this project is to demonstrate how an automation-first backend can be designed using n8n without building a traditional server-side application.

Instead of using a custom backend framework, the entire logic is handled through:
- Webhooks
- API integration
- Data transformation
- Automated response handling

This makes the system lightweight, scalable, and easy to maintain.

---

## How It Works

1. A client sends a POST request containing a long URL to the n8n webhook.
2. The webhook triggers an automation workflow.
3. The workflow calls a URL shortening API.
4. The shortened URL is extracted and formatted.
5. A clean JSON response is returned to the client.

---

## Workflow Structure

The n8n workflow follows these steps:

- Webhook node receives the request
- HTTP Request node sends the long URL to the URL shortening API
- Set / Code node formats the response
- Respond to Webhook node returns the final shortened URL

---

## Tech Stack

- n8n (Automation platform)
- Webhooks
- External URL Shortening API
- JSON-based request and response handling

---

## Frontend UI

A separate frontend UI has been built to interact with this backend.

Frontend repository:
https://github.com/Masud744/url-shortener-ui

Live UI:
https://masud744-url-shortener.netlify.app/

The frontend is a static website hosted on GitHub Pages and communicates with this backend using the webhook endpoint.

---

## Architecture

Frontend (Static UI)  
→ n8n Webhook  
→ URL Shortening API  
→ JSON Response  

The frontend and backend are intentionally separated to follow a clean, real-world architecture.

---

## Notes

- No API keys or secrets are exposed in this repository.
- All sensitive credentials are securely stored inside n8n.
- This project is intended for learning, demonstration, and portfolio use.
