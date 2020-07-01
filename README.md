# nginx-redirect
A very simple redirector using nginx and Docker

```
docker run -p 1234:80 --env RETURN_LOCATION='return 301 https://caprover.com$request_uri;' caprover/nginx-redirect
```


Open `http://localhost:1234` in your browser.
