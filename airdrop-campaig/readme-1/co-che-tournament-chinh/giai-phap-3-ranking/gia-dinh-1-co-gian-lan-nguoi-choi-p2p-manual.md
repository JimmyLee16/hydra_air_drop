# Giả định 1 - Có gian lận người chơi P2P manual

### 1. Phân tích cách tính điểm ranking:

* Thắng trận: +1 điểm.
* Chuỗi thắng 3 trận liên tiếp: +1 điểm bonus (tối đa 3 điểm bonus/ngày, tức là tối đa 3 chuỗi thắng/ngày).
* Thắng người rank cao hơn: +0.5 điểm (giả định "rank cao hơn" dựa trên bảng xếp hạng tại thời điểm trận đấu).
* Thua sát nút (hòa 2 ván đầu, thua ván cuối): +0.2 điểm danh dự.
* Giao diện: Bảng xếp hạng hiển thị điểm số, số trận đã chơi, và vị trí hiện tại.

### Giả định bổ sung để tạo dữ liệu:

* Mỗi ngày, một người chơi có thể chơi một số trận nhất định (tùy thuộc vào loại người chơi: chơi nhiều, chơi ít, v.v.).
* "Rank cao hơn" được xác định nếu đối thủ có vị trí cao hơn trên bảng xếp hạng tại thời điểm thi đấu.
* Một chuỗi thắng được tính khi thắng 3 trận liên tiếp trong cùng một ngày.
* Người chơi gian lận có thể thao túng kết quả (ví dụ: cố ý sắp xếp trận đấu với đối thủ yếu hơn hoặc giả mạo chuỗi thắng).
* Dữ liệu giả định được tính trong một khoảng thời gian nhất định (giả sử 1 tuần, 7 ngày) để có đủ dữ liệu cho bảng xếp hạng.

### 2. Các loại người chơi và trường hợp giả địnhDưới đây là mô tả các loại người chơi và 5 trường hợp cụ thể:

#### a. Người chơi công bằng (Player A - Minh)

* Hành vi: Chơi trung bình 5-10 trận/ngày, thắng thua xen kẽ, không cố ý chọn đối thủ yếu, thi đấu trung thực.
* Chiến lược: Tập trung cải thiện kỹ năng, không khai thác lỗ hổng hệ thống.
* Trường hợp giả định (Minh):
  * Chơi 7 trận/ngày (49 trận/tuần).
  * Tỷ lệ thắng: 60% (29 thắng, 20 thua).
  * 2 chuỗi thắng 3 trận liên tiếp/tuần (2 điểm bonus).
  * 5 trận thắng đối thủ rank cao hơn.
  * 3 trận thua sát nút.
  * Điểm dự kiến: 29 (thắng) + 2 (bonus) + 5 × 0.5 (thắng rank cao) + 3 × 0.2 (thua sát nút) = 33.1 điểm.

#### b. Người chơi gian lận (Player B - Hùng)

* Hành vi: Tìm cách thao túng hệ thống, ví dụ: sắp xếp đấu với bạn bè rank thấp để thắng dễ, hoặc giả mạo chuỗi thắng.
* Chiến lược: Tối đa hóa điểm bằng cách chọn đối thủ yếu và cố ý tạo chuỗi thắng.
* Trường hợp giả định (Hùng):
  * Chơi 10 trận/ngày (70 trận/tuần).
  * Tỷ lệ thắng: 90% (63 thắng, 7 thua) do chọn đối thủ yếu.
  * 3 chuỗi thắng/ngày (21 chuỗi/tuần, nhưng chỉ được tính tối đa 3 điểm bonus/ngày → 21 điểm bonus/tuần).
  * 10 trận thắng đối thủ rank cao hơn (do thao túng).
  * 2 trận thua sát nút.
  * Điểm dự kiến: 63 (thắng) + 21 (bonus) + 10 × 0.5 (thắng rank cao) + 2 × 0.2 (thua sát nút) = 89.4 điểm.

#### c. Người chơi nhiều (Player C - Lan)

* Hành vi: Chơi rất nhiều trận mỗi ngày, thắng thua công bằng, không gian lận.
* Chiến lược: Tăng điểm bằng cách chơi nhiều, tận dụng cơ hội chuỗi thắng tự nhiên.
* Trường hợp giả định (Lan):
  * Chơi 15 trận/ngày (105 trận/tuần).
  * Tỷ lệ thắng: 55% (58 thắng, 47 thua).
  * 5 chuỗi thắng/tuần (5 điểm bonus).
  * 8 trận thắng đối thủ rank cao hơn.
  * 5 trận thua sát nút.
  * Điểm dự kiến: 58 (thắng) + 5 (bonus) + 8 × 0.5 (thắng rank cao) + 5 × 0.2 (thua sát nút) = 68 điểm.

#### d. Người chơi ít (Player D - Phong)

* Hành vi: Chỉ chơi vài trận mỗi ngày do bận rộn, nhưng chơi công bằng.
* Chiến lược: Không tập trung vào ranking, chỉ chơi giải trí.
* Trường hợp giả định (Phong):
  * Chơi 3 trận/ngày (21 trận/tuần).
  * Tỷ lệ thắng: 50% (11 thắng, 10 thua).
  * 1 chuỗi thắng/tuần (1 điểm bonus).
  * 2 trận thắng đối thủ rank cao hơn.
  * 2 trận thua sát nút.
  * Điểm dự kiến: 11 (thắng) + 1 (bonus) + 2 × 0.5 (thắng rank cao) + 2 × 0.2 (thua sát nút) = 13.4 điểm.

#### e. Người chơi hỗn hợp (Player E - Ngọc)

* Hành vi: Chơi lượng trận trung bình, có lúc cố ý chọn đối thủ yếu hơn (nhưng không gian lận trắng trợn), thắng thua xen kẽ.
* Chiến lược: Cân bằng giữa giải trí và cố gắng leo rank.
* Trường hợp giả định (Ngọc):
  * Chơi 8 trận/ngày (56 trận/tuần).
  * Tỷ lệ thắng: 65% (36 thắng, 20 thua).
  * 3 chuỗi thắng/tuần (3 điểm bonus).
  * 6 trận thắng đối thủ rank cao hơn.
  * 4 trận thua sát nút.
  * Điểm dự kiến: 36 (thắng) + 3 (bonus) + 6 × 0.5 (thắng rank cao) + 4 × 0.2 (thua sát nút) = 42.8 điểm.

### 3. Tạo bảng xếp hạng giả định

Dựa trên các trường hợp trên, tôi sẽ tạo bảng xếp hạng cho 30 người chơi, bao gồm 5 người chơi cụ thể (Minh, Hùng, Lan, Phong, Ngọc) và 25 người chơi giả định khác. Các người chơi khác sẽ có số liệu ngẫu nhiên nhưng hợp lý trong phạm vi của các loại người chơi (công bằng, chơi nhiều, chơi ít, hoặc hỗn hợp). Điểm số được tính dựa trên quy tắc đã nêu, và vị trí được sắp xếp theo điểm từ cao đến thấp.Bảng xếp hạng (30 người chơi)

| Vị trí | Tên người chơi | Loại người chơi         | Điểm số | Số trận đã chơi | Thắng | Thua | Chuỗi thắng (bonus) | Thắng rank cao | Thua sát nút |
| ------ | -------------- | ----------------------- | ------- | --------------- | ----- | ---- | ------------------- | -------------- | ------------ |
| 1      | Hùng           | Gian lận                | 89.4    | 70              | 63    | 7    | 21.0 (21 chuỗi)     | 10 (5.0)       | 2 (0.4)      |
| 2      | Lan            | Chơi nhiều              | 68.0    | 105             | 58    | 47   | 5.0 (5 chuỗi)       | 8 (4.0)        | 5 (1.0)      |
| 3      | Tùng           | Chơi nhiều, kém kỹ năng | 56.1    | 105             | 42    | 63   | 2.0 (2 chuỗi)       | 21 (10.5)      | 8 (1.6)      |
| 4      | Ngọc           | Hỗn hợp                 | 42.8    | 56              | 36    | 20   | 3.0 (3 chuỗi)       | 6 (3.0)        | 4 (0.8)      |
| 5      | An             | Công bằng               | 38.2    | 60              | 32    | 28   | 3.0 (3 chuỗi)       | 5 (2.5)        | 3 (0.6)      |
| 6      | Bình           | Công bằng               | 35.6    | 50              | 30    | 20   | 2.0 (2 chuỗi)       | 4 (2.0)        | 4 (0.8)      |
| 7      | Minh           | Công bằng               | 33.1    | 49              | 29    | 20   | 2.0 (2 chuỗi)       | 5 (2.5)        | 3 (0.6)      |
| 8      | Cường          | Công bằng               | 31.8    | 45              | 27    | 18   | 2.0 (2 chuỗi)       | 4 (2.0)        | 2 (0.4)      |
| 9      | Dũng           | Công bằng               | 29.4    | 40              | 25    | 15   | 2.0 (2 chuỗi)       | 3 (1.5)        | 3 (0.6)      |
| 10     | Hà             | Công bằng               | 27.2    | 38              | 23    | 15   | 2.0 (2 chuỗi)       | 3 (1.5)        | 2 (0.4)      |
| 11     | Kiên           | Công bằng               | 25.0    | 35              | 21    | 14   | 1.0 (1 chuỗi)       | 3 (1.5)        | 2 (0.4)      |
| 12     | Linh           | Công bằng               | 23.6    | 32              | 20    | 12   | 1.0 (1 chuỗi)       | 2 (1.0)        | 3 (0.6)      |
| 13     | Mai            | Công bằng               | 22.4    | 30              | 19    | 11   | 1.0 (1 chuỗi)       | 2 (1.0)        | 2 (0.4)      |
| 14     | Nam            | Công bằng               | 20.8    | 28              | 17    | 11   | 1.0 (1 chuỗi)       | 2 (1.0)        | 2 (0.4)      |
| 15     | Oanh           | Công bằng               | 19.2    | 25              | 16    | 9    | 1.0 (1 chuỗi)       | 1 (0.5)        | 2 (0.4)      |
| 16     | Phương         | Chơi ít                 | 18.0    | 24              | 15    | 9    | 1.0 (1 chuỗi)       | 1 (0.5)        | 1 (0.2)      |
| 17     | Quang          | Chơi ít                 | 16.8    | 22              | 14    | 8    | 1.0 (1 chuỗi)       | 1 (0.5)        | 1 (0.2)      |
| 18     | Sơn            | Chơi ít                 | 15.6    | 20              | 13    | 7    | 1.0 (1 chuỗi)       | 1 (0.5)        | 1 (0.2)      |
| 19     | Tâm            | Chơi ít                 | 14.4    | 18              | 12    | 6    | 1.0 (1 chuỗi)       | 0 (0.0)        | 2 (0.4)      |
| 20     | Phong          | Chơi ít                 | 13.4    | 21              | 11    | 10   | 1.0 (1 chuỗi)       | 2 (1.0)        | 2 (0.4)      |
| 21     | Uyên           | Chơi ít                 | 12.2    | 16              | 10    | 6    | 0.0 (0 chuỗi)       | 1 (0.5)        | 1 (0.2)      |
| 22     | Vũ             | Chơi ít                 | 11.0    | 15              | 9     | 6    | 0.0 (0 chuỗi)       | 1 (0.5)        | 0 (0.0)      |
| 23     | Xuân           | Chơi ít                 | 10.2    | 14              | 8     | 6    | 0.0 (0 chuỗi)       | 1 (0.5)        | 1 (0.2)      |
| 24     | Yên            | Chơi ít                 | 9.4     | 12              | 7     | 5    | 0.0 (0 chuỗi)       | 1 (0.5)        | 1 (0.2)      |
| 25     | Ánh            | Chơi ít                 | 8.6     | 10              | 7     | 3    | 0.0 (0 chuỗi)       | 0 (0.0)        | 1 (0.2)      |
| 26     | Bảo            | Chơi ít                 | 7.8     | 9               | 6     | 3    | 0.0 (0 chuỗi)       | 0 (0.0)        | 1 (0.2)      |
| 27     | Chi            | Chơi ít                 | 7.0     | 8               | 5     | 3    | 0.0 (0 chuỗi)       | 1 (0.5)        | 0 (0.0)      |
| 28     | Đạt            | Chơi ít                 | 6.4     | 7               | 5     | 2    | 0.0 (0 chuỗi)       | 0 (0.0)        | 1 (0.2)      |
| 29     | Giang          | Chơi ít                 | 5.8     | 6               | 4     | 2    | 0.0 (0 chuỗi)       | 0 (0.0)        | 1 (0.2)      |
| 30     | Khang          | Chơi ít                 | 4.6     | 4               | 3     | 1    | 0.0 (0 chuỗi)       | 0 (0.0)        | 1 (0.2)      |

### 4. Phân tích bảng xếp hạng

* Hùng (gian lận) đứng đầu do khai thác tối đa chuỗi thắng và chọn đối thủ yếu, dẫn đến số điểm vượt trội (89.4).
* Lan (chơi nhiều) xếp thứ 2 nhờ số trận chơi lớn, dù tỷ lệ thắng không quá cao (68.0 điểm).
* Ngọc (hỗn hợp) đứng thứ 3, cân bằng giữa chơi nhiều và chiến lược chọn đối thủ (42.8 điểm).
* Minh (công bằng) ở vị trí thứ 6, phản ánh lối chơi trung thực nhưng không tối ưu hóa điểm (33.1 điểm).
* Phong (chơi ít) xếp gần cuối (19) do chơi ít trận, dù tỷ lệ thắng không tệ (13.4 điểm).
* Các người chơi khác có số liệu phân bố hợp lý, phản ánh sự đa dạng trong hành vi chơi (công bằng, chơi nhiều, chơi ít).

### 5. Gợi ý cải thiện hệ thống ranking

Dựa trên bảng xếp hạng, có thể thấy:

* Người chơi gian lận (Hùng) dễ dàng thống trị do khai thác chuỗi thắng và chọn đối thủ yếu. Hệ thống có thể cần giới hạn số trận đấu với cùng một đối thủ hoặc kiểm tra tính hợp lệ của chuỗi thắng.
* Người chơi nhiều (Lan) có lợi thế lớn nhờ số trận cao, nhưng điều này công bằng vì họ đầu tư thời gian.
* Người chơi ít (Phong) khó cạnh tranh, có thể thêm cơ chế thưởng điểm cho hiệu suất cao (ví dụ: tỷ lệ thắng cao trong ít trận).
* Điểm thua sát nút (+0.2) có tác động nhỏ, có thể cân nhắc tăng nhẹ để khuyến khích thi đấu cạnh tranh.
