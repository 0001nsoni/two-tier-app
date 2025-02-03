# Two-Tier Application using Docker Compose

This project sets up a **two-tier architecture** using **MySQL** as the database and a **Flask** application as the backend. The services are managed using **Docker Compose**.

## **Project Structure**
```
.
├── Dockerfile
├── docker-compose.yml
├── app/
│   ├── main.py
│   ├── requirements.txt
├── .gitignore
└── README.md
```

## **Technologies Used**
- **Docker & Docker Compose**
- **MySQL** (Database)
- **Flask** (Python Backend)

## **Setup Instructions**

### **1. Clone the Repository**
```bash
git clone https://github.com/your-username/two-tier-app.git
cd two-tier-app
```

### **2. Build & Run Containers**
```bash
docker-compose up --build -d
```
This will start both **MySQL** and **Flask** containers.

### **3. Verify Running Containers**
```bash
docker ps
```

### **4. Test the Application**
Check if the backend is running:
```bash
curl http://localhost:5000/health
```
If everything is correct, it should return a **200 OK** response.

## **Environment Variables**
The following environment variables are used:

| Variable        | Value       |
|----------------|------------|
| MYSQL_HOST     | mysql      |
| MYSQL_USER     | root       |
| MYSQL_PASSWORD | root       |
| MYSQL_DB       | devops     |

## **Stopping the Application**
To stop the application and remove containers:
```bash
docker-compose down
```

## **Database Persistence**
The MySQL data is stored in a **Docker volume** named `mysql-data`, ensuring persistence across container restarts.

## **Contributing**
Feel free to fork this repository, open issues, or submit pull requests!

## **License**
This project is licensed under the MIT License.

