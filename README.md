# 🌐 ZenHub

ZenHub is a comprehensive, scalable, and modular platform designed for cafes, integrating point-of-sale, inventory management, sales forecasting, expense tracking, and user authentication. Built with SvelteKit, Flutter, Node.js microservices, GraphQL, Docker, and AWS Lambda, ZenHub streamlines transactions, orders, and financial insights.

## 🚀 Features

- **POS System:** Manage customer transactions, orders, and payments.
- **Inventory Management:** Track stock, manage supplies, and reduce waste.
- **Sales Forecasting:** Analyze sales trends and forecast future demand.
- **Expense Tracking:** Keep tabs on operational costs and financial health.
- **User Management:** Secure authentication with role-based access control.
- **Notifications & Reporting:** Get real-time updates and detailed reports.

## 🛠️ Tech Stack

- **Frontend:** SvelteKit, Flutter
- **Backend:** Node.js Microservices, GraphQL, AWS Lambda
- **Database:** PostgreSQL
- **Caching:** Redis
- **Orchestration:** Docker, Docker Compose
- **CI/CD:** GitHub Actions

## 📁 Project Structure

```plaintext
zenhub/
├── svelte-ui/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   │   ├── atoms/
│   │   │   ├── molecules/
│   │   │   ├── organisms/
│   │   │   ├── templates/
│   │   │   └── pages/
│   │   ├── pages/
│   │   │   ├── login/
│   │   │   ├── dashboard/
│   │   │   └── inventory/
│   │   ├── layouts/
│   │   ├── styles/
│   │   ├── stores/
│   │   └── utils/
│   ├── static/
│   ├── tests/
│   │   ├── unit/
│   │   └── integration/
│   ├── storybook/
│   │   ├── stories/
│   │   └── config/
│   ├── README.md
│   └── svelte.config.js
├── flutter-pos/
│   ├── lib/
│   │   ├── components/
│   │   ├── pages/
│   │   └── utils/
│   ├── test/
│   ├── README.md
│   └── pubspec.yaml
├── services/
│   ├── pos-service/
│   │   ├── src/
│   │   │   ├── controllers/
│   │   │   ├── models/
│   │   │   ├── routes/
│   │   │   ├── graphql/
│   │   │   └── seeds/
│   │   ├── tests/
│   │   ├── Dockerfile
│   │   ├── README.md
│   │   └── server.js
│   ├── inventory-service/
│   │   ├── src/
│   │   │   ├── controllers/
│   │   │   ├── models/
│   │   │   ├── routes/
│   │   │   ├── graphql/
│   │   │   └── seeds/
│   │   ├── tests/
│   │   ├── Dockerfile
│   │   ├── README.md
│   │   └── server.js
│   ├── user-service/
│   │   ├── src/
│   │   │   ├── controllers/
│   │   │   ├── models/
│   │   │   ├── routes/
│   │   │   ├── graphql/
│   │   │   └── seeds/
│   │   ├── tests/
│   │   ├── Dockerfile
│   │   ├── README.md
│   │   └── server.js
│   ├── notification-service/
│   │   ├── src/
│   │   │   ├── controllers/
│   │   │   ├── models/
│   │   │   ├── routes/
│   │   │   ├── graphql/
│   │   │   └── seeds/
│   │   ├── tests/
│   │   ├── Dockerfile
│   │   ├── README.md
│   │   └── server.js
│   └── reporting-service/
│       ├── src/
│       │   ├── controllers/
│       │   ├── models/
│       │   ├── routes/
│       │   ├── graphql/
│       │   └── seeds/
│       ├── tests/
│       ├── Dockerfile
│       ├── README.md
│       └── server.js
├── libs/
│   ├── common/
│   └── utils/
├── docker/
│   ├── Dockerfile
│   └── docker-compose.yml
├── .github/
│   └── workflows/
│       └── ci-cd.yml
├── .env.example
├── lerna.json
├── package.json
└── README.md
