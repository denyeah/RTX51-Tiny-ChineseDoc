# RTX51 Tiny 中文文档
        2017.12.08 18:56 Upload the CHM and other files
***
## In the End    写在最后

        此文章随意转载，转载请注明出处。https://github.com/DIOLeo/RTX51-Tiny-ChineseDoc
        
八位单片机是众所周知的嵌入式工程师硬件控制的入门芯片，很多不管是本科进入嵌入式世界的freshman还是纯粹的民间爱好者，把单片机玩得风生水起逐渐成了入门标配。当看到这行文字时，你十有八九也是一位像我一样的捣鼓硬件的码农，而且为了51的操作系统才打开这篇文档的。  
那么恭喜你，来对地方了。  
两个星期之前，我萌生了翻译RTX51官方文档的想法，因为那个时候我要在板子上跑操作系统了，不出意外打开时满眼的西洋文字，找来找去没有翻译的较好的中文版，我心想，那我就自己动手翻译一份吧，于是磕磕绊绊两个星期这份RTX51 Tiny的中文版就出炉了，其中一定有翻译的不好的地方，那么请您指出，我的联系方式就在下面，您可以自己编译打包发过来，也可以直接告诉我改进意见。  
我之所以要翻译这篇文档并且无偿地分享出来，前者是我自己要用，后者我想帮助更多的像我一样的还在嵌入式的浑水里摸爬滚打的朋友。说到这里，我推荐一篇比较老的但是非常有用的文章《从单片机初学者迈向单片机工程师》，我也会放出下载链接。这篇文章对于初学者来说一定要读，不仅仅是里面作者的代码，更重要的是编程思想。  
就拿51单片机来说。可能大部分人使用的开发版都是某宝上面卖的又赠光盘又赠各种模块的光鲜亮丽的板子，我也一样，这并不重要，用什么设备只要不坏就行。关键是你怎么学呢？基本上分为两种渠道，一种是学校老师教；另一种是网上自学。现如今的很多高校课堂（至少我现在所处的环境）包括网上的一些商家所发布的商业版教程，大多数使用的都是单一演示视频，太过复杂的呢初学者又不太乐意看，嫌麻烦。不管是视频教程也好，老师上课讲的也好，即使是学了一年半载也还是不能脱离一个死循环里面挨个走任务的习惯，这其实是一个误区，单片机变成要想提高并不一定是掌握更多的模块传感器使用方法，不一定是用板子控制个什么温度传感器啊湿度传感器，确实有一定的帮助，可以积累经验，但是时间长了你写程序还是那一套，没什么长进。  
高校课堂教育暴露三个问题，一个是学生滥用delay函数，另一个是多任务不会协同工作，再一个是模块化设计掌握不到位。有能力的学生课下会自学，会去了解，他们还好，能知道用实时操作系统编程序；按部就班跟着老师走的可就遭了殃了，学了四年出来发现在学校里的一套到公司根本就不是那一回事儿。  
如果在看这篇文章的初学者你之前包括现在写程序还是像这篇文档第二部分“实时程序”里说的那样用的是“多任务程序”你可就要小心了。商家的演示程序是演示程序，它永远只是一个演示程序，只是演示你的模块没有坏，你的这部分功能可以实现，但是真是放到一个项目中，这么照搬过去肯定不行的，举个例子，DHT11模块是一个典型的温湿度传感器，每检测一次数据都需要将近20ms，如果你的项目需要它并且你直接把示例程序揉在里面，你会发现本来想要1s执行一次的任务可能要花2s甚至更多，芯片仿佛得了帕金森一样反应迟钝，其实原因就是出现在你的多任务协同没有做好，滥用delay函数。  
虽然我入行时间不长，但是至少就我看来，这个行业更考验人的智慧，甚至带一点天赋在里面。有人说，不写多少多少万行代码你就不会成为一个好的码农，有那么一点道理，量变产生质变嘛，但是我写上个十万行的hello world那也没用，一种类型的功能函数写上个几次记熟了就得了，到此为止，你需要做的是思考，想怎么用最少的代码量执行最短时间去完成那一个功能，这是每一个码农需要花最多的时间去考虑的。  
还有一点是互联网分享精神，不知道大家有没有发现为什么很多变成大牛都是国外的，很多使用方便广受好评的软件都是外国人在维护，这跟互联网分享精神大有联系。我们平时有什么精彩的代码想法可能会如获至宝，据为己有，生怕别人学了去。但是国外跟我们差别很大，他们都会贴在互联网上让所有人共同来出点子怎么样精益求精。这跟当年Linux发扬光大一个道理。我希望国内的一线工程师也都能抽一点自己的宝贵时间，哪怕只有一点也好，将自己的心路历程自己平时的经验技巧整理分享，国内这部分资料太匮乏了，真的太匮乏了。  
今后可能还会公布更多的使用操作系统的工程出来，如果您需要请给我发邮箱，哪怕只有一个人有需求，我也会利用我越来越少的宝贵时间来做这件事。  
2017.12.08  
