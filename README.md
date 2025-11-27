# 🏛️ JustiFlow - AI-Powered Differentiated Case Management System

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Python-3.11-blue)](https://www.python.org/)
[![React](https://img.shields.io/badge/React-18.3-61DAFB)](https://reactjs.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-Latest-009688)](https://fastapi.tiangolo.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-3178C6)](https://www.typescriptlang.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-47A248)](https://www.mongodb.com/)

> **A Next-Generation Legal Case Management System with Bharatiya Nyaya Sanhita (BNS) Integration**  
> Designed for Indian Courts to streamline judicial operations, reduce case backlog, and optimize resource allocation through AI and automation.

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Screenshots](#-screenshots)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [System Architecture](#-system-architecture)
- [Getting Started](#-getting-started)
- [User Roles & Permissions](#-user-roles--permissions)
- [API Documentation](#-api-documentation)
- [Troubleshooting](#-troubleshooting)
- [Deployment](#-deployment)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🌟 Overview

**JustiFlow** is a comprehensive Differentiated Case Management (DCM) platform built to revolutionize court operations in India. It combines cutting-edge AI technology with intuitive design to automate case classification, optimize judicial resource allocation, and significantly reduce case processing time.

### Why JustiFlow?

- **🎯 Problem**: Indian courts face a massive backlog of over 4 crore pending cases
- **💡 Solution**: AI-powered automation and intelligent scheduling to expedite case resolution
- **📈 Impact**: Reduce case processing time by 40%, optimize judge allocation, improve access to justice

### What Makes It Different?

- **BNS Integration**: First system to integrate Bharatiya Nyaya Sanhita (BNS) 2023
- **AI-Powered**: Machine learning models for case classification and prediction
- **Cloud-Native**: Scalable architecture using MongoDB Atlas
- **Role-Based Access**: Secure multi-user system with granular permissions
- **Real-Time Analytics**: Live dashboards and predictive insights

---

## 🖼️ Screenshots

### Dashboard Overview
![Dashboard](./screenshots/dashboard.png)
*Real-time analytics showing case statistics, pending hearings, and system performance metrics*

### Case Management Interface
![Case Management](./screenshots/cases.png)
*Comprehensive case listing with advanced filters, search, and bulk actions*

### Smart Scheduling System
![Smart Scheduling](./screenshots/schedule.png)
*AI-powered priority-based hearing allocation with conflict detection*

### User Management (Admin)
![User Management](./screenshots/users.png)
*Role-based user administration with permissions control*

### Document Upload & Management
![Documents](./screenshots/documents.png)
*Secure document storage with categorization and search functionality*

### Analytics Dashboard
![Analytics](./screenshots/analytics.png)
*Advanced analytics with trend visualization and predictive insights*

### Login Page
![Login](./screenshots/login.png)
*Secure authentication with JWT token-based system*

### Case Details View
![Case Details](./screenshots/case-details.png)
*Detailed case information with timeline, documents, and hearing history*

---

## ✨ Key Features

### 🤖 AI & Machine Learning

- **Automatic Case Classification**: Identifies case type (Civil, Criminal, Family, etc.) with 85%+ accuracy
- **BNS Section Recommendation**: Suggests relevant legal sections based on case description
- **Similar Case Finder**: Semantic search to find precedents and related cases
- **Document Analysis**: NLP-powered entity extraction and sentiment analysis
- **Predictive Analytics**: Forecasts case outcomes and resolution timelines

### 📊 Smart Case Management

- **Priority-Based Scheduling**: Greedy algorithm for optimal hearing allocation
- **Multi-Bench Optimization**: Distributes cases across judges based on expertise and availability
- **Conflict Detection**: Automatic identification of scheduling conflicts
- **Deadline Tracking**: Automated reminders and escalation for overdue tasks
- **Document Management**: Secure cloud storage for all case-related documents

### 🔐 Security & Compliance

- **JWT Authentication**: Secure token-based authentication with refresh tokens
- **Role-Based Access Control (RBAC)**: Four-tier permission system (Admin, Judge, Clerk, Lawyer)
- **Audit Trail**: Complete logging of all system activities
- **Data Encryption**: At-rest and in-transit encryption for sensitive data
- **GDPR Compliant**: Privacy-first architecture

### 📈 Analytics & Reporting

- **Real-Time Dashboards**: Live metrics on case status, judge workload, and system performance
- **Custom Reports**: Generate PDF/Excel reports with custom filters
- **Trend Analysis**: Historical data visualization for decision-making
- **Performance Metrics**: Track case resolution rates, hearing completion, and more

### 🎨 User Experience

- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile
- **Intuitive Interface**: Clean, modern UI with minimal learning curve
- **Dark Mode**: Eye-friendly interface for extended usage
- **Accessibility**: WCAG 2.1 AA compliant

---

## 🛠️ Tech Stack

### Backend (API Server)

| Technology | Version | Purpose |
|------------|---------|---------|
| **Python** | 3.11+ | Core programming language |
| **FastAPI** | Latest | High-performance async web framework |
| **MongoDB** | Atlas | Cloud NoSQL database |
| **Beanie ODM** | Latest | Async MongoDB object-document mapper |
| **Pydantic** | 2.x | Data validation and settings |
| **JWT (jose)** | Latest | Token-based authentication |
| **Passlib** | Latest | Password hashing (bcrypt) |
| **Uvicorn** | Latest | ASGI server |
| **Python-Dotenv** | Latest | Environment variable management |

### Frontend (User Interface)

| Technology | Version | Purpose |
|------------|---------|---------|
| **React** | 18.3.1 | UI library |
| **TypeScript** | 5.0+ | Type-safe JavaScript |
| **Vite** | 5.3+ | Build tool and dev server |
| **React Router** | 6.26+ | Client-side routing |
| **Tailwind CSS** | 3.4+ | Utility-first CSS framework |
| **Lucide React** | Latest | Icon library |
| **React Hook Form** | 7.52+ | Form management |
| **Zod** | 3.23+ | Schema validation |
| **Axios** | 1.7+ | HTTP client |
| **React Hot Toast** | 2.4+ | Notifications |
| **Recharts** | 2.12+ | Data visualization |

### AI/ML Components

| Technology | Purpose |
|------------|---------|
| **Scikit-learn** | Machine learning algorithms |
| **NLTK** | Natural language processing |
| **TF-IDF Vectorizer** | Text feature extraction |
| **SVM Classifier** | Case classification model |

### DevOps & Tools

| Tool | Purpose |
|------|---------|
| **Git** | Version control |
| **GitHub** | Code repository |
| **PowerShell** | Windows scripting |
| **VS Code** | Development IDE |
| **Postman** | API testing |

---

## 🏗️ System Architecture

### High-Level Architecture

```
┌─────────────────────────────────────────────────────────┐
│                     Client Layer                         │
│  (React + TypeScript + Tailwind CSS)                    │
│  Port: 3000                                              │
└─────────────────┬───────────────────────────────────────┘
                  │ HTTP/HTTPS
                  │ REST API Calls
                  ▼
┌─────────────────────────────────────────────────────────┐
│                   API Gateway Layer                      │
│  (FastAPI + Uvicorn)                                    │
│  Port: 8001                                              │
│  ├── Authentication (JWT)                               │
│  ├── Authorization (RBAC)                               │
│  ├── Request Validation                                 │
│  └── Rate Limiting                                      │
└─────────────────┬───────────────────────────────────────┘
                  │
        ┌─────────┴──────────┬────────────┐
        ▼                    ▼            ▼
┌──────────────┐   ┌─────────────┐   ┌──────────┐
│ Business     │   │  AI/ML      │   │  Auth    │
│ Logic        │   │  Services   │   │  Service │
│ Layer        │   │             │   │          │
│              │   │ - Classify  │   │ - Login  │
│ - Cases      │   │ - Predict   │   │ - Token  │
│ - Hearings   │   │ - Analyze   │   │ - RBAC   │
│ - Users      │   │ - Search    │   │          │
│ - Documents  │   │             │   │          │
└──────┬───────┘   └─────────────┘   └──────────┘
       │
       ▼
┌─────────────────────────────────────────────────────────┐
│              Data Persistence Layer                      │
│  MongoDB Atlas (Cloud NoSQL Database)                   │
│  Collections:                                            │
│  ├── users          (User accounts & profiles)          │
│  ├── cases          (Case records & metadata)           │
│  ├── hearings       (Hearing schedules)                 │
│  ├── documents      (File metadata & content)           │
│  └── audit_logs     (System activity logs)              │
└─────────────────────────────────────────────────────────┘
```

### Data Flow

1. **User Request**: Client sends HTTP request to backend API
2. **Authentication**: JWT token validated, user identity verified
3. **Authorization**: RBAC checks user permissions for requested action
4. **Business Logic**: Request processed by appropriate service layer
5. **Data Access**: MongoDB queried/updated via Beanie ODM
6. **Response**: JSON response returned to client
7. **UI Update**: React state updated, UI re-rendered

### Database Schema

**Collections:**

- **users**: User authentication and profile information
- **cases**: Case details, status, timeline, assignments
- **hearings**: Hearing schedules, bench assignments, outcomes
- **documents**: Document metadata and base64-encoded content
- **audit_logs**: System activity tracking

---

## 🚀 Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:

- **Python 3.11+** ([Download](https://www.python.org/downloads/))
- **Node.js 16+** ([Download](https://nodejs.org/))
- **MongoDB** (Local) OR **MongoDB Atlas** (Cloud) account
- **Git** ([Download](https://git-scm.com/))
- **Visual Studio Code** (Recommended)

### Installation

#### 1. Clone the Repository

```bash
git clone https://github.com/vigneshkriishna/Yukthi-Differentiated_caseflow_management-.git
cd Yukthi-Differentiated_caseflow_management-/caseflow_management_application
```

#### 2. Backend Setup

```powershell
# Navigate to backend directory
cd backend

# Install Python dependencies
pip install -r requirements.txt

# Configure environment variables
# Edit .env.mongodb with your MongoDB credentials
```

**MongoDB Atlas Setup:**

1. Go to [MongoDB Atlas](https://cloud.mongodb.com/)
2. Create a free cluster
3. Create a database user (e.g., `vigneshpop`)
4. **Network Access**: Whitelist your IP address
   - Go to Network Access → Add IP Address
   - Add your current IP or use `0.0.0.0/0` for testing (not recommended for production)
5. Get your connection string:
   - Go to Database → Connect → Connect your application
   - Copy the connection string
6. Update `.env.mongodb`:

```env
MONGODB_URL=mongodb+srv://vigneshpop:Lyrr0HuIyZMczzxu@cluster0.w7x5vdv.mongodb.net/
MONGODB_DATABASE=dcm_system
MONGODB_USERNAME=vigneshpop
MONGODB_PASSWORD=Lyrr0HuIyZMczzxu
JWT_SECRET_KEY=your-super-secret-key-change-this
JWT_ALGORITHM=HS256
JWT_EXPIRATION_HOURS=24
PORT=8001
HOST=0.0.0.0
```

#### 3. Frontend Setup

```powershell
# Navigate to frontend directory
cd ../frontend

# Install Node dependencies
npm install

# No additional configuration needed - automatically connects to localhost:8001
```

### Running the Application

#### Start Backend Server (PowerShell Window 1)

```powershell
# From backend directory
cd backend
python main_mongodb.py
```

**Expected Output:**
```
✅ Connected to MongoDB Atlas!
📊 Database: dcm_system
🌐 Server will be available at: http://localhost:8001
📚 API Documentation: http://localhost:8001/docs
```

⚠️ **Important**: Keep this PowerShell window open while using the application.

#### Start Frontend Server (PowerShell Window 2)

```powershell
# From frontend directory (new PowerShell window)
cd frontend
npm run dev
```

**Expected Output:**
```
VITE v5.4.19  ready in 224 ms
➜  Local:   http://localhost:3000/
➜  Network: http://192.168.x.x:3000/
```

⚠️ **Important**: Keep this PowerShell window open as well.

### Access the Application

- **Frontend**: http://localhost:3000
- **Backend API**: http://localhost:8001
- **API Documentation**: http://localhost:8001/docs

### Default Login Credentials

| Role | Username | Password | Access Level |
|------|----------|----------|--------------|
| Administrator | `admin` | `admin123` | Full system access |
| Judge | `judge1` | `demo123` | Case management, hearings |
| Clerk | `clerk1` | `demo123` | Data entry, scheduling |
| Lawyer | `lawyer1` | `demo123` | Case viewing, documents |

⚠️ **Security Note**: Change default passwords in production!

---

## 👥 User Roles & Permissions

### Administrator (`admin`)

**Full System Access**

- ✅ Create, edit, delete users
- ✅ Manage all cases and hearings
- ✅ Access all reports and analytics
- ✅ Configure system settings
- ✅ View audit logs
- ✅ Upload/delete any documents

### Judge (`judge`)

**Case Adjudication**

- ✅ View assigned cases
- ✅ Conduct hearings
- ✅ Update case status
- ✅ Upload orders and judgments
- ✅ View analytics dashboard
- ❌ Cannot manage users
- ❌ Cannot delete cases

### Clerk (`clerk`)

**Data Entry & Scheduling**

- ✅ Create new cases
- ✅ Schedule hearings
- ✅ Upload documents
- ✅ Update case details
- ✅ Generate reports
- ❌ Cannot delete cases
- ❌ Cannot manage users

### Lawyer (`lawyer`)

**Case Representation**

- ✅ View assigned cases
- ✅ Upload documents (petitions, evidence)
- ✅ View hearing schedules
- ✅ Download case documents
- ❌ Cannot edit case details
- ❌ Cannot schedule hearings
- ❌ Cannot access other lawyers' cases

---

## 📚 API Documentation

### Base URL

```
http://localhost:8001
```

### Authentication

All protected endpoints require JWT Bearer token:

```http
Authorization: Bearer <your_jwt_token>
```

### Key Endpoints

#### Authentication

```http
POST /auth/login           # Login and get JWT token
POST /auth/refresh         # Refresh expired token
GET  /auth/me              # Get current user info
```

#### Cases

```http
GET    /api/cases              # List all cases
POST   /api/cases              # Create new case
GET    /api/cases/{id}         # Get case details
PUT    /api/cases/{id}         # Update case
DELETE /api/cases/{id}         # Delete case
GET    /api/cases/search?q=... # Search cases
```

#### Hearings

```http
GET    /api/hearings           # List hearings
POST   /api/hearings           # Schedule hearing
GET    /api/hearings/{id}      # Get hearing details
PUT    /api/hearings/{id}      # Update hearing
GET    /api/hearings/upcoming  # Upcoming hearings
```

#### Users (Admin Only)

```http
GET    /api/users              # List all users
POST   /api/users              # Create user
GET    /api/users/{id}         # Get user details
PUT    /api/users/{id}         # Update user
DELETE /api/users/{id}         # Delete user
```

#### Documents

```http
GET    /api/documents          # List documents
POST   /api/documents/upload   # Upload document
GET    /api/documents/{id}     # Download document
DELETE /api/documents/{id}     # Delete document
```

#### Analytics

```http
GET    /api/analytics/dashboard    # Dashboard metrics
GET    /api/analytics/cases-trend  # Case trend analysis
GET    /api/analytics/judge-load   # Judge workload
```

#### NLP/AI

```http
POST   /api/nlp/classify       # Classify case text
POST   /api/nlp/similar        # Find similar cases
POST   /api/nlp/extract        # Extract entities
POST   /api/nlp/analyze        # Sentiment analysis
```

### Interactive API Docs

Visit **http://localhost:8001/docs** for interactive Swagger UI documentation with:
- All endpoints listed
- Request/response schemas
- Try-it-out functionality
- Authentication support

---

## 🔧 Troubleshooting

### Common Issues

#### 1. MongoDB Connection Failed

**Error**: `ServerSelectionTimeoutError` or DNS timeout

**Solutions**:
```powershell
# Option 1: Configure DNS to Google DNS
# Go to Network Settings → Change Adapter Options → Properties → Internet Protocol Version 4
# Set Preferred DNS to 8.8.8.8

# Option 2: Whitelist your IP in MongoDB Atlas
# Go to Network Access → Add IP Address → Add Current IP Address

# Option 3: Check internet connectivity
ping google.com
```

#### 2. Frontend Can't Connect to Backend

**Error**: `ERR_CONNECTION_REFUSED` or 404 errors

**Solutions**:
```powershell
# 1. Verify backend is running on port 8001
# Check the backend PowerShell window for: "Server will be available at: http://localhost:8001"

# 2. Check frontend configuration
# Open: frontend/src/services/config.ts
# Verify: BASE_URL: 'http://localhost:8001'

# 3. Clear browser cache and reload
# Press Ctrl+Shift+R in browser
```

#### 3. Login Not Working

**Error**: "Invalid credentials" or token errors

**Solutions**:
```powershell
# 1. Verify correct credentials:
# Username: admin (not admin@dcm.gov.in)
# Password: admin123

# 2. Check backend logs for authentication errors

# 3. Clear browser localStorage
# Open DevTools (F12) → Application → Local Storage → Clear All
```

#### 4. Users List Empty

**Error**: Empty list or "No users found"

**Solutions**:
```powershell
# 1. Verify you're logged in as admin
# Only admins can view users list

# 2. Check MongoDB connection
# Verify data exists in MongoDB Atlas console

# 3. Check browser console for errors
# Press F12 → Console tab
```

#### 5. Port Already in Use

**Error**: `Address already in use` or `EADDRINUSE`

**Solutions**:
```powershell
# Find process using the port
netstat -ano | findstr :8001

# Kill the process (replace <PID> with actual process ID)
taskkill /PID <PID> /F

# Or change port in backend/config.py:
# PORT = 8002
```

### Debug Checklist

- [ ] Both PowerShell windows are open and running
- [ ] Backend shows "Connected to MongoDB Atlas!"
- [ ] Frontend shows "Local: http://localhost:3000/"
- [ ] No error messages in either console
- [ ] Internet connection is stable
- [ ] IP address is whitelisted in MongoDB Atlas
- [ ] Using correct credentials (admin/admin123)
- [ ] Browser cache cleared if needed

---

## 🚢 Deployment

### Production Checklist

- [ ] Change all default passwords
- [ ] Set strong `JWT_SECRET_KEY` in `.env.mongodb`
- [ ] Update `CORS_ORIGINS` to your production domain
- [ ] Enable HTTPS/SSL
- [ ] Configure MongoDB Atlas IP whitelist (remove 0.0.0.0/0)
- [ ] Set up database backups in Atlas
- [ ] Configure monitoring (MongoDB Atlas monitoring, application logs)
- [ ] Enable rate limiting in FastAPI
- [ ] Set `DEBUG=false` in production
- [ ] Use environment-specific configuration files
- [ ] Set up logging aggregation (e.g., ELK Stack)
- [ ] Implement API versioning
- [ ] Add health check endpoints

### Environment Variables (Production)

**Backend (.env.mongodb):**

```env
# MongoDB Atlas Production
MONGODB_URL=mongodb+srv://prod_user:secure_password@cluster0.xxxxx.mongodb.net/
MONGODB_DATABASE=dcm_production
MONGODB_USERNAME=prod_user
MONGODB_PASSWORD=secure_password

# Security
JWT_SECRET_KEY=use-a-strong-randomly-generated-secret-key-here-min-32-chars
JWT_ALGORITHM=HS256
JWT_EXPIRATION_HOURS=8

# Application
APP_NAME=JustiFlow DCM System
APP_VERSION=2.0.0
ENVIRONMENT=production
DEBUG=false
PORT=8001
HOST=0.0.0.0

# CORS
CORS_ORIGINS=https://yourdomain.com,https://www.yourdomain.com

# Rate Limiting
RATE_LIMIT_ENABLED=true
RATE_LIMIT_PER_MINUTE=60
```

### Docker Deployment (Optional)

**Dockerfile for Backend:**

```dockerfile
FROM python:3.11-slim

WORKDIR /app

# Install dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy application
COPY . .

# Expose port
EXPOSE 8001

# Run application
CMD ["python", "main_mongodb.py"]
```

**Build and Run:**

```powershell
# Build Docker image
docker build -t justiflow-backend .

# Run container
docker run -p 8001:8001 --env-file .env.mongodb justiflow-backend
```

---

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Development Guidelines

- Follow PEP 8 for Python code
- Use ESLint and Prettier for TypeScript/React
- Write unit tests for new features
- Update documentation for API changes
- Keep commits atomic and descriptive
- Add comments for complex logic

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Authors

- **Vignesh Krishna** - *Lead Developer* - [@vigneshkriishna](https://github.com/vigneshkriishna)

---

## 🙏 Acknowledgments

- Bharatiya Nyaya Sanhita (BNS) 2023 for legal framework
- FastAPI team for excellent documentation
- React and TypeScript communities
- MongoDB Atlas for reliable cloud database services
- Indian judicial system for inspiration

---

## 📞 Support

For issues, questions, or suggestions:

- **GitHub Issues**: [Create an issue](https://github.com/vigneshkriishna/Yukthi-Differentiated_caseflow_management-/issues)
- **Documentation**: [Project Wiki](https://github.com/vigneshkriishna/Yukthi-Differentiated_caseflow_management-/wiki)

---

## 🗺️ Roadmap

### Version 2.1 (Q1 2025)
- [ ] Mobile app (React Native)
- [ ] WhatsApp/SMS notifications
- [ ] Multi-language support (Hindi, Tamil, etc.)
- [ ] Advanced AI case prediction models

### Version 2.2 (Q2 2025)
- [ ] Video conferencing integration
- [ ] E-filing integration with government systems
- [ ] Blockchain for document verification
- [ ] Advanced analytics dashboard with ML insights

### Version 3.0 (Q3 2025)
- [ ] Voice-to-text for case entry
- [ ] OCR for document scanning
- [ ] Integration with National Judicial Data Grid (NJDG)
- [ ] Mobile-first progressive web app

---

<div align="center">

**Made with ❤️ for the Indian Judicial System**

⭐ Star this repo if you find it helpful!

[![GitHub stars](https://img.shields.io/github/stars/vigneshkriishna/Yukthi-Differentiated_caseflow_management-.svg?style=social&label=Star)](https://github.com/vigneshkriishna/Yukthi-Differentiated_caseflow_management-)
[![GitHub forks](https://img.shields.io/github/forks/vigneshkriishna/Yukthi-Differentiated_caseflow_management-.svg?style=social&label=Fork)](https://github.com/vigneshkriishna/Yukthi-Differentiated_caseflow_management-/fork)

</div>
