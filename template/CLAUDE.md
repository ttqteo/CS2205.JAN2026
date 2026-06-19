# CLAUDE.md — Marp Slide Template (rules)

Quy ước khi tạo/sửa slide trong folder này (và mọi deck dùng template này).

## Công cụ & định dạng
- Slide viết bằng **Marp** (`slide.template.md` là file chính). Tỉ lệ **16:9** (mặc định Marp) — không dùng 4:3.
- Render: `npx -y @marp-team/marp-cli <file>.md --html --allow-local-files -o <file>.html`
  - Xuất nộp: thêm `--pdf` hoặc `--pptx`. Luôn có `--allow-local-files` (vì nhúng logo/ảnh cục bộ).
- Xem khi soạn: extension **Marp for VS Code** hoặc mở file `.html`.

## Theme (BẮT BUỘC giữ nhất quán)
- **Primary: navy `#1F3A68`**. Nền trắng, chữ `#1d2b36`.
- **Font: Be Vietnam Pro** (nạp qua `@import` Google Fonts trong khối `style:`). Cần mạng khi render/mở HTML.
- Bố cục kiểu Beamer "VSE":
  - Thanh **header navy tràn viền** dính đỉnh = viết tiêu đề slide bằng `## ...`
  - Slide bìa / chuyển mục / cảm ơn = thêm `<!-- _class: lead -->` (không có thanh navy)
  - **Footer 4 ô gradient** navy: `Tên · Đề tài · Ngày · Số trang`
  - **Số trang dạng `current / total`** (tự động qua `data-marpit-pagination-total`)
  - **Logo UIT** góc phải mọi slide (chip trắng) qua directive `header:` — không chèn từng slide
- Tên trường ghi tiếng Anh: **University of Information Technology, VNU-HCM (UIT)**.

## Sơ đồ Mermaid — QUAN TRỌNG
- **KHÔNG** nhúng Mermaid inline (`<div class="mermaid">` + `<script>`). Lý do: VS Code preview chặn script (không hiện gì), xuất PDF bị **cắt chữ** và **thừa 1 trang trắng**.
- **LUÔN pre-render ra SVG** rồi nhúng ảnh:
  1. Viết nguồn trong `diagrams/*.mmd`
  2. Render: `npx -y @mermaid-js/mermaid-cli -i diagrams/x.mmd -o diagrams/x.svg -c diagrams/mermaid-config.json -b transparent`
  3. Nhúng: `![h:300px](diagrams/x.svg)` trong `<div class="diagram">`
- Config Mermaid phải đặt `flowchart.htmlLabels: false` (chữ thành SVG text thật, không bị clip khi nhúng `<img>`) + theme navy.

## Hình ảnh
- Ảnh thật để trong `assets/`, nhúng `![h:300px](assets/figure.png)` trong `<div class="diagram">`. Không để placeholder ảnh vỡ.

## Văn phong (rule người dùng)
- **Hạn chế em-dash (—).** Nhãn → dùng dấu hai chấm (`Label: mô tả`); trong câu → dùng dấu phẩy hoặc middot `·`.
- **Hạn chế icon/emoji.** Blockquote/box đã có viền + nền nên không cần icon trang trí.
- Slide bìa theo thứ tự: hộp tiêu đề → tên thành viên → GVHD → môn `·` loại báo cáo → địa điểm, ngày. Không thêm dòng "Dựa trên: …" (trích dẫn nguồn để ở slide nội dung/cuối).

## Cấu trúc folder
```
template/
├── slide.template.md / .html
├── assets/        (logo, hình)
└── diagrams/      (*.mmd nguồn, *.svg đã render, mermaid-config.json)
```
