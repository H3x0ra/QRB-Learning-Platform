# QRB Learning Platform
*A deliberately vulnerable web application for cybersecurity training.*

QRB Learning Platform is an intentionally vulnerable PHP application designed to help students and security professionals practice real-world offensive security techniques in a safe, controlled lab environment.

This project includes multiple vulnerable modules aligned with **OWASP Top 10**, allowing hands-on practice with:

- SQL Injection
- Cross-Site Scripting (XSS)
- Local File Inclusion (LFI)
- File Upload Abuse

## ⭐ Features

- Full vulnerable web application written in PHP
- Clean and ready-to-import MySQL database
- Multiple independent labs (SQLi, XSS, LFI, Upload, BAC)
- Simple installation process
- Ideal for:
  - Cybersecurity students
  - CTF players
  - Ethical hacking learners
  - Web security training sessions

## ⚠️ Legal Notice

This platform is intentionally insecure.  
Use it **only** in isolated environments such as Kali Linux, VMs, or private labs.  
Do **NOT** deploy it on the internet.

The author is not responsible for any misuse.

# 🚀 Installation Guide (Kali Linux)

## 1️⃣ Clone the Repository

```bash
cd ~
git clone https://github.com/H3x0ra/QRB-Learning-Platform.git
cd QRB-Learning-Platform
```

## 2️⃣ Install Requirements

```bash
sudo apt update
sudo apt install -y apache2 php libapache2-mod-php php-mysqli mariadb-server unrar
sudo systemctl enable apache2 --now
sudo systemctl enable mariadb --now
```

## 3️⃣ Extract the Web Application

```bash
sudo unrar x QRB.rar
```

## 4️⃣ Deploy QRB to Apache

```bash
sudo rm -rf /var/www/html/QRB
sudo mv QRB /var/www/html/
```

## 5️⃣ Set Permissions

```bash
sudo chown -R www-data:www-data /var/www/html/QRB
sudo chmod -R 755 /var/www/html/QRB
```

## 6️⃣ Import the Database

```bash
mysql -uroot < Database.sql
```


## 7️⃣ Restart Apache

```bash
sudo systemctl restart apache2
```

## 8️⃣ Access the Platform

```
http://localhost/QRB/
```

# 🔐Create Account

### Admin
 Singup and then login


# 🧪 Lab Modules Included

### SQL Injection – `/Sql01/`
- Boolean-based  
- UNION-based  
- Authentication bypass  

### Cross-Site Scripting – `/Xss/`
- Stored XSS  
- Reflected XSS  

### File Upload Vulnerabilities – `/FileUpload/`
- Content-type bypass  
- Extension bypass  
- Uploading malicious files  

### Local File Inclusion – `/lfi_lab/`
- Path traversal  
- Reading system files  
- LFI to code execution  



# 📚 Purpose

- Web exploitation learning  
- OWASP Top 10 training  
- SOC analyst practice  
- University cybersecurity labs  
- Red/Blue team skill development  

# 👨‍💻 Author

**Qasim Tawalbeh — (H3x0ra)**  
GitHub: https://github.com/H3x0ra
LinkedIn: https://www.linkedin.com/in/qasim-tawalbeh-a3b75522b/
