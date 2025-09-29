# GraphQL Weather App 🌤️

An interactive weather app built with **Next.js**, **TypeScript**, **GraphQL**, and **StepZen**.
Fetch real-time weather data with GraphQL queries and display it in a clean UI.

------------------------------------------------------------

## 🧭 Table of Contents

- Features
- Tech Stack
- Project Structure
- Getting Started
  - Prerequisites
  - Environment Variables
  - Installation & Running
- GraphQL Schema & Queries
- Key Modules & Architecture
- Scripts

------------------------------------------------------------

## 🔍 Features

- Fetch current weather for a given location
- Use GraphQL API (via StepZen) to query weather data
- Search by city name
- Display temperature, humidity, wind, etc.
- Clean, responsive UI

------------------------------------------------------------

## 🧱 Tech Stack

- Next.js (with TypeScript)
- React + hooks
- GraphQL / StepZen
- Apollo Client (or GraphQL client)
- Styling: Tailwind CSS
- API key management via environment variables

------------------------------------------------------------

## 📁 Project Structure

```
.
├── app/                    # Next.js app route components
├── components/             # UI components
├── graphql/                # GraphQL queries / schema
├── lib/                    # Helper utilities (API client)
├── public/                 # Static assets
├── stepzen/                # StepZen config / endpoint setup
├── .eslintrc.json
├── next.config.js
├── package.json
├── tailwind.config.js
├── tsconfig.json
└── README.md
```

------------------------------------------------------------

## 🚀 Getting Started

### Prerequisites

- Node.js (v14+)
- A host or test account for StepZen (or GraphQL endpoint)
- Weather API key (e.g. OpenWeatherMap, etc.)

### Environment Variables

Create a `.env.local` file in the project root:

```env
OPENAI_API_KEY=your_openai_api_key
API_URL=your_stepzen_endpoint_url
NEXT_PUBLIC_STEPZEN_API_KEY=your_stepzen_api_key
```

### Installation & Running

```bash
# Install dependencies
npm install

# Start development server
npm run dev
# Open http://localhost:3000

# Build & run production
npm run build && npm start
```

------------------------------------------------------------

## 🔎 GraphQL Schema & Queries

- The GraphQL schema defines a `Weather` query (or similar) to fetch weather data
- Queries take location (city name, coordinates) as arguments
- Returns fields like: temperature, humidity, windSpeed, weatherDescription

You can inspect the GraphQL playground at your StepZen endpoint for more details.

------------------------------------------------------------

## 🧩 Key Modules & Architecture

- lib/apollo-client.ts — sets up GraphQL client with endpoint & auth
- graphql/queries — GraphQL query files (e.g. GET_WEATHER.gql)
- components/WeatherCard — displays weather details
- app/page.tsx — UI for search & display
- State & UI logic handled via React hooks

------------------------------------------------------------

## 🧪 Scripts

| Script | Description              |
|--------|--------------------------|
| dev    | Start dev server         |
| build  | Build for production     |
| start  | Run production server    |
| lint   | Run ESLint               |

------------------------------------------------------------
