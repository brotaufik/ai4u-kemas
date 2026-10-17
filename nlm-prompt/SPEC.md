# SPEC: NotebookLM Prompt Generator by Bro (AI4U)

Versi 0.2 · 17 Oktober 2026 · Diluluskan Bro Taufik, dibina dan diuji (T1 hingga T9 lulus)

---

## 1. Tujuan

Alat satu halaman yang membantu peserta AI4U menghasilkan prompt tersuai untuk **kesemua 9 fungsi Studio NotebookLM**, dalam Bahasa Melayu atau English, dengan konteks kerja KEMAS dan semakan warna data terbina.

Alat ini diilhamkan oleh *NotebookLM Prompt Generator* oleh Kee Man (nlmprompts.keeman.app, CC BY 4.0). Kita bina **code dan teks prompt sendiri**. Yang diambil hanyalah idea dan struktur umum: pilih pilihan, templat ayat, butang Shuffle dan Save.

## 2. Prinsip reka bentuk

| # | Prinsip | Maksud |
|---|---|---|
| P1 | Mula dengan masalah | Medan pertama ialah "Masalah / tujuan saya", selari dengan Slaid #28 Use Case |
| P2 | Human in the loop | Setiap prompt diakhiri arahan supaya output boleh disemak dengan sumber |
| P3 | Peraturan data | Pemilih 🟢🟡🔴 wajib. 🔴 menyekat butang Copy |
| P4 | BM-first | Antara muka BM. Prompt boleh dijana dalam BM atau English |
| P5 | Tiada AI di belakang | Semua dijana dalam browser daripada templat. Tiada data dihantar keluar |
| P6 | Satu fail | Satu fail HTML, tanpa library luar kecuali Google Fonts |
| P7 | Kredit | Footer menyatakan sumber ilham dan lesen CC BY 4.0 |

## 3. Pengguna

- **Utama:** peserta AI4U KEMAS (PPPAK, Pendidik Masyarakat, Penyelia, Pegawai daerah)
- **Kedua:** fasilitator semasa demo Modul 5

## 4. Struktur antara muka

1. **Header:** nama alat, butang tema gelap/cerah, pilihan bahasa output (BM / English)
2. **Pemilih fungsi Studio:** 9 jubin berwarna (sama warna dengan Slaid M5 Studio)
3. **Panel A · Konteks** (sama untuk semua fungsi)
4. **Panel B · Butiran fungsi** (berubah ikut fungsi dipilih)
5. **Panel C · Gaya** (hanya untuk fungsi visual: Infographic, Slide Deck, Video Overview)
6. **Output:** kotak prompt, butang Shuffle, Copy, Reset, Save
7. **Prompt tersimpan:** senarai, muat semula, padam, eksport JSON
8. **Footer:** kredit dan penafian

## 5. Panel A · Konteks (semua fungsi)

| Medan | Jenis | Pilihan / contoh | Wajib |
|---|---|---|---|
| Masalah / tujuan | Teks pendek | "Ibu bapa tak faham syarat pendaftaran TABIKA 2027" | Ya |
| Audiens | Chip + taip sendiri | Ibu bapa TABIKA, PPPAK, Pendidik Masyarakat, Penyelia daerah, Pengarah/pengurusan, Peserta kursus kemahiran, Komuniti umum, Murid prasekolah | Ya |
| Fokus kandungan | Teks pendek | "Tarikh, syarat dan dokumen yang perlu dibawa" | Tidak |
| Nada | Dropdown | Formal, Mesra, Mendidik, Ringkas dan padat, Bercerita, Memujuk, Teknikal | Ya |
| Bahasa output | Toggle | Bahasa Melayu (lalai), English | Ya |
| Warna data sumber | 3 butang | 🟢 Hijau, 🟡 Kuning, 🔴 Merah | Ya |

**Kelakuan warna data:**
- 🟢 Tiada amaran.
- 🟡 Banner kuning: "Guna akaun @kemas.gov.my sahaja. Buang nama individu sebelum muat naik sumber."
- 🔴 Banner merah dan butang Copy dinyahaktifkan: "Data Merah tidak boleh dimasukkan ke NotebookLM."

## 6. Panel B · Butiran ikut fungsi

Nota: nama pilihan dalam NotebookLM berubah dari semasa ke semasa. Lajur "Pilihan dalam NotebookLM" mesti disahkan dengan UI sebenar sebelum versi akhir.

| Fungsi | Medan tambahan dalam alat kita | Pilihan dalam NotebookLM (untuk disahkan) |
|---|---|---|
| 🎧 Audio Overview | Format (Ulasan mendalam / Ringkas / Kritikan / Debat), Panjang (Pendek / Biasa / Panjang), Perkara mesti disebut | Format, panjang, bahasa, arahan fokus |
| 🎬 Video Overview | Format (Penerangan / Ringkas), Gaya visual (Panel C), Bilangan mesej utama (3 hingga 5) | Format, gaya visual, arahan fokus |
| 📑 Reports | Jenis (Briefing doc / Study guide / FAQ / Garis masa / Tersuai), Panjang maksimum (1 muka / 2 muka), Struktur seksyen | Jenis laporan, arahan tersuai |
| ❓ Quiz | Bilangan soalan (5 / 10 / 15), Tahap (Mudah / Sederhana / Sukar), Topik khusus | Bilangan, tahap, topik |
| 📋 Data Table | Senarai lajur (taip, dipisah koma), Susunan baris | Arahan lajur |
| 🖼️ Slide Deck | Orientasi (Landskap / Potret), Bilangan slaid (5 / 8 / 10 / 12), Satu mesej setiap slaid (Ya/Tidak), Gaya visual (Panel C) | Jenis deck, panjang, arahan |
| 🧠 Mind Map | Tema utama, Kedalaman cabang (2 / 3 aras) | Prompt dalam Chat (Mind Map tiada kotak arahan sendiri) |
| 🃏 Flashcards | Bilangan kad (10 / 20 / 30), Tahap, Fokus (Istilah / Tarikh / Prosedur) | Bilangan, tahap, topik |
| 📊 Infographic | Susun atur (Satu lajur / 2 lajur / 3 lajur / Grid 2x2 / Grid 3x3 / Bento / Bebas), Orientasi, Gaya visual (Panel C) | Arahan, orientasi |

## 7. Panel C · Gaya visual (Infographic, Slide Deck, Video)

| Medan | Pilihan |
|---|---|
| Gaya | Profesional, Korporat, Minimalis, Akademik, Ilustrasi, Ikon rata (flat), Lakaran nota (sketch notes), Peta minda, Blueprint, Kertas potong (paper cut), Retro, Futuristik, Kartun mesra kanak-kanak, 3D, Clay |
| Palet warna | Biru korporat KEMAS, Pastel, Hangat, Sejuk, Monokrom, Cerah dan bertenaga, Neutral, Watercolour |
| Latar | Putih, Kelabu cair, Gelap, Gradien, Tekstur kertas, Papan kapur, Papan gabus |
| Fon | Sans-serif moden, Serif klasik, Bulat mesra, Tulisan tangan, Display tebal, Monospace |
| Motif tempatan (pilihan) | Corak batik, Motif Sarawak, Suasana kampung, Kelas TABIKA, Bandar moden Malaysia |

**Keputusan reka bentuk (v0.2):** "Motif tempatan" ditambah. Tema watak berhak cipta (Upin Ipin, BoBoiBoy, Ejen Ali, Marvel, Disney dan lain-lain) **dikekalkan sebagai pilihan** atas keputusan Bro Taufik, dengan amaran kuning: jangan guna untuk bahan rasmi, hebahan awam atau media sosial KEMAS.

## 8. Penjanaan prompt

### 8.1 Susunan slot

```
[PEMBUKA ikut fungsi] + [TUJUAN/MASALAH] + [AUDIENS] + [FOKUS]
+ [BUTIRAN FUNGSI] + [GAYA, jika visual] + [NADA] + [BAHASA OUTPUT]
+ [ARAHAN SEMAKAN SUMBER] + [PENUTUP]
```

### 8.2 Peraturan

1. **Medan kosong digugurkan** bersama kata penghubungnya. Tiada koma berganda atau ayat tergantung.
2. **Senarai digabung tanpa Oxford comma:** "a, b dan c" / "a, b and c".
3. **English: artikel a/an disesuaikan** ("an educational tone", "a formal tone"). Ini membetulkan bug yang diperhatikan pada laman asal.
4. **Arahan semakan sumber sentiasa ada** (P2), contoh: "Gunakan hanya maklumat daripada sumber dalam notebook ini dan nyatakan rujukan bagi setiap angka."
5. **Panjang sasaran:** 60 hingga 140 patah perkataan.

### 8.3 Shuffle

- Setiap slot teks tetap (pembuka, penghubung, arahan semakan, penutup) ada **kolam sekurang-kurangnya 4 variasi** dalam BM dan 4 dalam English, semuanya ditulis sendiri.
- Shuffle hanya menukar variasi frasa. **Pilihan pengguna tidak berubah.**
- Shuffle tidak mengulang kombinasi yang sama dua kali berturut-turut.

### 8.4 Contoh output sasaran (BM, Infographic)

> Hasilkan satu infografik satu muka untuk menerangkan syarat pendaftaran TABIKA 2027 kepada ibu bapa. Fokus pada tarikh penting, syarat kelayakan dan dokumen yang perlu dibawa. Susun dalam dua lajur dengan gaya ikon rata, palet biru korporat KEMAS, fon bulat mesra dan latar putih. Gunakan nada mesra dan bahasa yang mudah difahami. Gunakan hanya maklumat daripada sumber dalam notebook ini dan pastikan setiap tarikh sepadan dengan dokumen asal.

## 9. Simpan dan muat semula

- Prompt tersimpan dalam `localStorage` (kunci `ai4u-nlm-prompts`), dengan nama, fungsi, tarikh dan semua pilihan.
- Semua baca/tulis dibalut try/catch. Jika storage tiada, butang Save memaparkan "Tidak dapat simpan dalam browser ini".
- Eksport dan import JSON untuk pindah antara peranti.

## 10. Keperluan bukan fungsi

- Satu fail HTML, saiz di bawah 150 KB
- Tema gelap dan cerah, teks gelap dalam mod cerah
- Paparan telefon: lebar 360px tanpa skrol mendatar
- Semua kawalan boleh dicapai dengan papan kekunci
- Tiada panggilan rangkaian selain Google Fonts

## 11. Ujian penerimaan

| # | Ujian | Jangkaan |
|---|---|---|
| T1 | Pilih setiap 9 fungsi, isi medan wajib | Prompt dijana, 60 hingga 140 patah perkataan |
| T2 | Kosongkan medan tidak wajib | Tiada koma berganda, tiada slot kosong |
| T3 | English + nada "Educational" | Mengandungi "an educational tone" |
| T4 | Senarai 3 item | "a, b dan c", tiada Oxford comma |
| T5 | Shuffle 10 kali | Pilihan tidak berubah; teks berubah; tiada ulangan berturut-turut |
| T6 | Pilih 🔴 Merah | Butang Copy dinyahaktifkan |
| T7 | Audiens dan fokus diisi | Kedua-duanya muncul dalam prompt (laman asal gagal di sini) |
| T8 | Save, muat semula halaman, buka semula | Prompt dan pilihan kembali sama |
| T9 | **Ujian ke atas ujian:** suntik prompt rosak (koma berganda) | T2 mesti GAGAL. Jika lulus, ujian T2 tidak sah |

## 12. Kredit (footer)

> Diilhamkan oleh *NotebookLM Prompt Generator* oleh Kee Man (nlmprompts.keeman.app), CC BY 4.0. Versi ini ditulis semula sepenuhnya untuk kursus AI4U KEMAS, dengan 9 fungsi Studio, konteks KEMAS dan semakan data. Alat ini tidak berkaitan dengan Google.

## 13. Keputusan Bro Taufik (17 Okt 2026)

- Nama: **NotebookLM Prompt Generator by Bro**
- Lokasi: fail sendiri di `ai4u-kemas/nlm-prompt/` + pautan dari Slaid M5 Studio dan Slaid Enjin Prompt
- Bahasa lalai: **Bahasa Melayu**
- Tema watak: **dikekalkan dengan amaran**

### Senarai asal soalan

1. **Nama alat:** contoh "Studio Prompt AI4U" atau cadangan lain.
2. **Lokasi:** fail berdiri sendiri, ATAU dipautkan dari Slaid M5 Studio dan Enjin Prompt dalam portal AI4U, ATAU kedua-duanya.
3. **Bahasa lalai output:** BM (cadangan) atau English.
4. **Tema watak:** setuju digugurkan dan diganti Motif tempatan?
5. **Hosting:** GitHub Pages bersama repo `ai4u-kemas` (cadangan).

## 14. Perkara belum disahkan

- Nama pilihan sebenar dalam setiap panel Customize NotebookLM (lajur kanan Seksyen 6). Perlu disemak dengan akaun NotebookLM sebelum versi akhir.
- Sama ada Video Overview dan Infographic menerima arahan orientasi untuk semua akaun.
