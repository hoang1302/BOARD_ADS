# Trạng thái kiểm tra V2.0

Ngày đóng gói: 25/10/2026. Người thiết kế cho biết đã hoàn thiện V2. Hoàn tất thiết kế không được đồng nhất với đã thử nghiệm board thật.

| Nội dung | Trạng thái / bằng chứng |
| --- | --- |
| Bản sao schematic, PCB, SchLib, PcbLib và thư viện Header | So sánh SHA-256 với file đã lưu; giữ nguyên byte |
| Project đóng gói | Đường dẫn tài liệu tương đối; bỏ tham chiếu GeneratedDocument; thêm thư viện Header |
| Designator schematic / PCB | 49 / 49, tập designator trùng nhau; chưa xác nhận kết nối điện |
| Tên symbol / footprint đang đặt | Tìm thấy tên trong bộ thư viện đi kèm; chưa xác nhận hình học hoặc model schematic khớp PCB |
| Compile, ERC, ECO và DRC bản 25/10 | Chưa chạy trong lần đóng gói; kết nối Altium hiện không phản hồi |
| Gerber đang có | ZIP ngày 22/10, cũ hơn PCB đã lưu ngày 25/10; lưu trong archive, không xác nhận dùng đặt mạch |
| PDF và ảnh đang có | PDF/ảnh ngày 19–22/10; có nhãn ngày, cần xuất lại để đại diện bản cuối |
| Lắp ráp, đo nguồn, SPI và chất lượng tín hiệu | Chưa có kết quả thực nghiệm được cung cấp trong gói |

## Trước khi phát hành dữ liệu đặt mạch

1. Mở project từ bản clone và xác nhận đúng tài liệu, symbol, model và footprint. Xem các trường BOM còn chưa khớp.
2. Lưu nguồn, compile/ERC, đối chiếu schematic–PCB và chạy DRC trên đúng PCB này. Lưu báo cáo cùng revision.
3. Xuất lại PDF, Gerber và NC Drill từ bản nguồn đã chốt. Kiểm tra outline, lớp đồng/mask/silk, lỗ PTH/NPTH và định hướng qua CAM viewer.
4. Thay bộ archive bằng gói mới có ngày, mã SHA-256 và commit nguồn. Chỉ sau bước này mới mô tả Release là gói dùng đặt mạch.
5. Khi có board thật, bổ sung ngày lắp ráp, cấu hình module, nguồn/tải, thiết bị đo và kết quả nguồn/SPI/tín hiệu.

Các báo cáo review ngày 21–22/10 là lịch sử, không dùng để kết luận bản nguồn ngày 25/10 đã PASS. Việc đóng gói không thay đổi thiết kế điện hoặc cơ khí và không chứng nhận mức độ an toàn của hệ thống điện cực.
