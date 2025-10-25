## 🧱 **DDL (Data Definition Language)**  
> **DDL** là tập hợp các lệnh SQL dùng để **định nghĩa, tạo, sửa đổi và xóa cấu trúc** của cơ sở dữ liệu.  
> Nó tập trung vào **khung (schema)** của cơ sở dữ liệu chứ **không tác động trực tiếp đến dữ liệu** bên trong.

---

### ⚙️ **1. CREATE TABLE**
**Mục đích:** Tạo một bảng mới trong cơ sở dữ liệu.  

**Cú pháp:**
```sql
CREATE TABLE ten_bang (
    ten_cot_1 kieu_du_lieu [rang_buoc_cot],
    ten_cot_2 kieu_du_lieu [rang_buoc_cot],
    ...
    [CONSTRAINT ten_rang_buoc_bang] [loai_rang_buoc] [ten_cot_lien_quan],
    ...
);



