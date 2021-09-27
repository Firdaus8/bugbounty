## Ngorder - Bug Bounty

Tidak ada gading yang tak retak, begitu pula teknologi tidak ada yang sempurna. Kami sangat menghargai kolaborasi dengan para pentester guna meningkatkan keamanan kami. Jika Anda dengan yakin telah menemukan celah keamanan dengan senang hati kami akan berdiskusi dan meresponsnya.

## Cakupan

Semua konten yang terdapat pada domain berikut :

```markdown
- https://app.ngorder.id 
- https://api.ngorder.id
- Aplikasi Mobile Ngorder (android dan IoS)
```

## Rule 
In Scope
```markdown
1. Remote Command Execution (RCE)
Cukup tampilkan output dari command id dan IP internal sebagai PoC

2. Leaked Private Keys
Kecuali key sudah tidak digunakan lagi oleh Ngorder

3. Leaked PII
Informasi pengguna Ngorder yang bersifat rahasia.

4. SQL/NoSQL Injection
Cukup tampilkan output SELECT user() sebagai PoC

5. Local/Remote File Inclusion (LFI/RFI)
Authentication Bypass
Multi-factor Authentication Bypass
Bypass OTP untuk untrusted devices

6. Cross-Site Scripting (XSS)
Kecuali XSS yang hanya berdampak pada diri sendiri (Self-XSS)

7. Broken Access Control
Cukup tampilkan 1 atau 2 data sebagai PoC

8. Server-Side Request Forgery (SSRF)
Hanya SSRF ke jaringan internal

9. Cross-Site Request Forgery (CSRF)
Kecuali CSRF pada logout atau memang disengaja untuk user anonymous

10. Business Logic Flaws
Celah yang dapat merugikan Ngorder atau penggunanya
```
Out of Scope
```markdown
1. Temuan yang melanggar aturan dan/atau di luar cakupan
Temuan dengan risiko rendah
Self XSS, Login/Logout CSRF, CORS tanpa melampirkan bukti yang berakibat kepada pengguna lain

2. Pemakaian automated scanner
Hasil output dari tools seperti Nmap, SSL Scan, dan lainnya tidak diterima

3. Social engineering
Memanfaatkan phising/fraud diluar Bukalapak (email, sms, facebook messenger, whatsapp, dan lainnya)

4. Open redirects
Pada kasus tertentu, kami akan memproses jika risikonya tinggi. Misalnya mampu melakukan pencurian token

5. Missing security headers
Contoh: HSTS, cookie flags, X-Frame-Options, X-XSS-Protection, dll

6. DDoS
Kecuali DoS pada level aplikasi dan eksploitnya mudah

7. Clickjacking
Kesalahan pada konfigurasi SPF, DKIM, dan DMARC.
SPF, DKIM, dan DMARC yang hanya menggunakan teknik social engineering untuk eksploitasinya
```

## Tata Cara Pelaporan

1. Tulis laporan 
Anda tidak perlu menuliskan laporan pada file PDF, cukup tuliskan di badan email saja. Bagian-bagian yang wajib ada pada laporan adalah:
```markdown
- Jenis celah keamanan yang ditemukan.
- Langkah-langkah singkat yang diperlukan untuk mereplikasi celah keamanan.
- Bukti atau Proof of Concept (PoC) yang dapat berbentuk gambar atau video. Jadikan sebagai lampiran email.
- Dampak yang dapat ditimbulkan akibat adanya celah keamanan ini.
- Saran / Remediasi dalam perbaikan celah keamanan.
```

2. Kirim ke security@team.ngorder.id
3. Tunggu balasan

