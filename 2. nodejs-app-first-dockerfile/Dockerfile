FROM node

LABEL maintainer="datebank@gmail.com"

WORKDIR /app

COPY package.json /app

RUN npm install

# Thông thường chúng ta sẽ thay đổi toàn bộ source code, ngoại trừ package.json file
# do đó chúng ta nên ưu tiên thực thi COPY package.json vào container trước, ưu tiên cài đặt npm trước
# để tối ưu hiệu năng, tức là bộ nhớ cache
# Có nghĩa là mỗi khi chúng ta thay đổi source code thì không chạy thực thi lại COPY package.json
# và không cần thực thi RUN npm install nữa, điều này giúp giảm thời gian image build
# vì chỉ cần thực thi những dòng lệnh COPY ., EXPOSE 9999, CMD thôi
COPY . /app/

EXPOSE 9999

CMD ["node","server.js"]