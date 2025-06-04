# 🏦 CƠ CHẾ DONATE LIÊN KẾT VỚI STAKING POOL (EPOCH-BASED)

### 1. ⏱️ CƠ CHẾ TÍNH TOÁN THEO EPOCH (5 NGÀY)



**Mỗi Epoch (5 ngày), hệ thống tính:**

* Số ADA stake trong pool của người chơi
* Phần thưởng stake nhận được
* Tự động chuyển % reward vào Prize Pool

#### 🧮 Công thức Donate Tự Động:

DonateAmount=(StakeReward×DonateRate)+FixedBonus

Trong đó:

* `Stake_Reward` = ADA nhận được từ staking mỗi epoch (\~4–5% APY)
* `Donate_Rate` = Tỷ lệ tự động donate (tuỳ chọn 10%, 25%, 50%)
* `Fixed_Bonus` = Thưởng thêm nếu stake liên tục

***

### 2. 📊 BẢNG TỶ LỆ DONATE THEO STAKE



| Stake Amount (ADA) | Donate Rate | Epoch Bonus (ADA) | NFT Tier     |
| ------------------ | ----------- | ----------------- | ------------ |
| 1,000 - 5,000      | 10%         | 2                 | 🟤 Đồng      |
| 5,001 - 20,000     | 25%         | 5                 | ⚪ Bạc        |
| 20,001 - 100,000   | 50%         | 10                | 🟡 Vàng      |
| 100,000+           | 75%         | 20                | 💎 Kim Cương |

#### 📌 Ví dụ:



Người chơi stake 10,000 ADA (Tier Bạc):

* Stake reward/epoch ≈ 10 ADA
* Donate = (10 × 25%) + 5 = **7.5 ADA/epoch**

***

### 3. 🔁 CƠ CHẾ KHUYẾN KHÍCH DÀI HẠN



#### 📈 Multiplier Theo Số Epoch Liên Tục:



| Epochs Staked | Donate Multiplier |
| ------------- | ----------------- |
| 1–5           | 1.0×              |
| 6–15          | 1.2×              |
| 16–30         | 1.5×              |
| 31+           | 2.0×              |

#### 📌 Ví dụ:



Stake 50,000 ADA (Tier Vàng) qua 20 epoch:

* Reward/epoch ≈ 50 ADA
* Donate = (50 × 50% × 1.5) + 10 = **47.5 ADA/epoch**

***

### 4. ⚙️ QUY TRÌNH TỰ ĐỘNG



#### 🔄 Flow Sequence:



<details>

<summary></summary>



</details>

***

### 5. 🎁 LỢI ÍCH CHO NGƯỜI CHƠI



* 🔄 **Tự động hóa**: Không cần manual donate
* 💰 **Lợi kép**: Vừa nhận stake reward, vừa được game bonus
* 🎮 **Ưu đãi tích hợp**:
  * Donate ≥ 50 ADA/epoch → Vé tournament VIP
  * Donate ≥ 100 ADA/epoch → Quyền đề xuất luật game

***

### 6. 🛡️ KIỂM SOÁT RỦI RO



* ⚠️ **Giới hạn donate tối đa**: 80% stake reward
* 🔐 **Smart Contract an toàn**:
  * Chỉ chuyển % reward, không động vào stake gốc
  * Có thể hủy auto-donate bất kỳ lúc nào

***

### 7. 📈 VÍ DỤ TÁC ĐỘNG PRIZE POOL



**Giả sử:**

* 100 người stake trung bình 10,000 ADA
* Mỗi epoch:
  * Tổng donate ≈ 100 × 7.5 = **750 ADA**
  * Prize Pool tăng thêm ≈ 750 × 0.5 (matching) = **375 ADA**

📅 Sau 1 tháng (6 epoch): **Prize Pool +2,250 ADA**
