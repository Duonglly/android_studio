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

<img width="1125" height="2436" alt="image" src="https://github.com/user-attachments/assets/37c125e6-6fc5-490d-9416-b589281f58a6" />

<img width="1125" height="2436" alt="image" src="https://github.com/user-attachments/assets/f823d104-bdbc-4c2d-9d8f-0daa0b374cd0" />

## PHẦN 2: LÝ THUYẾT & THỰC HÀNH TRÊN ANDROID STUDIO
## I. Lý thuyết nền tảng Android & Java
1. AndroidManifest.xml là gì?
   
--Mô tả: Đây là file cấu hình bắt buộc và quan trọng nhất của mọi ứng dụng Android. Nó đóng vai trò như một "bản căn cước" khai báo với Hệ điều hành Android về: Tên ứng dụng, các Activity (màn hình), các Service, icon, và quan trọng nhất là các quyền (Permissions) truy cập phần cứng/hệ thống.

--Khai báo quyền Internet để ứng dụng làm việc: Thêm dòng sau vào phía trên thẻ <application>: <uses-permission android:name="android.permission.INTERNET" />

--Để làm gì? Hệ điều hành Android bảo mật rất nghiêm ngặt. Nếu không khai báo dòng này, mọi hành động kết nối mạng, gọi API, hay mở WebView sẽ lập tức bị hệ thống chặn lại và báo lỗi sập ứng dụng (SecurityException).

2. Vòng đời của một ứng dụng Android (Activity Lifecycle)
--Hàm onCreate(): Khi bạn tạo một Project mới, Android Studio luôn tự sinh hàm onCreate().

Tại sao? Vì đây là điểm khởi đầu (Entry Point) của một Activity. Khi người dùng bấm vào icon app, hệ điều hành sẽ nạp ứng dụng vào bộ nhớ và gọi hàm này đầu tiên. Nhiệm vụ của nó là khởi tạo các thiết lập cơ bản, thiết lập giao diện thông qua hàm setContentView(R.layout.activity_main) và liên kết các biến Code với các thành phần UI XML.

<img width="2000" height="2000" alt="anh" src="https://github.com/user-attachments/assets/64064955-638e-4b0b-ba43-0261e1f2f814" />

--Đoạn code Java kiểm tra quyền Runtime (Check Permission): Từ Android 6.0+, ngoài việc khai báo trong Manifest, các quyền nguy hiểm cần phải được người dùng đồng ý lúc đang chạy app.


"if (ContextCompat.checkSelfPermission(this, Manifest.permission.INTERNET) != PackageManager.PERMISSION_GRANTED) {
    // Nếu chưa có quyền, tiến hành yêu cầu người dùng cấp quyền
    ActivityCompat.requestPermissions(this, new String[]{Manifest.permission.INTERNET}, 101);
}"

--Ý nghĩa: Đảm bảo tính minh bạch và bảo mật, bảo vệ thông tin người dùng không bị ứng dụng ngầm trục lợi.

3. Quản lý Giao diện thông qua XML và Cơ chế Tham chiếu Resources
   
--Cú pháp tham chiếu: * Trong file XML: @string/ten_bien

--Trong code Java: R.string.ten_bien

--Ưu điểm vượt trội so với Hardcode (viết text trực tiếp):

--Tách biệt mã nguồn và dữ liệu: Dễ bảo trì, sửa một nơi - áp dụng toàn bộ app.

--Hỗ trợ Auto-adaptation theo hệ thống: OS tự động nhận diện thiết lập của người dùng để lấy giá trị tương ứng:

--LOCATION/LANGUAGE: Nếu máy cài tiếng Anh, OS tự tìm nạp file strings.xml trong thư mục values-en. Nếu máy cài tiếng Việt, nó nạp từ thư mục values-vi.

--THEME: Tự động đổi màu chữ/nền từ sáng (Light mode) sang tối (Dark mode) theo thiết lập hệ thống mà lập trình viên không cần viết thêm hàm if/else.

--Lợi ích: Giúp ứng dụng đạt chuẩn quốc tế hóa (Localization), mang lại trải nghiệm cá nhân hóa mượt mà cho mọi đối tượng người dùng.

4. Đối tượng chứa và Sắp xếp bố cục (LinearLayout)
   
--LinearLayout là một View Group có nhiệm vụ gom các thành phần con lại và xếp chúng nối đuôi nhau theo một quy luật duy nhất: theo chiều dọc (android:orientation="vertical") hoặc chiều ngang (android:orientation="horizontal").

--Gravity: * android:gravity: Sắp xếp nội dung bên trong chính đối tượng đó (Ví dụ: Chữ nằm giữa View).

--android:layout_gravity: Sắp xếp bản thân đối tượng đó trong không gian của View cha chứa nó.

5. Code tương tác tránh Hardcode (Localization-friendly)
   
--Để hiển thị văn bản đúng chuẩn ngôn ngữ hệ thống mà không dùng hardcode trong Java, ta dùng cú pháp: textView.setText(R.string.welcome_message);

6. Sự kiện (Event) người dùng tác động vào App
 
--Để một đoạn code chạy khi người dùng CLICK vào Button, ta xử lý như sau:

--Phía LAYOUT (XML): Phải định danh android:id="@+id/btn_submit" cho Button đó để Code Java có thể tìm thấy nó.


--Phía CODE (2 Cách viết):

Cách 1: Sử dụng Anonymous Inner Class (Hoặc Lambda) trong Java (Khuyên dùng)

Button btn = findViewById(R.id.btn_submit);
btn.setOnClickListener(new View.OnClickListener() {
    @Override
    public void onClick(View v) {
        // Thực hiện hành động ở đây
    }
});

7. Thư mục đặc biệt Assets
   
--Khái niệm: Thư mục assets chứa các tệp dữ liệu thô (JSON, Text, SQLite, HTML...) đi kèm theo ứng dụng khi đóng gói thành file .apk.

--Cú pháp truy cập dữ liệu trong thư mục Assets:

AssetManager assetManager = getAssets();
InputStream is = assetManager.open("data.json");

--Lợi ích của việc chuẩn bị sẵn file offline:

---Ứng dụng hoạt động ngay cả khi không có kết nối Internet (Offline hoàn toàn).

---Tốc độ tải dữ liệu tức thì, không bị trễ do băng thông mạng.

---Tiết kiệm chi phí vận hành Server lưu trữ dữ liệu cho lập trình viên.

## II. Hướng dẫn thực hành Bài tập lớn 2 trên Android Studio

--Đề tài : Smart Assistant Pro (Trợ lý Sinh viên Thông minh)

--Ứng dụng thực tế của Assets: Đọc một file cấu hình JSON chứa thông tin sinh viên offline từ thư mục assets, xử lý hiển thị lên màn hình chính.

 BƯỚC 0: KHỞI TẠO PROJECT CHUẨN (NẾU LÀM MỚI)
Nếu bạn tạo project mới từ đầu, hãy chú ý chọn đúng cấu hình:

Mở Android Studio -> Chọn New Project.

QUAN TRỌNG: Chọn mẫu là Empty Views Activity (nhớ là phải có chữ Views nhé, nếu chọn nhầm Empty Activity bản mới nó sẽ ra giao diện Jetpack Compose là không gõ được code XML đâu).

Ô Name: Điền Smart Assistant Pro.

Ô Package name: Điền đúng com.example.smartassistant.

Ô Language: Chọn Java. Nhấn Finish và đợi nó tải xong cấu trúc.

 BƯỚC 1: TẠO THƯ MỤC ASSETS & FILE JSON OFF-LINE
1. Cách tạo thư mục assets:
Nhìn vào cột bên trái, tìm thư mục lớn tên là app.

Bấm chuột phải vào thư mục app -> Chọn New -> Chọn Folder -> Chọn Assets Folder.

<img width="1469" height="1056" alt="image" src="https://github.com/user-attachments/assets/d3ad6a54-3787-43ee-a362-070b4c80c322" />

Một bảng hiện ra, bạn giữ nguyên các thông số mặc định và bấm nút Finish.

2. Cách tạo file student_profile.json:

--Lúc này, bạn nhìn lại cột bên trái, bên trong thư mục app đã xuất hiện một thư mục mới tinh tên là assets.

--Bấm chuột phải vào thư mục assets vừa tạo -> Chọn New -> Chọn File.

--Ô đặt tên hiện ra, bạn gõ chính xác: student_profile.json rồi nhấn Enter.

--Mở file vừa tạo ra và dán đoạn nội dung này vào (tôi đã đổi sẵn thông tin chính chủ của bạn cho xịn nhé):

{
  "name": "Dương Thị Ly",
  "id": "K22540106045",
  "class": "K58-KMT",
  "slogan": "Học không chơi đánh rơi tuổi trẻ, chơi không học vừa khỏe vừa vui!"
}

<img width="1707" height="391" alt="image" src="https://github.com/user-attachments/assets/337c7223-8bd4-43e1-b453-4d7cc1d72dbd" />

📋 BƯỚC 2: CẤU HÌNH FILE AndroidManifest.xml
Tìm file ở đâu: Ở cột lề trái, mở thư mục manifests -> Bạn sẽ thấy file AndroidManifest.xml. Mở nó lên.

Thao tác dán đoạn code này vào: 

<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.google.com/apk/res/android"
    package="com.example.smartassistant">

    <uses-permission android:name="android.permission.INTERNET" />

    <application
        android:allowBackup="true"
        android:icon="@mipmap/ic_launcher"
        android:label="Smart Assistant Pro"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.AppCompat.Light.DarkActionBar">
        
        <activity android:name=".MainActivity"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />
                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>

        <activity android:name=".MathActivity" />

        <activity android:name=".WebActivity" />
        
    </application>
</manifest>

🏠 BƯỚC 3: CÀI ĐẶT MÀN HÌNH CHÍNH (MainActivity)
Màn hình này đã có sẵn khi bạn tạo app, bạn chỉ cần tìm đúng file để sửa:

1. Phần Giao diện (XML):
Tìm file ở đâu: Vào theo đường dẫn thư mục: app -> res -> layout -> Mở file activity_main.xml.

Thao tác: Nhìn lên góc trên bên phải màn hình code, có 3 nút: Code / Split / Design. Hãy bấm vào nút Code để hiện text XML. Xóa hết đi và dán đoạn này vào:

<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.google.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp"
    android:gravity="center_horizontal">

    <TextView
        android:id="@+id/tv_title"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="THÔNG TIN SINH VIÊN (ASSETS)"
        android:textSize="20sp"
        android:textStyle="bold"
        android:layout_marginBottom="20dp"/>

    <TextView
        android:id="@+id/tv_profile"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:textSize="16sp"
        android:text="Đang tải dữ liệu từ Assets..."
        android:layout_marginBottom="30dp"/>

    <Button
        android:id="@+id/btn_goto_math"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Mở Màn Hình Giải Toán"
        android:layout_marginBottom="10dp"/>

    <Button
        android:id="@+id/btn_goto_web"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Mở Màn Hình WebView" />
</LinearLayout>

2. Phần Code xử lý (Java):
Tìm file ở đâu: Vào theo đường dẫn thư mục: app -> java -> com.example.smartassistant -> Mở file MainActivity.java.

Thao tác dán đoạn code logic này vào:

package com.example.smartassistant;

import android.content.Intent;
import android.os.Bundle;
import android.widget.Button;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;
import org.json.JSONObject;
import java.io.InputStream;
import java.nio.charset.StandardCharsets;

public class MainActivity extends AppCompatActivity {
    private TextView tvProfile;
    private Button btnMath, btnWeb;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        tvProfile = findViewById(R.id.tv_profile);
        btnMath = findViewById(R.id.btn_goto_math);
        btnWeb = findViewById(R.id.btn_goto_web);

        // Đọc dữ liệu JSON từ Assets hiển thị lên màn hình
        loadStudentDataFromAssets();

        // Nút chuyển sang màn hình Giải Toán
        btnMath.setOnClickListener(v -> {
            Intent intent = new Intent(MainActivity.this, MathActivity.class);
            startActivity(intent);
        });

        // Nút chuyển sang màn hình WebView
        btnWeb.setOnClickListener(v -> {
            Intent intent = new Intent(MainActivity.this, WebActivity.class);
            startActivity(intent);
        });
    }

    private void loadStudentDataFromAssets() {
        try {
            InputStream is = getAssets().open("student_profile.json");
            int size = is.available();
            byte[] buffer = new byte[size];
            is.read(buffer);
            is.close();

            String jsonStr = new String(buffer, StandardCharsets.UTF_8);
            JSONObject obj = new JSONObject(jsonStr);

            String formattedText = "Họ Tên: " + obj.getString("name") + "\n\n"
                    + "Mã SV: " + obj.getString("id") + "\n\n"
                    + "Lớp: " + obj.getString("class") + "\n\n"
                    + "Slogan: " + obj.getString("slogan");

            tvProfile.setText(formattedText);
        } catch (Exception e) {
            tvProfile.setText("Lỗi nạp file dữ liệu từ Assets!");
        }
    }
}

BƯỚC 4: TẠO VÀ CÀI ĐẶT MÀN HÌNH GIẢI TOÁN (MathActivity)

--Vì đây là màn hình thứ 2 nên chưa có sẵn, bạn phải tự tạo cả file Java và XML bằng cách click chuột tự động sau:

--Cách tạo tự động: Bấm chuột phải vào thư mục gói com.example.smartassistant (ở mục java) -> Chọn New -> Chọn Activity -> Chọn Empty Views Activity.

--Một cái bảng hiện lên, ở ô Activity Name, bạn gõ vào chữ: MathActivity rồi bấm nút Finish. Hệ thống sẽ tự tạo ra file Java và file layout XML.

<img width="1641" height="1009" alt="image" src="https://github.com/user-attachments/assets/6e976974-bf8c-4714-b1dd-bf87079e93cc" />


1. Giao diện Màn hình Toán (activity_math.xml):
Đường dẫn file: Vào app -> res -> layout -> Mở file activity_math.xml mới tinh vừa được sinh ra.

Thao tác: Bấm sang chế độ Code dán đoạn mã giao diện này vào:

<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.google.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="GIẢI PHƯƠNG TRÌNH ax + b = 0"
        android:textSize="18sp"
        android:textStyle="bold"
        android:layout_gravity="center"
        android:layout_marginBottom="20dp"/>

    <EditText
        android:id="@+id/edt_a"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Nhập hệ số a"
        android:inputType="numberDecimal|numberSigned" />

    <EditText
        android:id="@+id/edt_b"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Nhập hệ số b"
        android:inputType="numberDecimal|numberSigned" />

    <Button
        android:id="@+id/btn_solve"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Giải và Đồng bộ API"
        android:layout_marginTop="10dp"/>

    <TextView
        android:id="@+id/tv_math_result"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Kết quả bài toán..."
        android:textSize="16sp"
        android:layout_marginTop="20dp"
        android:textColor="#00796B"/>

    <TextView
        android:id="@+id/tv_api_status"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Trạng thái đồng bộ API..."
        android:textSize="14sp"
        android:layout_marginTop="10dp"
        android:textStyle="italic" />
</LinearLayout>

2. Code logic xử lý toán & API (MathActivity.java):
Đường dẫn file: Vào app -> java -> com.example.smartassistant -> Mở file MathActivity.java.

Thao tác: Xóa hết nội dung bên trong đi và dán đoạn code xử lý thuật toán tính toán + kết nối mạng gửi dữ liệu lên server này vào:

package com.example.smartassistant;

import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;
import org.json.JSONObject;
import java.io.OutputStream;
import java.net.HttpURLConnection;
import java.net.URL;
import java.nio.charset.StandardCharsets;
import java.util.Scanner;

public class MathActivity extends AppCompatActivity {
    private EditText edtA, edtB;
    private Button btnSolve;
    private TextView tvMathResult, tvApiStatus;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_math);

        edtA = findViewById(R.id.edt_a);
        edtB = findViewById(R.id.edt_b);
        btnSolve = findViewById(R.id.btn_solve);
        tvMathResult = findViewById(R.id.tv_math_result);
        tvApiStatus = findViewById(R.id.tv_api_status);

        btnSolve.setOnClickListener(v -> executeMathAndApi());
    }

    private void executeMathAndApi() {
        try {
            double a = Double.parseDouble(edtA.getText().toString());
            double b = Double.parseDouble(edtB.getText().toString());
            String ketLuan;
            double nghiem = 0;

            if (a == 0) {
                ketLuan = (b == 0) ? "Vô số nghiệm" : "Vô nghiệm";
            } else {
                nghiem = -b / a;
                ketLuan = "Có nghiệm duy nhất";
            }

            String localResult = "Kết luận: " + ketLuan + (a != 0 ? " (x = " + nghiem + ")" : "");
            tvMathResult.setText(localResult);

            // Gửi dữ liệu lên API bằng Thread riêng (Tránh lỗi NetworkOnMainThreadException)
            final double finalNghiem = nghiem;
            final String finalKetLuan = ketLuan;
            
            // Đã đổi mã sinh viên chuẩn của bạn vào luồng gửi dữ liệu
            new Thread(() -> sendDataToApi("K22540106045", a, b, finalKetLuan, finalNghiem)).start();

        } catch (Exception e) {
            tvMathResult.setText("Vui lòng nhập đầy đủ hệ số hợp lệ!");
        }
    }

    private void sendDataToApi(String maSv, double a, double b, String ketLuan, double nghiem) {
        try {
            URL url = new URL("https://k58kmt.tdh.io.vn/api");
            HttpURLConnection conn = (HttpURLConnection) url.openConnection();
            conn.setRequestMethod("POST");
            conn.setRequestProperty("Content-Type", "application/json; charset=UTF-8");
            conn.setDoOutput(true);

            // Đóng gói dữ liệu JSON theo đúng yêu cầu đề tài bài tập lớn
            JSONObject root = new JSONObject();
            root.put("app_by", maSv);

            JSONObject input = new JSONObject();
            input.put("a", a);
            input.put("b", b);
            input.put("c", 0); 
            input.put("name", "Giải phương trình bậc nhất");
            root.put("input", input);

            JSONObject output = new JSONObject();
            output.put("ketluan", ketLuan);
            output.put("abc", "Chuyển vế đổi dấu");
            output.put("nghiem", nghiem);
            root.put("output", output);

            // Đẩy luồng dữ liệu lên internet
            OutputStream os = conn.getOutputStream();
            os.write(root.toString().getBytes(StandardCharsets.UTF_8));
            os.close();

            // Nhận phản hồi phản hồi ngược lại từ server của nhà trường
            int responseCode = conn.getResponseCode();
            if (responseCode == HttpURLConnection.HTTP_OK) {
                Scanner scanner = new Scanner(conn.getInputStream());
                String response = scanner.useDelimiter("\\A").next();
                scanner.close();

                JSONObject resJson = new JSONObject(response);
                runOnUiThread(() -> tvApiStatus.setText("Đồng bộ thành công! Số thứ tự thao tác: " + resJson.optString("stt")));
            } else {
                runOnUiThread(() -> tvApiStatus.setText("Lỗi từ hệ thống Server: " + responseCode));
            }
            conn.disconnect();
        } catch (Exception e) {
            runOnUiThread(() -> tvApiStatus.setText("Lỗi: Không kết nối được Internet hoặc sai link API!"));
        }
    }
}

BƯỚC 5: TẠO VÀ CÀI ĐẶT MÀN HÌNH WEBVIEW (WebActivity)
Đây là màn hình số 3 để nhúng link trang web nhà trường kèm mã sinh viên cá nhân của bạn.

Cách tạo tự động: Tiếp tục bấm chuột phải vào thư mục gói com.example.smartassistant -> Chọn New -> Chọn Activity -> Chọn Empty Views Activity.

Ô Activity Name, gõ vào: WebActivity rồi bấm nút Finish.

<img width="1520" height="892" alt="image" src="https://github.com/user-attachments/assets/6c8dd652-0c81-4f4b-b774-952af0114343" />


1. Giao diện WebView (activity_web.xml):
Đường dẫn file: Vào app -> res -> layout -> Mở file activity_web.xml.

Thao tác: Chuyển sang tab Code, xóa hết đi và dán đoạn mã này:

<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.google.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical">

    <WebView
        android:id="@+id/my_webview"
        android:layout_width="match_parent"
        android:layout_height="match_parent" />
</LinearLayout>

2. Code xử lý nhúng link cá nhân hóa (WebActivity.java):
Đường dẫn file: Vào app -> java -> com.example.smartassistant -> Mở file WebActivity.java.

Thao tác: Xóa sạch nội dung cũ đi và dán đoạn mã điều khiển WebView này vào:

package com.example.smartassistant;

import android.os.Bundle;
import android.webkit.WebSettings;
import android.webkit.WebView;
import android.webkit.WebViewClient;
import androidx.appcompat.app.AppCompatActivity;

public class WebActivity extends AppCompatActivity {
    private WebView webView;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_web);

        webView = findViewById(R.id.my_webview);
        
        // Cấu hình ép buộc link web mở ngay bên trong app thay vì mở bằng trình duyệt Chrome ngoài máy
        webView.setWebViewClient(new WebViewClient()); 
        
        // Kích hoạt thực thi JavaScript để hiển thị đầy đủ giao diện web hiện đại
        WebSettings webSettings = webView.getSettings();
        webSettings.setJavaScriptEnabled(true); 

        // Tự động tạo link nhúng kèm mã số sinh viên chính chủ của bạn
        String maSv = "K22540106045"; 
        String targetUrl = "https://k58kmt.tdh.io.vn?masv=" + maSv;

        // Bắt đầu tải trang web
        webView.loadUrl(targetUrl);
    }

    // Xử lý nút Back vật lý trên điện thoại: Lùi lại trang trước đó của web thay vì thoát app đột ngột
    @Override
    public void onBackPressed() {
        if (webView.canGoBack()) {
            webView.goBack();
        } else {
            super.onBackPressed();
        }
    }
}

Activity 1 (MainActivity - About): Đã có thông tin sinh viên (đọc từ file JSON trong Assets) và 2 nút bấm để chuyển sang màn hình Giải toán và màn hình WebView.
<img width="1635" height="995" alt="image" src="https://github.com/user-attachments/assets/03d7aa00-14d9-4ec6-9c05-fd87e9ba9111" />


Activity 2 (MathActivity - Giải toán):Giải phương trình bậc nhất ax + b = 0.

Gửi API: Sử dụng POST gửi dữ liệu lên https://k58kmt.tdh.io.vn/api/ ngay sau khi giải xong.

<img width="1632" height="1022" alt="image" src="https://github.com/user-attachments/assets/854a1971-033f-4355-b5e1-0019145e78dd" />
<img width="1623" height="919" alt="image" src="https://github.com/user-attachments/assets/30bedda1-0c70-4ec0-91cf-780fb5b39ff0" />

Sử dụng WebView để truy cập link kèm mã sinh viên chính xác: https://k58kmt.tdh.io.vn?masv=K225480106045.
<img width="1623" height="420" alt="image" src="https://github.com/user-attachments/assets/f553344d-446d-4469-a8cf-80a5e2e89ac7" />
## Làm app2 Sinh tồn khi bị mắc kẹt trong rừng sâu

### 
Vấn đề đặt ra: Khi bị lạc trong rừng sâu, điện thoại sẽ bị mất sóng hoàn toàn (offline), không thể tra Google hay dùng 4G/5G. Người lạc cần một ứng dụng có sẵn dữ liệu cứu hộ khẩn cấp bên trong máy để cứu mạng.

Đặc thù dữ liệu: Dữ liệu là văn bản thô (Plain Text), được chuẩn bị trước mã hóa theo chuẩn UTF-8 (để hiển thị đúng tiếng Việt có dấu) lưu trong file sinhton.txt thuộc thư mục Assets.

Thuật toán xử lý: Sử dụng Stream I/O (Luồng vào/ra) của Java thông qua AssetManager. Đọc toàn bộ luồng Byte tuần tự từ file, nạp vào mảng bộ đệm byte[], sau đó dùng thuật toán chuyển đổi mảng Byte thành Chuỗi văn bản (String).

Đối tượng hiển thị: Sử dụng cấu trúc ScrollView chứa TextView. Vì tài liệu sinh tồn rất dài, bắt buộc phải dùng ScrollView để người dùng có thể vuốt cuộn màn hình lên xuống đọc bài (Thể hiện độ hoàn thiện và tính thực tế cao của App).

Bước 1: Tạo file dữ liệu sinhton.txt trong thư mục assets
Bạn nhấn chuột phải vào thư mục assets -> chọn New -> File -> Đặt tên chuẩn là: sinhton.txt và dán nội dung cẩm nang này vào:

CẨM NANG SINH TỒN KHI BỊ LẠC TRONG RỪNG SÂU
(Dữ liệu Cứu hộ Ngoại tuyến - An toàn tuyệt đối)

1. NGUYÊN TẮC "S.T.O.P" KHẨN CẤP
- S (Sit down): Ngồi xuống, giữ bình tĩnh, không hoảng loạn.
- T (Think): Suy nghĩ xem mình đi hướng nào, nhớ lại mốc đánh dấu.
- O (Observe): Quan sát xung quanh tìm nguồn nước, nơi trú ẩn an toàn.
- P (Plan): Lập kế hoạch tiết kiệm thức ăn và tìm cứu hộ.

2. TÌM KIẾM NGUỒN NƯỚC (QUAN TRỌNG NHẤT)
- Con người chỉ sống được 3 ngày nếu thiếu nước.
- Cách tìm: Hãy đi xuôi theo dòng chảy của thung lũng, lắng nghe tiếng suối.
- Hãy nhìn hướng bay của chim hoặc dấu chân thú rừng để tìm nguồn nước.
- Tuyệt đối: Đun sôi nước suối trước khi uống để tránh ký sinh trùng.

3. XÂY DỰNG NƠI TRÚ ẨN LƯU TRÚ
- Tìm vị trí cao ráo, tránh xa các bụi rậm có rắn rết, côn trùng độc.
- Dùng cành cây khô xếp thành hình chữ A, phủ lá cây chuối rừng hoặc lá cây rậm lên trên để che mưa, che sương đêm.
- Lót một lớp lá khô dày dưới đất trước khi nằm để tránh mất nhiệt cơ thể.

4. TẠO LỬA SƯỞI ẤM VÀ TÍN HIỆU CỨU HỘ
- Thu thập củi khô, lá mục khô làm mồi nhóm lửa.
- Có thể dùng thấu kính của kính cận, kính lúp, hoặc cọ xát gỗ khô để tạo lửa.
- Để tạo tín hiệu cứu hộ ban ngày: Đốt lửa và cho thêm lá cây tươi để tạo ra khói dày màu trắng, trực thăng hoặc đội cứu hộ từ xa dễ phát hiện.

  Bước 2: Thiết kế giao diện cuộn trong activity_main.xml
Thay vì chỉ dùng TextView thông thường, bạn bọc nó bằng ScrollView giúp giao diện trở nên chuyên nghiệp, hiện đại, không bị tràn màn hình khi chữ quá dài.

<?xml version="1.0" encoding="utf-8"?>
<ScrollView xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#F4F6F9"
    android:padding="20dp">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical">

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="ỨNG DỤNG SINH TỒN OFFLINE"
            android:textColor="#2E7D32"
            android:textSize="22sp"
            android:textStyle="bold"
            android:gravity="center"
            android:layout_marginBottom="20dp"/>

        <TextView
            android:id="@+id/txtCamNang"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Đang tải dữ liệu cẩm nang..."
            android:textColor="#333333"
            android:textSize="16sp"
            android:lineSpacingMultiplier="1.2" />

    </LinearLayout>
</ScrollView>
Bước 3: Viết code Java xử lý trong MainActivity.java
Bạn mở file MainActivity.java của Project mới lên và chép đoạn code xử lý luồng hoàn chỉnh này vào bên trong hàm onCreate:

package com.example.app1_assets; // Nhớ sửa lại đúng tên package của bạn nếu khác

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.widget.TextView;
import java.io.IOException;
import java.io.InputStream;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void bundle(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // Ánh xạ TextView từ giao diện XML sang Java
        TextView txtCamNang = findViewById(R.id.txtCamNang);

        try {
            // Bước 1: Mở tệp tin sinhton.txt nằm trong thư mục Assets
            InputStream is = getAssets().open("sinhton.txt");

            // Bước 2: Kiểm tra kích thước tệp tin và tạo mảng byte bộ đệm tương ứng
            int size = is.available();
            byte[] buffer = new byte[size];

            // Bước 3: Đọc toàn bộ dữ liệu từ tệp vào mảng bộ đệm và đóng luồng
            is.read(buffer);
            is.close();

            // Bước 4: Chuyển đổi mảng Byte thành định dạng Chuỗi String UTF-8 để nhận diện tiếng Việt
            String duLieuChuoi = new String(buffer, "UTF-8");

            // Bước 5: Cập nhật văn bản lên giao diện hiển thị cho người dùng cứu hộ
            txtCamNang.setText(duLieuChuoi);

        } catch (IOException e) {
            e.printStackTrace();
            // Trường hợp lỗi hệ thống không thấy file
            txtCamNang.setText("LỖI KHẨN CẤP: Không tìm thấy tệp dữ liệu sinh tồn!");
        }
    }
}

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1bcbce24-c8d8-4ea6-a195-7cf3e8a260e4" />
