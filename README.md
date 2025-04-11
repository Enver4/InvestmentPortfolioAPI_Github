# Investment Portfolio API (.NET 8)

This is a backend Web API project built using .NET 8, Entity Framework Core, MS SQL Server, and MongoDB.  
It allows users to manage and evaluate their currency-based investment portfolios, perform file uploads, and fetch real exchange rates from the internet (almost).

# Architecture & Approach

- .NET 8 Web API with RESTful endpoints using Controllers
- Entity Framework Core 8 with MS SQL Server for relational data
- MongoDB for logging transactions, system activity, and file uploads
- JWT-based authentication with Admin and User roles
- Layered structure: Controllers, Services, Data, Models
- Swagger for API testing and documentation
- Real exchange rates fetched via a public API and stored daily (Trying to fix this)

# Authentication & Roles

- JWT tokens are issued after login (no signup)
- Admin Users can:
  - View and manage all portfolios
  - Update asset types
  - Manually or automatically update exchange rates
- Regular Users can:
  - Manage their own assets and portfolios
  - Perform currency conversions
- Swagger allows token-based authorization

# Features Implemented

- User login (JWT-based)
- Asset tracking (Cash, Crypto, Stocks, Gold)
- Currency conversion (USD, EUR, TRY, GBP)
- Portfolio evaluation (in selected currency)
- CSV upload with per-line validation
- Profit/Loss calculation
- MongoDB logging (transactions, errors, uploads)
- Exchange rate fetch from (https://exchangerate.host) (There are still a bug. It calls but can't write to db)
- Role-based permissions and admin operations

# External API Usage

Used (https://exchangerate.host/latest) to fetch real exchange rates. (Trying to fix this)


