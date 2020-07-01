# nginx-redirect
A very simple redirector using nginx and Docker

```
docker run -p 1234:80 --env RETURN_LOCATION='return 301 https://caprover.com$request_uri;' caprover/nginx-redirect
```


Open `http://localhost:1234` in your browser.



This is available as a CapRover one click app. It's useful when you want to create domain aliases. For example you want all traffic from `http(s)://www.example.com` to be redirected to `https://example.com`. In this case:
- Create an "Nginx Redirect" one click app and enter `https://example.com` as your redirect URL.
- Once the app is deployed, go to your panel and connect `www.example.com` to this app.
- You can connect more domains if you want to, such as `www2.example.com` and etc.
- Enable HTTPS for any (or all) of these added domains if needed.
- You are done! Now navigating to any of these connected addresses should redirect the user to `https://example.com`
- You can connect `example.com` to your actual app.
