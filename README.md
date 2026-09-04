# qg

GitHub dashboard TUI — semua repo kamu dalam satu layar, arrow-key navigation.

## Jalankan
```bash
qg              # atau python3 ~/qg/qg
qg --no-cache   # paksa refresh dari GitHub
```

## Tombol

| Tombol | Aksi |
|--------|------|
| `↑` `↓` | navigasi kursor |
| `←` `→` | ganti halaman (25 repo/halaman) |
| `enter` | preview repo (`gh repo view`) |
| `/` | cari nama & deskripsi |
| `backspace` | hapus pencarian |
| `f` | filter tipe: all → fork → source → private → public |
| `m` | menu filter: tipe / bahasa (custom bebas, `!` exclude) / urutan / cari |
| `L` | cycle filter bahasa |
| `!` | exclude bahasa yang sedang difilter |
| `s` | star/unstar repo di kursor |
| `TAB` | multi-select repo |
| `S` | star semua repo terpilih |
| `c` | clone repo di kursor |
| `C` | clone semua repo terpilih |
| `n` | bikin repo baru (otomatis private) |
| `O` | ganti urutan: pushed → name → stars |
| `o` | buka repo di browser |
| `R` | force refresh data |
| `q` | keluar |

## Tabel

Kolom: `>` kursor · nomor baris (lanjut antar halaman) · badge `PRIV`/`PUB`/`FORK` · nama · deskripsi · last push · `*`+bahasa (bintang = kamu star repo itu).

Status bar bawah: total repo terfilter/total, halaman, pencarian & filter aktif, jumlah terpilih, total stars & issues (live dari GitHub).

## Deps
- `gh` (sudah login) + python3: `pip install rich`

Cache: `~/.cache/qg/repos.json` (1 jam).
