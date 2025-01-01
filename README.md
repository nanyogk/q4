# "Q4 (codename) UIkit based Quiz Webapp Mockup

## Try demo at -> https://nanyogk.github.io/q4/ 
This project is a mockup for a quiz web application built with UIkit, a lightweight and modular front-end framework. The app features a card-based layout, responsive design, and interactive elements like radio buttons, accordions, and buttons.

**Built by Gemini**

## Features

*   **Card-Based Layout:** Questions and choices are presented in visually appealing cards.
*   **Responsive Design:** The layout adapts seamlessly to different screen sizes, ensuring a good user experience on both desktop and mobile devices.
*   **Interactive Elements:**
    *   **Radio Buttons:** Used for selecting answers.
    *   **Accordions (Hidden Hints):** Each choice has a plus sign icon that reveals a hidden hint (and potentially a translation) when clicked.
    *   **Buttons:** "Show Answer" and "Next" buttons control the flow of the quiz.
*   **Answer Checking:** When the "Show Answer" button is clicked:
    *   The app checks if the selected answer is correct.
    *   Displays "Right!" or "Wrong!" along with an explanation.
    *   Highlights the correct answer card with a light green background.
*   **Clean State on New Question:** When a new question loads:
    *   Radio button selections are reset.
    *   Card background colors are reset to default.
    *   Hints are closed.
    *   The page scrolls to the top.

## Project Structure

*   **`index.html`:** The main HTML file containing the structure of the web application.
*   **`style.css`:** (Embedded in `index.html`) Contains custom CSS styles for the quiz app.
*   **JavaScript:** (Embedded in `index.html`) Handles the dynamic behavior of the quiz, including:
    *   Loading questions from a JSON data source (`quizData`).
    *   Initializing and updating card elements.
    *   Handling user interactions (radio button clicks, button clicks).
    *   Checking answers and providing feedback.
    *   Managing the quiz flow (loading the next question).

## Getting Started

1.  **Clone the Repository:**
    ```bash
    git clone <repository_url>
    ```
2.  **Open `index.html`:** Open the `index.html` file in your browser.

## Data Source (`quizData`)

The quiz questions and answers are stored in a JavaScript array called `quizData` within the `<script>` tag of `index.html`. Here is the structure of the JSON data:

```json
[
    {
        "question": "Choose a word which has the same syllable as the word",
        "body": "CAT",
        "choices": [
            { "id": 1, "choice": "CAKE", "hint": "/keɪk/" },
            { "id": 2, "choice": "BAT", "hint": "/bæt/" },
            { "id": 3, "choice": "CAR", "hint": "/kɑːr/" },
            { "id": 4, "choice": "HATE", "hint": "/heɪt/" }
        ],
        "answer": 2,
        "explanation": "The word 'CAT' has one syllable, and the vowel sound is pronounced as /æ/. Among the choices, only 'BAT' shares the same vowel sound and has one syllable."
    },
    // ... more questions
]
