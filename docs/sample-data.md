### Payload Explanation

The payload in the CURL command is a JSON object containing two main sections:

1. **Credential**: This section includes the Verifiable Credential (VC) data. It contains various fields such as `@context`, `type`, `issuer`, `issuanceDate`, and `credentialSubject`. The `credentialSubject` holds the actual data about the individual, such as `birthyear`, `disability_type`, etc., which are now replaced with placeholders.

2. **Config**: This section specifies the configuration for the verification method and the issuer. The `method` is set to "online", and the `issuerName` is "dhiway", indicating that the verification is done online by the issuer named Dhiway.

### Sample CURL Command

Below is a sample CURL command for the verification API:

```bash
curl --location 'http://localhost:3010/verification' \
--header 'sec-ch-ua-platform: "Linux"' \
--header 'Referer: http://localhost:3000/documentation/static/index.html' \
--header 'User-Agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/136.0.0.0 Safari/537.36' \
--header 'accept: application/json' \
--header 'sec-ch-ua: "Chromium";v="136", "Google Chrome";v="136", "Not.A/Brand";v="99"' \
--header 'Content-Type: application/json' \
--header 'sec-ch-ua-mobile: ?0' \
--data '{
    "credential": { VC Data},
    "config": {
        "method": "online",
        "issuerName": "dhiway"
    }
}'
```