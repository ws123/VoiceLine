
####VoiceLine，一个可以根据麦克风音量大小，显示一些波形效果的控件。一共有两种效果，波开和矩形，如下。也有一些自定义属性，包括波形的颜色，灵敏度，间隔等。

![image](https://github.com/ws123/VoiceLine/blob/master/line.gif)
![image](https://github.com/ws123/VoiceLine/blob/master/rect.gif)

引用方法：

```groovy
compile 'com.carlos.voiceline:mylibrary:1.0.4'
```
####自定义属性列表如下：
```xml
<resources>
    <declare-styleable name="voiceView">
        <!--中间线的颜色，就是波形的时候，大家可以看到，中间有一条直线，就是那个-->
        <attr name="middleLine" format="color" />
        <!--中间线的高度，因为宽度是充满的-->
        <attr name="middleLineHeight" format="dimension" />
        <!--波动的线的颜色，如果是距形样式的话，刚是距形的颜色-->
        <attr name="voiceLine" format="color" />
        <!--矩形的宽度-->
        <attr name="rectWidth" format="dimension" />
        <!--矩形之间的间隔-->
        <attr name="rectSpace" format="dimension" />
        <!--矩形的初始高度，就是没有声音的时候，矩形的高度-->
        <attr name="rectInitHeight" format="dimension" />
        <!--所输入音量的最大值-->
        <attr name="maxVolume" format="float" />
        <!--控件的样式，一共有两种，波形或者矩形-->
        <attr name="viewMode">
            <enum name="line" value="0" />
            <enum name="rect" value="1" />
        </attr>
        <!--灵敏度，默认值是4-->
        <attr name="sensibility">
            <enum name="one" value="1" />
            <enum name="two" value="2" />
            <enum name="three" value="3" />
            <enum name="four" value="4" />
            <enum name="five" value="5" />
        </attr>
    </declare-styleable>
</resources>
```
实际使用过程中，可以这样配置：

```xml
<com.carlos.voiceline.mylibrary.VoiceLineView  
    android:id="@+id/voicLine"  
    android:layout_width="match_parent"  
    android:layout_height="match_parent"  
    android:background="@android:color/white"  
    voiceView:middleLine="@android:color/holo_red_light"  
    voiceView:middleLineHeight="1dp"  
    voiceView:rectSpace="2dp"  
    voiceView:rectWidth="5dp"  
    voiceView:viewMode="line"  
    voiceView:voiceLine="@android:color/holo_red_light" />  
```

### License

	Copyright 2016 Jaeger Chen

	Licensed under the Apache License, Version 2.0 (the "License");	you may not use this file except in compliance with the License.
	You may obtain a copy of the License at
	
		http://www.apache.org/licenses/LICENSE-2.0

	Unless required by applicable law or agreed to in writing, software
	distributed under the License is distributed on an "AS IS" BASIS,
	WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
	See the License for the specific language governing permissions and
	limitations under the License.
