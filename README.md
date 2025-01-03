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
```

---

### **3. Build and configure**
```bash
mkdir build
cd build
sudo git clone https://github.com/gophish/gophish.git
cd gophish

sudo npm install --only=dev
sudo gulp
```

Apply specific code modifications:
```bash
sudo sed -i 's/X-Contact/X-Contact/g' models/email_request_test.go
sudo sed -i 's/X-Contact/X-Contact/g' models/maillog.go
sudo sed -i 's/X-Contact/X-Contact/g' models/maillog_test.go
sudo sed -i 's/X-Contact/X-Contact/g' models/email_request.go
sudo sed -i 's/X-Signature/X-Signature/g' webhook/webhook.go
sudo sed -i 's/const ServerName = "gophish"/const ServerName = "IGNORE"/' config/config.go
sudo sed -i 's/const RecipientParameter = "rid"/const RecipientParameter = "keyname"/g' models/campaign.go
```

Build the project:
```bash
go get -v && go build -v
sudo apt-get update && sudo apt-get install --no-install-recommends -y jq libcap2-bin && sudo apt-get clean
sudo rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
sudo sed -i 's/127.0.0.1/0.0.0.0/g' config.json
go build ./gophish
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







$\color{#a3a3a3}{Copyright (c)2024Stiimy}$

