## IIS Web Server – Flipkart Clone Application Deployment on Windows 11

### 1. Overview
Internet Information Services (IIS) is Microsoft’s enterprise-grade web server used to host websites and web applications on Windows operating systems. IIS supports static content such as HTML, CSS, and JavaScript, as well as dynamic applications built using ASP.NET and other frameworks.

In this hands-on lab, we deploy a **Flipkart Clone (static e-commerce web application)** on **Windows 11 using IIS**, simulating a real-world on-premises web hosting scenario.

---

### 2. Prerequisites
- Windows 11 system
- Administrator privileges
- Flipkart Clone source code (HTML, CSS, JavaScript)
- Basic understanding of web hosting concepts

---

### 3. Installing IIS on Windows 11
- Open **Control Panel**
- Navigate to **Programs → Turn Windows features on or off**
- Enable **Internet Information Services (IIS)**
  - Web Management Tools
  - World Wide Web Services
    - Common HTTP Features
    - Application Development Features
- Click **OK** and allow the installation to complete

---

### 4. Verifying IIS Installation
- Open a web browser
- Enter: `http://localhost`
- If the **IIS Welcome Page** appears, IIS has been installed successfully

---

### 5. Flipkart Clone Application Structure
Create a project folder named **FlipkartClone** containing:
- `index.html` (main entry file)
- `css/` (stylesheets)
- `js/` (JavaScript files)
- `images/` (banners, product images)

This structure reflects a standard static web application layout.

---

### 6. Deploying Website Files
- Copy the **FlipkartClone** folder
- Paste it into the IIS default web directory:
  - `C:\inetpub\wwwroot\`
- Final deployment path:
  - `C:\inetpub\wwwroot\FlipkartClone`

---

### 7. Opening IIS Manager
- Open **Start Menu**
- Search for **IIS Manager** and launch it

---

### 8. Creating a New Website in IIS
- In IIS Manager, right-click on **Sites**
- Select **Add Website**
- Enter the following details:
  - Site Name: `FlipkartClone`
  - Physical Path: `C:\inetpub\wwwroot\FlipkartClone`
  - Binding Type: `http`
  - IP Address: `All Unassigned`
  - Port: `8080` (or `80` if available)
- Click **OK** to create the site

---

### 9. Starting the Website
- Select **FlipkartClone** under Sites
- Click **Start** from the Actions panel

---

### 10. Accessing the Application
- Open a web browser
- Enter:
  - `http://localhost:8080`
- The Flipkart Clone web application should load successfully

---

### 11. Configuring Default Document
If the website does not load automatically:
- Select the site in IIS Manager
- Open **Default Document**
- Ensure `index.html` is listed and enabled

---

### 12. Resolving CSS or Image Loading Issues (MIME Types)
- Navigate to **MIME Types** in IIS Manager
- Verify the following entries exist:
  - `.css` → `text/css`
  - `.js` → `application/javascript`
  - `.png` → `image/png`
  - `.jpg` → `image/jpeg`

---

### 13. Firewall Configuration
If the site is not accessible:
- Open **Windows Defender Firewall**
- Go to **Advanced Settings → Inbound Rules**
- Allow the configured port (e.g., 8080)

---

### 14. Common Issues and Troubleshooting
- **404 Error**: Incorrect physical path
- **Blank Page**: Missing or misconfigured `index.html`
- **CSS/Images Not Loading**: MIME type misconfiguration
- **Port Conflict**: Another application using the same port

---

### 15. Real-World Use Cases
- Hosting static e-commerce UI demos
- Proof-of-concept (POC) deployments
- On-premises web hosting practice
- Training and learning environments

---

### 16. Interview Key Points
- IIS is a Windows-based web server by Microsoft
- Supports both static and dynamic web applications
- Default website directory: `C:\inetpub\wwwroot`
- Websites are hosted using HTTP/HTTPS bindings and ports

---

### 17. Summary
- IIS installed and verified
- Flipkart Clone application deployed
- Website configured and accessed successfully
- Common issues and solutions understood

---

**Trainer Reference – Cloud Tech Hacks**  
This lab provides a strong foundation for understanding IIS-based web hosting and real-world on-prem deployment scenarios.