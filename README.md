# CYBERSOFT ACADEMY

_(Lớp BootCamp Sáng 12 - Năm 2024 - Khoá Front-End)_

<div align="center">
	<picture>
		<img loading="lazy" width="100%" src="./img/banner-cybersoft-course.png" alt="Banner">
	</picture>
</div>

## [Buổi 10] THỰC HÀNH GIT

# Mục tiêu

1. Version Control System

2. Git và GitHub

3. Cài đặt Git

4. Khởi tạo dự án mới

5. Tham gia vào dự án có sẵn

6. Phát triển dự án

7. Branch

<hr>

> Bài làm của Trương Thục Vân.

# CÁC CÂU LỆNH THỰC HÀNH

## Khởi tạo Repository và Thêm Remote

```sh
git init
```

- Lệnh này khởi tạo một Git repository mới trong thư mục hiện tại. Sau khi chạy lệnh này, một thư mục ẩn .git sẽ được tạo ra.

```sh
git remote add origin https://github.com/MeiCloudie/demo_git.git
```

- Lệnh này thêm một remote repository mới có tên là origin, liên kết đến URL chỉ định.

- Remote repository là một phiên bản Git repository được lưu trữ trên mạng hoặc một máy chủ khác.

## Thêm và Kiểm tra Trạng thái Thay Đổi

```sh
git add .
```

- Lệnh này thêm tất cả các thay đổi trong thư mục hiện tại vào staging area (khu vực chờ để commit).

```sh
git status
```

- Lệnh này hiển thị trạng thái của working directory và staging area, cho biết những thay đổi nào đã được staged, chưa được staged và những file nào chưa được theo dõi.

## Commit và Xem Lịch Sử Commit

```sh
git commit -m "Initialize project"
```

- Lệnh này tạo một commit mới với thông điệp "Initialize project". Commit là một ảnh chụp của tất cả các thay đổi đã được staged.

```sh
git log
```

- Lệnh này hiển thị lịch sử các commit trong repository, bao gồm thông tin về tác giả, ngày tháng và thông điệp commit.

## Đẩy Thay Đổi Lên Remote Repository

```sh
git push -u origin master
```

hoặc

```sh
git push -u origin main
```

- Lệnh này đẩy các commit từ nhánh master/main lên remote repository origin.
- Tham số -u thiết lập nhánh upstream cho nhánh hiện tại, nghĩa là trong các lần push sau, chỉ cần sử dụng git push mà không cần chỉ định remote và nhánh.
- LƯU Ý: Lệnh **push** sẽ đi kèm với **-u origin** + tên nhánh => **THỰC HIỆN CHO LẦN ĐẦU TIÊN PUSH**!

- Các lần push sau chỉ cần câu lệnh đơn giản là:

```sh
git push
```

> Sau khi code xong 1 phần sẽ thực hiện: `git add .` => `git commit -m "nội dung commit"` => `git push`

## Quản Lý Các Nhánh

```sh
git branch
```

- Lệnh này liệt kê tất cả các nhánh hiện có trong repository, với nhánh hiện tại được đánh dấu bằng dấu sao (\*) hoặc màu xanh.

```sh
git branch nhanh1
```

- Lệnh này tạo một nhánh mới có tên "nhanh1" (chỉ tạo mà CHƯA nhảy qua nhánh nhanh1).

```sh
git checkout nhanh1
```

- Lệnh này chuyển đổi sang nhánh nhanh1 (nghĩa là khi sử dụng `git branch` nhánh hiện tại sẽ được chuyển qua "nhanh1").

```sh
git checkout -b nhanh1
```

- Lệnh này tạo một nhánh mới có tên "nhanh1" và chuyển đổi sang nhánh này ngay lập tức (câu lệnh kết hợp 2 thao tác trên).
