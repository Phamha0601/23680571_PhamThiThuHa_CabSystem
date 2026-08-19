# B1: Business Context (Ngữ cảnh nghiệp vụ) và Business Problem

### Khách hàng muốn giải quyết vấn đề gì?
- Tự động hóa việc đặt xe, tìm tài xế, theo dõi chuyến đi và quản lý thanh toán.

### Vì sao hệ thống hiện tại không thể đáp ứng?
- Phân công tài xế còn thủ công, dữ liệu thanh toán chưa tập trung, khó theo dõi chuyến và khó mở rộng khi số lượng người dùng tăng.

### Mục tiêu kinh doanh của CAB System
- Tự động hóa quy trình đặt xe và phân công tài xế.
- Nâng cao trải nghiệm khách hàng.
- Tăng hiệu quả vận hành, giảm thao tác thủ công.
- Quản lý tập trung chuyến đi, thanh toán và dữ liệu.
- Tăng khả năng mở rộng khi số lượng khách hàng và tài xế tăng.

### Ai sẽ sử dụng hệ thống này?
- Khách hàng (Customer).
- Tài xế (Driver).
- Nhân viên vận hành (Operator).
- Ban lãnh đạo (Management) để xem báo cáo.

### Giá trị hệ thống tạo ra so với hệ thống cũ
- Tự động hơn.
- Quản lý tập trung hơn.
- Theo dõi chuyến đi tốt hơn.
- Giảm chi phí và thao tác vận hành.
- Dễ mở rộng trong tương lai.

# B2: 
## 1. Xác định stakeholder

| Stakeholder                                        | Vai trò                                                            |
| -------------------------------------------------- | ------------------------------------------------------------------ |
| **Khách hàng (Customer)**                          | Đặt xe, theo dõi chuyến đi, thanh toán và đánh giá tài xế.         |
| **Tài xế (Driver)**                                | Nhận chuyến, thực hiện chuyến và cập nhật trạng thái.              |
| **Nhân viên vận hành (Operator)**                  | Quản lý khách hàng, tài xế, phương tiện, chuyến đi và xử lý sự cố. |
| **Ban lãnh đạo (Management)**                      | Theo dõi báo cáo, doanh thu và hiệu quả hoạt động.                 |
| **Nhà cung cấp thanh toán (Payment Provider)**     | Xử lý các giao dịch thanh toán điện tử.                            |
| **Nhà cung cấp thông báo (Notification Provider)** | Cung cấp dịch vụ gửi thông báo cho khách hàng và tài xế.           |
| **Business Analyst (BA)**                          | Phân tích nghiệp vụ, thu thập và làm rõ yêu cầu.                   |
| **Đội phát triển (Development Team)**              | Thiết kế, xây dựng và triển khai hệ thống CAB.                     |


##2: Vẽ Ma trận stakeholder để cho bt mức độ ảnh hưởng của các vai trò
 ## 3. Stakeholder Matrix

**Ma trận Stakeholder theo mức độ ảnh hưởng (Power) và mức độ quan tâm (Interest):**
### MA TRẬN STAKEHOLDER – POWER / INTEREST

|                         | **MỨC ĐỘ QUAN TÂM THẤP** | **MỨC ĐỘ QUAN TÂM CAO** |
|-------------------------|---------------------------|---------------------------|
| **ẢNH HƯỞNG CAO**       | 🟡 **KEEP SATISFIED**     | 🔴 **MANAGE CLOSELY**     |
|                         | • Nhà cung cấp thanh toán | • Ban lãnh đạo            |
|                         | • Nhà cung cấp thông báo  | • Nhân viên vận hành      |
| **ẢNH HƯỞNG THẤP**      | ⚪ **MONITOR**             | 🟢 **KEEP INFORMED**      |
|                         | • BA / Đội phát triển     | • Khách hàng               |
|                         |                           | • Tài xế                   |

### Chiến lược quản lý
- 🔴 **Manage Closely:** Thường xuyên trao đổi và tham gia quyết định.
- 🟡 **Keep Satisfied:** Đảm bảo nhu cầu và duy trì sự hài lòng.
- 🟢 **Keep Informed:** Cập nhật thông tin thường xuyên.
- ⚪ **Monitor:** Theo dõi và cập nhật khi cần.

### Sơ đồ Stakeholder Matrix

                    MỨC ĐỘ ẢNH HƯỞNG (POWER)
                              CAO
                               │
        KEEP SATISFIED        │        MANAGE CLOSELY
                               │
  • Nhà cung cấp thanh toán    │  • Ban lãnh đạo
  • Nhà cung cấp thông báo    │  • Nhân viên vận hành
                               │
───────────────────────────────┼────────────────────────
                               │
        MONITOR               │        KEEP INFORMED
                               │
  • BA / Đội phát triển        │  • Khách hàng
                               │  • Tài xế
                               │
                              THẤP
                         MỨC ĐỘ QUAN TÂM
                           THẤP  →  CAO

#B3: BUSINESS GOALS
1. BJ01 – Tăng tính linh hoạt và thuận tiện trong thanh toán:
* Hỗ trợ thanh toán bằng tiền mặt.
* Hỗ trợ thanh toán online/chuyển khoản.
--
2. BJ02 – Giảm thời gian chờ xe của khách hàng:
* Tìm tài xế tự động.
* Ưu tiên tài xế phù hợp và gần khách hàng.
---
3.  BJ03 – Nâng cao trải nghiệm đặt xe của khách hàng:
* Dễ dàng tạo yêu cầu đặt xe.
* Biết được trạng thái của yêu cầu đặt xe.
* Biết thông tin tài xế khi chuyến xe được xác nhận.
* Theo dõi được tình trạng chuyến đi.
---
4. BJ04 – Nâng cao hiệu quả quản lý và vận hành:
* Theo dõi được các chuyến xe đang diễn ra.
* Nắm được tình trạng hoạt động của tài xế.
* Hỗ trợ xử lý các trường hợp chuyến xe gặp vấn đề.
* Tra cứu được thông tin các giao dịch và chuyến đi.
---
5. BJ05 – Nâng cao hiệu quả hoạt động của tài xế
* Nắm được trạng thái hoạt động của tài xế.
* Phân công chuyến xe cho tài xế phù hợp.
* Ưu tiên tài xế có vị trí thuận lợi cho khách hàng.
* Hạn chế thời gian tài xế phải chờ nhận chuyến.
---
6. BJ06 – Nâng cao khả năng theo dõi và minh bạch thông tin chuyến đi
* Biết tài xế nào đang thực hiện chuyến.
* Biết thời gian dự kiến tài xế đến.
* Biết trạng thái hiện tại của chuyến xe.
* Tra cứu được lịch sử chuyến đi.
---
7. BJ07 – Nâng cao độ tin cậy của dịch vụ đặt xe
* Không làm gián đoạn toàn bộ dịch vụ khi thanh toán gặp lỗi.
* Không làm gián đoạn toàn bộ dịch vụ khi thông báo gặp lỗi.
* Có phương án xử lý khi không tìm được tài xế.
* Có phương án xử lý khi tài xế không phản hồi hoặc từ chối chuyến.
---
8. BJ08 – Nâng cao chất lượng thanh toán
* Hỗ trợ nhiều phương thức thanh toán.
* Thông báo rõ kết quả thanh toán.
* Có khả năng xử lý lại khi thanh toán điện tử thất bại.
* Bảo vệ thông tin thanh toán nhạy cảm của khách hàng.
---
9. BJ09 – Nâng cao chất lượng dịch vụ thông qua phản hồi khách hàng
* Đánh giá tài xế sau khi hoàn thành chuyến.
* Ghi nhận kết quả đánh giá của khách hàng.
* Sử dụng thông tin đánh giá để theo dõi chất lượng tài xế.
---
10. BJ10 – Nâng cao khả năng mở rộng của hệ thống
* Hệ thống có thể phục vụ số lượng lớn khách hàng và tài xế.
* Có thể mở rộng từng thành phần khi nhu cầu tăng.
* Có thể bổ sung các dịch vụ mới trong tương lai.
---

11. BJ11 – Tăng khả năng phát triển và thay đổi hệ thống
* Có thể thêm phương thức thanh toán mới.
* Có thể thêm nhà cung cấp thông báo mới.
* Có thể bổ sung các loại dịch vụ mới.
* Có thể thay đổi một số thành phần kỹ thuật khi cần thiết.
---
12. BJ12 – Nâng cao khả năng kiểm soát và bảo mật thông tin
* Bảo vệ thông tin cá nhân của khách hàng và tài xế.
* Bảo vệ dữ liệu vị trí.
* Bảo vệ dữ liệu giao dịch.
* Kiểm soát quyền truy cập của nhân viên.
* Lưu lại các thao tác quan trọng để phục vụ kiểm tra.


#B4: Xác định PHẠM VI SCOPE: 
1. Quản lý tài khoản người dùng
- Đăng ký và đăng nhập tài khoản khách hàng.
- Quản lý thông tin cá nhân khách hàng.
- Quản lý tài khoản và hồ sơ tài xế.
- Quản lý quyền truy cập của nhân viên vận hành và quản trị viên.
2. Quản lý tài xế và phương tiện
- Quản lý thông tin tài xế.
- Quản lý thông tin phương tiện.
- Theo dõi trạng thái hoạt động của tài xế.
- Theo dõi vị trí của tài xế.
- Quản lý khả năng nhận chuyến của tài xế.
3. Đặt xe và phân công tài xế
- Nhập điểm đón và điểm đến.
- Lựa chọn loại xe.
- Tiếp nhận yêu cầu đặt xe.
- Tìm kiếm tài xế phù hợp.
- Ưu tiên tài xế dựa trên vị trí, trạng thái và tiêu chí vận hành.
- Tiếp tục tìm tài xế khác khi tài xế từ chối hoặc không phản hồi.
- Thông báo khi không tìm được tài xế.
4. Quản lý chuyến đi
- Theo dõi trạng thái chuyến đi.
- Cập nhật trạng thái chuyến.
- Theo dõi thời gian dự kiến tài xế đến.
- Quản lý quá trình thực hiện chuyến.
- Xử lý các trường hợp chuyến bị hủy hoặc gặp sự cố.
- Lưu lịch sử chuyến đi.
5. Tính cước và thanh toán
- Xác định số tiền khách hàng phải trả.
- Hỗ trợ thanh toán bằng tiền mặt.
- Hỗ trợ thanh toán điện tử/chuyển khoản.
- Tích hợp với nhà cung cấp thanh toán bên ngoài.
- Xử lý kết quả thanh toán.
- Xử lý trường hợp thanh toán thất bại.
- Lưu lịch sử giao dịch.
- Không lưu trực tiếp thông tin nhạy cảm của thẻ hoặc tài khoản thanh toán.
6. Thông báo
- Thông báo cho khách hàng về trạng thái đặt xe.
- Thông báo khi tài xế nhận chuyến.
- Thông báo khi tài xế đến điểm đón.
- Thông báo khi chuyến hoàn thành.
- Thông báo kết quả thanh toán.
- Thông báo cho tài xế về chuyến mới và các thay đổi liên quan đến chuyến đi.
- Hỗ trợ mở rộng thêm các kênh thông báo trong tương lai.
7. Đánh giá và phản hồi
- Khách hàng đánh giá tài xế sau khi hoàn thành chuyến.
- Lưu thông tin đánh giá.
- Theo dõi chất lượng phục vụ của tài xế.
8. Quản trị và vận hành
- Quản lý khách hàng.
- Quản lý tài xế.
- Quản lý phương tiện.
- Theo dõi các chuyến đang diễn ra.
- Kiểm tra trạng thái tài xế.
- Hỗ trợ xử lý các chuyến bị lỗi.
- Tra cứu lịch sử giao dịch.
- Phân quyền các thao tác quản trị.
9. Báo cáo
- Báo cáo số lượng chuyến.
- Báo cáo doanh thu.
- Báo cáo tỷ lệ chuyến hoàn thành.
- Báo cáo tỷ lệ hủy chuyến.
- Báo cáo hiệu quả hoạt động của tài xế.
10. Bảo mật và kiểm soát
- Xác thực người dùng.
- Phân quyền truy cập.
- Bảo vệ thông tin cá nhân.
- Bảo vệ dữ liệu phương tiện.
- Bảo vệ dữ liệu vị trí.
- Bảo vệ dữ liệu giao dịch.
- Lưu vết các thao tác quan trọng.

#B5: Xác định Business Requirement
# B4. Business Requirements


#B6: Business Process (dùng mermaid)
khách hàng tạo chuyên đi -> hệ thống xác nhận yêu cầu khách hàng 
                            hệ thống tìm tài xế - nếu có: tài xế xác nhận hay từ từ chối -xác nhận
                                                                                        - từ chối :   
                                                - không có: 

