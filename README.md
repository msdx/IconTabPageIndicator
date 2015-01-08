#IconTabPageIndicator

带图标文字的底部导航栏，详见博客：http://blog.csdn.net/maosidiaoxian/article/details/38864679

##安装

先在根项目的build.gradle中添加此声明：
```
    repositories {
        jcenter()
    }
```

然后在你的app module中添加此依赖：

```
    compile 'com.githang:iconpagerindicator:1.1'
```

##使用

layout文件：
```
    <com.githang.viewpagerindicator.IconTabPageIndicator
           android:id="@+id/indicator"
           android:layout_alignParentBottom="true"
           android:layout_width="match_parent"
           android:layout_height="wrap_content"/>
       <View android:layout_width="match_parent"
             android:id="@+id/divider"
             android:layout_above="@id/indicator"
             android:layout_height="1px"
             android:background="#ababab"/>
       <android.support.v4.view.ViewPager
           android:layout_above="@id/divider"
           android:id="@+id/view_pager"
           android:layout_width="match_parent"
           android:layout_height="match_parent"/>
```

如果想自定义图标或文字大小，可以style.xml中指定：
```
    <style name="AppTheme" parent="Theme.AppCompat.Light">
        <item name="tabView">@style/TabView</item>
    </style>

    <style name="TabView">
        <item name="android:gravity">bottom|center_horizontal</item>
        <item name="android:layout_width">0dp</item>
        <item name="android:background">@android:color/white</item>
        <item name="android:layout_height">match_parent</item>
        <item name="android:textColor">@color/tab_text_selector</item>
        <item name="android:textSize">12sp</item>
        <item name="iconWidth">27dp</item>
        <item name="iconHeight">27dp</item>
        <item name="android:paddingTop">4dp</item>
        <item name="android:paddingBottom">4dp</item>
        <item name="android:drawablePadding">2dp</item>
    </style>
```