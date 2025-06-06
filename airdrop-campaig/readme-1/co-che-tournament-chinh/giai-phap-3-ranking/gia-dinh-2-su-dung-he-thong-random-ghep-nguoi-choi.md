# Giả định 2 - Sử dụng hệ thống random ghép người chơi

### 1. Tác động của việc chọn đối thủ ngẫu nhiên

* Loại bỏ gian lận chọn đối thủ: Người chơi như Hùng không thể cố ý đấu với đối thủ yếu để tăng tỷ lệ thắng hoặc thao túng điểm thắng rank cao hơn. Tỷ lệ thắng sẽ phụ thuộc vào kỹ năng thực tế và sự ngẫu nhiên.
* Điểm thắng rank cao hơn (+0.5): Vì đối thủ được chọn ngẫu nhiên, xác suất gặp người rank cao hơn phụ thuộc vào phân bố người chơi trong hệ thống. Giả sử bảng xếp hạng có phân bố đồng đều, khoảng 50% trận đấu có thể gặp đối thủ rank cao hơn.
* Chuỗi thắng (+1 điểm bonus): Vẫn có thể xảy ra, nhưng khó đạt được liên tục do đối thủ ngẫu nhiên, đặc biệt với người chơi gian lận. Người chơi nhiều (như Lan) vẫn có lợi thế vì chơi nhiều trận tăng cơ hội tạo chuỗi thắng.
* Thua sát nút (+0.2): Không bị ảnh hưởng bởi chọn đối thủ ngẫu nhiên, vì điều kiện này dựa trên kết quả trận đấu (hòa 2 ván đầu, thua ván cuối).
* Tính công bằng: Hệ thống ngẫu nhiên tăng tính công bằng, nhưng có thể làm giảm động lực cho người chơi chiến lược (như Ngọc) vì họ không thể tối ưu hóa đối thủ.

### 2. Điều chỉnh các trường hợp giả định

Điều chỉnh 5 trường hợp cụ thể (Minh, Hùng, Lan, Phong, Ngọc) dựa trên hệ thống chọn đối thủ ngẫu nhiên. Giả định:

* Tỷ lệ thắng trung bình của người chơi công bằng dao động quanh 50% (do đối thủ ngẫu nhiên).
* Người chơi gian lận vẫn có thể cố gắng khai thác hệ thống (ví dụ: sử dụng bot hoặc tài khoản phụ), nhưng hiệu quả giảm do không chọn được đối thủ yếu.
* Thời gian tính điểm: 1 tuần (7 ngày).

#### a. Người chơi công bằng (Player A - Minh)

* Hành vi: Chơi trung thực, không tìm cách gian lận.
* Điều chỉnh: Tỷ lệ thắng giảm nhẹ do không thể chọn đối thủ phù hợp.
* Trường hợp giả định:
  * Chơi 7 trận/ngày (49 trận/tuần).
  * Tỷ lệ thắng: 55% (27 thắng, 22 thua).
  * Chuỗi thắng: 1 chuỗi/tuần (1 điểm bonus).
  * Thắng rank cao hơn: 50% của trận thắng → 27 × 0.5 ≈ 14 trận (+7 điểm).
  * Thua sát nút: 3 trận (+0.6 điểm).
  * Điểm dự kiến: 27 (thắng) + 1 (bonus) + 7 (thắng rank cao) + 0.6 (thua sát nút) = 35.6 điểm.

#### b. Người chơi gian lận (Player B - Hùng)

* Hành vi: Cố gắng gian lận bằng cách sử dụng bot hoặc tài khoản phụ, nhưng không thể chọn đối thủ yếu trực tiếp.
* Điều chỉnh: Tỷ lệ thắng vẫn cao hơn bình thường (do gian lận), nhưng không áp đảo như trước.
* Trường hợp giả định:
  * Chơi 10 trận/ngày (70 trận/tuần).
  * Tỷ lệ thắng: 75% (53 thắng, 17 thua).
  * Chuỗi thắng: 3 chuỗi/tuần (3 điểm bonus).
  * Thắng rank cao hơn: 50% của trận thắng → 53 × 0.5 ≈ 27 trận (+13.5 điểm).
  * Thua sát nút: 2 trận (+0.4 điểm).
  * Điểm dự kiến: 53 (thắng) + 3 (bonus) + 13.5 (thắng rank cao) + 0.4 (thua sát nút) = 69.9 điểm.

#### c. Người chơi nhiều (Player C - Lan)

* Hành vi: Chơi nhiều trận, dựa vào số lượng để tích lũy điểm.
* Điều chỉnh: Tỷ lệ thắng giảm do đối thủ ngẫu nhiên, nhưng số trận cao giúp tăng cơ hội chuỗi thắng.
* Trường hợp giả định:
  * Chơi 15 trận/ngày (105 trận/tuần).
  * Tỷ lệ thắng: 50% (53 thắng, 52 thua).
  * Chuỗi thắng: 4 chuỗi/tuần (4 điểm bonus).
  * Thắng rank cao hơn: 50% của trận thắng → 53 × 0.5 ≈ 27 trận (+13.5 điểm).
  * Thua sát nút: 5 trận (+1 điểm).
  * Điểm dự kiến: 53 (thắng) + 4 (bonus) + 13.5 (thắng rank cao) + 1 (thua sát nút) = 71.5 điểm.

#### d. Người chơi ít (Player D - Phong)

* Hành vi: Chơi ít, công bằng, không tập trung leo rank.
* Điều chỉnh: Tỷ lệ thắng trung bình, ít cơ hội tạo chuỗi thắng.
* Trường hợp giả định:
  * Chơi 3 trận/ngày (21 trận/tuần).
  * Tỷ lệ thắng: 50% (11 thắng, 10 thua).
  * Chuỗi thắng: 0 chuỗi/tuần (0 điểm bonus).
  * Thắng rank cao hơn: 50% của trận thắng → 11 × 0.5 ≈ 6 trận (+3 điểm).
  * Thua sát nút: 2 trận (+0.4 điểm).
  * Điểm dự kiến: 11 (thắng) + 0 (bonus) + 3 (thắng rank cao) + 0.4 (thua sát nút) = 14.4 điểm.

#### e. Người chơi hỗn hợp (Player E - Ngọc)

* Hành vi: Chơi trung bình, cố gắng tối ưu hóa điểm nhưng không gian lận trắng trợn.
* Điều chỉnh: Không thể chọn đối thủ yếu, tỷ lệ thắng giảm so với trước.
* Trường hợp giả định:
  * Chơi 8 trận/ngày (56 trận/tuần).
  * Tỷ lệ thắng: 60% (34 thắng, 22 thua).
  * Chuỗi thắng: 2 chuỗi/tuần (2 điểm bonus).
  * Thắng rank cao hơn: 50% của trận thắng → 34 × 0.5 ≈ 17 trận (+8.5 điểm).
  * Thua sát nút: 3 trận (+0.6 điểm).
  * Điểm dự kiến: 34 (thắng) + 2 (bonus) + 8.5 (thắng rank cao) + 0.6 (thua sát nút) = 45.1 điểm.

### 3. Bảng xếp hạng giả định (30 người chơi)

Dựa trên các trường hợp đã điều chỉnh, tôi tạo bảng xếp hạng cho 30 người chơi, với 5 người chơi cụ thể và 25 người chơi khác có số liệu ngẫu nhiên nhưng hợp lý trong phạm vi các loại người chơi. Điểm số được tính theo quy tắc và xếp từ cao đến thấp.

Bảng xếp hạng

| Vị trí | Tên người chơi | Loại người chơi         | Điểm số | Số trận đã chơi | Thắng | Thua | Chuỗi thắng (bonus) | Thắng rank cao | Thua sát nút |
| ------ | -------------- | ----------------------- | ------- | --------------- | ----- | ---- | ------------------- | -------------- | ------------ |
| 1      | Lan            | Chơi nhiều              | 71.5    | 105             | 53    | 52   | 4.0 (4 chuỗi)       | 27 (13.5)      | 5 (1.0)      |
| 2      | Hùng           | Gian lận                | 69.9    | 70              | 53    | 17   | 3.0 (3 chuỗi)       | 27 (13.5)      | 2 (0.4)      |
| 3      | Tùng           | Chơi nhiều, kém kỹ năng | 50.1    | 105             | 37    | 68   | 2.0 (2 chuỗi)       | 19 (9.5)       | 8 (1.6)      |
| 4      | Ngọc           | Hỗn hợp                 | 45.1    | 56              | 34    | 22   | 2.0 (2 chuỗi)       | 17 (8.5)       | 3 (0.6)      |
| 5      | An             | Công bằng               | 40.2    | 60              | 31    | 29   | 2.0 (2 chuỗi)       | 15 (7.5)       | 4 (0.8)      |
| 6      | Bình           | Công bằng               | 37.8    | 50              | 28    | 22   | 2.0 (2 chuỗi)       | 14 (7.0)       | 3 (0.6)      |
| 7      | Minh           | Công bằng               | 35.6    | 49              | 27    | 22   | 1.0 (1 chuỗi)       | 14 (7.0)       | 3 (0.6)      |
| 8      | Cường          | Công bằng               | 33.4    | 45              | 25    | 20   | 1.0 (1 chuỗi)       | 12 (6.0)       | 3 (0.6)      |
| 9      | Dũng           | Công bằng               | 31.2    | 42              | 23    | 19   | 1.0 (1 chuỗi)       | 11 (5.5)       | 2 (0.4)      |
| 10     | Hà             | Công bằng               | 29.0    | 40              | 22    | 18   | 1.0 (1 chuỗi)       | 11 (5.5)       | 2 (0.4)      |
| 11     | Kiên           | Công bằng               | 27.1    | 38              | 21    | 17   | 1.0 (1 chuỗi)       | 10 (5.0)       | 2 (0.4)      |
| 12     | Linh           | Công bằng               | 25.3    | 35              | 19    | 16   | 1.0 (1 chuỗi)       | 9 (4.5)        | 2 (0.4)      |
| 13     | Mai            | Công bằng               | 23.6    | 32              | 18    | 14   | 1.0 (1 chuỗi)       | 9 (4.5)        | 1 (0.2)      |
| 14     | Nam            | Công bằng               | 21.8    | 30              | 16    | 14   | 1.0 (1 chuỗi)       | 8 (4.0)        | 1 (0.2)      |
| 15     | Oanh           | Công bằng               | 20.2    | 28              | 15    | 13   | 1.0 (1 chuỗi)       | 7 (3.5)        | 1 (0.2)      |
| 16     | Phương         | Chơi ít                 | 18.7    | 26              | 14    | 12   | 0.0 (0 chuỗi)       | 7 (3.5)        | 2 (0.4)      |
| 17     | Quang          | Chơi ít                 | 17.3    | 24              | 13    | 11   | 0.0 (0 chuỗi)       | 6 (3.0)        | 2 (0.4)      |
| 18     | Sơn            | Chơi ít                 | 16.0    | 22              | 12    | 10   | 0.0 (0 chuỗi)       | 6 (3.0)        | 1 (0.2)      |
| 19     | Tâm            | Chơi ít                 | 14.8    | 20              | 11    | 9    | 0.0 (0 chuỗi)       | 5 (2.5)        | 1 (0.2)      |
| 20     | Phong          | Chơi ít                 | 14.4    | 21              | 11    | 10   | 0.0 (0 chuỗi)       | 6 (3.0)        | 2 (0.4)      |
| 21     | Uyên           | Chơi ít                 | 13.2    | 18              | 10    | 8    | 0.0 (0 chuỗi)       | 5 (2.5)        | 1 (0.2)      |
| 22     | Vũ             | Chơi ít                 | 12.0    | 16              | 9     | 7    | 0.0 (0 chuỗi)       | 4 (2.0)        | 1 (0.2)      |
| 23     | Xuân           | Chơi ít                 | 11.0    | 14              | 8     | 6    | 0.0 (0 chuỗi)       | 4 (2.0)        | 1 (0.2)      |
| 24     | Yên            | Chơi ít                 | 10.1    | 12              | 7     | 5    | 0.0 (0 chuỗi)       | 3 (1.5)        | 1 (0.2)      |
| 25     | Ánh            | Chơi ít                 | 9.2     | 10              | 6     | 4    | 0.0 (0 chuỗi)       | 3 (1.5)        | 1 (0.2)      |
| 26     | Bảo            | Chơi ít                 | 8.4     | 9               | 5     | 4    | 0.0 (0 chuỗi)       | 2 (1.0)        | 1 (0.2)      |
| 27     | Chi            | Chơi ít                 | 7.6     | 8               | 5     | 3    | 0.0 (0 chuỗi)       | 2 (1.0)        | 0 (0.0)      |
| 28     | Đạt            | Chơi ít                 | 6.9     | 7               | 4     | 3    | 0.0 (0 chuỗi)       | 2 (1.0)        | 1 (0.2)      |
| 29     | Giang          | Chơi ít                 | 6.2     | 6               | 4     | 2    | 0.0 (0 chuỗi)       | 1 (0.5)        | 1 (0.2)      |
| 30     | Khang          | Chơi ít                 | 4.9     | 4               | 3     | 1    | 0.0 (0 chuỗi)       | 1 (0.5)        | 0 (0.0)      |

### 4. Phân tích bảng xếp hạng

* Lan (chơi nhiều) đứng đầu (71.5 điểm) nhờ số trận lớn, dù tỷ lệ thắng chỉ 50%. Điều này cho thấy chơi nhiều vẫn là lợi thế lớn trong hệ thống ngẫu nhiên.
* Hùng (gian lận) xếp thứ 2 (69.9 điểm), nhưng điểm số giảm đáng kể so với hệ thống cũ (89.4 điểm) do không thể chọn đối thủ yếu. Gian lận vẫn mang lại lợi thế, nhưng kém hiệu quả hơn.
* Ngọc (hỗn hợp) xếp thứ 3 (45.1 điểm), vẫn duy trì vị trí cao nhờ tỷ lệ thắng tốt và số trận trung bình.
* Minh (công bằng) ở vị trí thứ 6 (35.6 điểm), tương đối ổn định, cho thấy người chơi công bằng vẫn cạnh tranh được ở mức trung bình.
* Phong (chơi ít) gần cuối (19, 14.4 điểm), do số trận ít và không có chuỗi thắng.
* Tính công bằng tăng: Khoảng cách điểm giữa top và trung bình thu hẹp (Hùng giảm từ 89.4 xuống 69.9, Lan tăng từ 68.0 lên 71.5), cho thấy hệ thống ngẫu nhiên giảm lợi thế của gian lận.
