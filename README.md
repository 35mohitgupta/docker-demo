# docker-demo

<!-- build docker.dev file -->
sudo docker build -t devimg -f Dockerfile.dev .

<!-- run docker image with port mapping -->
sudo docker run -p 3000:3000 devimg

<!-- if development server stops automatically -->
sudo docker run -it -p 3000:3000 devimg
