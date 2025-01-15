# Fantasy-Sports
Qdrant Fantasy Sports
This repository contains a FastAPI application for providing fantasy sports suggestions using Qdrant as a vector database. The application takes user preferences and returns relevant player suggestions.

Features
Get player recommendations based on sport, team, and player preferences.
FastAPI framework for building APIs.
Qdrant client for handling vector data.
Installation
Clone this repository:

git clone https://github.com/manas95826/Qdrant-fantasy-sports.git
cd Qdrant-fantasy-sports
Install the required packages:

pip install fastapi uvicorn qdrant-client
Set up your Qdrant environment. Make sure to have Qdrant running locally or in a Docker container. If using Docker:

docker run -p 6333:6333 qdrant/qdrant
Optionally, set the QDRANT_URL environment variable if your Qdrant instance is hosted elsewhere.

Usage
Run the FastAPI application:

uvicorn app:app --reload
Open your browser and go to http://localhost:8000/docs to access the API documentation.

Use the /suggestions/ endpoint to get player suggestions based on user preferences.

Example Request
{
  "sport": "Basketball",
  "team": "Lakers",
  "player": "LeBron James"
}
Example Response
{
  "suggestions": [
    {
      "player": "Player A",
      "team": "Team X",
      "sport": "Basketball",
      "score": 95
    },
    {
      "player": "Player B",
      "team": "Team Y",
      "sport": "Basketball",
      "score": 88
    }
  ]
}
