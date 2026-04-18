# HCE-FMS: Hệ thống Quản lý tài chính – học phí tích hợp AI

## Giới thiệu
HCE-FMS (HCE Financial Management System) là Hệ thống Quản lý tài chính và học phí tích hợp AI được thiết kế và phát triển dành riêng cho Trường Cao đẳng Kinh tế TP.HCM (HCE). 
Mục tiêu cốt lõi của hệ thống là tự động hóa đến 95% quy trình nghiệp vụ kế toán, giải quyết triệt để tình trạng làm việc thủ công, đối soát chậm chạp, dữ liệu phân tán và giảm thiểu thời gian xếp hàng chờ đợi của sinh viên.

## Mục tiêu dự án
- Tự động hóa thanh toán: Loại bỏ hoàn toàn quy trình đóng học phí thủ công.
- Gạch nợ tức thời (Real-time): Hệ thống tự động giảm trừ số tiền công nợ của sinh viên ngay lập tức sau khi nhận được thông báo chuyển khoản thành công từ ngân hàng thông qua công nghệ Webhook, không cần kế toán thao tác tay.
- Đồng bộ dữ liệu: Nhắc nợ đồng bộ và đối soát tự động, đảm bảo dòng tiền khớp với sao kê ngân hàng.

## Lộ trình phát triển (Roadmap)

### Phiên bản v1.0 (MVP) - Cốt lõi Thanh toán
Được thiết kế để triển khai sớm các tính năng quan trọng nhất (Must-have):
- Thanh toán học phí trực tuyến (FEAT01 / UC05).
- Nhắc nợ đồng bộ cho sinh viên.
- Gạch nợ tự động bằng công nghệ Webhook.

### Phiên bản v1.1 - Số hóa Vay vốn
- Tích hợp module Hỗ trợ vay vốn online, giúp rút ngắn quy trình nộp hồ sơ và xét duyệt vốn chậm chạp của Phòng Công tác sinh viên.

### Phiên bản v2.0 - Trí tuệ nhân tạo (AI) & Báo cáo
- Tích hợp AI dự báo doanh thu, giúp nhà trường hoạch định tài chính chính xác.
- Cung cấp Dashboard báo cáo quản trị chuyên sâu theo thời gian thực phục vụ Ban Giám hiệu.

*(Ngoài phạm vi (Out of Scope): Dự án hiện tại không bao gồm các chức năng: Quản lý lương cán bộ, Khấu hao tài sản cố định và Kế toán nội bộ).*

## Môi trường & Công cụ
Hệ thống quản lý và phát triển dựa trên các công cụ chuẩn quy trình phần mềm:
- Quản lý dự án & Backlog: GitHub / Jira
- Thiết kế giao diện (Prototype): Figma
- Mô hình hóa (BPMN, Use Case): Draw.io
- Lưu trữ & Chia sẻ tài liệu: Google Drive

## Đảm bảo chất lượng & Rủi ro
- Quản lý thay đổi (Change Management): Mọi yêu cầu thay đổi (CR) đều đi qua Hội đồng kiểm soát thay đổi (CCB) với quy trình 5 bước nghiêm ngặt: Submit -> Review -> Approve -> Implement -> Verify.
- Cơ chế Rollback dữ liệu: Xử lý triệt để các kịch bản rớt mạng, sập nguồn bằng cơ chế Transaction Rollback, đảm bảo sinh viên không bị mất tiền oan nếu giao dịch bị gián đoạn.
- Dấu vết yêu cầu (Traceability): 100% Use Case được ánh xạ xuôi tới các Ca kiểm thử (Test Cases) đảm bảo đúng nghiệp vụ.

## Đội ngũ phát triển (Nhóm 11)
- Đào Đức Mạnh (Trưởng nhóm): Demo Web, thiết lập GitHub, mô hình hóa quy trình BPMN.
- Nguyễn Minh Đức: Phân tích Stakeholders, định nghĩa Thuật ngữ (Glossary).
- Lý Minh Hiếu: Lập kế hoạch quản lý yêu cầu (RMP), Yêu cầu bổ sung (SUPL).
- Tạ Đức Phúc: Xây dựng Tài liệu tầm nhìn (Vision Document), Kịch bản (Scenarios).
- Dương Quang Tiệp: Đặc tả Use Cases, Yêu cầu bổ sung (SUPL).
