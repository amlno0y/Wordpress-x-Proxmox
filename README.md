# Wordpress-x-Proxmox
buat anak imup belajar lov lov

## JOM MULAI
Pertama kamuu masukkan ini saat sudah masuk ke ubuntu di dalam proxmox
```bash
apt update && apt upgrade -y
```

```bash
apt install -y apache2 mysql-server php php-mysql php-curl php-gd php-mbstring php-xml php-zip libapache2-mod-php
```

```bash
sudo mysql -e "CREATE DATABASE wordpress; CREATE USER 'wpuser'@'localhost' IDENTIFIED BY 'P@ssw0rd123'; GRANT ALL ON wordpress.* TO 'wpuser'@'localhost'; FLUSH PRIVILEGES;"
```

```bash
cd /tmp
```

```bash
wget -q https://wordpress.org/latest.tar.gz
```

```bash
tar -xzf latest.tar.gz
```

```bash
mv wordpress /var/www/html/
```

```bash
chown -R www-data:www-data /var/www/html/wordpress
```

```bash
a2enmod rewrite && systemctl restart apache2
```

```bash
cd /var/www/html/wordpress
```

```bash
cp wp-config-sample.php wp-config.php
```

```bash
sed -i "s/database_name_here/wordpress/" wp-config.php
```

```bash
sed -i "s/username_here/wpuser/" wp-config.php
```

```bash
sed -i "s/username_here/wpuser/" wp-config.php
```

```bash
sed -i "s/password_here/P@ssw0rd123/" wp-config.php
```
