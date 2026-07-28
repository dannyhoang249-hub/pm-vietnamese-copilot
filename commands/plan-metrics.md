---
description: Thiết kế North Star, input metrics, guardrails và tracking plan cho sản phẩm, tính năng hoặc OKR.
argument-hint: "<sản phẩm, tính năng, outcome hoặc OKR>"
---

# /plan-metrics — Lập kế hoạch đo lường

**Ngôn ngữ | Language:** Match the requester’s language. When asked for bilingual output, preserve metric names, formulas, events, properties, and identifiers exactly.

1. Bắt đầu từ outcome và quyết định mà dữ liệu phải hỗ trợ; không bắt đầu từ danh sách event.
2. Đề xuất một North Star phù hợp, các input metrics có thể tác động và guardrails ngăn tối ưu cục bộ.
3. Với từng metric, nêu công thức, event/source, segment, baseline status, target, owner và cadence.
4. Lập tracking plan gồm event, thời điểm gửi, properties bắt buộc và mục đích. Giữ event name/code identifier nguyên trạng nếu được cung cấp.
5. Đặt decision rule trước: điều kiện nào dẫn đến ship, iterate, stop hoặc điều tra dữ liệu.
6. Nêu rủi ro dữ liệu như missing events, identity stitching, sample bias hoặc định nghĩa metric mơ hồ.
7. Trả về Measurement plan theo `references/templates-vi.md`.
