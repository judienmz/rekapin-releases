# Panduan Singkat Rekapin

*Bisnis Rapi, Data Terkendali.* Rekapin adalah aplikasi Windows **gratis** untuk seller Shopee & TikTok Shop yang punya banyak akun toko. Panduan ini membawamu dari pasang aplikasi sampai laporan pertama, kira-kira 15 menit.

**Isi:**
1. [Pasang aplikasi](#1-pasang-aplikasi)
2. [Buat akun owner](#2-buat-akun-owner)
3. [Tambah akun toko & profil bisnis](#3-tambah-akun-toko--profil-bisnis)
4. [Import file pertama](#4-import-file-pertama)
5. [Lengkapi produk, HPP & stok minimum](#5-lengkapi-produk-hpp--stok-minimum)
6. [Kas & Biaya (laba bersih)](#6-kas--biaya-laba-bersih)
7. [Lihat hasilnya](#7-lihat-hasilnya)
8. [Amankan data (penting)](#8-amankan-data-penting)
9. [Telegram Bot & Mini App (opsional)](#9-telegram-bot--mini-app-opsional)
10. [Fitur opsional lain](#10-fitur-opsional-lain)

---

## 1. Pasang aplikasi

1. Buka [halaman unduhan Rekapin](https://github.com/judienmz/rekapin-releases/releases/latest) lalu unduh `Rekapin-Setup-x.y.z.exe`.
2. Jalankan file itu. Kalau Windows menampilkan **"Windows protected your PC"**, klik **More info** → **Run anyway**. Ini muncul karena aplikasi belum memakai sertifikat berbayar, cukup sekali saat pasang pertama.
3. Butuh Windows 10/11 64-bit. Tidak perlu hak admin.

Versi baru ditawarkan otomatis di **Beranda** dan menu **Tentang & Update**. Update dicek tanda tangan digitalnya, jadi aman.

## 2. Buat akun owner

Saat pertama dibuka, isi **nama bisnis/toko**, **nama kamu**, dan **password** (minimal 8 karakter). Akun owner bisa melihat semua angka keuangan. Simpan password ini baik-baik.

## 3. Tambah akun toko & profil bisnis

- Menu **Akun Toko** → **Tambah akun Shopee** / **Tambah akun TikTok Shop**. Satu entri untuk setiap toko di Seller Center.
  - **Alias** = nama pendek yang muncul di laporan (mis. "AB Shopee").
  - **Username** toko: Shopee biasanya dikenali otomatis dari file; TikTok isi manual.
- Menu **Profil Bisnis**: isi nama, alamat, no. telepon. Dipakai sebagai kop laporan PDF/Excel.

## 4. Import file pertama

Unduh file export dari Seller Center masing-masing toko:

| Marketplace | File | Format | Isinya |
|---|---|---|---|
| Shopee | Pesanan | .xlsx | Pesanan & produk terjual |
| Shopee | Penghasilan | .xlsx | Dana cair & rincian biaya |
| Shopee | Iklan (riwayat saldo iklan) | .csv | Biaya iklan per hari |
| TikTok Shop | Pesanan | .xlsx | Pesanan & produk terjual |
| TikTok Shop | Penghasilan | .xlsx | Dana cair, biaya, iklan GMV Max |

Buka menu **Import** lalu tarik file ke kotak yang tersedia (boleh banyak sekaligus), atau klik **Pilih file**.

- Jenis file dikenali otomatis. Kalau ditanya *"File ini untuk akun mana?"*, pilih tokonya; Rekapin mengingatnya.
- Import file yang sama berulang kali **aman**: data diperbarui, tidak dobel.
- Untuk harian, cukup import file **Pesanan 30 hari terakhir**.
- Hasil dan catatan tiap file ada di **Riwayat Import**.

## 5. Lengkapi produk, HPP & stok minimum

- **Produk & SKU** → tab **SKU belum dikenal**: hubungkan SKU marketplace ke produk gudang (bisa juga dijadikan bundle), lalu isi **HPP** (modal per pcs). Tanpa HPP laba belum akurat dan stok SKU itu belum ikut terpotong.
- **Stok & Gudang** → **Stok masuk** untuk stok awal / kiriman supplier. Bisa sekalian mencatat pembayarannya ke Kas & Biaya.
- **Stok & Gudang** → tab **Saran restock**:
  - **Saran stok minimum** dihitung dari penjualan 30 hari × (lead time + 7 hari). Klik **Terapkan semua** kalau bingung harus isi berapa.
  - Produk yang belum punya minimum tetap dipantau dengan minimum "otomatis".
  - Kolom **Saran restock** = berapa pcs yang sebaiknya dipesan.

## 6. Kas & Biaya (laba bersih)

Menu **Kas & Biaya**:

1. Tab **Rekening**: tambahkan rekening bank, e-wallet, atau kas tunai beserta saldo awalnya.
2. **Catat transaksi**: kas masuk, keluar, atau transfer antar rekening, dengan kategori.
   - **Biaya operasional** (gaji, sewa, listrik, packing, dll.) **mengurangi laba bersih**.
   - **Pembelian stok, pencairan marketplace, modal, prive** hanya arus kas, *bukan* biaya/pendapatan (modal barang sudah dihitung lewat HPP).
3. Tab **Biaya rutin**: simpan gaji/sewa bulanan; Rekapin mengingatkan menjelang tanggalnya, kamu tinggal klik **Catat**.
4. Admin boleh mencatat pengeluaran kecil; nominalnya disembunyikan dan menunggu persetujuan owner di tab **Persetujuan**.

## 7. Lihat hasilnya

- **Beranda**: omzet, pesanan, laba, best seller, stok menipis.
- **Laporan**: Laba Rugi (dengan **Laba bersih**), Biaya, Iklan (ROAS & break-even), Retur, Dana, **Arus Kas**, Tutup Buku. Tombol **Excel** dan **PDF** di kanan atas.
- **Insight**: peringatan yang perlu ditangani; klik untuk melihat rinciannya.
- **Retur** dan **Stok Opname**: ACC retur dan hitung stok fisik.

## 8. Amankan data (penting)

Data tersimpan terenkripsi di PC ini. Buka menu **Backup**:

1. Simpan **kunci pemulihan** (bentuk `REKAPIN-XXXX-…`) di tempat aman. Tanpa kunci ini data tidak bisa dibuka lagi kalau Windows diinstal ulang atau pindah PC.
2. Atur folder backup. Arahkan ke folder Google Drive for Desktop / OneDrive supaya cadangan ikut tersimpan di cloud.

## 9. Telegram Bot & Mini App (opsional)

Menu **Telegram Bot**:

1. Buat bot di **@BotFather** (`/newbot`), tempel tokennya, klik **Sambungkan**.
2. **Hubungkan akun & grup** dengan kode: akun pribadi owner/admin, **Grup Owner** (keuangan), **Grup Operasional** (stok, tanpa Rupiah).
3. **Mode 24 Jam** (disarankan): pakai akun Cloudflare gratis milikmu supaya bot tetap jalan saat PC mati. Ikuti 4 langkah di kartu Mode 24 Jam.

Yang dikirim bot otomatis:

- **Rekap harian** (jam bisa diatur), **rekap stok** ke Grup Operasional (apa yang harus di-restock + jumlah saran), **rekap mingguan** (Senin), **laporan bulanan + PDF** (tanggal 1).
- **Peringatan**: stok perlu restock, retur lama di jalan, akun rugi setelah iklan, bulan ini rugi, dana belum cair >14 hari, biaya rutin jatuh tempo, catatan admin perlu disetujui, format file berubah.
- Perintah: `/omzet`, `/laba`, `/stok`, `/dana`, `/iklan`, `/tanya` (owner), dan kirim file Penghasilan/Iklan langsung ke bot.

**Mini App** (Mode 24 Jam): tekan tombol **Buka App** di chat bot.

- **Owner**: Beranda, Laporan (omzet, laba estimasi/aktual/bersih, iklan, retur, arus kas), Kas (saldo, catat, setujui), Gudang.
- **Admin**: Gudang (cek stok, stok masuk, opname, ACC retur) dan Kas (catat pengeluaran, tanpa melihat nominal).

## 10. Fitur opsional lain

- **Pengguna**: tambah admin dengan PIN. Admin bisa import pesanan dan mengurus stok, tapi **tidak melihat angka Rupiah**.
- **Asisten AI**: bantu mencocokkan format file baru dan menjawab `/tanya`. Memakai kunci API milikmu sendiri.

Semua fitur opsional boleh dilewati; aplikasi tetap berfungsi penuh tanpanya.

---

### Privasi

Semua data tersimpan di PC kamu sendiri dan terenkripsi. Rekapin tidak mengirim data ke pembuat aplikasi atau server mana pun. Bot & Mini App memakai akun Telegram dan Cloudflare milikmu sendiri, dan yang dikirim ke sana hanya ringkasan. Data pembeli (nama, alamat, no. HP) tidak pernah keluar dari PC.

### Kalau ada kendala

Kirim ke pembuat aplikasi:

- **Screenshot atau rekaman layar** (lebih jelas daripada foto layar pakai HP).
- Langkah yang kamu lakukan sebelum masalah muncul.
- Kalau soal import: nama file dan pesan di **Riwayat Import**. **Jangan kirim file export aslinya**, karena berisi data pembeli.
