# Multi-Agent AI Fitness Assistant

The Multi-Agent AI Fitness Assistant is a smart fitness tool designed to help users track their fitness journey with AI-powered assistance. It allows users to create a fitness profile, set fitness and nutrition goals, and receive AI-generated recommendations tailored to their needs. The assistant also enables users to keep fitness notes and interact with an AI agent for personalized fitness advice.

## Features

- User Profile Creation: Users input their personal details such as name, age, weight, height, gender, and activity level.

- Goal Setting: Set fitness goals like muscle gain, fat loss, or maintaining activity levels.

- Nutrition Goals: Manually input daily caloric intake, macronutrient goals (protein, fat, and carbs), or use the AI-powered macro agent to generate personalized nutrition suggestions.

- Fitness Notes: Keep track of personal fitness-related notes (e.g., injury restrictions, gym equipment availability, dietary restrictions).

- AI-Powered Fitness Assistance: Ask the AI assistant any fitness-related questions. The AI considers user notes and profiles to provide customized responses.

## Technologies Used

### AI & Machine Learning

- LangFlow: Designed AI flows for two different agents (macro agent and fitness assistant agent).

- OpenAI GPT-4o Mini API: Used to process AI queries and generate responses.

- AstraDB Vector Database: Stores user profiles and fitness notes for contextual AI responses.

- Parse DataFrame Processing Unit: Converts database entries into JSON format for efficient data handling.

### Backend

- Python: Used for implementing AI models, database interactions, and API integration.

- LangFlow Python API: Extracted and integrated API calls from LangFlow for AI processing.

- AstraDB API: Retrieves and stores user data securely.

### Frontend

- Streamlit: Built an interactive UI for user data entry and AI interaction.

## Implementation Details

### 1. Macro Agent Flow:

  - Takes user goals and profile as input.

  - Uses a prompt and OpenAI GPT-4o Mini API to generate personalized nutrition recommendations.

### 2. Ask AI Agent Flow:

  - Uses a conditional router to determine if the query involves calculations.

  - If calculations are required, it routes to a tool-calling agent with a calculator.

  - If no calculations are needed, it connects to a fitness specialist AI prompt before calling OpenAI API.

### 3. Database Integration:

  - Connected AstraDB vector database to store user profiles and notes.

  - Used a Parse DataFrame processor to convert database entries into JSON format.

### 4. Python Integration:

  - Extracted API Python code from LangFlow into ai.py.

  - Created multiple files for database initialization and profile retrieval.

  - Used Python to build the frontend with Streamlit in main.py.

### 5. Authentication & API Management:

  - Integrated OpenAI token, AstraDB token, and LangFlow token.

  - Configured AstraDB endpoint for seamless AI data retrieval.
