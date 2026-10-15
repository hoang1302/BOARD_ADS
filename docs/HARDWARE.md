# Giao tiếp phần cứng BOARD_ADS

Tài liệu ghi lại thiết kế đã lưu, chưa phải kết quả thử nghiệm. Pinout dưới đây đọc từ net/pad PCB; chưa xác nhận toàn bộ kết nối schematic–PCB bằng compile/ERC/ECO.

## Chức năng và phạm vi

Board kết nối kit ESP32 qua H1/H2 với module ADS1299 qua H4. IC ESP32 và ADS1299 không được triển khai trực tiếp thành một thiết kế IC hoàn chỉnh trên schematic này; project tập trung vào board giao tiếp và khối nguồn.

Các tín hiệu giữa ESP32 và module gồm DRDY, START, RESET, PWDN, CS, MOSI, MISO và SCLK. GPIO ghi trên schematic PDF cần được đối chiếu đúng phiên bản kit trước khi viết firmware.

## Khối nguồn

| Khối | Linh kiện | Vai trò theo schematic |
| --- | --- | --- |
| Nguồn dương | U1 LP5907MFX-2.5/NOPB | Tạo rail 2V5 từ VBAT, qua R4 = 0 Ω |
| Đảo nguồn | U3 TPS60403DBVR | Nhánh đảo nguồn từ VBAT qua các tụ và R2/R3 = 0 Ω |
| Nguồn âm | U2 TPS72325DBVR | Tạo rail -2V5 từ VBAT_NEG, qua R1 = 0 Ω |
| Phân phối | J1–J8 | Mỗi connector có chân 1 = 2V5, chân 2 = -2V5 |

Đây là tên rail và vai trò dự kiến trong thiết kế. Chưa có số đo điện áp, ripple, dòng tải, nhiệt độ hoặc trình tự khởi động. Dải VBAT, khả năng tạo -2V5 và điều kiện tải phải được đối chiếu datasheet và đo trước khi cấp nguồn cho module. J1–J8 được ghi PWR ELECTRODE trên schematic, không mặc định là tám ngõ vào analog của ADS1299.

## H3 — nguồn

| Chân | Net trên PCB |
| --- | --- |
| 1 | GND |
| 2 | 5V |
| 3 | VBAT |

5V và VBAT là hai net riêng; không tự nối chung nếu chưa xác định cách cấp nguồn của cả hệ thống.

## H1 — header kit ESP32

| Chân | Net trên PCB |
| --- | --- |
| 1 | 3V3 |
| 2 | 3V3 |
| 3 | (không gán net) |
| 4 | DRDY |
| 5 | START |
| 6 | RESET |
| 7 | PWDN |
| 8 | (không gán net) |
| 9 | (không gán net) |
| 10 | (không gán net) |
| 11 | (không gán net) |
| 12 | (không gán net) |
| 13 | (không gán net) |
| 14 | (không gán net) |
| 15 | (không gán net) |
| 16 | CS |
| 17 | MOSI |
| 18 | SCLK |
| 19 | MISO |
| 20 | (không gán net) |
| 21 | 5V |
| 22 | GND |

## H2 — header kit ESP32

| Chân | Net trên PCB |
| --- | --- |
| 1 | GND |
| 2 | (không gán net) |
| 3 | (không gán net) |
| 4 | (không gán net) |
| 5 | (không gán net) |
| 6 | (không gán net) |
| 7 | (không gán net) |
| 8 | (không gán net) |
| 9 | (không gán net) |
| 10 | (không gán net) |
| 11 | (không gán net) |
| 12 | (không gán net) |
| 13 | (không gán net) |
| 14 | (không gán net) |
| 15 | (không gán net) |
| 16 | (không gán net) |
| 17 | (không gán net) |
| 18 | (không gán net) |
| 19 | (không gán net) |
| 20 | (không gán net) |
| 21 | GND |
| 22 | GND |

## H4 — module ADS1299

| Chân | Net trên PCB |
| --- | --- |
| 1 | 3V3 |
| 2 | GND |
| 3 | (không gán net) |
| 4 | DRDY |
| 5 | MISO |
| 6 | (không gán net) |
| 7 | SCLK |
| 8 | START |
| 9 | RESET |
| 10 | PWDN |
| 11 | MOSI |
| 12 | (không gán net) |
| 13 | CS |

Hai pad cùng số chân 1 có cùng net 3V3 trong dữ liệu footprint hiện tại. Cần đối chiếu bản vẽ module và mục đích pad trước khi sửa footprint. Chân không gán net được giữ nguyên, không tự gán chức năng.

## Các điểm cần hoàn tất

- Xác nhận đúng model kit ESP32/module ADS1299, chiều nhìn header và kích thước cơ khí.
- Bổ sung footprint nguồn XH2.54M-3 của H3 vào thư viện project; PCB đang giữ hình học đã đặt.
- Đồng bộ Case/Package của C1–C29 với footprint thực tế.
- Bổ sung thông tin mua hàng và thông số còn thiếu trong [BOM tham khảo](../hardware/bom/BOM.md).
- Chạy compile/ERC/DRC, kiểm tra nguồn, mức logic và giao tiếp SPI với phần cứng thực tế.
