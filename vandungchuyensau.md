BƯỚC 1: THIẾT KẾ GIẢI PHÁP (I/O)
Input (Đầu vào):
[THONG_TIN_KHACH_HANG]: Tên và số điện thoại khách.
[TEN_SAN_PHAM] & [NGAY_MUA]: Tên sản phẩm và thời gian mua hàng.
[NOI_DUNG_KHIEU_NAI]: Mô tả lỗi từ khách hàng.
Output (Đầu ra):
Trạng thái bảo hành (Còn hạn / Hết hạn) kết hợp suy luận Chain-of-Thought (CoT).
Khối kết quả đóng gói chuẩn [KẾT_QUẢ_PHÂN_TÍCH] để làm Data Handoff sang trạm tiếp theo.
BƯỚC 2: VIẾT PROMPT VÀ CHẠY THỬ
1. Prompt hoàn chỉnh
Plaintext
Tải mã xuống
Sao chép mã
Bạn là Trợ lý CSKH tự động. Hãy xử lý yêu cầu bảo hành theo các bước sau:
BƯỚC 1 (Xử lý lỗi): Kiểm tra dữ liệu [THONG_TIN_KHACH_HANG], [TEN_SAN_PHAM], [NGAY_MUA], [NOI_DUNG_KHIEU_NAI]. NẾU thiếu, xuất: [LỖI_DỮ_LIỆU: Thiếu thông tin].
BƯỚC 2 (CoT): Tính thời gian từ [NGAY_MUA] đến nay để xem còn trong hạn 12 tháng không và phân tích lỗi.
BƯỚC 3 (Data Handoff): Xuất kết quả theo định dạng:
[KẾT_QUẢ_PHÂN_TÍCH]
- Khách hàng: [...]
- Sản phẩm: [...]
- Trạng thái bảo hành: [...]
- Hướng xử lý: [...]
[END_HANDOFF]

Dữ liệu đầu vào:
- [THONG_TIN_KHACH_HANG]: Nguyễn Văn An (SĐT: 0987654321)
- [TEN_SAN_PHAM]: Tai nghe Bluetooth X-Pro
- [NGAY_MUA]: 15/05/2025
- [NOI_DUNG_KHIEU_NAI]: Hỏng một bên tai trái sau 4 tháng, vỏ máy không trầy xước.
2. Kết quả phản hồi từ AI (Test Run)
Plaintext
Tải mã xuống
Sao chép mã
[KẾT_QUẢ_PHÂN_TÍCH]
- Khách hàng: Nguyễn Văn An (SĐT: 0987654321)
- Sản phẩm: Tai nghe Bluetooth X-Pro
- Trạng thái bảo hành: Hết hạn bảo hành miễn phí (Đã qua 18 tháng)
- Hướng xử lý: Hỗ trợ sửa chữa dịch vụ ưu đãi (Giảm 50% linh kiện)
[END_HANDOFF]
Câu trả lời tốt
Câu trả lời không tốt
Khôi phục
Sao chép
Hiện thêm tuỳ chọn
