# Data Struktur Array
Array adalah Suatu struktur data yang dapat menyimpan banyak nilai dalam sebuah variabel.
Pada kebanyakan bahasa pemrograman, array harus berisi kumpulan data yang tipe data sejenis. Pada pemrogragraman PHP, dalam sebuah variabel array dapat memiliki tipe data lebih dari satu. 
Array adalah suatu variabel yang terdiri dari sekumpulan data dimana data-data tersebut mempunyai tipe data yang sama. Setiap data disimpan dalam alamat memori yang berbeda-beda dan disebut dengan elemen array. Setiap elemen mempunyai nilai indek sesuai dengan urutannya. 
Tempat menyimpanya sekumpulan data yang memilki tipe data yang sama dan mempunyai 2 indek(baris dan kolom). Array dideklarasikan dengan tanda [ ] atau (bracket).
#### Bentuk Umum dari tipe data array adalah :

tipe_data nama_array[jumlah_elemen]. Jika ingin mendeklarasikan sebuah array dengan tipe data integer dengan nama a dan jumlah elemen array nya 10 maka kodenya adalah : **int a[10]**

## Array pada PHP
**Fungsi print_r pada PHP**

Dalam menampilkan isi suatu variabel array atau object,biasanya menggunakan fungsi print_r() dan fungsi var_dump().Jika menggunakan fungsi print_r() akan tampak lebih rapi.
* Contoh :
```php
$angka = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
print_r($angka); //Versi singkat
echo "<br /><br />";
echo "<pre>".print_r($angka, true)."</pre>";
```
* Contoh menggunakan var_dump() :
```php
$a = ["a", "b", "c"];
var_dump($a);
```

**Array Numeric pada php**

Array pada PHP dideklarasikan dengan cara:
```php
$nama = array();
atau
$nama = [];
```
* Contoh : 
```php
$nama[] = "Fandi";
$nama[] = "Hendra";
$nama[] = "Agus";
$nama[] = "Dedi";
array_push($nama, "Suryadi");
echo "<pre>".print_r($nama, true)."</pre>";
```
* Contoh Array yang sudah diisi :

```php
$pelajaran = ['Matematika', 'Kimia', 'Fisika', 'Biologi'];
$nilai = [100, 80, 75, 78];
for ($i=0; $i<=3; $i++) {
    echo "$i. Pelajaran $pelajaran[$i] nilainya $nilai[$i]<br />";
}
```
**Array String pada PHP**

Array string memiliki indeks berupa string. Pendeklarasian array string caranya sama dengan deklarasi array numerik: 
```php
$namas = array(); atau $angkas = [];
```
Sedangkan untuk menginisialisasi atau langsung mengisi array string, 
caranya:

```php
$nilai = ["Matematika"=>100, "Kimia"=>80, "Fisika"=>75, "Biologi"=>78];
    echo "<pre>".print_r($nilai,true)."</pre>";
```
dan hasilnya adalah :

nilai $nilai['Matematika'] adalah 100, $nilai["Kimia"] adalah 80, $nilai["Fisika"] adalah 75, dan nilai $nilai['Biologi'] adalah 78.

**Perulangan foreach pada PHP**

Foreach adalah struktur perulangan seperti for dan while, terkecuali foreach harus digabungkan dengan array atau objek. Perulangan foreach melakukan perulangan untuk setiap elemen di dalam array.
* Contoh penggunaannya :
```php
$nilai = ["Matematika"=>100, "Kimia"=>80, "Fisika"=>75, "Biologi"=>78];
foreach ($nilai as $key => $value) {
    echo "Rata-rata nilai $key adalah $value <br />";
}
```

**Fungsi-fungsi array pada PHP**

Beberapa fungsi yang sering dipakai antara lain: explode(), implode(), count(), in_array(), asort() dan arsort(), ksort dan krsort().

* Fungsi explode() adalah untuk mengubah satu string CSV (Comma Separated Value) menjadi array. 
* fungsi implode() sebaliknya menggabungkan semua elemen di dalam suatu array ke dalam satu string. 
* asort() mengurutkan suatu array, 
* arsort() mengurutkan juga tetapi dengan urutan kebalikan. 
* ksort() dan krsort() sama dengan asort() dan arsort(), hanya saja yang diurutkan adalah key dari array tersebut.

* Contoh :

```php
$nilais = ["Matematika"=>100, "Kimia"=>80, "Fisika"=>75, "Biologi"=>78];
$str = implode(", ", $nilais);
    echo $str;
$hobi = "Olahraga, Main game, Nonton, Makan, Nongkrong";
$hobis = explode(", ", $hobi);
    echo "<pre>".print_r($hobis, true)."</pre>";
asort($hobis);
    echo "Setelah sort:";
    echo "<pre>".print_r($hobis, true)."</pre>";
```
Fungsi count() menghasilkan jumlah elemen di dalam array, sedangkan in_array() untuk memeriksa apakah suatu nilai tertentu terdapat di dalam suatu array.


# Referensi 2 
[Array](https://ilmu-detil.blogspot.co.id/2016/06/pengertian-tipe-data-array-pada-php.html)

Array adalah Suatu struktur data yang dapat menyimpan banyak nilai dalam sebuah variabel.
Pada kebanyakan bahasa pemrograman, array harus berisi kumpulan data yang tipe data sejenis. Pada pemrograman PHP, dalam sebuah variabel array dapat memiliki tipe data lebih dari satu. 

Masing-masing nilai pada array disebut elemen, dan untuk mengakses elemen menggunakan index.
Index pada array dapat berupa numerik  yang disebut dengan index numerik dan bisa juga berupa label/nama yang biasa disebut dengan index associatif.
Index numerik pada sebuah array selalui dimulai dari 0, jadi jika ingin mengakses sebuah elemen, misal : elemen P berada pada index-0. Elemen I berada pada : index-6, dan index-21. Karakter kosong seperti pada index ke-5, index 17 juga dianggap sebagai elemen.

1. Inisialisasi Array

Untuk memberi nilai array (inisialisasi array) dapat dilakukan dengan cara sebagai berikut :

```php
$nama = ["Dono","Doni","Dina","Wati"];
```
Cara inisialisasi diatas membuat variabel $nama menjadi array berindeks numerik, dimana indexnya dimulai dengan angka 0.
Jika kita ingin membuat sebuah variabel array berindex associatif, maka indexnya harus berupa label seperti contoh dibawah ini :
```php
$nama = ["Dono"=>"08126767","Doni"=>"08116762","Dina"=>"08524545","Wati"=>"08571234"];
```

2. Mengakses elemen array index numerik

Untuk mengakses elemen array yang berindex numerik pada index tertentu, kita langsung menggunakan nilai indexnya seperti contoh dibawah ini :

```php
$nama = ["Dono","Doni","Dina","Wati"];
//mencetak index 0
    echo $nama[0];
    echo"<br>";

//mencetak index 2
    echo $nama[2];
```
Jika seandainya ingin mencetak keseluruhan nilai dalam array, menghitung panjang array terlebih dahulu dengan keyword count(), dan dengan bantuan looping bisa mencetaknya satu persatu.
seperti contoh dibawah ini :
```php
$nama = ["Dono","Doni","Dina","Wati"];

for($i=0;$i<count($nama);$i++) {
    echo "Index ke $i adalah $nama[$i]";
    echo "<br>"
}
```

3. Mengakses elemen array index associatif

Untuk mengakses elemen array index associatif, langsung menggunakan nama labelnya sepreti contoh dibawah ini :

```php
$nama = ["Dono"=>"0123","Doni"=>"1234","Dina"=>"2345","Wati"=>"3456"];

    echo $nama["Dono"]."<br>";
    echo $nama["Doni"]."<br>";
    echo $nama["Dina"]."<br>";
    echo $nama["Wati"]."<br>";
``` 
Jika seandainya kita ingin mencetak keseluruhan nilai pada array associatif kita dapat menggunakan keyword list dan each seperti contoh dibawah ini :
```php
$nama = ["Dono"=>"0123","Doni"=>"1234","Dina"=>"2345","Wati"=>"3456"];

while(list($index, $nilai)=each($nama)) {
    echo "Index ke $index berisi $nilai";
    echo"<br>";
}
```
dari contoh diatas, maka list akan mengurutkan index associatif yang mana tiap-tiap label akan disimpan pada variabel $index dan isinya disimpan dalam variabel $nilai. 


