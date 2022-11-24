# Tugas 7, 8 dan 9 PBP - Rebeka Alma 2106653060 - PBP E

## Tugas 7

## Jelaskan apa yang dimaksud dengan stateless widget dan stateful widget dan jelaskan perbedaan dari keduanya.
Stateful Widget merupakan widget yang dinamis atau dapat berubah. Berbanding terbalik dengan stateless, stateful widget dapat mengupdate tampilan, merubah warna, menambah jumlah baris dll. Jadi dapat disimpulkan bahwa apapun widget yang dapat berubah maka itulah stateful widget.
Stateless widget adalah widget yang tidak merubah atau immutable. Penampilan serta propertinya tidak berubah selama widget itu masih ada. Widget ini tidak bergantung pada perubahan data atau perilaku app. Dalam satu kata, stateless widget itu STATIK. Sebagai contoh adalah Text, Icon, dan RaisedButton.


## Sebutkan widget apa saja yang kamu pakai di proyek kali ini dan jelaskan fungsinya.
**Text** : Untuk menampilkan text


**FloatingActionButton** : Untuk membuat button yang berada di index paling dekat dengan surface


**Row** : membuat element dalam 1 row


**Colum** : membuat element didalamnya memiliki gap 1 column


**Padding** : Untuk sizing element


**Center** : Menaruh element container ke tengah halaman


**Icon** : Memberi icon ke sebuah elemen


## Apa fungsi dari setState()? Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut.
Setstate akan memberikan informasi ke system ketika sebuah variable berubah dan system akan melakukan render ke part yang berubah. Setstate perlu digunakan ketika ada perubahan yang ingin ditampilkan di UI.

Variabel yang terdampak tentu _counter itu sendiri karena yang mengalami perubahan adalah counter. Dari counter, akan berdampak ke text yang sudah dibuat yaitu ganjil atau genap.

## Jelaskan perbedaan antara const dengan final.
final merupakan keyword yang digunakan untuk hardcode nilai yang tidak akan diubah di masa depan. Disarankan untuk menggunakan final jika kita tidak tahu nilai tersebut di compile time.

keyword const mirip seperti final namun variabel dengan keyword const itu KONSTANT di compile-time saja. const akan membuat object tersebut frozen dan immutable.


## Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas.
- Membuat flutter app dengan perintah flutter create counter_7
- Tambah widget row pada floatingActionButton
- Bikin button untuk decrement
- Buat function untuk decrement counter
- Panggil function decrement ketika button decrement dipencet
- Buat conditional widget text untuk tiap counter yang sedang ditunjuk
- Buat conditional dimana button decrement hanya bisa terlihat jika _counter > 0



## Tugas 8


## Jelaskan perbedaan Navigator.push dan Navigator.pushReplacement


Push menambahkan satu route/page ke top of stack Navigator, sedangkan pushReplacement menggantikan page tersebut dengan yang baru.


## Sebutkan widget apa saja yang kamu pakai di proyek kali ini dan jelaskan fungsinya


- drawer: drawer/hamburger
- DropDown: Widget interaktif yang bisa memiliki pilihan drop-down
- Padding: Widget styling, untuk padding sebuah widget lain
- Card: Layout widget, untuk menata isi-isinya (child)


dsb


## Sebutkan jenis-jenis event yang ada pada Flutter 


- onPressed, tombol dipencet
- onChanged, untuk form field ketika data yang diubah
- onSaved, ketika form di-save
- onLongPress, ketika tombol ditahan


## Jelaskan bagaimana cara kerja Navigator dalam "mengganti" halaman dari aplikasi Flutter


Navigator merupakan stack dimana Top of Stack (TOS) merupakan halaman yang ditampilkan. Navigator mengganti halaman dengan mengganti top of stack (push / pushReplacement) sehingga aplikasi menampilkan halaman yang baru itu. Jika dia pop maka dia 'return' ke halaman sebelumnya (yang sudah pernah dibuka, karena ada di layer bawah stack)


## Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas


- Membuat file drawer yang berisi route untuk masing masing class untuk counter, showBudget, atau form.


- Membuat form dengan validation dan state


- File data akan diset untuk memiliki fungsi untuk menambahkan obj paada atribut classnya untuk menampung data yang diinput.


- Membuat showBudget dan melakukan loop dari ListBudget.len untuk diloop dan ditampilan sebagaimananya dengan Card view


## Tugas 9

## Apakah bisa kita melakukan pengambilan data JSON tanpa membuat model terlebih dahulu? Jika iya, apakah hal tersebut lebih baik daripada membuat model sebelum melakukan pengambilan data JSON?


Bisa, membuat template sebelum mengambil data JSON lebih baik karena dapat merepresentasikan data dan struktur data apa yang akan diterima ketika data JSON diambil agar sesuai dengan respon. Jika tidak membuat template, Anda perlu menyesuaikan data yang diterima dan tipe data secara manual saat kita menerima data respons.

## Sebutkan widget apa saja yang kamu pakai di proyek kali ini dan jelaskan fungsinya


- Widget ElevatedButton adalah tombol yang dapat diberikan tulisan dengan warna latar belakang pada tombol. Digunakan sebagai tombol kembali pada halaman detail.


- Widget flexibel yang mengontrol baris, kolom, atau widget fleksibel. Digunakan saat validasi string ditampilkan pada halaman data sehingga tidak meluap.


- Widget RichText yang menampilkan teks dalam berbagai style. Teks yang ditampilkan menggunakan objek TextSpan.


- Widget TextSpan yang dapat memformat teks. Dapat memiliki turunan widget untuk menentukan style turunan widget. Digunakan saat menampilkan teks pada halaman detail.


## Jelaskan mekanisme pengambilan data dari json hingga dapat ditampilkan pada Flutter


- Pertama dependensi HTTP. Flutter untuk melakukan permintaan HTTP seperti GET.


- Buat template class yang cocok dengan informasi respons yang akan diambil.


- Melakukan http GET request untuk mengambil data JSON.


- Mengkoversikan data JSON yang diambil ke template class yang sudah dibuat.


- Menampilkan data dengan FutureBuilder.

## Implementasi


Pada tugas ini, kita akan mengintegrasikan mywatchlist yang sudah  ada pada tugas 3 sebelumnya ke Flutter. Pengerjaan tugas ini akan menggunakan app yang sama dengan tugas Flutter sebelumnya.


 - Pertama, menambahkan tombol navigasi pada drawer/hamburger untuk ke halaman mywatchlist.


- Membuat satu file dart yang berisi model mywatchlist.


- Menambahkan halaman mywatchlist yang berisi semua watch list yang ada pada endpoint JSON di Django yang telah kamu deploy ke Heroku sebelumnya (Tugas 3). Pada bagian ini, kamu cukup menampilkan judul dari setiap mywatchlist yang ada.

- Membuat navigasi dari setiap judul watch list ke halaman detail Mywatchlist

- Menambahkan halaman detail untuk setiap mywatchlist yang ada pada daftar tersebut. Halaman ini menampilkan judul, release date, rating, review, dan status (sudah ditonton/belum).

- Menambahkan tombol untuk kembali ke daftar mywatchlist
