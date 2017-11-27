# 二、Hello World

接下来我们从左侧将下列 4 个节点拖到中间的主界面

![](/assets/Snipaste_2017-10-21_16-44-10.png)

我们双击右上角这个节点，开始配置

![](/assets/Snipaste_2017-10-21_16-45-43.png)

输入`thomsayan.cn`，如果你的 MQTT Broker 有账号密码，那就需要在“Security”中进行设置，我们本次 CodeLab 中是没有的，所以略过了本次环节，之后我们点击更新。

![](/assets/Snipaste_2017-10-21_16-46-57.png)



此时，我们发现我们的“Server”已经更新了，接下来我们在“Topic”一栏中输入`YourNameAndRandomNumber`，注意是全小写哦！之后我们点击完成即可！

![](/assets/Snipaste_2017-10-21_16-48-12.png)

接下来双击下图红框中的节点，选择“Server”为刚刚我们创建的 Server ，并填写我们刚刚设定的 Topic，并点击完成！

![](/assets/Snipaste_2017-10-21_16-49-41.png)

我们动动鼠标，用红框中的线分别连接第一行和第二行的节点，并点击右上角的红色部署按钮！

![](/assets/Snipaste_2017-10-21_16-50-42.png)

这个时候我们可以看到顶部的提示栏提示“部署成功”，同时紫色背景的节点下方也显示了“connected”，这说明我们部署成功，并且 mqtt in 和 mqtt out 这两个节点也连接上了我的服务器！

![](/assets/Snipaste_2017-10-21_16-51-03.png)

接下来，我们选中右上角的“Debug”小栏目

![](/assets/Snipaste_2017-10-21_16-51-25.png)

点击下图中红框的按钮

![](/assets/Snipaste_2017-10-21_16-51-50.png)

这时候右侧“Debug”小界面出现了一连串的数字，这是时间戳。好吧，这个时候你就完成了第一步，利用 mqtt out 节点转发了时间戳，并且用 mqtt in 节点成功接收到了刚刚发出去的时间戳！

![](/assets/Snipaste_2017-10-21_16-52-25.png)



