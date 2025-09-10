# Service Architecture

## Overview

This section provides an overview of the Verification SDK's architecture, including its components and interactions.

## Architecture Diagram

```mermaid
graph TD;
    A[Provider App] -->|Uses| B(Verification SDK);
    C[Beneficiary App] -->|Uses| B;
    B -->|Exposes| D[Verification API Endpoint];
    D -->|Handles| E[Verification Service];
    E -->|Processes| F[Credential JSON & Config];
    F -->|Returns| G[Verification Result];
    B -->|Built on| H[Fastify Framework];
    H -->|Provides| I[REST API];
```

### Explanation

- **Provider App & Beneficiary App**: These applications interact with the Verification SDK to verify documents.
- **Verification SDK**: Acts as the core component, exposing a REST API for verification.
- **Verification Service**: Processes the verification requests and returns results.
- **Fastify Framework**: Provides the underlying infrastructure for the REST API.

## Sequence Diagram

```mermaid
sequenceDiagram
    participant P as Provider App
    participant B as Beneficiary App
    participant V as Verification SDK
    participant S as Verification Service
    P->>V: Request Verification
    B->>V: Request Verification
    V->>S: Process Verification
    S-->>V: Return Result
    V-->>P: Send Verification Result
    V-->>B: Send Verification Result
    Note over V,S: Handle errors and log processing time
```

### Explanation

- **Request Verification**: Both apps send verification requests to the SDK.
- **Process Verification**: The SDK processes these requests through the Verification Service.
- **Return Result**: Results are returned to the apps, with error handling and logging.

## Data Flow Diagram

```mermaid
graph LR;
    A[Credential JSON & Config] -->|Input| B(Verification Service);
    B -->|Processes| C[Verification Logic];
    C -->|Validates| D[Data Integrity & Compliance];
    D -->|Output| E[Verification Result];
```

### Explanation

- **Input**: Credential JSON and configuration data are input into the Verification Service.
- **Processing**: Data undergoes verification logic and validation.
- **Output**: The final output is the verification result.
