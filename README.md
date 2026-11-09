# Keysa Birthday (Vercel)

Situs statis satu halaman, tanpa build. Isinya:

- `index.html`  : halaman utamanya (semua foto, lagu, voice note, dan model 3D sudah tertanam di dalamnya)
- `vercel.json` : header keamanan + cache
- `package.json`: biar Vercel mengenali ini project biasa

## Cara deploy

### Lewat CLI
```bash
npm i -g vercel
cd keysa-birthday
vercel --prod
```
Kalau ditanya: Framework = Other, Build Command = kosong, Output Directory = kosong.

### Lewat GitHub
1. Upload isi folder ini ke repo GitHub.
2. Di vercel.com/new, import repo itu.
3. Framework Preset: Other. Build Command dan Output Directory dibiarkan kosong. Klik Deploy.

## Catatan
- Three.js dan font dimuat dari jsDelivr dan Google Fonts (sudah diizinkan di `vercel.json`).
  Kalau kamu menambah sumber lain (CDN/gambar eksternal), tambahkan juga ke `Content-Security-Policy`.
- Header `X-Robots-Tag: noindex` membuat halaman ini tidak muncul di Google. Hapus barisnya kalau mau terindeks.
