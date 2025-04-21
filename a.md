RedTeam-Tools
<p align="center"> <img src="https://user-images.githubusercontent.com/100603074/210680426-20a92131-56f9-43ad-be82-f449e3215dda.png" height="300"> </p>
Kho lưu trữ GitHub này chứa tập hợp hơn 150+ công cụ và tài nguyên có thể hữu ích cho hoạt động Red Teaming.

Một số công cụ được thiết kế đặc biệt cho red teaming, trong khi những công cụ khác có thể mang tính chất chung và có thể được điều chỉnh để sử dụng trong bối cảnh red teaming.

🔗 Nếu bạn là Blue Teamer, hãy tham khảo BlueTeam-Tools

Cảnh báo

Tài liệu trong kho lưu trữ này chỉ nhằm mục đích cung cấp thông tin và giáo dục. Không được sử dụng cho bất kỳ hoạt động bất hợp pháp nào.

Lưu ý

Ẩn tiêu đề danh sách công cụ bằng biểu tượng mũi tên.

Nhấn 🔙 để quay lại danh sách.

Danh sách công cụ
<details open> <summary><b>Mẹo cho Red Team</b> 19 mẹo</summary> <ul> <li><b><a href="#improved-html-smuggling-with-mouse-move-eventlistener">Cải tiến kỹ thuật HTML smuggling bằng eventlistener di chuyển chuột</a></b><i> @pr0xylife</i></li> <li><b><a href="#google-translate-for-phishing">Dùng Google Translate cho phishing</a></b><i> @malmoeb</i></li> <li><b><a href="#hiding-the-local-admin-account">Ẩn tài khoản admin cục bộ</a></b><i> @Alh4zr3d</i></li> <li><b><a href="#cripple-windows-defender-by-deleting-signatures">Vô hiệu hóa Windows Defender bằng cách xóa chữ ký</a></b><i> @Alh4zr3d</i></li> <li><b><a href="#enable-multiple-rdp-sessions-per-user">Bật nhiều phiên RDP cho mỗi người dùng</a></b><i> @Alh4zr3d</i></li> <li><b><a href="#sysinternals-psexecexe-local-alternative">Thay thế cục bộ cho Sysinternals PsExec.exe</a></b><i> @GuhnooPlusLinux</i></li> <li><b><a href="#live-off-the-land-port-scanner">Dò cổng bằng cách tận dụng công cụ sẵn có</a></b><i> @Alh4zr3d</i></li> <li><b><a href="#proxy-aware-powershell-downloadstring">PowerShell DownloadString có hỗ trợ proxy</a></b><i> @Alh4zr3d</i></li> <li><b><a href="#looking-for-internal-endpoints-in-browser-bookmarks">Tìm endpoint nội bộ trong bookmark trình duyệt</a></b><i> @Alh4zr3d</i></li> <li><b><a href="#query-dns-records-for-enumeration">Truy vấn bản ghi DNS để enumeration</a></b><i> @Alh4zr3d</i></li> <li><b><a href="#unquoted-service-paths-without-powerup">Tìm đường dẫn dịch vụ không trích dẫn mà không cần PowerUp</a></b><i> @Alh4zr3d</i></li> <li><b><a href="#bypass-a-disabled-command-prompt-with-k">Vượt qua lệnh cmd bị khóa bằng /k</a></b><i> Martin Sohn Christensen</i></li> <li><b><a href="#stop-windows-defender-deleting-mimikatzexe">Ngăn Defender xóa mimikatz.exe</a></b><i> @GuhnooPlusLinux</i></li> <li><b><a href="#check-if-you-are-in-a-virtual-machine">Kiểm tra xem bạn có đang ở trong máy ảo không</a></b><i> @dmcxblue</i></li> <li><b><a href="#enumerate-applocker-rules">Liệt kê các rule của AppLocker</a></b><i> @Alh4zr3d</i></li> <li><b><a href="#cmd-shortcut-with-6-pixels-via-mspaint">Tạo lối tắt CMD bằng 6 điểm ảnh trong MSPaint</a></b><i> PenTestPartners</i></li> <li><b><a href="#link-spoofing-with-preventdefault-javascript-method">Giả mạo liên kết bằng phương thức JavaScript PreventDefault</a></b></li> <li><b><a href="#check-smb-firewall-rules-with-responder">Kiểm tra rule tường lửa SMB bằng Responder</a></b><i> @malmoeb</i></li> <li><b><a href="#disable-av-with-sysinternals-pssuspend">Vô hiệu hóa phần mềm AV bằng PsSuspend của Sysinternals</a></b><i> @0gtweet</i></li> </ul> </details>
Reconnaissance — Trinh sát
🔍 Tổng quan: Giai đoạn thu thập thông tin về mục tiêu, bao gồm tên miền phụ, dữ liệu OSINT, cấu hình DNS, dịch vụ chạy, lỗ hổng công khai...

🔙 spiderfoot
Công cụ tự động hoá OSINT

SpiderFoot tích hợp gần như mọi nguồn dữ liệu có sẵn và sử dụng nhiều phương pháp phân tích để thu thập thông tin một cách trực quan.

Cài đặt:

bash
Copy code
wget https://github.com/smicallef/spiderfoot/archive/v4.0.tar.gz
tar zxvf v4.0.tar.gz
cd spiderfoot-4.0
pip3 install -r requirements.txt
Sử dụng:

bash
Copy code
python3 ./sf.py -l 127.0.0.1:5001
🔙 reconftw
Tự động hoá toàn bộ quá trình trinh sát

Tự động tìm tên miền phụ, quét lỗ hổng, và thu thập thông tin mục tiêu.

Cài đặt:

bash
Copy code
git clone https://github.com/six2dez/reconftw.git;cd reconftw/;./install.sh
Sử dụng:

bash
Copy code
# Một mục tiêu đơn
./reconftw.sh -d target.com -r

# Nhiều tên miền
./reconftw.sh -m target -l domains.txt -r

# Trinh sát thụ động
./reconftw.sh -d target.com -p

# Tối đa hoá kiểm tra và khai thác
./reconftw.sh -d target.com -a
🛠 Một số công cụ khác trong nhóm Reconnaissance gồm:
subzy – Kiểm tra lỗ hổng takeover subdomain
smtp-user-enum – Liệt kê người dùng SMTP
crt.sh → httprobe → EyeWitness – Tự động chụp ảnh giao diện web từ crt.sh
jsendpoints – Trích xuất liên kết từ DOM của trang
nuclei – Trình quét lỗ hổng mạnh mẽ
certSniff – Theo dõi từ kho chứng chỉ transparency
gobuster – Brute-force đường dẫn website
feroxbuster – Phát hiện nội dung nhanh, viết bằng Rust
cloudbrute – Brute-force hạ tầng đám mây
dnsrecon – Liệt kê bản ghi DNS
shodan.io – Tìm kiếm hệ thống công khai
AORT – Tập hợp công cụ subdomain enumeration
spoofcheck – Kiểm tra bản ghi SPF/DMARC
