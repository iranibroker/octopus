# **🐙 Octopus Gold Trader**

**Octopus Gold Trader** is a retro-styled, gamified web application that allows users to predict the daily movement of the Gold market (XAUUSD). Built with a nostalgic 8-bit pixel art aesthetic, it integrates real-time market data and social sentiment analysis to create an engaging trading experience.


## **✨ Features**

* **Gamified Prediction:** Users vote "UP" (Bullish) or "DOWN" (Bearish) on the daily close price of Gold.  
* **Retro Arcade Aesthetic:** Custom pixel art graphics, "Press Start 2P" typography, and CRT-style layouts.  
* **Real-Time Data:** Integrated **TradingView Widget** for live XAUUSD price tracking.  
* **Community Sentiment:** Visual bar showing the percentage of Up vs. Down votes for the day.  
* **Leaderboards:** Weekly and Monthly top trader rankings based on XP.  
* **Dynamic Scheduling:** \- Voting locks daily at **14:00**.  
  * Market status updates automatically (Open/Closed/Weekend).  
* **Seamless Integration:** Designed to be embedded via iframe with JWT token authentication.

## **🛠️ Technologies**

* **Frontend:** HTML5, Vanilla JavaScript  
* **Styling:** Tailwind CSS (via CDN), Custom CSS for pixel art & animations  
* **Fonts:** Google Fonts (Press Start 2P)  
* **External Widgets:** TradingView Lightweight Widget  
* **API Integration:** Fetch API for backend communication (User auth, voting, leaderboards)

## **🚀 Getting Started**

### **Prerequisites**

This is a static HTML/JS application, but it requires a specific backend API to function correctly.

### **Installation**

1. **Clone the repository:**  
   git clone \[https://github.com/yourusername/octopus-gold-trader.git\](https://github.com/yourusername/octopus-gold-trader.git)

2. **Serve the file:**  
   You can use any static file server. For example, using Python:  
   python3 \-m http.server

   Or simply open index.html in your browser (note: API calls may fail due to CORS if not running on the whitelisted domain).

### **Authentication & Testing**

The application expects an authentication token in the URL query parameters to log the user in.

**URL Format:**

http://localhost:8000/?token=\<YOUR\_JWT\_TOKEN\>

If no token is provided, the app will show an "Invalid Token" error overlay.

## **🔌 API Integration**

The app communicates with the backend at https://api.ounce24.com/api.

**Key Endpoints Used:**

* GET /auth/me: Validate user and get profile.  
* GET /octopus/me/vote: Check if the user has already voted today.  
* POST /octopus/vote: Submit a new prediction.  
* GET /octopus/sentiment: Get community vote percentages.  
* GET /octopus/leaderboard/{type}: Fetch Weekly/Monthly rankings.

## **🕹️ How to Play**

1. **Check the Price:** Look at the live XAUUSD price on the retro monitor.  
2. **Make a Call:** Will the price close higher or lower than it is right now?  
3. **Vote:** Click the **UP** (Green) or **DOWN** (Red) button before **14:00**.  
4. **Wait:** Once the market closes, your prediction is settled.  
5. **Win XP:** Correct predictions earn you XP to climb the Global Leaderboard\!

## **📄 License**

This project is licensed under the [MIT License](https://www.google.com/search?q=LICENSE).

*Developed by \Mahdi Ketabdar \ *
