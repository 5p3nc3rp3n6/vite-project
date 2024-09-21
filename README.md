# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

docker build  -t kaipus/vite-project:3.0.0 .
docker push kaipus/vite-project:2.0.0

docker run -dp 127.0.0.1:5000:8000 kaipus/vite-project:0.0.1

# If you are using an M1 or newer chip, use the following command to create the Docker image:

docker buildx build --platform linux/amd64 -t kaipus/vite-project:1.0.0 .
docker push kaipus/vite-project:1.0.0

docker run -dp 127.0.0.1:80:2999 kaipus/server_social_media:1.0.0
docker run -dp 80:2999 kaipus/server_social_media:2.0.0

ssh -i "spencerdocker.pem" ec2-user@ec2-54-89-52-219.compute-1.amazonaws.com
scp -i "spencerdocker.pem" server_social_media.zip ec2-user@ec2-54-89-52-219.compute-1.amazonaws.com:/home/ec2-user/.

### clean containers
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)

### run dockers
cd vite-project
docker build  -t vite-project .
docker run -dp 8080:8000 vite-project

cd ../server_social_media
docker build -t server_social_media .
docker run -dp 8081:2999 server_social_media
