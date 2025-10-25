# 1. Tạo bảng BOOKS

**Mục đích:**  
Tạo bảng `BOOKS` trong cơ sở dữ liệu để lưu thông tin về sách, bao gồm **mã sách, tiêu đề, tác giả, thể loại, năm xuất bản**.

**Cú pháp SQL:**
```sql
CREATE TABLE BOOKS (
    book_id INT,
    tittle VARCHAR(200) NOT NULL,
    author VARCHAR(100),
    category VARCHAR(50),
    year_published INT,
    CONSTRAINT pk_BOOKS PRIMARY KEY (book_id)
);
```
# 2. Tạo bảng Readers
**Mục đích:**
Tạo bảng `Readers` trong cơ sở dữ liệu để lưu thông tin người đọc.
**Cú pháp SQL:**
```sql
CREATE TABLE Readers(
	 reader_id INT,
	 name VARCHAR(20) NOT NULL,
	 living VARCHAR(200),
	 phone VARCHAR(15),
	 CONSTRAINT pk_Readers PRIMARY KEY(reader_id)
);
```
