# 1. CREATE PROCEDURE

**Mục tiêu:**
Giả sử muốn tạo thủ tục để thêm một bản ghi mượn sách mới, giúp thêm bản ghi mượn sách mà không cần viết lại câu lệnh INSERT mỗi lần

**Cú pháp SQL:**
```sql
CREATE PROCEDURE AddBorrowRecord
    @borrow_id INT,
    @reader_id INT,
    @book_id INT,
    @borrow_date DATE,
    @return_date DATE = NULL,
    @status VARCHAR(20) = 'Đang mượn'
AS
BEGIN
    INSERT INTO BOOK_RECORDS (borrow_id, reader_id, book_id, borrow_date, return_date, Statuss)
    VALUES (@borrow_id, @reader_id, @book_id, @borrow_date, @return_date, @status);
END;
```
-Có thể gọi thủ tục bằng: 

**Cú pháp SQL:**
```sql
EXEC AddBorrowRecord 6, 2, 3, '2025-10-26';
```
