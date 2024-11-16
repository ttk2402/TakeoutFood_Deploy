# Sử dụng một image JDK chính thức
FROM openjdk:17-jdk-slim

# Cài đặt tzdata và thiết lập múi giờ
RUN set -eux; \
    apt-get update; \
    apt-get install -y --no-install-recommends tzdata; \
    ln -snf /usr/share/zoneinfo/Asia/Ho_Chi_Minh /etc/localtime; \
    echo "Asia/Ho_Chi_Minh" > /etc/timezone; \
    apt-get clean; \
    rm -rf /var/lib/apt/lists/*

# Tạo thư mục ứng dụng
RUN mkdir -p /app

# Đặt thư mục làm việc
WORKDIR /app

# Sao chép tệp JAR ứng dụng và đặt tên cố định là app.jar
COPY target/vnpay-service-0.0.1-SNAPSHOT.jar vnpay-service-0.0.1-SNAPSHOT.jar

# Cấu hình entrypoint để chạy ứng dụng
ENTRYPOINT ["java", "-jar", "vnpay-service-0.0.1-SNAPSHOT.jar"]
