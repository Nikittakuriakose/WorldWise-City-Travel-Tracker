# 🌍 WorldWise – City Travel Tracker

A simple yet powerful React app for exploring, adding, and managing cities around the world.
Built with **React Router**, **useReducer**, and **Context API**, this app demonstrates how to handle async data fetching and state management in a scalable way.

---

## 🚀 Features

* 🗺️ View all cities from a REST API (`/cities`)
* 🏙️ See details of a selected city
* ➕ Add new cities with a simple form
* ❌ Delete cities from the list
* 🌐 Filter by country
* 🔁 Auto navigation and page redirection
* ⚡ Global state management using Context + useReducer
* 🧭 Routing handled by React Router v6

---

## 🧠 Tech Stack

* **React 18**
* **React Router DOM**
* **Context API**
* **useReducer Hook**
* **JSON Server (local backend)**

---


## ⚙️ How It Works

1. When the app loads, the `CitiesProvider` fetches all cities from `http://localhost:8000/cities`.
2. The data is stored in a reducer-managed state (`cities`, `currentCity`, `isLoading`, `error`).
3. Components consume this global state using the `useCities()` hook.
4. Actions like *loading*, *creating*, *deleting*, and *fetching individual cities* are dispatched to the reducer.
5. Routes are handled using React Router:

   * `/` → Homepage
   * `/product` → Product page
   * `/pricing` → Pricing page
   * `/app/cities` → List of all cities
   * `/app/cities/:id` → City details
   * `/app/form` → Add new city
   * `/app/countries` → List of countries

---

## 🛠️ Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/your-username/worldwise.git
cd worldwise
```

### 2. Install dependencies

```bash
npm install
```

### 3. Start the backend (JSON Server)

If you’re using a local server for cities:

```bash
npx json-server --watch data/cities.json --port 8000
```

Make sure your `data/cities.json` file looks like this:

```json
{
  "cities": [
    { "id": 1, "cityName": "Paris", "country": "France" },
    { "id": 2, "cityName": "New York", "country": "USA" }
  ]
}
```

### 4. Run the app

```bash
npm run dev
```

Open the app at **[http://localhost:5173](http://localhost:5173)** (or as shown in your terminal).

---

## 🧩 Key Concepts Demonstrated

* How to use `useReducer` with async operations via dispatch patterns.
* How to structure Context for global data access.
* How to combine React Router nested routes with layout components.
* How to manage loading and error states in a clean, declarative way.

---
