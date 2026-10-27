# Checklist trip Jawa Tengah

Folder ini berisi `index.html` (aplikasinya) dan `supabase.sql` (skema database).

## 1. Siapkan Supabase
1. Buat proyek baru di supabase.com (paket gratis cukup).
2. Buka **SQL Editor**, tempel isi `supabase.sql`, lalu **Run**.
3. Buka **Project Settings > API**, salin **Project URL** dan kunci **anon public**.
4. Di `index.html`, ganti `PASTE_SUPABASE_URL` dan `PASTE_ANON_KEY` dengan nilai tadi.
   Jangan pernah memakai kunci `service_role` di sini.

## 2. Deploy ke Vercel
Di terminal, dari folder ini:

    npx vercel --prod

Atau unggah folder ke GitHub lalu impor repositori itu di vercel.com. Tidak perlu framework atau perintah build.

## 3. Bagikan ke teman
1. Buka alamat Vercel di HP-mu. Halaman membuat kode trip acak di belakang tanda `#`, lalu pilih **Saya pemilik tautan**.
2. Tekan **Salin tautan**, kirim ke temanmu (tautan harus lengkap dengan bagian `#...`), lalu ia memilih **Saya teman**.
3. Siapa pun yang punya tautan lengkap itu bisa mengedit, jadi jangan disebar.

## Cara kerja singkat
- Perubahan disimpan di HP dulu, lalu dikirim ke Supabase saat ada sinyal.
- Halaman memperbarui data tiap 8 detik dan saat dibuka kembali, bukan realtime.
- Tombol ≡ di kiri tiap barang dipakai untuk menggeser urutan (di keyboard: fokus ke ≡ lalu tekan panah atas/bawah). Urutan ikut tersinkron ke teman.
- Tombol × menyembunyikan barang (bisa dikembalikan dari "Item tersembunyi").
