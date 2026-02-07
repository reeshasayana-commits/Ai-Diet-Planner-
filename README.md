# AI Diet Planner

The AI Diet Planner is a Python-based web application built with Flask that generates personalized diet plans using artificial intelligence (OpenAI API via OpenRouter). It allows users to input their personal details, health goals, and dietary restrictions to receive tailored meal recommendations.

## Features

- **Personalized Diet Generation:** Creates customized breakfast, lunch, and dinner plans based on user input (age, weight, height, activity level, etc.).
- **Disease-Specific Considerations:** Adjusts recommendations for conditions like Diabetes, High Blood Pressure, and Cholesterol.
- **Save & Manage Plans:** Automatically saves generated plans to a local JSON database (`diet_plans.json`). Users can view and delete saved plans.
- **PDF Export:** Allows users to download their diet plan as a PDF document.
- **Fallback Mechanism:** Includes a default diet plan if the AI service is unavailable.
- **User-Friendly Interface:** simple web interface for easy data entry and result viewing.

## Technology Stack

- **Backend:** Python, Flask
- **AI Integration:** OpenAI API (via OpenRouter)
- **Data Storage:** JSON (`diet_plans.json`)
- **PDF Generation:** ReportLab
- **Frontend:** HTML/CSS (in templates)

## Project Structure

- `app.py`: Main application logic, handling routes, API calls, and data processsing.
- `diet_plans.json`: Local storage for generated diet plans.
- `templates/`: Contains HTML templates for the web interface (`index.html`, `result.html`, `saved.html`).
- `.env`: Environment variables file (stores API keys).

## Setup & Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/reeshasayana-commits/Ai-Doctor-Chatbot-
    ```
2.  **Install dependencies:**
    (You may need to create a `requirements.txt` file based on imports in `app.py`)
    ```bash
    pip install flask openai markdown reportlab python-dotenv
    ```
3.  **Configure Environment:**
    Create a `.env` file in the root directory and add your OpenRouter API key:
    ```
    OPENROUTER_API_KEY=your_api_key_here
    ```
4.  **Run the application:**
    ```bash
    python app.py
    ```
5.  **Access the app:**
    Open your browser and navigate to `http://127.0.0.1:5000/`.

## Usage

1.  Fill out the form on the home page with your personal details and health information.
2.  Click "Generate Diet Plan".
3.  View your personalized plan.
4.  Optionally save the plan or download it as a PDF.
5.  View saved plans via the "Saved Plans" link.
