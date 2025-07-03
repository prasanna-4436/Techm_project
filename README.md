 Welcome to Game Haven – your one-stop destination for discovering and buying the best games online!

# E-Commerce Website for Games

This project is built using Angular for the frontend and .NET Core for the backend, featuring secure login/signup functionality, game browsing, a shopping cart, wishlist, and more.

##  Project Structure

```bash
game-store/
├── GameStoreAPI/             # Backend (.NET Core Web API)
│   ├── Controllers/          # API controllers (e.g., GamesController)
│   ├── Models/               # Entity models (Game, Cart, Order)
│   ├── Data/                 # EF Core DbContext
│   ├── Properties/
│   └── Program.cs            # Entry point
│
├── frontend/                 # Frontend (Angular)
│   ├── src/
│   │   ├── app/
│   │   │   ├── home/         # HomeComponent
│   │   │   ├── cart/         # CartComponent
│   │   │   └── services/     # GameService, CartService
│   │   ├── assets/           # Game images and styles
│   │   └── environments/     # environment.ts
│   └── angular.json
│
├── README.md
```

---

## Features

###  Frontend (Angular)

* User-friendly UI built with Angular
* Game listing with image, rating, and price
* Add to cart functionality
* View cart and total amount
* Place order (simulated)

###  Backend (ASP.NET Core Web API)

* RESTful API for games, cart, and orders
* Entity Framework Core for data access
* SQL Server database
* CORS enabled for Angular integration

---

##  Objectives

* Build a real-time responsive game store
* Implement frontend-backend integration
* Demonstrate full-stack CRUD operations
* Showcase modular, scalable architecture

---

##  Tools & Technologies

| Technology         | Description                |
| ------------------ | -------------------------- |
| Angular            | Frontend Framework (v16+)  |
| ASP.NET Core       | Backend Web API (v7 or v8) |
| SQL Server         | Relational database        |
| Entity Framework   | ORM for .NET               |
| Postman            | API testing                |
| Visual Studio Code | Code Editor                |
| Swagger            | API documentation          |

---

##  How It Works

###  User Flow

1. Home page loads game data via API
2. User adds games to cart
3. Cart updates total price
4. Order is placed (POST API)
5. Order stored in database (EF Core)

###  Backend Flow

1. Angular makes HTTP request to `.NET Core API`
2. API controller receives request and uses DbContext
3. Data is fetched/updated in SQL Server
4. Response returned as JSON

---

##  API Endpoints

| Endpoint          | Method | Description    |
| ----------------- | ------ | -------------- |
| `/api/games`      | GET    | Get all games  |
| `/api/games/{id}` | GET    | Get game by ID |
| `/api/games`      | POST   | Add a new game |
| `/api/games/{id}` | PUT    | Update a game  |
| `/api/games/{id}` | DELETE | Delete a game  |

---

##  Setup Instructions

###  Backend Setup

```bash
cd GameStoreAPI
dotnet restore
dotnet ef migrations add InitialCreate
dotnet ef database update
dotnet run
```

* Make sure SQL Server is running
* Update `appsettings.json` with your DB connection string

###  Frontend Setup

```bash
cd frontend
npm install
ng serve
```

* Access at `http://localhost:4200`

---

##  Environment Configuration

Update API URL in:

```ts
// frontend/src/environments/environment.ts
export const environment = {
  production: false,
  apiUrl: 'http://localhost:5055/api'
};
```

---

##  Testing

* Use **Postman** to test API endpoints (`GET`, `POST`, `DELETE`)
* Use Angular DevTools or console logs for UI testing

---

##  Screenshots

> ### login page
![image](https://github.com/user-attachments/assets/41a4f783-22e1-43df-b92c-f5ba469fdbd4)
> ### Home Page
![WhatsApp Image 2025-06-27 at 4 55 13 PM](https://github.com/user-attachments/assets/4700d499-3f29-4c11-90c1-afbbc38330b7)
>### wishlist Page
![WhatsApp Image 2025-06-27 at 4 55 14 PM](https://github.com/user-attachments/assets/d8d51ccf-8bba-4fe7-b9c6-c43e41ca78c8)
> ### cart Page
![WhatsApp Image 2025-06-27 at 4 55 13 PM (1)](https://github.com/user-attachments/assets/ba45a59f-9e0e-4279-b26f-b5e05059b1a5)
> 







---

##  Results & Outcomes

* End-to-end working e-commerce prototype
* Functional frontend-backend integration
* Stored order history and games in SQL DB
* Learned modern web development stacks

---


## Future Enhancements:

Email verification during signup

Password reset through email

Admin dashboard for managing games

User profile management

Payment gateway integration

Thank you for exploring Game Haven!

