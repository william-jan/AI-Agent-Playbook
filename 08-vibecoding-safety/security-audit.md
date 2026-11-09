# Security Audit Playbook

**Scope:** seluruh route publik/privat, middleware, session, API, storage, dan dependency.

1. Petakan entry point dan trust boundary.
2. Identifikasi user roles dan resource ownership.
3. Uji unauthenticated request, wrong role, dan cross-account ID.
4. Periksa runtime input validation, output escaping, HTML injection dan query construction.
5. Tinjau session/JWT, cookie flags, CSRF, CORS, secret management, file upload.
6. Periksa rate limiting, audit log, dan kebocoran pesan error.
7. Verifikasi temuan dengan test yang tidak merusak data; dokumentasikan file, impact, reproduce, dan fix.

**Prompt:** `Audit keamanan repository ini secara read-only berdasarkan OWASP. Urutkan temuan menurut impact dan likelihood, tunjukkan file/line, jalur eksploitasi yang masuk akal, mitigasi, serta test verifikasi. Jangan mengklaim aman jika tidak diuji.`

Sumber: [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/), [OWASP Top 10](https://owasp.org/www-project-top-ten/).
