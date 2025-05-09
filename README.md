Dự án Chấm Thi Trắc Nghiệm Tự Động
Tổng quan
Dự án này triển khai một ứng dụng để tự động chấm bài thi trắc nghiệm từ hình ảnh phiếu trả lời. Ứng dụng sử dụng xử lý ảnh với OpenCV để nhận diện các ô được tô, xác định mã đề thi, số báo danh và tính điểm dựa trên đáp án đúng. Kết quả được hiển thị trên giao diện đồ họa (GUI) và lưu vào file CSV.

Tính năng
Nhận diện ô tô: Phát hiện các ô được tô trên phiếu trả lời bằng kỹ thuật xử lý ảnh.
Xác định mã đề và số báo danh: Đọc mã đề thi (6 chữ số) và số báo danh (3 chữ số) từ các ô được tô.
Chấm điểm: So sánh câu trả lời với đáp án đúng (4 bộ đáp án được định nghĩa sẵn) và tính điểm trên thang 10.
Hiển thị kết quả: Hiển thị điểm, mã đề, số báo danh trên GUI và hình ảnh phiếu trả lời với các ô được đánh dấu.
Lưu kết quả: Lưu điểm, mã đề, số báo danh vào file exam_results.csv.
Giao diện người dùng: Sử dụng Tkinter để chọn hình ảnh và hiển thị kết quả.
Bộ dữ liệu
Đầu vào: Hình ảnh phiếu trả lời trắc nghiệm (định dạng .jpg hoặc .png).
Cấu trúc phiếu trả lời:
120 câu hỏi trắc nghiệm, chia thành 4 cột (mỗi cột 30 câu).
Mỗi câu có 4 lựa chọn (A, B, C, D).
Khu vực mã đề thi (6 cột, mỗi cột 10 ô từ 0-9).
Khu vực số báo danh (3 cột, mỗi cột 10 ô từ 0-9).
Đáp án: 4 bộ đáp án (ANSWER_KEY_1, ANSWER_KEY_2, ANSWER_KEY_3, ANSWER_KEY_4) được định nghĩa sẵn cho 120 câu.
Yêu cầu
Để chạy dự án, cài đặt các gói Python sau:

bash

Sao chép
pip install opencv-python matplotlib imutils numpy pillow
Lưu ý: Đảm bảo Python đã được cài đặt Tkinter (thường có sẵn trong Python).

Cài đặt
Tải repository hoặc các file dự án.
Cài đặt các gói phụ thuộc được liệt kê ở phần Yêu cầu.
Đảm bảo file A39948.py và các hình ảnh phiếu trả lời nằm trong cùng thư mục.
Hướng dẫn sử dụng
Chạy file A39948.py:
bash

Sao chép
python A39948.py
Một cửa sổ GUI sẽ hiện ra với nút "Mở ảnh".
Nhấn nút "Mở ảnh", chọn file hình ảnh phiếu trả lời (.jpg hoặc .png).
Ứng dụng sẽ:
Xử lý hình ảnh, nhận diện các ô được tô.
Xác định mã đề thi và số báo danh.
Tính điểm dựa trên đáp án đúng.
Hiển thị kết quả (điểm, mã đề, số báo danh) trên GUI.
Hiển thị hình ảnh gốc và hình ảnh phiếu trả lời với các ô được đánh dấu (đúng: xanh, sai: đỏ).
Lưu kết quả vào file exam_results.csv.
Kết quả đầu ra
Trên GUI: Hiển thị điểm (thang 10), mã đề thi (6 chữ số), số báo danh (3 chữ số).
Hình ảnh: Hiển thị phiếu trả lời với các ô được đánh dấu:
Đáp án đúng: Viền xanh.
Đáp án sai: Viền đỏ.
File CSV (exam_results.csv): Lưu thông tin:
Điểm
Số báo danh
Mã đề thi
File liên quan
A39948.py: File mã nguồn chính.
exam_results.csv: File lưu kết quả chấm thi (tạo tự động khi chạy).
Cải tiến trong tương lai
Cải thiện độ chính xác khi nhận diện ô tô trong điều kiện ánh sáng kém.
Hỗ trợ nhiều định dạng phiếu trả lời hơn.
Thêm tính năng chỉnh sửa đáp án trực tiếp trên GUI.
Tích hợp cơ sở dữ liệu để quản lý kết quả thi.