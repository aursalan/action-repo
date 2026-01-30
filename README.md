# Action Repo

> A GitHub repository designed to generate real-world repository events (push, pull request, and merge) and forward them to an external system via GitHub Webhooks.

- This repository acts as an event producer in a distributed system setup.
- Any push, pull request, or merge action performed on this repository triggers a GitHub webhook.
- The webhook is configured in the repository settings and sends event payloads to an external Flask API.
- These events are later stored, processed, and visualized through downstream services.

## Table of Contents

1. [Tech Stack and Prerequisites](#1-tech-stack-and-prerequisites)
2. [How Webhooks Are Configured](#2-how-webhooks-are-configured)
3. [How to Use the Project](#3-how-to-use-the-project)

## 1. Tech Stack and Prerequisites

**Platform:** GitHub\
**Webhook Target:** External Flask API\
**Prerequisites:** GitHub account, Basic understanding of GitHub Webhooks

## 2. How Webhooks Are Configured

- A webhook is added via Repository Settings → Webhooks
- The webhook URL points to a Flask API endpoint hosted on Render
- Content type is set to `application/json`
- Relevant events are enabled

## 3. How to Use the Project

Perform any of the following actions:

- Push commits
- Open or merge pull requests

Each action automatically triggers the webhook and propagates data through the system.

