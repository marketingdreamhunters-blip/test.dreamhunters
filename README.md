# Travel Agency CRM

A comprehensive Customer Relationship Management (CRM) system designed specifically for travel agencies. Manage customers, bookings, itineraries, payments, and generate detailed reports.

## 📋 Features

- **Customer Management** - Store and manage customer profiles, preferences, and travel history
- **Booking System** - Create and track flight, hotel, and package bookings
- **Itinerary Management** - Build multi-leg trips with comprehensive travel details
- **Invoice & Payments** - Auto-generate invoices and track payment status
- **Vendor Management** - Manage airlines, hotels, tour operators, and commissions
- **Communications** - Email templates and booking notifications
- **Analytics Dashboard** - Sales reports, revenue tracking, and customer metrics
- **Real-time Updates** - Live booking status and payment notifications

## 🏗️ Project Structure

```
travel-agency-crm/
├── backend/                 # Node.js + Express API
│   ├── src/
│   │   ├── models/         # Database schemas
│   │   ├── routes/         # API endpoints
│   │   ├── controllers/    # Business logic
│   │   ├── middleware/     # Auth, validation
│   │   ├── services/       # Reusable services
│   │   └── config/         # Configuration
│   ├── database/
│   │   └── migrations/     # Database versioning
│   ├── tests/              # Backend tests
│   └── package.json
├── frontend/               # React + Tailwind UI
│   ├── src/
│   │   ├── pages/         # React pages
│   │   ├── components/    # Reusable UI components
│   │   ├── services/      # API integration
│   │   ├── store/         # State management
│   │   └── styles/        # Styling
│   ├── public/
│   └── package.json
├── docs/                   # Documentation
│   ├── DATABASE.md        # Schema docs
│   ├── API.md             # API reference
│   ├── SETUP.md           # Installation guide
│   └── ARCHITECTURE.md    # System architecture
├── docker-compose.yml     # Development environment
└── .gitignore
```

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- PostgreSQL 14+
- npm or yarn

### Backend Setup
```bash
cd backend
npm install
cp .env.example .env
npm run migrate
npm run dev
```

### Frontend Setup
```bash
cd frontend
npm install
cp .env.example .env
npm start
```

## 🗄️ Database

PostgreSQL with the following core entities:
- **Customers** - Customer profiles and preferences
- **Bookings** - Booking records with status tracking
- **Trips/Itineraries** - Trip details and segments
- **Invoices** - Invoice generation and tracking
- **Vendors** - Airlines, hotels, tour operators
- **Payments** - Payment records and status
- **Users** - Admin and staff accounts

## 📚 API Endpoints

### Customers
- `GET /api/customers` - List all customers
- `POST /api/customers` - Create new customer
- `GET /api/customers/:id` - Get customer details
- `PUT /api/customers/:id` - Update customer
- `DELETE /api/customers/:id` - Delete customer

### Bookings
- `GET /api/bookings` - List all bookings
- `POST /api/bookings` - Create new booking
- `GET /api/bookings/:id` - Get booking details
- `PUT /api/bookings/:id` - Update booking status
- `DELETE /api/bookings/:id` - Cancel booking

### Invoices
- `GET /api/invoices` - List invoices
- `POST /api/invoices` - Generate invoice
- `GET /api/invoices/:id` - Get invoice details

### Reports
- `GET /api/reports/sales` - Sales report
- `GET /api/reports/revenue` - Revenue report
- `GET /api/reports/customers` - Customer metrics

## 🔐 Authentication

JWT-based authentication with role-based access control (RBAC):
- Admin - Full system access
- Manager - Manage bookings and customers
- Agent - Create bookings and view reports
- Staff - Limited access

## 📧 Notifications

- Booking confirmations
- Payment reminders
- Invoice notifications
- Itinerary updates

## 📊 Tech Stack

**Backend:**
- Node.js + Express.js
- PostgreSQL
- Sequelize (ORM)
- JWT Authentication
- Nodemailer (Email)

**Frontend:**
- React 18
- Redux Toolkit (State)
- Axios (HTTP Client)
- Tailwind CSS (Styling)
- React Router (Navigation)

**DevOps:**
- Docker & Docker Compose
- GitHub Actions (CI/CD)

## 📖 Documentation

- [Setup Guide](./docs/SETUP.md)
- [Database Schema](./docs/DATABASE.md)
- [API Reference](./docs/API.md)
- [Architecture](./docs/ARCHITECTURE.md)

## 🛠️ Development

```bash
# Run entire stack
docker-compose up

# Run tests
npm run test

# Format code
npm run format

# Lint code
npm run lint
```

## 📝 License

MIT License - See LICENSE file for details

## 👥 Contributing

1. Create a feature branch: `git checkout -b feature/your-feature`
2. Commit changes: `git commit -m 'Add feature'`
3. Push to branch: `git push origin feature/your-feature`
4. Open a Pull Request

## 📞 Support

For issues and questions, please create a GitHub issue in this repository.

---

**Last Updated:** July 15, 2026
**Status:** 🚀 In Development
