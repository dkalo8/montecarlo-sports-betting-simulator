# MonteCarlo Sports Betting Simulator

A full-stack web application designed for sports enthusiasts and bettors to analyze upcoming match-ups. Built on the MERN stack (MongoDB, Express, React, Node.js), this platform tracks live sports data, fetches ongoing odds, and runs customizable Monte-Carlo simulations to forecast game outcomes. 

## Features

- **Live Games Tracking**: Up-to-date scores and lines for major sports leagues including NBA, NFL, Soccer, and Tennis. Auto-updating game statuses.
- **Monte-Carlo Predictions**: A bespoke prediction engine that runs thousands of randomized statistical trials based on current implied odds, helping users evaluate the true likelihoods of different outcomes.
- **Personalized Watchlists**: Save individual games and generated simulations. Includes real-time adjustments and drag-and-drop deterministic ordering for Saved Sims.
- **Google OAuth Authentication**: Secure user login flow for saving sessions and cross-platform syncing.

## Tech Stack

- **Frontend**: React, React Router, Bootstrap, React-DnD (for drag-and-drop)
- **Backend**: Node.js, Express, Google Auth Library, Mongoose
- **Database**: MongoDB 
- **External Integrations**: The Odds API (live data via cron scheduling) 

## Project Structure

This project adopts a clean separation of concerns architecture spanning two discrete directories:
- [`/danielkalo-frontend`](./danielkalo-frontend/README.md) - The React-based single-page user interface.
- [`/danielkalo-backend`](./danielkalo-backend/README.md) - The Express REST API and simulation engine.

Please refer to the enclosed `README.md` inside each sub-directory for environment configurations and local execution instructions.
