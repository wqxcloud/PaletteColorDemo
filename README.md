# PaletteColorDemo
  探索Palette 与 生成 渐变背景色

# BackGround：

  根据图标生成其渐变背景颜色
  (Generates its gradient background color according to the icon)

# Screen Recrode

  ![image](https://github.com/LABELNET/PaletteColorDemo/blob/master/Screen/1.gif)
  ![image](https://github.com/LABELNET/PaletteColorDemo/blob/master/Screen/2.gif)

# Test1- 源码运行观看 (clone simple source code )

  * (1) 打开Android Studio ，新建工程 ，打开新建工程所在的文件夹，在其跟目录下进行clone
  * (2) git clone https://github.com/LABELNET/PaletteColorDemo.git
  * (3) 配置新建工程下的settings.gradle , 添加 include ':palettecolordemo' 执行即可
  * (4) 注意：出错的话，注意修改v7包的版本；

# Test2- 下载与安装 APK (Download and Install simple.apk file)

  [Download SimpleApk](https://github.com/LABELNET/PaletteColorDemo/blob/master/Screen/simple.apk)

# Gradle Dependency 使用
  * Don't Gradle Dependency, You can learn from [ here](http://blog.csdn.net/LABLENET/article/details/52340634)
  * [ Android - 一个似神器而非神器之Palette探索与实践](http://blog.csdn.net/LABLENET/article/details/52340634)

# Sample Usage

**使用方法 ：**

**（1）** *init(Resource res,int resId,callback)*  方式

```
 PaletteUtil.getInstance()
                .init(getResources()
                ,R.mipmap.icon_one
                ,new PaletteUtil.PatternCallBack() {
            @Override
            public void onCallBack(Drawable drawable, int titleColor) {
                tv.setTextColor(titleColor);
                tv.setBackgroundDrawable(drawable);
            }
        });
```
**（2）** *init(bitmap,callback)*  方式

```
  Bitmap bitmap = BitmapFactory.decodeResource(getResources(),R.mipmap.icon_one);
                PaletteUtil.getInstance().init(bitmap, new PaletteUtil.PatternCallBack() {
                    @Override
                    public void onCallBack(Drawable drawable, int titleColor) {

                    }
                });
