# free-SSL-letsencrypt-
Manually install free letsencrypt SSL

### install certbot(ubuntu)
sudo apt-get install certbot

### letsencrypt SSL
sudo certbot certonly --manual -d yourdomain.com -d www.yourdomain.com --agree-tos --manual-public-ip-logging-ok --preferred-challenges http-01 --server https://acme-v02.api.letsencrypt.org/directory --register-unsafely-without-email --rsa-key-size 4096

### letsencrypt SSL(Wildcard certificate)
certbot certonly --manual -d *.yourdomain.com -d yourdomain.com --agree-tos --manual-public-ip-logging-ok --preferred-challenges dns-01 --server https://acme-v02.api.letsencrypt.org/directory --register-unsafely-without-email --rsa-key-size 4096


