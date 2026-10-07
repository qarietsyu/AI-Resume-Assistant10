# ATS Resume Checker

Upload a resume (PDF, DOCX or TXT) and get an ATS score, a score breakdown, missing keywords,
formatting issues and specific improvements. Optionally paste a job description for a role-specific score.

Built with Streamlit and Google Gemini Flash.

## Run locally
```bash
pip install -r requirements.txt
mkdir .streamlit
echo 'GEMINI_API_KEY = "your-key-here"' > .streamlit/secrets.toml
streamlit run app.py
```
Get a free API key at https://aistudio.google.com/apikey

## Deploy
1. Push this repo to GitHub (do NOT upload `.streamlit/secrets.toml`).
2. On https://share.streamlit.io click **Create app**, pick the repo, branch `main`, main file `app.py`.
3. Open **Advanced settings > Secrets** and paste: `GEMINI_API_KEY = "your-key-here"`
4. Deploy.

Optional secret/env var: `GEMINI_MODEL` (default `gemini-2.5-flash`).
