# BOARD_ADS — board kết nối ADS1299

Board kết nối module ADS1299 với kit xử lý, kèm khối nguồn và connector cho điện cực ngoài. Repository lưu cả bản nguồn V1 và V2.

**Phiên bản hiện tại: Hardware V2.0 — đóng gói nguồn ngày 25/10/2026.** Người thiết kế cho biết đã hoàn thiện thiết kế. Chưa bổ sung kết quả kiểm thử board thật; PDF và Gerber có sẵn chưa được xác nhận khớp nguồn mới nhất.

## Chọn phiên bản

| Phiên bản | Nguồn Altium | Tài liệu | Trạng thái |
| --- | --- | --- | --- |
| **V2.0** | [Mở thư mục project](hardware/v2.0/altium/) | [Hướng dẫn V2](hardware/v2.0/README.md) | Nguồn mới nhất; đầu ra chế tạo cần cập nhật |
| V1 | [Project V1](hardware/altium/BOARD_ADS.PrjPcb) | [README V1 lưu trữ](docs/README_V1.md) | Prototype đóng gói ngày 15/10/2026 |

## Mở bản V2

1. Clone hoặc tải toàn bộ repository.
2. Mở [BOARD_ADS _V2.0 (1).PrjPcb](hardware/v2.0/altium/BOARD_ADS%20_V2.0%20(1).PrjPcb) trong Altium Designer.
3. Giữ nguyên tên file và thư mục thư viện đi kèm; kiểm tra compile và liên kết model khi mở trên máy khác.

Chỉ cắm **ESP32 hoặc nRF52840** tại một thời điểm. Bảng pinout dùng số pad của PCB; cần đối chiếu đúng model và chiều module trước khi đấu dây.

## Tài liệu V2

- [BOM tham khảo](hardware/v2.0/docs/BOM.md) và [CSV](hardware/v2.0/docs/BOM.csv).
- [Pinout bản hiện tại](hardware/v2.0/docs/PINOUT.md).
- [Trạng thái kiểm tra và các bước chốt sản xuất](hardware/v2.0/docs/VALIDATION.md).
- [Ghi chú thư viện và đóng gói](hardware/v2.0/docs/PACKAGE_NOTES.md).
- [Tài liệu và ảnh tham khảo](hardware/v2.0/docs/README.md).
- [Dữ liệu chế tạo hiện có](hardware/v2.0/manufacturing/README.md).
- [Lịch sử thay đổi](CHANGELOG.md).

**Gerber hiện có được xuất ngày 22/10, trước PCB nguồn ngày 25/10.** ZIP được lưu trong archive để truy vết; chưa xác nhận là bộ đặt mạch của bản nguồn hiện tại. Xem trạng thái kiểm tra trước khi tải dữ liệu chế tạo.

Các file V1 trong `hardware/altium/`, `hardware/bom/`, `hardware/schematic/`, `docs/HARDWARE.md`, `docs/VALIDATION.md`, `docs/PACKAGE_NOTES.md` và `images/` được giữ làm tài liệu lịch sử. Không áp dụng pinout hoặc lỗi của V1 mặc định cho V2.
