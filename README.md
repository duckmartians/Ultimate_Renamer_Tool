# Ultimate Renamer Tool

Một công cụ mạnh mẽ và linh hoạt giúp bạn đổi tên hàng loạt file trong nhiều thư mục một cách nhanh chóng, an toàn và có kiểm soát. Giao diện được thiết kế trực quan để mọi người dùng đều có thể sử dụng dễ dàng.

## Tính năng nổi bật ✨

  * **Xử lý nhiều thư mục cùng lúc**: Dán bao nhiêu đường dẫn thư mục bạn muốn, tool sẽ xử lý tuần tự.
  * **Sắp xếp nâng cao**: Sắp xếp file theo tên, ngày tạo, kích thước, hoặc loại file trước khi đổi tên.
  * **Bộ lọc mạnh mẽ**: Chỉ đổi tên các file có định dạng bạn muốn (ví dụ: `.jpg`, `.png`, `.jpeg`).
  * **Quy tắc đặt tên linh hoạt**:
      * Đặt tên theo chuỗi ký tự đơn (`A`, `B`, `C`...).
      * Đặt tên theo cụm từ, tên dài (`Project_Alpha`, `Summer_Trip_2025`...).
  * **An toàn**: Sử dụng cơ chế đổi tên 2 bước để tránh xung đột và mất file.
  * **Giao diện hiện đại**: Sử dụng `ttkbootstrap` cho giao diện đẹp và thân thiện.
  * **Phản hồi thời gian thực**: Vùng log chi tiết cho bạn biết chính xác file nào đang được xử lý và kết quả ra sao.
<img width="802" height="682" alt="image" src="https://github.com/user-attachments/assets/0338ea5f-3f1c-472f-859c-dbd7df93e216" />

## Cách sử dụng 🚀

Rất đơn giản\! Bạn chỉ cần **tải về và chạy file `Ultimate Renamer Tool.exe`** để mở chương trình. Không cần cài đặt bất cứ thứ gì khác.

-----

## Hướng dẫn sử dụng chi tiết

Giao diện của tool được chia thành 3 khu vực chính.

### ➊ Khu vực 1: Đường dẫn thư mục

Đây là nơi bạn cung cấp danh sách các thư mục cần xử lý.

  * **Cách sử dụng**: Dán đường dẫn đến các thư mục của bạn vào ô text lớn. **Mỗi đường dẫn nằm trên một dòng riêng biệt.**
  * **Ví dụ**:
    ```
    C:\Users\MyUser\Pictures\Trip_DaNang
    D:\Projects\Render_Output\Final
    ```

### ➋ Khu vực 2: Tùy chọn

Đây là trung tâm điều khiển, nơi bạn thiết lập các quy tắc đổi tên.

  * **Sắp xếp theo**: Chọn tiêu chí để sắp xếp các file trước khi tiến hành đổi tên. Điều này quyết định thứ tự các file sẽ được đánh số.

      * `Thời gian tạo`: Sắp xếp file từ cũ nhất đến mới nhất.
      * `Kích thước file`: Sắp xếp file từ nhẹ nhất đến nặng nhất.
      * `Loại file`: Sắp xếp theo phần mở rộng (đuôi file), ví dụ tất cả file `.jpg` sẽ được xử lý trước các file `.png`.
      * `Tên file (mặc định)`: Sắp xếp theo thứ tự bảng chữ cái A-Z.

  * **Số file mỗi tiền tố**: Quy định số lượng file sẽ sử dụng chung một tiền tố trước khi chuyển sang tiền tố tiếp theo.

      * **Ví dụ**: Nếu bạn nhập `12` và dãy tiền tố là `A,B`, tool sẽ đổi tên 12 file đầu tiên thành `A (1)`, `A (2)`...`A (12)`, sau đó sẽ chuyển sang dùng tiền tố `B` cho 12 file tiếp theo.

  * **Chỉ đổi tên file loại**: Bộ lọc giúp bạn chỉ xử lý những định dạng file mong muốn.

      * **Cách sử dụng**: Nhập các đuôi file, phân cách bằng **dấu cách**. Dấu chấm `.` ở đầu là tùy chọn.
      * **Ví dụ**: `.jpg .png .jpeg` hoặc `jpg png jpeg` đều hợp lệ.
      * **Lưu ý**: Để trống ô này nếu bạn muốn đổi tên tất cả các file trong thư mục.

  * **Dãy tên tiền tố**: Đây là phần quan trọng nhất, quyết định tên mới của file.

      * **Quy tắc**: Nhập các tiền tố bạn muốn sử dụng, phân cách chúng bằng **dấu phẩy (,)**. Tool sẽ tự động loại bỏ các khoảng trắng thừa.
      * **Ví dụ 1 (Kiểu ký tự đơn)**: Để đổi tên file thành `A (1)`, `B (1)`... bạn nhập:
        ```
        A,B,C,D,E
        ```
      * **Ví dụ 2 (Kiểu cụm từ dài)**: Để đổi tên file thành `Summer_Trip (1)`, `Food_Photos (1)`... bạn nhập:
        ```
        Summer_Trip, Food_Photos
        ```

### ➌ Khu vực 3: Thực thi và Theo dõi

  * **Nút "Bắt đầu đổi tên"**: Sau khi đã thiết lập xong các tùy chọn, nhấn nút này để bắt đầu quá trình. Nút sẽ bị vô hiệu hóa và hiển thị "Đang xử lý..." trong khi tool hoạt động.
  * **Vùng Log**: Khung văn bản lớn ở dưới cùng sẽ hiển thị chi tiết tiến trình trong thời gian thực.
      * `✅ Đổi:`: Thông báo một file đã được đổi tên thành công.
      * `⚠️ Lỗi file:`: Thông báo một file cụ thể gặp lỗi và không thể đổi tên.
      * `❌ Lỗi nghiêm trọng`: Thông báo các lỗi lớn hơn như không tìm thấy thư mục.
      * `🎉 TẤT CẢ HOÀN TẤT!`: Thông báo cuối cùng kèm tổng kết số file đã được đổi tên.

-----

## Ví dụ quy trình làm việc

**Tình huống**: Bạn có 2 thư mục ảnh, một thư mục chứa ảnh render sản phẩm và một thư mục chứa ảnh hậu trường. Bạn muốn đổi tên tất cả các file `.png` và `.jpg` theo thứ tự thời gian chúng được tạo.

1.  **Dán đường dẫn**:
    ```
    C:\DuAn\HinhRender
    C:\DuAn\HinhHauTruong
    ```
2.  **Chọn tùy chọn**:
      * **Sắp xếp theo**: `Thời gian tạo`
      * **Số file mỗi tiền tố**: `50` (Giả sử mỗi thư mục có khoảng 50 ảnh)
      * **Chỉ đổi tên file loại**: `png jpg`
      * **Dãy tên tiền tố**: `Render_Product, Behind_The_Scenes`
3.  **Bắt đầu**: Nhấn nút **"Bắt đầu đổi tên"**.
4.  **Theo dõi**: Vùng log sẽ hiển thị quá trình xử lý thư mục `HinhRender` trước, đổi tên các file thành `Render_Product (1).png`, `Render_Product (2).jpg`... Sau khi xong, nó sẽ tự động chuyển qua thư mục `HinhHauTruong` và đổi tên các file thành `Behind_The_Scenes (1).jpg`...

## Tác giả

Tool được tạo bởi **Duck Martians**.
