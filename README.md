Before you start
```
sudo apt install apache2-utils
```

Then creat directory for store our authenticaion

```
mkdir auth && cd $_
```

Create a user

```
htpasswd -Bc registry.password username
```

To creat another users

```
htpasswd registry.password other_username
```

Change `yourdomain` in `docker-compose.yml` file to your domain name (it should point to your server public ip address that you clone this repo), and `your_email` in  `traefik/traefik.toml` to your email address


Now you can start your private docker registry


```
docker-compose up -d
```

Now go to `https://yourdomain/v2" to see your private docker registry
