# EcoTrack-AI

EcoTrack-AI is a full-stack carbon footprint analysis platform that helps users understand their environmental impact and take actionable steps toward sustainability. The application combines data-driven emission calculations with AI-powered insights to deliver clear breakdowns and personalized recommendations.

## Features

- Carbon footprint calculation across Transport, Electricity, and Diet
- Visual emission breakdown using interactive charts
- AI-generated insights including emission analysis and recommendations
- Analysis history to track past carbon footprint reports
- Secure authentication and session management
- Cloud-ready architecture for scalable deployment

## Project Structure

EcoTrack-AI/
- frontend/   React (Vite) frontend application
- backend/    FastAPI backend service
- .gitignore
- README.md

## Frontend Stack

- React (Vite)
- Recharts for data visualization
- Lucide React icons
- Supabase authentication
- CSS for styling

## Backend Stack

- FastAPI
- Python
- Supabase (database and authentication)
- Groq LLM for AI-generated insights
- JWT-based authentication

## AI Architecture

The system follows a modular multi-agent design:
- Input Agent: validates and normalizes user inputs
- Carbon Agent: calculates category-wise emissions
- Recommendation Agent: generates prioritized action items
- Explanation Agent: produces structured AI explanations
- Supervisor Agent: orchestrates the complete analysis workflow

This design ensures consistency, maintainability, and reliable outputs.

## Environment Variables

All sensitive keys are stored in `.env` files and are excluded from version control.

Backend environment variables:
- GROQ_API_KEY
- SUPABASE_URL
- SUPABASE_SERVICE_KEY
- JWT_SECRET

Frontend environment variables:
- VITE_SUPABASE_URL
- VITE_SUPABASE_ANON_KEY
- VITE_BACKEND_URL

## Security

- `.env` files are ignored by Git
- No sensitive keys are hard-coded
- Backend uses secure service-level keys
- Frontend uses public Supabase anon keys only

## Local Development

Backend:
- Create a virtual environment
- Install dependencies from requirements.txt
- Run the FastAPI server using uvicorn

Frontend:
- Install dependencies using npm
- Run the development server with Vite

## Deployment

- Frontend deployed on Vercel
- Backend deployed on Render
- Database and authentication managed via Supabase

## Future Improvements

- Region-specific emission factors
- Progress tracking and comparison analytics
- Sustainability goals and milestones
- Enhanced mobile responsiveness

