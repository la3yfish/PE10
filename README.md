# AI Content Generator

A FastAPI-based service that generates blog posts using OpenAI's GPT-5 model and incorporates the latest news on a given topic from Currents API.

## Features

- Generates catchy article titles
- Creates SEO-friendly meta descriptions
- Produces full blog posts with structure (introduction, main body, conclusion)
- Incorporates latest news and trends into content

## Setup

1. Create a `.env` file with the following variables:
   ```
   OPENAI_API_KEY=your_openai_api_key
   CURRENTS_API_KEY=your_currents_api_key
   PORT=8000
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Running the Service

```bash
python app.py
```

The service will start on `http://0.0.0.0:8000` by default.

## API Endpoints

- `GET /` - Health check
- `GET /heartbeat` - Service status check
- `POST /generate-post` - Generate a blog post

## Request Example

```bash
curl -X POST "http://localhost:8000/generate-post" \
  -H "Content-Type: application/json" \
  -d '{"topic": "artificial intelligence"}'
```

## Response

```json
{
  "title": "Article title",
  "meta_description": "SEO meta description",
  "post_content": "Full article content..."
}
```
