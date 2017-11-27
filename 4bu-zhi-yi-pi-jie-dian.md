四、布置好几串节点

刚刚我们已经能够看到温度的实时变化了，接下来我们接收并显示出体感温度、相对湿度、降水量、气压、以及风速数据。

由于还需要显示 5 种数据，对比这些数据结构可以发现他们的数据结构是相同的，都是一个变量名对应一个数值。因为刚刚我们配置了“Function”，那我们可以借用我们刚刚的配置成果，用`ctrl+c`复制上面这个红框中的“Function”节点，`ctrl+v`粘贴出个“Function”节点，并双击配置。

![](/assets/snipaste_20171026_134825.png)

分别配置 5 个“Function”节点，截图只展示其中一个，其他同。

hum：

```
msg.payload = msg.payload.hum;
return msg;
```

pcpn：

```
msg.payload = msg.payload.pcpn;
return msg;
```

fl：

```
msg.payload = msg.payload.fl;
return msg;
```

wind\_spd：

```
msg.payload = msg.payload.wind_spd;
return msg;
```

pres：

```
msg.payload = msg.payload.pres;
return msg;
```

![](/assets/snipaste_20171026_152951.png)

按照刚刚相同的复制粘贴的方法将仪表盘的节点复制 5 份，如下图。

![](/assets/snipaste_20171026_153614.png)

依次点击这些仪表盘，按照如下图配置，在“Range”一栏，最大值和最小值按照你codelab的时候估算来写。

![](/assets/snipaste_20171026_153953.png)

![](/assets/snipaste_20171026_154145.png)

![](/assets/snipaste_20171026_154346.png)

![](/assets/snipaste_20171026_154614.png)

好了，这五个数据都配置好了，稍微整理一下我们的逻辑思维，如下图。之后点击右上角的“部署”，相信你能弹出“部署成功”提示。我们将页面切换到刚刚打开的 Dashboard 显示效果页面。

![](/assets/snipaste_20171026_154658.png)

这是效果图，但是咋就这么丑呢。没事我们需要优化这个界面。

![](/assets/snipaste_20171026_203400.png)![](/assets/snipaste_20171026_203418.png)

回到编辑界面，看看这个“Dashboard”是不是可以编辑。在右侧点击“Dashboard”编辑界面，选择“Layout”，将鼠标移到 weather 一栏，可以看到“edit”，点击进入。

![](/assets/snipaste_20171026_203940.png)

这里我们发现这里有 width ，我们把 6 改成 12 试试，点击“Update”和“部署”，再看看效果。

![](/assets/snipaste_20171026_204017.png)

仪表盘变大了，也就是说仪表盘大小随着Dashboard的大小变化，那我们更改仪表盘的大小。

![](/assets/snipaste_20171026_211737.png)![](/assets/snipaste_20171026_212013.png)

![](/assets/snipaste_20171026_212031.png)

![](/assets/snipaste_20171026_212144.png)

我们的效果可以看出来了，那我们就把 weather 的宽度换成 24 ，哈哈这就是我们效果了！



![](/assets/snipaste_20171026_212229.png)

![](/assets/snipaste_20171026_212300.png)

当然，这个 Dashboard 界面还不够友好，需要再次进行优化，这个步骤留给诸位了！