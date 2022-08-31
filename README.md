# Flutter Fundamental Bagian 3

## Praktikum 1 - Menerapkan Gesture Detector 

### Langkah 1 : Menambahkan GestureDetector

Buka file `main.dart` lalu ganti bagian `body` dengan kode berikut. Untuk `MyImageWidget()` dapat Anda ganti dengan widget sendiri.

```
body: Center(
        child: GestureDetector(
            onTap: _incrementCounter,
            child: Column(
              mainAxisAlignment: MainAxisAlignment.center,
              children: <Widget>[
                const MyImageWidget(),
                Text(
                  '$_counter',
                  style: Theme.of(context).textTheme.headline4,
                ),
              ],
            )),
      ),
```

file widget `image.dart`.

```
import 'package:flutter/material.dart';

class MyImageWidget extends StatelessWidget {
  const MyImageWidget({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return const Image(
      image: AssetImage("logo_polinema.png"),
    );
  }
}
```
Jika project dijalankan maka kode program pada `MyImageWidget()` disini menampilkan logo Polinema seperti gambar berikut. Jika klik/tap pada gambar, maka angka di bawah akan terus bertambah, dikarenakan pada **GestureDetector** terdapat parameter **ontap: _ incrementCounter** yang mengakses state **incrementCounter**.

Output Program 

![Screenshot](images/01.png)

