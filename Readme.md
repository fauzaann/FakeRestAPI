# API Test Plan: Fake REST API

Dokumen test plan untuk pengujian **Fake REST API**, sebuah API simulator untuk sistem manajemen buku.

- **Swagger:** https://fakerestapi.azurewebsites.net/index.html
- **Base URL:** https://fakerestapi.azurewebsites.net
- **Penyusun:** Rizki Fauzan, QA Engineer
- **Tanggal:** 23 November 2026
- **Versi:** V1 (Draft)

## Tentang Proyek

Test plan ini menjelaskan rencana pengujian untuk memastikan kualitas, fungsionalitas, dan keandalan Fake REST API. Pengujian difokuskan pada operasi CRUD (POST, GET, PUT, DELETE), validasi data, penanganan error, dan performa dasar.

## Resource yang Diuji

| Resource | Endpoint | Method |
|---|---|---|
| Activities | `/api/v1/Activities`, `/api/v1/Activities/{id}` | GET, POST, PUT, DELETE |
| Authors | `/api/v1/Authors`, `/api/v1/Authors/{id}`, `/api/v1/Authors/authors/books/{idBook}` | GET, POST, PUT, DELETE |
| Books | `/api/v1/Books`, `/api/v1/Books/{id}` | GET, POST, PUT, DELETE |
| CoverPhotos | `/api/v1/CoverPhotos`, `/api/v1/CoverPhotos/{id}`, `/api/v1/CoverPhotos/books/covers/{idBook}` | GET, POST, PUT, DELETE |
| Users | `/api/v1/Users`, `/api/v1/Users/{id}` | GET, POST, PUT, DELETE |

## Isi Dokumen

1. Objective
2. API Description
3. Scope (In Scope dan Out of Scope)
4. Test Environment
5. Test Data
6. Test Strategy
7. Contoh Skenario Pengujian
8. Defect Reporting Procedure
9. Test Schedule
10. Test Coverage
11. Risk and Mitigation
12. Testing Tools
13. Roles and Responsibilities
14. Test Deliverables
15. Approvers List

## Jenis Pengujian

- Functional Testing
- Data Validation Testing
- Error Handling Testing
- Integration Testing
- Regression Testing
- Performance dan Load Testing
- Security Testing (dasar)
- Documentation Review

## Tools

| Tool | Fungsi | Status |
|---|---|---|
| Swagger UI | Eksplorasi endpoint dan smoke test manual | Utama |
| Postman | Pengujian manual penuh, termasuk input tidak valid | Utama |
| Newman | Menjalankan koleksi Postman otomatis | Opsional |
| JMeter | Load dan performance testing | Opsional |
| OWASP ZAP | Security testing dasar | Opsional |
| JIRA / spreadsheet | Pencatatan defect | Opsional |

## Jadwal

| Task | Mulai | Selesai |
|---|---|---|
| Membuat Test Plan | 23 Nov 2026 | 23 Nov 2026 |
| Membuat Test Case | 24 Nov 2026 | 26 Nov 2026 |
| Eksekusi Test Case | 27 Nov 2026 | 3 Des 2026 |
| Regression dan Retest | 4 Des 2026 | 7 Des 2026 |
| Summary Report | 8 Des 2026 | 8 Des 2026 |

## Catatan Penting

- Fake REST API adalah **simulator**: data dari POST, PUT, dan DELETE kemungkinan besar tidak tersimpan permanen, sehingga verifikasi dilakukan lewat respons API.
- API tidak menyediakan autentikasi, jadi pengujian autentikasi dan otorisasi berada di luar scope.
- Swagger UI hanya memvalidasi input di sisi klien, sehingga skenario input tidak valid diuji memakai Postman.

## Struktur Repository

```
api-test-plan-fakerestapi/
├── README.md
├── docs/
│   └── API_Test_Plan_FakeRESTApi.pdf
├── postman/                 (opsional)
│   └── FakeRESTApi.postman_collection.json
└── screenshots/             (opsional)
```

## Penulis

Rizki Fauzan, QA Engineer