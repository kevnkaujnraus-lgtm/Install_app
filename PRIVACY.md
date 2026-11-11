# Privacy policy / Chính sách quyền riêng tư — Pass Show

Last updated / Cập nhật lần cuối: 2026-11-11 (app version / phiên bản 1.0.26)

[English](#english) · [Tiếng Việt](#tiếng-việt)

---

## English

**Summary.** Pass Show is an offline-first password manager. The developer runs no server, collects no analytics, shows no ads, and receives none of your data. Your vault is encrypted on your device with a key derived from your master password; the developer cannot read it and cannot recover it for you.

### 1. What is stored on your device
- Your logins, notes and settings, encrypted with a key protected by your master password (Argon2id + AES-256-GCM). Nothing is readable without the master password (or your recovery key / key file, if you set them up).
- Unlock helpers you choose to enable (fingerprint / face, PIN, pattern). They are protected by the Android Keystore on your device.
- A small local **error log** (Settings > Error log) with the app version, Android version and the technical call stack of the last crash. Exception messages are deliberately left out so your text is never recorded. It never leaves the device unless you copy it yourself, and you can clear it at any time.

Uninstalling the app removes all local data. Android backup and device-transfer of app data are turned off for this app.

### 2. Google Drive backup (optional)
If you sign in with Google, the app uploads one encrypted file (`vault.enc`) to the hidden app-data folder of **your own** Drive (scope `drive.appdata`). It cannot see or touch your other Drive files. Google stores the file but cannot read it, because it does not have your master password. The app also reads the e-mail address of the linked account to show which account is connected; it is not sent anywhere else.

After you edit data the app syncs in the background (and once a day if you turn on the daily backup in Settings), only while you are signed in.

To stop: sign out in Settings, revoke access at myaccount.google.com/permissions, and delete the hidden app data in Google Drive settings.

### 3. Breached-password check (optional)
Only when you open Settings > Security check, tap "Check breached passwords" and confirm, the app sends the **first 5 characters of the SHA-1 hash** of each password to the Pwned Passwords service (`api.pwnedpasswords.com`, Have I Been Pwned) and compares the answer on your device. The password and the rest of the hash never leave the device and no account or identifier is sent. The service sees your IP address, as any web service does. Results are kept in memory only and discarded when the vault locks.

### 4. App updates (optional)
The app is distributed outside Google Play. Only when you open Settings > App update and tap Check for updates or Download (or, if you switch on the automatic check there, at most once a day when the app opens; it is off by default and never downloads or installs anything by itself), the app contacts `api.github.com` to read the releases of the one fixed public repository it was built with and to download the APK. GitHub sees your IP address, as any web service does. No vault data is sent. Before Android offers to install an update, the app checks that it has the same package name, a higher version number and the same signing certificate as the installed app; you confirm every install yourself.

### 5. Things you do that move data out of the app
- **Copy to clipboard:** the item is marked as sensitive and the app clears it after 30 seconds if it is still the one it copied. Other apps with clipboard access on your device may still read it during that time.
- **QR code of a login:** shown only after your passcode / fingerprint check; it contains the password in clear text, the screen cannot be captured, and it closes after 60 seconds. Scanning a QR code uses the Google Play services code scanner (its own camera screen). Pass Show needs no camera permission and only receives the text of the code.
- **Export backup (.psv):** an encrypted file you choose where to save or share.
- **Export CSV:** a **plain-text, unencrypted** file. Anyone who gets the file can read every password in it. Delete it when you no longer need it.
- **Send recovery key to myself:** opens a draft in your mail app addressed only to the Google account linked for Drive. Pass Show sends nothing; you press Send in your mail app, and the key will then be stored in that mailbox.
- **Autofill (only if you turn it on):** the app offers logins to the app or website you are on. For websites it only fills in supported browsers and only on the exact trusted domain over https.

### 6. Permissions
Internet (Drive sync, and the optional breached-password check and app update above); biometrics (unlock); permission to hand a downloaded update to the Android installer; and the Android autofill service (only if you enable it). No camera, contacts, location, microphone or storage permissions.

### 7. Third parties
Google (Drive sign-in and storage, Play services QR scanner), Have I Been Pwned (breach check) and GitHub (updates), each only in the optional cases above and under their own privacy policies. No advertising, analytics or tracking SDKs are included. The developer does not sell or share your data.

### 8. Your control and your responsibility
You can disable or delete every optional feature above at any time. Because the developer holds no copy of your data, **if you lose your master password and your recovery key / key file, your data cannot be recovered by anyone.** Keep your recovery key somewhere safe.

### 9. Children
Pass Show is not directed at children.

### 10. Changes and contact
If this policy changes, the date above changes and the new text ships with the app version it applies to.
Contact: **[your contact e-mail]**

---

## Tiếng Việt

**Tóm tắt.** Pass Show là trình quản lý mật khẩu ưu tiên chạy ngoại tuyến. Nhà phát triển không có máy chủ, không thu thập thống kê, không quảng cáo và không nhận bất kỳ dữ liệu nào của bạn. Kho mật khẩu được mã hóa ngay trên thiết bị bằng khóa sinh từ mật khẩu chính; nhà phát triển không thể đọc và cũng không thể khôi phục giúp bạn.

### 1. Dữ liệu lưu trên thiết bị
- Tài khoản, ghi chú và cài đặt của bạn, được mã hóa bằng khóa do mật khẩu chính bảo vệ (Argon2id + AES-256-GCM). Không có mật khẩu chính (hoặc mã khôi phục / tệp khóa nếu bạn đã thiết lập) thì không đọc được.
- Các cách mở khóa nhanh bạn chọn bật (vân tay / khuôn mặt, PIN, hình vẽ), được bảo vệ bằng Android Keystore trên máy.
- Một **nhật ký lỗi** nhỏ lưu trong máy (Cài đặt > Nhật ký lỗi): phiên bản app, phiên bản Android và chuỗi gọi kỹ thuật của lần lỗi gần nhất. Nội dung thông báo lỗi được cố ý loại bỏ để không ghi lại chữ của bạn. Nhật ký không rời khỏi máy trừ khi bạn tự sao chép, và bạn xóa được bất cứ lúc nào.

Gỡ app sẽ xóa toàn bộ dữ liệu trong máy. Sao lưu và chuyển dữ liệu app của Android bị tắt đối với app này.

### 2. Sao lưu Google Drive (tùy chọn)
Nếu bạn đăng nhập Google, app tải một tệp mã hóa (`vault.enc`) lên thư mục dữ liệu ẩn của app trong Drive **của chính bạn** (quyền `drive.appdata`). App không thấy và không đụng tới các tệp Drive khác. Google lưu tệp nhưng không đọc được vì không có mật khẩu chính của bạn. App cũng đọc địa chỉ e-mail của tài khoản đã liên kết để hiển thị tài khoản nào đang kết nối; địa chỉ này không gửi đi đâu khác.

Sau khi bạn sửa dữ liệu, app đồng bộ ngầm (và mỗi ngày một lần nếu bạn bật sao lưu hằng ngày trong Cài đặt), chỉ khi đang đăng nhập.

Để dừng: đăng xuất trong Cài đặt, thu hồi quyền tại myaccount.google.com/permissions, và xóa dữ liệu ẩn của app trong cài đặt Google Drive.

### 3. Kiểm tra mật khẩu bị lộ (tùy chọn)
Chỉ khi bạn mở Cài đặt > Kiểm tra bảo mật, bấm "Kiểm tra mật khẩu bị lộ" và xác nhận, app mới gửi **5 ký tự đầu của mã băm SHA-1** của từng mật khẩu tới dịch vụ Pwned Passwords (`api.pwnedpasswords.com`, Have I Been Pwned) và so sánh kết quả ngay trên máy. Mật khẩu và phần còn lại của mã băm không rời khỏi máy, không gửi tài khoản hay mã định danh. Dịch vụ thấy địa chỉ IP của bạn như mọi dịch vụ web. Kết quả chỉ giữ trong bộ nhớ và bị xóa khi kho khóa lại.

### 4. Cập nhật app (tùy chọn)
App được phân phối ngoài Google Play. Chỉ khi bạn mở Cài đặt > Cập nhật app và bấm Kiểm tra cập nhật hoặc Tải về (hoặc, nếu bạn bật kiểm tra tự động ở đó, tối đa mỗi ngày một lần khi mở app; mặc định tắt và không bao giờ tự tải hay tự cài), app mới kết nối `api.github.com` để đọc các bản phát hành của đúng một kho công khai cố định mà app được build kèm, và tải tệp APK. GitHub thấy địa chỉ IP của bạn như mọi dịch vụ web. Không có dữ liệu kho nào được gửi. Trước khi Android đề nghị cài, app kiểm tra bản mới có cùng tên gói, số phiên bản cao hơn và cùng chứng chỉ ký với bản đang cài; bạn tự xác nhận mỗi lần cài.

### 5. Những thao tác của bạn đưa dữ liệu ra ngoài app
- **Sao chép vào bộ nhớ tạm:** mục được đánh dấu nhạy cảm và app xóa sau 30 giây nếu vẫn là nội dung do app chép. Trong thời gian đó, ứng dụng khác có quyền đọc bộ nhớ tạm trên máy vẫn có thể đọc được.
- **Mã QR của tài khoản:** chỉ hiện sau khi xác thực mã khóa / vân tay; mã chứa mật khẩu dạng rõ, màn hình không chụp được và tự đóng sau 60 giây. Quét mã QR dùng trình quét của Google Play services (màn hình camera riêng). Pass Show không cần quyền camera và chỉ nhận nội dung chữ của mã.
- **Xuất bản sao lưu (.psv):** tệp đã mã hóa, bạn chọn nơi lưu hoặc chia sẻ.
- **Xuất CSV:** tệp **chữ thường, không mã hóa**. Ai có tệp này đọc được mọi mật khẩu trong đó. Hãy xóa khi không còn cần.
- **Gửi mã khôi phục cho chính mình:** mở bản nháp trong ứng dụng thư, chỉ gửi tới tài khoản Google đã liên kết Drive. Pass Show không gửi gì; bạn tự bấm Gửi, và mã sẽ nằm trong hộp thư đó.
- **Tự điền (chỉ khi bạn bật):** app gợi ý tài khoản cho ứng dụng hoặc trang web bạn đang dùng. Với web, chỉ điền trên trình duyệt được hỗ trợ và chỉ đúng tên miền tin cậy qua https.

### 6. Quyền truy cập
Internet (đồng bộ Drive, và kiểm tra mật khẩu bị lộ, cập nhật app tùy chọn ở trên); sinh trắc học (mở khóa); quyền chuyển bản cập nhật đã tải cho trình cài đặt của Android; và dịch vụ tự điền của Android (chỉ khi bạn bật). Không xin quyền camera, danh bạ, vị trí, micro hay bộ nhớ.

### 7. Bên thứ ba
Google (đăng nhập và lưu trữ Drive, trình quét QR của Play services), Have I Been Pwned (kiểm tra lộ mật khẩu) và GitHub (cập nhật), mỗi bên chỉ trong các trường hợp tùy chọn nêu trên và theo chính sách riêng của họ. App không có SDK quảng cáo, thống kê hay theo dõi. Nhà phát triển không bán hay chia sẻ dữ liệu của bạn.

### 8. Quyền kiểm soát và trách nhiệm của bạn
Bạn có thể tắt hoặc xóa mọi tính năng tùy chọn ở trên bất cứ lúc nào. Vì nhà phát triển không giữ bản sao dữ liệu của bạn, **nếu mất cả mật khẩu chính lẫn mã khôi phục / tệp khóa thì không ai có thể khôi phục dữ liệu.** Hãy cất mã khôi phục ở nơi an toàn.

### 9. Trẻ em
Pass Show không hướng tới trẻ em.

### 10. Thay đổi và liên hệ
Nếu chính sách thay đổi, ngày ở đầu trang sẽ đổi và nội dung mới đi kèm phiên bản app áp dụng.
Liên hệ: **[e-mail liên hệ của bạn]**
