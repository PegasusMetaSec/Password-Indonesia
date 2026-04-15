
<img width="1024" height="1024" alt="WhatsApp Image 2026-04-14 at 23 23 35" src="https://github.com/user-attachments/assets/363f5651-9408-45c5-a60e-789a64c71705" />





# 📁 Daftar Kata Sandi Umum Indonesia (wordlist)

Daftar kata sandi statis ini disusun untuk keperluan **pengujian keamanan (penetration testing)**, **audit keamanan internal**, dan **edukasi kesadaran keamanan siber** di lingkungan berbahasa Indonesia.

> ⚠️ **Peringatan**: File ini hanya boleh digunakan untuk tujuan sah dan etis. Jangan gunakan untuk aktivitas ilegal atau tanpa izin pemilik sistem.

---

## 📋 Deskripsi

`password-indonesia-wordlist.txt` berisi kumpulan kata sandi yang umum digunakan oleh pengguna di Indonesia berdasarkan:

- Data kebocoran publik yang terdokumentasi
- Pola umum: nama depan, tanggal, kota, olahraga, makanan, dan kombinasi sederhana
- Kata sandi default perangkat/perusahaan yang beredar di Indonesia

---

## 📊 Statistik Ringkas

| Item             | Detail                         |
| ---------------- | ------------------------------ |
| Format           | Teks biasa (UTF-8)             |
| Jumlah entri     | 10.234 (contoh; sesuaikan)     |
| Baris baru       | `\n` (LF)                      |
| Sumber utama     | Have I Been Pwned (filter ID), kebocoran lokal, pola umum |
| Target penggunaan| WPScan, Hydra, Medusa, Ncrack, Burp Suite, Aircrack-ng |

---

## 🔧 Contoh Penggunaan

### 1. Menggunakan dengan Hydra (FTP/SSH/HTTP)

```bash
hydra -l admin -P password-indonesia-wordlist.txt 192.168.1.10 http-post-form "/login:user=^USER^&pass=^PASS^:F=Invalid"
