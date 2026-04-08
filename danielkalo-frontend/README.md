# MonteCarlo Sports Betting Simulator - Frontend

The client-facing React application that allows users to seamlessly browse upcoming games, analyze simulations, and manage their watchlists.

## Project Gallery

**Dashboard Home**  
![New Homepage](public/images/new_homepage.png)

**Today's Matches & Filtering**  
![Today's Games](public/images/todays_games_iter3.png)  
![Upcoming Games Filter](public/images/upcoming_games_w_sport_filter.png)

**Monte-Carlo Match Simulator**  
![Ran Simulation](public/images/ran_simulation_iter3.png)

**Interactive Watchlists (Drag & Drop)**  
![My Sims](public/images/my_sims_iter3.png)

## Core Capabilities

- **Secure Data Fetching**: Utilizes a centralized Axios client that natively manages and attaches Google OAuth Bearer tokens across the application.
- **Advanced State Management**: Custom React Hooks such as `useWatchlist()` power universal toggle logic across the platform.
- **Interactive UI Components**: Leveraging `react-dnd` allows deterministic, drag-and-drop ordering for user-saved simulations. Custom status badges auto-refresh on a 30s background interval without interrupting the user flow.

## Local Set-Up Instructions

1. **Install Dependencies**:
   ```bash
   npm install
   ```
   *(Or `yarn install` if preferred)*

2. **Environment Variables**:
   Create a `.env` file at the root of the frontend folder and add your credentials:
   ```
   REACT_APP_API_URL=http://localhost:5001/api
   REACT_APP_GOOGLE_CLIENT_ID=your_google_client_id_here
   ```

3. **Start the Dev Server**:
   ```bash
   npm start
   ```
   Open [http://localhost:3000](http://localhost:3000) to view it in the browser. 

The build is configured to compile optimally via `npm run build` for production distributions.