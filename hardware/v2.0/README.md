# BOARD_ADS — Hardware V2.0

Board kết nối module ADS1299 với ESP32 hoặc nRF52840, kèm khối nguồn cho điện cực ngoài. Chỉ cắm một trong hai bộ xử lý tại một thời điểm.

**Trạng thái: bản nguồn V2 đã được người thiết kế hoàn thiện; gói GitHub ngày 25/10/2026. Chưa có bằng chứng kiểm thử phần cứng hoặc bộ Gerber được xác nhận khớp revision nguồn này trong lần đóng gói.**

## Mở project

Mở [BOARD_ADS _V2.0 (1).PrjPcb](altium/BOARD_ADS%20_V2.0%20(1).PrjPcb). PCB chính là [BOARD_ADS _V2.0 (3).PcbDoc](altium/BOARD_ADS%20_V2.0%20(3).PcbDoc). Giữ nguyên cấu trúc thư mục `altium/`, gồm hai thư viện Header trong `altium/libraries/`.

Project đóng gói dùng đường dẫn tài liệu tương đối. Chạy compile, xem liên kết model và đối chiếu schematic–PCB trước khi cập nhật thư viện hoặc xuất sản xuất.

## Sử dụng hệ thống

- H1/H2: vị trí kit ESP32; H3/H5: vị trí module nRF52840; H4: module ADS1299. Header không xác định đầy đủ model module thực tế.
- Theo cấu hình người thiết kế, dùng boost từ VBAT lên 5 V cho ESP32; nguồn analog dương/âm phục vụ điện cực ngoài. Cần đối chiếu đấu dây và tải thực tế.
- Connector bản hiện tại là H6–H12; dùng [pinout từ PCB](docs/PINOUT.md), không dùng bảng J1–J10 của bản cũ.

## File đi kèm

| Thư mục | Nội dung |
| --- | --- |
| `altium/` | Project, schematic, PCB và thư viện nguồn |
| `docs/` | BOM, pinout, trạng thái kiểm tra, provenance và ảnh/PDF lịch sử |
| `manufacturing/` | Gerber ZIP ngày 22/10 được đánh dấu archive/unverified |

Xem [BOM](docs/BOM.md), [ghi chú đóng gói](docs/PACKAGE_NOTES.md) và [trạng thái kiểm tra](docs/VALIDATION.md). Các tài liệu V1 ngoài thư mục này chỉ đại diện bản cũ.

## Chốt gói chế tạo

PCB và schematic đã lưu ngày 25/10; Gerber đang có từ 22/10, PDF từ 19/10. Cần xuất/đối chiếu lại đầu ra, lưu DRC bản cuối và cập nhật Release trước khi dùng gói này để đặt mạch. Không mô tả các báo cáo lịch sử là kết quả PASS của revision mới.
