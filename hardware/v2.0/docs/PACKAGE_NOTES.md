# Ghi chú đóng gói V2.0

- Nguồn là các file Altium đã lưu ngày 25/10/2026. Không xác nhận được nội dung chưa lưu trong phiên Altium vì bridge không phản hồi.
- Schematic, PCB, SchLib, PcbLib và hai thư viện Header được giữ nguyên byte. Chỉ chỉnh bản sao PrjPcb để bỏ 16 tham chiếu GeneratedDocument và thêm hai thư viện Header bằng đường dẫn tương đối.
- Giữ nguyên tên file Altium để bảo toàn các tham chiếu hiện có. Các trường SourceLibraryName/SourceFootprintLibrary lịch sử bên trong file nhị phân vẫn được giữ nguyên; tên thư viện cũ có thể khác tên file hiện tại. Chọn đúng thư viện trong project khi cập nhật, không chạy thay thế toàn bộ mà không xem diff/ECO.
- Thư viện Header đi kèm chứa symbol `Header 2P 2.54 Duc Thang` và footprint `XH2.54M-2` mà phiên bản này sử dụng. Việc tìm thấy tên không xác nhận model schematic và footprint đang đặt giống nhau.
- Mô hình đã nhúng trong PCB/PcbLib được giữ cùng file nhị phân. Chưa mở lại project bằng Altium trên máy khác để kiểm tra đầy đủ model 3D và liên kết thư viện; không tự sửa hoặc tải lại STEP từ bên ngoài.
- PDF và ảnh cũ được giữ để tham khảo, có nhãn ngày. Gerber cũ nằm trong archive và không được gắn trạng thái manufacturing-ready.
- Không đưa History, cache, log, thư mục review với môi trường Python/vendor hoặc toàn bộ Project Outputs lên GitHub.
- Không thay đổi giấy phép hay xóa metadata nguồn của thư viện/model bên ngoài. Gói không tự gán giấy phép mới cho toàn bộ thiết kế.

`package-manifest.json` lưu mã SHA-256, kích thước và thời điểm nguồn cho từng file được sao chép; không công bố đường dẫn tuyệt đối trên máy người thiết kế.
