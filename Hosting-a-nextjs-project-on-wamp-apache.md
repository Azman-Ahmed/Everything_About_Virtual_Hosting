Apache HTTP Server is the web server component of WAMP. It is responsible for handling requests from clients (typically web browsers) and serving web pages and other content over the internet or local networks.

# Add a VirtualHost
## Open the httpd-vhosts.conf file:

Path:
```bash
C:\wamp64\bin\apache\apache2.4.59\conf\extra\httpd-vhosts.conf
```

## Add the VirtualHost configuration for your project:

```bash
<VirtualHost *:80>
    ServerName myproject.local
    DocumentRoot "F:/Azman-Ahmed-website/azmanahmed"
    <Directory "F:/Azman-Ahmed-website/azmanahmed/">
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>
```
- Replace myproject.local with your desired local domain.
- Update the DocumentRoot and <Directory> paths to the location of your project.

# Update the Hosts File
## Open the hosts file:

Path:
```bash
C:\Windows\System32\drivers\etc\hosts
```
## Add this entry:

```bash
127.0.0.1 myproject.local
```
- Save the file.


# Restart WAMP Server
- Click on the WAMP icon in the system tray.
- Select Restart All Services to reload the configuration.

