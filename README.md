# Random Cat Viewer

A React + TypeScript + Vite app that fetches and displays random cat breed information using the [FreeAPI](https://freeapi.app) public cats endpoint.

<img width="531" height="615" alt="Screenshot (265)" src="https://github.com/user-attachments/assets/db36fbfc-c17d-42c1-9893-e3e484017ec3" />


## Features

- Fetches a random cat breed on load and on demand
- Displays cat image, name, origin, description, lifespan, and weight
- Shows temperament and stat bars for adaptability, intelligence, affection, energy, child-friendliness, and dog-friendliness
- Links to Wikipedia and VetStreet where available
- 16:9 image area with `object-fit: contain` — no cropping or distortion for any image shape
- Error handling for network failures
- Responsive dark-themed UI

## Tech Stack

| Tool | Version |
|------|---------|
| React | 19 |
| TypeScript | 6 |
| Vite | 8 |
| CSS | Custom dark theme |

## Getting Started

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## File Structure

```
FreeAPI Random Cat Viewer/
├── src/
│   ├── App.tsx        # Main app component + StatBar component
│   ├── App.css        # Component styles (dark theme)
│   ├── index.css      # Global reset
│   └── main.tsx       # React entry point
├── index.html         # HTML template
├── vite.config.ts     # Vite configuration
├── tsconfig.json      # TypeScript base config
├── tsconfig.app.json  # TypeScript app config
├── tsconfig.node.json # TypeScript node config
└── package.json       # Dependencies and scripts
```

## API

**Endpoint:** `GET https://api.freeapi.app/api/v1/public/cats/cat/random`

**Sample Response:**

```json
{
  "statusCode": 200,
  "data": {
    "id": 52,
    "name": "Savannah",
    "origin": "United States",
    "description": "Savannah is the feline version of a dog...",
    "temperament": "Curious, Social, Intelligent, Loyal",
    "life_span": "17 - 20",
    "weight": { "imperial": "8 - 25", "metric": "4 - 11" },
    "adaptability": 5,
    "affection_level": 5,
    "child_friendly": 4,
    "dog_friendly": 5,
    "energy_level": 5,
    "intelligence": 5,
    "image": "https://cdn2.thecatapi.com/images/a8nIYvs6S.jpg",
    "wikipedia_url": "https://en.wikipedia.org/wiki/Savannah_cat",
    "vetstreet_url": "http://www.vetstreet.com/cats/savannah"
  },
  "message": "Cat fetched successfully",
  "success": true
}
```

## Components

### `App`
Root component. Manages fetch state (`loading`, `error`, `cat`) and renders the card layout.

### `StatBar`
Reusable bar component that renders a labeled progress bar for a trait score out of 5.

```tsx
<StatBar label="Intelligence" value={5} />
```

## Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start local dev server |
| `npm run build` | Type-check and build for production |
| `npm run preview` | Preview the production build locally |
| `npm run lint` | Run ESLint |
