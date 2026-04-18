# HCE-FMS: Hệ thống Quản lý Tài chính và Học phí Tích hợp AI

HCE-FMS là hệ thống quản lý tài chính và học phí thông minh, tập trung vào việc tự động hóa 95% các nghiệp vụ tài chính tại môi trường giáo dục. Hệ thống được phát triển bởi Nhóm 11 với mục tiêu cốt lõi là tính chính xác, khả năng kiểm soát thay đổi và trải nghiệm người dùng tối giản.

## 1. Mục tiêu Chiến lược (Core Insights)

### Tự động hóa
Đạt tỷ lệ 95% tự động hóa trong các quy trình Thanh toán, Đối soát và Hoàn phí.

### Tiêu chuẩn SUPL02
Thời gian đào tạo cán bộ kế toán mới phải dưới 2 giờ. Mọi thiết kế giao diện phải tối giản.

### Toàn vẹn dữ liệu
Đảm bảo tính truy xuất nguồn gốc thông qua Ma trận dấu vết (Traceability Matrix) từ yêu cầu đến code và kiểm thử.

## 2. Các Module Chức năng chính

### Thu học phí
Thanh toán online, tích hợp Webhook ngân hàng và phát hiện giao dịch bất thường.

### Công nợ
Quản lý nợ đọng và dự báo khả năng nợ xấu bằng AI.

### Hoàn phí
Quy trình rollback tự động khi có sự cố mạng hoặc lỗi hệ thống.

### Hỗ trợ vay vốn
Kết nối tín dụng dựa trên lịch sử học tập và tài chính.

### AI Analytics
Dự báo dòng tiền và báo cáo tài chính thông minh (Trọng tâm của MVP v1.0).

## 3. Quy tắc Quản trị và Kỹ thuật (Governance)

Mọi hoạt động phát triển phải tuân thủ các quy tắc sau:

### Quy trình CCB (Change Control Board)
Mọi thay đổi phải đi qua 5 bước: Submit -> Review -> Approve -> Implement -> Verify.

### Ma trận Dấu vết (Traceability)
- Mọi Use Case (UC) phải được link trực tiếp đến một Feature (FEAT) tương ứng.
- Mọi đoạn code phải có Ca kiểm thử (Test Case) đi kèm, đặc biệt là các kịch bản lỗi (Rollback khi sập mạng, Hủy giao dịch quá hạn).

### Hệ thống Nhãn (Labeling)
Khi tạo Issue hoặc Commit, phải sử dụng hệ thống nhãn sau:

- **Priority**: Must (Bắt buộc cho MVP), Should, Could.
- **Difficulty**: High, Medium, Low.
- **Stability**: Stable, Low (Các yêu cầu có độ ổn định thấp cần được ưu tiên phân tích kỹ).

## 4. Hướng dẫn cho AI Agent (System Prompt)

Sử dụng nội dung dưới đây làm chỉ thị cho AI Agent làm việc trên Repository này:

### Role
Bạn là Chuyên gia DevOps/TestOps thuộc Nhóm 11 của dự án HCE-FMS.

### Context
Bạn đang làm việc trên mã nguồn của MVP v1.0. Bạn phải tuân thủ nghiêm ngặt tài liệu RMP và các tài liệu BPMN đã thống nhất.

### Guidelines
- Khi viết code mới, hãy kiểm tra xem logic có phù hợp với tiêu chuẩn SUPL02 (Dễ sử dụng) hay không.
- Mọi logic giao dịch tài chính phải có hàm Rollback hoặc xử lý lỗi khi mất kết nối.
- Khi thực hiện Push code hoặc Commit, hãy phân loại theo nhãn: Type (FEAT/BUG), Priority (Must), và ghi rõ Use Case liên quan.
- Ưu tiên giải quyết các yêu cầu có nhãn Stability: Low để giảm thiểu rủi ro cho dự án.
- Luôn đảm bảo Forward Traceability: Code phải tương ứng với yêu cầu trong tài liệu quản lý của nhóm.

## 5. Cấu trúc Kho lưu trữ (Repository Structure)

```
docs/          - Tài liệu RMP, BPMN, Kế hoạch quản lý rủi ro.
src/           - Mã nguồn ứng dụng.
tests/         - Kịch bản kiểm thử và dữ liệu đối soát.
scripts/       - Script tự động hóa quy trình CI/CD và thông báo.
.github/       - Workflow quản lý Issue và quy trình CCB.
frontend/      - Frontend ReactJS application.
```

## 6. Lộ trình Phát triển (MVP v1.0 Roadmap)

1. Thiết lập RMP và công cụ quản lý trên GitHub Projects.
2. Chuẩn hóa biểu đồ BPMN cho các quy trình thanh toán và hoàn phí.
3. Xây dựng module Thu học phí tích hợp Webhook.
4. Triển khai module AI dự báo dòng tiền.
5. Hoàn thiện Usability Plan và Video đào tạo.

## 7. Công nghệ Sử dụng

### Frontend
- ReactJS
- Tailwind CSS
- Lucide React Icons
- React Router

### Backend
- Spring Boot
- Java
- Redis
- AI Integration

## 8. Quy trình Phát triển

### Quy trình CCB
1. **Submit**: Đệ trình yêu cầu thay đổi
2. **Review**: Đánh giá bởi team
3. **Approve**: Phê duyệt thay đổi
4. **Implement**: Triển khai code
5. **Verify**: Kiểm thử và xác nhận

### Quy trình Commit
- Format: `[Type] Priority: Description - Use Case`
- Ví dụ: `[FEAT] Must: Add payment webhook - UC05`

---

**Copyright 2026 Group-11-PT-ICTU-Alternative. All rights reserved.**
