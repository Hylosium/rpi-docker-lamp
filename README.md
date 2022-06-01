Watch the video 👇

[![Watch the video](https://img.youtube.com/vi/v-r_12oezds/maxresdefault.jpg)](https://youtu.be/v-r_12oezds)

# rpi-docker-lamp for RaspberryPi

Docker with Apache, MariaDB, PHPMyAdmin and PHP.

I use docker-compose as an orchestrator. To run these containers:

```
docker-compose up -d
```

| Service |  Port |
| ------- | ----: |
| HTTP    |    80 |
| PHPADM  |  8000 |
| SQL     |  3306 |


Open phpmyadmin at [http://127.0.0.1:8000](http://127.0.0.1:8000) No password needed, only `root` user.
Open web browser to look at a simple php example at [http://127.0.0.1:80](http://127.0.0.1:80)

Clone YourProject on `www/` and then, open web [http://127.0.0.1/YourProject](http://127.0.0.1/YourProject)

Run MySQL client:

- `docker-compose exec db mysql -u root -p` 

Infrastructure as code!

Structure of folders:

```
/docker-lamp/
├── docker-compose.yml
├── Dockerfile
│
├── conf/
│
├── dump/
│   └── myDb.sql
└── www/
    └── index.php
```
