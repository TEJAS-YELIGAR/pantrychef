# 🍳 PantryChef - Recipe Recommendation System Based on Available Ingredients

A full-stack web application that recommends recipes based on ingredients you have at home.

## Tech Stack
- **Frontend**: React.js + Tailwind CSS
- **Backend**: Java Spring Boot
- **Database**: MySQL
- **API**: Spoonacular Recipe API

## Features
- 🔍 Search ingredients and get matching recipes instantly
- ✅ See recipes you can make with what you have
- ❤️ Save favorite recipes
- 👤 User authentication (Register/Login)
- 📋 Detailed recipe instructions
- 🧺 Pantry Essentials quick-add

## Setup Instructions

### Prerequisites
- Java 17+
- Node.js 18+
- MySQL 8+
- Spoonacular API Key (free at spoonacular.com)

### Backend Setup
1. Clone the repository
2. Open `pantrychef-backend` in IntelliJ IDEA
3. Create `src/main/resources/application.properties`:
\`\`\`properties
server.port=8080
spring.datasource.url=jdbc:mysql://localhost:3306/pantrychef?useSSL=false&serverTimezone=UTC&allowPublicKeyRetrieval=true
spring.datasource.username=root
spring.datasource.password=YOUR_MYSQL_PASSWORD
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQLDialect
spoonacular.api.key=YOUR_SPOONACULAR_API_KEY
spoonacular.api.url=https://api.spoonacular.com
spring.application.name=pantrychef-backend
\`\`\`
4. Create MySQL database:
\`\`\`sql
CREATE DATABASE pantrychef;
\`\`\`
5. Run `PantrychefApplication.java`
6. Backend runs on `http://localhost:8080`

### Frontend Setup
1. Open `pantrychef-frontend` in VS Code
2. Run:
\`\`\`bash
npm install
npm start
\`\`\`
3. Frontend runs on `http://localhost:3000`

## API Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/register` | Register user |
| POST | `/api/auth/login` | Login user |
| GET | `/api/spoonacular/recipes/match?ingredients=tomato,pasta` | Match recipes |
| GET | `/api/spoonacular/recipes/{id}` | Recipe detail |
| GET | `/api/pantry/{userId}` | Get user pantry |
| POST | `/api/pantry/{userId}/{ingredientId}` | Add to pantry |
| GET | `/api/saved/{userId}` | Get saved recipes |
| POST | `/api/saved/{userId}/{recipeId}` | Save recipe |

## Team
- Built with ❤️ for Full Stack Development Project