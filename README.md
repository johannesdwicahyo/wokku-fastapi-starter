# Wokku FastAPI Starter

A bare-bones [FastAPI](https://fastapi.tiangolo.com/) application that deploys cleanly on [Dokku](https://dokku.com) via the Heroku Python buildpack — deploy it in one click from [Wokku](https://wokku.cloud) and get a production-grade async Python API running on your own server in under two minutes.

## One-click deploy on Wokku

[![Deploy on Wokku](https://wokku.cloud/deploy-button.svg)](https://wokku.cloud/deploy?template=wokku-fastapi-starter)

## Manual deploy (Dokku)

```bash
# On your Dokku server
dokku apps:create my-fastapi-app

# From your local machine
git remote add dokku dokku@<your-server>:my-fastapi-app
git push dokku main
```

## Stack

- **Python 3.12.7**
- **FastAPI 0.115** — async web framework
- **Gunicorn + UvicornWorker** — production ASGI server

## Local development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
uvicorn main:app --reload
```

Open <http://localhost:8000>.
