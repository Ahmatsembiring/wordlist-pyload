# 🎭 Cross-Site Scripting (XSS) Arsenal

Koleksi payload XSS terkurasi untuk keperluan Pentesting, Bug Bounty, dan CTF.

## 📂 Struktur Payload

| File | Deskripsi | Kapan Digunakan |
|------|-----------|-----------------|
| `xss-basic.txt` | Payload standar | Deteksi awal (Proof of Concept) |
| `xss-context-attribute.txt` | Break Attribute | Saat input berada di dalam `value="..."` |
| `xss-context-script.txt` | Break Script | Saat input berada di dalam `<script>var x = "..."</script>` |
| `xss-bypass-waf.txt` | WAF Evasion | Menghindari filter Cloudflare/AWS/ModSecurity |
| `xss-polyglot.txt` | Polyglot | Payload "sakti" yang bekerja di banyak konteks sekaligus |

## 🛠️ Integrasi Tools

### Burp Suite Intruder
1. Buka tab **Intruder** > **Payloads**.
2. Pilih **Payload type**: `Simple list`.
3. Klik **Load** dan arahkan ke file `.txt` di folder `payloads/`.

### VS Code Snippets
Saya telah menyertakan file `snippets/xss-payloads.code-snippets`. 
Import file ini ke VS Code Anda untuk memanggil payload XSS dengan cepat saat menulis laporan atau kode.

## ⚠️ Disclaimer
Gunakan payload ini hanya pada sistem yang Anda miliki atau memiliki izin tertulis.
