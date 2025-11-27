# 🔧 MongoDB Setup Guide for JustiFlow

## ❌ Current Problem
Your network is **blocking MongoDB Atlas** connections. DNS queries to `cluster0.w7x5vdv.mongodb.net` are timing out due to firewall/proxy restrictions.

---

## ✅ Solution: Install Local MongoDB

### **Option 1: Install MongoDB Community Edition (RECOMMENDED)**

#### Step 1: Download MongoDB
1. Open browser and go to: **https://www.mongodb.com/try/download/community**
2. Select:
   - Version: **7.0** (or latest)
   - Platform: **Windows x64**
   - Package: **MSI**
3. Click **Download**

#### Step 2: Install MongoDB
1. Run the downloaded `.msi` installer
2. Click **Next** through the welcome screen
3. Accept the license agreement
4. Choose **Complete** installation type
5. **IMPORTANT**: On "Service Configuration" screen:
   - ✅ Check **"Install MongoDB as a Service"**
   - ✅ Check **"Run service as Network Service user"**
   - Service Name: `MongoDB`
   - Data Directory: `C:\Program Files\MongoDB\Server\7.0\data\`
   - Log Directory: `C:\Program Files\MongoDB\Server\7.0\log\`
6. **Uncheck** "Install MongoDB Compass" (optional UI tool, not needed now)
7. Click **Install** and wait for completion
8. Click **Finish**

#### Step 3: Verify Installation
Open PowerShell and run:
```powershell
.\verify_mongodb.ps1
```

Or manually check:
```powershell
Get-Service -Name "MongoDB"
Test-NetConnection -ComputerName localhost -Port 27017
```

You should see:
- ✅ Service Status: **Running**
- ✅ Port 27017: **Open**

#### Step 4: Switch to Local MongoDB
```powershell
# Backup current config
Copy-Item .env.mongodb .env.mongodb.backup

# Use local config
Copy-Item .env.local .env.mongodb

# Or manually edit .env.mongodb and change this line:
# MONGODB_URL=mongodb://localhost:27017/
```

#### Step 5: Start the Backend
```powershell
python main_mongodb.py
```

---

### **Option 2: Use MongoDB Docker Container (If Docker is installed)**

#### Quick Setup:
```powershell
# Start MongoDB in Docker
docker run -d `
  --name mongodb-justiflow `
  -p 27017:27017 `
  -e MONGO_INITDB_ROOT_USERNAME=admin `
  -e MONGO_INITDB_ROOT_PASSWORD=password123 `
  mongo:7.0

# Update .env.mongodb
MONGODB_URL=mongodb://admin:password123@localhost:27017/
```

---

### **Option 3: Try Different Network**

If you can't install MongoDB locally:
1. **Mobile Hotspot**: Connect to your phone's internet
2. **VPN**: Use a VPN service to bypass network restrictions
3. **Different Network**: Try from home/café WiFi

---

## 🚀 Quick Start After Installation

1. **Verify MongoDB is running:**
   ```powershell
   Get-Service MongoDB
   ```

2. **Update configuration:**
   ```powershell
   Copy-Item .env.local .env.mongodb -Force
   ```

3. **Start backend:**
   ```powershell
   python main_mongodb.py
   ```

4. **Check backend:**
   - API: http://localhost:8001/docs
   - Health: http://localhost:8001/

---

## 🔍 Troubleshooting

### MongoDB Won't Start
```powershell
# Check service
Get-Service MongoDB | Start-Service

# Check logs
Get-Content "C:\Program Files\MongoDB\Server\7.0\log\mongod.log" -Tail 20
```

### Port 27017 Already in Use
```powershell
# Find what's using the port
netstat -ano | findstr :27017

# Kill that process (replace PID)
Stop-Process -Id <PID> -Force
```

### Backend Still Can't Connect
```powershell
# Test connection manually
Test-NetConnection localhost -Port 27017

# Check if MongoDB is listening
netstat -ano | findstr :27017
```

---

## 📝 Files Created

- ✅ `verify_mongodb.ps1` - Script to verify MongoDB installation
- ✅ `.env.local` - Local MongoDB configuration
- ✅ `.env.mongodb.backup` - Backup of Atlas config (after copying)

---

## 🎯 Next Steps

1. Install MongoDB Community Edition
2. Run `.\verify_mongodb.ps1`
3. Copy `.env.local` to `.env.mongodb`
4. Start backend: `python main_mongodb.py`
5. Access frontend: http://localhost:3000

---

## ❓ Need Help?

If you encounter issues:
1. Check Windows Firewall allows MongoDB
2. Ensure MongoDB service is running
3. Verify port 27017 is not blocked
4. Check MongoDB logs for errors
