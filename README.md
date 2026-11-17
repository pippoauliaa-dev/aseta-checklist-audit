# Aseta — Checklist Audit Aset (Interaktif)

Checklist audit aset 25 poin yang bisa diisi langsung di browser. Customer memilih skor 0/1/2 per poin, skor total dan interpretasi terhitung otomatis, lalu hasilnya bisa dikirim ke sales via WhatsApp.

## File

- `index.html` — aplikasi checklist (self-contained, tanpa dependency).

## Cara pakai

1. Host `index.html` di URL publik (Netlify, cPanel, GitHub Pages, dll).
2. Kirim link ke prospek.
3. Prospek mengisi checklist dan klik **"Kirim ke Sales via WhatsApp"**.
4. Hasil masuk ke nomor sales yang tertera.

## Ganti nomor sales

Edit baris berikut di `index.html`:

```js
var SALES_WA = '6281217984959';
```

Gunakan format internasional tanpa `+` (mis. `62812...`).

## Deploy

### Netlify Drop

Drag folder ini ke https://app.netlify.com/drop

### cPanel (aseta.id)

Upload `index.html` ke folder `checklist/` → URL: `https://aseta.id/checklist/`

### GitHub Pages

Settings → Pages → Deploy from branch `main` → root.

## Catatan

- Statis, tanpa backend. Tidak ada data yang disimpan di server.
- Hasil dikirim melalui WhatsApp deep link (`wa.me`).
- Untuk integrasi ke CRM/SLM, perlu backend/API tambahan.
