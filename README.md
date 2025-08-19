# Flash Cards App

A modern, interactive flash cards application built with SvelteKit and TypeScript. This app helps users learn programming concepts through an engaging and intuitive interface.

## Features

- 📚 Interactive flash cards with programming-related questions and answers
- 🔄 Smooth card flip animations
- ⏮️ Navigation between cards with previous and next buttons
- 📊 Progress tracking bar
- 💅 Clean and responsive design
- 🚀 Built with modern web technologies

## Technology Stack

- **Framework**: SvelteKit 2.x
- **Language**: TypeScript
- **Build Tool**: Vite
- **Styling**: CSS
- **Code Quality**: ESLint, Prettier
- **Development Tools**: 
  - svelte-check
  - TypeScript
  - Prettier with Svelte plugin
  - ESLint with Svelte plugin

## Getting Started

### Prerequisites

- Node.js (Latest LTS version recommended)
- npm or pnpm

### Installation

1. Clone the repository:
```bash
git clone https://github.com/MrRyt247/flash-card-app.git
cd flash-cards
```

2. Install dependencies:
```bash
npm install
```

### Development

To start the development server:
```bash
npm run dev

```

The application will be available at `http://localhost:5173`

### Building for Production

To create a production build:
```bash
npm run build
# or
pnpm build
```

You can preview the production build with `npm run preview`.

### Available Scripts

- `dev`: Start development server
- `build`: Create production build
- `preview`: Preview production build
- `check`: Run Svelte type checking
- `format`: Format code with Prettier
- `lint`: Run linting checks

## Project Structure

```
flash-cards/
├── src/
│   ├── lib/
│   │   └── assets/
│   ├── routes/
│   │   ├── components/
│   │   │   ├── Button.svelte
│   │   │   ├── Card.svelte
│   │   │   └── Progressbar.svelte
│   │   ├── data/
│   │   │   └── data.js
│   │   ├── +layout.svelte
│   │   └── +page.svelte
│   ├── app.html
│   └── app.d.ts
├── static/
├── vite.config.ts
├── svelte.config.js
└── tsconfig.json
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Feel free to submit issues and pull requests.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request
