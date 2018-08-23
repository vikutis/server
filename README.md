# Server (Express + MySQL) + Client (JavaScript + Bootstrap)

## Install MySQL
```bash
sudo apt install mariadb-server
```

## Create db and user
```sql
CREATE DATABASE server_db;
CREATE USER server_admin@localhost IDENTIFIED BY 'secret';
GRANT ALL PRIVILEGES on server_db.* to server_admin@localhost;
FLUSH PRIVILEGES;
```

### Create users table
```
{
  id: number;
  username: string;
  password: string;
}
```

```sql
CREATE TABLE users (
  id INT(6) UNSIGNED AUTO_INCREMENT PRIMARY KEY,
  username VARCHAR(30) NOT NULL,
  password VARCHAR(30) NOT NULL
);
```

### Insert users
```sql
INSERT INTO users(username, password) VALUES('user', 'secret');
```


