# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 08
- **Họ tên:** Hồ Anh Hào
- **Lớp:** CNTT2
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt lịch khám ra JSON

**KET QUA AI**

```text
[
  {
    "ma_dich_vu": "TRAM",
    "ngay_hen": "2026-12-17",
    "nguoi_lon": 2,
    "tre_em": 1,
    "khung_gio": "chieu",
    "ghi_chu": null
  },
  {
    "ma_dich_vu": "CAOVOI",
    "ngay_hen": "2027-01-06",
    "nguoi_lon": 3,
    "tre_em": 0,
    "khung_gio": null,
    "ghi_chu": "Một người bị tiểu đường"
  },
  {
    "ma_dich_vu": "TAYTRANG",
    "ngay_hen": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "khung_gio": "sang",
    "ghi_chu": "Một người dị ứng thuốc tê"
  }
]
```

**Link trò chuyện:** https://chatgpt.com/share/6b0818dd-7fc0-83ec-8ded-bc39348ae033

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
### **1. Tiền người lớn**

Có 6 người lớn, mỗi người sử dụng dịch vụ CAOVOI với giá 350.000 đồng.

Phép tính:

\\(6 \times 350.000 = 2.100.000\\) đồng.

### **2. Tiền trẻ em**

- Trẻ 7 tuổi: \\(350.000 \times 80\\% = 280.000\\) đồng.
- Trẻ 11 tuổi: \\(350.000 \times 80\\% = 280.000\\) đồng.
- Bé 4 tuổi: Được khám miễn phí = 0 đồng.

Tổng tiền trẻ em:

\\(280.000 + 280.000 + 0 = 560.000\\) đồng.

### **3. Tiền dịch vụ**

Tiền dịch vụ = Tiền người lớn + Tiền trẻ em.

\\(2.100.000 + 560.000 = 2.660.000\\) đồng.

### **4. Giảm giá nhóm**

Nhóm có 6 người lớn (đạt điều kiện từ 5 người lớn trở lên), được giảm 10% trên tổng tiền dịch vụ.

\- Tiền giảm giá:

\\(2.660.000 \times 10\\% = 266.000\\) đồng.

\- Tiền dịch vụ sau giảm:

\\(2.660.000 - 266.000 = 2.394.000\\) đồng.

### **5. Phí chụp X-quang**

Có 3 người cần chụp X-quang, mỗi người 1 phim, giá 150.000 đồng/phim.

\\(3 \times 150.000 = 450.000\\) đồng.

Lưu ý: Phí X-quang không được giảm giá.

### **6. Tổng tiền**

Tổng tiền = Tiền dịch vụ sau giảm + Phí chụp X-quang.

\\(2.394.000 + 450.000 = 2.844.000\\) đồng.

Kết quả cuối cùng

[RESULT: 2.844.000 đồng]
```

**Link trò chuyện:** https://chatgpt.com/share/6b081940-23bc-83ec-82a2-7f6a65b84ab2

### b) Kiểm tra kết quả AI

(Ghi kết luận AI đúng hay sai; nếu sai, ghi bước sai đầu tiên và kết quả đúng của bước đó – xoá dòng này)

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text

{\
&#x20; "loai_su_co": "tre_hen",\
&#x20; "so_khach": 3,\
&#x20; "so_lan_hen_bi_tre": 2,\
&#x20; "tom_tat": "Gia đình 3 người phải chờ hơn 1 tiếng trong cả 2 lần hẹn cạo vôi răng."\
}
```

**Link trò chuyện:** https://chatgpt.com/share/6b0819b0-05f0-83ec-9b08-a688d442c2b0

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí                    | Điểm        | Minh chứng                                                                                                                                                                                                                                         | Đề xuất sửa                                                                                                                                                                                 |
| --------------------------- | ----------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Đúng thông tin (50%)** | **1,0/5,0** | - Câu bị lỗi: “Trám răng bên em 450k/răng thôi” → Sai giá, giá chuẩn là **500.000 đồng/răng**. <br>- Câu bị lỗi: “Bong sau 8 tháng thì em làm lại free cho anh nha.” → Sai chính sách. Sau 8 tháng chỉ được giảm 50%, không được làm lại miễn phí. | “Dịch vụ trám răng thẩm mỹ có giá 500.000 đồng/răng. Nếu miếng trám bị bong sau 8 tháng, anh được hỗ trợ làm lại với mức giảm 50% chi phí.”                                                 |
| **2. Đầy đủ (30%)**         | **1,5/3,0** | - Câu bị lỗi: “Cần gì cứ inbox em ạ!” → Chưa chủ động mời khách cung cấp ngày hẹn và khung giờ để đặt lịch. <br>- Đã trả lời cả hai nội dung khách hỏi nhưng thông tin bảo hành sai.                                                               | “Anh vui lòng cung cấp ngày hẹn và khung giờ mong muốn để bên em hỗ trợ đặt lịch nhé!”                                                                                                      |
| **3. Giọng điệu (20%)**     | **1,0/2,0** | - Câu bị lỗi: “450k/răng thôi”, “đẹp như răng thật luôn”, “làm lại free”, “Cần gì cứ inbox em ạ!” → Cách diễn đạt thiếu chuyên nghiệp, sử dụng từ ngữ suồng sã và quảng cáo thiếu căn cứ.                                                          | Sử dụng cách diễn đạt lịch sự, chuyên nghiệp: “Dạ, dịch vụ trám răng thẩm mỹ bên em có giá 500.000 đồng/răng. Bên em sẵn sàng hỗ trợ anh đặt lịch và tư vấn thêm về chính sách bảo hành ạ.” |
| **Tổng điểm**               | **3,5/10**  | Bài làm sai cả giá dịch vụ và chính sách bảo hành, chưa đáp ứng đầy đủ yêu cầu đặt lịch và cần cải thiện cách giao tiếp.                                                                                                                           | Cần kiểm tra thông tin theo chính sách công ty trước khi tư vấn khách hàng.                                                                                                                 |

**Nhận xét chung:**

Nhân viên đã có thái độ chào hỏi khách hàng nhưng mắc lỗi nghiêm trọng về thông tin giá và bảo hành. Đặc biệt, việc cam kết làm lại miễn phí sau 8 tháng có thể gây thiệt hại cho công ty và tạo kỳ vọng sai cho khách hàng.

**Mẫu câu trả lời đạt yêu cầu:**

“Dạ, dịch vụ trám răng thẩm mỹ bên em có giá 500.000 đồng/răng ạ. Theo chính sách bảo hành, nếu miếng trám bị bong sau 8 tháng, anh sẽ được hỗ trợ làm lại với mức giảm 50% chi phí. Anh vui lòng cho em xin ngày hẹn và khung giờ mong muốn để em hỗ trợ đặt lịch ạ!”

**Kết luận:**&#x20;

Chưa đạt yêu cầu

&#x20;Nhân viên cần được hướng dẫn lại về bảng giá, chính sách bảo hành và kỹ năng tư vấn chuyên nghiệp.

```

**Link trò chuyện:** https://chatgpt.com/share/6b081a0f-f694-83ec-9d38-adb30fdb11ed
