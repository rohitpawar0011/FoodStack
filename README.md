# FoodStack

> Full-stack food ordering web application (Frontend + Backend)

Live demo: [https://food-stack-8nk8.vercel.app/](https://food-stack-8nk8.vercel.app/)

---

## Table of Contents

* [About](#about)
* [Features](#features)
* [Tech Stack](#tech-stack)
* [Prerequisites](#prerequisites)
* [Folder Structure](#folder-structure)
* [Environment Variables](#environment-variables)
* [Local Setup](#local-setup)

  * [Backend](#backend)
  * [Frontend](#frontend)
* [Build & Deploy](#build--deploy)
* [API Endpoints (example)](#api-endpoints-example)
* [Contributing](#contributing)
* [License](#license)

---

## About

FoodStack is a full-stack web application that demonstrates a typical food ordering flow: browse restaurants/menus, add items to cart, place orders and manage user authentication. This README provides setup instructions and notes so contributors can get the project running locally.

## Features

* User authentication (signup / login)
* Browse restaurants and menus
* Add/remove items to cart
* Place orders and view order history
* Admin or vendor pages (optional) to manage menu/items

> Note: Exact feature availability depends on the code in `frontend/` and `backend/` folders. Treat the sections below as a tested, generic guide — replace any placeholders with actual values from your project.

## Tech Stack

* Frontend: JavaScript (React) — likely Vite or CRA
* Backend: Node.js + Express (or similar)
* Database: MongoDB / PostgreSQL (configure via env)
* Deployment: Vercel (frontend) and any Node host / Vercel for backend

## Prerequisites

* Node.js (v16+ recommended)
* npm or yarn
* Database (MongoDB Atlas or local) if the backend uses a DB

## Folder Structure

```
FoodStack/
├─ backend/          # Node/Express API
├─ frontend/         # React app
├─ .gitignore
└─ README.md         # <- this file
```

## Environment Variables

Create `.env` files in `backend/` and `frontend/` (if needed). Example variables:

**backend/.env**

```
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_here
```

**frontend/.env**

```
VITE_API_URL=http://localhost:5000/api
# or REACT_APP_API_URL=http://localhost:5000/api (for CRA)
```

Replace the variable names above with whatever your code expects.

## Local Setup

### Backend

1. Open a terminal and navigate to the `backend/` folder:

```bash
cd backend
```

2. Install dependencies:

```bash
npm install
# or
# yarn
```

3. Create `.env` in `backend/` with the required variables (see above).
4. Start the server (common scripts):

```bash
npm run dev    # if using nodemon
# or
npm start      # for production start
```

5. The API should be available at `http://localhost:5000` (or whatever PORT you set).

### Frontend

1. Open another terminal and navigate to `frontend/`:

```bash
cd frontend
```

2. Install dependencies:

```bash
npm install
# or yarn
```

3. Create `.env` in `frontend/` and set `VITE_API_URL` or `REACT_APP_API_URL` to point to your backend.
4. Start the dev server:

```bash
npm run dev
# or
npm start
```

5. Visit `http://localhost:3000` (or port printed by the dev server).

## Build & Deploy

* Frontend: `npm run build` will create a production bundle (for Vercel/Netlify deploy).
* Backend: Ensure environment variables are set in your host and run `npm start`.

If you deploy frontend on Vercel (as in the repo README link), point the frontend's API environment variable in Vercel dashboard to your backend URL.

## API Endpoints (example)

*These are example endpoints to test your local backend. Update them to match your code.*

```
POST /api/auth/register   # signup
POST /api/auth/login      # login
GET  /api/restaurants     # list restaurants
GET  /api/restaurants/:id # restaurant menu
POST /api/orders          # create order
GET  /api/orders/:userId  # user orders
```

Use a tool like Postman or Insomnia to test APIs.

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feat/my-feature`
3. Commit your changes: `git commit -m "Add some feature"`
4. Push to your branch: `git push origin feat/my-feature`
5. Open a Pull Request

Please follow any coding style/contribution rules you want to enforce and include clear commit messages.

## Troubleshooting

* If `npm install` fails, try clearing `node_modules` and reinstalling:

```bash
rm -rf node_modules package-lock.json
npm install
```

* If the frontend cannot reach backend, ensure CORS is enabled in backend or both run on same host. Also verify the API URL in your frontend `.env`.

## License

Specify a license (e.g. MIT) or add one to the repository. Example:

```
MIT License

Copyright (c) 2025 Rohit Pawar

Permission is hereby granted, free of charge, to any person obtaining a copy
... (add full MIT text if desired)
```

---

### Want it committed?

If you'd like, I can create a `README.md` file in the repository (or a PR) with this content — tell me whether to include any project-specific details (exact start scripts, DB type, JWT usage, screenshots, or license) and I’ll add them.
