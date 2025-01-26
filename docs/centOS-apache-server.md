# Enabling Apache HTTP Server and Allowing Traffic on CentOS

Follow the steps below to ensure the Apache HTTP server is enabled and HTTP traffic is allowed on a CentOS server.

## Steps

### Step 1: Start and Enable Apache
By default, the Apache service is not started automatically after installation. Start the service using:

```bash
sudo systemctl start httpd
```

Enable Apache to start on boot:

```bash
sudo systemctl enable httpd
```

### Step 2: Allow HTTP Traffic Through the Firewall
To allow HTTP traffic on port 80, add the rule to the firewall:

```bash
sudo firewall-cmd --add-port=80/tcp --permanent
sudo firewall-cmd --reload
```

With these steps, your Apache HTTP server should be enabled, and traffic on port 80 will be allowed.

