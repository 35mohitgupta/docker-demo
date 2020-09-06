# docker-demo

<!-- build docker.dev file -->
sudo docker build -t devimg -f Dockerfile.dev .

<!-- run docker image with port mapping -->
sudo docker run -p 3000:3000 devimg

<!-- if development server stops automatically -->
sudo docker run -it -p 3000:3000 devimg

<!--  Docker volumes and bookmarking volumes for automatic reload -->
sudo docker run -it -p 3000:3000 -v /app/node_modules -v $(pwd):/app devimg

<!-- docker-compose  -->
sudo docker-compose up --build
sudo docker-compose up
sudo docker-compose down

<!-- run for production dockerfile -->
sudo docker build -t prodimg .
sudo docker run -p "8080:80" prodimg   <!-- 80 is the default port of nginx -->

