# 收集的一些字体

我收集了若干字体；

- 在`ubuntu`下执行以下命令即可完成安装（我的工作环境是Ubuntu）。

```bash
	git clone https://github.com/jiaxiaochu/font.git && cd font && ./install.sh
```

- Windows下你只需要将字体文件复制到`C:\Windows\Fonts`文件夹就能完成安装。

- Mac下你只需要在launchpad中打开`字体册`程序，然后将字体拖入到窗口即可，或者菜单，文件-添加字体，进行添加字体。

# 字体分类说明

收集的字体总的来说可以这样分类。

## 编程字体(fonts for programmer)

我是一个喜欢折腾编程工具的人，所以也收集了一些适用于编程的漂亮字体，比如说雅黑和Consolas混合(YaHei.Consolas.1.11b.ttf)，中文用雅黑，英文用Consolas，非常完美。这也是我最推荐的一个字体。

![yahei_consolas](https://cloud.githubusercontent.com/assets/4246425/13220862/75386cb2-d9b3-11e5-9d56-d59100ae1c7f.png)

还有比如说苹果字体`monaco`，也很漂亮。

![monaco](https://cloud.githubusercontent.com/assets/4246425/13221785/092c53f8-d9b8-11e5-93e7-7d2f4c3dee90.png)

还有`yahei_mono`也是另外一个组合字体，也很漂亮。

# 解决 matplotlib 绘制图形中文字体显示问题

下载字体库中的**simhei** 字体（或者其他的支持中文显示的字体也行）

- 安装字体

  - linux下：拷贝字体到 usr/share/fonts 下：

    ```
    sudo cp ~/simhei.ttf /usr/share/fonts/simhei.ttf
    ```

  - windows和mac下：双击安装
    修改配置文件matplotlibrc 并且在~/.matplotlib/matplotlibrc也进行修改

    在安装的地方找到虚拟环境your path`/home/allen/workspace/AI/lib/python3.6/site-packages/matplotlib/mpl-data`目录下的matplotlibrc文件，修改下面三项配置

    ```
    font.family         : sans-serif	# 将此行注释打开即可       
    
    font.sans-serif     : SimHei, Bitstream Vera Sans, Lucida Grande, Verdana, Geneva, Lucid, Arial, Helvetica, Avant Garde, sans-serif		# 将此行注释打开，并将SimHei添加进去
    
    axes.unicode_minus  : False		# 将此行注释打开并修改为False       
    ```

- 删除matplotlib字体缓存：

  将`~/.cache/matplotlib/fontList.json`目录中的 fontList.json 删除

  ```
  sudo rm -rf ~/.cache/matplotlib/fontList.json
  ```

## WPS 在 ubuntu 下需要安装的字体(fonts for WPS Office)

另外在ubuntu安装WPS Office之后需要另外装一些字体进而解决乱码和缺失字体的问题，我也把它放在这个仓库了。

下载仓库中的  **wps-office** 字体库

```
# 将从仓库下载后的 wps-office 放到`/usr/share/fonts/`目录下
sudo cp wps-office /usr/share/fonts/
```

消除一下缓存和生成新的缓存

```
sudo mkfontscale
sudo mkfontdir
sudo fc-cache
```

##  Windows下常见的一些字体。(Fonts in Windows)

由于我的工作环境是ubuntu，在编写文档后，为了不至于拿到Windows下变了样子，所以希望保持文档所用字体的一致，所以收集下Window下的一些字体，用Windows的同学可以忽略这部分字体（宋体，黑体等）。

。。
