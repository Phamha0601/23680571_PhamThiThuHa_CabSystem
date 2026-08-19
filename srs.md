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
```text
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
```

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

| Mã | Tên | Diễn giải |
|---|---|---|
| BR01 | Đặt chuyến xe | Hệ thống cho phép khách hàng đặt chuyến bằng cách xác định vị trí hiện tại, điểm đón, điểm đến và lựa chọn loại xe phù hợp. |
| BR02 | Tìm và phân công tài xế | Hệ thống cho phép tìm và lựa chọn tài xế phù hợp với chuyến đi dựa trên vị trí, trạng thái sẵn sàng và các tiêu chí vận hành. |
| BR03 | Theo dõi chuyến đi | Hệ thống cho phép khách hàng theo dõi trạng thái chuyến đi trong suốt quá trình di chuyển. |
| BR04 | Quản lý tài xế | Hệ thống cho phép doanh nghiệp quản lý thông tin tài xế, phương tiện và trạng thái hoạt động của tài xế. |
| BR05 | Quản lý chuyến đi | Hệ thống cho phép quản lý và cập nhật trạng thái chuyến đi từ khi tạo yêu cầu đến khi hoàn thành hoặc hủy chuyến. |
| BR06 | Tính cước | Hệ thống cho phép xác định số tiền khách hàng phải trả dựa trên loại dịch vụ và thông tin chuyến đi. |
| BR07 | Thanh toán | Hệ thống cho phép khách hàng thanh toán bằng tiền mặt hoặc phương thức thanh toán điện tử thông qua nhà cung cấp thanh toán bên ngoài. |
| BR08 | Thông báo | Hệ thống cung cấp thông báo cho khách hàng và tài xế về các sự kiện quan trọng trong quá trình đặt và thực hiện chuyến. |
| BR09 | Đánh giá tài xế | Hệ thống cho phép khách hàng đánh giá tài xế sau khi chuyến đi hoàn thành. |
| BR10 | Quản lý vận hành | Hệ thống cung cấp giao diện để nhân viên vận hành quản lý khách hàng, tài xế, phương tiện, chuyến đi và giao dịch. |
| BR11 | Báo cáo hoạt động | Hệ thống cung cấp báo cáo về số lượng chuyến, doanh thu, tỷ lệ hoàn thành, tỷ lệ hủy và hiệu quả hoạt động của tài xế. |
| BR12 | Bảo mật và phân quyền | Hệ thống đảm bảo người dùng được xác thực, phân quyền phù hợp và bảo vệ thông tin cá nhân, dữ liệu vị trí và giao dịch. |


#B6: Business Process (dùng mermaid)
# Business Process – CAB System
1. Quy trình đặt chuyến xe – BR01

```mermaid
flowchart TD
    A([Bắt đầu]) --> B[Khách hàng đăng nhập]
    B --> C[Nhập vị trí hiện tại]
    C --> D[Nhập điểm đón]
    D --> E[Nhập điểm đến]
    E --> F[Chọn loại xe]
    F --> G[Gửi yêu cầu đặt xe]
    G --> H[Hệ thống tiếp nhận yêu cầu]
    H --> I[Thông báo yêu cầu đã được tiếp nhận]
    I --> J([Chuyển sang tìm tài xế])
```
2. Quy trình tìm và phân công tài xế – BR02
```mermaid
flowchart TD
    A([Nhận yêu cầu đặt xe]) --> B[Xác định các tài xế phù hợp]
    B --> C[Kiểm tra vị trí tài xế]
    C --> D[Kiểm tra trạng thái sẵn sàng]
    D --> E[Ưu tiên tài xế phù hợp và gần khách hàng]
    E --> F{Có tài xế phù hợp?}

    F -- Không --> G[Thông báo không tìm được tài xế]
    G --> H([Kết thúc])

    F -- Có --> I[Gửi yêu cầu chuyến đến tài xế]
    I --> J{Tài xế phản hồi?}

    J -- Không --> K[Chờ hết thời gian phản hồi]
    K --> L[Tìm tài xế tiếp theo]
    L --> I

    J -- Có --> M{Tài xế chấp nhận?}
    M -- Không --> L
    M -- Có --> N[Phân công chuyến cho tài xế]
    N --> O[Thông báo cho khách hàng]
    O --> P([Bắt đầu chuyến])
```

#B7: Phân rã yêu cầu về chức năng
| FR       | Chức năng         | Mô tả                                                                    |
| -------- | ----------------- | ------------------------------------------------------------------------ |
| **FR01** | Quản lý tài khoản | Đăng ký, đăng nhập và cập nhật thông tin người dùng.                     |
| **FR02** | Đặt xe            | Nhập điểm đón, điểm đến và chọn loại xe để gửi yêu cầu.                  |
| **FR03** | Tìm tài xế        | Xác định và ưu tiên tài xế phù hợp, gần khách hàng.                      |
| **FR04** | Phân công tài xế  | Gửi yêu cầu cho tài xế và tìm tài xế khác nếu bị từ chối.                |
| **FR05** | Quản lý chuyến đi | Theo dõi và cập nhật trạng thái chuyến đi.                               |
| **FR06** | Theo dõi vị trí   | Lưu và cập nhật vị trí tài xế để hỗ trợ tìm xe và dự kiến thời gian đến. |
| **FR07** | Tính cước         | Tính số tiền khách hàng phải trả dựa trên thông tin chuyến đi.           |
| **FR08** | Thanh toán        | Hỗ trợ thanh toán tiền mặt và thanh toán điện tử.                        |
| **FR09** | Thông báo         | Gửi thông báo về đặt xe, tài xế, chuyến đi và thanh toán.                |
| **FR10** | Đánh giá tài xế   | Cho phép khách hàng đánh giá tài xế sau khi hoàn thành chuyến.           |
| **FR11** | Quản lý vận hành  | Quản lý khách hàng, tài xế, phương tiện và chuyến đi.                    |
| **FR12** | Báo cáo           | Cung cấp báo cáo về chuyến đi, doanh thu, tỷ lệ hủy và hiệu quả tài xế.  |
| **FR13** | Phân quyền        | Kiểm soát quyền truy cập các chức năng quản trị.                         |
| **FR14** | Quản lý lịch sử   | Tra cứu lịch sử chuyến đi và giao dịch.                                  |

## B8: Business Goal and Acceptance Criteria

| ID       | Business Goal                                | Acceptance Criteria                                                                                                                                                                                                                                                                                    |
| -------- | -------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **BG01** | **Ưu tiên tài xế phù hợp**                   | • Ưu tiên tài xế đang sẵn sàng nhận chuyến.<br>• Ưu tiên tài xế có vị trí gần khách hàng.<br>• Có thể xem xét thêm ranking/đánh giá tài xế.<br>• Không đề xuất tài xế đang bận hoặc không sẵn sàng.                                                                                                    |
| **BG02** | **Giảm thời gian tìm tài xế**                | • Hệ thống tự động tìm tài xế sau khi khách hàng đặt xe.<br>• Gửi yêu cầu đến tài xế phù hợp.<br>• Tài xế không phản hồi trong thời gian quy định được xem là không nhận chuyến.<br>• Hệ thống tiếp tục tìm tài xế khác.                                                                               |
| **BG03** | **Xử lý tài xế từ chối hoặc không phản hồi** | • Nếu tài xế từ chối, hệ thống tìm tài xế khác.<br>• Nếu tài xế không phản hồi, hệ thống chuyển sang tài xế khác.<br>• Không gửi lại yêu cầu cho tài xế đã từ chối cùng chuyến.<br>• Khách hàng không cần tạo lại yêu cầu.                                                                             |
| **BG04** | **Xử lý khi không tìm được tài xế**          | • Nếu khu vực không có tài xế phù hợp, hệ thống thông báo cho khách hàng.<br>• Không để yêu cầu ở trạng thái “đang tìm tài xế” vô thời hạn.<br>• Lưu trạng thái không tìm được tài xế.<br>• Khách hàng có thể thực hiện lại yêu cầu.                                                                   |
| **BG05** | **Theo dõi trạng thái chuyến đi**            | • Khách hàng biết tài xế đã nhận chuyến.<br>• Cập nhật khi tài xế đến điểm đón.<br>• Cập nhật khi đã đón khách.<br>• Cập nhật khi đang di chuyển.<br>• Cập nhật khi chuyến hoàn thành.                                                                                                                 |
| **BG06** | **Đảm bảo thanh toán thành công**            | • Xác định số tiền phải thanh toán sau khi chuyến hoàn thành.<br>• Hỗ trợ nhiều phương thức thanh toán.<br>• Ghi nhận giao dịch khi thanh toán thành công.<br>• Thông báo kết quả thanh toán cho khách hàng.                                                                                           |
| **BG07** | **Xử lý thanh toán thất bại**                | • Thông báo cho khách hàng khi thanh toán thất bại.<br>• Ghi nhận giao dịch ở trạng thái thất bại.<br>• Cho phép thanh toán lại theo chính sách doanh nghiệp.<br>• Lỗi thanh toán không làm toàn bộ hệ thống đặt xe ngừng hoạt động.<br>• Không lưu thông tin thẻ nhạy cảm.                            |
| **BG08** | **Hỗ trợ thanh toán tiền mặt**               | • Khách hàng có thể chọn tiền mặt.<br>• Ghi nhận số tiền cần thanh toán.<br>• Ghi nhận kết quả thanh toán theo quy định.<br>• Lưu lịch sử giao dịch.                                                                                                                                                   |
| **BG09** | **Đảm bảo thông báo kịp thời**               | • Thông báo khi yêu cầu được tiếp nhận.<br>• Thông báo khi tài xế nhận chuyến.<br>• Thông báo khi tài xế đến điểm đón.<br>• Thông báo khi chuyến hoàn thành.<br>• Thông báo kết quả thanh toán.<br>• Tài xế nhận thông báo khi có chuyến mới.                                                          |
| **BG10** | **Xử lý hủy chuyến**                         | • Khách hàng chỉ được hủy theo chính sách doanh nghiệp.<br>• Cập nhật trạng thái chuyến thành “Đã hủy”.<br>• Thông báo cho tài xế khi chuyến bị hủy.<br>• Xác định phí hủy nếu có.<br>• Lưu lịch sử hủy chuyến.                                                                                        |
| **BG11** | **Đảm bảo bảo mật và phân quyền**            | • Người dùng phải xác thực trước khi sử dụng chức năng yêu cầu tài khoản.<br>• Nhân viên chỉ được thực hiện thao tác theo quyền được cấp.<br>• Ngăn người không có quyền thực hiện thao tác quản trị nhạy cảm.<br>• Lưu vết các thao tác quan trọng.<br>• Bảo vệ dữ liệu cá nhân, vị trí và giao dịch. |
| **BG12** | **Xử lý mất kết nối mạng**                   | • Không hủy chuyến ngay khi tài xế mất kết nối tạm thời.<br>• Ghi nhận thời điểm mất kết nối.<br>• Đồng bộ lại trạng thái khi tài xế kết nối lại.<br>• Xử lý theo chính sách nếu mất kết nối quá lâu.<br>• Thông báo cho khách hàng nếu ảnh hưởng đến chuyến.                                          |
| **BG13** | **Nâng cao chất lượng dịch vụ**              | • Khách hàng được đánh giá sau khi chuyến hoàn thành.<br>• Không cho phép đánh giá chuyến chưa hoàn thành.<br>• Lưu kết quả đánh giá.<br>• Sử dụng dữ liệu đánh giá để theo dõi chất lượng tài xế.                                                                                                     |
| **BG14** | **Hỗ trợ báo cáo hoạt động**                 | • Có thông tin số lượng chuyến.<br>• Có thông tin doanh thu.<br>• Có tỷ lệ chuyến hoàn thành.<br>• Có tỷ lệ chuyến hủy.<br>• Có thông tin hiệu quả hoạt động của tài xế.                                                                                                                               |

