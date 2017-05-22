# Nginx default config

![nginx](https://img.shields.io/badge/nginx-1.13.0-green.svg)
![pagespeed](https://img.shields.io/badge/pagespeed-1.11.33.4-green.svg)
![pagespeed](https://img.shields.io/badge/ubuntu-14.04.4-green.svg)

I started this repository as a reminder for myself next time I need to go trough this process. Feedback === welcome.

This setup is made to make websites run faster and get a good [Google pagespeed test tool](https://developers.google.com/speed/pagespeed/insights) score. 

## Installing Nginx with PageSpeed (latest)

1. Install Nginx `$ sudo apt-get update && sudo apt-get install nginx`

2. Install Nginx dependencies: `$ sudo apt-get build-dep nginx`

3. Make sure nginx is not running.

4. Run: `$ bash <(curl -f -L -sS https://ngxpagespeed.com/install) --nginx-version latest`

5. When you get to the configure arguments list, insert the following: 

``` bash
--with-http_ssl_module --with-http_stub_status_module  --prefix=/usr/share/nginx --conf-path=/etc/nginx/nginx.conf --sbin-path=/usr/sbin --error-log-path=/var/log/nginx/error.log
```

You should now have Nginx installed with PageSpeed at the same location as Nginx would normally be installed.

## Include these default config files

1. Clone the repository into your server, and make sure the right permissions are set.


