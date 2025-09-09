# System Overview

## Introduction
The UBI Verification SDK is a lightweight, modular Node.js library for verifying W3C Verifiable Credentials (VCs). It supports both online and offline verification workflows.

## Capabilities
- **Tamper Detection**: Uses cryptographic proof validation.
- **Schema Compliance**: Ensures credentials meet required schemas.
- **Revocation Check**: Utilizes issuer's status registry.
- **Issuer Trust Verification**: Confirms the trustworthiness of credential issuers.

## Architecture
- Built on Fastify, providing a REST API with Swagger documentation.
- Supports extensibility for new verifiers via an interface contract.

## External Dependencies
- **Node.js**: Runtime environment.
- **Fastify**: Web framework.
- **Swagger**: API documentation.
