# lab2Web

# Tugas Pemograman Web 2
## Profil
| #               | My Data               |
| --------------- | -----------------     |
| **Nama**        | Muhamad Suryanegara   |
| **NIM**         | 312110447             |
| **Kelas**       | TI.21.A.1             |
| **Mata Kuliah** | Pemrograman Web 2     |

# Persiapan
Untuk memulai membuat kode php, perlu disiapkan web server dan interpreter PHP terlebih dahulu. Web server yang kita gunakan adalah Apache2 dan interpreter PHP 8. Untuk memudahkan proses praktikum, kita gunakan aplikasi bundle web server yaitu XAMPP.

## Install XAMPP
1. Unduh XAMPP [Disini](https://www.apachefriends.org/download.html) dan sesuaikan dengan sistem operasi kalian, lalu pilih versi php (disini saya pilih PHP 8). lalu klik Download.
2. Kemudian buka installer XAMPP nya, setelah itu next - next saja hingga selesai.
3. Secara default XAMPP itu akan disimpan dalam Local Disk (C:)

![Install XAMPP]![folder](https://user-images.githubusercontent.com/92678339/226803624-e69095d1-ff0e-4e6d-b3d7-74a9b048f7f0.png)



4. Buka XAMPP Control Panel.
5. Lalu klik Start pada Apache dan MySQL.

![XAMPP PANEL]![xampp](https://user-images.githubusercontent.com/92678339/226928668-28716082-672d-4160-9d2e-853dee736a2f.png)



6. Kemudian uji coba apakah web server sudah bekerja dengan baik dengan mengetik http://127.0.0.1 atau http://localhost

## Memulai PHP
<p>Buat folder `Lab2Web` pada root direktori web server (C:\xampp\htdocs)

![Buat Folder]![folder2](https://user-images.githubusercontent.com/92678339/226928837-ed4d21dd-5584-4974-a832-fecd6bbcde92.png)

<p>Kemudian untuk mengakses direktori tersebut pada web server dengan mengakses URL: http://localhost/Lab2Web/

![Lab2Web]![index](https://user-images.githubusercontent.com/92678339/226929011-63ccbb54-e1c8-4722-a5ed-a3aab708e672.png)

## PHP Dasar
<p>Buat file baru dengan nama php_dasar.php pada directory tersebut. Kemudian buat kode seperti berikut.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>PHP DASAR</title>
</head>
<body>
  <h1>Belajar PHP Dasar</h1> 
  <?php
  echo "Hello World!";
  ?>
</body>
</html>
```

<p>Kemudian untuk mengakses hasilnya melalui URL: http://localhost/Lab2Web/php_dasar.php

![PHP DASAR]![hello](https://user-images.githubusercontent.com/92678339/226929194-ff2ed5d1-4e20-4f6b-b1e0-e13287a64ebd.png)

## Variable PHP
<p>Menambahkan variable pada program.

```html
<h2>Menggunakan Variable</h2>
<?php
$nim = "312110447";
$nama = "Muhamad Suryanegara";
echo "NIM : " . $nim . "<br>";
echo "Nama : $nama";
?>
```

![Variable PHP]![variable2](https://user-images.githubusercontent.com/92678339/226929442-5968e9c5-97df-4663-b4f4-a2ae1d478619.png)

## Predefine Variable $_GET
<p>Buat file `latihan2.php` dalam direktori Lab2Web. lalu masukan kode berikut.

```html
<h2>Predefine Variable $_GET</h2>

<?php
echo "Selamat Datang " . $_GET['nama'];
?>
```

<p>Untuk mengaksesnya gunakan URL: http://localhost/Lab2Web/latihan2.php?nama=farhan 

![Predefine Variable]![variable](https://user-images.githubusercontent.com/92678339/226929577-888ca6ae-02be-48f0-9025-b34c17746a8b.png)

## Membuat Form Input
- Buat file `latihan3.php` didalam direktori Lab2Web, Kemudian tambahkan kode berikut.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>PHP DASAR</title>
</head>
<body>
  <h2>Form Input</h2>
  <form action="" method="post">
    <label for="">Nama : </label>
    <input type="text" name="nama" placeholder="Masukan Nama">
    <input type="submit" value="kirim">
  </form>
  <?php
  echo "Selamat Datang " . $_POST['nama'];
  ?>
</body>
</html>
```

- Lalu inputkan sesuatu dalam kolom form tersebut, kemudian klik Kirim.
- Maka, hasilnya akan seperti berikut:

![Form Input]![input](https://user-images.githubusercontent.com/92678339/226929757-22cac020-b2fd-4da9-86ce-ce342bf40953.png)

## Operator
- Masukan kode berikut.

```html
$gaji = 1000000;
$pajak = 0.1;
$thp = $gaji - ($gaji*$pajak);
echo "Gaji sebelum pajak = Rp. $gaji <br>";
echo "Gaji yang dibawa pulang = Rp. $thp";
```

- Maka, hasilnya akan seperti berikut.

![Operator]![gaji](https://user-images.githubusercontent.com/92678339/226930089-1c85899c-049c-4234-a647-f5537451433c.png)

## Kondisi IF
- Masukan kode berikut.

```html
$nama_hari = date("l");
if ($nama_hari == "Sunday") {
echo "Minggu";
} elseif ($nama_hari == "Monday") {
echo "Senin";
} else {
echo "Selasa";
}
```

- Maka, hasilnya akan seperti berikut.

![Kondisi IF]![selasa](https://user-images.githubusercontent.com/92678339/226930367-3c7e3c30-c201-4852-adca-11574b7b2bfe.png)
## Kondisi Switch
- Masukan kode berikut.

```html
$nama_hari = date("l");
switch ($nama_hari) {
  case "Sunday":
    echo "Minggu";
    break;
  case "Monday":
    echo "Senin";
    break;
  case "Tuesday":
    echo "Selasa";
    break;
  default:
echo "Sabtu";
}
```

- Maka, hasilnya akan seperti berikut.

![Kondisi Switch]![sabtu](https://user-images.githubusercontent.com/92678339/226930328-d1e65f9f-e406-4040-8937-5333d3de020e.png)

## Perulangan FOR
- Masukan kode berikut.

```html
echo "Perulangan 1 sampai 10 <br />";
for ($i=1; $i<=10; $i++) {
echo "Perulangan ke: " . $i . '<br />';
}
echo "Perulangan Menurun dari 10 ke 1 <br />";
for ($i=10; $i>=1; $i--) {
echo "Perulangan ke: " . $i . '<br />';
}
```

- Maka, hasilnya akan seperti berikut.

![Perulangan For]![perulangan](https://user-images.githubusercontent.com/92678339/226930516-b64c87f8-274f-48c1-8774-11a85e2a0bb6.png)

## Perulangan While
- Masukan kode berikut.

```html
echo "Perulangan 1 sampai 10 <br />";
$i=1;
while ($i<=10) {
echo "Perulangan ke: " . $i . '<br />';
$i++;
}
```

- Maka, hasilnya akan seperti berikut.

![Perulangan While]![perulangan2](https://user-images.githubusercontent.com/92678339/226930618-1154059b-9463-4f25-aba1-68ba2bf810fe.png)

## Perulangan Do While
- Masukan kode berikut.

```html
echo "Perulangan 1 sampai 10 <br />";
$i=1;
do {
echo "Perulangan ke: " . $i . '<br />';
$i++;
} while ($i<=10);
```

- Maka, hasilnya sama saja dengan perulangan sebelumnya.

# Pertanyaan dan Tugas
<p>Buatlah program PHP sederhana dengan menggunakan form input yang menampilkan nama, tanggal lahir dan pekerjaan. Kemudian tampilkan outputnya dengan menghitung umur berdasarkan inputan tanggal lahir. Dan pilihan pekerjaan dengan gaji yang berbeda-beda sesuai pilihan pekerjaan.

## Praktikum
- Buat file `index.php` dalam direktori Praktikum agar terlihat rapih
- Masukan kode berikut.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Tugas</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <h1>Tugas PHP Dasar</h1>
    <form action="" method="post" class="container">
      <div class="form-control">
        <label for="nama">Nama</label>
        <input type="text" name="nama" placeholder="Masukan nama" required />
      </div>
      <div class="form-control">
        <label for="nama">Tanggal Lahir</label>
        <input type="date" name="tgl_lahir" required />
      </div>
      <div class="form-control">
        <label for="nama">Pekerjaan</label>
        <select name="pekerjaan" required>
          <option value="">- Pilih Pekerjaan -</option>
          <option value="Web Developer">Web Developer</option>
          <option value="Data Scientist">Data Scientist</option>
          <option value="DevOps">DevOps</option>
          <option value="Mobile Application Developer">
            Mobile Application Developer
          </option>
        </select>
      </div>
      <button type="submit">Kirim</button>
    </form>

    <?php
    if ($_SERVER['REQUEST_METHOD'] == "POST" && $_POST['nama'] != '') {
        $nama = ucwords(strtolower($_POST['nama']));

        // Tanggal Lahir
        $lahir = date_format(date_create($_POST['tgl_lahir']), "d F Y");

        // Hitung Umur
        $tgl = new DateTime($_POST['tgl_lahir']);
        $today = new DateTime('today');
        $umur = $today->diff($tgl)->y;

        // Pekerjaan dan Gaji
        $pekerjaan = $_POST['pekerjaan'];
        $gaji = "";

        switch ($pekerjaan) {
            case 'Mobile Application Developer' :
                $gaji = "36 Juta";
                break;

            case 'Data Scientist':
                $gaji = "19 Juta";
                break;

            case 'Web Developer':
                $gaji = "25 Juta";
                break;

            case 'DevOps':
                $gaji = "35 Juta";
                break;

            default :
                $gaji = '0';
                break;
        }        
    ?>

    <div class="container">
      <h3>Hasil</h3>
      <hr />
      <table>
        <tr>
          <td>Nama</td>
          <td>
            :
            <?= $nama ?>
          </td>
        </tr>

        <tr>
          <td>Tanggal Lahir</td>
          <td>
            :
            <?= $lahir ?>
          </td>
        </tr>

        <tr>
          <td>Umur</td>
          <td>
            :
            <?= $umur ?>
            Tahun
          </td>
        </tr>

        <tr>
          <td>Pekerjaan</td>
          <td>
            :
            <?= $pekerjaan ?>
          </td>
        </tr>

        <tr>
          <td>Gaji</td>
          <td>: Rp.<?= $gaji ?></td>
        </tr>
      </table>
    </div>
    <?php
    }
    ?>
  </body>
</html>
```

- Kemudian buat file `style.css` didalam folder yang sama agar mudah diakses
- Lalu, masukan kode berikut.

```bash
* {
    font-family: sans-serif;
    margin: 0;
    padding: 0;
}

h1 {
    text-align: center;
    margin: 20px 0;
}

h3 {
    text-align: center;
    margin-bottom: 10px;
}

.container {
    border: 1px solid black;
    width: 30%;
    margin: auto;
    padding: 20px;
    border-radius: 5px;
    margin-bottom: 30px;
}

.form-control {
    margin-bottom: 10px;
    display: flex;
    flex-direction: column;
}

input, select {
    padding: 5px;
    margin-top: 5px;
    border: 1px solid black;
    border-radius: 3px;
}

button {
    background-color: dodgerblue;
    border: none;
    padding: 8px;
    width: 100%; 
    color: white;
    margin-top: 10px;
    border-radius: 5px;
}

table {
    width: 100%;
}

td {
    padding: 5px 0;
}

span {
    color: red;
}
```

- Maka, hasilnya akan seperti berikut.

![Praktikum1]![datadiri](https://user-images.githubusercontent.com/92678339/226930824-44ec2c77-aa91-45d3-a688-5194b02e8459.png)


- Sesudah diinputkan.

![Praktikum2]![datadiri2](https://user-images.githubusercontent.com/92678339/226930900-10f631c5-79a3-4ffe-bcb4-7c7a8340a5a1.png)



# Terima Kasih!
