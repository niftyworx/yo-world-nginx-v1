Yo world v1! - via nginx
=================

docker build -t nifyworx/yo-world-nginx-v1:latest .
docker run -p 80:80 nifyworx/yo-world-nginx-v1:latest

curl localhost:80 | http://localhost:80
curl localhost:80/v1/ | http://localhost:80/v1/

