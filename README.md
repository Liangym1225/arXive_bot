# ArXiv Paper Management Tool


This project helps researchers stay updated with the daily papers published on arXiv. It includes:
* A backend to fetch and rank papers by relevance using an LLM.
* A frontend to view paper titles, abstracts, and relevance scores
* An Integration with Notion for easy organization



https://github.com/user-attachments/assets/a188dc4b-ce54-4f58-9e41-4ee245c95661




<img width="829" alt="demo" src="https://github.com/user-attachments/assets/032487af-17a0-46dc-b337-82679a62c5fd" />

# Features

1. **Fetch Papers**
  * Retrieves papers from arXiv within a specific category published in the last 24 hours.
2. **Relevance Calculation with a Language Model**
  * Uses a pretrained text embedding model (`jinaai/jina-embeddings-v3`) to generate embeddings for paper abstracts.
  * Calculates cosine similarity between fetched papers and predefined reference texts.
  * Sorts papers by relevance score.
3. **Notion Integration**
  * Adds selected papers to a Notion database via the Notion API.
4. **Web UI**
  * Displays titles, abstracts, and relevance scores of fetched papers.
  * Allows users to add papers to Notion with a single click.



# Usage
```
git clone https://github.com/Liangym1225/arXiv_app.git
```
Install Pytorch, Transformers  
Create `.env` with your notion api token as `/backend/.env.sample`
```
cd arXiv_app
cd backend
python -m uvicorn main:app --reload
```
```
npm install
npm run start
```
