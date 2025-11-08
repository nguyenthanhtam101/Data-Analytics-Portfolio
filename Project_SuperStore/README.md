📈 Dự án: Phân tích Doanh số & Lợi nhuận Global Superstore
Đây là một dự án phân tích dữ liệu trọn vẹn (end-to-end), thực hiện quy trình từ làm sạch dữ liệu thô, phân tích, và trực quan hóa để tìm ra các xu hướng kinh doanh quan trọng.

1. Mục tiêu (Ask)
Mục tiêu của dự án là trả lời các câu hỏi kinh doanh chính từ Ban Giám đốc:

Tình hình tăng trưởng doanh thu và lợi nhuận theo thời gian?

Khu vực (Market) và Phân khúc khách hàng (Segment) nào đang hoạt động hiệu quả nhất?

Những danh mục sản phẩm (Category) nào đang mang lại lợi nhuận cao nhất và sản phẩm nào đang bán lỗ?

2. Chuẩn bị & Xử lý (Prepare & Process)
Công cụ: Python (thư viện Pandas).

Quá trình:

Dữ liệu ban đầu (lấy từ Kaggle) gồm 51,290 dòng.

Phát hiện và xử lý:

Chuyển đổi cột Order Date và Ship Date từ kiểu 'object' sang 'datetime'.

Xử lý các giá trị số liệu (nếu có).

Tạo các cột tính toán mới (Feature Engineering) như Profit Margin (Biên lợi nhuận) và Processing Time (Thời gian xử lý đơn) để làm giàu thêm dữ liệu.

Dữ liệu sạch được xuất ra file Superstore_Cleaned.csv để chuẩn bị cho bước phân tích.

3. Phân tích (Analyze)
Công cụ: SQLite (để lưu trữ) và SQL (để truy vấn).

Các câu truy vấn chính được sử dụng để khám phá dữ liệu, ví dụ:

Tìm Top 5 thị trường có lợi nhuận cao nhất (GROUP BY Market, ORDER BY TotalProfit).

Phân tích các sản phẩm con (Sub-Category) đang bán lỗ (HAVING SUM(Profit) < 0).

Tính tổng doanh thu theo từng phân khúc khách hàng (GROUP BY Segment).

4. Trình bày (Share)
Công cụ: Power BI.

Xây dựng một dashboard tương tác để trình bày các kết quả phân tích.

Các chức năng chính của Dashboard:

Các thẻ (Cards) hiển thị 3 chỉ số KPI chính: Tổng Doanh thu, Tổng Lợi nhuận, Biên lợi nhuận trung bình.

Biểu đồ đường (Line chart) thể hiện xu hướng Doanh thu/Lợi nhuận theo thời gian.

Biểu đồ cột (Bar chart) cho thấy Top 5 thị trường lợi nhuận cao nhất.

Biểu đồ tròn (Donut chart) thể hiện tỷ trọng doanh thu theo Phân khúc khách hàng.

Biểu đồ bản đồ (Filled Map) tô màu lợi nhuận theo từng quốc gia.

Dashboard có 2 bộ lọc (Slicers) tương tác: Lọc theo Khu vực (Region) và Lọc theo Ngày (Order Date).

5. Công cụ sử dụng
Python (Pandas): Để làm sạch và chuẩn bị dữ liệu.

SQL (SQLite): Để lưu trữ và truy vấn phân tích.

Power BI: Để xây dựng dashboard trực quan hóa tương tác.
