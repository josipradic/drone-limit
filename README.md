docker build -t drone-limit:latest .
docker run -d --rm --name drone-limit -p 2000:80 -p 2443:443 -e DRONE_GITEA_SERVER=http://gitea.192.168.1.158.xip.io -e DRONE_SERVER_HOST=drone.192.168.1.158.xip.io drone-limit:latest
