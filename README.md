# RAG AI Order Web System   By SpartanRaccon

An intelligent order management system combining OpenAI and LangChain, providing AI-driven conversational ordering service with advanced RAG (Retrieval Augmented Generation) capabilities.

## Key Features

### 🤖 AI Conversation System
- Natural language processing using OpenAI's GPT models
- Context-aware responses maintaining conversation history
- Dynamic system prompts for consistent AI personality
- Intelligent order processing and recommendation system

### 📚 Advanced RAG Implementation
- **Document Processing**:
  - Multi-format support (TXT, PDF, PowerPoint)
  - Automatic text chunking and embedding
  - Dynamic knowledge base updates

- **Vector Search**:
  - FAISS vector database integration
  - Semantic similarity search
  - Real-time query enhancement

- **Knowledge Integration**:
  - Menu and product information retrieval
  - Dynamic pricing and availability updates
  - Contextual recommendations

### 🔄 Real-time System
- WebSocket for instant order status updates
- Live chat interface with typing indicators
- Real-time inventory synchronization

### 📊 Order Management
- Complete order lifecycle management
- Order history and analytics
- Status tracking and notifications

### 🎯 Customization
- Flexible order customization options
- Dynamic menu modifications
- Personalized user preferences

## Technical Implementation

### Core Technologies
- Python 3.8+
- Flask + Flask-SocketIO
- SQLAlchemy + SQLite

### AI & NLP
- OpenAI GPT API
  - Role-based system prompts
  - Context management
  - Response streaming

### RAG Architecture
- LangChain
  - Document loaders for multiple formats
  - Text splitters for optimal chunking
  - OpenAI embeddings for vectorization
- FAISS Vector Database
  - High-performance similarity search
  - In-memory vector storage
  - Fast nearest neighbor search

### Real-time Communication
- WebSocket protocol
- Asynchronous event handling
- Real-time data synchronization

## System Architecture

```
+------------------+     +-------------------+     +------------------+
|   Client Side    |     |   Server Side     |     |   AI & RAG Layer  |
+------------------+     +-------------------+     +------------------+
| - Web Interface  |     | - Flask Server    |     | - OpenAI API     |
| - WebSocket      |<--->| - SocketIO        |<--->| - LangChain      |
| - Real-time UI   |     | - SQLAlchemy      |     | - FAISS DB       |
+------------------+     +-------------------+     +------------------+
                         |   Knowledge Base   |
                         +-------------------+
                         | - Menu Data       |
                         | - Product Info    |
                         | - Order History   |
                         +-------------------+
```

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

