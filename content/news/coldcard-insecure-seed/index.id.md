---
title: "Seed COLDCARD Tidak Aman"
date: "2026-08-02"
draft: false
description: "Panduan singkat untuk memindahkan dana dari seed yang dibuat pada perangkat Coinkite."
---

[Coinkite telah mengungkap kelemahan dalam pembuatan seed pada firmware COLDCARD yang terdampak](https://blog.coinkite.com/coldcard-mk3-seed-generation-warning/). Baca juga [analisis teknis Block tentang fallback RNG yang dapat diprediksi dan reseed 32-bit](https://engineering.block.xyz/blog/predictable-rng-fallback-and-32-bit-reseed-in-coldcard-firmware). Memperbarui firmware tidak memperbaiki seed yang sudah ada.

**Jika Anda membuat seed dengan produk Coinkite apa pun, segera lakukan migrasi!**

## Daftar periksa migrasi

1. Pada **perangkat penandatangan non-COLDCARD** ([lihat perangkat yang didukung]({{< ref "library/supported-hardware-signers" >}})), buat dompet yang benar-benar baru dengan panduan pengaturan Bitcoin-Safe: pilih [dompet tanda tangan tunggal]({{< ref "library/setup-singlesig-wallet" >}}) atau [dompet multisig]({{< ref "library/setup-multisig-wallet" >}}). Jangan gunakan kembali seed lama.
   - Jika tidak tersedia penandatangan perangkat keras selain COLDCARD, [MetroVault]({{< ref "library/supported-hardware-signers/metrovault" >}}) dapat digunakan pada perangkat Android khusus yang sudah direset ke setelan pabrik, selalu offline, dan hanya digunakan untuk menandatangani.
   - Selesaikan pengujian menerima dan mengirim dalam panduan untuk memastikan dompet baru telah disiapkan dengan benar: verifikasi cadangan dan alamat penerimaan pada penandatangan baru, terima sejumlah kecil dana pengujian, lalu lakukan pengiriman mandiri ke alamat lain yang telah diverifikasi dalam dompet baru.
2. Tandatangani transaksi migrasi, tetapi **jangan siarkan dengan cara biasa**. Salin transaksi mentah yang sudah ditandatangani dan kirim langsung melalui [MARA Slipstream](https://slipstream.mara.com/) untuk mengurangi waktu kunci publik dompet lama terekspos di mempool publik.
3. Simpan COLDCARD lama sampai seluruh saldo telah tiba dan dikonfirmasi di dompet baru, lalu perbarui ke firmware terbaru.

Jika Anda membantu seseorang melakukan migrasi, jangan pernah meminta mereka membagikan, memotret, atau mengetik kata-kata seed. Seed harus tetap bersifat pribadi dan hanya dimasukkan pada perangkat penandatangan.
