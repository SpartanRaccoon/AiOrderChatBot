# ARG AI Order Web System

An intelligent order management system combining OpenAI and LangChain, providing AI-driven conversational ordering service.

## Features

- 🤖 AI Conversation: Natural dialogue using OpenAI API
- 📚 Knowledge Base: RAG implementation with LangChain + FAISS
- 🔄 Real-time Updates: WebSocket for instant order status updates
- 📊 Order Management: Complete order lifecycle management
- 🎯 Customization: Flexible order customization options

## Tech Stack

- Python 3.8+
- Flask + Flask-SocketIO
- SQLAlchemy + SQLite
- OpenAI API
- LangChain + FAISS

## Installation

1. Clone the repository:
```bash
git clone https://github.com/SpartanRaccoon/AiOrderChatBot.git
cd AiOrderChatBot
```

2. Create virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
# or
venv\Scripts\activate  # Windows
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
```bash
cp .env.example .env
```
Edit the `.env` file with your configuration

5. Initialize database:
```bash
python init_db.py
```

6. Run the application:
```bash
python app.py
```

Visit http://localhost:8080 to start using the application

## Configuration

Configure the following parameters in your `.env` file:

- `OPENAI_API_KEY`: Your OpenAI API key
- `FLASK_ENV`: Runtime environment (development/production)
- `SECRET_KEY`: Flask secret key
- `SQLALCHEMY_DATABASE_URI`: Database connection URI

## Project Structure

```
.
├── app.py              # Main application
├── models.py           # Database models
├── init_db.py         # Database initialization script
├── requirements.txt    # Dependencies list
├── templates/         # HTML templates
├── uploads/           # File upload storage
└── instance/          # Instance configuration
```

## Contributing

Issues and Pull Requests are welcome!

## License

MIT License

