# JustSpeak：在Android上启用通用语音控制
**摘要** 在本文中，我们将介绍JustSpeak，这是一种针对Android操作系统的非视觉访问的通用语音控制解决方案。与现有系统相比，JustSpeak提供了两个贡献。首先，它可以在Android上启用系统范围的语音控制功能，以适应任何应用。 JustSpeak根据应用程序上下文构造一组可用的语音命令;这些命令是直接从屏幕标签和辅助功能元数据合成的，并且不需要应用程序开发人员的进一步干预。其次，它提供了更有效和自然的交互，并支持同一话语中的多个语音命令。我们介绍JustSpeak的系统设计，并描述它在各种用例中的实用性。然后我们讨论在其他平台上像JustSpeak这样的服务所需的系统级支持。通过消除目标定位和指向任务，JustSpeak可以显着改善盲人和运动障碍用户的图形界面交互体验。

## 简介
鼠标和多点触控表面已被广泛用作计算机和移动设备的主要输入方式，因为它们的可靠精度。但是，在视觉上不能显示或妨碍显示的情况下，或者对于敏捷问题的用户来说，指向目标很困难，因此往往效率不高。

有远见的人也经常遇到这个问题，例如开车时。至于运动障碍的人，当指向目标时，他们会面临挑战，因为大多数GUI交互技术需要手或手指的准确物理运动。语音控制是一种有效的替代输入模式，不需要目标定位和指向，这通常需要根据费茨定律完成交互所需的大部分时间[12]。对于mer研究表明，考虑到这种优势，语音输入是优选的盲人在进行文字输入时[3]。当然，语音界面也存在挑战，如纠错困难[3]，较大的学习开销和较低的噪声环境中的可用性。现有的语音控制系统受到许多方面的限制。它们中的大多数是建立在应用程序级（例如语音输入方法）上的，或者是受预定义命令集限制的。

在本文中，我们将介绍JustSpeak，它是在Android的系统级别上根据不同的架构设计和构建的。 JustSpeak旨在实现对Android操作系统的通用语音控制，帮助用户快速自然地控制系统，无需视觉和免提。应用程序作为系统服务在后台运行，无论前台运行哪种应用程序，都可以使用简单手势或近场通信（NFC）标签激活该服务。当被激活时，JustSpeak记录虚假言语。然后将音频转换为纯文本并解析为可自动执行的计算机可理解的命令。与大多数当前系统不同，JustSpeak可以在任何已安装的应用程序内容纳命令。而且，JustSpeak在一个话语中支持多个命令。为了立场，要打开Gmail应用程序然后刷新收件箱，可以一起说两个命令“打开Gmail然后刷新”。这两个功能使Just-Speak能够提供更直观，更高效的免视和免提交互。

本文的贡献包括：
•移动应用程序JustSpeak，可在Android设备上实现通用语音控制;
•描述系统设计，赋予适应性命令解析和链接的适应性; 和
•讨论如何利用言语增强盲人和敏捷问题人士的互动。

## 相关工作

### 非视觉交互
在过去的二十年中，许多屏幕阅读器[1,4,9]已成功地为多个平台上的盲人用户改进GUI可访问性。然而，盲人用户仍需要适应需要发现目标的传统输入技术。在非触摸设备上，它们有十个使用键盘快捷键以线性（从上到下，从左到右）遍历界面来查找对象，并在触摸界面上使用类似的手势。这些互动技巧经常无法满足盲人用户的需求，因此，他们为解决这些情况而自发开发了许多解决方法和策略并不令人惊讶[5,14]。还投入了许多研究工作来解决盲人用户的交互障碍，特别是在多点触摸屏上[8,10]。对于不使用屏幕阅读器的有视力的人来说，他们几乎不可能在非视觉上与他们的设备进行交互。虽然这对他们来说通常只是滋扰，但有时会造成很大的不便，即当有人想要在开车时检查地图时。

### 语音控制系统
我们将语音控制系统定义为通过人声控制的应用程序或设备。所有主流智能手机现在都支持不同级别的语音控制[15]。最先进和最受欢迎的语音控制应用程序是Google Now和Siri。

Google即时是Android上的对话系统（4.1及更高版本），支持在设备上执行一系列操作，包括大多数Google产品的功能。 [6]苹果公司首次将简单的语音控制功能引入iOS作为iOS 3的一项新功能，随后他们与Nuance合作将Siri [2]引入iPhone 4S和更新的模型中。

Google Now和Siri受限于他们定义命令的方式。实质上，每个命令只能有一个指定预定义函数的关键字或短语，例如“日历”。如果没有关键词或句子不满足语法，则话语将被视为网络搜索查询。因此，他们不能使用第三方应用程序。另外，如果用户想要执行多个命令，他/她必须多次重复该过程。

### Android Accessibility API
Android可访问性API [13]为开发人员提供了改善对具有特殊需求的用户的访问能力的能力。借助这些API，开发人员可以使自己的应用程序更易于访问，或者提供可访问性服务，从而为其他应用程序提供增强功能。

### JustSpeak
JustSpeak是一款Android无障碍服务，专为适用于Android 4.2以上的任何现有应用程序和辅助服务（例如TalkBack）而设计。使用JustSpeak的交互操作非常直观，可供盲人用户完全访问。它已经在Google Play商店免费发布。

在本节中，我们首先讨论JustSpeak如何处理单个命令语音，然后描述支持多个命令的系统设计。

### 系统描述
一旦安装，JustSpeak可以在Settings - > Accessibility下启用，这个操作只需要一次完成。 JustSpeak也可以在那里禁用。

![enter description here](./images/2018-06-05 23.33.17.png)
如图1所示，JustSpeak有三个模块。首先是语音识别，然后话语分析将识别结果处理成命令。最后，我们使用命令参数在屏幕上搜索可操作对象，并操纵最高匹配对象或相应地启动系统命令。

JustSpeak在睡眠模式下运行时没有被使用，因此功效非常高。当用户想要发出语音命令时，可以通过拖动主页按钮或扫描NFC标签来轻松激活JustSpeak。然后提供视觉和音频提示以提醒用户激活。为了让有视力的用户轻松发现有效的命令，JustSpeak简要说明激活后每个可操作对象顶部的标签。盲人用户通过屏幕阅读器提供的UI的口头表达直观地学习有效的命令。

### 语音识别
JustSpeak使用Google ASR服务，除了可靠的性能外，Google ASR还为开发者提供了离线和在线识别的灵活性[11]。因此，JustSpeak可以在没有互联网连接的情况下使用。当然，使用离线识别时，在线识别具有多种得分结果而不是单一结果。例如，在用户说“设置”的试用期间，Google在线ASR返回了三个不同的结果：“设置（0.90），设置（0.08），坐下（0.02）”。这个特性使JustSpeak能够增加语音识别误差和语音命令的成功率。

### 话语分析
JustSpeak支持语音控制​​所有由Android可访问API支持的命令以及一些全局系统命令（如说明1中所列）。

JustSpeak具有灵活的基于语法的解析过程。命令可以用不同的方式表达，例如人类之间的通信。当JustSpeak从ASR接收到评分结果时，它会尝试使用定义的语法处理每个结果。一旦语音识别结果通过了语法检查，我们将其以命令名和参数的形式包装起来，然后将其传递给执行模块。

### 命令执行
大多数全局命令可以直接执行。但是，本地命令有与屏幕控制相关的参数。为了查找本地命令的可操作对象，我们在JustSpeak中维护一个视图索引器，这个索引器是一个映射文本和相关接口元素的散列表映射。由于屏幕内容不断更新，JustSpeak监听可访问性事件2并动态更新索引器。

当本地命令到达时，执行模块查询索引器及其参数以查找匹配节点。由于用户输入并不总是与标签匹配，所以我们使用基于灵活字符重叠的排序算法。例如，对于命令“撰写邮件”，“撰写新邮件”的得分高于“显示邮件”。一旦索引器返回一个节点，Just-Speak验证是否可以对其执行该命令，如果不是，则继续到较低等级的节点。

如前所述，在线ASR返回多个结果成为多个命令，JustSpeak试图按降序排列顺序来处理每个结果。语音反馈在执行命令时默认提供。

### 命令链接
命令链接的支持是JustSpeak的一个重要特性，有两个原因。首先，组合多个命令比重复对话轮回更有效;其次，它更自然，并与自发演讲的方式一致。在JustSpeak中，所有支持的函数可以链接成一个句子，然后解析成一个命令数组。这里的挑战是消除歧义，即句子'点击重置和家'可以被视为一个命令：点击按钮'重置和家'或两个命令：点击'重置'按钮，然后进入主屏幕。为了克服这个挑战，每个支持的操作的语法都有详细的定义，JustSpeak也为当前屏幕上可以验证的命令分配更高的优先级。因此，如果有'重置'按钮，那么这两个命令的结果将是首选。由于一个动作的执行通常会导致一些接口更新，所以这个命令数组不能同时执行。实际上，执行模块只会尝试处理第一个命令，然后等待，直到前一个命令触发的所有事件都已解决，然后继续执行下一个命令。链接命令的效率在很大程度上取决于设备的处理接口更新速度。 ASR只需要非常少量的时间，这几乎与语音长度无关。

### 使用案例和讨论
JustSpeak通过语音控制的方式创新性地为所有Android机器人应用程序和Android系统本身提供增强功能，可以在整个平台上以非视觉和免提的方式进行访问。其价值不仅限于帮助盲人用户。

### 对于盲人用户
作为非视觉交互技术的主要用户群体，我们相信Android的盲人用户可以使用JustSpeak更快更轻松地与他们的设备进行交互。在Android上，JustSpeak不会干扰现有的屏幕阅读器，但可以与他们一起工作。我们观察到盲人用户通常花费大量时间在移动界面上查找对象。主要原因是屏幕阅读器被设计成线性屏幕阅读器，尽管盲人用户通常有策略来加速与屏幕阅读器的交互，但他们仍然需要更多的时间和精力才能找到目标。 Just-Speak可以减少为盲人用户访问应用程序控制所需的时间和精力。一个简单的例子是，盲人用户从JustSpeak中受益良多，正在推出应用程序。通过应用程序图标页面来浏览它通常是一场噩梦。在JustSpeak的帮助下，此操作可以像说出应用程序名称一样简单。 JustSpeak发布之后，我们注意到许多盲人和未成年人都将其用作常规应用程序启动器。

### 针对近视用户
有见地的用户经常发现他们不可避免地被置于需要非视觉或免提交互的情况下。 JustSpeak是在这些情况下完成紧急任务的有效替代方案。在正常情况下，JustSpeak也可以省却麻烦点击几个级别，通过链接命令查找常用功能。发布JustSpeak后，我们观察到许多用户开发和共享的命令链。

例如，TalkBack的开关隐藏在3层设置应用程序的最后一页，我们的一个用户创建了该页面的快捷方式，并且能够启动快捷方式并使用一个句子打开/关闭对话。许多其他用户适应他的策略，并评估说它更容易。

从我们收集的用户反馈中，我们发现了另一个意外用户组，这也从JustSpeak中受益。我们的一位用户指出，JustSpeak也是“敏捷问题任何人”的绝佳工具。对于他们来说，在多点触摸屏上用手指精确指向对象通常是一项艰巨的任务，JustSpeak可以减轻他们移动设备的负担，以便他们可以将它放在可以激活JustSpeak的位置，并且使用口语命令来执行交互。

## 讨论
如上所述，我们已经在Play Store上发布了JustSpeak作为测试版3。自2013年10月以来，我们已经有数百个用户，他们给了我们很多有意义的建议4，总体反馈是积极的。

作为一项可访问的服务，JustSpeak依赖于屏幕控件的标签。不幸的是，应用程序开发人员通常对可访问性的优先级低于其他功能。他们的粗心往往会导致残疾用户的诉讼和障碍。我们相信，通过设计和推广可使更多用户群体受益的JustSpeak和其他服务，我们可以让开发人员更加了解可访问性需求。

类似于JustSpeak的系统设计可以在Android以外的平台上轻松应用。所需的基本支持是系统层和应用层之间的委托层，它与JustSpeak中的访问可用性API具有相同的作用。通过用户的权限，该层需要能够调用接口和系统命令。它还需要监视接口内容和事件并将更新传递到已注册的应用程序。对于该层存在或可以构建的操作系统，可以使用相同的三个模块架构来实现通用语音控制。

### 未来的工作
我们已经多次更新JustSpeak，以根据用户反馈添加新功能并修复问题。我们计划继续倾听我们的用户，并对他们的使用行为进行系统的研究。除了维护和改进JustSpeak以提高其可用性外，我们还希望通过添加更多的语言支持来吸引更多的用户。

我们还在探索激活Just-Speak的其他技术，最近一些移动设备已经配备了总是聆听热词识别功能，例如在Motorola X上，用户可以通过说“OK，Google”来发起Google语音搜索。我们正在研究在JustSpeak中使用相同技术的可能性，以实现真正的纯语音交互。

## 结论
在本文中，我们介绍了Android上通用语音控制助手JustSpeak的系统设计和使用案例。 JustSpeak的贡献是双重的。首先，它通过综合从屏幕上下文中设置的命令，为在移动系统上运行的所有应用程序提供增强。其次，它支持链接多个命令，从而实现更自然和无缝的交互体验。作为向公众开放的应用程序，JustSpeak可以通过通用的免提和免提语音控制移动设备，为大量用户带来好处。用户反馈显示Just-Speak受到真实世界用户的欢迎。其框架可能有助于塑造未来的语音控制设备。