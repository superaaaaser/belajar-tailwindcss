# Istall Tailwindcss

Tailwind CSS bekerja dengan memindai semua file HTML, komponen JavaScript, dan template lainnya untuk mencari nama kelas, menghasilkan gaya yang sesuai, lalu menulisnya ke file CSS statis.

## Menggunakan CLI

- Instal `tailwindcss` melalui npm, dan membuat file `tailwind.config.js`.

```sh
npm install -D tailwindcss
```

```sh
npx tailwindcss init
```

- Konfigurasi template path

```json
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
