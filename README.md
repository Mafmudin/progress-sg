# progress-svg-gif
android progress bar with svg or gif file

### Add to android studio with gradle

1. Add following code to ```build.gradle```

```
allprojects {
  repositories {
    ...
    maven { url 'https://jitpack.io' }
   }
}
```

2. Then add the dependency
```
dependencies {
  implementation 'com.github.Mafmudin:progress-sg:0.0.1'
}
```


### Add to android studio with maven

1. Add the JitPack repository to your build file

```
<repositories>
  <repository>
    <id>jitpack.io</id>
    <url>https://jitpack.io</url>
  </repository>
</repositories>
```

2. Add the dependency

```
<dependency>
  <groupId>com.github.Mafmudin</groupId>
  <artifactId>progress-sg</artifactId>
  <version>0.0.1</version>
</dependency>
```

## How to use
1. Make sure you place the svg file inside the assets directory

### Image assets (svg) example
<img src='https://github.com/Mafmudin/myassets/blob/master/images/assets.png'></br>
* Make assets folder if no exsist (<a href='https://stackoverflow.com/questions/26706843/adding-an-assets-folder-in-android-studio?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa'>Add assets folder</a>)

2. Use it like a ProgressDialog
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

*To dismiss the progress, call ```dismiss()``` method*
example : ```progressSvg.dismiss()```
<br/> enjoy the progress with svg file you have -_-


# How to use gif resources
1. Prepare your gif resources, place it on drawable directory
</br><img src='https://github.com/Mafmudin/myassets/blob/master/images/gif.png'/></br>
2. Use it like ProgressDialog
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

#### Download loading / progress svg, gif or apng file on
([Loading.io](https://loading.io/))
