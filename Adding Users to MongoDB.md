## 1. Connect to MongoDB
```bash
mongosh --eval 'db.adminCommand({listDatabases: 1})'
```

## 2. Create a User
To create a user for a specific database (e.g., mydatabase), run:
```bash
mongosh --eval 'use mydatabase; db.createUser({user: "myUser", pwd: "mySecurePassword", roles: [{role: "readWrite", db: "mydatabase"}]})'
```

If you want to create an admin user:
```bash
mongosh --eval 'use admin; db.createUser({user: "adminUser", pwd: "strongPassword", roles: [{role: "root", db: "admin"}]})'
```

## 3. Verify User Creation
To list users:
```bash
mongosh --eval 'use mydatabase; show users'
```

## 4. Enable Authentication (Optional)
If authentication is disabled, open the MongoDB config file (/etc/mongod.conf or /usr/local/etc/mongod.conf) and enable authentication:
```bash
sudo sed -i '/security:/a \  authorization: enabled' /etc/mongod.conf
sudo systemctl restart mongod
```
or
```bash
sudo nano /etc/mongod.conf
```
Find the security section in the file. If it doesn’t exist, add it under the main YAML structure:
```yaml
security:
  authorization: enabled
```
```bash
sudo systemctl restart mongod
```

If authentication is enabled, you'll get an "Unauthorized" error.
Now, connect with a valid user:
```bash
mongosh -u myUser -p mySecurePassword --authenticationDatabase admin
```

## 5. Connect as the New User
```bash
mongosh -u myUser -p mySecurePassword --authenticationDatabase mydatabase
```
