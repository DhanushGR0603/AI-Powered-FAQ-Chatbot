 AI-Powered FAQ Chatbot
An intelligent FAQ chatbot built using React and Node.js, powered by NLP techniques via either a small ML model (TensorFlow.js) or OpenAI API (free tier). This bot answers frequently asked questions, provides an interactive messaging UI, and learns from user feedback and unanswered queries.

📌 Objective
Build a smart chatbot that can:

Understand and respond to FAQ-style queries.

Use a lightweight machine learning model or keyword matching.

Continuously improve based on user feedback.

🛠️ Tech Stack
Frontend	Backend	AI/NLP	Storage
React.js	Node.js	TensorFlow.js or OpenAI API (Free Tier)	MongoDB / JSON file / SQLite

🧠 Features
✅ OpenAI Integration – Uses AI to answer FAQ-style questions.
✅ Modular Architecture – Well-structured with controllers, services, and config layers.
✅ Secure API – Implements security best practices using helmet and cors.
✅ CommonJS Compatibility – Uses require for backward compatibility.
✅ Environment-Based Config – API keys and URLs are managed in .env.
✅ Logging & Error Handling – Uses morgan for request logging and robust error handling.

📁Project Structure
ai-faq-bot/
│── src/
│   ├── config/
│   │   ├── openConfig.js   # OpenAI (OpenAI) API configuration  
│   ├── controllers/
│   │   ├── faqController.js # Handles user requests  
│   ├── services/
│   │   ├── faqService.js # Calls OpenAI API  
│   ├── routes/
│   │   ├── faqRoutes.js # Defines API endpoints  
│── .env  # API keys and environment variables  
│── package.json  
│── server.js  # Main Express app  


🚀 Getting Started
1️⃣ Clone the Repository
git clone https://github.com/JawherKl/ai-faq-bot.git  
cd ai-faq-bot
2️⃣ Install Dependencies
npm install
3️⃣ Configure Environment Variables
Create a .env file in the root directory:

PORT=3000
BASE_URL=https://openrouter.ai/api/v1
API_KEY=your-api-key-here
4️⃣ Start the Server
npm start
The API will run at http://localhost:3000.


🎯 API Endpoints
🔹 Ask a Question (POST /api/faq/ask)
Request:

curl -X POST http://localhost:3000/api/faq/ask \
     -H "Content-Type: application/json" \
     -d '{"model": "models-name-example","question": "What is OpenAI AI?"}'
Response:

{
  "answer": "OpenAI AI is an advanced AI model providing intelligent responses..."
}


🛠️ Technologies Used
Node.js (Express) – Backend framework
OpenAI – AI model for FAQ responses
dotenv – Environment variable management
helmet, cors, morgan – Security and logging


📌 Future Improvements
✅ Support multiple AI models (OpenAI, Cohere, etc.)
✅ Implement Redis caching for frequent queries
✅ Add database support (MongoDB, PostgreSQL) for logging questions
✅ Deploy on Railway, Render, or Vercel

🤖 Demo

![Screenshot 2025-06-20 141853](https://github.com/user-attachments/assets/fe966519-4774-41c1-8175-1b2da0b65c62)

