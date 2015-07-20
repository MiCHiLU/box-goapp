# goapp box

Box that extends the default wercker/golang box to include go-appengine for easy use with Google App Engine applications.

[![wercker status](https://app.wercker.com/status/6491bd9bfdd500650f12b2a6454ff49f/m "wercker status")](https://app.wercker.com/project/bykey/6491bd9bfdd500650f12b2a6454ff49f)

How to use this box:
In the wercker.yml of your application use the following box definition:
```
box: michilu/goapp
```

If you want deploy to production of Google App Engine:
```
box: michilu/goapp
deploy:
  steps:
  - setup-go-workspace
  - michilu/go-appengine-deploy:
      token:    $APP_ENGINE_TOKEN
```
