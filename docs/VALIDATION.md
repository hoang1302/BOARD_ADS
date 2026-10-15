# Kế hoạch kiểm tra

Tài liệu này là danh sách việc cần thực hiện, **không phải báo cáo đã đạt**. Gói chưa có dữ liệu đo hoặc xác nhận hoạt động phần cứng từ người thiết kế.

## Kiểm tra thiết kế

- Compile schematic và xác nhận kết nối schematic–PCB.
- Chạy ERC/DRC trên đúng bản lưu; giữ báo cáo, thời điểm chạy và revision.
- Đối chiếu footprint, cực tính, điện áp/công suất định mức và bản vẽ cơ khí.
- Chốt BOM, DNP và linh kiện/module mua riêng.

## Kiểm tra phần cứng

| Phép kiểm tra | Bằng chứng cần lưu |
| --- | --- |
| Kiểm tra nguồn | Đo VBAT, 2V5, VBAT_NEG và -2V5 khi không tải và có tải; ghi ripple, dòng tải, nhiệt độ và trình tự khởi động. |
| Kiểm tra kit/module | Xác nhận đúng model ESP32/module ADS1299, kích thước, chiều chân 1 và mức logic. |
| Kiểm tra giao tiếp | Ghi lại cấu hình firmware, kết quả giao tiếp SPI, DRDY và các tín hiệu điều khiển. |
| Kiểm tra nhiễu | So sánh dữ liệu đo với các điều kiện tải/nguồn dự kiến; công bố giới hạn từ số đo thực tế. |

## Nội dung báo cáo kết quả

Ghi hardware revision, ngày đo, sơ đồ đấu nối, thiết bị đo, cấu hình nguồn/tải, mẫu thử, số lần lặp, kết quả, lỗi còn mở và ảnh board thực tế. Chỉ điền kết quả sau khi đã thực hiện; không suy ra PASS chỉ từ schematic hoặc báo cáo cũ.
