Notion Budget Tracker 📊
A lightweight, fully responsive, and multi-currency financial budget tracker designed to be embedded directly into Notion or used as a standalone web app on tablets and desktops. It features real-time currency conversion, dynamic budgeting periods (monthly, bi-weekly, or weekly), and an automated conversion exchange summary.
✨ Key Features
 * Multi-Currency Support & Robust Symbols: Define a base currency and multiple additional currencies. Symbols ($, ₡, €, etc.) are securely handled across all devices and browsers.
 * Dynamic Budget Frequencies: Choose between Monthly (1 period), Bi-Weekly / Quincenal (2 periods), or Weekly (4 periods) from the configuration panel, and the navigation tabs will adapt automatically.
 * Smart Dashboard Calculations:
   * Income & Remaining Balance: Represented as global financial pools converted across all active currencies using live/manual exchange rates.
   * Expenses & Savings: Show direct real totals accumulated per currency so you can track exact financial obligations.
   * Visual Overdraft Indicator: Remaining balance turns green when positive and red if you enter a deficit.
 * Automated Currency Conversion Helper: If your expenses or savings in a secondary currency exceed the income in that same currency, the app calculates precisely how much base currency you need to exchange.
 * Local Storage Persistence: All your transactions, configurations, and custom exchange rates are safely stored locally in your browser/Notion widget.
 * Quick Management: Easily add, edit, or delete transactions with pre-populated category options.
🚀 Getting Started
 * Download/Copy: Copy the complete HTML code provided.
 * Usage in Notion:
   * Add a Code block inside your Notion page.
   * Paste the HTML code into the block and preview it, or host it on a platform like GitHub Pages, Vercel, or Netlify and embed it using a Embed block.
 * Standalone: Save the code as an index.html file and open it in any modern browser or tablet.
⚙️ Configuration
 * Go to the ⚙️ Configuración tab.
 * Select your preferred Budget Frequency (Mensual, Quincenal, Semanal).
 * Set your Base Currency (e.g., USD) and Additional Currencies (e.g., CRC, EUR).
 * Adjust exchange rates or click 🔄 Forzar Actualización de API to fetch daily global rates automatically.
 * Click Guardar Configuración.
🛠️ Built With
 * HTML5 / CSS3: Clean, modern Notion-inspired aesthetic utilizing the Inter font family.
 * Vanilla JavaScript: Zero dependencies, fully client-side execution with localStorage support.
 * Exchange Rate API: Integrates global rates from open.er-api.com.
