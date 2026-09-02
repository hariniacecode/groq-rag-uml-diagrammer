# Groq RAG UML Diagrammer

An interactive UML diagram generator with AI-powered Q&A using Groq API, RAG (Retrieval Augmented Generation), and PostgreSQL.

## 🎯 Features

- **Interactive UML Canvas** - Create and edit software engineering diagrams in real-time
- **Groq AI Integration** - Fast inference for diagram generation and analysis
- **RAG System** - Semantic search over UML patterns and best practices
- **Beautiful UI** - Modern design with Tailwind CSS
- **Real-time Chat** - Ask questions about your diagrams, get AI-powered insights
- **Database Persistence** - PostgreSQL storage for diagrams and chat history
- **Dark Theme** - Eye-friendly interface for long coding sessions

## 🛠 Tech Stack

### Backend
- **FastAPI** - Modern Python web framework
- **PostgreSQL** - Relational database
- **Groq API** - Fast LLM inference
- **SQLAlchemy** - ORM
- **LangChain** - RAG and embeddings

### Frontend
- **HTML5** - Semantic markup
- **Tailwind CSS** - Utility-first styling
- **Vanilla JavaScript** - Dynamic interactions (no framework bloat)
- **SVG Canvas** - Diagram rendering

## 📁 Project Structure

```
groq-rag-uml-diagrammer/
├── backend/
│   ├── app/
│   │   ├── main.py
│   │   ├── models.py
│   │   ├── schemas.py
│   │   ├── database.py
│   │   ├── config.py
│   │   └── routes/
│   │       ├── diagrams.py
│   │       ├── chat.py
│   │       └── rag.py
│   ├── requirements.txt
│   └── .env.example
├── frontend/
│   ├── index.html
│   ├── css/
│   │   └── style.css
│   └── js/
│       ├── app.js
│       ├── canvas.js
│       ├── chat.js
│       ├── api.js
│       └── utils.js
├── docs/
│   └── API.md
└── docker-compose.yml
```

## 🚀 Quick Start

### Prerequisites
- Python 3.10+
- Node.js (for frontend dev tools, optional)
- PostgreSQL 14+
- Groq API Key

### Installation

1. Clone the repository
```bash
git clone https://github.com/hariniacecode/groq-rag-uml-diagrammer.git
cd groq-rag-uml-diagrammer
```

2. Backend setup
```bash
cd backend
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

3. Environment configuration
```bash
cp .env.example .env
# Edit .env with your Groq API key and PostgreSQL credentials
```

4. Database initialization
```bash
python -m app.database init
```

5. Run FastAPI server
```bash
uvicorn app.main:app --reload
```

6. Open frontend
```bash
# In another terminal, from project root
python -m http.server 8080 --directory frontend
```

Visit: `http://localhost:8080`

## 📚 API Endpoints

### Diagrams
- `GET /api/diagrams` - List all diagrams
- `POST /api/diagrams` - Create new diagram
- `GET /api/diagrams/{id}` - Get diagram details
- `PUT /api/diagrams/{id}` - Update diagram
- `DELETE /api/diagrams/{id}` - Delete diagram

### Chat & RAG
- `POST /api/chat` - Send message to AI
- `GET /api/chat/history/{diagram_id}` - Get chat history
- `POST /api/rag/search` - Semantic search

## 🔑 Environment Variables

```
GROQ_API_KEY=your_key_here
DATABASE_URL=postgresql://user:password@localhost/uml_db
JWT_SECRET=your_secret_key
```

## 📖 Usage

1. **Create a Diagram** - Click "New Diagram" and select type (Class, Sequence, Use Case, etc.)
2. **Draw Elements** - Drag shapes from toolbar onto canvas
3. **Ask AI** - Use the chat panel to ask questions or get suggestions
4. **Save & Export** - Save to database or export as SVG/PNG

## 🤝 Contributing

Pull requests welcome! Please follow the existing code style.

## 📄 License

MIT

## 📞 Support

For issues and questions, please open a GitHub issue.
