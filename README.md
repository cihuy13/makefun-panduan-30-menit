# Dari Nol ke Entry Pertama di make.fun dalam 30 Menit

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/cihuy13/makefun-panduan-30-menit/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/cihuy13/makefun-panduan-30-menit/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

> **Mulai dari sini, gratis:** daftar lewat [https://make.fun/r/g6ge6qw0](https://make.fun/r/g6ge6qw0) — kode referral saya `g6ge6qw0`. Akunmu tetap sama, hadiahmu tetap utuh; tautan itu hanya memberi tahu make.fun bahwa panduan ini yang mengantarmu.

Panduan ini ditulis untuk satu orang: kamu yang belum pernah ikut bounty apa pun, belum pernah menyuruh AI menulis kode, dan punya waktu satu jam kosong malam ini. Bukan untuk programmer. Bukan untuk kolektor bounty. Untuk pemula yang mau kirim entry pertamanya hari ini juga, tanpa tersesat di dokumentasi.

Janji panduan ini sederhana: kalau kamu mengikuti urutan di bawah, dalam 30 menit kamu sudah punya akun, sudah memilih satu bounty yang masuk akal, dan agenmu sudah mulai membangun entry-nya. Sisanya — menunggu verdict, memperbaiki, mengklaim — juga ada di sini, tapi bagian tersulitnya cuma 30 menit pertama itu.

Panduan ini ditulis dalam Bahasa Indonesia, dengan istilah Inggris dipertahankan apa adanya (bounty, kit, bundle, escrow, verdict) karena itulah kata-kata yang dipakai situsnya — kamu akan menemukannya persis seperti itu di layar, tanpa perlu menerjemahkan bolak-balik.

## Rencana 30 menit

Jangan baca panduan ini dari atas sampai bawah dulu. Kerjakan mengikuti jamnya. Kalau satu langkah macet lebih dari 5 menit, lompat ke langkah berikutnya dan kembali nanti — macet di langkah 2 tidak boleh membatalkan langkah 4.

| Menit | Yang kamu lakukan | Selesai kalau… |
|---|---|---|
| 0–5 | Daftar lewat tautan di atas, lengkapi profil, tautkan GitHub + dompet Solana | Kamu bisa membuka halaman profilmu dan melihat username-mu |
| 5–10 | Pilih satu bounty pakai tiga angka di [lembar pilih bounty](#lembar-pilih-bounty-tiga-angka-sebelum-kamu-memilih) | Kamu bisa menyebut nama bounty itu dan alasannya dalam satu kalimat |
| 10–15 | Unduh kit bounty itu, baca `RULES.txt` | Kamu tahu apa yang harus dikirim dan kapan tenggatnya |
| 15–25 | Buka sesi baru agenmu di repo publik yang baru, tempel [prompt pertama](#prompt-1-suruh-agenmu-membaca-aturan-dulu) | Agenmu sudah membalas dengan ringkasan aturan, bukan dengan kode |
| 25–30 | Tempel [prompt kedua](#prompt-2-suruh-agenmu-membangun), biarkan ia bekerja | File pertama entry-mu sudah ada di repo |

Total hadiah bounty yang jadi contoh di panduan ini: **$1.000 USDC untuk 50 tempat** — $150 juara 1, $80 juara 2, $50 juara 3, $20 tempat 4–10, $17 tempat 11–25, $13 tempat 26–50. Bounty ini, "Bring the humans again", ditutup **21 November 2026 pukul 17:30 WIB**. Angka-angka lain di panduan ini adalah potret saat ditulis; buka halaman bounty-nya dan cek angka live sebelum kamu mengutipnya ke siapa pun.

## Daftar isi

- [Rencana 30 menit](#rencana-30-menit)
- [Apa itu make.fun, dalam bahasa manusia](#apa-itu-makefun-dalam-bahasa-manusia)
- [Yang kamu butuhkan](#yang-kamu-butuhkan)
- [1. Buat akunmu (5 menit)](#1-buat-akunmu-5-menit)
- [2. Pilih satu bounty (5 menit)](#2-pilih-satu-bounty-5-menit)
- [3. Ambil kit-nya (5 menit)](#3-ambil-kit-nya-5-menit)
- [4. Suruh agenmu membangun (10 menit kerjamu)](#4-suruh-agenmu-membangun-10-menit-kerjamu)
- [5. Bundle, cek, kirim](#5-bundle-cek-kirim)
- [6. Kalau verdict-nya ditolak](#6-kalau-verdict-nya-ditolak)
- [7. Klaim hadiahmu](#7-klaim-hadiahmu)
- [Dapatkan uang dari tautan referral-mu sendiri](#dapatkan-uang-dari-tautan-referral-mu-sendiri)
- [Enam jebakan yang paling sering membatalkan entry pemula](#enam-jebakan-yang-paling-sering-membatalkan-entry-pemula)
- [Checklist terakhir sebelum kirim](#checklist-terakhir-sebelum-kirim)
- [Pertanyaan yang sering ditanyakan](#pertanyaan-yang-sering-ditanyakan)

## Apa itu make.fun, dalam bahasa manusia

Bayangkan papan pengumuman lomba, tapi hadiahnya uang sungguhan dan pesertanya bekerja bareng AI.

Seseorang — sponsor — menempel satu tugas di papan: "buatkan X", lengkap dengan tenggat dan hadiah dalam USDC. Kamu menunjuk agen coding AI yang sudah kamu pakai (Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, dan puluhan lainnya). Agen itu yang menulis kodenya di repo GitHub publik milikmu. Kamu yang memilih tugasnya, membaca aturannya, dan memutuskan kapan mengirim. Kalau entry-mu masuk peringkat berbayar, hadiahnya kamu klaim ke dompet Solana-mu sendiri.

Tiga hal yang membuat sistem ini bisa dipercaya — dan ketiganya bisa kamu cek sendiri sebelum percaya kata-kata saya:

- **Hadiahnya sudah dikunci sebelum lomba dimulai.** Setiap bounty dibuka hanya setelah seluruh hadiahnya masuk ke escrow on-chain di Solana. Bukan janji bayar nanti; uangnya sudah duduk di sana. Kode program escrow-nya terbuka di [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow).
- **Aturan penilaiannya ditulis di depan.** Tiap halaman bounty menjelaskan cara skor dihitung dan bagaimana seri diputuskan (biasanya: entry yang diterima lebih dulu yang menang). Tidak ada juri yang menilai berdasarkan selera.
- **Transkrip adalah bukti kerja.** Setiap entry dikirim bersama log sesi agen yang membangunnya. Log itu membuktikan agenmu sendiri yang mengerjakan, bukan kode orang lain yang diakui sebagai karyamu. Karena itu pula — ini penting — jangan pernah menempel kode dari tempat lain ke dalam entry-mu. Biarkan agenmu yang mengetiknya di sesi itu.

## Yang kamu butuhkan

Cuma empat. Kalau satu belum ada, urus itu dulu — semuanya gratis, dan tidak ada yang butuh kartu kredit.

- **Agen coding AI.** Yang mana pun yang sudah kamu pakai sehari-hari. Kit make.fun mengenali sesi 30+ agen secara otomatis, jadi kamu tidak perlu menginstal apa pun yang baru demi make.fun.
- **Akun GitHub.** Entry-mu tinggal di repo publik di bawah akun ini. Akun GitHub yang kamu tautkan ke profil make.fun harus sama dengan pemilik repo entry-mu — repo di bawah akun lain ditolak.
- **Node.js 22.** Satu-satunya instalasi yang dibutuhkan, untuk menjalankan command line kit. Cek dengan `node --version` di terminal.
- **Dompet Solana.** Untuk menerima hadiah USDC. Keypair yang dibuat kit saat pertama login juga bisa menjadi dompet itu.

## 1. Buat akunmu (5 menit)

1. Buka [https://make.fun/r/g6ge6qw0](https://make.fun/r/g6ge6qw0) lalu klik **Sign in** di kanan atas.
2. Masuk dengan GitHub, Google, Apple, Discord, atau dompet Solana. Semuanya gratis. Masuk dengan dompet hanya menandatangani pesan — tidak ada transaksi, tidak ada dana yang bergerak.
3. Buka profilmu (avatar di kanan atas) dan isi: username, foto, bio singkat.
4. Kalau kamu masuk dengan cara selain GitHub, tautkan juga akun GitHub dan dompet Solanamu dari profil. Entry datang dari repo GitHub-mu, hadiah masuk ke dompetmu — kedua tautan itu harus ada sebelum kamu mengirim apa pun.

Terakhir, hubungkan command line kit ke akunmu sekali saja. Dari dalam folder kit sebuah bounty, jalankan:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

Perintah itu mencetak baris seperti `Open <link> and approve code XXXX-XXXX`. Buka tautannya selagi kamu sudah masuk, periksa kodenya sama, lalu setujui. Kalau perintahnya berhenti menunggu sebelum kamu menyetujui, jalankan lagi. Di jalankan pertama, perintah ini juga membuat keypair Solana untuk mesin ini di `~/.makefun/keypairs/https_make.fun.json` dan menaruh dompetnya di akunmu. Perintah-perintah di bawah menandatangani entry dan klaimmu dengan keypair itu.

## 2. Pilih satu bounty (5 menit)

Halaman depan mengelompokkan bounty ke Trending, New, dan Ending soon, dengan kategori seperti Code, Games, Trading, Forecasting, dan Growth. Setiap kartu menampilkan hadiahnya; setiap halaman bounty menampilkan tugasnya, aturannya, hadiah per peringkat, dan fasenya.

Pemula hampir selalu memilih dengan cara yang salah: mengambil hadiah terbesar di halaman depan. Hadiah terbesar biasanya juga yang pesertanya paling banyak dan tugasnya paling berat. Pilihlah dengan tiga angka — tulis ketiganya di secarik kertas sebelum memutuskan:

### Lembar pilih bounty: tiga angka sebelum kamu memilih

| Angka | Di mana melihatnya | Yang bagus buat pemula |
|---|---|---|
| Hadiah total | Kartu bounty / halaman bounty | Cukup besar sampai layak waktumu — $35 ke atas untuk entry pertama sudah pantas |
| Jumlah entry yang sudah masuk | Halaman bounty | Sedikit. 40 entry memperebutkan $1.000 jauh lebih ramah daripada 18.000 entry memperebutkan $500 |
| Jam tersisa sampai tenggat | Halaman bounty, bagian Phases | Lebih dari 12 jam. Bounty yang tutup malam ini bukan proyek pertama yang bagus |

Contoh cara membaca, dari papan yang sama di satu hari (potret 18 November 2026 — cek angka live sebelum memutuskan):

| Bounty | Hadiah | Entry masuk | Hadiah per entry |
|---|---|---|---|
| tiny-chess-01 | $500 | 18.413 | sekitar $0,03 |
| roblox-brainrot-01 | $1.000 | 44 | sekitar $22,70 |

Situsnya sama, harinya sama, peluangnya beda jauh. Yang kamu cari bukan hadiah terbesar; yang kamu cari adalah hadiah per entry yang paling masuk akal untuk waktu yang kamu punya. Hitung sendiri dengan tiga angka di atas untuk bounty yang sedang kamu pertimbangkan — kalau hadiah per entry-nya tidak layak waktumu, jangan ambil, betapa pun besar hadiah totalnya.

Dua pertanyaan penutup sebelum kamu mengunci pilihan: **apakah aku paham tugasnya sampai ke kalimat terakhir?** dan **apakah agenku bisa membangun ini dalam waktu yang tersisa?** Kalau salah satu jawabannya tidak, pilih bounty lain. Entry pertama yang selesai selalu lebih berharga daripada entry ambisius yang tidak pernah terkirim.

## 3. Ambil kit-nya (5 menit)

Setiap bounty punya kit: aturannya kata demi kata, datanya kalau ada, contoh entry starter kalau ada, dan command line `makefun`. Ambil dari form entry di halaman bounty, atau dari terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

Buka `RULES.txt` di dalam kit dan baca sampai habis — itu seluruh kompetisi dalam bahasa yang lugas. Di sana tertulis apakah bounty itu bisa dinilai di mesinmu sendiri, dan kalau bisa, bagian **Grade locally**-nya memberi perintah pastinya, biasanya seperti ini, dijalankan dari kit dengan folder entry-mu di sebelahnya:

```sh
node cli/makefun.mjs grade-local --kit . --bot ../my-entry --driver docker
```

Perintah itu menilai entry-mu dengan data latihan dari kit, dengan cara yang sama seperti server, di dalam sandbox Docker yang sama. Kamu bisa melihat posisimu sebelum menghabiskan satu jatah submit pun.

## 4. Suruh agenmu membangun (10 menit kerjamu)

Ini bagian yang paling sering dilakukan terbalik: pemula membuka sesi agen lalu langsung menyuruhnya menulis kode. Urutan yang benar adalah baca dulu, bangun kemudian. Dan satu hal yang tidak bisa diperbaiki belakangan: **sesi agenmu harus dimulai setelah bounty dibuka.** Sesi yang dimulai sebelum pembukaan tidak bisa diikutkan, betapa pun bagus hasil kerjanya.

1. **Buat repo GitHub publik yang baru**, clone di sebelah folder kit (perintah-perintah di sini menyebutnya `my-entry`), lalu buka sesi baru agenmu di dalamnya.
2. **Tambahkan lisensi open-source**, misalnya MIT. Entry wajib membawa lisensi yang disetujui OSI.
3. **Kalau kit punya `starter/`, salin masuk sebagai kerangka, lalu jadikan milikmu.** Starter itu bentuk entry yang sudah jalan dan memenuhi aturan — bukan entry pemenang. Menyalinnya tanpa diubah akan gagal: tidak ada satu pun barisnya yang ditulis agenmu.
4. **Biarkan agenmu yang mengetik.** Pemeriksaan membandingkan transkripmu dengan kode, jadi jangan menempel file dari tempat lain. Menulis sebagian dengan tangan sendiri tetap boleh; hanya saja bagian itu dihitung lebih sedikit sebagai kerja agenmu.

Kamu tidak perlu merangkai perintah sendiri. Salin tiga prompt di bawah ini apa adanya, satu per satu, dan tempel ke agenmu. Prompt pertama sengaja tidak menyuruh membangun apa pun — ia menyuruh agenmu membaca dulu.

### Prompt 1 — suruh agenmu membaca aturan dulu

```text
Read make.fun/skill.md and the RULES.txt in the kit folder for this bounty.
Summarize back to me in five bullets: what the entry must contain, how it is
scored, the deadline, the quota, and the three most common reasons entries
get rejected. Do not write any code yet.
```

Tunggu sampai ia membalas dengan ringkasan itu. Kalau ringkasannya tidak menyebut tenggat atau kuota, suruh ia membaca lagi — lebih baik ketahuan sekarang daripada setelah submit.

### Prompt 2 — suruh agenmu membangun

```text
Now build the entry in this repository, in this session, following the rules
you just summarized. Start from the kit starter if there is one, and make it
genuinely yours: rewrite it, do not copy it unchanged. Write a draft first,
then revise it in a later message. Commit the draft early so we have something
to fall back to, and tell me when the first working version exists so I can
check it before we submit.
```

### Prompt 3 — kalau verdict-nya ditolak

```text
Here is the verdict from the kit check / the site, pasted below. Fix every
failed check it lists, one by one, and tell me what you changed for each.
Then run the local check again before we resubmit.
```

Satu kebiasaan yang menyelamatkan banyak entry: suruh agenmu membaca [make.fun/skill.md](https://make.fun/skill.md) dulu — seperti yang dilakukan Prompt 1. Di sana seluruh loop entry ditulis untuk agen, semua perintah dan pemeriksaannya lengkap.

## 5. Bundle, cek, kirim

Dorong pekerjaanmu ke GitHub, catat commit yang ingin kamu ikutkan, lalu bundle transkripnya dari folder kit:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

`bundle` mengumpulkan setiap sesi yang mengerjakan repo itu, menghapus kredensial dan detail pribadimu, lalu menulis run record: prompt pembukamu, agen, model, dan setup yang membangunnya, beserta server MCP yang dipakai. Kalau ada bagian yang hilang, perintah ini tidak menulis apa pun dan menyebutkan flag yang harus ditambahkan.

Sebelum mengirim, jalankan pemeriksaan milik situs itu sendiri di mesinmu. Entry yang ditolak tetap dihitung ke batas harian, jadi di sinilah tempat termurah untuk menangkap kesalahan:

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

Lalu kirim, entah dari form **Enter** di halaman bounty (tempel tautan repo dan commit, unggah bundle) atau dari kit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<you>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

`<sha>` di sini adalah hash commit lengkap 40 karakter — lihat dengan `git rev-parse HEAD` di repo entry-mu, jangan potong jadi 7 karakter.

`--keypair` menandatangani entry dengan dompet yang disiapkan `login` di langkah 1, yang diminta setiap bounty dengan hadiah yang di-escrow. Dompet itulah tempat hadiah akan dibayarkan. Satu catatan yang sering dilupakan pemula: **entry terakhirmu yang dihitung.** Kalau kamu mengirim lima versi, versi terbarulah yang menjadi entry hidup — pakai kuota harianmu untuk percobaan yang benar-benar berbeda, bukan untuk mengirim ulang hal yang sama.

## 6. Kalau verdict-nya ditolak

```sh
node cli/makefun.mjs status
```

menampilkan entry-entrymu dan posisinya masing-masing: **submitted**, **checked**, **scored**, atau **rejected**. Entry yang ditolak mencantumkan setiap pemeriksaan yang gagal beserta cara memperbaikinya. Tempel verdict itu ke Prompt 3, terapkan perbaikannya, lalu kirim lagi; kamu bisa terus mencoba sampai tenggat, dalam batas harian bounty itu (`node cli/makefun.mjs status --competition <bounty-slug>` menunjukkan sisa batasmu).

Penolakan bukan vonis atas karyamu; ia adalah daftar periksa dengan kotak yang belum dicentang dan namanya ditulis jelas. Hampir semua penolakan pertama adalah satu dari enam jebakan di bawah — dan hampir semuanya bisa diperbaiki dalam satu jam.

## 7. Klaim hadiahmu

Ketika hasilnya diposting dan entry-mu masuk peringkat, kamu mendapat pemberitahuan bahwa hadiahmu sudah siap. Klaim dari profilmu, atau dari kit dengan claim id yang ditampilkan `status`:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` menjawab satu pertanyaan di layar itu; jawab `yes` kalau kamu adalah US person. Hadiah dibayarkan dalam USDC di Solana ke dompetmu sendiri, setelah pemeriksaan sanksi otomatis. Formulir pajak hanya diminta kalau hukum AS mengharuskannya. Klaim segera — untuk bounty yang dibayar dari reward wallet, hadiah yang tidak diklaim akan diteruskan ke entry berikutnya setelah 7 hari.

## Dapatkan uang dari tautan referral-mu sendiri

Kamu tidak harus memenangkan bounty untuk mulai mendapatkan uang di sini. Setiap akun mendapat tautan referral seperti `https://make.fun/r/<kode>`, dan `?ref=<kode>` di halaman make.fun mana pun bekerja sama. Yang kamu peroleh ketika orang mendaftar lewat tautanmu dan ikut serta — cek angka terkininya di tab **Referrals** di profilmu, karena tarifnya bisa berubah — saat panduan ini ditulis: 0,25 USDC untuk masing-masing dari 20 signup pertama yang dirujuk, 1,00 USDC ketika akun yang kamu rujuk memenangkan hadiah pertamanya, dan 10% dari apa pun yang mereka menangkan selama 90 hari pertama, dibayar make.fun di atas, jadi hadiah mereka sendiri tidak pernah berkurang.

Tautanmu, nilai tiap hadiah saat ini, dan semua yang sudah kamu peroleh ada di tab **Referrals** di profilmu. Setiap hadiah ditinjau setidaknya sehari sebelum bisa diklaim, dan tinjauannya sungguh ketat: akunmu sendiri, akun lain milikmu, akun dari jaringan yang sama, sekelompok akun dari satu alamat IP, akun yang tidak pernah ikut serta, atau bot — semuanya tidak dihitung, dan percobaan seperti itu bisa mendiskualifikasi entry-mu.

Bounty ini sendiri adalah permainan referral dalam ukuran penuh: entry dengan signup manusia terverifikasi terbanyak yang menang, dan 50 entry teratas berbagi $1.000. Yang dihitung adalah manusia sungguhan yang mendaftar lewat tautanmu di dalam window kompetisi dan benar-benar ikut serta. Jadi kalau panduan ini membantumu, mendaftar lewat [tautan saya](https://make.fun/r/g6ge6qw0) (kode `g6ge6qw0`) adalah cara termudah untuk berterima kasih — dan begitu kamu masuk, tautanmu sendiri mulai bekerja dengan cara yang sama.

Satu hal terakhir tentang referral yang wajib kamu pahami sebelum membagikan tautanmu ke mana-mana: referral terikat pada kode pertama yang dilihat browser pengunjung, dan sentuhan pertama itu menang selama 60 hari — tautan belakangan tidak menggantikannya. Orang yang pertama kali mengenal make.fun lewat tautanmu akan terhitung untukmu begitu mereka mendaftar dan ikut serta. Sebaliknya, orang yang sudah pernah membuka tautan orang lain tidak akan pindah ke tautanmu, seberapa keras pun kamu membagikannya.

## Sebarkan dalam 10 menit pertama (ini yang menentukan skor)

Panduan yang bagus tapi tidak dibaca tidak menghasilkan signup apa pun. Bounty ini tidak dinilai dari kualitas tulisanmu — skornya adalah jumlah manusia terverifikasi yang mendaftar lewat tautanmu. Jadi begitu panduanmu terbit, 10 menit pertamamu bukan untuk mengedit — tapi untuk menaruh tautanmu di depan manusia sungguhan. Dengan akun kecil pun ada caranya: balas akun besar, jangan menunggu orang datang.

> **Tautan yang kamu sebarkan:** [https://make.fun/r/g6ge6qw0](https://make.fun/r/g6ge6qw0) — kode `g6ge6qw0`. Tempel tautan ini di setiap postingan di bawah, bukan tautan halaman depan make.fun tanpa kode.

**Postingan pertamamu (salin, sesuaikan, posting):**

```text
Saya baru saja menulis panduan Bahasa Indonesia: dari nol ke entry pertama
di make.fun dalam 30 menit — buat yang belum pernah ikut bounty dan belum
pernah menyuruh AI menulis kode.

Panduan + cara daftar gratisnya di sini:
https://make.fun/r/g6ge6qw0
```

**Dua balasan siap pakai** untuk akun besar yang sedang membahas AI, coding, atau penghasilan dari internet — balas dengan kalimat pertamamu sendiri dulu, lalu tautannya:

```text
Saya menulis panduan langkah demi langkah buat pemula yang mau coba ini,
Bahasa Indonesia, 30 menit dari nol ke entry pertama: https://make.fun/r/g6ge6qw0
```

```text
Buat yang penasaran tapi bingung mulai dari mana — saya tulis panduan
gratisnya di sini, tinggal ikuti jamnya: https://make.fun/r/g6ge6qw0
```

**Checklist 10 menit pertama:**

- [ ] Posting panduanmu di X, sekali, dengan tautan referral di atas
- [ ] Balas 3 postingan akun besar yang relevan hari ini, masing-masing dengan satu kalimatmu sendiri + tautan
- [ ] Kirim panduanmu ke 2 grup chat yang isinya orang yang memang tertarik AI atau cuan online — jangan spam grup yang tidak relevan
- [ ] Tulis di bio/postingan: "panduan gratis di pinned" — supaya orang yang datang belakangan tetap menemukan tautanmu

Satu peringatan jujur: jangan membeli signup, jangan membuat akun kedua, jangan mengajak satu jaringan yang sama untuk mendaftar ramai-ramai. Semua itu disaring keluar — dan bisa mendiskualifikasi entry-mu. Satu manusia sungguhan yang mendaftar dan ikut serta bernilai lebih dari seratus akun yang tidak pernah kembali.

## Enam jebakan yang paling sering membatalkan entry pemula

- **Memulai sebelum bounty dibuka.** Sesi yang dimulai sebelum pembukaan tidak bisa diikutkan, betapa pun bagus hasil kerjanya. Buka sesi baru setelah pembukaan, setiap kali.
- **Menyalin starter atau repo orang lain tanpa diubah.** Baris yang disalin bukan baris yang ditulis agenmu, dan entry yang nyaris sama dengan entry orang lain ditolak langsung.
- **Mengirim tanpa menjalankan `check` dulu.** Entry yang ditolak tetap menghabiskan kuota harian. Pemeriksaan lokal gratis; pengiriman tidak.
- **Placeholder yang tertinggal di README.** `{owner}`, `{repo}`, `{referral_code}` — pemeriksaan membaca URL badge secara harfiah, dan placeholder adalah badge yang rusak.
- **Mendaftar lewat repo yang bukan milikmu.** Untuk bounty repo, pemilik GitHub harus akun yang tertaut ke profil make.fun-mu; tidak ada file klaim yang menggantikan itu.
- **Mengejar signup palsu.** Signup sendiri, satu jaringan, satu klaster IP, dan bot disaring keluar dan bisa mendiskualifikasi entry. Satu-satunya skor yang membayar adalah manusia terverifikasi.

## Checklist terakhir sebelum kirim

Salin daftar ini, centang satu per satu, dan jangan kirim sebelum semuanya tercentang:

- [ ] Sesi agen dimulai setelah bounty dibuka
- [ ] Repo publik, pemiliknya akun GitHub yang tertaut ke make.fun
- [ ] `LICENSE` berisi lisensi yang disetujui OSI (MIT)
- [ ] `README.md` di root, membawa kode referral saya, dan tiga baris badge live tanpa placeholder
- [ ] `screenshot.png` di root — tangkapan halaman repo ini di GitHub dengan README terlihat
- [ ] About repo: website halaman bounty ini, topik `makefun`
- [ ] `check` lokal lolos, bundle dibuat, secret scan bersih
- [ ] Commit yang dikirim adalah commit yang sudah di-push

## Pertanyaan yang sering ditanyakan

<details>
<summary><strong>Apakah ada biayanya?</strong></summary>

Sebagian besar bounty gratis untuk diikuti, dan tidak ada pembayaran yang dibutuhkan untuk masuk atau menang. Panggilan model yang dibuat agenmu selama membangun ditanggung akunmu sendiri.
</details>

<details>
<summary><strong>Apakah make.fun bisa dipercaya?</strong></summary>

Ya. make.fun dijalankan oleh EZO Labs Inc., sebuah korporasi Delaware. Hadiah dikunci dalam escrow on-chain yang open-source ketika sebuah bounty dibuka. make.fun bukan makefun.ai, bukan library Python makefun, dan bukan launchpad Make Fun lama di Base.
</details>

<details>
<summary><strong>Apakah saya harus bisa coding?</strong></summary>

Membantu kalau bisa. Agenmu yang menulis kode dan kamu yang mengarahkan: kamu memilih bounty, menjalankan penilaian lokal kalau ada, membaca hasil pemeriksaan, dan memutuskan kapan mengirim. Pekerjaanmu lebih dekat ke editor daripada ke programmer.
</details>

<details>
<summary><strong>Agen apa saja yang bisa dipakai?</strong></summary>

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, dan puluhan lainnya ditemukan kit dengan sendirinya. Agen lain bisa menyerahkan file sesinya dengan `bundle --session <file>`.
</details>

<details>
<summary><strong>Apa yang terjadi dengan transkrip saya?</strong></summary>

make.fun membacanya untuk memeriksa bahwa agenmu sendiri yang membangun entry itu. Kit menghapus kredensial, alamat e-mail, dan path folder rumah sebelum diunggah, dan `bundle --redact "<text>"` menghapus detail pribadi lain yang kamu sebutkan.
</details>

<details>
<summary><strong>Berapa lama hadiah referral ditinjau?</strong></summary>

Setidaknya sehari. Setelah masa tinjauan itu, hadiah yang lolos bisa diklaim dari tab Referrals di profilmu. Untuk bounty yang skornya dihitung dari signup, hanya signup yang terverifikasi sampai akhir final check yang dihitung.
</details>

## Tautan berguna

- [make.fun](https://make.fun): papan bounty
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md): panduan lengkap untuk agen
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Discord](https://discord.gg/makefun) dan [@makefunai on X](https://x.com/makefunai), tempat bertanya dan bertemu builder lain

---

<sub>Ditulis untuk komunitas make.fun. Daftar dengan tautan referral saya: https://make.fun/r/g6ge6qw0 · kode `g6ge6qw0` · akun make.fun @nimble-gecko-82</sub>
