# DumbBudget

A simple, secure personal budgeting app with PIN protection. Track your income and expenses with a clean, modern interface.

![image](https://github.com/user-attachments/assets/7874b23a-159f-4c93-8e5d-521c18666547)


## Features

- 🔒 PIN-protected access
- 💰 Track income and expenses
- 📊 Real-time balance calculations
- 🏷️ Categorize transactions
- 📅 Date range filtering
- 🔄 Sort by date or amount
- 📱 Responsive design
- 🌓 Light/Dark theme
- 📤 Export to CSV
- 🔍 Filter transactions by type
- 💱 Multi-currency support

## Supported Currencies

DumbBudget supports the following currencies:
- USD (US Dollar) 🇺🇸
- EUR (Euro) 🇪🇺
- GBP (British Pound) 🇬🇧
- JPY (Japanese Yen) 🇯🇵
- AUD (Australian Dollar) 🇦🇺
- CAD (Canadian Dollar) 🇨🇦
- CHF (Swiss Franc) 🇨🇭
- CNY (Chinese Yuan) 🇨🇳
- HKD (Hong Kong Dollar) 🇭🇰
- NZD (New Zealand Dollar) 🇳🇿

Set your preferred currency using the `CURRENCY` environment variable (defaults to USD if not set).

### Using Docker

```bash
docker run -d \
  -p 3000:3000 \
  -e DUMBBUDGET_PIN=12345 \
  -e CURRENCY=USD \
  dumbwareio/dumbbudget:latest
```

### Environment Variables

| Variable | Description | Required | Default | Example |
|----------|-------------|----------|---------|---------|
| `DUMBBUDGET_PIN` | PIN code for accessing the application | Yes | - | `12345` |
| `PORT` | Port number for the server | No | `3000` | `8080` |
| `NODE_ENV` | Environment mode | No | `production` | `development` |
| `CURRENCY` | Currency code for transactions | No | `USD` | `EUR` |

## Development Setup

1. Clone the repository:
```bash
git clone https://github.com/DumbWareio/DumbBudget.git
cd DumbBudget
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file:
```env
DUMBBUDGET_PIN=12345
PORT=3000
NODE_ENV=development
```

4. Start the development server:
```bash
npm run dev
```

5. Open http://localhost:3000 in your browser

## Building from Source

```bash
# Build the Docker image
docker build -t dumbwareio/dumbbudget:latest .

# Run the container
docker run -d -p 3000:3000 -e DUMBBUDGET_PIN=12345 dumbwareio/dumbbudget:latest
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Security

DumbBudget includes several security features:
- PIN protection for access
- Rate limiting on PIN attempts
- Temporary lockout after failed attempts
- No sensitive data stored in browser storage
- Secure session handling

## Support

- Report bugs by opening an issue
- Request features through issues
- [Join our community discussions](https://discord.gg/zJutzxWyq2)

## Support the Project

<a href="https://www.buymeacoffee.com/dumbware" target="_blank">
  <img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" height="60">
</a>

---
Made with ❤️ by [DumbWare.io](https://github.com/DumbWareio)
