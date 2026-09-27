# Konsep Game — *Merdeka atau Mati* (Operasi Garuda)

Dokumen ini menjelaskan konsep, cerita, desain permainan, dan teknologi di balik kampanye **Merdeka atau Mati**, kampanye sinematik dalam game **Operasi Garuda**.

---

## 1. Ringkasan

| | |
|---|---|
| **Genre** | Tembak orang ketiga / orang pertama, bercerita (*cinematic campaign*) |
| **Latar** | Perang Kemerdekaan Indonesia, 1945–1949 |
| **Platform** | Browser desktop (WebGL), tanpa instalasi |
| **Bahasa** | Indonesia (dialog musuh sesekali dalam bahasa Inggris & Belanda) |
| **Target pemain** | Remaja–dewasa yang suka game aksi dan ingin mengenal sejarah dengan cara menarik |
| **Durasi kampanye** | ±60–90 menit (3 bab) |

**Satu kalimat:** *Mainkan film perjuangan kemerdekaan — dari robeknya bendera di Hotel Yamato sampai gerilya Jenderal Soedirman — langsung di browser.*

---

## 2. Pilar desain

1. **Film yang bisa dimainkan.** Setiap bab dibuka, diselingi, dan ditutup dengan adegan film yang dibuat di dalam mesin game: pemain melihat dunia yang sama dengan yang nanti ia jelajahi.
2. **Rakyat adalah bagian dari cerita.** Perjuangan 1945 bukan hanya soal tentara. Warga sipil hadir di peta: berjalan, mengobrol, panik saat ditembaki, dan harus dilindungi.
3. **Autentik, tetapi terbuka untuk semua.** Seragam, senjata, dan tempat mengikuti zamannya. Sejarah diceritakan ringkas, dengan bahasa sederhana, tanpa menggurui.
4. **Ringan dan langsung main.** Semua bangunan, senjata, dan suara dibuat oleh kode, sehingga unduhan kecil dan cukup satu klik untuk bermain.

---

## 3. Cerita

Tokoh utama (pemain) dan rekan-rekannya adalah tokoh fiktif. Peristiwa, tempat, dan tokoh sejarah disederhanakan; beberapa urutan dan lokasi digabung agar bisa dimainkan.

### Bab 1 — Arek-Arek Suroboyo (Surabaya, 19 September – 10 November 1945)

| # | Jenis | Isi |
|---|---|---|
| 1 | Film | **Prolog (gaya arsip hitam-putih).** Proklamasi 17 Agustus 1945; kabar menjalar ke Surabaya; Sekutu datang membonceng NICA. |
| 2 | Film | **Insiden Hotel Yamato.** Bendera Belanda dikibarkan di puncak hotel. Massa memadati halaman, Residen Sudirman masuk berunding, perundingan gagal, pemuda naik ke menara dan merobek warna birunya. |
| 3 | Film | **Ultimatum.** Setelah Brigadir Mallaby tewas, pesawat Inggris menyebar selebaran. Warga mendengarkan siaran Bung Tomo di pos ronda. Pukul 06.00, 10 November, kota digempur. |
| 4 | Misi | **Bertahan** di alun-alun Hotel Yamato dari serbuan dari utara. |
| 5 | Misi | **Evakuasi** warga Kampung Peneleh ke Pos Palang Merah (warga mengikuti pemain). |
| 6 | Film | **Serbuan bambu runcing** ke arah Gedung Internatio. |
| 7 | Misi | **Rebut** Gedung Internatio. |
| 8 | Misi | **Hancurkan** truk amunisi di Jembatan Merah. |
| 9 | Misi | **Tahan** Jembatan Merah dari serangan balik seberang Kalimas. |
| 10 | Film | **Penutup.** Merah Putih dikibarkan di Jembatan Merah; 10 November menjadi Hari Pahlawan. |

### Bab 2 — Palagan Ambarawa (12–15 Desember 1945)

Film pembuka: Sekutu bertahan di Benteng Willem I; Kolonel Soedirman memerintahkan serangan serentak **"Supit Urang"** (capit udang); pasukan TKR memberi hormat; mengenang Letkol Isdiman yang gugur. Misi: bergerak senyap ke desa → sergap patroli di sawah → rebut stasiun → *(film: pengepungan dari dua sisi)* → lumpuhkan meriam di bukit → tahan serangan balik di kota → kepung dan rebut benteng. Penutup: Sekutu mundur ke Semarang — Hari Juang Kartika.

### Bab 3 — Jalan Gerilya (19 Desember 1948 – 27 Desember 1949)

Film pembuka (arsip): Agresi Militer Belanda II, pasukan payung di Maguwo, Yogyakarta jatuh. Panglima Besar Soedirman, sakit parah, memimpin gerilya. Misi: kawal rombongan Panglima menembus hutan (misi gagal bila beliau gugur) → sergap patroli NICA → putuskan jembatan → hancurkan pos radio → bertahan sampai rombongan lolos. Penutup: Serangan Umum 1 Maret 1949 dan pengakuan kedaulatan 27 Desember 1949.

---

## 4. Tokoh, faksi, dan kostum

| Faksi | Tampilan | Senjata |
|---|---|---|
| **Pejuang / arek Suroboyo** | Kemeja putih atau lurik, ikat kepala merah putih atau peci, ban lengan merah putih | Arisaka rampasan Jepang, Lee-Enfield, Sten |
| **Laskar rakyat** | Kemeja sederhana, ikat kepala | Bambu runcing (dipegang tegak, atau ditusukkan saat menyerbu) |
| **TKR / TNI** | Seragam khaki, pet lapangan dengan lencana merah putih, sabuk | Lee-Enfield, Arisaka, Sten |
| **Sekutu (Inggris-India)** | Seragam hijau rimba, helm Brodie ("piring"), sabuk & kantong peluru dada; sebagian bersorban | Lee-Enfield, Sten |
| **NICA / KNIL** | Seragam hijau zaitun, helm M1 | Lee-Enfield, Sten |
| **Warga** | Kemeja, celana panjang, peci atau caping | — |
| **Tokoh khusus** | Kolonel Soedirman (seragam TKR + peci), Panglima Besar (mantel gelap), Residen (setelan putih) | — |

Satu model karakter dipakai untuk semua tokoh. Warnanya diganti per bagian tubuh lewat *shader*, lalu perlengkapan (helm, peci, caping, ikat kepala, sabuk) ditempelkan ke tulang kepala, lengan, dan pinggul.

---

## 5. Desain permainan

### Lingkaran permainan
**Film** (konteks & emosi) → **Tujuan** (bertahan / rebut / kawal / hancurkan / bergerak) → **Pertempuran** (perlindungan, sikap tubuh, amunisi terbatas) → **Tujuan tercapai** → film atau tujuan berikutnya.

### Jenis tujuan
- **Bertahan** — tahan zona selama waktu tertentu; musuh datang bergelombang dari arah tertentu.
- **Rebut wilayah** — kosongkan zona dari musuh lalu kuasai beberapa detik.
- **Lumpuhkan** — kalahkan semua penjaga di satu lokasi.
- **Hancurkan sasaran** — ledakkan tong mesiu / generator.
- **Kawal / evakuasi** — jemput warga atau rombongan, bawa ke tempat aman; mereka mengikuti pemain dan bisa gugur kena tembakan atau ledakan.
- **Bergerak** — capai lokasi tertentu.

### Senjata zaman itu
| Senjata | Sifat |
|---|---|
| **Arisaka Type 99** | 5 peluru, satu tembakan hampir melumpuhkan, harus dikokang (ada animasinya) |
| **Lee-Enfield No.4** | 10 peluru, kokang lebih cepat |
| **Sten Mk II** | Senapan mesin ringan, otomatis, akurat di jarak dekat |
| **Colt M1911** | Pistol cadangan |
| **Granat** | Untuk bunker dan kelompok musuh |

### Kecerdasan buatan
- **Tentara musuh & rekan**: mencari lawan, bersembunyi, berganti sikap (berdiri/jongkok/tiarap), dan menembak sesuai senjatanya (beruntun atau satu-satu). Mereka berteriak ("Musuh di depan!", "Contact front!", "Vuur!").
- **Warga**: berjalan-jalan dan mengobrol; saat mendengar tembakan atau ledakan, mereka lari menjauh lalu jongkok berlindung. Mereka bisa diperintah mengikuti pemain.

### Aturan moral
Menembak warga sipil memberi penalti skor dan peringatan lewat radio. Musuh tidak menarget warga: fokus cerita adalah perjuangan, bukan kekejaman.

---

## 6. Arah visual & audio

- **Warna**: sepia hangat saat bermain; sepia lebih kuat saat film; hitam-putih berbintik & bergaris untuk kilas balik bergaya arsip.
- **Sinematografi**: letterbox, kamera genggam yang sedikit bergoyang, dolly, orbit, dan kamera yang mengikuti tokoh; kartu judul bergaya mesin ketik.
- **Suasana**: kota berasap, bangunan rusak, kawah bom, api; pesawat melintas dengan pita putih SEAC.
- **Audio**: seluruh suara disintesis (Web Audio): tembakan dengan gema, kokang senapan, ledakan, dengung pesawat dengan efek Doppler, siulan bom, sirene, kentongan, riuh massa. Narasi dan dialog dibacakan suara bawaan browser (Web Speech).

---

## 7. Teknologi

| Bagian | Pendekatan |
|---|---|
| Rendering | three.js / WebGL, bayangan dinamis, langit shader, vegetasi *instanced* per chunk |
| Dunia | Medan dari *noise*, sungai & laut, jalan, lalu bangunan prosedural digabung per bahan agar ringan |
| Karakter | Kerangka Mixamo; animasi dua lapis (tubuh atas / bawah) + IK dua tulang untuk memegang senjata, bidikan, gestur, dan tatapan |
| Kostum | *Shader* mewarnai ulang tekstur per bagian tubuh + perlengkapan yang ditempel ke tulang |
| Film | "Sutradara" berbasis data: shot kamera, aksi aktor, subtitle, suara, efek |
| Fisika | Collider kotak dalam grid spasial, raycast untuk peluru & garis pandang |
| Multiplayer | WebSocket (server sendiri) atau P2P WebRTC (PeerJS) saat hosting statis |
| Distribusi demo | Kode di-bundle & di-minify dengan esbuild; dihosting statis (Vercel) |

---

## 8. Rencana pengembangan

- Model karakter khusus per faksi (Meshy + Mixamo) untuk wajah dan postur yang lebih beragam.
- Animasi khusus: menikam dengan bambu runcing, memanggul tandu, memanjat.
- Pengisi suara manusia untuk narasi dan dialog utama.
- Bab tambahan: Bandung Lautan Api (1946), Pertempuran Lima Hari di Semarang, Serangan Umum 1 Maret sebagai misi yang dimainkan.
- Kontrol untuk ponsel & tablet.
