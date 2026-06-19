---
marp: true
title: "Title of your presentation"
author: "Your Name"
paginate: true
html: true
math: katex
backgroundColor: "#ffffff"
color: "#1d2b36"
# ============================================================
#  MARP TEMPLATE — phỏng theo Beamer theme "VSE" (primary navy #1F3A68)
#  Quy ước dùng:
#   - Mỗi slide ngăn nhau bằng `---`
#   - Tiêu đề frame nội dung  ->  dùng `## ...` (sẽ ra THANH NAVY tràn viền)
#   - Slide bìa / cảm ơn      ->  thêm `<!-- _class: lead -->`
#   - Footer (tên · đề tài · ngày) sửa ở dòng `footer:` cuối frontmatter
#   - Công thức: KaTeX  $...$ / $$...$$    |  Hình: ![w:600px](path)
# ============================================================
style: |
  @import url('https://fonts.googleapis.com/css2?family=Be+Vietnam+Pro:ital,wght@0,400;0,600;0,700;1,400&display=swap');
  section {
    font-family: "Be Vietnam Pro", "Segoe UI", system-ui, sans-serif;
    font-size: 24px;
    padding: 100px 64px 64px 64px;      /* chừa 100px trên cho thanh header absolute */
    background: #ffffff;
    color: #1d2b36;
    display: flex;
    flex-direction: column;
    justify-content: flex-start !important;   /* body căn sát mép trên (dưới header) */
    align-content: flex-start;
  }
  /* --- THANH HEADER CAM tràn viền dính đỉnh (dùng cho ## slide nội dung) --- */
  h2 {
    position: absolute;
    top: 0; left: 0; right: 0;
    margin: 0;
    background: #1F3A68;
    color: #ffffff !important;
    font-size: 30px;
    font-weight: 600;
    padding: 16px 64px;
  }
  h3 { color:#1F3A68; font-size:24px; margin-bottom:4px; }
  strong { color:#1F3A68; }
  em { color:#1d4ed8; font-style:normal; }
  a { color:#1F3A68; }
  code { background:#e7edf6; color:#1F3A68; padding:1px 6px; border-radius:4px; }
  /* --- bullet markers màu navy như Beamer --- */
  ul { list-style:none; padding-left:6px; }
  ul li { position:relative; padding-left:24px; margin:10px 0; }
  ul li::before { content:"●"; color:#1F3A68; font-size:14px; position:absolute; left:0; top:4px; }
  ol li { margin:10px 0; }
  /* --- bảng --- */
  table { font-size:21px; border-collapse:collapse; margin:6px 0; }
  th { background:#1F3A68; color:#ffffff; }
  td { background:#ffffff; }
  td,th { border:1px solid #c3d2ea; padding:5px 12px; }
  blockquote { border-left:4px solid #1F3A68; background:#e7edf6; color:#20324f; padding:8px 18px; }
  /* --- footer thanh chia 4 ô gradient (Name | Title | Date | page) --- */
  footer { left:0; bottom:0; width:100%; box-sizing:border-box;
           display:flex; padding:0; height:26px; font-size:13px; color:#ffffff;
           background:linear-gradient(90deg,#0e1d38 0%,#16294d 30%,#1f3a68 62%,#2a4d86 100%); }
  footer span { flex:1; display:flex; align-items:center; justify-content:center;
                border-right:1px solid rgba(255,255,255,.3); }
  footer span:nth-child(4) { flex:0 0 64px; }      /* ô số trang hẹp hơn */
  footer span:last-child { border-right:none; }
  section::after { position:absolute; right:18px; bottom:5px; z-index:10;
                   color:#ffffff; font-weight:600; font-size:13px;
                   content: attr(data-marpit-pagination) " / " attr(data-marpit-pagination-total); }  /* dạng 1 / 11 */
  /* --- logo UIT góc phải, hiện trên MỌI slide (qua directive header:) --- */
  header { position:absolute; top:9px; right:16px; left:auto; margin:0; padding:0;
           background:none; box-shadow:none; z-index:40; }
  header img { height:46px; display:block; background:#ffffff; border-radius:8px;
               padding:4px 7px; box-shadow:0 1px 5px rgba(0,0,0,.22); }
  /* --- slide bìa / cảm ơn --- */
  section.lead { text-align:center; justify-content:flex-start; }
  /* hộp tiêu đề rộng cả slide, chứa cả title + subtitle */
  .titlebox { width:100%; box-sizing:border-box; background:#1F3A68;
    border-radius:10px; padding:24px 40px; margin:48px 0 30px 0;
    box-shadow:0 5px 12px rgba(0,0,0,.18); text-align:center; }
  .titlebox h1 { background:none; border:none; box-shadow:none; display:block;
    color:#ffffff !important; font-size:38px; margin:0; padding:0; }
  .titlebox h3 { color:#ffffff !important; font-weight:400; margin:8px 0 0 0; }
  section.lead h3 { color:#1d2b36; font-weight:400; margin-top:0; }
  /* slide cảm ơn: tiêu đề lớn màu navy, KHÔNG hộp */
  .thanks h1 { background:none; border:none; box-shadow:none;
    color:#1F3A68 !important; font-size:46px; font-weight:700;
    margin:60px 0 28px 0; padding:0; }
  .small { font-size:18px; color:#777; }
  .caption { font-size:16px; color:#888; font-style:italic; }
  .cols { display:flex; gap:30px; }
  .col { flex:1; }
  .box { background:#e7edf6; border:1px solid #c3d2ea; border-radius:10px; padding:12px 20px; }
  /* --- sơ đồ (ảnh SVG pre-render từ Mermaid): căn giữa, giới hạn chiều cao --- */
  .diagram { text-align:center; margin-top:14px; }
  .diagram img { max-height:330px; width:auto; }
footer: '<span>Your Name</span><span>Title</span><span>January 14, 2026</span><span></span>'
header: '<img src="assets/UIT_logo.svg" alt="UIT">'
---

<!-- _class: lead -->

<div class="titlebox">

# Title of your presentation
### Subtitle of your presentation

</div>

**Your Name**
Department of International Economic Relations

<br>

<span class="small">University of Information Technology, VNU-HCM (UIT)</span>

---

## Contents

1. **Motivation**
2. **Research gap & Aim of the paper**
3. **Theoretical background**
4. **Methodology**
5. **Data**
6. **Results & Discussion**
7. **Further research & Limitations**

---

## Motivation

- XYZ — your text
- (...your text)
- XYZ — your text
- tbc ...

> Dùng `<!-- _class: lead -->` ở slide để chỉ tiêu đề lớn không có thanh navy (cho slide chuyển mục).

---

## Research gap & Aim of the paper

To insert a table:

**Table:** Summary statistics of XX

| Country | Mean X | Min X | Max X |
|---|---|---|---|
| AT | 0.29 | 0.28 | 0.30 |
| BE | 0.27 | 0.25 | 0.29 |
| BG | 0.23 | 0.20 | 0.28 |

<span class="caption">Source: own elaboration based on ...</span>

---

## Theoretical background

To insert an equation (KaTeX):

$$
Y = \beta_0 + \beta_1 X + \epsilon \qquad (1)
$$

- Inline math: giá trị kỳ vọng $\mathbb{E}[Y\mid X]$ ...
- Giải thích biến: $\beta_0$ — hệ số chặn, $\beta_1$ — hệ số góc, $\epsilon$ — nhiễu.

---

## Methodology

Your text

<div class="cols">
<div class="col">

**Bước 1 — ...**
- your text

</div>
<div class="col">

**Bước 2 — ...**
- your text

</div>
</div>

---

## Methodology — sơ đồ quy trình (Mermaid → SVG)

<div class="diagram">

![h:300px](diagrams/methodology.svg)

</div>

<span class="caption">Sửa sơ đồ trong <code>diagrams/methodology.mmd</code> rồi render lại:<br>
<code>npx -y @mermaid-js/mermaid-cli -i diagrams/methodology.mmd -o diagrams/methodology.svg -c diagrams/mermaid-config.json -b transparent</code></span>

---

## Data

Your text

<div class="box">

**Nguồn dữ liệu:** ... · **Khoảng thời gian:** ... · **Số quan sát:** ...

</div>

---

## Results & Discussion

<div class="diagram">

![h:300px](assets/figure.png)

</div>

<span class="caption">Figure: XYZ — Source: Authors' calculations &nbsp;·&nbsp; thay ảnh ở <code>assets/figure.png</code></span>

---

## Further research & Limitations

- **Limitation 1** — your text
- **Limitation 2** — your text
- **Future work** — your text

---

## References

1. Author, A. (Year). *Title of the work.* Journal/Publisher.
2. Author, B. (Year). *Title of the work.* Journal/Publisher.

<span class="small">Mẹo: nếu nhiều tài liệu, tách thành "References I", "References II" trên nhiều slide.</span>

---

<!-- _class: lead -->

<div class="thanks">

# Thank you for your attention

</div>

**Your Name**
your.email@email.com

<span class="small">University of Information Technology, VNU-HCM (UIT)</span>
