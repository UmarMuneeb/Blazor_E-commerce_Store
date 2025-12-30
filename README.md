# Visual Programming E-commerce Project

A robust **Blazor Server** e-commerce application built with a modern 3-layer architecture and SQL Server integration. This project demonstrates a clean separation of concerns between the user interface, business logic, and data access layers.

## 🚀 Key Features

-   **Product Catalog**: Browse a wide range of products with detailed views.
-   **Category Management**: Filter and explore products based on specific categories.
-   **Shopping Cart**: A fully functional cart system allowing users to:
    -   Add items to the cart.
    -   Update item quantities.
    -   Remove items from the cart.
-   **SQL Persistence**: All cart operations are persisted in a SQL Server database using stored procedures.
-   **Modern UI**: Responsive design built with Blazor Server components.

## 🛠️ Technology Stack

-   **Frontend**: Blazor Server (ASP.NET Core)
-   **Language**: C#
-   **Database**: Microsoft SQL Server
-   **Architecture**: 3-Layer Architecture (Web, Data Access, Model Library)
-   **Data Access**: ADO.NET with `System.Data.SqlClient`

## 📁 Project Structure

The solution consists of three main projects:

1.  **Vp_project**: The core Blazor Server application containing:
    -   `Pages/`: UI components (Index, ProductDetails, CartItems).
    -   `Services/`: Business logic for Products and Categories.
    -   `Shared/`: Reusable UI components and layouts.
2.  **DataAccessLayer**: Handles all database interactions.
    -   `DBcontext.cs`: Implements CRUD operations for the shopping cart.
    -   `DBhelper.cs`: Manages database connections.
3.  **ModelClassLibrary**: Defines the domain models used across the application.
    -   `Product.cs`, `Category.cs`, `Cart.cs`.

## ⚙️ Database Setup

To set up the database, execute the `SQLQuery1.sql` script located in the project root. This script will:
1.  Create the `Ecommerce` database.
2.  Create the `Cart` table.
3.  Initialize essential stored procedures:
    -   `AddItem`: Adds or merges items in the cart.
    -   `DeleteItem`: Removes an item by ID.
    -   `GetProducts`: Retrieves all cart items.

## 🚀 Getting Started

1.  **Restore Dependencies**:
    ```bash
    dotnet restore
    ```
2.  **Configuration**: Update the connection string in `DataAccessLayer/DBhelper.cs` to match your local SQL Server instance.
3.  **Run Application**:
    ```bash
    dotnet run --project Vp_project/Vp_project.csproj
    ```

---
*Developed as part of the Visual Programming course project.*
