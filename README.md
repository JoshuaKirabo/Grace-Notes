Grace Notes

⸻

Emotion-Based Music for Better Direction

Grace Notes is an emotion-aware music application that responds to what the user is feeling through text or voice, then builds music recommendations that do more than just mirror the mood. Instead of keeping the listener stuck in anger, heartbreak, bitterness, or emotional chaos, Grace Notes aims to guide the moment toward something healthier such as peace, healing, joy, gratitude, release, reflection, or hope.

The app is built around a simple idea: music shapes people. Because of that, Grace Notes is not only concerned with whether a song matches the feeling, but also with where that song may lead the listener emotionally. By combining mood understanding, intent detection, curated recommendation logic, and streaming platform integrations, Grace Notes is designed as a thoughtful music experience rather than just another playlist generator.

⸻

Project Scope
	•	Text-based mood input
	•	Voice-based mood input
	•	Emotion and intent detection from user input
	•	Playlist generation based on emotional direction
	•	Spotify API integration for track and playlist retrieval
	•	Apple Music integration planned for later
	•	Recommendation logic focused on uplifting, grounding, calming, healing, and joyful outcomes

⸻

Core Features
	•	Mood detection from natural language input
	•	Voice or text check-in flow
	•	Intent-aware recommendation logic, not just emotion matching
	•	Playlist generation based on emotional path such as peace, healing, gratitude, release, or joy
	•	Music filtering that avoids content likely to keep users stuck in harmful emotional loops
	•	Short supportive response before playback
	•	Future support for saving sessions, feedback, and personalization

⸻

Tech Stack

Frontend

<p align="left">
  <img src="https://skillicons.dev/icons?i=nextjs,tailwind" alt="Frontend Icons" />
</p>


Next.js and Tailwind CSS

Backend

<p align="left">
  <img src="https://skillicons.dev/icons?i=python,fastapi" alt="Backend Icons" />
</p>


Python and FastAPI

This project uses a Python backend instead of Spring Boot to keep the stack a bit different and let the recommendation logic move faster during early development.

APIs and Integrations

<p align="left">
  <img src="https://skillicons.dev/icons?i=spotify" alt="Spotify Icons" />
</p>


Spotify Web API for catalog search, tracks, playlists, and playback handoff

Future Expansion
	•	Apple Music API
	•	Speech-to-text support
	•	Smarter personalization based on user feedback

Infrastructure and DevOps

<p align="left">
  <img src="https://skillicons.dev/icons?i=docker,git,github" alt="Infrastructure Icons" />
</p>


Docker, Git, and GitHub

⸻

System Architecture

Grace Notes follows a modular full-stack structure so the recommendation logic stays independent from the streaming provider.
	•	The Next.js frontend handles the user check-in flow, voice or text input, playlist display, and playback handoff.
	•	The backend manages mood parsing, intent detection, recommendation logic, and provider integration.
	•	The emotion engine converts natural language such as “I need to forgive” or “I feel grateful for my friends” into mood tags, intent tags, and emotional direction.
	•	The recommendation engine maps those tags into musical traits such as calm, reflective, warm, bright, healing, or celebratory.
	•	The provider layer connects to Spotify first, with room to add Apple Music later without rewriting the main logic.

Example Recommendation Flow
	1.	User enters or speaks how they feel.
	2.	Grace Notes identifies the emotional state and what the user may need.
	3.	The backend builds a recommendation profile.
	4.	Spotify returns matching songs or playlists.
	5.	The app presents a short supportive line and the resulting playlist.

⸻

Why This Project Exists

Grace Notes was inspired by the belief that music does more than fill silence. It can shape thought patterns, emotional habits, language, and identity over time. Many music apps focus on matching a mood, but that alone is not always helpful. Someone who feels angry may not need music that deepens anger. Someone who feels heartbroken may not need songs that trap them in despair. Someone who feels joyful may want music that helps them celebrate in a healthy and meaningful way.

This project exists to explore a better approach. Grace Notes tries to meet the listener where they are emotionally, while also helping move them toward a better place. That better place might be peace instead of rage, healing instead of bitterness, gratitude instead of emptiness, or joy instead of emotional numbness.

At its core, Grace Notes is a fun project with a serious idea behind it: what people repeatedly listen to can influence who they are becoming. Because of that, this app is built to recommend music that is emotionally aware, but also thoughtful about direction.

⸻

Current MVP Direction

The first version of Grace Notes focuses on simplicity.
	•	User types how they feel
	•	The system identifies the mood and intent
	•	The backend maps that to emotional categories such as peace, healing, joy, gratitude, release, or reflection
	•	Spotify is used to fetch songs or playlists that match the target direction
	•	The app returns a playlist and a short supportive line

Examples:
	•	“I’m angry” -> release, then peace
	•	“I need to forgive” -> reflection, healing, calm
	•	“I’m in love” -> warmth, joy
	•	“I’m grateful for my friends” -> gratitude, celebration
	•	“I feel heavy” -> comfort, peace

⸻

Prerequisites

To run this project locally, install the following:
	•	Node.js and npm
	•	Python 3.11+
	•	Git
	•	Spotify Developer credentials
	•	Docker, optional for containerized setup

⸻

Local Setup

1. Clone the Repository

git clone https://github.com/your-username/grace-notes.git
cd grace-notes

2. Configure Environment Variables

Create a .env file and add the required values.

Example:

SPOTIFY_CLIENT_ID=your_client_id
SPOTIFY_CLIENT_SECRET=your_client_secret

3. Install Dependencies

Frontend:

cd frontend
npm install

Backend:

cd backend
pip install -r requirements.txt

4. Run the Project

Frontend:

npm run dev

Backend:

uvicorn app.main:app --reload

5. Access the Application
	•	Frontend: http://localhost:3000
	•	Backend API: http://localhost:8000

⸻

Future Ideas
	•	Voice input with speech-to-text
	•	Apple Music support
	•	Save past mood sessions
	•	Playlist refinement controls such as more hopeful, less intense, or more calm
	•	Light journaling tied to music sessions
	•	User feedback loop to improve recommendations over time

⸻

Repository Structure

grace-notes/
├── frontend/          # Next.js UI for mood input, playlist display, and playback handoff
├── backend/           # FastAPI backend for mood parsing and recommendations
├── docs/              # notes, diagrams, and planning docs
├── .github/           # workflows and repo config
├── .env.example
└── README.md


⸻

Notes

This project is currently being built as a personal learning project and creative experiment. The focus is on building something meaningful, enjoyable, and technically solid while exploring how emotion-aware software can shape a better listening experience.
