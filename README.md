<p align="center"><img src="https://laravel.com/assets/img/components/logo-laravel.svg"></p>
le
<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/d/total.svg" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/license.svg" alt="License"></a>
</p>
# tutorial laravel
# untuk tutorial laravel bisa cek di
<pre>
  www.malasngoding.com
</pre>
# kode kode laravel

#kode laravel 2

Belajar Route dan View Pada Laravel – Selamat datang kembali di seri tutorial laravel lengkap dari dasar sampai mahir di www.malasngoding.com.

Sebelumnya kita telah belajar cara menginstall laravel. pada tutorial laravel part 1 sebelumnya juga sudah dijelaskan apa itu laravel, kenapa kita menggunakan laravel serta apa kelebihan laravel.

Maka pada tutorial laravel part 2 ini kita akan belajar route dan view pada laravel. yuk langsung simak penjelasan berikut ini.

Belajar Route dan View Pada Laravel
Route dan view adalah sesuatu yang paling dasar yang harus kita pahami di dalam menggunakan laravel sebelum kita melanjutkan tutorial laravel ke tahap yang selanjutnya. pada seri tutorial laravel lengkap ini akan dijelaskan menggunakan penjelasan yang insyallah mudah dipahami.

Wajib baca : Tutorial Laravel Part 1 : Cara Install Laravel

Route jika kita artikan ke dalam bahasa indonesia, maka artinya adalah rute atau jalur. jadi bisa kita ambil kesimpulannya bahwa route pada laravel adalah bagian yang mengatur rute pada project aplikasi yang kita bangun dengan laravel. contoh kecilnya kita bisa mengatur rute url pada aplikasi yang kita buat dengan laravel. misalnya kita membuat route “blog”. maka kita bisa memerintahkan untuk membuka view, menjalankan controller dan lain-lain pada saat route blog di akses. Bingung ? tenang, jika sudah masuk ke contoh kasusnya pasti teman-teman lebih bisa memahaminya.

Oke kita masuk ke penjelasan View, jika teman-teman sudah pernah belajar Codeigniter di www.malasngoding.com, tentu teman-teman sudah familiar dengan yang nama nya View dalam konsep MVC. Sama seperti pada framework PHP lainnya yang menggunakan konsep MVC, View bertugas untuk menangani atau mengurus bagian tampilan.

Jadi segala sesuatu yang akan tampil pada user interface, akan kita buat pada view. misalnya menampilkan data dan lain-lain.

Tutorial Belajar Route dan View Pada Laravel
Setelah membaca sedikit penjelasan di bagian atas tadi, kita akan langsung masuk ke contoh,

Coba lihat pada tampilan awal project laravel yang sudah berhasil kita install sebelumnya.

Belajar Route dan View Pada Laravel
Belajar Route dan View Pada Laravel

Tampilan awal project laravel ini berada pada view yang bernama welcome.blade.php. letaknya ada di dalam folder resources.

view welcome.blade.php tersebut diperintahkan secara default untuk tampil pada route web.php yang terletak dalam folder routes.

Coba buka file web.php dalam folder routes, seperti gambar berikut.

tutorial route dan view laravel
tutorial route dan view laravel

Di sana kita menjumpai syntax berikut
<pre>
Route::get('/', function () {
    return view('welcome');
});
</pre>
yang tujuannya adalah pada saat direktori awal ( / ) project dijalankan, maka akan menampilkan atau me-return view welcome (welcome.blade.php).

Kita tidak perlu menuliskan ekstensi .blade.php, kita cukup menulisakan nama view nya saja. seperti pada contoh di atas, cukup menuliskan “welcome” untuk menampilkan view welcome.blade.php.

dan isi dari view welcome.blade.php adalah tampilan awal yang kita lihat pada gambar pertama di atas.

Teman-teman jangan menghiraukan dulu ekstensi .blade.php nya. ini adalah sistem templating dari laravel. dan kita akan mempelajari nya pada tutorial selanjutnya, agar materi belajar laravel kita lebih terstruktur dan terarah.jadi teman-teman yang baru belajar tidak kebingungan dengan banyak nya istilah-istilah baru yang dijumpai.

Sekarang buka view welcome.blade.php nya dan kita akan mencoba merubah sedikit, untuk membuktikan benar atau tidak bahwa file view welcome.blade.php yang di tampilkan.

Kita akan mencoba merubah pada bagian tulisan “Laravel” menjadi “Malas Ngoding”.

Tutorial Laravel Lengkap Dari Dasar
Tutorial Laravel Lengkap Dari Dasar

Save, dan reload/refresh web browsernya.

http://localhost:8000

Tutorial laravel untuk pemula
Tutorial laravel untuk pemula

Nah, tulisan yang awalnya “Laravel”, telah berubah menjadi “Malas Ngoding”.

Membuat Route Baru Laravel
Untuk memperbanyak contoh, sekarang kita akan membuat route baru.

tulis syntax berikut ini di bawah route sebelumnya, selain me-return view, kita juga bisa me-return string.

belajar_laravel/routes/web.php
<pre>
Route::get('halo', function () {
	return "Halo, Selamat datang di tutorial laravel www.malasngoding.com";
});
</pre>
membuat route laravel
membuat route laravel

sekarang coba kita jalankan route halo nya. dengan mengakses http://localhost:8000/halo.

Tutorial route laravel
Tutorial route laravel

Seperti yang teman-teman lihat pada gambar di atas, maka akan tampil string “Halo, Selamat datang di tutorial laravel www.malasngoding.com”, sesuai dengan yang kita perintahkan jika route halo di jalankan.

Selanjutnya kita akan belajar membuat route baru lagi untuk menampikan view baru.

Buat route baru lagi di bawah route halo. di sini kita akan mencoba membuat route “blog”.

belajar_laravel/routes/web.php
<pre>
Route::get('blog', function () {
	return view('blog');
});
</pre>
Sehingga isi full file route web.php nya akan seperti berikut.

<pre>
<?php
 
/*
|--------------------------------------------------------------------------
| Web Routes
|--------------------------------------------------------------------------
|
| Here is where you can register web routes for your application. These
| routes are loaded by the RouteServiceProvider within a group which
| contains the "web" middleware group. Now create something great!
|
*/
</pre>
 <pre>
Route::get('/', function () {
	return view('welcome');
});
 </pre>
 <pre>
Route::get('halo', function () {
	return "Halo, Selamat datang di tutorial laravel www.malasngoding.com";
});
 </pre>
 <pre>
Route::get('blog', function () {
	return view('blog');
});
</pre>
pada route blog kita mencoba menampilkan atau memanggil view blog. jadi sekarang kita buat view baru dengan nama blog.blade.php dalam folder views.

belajar_laravel/resources/views/blog.blade.php

<pre>
<!DOCTYPE html>
<html>
<head>
	<title>Tutorial Laravel - www.malasngoding.com</title>
</head>
<body>
	<h3>www.malasngoding.com</h3>
	<p>Seri Tutorial Laravel Lengkap Dari Dasar</p>
	<p>Ini adalah view blog. ada di route blog.</p>
</body>
</html>
</pre>
Sekarang coba akses route “blog” dengan alamat http://localhost:8000/blog.

tutorial laravel lengkap

