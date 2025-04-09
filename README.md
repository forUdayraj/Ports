# 🔌 Default Ports and Configuration Guide

This README contains quick info about default ports for commonly used technologies and how to change them.

---

## 1️⃣ Spring Boot

- **Default Port:** `8080`

### ✅ Change the Port:

**Using `application.properties`:**
```properties
server.port=9090
```

**Using `application.yml`:**
```yaml
server:
  port: 9090
```

**Programmatically in Java:**
```java
@Bean
public WebServerFactoryCustomizer<ConfigurableWebServerFactory> webServerFactoryCustomizer() {
    return factory -> factory.setPort(9090);
}
```

---

## 2️⃣ React

- **Default Port:** `3000`

### ✅ Change the Port:

**Temporarily (one-time use):**

- On macOS/Linux:
```bash
PORT=4000 npm start
```

- On Windows CMD:
```cmd
set PORT=4000 && npm start
```

**Permanently:**

Create a `.env` file in the project root:
```env
PORT=4000
```

---

## 3️⃣ MySQL

- **Default Port:** `3306`

### ✅ Check/Change the Port:

- **Linux Config File:** `/etc/mysql/my.cnf` or `/etc/my.cnf`
- **Windows Config File:** `my.ini`

**Look for:**
```ini
[mysqld]
port=3306
```

**To Change:**
```ini
[mysqld]
port=3307
```

> Restart MySQL server after changing the port.

---

## ✅ Summary Table

| Technology     | Default Port | Changeable via           |
|----------------|--------------|---------------------------|
| Spring Boot    | 8080         | `application.properties` / `yml` / code |
| React          | 3000         | `.env` or terminal        |
| MySQL          | 3306         | `my.cnf` / `my.ini`       |

---

Happy Coding! 🚀
