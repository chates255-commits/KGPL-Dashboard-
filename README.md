# KGPL LPG Cloud Dashboard (IHB)

Shared web application for Kandla–Gorakhpur LPG Pipeline allocation, availability, demand and tariff.

## Features
- Role-based login: Master / Plant / Source
- Product Availability at Source (OMC-wise)
- Daily Demand with availability validation
- Actual receipt + tariff (₹3.95/MT/Km + ₹0.01 + GST 18%)
- OMC-wise and date-wise billing
- Shared database — all PCs see the same data

## Deploy on Render.com (Free)

1. Create account at https://render.com
2. New → Web Service → connect your GitHub repo (or upload this folder)
3. Settings:
   - **Build Command:** `pip install -r requirements.txt`
   - **Start Command:** `gunicorn app:app --bind 0.0.0.0:$PORT`
   - **Environment:** Python 3
4. Add environment variable (optional): `SECRET_KEY` = any long random string
5. Deploy → you get a public URL like `https://kgpl-xxxxx.onrender.com`

## Local run
```bash
pip install -r requirements.txt
python app.py
```
Open http://127.0.0.1:5000

## Default Master Login
- User ID: `master`
- Password: `Master@IHB2026`

Change password after first login.
Plant and source credentials are in Masters page (Master login only).
