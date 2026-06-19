# Slide Template (Marp)

Template trình chiếu Marp — theme navy `#1F3A68`, font Be Vietnam Pro, phỏng theo Beamer VSE.

## Cấu trúc
```
template/
├── slide.template.md      # FILE CHÍNH — sửa nội dung ở đây
├── slide.template.html    # bản render để mở/chiếu
└── diagrams/
    ├── methodology.mmd        # nguồn sơ đồ Mermaid (sửa ở đây)
    ├── mermaid-config.json    # theme navy cho sơ đồ
    └── methodology.svg        # sơ đồ đã render (nhúng vào slide)
```

## Xem & xuất file
```bash
# Xem trực tiếp: mở slide.template.html, hoặc dùng extension "Marp for VS Code"
npx -y @marp-team/marp-cli slide.template.md --html --allow-local-files -o slide.template.html
npx -y @marp-team/marp-cli slide.template.md --pdf  --allow-local-files   # nộp PDF
npx -y @marp-team/marp-cli slide.template.md --pptx --allow-local-files   # mở bằng PowerPoint
```

## Quy ước trong file .md
- Tiêu đề slide nội dung → `## ...` (tự ra thanh header navy tràn viền)
- Slide bìa / cảm ơn → thêm `<!-- _class: lead -->`
- Tên · đề tài · ngày → sửa ở dòng `footer:` trong frontmatter
- Công thức: KaTeX `$...$` / `$$...$$`  |  Bảng: Markdown thường  |  Hình: `![w:560px](path)`
- Số trang hiện dạng `current / total` tự động

## Sơ đồ Mermaid (QUAN TRỌNG)
Marp **không** render Mermaid trực tiếp (VS Code preview chặn script, PDF cắt chữ).
→ Cách dùng: viết Mermaid trong `diagrams/*.mmd`, render ra SVG, rồi nhúng `![](diagrams/x.svg)`.

Sửa sơ đồ → chạy lại:
```bash
npx -y @mermaid-js/mermaid-cli -i diagrams/methodology.mmd -o diagrams/methodology.svg -c diagrams/mermaid-config.json -b transparent
```
Thêm sơ đồ mới: tạo `diagrams/ten.mmd`, render thành `ten.svg`, rồi nhúng vào slide bằng `![h:300px](diagrams/ten.svg)`.

> Lưu ý: font Be Vietnam Pro tải từ Google Fonts → cần mạng lúc render/mở HTML. Cần offline thì tải `.ttf` về và nhúng bằng `@font-face`.
