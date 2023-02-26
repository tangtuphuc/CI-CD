# Chọn một image để sử dụng làm cơ sở
FROM ubuntu:lasted

#setup trước 1 số câu lệnh trong container mới tạo ra
RUN sudo apt update
RUN sudo apt install apache2
RUN sudo ufw allow 'Apache'
RUN sudo vim
# Tạo thư mục làm việc cho ứng dụng của bạn
WORKDIR /var/www/html

# Đặt cổng mặc định của ứng dụng là 3000
EXPOSE 3000
ADD ./index.html var/www/html
# Chạy ứng dụng của bạn
ENTRYPOINT ["httpd"]
CMD ["-D","FOREGROUND"]
