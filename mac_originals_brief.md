# 工单：把 notion-archive 里标着「未取得」的原件补存进去

Frank 2026-11-08 批准。Frank 人在电脑旁：遇到 DocSend 邮件验证或 captcha 时，在对话里请他处理。草稿 · Frank 确认前不对外使用；只做本单。

## 准备
1. 仓库：`~/notion-archive`（hfu26/notion-archive）。不存在就 `git clone https://github.com/hfu26/notion-archive ~/notion-archive`，否则先 `git pull`。另需 `~/meeting-pipeline`（hfu26/meeting-pipeline，用来跑检查脚本），同样 clone 或 pull。
2. skill：`~/.claude/skills/docsend2pdf`，必须是 hfu26/claude-config 的最新版（含 rename.py 和 data room 表格路线，commit 5a43845），用前先 pull。按 SKILL.md 的三种方式依次尝试：
   - 先用 convert.sh，email 填 frank@iosg.vc；
   - 失败再用 direct.py；
   - 再不行用浏览器方式（pinchtab / agent-browser，或 Claude 内置浏览器），驱动 Frank 自己的 Chrome。
   data room 里的 Excel，按 SKILL.md 新增的「Data-room spreadsheets」一节处理。每份下载后都用 rename.py 改成可读名，优先用 DocSend 原标题（--name）。
3. 不要把任何 token、cookie、口令写进文件或提交。

## 要补的原件（链接 → 放进哪个文件夹的 files/）
所有路径都相对 `~/notion-archive/`。同一份原件对应多个文件夹时，每个文件夹都放一份。

### DocSend
- 已全部由云端会话完成(2026-11-08):Compute Labs、1Money、Combinder、Grimoire、Arbital 已入库;其余 7 条为发送方关闭链接,已记录。本单不再处理 DocSend。

### Google Drive
在 Frank Mac 的 Google Drive 同步目录里找（通常在 ~/Library/CloudStorage/GoogleDrive-*/ 下）：
- 1F-GiMIYGFixyEAnTG1sgjYkk9T3mdqE-「Compute Labs Memo v.F - Benji Siem.pptx」（≈12.8MB，owner yiping@iosg.vc）→ Meeting Materials/Compute Labs Memo v.F - Benji Siem__1F-GiMIY，以及 Compute Labs Summary (2-4-2026)__2fcf0ada
- 1dRVLKw7VLT2OXdTNd7nU4ZgTc1OVEvr7「Immersve Memo v.1 - Benji Siem.pptx」（≈7.1MB）→ Meeting Materials/Immersve Memo v.1 - Benji Siem__1dRVLKw7
- 1nWDt5GZ9ft4lf3zYOgBjdi-dWmIwD8uv（Index network 页里的 Drive 文件，名字未知）→ Meeting Materials/Index network summary 12-14-2025__2c4f0ada。同步目录里找不到，就在浏览器打开 https://drive.google.com/file/d/1nWDt5GZ9ft4lf3zYOgBjdi-dWmIwD8uv/view 下载；没权限就跳过。

不要碰这两个：1t8v0NYsmpjbxkb-hQ3yBN3QNtUJPxuTp（Frank 已决定不追）、b2evijv4mfp66tm9（链接已失效）。

## 每存一件
在该文件夹 README.md 末尾的 `## 原文件 / Originals` 一节：
- 删掉对应的那行 `- 未取得 <id> — …`；
- 加一行 `- [<文件名>](files/<URL 编码的文件名>) ← docsend.com/view/<id>`（Drive 文件写成 `← drive.google.com/file/d/<id>`）；
- 实在拿不到的，把「未取得」那行的原因改成这次的真实原因（比如「Frank 浏览器也要求口令，未提供」）。

## 提交
1. 跑检查：`python3 ~/meeting-pipeline/scripts/check_md_pitfalls.py --archive ~/notion-archive`，必须输出 clean。
2. 在 ~/notion-archive 提交。commit message 用中文写清补了哪些，结尾加两行：
   `Co-Authored-By: Claude Opus 5.5 <noreply@anthropic.com>`
   `Claude-Session: <本会话链接>`
3. 推送到 main：先 `git pull --rebase`；单次推送超过约 80MB，就拆成几个 commit 分开推。
4. 最后在对话里列清楚：存了哪些（文件名 → 文件夹）、哪些仍未取得及原因、commit 哈希。Frank 会把结果转给云端主会话核对。
