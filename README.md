
效果图
---

- ![效果图](https://github.com/ly931126/TestHorizontalProgressBar/blob/master/device-2017-08-01-110511.png)

- [参考链接]( http://www.jb51.net/article/91491.htm)

### 1.在布局中调用
```
<ProgressBar
        style="@android:style/Widget.ProgressBar.Horizontal"
        android:layout_width="320dp"
        android:layout_height="7dp"
        android:layout_margin="10dp"
        android:max="100"
        android:layout_centerInParent="true"
        android:progress="60"
        android:progressDrawable="@drawable/install_progress_drawable" />
```
### 2.在drawable中画进度条的drawable  (install_progress_drawable)
```
<?xml version="1.0" encoding="utf-8"?>
<layer-list xmlns:android="http://schemas.android.com/apk/res/android">

    <item
        android:id="@android:id/background"
        android:drawable="@drawable/install_progressbar_bg" />

    <item android:id="@android:id/progress">

        <scale
            android:drawable="@drawable/install_progressbar_progress"
            android:scaleWidth="100%" />

    </item>

</layer-list>
```
### 3.画进度条的背景(install_progressnar_bg）
```
<shape xmlns:android="http://schemas.android.com/apk/res/android">

    <corners android:radius="10dp" />
    <solid android:color="#717276" />

</shape>
```
### 4.画进度条的进度(install_progressbar_progress)
```
<?xml version="1.0" encoding="utf-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android">

    <corners android:radius="10dp" />
    <solid android:color="#187a9f" />

</shape>
```


