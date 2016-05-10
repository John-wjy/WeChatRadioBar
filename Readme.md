## WechatRadioBar
### 效果图
![](http://ww1.sinaimg.cn/mw690/b5405c76gw1f3qb7xo3wug20ax0ad4a1.gif)
### 用法
#### xml
```xml
<io.github.leibnik.wechatradiobar.WechatRadioGroup
        xmlns:app="http://schemas.android.com/apk/res-auto"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal"
        android:layout_alignParentBottom="true">

        <io.github.leibnik.wechatradiobar.WechatRadioButton
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:checked="true"
            android:drawablePadding="3dp"
            android:gravity="center_horizontal"
            android:paddingBottom="5dp"
            android:paddingTop="3dp"
            android:text="微信"
            android:textColor="#555"
            app:focus_color="#50ba26"
            app:defocus_icon="@drawable/chats"
            app:focus_icon="@drawable/chats_green"/>

        <io.github.leibnik.wechatradiobar.WechatRadioButton
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:drawablePadding="3dp"
            android:gravity="center_horizontal"
            android:paddingBottom="5dp"
            android:paddingTop="3dp"
            android:text="通讯录"
            android:textColor="#555"
            app:focus_color="#50ba26"
            app:defocus_icon="@drawable/contacts"
            app:focus_icon="@drawable/contacts_green"/>
</io.github.leibnik.wechatradiobar.WechatRadioGroup>
```

* `app:focus_color`:选中状态文字的颜色
* `app:focus_icon`:选中状态的图标
* `app:defocus_icon`:非选中状态的图标

#### java
```java
viewPager = (ViewPager) findViewById(R.id.viewpager);
gradualRadioGroup = (WechatRadioGroup) findViewById(R.id.radiogroup);
viewPager.setAdapter(adapter);
// 关键代码
gradualRadioGroup.setViewPager(viewPager);
```


