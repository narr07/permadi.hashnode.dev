---
title: "Install Module (Tailwind css) pada Nuxt.js 3"
seoTitle: "Install Tailwind css pada Nuxt.js 3"
seoDescription: "Install Tailwind css pada Nuxt.js 3"
datePublished: Fri Mar 31 2023 02:04:51 GMT+0000 (Coordinated Universal Time)
cuid: clfvwjjeu000509l4a3cegk46
slug: install-module-tailwind-css-pada-nuxtjs-3
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1680229764678/71dd9cb6-26b2-4333-8c57-3931ffeadb64.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1680229562449/59046fba-2f0d-4d66-a320-6e32e7351794.png
tags: storyblok, nuxtjs, tailwind-css, nuxt3

---

## **Nuxt Tailwind**

Website module tailwind nuxt js =&gt; [**Nuxt Tailwind**](https://tailwindcss.nuxtjs.org/)

Website resmi [Tailwind CSS](https://tailwindcss.com/)

## Install dependensi Tailwind css

```bash
npm install -D @nuxtjs/tailwindcss
```

Setelelah selesai, buka file `nuxt.config.ts` dan edit sehingga jadi seperti iniexport

```typescript
export default defineNuxtConfig({
  modules: [
    "@nuxtjs/tailwindcss",
    ],
  tailwindcss: {
    cssPath: "~/assets/css/tailwind.css",
    configPath: "tailwind.config.js",
    viewer: true,
  },
});
```

## Membuat file tailwind config

Ketikan code berikut pada terminal sehingga akan menggenerate file `tailwind.config.js`

```bash
npx tailwindcss init
```

Kemudian tambahkan code berikut pada file `tailwind.config.js`

```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./components/**/*.{js,vue,ts}",
    "./layouts/**/*.vue",
    "./pages/**/*.vue",
    "./plugins/**/*.{js,ts}",
    "./nuxt.config.{js,ts}",
    "./app.vue",
    "./Error.{js,ts,vue}",
    "./storyblok/**/*.{vue,js}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

## Memmbuat file css Tailwind

Buat folder baru bernama `assets`, lalu didalamnya buat folder lagi dengan nama `css` dan buat file dengan nama `tailwind.css`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680227403596/e312f5c1-4a91-4328-87b0-696e497879c9.png align="center")

Ketikan kode berikut pada file `tailwind.css`

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

oke sudah selesai untuk installasi tailwind css pada nuxt 3,

## Kenapa Menggunakan tailwind css?

Tailwind CSS adalah kerangka kerja CSS yang berbasis utilitas untuk membuat menarik tampilan dari web menjadi lenih fleksibel. Ada beberapa manfaat menggunakan Tailwind CSS:

1. Menulis lebih sedikit CSS khusus: Dengan Tailwind, Anda dapat menata elemen dengan menerapkan kelas yang sudah ada sebelumnya langsung di HTML.
    
2. Menyimpan file CSS kecil: Dengan menggunakan utilitas seperti flexbox dan utilitas padding Tailwind, sebagian besar gaya dapat digunakan kembali sehingga jarang perlu menulis CSS baru.
    
3. Tidak perlu menemukan nama kelas: Saat menggunakan Tailwind, Anda memilih kelas dari sistem desain yang telah ditentukan sebelumnya. Itu berarti Anda tidak perlu bersusah payah memilih nama kelas “sempurna” untuk gaya dan komponen tertentu.
    
4. Dapat membuat perubahan yang lebih aman.