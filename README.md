# MobileApp Manager — SOA Exam Project
**Student ID: 2400031389**

A full-stack Mobile App CRUD application built with:
- **Frontend:** React 19 + Vite + Axios (deployed on Firebase Hosting)
- **Backend:** Spring Boot 3 + Spring Data JPA + MySQL + Eureka Client + Swagger UI

---

## Project Structure
```
mobileapp/
├── backend/
│   ├── CrudService/      # REST API — port 8084
│   ├── APIGateway/       # API Gateway — port 8083
│   └── EurekaServer/     # Service Discovery — port 8761
└── project frontend/     # React Vite app
```

## Running Locally

### Backend
1. Start MySQL and ensure database `exam_2400031389` exists
2. Start `EurekaServer` → `http://localhost:8761`
3. Start `CrudService` → `http://localhost:8084`
4. Start `APIGateway` → `http://localhost:8083`

### Frontend
```bash
cd "project frontend"
npm install
npm run dev        # http://localhost:3000
```

## API Endpoints
| Method | URL | Description |
|--------|-----|-------------|
| GET | `/DisplayAll` | List all mobile apps |
| POST | `/Add` | Add a new mobile app |
| DELETE | `/Delete/{id}` | Delete an app by ID |

## Firebase Hosting (Frontend)
```bash
npm run build
firebase login
firebase deploy
```
