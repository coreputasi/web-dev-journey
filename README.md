# 🌐 web-dev-journey

> *Dari `<div>` pertama sampai (semoga) jadi web developer beneran.*

Selamat datang di **web-dev-journey** — dokumentasi perjalanan belajar web development saya, dari nol banget. Repo ini bukan cuma kumpulan kode, tapi juga jejak progres, catatan error yang bikin pusing, dan kemenangan-kemenangan kecil di sepanjang jalan.

---

## 🎯 Kenapa Repo Ini Ada?

Belajar coding itu jauh lebih seru (dan konsisten) kalau ada bukti nyata dari progres yang sudah dijalani. Jadi, tujuan repo ini:

- 📚 Mendokumentasikan setiap topik yang dipelajari, step by step
- 🛠️ Menyimpan project-project kecil sebagai bukti praktik nyata
- 📈 Melihat progres dari waktu ke waktu — dari HTML dasar sampai (nantinya) full stack
- 💼 Membangun portofolio yang bisa ditunjukkan ke siapa saja

---

## 🗺️ Roadmap Belajar

- [x] **HTML Dasar** — struktur, semantic tags, forms, table
- [x] **Media Element** — audio, video, iframe, SVG
- [x] **CSS** — styling, layout, flexbox, grid
- [x] **CSS Responsive & Animation**
- [ ] **JavaScript Dasar**
- [ ] **JavaScript DOM & Interaktivitas**
- [ ] **Framework/Library (TBD)**
- [ ] **Proyek Akhir**

*(checklist ini akan terus di-update seiring progres)*

---

## 📁 Struktur Folder

```
web-dev-journey/
├── README.md
├── 01-html-basics/
├── 02-media-elements/
├── 03-css/
├── ...
└── notes/
    └── catatan-harian.md
```

Setiap folder mewakili satu topik atau milestone belajar, biar mudah ditelusuri kapan pun.

---

## 🧰 Tools yang Dipakai

- **VS Code** — code editor utama
- **Git & GitHub** — version control dan dokumentasi progres
- **Emmet** — biar ngoding HTML/CSS lebih ngebut

---

## ✨ Catatan

Setiap commit di repo ini adalah bagian dari proses belajar — termasuk yang typo, yang bug, dan yang akhirnya berhasil setelah dicoba berkali-kali. Progres kecil tetap progres. 🚀

---

<p align="center">
  <i>Dibangun satu tag, satu commit, satu error pada satu waktu.</i>
</p>


# Git Workflow — Cheat Sheet Harian

Cheat sheet ini buat proyek `web-dev-journey`, khususnya kerja di branch `feature-css`.

---

## 🌅 Sebelum Mulai Kerja

```bash
git branch                      # cek kamu ada di branch yang benar
git status                      # cek ada perubahan belum ke-commit atau nggak
git pull origin feature-css     # tarik update terbaru dari GitHub
```

Kalau ketiga command lancar tanpa error → **langsung lanjut ngoding**.

---

## 🌙 Setelah Selesai Kerja

```bash
git add .
git commit -m "pesan yang jelas soal apa yang kamu kerjain"
git push origin feature-css
```

Cek sekali lagi:
```bash
git status
```
Kalau muncul `nothing to commit, working tree clean` → aman, semua sudah ke GitHub.

---

## 🛠️ Kalau Push Ditolak (non-fast-forward)

Artinya ada perubahan di GitHub yang belum ada di laptop kamu.

```bash
git pull origin feature-css
```

- Kalau muncul editor Vim minta commit message → tekan `Esc`, ketik `:wq`, Enter (simpan pesan default).
- Kalau ada conflict → buka file yang bentrok, cari tanda `<<<<<<<`, `=======`, `>>>>>>>`, edit manual, lalu:
  ```bash
  git add <nama_file>
  git commit
  ```

Setelah beres:
```bash
git push origin feature-css
```

---

## 📋 Format Commit Message yang Bagus

| Prefix | Kapan dipakai |
|---|---|
| `feat:` | Menambah fitur baru |
| `fix:` | Memperbaiki bug |
| `style:` | Perubahan tampilan/CSS, bukan logic |
| `refactor:` | Merapikan kode tanpa mengubah fungsi |
| `docs:` | Update dokumentasi/README |

Contoh: `feat: add greeting card html structure`

---

## 🔍 Command Cek Cepat

```bash
git log --oneline -5              # lihat 5 commit terakhir
git log --oneline --graph --all   # lihat history + branch secara visual
git branch                        # lihat branch aktif
git status                        # lihat perubahan yang belum ke-commit
```

---

## 🧠 Aturan Emas

1. **Selalu `pull` sebelum mulai kerja.**
2. **Selalu `add → commit → push` sebelum menutup laptop.**
3. **Commit kecil & sering**, jangan numpuk banyak perubahan sekaligus.
4. **Jangan panik kalau push ditolak** — itu normal, tinggal `pull` lalu `push` lagi.
