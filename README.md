Chỉnh lại email quản trị //OrderControl.java
Chỉnh lại đường dẫn xuất file excel // XuatExcelControl.java

mở chế độ cho phép truy cập từ ứng dụng kém an toàn
https://myaccount.google.com/security

Tài khoản full quyền:
bao
123456

Vào cms quản trị
http://localhost:8080/WebsiteBanBaoGiay/admin

Lỗi không mở được SQL Server Configuration nhớ chạy cmd quyền admin -> https://stackoverflow.com/questions/44753745/sql-server-config-manager-error-cannot-connect-to-wmi-provider

Chú ý lúc import project chọn File->Import->Maven->Existing Maven Project

Chú ý lỗi maven có dấu x đỏ 
This worked for me in Windows as well.
Locate the {user}/.m2/repository (Using Juno /Win7 here)
In the Search field in upper right of window, type ".lastupdated". Windows will look through all subfolders for these files in the directory. (I did not look through cache.)
Remove them by Right-click > Delete (I kept all of the lastupdated.properties).
Then go back into Eclipse, Right-click on the project and select Maven > Update Project. I selected to "Force Update of Snapshots/Releases". Click Ok and the dependencies finally resolved correctly.
->https://stackoverflow.com/questions/5074063/maven-error-failure-to-transfer

Chú ý lỗi không tìm thấy SQL server Configuration Manager not found in Windows 11
->https://www.youtube.com/watch?v=txRtKWWk3u0

Chú ý giải quyết lỗi file jsp bị dấu chấm thang đỏ do lúc đầu đã cài tomcat10 bị chuyển sang một servlet khác nên khi cast qua tomcat 9 rất mất công
Video hướng dẫn giải quyết: https://www.youtube.com/watch?v=jM-eWX102LQ

Chú ý nếu đã để đúng password và email cho OrderControl rồi mà vẫn không gửi email được là do cần vô Gmail để 
mở file email Google gửi cách báo bảo mật và nhấn Kiểm tra sau đó cho phép là chạy lại được
Chỉ cần thêm download javax-mail-1.6.2.jar và activation-1.1 của nó đã tải kèm theo
->(thu vien javax-mail1.6.2)
https://jar-download.com/artifacts/com.sun.mail/javax.mail/1.6.2/source-code
Tham khảo video:https://www.youtube.com/watch?v=Fousdqr6Si4


chú ý phải set fullcontrol cho các thư mục .metadata của workspace eclipse chỗ chứa source code và fullcontrol cho thư mục tomcat(thư mục ngoài cùng apache tomcat ..) và thư mục XuatHoaDonControl cũng set fullcontrol và tạo thêm tài khoản Everyone tạo fullcontrol 

chú ý khi dùng bản jdbc jre11 xem bản đó có hổ trợ đúng phiên bản jdk java không ví dụ jdk16
thì dùng bản này https://jar-download.com/artifacts/com.microsoft.sqlserver/mssql-jdbc/9.4.1.jre11/source-code

bật login bằng sql server chỗ sql server right click chọn properties chọn tab security bật chấp nhận đăng nhập bằng sql server


Tổng hợp một số lỗi thường gặp khi các bạn cài đặt
+Tài liệu cài đặt từ đầu: từ cài jdk17 hoặc 16, jre1.8, cài tomcat, cấu hình tomcat
https://drive.google.com/file/d/1LGMQOoCpEDvThcPjg8XuLteHQqfMicqs/view?usp=sharing
+ bỏ thêm cái jdbc jar vào cái thư mục lib thứ hai chỗ src/main/webapp/WEB_INF/lib
+ chỗ jdbc chọn bản jre11
+ chắc là bỏ source code web vào workspace của eclipse rồi mới import vào, import từ cái source trong workspace
+ chỗ cái thư mục workspce cho nó fullcontrol luôn với cái thư mục chứa tomcat cho nó fullcontrol luôn
+ Bạn chỗ menu eclipse chọn Window -> Preferences -> General -> Web Browser->Chrome để đặt trình duyệt mặc đình là chrome
+ menu eclipse chọn Project -> Properties -> Resource -> UTF-8 -> apply and close


Link demo lỗi: https://www.youtube.com/watch?v=ik7QhaRmeqM
