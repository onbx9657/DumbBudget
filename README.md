# DumbBudget

A simple, secure personal budgeting app with PIN protection. Track your income and expenses with a clean, modern interface.

![DumbBudget Logo](https://raw.githubusercontent.com/DumbWareio/DumbBudget/main/public/logo.png)

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

## Quick Start

### Using Docker

```bash
docker run -d \
  -p 3000:3000 \
  -e DUMBBUDGET_PIN=12345 \
  dumbwareio/dumbbudget:latest
```

### Environment Variables

| Variable | Description | Required | Default | Example |
|----------|-------------|----------|---------|---------|
| `DUMBBUDGET_PIN` | PIN code for accessing the application | Yes | - | `12345` |
| `PORT` | Port number for the server | No | `3000` | `8080` |
| `NODE_ENV` | Environment mode | No | `production` | `development` |

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
- Join our community discussions

---
Made with ❤️ by [DumbWare.io](https://github.com/DumbWareio)