
## **Important Points About Security Groups**

- Region specific.
- Only **Allow** rules (no **Deny** rules).
- All inbound traffic is blocked, and outbound traffic is allowed by default.

### **You Define Rules For Specific**

- **Protocols** (like HTTP, HTTPS, SSH, etc.).
- **Port numbers** (e.g., Port 80 for HTTP, Port 22 for SSH).
- **IP addresses or ranges** (e.g., allow traffic only from a specific IP or range of IPs).

### **Automatic Response Traffic**

- If you allow incoming traffic on a specific port (e.g., Port 80 for HTTP), the outgoing response traffic is automatically allowed without requiring an explicit outbound rule.

---

## **Some Ports You Should Be Aware Of**

- **HTTP (Port 80)** – Unencrypted web traffic.
- **HTTPS (Port 443)** – Encrypted web traffic (SSL/TLS).
- **SSH (Port 22)** – Secure remote access to servers (Linux/Unix).
- **FTP (Port 21)** – File Transfer Protocol (unsecured).
- **SFTP (Port 22)** – Secure File Transfer Protocol.
- **SMTP (Port 25)** – Simple Mail Transfer Protocol (email sending).
- **RDP (Port 3389)** – Remote Desktop Protocol (Windows remote access).
- **MySQL (Port 3306)** – MySQL database connections.
- **PostgreSQL (Port 5432)** – PostgreSQL database connections.
- **DNS (Port 53)** – Domain Name System (converts domain names to IP addresses).

---