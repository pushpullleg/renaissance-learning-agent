# renaissance-learning-agent

A Streamlit app that walks learners through a personalized career roadmap, with an AI tutor and a live analytics panel. Built for the Business Analytics and Data Engineering tracks.

The tutor is powered by OpenAI. The analytics panel reads from a local event log so it works without any external services. Everything runs inside Streamlit — no backend, no database required.

## Running locally

```bash
pip install -r requirements.txt
```

Add your OpenAI key if you want the tutor to respond (optional — the rest of the app works without it):

```
# .env
OPENAI_API_KEY=sk-your-key
```

```bash
streamlit run app/main_app.py
```

## Structure

```
app/
├── main_app.py           # navigation and global state
├── components/           # tutor and analytics panels
├── pages/                # landing, onboarding, roadmap pages
└── data/tutor_events.json
assets/                   # images and branding
```

`app/data/tutor_events.json` contains pre-populated events so the analytics tab renders on first load. Delete it to start fresh.

Only the Business Analytics → Data Engineer path is wired end-to-end. Other roadmap branches exist in the UI but are not yet interactive.

## License

MIT
