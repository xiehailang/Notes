# 2016：What Can I say? Addressing User Experience Challenges of a Mobile Voice User Interface for Accessibility

**摘要**：语音在移动设备上，为方便用户，常被用来增强或补充基于触摸的交互。但是，对于双手残疾的人来说，语音会在某些情况下帮助他们与移动设备进行独立的交互。对于这些用户来说，允许完全免提通话的移动语音用户界面（M-VUI）将提供高度的可访问性和独立性。实施这样的系统需要解决语音交互长期存在的可用性挑战，这些挑战是难以学习和发现语音命令，且影响用户体验。在本文中，我们解决了这些问题，论述了为提高Android平台上开发的M-VUI应用程序的语音命令的可见性和可学性而进行的研究。我们的研究确认了语音交互的长期挑战，同时探索了改善语音引入和学习语音命令的几种方法。基于我们的发现，我们为M-VUI的设计提供了一系列的影响。
**关键词**：Accessibility; Voice user interfaces; Universal voice control

## 简介
在移动人机交互中使用语音作为控制模式是无处不在并且不断增长的。例如，大多数主要的移动操作系统通过语音命令向智能助手（如Google Now，Siri和Cortana）提供信息访问。此外，通过语音听写的文本输入已成为智能手机的标准功能。这些语音功能为移动人机交互设备的移动环境提供了备用控制模式，这种模式通常会引入情景障碍，例如在驾驶时受到有限的视觉注意或在某些活动期间手的可用性受限。在这些情况下，语音交互对用户而言可能比物理交互更方便;然而，人机交互设计的一般最佳实践和交互设计建议不要将语音作为主要的交互模式，因为物理交互通常被认为是最有效的[3,13]。另一方面，对于手部灵巧有限的人来说，这种动态是相反的。对于这些用户来说，作为主要控制模式的语音可能是最有效的交互形式，或者在极端情况下是唯一可行的交互方式[11]。因此，可接入性HCI研究人员已经探索使用语音用户界面（VUI）作为主要控制模式。这已在各种情况下完成。例如，Sears [9]开发了一个基于语音的光标来控制和导航桌面计算机接口，Harada [17]开发了一个系统“VoiceDraw”，允许在计算机上进行语音驱动的自由图形绘制，而Soronen等[27]在电视指南界面的语音控制。

虽然可访问性研究已经在桌面计算领域的VUI方面取得了重大进展，但移动HCI已经提出了尚未解决的新挑战和用例。此外，尽管在桌面VUI上完成的一些研究可以推广到移动设备，但大部分研究并不直接适用。总的来说，移动设备HCI为交互设计[29]和可访问性[20]提供了独特的挑战，这需要研究和设计针对这些条件。最近，张等人在介绍JustSpeak应用[33]的无障碍移动HCI方面取得了重大进展。 JustSpeak是一个移动语音用户界面（M-VUI）应用程序，允许对Android设备进行完整的语音控制。 JustSpeak通过允许语音交互取代触摸手势来执行常见的移动设备活动，例如启动应用程序，导航，撰写和发送消息以及拨打电话，为手部灵活度有限的用户提供前所未有的访问和控制级别。

尽管像JustSpeak这样的M-VUI应用程序具有高度的可访问性，但对于手部灵活度有限的人来说，这在某种程度上是一把双刃剑。首先，语音交互作为移动设备导航的主要控制模式对于用户而言仍然是新颖且不熟悉的。除此之外，一般存在长期存在的可发现性和语音交互可学性问题[14]。语音命令的可发现性是任何使用语音作为输入模式的应用程序的基本挑战[21,32]。用户通常会有不一致的和不准确的心理模型，说明与系统交互的内容可以说什么也不说。语音作为一种输入方法的短暂性不允许直接操纵交互的相同水平的学习和可发现性，这些直接操纵交互通过可供性和隐喻来指导用户[1,26]。例如，[25] [27]西尔斯表明，不恰当的语音命令的使用在语音听写应用中是一个重要的可用性问题，因为用户很难发现和学习命令。 Feng等人在一项类似的研究中发现，即使将用户暴露给命令用户列表后，他们也会忘记或者仍然误用命令。 Hu [18]和Feng [12]发现，超时用户在命令发现和使用方面获得了高效率，指出它处于语音交互的初始阶段，用户需要最多的帮助才能有效地将其用于正确使用。总之，这些作品表明，为了建立更有效的语音交互模型，需要以用户为中心的研究和明智的设计。

在本文中，我们提供了一个移动语音交互设计案例研究，旨在提高未发布的名为VoiceNavigator的M-VUI应用程序代码的可发现性和可学性。 VoiceNavigator最初的可用性研究表明，用户面临有效和令人满意的交互的几个挑战。根据最初研究的结果，开发并测试了VoiceNavigator的原型版本，该版本的特征和功能通过调整以前的HCI关于软件可学性和可发现性的研究而得到了通知。我们结束我们的论文，描述了M-VUI交互设计的可发现性，可学习性可访问性的几个设计含义。

## 相关工作

### VUI的易学性和可发现性
可学习性是技术整体可用性的关键方面之一[23]。根据Grossman [7]的研究，可学习性被定义为“新用户可以轻松开始有效的交互并实现最佳性能”。可学习性通常用用户达到合理使用熟练程度所需的时间来衡量。这个时间方面很重要，因为在用户最初遇到技术时可学习性是最具挑战性的[23]。
Chen [15]指出了几个可共同促进可学性的因素：
培训/教程的可用性和有效性
系统积极协助用户变得精通使用的能力
用户过去的经验和技能程度
系统的有效反馈和可行性
用户在过程中遇到的困难程度

### 发现系统功能
最后一点，可发现性对于语音交互而言特别困难，因为它们本质上是不可见的。 Yankelovich [32]讨论了语音交互的短暂性如何在可学习性和可发现性方面引入两个基本挑战：
1.用户会认为系统可以理解得比实际能力更多
2.用户将不知道可用的功能。

Karsenty进一步讨论了VUI的不透明特性如何抑制用户生成精确心智模型的能力[21]。事实上，智力模型的形成，可发现性，可学性和技术的整体可用性之间存在直接关系。更具体地看待可发现性的作用揭示了它如何影响诺曼[24]的几个设计原则。例如，考虑映射的原理，它指出一个控制应该适当地关联到它在世界上的影响。良好的映射需要利用“物理类比和文化标准”的优势，这反过来又简化了可学习性和可发现性。在VUI中映射语音命令要复杂得多，因为缺乏自然语言中的物理类比和各种各样的文化标准。在VUI中实现映射的最广泛使用的方法是所谓的“说出你能看到”的方法[32]，这就是说，任何可用的语音交互都应该在界面上清晰标记和可见。 

Christian等[8]和James [19]的工作都提供了这种技术的例子。这已经证明对于桌面应用是有效的，但是在不具有相同数量的屏幕空间的移动设备上难以实现以充分地标记每个可能的交互。 Norman的约束原则出现了另一个挑战，那就是物理强制函数用于限制特定时间的可能交互，以简化用户体验。语音交互更难以约束。提示[31]和反馈[28]已被VUI研究人员用于限制语音交互，但与诺曼描述的物理约束的有效性相比，这些只能提供近似值。最后，Affordance原则是一个对象的属性，它提供了有关如何与它们交互的概念信息。语音控制的飘渺本质使得人们对可供性的认识几乎不可能。

总之，VUI研究人员采取了许多不同的方法来解决Yankelovich和Karsenty描述的语音交互的基本挑战。此外，HCI研究具有丰富的可学习性和可发现性的技术和方法，这对于VUI尤其如此的技术在最初的用户体验中最为关键。对于这里的工作，我们感兴趣的是应用这些知识体系来提高VoiceNavigator的可学性和可发现性，VoiceNavigator旨在为手部灵活度有限的人提供可访问的手机使用。我们的工作表明，解决桌面语音交互设计的易学性和可发现性的技术和设计原则在M-VUI环境中受到限制。我们将在用户研究中详细说明这些限制，以及我们如何试图在我们的原型设计中解决这些限制。在下一节中，我们将介绍VoiceNavigator应用程序，然后介绍结果用户评估，以便我们探索替代交互设计技术。

### 语音导航器描述
VoiceNavigator是目前正在开发的M-VUI应用程序（图1）。 VoiceNavigator利用语音识别来提供模拟触摸手势的语音交互，从而允许手部灵活度有限的用户执行常见的移动设备活动，例如启动应用程序，导航，撰写和发送消息以及拨打电话。 VoiceNavigator在操作系统级别工作以识别当前屏幕中可用的所有可能交互。例如，通常在电话的主屏幕上启动电子邮件应用程序，然后刷新收件箱中的最新消息。要启动电子邮件应用程序，必须物理双击图标，然后找到并选择刷新选项。对于有强烈手部震颤的人来说，执行该序列可能会很困难且耗时。 VoiceNavigator允许用户通过语音命令执行相同的任务。为此，用户需要说：“打开电子邮件”，然后“刷新”来更新收件箱。此外，VoiceNavigator还提供了一系列全局操作，可以从任何屏幕进行导航（例如，“回家”返回到主屏幕），修改设备的状态（例如“打开Wi-Fi”），显示系统窗口（例如“打开最近的应用程序”），以及启动应用程序。用户可以说“帮助”或“我能说什么？”来打开一个菜单，其中包含语音命令列表和访问教程。除了说出应用程序的名称或所需的交互外，VoiceNavigator还提供了叠加在屏幕上图标上的编号标签。例如，在电子邮件应用程序中，所有可用的功能（刷新，撰写，草稿等）通常由各种图标以图形方式表示。在这些情况下，可能不会立即清楚可用的功能，因为图标可能带有或不带有文本标签。为了在这些情况下帮助用户，VoiceNavigator在每个功能旁都放置了一个小数字标签。例如，在图1中，用户可以说“电话”或数字“2”来调出拨号菜单。

### 初步用户评估
这项研究的目的是观察VoiceNavigator在第一次互动中新手有限的灵巧手。该研究旨在回答以下问题：
Voice Navigator的可用性如何提高？
用户是否知道该说什么来浏览VoiceNavigator？
用户是否发现VoiceNavigator的核心功能？
VoiceNavigator教程是否使参与者能够独立使用应用程序？
我们通过与当地特定震颤组，康复中心和帕金森氏病协会合作招募了9名参与者，这些参与者有各种运动障碍，限制了他们的手的灵活性（见表1）。

### 方法和参与者
我们进行了10次可用性研究会议（每次90分钟），参与者因各种运动障碍而难以或无法使用智能手机，因为他们无法轻松操作触摸屏。研究在配备视频的UX实验室进行。音频和视频文件从每个会话收集并得到参与者的许可。 VoiceNavigator软件已在运行操作系统Android Kitkat的Nexus 5 Android设备上进行测试。
在简短的介绍之后，参与者完成了首次激活应用程序时自动启动的VoiceNavigator教程。教程完成后，参与者被允许在被指示完成一组常用用例之前自由地探索应用程序。示例用例是切换到不同的Wi-Fi网络，撰写电子邮件并创建详细的日历条目。鼓励与会者阐明问题，并在他们无法完成特定任务时提供协助。最后，参与者被要求反思他们的经历，提供反馈，并提出如何改善用户体验的建议。

## 结果

### VoiceNavigator的可用性如何提高？
检测到的最大可用性问题之一是VoiceNavigator在研究时无法提供连续的聆听模式。参与者希望在任何时候都能听到和理解，只要他们继续讲话，即使在暂停反思之间，也应该听取他们的意见。参与者不喜欢由于每个触摸目标带有一个盒子和一个相关联的数字而引起的视觉混乱。用户偶尔甚至错过了相关信息，因为部分视觉界面被覆盖层遮挡了。当从导航切换到听写模式时，用户不确定他们的语音输入被视为口述文本（例如，“然后我希望你回家”），而不是导航命令（“回家”导航回到主屏幕）。

### 用户是否知道该说什么来浏览VoiceNavigator？
我们发现，用户在尝试弄清楚发生什么事情以便归档某个特定行为时，大部分人都在猜测。当屏幕上有许多没有明显名称/标签的视觉元素时，很难猜测该说些什么。有些用户会咨询“我能说什么？”（“WCIS？”）菜单。但并不是每个人都记得这个语音命令的文档对他们是可用的，以及为了打开它而说什么。 VoiceNavigator提供的数字系统被认为是一种便捷的回退模式。特别是当用户经历更长的用户旅程时，这些数字成为流行的快捷方式，弥补了用户不知道如何称呼某个触摸目标时的差距。一些用户制定了策略，思考他们将如何执行某种物理交互，然后将其转化为语音命令。

### 用户是否发现了VoiceNavigator的核心功能？
通过提供教程，指导新手用户的入职体验非常有效。所有用户都能够在手机的生态系统中应用稍后在教程中学到的命令。他们通过尝试附加命令增加了这方面的知识。一旦命令导致成功的交互，用户就会记住它并且经常能够在相似的情况下应用相同的命令。少数用户通过查阅“WCIS？”菜单在整个旅程中学习了更多命令。所有研究参与者都希望获得更全面的WCIS结构？菜单。

### VoiceNavigator教程是否使参与者能够独立使用该功能？
所有参与者在完成教程后都有信心尝试VoiceNavigator。他们能够在教程之后应用简单的命令，例如启动VoiceNavigator，滚动，通过数字浏览系统UI或者说明触摸目标的名称。在独立进入他们的应用程序之前，测试用户表达了对学习和获取练习机会的更大需求。为此，他们希望在最常用的应用环境中采用安全实践和试验模式。由于VoiceNavigator的特定交互模式对所有参与者来说都是新的，并且与以前的语音交互系统体验明显不同，因此一些用户表示希望以视频的形式介绍和演示核心功能。 “我能说什么？”命令的列表受到赞赏，但用户希望它的结构更好，与当前挑战具有上下文相关性，并始终在与系统交互的同时达到。教程可以为使用户在VoiceNavigator中执行第一步奠定基础。对于持续，独立和成功的互动，用户需要额外的支持，并在整个入职流程中提供帮助。

## 讨论
我们发现用户需要额外的线索，并有助于在复杂任务的环境中使用VoiceNavigator。特别是在初始交互中，用户基本上在猜测如何制定命令。他们以前使用语音交互系统的经验会影响他们的可能交互心理模型以及他们喜欢的交互风格。该教程对于使用户参与新的交互模型以及向他们传授产品特定细节（如与触摸目标相关的数字）至关重要。即使在被要求执行后续任务时，所有参与者都不会记住他们在教程中学习并应用的交互命令，但需要这些命令。他们愿意学习新系统并容忍系统的弱点和缺点似乎直接与损害的严重程度和用户需要将语音作为替代访问形式提供给他们。
根据这项研究的结果，很明显，需要增强可发现性和可学习性机制，以改善VoiceNavigator的用户体验。在下一节中，我们重点介绍一些我们开发的概念，以提高系统的可学性和可发现性。

## 改进焦点

### 学习“随时随地”
教程和培训材料的可用性和有效性是可学习性的关键要素。最初的研究表明，VoiceNavigator教程中涵盖的一些概念并未转移到实际使用中。我们考虑了Hakuline等人[16]的工作，该工作着眼于使用交互式辅导教师vs静态网络教程来训练用户与VUI交互的结果。他们进行了一个实验，在这个实验中，每个团队在使用VUI电子邮件应用程序之前都经过了培结果显示，使用交互式导师进行培训的用户开发出了更有利的系统心智模型。互动式导师在与系统互动的前20分钟内有效地改善了用户学习。

建立一个完整的互动式教练已经超出了这里的工作范围，但Hakuline研究的主要结论是，如果在实际使用环境中发生学习，学习似乎更有效。为了进一步告知我们的方法，我们考虑了Krilsler等[22]。他们的研究工作评估了如何为HotKey使用的教学提供内容相关的辅导。他们开发了一个名为“HotKeyCoach”的应用程序，将使用建议作为弹出提示发送给参与者。该应用程序通过集成到使用环境中，更有效地支持用户学习。

基于这些见解，我们决定将简介教程简化为三个屏幕，以便将学习直接转移到上下文使用中。我们希望应用导师能够使用类似于Hakuline介绍的会话语气，但最小的设计和Krisler的HotKeyCoach入侵。借鉴这些作品，我们对以下功能进行了原型设计（图2）：
共有八个导师信息。每条消息都涵盖了VoiceNavigator的关键交互。这些导师信息只会出现在主屏幕上。消息框会突出显示，然后完成后消失。

### 基于发现的学习
在我们最初的研究中，我们观察了用户如何采用猜测方法与Voice Navigator进行交互。似乎这种反复试验方法对于语音交互是一种自然的人为倾向，因为在之前的VUI研究中也观察到了这种倾向。我们有兴趣确定如何利用这种行为来提高可学习性;换句话说，通过可猜测性来提高可学习性。在[30]中，Wobbrock表示：“尽管用户对相关符号缺乏了解，但用户尝试执行手势，输入命令或使用按钮或菜单项的初始尝试必须成功。这需要高度的可猜测性。“为了探索利用可学习性的潜力，我们考虑了Discovery Based Learning，它首次引入了学习心理学领域[2]，但已经发现HCI研究人员寻求提高可学习性的许多应用程序[5]。以发现为基础的学习“鼓励通过探索与环境相互作用，与问题搏斗并进行实验来进行学习。 [10] Dong等人[10]运用这个概念在Adobe Photoshop中开发一个“Jigsaw”学习游戏，旨在教会用户如何使用该软件的工具和技术。游戏促进了游戏化，游戏化的学习。

基于Dong的工作，我们对以下功能进行了原型设计（图3）：这些“发现提示”旨在提供有关可猜测性的反馈和指导。通过提供命令的确认并揭示其他类似命令的存在，我们希望以更有条理的方式鼓励发现和猜测。每当第一次使用语音命令时，发现提示将从屏幕的底部滑入。

### 情景化帮助
“我能说什么菜单”中的命令列表的结构和用途是另一个需要改进的领域。用户希望帮助材料能够处于上下文位置，而不是通常可以使用的静态命令菜单。此外，甚至命名命令来激活菜单“我能说什么？”是有问题的，因为它没有传达预期的功能。我们观察到，用户在词语“我能说什么？”这句话时毫不夸张地说，在当前情况下向系统提出问题;如“我可以在这里说什么？”，而不是“我可以说什么一般？”Carroll等人[6]也提到了情境化，用户相关帮助材料的重要性。在两个项目中，最小手册[6]和指导性探索[4]中，Carroll展示了如何设计帮助材料，以提供与手头任务或目标相关的即时援助，而不是对系统进行全面和基本的学习。

基于Carroll的工作和我们自己的研究成果，我能说的手册被重新设计，如下图所示（图4）：新菜单是围绕当前上下文中可用的操作设计的（帮助菜单项目在电子邮件中会有所不同应用程序与日历应用程序）。

## 原型用户评估
我们进行了第二次用户研究，以获得关于我们新的可学习性和可发现性功能的设计和功能的初步反馈。我们旨在回答以下研究问题：
应用内教程信息是否提高了对命令的了解？
发现消息是否提高了对命令的了解？
上下文特定的“我能说什么”菜单提高了对命令的了解吗？
新的介绍体验如何影响初始学习？

### 方法和参与者
我们共进行了五次研究会议（每次90分钟），参与者因各种运动障碍而限制了他们的手的灵活性（见表2）。 VoiceNavigator的原型被用于运行Android Marshmallow操作系统的Google Nexus 5设备上。我们决定为这项研究招募新的参与者，以避免以前与VoiceNavigator的互动带来的潜在影响。与之前的研究类似，参与者首先完成了教程，并允许以非指导的方式探索应用程序几分钟。然后，我们指示他们完成与之前研究中概述的完全相同的任务。每个研究课程结束时都会向与会者反馈和反思阶段。

## 结果

### In App Tutorial消息是否可以提高对命令的了解？
所有参与者都能记住和使用导师介绍的命令。他们还成功完成了所有In App Tutor消息。有几位用户表示担心能否解雇邮件，因为他们害怕他们可能再次需要这些信息，并且不知道如何检索邮件。我们还发现教师信息没有明显混淆界面。 In App Tutor消息缩短了漫长的学习体验，将学习体验成功转移到应用环境中，并提供适用于日常应用使用的直接体验。

### 发现消息是否提高了对命令的了解？
我们发现这些发现消息围绕着用户的注意力进行竞争，并使他们感到匆忙。参与者报告觉得他们可能错过了某些东西。其他人则认为这些消息在那个特定时刻与他们无关，因为他们没有包含有关他们确切应用交互的有用信息。虽然这些信息没有激励用户以有指导的方式进行探索，但一位用户说：“也许我不在乎我做了什么，只要我做了成功”（P4B）。

### 做具体的背景“我能说什么”（WCIS）菜单提高命令的知识？
所有参与者都对情景化的WCIS菜单感到高兴，因为它经常包含对他们直接适用于他们目前的挑战的提示。我们发现用户希望命令可以在菜单中执行。向前移动菜单需要清楚显示可滚动内容以及解除选项。一位用户表示他们喜欢以下方式：“我可以看到这是我一直在使用的东西，因为它易于访问且易于解雇。” （P3B）。

### 新介绍体验如何影响初始学习？
新的介绍经验提供了清晰和精简的体验。使用这两种选项进行比较的用户更喜欢新版本，因为它更加注重实践并在现实应用环境中显示练习。与此同时，用户的反馈意见表明数字的视觉显着性需要改进。所有用户在完成介绍后都能够独立完成基本的导航和选择任务：“这看起来非常精致;我期望从专业应用程序中获得”（P4B）

## 讨论
新教程提供了简化的入职体验，为用户进行首次互动提供了准备。未来的工作将需要量化教程长度的最佳截止点。所有用户都喜欢这种情境化的“我能说什么”菜单，以便在需要时快速访问相关资源。 In App Tutor Messages受到赞赏，但其对用户效率的影响尚无定论。由于视觉注意力范围有限且用户总体上不认为内容相关，因此发现消息的效果低于预期。向前推进VoiceNavigator应该尽可能地将尽可能多的学习内容转移到真实的应用环境中。与此同时，研究帮助用户管理他们注意力的概念并将他们的注意力集中在那些在任何特定时刻与他们最相关的交互命令将是至关重要的。

## M-VUI设计的含义

### 情景化帮助
情境化帮助功能可能是M-VUI环境中可学习性和可发现性最有用的资产。帮助内容应围绕在当前情况下可用且相关的行动而非一般信息。此外，帮助中显示的每个操作应该可以从菜单屏幕中操作，而不是让用户关闭菜单，调出正确的命令，然后说出来执行操作。允许用户在菜单屏幕中执行操作可减少认知负担并降低执行操作所涉及的步骤数量。从设计的角度来看，这意味着菜单应该采用透明叠加层的形式，为用户提供可用的操作，而不会明显遮蔽当前的屏幕环境。
总体而言，我们的研究结果表明，M-VUI的入职培训和学习经历需要针对行动而非整体知识进行设计。 Carroll等人[5]在描述“活动用户悖论”时提出了一个有用的方法来解释为什么这很重要，其中：“新用户在引入应用系统时倾向于直接跳入。如果他们的培训材料中提到了一项操作，他们希望立即尝试。反对的描述和实践遭到抵制......“在M-VUI的背景下，活跃用户悖论似乎特别流行。这可能是对移动人机交互设备的上下文和快速交互的自然回应。换句话说，用户在移动人机交互界面学习的耐心水平可能比坐在桌面计算机前的人要低。这表明在学习能力领域以及设备（桌面与移动设备）和交互风格（语音与直接操作）如何影响它的其他研究。

### Key-Takeaway:
M-VUI帮助材料应该围绕特定情况下的可用行为和相关行为进行设计。此外，行动应该在帮助材料内执行，而不是在退出后有额外的步骤来调用命令。

### 同化偏见
与主要移动操作系统上的其他流行语音应用程序（Google Now，Siri）不同，VoiceNavigator不作为提供口头反馈或接受对话输入的会话代理。相反，VoiceNavigator作为一项实用功能运行，只有一组有限的命令和范围。虽然它确实允许一些高级别的全局命令和命令的同义词，但它不是为高级自然语音交互而设计的。这是有问题的，因为用户假设从其他普遍可用的会话代理（Siri，Cortana）到VoiceNavigator的交互的心智模型。这也被称为“负转移”，即当前学习受到先前经验的抑制。 Carroll等人[5]讨论了消极转移如何产生“同化偏见”：“可以误导用户系统如何工作，但也可能会在某种程度上误导用户，使他们无法充分预测可用功能。先前知识的这种负面影响可能会特别虚弱，因为学习者通常可能完全不了解问题。“
尽管自然语言和会话反馈对于信息查询非常适用，但在VoiceNavigator寻求实现完全免提控制和导航的环境中，更有限的命令词汇可能更为有效。有限的命令词汇往往比会话式（在语音识别错误率方面）更准确[14,25]。然而，最终不管哪种形式的交互更适合于使用环境（会话vs命令），对于M-VUI而言，似乎至少从用户体验的角度来看，会话风格是优选和期望的。这激发了开发团队目前的研究工作，探索VoiceNavigator如何以更加对话的方式运作。

### Key-Takeaway:
任何M-VUI的设计都应该考虑到会话语音代理的经验会如何影响用户的期望，行为以及最终对新应用程序的满意度。

### 设计M-VUI以实现有限的视觉注意
围绕移动设备的有限屏幕空间进行设计是移动交互设计人员所熟知的问题。 Voice Navigator的初始设计除了与其关联的数字标签外，还绘制了突出显示可操作项目的方框，从而概括了屏幕上的所有可用操作。如图所示，在我们进行的第一项研究中，当屏幕变得混乱造成重大混乱和沮丧时，这种设计方案可能很难实现。
我们通过在原型版本中引入更小的设计来解决这个问题，该原型版本仅在没有网格结构的情况下使用数字标签。这似乎是一个有效的设计选择;用户在接触这两种设计时都会比较偏爱新设计。虽然这一新设计在改进视觉设计方面迈出了一步，但引入了两项新功能：向屏幕上半部分显示的导师消息和从屏幕底部向上滑动的发现消息无意中引入了新的功能挑战。虽然这些技术已被证明在桌面环境中用于学习和培训方面很有效，但由于屏幕空间有限和视觉受到关注，因此它们在移动设备上显得不太合适。

### Key-Takeaway:
M-VUI界面设计应该考虑到有限的屏幕空间的最小设计方法，并且要考虑到不会超出用户的视觉注意范围。

### 语境中的训练
最初的研究建议在实际使用之前提供广泛的教程对学习无效。意识到这一点，我们试图通过应用内导师信息将学习转移到实际使用环境中。此外，我们希望探索技术来协助用户的猜测和试错方法的自然倾向。此前对基于发现的学习的研究似乎是一种有希望的方法。不幸的是，由于屏幕空间和有限的视觉关注范围，我们特定的基于发现的学习实施提出了新的挑战。因此，很难对这些方法的有效性提出强烈要求。


### Key-Takeaway:
M-VUI最初的培训应该通过提供一个简要的概述，然后将学习转化为使用背景来寻求引导用户进行交互的平衡。基于发现的学习似乎是一种很有前途的技术，但需要探索如何有效实施它的各种方法。

### 完整的移动可访问性
如上所述，在隐形话音接口的环境中，易学性和可发现性特别具有挑战性。当涉及到无障碍需求的用户时，情况就更具挑战性。对于大多数主流用户来说，语音交互提供了便利，并为他们的移动设备提供了一种对他们非常重要的事情。相比之下，对于严重运动障碍影响双手灵活性的用户而言，M-VUI可以是一种授权体验，可以进行复杂的交互，如打开，阅读，回答，转发和存档电子邮件对话。这代表了端到端的可访问性，而现有的通过Siri或Google NOW进行的移动语音交互并不能为所有任务提供完全免提交互。我们鼓励研究界从那些无法弥合当前移动语音交互软件差距的人的角度思考完整的用户体验。 VoiceNavigator具有弥补这些差距的巨大潜力，并最终实现真正免提的M-VUI。

### Key-Takeaway:
在设计M-VUI时，无障碍研究人员应考虑手部灵活度有限的用户的整体交互需求。

## 结论
随着移动设备和语音交互的使用不断增加，移动HCI研究需要解决可学习性和可发现性方面的具体挑战。我们在本文中的工作提供了一个案例研究，描述了我们努力提高M-VUI应用程序的可学性和可发现性，代码为VoiceNavigator，旨在为手机提供完全免提的语音控制访问。我们最初的用户评估强调了VoiceNavigator的几个可用性挑战。我们试图通过以往关于可学性，可发现性和VUI交互设计研究的原型概念来解决这些挑战。我们发现虽然以前桌面HCI的研究可能对灵感或初始起点有用，但某些特定技术并不能直接适用。我们主张专门针对移动领域的语音交互设计理论的未来发展。随着移动HCI在公平和规模上的持续增长，该领域的时间已经到来，以确定其自己的理论，而不是不得不从桌面HCI中不断借用和翻译。正如这项工作所显示的，这种需求的一个范例是在语音交互领域。语音交互对于移动HCI具有很大的希望，但在许多方面仍然是一个新的前沿。在这篇论文中，我们探讨了一些手语灵活性有限的人在语音通达方面的可能前沿。我们预计随着理论和设计原理的发展，我们将探索其他应用领域，并与其相伴随。

## 参考文献
1. James H. Bradford. 1995. The human factors of speech-based interfaces: a research agenda. ACM SIGCHI Bulletin 27, 2: 61. http://doi.org/10.1145/202511.202527

2. Jerome S. Bruner. The act of discovery.

3. Ron Van Buskirk and M LaLomia. 1995. A Comparison of Speech and Mouse/Keyboard GUI Navigation. Conference companion on Human factors in: 89791. Retrieved from http://dl.acm.org/citation.cfm?id=223447

4. John M. Carroll, Robert L. Mack, Clayton H. Lewis, Nancy L. Grischkowsky, and Scott R. Robertson. 2009. Exploring Exploring a Word Processor. Human–Computer Interaction 1, 3: 283– 307. http://doi.org/10.1207/s15327051hci0103_3

5. John M. Carroll and Mary Beth Rosson. 1987. Paradox of the Active USer. In Interfacing Thought: Cognitive Aspects of Human-Computer Interaction. MIT Press, 80–111. http://doi.org/10.1017/CBO9781107415324.004

6. John Carroll, Penny Smith-Kerker, James Ford, and Sandra Mazur-Rimetz. 1987. The Minimal Manual. Human-Computer Interaction 3: 123–153. http://doi.org/10.1207/s15327051hci0302_2

7. Fang Chen. 2006. Designing Human Interface in Speech Technology. Springer. Retrieved February
13, 2016 from https://books.google.com/books?hl=en&lr=&id=sjJ o_8QfEo8C&pgis=1

8. Kevin Christian, Bill Kules, Ben Shneiderman, and Adel Youssef. 2000. A comparison of voice controlled and mouse controlled web browsing. Proceedings of the fourth international ACM conference on Assistive technologies - Assets ’00: 72–79. http://doi.org/10.1145/354324.354345

9. Liwei Dai, Rich Goldman, Andrew Sears, and Jeremy Lozier. 2004. Speech-based cursor control:a study of grid-based solutions. Assets ’04: Proceedings of the 6th international ACM SIGACCESS conference on Computers and accessibility: 94–101. http://doi.org/http://doi.acm.org/10.1145/1028630.1 028648

10. Tao Dong, Mira Dontcheva, and Diana Joseph. 2012. Discovery-based games for learning software. Chi 2012. Retrieved from http://dl.acm.org/citation.cfm?id=2208358

11. J Feng, S Zhu, R Hu, and A Sears. 2011. Speech- based navigation and error correction: A comprehensive comparison of two solutions. Universal Access in the Information Society 10, 1: 17–31. http://doi.org/10.1007/s10209-010-0185-9

12. Jinjuan Feng, Clare Marie Karat, and Andrew Sears. 2005. How productivity improves in hands- free continuous dictation tasks: Lessons learned from a longitudinal study. Interacting with Computers 17, 3: 265–289. http://doi.org/10.1016/j.intcom.2004.06.013

13. Jinjuan Feng and Andrew Sears. 2004. Are we speaking slower than we type?: exploring the gap between natural speech, typing and speech-based dictation. ACM SIGACCESS Accessibility and Computing, 6–9.

14. G. W. Furnas, T. K. Landauer, L. M. Gomez, and S. T. Dumais. 1987. The vocabulary problem in human-system communication. Communications of the ACM 30, 11: 964–971. http://doi.org/10.1145/32206.32212

15. Tovi Grossman, George Fitzmaurice, and Ramtin Attar. 2009. A Survey of Software Learnability: Metrics, Methodologies and Guidelines. Proceedings of the 27th international conference on Human factors in computing systems (CHI’09): 649–658. http://doi.org/10.1145/1518701.1518803

16. Jaakko Hakulinen, Markku Turunen, and Esa-pekka Salonen. 2005. Software Tutors for Dialogue Systems. LNAI: 412–419.

17. Susumu Harada, Jacob O Wobbrock, and James A Landay. 2007. VoiceDraw: A Hands-Free Voice- Driven Drawing Application for People with Motor Impairments. 9th international ACM SIGACCESS conference on Computers and accessibility, ACM, 27–34.

18. Ruimin Hu, Shaojian Zhu, Jinjuan Feng, and Andrew Sears. 2011. Use of speech technology in real life environment. Universal Access in Human- Computer: 62–71. http://doi.org/10.1007/978-3- 642-21657-2_7

19. F James and J Roelands. 2002. Voice over Workplace (VoWP): voice navigation in a complex business GUI. Proceedings of the fifth international ACM: 197–204. Retrieved from http://dl.acm.org/citation.cfm?id=638285

20. Shaun K Kane, Chandrika Jayant, Jacob O Wobbrock, and Richard E Ladner. 2009. Freedom to roam: a study of mobile device adoption and accessibility for people with visual and motor disabilities. Proceedings of the 9th international ACM SIGACCESS conference on Computers and accessibility - Assets ’09, 115–122. http://doi.org/10.1145/1639642.1639663

21. Laurent Karsenty. 2002. Shifting the Design Philosophy of Spoken Natural Language Dialogue : International Journal of Speech Technology 5, 2: 147–157.

22. Brian Krisler and Richard Alterman. 2008. Training towards mastery. Proceedings of the 5th Nordic conference on Human-computer interaction building bridges - NordiCHI ’08: 239. http://doi.org/10.1145/1463160.1463186

23. Jakob Nielsen. 1994. Usability Engineering. Elsevier Science. Retrieved February 13, 2016 from https://books.google.com/books?hl=en&lr=&id=D BOowF7LqIQC&pgis=1

24. DA Norman. 2002. The design of everyday things. Retrieved January 12, 2015 from http://scholar.google.com/scholar?hl=en&btnG=Sea rch&q=intitle:Design+of+everyday+things#0

25. Andrew Sears, Jinhuan Feng, Kwesi Oseitutu, and Claire-Marie Karat. 2003. Hands-Free, Speech- Based Navigation During Dictation: Difficulties, Consequences, and Solutions. Human-Computer Interaction 18, 3: 229–257. http://doi.org/10.1207/S15327051HCI1803_2

26. Ben Shneiderman. 2000. The limits of speech recognition. Communications of the ACM 43, 9: 63–65. http://doi.org/10.1145/348941.348990

27. Hannu Soronen, Santtu Pakarinen, Mervi Hansen, et al. 2009. User Experience of Speech Controlled Media Center for Physically Disabled Users. Proceedings of the 13th International MindTrek Conference: Everyday Life in the Ubiquitous Era: 2–5. http://doi.org/10.1145/1621841.1621843

28. Stefanie Tomko and Roni Rosenfeld. 2004. Shaping Spoken Input in User-Initiative Systems. In Proceedings of the 8th International Conference on Spoken Language Processing (ICSLP), Jeju Island, South Korea.: 2–5.

29. Jacob O Wobbrock. 2006. The Future of Mobile Device Research in HCI. Access, 131–134. Retrieved from http://faculty.washington.edu/wobbrock/pubs/chi- 06-wkshp.pdf

30. Jo Wobbrock and Hh Aung. 2005. Maximizing the guessability of symbolic input. CHI’05 extended abstracts: 5–8.http://doi.org/10.1145/1056808.1057043

31. Nicole Yankelovich, Gina-Anne Levow, and Matt Marx. 1995. Designing SpeechActs. Proceedings of the SIGCHI conference on Human factors in computing systems - CHI ’95: 369–376. http://doi.org/10.1145/223904.223952

32. Nicole Yankelovich. 1996. How Do Users Know What to Say? Interactions 3, 6: 32–43.http://doi.org/http://dx.doi.org/10.1145/242485.242 500

33. Yu Zhong, T V Raman, Casey Burkhardt, Fadi Biadsy, and Jeffrey P Bigham. 2014. JustSpeak: Enabling Universal Voice Control on Android. Proceedings of the 11th Web for All Conference on - W4A ’14: 1–4.http://doi.org/10.1145/2596695.2596720