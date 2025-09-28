# Movie Rental API (ASP.NET Core + SQL Server)

A RESTful backend for a movie-rental service. It lets clients **register/login users**, **browse/manage movies**, and **rent/return movies**. Data access runs through a small DAL that calls **SQL Server stored procedures**, and passwords are protected with **PBKDF2** hashing.

---

## Features

- **Users**
  - Register with email/password (PBKDF2 hashing + salt)
  - Login (verify password) and fetch basic profile
  - Admin-style list/delete endpoints (optional)

- **Movies**
  - CRUD: create, update, delete, get by id
  - List & search (by title and/or release date range)

- **Rentals**
  - Rent a movie for a user
  - List a user’s current rentals
  - Return (end) a rental

- **Data Layer**
  - SQL Server with **stored procedures** (no ORM required)
  - One DAL (`DBservices`) to execute all procedures
