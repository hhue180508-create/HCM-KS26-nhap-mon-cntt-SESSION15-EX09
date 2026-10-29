

# **BÀI TỔNG HỢP SESSION 14: LÀM VIỆC NHÓM TRÊN CLOUD WORKSPACE**

## **PHẦN 1: THIẾT LẬP HYBRID WORKFLOW**

### **Câu 1: Nếu laptop hỏng ổ cứng thì file có bị mất không?**

Theo em, nếu nhóm đã thiết lập Hybrid Workflow và bật Auto Sync từ đầu thì khả năng mất file sẽ thấp hơn rất nhiều. Vì khi mình làm việc trên laptop, những thay đổi trong file sẽ được đồng bộ lên Cloud. Nếu máy tính bị hỏng, mình vẫn có thể đăng nhập trên thiết bị khác để lấy lại bản đã đồng bộ.

Tuy nhiên, nếu file mới nhất chưa kịp đồng bộ thì những thay đổi đó vẫn có thể bị mất. Vì vậy, sau khi làm xong, mọi người nên kiểm tra xem file đã đồng bộ thành công chưa.

### **Câu 2: Ba bước thiết lập Auto Sync**

Đầu tiên, mọi người đăng nhập vào tài khoản Cloud mà nhóm đang sử dụng, ví dụ như Google Drive.

Tiếp theo, cài đặt ứng dụng đồng bộ trên laptop và chọn thư mục dự án SmartCampus cần đồng bộ.

Cuối cùng, bật Auto Sync rồi kiểm tra trạng thái đồng bộ. Mọi người có thể thử tạo hoặc chỉnh sửa một file để xem nội dung đã xuất hiện trên Cloud chưa.

### **Câu 3: Khôi phục hai trang bị xóa nhầm**

Trong trường hợp này, mình không cần phải ngồi gõ lại từ đầu mà có thể sử dụng tính năng Version History, tức là lịch sử phiên bản.

Cụ thể, mình mở file báo cáo, vào phần lịch sử phiên bản, chọn phiên bản được lưu trước khi xóa nhầm rồi kiểm tra và khôi phục nội dung cần thiết. Nếu muốn giữ những thay đổi mới hơn, mình có thể sao chép hai trang từ phiên bản cũ sang bản hiện tại để tránh mất các nội dung đã hoàn thành sau đó.

### **Câu 4: Sai lầm khi đồng bộ `node_modules` và phim 4K**

Theo em, đây là hai sai lầm cần tránh khi sử dụng Cloud Workspace.

Thứ nhất, đồng bộ thư mục `node_modules` với quá nhiều file nhỏ sẽ khiến quá trình đồng bộ chậm và tốn tài nguyên. Cách xử lý là loại thư mục này khỏi phạm vi đồng bộ và sử dụng các file quản lý thư viện như `package.json` để cài đặt lại khi cần.

Thứ hai, đưa các file phim 4K không liên quan đến đồ án lên Cloud sẽ làm tốn dung lượng lưu trữ. Vì vậy, nhóm chỉ nên đồng bộ những file thực sự cần cho dự án, còn phim giải trí thì chuyển sang nơi lưu trữ cá nhân.

---

## **PHẦN 2: PHÂN QUYỀN CHIA SẺ AN TOÀN**

### **Câu 1: Phân quyền cho từng file**

Theo em, khi chia sẻ file, mình phải xem ai là người nhận và họ cần làm gì để chọn quyền phù hợp.

| File | Mức quyền | Phạm vi chia sẻ | Giải thích |
| ----- | ----- | ----- | ----- |
| `BaoCao_CuoiKy_SmartCampus.docx` | Viewer | Restricted | Giảng viên chỉ cần xem và chấm điểm nên không cần quyền chỉnh sửa. |
| `Slide_BaoCao.pptx` | Editor | Restricted | Cả 5 thành viên cần cùng chỉnh sửa slide nên được cấp quyền Editor, nhưng chỉ những người trong nhóm mới được truy cập. |
| `GopY_BanNhap.docx` | Commenter | Restricted | Anh khóa trên có thể đọc và nhận xét nhưng không thể sửa trực tiếp nội dung. |
| `ThongTin_CaNhan_NhomVien.xlsx` | Editor cho người thực sự cần cập nhật | Restricted | File chứa CCCD và số điện thoại nên chỉ người được chỉ định mới được truy cập. |

Riêng file thông tin cá nhân, nếu người nhận chỉ cần xem thì mình nên cấp Viewer thay vì Editor để hạn chế rủi ro.

### **Câu 2: Quy tắc Cờ Đỏ Bảo mật**

Quy tắc Cờ Đỏ Bảo mật theo em là phải đặc biệt cẩn thận với những file chứa thông tin nhạy cảm, chẳng hạn như CCCD, số điện thoại hoặc dữ liệu cá nhân.

Đối với file `ThongTin_CaNhan_NhomVien.xlsx`, nhóm phải để phạm vi chia sẻ là Restricted, nghĩa là chỉ những người được cấp quyền mới có thể truy cập.

Mình tuyệt đối không nên chọn Anyone with the link kết hợp với Editor, vì bất kỳ ai có đường dẫn đều có thể có quyền truy cập và chỉnh sửa file. Nếu đường dẫn bị gửi nhầm ra ngoài, thông tin của cả nhóm có thể bị lộ hoặc bị thay đổi.

### **Câu 3: Hai thao tác trong Settings để bảo vệ file PowerPoint**

Vì cả 5 thành viên đều có quyền Editor, theo em nhóm nên kiểm tra hai thiết lập sau.

Thứ nhất, tắt quyền cho phép Editor thay đổi quyền truy cập hoặc chia sẻ file cho người khác, nếu dịch vụ Cloud đang dùng có hỗ trợ tùy chọn này. Như vậy, thành viên sẽ khó tự ý chia sẻ file cho người ngoài.

Thứ hai, kiểm tra các tùy chọn tải xuống, in và sao chép đối với người xem hoặc người nhận xét. Nếu cần hạn chế việc sao chép nội dung, nhóm có thể điều chỉnh các quyền này cho phù hợp. Tuy nhiên, không nên hạn chế đến mức làm ảnh hưởng việc chỉnh sửa slide của 5 thành viên.

---

## **PHẦN 3: TỔ CHỨC GIAO TIẾP NHÓM CHUẨN DOANH NGHIỆP**

### **Câu 1: Ba vấn đề trong đoạn hội thoại Zalo**

Theo em, đoạn hội thoại hiện tại có ba vấn đề chính.

**Thứ nhất là No-Hello.** Lan chỉ nhắn “có ai rảnh không” mà không nói rõ mình cần giúp việc gì. Người khác phải hỏi lại mới hiểu vấn đề, khiến việc trao đổi mất thời gian.

**Thứ hai là tin nhắn công việc và tin nhắn giải trí bị trộn lẫn.** Trong nhóm có cả nội dung hỏi việc, ảnh mèo và bình luận vui vẻ. Điều này khiến các thông tin quan trọng dễ bị trôi, nhất là khi gần đến hạn nộp bài.

**Thứ ba là lạm dụng `@all` vào giờ khuya.** Trưởng nhóm nhắn lúc 23 giờ 47 phút và tag tất cả mọi người, dù có thể chỉ một vài thành viên chưa hoàn thành công việc. Cách này dễ làm phiền những người không liên quan. Thay vào đó, trưởng nhóm nên đặt lịch gửi vào 8 giờ sáng và tag đúng người cần xử lý.

### **Câu 2: Những kênh nhóm nên tạo trên Lark hoặc Slack**

Theo em, nhóm nên chia thành các kênh riêng để việc trao đổi rõ ràng hơn.

* **`#thong-bao`** dùng để đăng deadline, thông báo chính thức và những thay đổi quan trọng.  
* **`#tien-do-cong-viec`** dùng để cập nhật tiến độ, người phụ trách và những phần còn thiếu.  
* **`#trao-doi-do-an`** dùng để thảo luận nội dung báo cáo và slide.  
* **`#tam-su-giai-tri`** dành cho những nội dung vui vẻ ngoài công việc.

Ngoài ra, khi trao đổi về một nhiệm vụ cụ thể, mọi người nên trả lời bằng Thread để các tin nhắn không bị lẫn sang những chủ đề khác.

### **Câu 3: Viết lại tin nhắn của Lan theo tư duy Asynchronous**

Em sẽ viết lại tin nhắn của Lan như sau:

writing{variant="chat\_message" id="58322" title="Tin nhắn nhờ hỗ trợ"}  
Mọi người ơi, mình đang hoàn thiện slide SmartCampus nhưng còn thiếu phần mô tả chức năng đăng ký học phần. Bạn nào đang phụ trách phần này gửi giúp mình nội dung trước 18h hôm nay nhé. Nếu chưa hoàn thành kịp thì mọi người báo thời gian dự kiến để mình chủ động sắp xếp lại slide. Cảm ơn mọi người\!  
:::

Tin nhắn này có đủ nội dung cần hỗ trợ, thời hạn hoàn thành và cách phản hồi. Vì vậy, dù mọi người đọc tin nhắn vào 2 giờ chiều hay 10 giờ đêm thì vẫn hiểu rõ vấn đề và có thể trả lời ngay mà không cần hỏi lại.

### **Câu 4: Viết lại tin nhắn nhắc deadline và đặt lịch gửi**

Thay vì nhắn lúc 23 giờ 47 phút và dùng `@all`, em sẽ đặt lịch gửi tin nhắn vào **8 giờ sáng hôm sau** và chỉ tag những người còn thiếu phần việc.

@Lan, bạn cập nhật giúp mình phần nội dung còn thiếu trong báo cáo trước 9h sáng nay nhé.

@Nam, bạn kiểm tra và hoàn thiện phần slide còn lại trước 9h sáng nay giúp mình.

Nếu có phần nào chưa làm xong hoặc đang gặp khó khăn, hai bạn báo rõ tình hình và thời gian dự kiến hoàn thành để nhóm kịp thời hỗ trợ. Cảm ơn hai bạn\!

Trước khi gửi, em sẽ thay Lan và Nam bằng đúng tên những thành viên còn thiếu phần việc. Việc đặt lịch gửi giúp mọi người nhận được thông báo vào thời điểm hợp lý hơn, còn việc tag đích danh giúp người nhận biết rõ trách nhiệm của mình.

---

## **PHẦN 4: THÔNG BÁO TỔNG HỢP TRÊN KÊNH `#thong-bao`**

Mọi người ơi, mình đã bật Auto Sync cho thư mục dự án SmartCampus để các file được tự động đồng bộ lên Cloud. Từ giờ, sau khi chỉnh sửa xong, mọi người nhớ kiểm tra trạng thái đồng bộ để tránh mất bản mới nhất nếu máy tính gặp sự cố nhé.

Mình cũng đã chia sẻ file `BaoCao_CuoiKy_SmartCampus.docx` cho giảng viên theo quyền Viewer và phạm vi Restricted. Như vậy, giảng viên có thể xem báo cáo để chấm điểm mà không chỉnh sửa trực tiếp được, đồng thời file cũng không bị chia sẻ công khai.

Hiện tại, nhóm vẫn còn một số phần cần hoàn thiện trước hạn nộp. @Lan, bạn cập nhật giúp mình phần nội dung còn thiếu; @Nam, bạn kiểm tra và hoàn thiện phần slide còn lại trước 9h sáng nay nhé. Nếu có khó khăn hoặc không kịp thời hạn, hai bạn báo sớm để cả nhóm cùng hỗ trợ.

Mọi người nhớ trao đổi đúng kênh, phản hồi rõ ràng và kiểm tra quyền chia sẻ trước khi gửi file cho người ngoài nhóm. Cố gắng hoàn thiện đồ án đúng hạn nha\!

**Kết luận:** Qua tình huống này, em thấy làm việc nhóm trên Cloud không chỉ là đưa file lên mạng mà còn phải biết đồng bộ dữ liệu, phân quyền đúng người và giao tiếp rõ ràng. Nếu nhóm thực hiện tốt cả ba việc này thì sẽ hạn chế được tình trạng mất file, sửa nhầm nội dung và bỏ sót công việc khi gần đến deadline.  
:::

**Lưu ý trước khi nộp:** Ở phần thông báo cuối, chỉ viết “đã bật Auto Sync” và “đã chia sẻ file” sau khi bạn thực sự thực hiện các thao tác đó. Đồng thời, thay tên Lan và Nam bằng đúng thành viên còn thiếu việc trong nhóm.

