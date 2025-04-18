# Secure Note + Tools

This is a simple HTML-based utility for encrypting/decrypting notes and performing basic text manipulation. It runs entirely in your browser using the Web Crypto API for encryption.

## Features

*   **Encrypt:** Securely encrypt messages using AES-GCM with a password.
*   **Decrypt:** Decrypt messages that were previously encrypted using this tool.
*   **Replace Characters:** Swap all occurrences of one character with another within a given text.

## How to Use

1.  Save the `index.html` file.
2.  Open the [`index.html`](index.html) file in your web browser.
3.  Alternatively, access the live demo at [securenote.asanchez.dev](https://securenote.asanchez.dev).
4.  Use the tabs at the top to switch between the different tools: Encrypt, Decrypt, and Replace Characters.

### Encrypt

1.  Go to the "Encrypt" tab.
2.  Enter the message you want to encrypt in the text area.
3.  Enter a strong password in the password field.
4.  Click the "Encrypt" button.
5.  The encrypted message (a base64 encoded string) will appear in the output box below. Copy this text to save or share it.

### Decrypt

1.  Go to the "Decrypt" tab.
2.  Paste the previously encrypted message (the base64 string) into the text area.
3.  Enter the *exact same password* used for encryption.
4.  Click the "Decrypt" button.
5.  The original message will appear in the output box. If the password is incorrect or the data is corrupted, an error message will be shown.

### Replace Characters

1.  Go to the "Replace Characters" tab.
2.  Enter the text you want to modify in the text area.
3.  Enter the single character you want to replace in the "From" field.
4.  Enter the single character you want to replace it with in the "To" field.
5.  Click the "Replace" button.
6.  The modified text will appear in the output box.


## Security Notes

*   **Client-Side Operation:** This tool runs entirely in your web browser. No data, including your messages or passwords, is ever sent to any external server. All processing happens locally on your machine.
*   **Strong Encryption:** Encryption uses the standard Web Crypto API, specifically AES-GCM, which is a widely recognized and secure authenticated encryption algorithm. The key is derived from your password using PBKDF2 with 100,000 iterations and SHA-256, adding significant protection against brute-force attacks.
*   **Password Security:** The security of your encrypted message relies heavily on the strength of your password. Use a long, complex, and unique password.
*   **No Recovery:** If you forget your password, there is absolutely no way to recover the encrypted message. Store your password securely.