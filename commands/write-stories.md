---
description: Chuyển PRD hoặc mô tả tính năng thành backlog có user story, acceptance criteria, trạng thái biên và dependency.
argument-hint: "<PRD, tính năng hoặc phạm vi cần chia nhỏ>"
---

# /write-stories — Chia backlog

**Ngôn ngữ | Language:** Match the requester’s language. When asked for bilingual output, write paired Vietnamese-English user stories and acceptance criteria.

1. Xác định outcome, persona, phạm vi in/out và luồng người dùng trước khi tách ticket.
2. Chia theo lát cắt tạo giá trị cho người dùng; tránh tách thuần theo layer kỹ thuật nếu không cần thiết.
3. Mỗi item phải có user story, giá trị, acceptance criteria quan sát được và dependency/câu hỏi mở.
4. Bổ sung loading, empty, error, permission, mobile/accessibility và analytics khi áp dụng.
5. Gắn nhãn MVP, fast-follow hoặc out of scope để tránh hiểu nhầm về cam kết.
6. Trả về danh sách backlog theo mẫu `Backlog item` trong `references/templates-vi.md`, sắp theo thứ tự triển khai hợp lý.

Không tự tạo API contract, thiết kế UI hoặc estimate kỹ thuật khi đầu vào không cung cấp.
