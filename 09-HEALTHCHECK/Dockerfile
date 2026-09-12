FROM docker.io/redhat/ubi9:latest
RUN  dnf install nginx -y
ENTRYPOINT ["nginx", "-g", "daemon off;"]
EXPOSE 80/tcp
HEALTHCHECK --interval=30s --timeout=30s CMD curl -f http://localhost:80/ || exit 1

