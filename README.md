# Keybox Checker


Download the code.
```shell
git clone https://github.com/dnascorpionOfficialX/KeyboxChecker.git
cd KeyboxChecker
```

Copy configuration file.
```shell
cp .env.exp .env
```

Fill out the configuration file.
```
TELEGRAM_BOT_TOKEN=xxx
# TELEGRAM_BOT_PROXY_ADDRESS=socks5://127.0.0.1:7890
```

-- Local Deployment
Install dependencies and run.
```shell
pip3 install pdm
pdm install
pdm run python main.py
```
Use PM2 to daemonize the process.
```shell
pm2 start pm2.json
pm2 monit
pm2 restart pm2.json
pm2 stop pm2.json
```

Docker Deployment
Use pre-built image.
```shell
docker run -d --name keyboxchecker --env-file .env ghcr.io/kimmyxyc/keyboxchecker:main
```

Usage
/check  
Send the keybox.xml file in the private chat or reply with /check to keybox.xml file.

![Usage](./screenshot.png)
