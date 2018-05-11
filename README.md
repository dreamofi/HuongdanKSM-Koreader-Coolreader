# HƯỚNG DẪN CÀI ĐẶT & SỬ DỤNG KSM, KOREADER VÀ COOLREADER CHO MÁY ĐỌC SÁCH KOBO
_Viết bằng FocusWriter, chạy trên Linux Mint 18.2, ngày 27/8/2017_
# Mục lục
1. Giới thiệu về Kobo Start Menu, Koreader và Coolreader<br>
1.1. Giới thiệu về Kobo Start Menu (KSM)<br>
1.2. Giới thiệu về Koreader<br>
1.3. Giới thiệu về Coolreader<br>
2. Cách cài đặt KSM<br>
2.1. Lưu ý trước khi cài đặt<br>
2.2. Tiến hành cài đặt<br>
2.2.1. Cài đặt KSM<br>
2.2.2. Cài đặt patch bổ sung cho KSM<br>
2.2.2.1. Cảnh báo<br>
2.2.2.2. Các bước cài patch cho các máy Kobo đời trước Aura H2O Edition 2<br>
2.2.3. Gỡ bỏ KSM<br>
3. Sử dụng Koreader<br>
3.1. Lưu ý trước khi cài đặt<br>
3.2. Tiến hành cài đặt<br>
3.3. Hướng dẫn sử dụng cơ bản<br>
3.3.1. Giao diện sử dụng (đang cập nhật)<br>
3.3.2. Cài đặt thêm từ điển<br>
3.3.3. Cài đặt thêm font<br>
4. Sử dụng Coolreader<br>
4.1. Cài đặt<br>
4.2. Hướng dẫn sử dụng cơ bản<br>
5. Khắc mục một số vấn đề khi sử dụng KSM / Koreader & Coolreader (còn cập nhật)<br>
5.1. KSM/Koreader/Coolreader hay bị đơ<br>
6. Nguồn tham khảo<br>

## 1. Giới thiệu về Kobo Start Menu, Koreader và Coolreader
### 1.1. Giới thiệu về Kobo Start Menu (KSM)
Kobo Start Menu là ứng dụng cài thêm cho máy đọc sách Kobo, với tính năng chính là:
- Cho phép chuyển qua lại và quản lý các ứng dụng đọc sách (ứng dụng đọc sách mặc định của Kobo có tên là Nickel, các ứng dụng có thể cài đặt bổ sung phổ biến là Koreader và Coolreader) và quản lý các bản cập nhật, cài đặt firmware.
- Chạy các đoạn mã từ bộ nhớ trong và thẻ nhớ ngoài (hệ điều hành mà Kobo sử dụng dựa trên nền Linux, do vậy các đoạn mã (script) thường có đuôi .sh, bác nào dùng Linux thì có thể xem code trong các file này)
- Chạy Terminal (cái này em không đi vào chi tiết, bác nào rành Linux thì nghiên cứu thêm nhé :D)
- Quản lý, tải và cài đặt các bản cập nhật mới  (firmware) cho máy mà vẫn giữ lại được KSM (bình thường nếu không chạy cập nhật thông qua KSM thì KSM sẽ bị xóa).

### 1.2. Giới thiệu về Koreader
Koreader là ứng dụng đọc sách mở rộng cho máy đọc sách của Kobo và Kindle (trong phạm vi hướng dẫn này thì em chỉ giới hạn ở máy Kobo), ưu điểm chính so với Nickel là:
- Đọc được nhiều định dạng file, đặc biệt xử lý PDF nhanh hơn so với Nickel. Các file hỗ trợ: PDF, DjVu, XPS, CBZ, FB2, PDB, TXT, HTML, RTF, CHM, EPUB, DOC, MOBI, ZIP
- Hỗ trợ đa số các loại ngôn ngữ phổ biến, trong đó có tiếng Việt mà không cần cài đặt gì thêm (do sử dụng font mặc định là bộ Noto của Google), và có thể thêm cài đặt thêm font chữ một cách nhanh gọn nhẹ (chỉ bao gồm copy và paste).
- Hỗ trợ cài đặt nhiều từ điển (theo định dạng Stardict)
- Điều chỉnh cách hiển thị, dàn chữ PDF, đèn nền (với các máy có hỗ trợ như H2O)
- Đồng bộ hóa với Evernote, Zsync

### 1.3. Giới thiệu về Coolreader
Coolreader là một ứng dụng tương tự như Koreader, các tính năng chính là:
- Hỗ trợ đọc các file epub (non-DRM), fb2, doc, txt, rtf, html, chm, tcr, pdb, prc, mobi (non-DRM), pml. Theo ghi nhận thì Coolreader đọc mobi tốt hơn koreader.
- Trong bộ cài đặt có thêm các ứng dụng đi kèm là:
  * pbchess (chess trainer) (Touch) [chơi cờ vua, phải mất $ mua, nếu không mua thì cứ một lúc lại hiện thông báo]
  * checkers (Touch, Non-touch) [kiểu như cờ ca rô]
  * reversi (othello) (Touch, Non-touch) [một trò chơi nữa]
  * sokoban (Touch, Non-touch) [một trò chơi nữa]
  * sudoku (touch only) [một trò chơi nữa]
  * notepad (Touch, Non-touch) [ứng dụng cho ghi chépư
  * calculator (Touch, Non-touch) [máy tính]
  * dictionary (touch only) [từ điển, hỗ trợ dạng stardict]
  * file manager (touch only) [trình duyệt file, cho phép copy, paste, xóa file ngay trong máy Kobo mà không cần kết nối máy tính]

## 2. Cách cài đặt KSM
### 2.1. Lưu ý trước khi cài đặt
[Cập nhật 11/5/2018]
- Cần sạc pin đầy một chút trước khi cài KSM
- Phiên bản KSM 08 không hoạt động trên Kobo Aura H2O Edition 2 và không tốt lắm trên Kobo Aura One. Phiên bản KSM 09 vừa ra gần đây về sơ bộ đã hỗ trợ tất cả các máy, do đó hướng dẫn này đã cập nhật để cài đặt KSM 09.
- KSM hoạt động được với Firmware 2.6.0 đến 4.3.8842 và có thể cả các bản về sau (hiện tại xác nhận hoạt động tốt trên firmware 4.5.xxxx). Tuy nhiên nên tránh các bản FW  3.16.10 và 3.17.0. 
- Với máy Aura One và Aura Edition 2 thì khuyến cáo nên cập nhật firmware lên bản mới nhất trước khi cài đặt KSM, nếu không thì có thể có vấn đề về kết nối USB. 
- Với các máy chạy firmware từ bản 4.2.8432 trở lên (đặc biệt là Aura One và Aura Edition 2) thì nếu cài KSM 08 sẽ cần cài thêm một bản patch, đối với KSM 09 thì cần cài thêm bản Update 2 (xem phần 2.2.2.2). Ở đây chúng ta sẽ chỉ quan tâm đến KSM 09.
- Một điểm cần lưu ý nữa là rủi ro hỏng máy có thể xảy ra trong khi cài KSM tuy là rất thấp nhưng không thể loại trừ khả năng. Do vậy các bác nên sao lưu thẻ nhớ trong ra một thẻ nhớ khác hoặc lưu vào máy tính. Các bác có thể sử dụng HDD Raw Copy (trên Windows, link http://hddguru.com/software/HDD-Raw-Copy-Tool/) hoặc lệnh dd (trên Linux, cần thiết lập flag là "conv=noerror,notrunc,sync").
- Nếu vì một lý do nào đó mà các bác cài bản FW cũ đè lên FW mới (downgrade), thì các bác cần thực hiện factory reset, nếu không Nickel có thể không hoạt động sau khi cài KSM. Lý do là vì KSM sẽ quét một số file nào đó trong bộ nhớ trong để xác định phiên bản FW, nếu không chạy factory reset thì thông số sẽ bị lệch mất.

### 2.2. Tiến hành cài đặt
#### 2.2.1. Cài đặt KSM

- Kết nối máy Kobo với máy tính qua cáp USB, chúng ta sẽ thấy hiện ra ổ có tên KoboReader, và ổ này sẽ là thư mục gốc (root) để tiến hành cài đặt.

- Vào link sau: https://www.mobileread.com/forums/showthread.php?t=293804, sau đó tải file KBStartMenu_09_plus_update_001.zip và  	KSM09_update002.zip (file này sẽ để đến bước 2.2.2.2) về máy. Giải nén file KBStartMenu_09_plus_update_001.zip ra ta sẽ được một file là "Koboroot.tgz" và một thư mục là "kbmenupngs". Copy thư mục "kbmenupngs" vào thư mục gốc (ngay ngoài ổ KoboReader). Chạy safely remove với ổ KoboReader và rút cáp USB. Máy sẽ tự động xử lý và hiển thị màn hình có chữ "Processing". Khởi động lại máy và kiểm tra trong thư viện (Library) có các file sau:

  * exit_nickel.png [thoát nickel ra KSM]
  * poweroff.png [tắt máy]
  * run_test_script.png [chạy lệnh test]
  * simulate_usb_connection.png [giả lập kết nối usb]
  * switchtokoreader.png [chuyển sang koreader]
  * toggle_nightmode.png [bật chế độ đọc đêm, nền đen chữ trắng]

Các file này không phải là file ảnh đơn thuần, mà về sau sau khi cài KSM và koreader, nếu nhấn vào một trong các file này thì sẽ thi hành lệnh như trong phần ngoặc vuông.
 
- Lại cắm Kobo vào máy tính, copy file "KoboRoot.tgz" vừa giải nén vào trong thư mục .kobo (phải chắc chắn là file được copy vào TRONG thư mục này), sau đó lại safely remove và rút cáp USB, Kobo sẽ tự động cập nhật và chúng ta sẽ thấy màn hình có dòng chữ Updating. Sau khi chạy xong máy sẽ tự động khởi động lại và vào giao diện của KSM (nếu máy chạy vào Nickel thì chúng ta vào thư viện và chọn file exit_nickel.png như trên để thoát ra KSM).

- Tại giao diện của KSM, chọn "tools" > "activate" > "set runmenu settings.msh" > "always". Đến đây về cơ bản KSM đã cài xong, tuy nhiên nó sẽ thiếu mất một số tính năng quan trọng, do vậy chúng ta sẽ cần cài thêm bản patch.

- Bình thường thi khi ở chế độ sử dụng KSM, nếu cắm Kobo vào máy tính thì máy tính sẽ không nhận ổ. Để kết nối với máy tính từ KSM thì trước khi nối cáp USB, trên menu KSM nhấn vào "usb" > "usb enable.sh". Chờ cho đến khi phần hiển thị bên trên hiện là “USB support: enable” thì hãng cắm cáp USB.

#### 2.2.2. Cài đặt update bổ sung cho KSM
##### 2.2.2.1. Cảnh báo
- Phải chắc chắn rằng KSM 09 đã được cài đặt thành công trước khi cài patch.
- Các đời máy mới có ít tùy chọn reset và phục hồi, cho nên khả năng các máy đời mới có khả năng "ra đi" cao hơn so với các đời cũ. Như vậy chúng ta nên sao lưu trước để đề phòng (xem lại phần 2.1).

##### 2.2.2.2. Các bước cài update
- Kết nối máy Kobo với máy tính
- Copy file KSM09_update002.zip đã tải ở bước 2.2.1 vào folder .adds\kbmenu_user
- Safely remove và trên máy Kobo nhấn chọn "usb disable.sh" và "return" để về màn hình chính của KSM. Lúc này KSM sẽ hiện thêm dòng "handle KSM update", nhấn vào đó và chọn  "install KSM update". Chờ cho máy chạy cập nhật và khi nó hiện thông báo đã chạy xong thì nhấn vào giữa màn hình, một nút Close sẽ hiện ra, nhấn vào đó thì máy sẽ khởi động lại, vậy là chúng ta đã cài xong KSM :D.<br>
![Giao diện update](https://github.com/dreamofi/HuongdanKSM-Koreader-Coolreader/blob/master/ksm%20update.jpg)
![Update 2](https://github.com/dreamofi/HuongdanKSM-Koreader-Coolreader/blob/master/ksm%20update2%20done.jpg)
![Giao diện KSM](https://github.com/dreamofi/HuongdanKSM-Koreader-Coolreader/blob/master/ksm%20interface.jpg)

#### 2.2.3. Gỡ bỏ KSM
Nếu một lúc nào đó mà các bác muốn gỡ bỏ KSM thì thực hiện như sau:
- Trong giao diện KSM chọn "tools" > "ksm diverse.msh" > "del KSM.sh" > "delete ksm". Máy sẽ tự khởi động lại sau đó và chạy Nickel.
- Xóa thư mục kbmenupngs trong .kobo

## 3. Sử dụng Koreader
### 3.1. Lưu ý trước khi cài đặt
- Để giảm thiểu tối đa hỏng hóc có thể xảy ra, nếu máy có khe cắm thẻ nhớ thì các bác nên copy sách vào thẻ nhớ.
- Cơ chế lưu thông tin sách của Nickel là quét thông tin và lưu vào cơ sở dữ liệu (CSDL). Tuy nhiên Nickel nổi tiếng là rất hay xảy ra lỗi về CSDL trong quá trình quét thông tin (ví dụ như khi gặp các file bị lỗi). Koreader thì sử dụng cơ chế duyệt file nên không gây ra lỗi. Nếu các bác đã hoặc đang chuẩn bị cài koreader và không muốn nickel quét thư viện sách (trong trường hợp lỡ có ấn nhầm), thì chỉ việc thêm 2 dấu chấm vào đầu và cuối thư mục chứa sách. Ví dụ các bác để sách trong thư mục tên "Books", trên Windows hãy đổi tên nó thành ".Books.", Nickel sẽ coi đây là thư mục ẩn và bỏ qua. Koreader mặc định cũng sẽ không nhìn thấy các thư mục ẩn này, tuy nhiên chỉ cần vuốt một đường từ cạnh trên màn hình xuống để hiện ra menu, sau đó nhấn vào nút hình bánh răng, chọn "Show hidden files".

### 3.2. Tiến hành cài đặt
- Vào link sau http://build.koreader.rocks/download/nightly/, chọn phiên bản mới nhất, thường là dòng cuối cùng (ví dụ v2015.11-1159-g17014f9"). Sau đó chọn dòng nào giống như sau "koreader-kobo-arm-kobo-linux-gnueabihf-v2015.11.." (thường là sẽ có 2 dòng giống như vậy, dòng trên cho tải file có đuôi .targz, dòng dưới cho tải file đuôi .zip => chọn dòng dưới).
- Giải nén file vừa tải, chúng ta sẽ thấy có thư mục koreader và một vài file, bỏ qua các file khác và copy thư mục "koreader" này vào thư mục .adds trên máy Kobo.

[Ghi chú 1: Ngay tại bước này các bác cũng có thể cài thêm Coolreader trước khi rút cáp USB (chi tiết xem phần 4.)]

- Bấm Safely remove và rút cáp USB, trên giao diện của KSM sẽ hiện dòng "start koreader", nhấn vào đây chúng ta sẽ vào được koreader.

[Ghi chú 2: Về sau để nâng cấp bản mới cho koreader thì các bác chỉ việc copy thư mục koreader của bản mới đè vào thư mục của bản cũ trên máy.]

### 3.3. Hướng dẫn sử dụng cơ bản
#### 3.3.1. Giao diện sử dụng (đang cập nhật)
- Menu có 2 hàng, một trên đỉnh một dưới đáy. Để vào menu trên thì vuốt từ giữa cạnh trên màn hình xuống, menu dưới thì vuốt từ giữa cạnh dưới lên.
- Menu trên thì có cái nút thứ 2 từ phải qua, nhấn vào đó sẽ ra cái để chọn file. Để thoát ra KSM thì nhấn vào cái nút góc phải hình 3 đường sọc > exit.
- Menu dưới đáy cho phép chỉnh cách hiển thị, tăng độ tương phản, xoay trang. Nếu muốn nó thị full trang (không phải kiểu cuộn dần dần khi đọc các file truyện tranh) thì vào nút hình 2 cái cột sọc, ở dòng Scroll Mode chọn "off"

#### 3.3.2. Cài đặt thêm từ điển
Em xin tặng các bác link tải từ điển dạng stardict để dùng với koreader: 
- Link tải từ điển Anh-Việt và Việt-Anh: https://github.com/dreamofi/HuongdanKSM-Koreader-Coolreader/blob/master/E-V%20dict.zip
- Link tổng các thể loại từ điển khác: https://github.com/dreamofi/HuongdanKSM-Koreader-Coolreader

Để cài từ điển cho koreader thì các bác chỉ việc giải nén mấy cái file từ điển về, mỗi loại từ điển nên cho nó vào một thư mục riêng. Thường thì trong mỗi thư mục từ điển sẽ có vài file có đuôi .ifo, .idx, .dz, .oft. Xong rồi các bác cứ copy các folder từ điển vào thư mục .adds/koreader/data/dict trên máy Kobo. Để tra từ thì chỉ việc dùng ngón tay giữ vào từ cần tra. Lần đầu khởi chạy thì nếu các bác cài nhiều từ điển (em cài khoảng 7-8 cái, trong đó có 2-3 cái từ điển dung lượng >100mb) thì sẽ mất khoảng vài phút. Các bác thấy máy nó như kiểu không chạy thì cứ để im đấy nhé, một lúc là sẽ chạy xong.<br>
![Từ điển Koreader](http://i.imgur.com/Om888hT.jpg)

Trong trường hợp mà từ điển khi tra hiện ra thông báo là "No definition found" thì các bác có thể thử lần lượt từng bước sau:
  * Xóa đi cài lại koreader bản nightly mới nhất
  * Tải file này https://github.com/koreader/koreader/files/1489711/sdcv-arm-linux-gnuabihf.zip ; giải nén ra sẽ được 1 file là sdcv, copy đè cái file đó vào folder koreader
  * Downgrade firmware xuống 4.5 / 4.4 rồi cài lại koreader

#### 3.3.3. Cài đặt thêm font
Các bác copy font bất kỳ vào .adds/koreader/fonts

## 4. Sử dụng Coolreader
### 4.1. Cài đặt
- Tải Coolreader tại đây: http://www.pbchess.vlasovsoft.net/en/index.html (phần download ở dưới đáy) 
- Giải nén file vừa tải sẽ được thư mục vlasovsoft và các file khác, tương tự như cài koreader, bỏ qua các file khác và copy thư mục vlasovsoft vào ".adds" trên máy Kobo
- Ở trong giao diện KSM 09 thì nhấn vào dòng "Toggle btw full and short menu" để hiện ra đủ menu.
![Toggle Menu](https://github.com/dreamofi/HuongdanKSM-Koreader-Coolreader/blob/master/ksm%20update.jpg)
- Nhấn vào dòng start vlasovsoftlauncher
![Chạy coolreader](https://github.com/dreamofi/HuongdanKSM-Koreader-Coolreader/blob/master/ksm%20full%20menu.jpg)
- Để nâng cấp Coolreader thì cũng chỉ việc copy đè thư mục vlasovsoft bản mới vào ".adds".

### 4.2. Hướng dẫn sử dụng cơ bản
Cái này menu khá là rõ rồi nên sẽ cập nhật chi tiết sau.<br>
![Giao diện CR](https://www.mobileread.com/forums/attachment.php?attachmentid=131486&d=1416770007)

## 5. Khắc mục một số vấn đề khi sử dụng KSM / Koreader & Coolreader.
### 5.1. KSM/Koreader/Coolreader hay bị đơ
Có thể do thẻ nhớ có vấn đề, các bác có thể thay thẻ nhớ khác xem vấn đề có được khắc phục không. Theo như ghi nhận thì thẻ của Sandisk hoạt động khá tốt, thẻ của Stratium không tốt lắm, các hãng khác chưa có ghi nhận.

## 6. Nguồn tham khảo
- https://www.mobileread.com/forums/showthread.php?t=240302
- https://www.mobileread.com/forums/showthread.php?t=266821
