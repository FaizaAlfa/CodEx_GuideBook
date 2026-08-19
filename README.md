# GuideBook CODEX 2026

Dokumentasi CODEX 2026 dibuat dengan Jekyll dan tema [Just the Docs](https://just-the-docs.com/).

## Menjalankan secara lokal

### Prasyarat

- Ruby 3.3 atau yang lebih baru
- Bundler (`gem install bundler`)

Di Windows, cara termudah memasang Ruby adalah menggunakan [RubyInstaller](https://rubyinstaller.org/downloads/). Pilih installer yang menyertakan MSYS2, lalu buka terminal baru setelah instalasi selesai.

### Instalasi dan server development

Jalankan dari root repository:

```powershell
bundle install
bundle exec jekyll serve --livereload
```

Buka <http://localhost:4000>. Jekyll akan membangun ulang halaman ketika file Markdown atau konfigurasi berubah.

Untuk hanya menguji proses build:

```powershell
bundle exec jekyll build
```

Jika `ruby` atau `bundle` tidak dikenali, Ruby belum terpasang atau terminal belum dibuka ulang. Perintah `source 'https://rubygems.org'` bukan perintah PowerShell; URL tersebut hanya deklarasi sumber gem di `Gemfile`.

## Deploy

Workflow GitHub Actions di `.github/workflows/pages.yml` membangun dan menerbitkan situs ke GitHub Pages setiap push ke branch `main`.
