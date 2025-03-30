Đây là dự án phân tích dữ liệu doanh số bán hàng sử dụng Python, Pandas và Matplotlib. Dự án tập trung vào việc xử lý dữ liệu từ các file CSV của năm 2019 và xây dựng báo cáo thông qua các task cụ thể.
![image](https://github.com/user-attachments/assets/7b4287c1-249b-4bfd-a28f-784375ec9253)

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

Dữ liệu được phân tích bao gồm doanh thu (Sales) và số đơn hàng (Orders) theo từng tháng trong năm.
Doanh thu được tính bằng công thức:
df['Sales'] = df['Quantity Ordered'] * df['Price Each']
Sau đó, doanh thu được tổng hợp theo tháng bằng groupby('Month')['Sales'].sum().

Số đơn hàng được tính bằng value_counts() của cột 'Month' và sắp xếp theo thứ tự tháng
![image](https://github.com/user-attachments/assets/cdfe9040-6de6-4dc7-a07e-e879a54913d6)
![image](https://github.com/user-attachments/assets/c179737f-6ee5-4779-a308-b82690d0cf6d)


Kết quả nổi bật
Tháng có doanh thu cao nhất: Tháng 12 với doanh thu đạt 4,613,443.5 USD. Điều này cho thấy tháng 12 là tháng kinh doanh hiệu quả nhất trong năm, có thể do ảnh hưởng của mùa mua sắm cuối năm (ví dụ: Giáng sinh, năm mới).

Biểu đồ doanh thu theo tháng:

Dạng biểu đồ: Cột (bar chart).

Xu hướng: Doanh thu có xu hướng tăng dần từ đầu năm đến cuối năm, với đỉnh điểm vào tháng 12. Các tháng giữa năm (như tháng 6, 7, 8) cũng có doanh thu khá ổn định.

Biểu đồ số đơn hàng theo tháng:

Dạng biểu đồ: Đường (line chart) với điểm đánh dấu (marker).

Xu hướng: Số đơn hàng dao động nhưng không có sự tăng trưởng rõ rệt như doanh thu. Điều này cho thấy giá trị trung bình mỗi đơn hàng (Average Order Value - AOV) có thể tăng vào các tháng cuối năm, đặc biệt là tháng 12.
Tháng 12 là tháng đạt doanh thu cao nhất, nhưng số đơn hàng không tăng đột biến, cho thấy giá trị trung bình mỗi đơn hàng cao.

Xu hướng doanh thu tăng dần vào cuối năm, phù hợp với đặc điểm mùa vụ.

Cần phân tích thêm để hiểu rõ nguyên nhân và tối ưu hóa chiến lược kinh doanh cho các tháng khác trong năm.
![image](https://github.com/user-attachments/assets/3aa1f0a6-952b-4231-a55e-f8b4912ebfaf)
![image](https://github.com/user-attachments/assets/e8b680fb-f824-4f7f-965d-dd92a6d4cd30)
Thành phố có doanh thu cao nhất: San Francisco với tổng doanh thu đạt 8,262,294.0 USD. Điều này cho thấy San Francisco là thị trường mạnh nhất trong dataset.

Biểu đồ doanh thu theo thành phố:

Dạng biểu đồ: Cột (bar chart), với thành phố có doanh thu cao nhất (San Francisco) được tô màu đỏ để nổi bật.


Các thành phố lớn như New York City, Los Angeles, và Boston cũng có doanh thu cao, nhưng thấp hơn đáng kể so với San Francisco.

Các thành phố như Austin, Atlanta, và Portland có doanh thu thấp hơn nhiều.

Nguyên nhân San Francisco dẫn đầu:

Mật độ dân số và thu nhập cao: San Francisco là trung tâm công nghệ với nhiều cư dân có thu nhập cao, dẫn đến khả năng chi tiêu lớn.

Hoạt động thương mại sôi động: Thành phố này có nhiều cửa hàng, trung tâm mua sắm hoặc đơn vị phân phối lớn.

Chiến dịch marketing hiệu quả: Các chương trình khuyến mãi hoặc ưu đãi đặc biệt có thể được triển khai mạnh ở đây.

![image](https://github.com/user-attachments/assets/fd9cddf2-48b8-4b8e-b8dd-0a6791f06983)
![image](https://github.com/user-attachments/assets/a73cd67a-c7fb-47de-b3c7-8be045609feb)
![image](https://github.com/user-attachments/assets/6450c887-fc27-4e05-9f69-85d6f2ee9ff0)

3. Nhận xét chi tiết
Tại sao 19h là khung giờ lý tưởng?

Thời gian rảnh rỗi: 19h là thời điểm sau giờ làm việc, khách hàng có xu hướng mua sắm hoặc xem quảng cáo.

Hiệu ứng buổi tối: Nhu cầu mua sắm trực tuyến thường tăng vào buổi tối khi người dùng có nhiều thời gian cá nhân.

Chiến dịch khuyến mãi: Các chương trình giảm giá "flash sale" thường được triển khai vào buổi tối để thu hút khách hàng.

Các khung giờ tiềm năng khác:

11h-12h (trưa): Thời gian nghỉ trưa, khách hàng có thể duyệt web hoặc mua sắm nhanh.

16h-17h (chiều): Kết thúc giờ làm việc, khách hàng có xu hướng kiểm tra email hoặc mạng xã hội.

Khung giờ ít hiệu quả:

2h-6h (đêm và sáng sớm): Doanh thu và số đơn hàng thấp nhất do khách hàng đang ngủ hoặc ít hoạt động.

4. Đề xuất chiến lược quảng cáo
Tập trung ngân sách quảng cáo vào khung giờ 18h-20h:

Chạy quảng cáo trên các nền tảng như Facebook, Google Ads, TikTok vào thời điểm này để tận dụng lượng khách hàng cao nhất.

Ưu tiên quảng cáo sản phẩm có giá trị cao hoặc combo khuyến mãi.

Tăng cường quảng cáo vào giờ trưa (11h-12h):

Phù hợp với khách hàng văn phòng hoặc người dùng di động trong giờ nghỉ.

Hạn chế quảng cáo từ 2h-6h:

Có thể dừng hoặc giảm ngân sách quảng cáo trong khung giờ này để tiết kiệm chi phí.

![image](https://github.com/user-attachments/assets/eb8d5e30-be06-4c54-88e9-6f503d024bbd)
![image](https://github.com/user-attachments/assets/12a837bc-a6d8-4b34-81c1-4a772f0c0542)
![image](https://github.com/user-attachments/assets/21672e46-7d00-4138-978c-26b2a9a79e2c)
![image](https://github.com/user-attachments/assets/4c3362c1-bc1c-4645-bc99-bfec37f4fa6f)
![image](https://github.com/user-attachments/assets/0f3d86c6-e7cf-4129-88d2-47cf45042f83)
![image](https://github.com/user-attachments/assets/18cefcd2-5f83-4ded-aa2f-becdb2d1071a)


Tại sao AAA Batteries bán chạy nhất?
Giá thấp, nhu cầu phổ biến: Pin là mặt hàng thiết yếu, dễ mua nhiều lần.

Khối lượng bán theo gói: 4-pack tăng số lượng trên mỗi đơn hàng.

Khả năng mua kèm: Thường được thêm vào giỏ hàng như sản phẩm phụ.

b. Tại sao Macbook Pro có doanh thu cao nhất?
Giá trị đơn vị cao: Dù số lượng bán ít, nhưng giá mỗi chiếc (~1,200 USD) đóng góp lớn vào doanh thu.

Nhóm khách hàng mục tiêu: Doanh nghiệp hoặc người dùng cao cấp sẵn sàng chi trả.

c. Mâu thuẫn giữa số lượng và doanh thu
Sản phẩm bán chạy ≠ Doanh thu cao:

AAA Batteries bán nhiều nhưng doanh thu thấp (~3 USD/gói).

Macbook Pro bán ít nhưng doanh thu khổng lồ.

Chiến lược cân đối:

Duy trì cả 2 nhóm: Sản phẩm giá rẻ (tăng lượng khách) và giá cao (tăng lợi nhuận).


![image](https://github.com/user-attachments/assets/ebf8be22-8eee-4486-871d-e66cd93b7396)

![image](https://github.com/user-attachments/assets/00daa0a3-8933-410f-8881-bdafad559fc6)
![image](https://github.com/user-attachments/assets/8831baf5-8aec-4423-bc42-f114824b2551)
![image](https://github.com/user-attachments/assets/bba7929a-9523-4c0b-93e4-e240f2cfd663)
![image](https://github.com/user-attachments/assets/2c8abe0b-f3b7-4692-ab14-953f58362552)

Tại sao San Francisco dẫn đầu?
Trung tâm công nghệ: Dân cư có thu nhập cao, nhu cầu mua sắm lớn (điện tử, phụ kiện).

Hoạt động thương mại sôi động: Nhiều cửa hàng trực tuyến hoặc vật lý tập trung tại đây.

Chiến dịch marketing hiệu quả: Ưu đãi địa phương hoặc giao hàng nhanh.

b. Sự chênh lệch giữa các thành phố
Thành phố lớn vs. nhỏ:

SF, LA, NYC chiếm tổng cộng 53.4% đơn hàng → Tập trung kinh tế.

Austin, Portland dưới 6% → Cần phân tích thêm về nhân khẩu học hoặc hạ tầng logistics.

Khác biệt theo vùng:

Miền Tây (SF, LA) chiếm 40%, trong khi miền Đông (NYC, Boston) chỉ 24.1%.

c. Cơ hội cải thiện
Tăng thị phần tại thành phố nhỏ:

Ưu đãi vận chuyển hoặc khuyến mãi đặc biệt cho Austin, Dallas.

Tối ưu hóa tại thành phố lớn:

Mở rộng kho hàng ở SF/LA để giảm thời gian giao hàng.
![image](https://github.com/user-attachments/assets/297a82b6-86fc-4565-9442-661509b1121e)
![image](https://github.com/user-attachments/assets/50647fc0-2926-41ea-9f41-66e318a9b17d)
![image](https://github.com/user-attachments/assets/c7327472-efc7-491d-9834-5d8e9f807c47)

Sản phẩm bán ít nhất xuất hiện nhiều lần:

"Minimize Machine": Bán chỉ 2 đơn/tháng (Tháng 1 và 2).

Các sản phẩm khác: Mỗi tháng có một sản phẩm khác nhau nằm ở vị trí cuối.

Xu hướng chung:

Sản phẩm bán chậm thường là hàng chuyên dụng hoặc giá cao (ví dụ: máy móc công nghiệp).

Không có sản phẩm phổ thông (pin, cáp sạc) trong danh sách này.

4. Nhận xét chi tiết
a. Nguyên nhân bán chậm
Nhu cầu thị trường thấp:

"Minimize Machine" có thể là sản phẩm ngách, chỉ phục vụ nhóm khách hàng đặc thù.

Giá cả không hợp lý:

Sản phẩm giá cao nhưng không đủ giá trị gia tăng để thuyết phục khách hàng.

Thiếu tiếp cận khách hàng:

Không được quảng cáo đúng đối tượng hoặc hiển thị kém trên website.

b. Gợi ý cải thiện
Với sản phẩm ngách (ví dụ: Minimize Machine):

Bundle với sản phẩm phổ biến: Giảm giá khi mua kèm với sản phẩm bán chạy.

Target marketing: Quảng cáo đến đúng nhóm khách hàng doanh nghiệp hoặc kỹ thuật.

Với sản phẩm theo mùa:

Điều chỉnh chiến dịch quảng cáo theo thời điểm (ví dụ: máy móc nông nghiệp bán vào mùa vụ).
