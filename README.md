# Whatsplaid API documentation

This repository contains the public technical contracts for the Whatsplaid API, outgoing webhooks, and Custom Data Connector.

## Interactive documentation

- [Whatsplaid API documentation](https://api.whatsplaid.com/docs/)
- [Whatsplaid website](https://whatsplaid.com/)

## Published specifications

- `whatsplaid_v1.yaml`: REST API for account capabilities, contacts, conversations, messages, human handoff, tickets, products, and orders.
- `whatsplaid_outgoing_webhooks.yaml`: Events sent by Whatsplaid, including payloads, delivery headers, and retry behavior.
- `whatsplaid_connector_contract.yaml`: Contract that external ecommerce, ERP, CRM, or custom systems can implement so Whatsplaid can query customer data.

## Versioning

Each OpenAPI specification declares its own semantic version in `info.version`:

- `PATCH` for backward-compatible corrections and clarifications.
- `MINOR` for backward-compatible additions.
- `MAJOR` for incompatible contract changes.

The OpenAPI specifications are the authoritative public contracts. Integrations should rely on the documented request and response schemas rather than undocumented implementation details.

## Security

Never publish credentials, access tokens, private endpoints, customer data, or examples derived from real accounts. Use only fictional values in public examples.
