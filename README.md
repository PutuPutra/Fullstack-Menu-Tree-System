# Fullstack Menu Tree System

## Setup Instructions

1. Clone the repo.
2. Copy .env.example to .env and fill values.

## Development Mode

- Backend: cd backend && npm install && npm run start:dev
- Frontend: cd frontend && npm install && npm run dev
- Access frontend at http://localhost:3001

## Production Mode

- Build: cd backend && npm build; cd frontend && npm build
- Run: node dist/main (backend), npm start (frontend)

## Docker (Bonus)

- docker-compose up
- Access frontend at http://localhost:3001, backend API at http://localhost:3000

## API Documentation

- GET /api/menus: Get tree
- GET /api/menus/:id: Get one
- POST /api/menus: Create {name, systemCode, parentData, parentId}
- PUT /api/menus/:id: Update
- DELETE /api/menus/:id: Delete
- PATCH /api/menus/:id/move: {newParentId}
- PATCH /api/menus/:id/reorder: {newOrder}

## Technology Choices

- Backend: NestJS 11 for structured API, TypeORM 0.3.27 for ORM with tree support.
- Frontend: Next.js 16 for SSR, Tailwind 4.1 for styling, Zustand 5.0 for state, react-dnd for drag-drop.
- Docker for containerization.
- Architecture: MVC in backend, component-based in frontend with recursive tree.

## Running Tests

- Backend: cd backend && npm test
