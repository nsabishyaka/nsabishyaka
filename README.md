# Community Health Hub - n8n Workflows

Automated n8n workflows for daily background aggregation, search log processing, and threshold alert triggers.

## Overview

This repository contains n8n automation pipelines designed to process query logs, analyze key service trends, and generate alerts when critical thresholds are exceeded.

## Features

- **Daily Scheduled Execution:** Automatically triggers processing tasks on a nightly schedule.
- **Data Aggregation:** Pulls raw query data from Google Sheets or HTTP API endpoints.
- **Keyword Analysis:** Evaluates log entries for specific tracked health and service keywords.
- **Automated Alerting:** Flags active alerts when request counts meet or exceed defined threshold criteria.

## Workflow Setup

1. **Schedule Trigger:** Set to execute daily at midnight.
2. **Data Fetching:** Connect your data source (Google Sheets or HTTP Request node).
3. **JavaScript Code Node:** Processes array items, formats dates, counts tracked keywords, and outputs a structured summary.
4. **Alert Action:** Connect downstream nodes (e.g., Email, Slack, or Webhook) conditioned on `triggerAlert`.

## License

MIT
