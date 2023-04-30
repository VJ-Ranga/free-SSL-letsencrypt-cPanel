# free-SSL-letsencrypt
Manually install free letsencrypt SSL

### install certbot(ubuntu)
sudo apt-get install certbot

### letsencrypt SSL
sudo certbot certonly --manual -d yourdomain.com -d www.yourdomain.com --agree-tos --manual-public-ip-logging-ok --preferred-challenges http-01 --server https://acme-v02.api.letsencrypt.org/directory --register-unsafely-without-email --rsa-key-size 4096

### letsencrypt SSL(Wildcard certificate)
certbot certonly --manual -d *.yourdomain.com -d yourdomain.com --agree-tos --manual-public-ip-logging-ok --preferred-challenges dns-01 --server https://acme-v02.api.letsencrypt.org/directory --register-unsafely-without-email --rsa-key-size 4096


# free-SSL-letsencrypt-cPanel
Manually install free letsencrypt SSL cPanel (namecheap, godaddy,etc...)

### install acme.sh
curl https://get.acme.sh | sh

### letsencrypt SSL
.acme.sh/acme.sh --issue -d example.com -w /home/wwwroot/example.com

### letsencrypt SSL(Cloudflare)
export CF_Key="sdfsdfsdfljlbjkljlkjsdfoiwje"

export CF_Email="xxxx@sss.com"

.acme.sh/acme.sh  --issue --force --server letsencrypt -d example.com  -d '*.example.com'  --dns dns_cf

### Install SSL
.acme.sh/acme.sh --deploy --deploy-hook cpanel_uapi --domain example.com


### Hestiacp SSL issue fix
sudo /usr/local/hestia/bin/v-add-letsencrypt-host
