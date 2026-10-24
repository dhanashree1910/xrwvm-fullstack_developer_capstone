# Best Cars Dealership

**Repository name:** `xrwvm-fullstack_developer_capstone`
**Project name:** Best Cars Dealership – Full Stack Django + React Application

## Overview

Best Cars is a full stack dealership review application built with Django, React and Node/Express microservices. Users can browse dealerships, filter them by state, read and post reviews, and see the sentiment of each review.

## Features

- User registration, login and logout (Django authentication)
- Dealer listing, filtering by state and dealer detail pages
- Dealer reviews with sentiment analysis (positive / neutral / negative)
- Car makes and models catalogue
- Static pages: Home, About Us, Contact Us
- Django admin site for managing car makes and models
- CI/CD with GitHub Actions and deployment to the cloud

## Tech Stack

| Layer | Technology |
|-------|------------|
| Backend | Django, Django REST-style views |
| Frontend | React, HTML, CSS, Bootstrap |
| Dealer/review service | Node.js, Express, MongoDB, Docker |
| Sentiment service | Flask / Cloud service |
| CI/CD | GitHub Actions |

## Project Structure

```
server/
├── djangoproj/          # Django project settings and root URLs
├── djangoapp/           # Django app: views, models, API proxies
├── database/            # Express + MongoDB dealer/review service
└── frontend/
    ├── static/          # About.html, Contact.html, Home, CSS, images
    └── src/components/  # React components (Login, Register, Dealers, ...)
```

## Getting Started

```bash
# Backend
cd server
python3 -m venv venv && source venv/bin/activate
pip install -r requirements.txt
python manage.py makemigrations
python manage.py migrate --run-syncdb
python manage.py createsuperuser
python manage.py runserver

# Frontend
cd server/frontend
npm install
npm run build
```

## Main API Endpoints

| Purpose | Endpoint |
|---------|----------|
| Login | `POST /djangoapp/login` |
| Logout | `GET /djangoapp/logout` |
| Register | `POST /djangoapp/register` |
| All dealers | `GET /djangoapp/get_dealers` |
| Dealers by state | `GET /djangoapp/get_dealers/<state>` |
| Dealer by ID | `GET /djangoapp/dealer/<id>` |
| Dealer reviews | `GET /djangoapp/reviews/dealer/<id>` |
| Car makes and models | `GET /djangoapp/get_cars` |
| Post review | `POST /djangoapp/add_review` |

## License

This project was created for educational purposes.
