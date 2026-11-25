# BÀI LÀM PHA 2 (ĐỀ LUYỆN TẬP CHỦ ĐỀ CHẠY AFFILIATE)

- **Họ tên:**Nguyễn Thế Huy
- **Lớp:**CNTT3
- **Link repository Pha2:**https://github.com/mrwe08/test_promting_final
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**gemini

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đăng ký gói Affiliate ra JSON

**KET QUA AI**

```text
[
  {
    "ma_goi": "TT",
    "ngay_bat_dau": "2026-12-20",
    "creator_chinh": 2,
    "thuc_tap_sinh": 1,
    "hang_tai_khoan": "thuong",
    "ghi_chu": null
  },
  {
    "ma_goi": "SP",
    "ngay_bat_dau": "2027-01-08",
    "creator_chinh": 3,
    "thuc_tap_sinh": 0,
    "hang_tai_khoan": "thuong",
    "ghi_chu": "Có một bạn đang bó bột chân cần ngồi bàn gần cửa ra vào"
  },
  {
    "ma_goi": "PRO",
    "ngay_bat_dau": null,
    "creator_chinh": 4,
    "thuc_tap_sinh": 0,
    "hang_tai_khoan": "vip",
    "ghi_chu": "cần mượn thêm đèn trợ sáng và phông xanh để quay mẫu"
  }
]
```

**Link trò chuyện:**https://share.gemini.google/PTJCzyi3Z2mj

## 4.3. Báo giá gói Affiliate bằng Chain-of-Thought

**KET QUA AI**

```text
Tiền Creator chính: 4 × 1.500.000 = 6.000.000 đồng

Tiền thực tập sinh: (2 × 1.500.000 × 60%) + (1 × 0) = 1.800.000 đồng

Tổng tiền gói: 6.000.000 + 1.800.000 = 7.800.000 đồng

Giảm giá team: 7.800.000 × 10% = 780.000 đồng (còn 7.800.000 - 780.000 = 7.020.000 đồng)

Phụ thu thuê mic: 2 × 250.000 = 500.000 đồng

Tổng tiền: 7.020.000 + 500.000 = 7.520.000 đồng

[RESULT: 7.520.000 đồng]
```

**Link trò chuyện:**https://share.gemini.google/4ga74qeM2VBU

### b) Kiểm tra kết quả AI

đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "sai_phong",
  "so_khach": 3,
  "so_ca_bi_anh_huong": 2,
  "tom_tat": "Nhóm 3 khách hàng (gói TT đợt thực chiến Mega Sale ngày 11/11/2026) bị xếp nhầm sang phòng học thường thiếu đèn livestream và vách cách âm như cam kết trong 2 ca thực hành đầu. Mức đền bù theo chính sách: hoàn 300.000 đồng/khách/ca x 3 khách x 2 ca = 1.800.000 đồng. Vì tổng mức đền bù trên 1.500.000 đồng, cần trình Trưởng bộ phận Chăm sóc Publisher duyệt trước khi phản hồi khách hàng."
}
```

**Link trò chuyện:**https://share.gemini.google/5nt5tF2oogLH

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
```markdown
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| :--- | :--- | :--- | :--- |
| **Đúng thông tin** (5,0 điểm) | 0,0 / 5,0 | **Lỗi 1:** "Gói TikTok Affiliate bên mình giá chỉ 1.200.000đ/người thôi"<br>- *Lý do sai:* Sai mức giá chuẩn của trung tâm (giá đúng là 1.500.000 đồng/Creator chính).<br><br>**Lỗi 2:** "Bạn báo huỷ trước 5 ngày thì được hoàn lại đủ 100% tiền nha"<br>- *Lý do sai:* Sai chính sách hoàn tiền (huỷ trước 3 đến 6 ngày chỉ được hoàn 50%, không phải 100%). | **Sửa lỗi 1:** "Hiện tại gói TikTok Affiliate (TT) bên trung tâm có mức phí là 1.500.000 đồng/Creator chính ạ."<br><br>**Sửa lỗi 2:** "Theo chính sách của trung tâm, nếu anh/chị báo huỷ trước ngày bắt đầu 5 ngày (thuộc mốc từ 3 đến 6 ngày), anh/chị sẽ được hoàn lại 50% học phí ạ." |
| **Đầy đủ** (3,0 điểm) | 1,5 / 3,0 | **Lỗi:** Toàn bộ bài làm thiếu phần kêu gọi hành động.<br>- *Lý do sai:* Đã trả lời đủ 2 câu hỏi của khách (dù sai thông tin) nhưng thiếu nội dung mời khách hàng cung cấp ngày đợt thực chiến và số lượng suất muốn đăng ký. | **Bổ sung cuối câu trả lời:** "Anh/chị vui lòng cho bên em xin thông tin về ngày đợt thực chiến dự kiến tham gia và số lượng suất muốn đăng ký để em hỗ trợ giữ chỗ cho mình nhé." |
| **Giọng điệu** (2,0 điểm) | 0,0 / 2,0 | **Lỗi 1:** "Dạ hello bạn nha!", "cứ chốt lẹ kẻo hết slot nè!"<br>- *Lý do sai:* Sử dụng ngôn ngữ suồng sã, thiếu tính chuyên nghiệp trong tư vấn.<br><br>**Lỗi 2:** "đăng ký xong gắn link là nổ đơn hoa hồng trăm triệu luôn ạ."<br>- *Lý do sai:* Vi phạm quy định khi cam kết doanh thu/hoa hồng ảo cho khách hàng. | **Sửa lỗi 1:** Thay bằng lời chào và kết câu lịch sự: "Dạ chào anh/chị ạ!", "Anh/chị phản hồi sớm để bên em hỗ trợ giữ suất tham gia nhé ạ."<br><br>**Sửa lỗi 2:** Xoá bỏ hoàn toàn câu cam kết doanh thu ảo này khỏi nội dung tư vấn. |
| **Tổng điểm** | **1,5 / 10** | | |

```
```

**Link trò chuyện:**https://share.gemini.google/zkAIu4DTHLZk
