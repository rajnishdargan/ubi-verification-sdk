# Environment Variables

The UBI Verification SDK uses several environment variables to configure its behavior. Below is a list of these variables along with their descriptions and example values.

## List of Environment Variables

```env
# Specifies the environment in which the application is running
NODE_ENV=development

# The port number on which the application will run
PORT=3000

# The host address for the application
HOST=0.0.0.0

# API endpoint for Dhiway verifier
DHIWAY_VERIFIER_VERIFICATION_API=https://api.dhiway.com/verify

# API token for Dhiway verifier
DHIWAY_VERIFIER_VERIFICATION_API_TOKEN=your_api_token_here

# Expiry field for Dhiway verifier, defaults to 'validUntil'
DHIWAY_VERIFIER_EXPIRY_FIELD=validUntil
```