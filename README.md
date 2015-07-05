Android-Percent-Layout-Sample
---
This is a sample for using android percent layout.
---

![PercentLayout](https://raw.githubusercontent.com/lusfold/Android-Percent-Layout-Sample/master/percent_layout_show.png)

### Add support library
```xml
dependencies {
    compile 'com.android.support:percent:22.2.0'
}
```

###Layout
```xml
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingBottom="@dimen/activity_vertical_margin"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    tools:context=".MainActivity">

    <android.support.percent.PercentRelativeLayout xmlns:app="http://schemas.android.com/apk/res-auto"
        android:layout_width="match_parent"
        android:layout_height="match_parent">

        <View
            android:id="@+id/relative_top"
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_alignParentTop="true"
            android:background="#000000"
            app:layout_heightPercent="30%"
            app:layout_widthPercent="100%" />

        <android.support.percent.PercentFrameLayout xmlns:android="http://schemas.android.com/apk/res/android"
            xmlns:app="http://schemas.android.com/apk/res-auto"
            android:id="@+id/relative_middle"
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_below="@+id/relative_top"
            android:background="#0000ff"
            app:layout_heightPercent="40%"
            app:layout_widthPercent="50%">

            <View
                android:id="@+id/frame_0"
                android:layout_width="0dp"
                android:layout_height="0dp"
                android:background="#00ffff"
                app:layout_heightPercent="25%"
                app:layout_widthPercent="75%"
                app:layout_marginTopPercent="75%"
                app:layout_marginLeftPercent="25%"/>

            <View
                android:id="@+id/frame_1"
                android:layout_width="0dp"
                android:layout_height="0dp"
                android:background="#ffff00"
                app:layout_heightPercent="75%"
                app:layout_widthPercent="25%" />
        </android.support.percent.PercentFrameLayout>

        <View
            android:id="@+id/relative_bottom"
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:layout_below="@id/relative_middle"
            android:background="#00ff00"
            app:layout_heightPercent="30%"
            app:layout_widthPercent="100%" />
    </android.support.percent.PercentRelativeLayout>
</RelativeLayout>
```

###The attributes that you can use

- layout_widthPercent
- layout_heightPercent
- layout_marginPercent
- layout_marginLeftPercent
- layout_marginTopPercent
- layout_marginRightPercent
- layout_marginBottomPercent
- layout_marginStartPercent
- layout_marginEndPercent

## License

    Copyright 2015 Lusfold

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.