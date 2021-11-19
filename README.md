### dockerizing-flask-app
Running Flask application inside alpine Container using docker compose

```sh
# tree .
# tree .
.
├── apps
│   ├── app.py
│   └── requirements.txt
├── docker-compose.yml
└── Dockerfile



```sh
# docker-compose up -d
Step 8/8 : CMD [ "python3" , "app.py"]
 ---> Running in 981ec1eb38c6
Removing intermediate container 981ec1eb38c6
 ---> aea300e5d282
Successfully built aea300e5d282
Successfully tagged apps_web:latest
WARNING: Image for service web was built because it did not already exist. To rebuild this image you must use `docker-compose build` or `docker-compose up --build`.
Creating apps_web_1 ... done
```



```sh
# docker ps -a
CONTAINER ID   IMAGE                  COMMAND                  CREATED              STATUS              PORTS                                       NAMES
ebd73f13f49b   apps_web               "python3 app.py"         About a minute ago   Up About a minute   0.0.0.0:5000->5000/tcp, :::5000->5000/tcp   apps_web_1

```

