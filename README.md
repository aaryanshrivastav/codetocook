# CodeToCook - AI Recipe Generator

A beautiful web application that generates personalized recipes using AI. Simply provide your available ingredients, and the app will create a custom recipe tailored to your preferences.

![Sunset Cafe](https://images.unsplash.com/photo-1560359614-870d1a7ea91d)

## 🌟 Features

- **AI-Powered Recipe Generation**: Uses Google Gemini AI to create unique recipes based on your ingredients
- **Customizable Filters**: Choose from meal types, cuisines, and dietary restrictions
- **Beautiful UI**: Modern, responsive design with a sunset beach theme
- **Recipe Details**: Includes prep time, cook time, servings, ingredients, and step-by-step instructions
- **Fast & Reliable**: Built with FastAPI backend and React frontend

## 🛠️ Tech Stack

### Backend
- **FastAPI** - Modern Python web framework
- **Google Gemini AI** - AI model for recipe generation
- **Uvicorn** - ASGI server

### Frontend
- **React** - UI library
- **Tailwind CSS** - Utility-first CSS framework
- **Axios** - HTTP client
- **Framer Motion** - Animation library

## 📋 Prerequisites

- Python 3.8+ 
- Node.js 14+ and npm
- Google Gemini API Key ([Get one here](https://makersuite.google.com/app/apikey))

## 🚀 Installation

### 1. Clone the repository

```bash
git clone <repository-url>
cd codetocook
```

### 2. Backend Setup

```bash
# Install Python dependencies
pip install -r requirements.txt

# Create a .env file in the root directory
# Add your Gemini API key
echo "GEMINI_API_KEY=your_api_key_here" > .env
```

### 3. Frontend Setup

```bash
cd recipe-frontend
npm install
```

## 🎯 Usage

### Running the Backend

From the root directory:

```bash
# Run the FastAPI server
uvicorn nodel:app --reload
```

The backend will be available at `http://127.0.0.1:8000`

### Running the Frontend

From the `recipe-frontend` directory:

```bash
npm start
```

The frontend will be available at `http://localhost:3000`

### Using the Application

1. Open your browser and navigate to `http://localhost:3000`
2. Optionally select meal type, cuisine, and dietary restrictions
3. Enter your available ingredients (comma-separated)
4. Click "Generate Recipe"
5. View your custom recipe with detailed instructions

## 📁 Project Structure

```
codetocook/
├── nodel.py                 # FastAPI backend server
├── requirements.txt         # Python dependencies
├── .env                     # Environment variables (create this)
├── recipe-frontend/
│   ├── src/
│   │   ├── App.js          # Main React component
│   │   └── ...
│   ├── package.json        # Node.js dependencies
│   └── tailwind.config.js  # Tailwind CSS configuration
└── README.md
```

## 🔧 Environment Variables

Create a `.env` file in the root directory with:

```env
GEMINI_API_KEY=your_gemini_api_key_here
```

## 📝 API Endpoint

### POST `/generate-recipe`

Generates a recipe based on provided ingredients.

**Request Body:**
```json
{
  "ingredients": "tomato, onion, garlic, olive oil"
}
```

**Response:**
```json
{
  "dish_name": "Garlic Tomato Pasta",
  "ingredients": ["tomato", "onion", "garlic", "olive oil"],
  "steps": [
    "Chop onion and garlic.",
    "Sauté in olive oil until golden.",
    "Add chopped tomato and cook until soft.",
    "Toss with cooked pasta and serve."
  ],
  "prep_time": "10 min",
  "cook_time": "20 min",
  "servings": 2
}
```

## 🧪 Development

### Running Tests

```bash
# Frontend tests
cd recipe-frontend
npm test

# Backend - Add your tests here
```

### Building for Production

```bash
# Build frontend
cd recipe-frontend
npm run build

# The build folder contains the production-ready app
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is open source and available under the MIT License.

## 🙏 Acknowledgments

- Google Gemini AI for recipe generation
- Unsplash for beautiful images
- FastAPI and React communities

---

**Enjoy cooking with CodeToCook! 🍳✨**
