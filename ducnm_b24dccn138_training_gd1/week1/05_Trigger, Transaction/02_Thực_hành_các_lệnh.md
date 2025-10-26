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

# 2. CREATE FUNCTION

**Mục tiêu:**
Giả sử muốn tạo hàm để kiểm tra xem một cuốn sách có đang được mượn hay không

**Cú pháp SQL:**
```sql
CREATE FUNCTION CHECK_BOOK(@book_id INT)
RETURN VARCHAR(20)
AS
BEGIN
DECLARE @status VARCHAR(20);
    SELECT @status = Statuss
    FROM BOOK_RECORDS
    WHERE book_id = @book_id
      AND Statuss = 'Đang mượn';
    
    IF @status IS NULL
        RETURN 'Chưa mượn';
    ELSE
        RETURN 'Đang mượn';
END;
```

-Có thể sử dụng hàm trong câu lệnh SELECT để kiểm tra trạng thái mượn sách
**Cú pháp SQL:**
```sql
SELECT dbo.CHECK_BOOK(3)
```
