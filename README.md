# PrakPemin-A_Tugas3
1. Lakukan pembuatan folder dengan nama express-mongodb dan masuk ke dalam
folder tersebut lalu buka melalui text editor masing-masing
2. Lakukan npm init untuk mengenerate file package.json dengan menggunakan
command npm init -y
![Screenshot 2023-09-27 023206](https://github.com/askenas/PrakPemin-A_Tugas3/assets/134838656/2648f341-3448-4e70-8091-8fbbb4d2e9b7)
3. Lakukan instalasi express, mongoose, dan dotenv dengan menggunakan command
npm i express mongoose dotenv
![Screenshot 2023-09-27 023335](https://github.com/askenas/PrakPemin-A_Tugas3/assets/134838656/c28b9ef1-64ef-4b49-af59-2a55bd3d9281)
1. Buatlah file index.js pada root folder dan masukkan kode di bawah ini
   ![Screenshot 2023-09-27 032044](https://github.com/askenas/PrakPemin-A_Tugas3/assets/134838656/d12418ba-3445-461f-b24a-3ac411b08659)
Setelah itu coba jalankan aplikasi dengan command node index.js
2. Lakukan pembuatan file .env dan masukkan baris berikut
   ![Screenshot 2023-09-27 032349](https://github.com/askenas/PrakPemin-A_Tugas3/assets/134838656/3ac0fca9-950e-4c7d-ba2e-321d56045356)
Setelah itu ubahlah kode pada listening port menjadi berikut dan coba jalankan aplikasi
kembali
![Screenshot 2023-09-27 032536](https://github.com/askenas/PrakPemin-A_Tugas3/assets/134838656/c1800dbd-6851-4452-b4f4-3a4d5af85941)
3. Copy connection string yang terdapat pada compas atau atlas dan paste kan pada
.env seperti berikut
4. Tambahkan baris kode berikut pada file index.js
   require('dotenv').config();
const express = require('express');
const mongoose = require('mongoose');
mongoose.connect(process.env.MONGO_URI);
const db = mongoose.connection;
db.on('error', (error) => {
console.log(error);
});
db.once('connected', () => {
console.log('Mongo connected');
})
1. Lakukan pembuatan direktori routes di tingkat yang sama dengan index.js
![Screenshot 2023-09-27 032626](https://github.com/askenas/PrakPemin-A_Tugas3/assets/134838656/4a56be3d-5d1a-46db-b322-652128953c65)
2. Buatlah file book.route.js di dalamnya
3. Tambahkan baris kode berikut untuk fungsi getAllBooks
![Screenshot 2023-09-27 032712](https://github.com/askenas/PrakPemin-A_Tugas3/assets/134838656/2f19e0aa-c2e8-4c65-97f8-2f35b8478277)
4. Lakukan hal yang sama untuk getOneBook, createBook, updateBook, dan
deleteBook
![Screenshot 2023-09-27 033015](https://github.com/askenas/PrakPemin-A_Tugas3/assets/134838656/346d8bed-8ade-4d5f-9cd4-0e7777b59d6a)
4. Lakukan hal yang sama untuk getOneBook, createBook, updateBook, dan
deleteBook
![Screenshot 2023-09-27 042246](https://github.com/askenas/PrakPemin-A_Tugas3/assets/134838656/a4978da9-2c00-41c1-aa51-c37ba0812af1)
5. Lakukan import book.route.js pada file index.js dan tambahkan baris kode berikut

1. Lakukan pembuatan direktori controllers di tingkat yang sama dengan index.js
   ![Screenshot 2023-09-27 041957](https://github.com/askenas/PrakPemin-A_Tugas3/assets/134838656/8a27ec59-bbc0-483f-bf88-c24539aea8aa)
2. Buatlah file book.controller.js di dalamnya
3. Salin baris kode dari routes untuk fungsi getAllBooks
4. Lakukan hal yang sama untuk getOneBook, createBook, updateBook, dan
deleteBook
![Uploading Screenshot 2023-09-27 042246.png…]()
5. Lakukan import book.controller.js pada file book.route.js
![Screenshot 2023-09-27 042340](https://github.com/askenas/PrakPemin-A_Tugas3/assets/134838656/f362af74-2b6f-4061-85cf-21a48fac1d49)
6. Lakukan perubahan pada fungsi agar dapat memanggil fungsi dari book.controller.js
![Screenshot 2023-09-27 042452](https://github.com/askenas/PrakPemin-A_Tugas3/assets/134838656/011da78f-018d-488a-847a-ede0f884b214)
7. Lakukan pengujian kembali, pastikan response tetap sama

1. Lakukan pembuatan direktori models di tingkat yang sama dengan index.js
![Screenshot 2023-09-27 042558](https://github.com/askenas/PrakPemin-A_Tugas3/assets/134838656/4ffb1d69-27c0-4216-b022-f76b520935e0)
2. Buatlah file book.model.js di dalamnya
3. Tambahkan baris kode berikut sesuai dengan tabel di atas
![Screenshot 2023-09-27 042647](https://github.com/askenas/PrakPemin-A_Tugas3/assets/134838656/6cb93e64-76f8-4649-b7d2-13742f3cb1ff)
1. Hapus semua data pada collection books



