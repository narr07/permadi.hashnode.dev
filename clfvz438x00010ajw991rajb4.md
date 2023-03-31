---
title: "Install Storyblok pada Nuxt.js"
seoTitle: "Install Storyblok pada Nuxt.js"
seoDescription: "Storyblok adalah CMS headless yang memberikan pengalaman konten yang kuat di platform digital apa pun."
datePublished: Fri Mar 31 2023 03:16:49 GMT+0000 (Coordinated Universal Time)
cuid: clfvz438x00010ajw991rajb4
slug: install-storyblok-pada-nuxtjs
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1680230194320/c575fabf-3e2c-45f5-a8a1-c7b047e19c06.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1680232568495/290b759b-a8e2-4308-9657-c78f00eb7b74.png
tags: nuxt, storyblok, tailwind-css, nuxt3

---

## Kenapa menggunakan storyblok?

Storyblok adalah CMS headless yang memungkinkan pengembang dan pemasar untuk memberikan pengalaman konten yang kuat di platform digital apa pun. Ada beberapa alasan mengapa seseorang mungkin ingin menggunakan Storyblok sebagai CMS:

1. Efisiensi proses konten: Streamline alur kerja konten Anda dan memberikan pengalaman yang lebih baik dan dipersonalisasi. Storyblok membantu Anda membuat situs web yang lebih baik dan mengelola konten Anda lebih cepat.
    
2. Pengalaman yang cepat: Kurangi tingkat keluar Anda dengan memberikan pengalaman yang cepat kepada pengguna Anda, tidak peduli browser atau platform web apa yang digunakan.
    
3. Membuat sekali, publikasikan di mana saja: Dengan CMS web headless Storyblok, konten yang diterbitkan dikirim melalui API. Perubahan dibuat sekali dan akan muncul di mana saja: situs web, seluler, IoT, AR / VR, dan lainnya.
    
4. Pengalaman visual yang sederhana namun kuat untuk editor dan pemasar.
    

## Buat akun storyblok

Buka website resminya [Storyblok](https://www.storyblok.com/), kalian daftar dengan akun baru kalau belum punya. Setelah daftar akun, login dan tampilanya akan sepeti berikut

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680230558209/d5155735-f943-4b5c-9fdb-4541e42c813f.png align="center")

Klik add space di pojok kanan dan beri nama bebas semau kalian, saya senidir nama space nya belajar nuxt

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680230630218/a009083c-c656-40c4-b821-904f5c49effc.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680230712453/044d7d4b-f367-46f2-b7cf-30685220e6ae.png align="center")

Klik **Back to V1**, karena saya akan menggunakan storyblok versi1, supaya lebih mempermudah. maka tampilannya akan berubah

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680231208249/bc547592-04ae-4832-a7ac-df51f5ee77cb.png align="center")

Klik tab **setting,** lalu pilih versi 1. Kemduian pada **Location (default environment)** isikan dengan `http://localhost:3000/` lalu klik save.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680231594775/001729a0-39e6-470c-a6cb-b491fafb0beb.png align="center")

kemudian pada terminal ketikan `npm run dev -- -o`

Buka tab **content** dan buka **Home**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680231753471/2a8543c2-dee7-476e-85cb-0813f5b44173.png align="center")

Buka tab **config**, gulir kebawah cari **real path,** isi dengan `/`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680231802534/fc919ecb-b302-42d1-b8ae-4179ba360de5.png align="center")

## Menghubungkan Nuxt ke Storyblok

Install [Module Storyblok](https://github.com/storyblok/storyblok-nuxt) ikuti cara berikut, buka terminal kalian pada VS Code dengan projek sebelumnya, ketikan kode berikut.

```bash
npm install @storyblok/nuxt
```

Tuggu sampai selesai, kemudian buka lagi space storyblok kalian, masuk ke tab **settings**, kemudian tab **API-Key,** copy api keynya

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680232069181/caedcf4d-d11c-44d8-a940-d88c2a33cde7.png align="center")

Kalau sudah di copy, kemabli ke VS code, buka file `nuxt.config.ts` tambahkan kode sehingga menjadi seperti berikut `["@storyblok/nuxt", { accessToken: process.env.STORYBLOK_ACCESS_TOKEN }],`

```typescript
export default defineNuxtConfig({
  modules: [
    "@nuxtjs/tailwindcss",
    ["@storyblok/nuxt", { accessToken: process.env.STORYBLOK_ACCESS_TOKEN }],
    ],
  tailwindcss: {
    cssPath: "~/assets/css/tailwind.css",
    configPath: "tailwind.config.js",
    viewer: true,
  },
});
```

buat file baru dengan nama `.env` (ingat ada titiknya) dan masukan kode berikut tetapi api key sesuai dengan masing-masing yang kalian tadi copy dari storyblok `STORYBLOK_ACCESS_TOKEN=apikey`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680232448065/afb80a00-274a-4e96-86fc-e720537ba040.png align="center")

Oke sampai sini berarti nuxt dan storyblok sudah terhubung 😎😎