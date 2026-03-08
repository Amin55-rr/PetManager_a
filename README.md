# PetManager

PetManager is a pet management web application built with HTML, CSS, and vanilla JavaScript.
It includes authentication, role-based access, an admin dashboard with charts, multilingual UI (FR/EN/AR), and CRUD workflows for core pet-care data.

## Features

- Login system with 2 roles:
  - **Admin**: full access to dashboard and management pages
  - **Client**: personal account page with only their animals, food purchases, vaccinations, and appointments
- Dashboard with dynamic KPIs and charts (Chart.js)
- Management modules:
  - Animals
  - Species
  - Food purchases
  - Vaccinations
  - Appointments
- Search, filters, sorting, and pagination in list pages
- CSV export in list modules and PDF export in selected views
- Multilingual interface via JSON files (`fr`, `en`, `ar`)
- Local data initialization from `data/database.json`

## Tech Stack

- HTML5
- CSS3
- JavaScript (ES6)
- LocalStorage (client-side persistence)
- External CDNs:
  - SweetAlert2
  - Chart.js
  - Font Awesome
  - jsPDF

## Project Structure

```text
PetManager/
├── index.html
├── assets/
│   ├── CSS/
│   ├── JS/
│   └── img/
├── data/
│   └── database.json
├── languages/
│   ├── fr.json
│   ├── en.json
│   └── ar.json
└── pages/
    ├── dashboard.html
    ├── animaux/
    ├── especes/
    ├── nourriture/
    ├── RDV/
    ├── vaccinations/
    └── compte/
```

## Getting Started

### 1) Clone the repository

```bash
git clone https://github.com/Amin55-rr/PetManager.git
cd PetManager
```

### 2) Start a local server
Because the app uses `fetch()` for JSON files, run it through HTTP (not directly with `file://`).

```bash
python -m http.server 8000
```

Or on Windows with Python launcher:

```powershell
py -m http.server 8000
```

### 3) Open in your browser

- http://localhost:8000/

> You can also use the VS Code **Live Server** extension.

## Demo Accounts

### Admin
- Email: `admin@app.com`
- Password: `admin@123`

### Client examples
- `jean@example.com` / `password123`
- `marie@example.com` / `password123`
- `sophie@example.com` / `password123`
- `pierre@example.com` / `password123`

## Data & Session Notes

On first load, data from `data/database.json` is copied to LocalStorage keys such as:

- `db`
- `animaux`
- `comptes`
- `sessionUser`
- `lang`

If you want a clean reset:

1. Open browser dev tools
2. Clear LocalStorage for the site
3. Refresh the app

## Authors

Amine RACHID
Nizar Bitit

