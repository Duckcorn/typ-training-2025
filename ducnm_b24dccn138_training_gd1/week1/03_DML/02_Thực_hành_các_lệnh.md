# 1. INSERT

**Mục tiêu:**
Thêm thông tin của một số cuốn sách bao gồm: book_id, tiêu đề, tác giả, thể loại, năm sản xuất vào trong cấu trúc bảng 'BOOKS'

**Cú pháp SQL:**
```sql
INSERT INTO BOOKS (book_id, tittle, author, category, year_published)
VALUES (1, 'To Kill a Mockingbird', 'Harper Lee', 'Fiction', 1960);

INSERT INTO BOOKS (book_id, tittle, author, category, year_published)
VALUES (2, '1984', 'George Orwell', 'Dystopian', 1949);

INSERT INTO BOOKS (book_id, tittle, author, category, year_published)
VALUES (3, 'The Great Gatsby', 'F. Scott Fitzgerald', 'Classic', 1925);

INSERT INTO BOOKS (book_id, tittle, author, category, year_published)
VALUES (4, 'Pride and Prejudice', 'Jane Austen', 'Romantic', 1813);

INSERT INTO BOOKS (book_id, tittle, author, category, year_published)
VALUES (5, 'The Hobbit', 'J.R.R. Tolkien', 'Fantasy', 1937);
```


**Mục tiêu:**
Thêm thông của một số người mượn sách vào trong cấu trúc bảng 'Readers'

**Cú pháp SQL:**
```sql
INSERT INTO READERS (reader_id, name, living, phone)
VALUES (1, 'Bùi Hoàng Vinh', 'Thái Bình', '0912345678');

INSERT INTO READERS (reader_id, name, living, phone)
VALUES (2, 'Ngô Xuân Hòa', 'Thái Bình, '0987654321');

INSERT INTO READERS (reader_id, name, living, phone)
VALUES (3, 'Lê Hoàng Long', 'TP. Hồ Chí Minh', '0905123456');

INSERT INTO READERS (reader_id, name, living, phone)
VALUES (4, 'Phạm Minh Châu', 'Cần Thơ', '0934678901');

INSERT INTO READERS (reader_id, name, living, phone)
VALUES (5, 'Ngô Minh Đức', 'Hải Phòng', '0978123456');
```

**Mục tiêu:**
Thêm thông tin về mượn trả sách của từng độc giả vào cấu trúc bảng 'BOOK_RECORDS'

**Cú pháp SQL:**
```sql
INSERT INTO BOOK_RECORDS (borrow_id, reader_id, book_id, borrow_date, return_date, Statuss)
VALUES (1, 1, 2, '2025-10-01', '2025-10-15', 'Đã trả');

INSERT INTO BOOK_RECORDS (borrow_id, reader_id, book_id, borrow_date, return_date, Statuss)
VALUES (2, 2, 4, '2025-10-05', NULL, 'Đang mượn');

INSERT INTO BOOK_RECORDS (borrow_id, reader_id, book_id, borrow_date, return_date, Statuss)
VALUES (3, 3, 1, '2025-09-25', '2025-10-02', 'Đã trả');

INSERT INTO BOOK_RECORDS (borrow_id, reader_id, book_id, borrow_date, return_date, Statuss)
VALUES (4, 4, 5, '2025-10-10', NULL, 'Đang mượn');

INSERT INTO BOOK_RECORDS (borrow_id, reader_id, book_id, borrow_date, return_date, Statuss)
VALUES (5, 5, 3, '2025-09-30', '2025-10-12', 'Đã trả');
```

# 2. UPDATE
