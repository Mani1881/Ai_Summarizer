## Project Overview

This project is a web application designed to provide text summarization functionality. It uses a combination of HTML, CSS, JavaScript for the front end, and Node.js for the backend. The backend integrates with the Hugging Face Inference API to generate summarized text from user input.

## Project Structure

```
/text-summarizer-web-app
│
├── /public                # Frontend files
│   ├── index.html         # Main HTML file
│   ├── style.css          # CSS file for layout and styling
│   └── script.js          # JavaScript file for frontend interactions
│
├── /node_modules          # Node.js dependencies
│
├── index.js
├──summarize.js             # Backend server file (Node.js)
├── package.json           # Project metadata and dependencies
├── .env                   # Environment variables (Hugging Face API Key)
└── README.md              # Project documentation
```

## Features

- **User Input**: A text area where users can input the text they want to summarize.
- **Submit Button**: Triggers the backend to summarize the text.
- **Summary Output**: Displays the summarized text once the backend processes the input.
- **Frontend Validation**: Ensures the text length is within a valid range (200 to 100,000 characters).

## Installation

### 1. Clone the repository
```bash
git clone <repository-url>
cd <project-directory>
```

### 2. Install dependencies
For backend dependencies:
```bash
npm install
```

### 3. Set up Hugging Face API
- Sign up on [Hugging Face](https://huggingface.co/) and obtain an API key.
- Add your API key as shown as ![Screenshot 2024-12-05 093924](https://github.com/user-attachments/assets/1eeab99c-0d2f-456e-a295-746427a93965)
```bash
HUGGINGFACE_API_KEY=<your-api-key>
```

## Running the Application

###  Start the backend server
```bash
node index.js
```

## Project Flow

### Frontend
1. **User Input**: The user enters text in the input field.
2. **Validation**: The text length is validated (ensuring it’s between 200 and 100,000 characters).
3. **Submit**: The user clicks the submit button to send the input to the backend.
4. **User Request**: The frontend sends an  POST request to the `/summarize` endpoint.
5. **Display Summary**: Once the backend responds with the summary, it’s displayed in a designated area.

### Backend
1. **Receive Request**: The backend receives the text from the frontend via the `/summarize` endpoint.
2. **API Call**: The backend makes an authenticated request to the Hugging Face Inference API.![Screenshot 2024-12-05 092837](https://github.com/user-attachments/assets/ad80d064-5944-4b70-a613-4c5cb6f920ce)
3. **Process Response**: The summarized text is returned from the API.
4. **Send Response**: The backend sends the summarized text back to the frontend.
5. **Display Summary**: The frontend displays the summarized text to the user. ![Screenshot 2024-12-05 092914](https://github.com/user-attachments/assets/934185d1-8170-4fcc-a81e-1ad29458b318)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---


