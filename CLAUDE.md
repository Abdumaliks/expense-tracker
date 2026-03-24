# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Expense/finance tracker starter app built with React 19 and Vite 7. This is a course project that intentionally contains bugs, poor UI, and messy code to be fixed as exercises.

## Commands

- `npm run dev` — start dev server (http://localhost:5173)
- `npm run build` — production build to `dist/`
- `npm run lint` — run ESLint
- `npm run preview` — preview production build

## Architecture

Single-component React app — all logic lives in `src/App.jsx` with no routing, no state management library, and no backend. Transactions are hardcoded in state (no persistence).

**Known intentional issues:**
- Transaction amounts are stored as strings, causing the summary calculations (totalIncome, totalExpenses, balance) to concatenate instead of sum
- "Freelance Work" is typed as "expense" instead of "income"
- No delete functionality (CSS class `.delete-btn` exists but is unused)
- No number formatting (e.g. `toFixed(2)`)

## Tech Stack

- React 19 (JSX, no TypeScript)
- Vite 7 with `@vitejs/plugin-react`
- ESLint 9 flat config with react-hooks and react-refresh plugins
- No test framework configured
