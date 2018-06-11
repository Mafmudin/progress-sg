<link rel="shortcut icon" type="image/x-icon" href="favicon.ico">

# Progress-svg-gif
android progress dialog dengan menggunakan file svg atau gif

### cara menambahkan progress-svg-gif ke project android studio dengan menggunakan gradle
* tambahkan kode di bawah kedalam file ```build.gradle``` (root project)

```
allprojects {
  repositories {
    ...
    maven { url 'https://jitpack.io' }
   }
}
```

* lalu, tambahkan dependesi berikut kedalam file ```build.gradle``` (module aplikasi)

```
dependencies {
  implementation 'com.github.Mafmudin:progress-sg:0.0.1'
}
```

### cara menambahkan progress-svg-gif ke project android studio dengan menggunakan maven
* tambahkan *jitpack repository* ke dalam build file maven

```
<repositories>
  <repository>
    <id>jitpack.io</id>
    <url>https://jitpack.io</url>
  </repository>
</repositories>
```

* tambahkan dependesinya

```
<dependency>
  <groupId>com.github.Mafmudin</groupId>
  <artifactId>progress-sg</artifactId>
  <version>0.0.1</version>
</dependency>
```

## cara menggunakan progress-svg-gif
* pastikan sudah disiapkan file svg di dalam folder assets

<img src='https://github.com/Mafmudin/myassets/blob/master/images/assets.png?raw=true' alt="contoh tampilan susuna folder assets"/>

*contoh tampilan lokasi file svg dalam folder assets, buatlah folder assets jika belum tersedia* (<a href='https://stackoverflow.com/questions/26706843/adding-an-assets-folder-in-android-studio?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa'>Link cara menambahkan folder assets</a>)

* gunakan progress-svg-gif seperti penggunaan progress dialog, contoh penggunaannya yaitu:

```
ProgressSvg progressSvg = new ProgressSvg(MainActivity.this);
//create an object form this class with a Context
progressSvg.setSvgAssets("loading_circle.svg");
//set svg with a resource you have prepare before
progressSvg.setMessage(getResources().getString(R.string.please_wait));
//set text message as you want
progressSvg.setTextColor(ContextCompat.getColor(MainActivity.this, R.color.colorAccent));
//set text color as you want
progressSvg.setTextSize(11.0f);
//set text size as you want
progressSvg.setBackgroundColor(Color.GRAY);
//set background as you want
progressSvg.show();
//call show() method to show the proggress
```

*untuk menyembunyikan progress, panggil fungsi ```dismiss()``` *
contoh : ```progressSvg.dismiss()```

yap, *enjoy* penggunaan progress-svg-gif :)


## Cara menggunakan file gif
* siapkan file gif dan simpan di dalam folder drawable (res/drawable)

<img src='https://github.com/Mafmudin/myassets/blob/master/images/gif.png?raw=true' alt="simpan file gif di dalam folder drawable"/>

*contoh tampilan susuan folder drawable*

* contoh pennggunaan progress-svg-giff yaitu: 

```
 ProgressGif progressGif = new ProgressGif(MainActivity.this);
 //create an object with a Context as a parameter
 progressGif.setGifResource(R.drawable.mag);
 //set progress with a gif file prepared before
 progressGif.setMessage(getResources().getString(R.string.searching));
 //set text message on progress
 progressGif.show();
 //show the progress
```

#### Download loading / progress svg, gif atau apng file di link berikut
([Loading.io](https://loading.io/))
