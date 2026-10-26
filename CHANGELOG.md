# Lịch sử thay đổi

## Bộ ảnh 3D hai cấu hình — 26/10/2026

- Bổ sung đúng ba ảnh từ IMAGE/3D: top_nRF52840.png, top_esp32.png và Bottom.png.
- Đặt hai cấu hình nRF52840/ESP32 cạnh nhau trong README; bổ sung ảnh mặt dưới tại phần nguồn.
- Sửa gallery, chú thích và nguồn ảnh; giữ ảnh 2D làm tham khảo và không thay đổi thiết kế Altium.

## Ảnh do tác giả cung cấp — 26/10/2026

- Tải nguyên bản Top Layer, Bottom Layer và Schematic từ thư mục IMAGE của project V2.
- Đưa hai ảnh layout ngày 26/10 vào README và trang giới thiệu linh kiện, thay các hình 3D đang làm ảnh chính.
- Thêm bộ ảnh, chú thích ngày và SHA-256; schematic ngày 19/10 được ghi rõ là tham khảo.
- Giữ nguyên nguồn Altium, BOM, pinout, Gerber và các ảnh lịch sử.

## Tài liệu trực quan V2.0 — 25/10/2026

- Thêm hai ảnh 3D chụp từ PCB V2 hiện tại trong Altium, kèm thông tin nguồn và SHA-256.
- Viết lại README theo mục đích dự án EEG, luồng tín hiệu, khối nguồn và vai trò module/linh kiện.
- Thêm BOARD_OVERVIEW với mô tả U1–U3, các tụ, điện trở 0 Ω, H1–H12 và TP1–TP5; bổ sung nguồn datasheet hãng.
- Giữ nguyên source Altium, BOM và các đầu ra chế tạo; không tuyên bố đã có firmware, số đo EEG hoặc DRC mới.

## Hardware V2.0 — 25/10/2026

- Thêm snapshot nguồn V2 tại `hardware/v2.0/`, giữ nguyên nguồn V1 và lịch sử Git.
- Bản đã lưu có 49 linh kiện schematic và 49 linh kiện PCB; V1 có 48 / 48. Đây là số linh kiện được đặt, không phải xác nhận hoạt động điện.
- Designator mới so với V1: H5, H6, H7, H8, H9, H10, H11, H12, TP1, TP2, TP3, TP4, TP5.
- Designator không còn trong snapshot V2 so với V1: C17, C18, C19, C20, J1, J2, J3, J4, J5, J6, J7, J8. Đây là thay đổi tên/tập linh kiện, không tự kết luận thay đổi chức năng tương ứng.
- Thêm vị trí module nRF qua H3/H5, cùng vị trí ESP32 và ADS1299. Cấu hình sử dụng: chỉ cắm ESP32 hoặc nRF tại một thời điểm.
- Connector H6–H12 đang dùng footprint PCB `XH2.54M-2`; bổ sung thư viện Header nguồn để đóng gói đủ các tên symbol/footprint đang sử dụng.
- Thêm BOM tham khảo, pinout đọc từ PCB, manifest SHA-256 và trạng thái kiểm tra riêng cho V2.
- Giữ PDF/ảnh ngày 19–22/10 và Gerber ngày 22/10 trong tài liệu lịch sử/archive. Cần xuất lại hoặc xác nhận đầu ra khớp source ngày 25/10 trước khi dùng để chế tạo.
- Chưa bổ sung firmware hoặc kết quả đo board thật trong lần cập nhật này.

## V1 — 15/10/2026

- Bản prototype đầu tiên trên repository: project Altium, thư viện và tài liệu tiếng Việt.
- Nguồn và ghi chú V1 được giữ nguyên; xem `docs/README_V1.md`.
