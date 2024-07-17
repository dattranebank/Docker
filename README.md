# Hướng dẫn sử dụng Docker repository
Chào các bạn, mình là Đạt, đây là những ví dụ thực hành Docker dành cho người mới tìm hiểu Docker
## Mục lục
1. Tải và cài đặt Docker trên Windows 10 Pro
2. Thiết lập
3.  Demo
## 1. Tải và cài đặt Docker trên Windows 10 Pro
* Link tải Docker trên Win 10: https://docs.docker.com/desktop/install/windows-install/ 
* Bật Hyper-V trên Win 10 Pro: https://learn.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v 
* Bật Container trên Win 10 Pro: https://stackoverflow.com/questions/36590514/how-to-enable-the-windows-10-containers-feature 
* Link tham khảo: https://medium.com/@polingtonalphonse/docker-containerization-without-docker-desktop-b65e35a1059c
## 2. Thiết lập
Chúng ta cần chuẩn bị:
* Tải Visual Studio Code để thực hiện các demo
* Khởi động VS Code và cài đặt các extensions: Docker, Prettier - Code formatter

![image](https://github.com/user-attachments/assets/7d7ddb05-68d9-4aea-9b3c-099e6cd6510a)

## 3. Demo
### 3.1. first-demo-starting-setup
Thực hiện các bước:
1. Khởi động Docker Desktop
2. Tải project
3. Mở project bằng VS Code Chúng ta tải project về
4. Mở Terminal và nhập \
`docker image build .` \
Ta sẽ thấy được image id của container vừa build, ví dụ như sha256:77ba824dbfa8a12a81b98d8e73e4d1f2580608733df12b36c566ae7119a98e63 \
`docker container run -p 5000:3000 77ba824dbfa8a12a81b98d8e73e4d1f2580608733df12b36c566ae7119a98e63`
