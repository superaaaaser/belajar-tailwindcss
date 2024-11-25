# Istall Tailwindcss

Tailwind CSS bekerja dengan memindai semua file HTML, komponen JavaScript, dan template lainnya untuk mencari nama kelas, menghasilkan gaya yang sesuai, lalu menulisnya ke file CSS statis.

## Menggunakan CLI

- Instal `tailwindcss` melalui npm, dan membuat file `tailwind.config.js`.

```sh
npm install -D tailwindcss
npx tailwindcss init
```

- Konfigurasi template path

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

- Tambahkan `@tailwind` ke CSS utama kalian

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

- Jalankan CLI untuk memindai file template kalian untuk mencari kelas CSS

```sh
npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
```

- Tambahkan CSS yang sudah di kompile di dalam `<head>` dan bisa memulai class tailwind di dalam konten kalian

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link href="./output.css" rel="stylesheet" />
  </head>
  <body>
    <h1 class="text-3xl font-bold underline">Hello world!</h1>
  </body>
</html>
```

## Menggunakan CDN

- Tambahkan tag skrip Play CDN ke `<head>` file HTML kalian, dan mulai gunakan kelas utilitas Tailwind untuk menata gaya konten kalian.

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <script src="https://cdn.tailwindcss.com"></script>
  </head>
  <body>
    <h1 class="text-3xl font-bold underline">Hello world!</h1>
  </body>
</html>
```
