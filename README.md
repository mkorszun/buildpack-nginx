
buildpack-nginx
===============

Setup
-----

Put your configuration into `.nginx-conf/*.conf` in the root of your
repository. Example:

```
location / {
  uwsgi_pass unix:///tmp/uwsgi.sock;
  include uwsgi_params;
}

location /static {
  autoindex on;
}
```
