🏨 Hotel Grande ERP System
A full-stack Hotel Enterprise Resource Planning (ERP) system built for the Business Process & ERP Systems group assignment. It integrates reservations, room management, billing, customer management, housekeeping, maintenance, and employee management into a single role-based platform.

Live Demo: green-meadow-0fb159f00.7.azurestaticapps.net · 
Repository: github.com/Lakshan994/hotelgrande-erp-system

📋 Table of Contents
•	Overview
•	Features
•	Tech Stack
•	Project Structure
•	Prerequisites
•	Getting Started
•	Default Login
•	User Roles
•	API Modules
•	Branching Strategy
•	Contributors

📖 Overview
The Hotel Grande ERP System is a web-based application that automates hotel operations by integrating multiple business functions into one system — reducing manual work and giving management real-time visibility into rooms, reservations, guests, billing, and staff.

✨ Features
•	🔐 Secure JWT-based authentication with role-based access control
•	📊 Role-specific dashboards (Admin, Manager, Receptionist, Housekeeper)
•	🛏️ Room management with real-time status tracking
•	📅 Reservation and booking management (check-in / check-out)
•	👤 Customer profile and history management
•	💳 Billing, invoicing, and payment tracking
•	🧹 Housekeeping task assignment and cleaning history
•	🔧 Maintenance request tracking
•	👥 Employee management with roster and permissions
•	🌗 Dark / light theme toggle
•	☁️ Deployed on Microsoft Azure

🛠 Tech Stack
Layer	Technology
Frontend	React 18, Vite, Tailwind CSS, React Router, Recharts, Lucide Icons
Backend	Spring Boot 3.3 (Java 21), Spring Security, Spring Data JPA
Database	MySQL
Auth	JWT (jjwt)
Deployment	Microsoft Azure (Static Web Apps / App Service)
Version Control	Git & GitHub
📁 Project Structure
Code
hotelgrande-erp-system/
├── backend/                  # Spring Boot REST API
│   └── src/main/java/com/hotelgrande/erp/
│       ├── config/           # Security, CORS, JWT, data seeding
│       ├── controller/       # REST controllers (Auth, Room, Reservation, Billing, etc.)
│       ├── dto/              # Request/response DTOs
│       ├── entity/           # JPA entities
│       ├── enums/            # Role and status enums
│       ├── repository/       # Spring Data repositories
│       └── service/          # Business logic (JWT, User)
├── frontend/                 # React application
│   └── src/
│       ├── components/       # Atoms / molecules / organisms / templates
│       ├── context/          # Theme context (dark/light mode)
│       ├── data/             # Mock/reference data
│       ├── pages/            # Feature pages (reservations, rooms, billing, employees, etc.)
│       └── utils/            # API client, permissions helpers
└── README.md
✅ Prerequisites
•	Java 21 (Temurin/OpenJDK)
•	Maven 3.9+
•	Node.js 18+ and npm
•	MySQL (running on port 3306)
•	Git
🚀 Getting Started
1.	Clone the repository
bash
git clone https://github.com/Lakshan994/hotelgrande-erp-system.git
cd hotelgrande-erp-system

2.	Start MySQL Default connection: root user, no password. Update application.properties if needed.

3.	Run the backend
bash
cd backend
mvn clean install
mvn spring-boot:run
API starts at http://localhost:8080.

4.	Run the frontend
bash
cd frontend
npm install
npm run dev
App opens at http://localhost:5173.

🔑 Default Login
Field	Value
Email	admin@hotelgrande.com
Password	admin123
⚠️ Change these credentials before production deployment.

👥 User Roles
Role	Access
Admin	Full system access, employee management, system settings
Manager	Reservations, billing, reports, staff oversight
Receptionist	Check-in/out, reservations, customer management, billing
Housekeeper	Housekeeping tasks and cleaning history

🔌 API Modules
Controller	Responsibility
AuthController	Login and authentication
RoomController	Room CRUD and status
ReservationController	Bookings, check-in/out
CustomerController	Guest profiles
BillingController	Invoices and payments
HousekeepingController	Cleaning task management
MaintenanceController	Maintenance requests
EmployeeController	Staff records and system accounts

🌿 Branching Strategy
•	main — stable, deployment-ready code
•	dev — integration branch; all features merge here first
•	feature/* — one branch per module/feature

🔀 Feature Branches
Branch	Module	Scope
feature/01-auth-core-infra	Auth & Security	Config, JWT, permissions
feature/02-customer-management	Customers	Guest profiles & database
feature/03-room-management	Rooms	Room grid, inventory
feature/04-reservations-bookings	Reservations	Booking, check-in/out
feature/05-billing-invoices	Billing	Invoices, payments
feature/06-housekeeping	Housekeeping	Task allocation & logs
feature/07-maintenance	Maintenance	Facility requests
feature/08-employee-management	Employees	Staff records & shifts
feature/09-dashboards-layout	Dashboards	Layouts, sidebar, topbar
feature/10-ui-kit-shared	UI Kit	Shared components & styles

👨‍👩‍👧‍👦 Contributors
Member	Module
Lakshan (Lead github)	Repository management, GitHub workflow, review & merge
Member 1(SMKMB Senanayake)    Authentication & Core Infra
Member 2(S.D.L.Weerasinghe)	  Customer Management
Member 3(M.D.A.H Mudalige)	  Room Management
Member 4(K I S Samaraweera)	  Reservations
Member 5(G W T Samararathna)  Billing
Member 6(A.M.S.Sharanga )	  Housekeeping
Member 7(B.M.A.M.Basnayake)   Maintenance
Member 8(G.Y.Lakshan Aroshana)Employee Management
Member 9(G.s.Vithanage )	 Dashboards
Member 10(J K N S Jayakody)	UI Kit & Shared Components

Built for the Business Process & ERP Systems module — Group 11.

