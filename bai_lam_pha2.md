# BÀI LÀM PHA 2 (ĐỀ LUYỆN TẬP CHỦ ĐỀ TÀI CHÍNH CÁ NHÂN)

- **Họ tên:Lê Đức Anh**
- **Lớp:CNTT3**
- **Link repository Pha2:https://github.com/danhle220508/on_tap **
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):gemini**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đăng ký hội thảo ra JSON

**KET QUA AI**

```text
[
  {
    "ma_goi": "DT",
    "ngay_hoi_thao": "2026-12-20",
    "nguoi_lon": 2,
    "tre_em": 1,
    "loai_ve": "thuong",
    "ghi_chu": null
  },
  {
    "ma_goi": "CB",
    "ngay_hoi_thao": "2027-01-10",
    "nguoi_lon": 3,
    "tre_em": 0,
    "loai_ve": null,
    "ghi_chu": "Có một người dùng xe lăn cần lối đi riêng"
  },
  {
    "ma_goi": "VIP",
    "ngay_hoi_thao": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "loai_ve": null,
    "ghi_chu": "có một anh mắt kém cần ngồi bàn đầu gần màn hình chiếu"
  }
]
```

**Link trò chuyện:https://share.gemini.google/ClpTy5Kv68ao**

## 4.3. Báo giá vé hội thảo bằng Chain-of-Thought

**KET QUA AI**

```text
1. **Tiền người lớn:**
* Chọn gói DT (Gói Đầu Tư): `1.500.000` đồng/người lớn.
* Số lượng: `4` người lớn.
* Phép tính: `4 × 1.500.000 = 6.000.000` đồng.


2. **Tiền trẻ em:**
* Trẻ 8 tuổi và 11 tuổi (từ 6 đến 12 tuổi): tính `50%` giá người lớn (`50% × 1.500.000 = 750.000` đồng/trẻ), có `2` trẻ.
* Bé 4 tuổi (dưới 6 tuổi): miễn phí (`0` đồng).
* Phép tính: `2 × (1.500.000 × 0,5) + 1 × 0 = 2 × 750.000 + 0 = 1.500.000` đồng.


3. **Tiền vé:**
* Phép tính: `6.000.000 + 1.500.000 = 7.500.000` đồng.


4. **Giảm giá nhóm:**
* Nhóm có `4` người lớn (từ 4 người lớn trở lên): giảm `10%` trên tiền vé.
* Tiền giảm: `7.500.000 × 10% = 750.000` đồng.
* Tiền vé sau giảm: `7.500.000 - 750.000 = 6.750.000` đồng.


5. **Phụ thu sổ tay:**
* Đặt mua `2` bộ sổ tay, giá `200.000` đồng/bộ (không được giảm giá).
* Phép tính: `2 × 200.000 = 400.000` đồng.


6. **Tổng tiền:**
* Phép tính: `6.750.000 + 400.000 = 7.150.000` đồng.



[RESULT: 7.150.000 đồng]
```

**Link trò chuyện:https://share.gemini.google/ZmTiWxnsojlR**

### b) Kiểm tra kết quả AI

đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "sai_khu_vuc",
  "so_khach": 2,
  "so_phien_bi_anh_huong": 2,
  "tom_tat": "Khách gói DT bị xếp ghế phụ thiếu bàn viết cam kết trong 2 phiên học đầu."
}
```

**Link trò chuyện:https://share.gemini.google/wnKEPndCUmib**

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| **Đúng thông tin (50% - Tối đa 5.0đ)** | **5.0 / 5.0** *(Lưu ý: Chưa có dữ liệu chuẩn đối chiếu)* | - Câu trích dẫn: *"Vé gói Đầu Tư bên em giá chỉ 1.200.000đ/người thôi"*, *"Anh/chị báo huỷ trước 4 ngày thì bên em hoàn lại đủ 100% tiền vé nha"*.<br>

<br>- Lý do: Nội dung đã nêu rõ con số về giá vé và điều kiện hoàn tiền. (Tạm tính điểm tối đa do đề bài chưa cung cấp thông tin chuẩn của BTC để đối chiếu tính chính xác thực tế). | *"Vé gói Đầu Tư hiện có mức phí là 1.200.000đ/người. Trong trường hợp cần hủy vé, anh/chị vui lòng thông báo trước 4 ngày diễn ra sự kiện để được hỗ trợ hoàn lại 100% chi phí."* |
| **Đầy đủ (30% - Tối đa 3.0đ)** | **1.5 / 3.0** | - Câu bị lỗi: Toàn bộ đoạn văn thiếu thông tin điều hướng khách hàng chốt đơn.<br>

<br>- Lý do sai: Nhân viên đã trả lời được 2 ý về giá vé và chính sách hủy, nhưng hoàn toàn bỏ sót phần kêu gọi hành động (mời khách hàng cung cấp ngày hội thảo và số lượng vé muốn đăng ký). | Bổ sung vào cuối câu trả lời: *"Để bên em hỗ trợ giữ chỗ, anh/chị vui lòng cho biết ngày tham dự hội thảo và số lượng vé mình muốn đăng ký nhé ạ."* |
| **Giọng điệu (20% - Tối đa 2.0đ)** | **0.0 / 2.0** | - Câu bị lỗi 1: *"Dạ chào anh/chị nha!"*, *"hoàn lại đủ 100% tiền vé nha, cứ yên tâm chốt đơn đi ạ!"*<br>

<br>- Lý do sai 1: Sử dụng các từ ngữ mang tính suồng sã, thiếu chuyên nghiệp trong giao tiếp tư vấn dịch vụ (*"nha"*, *"chốt đơn đi ạ"*).<br>

<br>

<br>- Câu bị lỗi 2: *"đi học về đầu tư chứng khoán lời khủng luôn ạ."*<br>

<br>- Lý do sai 2: Cam kết và hứa hẹn lợi nhuận quá đà (*"lời khủng luôn"*), gây rủi ro về mặt truyền thông và vi phạm quy chuẩn tư vấn tài chính. | - Sửa lỗi 1: *"Dạ chào anh/chị!"*, *"bên em sẽ hoàn lại 100% chi phí vé. Anh/chị hoàn toàn có thể yên tâm đăng ký ạ."*<br>

<br>

<br>- Sửa lỗi 2: *"Khóa học sẽ cung cấp các kiến thức và phương pháp thực chiến giúp anh/chị tối ưu hóa hiệu quả đầu tư chứng khoán."* |
| **TỔNG ĐIỂM** | **6.5 / 10** |  |  |

---



**Link trò chuyện:https://share.gemini.google/a5rX2O3TG1Go**
