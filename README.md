# SIT323 - 2.1P: Node.js and Express Web Server  

## 📖 Overview  
This project is a simple **Node.js web server** built using the **Express framework**. The server serves a basic HTML page with the following features:  
✅ Displays **your name in red**  
✅ Has a **light blue background**  
✅ Runs on `http://localhost:3000`  

The purpose of this project is to practice setting up a **web server with Express** and serving a static HTML page.  

---

---

## 🛠️ Steps to Set Up & Run the Project  

### **1️⃣ Install Node.js and Express**  
Before running the project, ensure you have **Node.js installed**. You can check by running:  

```sh
node -v
npm init -y   # Initializes a Node.js project (creates package.json)
npm install express
const express = require('express');
const app = express();
const port = 3000;

app.use(express.static(__dirname)); // Serves static files

app.get('/', (req, res) => {
    res.sendFile(__dirname + '/index.html');
});

app.listen(port, () => {
    console.log(`Server is running on http://localhost:${port}`);
});
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Web Page</title>
    <style>
        body {
            background-color: lightblue;
            text-align: center;
            font-family: Arial, sans-serif;
        }
        h1 {
            color: red;
        }
    </style>
</head>
<body>
    <h1>My Name</h1>
    <p>Welcome to my simple webpage using Node.js and Express!</p>
</body>
</html>
🌍 Deploying to GitHub

5️⃣ Initialize Git & Push Code to GitHub
1️⃣ Initialize Git in the project folder:
git init
2️⃣ Add all files to Git:
git add .
3️⃣ Commit the changes:
git commit -m "Initial commit - Added web server and webpage"
4️⃣ Create a GitHub repository named sit323-2025-prac2p and copy the remote URL.

5️⃣ Connect your local project to GitHub:

git remote add origin https://github.com/your-username/sit323-2025-prac2p.git
6️⃣ Push your code to GitHub:

git push origin main
