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
```

## **Setup Instructions**

### **1. Clone the Repository**

```bash
git clone https://github.com/your-username/zenhub.git
cd zenhub
```

## 🛠️ Install Dependencies
Navigate to each service and application directory to install dependencies.


```bash
cd apps/svelte-ui
pnpm install
```

For pos-service, inventory-service, user-service, notification-service, and reporting-service:
```bash
cd services/pos-service
pnpm install

cd ../inventory-service
pnpm install

cd ../user-service
pnpm install

cd ../notification-service
pnpm install

cd ../reporting-service
pnpm install
```

## 🔧 Configure Environment Variables
Create .env files in the root of each service directory and populate them with appropriate configuration settings. Example:
```env
DATABASE_URL=postgres://user:password@localhost:5432/yourdatabase
REDIS_URL=redis://localhost:6379
```

## 📊 Set Up and Seed the Database
Ensure your PostgreSQL database is running. Then, seed the database with mock data.

Database Migration:
```bash
cd services/pos-service
pnpm run migrate
```

Seed the Database:
```bash
cd services/pos-service
pnpm run seed
```

Repeat for other services if needed.



🚀 Run the Project Locally

Start Docker Containers:
```bash
docker-compose up
```

Start Development Servers:
For svelte-ui:

```bash
cd apps/svelte-ui
pnpm run dev
```

For Microservices:
```bash
cd services/pos-service
pnpm run start
```
Repeat for other services as needed.


## 🌐 Access the Application
- Frontend (SvelteKit): Open http://localhost:3000 in your browser.
- Microservices: Ensure the services are accessible on their respective ports as defined in your .env files and docker-compose.yml.

## 🧪 Running Tests
To run unit tests for each service, navigate to the service directory and execute:

```bash
pnpm test
```

## ☸️ Kubernetes Deployment
For deploying with Kubernetes, ensure you have Kubernetes configured locally or use a cloud-based cluster. Deploy the services using:

```bash
kubectl apply -f kubernetes/
```

## Additional Information
For detailed information on each service and component, refer to the specific README.md files located within each service and application directory.

## Troubleshooting
- Ensure all services are running and accessible.
- Verify environment variables are correctly set.
- Check Docker logs for errors and consult service-specific logs.

For further assistance, open an issue on the ZenHub GitHub repository.



