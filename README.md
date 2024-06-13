<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

<b>Requirement/Persyaratan</b>
---
> #### Php versi 8
>> - Cara menginstal php dalam bahasa indonesia : <a href="https://youtu.be/Uw3ZGIMvIdA?si=mBVZ-lBnoCilASzo">install php
>> - Cara menginstal php dalam bahasa inggris : <a href="https://youtu.be/MPRLUd8Pmyo?si=FqN54nVr4duH4Keg"> install php
-----
> #### Laravel versi 10.2.5
>> - cara menginstal laravel yang versi yang sama : 
>>   ```
>>   composer create-project laravel/laravel=v10.2.5 belajar-laravel-eloquent
>>   ```
---
> #### Laravel breeze
> > - setelah kita membuat project laravel kalian bisa lanjut untuk menginstall laravel breeze :
>>  ```
> > composer require laravel/breeze=versi -dev
> > ```
> > - jika kalian ingin melihat versi laravel/breeze kalian bisa  <a href="https://packagist.org/packages/laravel/breeze"> lihat di sini
---
<b>Cara menjalankannya</b>
---
> - langkah pertaman : lakukan git clone seperti di bawah ini :
```
 git clone https://github.com/Usmanganteng/belajar-laravel-security.git
```
> - langkah kedua : copy file .env.example dan ganti namanya menjadi .env seperti perintah di bawah ini ketika sudah kalian lakukan, kalian bisa tulis perintah setelah nya yaitu composer install 
```
 cp .env.example .env
 composer install
```
> - langkah ketiga : lakukan perintah seperti di bawah ini :
```
php artisan key:generate
```
> - langkah keempat : kalian bisa buat database dengan nama belajar_laravel_database lalu ganti nama database yang ada di .env dengan nama database yang sudah kalian buat lalu lakukan perintah :
```
php artisan migrate
```
> - langkah terakhir : kailan bisa langsung jalankan atau run dengan menulilskan perintah :
```
php artisan serve
```
---
<b>Materi/Bahasan</b>
---
> #### Apa itu laravel sevurity
> - Laravel security adalah serangkaian praktik untuk melindungi aplikasi web yang dibangun dengan framework Laravel dari serangan-serangan seperti SQL injection, cross-site scripting (XSS), dan lainnya. Ini mencakup validasi input, perlindungan CSRF, XSS, penggunaan ORM untuk mencegah SQL injection, otentikasi yang kuat, pengaturan header keamanan HTTP, dan pembaruan reguler.
---
> #### Apa itu laravel breeze
> - Laravel Breeze adalah paket resmi Laravel untuk otentikasi pengguna yang cepat dan mudah. Ini menyediakan fitur-fitur dasar seperti login, pendaftaran, dan reset kata sandi dengan integrasi Tailwind CSS. Cocok untuk proyek sederhana atau menengah yang membutuhkan otentikasi pengguna yang cepat.
---
> #### authentication
> - authentication adalah proses verifikasi identitas pengguna untuk memberikan akses ke sistem atau aplikasi tertentu. Ini melibatkan validasi kredensial yang dimiliki pengguna, seperti nama pengguna dan kata sandi, untuk memastikan bahwa mereka adalah orang yang sebenarnya yang memiliki hak akses yang diberikan. Otentikasi biasanya merupakan langkah pertama dalam proses keamanan untuk melindungi data dan sumber daya yang sensitif. Dalam konteks pengembangan web, otentikasi sering digunakan untuk mengamankan akses ke halaman web atau API, memastikan bahwa hanya pengguna yang memiliki hak akses yang benar yang dapat menggunakan fitur-fitur tertentu dari aplikasi tersebut.
---
> #### hash
> - Hashing adalah proses mengonversi data menjadi nilai hash, string karakter panjang tetap yang mewakili data asli. Nilai hash tidak dapat dikembalikan ke data aslinya, dan bahkan perubahan kecil pada data input menghasilkan hash yang sepenuhnya berbeda. Ini digunakan dalam keamanan, seperti penyimpanan dan verifikasi kata sandi.
---
> #### guard
> - Guard dalam Laravel adalah bagian dari sistem otentikasi yang menangani cara pengguna diautentikasi dan mengakses sumber daya terproteksi dalam aplikasi web. Anda dapat memiliki beberapa guard dengan konfigurasi otentikasi yang berbeda, seperti guard "web" untuk otentikasi melalui sesi HTTP dan guard "api" untuk otentikasi melalui token API.
---
> #### Gate
> - Gate dalam konteks Laravel adalah bagian dari sistem otentikasi yang bertanggung jawab untuk mengatur akses pengguna ke berbagai sumber daya atau tindakan dalam aplikasi. Ini memungkinkan Anda untuk menentukan kebijakan akses yang kompleks berdasarkan peran atau hak pengguna.
> - Dengan menggunakan Gate, Anda dapat menentukan logika yang harus dipenuhi untuk mengizinkan pengguna untuk melakukan tindakan tertentu atau mengakses sumber daya tertentu. Misalnya, Anda dapat memeriksa peran pengguna, kepemilikan sumber daya, atau kriteria lainnya sebelum memberikan izin kepada pengguna untuk melanjutkan.
> - Penggunaan Gate seringkali terlihat dalam laravel dengan menggunakan metode `authorize()` pada objek request dalam kontroler atau dalam tampilan untuk menentukan apakah pengguna memiliki izin untuk menampilkan atau melakukan tindakan tertentu.
> - Ini memungkinkan Anda untuk menerapkan kebijakan akses dengan lebih fleksibel dan terstruktur, memastikan bahwa pengguna hanya memiliki akses ke fungsi atau data yang sesuai dengan peran dan izin mereka.
---
> #### policy
> - Berikut adalah contoh sintaks penggunaan Policy dalam Laravel:
> - Membuat Policy:Anda dapat membuat Policy di Laravel dengan menggunakan perintah artisan `make:policy`. Misalnya, untuk membuat Policy untuk model `Post`, Anda dapat menjalankan perintah berikut:
>>```
>>  php artisan make:policy PostPolicy --model=Post
>>```
>> - Ini akan membuat file `PostPolicy.php` di direktori `app/Policies` yang berisi logika otorisasi.
> - Menentukan Kebijakan:Anda dapat menentukan logika otorisasi dalam method-method yang didefinisikan dalam policy. Misalnya:
>> ```
>> public function view(User $user, Post $post)
>>{
>>    return $user->id === $post->user_id;
>>}
>>```
>> - Ini menentukan bahwa pengguna dapat melihat post jika mereka adalah pemiliknya.
> - Menggunakan Policy di Kontroler:Anda kemudian dapat menggunakan policy ini dalam kontroler Anda untuk mengotorisasi tindakan tertentu. Misalnya:
>> ```
>> public function show(Post $post)
>>{
>>    $this->authorize('view', $post);
>>    return view('post.show', compact('post'));
>>}
>>```
>> - Metode `authorize()` akan memeriksa izin menggunakan policy yang sesuai.
---
> #### authorizable
> - `Authorizable` adalah kontrak yang digunakan pada model pengguna di Laravel untuk memungkinkan pengecekan izin. Ini memungkinkan pengguna untuk menggunakan metode `can()` dan `cant()` untuk mengotorisasi tindakan.
> - Contoh sintaks:
> ```
> if ($user->can('view', $post)) {
>    // Lakukan sesuatu jika pengguna memiliki izin untuk melihat post
>} else {
>    // Lakukan sesuatu jika pengguna tidak memiliki izin untuk melihat post
>}
>```
> - Ini memungkinkan pengguna untuk mengontrol akses ke fitur-fitur tertentu dalam aplikasi dengan mudah.
---
> #### before after
> - Dalam Laravel, Anda dapat menggunakan metode `before` dan `after` dalam policy untuk menentukan logika otorisasi yang harus dievaluasi sebelum atau setelah metode otorisasi lainnya dipanggil. Ini memungkinkan Anda untuk memberikan aturan global sebelum atau setelah evaluasi otorisasi tertentu dilakukan.
> - Contoh sintaks:
> ```
> class PostPolicy
>{
>    public function before($user, $ability)
>    {
>        if ($user->isAdmin()) {
>            return true; // Izinkan semua akses jika pengguna adalah admin
>        }
>    }
>
>   public function view(User $user, Post $post)
>    {
>        return $user->id === $post->user_id;
>    }
>}
>```
> - Dalam contoh ini, metode `before`digunakan untuk memberikan izin global kepada admin untuk mengakses semua tindakan, dan metode `view` digunakan untuk menentukan izin khusus untuk melihat post. Jika metode `before` mengembalikan `true`, metode `view` tidak akan dievaluasi karena akses akan diberikan secara global. Jika metode `before` tidak mengembalikan `true`, maka metode `view` akan dievaluasi untuk menentukan izin spesifik untuk tindakan tersebut.
---
> #### guest access
> - Akses tamu dalam Laravel memungkinkan pengguna yang belum login untuk mengakses halaman atau fitur tertentu. Ini diterapkan dengan menggunakan middleware `guest` pada rute-rute yang ingin dibatasi hanya untuk pengguna yang belum masuk. Misalnya:
> ```
> Route::middleware('guest')->group(function () {
>    Route::get('/login', 'Auth\LoginController@showLoginForm')->name('login');
>    Route::post('/login', 'Auth\LoginController@login');
>});
>```
> - Dengan ini, halaman login hanya dapat diakses oleh pengguna yang belum login.
> #### encryption
> - Enkripsi adalah proses mengubah data menjadi format yang tidak dapat dibaca atau dimengerti tanpa memiliki kunci atau metode dekripsi yang sesuai. Ini adalah teknik yang umum digunakan dalam keamanan informasi untuk melindungi data sensitif dari akses yang tidak sah.
> - Dalam konteks pengembangan perangkat lunak, enkripsi sering digunakan untuk melindungi data yang disimpan di database atau data yang dikirimkan melalui jaringan. Misalnya, kata sandi pengguna sering disimpan dalam format terenkripsi di database untuk menghindari akses yang tidak sah.
> - Laravel menyediakan dukungan bawaan untuk enkripsi melalui fitur "Encryption" yang memanfaatkan OpenSSL, yang memudahkan pengembang untuk mengenkripsi dan mendekripsi data dengan mudah.
> - Contoh penggunaan enkripsi dalam Laravel:
> ```
> use Illuminate\Support\Facades\Crypt;
>
>// Mengenkripsi data
>$encrypted = Crypt::encryptString('Hello, world!');
>
>// Mendekripsi data
>$decrypted = Crypt::decryptString($encrypted);
>```
> - Dengan menggunakan enkripsi, Anda dapat meningkatkan keamanan data dalam aplikasi Anda, memastikan bahwa hanya pihak yang sah yang dapat mengakses informasi sensitif.
---
<b> Terima Kasih</b>
---
