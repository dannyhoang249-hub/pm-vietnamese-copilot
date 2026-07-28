+# Vietnamese PM Copilot
+
+A Vietnamese-first, bilingual Agent Skill for turning incomplete product inputs into decision-ready, delivery-ready PM artifacts.
+
+Use it for product discovery, PRDs, user stories and acceptance criteria, prioritization, OKRs, roadmaps, metric plans, experiments, meeting synthesis, and stakeholder communication—in Vietnamese, English, or both.
+
+## Claude Code / Claude Cowork
+
+Install directly from GitHub:
+
+```bash
+claude plugin marketplace add dannyhoang249-hub/pm-vietnamese-copilot
+claude plugin install pm-vietnamese-copilot@pm-vietnamese-copilot
+```
+
+Then invoke it in a prompt:
+
+```text
+Dùng $pm-vietnamese-copilot để biến ghi chú dưới đây thành PRD tiếng Việt cho tính năng đặt lịch khám.
+```
+
+## Codex
+
+The canonical skill is in [`skills/pm-vietnamese-copilot`](skills/pm-vietnamese-copilot). It includes `SKILL.md`, Codex agent metadata, and Vietnamese-first templates.
+
+## What it covers
+
+- **Discovery:** problem framing, JTBD, assumptions, research, experiments
+- **Execution:** Lean PRDs, user stories, acceptance criteria, test scenarios
+- **Strategy:** outcomes, prioritization, roadmaps, OKRs
+- **Data & communication:** metric definitions, decision memos, meeting actions
+
+## License
+
+[MIT](LICENSE)
+EOF
cat > LICENSE <<'EOF'
+MIT License
+
+Copyright (c) 2026 Hoang Dung Nguyen
+
+Permission is hereby granted, free of charge, to any person obtaining a copy
+of this software and associated documentation files (the "Software"), to deal
+in the Software without restriction, including without limitation the rights
+to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
+copies of the Software, and to permit persons to whom the Software is
+furnished to do so, subject to the following conditions:
+
+The above copyright notice and this permission notice shall be included in all
+copies or substantial portions of the Software.
+
+THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
+IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
+FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
+AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
+LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
+OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
+SOFTWARE.
+EOF
file README.md LICENSE .claude-plugin/plugin.json skills/pm-vietnamese-copilot/SKILL.md
find . -maxdepth 4 -type f -not -path './.git/*' | sort