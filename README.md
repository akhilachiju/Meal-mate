# Meal-mate

Smart meal planning and grocery management application that helps you save time on cooking, manage grocery needs, track monthly expenses, and plan recipes efficiently.

## Project Overview

This application solves common meal planning challenges by providing:
- Daily meal suggestions (breakfast, lunch, dinner)
- Automated grocery list generation based on planned meals
- Price calculation and expense tracking
- Holiday and special event planning
- Recipe management with categories (breakfast, lunch, dinner, snacks, drinks)
- Outside food tracking for budget management

## Tech Stack

- **Frontend**: React 18, TypeScript, Tailwind CSS, Vite
- **Backend**: Node.js, Express, TypeScript
- **Database**: PostgreSQL with Prisma ORM (planned)
- **State Management**: Zustand (planned)
- **Authentication**: JWT (planned)

## Project Structure

```
meal-mate/
├── client/                 # React frontend application
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/          # Route components
│   │   │   ├── Dashboard.tsx
│   │   │   ├── Recipes.tsx
│   │   │   ├── GroceryList.tsx
│   │   │   └── Expenses.tsx
│   │   ├── hooks/          # Custom React hooks
│   │   ├── store/          # State management
│   │   ├── utils/          # Utility functions
│   │   └── types/          # TypeScript type definitions
│   └── package.json
├── server/                 # Node.js backend API
│   ├── src/
│   │   ├── routes/         # API route handlers
│   │   ├── controllers/    # Business logic
│   │   ├── middleware/     # Express middleware
│   │   └── shared/         # Shared types and utilities
│   ├── prisma/             # Database schema and migrations
│   └── package.json
└── docs/                   # Project documentation
```

## Current Status 

### Completed Setup
- [x] Project structure with client/server separation
- [x] React 18 + TypeScript + Tailwind CSS frontend
- [x] Vite build tool with hot reload
- [x] Node.js + Express + TypeScript backend
- [x] API proxy configuration (client → server)
- [x] Basic routing setup with 4 main pages
- [x] CORS and JSON middleware configured
- [x] Environment variables template

### Verified Working
- [x] Frontend development server (port 3000)
- [x] Backend API server (port 5000)
- [x] Frontend-backend communication via proxy
- [x] Tailwind CSS styling system
- [x] TypeScript compilation for both client and server

### Ready for Development
- [ ] Database schema design and Prisma setup
- [ ] Authentication system implementation
- [ ] Recipe management features
- [ ] Meal planning functionality
- [ ] Grocery list generation
- [ ] Expense tracking system
- [ ] Holiday planning features

## Getting Started

### Prerequisites
- Node.js (v18 or higher)
- PostgreSQL database
- npm or yarn package manager

### Installation

1. Install client dependencies:
```bash
cd client && npm install
```

2. Install server dependencies:
```bash
cd server && npm install
```

3. Set up environment variables:
```bash
cp server/.env.example server/.env
# Update database credentials and JWT secret in server/.env
```

4. Start development servers (in separate terminals):
```bash
# Terminal 1 - Frontend
cd client && npm run dev

# Terminal 2 - Backend  
cd server && npm run dev
```

This will start:
- Frontend: http://localhost:3000
- Backend: http://localhost:5000

### Available Scripts

**Client (Frontend):**
- `cd client && npm run dev` - Start frontend development server
- `cd client && npm run build` - Build frontend for production

**Server (Backend):**
- `cd server && npm run dev` - Start backend development server
- `cd server && npm run build` - Build backend for production
- `cd server && npm start` - Start production server

## Development Guidelines

### Code Style
- Use TypeScript for type safety
- Follow React functional components with hooks
- Use Tailwind CSS for styling
- Implement proper error handling
- Write clean, readable code with meaningful variable names

### Git Workflow
- Create feature branches from main
- Use descriptive commit messages
- Test functionality before pushing
- Keep commits focused and atomic

## Next Steps for Contributors

1. **Database Setup**: Implement Prisma schema and migrations
2. **Authentication**: Add user registration/login system
3. **Recipe Management**: Create CRUD operations for recipes
4. **Meal Planning**: Build weekly meal planning interface
5. **Grocery Lists**: Implement automatic grocery list generation
6. **Expense Tracking**: Add expense categorization and reporting

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License.
