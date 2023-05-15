---
title: "Membuat Web Next.js 13 and Sanity CMS (Bagian 1)"
datePublished: Mon May 15 2023 11:46:00 GMT+0000 (Coordinated Universal Time)
cuid: clhos487m001j09lk5o5qaghv
slug: membuat-web-nextjs-13-and-sanity-cms-bagian-1
tags: nextjs, sanity, tailwind-css

---

## Install Next JS

```bash
npx create-next-app@latest
```

```typescript
npx create-next-app@latest

What is your project named? ... permadi-sanity
Would you like to use TypeScript with this project? ... No / Yes
Would you like to use ESLint with this project? ... No / Yes
Would you like to use Tailwind CSS with this project? ... No / Yes
Would you like to use `src/` directory with this project? ... No / Yes
Use App Router (recommended)? ... No / Yes
Would you like to customize the default import alias? ... No / Yes
```

## Penggunaan **Turbopack**

Buka folder projek kalian, bukan file `package.json` dan edit sperti berikut:

```typescript
...
{
  "scripts": {
    "dev": "next dev --turbo",
    "build": "next build",
    "start": "next start",
    "lint": "next lint"
  }
}
...
```

## Install Sanity

Sign/Sign up ke [Saniti.io](https://www.sanity.io/), Buat Project Baru

![sanity dasboard](https://cdn.hashnode.com/res/hashnode/image/upload/v1684150956421/d83fa552-36a4-495a-a77f-bbf51154194b.png align="center")

Masih di folder projek kalian, buka terminal dan ketikan kode berikut:

```typescript
npm create sanity@latest
```

```typescript
Select project to use darkgrey-kangaroo [i21lds23]
Select dataset to use production
Would you like to add configuration files for a Sanity project in this Next.js folder? Yes
Do you want to use TypeScript? Yes
Would you like an embedded Sanity Studio? Yes
Would you like to use the Next.js app directory for routes? Yes
What route do you want to use for the Studio? /studio
Select project template to use Blog (schema)
Would you like to add the project ID and dataset to your .env file? Yes
```

Berikut tampilan ketika semua sudah di install

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684151068382/39e122cb-0700-4282-8def-6413a6c534af.png align="center")

## Install **next-sanity**

Untuk lebih jelasnya kalian bisa [dokumentasinya](https://www.npmjs.com/package/next-sanity#live-real-time-preview)

Buka terminal kalian pada projek tadi dan ketikan kode berikut

```css
npm install next-sanity @portabletext/react @sanity/image-url
```