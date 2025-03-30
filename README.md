Đây là dự án phân tích dữ liệu doanh số bán hàng sử dụng Python, Pandas và Matplotlib. Dự án tập trung vào việc xử lý dữ liệu từ các file CSV của năm 2019 và xây dựng báo cáo thông qua các task cụ thể.

Dự án này thực hiện phân tích dữ liệu bán hàng của ZoneTech (Mỹ) được tổng hợp thành 12 file csv với hơn 20000 dòng dữ liệu với 7 cột dữ  trên KAGGLE tói hơn với mục đích:

Tổng hợp dữ liệu từ 12 file CSV của năm 2019.

Tiền xử lý dữ liệu (loại bỏ giá trị không hợp lệ, chuyển đổi kiểu dữ liệu,...).

Tính toán doanh số theo tháng và xác định tháng có doanh số cao nhất.

Visual hóa kết quả bằng các biểu đồ.

![image](https://github.com/user-attachments/assets/8525f4bb-7112-46b4-a266-b9bf0f828d63)

Dòng code trên sẽ đọc file sales2019_5.csv từ thư mục chỉ định và hiển thị 10 dòng đầu tiên của dữ liệu.

Task 2.1 : gôp tất cả dữ liệu của 12 file csv thành một file dữ liệu csv duy nhất 

Gán filepath bằng đường dẫn tệp CSV.

Đọc tệp CSV vào df1.

Thêm df1 vào danh sách frames.

Gộp tất cả các DataFrame trong frames thành result.

Lấy số dòng của df1 và lưu vào all_length.

Gán result vào df để chứa toàn bộ dữ liệu từ các tệp CSV.

![image](https://github.com/user-attachments/assets/56b02d28-0d7b-4321-b9b9-5a54200998d4)

Đọc từng file CSV từ thư mục và loại bỏ những dòng có tiêu đề lặp lại.

Gộp các DataFrame thành một DataFrame duy nhất và lưu vào file Sales2019_Clean.csv.

![image](https://github.com/user-attachments/assets/b47d13f0-7fbd-4f94-bc13-1c7fb2f03a16)
![image](https://github.com/user-attachments/assets/c4c91275-cd90-4f8f-b2d6-9f9aaf73b3fe)



