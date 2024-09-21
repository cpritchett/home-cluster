## Creating a Kubernetes Secret for 1Password Connect

This section provides instructions on how to create a Kubernetes secret for 1Password Connect by grabbing the JSON file, encoding it, and grabbing a token.

### Steps

1. **Grab the JSON file**: Ensure you have the JSON file containing your 1Password Connect credentials. This file is typically named `1password-credentials.json`.

2. **Encode the JSON file**
    ```sh
    cat 1password-credentials.json | base64 | tr '/+' '_-' | tr -d '=' | tr -d '\n' > op-session
    ```

    This command will output a long string of encoded text. Copy this encoded string.


