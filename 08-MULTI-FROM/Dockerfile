FROM redhat/ubi9:latest
RUN dnf install -y --setopt=install_weak_deps=False maven git && \
    dnf clean all && \
    rm -rf /var/cache/dnf
RUN git clone https://github.com/roboshop-devops-project-v3/shipping.git /app
WORKDIR /app
RUN mvn clean package
ENTRYPOINT ["java", "-jar", "/app/target/shipping-1.0.jar"]


FROM redhat/ubi9:latest
RUN dnf install -y java-17-openjdk-headless
copy --from=builder /app/target/shipping-1.0.jar /shipping-1.0.jar
ENTRYPOINT ["java", "-jar", "/shipping-1.0.jar"]