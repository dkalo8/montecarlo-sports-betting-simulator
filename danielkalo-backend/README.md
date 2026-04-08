# MonteCarlo Sports Betting Simulator - Backend

This service acts as the central hub for the platform, executing mathematical scenarios, dispatching API requests for live odds to 3rd parties, and managing securely-typed schema collections. Built natively on Node.js and Express.

## Core Infrastructure

- **Watchlist & User State Verification**: Enforces deterministic ordering by persisting drag-and-drop UI actions. Uses strict authentication middleware (`verifyGoogleToken`) evaluating OAuth properties dynamically. 
- **Cron Job Configuration**: Employs an automated schedule using `scripts/realGames.js` and `scripts/realScores.js` ensuring minimal quota usages on standard REST queries to external providers. 
- **Bespoke Algorithm Runner**: Houses `runMonteCarlo` mathematical logic natively abstracted inside `utilities/simulationUtilities.js` enabling modular expansion. 
- **The Odds API Handler**: Maps heavily nested structures effectively to the frontend utilizing caching architectures.

## Key API Endpoints

**Public Utilities**
- `GET /api/health` - Simple health check returning metadata.
- `GET /api/games` - Retrieve matching game listings dependent on requested filters, sport configurations, and pagination directives.

**Authenticated Services (Requires Bearer Google Tokens)**
- `GET /api/simulations` - Retrieve a user's generated simulation history.
- `POST /api/simulations` - Dispatches engine, creates record, and returns results.
- `PUT /api/simulations/order` - Manages algorithmic array updates for ordering.
- `GET | POST | DELETE /api/watchlist` - Universal routes for generic user-save actions.

## Local Set-Up Instructions

1. **Install Dependencies**:
   ```bash
   npm install
   ```
   *(Or `yarn install`)*

2. **Environment Assignments**:
   Establish a root-level `.env` file containing your local configurations:
   ```
   PORT=5001
   MONGODB_URI=your_mongo_connection_string
   ODDS_API_KEY=your_odds_api_key
   GOOGLE_CLIENT_ID=your_google_auth_key
   ```
   
3. **Local Database Seeding**:
   ```bash
   npm run real:games
   # or
   yarn seed:games
   ```
   This will bootstrap the database with relevant testing data for the frontend to render.

4. **Bootstrapping the Server**:
   ```bash
   npm run dev
   ```
   Available on `http://localhost:5001` or your configured respective internal port structure.