# Gophish-Reloaded  
 
![Version](https://img.shields.io/badge/version-0.1-purple)  ![License](https://img.shields.io/badge/license-MIT-darkred)  ![Warning](https://img.shields.io/badge/Educational%20Purpose%20Only%20!!!-indigo)  
 
**Gophish-Reloaded** is an enhanced version of [Gophish](https://getgophish.com/) with additional features to simplify and improve phishing campaigns.  
 
---  
 
## 🚀 **Installation**  
 
### **1. System Update**  
 
Open a terminal and run the following command to update your system:  
 
```bash
sudo apt update && sudo apt upgrade -y
```  
 
*(Note: If your network blocks certain sites, consider using a mobile hotspot.)*  
 
---  
 
### **2. Prerequisites and Download**  
 
Install the required dependencies:  
 
```bash
cd Documents
 
sudo apt update && sudo apt install -y golang
 
sudo apt install npm
 
sudo npm install gulp gulp-cli -g  
 
sudo apt update && sudo apt install git
```  
 
Clone the Gophish repository:  
 
```bash
sudo git clone https://github.com/gophish/gophish.git
 
cd gophish
```  
 
---  
 
### **3. Compilation and Configuration**  
 
Install project dependencies:  
 
```bash
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
 
Prepare the environment and compile:  
 
```bash
go get -v && go build -v
 
sudo apt-get update && sudo apt-get install --no-install-recommends -y jq libcap2-bin && sudo apt-get clean
 
sudo rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
```  
 
Modify the configuration to allow remote access:  
 
```bash
sudo sed -i 's/127.0.0.1/0.0.0.0/g' config.json
```  
 
Add the directory as a safe repository for `git`:  
 
```bash
git config --global --add safe.directory /home/keran/Documents/build/gophish
```  
 
Compile Gophish:  
 
```bash
sudo go build -v
```  
 
---  
 
## 🔑 **Accessing the Gophish Interface**  
 
1. Locate the generated username and password in the logs:  
 
```  
time="2024-10-17T11:07:33+02:00" level=info msg="Please login with the username admin and the password 0f056811491fd558"
```  
 
2. Note the server startup URL:  
 
```  
time="2024-10-17T11:07:33+02:00" level=info msg="Starting admin server at https://127.0.0.1:3333/"
```  
 
3. Log in to the interface and start configuring your phishing campaigns.  
 
---  
 
## 🤝 **Contributions**  
 
Contributions are welcome! Open an issue or submit a Pull Request.  
 
---  
 
## ⚖️ **License**  
 
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.  
 
---  
 
## 📸 **Screenshot**  
 
![Gophish Interface](images/demo.png)  
 
---  
 
## ⚠️ **Disclaimer**  
 
This project is for educational purposes only. The author is not responsible for any misuse or consequences resulting from it.  
 
---  
 
$ \color{#a3a3a3}{Copyright (c)2024Stiimy}$

