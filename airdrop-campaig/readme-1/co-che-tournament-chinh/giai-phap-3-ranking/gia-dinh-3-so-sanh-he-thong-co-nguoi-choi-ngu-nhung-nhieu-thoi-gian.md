# Giả định 3 - so sánh hệ thống có người chơi ngu nhưng nhiều thời gian

### 1. Phân tích loại người chơi mới

* Người chơi nhiều nhưng chơi ngu, công bằng:
* Hành vi: Chơi rất nhiều trận mỗi ngày, tương tự người chơi nhiều (Lan), nhưng kỹ năng kém dẫn đến tỷ lệ thắng thấp. Không gian lận, đối thủ được chọn ngẫu nhiên (theo hệ thống bạn yêu cầu trước đó).
* Chiến lược: Không có chiến lược cụ thể, chỉ chơi nhiều vì đam mê hoặc muốn cải thiện, nhưng kết quả kém do thiếu kỹ năng.
* Tác động trong hệ thống:
  * Tỷ lệ thắng thấp (dưới 50%) do kỹ năng kém.
  * Vẫn có cơ hội tạo chuỗi thắng do chơi nhiều trận, nhưng ít hơn người chơi nhiều có kỹ năng (Lan).
  * Điểm thắng rank cao hơn (+0.5) vẫn xuất hiện do đối thủ ngẫu nhiên, nhưng số trận thắng ít.
  * Điểm thua sát nút (+0.2) có thể cao hơn, vì người chơi kém thường thua nhiều trận cạnh tranh.

Trường hợp giả định (Player F - Tùng)

* Mô tả: Tùng chơi nhiều trận, công bằng, nhưng kỹ năng kém, dẫn đến tỷ lệ thắng thấp.
* Chi tiết:
  * Chơi 15 trận/ngày (105 trận/tuần, tương đương Lan).
  * Tỷ lệ thắng: 35% (37 thắng, 68 thua).
  * Chuỗi thắng: 2 chuỗi/tuần (2 điểm bonus), do số trận nhiều vẫn tạo cơ hội ngẫu nhiên cho chuỗi thắng.
  * Thắng rank cao hơn: 50% của trận thắng → 37 × 0.5 ≈ 19 trận (+9.5 điểm).
  * Thua sát nút: 8 trận (+1.6 điểm), do thua nhiều trận cạnh tranh.
  * Điểm dự kiến: 37 (thắng) + 2 (bonus) + 9.5 (thắng rank cao) + 1.6 (thua sát nút) = 50.1 điểm.

### 2. Cập nhật các trường hợp giả định khác

Tôi sẽ giữ nguyên các trường hợp trước đó (đã điều chỉnh cho hệ thống chọn đối thủ ngẫu nhiên) để đảm bảo tính nhất quán. Dưới đây là tóm tắt lại 5 trường hợp cũ:

* Minh (công bằng):
  * 49 trận/tuần, thắng 27, thua 22, 1 chuỗi thắng, 14 thắng rank cao, 3 thua sát nút.
  * Điểm: 35.6.
* Hùng (gian lận):
  * 70 trận/tuần, thắng 53, thua 17, 3 chuỗi thắng, 27 thắng rank cao, 2 thua sát nút.
  * Điểm: 69.9.
* Lan (chơi nhiều):
  * 105 trận/tuần, thắng 53, thua 52, 4 chuỗi thắng, 27 thắng rank cao, 5 thua sát nút.
  * Điểm: 71.5.
* Phong (chơi ít):
  * 21 trận/tuần, thắng 11, thua 10, 0 chuỗi thắng, 6 thắng rank cao, 2 thua sát nút.
  * Điểm: 14.4.
* Ngọc (hỗn hợp):
  * 56 trận/tuần, thắng 34, thua 22, 2 chuỗi thắng, 17 thắng rank cao, 3 thua sát nút.
  * Điểm: 45.1.

### 3. Bảng xếp hạng giả định (30 người chơi)

Tôi sẽ tạo bảng xếp hạng mới, bao gồm 6 người chơi cụ thể (Minh, Hùng, Lan, Phong, Ngọc, Tùng) và 24 người chơi khác với số liệu ngẫu nhiên nhưng hợp lý, phản ánh các loại người chơi (công bằng, chơi nhiều, chơi ít, hỗn hợp, chơi nhiều kém kỹ năng). Điểm số được tính theo quy tắc và xếp từ cao đến thấp.Bảng xếp hạng

| Vị trí | Tên người chơi | Điểm số | Số trận đã chơi | Thắng | Thua | Chuỗi thắng (bonus) | Thắng rank cao | Thua sát nút |
| ------ | -------------- | ------- | --------------- | ----- | ---- | ------------------- | -------------- | ------------ |
| 1      | Lan            | 71.5    | 105             | 53    | 52   | 4                   | 27             | 5            |
| 2      | Hùng           | 69.9    | 70              | 53    | 17   | 3                   | 27             | 2            |
| 3      | Tùng           | 50.1    | 105             | 37    | 68   | 2                   | 19             | 8            |
| 4      | Ngọc           | 45.1    | 56              | 34    | 22   | 2                   | 17             | 3            |
| 5      | An             | 40.2    | 60              | 31    | 29   | 2                   | 15             | 4            |
| 6      | Bình           | 37.8    | 50              | 28    | 22   | 2                   | 14             | 3            |
| 7      | Minh           | 35.6    | 49              | 27    | 22   | 1                   | 14             | 3            |
| 8      | Cường          | 33.4    | 45              | 25    | 20   | 1                   | 12             | 3            |
| 9      | Dũng           | 31.2    | 42              | 23    | 19   | 1                   | 11             | 2            |
| 10     | Hà             | 29.0    | 40              | 22    | 18   | 1                   | 11             | 2            |
| 11     | Kiên           | 27.1    | 38              | 21    | 17   | 1                   | 10             | 2            |
| 12     | Linh           | 25.3    | 35              | 19    | 16   | 1                   | 9              | 2            |
| 13     | Mai            | 23.6    | 32              | 18    | 14   | 1                   | 9              | 1            |
| 14     | Nam            | 21.8    | 30              | 16    | 14   | 1                   | 8              | 1            |
| 15     | Oanh           | 20.2    | 28              | 15    | 13   | 1                   | 7              | 1            |
| 16     | Phương         | 18.7    | 26              | 14    | 12   | 0                   | 7              | 2            |
| 17     | Quang          | 17.3    | 24              | 13    | 11   | 0                   | 6              | 2            |
| 18     | Sơn            | 16.0    | 22              | 12    | 10   | 0                   | 6              | 1            |
| 19     | Tâm            | 14.8    | 20              | 11    | 9    | 0                   | 5              | 1            |
| 20     | Phong          | 14.4    | 21              | 11    | 10   | 0                   | 6              | 2            |
| 21     | Uyên           | 13.2    | 18              | 10    | 8    | 0                   | 5              | 1            |
| 22     | Vũ             | 12.0    | 16              | 9     | 7    | 0                   | 4              | 1            |
| 23     | Xuân           | 11.0    | 14              | 8     | 6    | 0                   | 4              | 1            |
| 24     | Yên            | 10.1    | 12              | 7     | 5    | 0                   | 3              | 1            |
| 25     | Ánh            | 9.2     | 10              | 6     | 4    | 0                   | 3              | 1            |
| 26     | Bảo            | 8.4     | 9               | 5     | 4    | 0                   | 2              | 1            |
| 27     | Chi            | 7.6     | 8               | 5     | 3    | 0                   | 2              | 0            |
| 28     | Đạt            | 6.9     | 7               | 4     | 3    | 0                   | 2              | 1            |
| 29     | Giang          | 6.2     | 6               | 4     | 2    | 0                   | 1              | 1            |
| 30     | Hoa            | 5.6     | 5               | 3     | 2    | 0                   | 1              | 1            |

### 4. Phân tích bảng xếp hạng

* Lan (chơi nhiều) vẫn dẫn đầu (71.5 điểm) nhờ số trận lớn và tỷ lệ thắng trung bình (50%), cho thấy chơi nhiều vẫn là lợi thế lớn trong hệ thống ngẫu nhiên.
* Hùng (gian lận) xếp thứ 2 (69.9 điểm), nhưng khoảng cách với Lan rất nhỏ, cho thấy gian lận kém hiệu quả hơn khi đối thủ ngẫu nhiên.
* Tùng (chơi nhiều, kém kỹ năng) xếp thứ 3 (50.1 điểm), vượt qua Ngọc (45.1 điểm) dù tỷ lệ thắng thấp (35%). Điều này cho thấy số trận chơi nhiều vẫn giúp tích lũy điểm đáng kể, nhờ điểm thắng rank cao và thua sát nút.
* Ngọc (hỗn hợp) tụt xuống vị trí 4, do số trận ít hơn Tùng và không thể chọn đối thủ để tối ưu hóa.
* Minh (công bằng) ở vị trí 7 (35.6 điểm), ổn định ở nhóm trung bình, phản ánh lối chơi công bằng nhưng không nổi bật.
* Phong (chơi ít) gần cuối (20, 14.4 điểm), do số trận ít và không có chuỗi thắng.
* Tính công bằng: Hệ thống ngẫu nhiên tiếp tục tăng tính công bằng, nhưng người chơi nhiều (dù kỹ năng kém như Tùng) vẫn có lợi thế lớn nhờ số trận. Tùng vượt qua nhiều người chơi có kỹ năng tốt hơn (như Ngọc, Minh) chỉ vì chơi nhiều.
