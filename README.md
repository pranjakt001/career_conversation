# AI Career Conversation Assistant

An intelligent chatbot powered by OpenAI GPT-4 that represents my professional background, skills, and experience. This assistant can answer questions about my career, engage with potential employers or clients, and collect contact information from interested parties.

🔗 **[Try Live Demo](https://huggingface.co/spaces/pranjakt/career_conversation)**

## Features

- **Intelligent Conversation**: Uses GPT-4o-mini to engage in natural, professional conversations
- **Context-Aware**: Draws from LinkedIn profile and professional summary to provide accurate information
- **Lead Capture**: Automatically records user contact details when they express interest
- **Question Tracking**: Logs questions that couldn't be answered for continuous improvement
- **Real-time Notifications**: Sends notifications via Pushover when users engage

## Tech Stack

- **Python 3.x**
- **OpenAI GPT-4o-mini** - Language model for natural conversation
- **Gradio** - Web interface for the chatbot
- **PyPDF** - PDF parsing for LinkedIn profile
- **Pushover API** - Push notifications for engagement tracking

## Project Structure

```
.
├── app.py              # Main application file
├── requirements.txt    # Python dependencies
├── linkedin.pdf        # LinkedIn profile export (not included)
├── summary.txt         # Professional summary (not included)
├── .env               # Environment variables (not included)
└── README.md          # This file
```

## Setup Instructions

### Prerequisites

- Python 3.8 or higher
- OpenAI API key
- Pushover account (for notifications)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/career-conversation.git
cd career-conversation
```

2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Create a `.env` file with your credentials:
```bash
cp .env.example .env
```

5. Edit `.env` and add your API keys:
```
OPENAI_API_KEY=your_openai_api_key_here
PUSHOVER_TOKEN=your_pushover_token_here
PUSHOVER_USER=your_pushover_user_key_here
```

6. Prepare your content files:
   - Export your LinkedIn profile as a PDF and save it as `linkedin.pdf`
   - Create a `summary.txt` file with your professional summary

7. Run the application:
```bash
python app.py
```

The application will launch a Gradio interface accessible at `http://localhost:7860`

## Environment Variables

| Variable | Description |
|----------|-------------|
| `OPENAI_API_KEY` | Your OpenAI API key for GPT-4 access |
| `PUSHOVER_TOKEN` | Pushover application token |
| `PUSHOVER_USER` | Pushover user key |

## Usage

1. Visit the live demo or run locally
2. Start chatting with the AI assistant
3. Ask questions about professional background, skills, or experience
4. Provide contact information if interested in connecting

## How It Works

The assistant uses function calling to:
- **record_user_details**: Captures email addresses and contact information from interested users
- **record_unknown_question**: Logs questions that couldn't be answered for future improvements

All interactions trigger push notifications via Pushover for real-time engagement tracking.

## Deployment

This project is deployed on Hugging Face Spaces. To deploy your own version:

1. Create a Hugging Face account
2. Create a new Space with Gradio SDK
3. Upload your files
4. Add secrets in Space settings for environment variables

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Contact

For questions or collaboration opportunities, please visit the [live demo](https://huggingface.co/spaces/pranjakt/career_conversation) and chat with the assistant!

## Acknowledgments

- OpenAI for GPT-4 API
- Gradio for the excellent web interface framework
- Pushover for notification services
