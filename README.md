# 📰 News API

<div align="center">
  
  *A lightweight news API built with FastAPI and Supabase*
  
  [![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=flat&logo=fastapi)](https://fastapi.tiangolo.com)
  [![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat&logo=supabase&logoColor=white)](https://supabase.com)
  [![Render](https://img.shields.io/badge/Render-46E3B7?style=flat&logo=render&logoColor=white)](https://render.com)
  
</div>

## 🚀 Local Development

```bash
# Install dependencies
pip install -r requirements.txt

# Run the server
uvicorn main:app --reload --port 8000
```

Your API will be available at `http://localhost:8000`

---

## ☁️ Deploy on Render

### Prerequisites
- [Render](https://render.com) account (free tier available)
- [Supabase](https://supabase.com) project
- Git repository (GitHub/GitLab/Bitbucket)

### Quick Deploy

<details>
<summary><b>📦 1. Repository Setup</b></summary>

Ensure your repo includes:
- `main.py`
- `requirements.txt`
- No `.env` file (use environment variables instead)
</details>

<details>
<summary><b>⚙️ 2. Create Web Service</b></summary>

1. Go to [dashboard.render.com](https://dashboard.render.com)
2. Click **"New +"** → **"Web Service"**
3. Connect your repository

**Configuration:**
- **Name**: `news-api` (or your choice)
- **Runtime**: `Python 3`
- **Build Command**: `pip install -r requirements.txt`
- **Start Command**: `uvicorn main:app --host 0.0.0.0 --port $PORT`
</details>

<details>
<summary><b>🔐 3. Environment Variables</b></summary>

Add these from your [Supabase settings](https://app.supabase.com/project/_/settings/api):

| Variable | Description |
|----------|-------------|
| `SUPABASE_URL` | Your project URL |
| `SUPABASE_ANON_KEY` | Your anon/public key |
| `TABLE_NEWS` | `news` (table name) |

</details>

<details>
<summary><b>🚀 4. Deploy</b></summary>

- Select **Free** plan
- Click **"Create Web Service"**
- Wait 2-3 minutes for first deployment
- Access your API at: `https://news-api.onrender.com`
- Interactive docs at: `https://news-api.onrender.com/docs`
</details>

---

## ⚡ Free Tier Notes

- 💤 App sleeps after **15 minutes** of inactivity
- ⏰ First request may take **~30 seconds** (cold start)
- ⏱️ Includes **750 hours/month** of runtime

---

## 🔧 Troubleshooting

| Issue | Solution |
|-------|----------|
| App fails to start | Check start command includes `$PORT` |
| Missing env vars | Verify `SUPABASE_URL` and `SUPABASE_ANON_KEY` are set |
| Auto-deploy not working | Check branch settings in Render dashboard |

---

<div align="center">
  
  ***Live Demo**: `https://news-api.onrender.com` (probably not working at the moment you saw this)
  
</div>
