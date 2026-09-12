FROM redhat/ubi9:latest
RUN dnf install -y maven git
RUN mkdir /app
RUN git clone https://github.com/roboshop-devops-project-v3/shipping.git /app
WORKDIR /app