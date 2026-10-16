Phần 1. Phân tích bài toán (Cơ chế Token)Tokenization & Độ dài: HTML chứa thẻ rườm rà (<strong>...</strong> -> 25 ký tự, nhiều token) tốn gấp 2–3 lần Markdown (**...** -> 12 ký tự, ít token).
Vì sao Markdown giúp AI nhanh hơn?
Giảm Latency: AI sinh văn bản theo từng token. Ít token hơn -> AI sinh xong câu trả lời nhanh hơn.
Tiết kiệm chi phí: Cắt giảm 30%–50% chi phí API Token cho hệ thống.
Tối ưu Context Window: Dành thêm không gian chứa thông tin tư vấn nông nghiệp thay vì chứa cú pháp mã.
Phần 2. So sánh & Đánh giá giải pháp GreenTech1.
Markdown
Số ký tự & Token:	Tối giản, tiêu tốn rất ít token
Human-readable:	Rất cao, đọc trực tiếp dạng text thô vẫn dễ dàng
Hiệu suất AI:	Nhanh, ổn định, hiếm khi lỗi cú pháp
HTML
Số ký tự & Token: Cồng kềnh, tốn nhiều token cho các thẻ mở/đóng.
Human-readable: Thấp, mã thô bị nhiễu do dày đặc thẻ tag
Hiệu suất AI: Chậm hơn, dễ gặp lỗi AI quên đóng thẻ tag
2. Giải pháp cho GreenTech
Lựa chọn: Sử dụng Markdown.
Lý do:
Nhanh & Nhẹ: Truyền tải mượt mà qua mạng 3G/4G trên đồng ruộng, câu trả lời hiển thị tức thì.
Dễ đọc: Nông dân đọc hiểu tốt ngay cả khi ứng dụng không render giao diện (dạng text thô).
Tối ưu vận hành: Giảm chi phí API và tránh lỗi vỡ giao diện hệ thống.
| Tiêu chí so sánh | Markdown (`.md`) | HTML (`.html`) |
| :--- | :--- | :--- |
| **Cú pháp định dạng** <br>*(Ví dụ in đậm)* | `**Bón phân đúng liều lượng**`<br>*(4 ký tự định dạng)* | `<strong>Bón phân đúng liều lượng</strong>`<br>*(17 ký tự định dạng)* |
| **Hiệu quả tiêu thụ Token** | **Tối ưu:** Tiết kiệm từ 30% đến 50% số lượng token cho cùng một nội dung. | **Lãng phí:** Các thẻ đóng/mở (`<div>`, `<p>`, `<span>`) chiếm dung lượng token lớn. |
| **Độ dễ đọc cho con người** <br>*(Human-readable)* | **Rất cao:** Văn bản thô trực quan, người nông dân hoặc kỹ sư có thể đọc ngay cả khi chưa qua render. | **Thấp:** Bị nhiễu bởi vô số thẻ lệnh đóng mở, gây rối mắt cho người đọc trực tiếp. |
| **Khả năng hiển thị đa nền tảng** | Dễ dàng chuyển đổi (Render) sang HTML, PDF, hoặc hiển thị mượt mà trên App mobile/Zalo/SMS. | Bắt buộc phải có trình duyệt hoặc WebView để hiển thị đúng định dạng đồ họa. |
