# 📊 Secure Financial Dashboard

A secure, fully client-side, multi-currency financial tracker designed for privacy. It runs entirely in the browser via GitHub Pages, with all local data encrypted at rest using industry-standard cryptography. No external servers, no tracking, and zero database dependencies.

---

## 🔒 Security Architecture

This application is built with security and data privacy at its core:

* **Encryption at Rest (AES-GCM 256-bit):** All your financial transactions, settings, and categories are encrypted locally using a master passphrase combined with `PBKDF2` key derivation (100,000 iterations) and random salts via the native browser Web Crypto API.
* **Passphrase-Protected Gate:** Upon loading the application, a lock screen prevents any unauthorized access to your stored data unless the correct passphrase is provided.
* **Zero-Knowledge Architecture:** Your passphrase never leaves your device. Data is encrypted before being stored in browser `localStorage`.
* **XSS Mitigation:** All UI elements and user-supplied descriptions are rendered safely using secure DOM APIs (`.textContent`) rather than unescaped string injection.
* **Content Security Policy (CSP):** Strict CSP headers are enforced to prevent unauthorized script execution or cross-site resource loading.

---

## ✨ Key Features

* **Multi-Currency Support:** Track your base currency (e.g., USD) alongside secondary currencies (e.g., CRC, EUR).
* **Automatic Exchange Rates:** Automatically fetches daily exchange rates from `open.er-api.com` with graceful fallbacks.
* **Flexible Budget Frequencies:** Switch seamlessly between Monthly, Bi-weekly (Quincenal), or Weekly periods.
* **Smart Currency Conversion Summary:** Automatically calculates whether you need to exchange money from your base currency to cover expenses in alternative currencies.
* **Bilingual Interface:** Fully toggleable between Spanish and English (`es` / `en`).
* **Fully Client-Side:** Lightweight single-file setup (`index.html`), making it lightning-fast and ideal for deployment on GitHub Pages.

---

## 🚀 Deployment & Setup

### 1. Host on GitHub Pages (Recommended: Private Repository)
To keep your source code completely hidden from the public internet, you can host GitHub Pages directly from a **Private Repository**:
1. Create a new repository on GitHub and set its visibility to **Private**.
2. Upload your `index.html` file to the root of the repository.
3. Go to your repository **Settings** > **Pages**.
4. Under **Build and deployment**, select **Deploy from a branch** and choose your `main` (or `master`) branch.
5. Access your secure dashboard via your generated GitHub Pages URL.

### 2. First-Time Run
1. Open your GitHub Pages URL in your browser.
2. You will be greeted by the **Create Master Passphrase** lock screen.
3. Enter a strong, memorable passphrase. *(Note: Because there is no backend server, there is no "forgot password" feature. If you lose your passphrase, you will need to clear local storage to reset).*
4. Begin adding your income, fixed/variable expenses, and savings!

---

## ⚠️ Important Cryptographic Disclaimer

Because this is a completely static, client-side application running in an open browser environment:
* **Active Session Memory:** Once unlocked, your decryption key and decrypted data reside in the browser's active RAM for the duration of the session. Always lock or close your browser tab when stepping away from your device.
* **Backups:** If you clear your browser cache or `localStorage`, your encrypted data will be wiped. Ensure you note down your transactions if performing major browser cleanups.
