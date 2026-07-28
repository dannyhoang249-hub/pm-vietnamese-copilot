# PM Copilot cá nhân song ngữ | Personal Bilingual PM Copilot

Skill PM **Việt–Anh** cho công việc hằng ngày: biến ghi chú rời rạc thành quyết định rõ ràng, tài liệu đủ để thực thi và kế hoạch đo lường được. This is a personal PM toolkit for turning incomplete notes into actionable, decision-ready deliverables in Vietnamese, English, or both.

> ## 🧠 Tư duy Karpathy cho Product Management
>
> Bộ skill tích hợp tư duy từ [multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills), được điều chỉnh cho **ra quyết định sản phẩm** thay vì chỉ code. Trước khi biến một yêu cầu thành PRD, roadmap hoặc feature, PM Copilot luôn ưu tiên:
>
> 1. **Think before acting | Nghĩ trước khi làm** — làm rõ facts, assumptions, cách hiểu khác nhau và đánh đổi; không âm thầm đoán ý.
> 2. **Simplicity first | Đơn giản trước** — chọn scope, experiment hoặc release nhỏ nhất vẫn kiểm chứng được outcome; không “future-proof” vô cớ.
> 3. **Surgical scope | Phạm vi có chủ đích** — mỗi requirement phải truy vết được về user outcome, risk hoặc constraint; không biến request nhỏ thành roadmap lớn.
> 4. **Goal-driven execution | Thực thi theo mục tiêu** — xác định `success criteria → signal → decision` trước khi commit nguồn lực.
>
> **Khi nào dùng:** ý tưởng còn mơ hồ, PRD/roadmap có nguy cơ phình scope, feature request đang solution-led, hoặc trước khi đưa quyết định go/no-go. Gọi `$pm-karpathy-thinking` hoặc `/decision-check`.

## Ngôn ngữ | Language

- **Tiếng Việt:** khi bạn viết/yêu cầu bằng tiếng Việt.
- **English:** when you write/request in English.
- **Song ngữ | Bilingual:** thêm `song ngữ`, `bilingual`, hoặc `VI/EN` vào prompt. Headings, quyết định, requirements, metric definitions và action items sẽ được ghi theo cả hai ngôn ngữ; không lặp lại phần diễn giải không cần thiết.

## Có gì trong bộ này?

| Khi cần | Dùng command | Kết quả |
| --- | --- | --- |
| Làm rõ ý tưởng hoặc vấn đề | `/discover` | Discovery brief, giả định rủi ro, thử nghiệm nhỏ nhất |
| Viết yêu cầu tính năng | `/write-prd` | Lean PRD, phạm vi, chỉ số, rủi ro và kế hoạch phát hành |
| Chia việc cho team | `/write-stories` | Backlog, acceptance criteria, trạng thái biên và analytics |
| Chọn việc nên làm trước | `/prioritize` | So sánh RICE có ghi rõ mức độ tin cậy và khuyến nghị |
| Thiết kế hệ đo lường | `/plan-metrics` | North Star, input/guardrail metrics và tracking plan |
| Đọc phản hồi người dùng | `/analyze-feedback` | Chủ đề, bằng chứng, cơ hội và hành động tiếp theo |
| Chốt sau cuộc họp | `/meeting-notes` | Quyết định, việc cần làm, người phụ trách và hạn |
| Rà rủi ro trước khi làm/ra mắt | `/pre-mortem` | Tigers, Paper Tigers, Elephants và checklist go/no-go |
| Phản biện một quyết định hoặc scope | `/decision-check` | Facts/assumptions, phương án đơn giản hơn và loop go/no-go |

Không cần command nếu yêu cầu đơn giản. Gọi `$pm-vietnamese-copilot`, `$pm-bilingual-copilot`, `$pm-karpathy-thinking` hoặc mô tả thẳng việc cần làm; skill sẽ chọn workflow phù hợp.

## Tutorial cài đặt và sử dụng | Installation tutorial

### 1. Chọn AI phù hợp | Choose your AI

| AI / môi trường | Mức hỗ trợ | Cách dùng |
| --- | --- | --- |
| **Claude Code / Claude Cowork** | Native plugin | Cài marketplace; dùng skills và `/commands`. |
| **Codex** | Native skill | Copy ba thư mục trong `skills/` vào `~/.codex/skills`. |
| **ChatGPT, Gemini, Perplexity, Microsoft Copilot** | Manual | Dán nội dung skill vào custom instructions/project hoặc prompt của cuộc trò chuyện. |
| **Cursor, Windsurf, VS Code Copilot, Cline** | Manual / tùy công cụ | Đưa `SKILL.md` vào project rules/instructions rồi dùng prompt mẫu. |

> **Lưu ý:** Không phải mọi AI đều hiểu định dạng Claude plugin hoặc Codex skill. Với các AI ở chế độ **Manual**, nội dung workflow vẫn dùng được nhưng `/commands` và `$skill-name` có thể không được nhận diện tự động.

### 2. Chuẩn bị repository | Prepare the repository

Clone repository hoặc tải file ZIP. Với Git:

```bash
git clone https://github.com/<owner>/<repo>.git
cd <repo>
```

Thay `<owner>/<repo>` bằng repository GitHub của bạn. Nếu đang làm trực tiếp trong repository này, bỏ qua bước clone.

### 3. Claude Code / Claude Cowork — cài native plugin

Thêm marketplace và cài plugin:

```bash
claude plugin marketplace add <owner>/<repo>
claude plugin install pm-vietnamese-copilot@pm-vietnamese-copilot
```

Plugin Claude bao gồm:

- **3 skills**
  - `$pm-vietnamese-copilot`: full PM workflow; tự chọn tiếng Việt, English hoặc song ngữ theo yêu cầu.
  - `$pm-bilingual-copilot`: chuyên tạo/chuyển giao artifact PM Việt–Anh cho product, engineering và stakeholders.
  - `$pm-karpathy-thinking`: phản biện một quyết định/PRD/roadmap theo bốn nguyên tắc: giả định rõ ràng, đơn giản trước, scope có chủ đích, và verification loop.
- **9 commands:** `/discover`, `/write-prd`, `/write-stories`, `/prioritize`, `/plan-metrics`, `/analyze-feedback`, `/meeting-notes`, `/pre-mortem`, `/decision-check`.

**Ví dụ 1 — gọi skill:**

```text
Use $pm-bilingual-copilot to create a Vietnamese-English PRD from the following feature notes.
```

**Ví dụ 2 — gọi command:**

```text
/prioritize Chọn giữa onboarding mới, import Excel và nhắc khách quay lại. Mục tiêu quý này là tăng activation. Trả về song ngữ VI/EN.
```

**Ví dụ 3 — quality gate trước khi commit:**

```text
Use $pm-karpathy-thinking to stress-test this proposal. Surface assumptions, reduce it to the smallest viable scope, and define a measurable proceed / simplify / validate decision.
```

Sau khi cài hoặc nâng cấp, mở một cuộc hội thoại Claude mới để metadata skill được nạp lại.

### 4. Codex — cài native skills

Repository có ba skills cho Codex:

- `pm-vietnamese-copilot`: workflow PM đầy đủ, hỗ trợ tiếng Việt, English và song ngữ.
- `pm-bilingual-copilot`: tối ưu cho tài liệu PM Việt–Anh.
- `pm-karpathy-thinking`: quality gate cho quyết định mơ hồ, scope quá lớn và kế hoạch cần một verification loop rõ ràng.

Copy cả ba thư mục vào thư mục skills cá nhân:

```bash
mkdir -p ~/.codex/skills
cp -R skills/pm-vietnamese-copilot ~/.codex/skills/pm-vietnamese-copilot
cp -R skills/pm-bilingual-copilot ~/.codex/skills/pm-bilingual-copilot
cp -R skills/pm-karpathy-thinking ~/.codex/skills/pm-karpathy-thinking
```

Khởi động một phiên Codex mới, sau đó dùng:

```text
Use $pm-vietnamese-copilot to turn these notes into a Lean PRD in English.
```

```text
Dùng $pm-bilingual-copilot để tạo decision memo song ngữ Việt–Anh từ các lựa chọn bên dưới.
```

```text
Use $pm-karpathy-thinking to review this roadmap item before we commit. Give a clear proceed, simplify then proceed, or validate before committing recommendation.
```

### 5. ChatGPT, Gemini, Perplexity, Microsoft Copilot — dùng thủ công

Các AI chat này có thể không tự nạp plugin từ repository. Dùng một trong hai cách sau:

#### Cách A — Custom GPT, Project, Gems hoặc Instructions

1. Mở `skills/pm-vietnamese-copilot/SKILL.md` để dùng workflow PM tổng quát; `skills/pm-bilingual-copilot/SKILL.md` nếu chủ yếu làm tài liệu Việt–Anh; hoặc `skills/pm-karpathy-thinking/SKILL.md` để phản biện quyết định và scope.
2. Copy toàn bộ nội dung file vào phần **Instructions**, **Project instructions**, **Custom GPT instructions** hoặc **Gem instructions** của AI bạn dùng.
3. Nếu AI hỗ trợ knowledge files, tải lên file `references/templates-bilingual.md` cùng skill đã chọn.
4. Tạo chat mới và dùng prompt bên dưới.

#### Cách B — Dùng trong một cuộc trò chuyện

1. Dán nội dung `SKILL.md` ở tin nhắn đầu tiên.
2. Dán prompt tác vụ ở tin nhắn tiếp theo.
3. Với yêu cầu song ngữ, luôn ghi rõ `Trả về song ngữ Việt–Anh` hoặc `Return a bilingual Vietnamese-English artifact`.

Prompt mẫu:

```text
Act as the PM Copilot defined above. Create a bilingual Vietnamese-English Lean PRD from these notes. Separate facts, assumptions, and recommendations. End with one recommended next action.

[Dán ghi chú tại đây]
```

### 6. Cursor, Windsurf, VS Code Copilot, Cline — dùng trong project

1. Thêm nội dung của `skills/pm-vietnamese-copilot/SKILL.md` vào project rules/instructions của công cụ bạn dùng. Nếu muốn áp dụng quality gate cho mọi đề xuất lớn, thêm cả `skills/pm-karpathy-thinking/SKILL.md`.
2. Nếu công cụ hỗ trợ reference files, thêm `references/templates-bilingual.md`.
3. Trong chat của IDE, ghi rõ artifact và ngôn ngữ mong muốn.

Ví dụ:

```text
Using the project PM instructions, review docs/onboarding-notes.md and write a bilingual Vietnamese-English prioritization memo. Label all estimates as assumptions.
```

### 7. Cập nhật | Update

Khi repository có thay đổi:

```bash
git pull
```

- **Claude:** cài lại hoặc nâng cấp plugin theo workflow marketplace của Claude, rồi mở chat mới.
- **Codex:** chạy lại ba lệnh `cp -R` ở bước 4, rồi mở phiên mới.
- **AI dùng manual:** copy lại `SKILL.md` và template mới vào instructions/project của bạn.

## Cách dùng

### Gọi nhanh theo workflow

```text
/discover Người bán online thường bỏ cuộc khi phải tạo sản phẩm từng cái một.

/write-prd Tính năng import sản phẩm từ file Excel cho ứng dụng quản lý bán hàng.

/prioritize Chọn giữa onboarding mới, import Excel và nhắc khách quay lại. Mục tiêu quý này là tăng activation.

/meeting-notes [dán transcript hoặc ghi chú họp]

/decision-check Kế hoạch xây một analytics dashboard mới với 25 chỉ số trước quý tới.
```

### Gọi skill trực tiếp

```text
Dùng $pm-vietnamese-copilot để chuyển các ghi chú dưới đây thành PRD tiếng Việt.
```

```text
Use $pm-vietnamese-copilot to evaluate these onboarding ideas. Write the recommendation in Vietnamese and keep key PM terms bilingual.
```

```text
Use $pm-bilingual-copilot to turn these meeting notes into a bilingual Vietnamese-English decision record for product and engineering.
```

```text
Use $pm-karpathy-thinking to challenge this feature proposal before we commit engineering time.
```

## Nguyên tắc làm việc

- **Theo ngôn ngữ và đối tượng đọc:** trả lời bằng tiếng Việt hoặc English theo yêu cầu; khi cần song ngữ, dùng tiêu đề và thông tin bàn giao quan trọng bằng cả hai ngôn ngữ.
- **Không bịa dữ liệu:** tách rõ sự thật, giả định và khuyến nghị; không tự tạo số liệu, trích dẫn khách hàng hay sự đồng thuận.
- **Ra quyết định trước, tài liệu sau:** ưu tiên quyết định, bằng chứng cần có và bước tiếp theo nhỏ nhất thay vì tạo tài liệu dài.
- **Thực thi được:** PRD/backlog luôn xét phạm vi, tiêu chí chấp nhận, trạng thái biên, phụ thuộc và cách đo lường khi phù hợp.
- **Thẳng thắn về rủi ro:** nếu thông tin thiếu, nêu giả định hợp lý và đề xuất cách kiểm chứng rẻ nhất.
- **Tư duy Karpathy:** làm rõ trước khi làm, đơn giản trước, giữ scope có chủ đích và đặt tín hiệu kiểm chứng trước khi commit.

## Cấu trúc repository

```text
.
├── SKILL.md                              # Skill dùng cho Claude plugin
├── commands/                             # Các workflow gọi bằng /command
├── references/                           # Mẫu PM tiếng Việt và song ngữ
├── skills/pm-vietnamese-copilot/         # Full PM workflow skill for Claude and GPT-5.5/Codex
├── skills/pm-bilingual-copilot/           # Bilingual PM skill for Claude and GPT-5.5/Codex
├── skills/pm-karpathy-thinking/           # Decision-quality skill inspired by Karpathy guidelines
└── .claude-plugin/                       # Metadata marketplace Claude
```

## Tuỳ biến cho cách làm việc của bạn

- Sửa `references/templates-vi.md` nếu team có format PRD, ticket hoặc decision log riêng.
- Sửa `references/templates-bilingual.md` để thay đổi thuật ngữ Việt–Anh chuẩn của team.
- Sửa command trong `commands/` để thêm framework, naming convention hoặc tiêu chuẩn release của bạn.
- Giữ `SKILL.md` ở root và `skills/pm-vietnamese-copilot/SKILL.md` đồng bộ khi thay đổi nguyên tắc cốt lõi.

## Ghi nhận

Tư duy phản biện và thực thi theo mục tiêu được lấy cảm hứng từ [multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills), vốn dựa trên các quan sát của Andrej Karpathy về các lỗi thường gặp của coding agents. Repository này không sao chép nguyên skill coding; bốn nguyên tắc được chuyển thể thành workflow PM Việt–Anh.

## License

[MIT](LICENSE)
