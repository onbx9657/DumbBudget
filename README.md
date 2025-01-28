# Dumb Boilerplate

A simple boilerplate for creating "Dumb" line of applications with PIN authentication and theme support.

WHEN COPYING THIS BOILERPLATE, CHANGE THE PIN NAME, CHANGE PACKAGE.JSON NAME AND RUN NPM INSTALL.

## Features

- PIN-based authentication
- Light/Dark theme toggle
- Secure session management
- Modern responsive design
- Mobile-friendly PIN input

## Setup

1. Install dependencies:
```bash
npm install
```

2. Create a `.env` file in the root directory and add your PIN:
```bash
# Replace DUMB_BOILERPLATE with your project name in uppercase, with hyphens replaced by underscores
DUMB_BOILERPLATE_PIN=1234
```

3. Start the server:
```bash
# Development mode with auto-reload
npm run dev

# Production mode
npm start
```

## Security Features

- Constant-time PIN comparison to prevent timing attacks
- Secure session cookies
- CSP headers with Helmet.js
- HTTPS ready (recommended for production)
- XSS protection
- CSRF protection

## Customization

1. Update the project name in `package.json`
2. Modify the title in `public/index.html`
3. Customize styles in `public/styles.css`
4. Add your own routes in `server.js`

## Development

The boilerplate uses the following structure:
```
.
├── public/
│   ├── index.html
│   ├── login.html
│   ├── styles.css
│   └── script.js
├── server.js
├── package.json
└── .env
```

## Production Deployment

1. Set `NODE_ENV=production` in your environment
2. Use HTTPS in production
3. Set appropriate session secret
4. Configure secure cookie settings

## License

MIT 