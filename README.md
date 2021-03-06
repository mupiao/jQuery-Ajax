# jQuery-Ajax 文件上传，带进度条 

>代码描述：上传进度条，%百分比显示，Ajax文件上传 带进度条

![image](https://github.com/MuGuiLin/jQuery-Ajax/blob/master/img/%E6%95%88%E6%9E%9C%E5%9B%BE.jpg?raw=true)

HTML5 file 在选择上传文件的时候，根据需要可限制指定的文件类型(***默认任意类型*** )。在 input type="file" 加上 accept="指定要上传的文件类型"即可

-------------
**例如：**
```
<input type="file" id="oFile" name="myFiles" accept=".doc, .docx, .xls, .txt" onchange="FileChangeFn(event)" />
```

* accept=".doc, .docx, .xls, .txt" 只能上传word, exls, .txt文件
* accept=".rar, .zip" 只能上传压缩文件
* accept=".mp3" 只能上传mp3文件
* accept=".mp4, .avi, .swf, .mpeg" 只能上传视频文件
* accept=".jpg, .jpeg .png, .gif, .bmp" 只能上传指定的这些图片文件
* accept="image/*" image表示图片，*表示所有支持的格式， video/* video表示视频，*表示所有支持的格式
* accept="video/mp4, .avi, audio/mp3, .ogg, image/jpeg, .png, .gif" 可选择、指定多种不同类型、格式

<br/>
**注：如果不加accept属性，则上传任意类型的文件(默认)**

Html5 file 在选择上传文件的时候，根据需要可限制选择 1个 或 多个 文件。在 input type="file" 加上 multiple 属性 即可!

**例如：**
```
<input type="file" id="oFile" name="myFiles" multiple onchange="FileChangeFn(event)" />
```

加上 multiple 属性 就可以多选啦：可按住鼠标左键拖动进行多选，或按下键盘上的<kbd>Ctrl键</kbd>，或 <kbd>Shitf键</kbd> 再鼠标左键点选，或<kbd> Ctrl + A </kbd> 

**注： 默认情况下一般都没加multiple 属性，所以只能选择1件文件**

最后：如果以上两种情况都要用到时，就同时加上 multiple属性 和 accept="指定要上传的文件类型"属性即可！

**例如：**
```
<input type="file" id="oFile" name="myFiles" multiple accept=".jpg, .jpeg .png, .gif, .bmp" onchange="FileChangeFn(event)" />
```
>**使用说明:**
>- 1、默认情况下：上传按扭，上传进度条，文件大小，文件类型，都是被隐藏的，要先选择文件后才能显示出来。
>- 2、在中间的大灰色框中，可根据所选择的上传类型，显示出来，类型为：音频，视频，图片。
>- 3、代码中的后端上传地址，只支持图片类型，其他类型的文件不能上传（根自己需求，正确配置后端上传地址）。
>- 4、上传时如果文件太小，上传进度条可能一闪而过，（可将浏览器网络模拟成3G网等，或选择稍大点的文件）。
>- 5、点击[选择上传文件]按扭时，弹出浏览框有点慢，这是因为input file类型 标签中 没有指定 accept="*"文件类型，所以它会检索全部类型，从而导致弹出时慢。
