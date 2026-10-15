# Ghi chú đóng gói

Ngày đóng gói: 15/10/2026. Nguồn là các file đã lưu của project BOARD_ADS. Không thay đổi thiết kế điện, vị trí linh kiện, route hoặc nội dung thư viện.

## Nội dung đã kiểm tra

- Tính toàn vẹn file nguồn và bản sao bằng SHA-256.
- 48 linh kiện schematic và 48 linh kiện trên PCB chính.
- Tham chiếu tài liệu trong bản sao project đều trỏ tới file đi kèm.
- Tên footprint được schematic/PCB sử dụng so với các mục trong PcbLib đi kèm. Đây là kiểm tra tên, chưa xác nhận hình học footprint.
- PDF nguồn có 1 trang, thời điểm tạo theo metadata: 2026-10-15 08:54:03+07:00.

## Thư viện và phần còn mở

- Footprint XH2.54M-3 của H3 có trên PCB đã đặt nhưng không tìm thấy trong BOARD_ADS.PcbLib. Cần bổ sung thư viện nguồn đúng footprint trước khi cập nhật từ thư viện.
- Schematic còn tham chiếu lịch sử Altium_Lib_by_KhueNguyenCreator.IntLib; thư viện ngoài này chưa tìm thấy trong các vị trí đã kiểm tra. Gói chỉ chứa thư viện nguồn hiện có, không tự thay thế model.
- C1–C29 có Case/Package = 0402 nhưng model schematic là C0805L; giữ nguyên và ghi rõ trong BOM.
- PCB1.PcbDoc là tài liệu bổ sung của project, đọc được 0 linh kiện; giữ nguyên để tránh bỏ tài liệu nguồn.
- PDF nguồn được tạo trước lần lưu schematic gần nhất trong cùng ngày; cần xuất lại sau khi chốt thiết kế. Title/Revision/Drawn By trên PDF chưa điền đầy đủ.

## Phạm vi kiểm tra

Chưa mở/compile bản đóng gói trong Altium, chưa chạy lại ERC/DRC và chưa thử phần cứng. Các báo cáo cũ trong thư mục output không dùng làm bằng chứng bản hiện tại đã đạt. Danh sách linh kiện được tạo để tham khảo; nhiều thông số mua hàng còn thiếu.

Gói không kèm cache, History, log, báo cáo output cũ, Gerber/CPL chưa xác nhận hoặc firmware chưa có. Metadata nguồn thư viện được giữ nguyên; các ghi chú bản quyền của linh kiện/thư viện ngoài không được thay đổi. Chưa gán giấy phép sử dụng mới cho toàn bộ thiết kế.
