# 🔍 visa-scope-ui

> **Frontend for VisaScope — H1B Petition Tracker**  
> Search, explore, and analyze H1B petition data across U.S. employers.

![Angular](https://img.shields.io/badge/Angular-8-DD0031?style=for-the-badge&logo=angular&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3.x-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Angular Material](https://img.shields.io/badge/Angular%20Material-8-757575?style=for-the-badge&logo=angular&logoColor=white)
![Hosted on S3](https://img.shields.io/badge/Hosted%20on-AWS%20S3-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)

---

## 🌐 Live Demo

> 🔗 [Coming Soon — hosted on AWS S3]

---

## 📸 Screenshots

> _(Add screenshots here once the UI is built)_

---

## ✨ Features

- 🔎 **Company Search** — Search any U.S. employer by name instantly
- 📊 **Data Table** — Sortable, paginated H1B petition records from USCIS
- ✅ **2-Year Filing Check** — Instantly see if a company filed new H1Bs or H1B transfers in the last 2 fiscal years
- 📁 **Fiscal Year Filtering** — Filter results by year
- 📱 **Responsive Design** — Works on desktop and mobile

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Framework | Angular 8 |
| Language | TypeScript |
| UI Components | Angular Material 8 |
| HTTP Client | Angular HttpClient |
| Styling | CSS + Angular Material Theming |
| Build Tool | Angular CLI |
| Hosting | AWS S3 (Static Website) |

---

## 🗂️ Project Structure

```
visa-scope-ui/
├── src/
│   └── app/
│       ├── components/
│       │   ├── search/          # Search bar component
│       │   └── data-table/      # H1B data table component
│       ├── services/
│       │   └── h1b.service.ts   # API calls to visa-scope-api
│       ├── app.module.ts
│       └── app.component.ts
├── angular.json
├── package.json
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

- Node.js v10+ → [Download](https://nodejs.org)
- Angular CLI 8 → `npm install -g @angular/cli@8`

### Installation

```bash
# Clone the repo
git clone https://github.com/hvemuri9/visa-scope-ui.git
cd visa-scope-ui

# Install dependencies
npm install

# Start development server
ng serve

# Open in browser
http://localhost:4200
```

### Environment Setup

Update the API base URL in `src/app/services/h1b.service.ts`:

```typescript
private baseUrl = 'http://localhost:8080/api/h1b'; // local dev
// Change to your EC2 IP for production
```

---

## 🏗️ Build for Production

```bash
ng build --prod
# Output goes to: dist/visa-scope-ui/
# Upload contents of dist/ to your AWS S3 bucket
```

---

## 🔗 Backend Repo

This app connects to **[visa-scope-api](https://github.com/hvemuri9/visa-scope-api)** — the Spring Boot backend that serves H1B data from USCIS.

---

## 📡 API Endpoints Used

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/h1b/search?company=Google` | Search by company name |
| GET | `/api/h1b/check-recent?company=Google` | Check last 2 years filings |
| GET | `/api/h1b/all?page=0&size=20` | Paginated full dataset |

---

## 🛣️ Roadmap

- [ ] Company search with autocomplete
- [ ] Bar chart showing H1B trends by year
- [ ] Export results to CSV
- [ ] State-level map view
- [ ] Dark mode toggle

---

## 👨‍💻 Author

**hvemuri9**  
GitHub: [@hvemuri9](https://github.com/hvemuri9)

---

## 📄 License

MIT License — free to use and modify.
