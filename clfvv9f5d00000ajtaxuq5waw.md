---
title: "Install Nuxt.js 3 pada windows"
seoTitle: "Tutorial Membuat Website dengan Nuxt.js 3 dan Storyblok"
seoDescription: "Tutorial Membuat Website dengan Nuxt.js 3 dan Storyblok"
datePublished: Fri Mar 31 2023 01:29:00 GMT+0000 (Coordinated Universal Time)
cuid: clfvv9f5d00000ajtaxuq5waw
slug: install-nuxtjs-3-pada-windows
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1680229858763/07e3ad02-6b57-46f8-bb09-f530a7aac305.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1680229869984/21e4804f-17d4-4dec-a423-527ae784f479.png
tags: website, jamstack, nuxt, storyblok, nuxt3

---

Sebelumnya, saya anggap kalian sudah menginstall beberapa environment yang di perlukan dalam mengintal nuxt yaa😎, bisa di baca di website resminya =&gt; [**Intall Nuxt**](https://nuxt.com/docs/getting-started/installation)

Buka terminal (jika Anda menggunakan Visual Studio Code, Anda dapat membuka terminal terintegrasi) dan menggunakan perintah berikut untuk membuat proyek nuxt.js 3 baru:

```bash
npx nuxi init <nama-projek>
```

Kalau saya sendiri, memberi nama projek saya `belajar-nuxt3` , tunggu sampai selesai sehingga seperti berikut kalau sudah selesai:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680224739680/e2798411-bcc0-45a7-965b-98e71856a9f3.png align="center")

Buka folder proyek Anda di Visual Studio Code

```bash
cd belajar-nuxt3
```

```bash
code .
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680224926376/534bdf6c-6f92-486c-a3e7-e28c228279bb.png align="center")

Maka VS Code kalian akan terbuka, tampilan awal project kalian akan seperti berikut

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680225029050/c876e3c3-8358-465b-860f-fc50e4557285.png align="center")

Sekarang tutup cmd kalian, dan kita akan mengguanakan terminal yang ada pada VS Code, tetntunya yang sudah di integrasikan dengan CMD Windows.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680225110624/0e715338-5296-47e5-818e-93487543c089.png align="center")

**Install dependensi,** sebeneranya ada tiga cara yang di sediakan. Saya mengguakan cara yang menggunakan `npm` untuk menginstall nya

```bash
npm install
```

Tunggu sampai selesai, (lamanya install tergantung kokesi internet) maka tampilanya akan seperti ini

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680225626375/e89b9e22-2d07-4306-8899-592568e4792c.png align="center")

Selanjutnya kita test apakah sudah bisa berjalan belum dengan mengetikan kode berikut pada terminal:

```bash
npm run dev -- -o
```

Jika browser kalian terbuka dan muncul seperti gambar di bawah berarti sudah berhasil 😎😎

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680225959486/63e86610-e74b-42ba-8371-ca529cd3470a.png align="center")