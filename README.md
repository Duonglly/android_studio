# android_studio
# Đề tài: EduKit-Mini (Ứng dụng Hỗ trợ Học tập Đa năng)
## PHẦN 1:LÝ THUYẾT & THỰC HÀNH TRÊN MIT APP INVENTOR
## I. Lý thuyết nền tảng
### 1. Tổng quan giao diện Thiết kế (Designer)
--Thanh công cụ (Palette): Nằm ở phía bên trái giao diện. Đây là "kho vũ khí" chứa tất cả các thành phần (Components) từ cơ bản đến nâng cao được chia theo nhóm (User Interface, Layout, Media, Sensors...). Bạn chỉ cần chọn, giữ chuột và kéo thả chúng vào màn hình mô phỏng.

--Kéo thả + Thay đổi thuộc tính (Properties): * Làm như thế nào? Chọn cấu phần ở cột Components, sau đó nhìn sang cột Properties ở góc bên phải để chỉnh sửa các thông số như kích thước (Width, Height), màu sắc (BackgroundColor), cỡ chữ (FontSize), văn bản hiển thị (Text)...

--Để làm gì? Định hình giao diện người dùng (UI), giúp ứng dụng có vẻ ngoài trực quan, cân đối và thẩm mỹ trước khi tiến hành viết logic xử lý.

### 2. Bản chất của việc lập trình khối (Blocks)
--Bản chất: Thay vì gõ các dòng mã lệnh khô khan dễ sai cú pháp, bạn sẽ lắp ghép các "khối logic" có màu sắc và hình khối đặc thù (giống như trò chơi xếp hình Lego). Mỗi khối đại diện cho một câu lệnh, một hàm hoặc một sự kiện. Các khối chỉ có thể khớp với nhau nếu chúng hợp lệ về mặt logic toán học hoặc lập trình.

--Ưu điểm so với viết code truyền thống:

---Trực quan, dễ học, cực kỳ phù hợp cho người mới bắt đầu.

---Loại bỏ hoàn toàn lỗi cú pháp (Syntax Error) như thiếu dấu chấm phẩy ;, sai chính tả từ khóa.

---Tư duy logic được thể hiện rõ ràng qua các khối màu (Sự kiện màu cam, Điều khiển màu vàng, Toán học màu xanh...).

--Nhược điểm:

---Khi ứng dụng lớn, số lượng khối quá nhiều sẽ gây rối mắt, lag trình duyệt và khó quản lý.

---Hạn chế khả năng can thiệp sâu vào hệ thống phần cứng phức tạp của thiết bị.

---Tốc độ "gõ" logic chậm hơn so với việc một lập trình viên chuyên nghiệp gõ code bằng bàn phím.

---Tính năng Balo (Backpack): Là công cụ nằm ở góc trên bên phải màn hình Blocks. Nó hoạt động như một khay nhớ tạm (Clipboard) dùng chung. Bạn có thể kéo một cụm khối logic thả vào Balo để copy, sau đó chuyển sang một Screen khác và kéo từ Balo ra ngoài để paste. Việc này giúp tái sử dụng mã nguồn cực kỳ nhanh chóng.

## II. Thực hành

### Bước 1: Tạo cấu trúc 3 Màn hình (Screen)
--Truy cập ai2.appinventor.mit.edu, tạo Project mới tên là EduKit_Mini.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/881fa53e-a16d-4a4a-a872-b3a90a338b7b" />

--Mặc định đã có Screen1. Nhấn nút Add Screen ở phía trên, đặt tên là Screen_GiaiToan. Nhấn tiếp Add Screen, đặt tên là Screen_WebView.

<img width="459" height="196" alt="image" src="https://github.com/user-attachments/assets/14d3d38f-850e-42a2-b37d-7c1e8866c4b0" />

### Bước 2: Thiết kế và Lập trình Screen1 (About Bản thân & Điều hướng)
1. Kéo thả giao diện (Designer)
--Kéo một Label vào màn hình: Đổi thuộc tính Text thành: "Họ và tên: Nguyễn Văn A \n Mã SV: TEE123456 \n Lớp: TEE0419". Chỉnh FontSize thành 18, FontBold thành True.

--Kéo một HorizontalArrangement (trong mục Layout) vào dưới Label: Chỉnh Width thành Fill parent.

--Kéo 2 cái Button đặt nằm cạnh nhau vào trong cái HorizontalArrangement vừa kéo:

--Button1: Đổi tên thành Btn_Toan. Thuộc tính Text sửa thành "Giải Toán".

--Button2: Đổi tên thành Btn_Web. Thuộc tính Text sửa thành "Xem Website".

<img width="455" height="816" alt="image" src="https://github.com/user-attachments/assets/c8e5c925-c12b-48ae-adbe-e5714b158585" />


2. Ghép khối logic (Blocks)
--Chuyển sang tab Blocks. Chọn Btn_Toan từ danh mục bên trái, kéo khối when Btn_Toan.Click do ra màn hình.

--Vào mục Control, tìm và kéo khối open another screen screenName gắn vào trong khối click trên.

--Vào mục Text, kéo khối chuỗi trống "" gắn vào vị trí screenName, gõ chính xác tên màn hình: Screen_GiaiToan.


--Làm tương tự cho Btn_Web để mở Screen_WebView.

<img width="931" height="442" alt="image" src="https://github.com/user-attachments/assets/ab38ed19-9a1b-43fb-ad87-323263ab2cbb" />


### Bước 3: Thiết kế và Lập trình Screen_GiaiToan (Giải toán đơn giản)
--Bài toán lựa chọn: Tính diện tích tam giác khi biết đáy và chiều cao.

<img width="447" height="94" alt="image" src="https://github.com/user-attachments/assets/ec628ebd-7e10-41f2-9e7d-993c8e8486ab" />

1. Kéo thả giao diện (Designer)
--Chọn màn hình Screen_GiaiToan từ menu thả xuống phía trên.

--Kéo 2 TextBox vào màn hình:

--TextBox1: Đổi tên thành Txt_Day, thuộc tính Hint ghi "Nhập chiều dài cạnh đáy", tích chọn NumbersOnly.

--TextBox2: Đổi tên thành Txt_Cao, thuộc tính Hint ghi "Nhập chiều cao", tích chọn NumbersOnly.

--Kéo 1 Button: Đổi tên thành Btn_Tinh, thuộc tính Text ghi "Tính Diện Tích".

--Kéo 1 Label: Đổi tên thành Lbl_KetQua, thuộc tính Text ghi "Kết quả sẽ hiển thị ở đây", TextColor chọn màu đỏ.

<img width="480" height="819" alt="image" src="https://github.com/user-attachments/assets/d1f11619-bf7f-4459-8f50-9af8e7d4652b" />

2. Ghép khối logic (Blocks)
   
--Kéo khối when Btn_Tinh.Click do.

--Kéo khối set Lbl_KetQua.Text to.

--Vào mục Math, kéo khối phép nhân x và khối phép chia /. Lắp ghép logic toán học sao cho bằng: ( Txt_Day.Text * Txt_Cao.Text ) / 2.

<img width="1193" height="318" alt="image" src="https://github.com/user-attachments/assets/6fd37163-12d1-4c5b-bc5e-d8fea83908e3" />

### Bước 4: Thiết kế và Lập trình Screen_WebView (Hiển thị trang web hỗ trợ di động)

1. Kéo thả giao diện (Designer)
   
--Chuyển sang màn hình Screen_WebView.

--Vào mục User Interface, kéo thành phần WebViewer thả vào màn hình.

--Tại bảng thuộc tính Properties của WebViewer1, tìm mục HomeUrl và dán link này vào: https://m.wikipedia.org (Trang Wikipedia bản mobile, cực kỳ tối ưu cho điện thoại).


<img width="1125" height="2436" alt="image" src="https://github.com/user-attachments/assets/33352d41-62d6-4b19-b9c1-07b110f3818f" />

<img width="1125" height="2436" alt="image" src="https://github.com/user-attachments/assets/128d60be-6261-4be8-942f-f95a05c48281" />












