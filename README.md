# X_Clone
# X_Clone

A minimal Twitter/X-like clone (frontend + Express/MongoDB backend). This repo contains a `server` (Express + MongoDB) and a `client` (React + Vite + Tailwind).

## Features
- User signup / login (JWT in cookie)
- Create and list posts (with optional image uploads via Cloudinary)
- Follow/unfollow users, notifications

## Tech stack
- Backend: Node.js, Express, Mongoose (MongoDB)
- Frontend: React, Vite, Tailwind CSS
- Auth: JWT stored in HTTP-only cookies
- Image hosting (optional): Cloudinary

## Environment
- Copy `.env.example` to a new file named `.env` at the project root and fill in real values.
- `.env` is ignored by git; keep secrets out of the repo.

## Setup (Windows PowerShell)

From project root (install server deps and run the backend):

```powershell
cd c:\Users\firas\Desktop\X_Clone-main
cd server
npm install
cd ..
npm run dev
```

In a separate terminal, start the frontend:

```powershell
cd c:\Users\firas\Desktop\X_Clone-main\client
npm install
npm run dev
```

The client runs on port `4000` and proxies API requests starting with `/api` to the backend at `http://localhost:5000` (configured in `client/vite.config.js`).

## Common issues
- `ECONNREFUSED` from Vite proxy: ensure the backend is running and listening on the same port as configured in `client/vite.config.js` (default `5000`).
- DB connection errors: confirm `MONGODB_URI` in your `.env` and that MongoDB is reachable.

## Deployment
- For production, build the client (`cd client && npm run build`) and deploy the server and built client to your host of choice. Review cookie settings for `secure` and `sameSite` in `server/security/generateToken.js`.

## Contributing
- Open issues or PRs. If you plan to run locally, follow the setup steps above and ensure you have a local MongoDB instance or a cloud MongoDB URI.


