## DDL(Data Definition Language) là một tập hợp các lệnh SQL được sử dụng để định nghĩa, tạo, sửa đổi và xóa các cấu trúc của cơ sở dữ liệu. Nó tập trung vào "khung" của cơ sở dữ liệu chứ không phải dữ liệu bên trong.

## Các câu lệnh cơ bản trong DDL gồm: CREATE, ALTER, DROP, CREATE VIEW, DROP VIEW.

1. CREATE TABLE
- Mục đích: Lệnh này để tạo một bảng mới trong cơ sở dữ liệu.
- Cú pháp:
CREATE TABLE ten_bang(
    ten_cot_1 kieu_du_lieu[rang_buoc_cot],
    ten_cot_2 kieu_du_lieu[rang_buoc_cot],
    ...
    [CONSTRAINT ten_rang_buoc_bang] [loai_rang_buoc] [ten_cot_lien_quan],
    ...
);   

2. ALTER TABLE
- Mục đích: Lệnh này dùng để sửa đổi cấu trúc của một bảng đã tồn tại. Nó có nhiều mệnh đề con khác nhau.
- Cú pháp:
ALTER TABLE ten_bang[hanh_dong];

3. DROP TABLE
- Mục đích: Lệnh này để xóa vĩnh viễn một bảng và tất cả dữ liệu bên trong nó.
- Cú pháp:
DROP TABLE ten_bang;

4. CREATE VIEW
- Mục đích: Dùng để tạo mới một "view". "View" là một bảng ảo được định nghĩa bởi câu lệnh SELECT. Nó không lưu trữ dữ liệu thực tế mà chỉ lưu trữ câu truy vấn. Khi bạn truy vấn view, hệ thống sẽ chạy câu SELECT đó để lấy dữ liệu mới nhất.
- Cú pháp:
CREATE VIEW ten_view AS
SELECT cot_1, cot_2,...
FROM ten_bang
WHERE [dieu_kien];

5. DROP VIEW
- Mục đích: Dùng để xóa vĩnh viễn một view đã tồn tại. Lệnh này chỉ xóa định nghĩa của view, không ảnh hưởng đến dữ liệu trong bảng gốc mà view đó tham chiếu tới.
- Cú pháp:
DROP VIEW ten_view;




