# Logic Builder - Máy tính mini

## Prompt yêu cầu viết chương trình

> Viết một trang HTML có nhúng JavaScript để yêu cầu người dùng nhập điểm từ 0 đến 10 bằng `prompt()`. Dùng `if-else` để kiểm tra dữ liệu và xếp loại: Giỏi (trên 8), Khá (trên 6.5), Trung bình (từ 5 đến 6.5), Yếu (dưới 5). Nếu điểm từ 5 trở lên, hiển thị “Chúc mừng bạn đã đạt!”; nếu thấp hơn 5, hiển thị “Rất tiếc, hãy cố gắng hơn!”. Thông báo kết quả bằng `alert()`, đồng thời xử lý trường hợp người dùng hủy hoặc nhập điểm không hợp lệ.

## Giải thích từng dòng trong `index.html`

- `<!DOCTYPE html>`: Khai báo tài liệu sử dụng chuẩn HTML5.
- `<html lang="vi">`: Bắt đầu trang HTML và đặt ngôn ngữ là tiếng Việt.
- `<head>`: Mở phần chứa thông tin cấu hình của trang.
- `<meta charset="UTF-8">`: Cho phép hiển thị tiếng Việt chính xác.
- `<meta name="viewport" content="width=device-width, initial-scale=1.0">`: Giúp trang hiển thị phù hợp trên màn hình điện thoại và máy tính.
- `<title>Logic Builder - Máy tính mini</title>`: Đặt tiêu đề trên tab trình duyệt.
- `</head>`: Kết thúc phần cấu hình.
- `<body>`: Bắt đầu phần nội dung hiển thị trên trang.
- `<h1>Logic Builder - Kiểm tra điểm</h1>`: Hiển thị tiêu đề chính.
- `<p>Nhập điểm từ 0 đến 10 để xem kết quả.</p>`: Hướng dẫn người dùng nhập điểm.
- `<script>`: Bắt đầu đoạn mã JavaScript.
- `const input = prompt("Vui lòng nhập điểm của bạn (từ 0 đến 10):");`: Hiện hộp thoại yêu cầu nhập điểm và lưu nội dung người dùng nhập vào `input`.
- `if (input === null || input.trim() === "") {`: Kiểm tra người dùng đã hủy hộp thoại hoặc chỉ nhập khoảng trắng hay chưa.
- `alert("Bạn chưa nhập điểm.");`: Báo cho người dùng biết chưa có điểm để xử lý.
- `} else {`: Nếu có dữ liệu, tiếp tục kiểm tra điểm.
- `const diem = Number(input);`: Chuyển dữ liệu dạng chuỗi thành số.
- `if (!Number.isFinite(diem) || diem < 0 || diem > 10) {`: Kiểm tra dữ liệu có phải số hữu hạn và nằm trong khoảng từ 0 đến 10 không.
- `alert("Điểm không hợp lệ. Vui lòng nhập một số từ 0 đến 10.");`: Thông báo khi dữ liệu không hợp lệ.
- `} else {`: Nếu điểm hợp lệ, bắt đầu xếp loại.
- `let xepLoai;`: Tạo biến để lưu kết quả xếp loại.
- `if (diem > 8) {`: Kiểm tra điểm lớn hơn 8.
- `xepLoai = "Giỏi";`: Xếp loại Giỏi khi điểm lớn hơn 8.
- `} else if (diem > 6.5) {`: Nếu không thuộc loại Giỏi, kiểm tra điểm lớn hơn 6.5.
- `xepLoai = "Khá";`: Xếp loại Khá khi điểm lớn hơn 6.5 và không quá 8.
- `} else if (diem >= 5) {`: Nếu chưa thuộc hai loại trên, kiểm tra điểm từ 5 trở lên.
- `xepLoai = "Trung bình";`: Xếp loại Trung bình khi điểm từ 5 đến 6.5.
- `} else {`: Các điểm còn lại đều nhỏ hơn 5.
- `xepLoai = "Yếu";`: Xếp loại Yếu khi điểm nhỏ hơn 5.
- `if (diem >= 5) {`: Kiểm tra điểm có đạt ngưỡng 5 hay không.
- ``alert(`Chúc mừng bạn đã đạt! Xếp loại: ${xepLoai}.`);``: Thông báo đạt và chèn xếp loại vào nội dung bằng template literal.
- `} else {`: Xử lý trường hợp điểm dưới 5.
- ``alert(`Rất tiếc, hãy cố gắng hơn! Xếp loại: ${xepLoai}.`);``: Thông báo chưa đạt và hiển thị xếp loại.
- Các dấu `}`: Đóng những khối điều kiện `if-else` tương ứng.
- `</script>`: Kết thúc đoạn JavaScript.
- `</body>`: Kết thúc phần nội dung trang.
- `</html>`: Kết thúc tài liệu HTML.
