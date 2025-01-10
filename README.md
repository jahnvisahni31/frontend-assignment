# frontend-assignment

🚀 A full-stack application providing real-time cryptocurrency statistics. The application fetches data from the CoinGecko API and displays it with an elegant, responsive design built using Vite.js and Tailwind CSS.

## Features

### Backend
- Fetches cryptocurrency data (price, market cap, 24-hour change) using the CoinGecko API every 2 hours
- Provides RESTful APIs for:
  - Fetching the latest data
  - Calculating price deviation
- Stores data in MongoDB

### Frontend
- Displays cryptocurrency stats for Bitcoin, Ethereum, and Matic automatically
- Fully responsive design implemented with Tailwind CSS
- Includes the following sections:
  - **Cryptocurrency Stats:** Shows price, market cap, and 24-hour price change
  - **TradingView Charts:** Integrated TradingView advanced chart for tokens
  - **Trending Coins (24h):** Displays top 3 trending cryptocurrencies
  - **You May Also Like:** Horizontally scrollable carousel showcasing trending coins

## API Details

### CoinGecko API Integration

#### 1. `/simple/price`
- **Parameters**:
  - `ids`: `bitcoin`
  - `vs_currencies`: `inr,usd`
  - `include_24hr_change`: `true`
- **Purpose**: Fetch Bitcoin's price in INR, USD, and 24-hour change
- **Sample Response**:
  ```json
  {
    "bitcoin": {
      "inr": 5697177,
      "inr_24h_change": 3.65,
      "usd": 68726,
      "usd_24h_change": 3.67
    }
  }
  ```

#### 2. `/search/trending`
- **Purpose**: Fetch the top 3 trending coins

#### 3. `/coins/{id}`
- **Purpose**: Fetch details about a specific cryptocurrency (used to render dynamic charts for tokens)

## Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/jahnvisahni31/frontend-assignment
   cd frontend-assignment
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

4. Start the development server:
   ```bash
   npm run dev
   ```

5. Open the application in your browser:
   ```
   http://localhost:5173
   ```

## Deployment
- Deploy the application on platforms like Heroku, Render, or Vercel
- Ensure the MongoDB connection is properly configured
- Set up environment variables in your deployment platform

## Project Structure
```
frontend-assignment/
├── src/
│   ├── components/
│   ├── pages/
│   ├── assets/
│   ├── App.jsx
│   └── main.jsx
├── public/
├── tailwind.config.js
├── vite.config.js
└── package.json
```

## Optional Features
- Dynamic token details using the URL (e.g., `/bitcoin`, `/ethereum`)
- Symbol-based TradingView chart integration

## Technologies Used
- Vite.js
- React.js
- Node.js
- Express.js
- Tailwind CSS
- Axios
