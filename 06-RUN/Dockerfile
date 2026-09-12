FROM docker.io/redhat/ubi9:latest
RUN  dnf install nginx -y
ENTRYPOINT ["nginx", "-g", "daemon off;"]
EXPOSE 80/tcp
