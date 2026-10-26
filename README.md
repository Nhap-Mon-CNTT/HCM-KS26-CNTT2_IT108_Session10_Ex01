# Yêu cầu đầu ra

## Phần 1: Phân tích:
- Record: Chứa thông tin cụ thể của một đối tượng, chứa nhiều loại dữ liệu, và là một hàng
- Field: Chứa 1 thuộc tính riêng biệt của đối tượng, chứa một loại dữ liệu cụ thể, và là một cột
- Vd trong file excel: [PayKX_DoiSoat.xlsx](PayKX_DoiSoat.xlsx)
  + Field: là các cột từ A đến H.
  + Record: là từ hàng 2 đến hàng 31
## Phần 2: Triển khai
- Word: [PayKX_SRS.docx](PayKX_SRS.docx)
- Excel: [PayKX_DoiSoat.xlsx](PayKX_DoiSoat.xlsx)
- PowerPoint: [PayKX_BaoCao.ppt](PayKX_BaoCao.ppt)
## Phần 3: Kiểm thử
- Lỗi #N/A (Not Available) là lỗi không tìm thấy giá trị mà yêu cầu
- Có thể tìm kiếm nguyên nhân bằng phương pháp 4 điểm dưới đây:
  + Khoảng trắng thừa: bấm vào ô mã, đặt con trỏ ở cuối nội dung để xem có khoảng trắng dư không. Nếu có, dùng TRIM làm sạch cả hai cột khóa (bảng giao dịch và bảng tra cứu), rồi cho VLOOKUP tra trên các cột đã làm sạch.
  + Kiểu dữ liệu: nhìn căn lề của ô. Số thường nằm sát phải, văn bản nằm sát trái. Hai bên lệch nhau thì chuyển về cùng kiểu.
  + Công thức: kiểm tra khóa nằm ở cột đầu tiên của vùng tra cứu, số thứ tự cột đúng, vùng được khóa bằng $ (phím F4) để không trượt khi kéo xuống, và tham số cuối là FALSE. Nếu sai thì sửa công thức.
  + Sự tồn tại: dùng Ctrl+F tìm mã đó trong bảng tra cứu. Nếu không có, bảng đang thiếu bản ghi, và #N/A là kết quả đúng. Lúc này cần bổ sung dữ liệu hoặc báo lại bên cung cấp, không sửa công thức cho hết lỗi.