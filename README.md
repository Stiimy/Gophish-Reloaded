# Gophish-Reloaded

![Version](https://img.shields.io/badge/version-0.1-purple)
![License](https://img.shields.io/badge/license-MIT-darkred)
![Warning](https://img.shields.io/badge/Educational%20Purpose%20Only%20!!!-indigo)

**Gophish-Reloaded** is an improved version of [Gophish](https://getgophish.com/) with additional features to simplify and enhance phishing campaigns.

---

## 🚀 **Installation**

### **1. Update the system**
Open a terminal and run the following command to update your system:
```bash
sudo apt update && sudo apt upgrade -y
```
*(Note: If your network blocks certain sites, consider using a connection sharing setup.)*

---

### **2. Prerequisites and download**
Install the required dependencies:
```bash
cd Documents
sudo apt install npm
sudo npm install gulp gulp-cli -g 
sudo apt update && apt install git
git clone  -b main-clone https://github.com/Stiimy/Gophish-Reloaded.git
cd Gophish-Reloaded
```
Check File Existence: 
```bash
ls -l ./gophish
```
Check Execution Permissions:
```bash
chmod +x gophish
```
Launch Gophish:
```bash
sudo ./gophish
```

---

## 🔑 **Accessing the Gophish Interface**

1. Locate the username and password generated in the logs:
```
time="2024-10-17T11:07:33+02:00" level=info msg="Please login with the username admin and the password 0f056811491fd558"
```

2. Note the server startup URL:
```
time="2024-10-17T11:07:33+02:00" level=info msg="Starting admin server at https://127.0.0.1:3333/"
```

3. Log in to the interface and start setting up your phishing campaigns.

---

## 🤝 **Contributions**
Contributions are welcome! Please open an issue or submit a Pull Request.

---

## ⚖️ **License**
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.

---

## 📸 **Screenshot**
![Gophish Interface](images/demo.png)

---

## ⚠️ **Disclaimer**
This project is intended for educational purposes only. The author is not responsible for any misuse or consequences resulting from its use.

---







$\color{#a3a3a3}{Copyright (c)  2024 Stiimy}$

