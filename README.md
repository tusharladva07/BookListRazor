# 📚 BookListRazor

A simple CRUD application built using **ASP.NET Core Razor Pages** and **Entity Framework Core**.  
This project demonstrates how to manage books (Create, Read, Update, Delete) with SQL Server as the database.

---

## 🚀 Features
- Add new books (Name, Author)
- View all books in a table
- Edit book details
- Delete books
- Entity Framework Core integration
- Razor Pages structure (separation of UI and logic)

---

## 🛠️ Tech Stack
- **ASP.NET Core 6+**
- **Razor Pages**
- **Entity Framework Core**
- **SQL Server**
- **Bootstrap (UI Styling)**

---

## 📂 Project Structure
```
BookListRazor/
│
├── Data/
│   └── ApplicationDbContext.cs   # EF Core DbContext
│
├── Models/
│   └── Book.cs                   # Book entity (table)
│
├── Pages/
│   ├── Books/
│   │   ├── Index.cshtml          # List all books
│   │   ├── Create.cshtml         # Add book
│   │   ├── Edit.cshtml           # Edit book
│   │   └── Delete.cshtml         # Delete book
│   └── Shared/_Layout.cshtml     # Common layout
│
├── wwwroot/                      # Static files (CSS, JS)
├── appsettings.json              # DB connection string
├── Program.cs                    # App configuration
└── BookListRazor.csproj
```

---

## ⚙️ Getting Started

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/BookListRazor.git
cd BookListRazor
```

### 2️⃣ Update Database Connection
Edit **`appsettings.json`** with your SQL Server connection string:
```json
"ConnectionStrings": {
  "DefaultConnection": "Server=YOUR_SERVER_NAME;Database=BookListRazor;Trusted_Connection=True;MultipleActiveResultSets=true"
}
```

### 3️⃣ Run Migrations
Create and apply database migrations:
```bash
dotnet ef migrations add InitialCreate
dotnet ef database update
```

### 4️⃣ Run the Application
```bash
dotnet run
```
Open your browser at:  
👉 `https://localhost:5001` or `http://localhost:5000`

---

## 📖 Razor Pages Flow
1. `OnGet` → Loads data from the database  
2. `OnPost` → Handles form submissions (create, edit, delete)  
3. `DbContext` (`ApplicationDbContext`) → Talks to SQL Server  
4. Data is displayed in `.cshtml` files using Razor syntax  

---

## 🤝 Contributing
Feel free to fork this repo, create a branch, and submit a pull request with improvements.

---

## 📜 License
This project is open-source and available under the [MIT License](LICENSE).
