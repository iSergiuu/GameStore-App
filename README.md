# GameStore-App

A game store application built to manage products, shopping cart functionality, orders, and administrative operations in a simple and scalable web platform.

## Overview

GameStore-App is a full-stack e-commerce style project focused on the sale of video games. It provides a user-facing storefront, a shopping cart flow, and administrative tools for managing the product catalog and customer orders.

The project is designed to showcase a complete online shopping experience with a clean separation between the frontend and backend layers.

---

## Key Features

- Browse and view game products
- Add games to the shopping cart
- Manage cart items and quantities
- Checkout and order creation flow
- User authentication and session management
- Product management for admins
- Order tracking and order history
- Responsive UI
- REST API backend

---

## Tech Stack

| Layer | Technology |
|------|------------|
| Frontend | React + Vite |
| Backend | Node.js / Express |
| Database | PostgreSQL / MongoDB (depending on setup) |
| API Communication | Axios |
| Language | JavaScript |
| Styling | CSS / SCSS |
| Build Tool | Vite |

---

## Project Structure

```text
GameStore-App/
├── backend/
│   ├── src/
│   │   ├── controllers/
│   │   ├── models/
│   │   ├── routes/
│   │   ├── services/
│   │   ├── config/
│   │   └── server.js
│   ├── package.json
│   └── .env
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   ├── vite.config.js
│   └── index.html
├── README.md
├── .gitignore
└── package.json
```

---

## Prerequisites

Before running the project, make sure you have:

- Node.js 18 or newer
- npm
- A database instance (PostgreSQL or MongoDB depending on backend configuration)
- Git

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/iSergiuu/GameStore-App.git
cd GameStore-App
```

### 2. Install dependencies

Install both frontend and backend dependencies:

```bash
cd backend
npm install

cd ../frontend
npm install
```

---

## Configuration

Create environment files for the backend and frontend if needed.

### Backend `.env`

```env
PORT=5000
DATABASE_URL=your_database_url
JWT_SECRET=your_secret_key
```

### Frontend example

```env
VITE_API_BASE_URL=http://localhost:5000/api
```

---

## Running the Application

### Start the backend

```bash
cd backend
npm run start
```

If the backend uses `nodemon` for development:

```bash
npm run dev
```

### Start the frontend

```bash
cd frontend
npm run dev
```

Then open the app in the browser:

```text
http://localhost:5173
```

---

## Main API Endpoints

Below are common endpoints used in a game store application:

```http
GET /api/products
GET /api/products/:id
POST /api/products
PUT /api/products/:id
DELETE /api/products/:id

POST /api/auth/login
POST /api/auth/register

GET /api/cart
POST /api/cart/add
PUT /api/cart/update
DELETE /api/cart/remove

POST /api/orders
GET /api/orders/:id
GET /api/orders
```

---

## Usage

1. Open the storefront in the browser.
2. Browse the game catalog.
3. Add items to the cart.
4. Proceed to checkout.
5. Complete the order flow.
6. Admin users can manage products and order information.

---

## Roles and Permissions

| Role | Permissions |
|------|------------|
| Customer | Browse products, add to cart, place orders |
| Admin | Manage catalog, update product data, view orders |

---

## Testing

### Run backend tests

```bash
cd backend
npm test
```

### Run frontend build

```bash
cd frontend
npm run build
```

---

## Troubleshooting

### Backend not starting

- Check whether the port is already in use
- Verify the database connection string
- Confirm environment variables are correctly set

### Frontend not connecting to backend

- Make sure the backend server is running
- Verify `VITE_API_BASE_URL` in the frontend environment
- Confirm the backend CORS settings are enabled

### `npm install` fails

```bash
rm -rf node_modules package-lock.json
npm install
```

---

## Contribution

Contributions are welcome.

```bash
git checkout -b feature/new-feature
git commit -m "Add new feature"
git push origin feature/new-feature
```

Then open a Pull Request on GitHub.

---

## License

This project is intended for educational and personal use.

---

## Support

If you encounter issues, open a GitHub issue or contact the project maintainer.

---

Last updated: October 2026
Version: 1.0.0
