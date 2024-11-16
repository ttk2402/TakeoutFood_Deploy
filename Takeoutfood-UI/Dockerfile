# Sử dụng Node.js runtime chính thức làm image nền
FROM node:20-alpine

# Thiết lập thư mục làm việc trong container
WORKDIR /app

# Sao chép các file package.json và package-lock.json vào container
COPY package.json package-lock.json ./

# Cài đặt các dependencies của dự án
RUN npm install

# Sao chép các file còn lại của dự án vào container
COPY . .

# Mở cổng 5173 cho server phát triển
EXPOSE 5173

# Chạy ứng dụng ở chế độ phát triển và lắng nghe trên tất cả các địa chỉ IP
CMD ["npm", "run", "dev", "--", "--host"]
