# WS101 Pokémon List

A responsive, type-safe Pokémon database built for the WS101 prelim project using React, TypeScript, Vite, and PokéAPI.

## Features

- Search Pokémon by name across the complete loaded PokéAPI catalog (case-insensitive and substring matching)
- Exactly 20 Pokémon displayed per page
- Previous / Next pagination
- Pokémon detail modal with types, abilities, dimensions, experience, and base stats
- Light / dark theme toggle with localStorage persistence
- Favorites counter with localStorage persistence
- Responsive Pokémon card grid
- Loading, error, and empty-search states
- Typed React components and API interfaces
- Generic `useFetch<T>` hook using a discriminated async-state union
- `useReducer` for search/page state

## Project structure

```text
src/
├── components/
│   ├── Card.tsx
│   ├── ItemList.tsx
│   └── SearchBar.tsx
├── hooks/
│   └── useFetch.ts
├── contexts/
│   └── ThemeContext.tsx
├── types/
│   └── api.ts
├── App.tsx
├── App.css
└── main.tsx
```

## Setup

```bash
npm install
npm run dev
```

Type-check the project:

```bash
npx tsc --noEmit
```

Build for production:

```bash
npm run build
```

## API

PokéAPI: https://pokeapi.co/

## Notes

The catalog is loaded from PokéAPI's Pokémon endpoint. The application keeps the complete name catalog in memory so searching works regardless of the current page. The UI then loads the 20 Pokémon needed for the selected page.
