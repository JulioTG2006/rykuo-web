
# Environment Setup

## Prerequisites
- Node.js (v16 or higher)
- npm or yarn
- Git

## Installation

1. Clone the repository
```bash
git clone <repository-url>
cd rykuo-web
```

2. Install dependencies
```bash
npm install
```

3. Create `.env` file in the root directory
```bash
cp .env.example .env
```

4. Configure environment variables
```
REACT_APP_API_URL=http://localhost:3000
REACT_APP_ENV=development
```

## Development

Start the development server:
```bash
npm run dev
```

## Build

Production build:
```bash
npm run build
```

## Testing

Run tests:
```bash
npm test
```

## Additional Resources

- [Node.js Documentation](https://nodejs.org/docs/)
- [React Documentation](https://react.dev/)
