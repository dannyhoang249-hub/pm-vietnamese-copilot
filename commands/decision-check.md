---
description: Phản biện chất lượng một quyết định PM bằng giả định rõ ràng, scope tối giản, đánh đổi và tiêu chí kiểm chứng.
argument-hint: "<ý tưởng, PRD, roadmap, quyết định hoặc kế hoạch cần kiểm tra>"
---

# /decision-check — Kiểm tra chất lượng quyết định

**Nguồn cảm hứng | Inspiration:** chuyển bốn nguyên tắc của `multica-ai/andrej-karpathy-skills` thành workflow cho product management.

**Ngôn ngữ | Language:** Match the requester’s language. When asked for bilingual output, use paired Vietnamese-English headings and a single shared set of facts, assumptions, and numbers.

1. **Nghĩ trước khi làm | Think before acting:** tách facts, assumptions và unknowns. Nếu có nhiều cách hiểu hợp lý, trình bày chúng cùng tác động đến quyết định; không âm thầm chọn một cách hiểu.
2. **Đơn giản trước | Simplicity first:** xác định phiên bản nhỏ nhất có thể kiểm chứng outcome. Loại bỏ scope, abstraction, metric hoặc process được thêm chỉ để phòng xa.
3. **Phạm vi có chủ đích | Surgical scope:** đối chiếu từng hạng mục với user outcome hoặc constraint đã nêu. Đánh dấu phần ngoài scope và dependency chưa được chứng minh cần thiết.
4. **Thực thi theo mục tiêu | Goal-driven execution:** định nghĩa success criteria, failure/stop condition, cách đo, owner và bước xác thực kế tiếp. Viết kế hoạch theo dạng `bước → tín hiệu kiểm chứng`.
5. Kết luận bằng một trong ba khuyến nghị: **proceed**, **simplify then proceed**, hoặc **validate before committing**.

Trả về format sau:

```markdown
# Decision quality check — [Tên] | Kiểm tra chất lượng quyết định — [Tên]

## Decision and intended outcome | Quyết định và outcome mong muốn
## Facts, assumptions, and unknowns | Sự thật, giả định và điều chưa biết
## Simpler viable path | Phương án đơn giản hơn vẫn khả thi
## Scope and trade-offs | Phạm vi và đánh đổi
## Success criteria and verification loop | Tiêu chí thành công và vòng lặp kiểm chứng
| Step / Bước | Verify with / Kiểm chứng bằng | Owner | Decision triggered / Quyết định được kích hoạt |
| --- | --- | --- | --- |

## Recommendation | Khuyến nghị
```
