# Learnability through Adaptive Discovery Tools in Voice User Interfaces
**摘要**：VUI不可见的特性归因于VUI的可发现性具有挑战性。 可发现性低通常会导致可学习性问题。 研究人员为VUI设计了可视化工具，以帮助用户随时学习。 然而，很少有人使用适应来确保借助这些工具的可学习性超出了最初的使用范围。 我们设计了DiscoverCal，这是一款使用自适应发现工具设计的日历应用程序，用于提高VUI中的可学习性。 在本文中，我们确定了现有发现工具的关键特征。 我们提出了基于**上下文相关性**和**用户性能**的VUI设计，以便在初次使用之后扩展可学习性。 我们简要讨论我们的用户研究设计。
**关键词**：Voice User Interface; Learnability; Discoverability; Adaptive Interface
## 简介
我们的交互方式迅速发展，为键盘和鼠标之外的新互动模式腾出空间。语音用户界面（VUI）近年来已经显着成熟，现在已经融入到我们每天与智能手机，电视机和汽车互动的许多设备中。然而，尽管有这些最新的进展，VUI的主流使用仍然有限。最近的一项研究发现，尽管98％的iPhone用户已经测试过Siri，但70％的受访用户继续仅使用Siri“有时”或“很少”[13]。

VUI的“无形”特性可以挑战用户发现其能力和限制的能力[7,11]。当可发现性具有挑战性时，可学习性可能会受到影响。可学习性可以被描述为新手用户轻松学习如何使用新系统以最大化生产力，而无需任何预先培训的能力[7,8]。已应用不同的方法来改善用商用VUI进行发现，包括教程，伴随应用程序或用户手册文档。一些研究人员设计了一些工具来帮助用户学习[7,9,17]。然而，很少有人研究过这些工具的适应性会如何影响初次使用后的可学习性。

我们的目标是为语音控制日历DiscoverCal设计可视化自适应发现工具（ADT），以提高VUI中的可学习性。 ADT是帮助用户学习尚未发现的活动和命令的指南。我们使用API​​.AI进行语音输入和输出，以及用于视觉反馈的壁挂式显示器。 API.AI是一个平台，用于开发自然语言交互，如Facebook chatbots和亚马逊Alexa技能。我们专注于为这个项目建立与API.AI的语音交互，尽管我们相信我们的发现可以推广到各种类似的VUI。由于API.AI的开源特性以及该项目的易用性，因此选择了API.AI。基于用户性能，发现工具可以调整内容和可见性级别。 ADT的目标是在交互过程中向用户提供上下文相关的帮助，并根据改进的用户性能进行调整，以便学习如何使用系统以实现最高生产力。

本文概述了我们的设计方法，以解决VUI中可学习性带来的一些挑战。一个相关的工作部分强调了最先进的技术，其次是一个部分，标识在相关工作中发现的特征，可以通知设计过程的可发现性。然后，我们讨论我们如何整合适应性方法以提高可学习性。最后，我们介绍我们的研究设计和未来工作计划。

## 相关工作
对于新手用户来学习如何使用新系统，重要的是要他们首先发现其功能和局限性。可发现性是实现可学习性的一种手段[6,7]。 Tovi Grossman指出可学习性有两种类型，初始可学习性和可扩展可学习性[8]。初始可学习性是新手用户在初始任务期间表现良好的能力，而扩展可学习性则是他们能够很好地执行或提高性能[8]。

教程是应用于提高VUI中可发现性的最常用方法[10]。但是，他们依赖用户保留重要信息，并且稍后检索它可能会很麻烦。一些商业VUI使用不同的方法。例如，亚马逊的Alexa有一个视觉伴侣应用程序，其中列出了“要尝试的东西”，其中包括“新功能”和“发现音乐”等子菜单。尽管对初次使用有益，但随着用户熟悉该技术，基本菜单选项变得多余，并且用户立即需要的信息被埋在导航层之下。像亚马逊和谷歌这样的公司不断添加与其VUI兼容的新功能，这使得用户能够轻松地随时访问信息以及发现更多高级功能以扩展可学习性非常重要。在本节的其余部分中，我们将重点讨论两种提高VUI可学习性的方法：

1.随时了解方法：随时随地为用户提供信息，以便他们逐渐开发界面的心理模型[7]。
2.自适应方法：调整界面以满足用户的需求，以便延伸学习的初始使用范围[2，5]。

**随着你的方法学习**
随着学习方法的发展，强调了对交互过程中发现的接口工具的需求。许多项目已经通过设计我们将称为发现工具的东西来实施这种方法。例如，用于家庭自动化的辅助VUI ALADIN结合了一个平板应用程序，该应用程序使用可视化工具告知用户可以控制哪些设备以及每个设备可用的交互方式[9]。在另一项研究中，JustSpeak是Android的通用语音控制系统，它通过在每个可操作对象顶部的标签发现特定于上下文的命令，便于在旅途中发现[17]。 VoiceNavigator是一款移动VUI，利用“发现提示”等工具突出新发现，以及“我能说什么”菜单，以帮助用户不确定说什么[7]。

虽然这些VUI项目在您使用发现工具时采用了学习方法，但它们会利用额外的输入模式（即touch）来专门迎合具有无障碍需求的用户。但是，随着VUI的普遍使用，提供额外的输入模式可能会过度补偿其局限性。另一种输入源可能会导致用户使用更为熟悉的触摸方式，从而抑制了VUI的可学习性。使用手机或平板电脑也禁止VUI作为免提接口的好处。我们的项目打算使用发现工具来无处不在地使用使用壁挂式显示器的VUI，其中显示器仅用于提供视觉反馈。

像Alexa应用一样，ALADIN [9]，JustSpeak [17]和VoiceNavigator [7]主要关注初始可学习性。发现工具中的重复信息（如Alexa应用程序中的信息）可能会变得多余，甚至可能会阻止用户[1]。呈现扩展学习所需的额外信息可能与某些人无关，并可能使界面变得混乱。可以利用自适应方法来根据用户需求个性化发现工具。

**适应性方法**
自适应接口的设计使它们的行为适应用户的需求[2，5]。同样，ADT可以设计为适应用户的专业水平和使用环境。

基于触发器推断接口适配。用户响应时间和hastiness已被用作触发器以适应VUI中的回放速度或语言内容[15]。移动设备也使用相同的触发器来产生关于VUI或目标域的视觉和口头反馈[12]。在两种情况下，当适应性反馈与他们的技能水平相关时，互动更快，用户报告更高的满意度[15,12]。自适应图形用户界面（GUI）中应用的某些模式可以扩展到ADT的设计，例如减少初始使用后不需要的元素的可视化[16]。其他模式包括调整内容和提示使用频率。

在大多数情况下，用VUI进行适应是由用户语音的质量触发的。使用响应时间作为触发可能是有风险的，因为新手用户的中断或犹豫可能与他们的技能不相称。研究表明，适应性接口不应该给用户减少控制的感觉[16]。

从现有的工作中，我们可以看到一些研究在设计工具的帮助下实现了学习，帮助用户发现VUI。然而，很少有人关注适应性方法，鼓励可学习性超越最初的使用范围。我们建议设计ADT for DiscoverCal，通过适应上下文相关性和用户的界面表现来扩展可学习性。

**在VUI中设计可发现性**
为了改进VUI可发现性的设计，我们调查了现有项目[7,9,17]，这些项目利用视觉辅助来提高VUI中的可发现性，并对其中的关键设计元素进行了分类。这些特性总结在图1中。

在VUI中设计Discoverability时，重要的是做出可能的活动（用户打算完成的任务）和命令（用户需要说明完成任务的内容），以便轻松发现它们。这是通过为ALADIN，JustSpeak和VoiceNavigator创建的工具中体现的一些特征实现的[7,9,17]。例如，可视化活动或命令是所有这些项目中的重要特征。在ALADIN中，大按钮突出显示活动，并在其中列出相关命令。在JustSpeak中，相关命令被标记在每个可操作对象上。在VoiceNavigator中，据说“我能说什么”菜单在内容与上下文相关时提高可学习性。 VoiceNavigator的另一个特点是通过“发现提示”来可视化新发现。

不幸的是，用户报告发现提示为争夺用户的注意力而战。主要原因是用于此项目的移动设备上的屏幕空间有限。

可视化（活动）和可以说的（命令）直接解决了VUI作为不可见接口面临的挑战。可视化发现可以让用户在逐渐浏览界面时感到自信。与GUI导航不同，单个命令导致一个动作，VUI为相同的动作提供许多命令。可视化发现为用户提供了一个视觉追踪他们的进展。在实施随学习的学习方法时，上下文相关对于确保学习内容反映用户当前的上下文非常重要。

我们确定这些特征来为我们的项目设计提供信息。但是，我们发现它们可以作为通用原则来设计VUI中的可发现性。 VoiceNavigator成功应用并测试了其中的一些工具以提高可学性。但是，它们没有解决扩展的可学习性问题。我们通过重新创建一些工具（命令列表和发现提示）并基于已识别的特征实施其他工具来设计DiscoverCal以扩展此项目。图1列出了DiscoverCal中使用的工具。

## DiscoverCal
DiscoverCal（图2）是一个具有语音和视频界面的日历系统。用户使用语音控制来管理他们的时间表并在屏幕上接收视觉反馈。特别是，我们使用API​​.AI作为我们的VUI。该屏幕被设计成任何通用计算机或电视屏幕。重点是探索如何设计ADT以提高初始和扩展的可学习性。

这项研究的目的是调查适应性发现工具如何增加语音用户界面中的可学习性。我们使用日历测试为该项目设计的工具（图1中的第二列），因为它提供了足够的复杂性来引入适应并延长间歇性的可学习性。我们选择家庭作为使用的上下文。最近的一项研究发现，39％的用户在家中使用语音接口，而只有6％的用户在公共场合使用它们[13]。任务管理和家庭自动化最近已经为亚马逊的Alexa和Google Home等VUI提供了一个流行的应用领域，但是现有的系统没有ADT。

一旦设置了DiscoverCal，用户就可以开始学习通过ADT明显可发现的基本活动和命令。在命令或活动成功使用后，菜单中的内容会适应。适应是由（a）用户表现和（b）上下文相关性触发的。根据每个用户与系统的交互方式，ADT建议活动和命令。例如（图3），经常创建事件的用户是推进该活动的推荐内容。一旦系统检测到用户已成功执行该活动三次，系统会将其标记为“已学习”并将其从显示它的菜单中移除（图4）。一旦用户开始使用在工具中不再可视化的学习活动和命令，界面就会调整为隐藏它们（图4至5），允许用户在需要时使用显示的命令将其拉起。此外，它还调整了与该活动相关的工具的内容。例如（图6），内容可以适用于在创建事件时推荐相关的活动和相应的命令。

DiscoverCal中的ADT利用学习方法帮助用户发现与当前活动相关的功能，并扩展他们对VUI功能的了解。通过自适应方法使用发现作为实现可学习性的一种手段，可操作性设计中确定的特征已经实现。一旦用户成功学习了如何使用VUI，DiscoverCal就可以补充交互，而不是引导它。以下角色和用例演示了典型用户与系统的交互。

**角色和用例**
Lisa是一位单身母亲，在追求MBA的同时兼职。当她记得更新她的日历时，她经常在家里做家务，所以当她听说DiscoverCal时，她决定订购它。

星期一，Lisa在客厅的壁挂式显示屏上设置了DiscoverCal。她很快学习使用列出的命令添加提醒和事件的基本任务，以便使用DiscoverCal可以完成的任务。在她成功完成一项活动并且它的命令有几次后，该菜单将适应显示更高级的选项。例如，它从“计划事件”改为“使用多个日历”。发现提示标记未发现的功能，并在发现它时简要突出显示一条命令，增加她的信心。

到本周末，Lisa对“我该做什么菜单”中的活动感到满意，并且正在学习新的命令以在其中执行。最近多次，Lisa要求DiscoverCal邀请联系人参加个人活动。星期六，她注意到一个未被发现的活动，在“我能做什么”菜单中的“为事件添加人物”，并认为：“我可以与妈妈分享，这样她就不会忘记孩子们将与她一起度过的周末。”她看到列出的适当命令共享日历，“与妈妈共享日历”。

在接下来的几周里，Lisa继续与DiscoverCal交互，在ADT的帮助下学习新的活动和命令。

**用户研究设计**
在用形成性评估反馈迭代我们的设计之后，我们计划通过用户研究来评估我们的方法。 DiscoverCal专为广泛的用户而设计。 VUI的新手用户，每月使用VUI不到一次，年龄超过18岁，将被招募。评估将是一个主题间设计，它将静态发现工具（在整个交互过程中保持不变）与ADT为DiscoverCal设计的工具进行比较。参与者将被随机分配到一个控制或测试组（每组n = 5）[14]，并将被邀请用DiscoverCal完成一组任务。参加者将在十天内以三个30分钟的间隔进行测试。任务将从基础活动（如创建活动）到更复杂的活动（如添加新日历）的时间间隔提前。

将使用任务度量分析和系统可用性量表（SUS）问卷来对两个用户群体中的可学习性进行统计分析。任务度量标准用于存储成功完成任务所需的数据以及完成此任务所需的时间。 SUS是一个十项规模，它提供了关于系统随着时间的整体可用性的主观定量用户反馈[3]。观察和半结构式访谈将用于评估可学性[4]的主题分析。通过比较两组新手用户随时间的数据，我们可以用系统评估他们的可学习性[8,3]。

## 结论和未来工作
我们已经提出了我们的方法来解决改善VUI中可发现性的挑战，以便在初次使用之外扩展可学习性。 在检查现有项目后，我们开发了一系列有助于改进VUI中可发现性的特性。 我们进一步扩展了为VoiceNavigator创建的工具的设计[7]，通过设计和实现适用于DiscoverCal的ADT的自适应方法，以便在最初使用之外扩展可学习性。 用户研究介绍了我们未来的计划，为我们的设计提供经验评估。

## 参考文献
[1] Ken Abbott. 2002. VUI Design Principles and Techniques. Apress, Berkeley, CA, 87–103.
[2] Pierre A. Akiki, Arosha K. Bandara, and Yijun Yu.
2014. Adaptive Model-Driven User Interface Development Systems. ACM Comput. Surv. 47, 1, Article 9 (May 2014), 33 pages.
[3] Jonatan Andersson. 2016. Assessment and Improvement of Initial Learnability in Complex Systems: A Qualitative Study to Promote Intuitive Software Development. (2016).
[4] Virginia Braun and Victoria Clarke. 2006. Using thematic analysis in psychology. Qualitative research in psychology 3, 2 (2006), 77–101.
[5] Dermot Browne. 2016. Adaptive User Interfaces. Elsevier Science.
[6] Fang Chen. 2006. Designing Human Interface in Speech Technology. Springer US.
[7] Eric Corbett and Astrid Weber. 2016. What Can I Say?: Addressing User Experience Challenges of a Mobile Voice User Interface for Accessibility. In Proceedings of the 18th International Conference on Human-Computer Interaction with Mobile Devices and Services (MobileHCI ’16). ACM, New York, NY, USA, 72–82.
[8] Tovi Grossman, George Fitzmaurice, and Ramtin Attar. 2009. A Survey of Software Learnability: Metrics, Methodologies and Guidelines. In Proceedings of the SIGCHI Conference on Human Factors in Computing Systems (CHI ’09). ACM, New York, NY, USA, 649–658.
[9] Jonathan Huyghe, Jan Derboven, and Dirk De Grooff. 2014. ALADIN: Demo of a Multimodal Adaptive Voice Interface. In Proceedings of the 8th Nordic Conference on Human-Computer Interaction: Fun, Fast, Foundational (NordiCHI ’14). ACM, New York, NY, USA, 1035–1038.
[10] Candace A Kamm, Diane J Litman, and Marilyn A
Walker. 1998. From novice to expert: the effect of tutorials on user expertise with spoken dialogue systems.. In ICSLP. Citeseer.
[11] Laura Klein. 2015. Design for Voice Interfaces. O’Reilly Media, Sebastopol, CA.
[12] Kazunori Komatani, Shinichi Ueno, Tatsuya Kawahara, and Hiroshi G. Okuno. 2005. User Modeling in Spoken Dialogue Systems to Generate Flexible Guidance. User Modeling and User-Adapted Interaction 15, 1 (2005), 169–183.
[13] Carolina Milanesi. 2016. Voice Assistant Anyone? Yes please, but not in public! (June 2016). http://creativestrategies.com/
voice- assistant- anyone- yes- please- but- not- in- public/
[14] Jakob Nielsen. 2000. Why You Only Need to Test with 5 Users. (March 2000). https://www.nngroup.com/articles/ why- you- only- need- to- test- with- 5- users/
[15] Daniel O’Sullivan. 2009. Using an Adaptive Voice User Interface to Gain Efficiencies in Automated Calls. Technical Report. Contact Solutions | Inventing Real Customer Service, Smithtown, USA.
[16] Qian Yang, John Zimmerman, Aaron Steinfeld, and Anthony Tomasic. 2016. Planning Adaptive Mobile Experiences When Wireframing. In Proceedings of the 2016 ACM Conference on Designing Interactive Systems (DIS ’16). ACM, New York, NY, USA, 565–576.
[17] Yu Zhong, T. V. Raman, Casey Burkhardt, Fadi Biadsy, and Jeffrey P. Bigham. 2014. JustSpeak: Enabling Universal Voice Control on Android. In Proceedings of the 11th Web for All Conference (W4A ’14). ACM, New York, NY, USA, Article 36, 4 pages.