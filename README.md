# Công cụ Red Team

<p align="center">
<img src="[https://user-images.githubusercontent.com/100603074/210680426-20a92131-56f9-43ad-be82-f449e3215dda.png](https://user-images.githubusercontent.com/100603074/210680426-20a92131-56f9-43ad-be82-f449e3215dda.png)" height="300">
</p>

Kho lưu trữ **github** này chứa một bộ sưu tập gồm **hơn 150 công cụ** và **tài nguyên** có thể hữu ích cho các **hoạt động red team**.
 Một số công cụ có thể được thiết kế đặc biệt cho **hoạt động red team**, trong khi những công cụ khác mang tính tổng quát hơn và có thể được điều chỉnh để sử dụng trong **bối cảnh red team**.
 > 🔗 Nếu bạn là một **Blue Teamer**, hãy xem [BlueTeam-Tools](https://github.com/A-poc/BlueTeam-Tools)

> **Cảnh báo**
>
> *Các tài liệu trong kho lưu trữ này chỉ dành cho mục đích thông tin và giáo dục.
[source: 4] Chúng không nhằm mục đích sử dụng trong bất kỳ hoạt động bất hợp pháp nào.*

> **Lưu ý**
>
> *Ẩn các tiêu đề Danh sách Công cụ bằng mũi tên.*
>
> *Nhấp vào 🔙 để quay lại danh sách.*

# Danh sách Công cụ
<details open>
    <summary><b>Mẹo Red Team</b> 19 mẹo</summary>
    <ul>
        <ul>
        	<li><b><a href="#improved-html-smuggling-with-mouse-move-eventlistener">Cải thiện **HTML smuggling** bằng **mouse move eventlistener**</a></b><i> @pr0xylife</i></li>
        	<li><b><a href="#google-translate-for-phishing">**Google translate** cho **phishing**</a></b><i> @malmoeb</i></li>
            <li><b><a href="#hiding-the-local-admin-account">Ẩn **tài khoản admin cục bộ**</a></b><i> @Alh4zr3d</i></li>
  
[source: 5]           <li><b><a href="#cripple-windows-defender-by-deleting-signatures">Làm tê liệt **windows defender** bằng cách xóa **signatures**</a></b><i> @Alh4zr3d</i></li>
            <li><b><a href="#enable-multiple-rdp-sessions-per-user">Cho phép nhiều phiên **RDP** cho mỗi người dùng</a></b><i> @Alh4zr3d</i></li>
            <li><b><a href="#sysinternals-psexecexe-local-alternative">Giải pháp thay thế cục bộ cho **Sysinternals** **PsExec.exe**</a></b><i> @GuhnooPlusLinux</i></li>
            <li><b><a href="#live-off-the-land-port-scanner">**Port scanner** theo kiểu **Live off the land**</a></b><i> @Alh4zr3d</i></li>
            <li><b><a href="#proxy-aware-powershell-downloadstring">**PowerShell DownloadString** nhận biết **Proxy**</a></b><i> @Alh4zr3d</i></li>
           
[source: 6]  <li><b><a href="#looking-for-internal-endpoints-in-browser-bookmarks">Tìm kiếm các **endpoint** nội bộ trong bookmark trình duyệt</a></b><i> @Alh4zr3d</i></li>
            <li><b><a href="#query-dns-records-for-enumeration">Truy vấn bản ghi **DNS** để thu thập thông tin</a></b><i> @Alh4zr3d</i></li>
            <li><b><a href="#unquoted-service-paths-without-powerup">**Đường dẫn dịch vụ không được trích dẫn** mà không cần **PowerUp**</a></b><i> @Alh4zr3d</i></li>
            <li><b><a href="#bypass-a-disabled-command-prompt-with-k">Vượt qua **command prompt** bị vô hiệu hóa bằng **/k**</a></b><i> Martin Sohn Christensen</i></li>
            <li><b><a href="#stop-windows-defender-deleting-mimikatzexe">Ngăn chặn **windows defender** xóa **mimikatz.exe**</a></b><i> @GuhnooPlusLinux</i></li>
            <li><b><a href="#check-if-you-are-in-a-virtual-machine">Kiểm tra xem 
[source: 7] bạn có đang ở trong **máy ảo** hay không</a></b><i> @dmcxblue</i></li>
            <li><b><a href="#enumerate-applocker-rules">Liệt kê các quy tắc **AppLocker**</a></b><i> @Alh4zr3d</i></li>
            <li><b><a href="#cmd-shortcut-with-6-pixels-via-mspaint">Shortcut **CMD** với 6 pixel thông qua **mspaint**</a></b><i> PenTestPartners</i></li>
            <li><b><a href="#link-spoofing-with-preventdefault-javascript-method">**Giả mạo liên kết** bằng phương thức **JavaScript** **PreventDefault**</a></b><i> </i></li>
            <li><b><a href="#check-smb-firewall-rules-with-responder">Kiểm tra quy tắc tường lửa **SMB** bằng **Responder**</a></b><i> @malmoeb</i></li>
            <li><b><a href="#disable-av-with-sysinternals-pssuspend">Vô hiệu hóa **AV** bằng **SysInternals** **PsSuspend**</a></b><i> @0gtweet</i></li>
  
[source: 8]       </ul>
    </ul>        
</details>
<details open>
    <summary><b>Thu thập Thông tin (Reconnaissance)</b> 24 công cụ</summary>
    <ul>
        <ul>
            <li><b><a href="#spiderfoot">**spiderfoot**</a></b><i> **OSINT** tự động và **lập bản đồ bề mặt tấn công (attack surface mapping)**</i></li>
            <li><b><a href="#reconftw">**reconftw**</a></b><i> Công cụ tự động **thu thập thông tin tên miền phụ (subdomain)** và **lỗ hổng (vulnerability recon)**</i></li>
            <li><b><a href="#subzy">**subzy**</a></b><i> Công cụ kiểm tra **lỗ hổng chiếm quyền tên miền phụ (Subdomain takeover vulnerability)**</i></li>
        
[source: 9]     <li><b><a href="#smtp-user-enum">**smtp-user-enum**</a></b><i> **Liệt kê người dùng SMTP (SMTP user enumeration)**</i></li>
            <li><b><a href="#crtsh---httprobe---eyewitness">**crt.sh** -> **httprobe** -> **EyeWitness**</a></b><i> Tự động chụp ảnh màn hình tên miền</i></li>
            <li><b><a href="#jsendpoints">**jsendpoints**</a></b><i> Trích xuất các liên kết **DOM** của trang</i></li>
            <li><b><a href="#nuclei">**nuclei**</a></b><i> **Trình quét lỗ hổng (Vulnerability scanner)**</i></li>
            <li><b><a href="#certsniff">**certSniff**</a></b><i> Công cụ dò từ khóa trong **log minh bạch chứng chỉ (Certificate transparency log)**</i></li>
            <li><b><a href="#gobuster">**gobuster**</a></b><i> **Brute force** đường dẫn trang web</i></li>
[source: 10]        <li><b><a href="#feroxbuster">**feroxbuster**</a></b><i> Công cụ khám phá nội dung nhanh được viết bằng **Rust**</i></li>
            <li><b><a href="#cloudbrute">**CloudBrute**</a></b><i> **Brute force** hạ tầng đám mây (**Cloud**)</i></li>
            <li><b><a href="#dnsrecon">**dnsrecon**</a></b><i> Liệt kê bản ghi **DNS**</i></li>
            <li><b><a href="#shodanio">**Shodan.io**</a></b><i> Cơ sở tri thức về các hệ thống public</i></li>
            <li><b><a href="#aort">**AORT** (All in One Recon Tool)</a></b><i> **Liệt kê tên miền phụ (Subdomain enumeration)**</i></li>
            <li><b><a href="#spoofcheck">**spoofcheck**</a></b><i> 
[source: 11] Công cụ kiểm tra bản ghi **SPF**/**DMARC**</i></li>
            <li><b><a href="#awsbucketdump">**AWSBucketDump**</a></b><i> Liệt kê **bucket S3 (S3 bucket enumeration)**</i></li>
            <li><b><a href="#githarvester">**GitHarvester**</a></b><i> Công cụ tìm kiếm **thông tin xác thực GitHub (GitHub credential)**</i></li>
            <li><b><a href="#trufflehog">**truffleHog**</a></b><i> Công cụ quét **thông tin xác thực GitHub (GitHub credential scanner)**</i></li>
<li><b><a href="#dismap">**Dismap**</a></b><i> Khám phá/Nhận dạng tài sản (**Asset discovery**/**identification**)</i></li>
            <li><b><a href="#enum4linux">**enum4linux**</a></b><i> Liệt kê thông tin **Windows**/**Samba (samba enumeration)**</i></li>
            <li><b><a href="#skanuvaty">**skanuvaty**</a></b><i> **Trình quét dns**/**mạng (network)**/**cổng (port scanner)** cực nhanh</i></li>
   
[source: 12]          <li><b><a href="#metabigor">**Metabigor**</a></b><i> Công cụ **OSINT** không cần **API**</i></li>
            <li><b><a href="#gitrob">**Gitrob**</a></b><i> Công cụ quét thông tin nhạy cảm trên **GitHub**</i></li>
            <li><b><a href="#gowitness">**gowitness**</a></b><i> Tiện ích chụp ảnh màn hình web sử dụng **Chrome Headless**</i></li>
        </ul>
    </ul>
</details>
<details open>
    <summary><b>Phát triển Tài nguyên (Resource Development)</b> 12 công cụ</summary>
    <ul>
        <ul>
            <li><b><a href="#remoteinjector">**remoteinjector**</a></b><i> Chèn liên kết mẫu (template) từ xa 
[source: 13] vào **tài liệu word (word document)**</i></li>
            <li><b><a href="#chimera">**Chimera**</a></b><i> Làm rối mã **PowerShell (PowerShell obfuscation)**</i></li>
            <li><b><a href="#msfvenom">**msfvenom**</a></b><i> Tạo **Payload (Payload creation)**</i></li>
            <li><b><a href="#shellter">**Shellter**</a></b><i> Công cụ **tiêm shellcode (shellcode injection)** động</i></li>
            <li><b><a href="#freeze">**Freeze**</a></b><i> Tạo **Payload (Payload creation)** (vượt qua **EDR**)</i></li>
            <li><b><a href="#wordsteal">**WordSteal**</a></b><i> Đánh cắp **hash NTML (NTML hashes)** bằng **Microsoft Word**</i></li>
            <li><b><a href="#ntapi-undocumented-functions">**NTAPI Undocumented Functions**</a></b><i> **Nhân Windows NT (Windows NT Kernel)**, **Native API** và **trình điều khiển (drivers)**</i></li>
[source: 14] 
            <li><b><a href="#kernel-callback-functions">**Kernel Callback Functions**</a></b><i> Các **API Windows (Windows APIs)** không được tài liệu hóa</i></li>
            <li><b><a href="#offensivevba">**OffensiveVBA**</a></b><i> Kỹ thuật thực thi mã **macro Office (Office macro code execution)** và kỹ thuật tránh né</i></li>
            <li><b><a href="#wsh">**WSH**</a></b><i> **Payload Wsh (Wsh payload)**</i></li>
            <li><b><a href="#hta">**HTA**</a></b><i> **Payload Hta (Hta payload)**</i></li>
            <li><b><a href="#vba">**VBA**</a></b><i> **Payload Vba (Vba payload)**</i></li>
        
[source: 15] </ul>
    </ul>
</details>
<details open>
    <summary><b>Tiếp cận Ban đầu (Initial Access)</b> 10 công cụ</summary>
    <ul>
        <ul>
            <li><b><a href="#credmaster">**CredMaster**</a></b><i> Công cụ **password spraying** **CredKing**</i></li>
            <li><b><a href="#trevorspray">**TREVORspray**</a></b><i> **Công cụ dò mật khẩu (Password sprayer)** với **luồng (threading)**</i></li>
            <li><b><a href="#evilqr">**evilqr**</a></b><i> **PoC phishing** **QRLJacking**</i></li>
            <li><b><a href="#cupp">**CUPP**</a></b><i> Common User Passwords Profiler (**CUPP**)</i></li>
        
[source: 16]     <li><b><a href="#bash-bunny">**Bash Bunny**</a></b><i> Công cụ **tấn công USB (USB attack)**</i></li>
            <li><b><a href="#evilgophish">**EvilGoPhish**</a></b><i> Framework **chiến dịch phishing (Phishing campaign)**</i></li>
            <li><b><a href="#social-engineer-toolkit-set">**The Social-Engineer Toolkit**</a></b><i> Framework **chiến dịch phishing (Phishing campaign)**</i></li>
            <li><b><a href="#hydra">**Hydra**</a></b><i> Công cụ **Brute force**</i></li>
            <li><b><a href="#squarephish">**SquarePhish**</a></b><i> Framework **phishing** **OAuth**/**mã QR (QR code)**</i></li>
            <li><b><a href="#king-phisher">**King Phisher**</a></b><i> Framework **chiến dịch phishing (Phishing campaign)**</i></li>
       
[source: 17]  </ul>
    </ul>
</details>
<details open>
    <summary><b>Thực thi (Execution)</b> 13 công cụ</summary>
    <ul>
        <ul>
            <li><b><a href="#responder">**Responder**</a></b><i> Công cụ đầu độc **LLMNR**, **NBT-NS** và **MDNS (MDNS poisoner)**</i></li>
            <li><b><a href="#secretsdump">**secretsdump**</a></b><i> Công cụ dump **hash (hash dumper)** từ xa</i></li>
            <li><b><a href="#evil-winrm">**evil-winrm**</a></b><i> **Shell WinRM (WinRM shell)**</i></li>
            <li><b><a href="#donut">**Donut**</a></b><i> Thực thi **.NET** trong bộ nhớ (**In-memory .NET execution**)</i></li>
           
[source: 18]  <li><b><a href="#macro_pack">**Macro_pack**</a></b><i> Làm rối mã **Macro (Macro obfuscation)**</i></li>
            <li><b><a href="#powersploit">**PowerSploit**</a></b><i> Bộ **script PowerShell (PowerShell script suite)**</i></li>
            <li><b><a href="#rubeus">**Rubeus**</a></b><i> Công cụ **hack Active Directory (Active directory hack)**</i></li>
<li><b><a href="#sharpup">**SharpUp**</a></b><i> Công cụ nhận dạng **lỗ hổng Windows (Windows vulnerability)**</i></li>
            <li><b><a href="#sqlrecon">**SQLRecon**</a></b><i> Bộ công cụ tấn công **MS-SQL**</i></li>
            <li><b><a href="#ultimateapplockerbypasslist">**UltimateAppLockerByPassList**</a></b><i> Các kỹ thuật **Vượt qua AppLocker (AppLocker Bypass)** phổ biến</i></li>
            <li><b><a href="#starfighters">**StarFighters**</a></b><i> 
[source: 19] **Trình khởi chạy Empire (Empire Launcher)** dựa trên **JavaScript** và **VBScript**</i></li>
            <li><b><a href="#demiguise">**demiguise**</a></b><i> Công cụ **mã hóa HTA (HTA encryption)**</i></li>
            <li><b><a href="#powerzure">**PowerZure**</a></b><i> **Framework PowerShell** để đánh giá **bảo mật Azure (Azure security)**</i></li>
        </ul>
    </ul>
</details>
<details open>
    <summary><b>Duy trì Truy cập (Persistence)</b> 4 công cụ</summary>
    <ul>
        <ul>
            <li><b><a href="#impacket">**Impacket**</a></b><i> Bộ **script Python (Python script suite)**</i></li>
            <li><b><a 
[source: 20] href="#empire">**Empire**</a></b><i> **Framework sau khai thác (Post-exploitation framework)**</i></li>
            <li><b><a href="#sharpersist">**SharPersist**</a></b><i> Bộ công cụ **duy trì truy cập Windows (Windows persistence)**</i></li>
            <li><b><a href="#ligolo-ng">**ligolo-ng**</a></b><i> Công cụ **tạo đường hầm (Tunneling)** sử dụng **giao diện TUN (TUN interface)**</i></li>
        </ul>
    </ul>
</details>
<details open>
    <summary><b>Leo thang Đặc quyền (Privilege Escalation)</b> 11 công cụ</summary>
    <ul>
        <ul>
            <li><b><a href="#crassus">**Crassus**</a></b><i> Công cụ khám phá **leo thang đặc quyền Windows (Windows privilege escalation)**</i></li>
            
[source: 21] <li><b><a href="#linpeas">**LinPEAS**</a></b><i> **Leo thang đặc quyền Linux (Linux privilege escalation)**</i></li>
            <li><b><a href="#winpeas">**WinPEAS**</a></b><i> **Leo thang đặc quyền Windows (Windows privilege escalation)**</i></li>
            <li><b><a href="#linux-smart-enumeration">**linux-smart-enumeration**</a></b><i> **Leo thang đặc quyền Linux (Linux privilege escalation)**</i></li>
            <li><b><a href="#certify">**Certify**</a></b><i> **Leo thang đặc quyền Active Directory (Active directory privilege escalation)**</i></li>
            <li><b><a href="#get-gpppassword">**Get-GPPPassword**</a></b><i> Trích xuất **mật khẩu Windows (Windows password extraction)**</i></li>
            <li><b><a href="#sherlock">**Sherlock**</a></b><i> Công cụ **leo thang đặc quyền PowerShell (PowerShell privilege escalation)**</i></li>
            <li><b><a href="#watson">**Watson**</a></b><i> 
[source: 22] Công cụ **leo thang đặc quyền Windows (Windows privilege escalation)**</i></li>
            <li><b><a href="#impulsivedllhijack">**ImpulsiveDLLHijack**</a></b><i> Công cụ **DLL Hijack**</i></li>
            <li><b><a href="#adfsdump">**ADFSDump**</a></b><i> Công cụ **dump AD FS (AD FS dump)**</i></li> 
            <li><b><a href="#beroot">**BeRoot**</a></b><i> Dự án **Leo thang Đặc quyền (Privilege Escalation)** Đa **Hệ điều hành (OS)**</i></li>
        </ul>
    </ul>
</details>
<details open>
    <summary><b>Lẩn tránh Phòng thủ (Defense Evasion)</b> 8 công cụ</summary>
    <ul>
        <ul>
            <li><b><a 
[source: 23] href="#invoke-obfuscation">**Invoke-Obfuscation**</a></b><i> Công cụ làm rối mã **Script (Script obfuscator)**</i></li>
	        <li><b><a href="#veil">**Veil**</a></b><i> Công cụ làm rối mã **payload Metasploit (Metasploit payload obfuscator)**</i></li>
            <li><b><a href="#sharpblock">**SharpBlock**</a></b><i> **Vượt qua EDR (EDR bypass)** thông qua ngăn chặn thực thi điểm nhập (**entry point execution prevention**)</i></li>
            <li><b><a href="#alcatraz">**Alcatraz**</a></b><i> Công cụ làm rối mã **nhị phân x64 (x64 binary obfuscator)** có **giao diện đồ họa (GUI)**</i></li>
            <li><b><a href="#mangle">**Mangle**</a></b><i> Thao tác **tệp thực thi (executable manipulation)** đã biên dịch</i></li>
            <li><b><a href="#amsi-fail">**AMSI Fail**</a></b><i> Các **đoạn mã PowerShell (PowerShell snippets)** làm hỏng hoặc vô hiệu hóa **AMSI**</i></li>
            
[source: 24] <li><b><a href="#scarecrow">**ScareCrow**</a></b><i> **Framework tạo payload (Payload creation framework)** được thiết kế xoay quanh việc **vượt qua EDR (EDR bypass)**</i></li>
            <li><b><a href="#moonwalk">**moonwalk**</a></b><i> Công cụ xóa **log hệ thống Linux (Linux system log)** và **dấu thời gian hệ thống tệp (filesystem timestamp)**</i></li>
        </ul>
    </ul>
</details>
<details open>
    <summary><b>Truy cập Thông tin Xác thực (Credential Access)</b> 11 công cụ</summary>
    <ul>
        <ul>
            <li><b><a href="#mimikatz">**Mimikatz**</a></b><i> Trình trích xuất **thông tin xác thực Windows (Windows credential)**</i></li>
            <li><b><a href="#lazagne">**LaZagne**</a></b><i> Trình trích xuất **mật khẩu cục bộ (local password extractor)**</i></li>
        
[source: 25]     <li><b><a href="#hashcat">**hashcat**</a></b><i> Bẻ khóa **hash mật khẩu (Password hash cracking)**</i></li>
            <li><b><a href="#john-the-ripper">**John the Ripper**</a></b><i> Bẻ khóa **hash mật khẩu (Password hash cracking)**</i></li>
	        <li><b><a href="#scomdecrypt">**SCOMDecrypt**</a></b><i> Công cụ **Giải mã Thông tin Xác thực SCOM (SCOM Credential Decryption)**</i></li>
	        <li><b><a href="#nanodump">**nanodump**</a></b><i> Tạo **minidump tiến trình LSASS (LSASS process minidump)**</i></li>
<li><b><a href="#eviltree">**eviltree**</a></b><i> Bản làm lại của Tree cho việc **khám phá thông tin xác thực (credential discovery)**</i></li>
	        <li><b><a href="#seeyoucm-thief">**SeeYouCM-Thief**</a></b><i> Phân tích **tệp cấu hình hệ thống điện thoại Cisco (Cisco phone systems configuration file parsing)**</i></li>
            <li><b><a href="#mailsniper">**MailSniper**</a></b><i> Công cụ Tìm kiếm Thư **Microsoft Exchange (Microsoft Exchange Mail Searcher)**</i></li>
  
[source: 26]           <li><b><a href="#sharpchromium">**SharpChromium**</a></b><i> Trình trích xuất **Cookie**, **lịch sử (history)** và **thông tin đăng nhập đã lưu (saved login)** của **Chromium**</i></li>
            <li><b><a href="#dploot">**dploot**</a></b><i> Thu thập **DPAPI (DPAPI looting)** từ xa bằng **Python**</i></li>
        </ul>
    </ul>
</details>
<details open>
    <summary><b>Khám phá (Discovery)</b> 6 công cụ</summary>
    <ul>
        <ul>
            <li><b><a href="#pcredz">**PCredz**</a></b><i> Khám phá **Thông tin xác thực (Credential discovery)** từ **PCAP**/**giao diện trực tiếp (live interface)**</i></li>
            <li><b><a href="#pingcastle">**PingCastle**</a></b><i> Công cụ đánh giá **Active Directory** [source: 27] (Active directory assessor)</i></li>
    	    <li><b><a href="#seatbelt">**Seatbelt**</a></b><i> **Trình quét lỗ hổng (vulnerability scanner)** cục bộ</i></li>
<li><b><a href="#adrecon">**ADRecon**</a></b><i> **Thu thập thông tin Active Directory (Active directory recon)**</i></li>
    	    <li><b><a href="#adidnsdump">**adidnsdump**</a></b><i> **Dump DNS tích hợp Active Directory (Active Directory Integrated DNS dumping)**</i></li>
    	    <li><b><a href="#scavenger">**scavenger**</a></b><i> Công cụ quét để lùng sục hệ thống (scavenging systems)</i></li>
        </ul>
    </ul>
</details>
<details open>
    <summary><b>Di chuyển Ngang (Lateral Movement)</b> 12 công cụ</summary>
    <ul>
        <ul>
            <li><b><a href="#crackmapexec">**crackmapexec**</a></b><i> Bộ công cụ **di chuyển ngang (lateral movement)** **Windows**/**Active Directory** [source: 28] </i></li>
            <li><b><a href="#wmiops">**WMIOps**</a></b><i> **Lệnh WMI từ xa (WMI remote commands)**</i></li>
            <li><b><a href="#powerlessshell">**PowerLessShell**</a></b><i> **PowerShell** từ xa không cần **PowerShell**</i></li>
            <li><b><a href="#psexec">**PsExec**</a></b><i> Công cụ thay thế **telnet** hạng nhẹ</i></li>
            <li><b><a href="#liquidsnake">**LiquidSnake**</a></b><i> **Di chuyển ngang không cần tệp (Fileless lateral movement)**</i></li>
            <li><b><a href="#enabling-rdp">Bật RDP</a></b><i> Lệnh bật **RDP Windows (Windows RDP)**</i></li>
            <li><b><a href="#upgrading-shell-to-meterpreter">Nâng cấp shell lên 
[source: 29] **meterpreter**</a></b><i> Cải thiện **Reverse shell**</i></li>
<li><b><a href="#forwarding-ports">Chuyển tiếp Cổng (Forwarding Ports)</a></b><i> Lệnh **chuyển tiếp cổng (port forward)** cục bộ</i></li>
            <li><b><a href="#jenkins-reverse-shell">**Reverse shell** **Jenkins**</a></b><i> Lệnh **shell Jenkins**</i></li>
            <li><b><a href="#adfspoof">**ADFSpoof**</a></b><i> Giả mạo **token bảo mật AD FS (AD FS security tokens)**</i></li>
            <li><b><a href="#kerbrute">**kerbrute**</a></b><i> Công cụ thực hiện **bruteforce Kerberos pre-auth (Kerberos pre-auth bruteforcing)**</i></li>
            <li><b><a href="#coercer">**Coercer**</a></b><i> Ép buộc **máy chủ Windows (Windows server)** xác thực</i></li>
    
[source: 30]         <li><b><a href="#wmiops">**WMIOps**</a></b><i> **Lệnh WMI từ xa (WMI remote commands)**</i></li>
        </ul>
    </ul>
</details>
<details open>
    <summary><b>Thu thập (Collection)</b> 3 công cụ</summary>
    <ul>
        <ul>
            <li><b><a href="#bloodhound">**BloodHound**</a></b><i> Trực quan hóa **Active Directory (Active directory visualisation)**</i></li>
            <li><b><a href="#snaffler">**Snaffler**</a></b><i> Công cụ thu thập **thông tin xác thực Active Directory (Active directory credential)**</i></li>
            <li><b><a href="#linwinpwn">**linWinPwn**</a></b><i> **Liệt kê Active Directory (Active Directory Enumeration)** và kiểm tra **Lỗ hổng (Vulnerability checks)**</i></li>
     
[source: 31]    </ul>
    </ul>
</details>
<details open>
    <summary><b>Chỉ huy và Điều khiển (Command and Control)</b> 9 công cụ</summary>
    <ul>
        <ul>
            <li><b><a href="#living-off-trusted-sites-project">**Living Off Trusted Sites Project**</a></b><i> Tận dụng các tên miền hợp pháp cho **C2** của bạn</i></li>
            <li><b><a href="#havoc">**Havoc**</a></b><i> **Framework chỉ huy và điều khiển (Command and control framework)**</i></li>
    	    <li><b><a href="#covenant">**Covenant**</a></b><i> **Framework chỉ huy và điều khiển (.NET) (Command and control framework (.NET))**</i></li>
    	    <li><b><a href="#merlin">**Merlin**</a></b><i> **Framework chỉ huy và điều khiển (Golang) (Command and control framework (Golang))**</i></li>
    
[source: 32] 	    <li><b><a href="#metasploit-framework">**Metasploit Framework**</a></b><i> **Framework chỉ huy và điều khiển (Ruby) (Command and control framework (Ruby))**</i></li>
<li><b><a href="#pupy">**Pupy**</a></b><i> **Framework chỉ huy và điều khiển (Python) (Command and control framework (Python))**</i></li>
    	    <li><b><a href="#brute-ratel">**Brute Ratel**</a></b><i> **Framework chỉ huy và điều khiển ($$$) (Command and control framework ($$$))**</i></li>
            <li><b><a href="#nimplant">**NimPlant**</a></b><i> **Implant C2 (C2 implant)** được viết bằng **Nim**</i></li>
            <li><b><a href="#hoaxshell">**Hoaxshell**</a></b><i> **Reverse shell PowerShell**</i></li>
        </ul>
    </ul>
</details>
<details open>
    <summary><b>Rút trích Dữ liệu (Exfiltration)</b> 5 công cụ</summary>
    <ul>
   
[source: 33]      <ul>
	        <li><b><a href="#dnscat2">**Dnscat2**</a></b><i> **C2** thông qua **tạo đường hầm DNS (DNS tunneling)**</i></li>
	        <li><b><a href="#cloakify">**Cloakify**</a></b><i> **Chuyển đổi dữ liệu (Data transformation)** cho việc **rút trích (exfiltration)**</i></li>
            <li><b><a href="#pyexfil">**PyExfil**</a></b><i> **PoC Rút trích Dữ liệu (Data exfiltration PoC)**</i></li>
            <li><b><a href="#powershell-rat">**Powershell RAT**</a></b><i> **Backdoor** dựa trên **Python**</i></li>
            <li><b><a href="#gd-thief">**GD-Thief**</a></b><i> Rút trích dữ liệu **Google Drive (Google drive exfiltration)**</i></li>
        </ul>
    </ul>
</details>
<details open>
    <summary><b>Gây ảnh hưởng (Impact)</b> 4 công cụ</summary>
 
[source: 34]    <ul>
        <ul>
            <li><b><a href="#conti-pentester-guide-leak">**Conti Pentester Guide Leak**</a></b><i> Bộ công cụ chi nhánh của nhóm **ransomware Conti**</i></li>
            <li><b><a href="#slowloris">**SlowLoris**</a></b><i> **Tấn công từ chối dịch vụ (denial of service)** đơn giản</i></li>
            <li><b><a href="#usbkill">**usbkill**</a></b><i> **Công tắc hủy chống điều tra số (Anti-forensic kill-switch)**</i></li>
            <li><b><a href="#keytap">**Keytap**</a></b><i> Lấy các phím đã nhấn từ âm thanh gõ phím</i></li>
        </ul>
    </ul>
</details>
[source: 35]
