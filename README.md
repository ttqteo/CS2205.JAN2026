# CS2205.CH203 — Scientific Research Methodology

<p align="center">
  <a href="https://www.uit.edu.vn/"><img src="assets/UIT_logo.svg" alt="UIT Logo" width="180"></a>
</p>
<h1 align="center"><b>CS2205.JAN2026 — Phương pháp Nghiên cứu Khoa học</b></h1>
<p align="center"><i>Scientific Research Methodology</i></p>

## Giới thiệu

- **Tên môn học:** PHƯƠNG PHÁP LUẬN NGHIÊN CỨU KHOA HỌC — Scientific Research Methodology
- **Mã môn:** CS2205.JAN2026

### Giảng viên

- PGS.TS Lê Đình Duy — duyld@uit.edu.vn

### Học viên

| STT | Họ tên        | MSHV      | Github                              |
| :-: | ------------- | --------- | ----------------------------------- |
|  1  | Trần Tú Quang | 250201084 | [ttqteo](https://github.com/ttqteo) |

## Đề tài

**Tổng hợp bằng chứng khai thác dựa trên phân tích vết nhiễm vi phân cho lỗ hổng web npm**
_Differential Taint-Guided Proof-of-Vulnerability Synthesis for NPM Web Vulnerabilities_

Sinh PoV cho hệ sinh thái npm/Node.js dựa trên phân tích vết nhiễm vi phân từ bản vá — so sánh đường truyền dữ liệu trước/sau khi vá, trích ràng buộc bị thiếu và dùng ràng buộc đó dẫn đường sinh payload khai thác.

- **Hướng tiếp cận:** differential taint analysis từ bản vá → trích ràng buộc → guided PoV synthesis
- **Phạm vi lỗ hổng:** Command Injection (CWE-77/78), Path Traversal (CWE-22), Prototype Pollution (CWE-1321)
- **Tập đánh giá:** SecBench.js
- **Baseline so sánh:** NodeMedic-FINE (NDSS 2025), PoCGen (2025)

### Câu hỏi nghiên cứu

- **RQ chính:** Ràng buộc trích từ bản vá có giúp sinh PoV cho các lỗ hổng mà công cụ không dùng bản vá khó xử lý không?
- **RQ phụ:** Nguồn ràng buộc từ bản vá có bổ sung cho các nguồn ràng buộc hiện có (NodeMedic-FINE, PoCGen) không?

## Tài liệu

| Loại         | Tệp                                                                          |
| ------------ | ---------------------------------------------------------------------------- |
| Báo cáo (Doc) | [Final Report — Doc](Quang%20Tr%E1%BA%A7n%20T%C3%BA%20-%20CS2205.JAN2026.DeCuong.FinalReport.Template.Doc.pdf) |
| Slide        | [Final Report — Slide](Quang%20Tr%E1%BA%A7n%20T%C3%BA%20-%20CS2205.JAN2026.DeCuong.FinalReport.Template.Slide.pdf) |
| Poster       | [Final Report — Poster](Quang%20Tr%E1%BA%A7n%20T%C3%BA%20-%20CS2205.JAN2026.DeCuong.FinalReport.Template.Poster.png) |
