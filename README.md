# CS519 — Scientific Research Methodology

<p align="center">
  <a href="https://www.uit.edu.vn/"><img src="assets/UIT_logo.svg" alt="UIT Logo" width="180"></a>
</p>
<h1 align="center"><b>CS519 — Phương pháp Nghiên cứu Khoa học</b></h1>
<p align="center"><i>Scientific Research Methodology</i></p>

## Giới thiệu

- **Tên môn học:** PHƯƠNG PHÁP LUẬN NGHIÊN CỨU KHOA HỌC — Scientific Research Methodology
- **Mã môn:** CS519

### Giảng viên

- PGS.TS Lê Đình Duy — duyld@uit.edu.vn

### Học viên

| STT | Họ tên        | MSHV      | Github                              |
| :-: | ------------- | --------- | ----------------------------------- |
|  1  | Trần Tú Quang | 250201084 | [ttqteo](https://github.com/ttqteo) |

## Đề tài

**Patch-Aware Taint-Guided PoV Synthesis for Recurring Web Vulnerability Detection**
Recurring Vulnerability Detection cho hệ sinh thái npm/Node.js — program analysis + PoV synthesis để validate.

- **Hướng tiếp cận:** taint signature representation + cross-project matching
- **Case study đầu tiên:** CVE-2019-10744 (lodash prototype pollution)
- **Nền tảng lý thuyết:** AntMan (ISSTA 2025), NodeMedic-FINE (NDSS 2025)

### Câu hỏi nghiên cứu

- **RQ chính:** Taint-signature matching có phát hiện recurring vulnerabilities trên npm chính xác hơn code-clone-based approaches không?
- **RQ phụ:** PoV synthesis có cải thiện precision của RVD không?
