Running Jenkins via nginx reverse proxy with the Let's Encrypt cert:

1. Install Nginx
2. Create a server block with the subdomain.domain.tld config in /etc/nginx/sites-available, create a link to sites-enabled/
3. Add A record to the DNS zone for subdomain.domain.tld with the IP of your server
4. Install certbot & certificate for the subdomain
5. Install jenkins with the default settings
6. Change nginx config to forward incoming 443 traffic to localhost:8080
7. Change /etc/default/jenkins to listen on 127.0.0.1:8080
8. Restart nginx, jenkins. This should be all :)

Test page available: https://jenkins.moonhome.net/
