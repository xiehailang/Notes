# 2018：Voice Interfaces in Everyday Life
**摘要**语音用户界面（VUI）正变得无处不在，通过智能手机嵌入到日常移动中，并通过“助理”设备嵌入到家庭生活中。然而，这些设备的用户究竟如何将其用于日常社交互动的实际情况仍然未得到充分研究。通过收集和研究在参与者家中长达一个月的亚马逊Echo部署中的音频数据 - 通过民族方法学和对话分析 - 我们的研究记录了VUI用户的方法实践以及如何在复杂的社交生活中完成VUI用户的使用家。我们提供的数据显示了设备如何对会话设置负责，并嵌入到各种同时活动正在实现的家庭聚餐中。我们讨论VUI如何与顺序组织的谈话进行精细协调。最后，我们找到VUI交互问责制，请求和响应设计的含义，并提出设计'对话'接口概念的概念性挑战。
**关键词**Amazon Echo; conversational agent; conversational user interface; conversation analysis; intelligent personal assistants; ethnomethodology; collocated interaction

## 简介
语音交互已成为许多商业设备（如手机和平板电脑）的一项功能。最近，语音已成为独立无屏幕设备（如Amazon Echo和Google Home）的主要接口。这些界面通常被称为语音用户界面（VUI），会话代理或智能或虚拟个人助理，被描述为体现虚拟管家的想法[23]，可帮助您完成任务。研究人员采用诸如“会话界面”这样的技术[20]（我们的强调）在许多方面与这种设备的广告用户体验产生共鸣：特别是与技术“可以进行对话”并“只是问”的问题。此外，一些VUI（销售为'smartspeakers'）被认为特别适合在家中用于各种用途：帮助烹饪，播放音乐，获取新闻和信息，或与其一起玩游戏。

尽管在自然语言处理，对话系统和计算社会语言学等计算语言学方面进行了大量有益的研究，但缺乏经验地研究VUI在日常使用中的社会和交互问题的研究[21]。换句话说，除少数例外，对与VUI交互的实际成就以及VUI用户日常生活中嵌入的这种交互如何展开的阐述知之甚少。我们认为这种缺席是显着的，因为我们自己的研究表明，在设计家庭设置的VUI时可能需要考虑一系列概念上的变化，更广泛地说。

我们的工作是在HCI和CSCW研究的传统中进行的，这些研究部署了技术来研究家庭中位置和紧急的生活体验[37]。通过这种方式，我们正在继续最近在CSCW中出现的一些工作，这些工作已经开始在合作行为[26]中检查VUI，在会议等社交环境中[18]以及在咖啡馆中与朋友交流[27]。我们的研究报告了在五个家庭中使用Alexa语音代理的Echo一个月的部署情况。音频捕获由独立的设备 - 有条件的语音记录器选择性地执行，以某种方式收集超过6小时的涉及Echo的口头交流。

我们的研究借鉴了HCI文献（例如[24]）中常见的民族方法学和对话分析（EMCA）[8,32]的传统，以检验Echo与说话有关的各种方式。在我们的研究的主要部分，我们探讨了Echo如何嵌入到家庭的情境紧急情况中（如使用过程中发生的其他活动），以及用户如何解释使用涉及到的互动工作。然后，我们看看VUI使用的顺序组织方式在多方会话环境中实现，并通过讨论我们发现的三个关键问题来结束：关于将VUI与VUI交互作为“对话”的框架的概念性问题;由用户向VUI提出请求的问责所产生的影响;最后，来自VUI的响应的设计和角色作为进一步行动的交互资源。

## 相关工作
我们的研究涉及三大领域。首先，我们通过覆盖VUI的发展为我们的论文设定了场景。然后我们考虑谈话分析在HCI中的作用，特别是在讨论VUI时，注意到明确的缺席并且也正在形成一个新兴的新领域的形状。最后，我们将正交视角考虑在内：即与家庭技术设计，部署和研究相关的方法论挑战。

### 语音用户界面
正如我们已经注意到的，人们可以通过多种方式来命名机器，包括会话代理或智能个人助理。然而，这是一个广泛的范畴，因此我们使用VUI来表明我们专注于口语词汇互动。在这样做的过程中，我们必须将我们的工作与研究诸如Facebook M等聊天机器人的工作区分开来，这些工作涉及阅读和书写练习（输入消息和阅读答案）。我们专注于主要基于语音的接口，其中用户与设备通话并且设备以合成语音进行响应。当前的商业可用示例包括在Amazon Echo中找到的Alexa和在Google Home中找到的助理。我们还注意到，这种兴趣与虚拟或体现的人类/代理人（如SimSensei [5]）之间存在一些细微的区别，这些区别是通过语音和视觉回应的方式进行的。
当然，通过“自然对话”可以讲的机器在科幻小说（如2001年的HAL 9000：A Space Odyssey）和研究（参考文献[16]）中都有相当的传承。我们注意到，这些想法中的许多已经被实现，其中有不同的系统被创建用于帮助诸如医疗保健决策[5]，指导博物馆中的访客[14]以及老年人[40]等领域。早期的系统侧重于特定的任务，例如通过电话向用户提供天气信息[42]，然而随着时间的推移，他们已经采用了越来越复杂的形式和功能，包括拟人化特征的体现[23]。最近为家庭使用而设计的系统使用互联网连接进行语音处理和信息检索，首先在便携式移动设备上进行探索[13]。

### 与计算机交谈
虽然语音技术研究一般长期以来一直考虑语言模型及其与VUI的关系，但会话分析与VUI之间的联系是有限的。吉尔伯特等人。 [9]认为对话分析的结果确实可以用于人机交互的设计。这种先前的工作采用会话分析来通知会话计算模型的设计和开发，以支持“会话式”代理，例如，代理被设计为采用轮换系统的元素[33]。然而，这种方法存在一些固有的矛盾，特别是在对话分析中被采用作为“建模”对话的一种方式。有人指出，谈话分析采用民族方法学的观点[8]，表明人与人之间的谈话实际上并不受规则的约束或限制，或可以形式化，而是由话语和转向在本地进行管理，并通过其生产进行谈判[3]。尽管如此，我们的工作并不关心是否可以创建一个可以“说出”如同它是人类的电脑的问题，而是将这些问题放在一边，而不是定位于解开与VUI交互的民族方法学视角在谈话内。具体而言，本文试图阐明人们在日常家庭生活中常常如何处理，处理问题以及协作管理Alexa VUI周围的交互。

除了20世纪90年代EMCA知情的研究人员，HCI和AI [9]之间的短期利益汇合之外，关于VUI使用的研究最近才作为HCI和CSCW社区内的关注主题返回。 Luger和Sellen [17]通过访谈发现，现有商用VUI的有限功能存在问题，规定系统的预期能力和实际能力之间存在“鸿沟”。然而，Luger和Sellen并没有将他们的工作重点放在检查使用的实际设置上。然而，与我们这里的论文更密切相关的是Pelikan和Broth [24]的工作，他们检查人机交互的互动组织，确定所讨论机器人的用户通过适应他们的谈话来提高准确性的实际能力通过机器人的口头词汇转录，展示了如何通过用户方面的方法创新部分克服自动语音识别的局限性。也许与本文相关的大多数是我们之前的研究[27]，该研究确定了移动设备上与VUI交互的特征以及这种交互在多方社交环境中如何展开。本工作将检查对VUI的请求在设置中是如何执行，关注和管理的。然而，据我们所知，我们发现没有考察VUI的用户实际上为家庭设计的方式，并且在他们正在进行的会话环境中以交互方式从设备中定位“话语”，也不检查用户自己的话语被按照指示的要求带到设备。

### 在家学习技术
我们在这个三角测量中的最后一套文献并不涉及VUI，而是涉及到像Echo或Google Home这样的设备所针对的预期设置的性质。像HCI和Ubicomp这样的家庭这样的地方已经成为重要的方法论问题。通过这种方式，我们将我们的工作置于一个由Ubicomp成长而成立的传统之中，但也在HCI中得到广泛的应用。这种方法试图理解交互是如何发生并嵌入到生活体验中的[38]，以及这些质量如何被用于设计[4]。与这一工作相关的方法论复杂性[37]可能导致研究人员尝试一系列的数据捕获方法，以收集更多的“嵌入性”的更多理解。例如，Ferdous等人[7]将家庭访问和技术使用视频捕获纳入家庭活动中，而Rooksby等人[31]设立摄像机来捕捉电视观看和使用移动设备。然而，尽管在家庭中使用视频捕捉提供了非常丰富的分析的机会，因为我们有兴趣在更长的时间内考虑VUI的使用（再加上对于许多VUI缺乏常规化的，可预测的用例） ，我们被导致从视频转向仅音频。正如我们接下来描述的那样，为了回应这个问题，我们开发了一种设备，与Echo一起部署，以自动记录与Echo的交互，本着Pizza等人的精神。 [25]。

### 在家中录制VUI交互
我们招募了五个家庭参加为期一个月的研究，以便在家中捕捉回声的自然使用。我们五户中有三户居住着夫妻，另外两户住户则由两个父母和两个孩子组成的家庭居住。参与者的年龄范围跨越20世纪50年代至50年代中期。每个家庭都获得了Echo，配置了家庭成员的亚马逊账户，并在其个人智能手机上安装了Alexa伴侣应用。家庭自由选择Echo的位置，并可根据需要重新定位。四个家庭将Echo放在厨房或用餐区，而另一个将它放在客厅里。为了捕获Alexa使用，我们部署了第二个专用设备，即图1所示的条件录音机（CVR），该设备在使用最接近的Echo时被激活。 CVR使用会议麦克风捕捉音频，但只保留临时缓冲区中的最后一分钟。当检测到'唤醒词'Alexa时，CVR保存前一分钟并记录下一分钟的音频（如果在随后的分钟内听到唤醒词，则延长该时间段）。 CVR还具有一个关闭音频捕捉的按钮，以及两个指示CVR“正在聆听”（蓝色）和何时正在录音（红色）的LED（蓝色和红色）。

最终的语料库包含超过6小时的记录数据。在此范围内，我们确定了超过883个不同的“请求”话语，即针对Echo的谈话似乎试图让它“做某事”，例如，回答琐事问题，播放特定音乐，或设定计时器。通常这些请求形成了一个更大序列的一部分，可能包含时间或局部相关的各种其他请求。我们的语料库包含185个。

### 接近数据和交互现象
采取民族方法论和对话分析观点[8,32]，我们对参与者如何组织他们在Echo及其周围的行动感兴趣。特别是，我们研究了作为对话者的参与者如何分析与设备（及其他设备）之间的相互作用。我们的直觉是，各种会话方法将会发挥作用，并被调整以便与Echo“完成任务”。我们注意到，我们在分析中没有做的是试图将设备视为对话的参与者。使用会话分析作为一种工具来解开定位操作的顺序和嵌入式实践是人机交互中已建立的技术（例如[9]）。
我们提供的数据片段遵循一套标准的转录惯例[1,11]。作为参考，我们注意到发生停顿的时间（（。）或（1.4）分别为0.1秒和1.4秒），其中谈话是LOUD或°安静°，在那里说话<比通常更快>，并且话语是延长的::: ated。重叠说话使用缩进和[方括号]，（（未说出的动作））用双括号表示。所有的名字都从原始文本中改变过来。似乎主要针对VUI的对话以粗体突出显示，并具有蓝色背景。反过来，由Echo生成的合成语音在成绩单中由标签“ALE”（即ALExa）标识并具有绿色背景。将合成语音作为转录本的一部分并不意味着参与者和回声之间有任何概念上的等同，而仅仅是一种呈现设备输出的便捷方式，因为它在时间上呈现在互动中。
我们在本文中研究的片段来自我们称之为肯特家族的一个家庭。我们选择了Kents作为单个案例的分析[34]，以提供一系列我们发现参与者在整个语料库中使用的各种方法的“生动展示”[2] [2]。也就是说，通过我们的分析，我们确定了参与者使用Echo的方式，并将这些片段作为参与者进行交互式工作的意义的示例;然而，它们并不是我们语料库中这种交互方法的唯一例子。按照民族方法论的定位，我们认为参与者不断地为了他们自己的互动而工作，并且依赖他人的有序特征（以便分析彼此之间正在做什么，从而“继续”）。这意味着我们正试图展示参与者将Echo实际应用于交互顺序（即，在这种情况下为家庭聚餐）的一些方式。我们将其留待今后的工作来验证，驳斥或增加我们的发现。在我们的考试中，我们不仅要承担我们自己使用Echo的经历，还要承担诸如Google Home和Siri等其他VUI。
受到里夫斯和布朗[28]的类似方法的启发，我们通过两种相互关联的方式来看待家庭的相互作用。首先，我们考察一下Echo是如何“在家中”并嵌入到家庭生活的各种活动中的。与设备的相互作用不是作为一个单一的不分皂白的事件发生，而是作为位于家庭生活中的一部分或更确切地说是嵌入的行为来实现的。其次，我们转而解开VUI在连续行动过程中的特征，即对话的有序生成。

### VUI交互如何在家中进行
有两位父母，苏珊和卡尔，还有两个十岁左右的孩子，肯特家族的利亚姆和艾玛。他们一直在使用亚马逊Echo大约一周，并且已经开发出合理的熟悉度和使用能力。当然，我们将使用的片段以及我们更广泛的数据集并不能清晰地显示长期拨款。相反，它通过在使用初期捕获它所做的工作就是展示参与者探索设备使用和工作的一些初始方式（尽管通常不成功），使Echo与社交环境家。

### 将回声嵌入到家庭活动中
在回家时，Echo会在那里发生的各种正在进行的活动中不可避免地交织在一起。我们的数据充满了互动序列，参与者以某种方式处理回声，并将其输出结合到场景中，同时参与多方对话并完成家中的其他活动（我们将会看到）。肯特家族在母亲节的晚餐桌上一起吃晚餐。 Echo放在书柜的顶部，用作餐厅的餐具柜。我们的第一部分片段从母亲苏珊开始，向其他人宣布，她希望在一分钟内播放Beat the Intro。击败介绍是一个可用于Echo的游戏，肯特以前一起玩过;它包括从播放歌曲开始几秒后听到播放器必须通过宣布歌曲和艺术家来猜测。该游戏是一个“技能”，为Echo开发的第三方安装功能。苏珊宣布后，利亚姆对此进行了评估（“哦不”），然后拉长了“不”，因为苏珊然后指示Echo玩这个游戏。卡尔提到母亲节，而苏珊指示利亚姆吃他的食物。苏珊然后尝试另一个指示，以Alexa“打败了介绍”。
我们的第一个观察结果是，如果您愿意，可以在多重活动或“行动方案”中嵌入指示“打败介绍”的Echo，以确保家人正在共同完成工作。例如，这个家庭一起吃晚餐，他们正在谈论这种饮食（特别是07-10行）。利亚姆的合规请求由卡尔在苏珊对Echo的最初指示（第03行）中产生，卡尔反驳利亚姆对苏珊准备话语“我想玩一分钟就打败介绍”的消极回应，提醒“这是母亲节吗？“（06行）。我们也可能会广泛地称赞为“养育子女”，以便在进餐时建立适当的行为方式，特别是对于年轻家庭成员，例如指示利亚姆“继续吃橙子”。一直以来，我们发现这些其他并行活动与苏珊对Echo的进一步请求的组织密切相关。例如，苏珊从第11行开始的第二条指令与卡尔延续苏珊先前的请求交叉给利亚姆吃他的食物。卡尔在第10行提供了一系列开头的转折：“和你的绿色东西”，以及第12行的“和你的褐色东西”。
这些初步观察提供了与家庭技术使用的先前研究的一致性，以及这些技术如何被吸引到家庭生活组织中作为行动资源（例如参见Rooksby等[31]）。像这样的经验性陈述提出了一种更细致的视角来概念化像Echo这样的技术，通过将注意力从与共同出席他人的互动中吸引掉，从而破坏已建立的道德秩序[39]。相反，我们在这里看到，家庭本质上是多种活动环境，在这些环境中，设备被招募进来并通过在家中进行的合作和搭配活动进行管理[29,31,38]。
同样重要的是要注意VUI的设计功能，这些功能倾向于允许与家中的活动进行啮合。具体而言，像Echo这样的设备提供了“永远在线”的“始终聆听”能力（尽管存在相当大的道德和隐私难题，但是在认识到这个主题的重要性的同时，我们注意到这些问题不属于本文的一部分） 。这导致通过唤醒词连续获得地址。
因此，使用Echo并且继续与它互动，对其他成员的移动或者很少的协调行动几乎没有要求（尽管我们后面会看到，它比关于沉默的产生更加微妙） 。这意味着Echo的使用可以通过日常谈话相对容易地进行，并且可以在其他正在进行的活动中煞费苦心。这是该设备的初步可用性，我们很少看到在01号线可以偶然看到的那种行动，其中由Susan提供了一个预备帐户。

### 回声使用和控制的“政治”
毫不奇怪，VUI使用的规定 - 谁可以处理Echo，何时以及如何 - 通过各种会话方式实现参与者。我们最初的片段1为我们提供了对Echo的控制方式的理解，这些方式是作为一种社会组织的事物来管理的，我们可以将其作为“家庭的政治”来形容。具体来说，我们再次提醒注意片段1中的01-06行，以及处理Echo的方式，它提供的活动的选择（打Beat the Intro），以及它对组合家庭的影响（即它将参与桌上游戏的集体参与）发生在参与者对这次特定家庭聚会的具体细节的“调节性工作”的定位上。所以，例如，我们看到这个规范性的工作构成了卡尔提醒它是母亲节，针对利亚姆，他的负面反应是苏珊对Echo的指示引起的。卡尔的提醒在此构成了对苏珊权利的分析：即轮到她回应Echo，并且她有权制定指导及其对坐下的家庭的影响。
深化这一点，我们现在转向我们的第二个片段，在那里处理Echo的方式是以不同的方式进行调节的。这部分片段来自于家庭完成了Beat the Intro之后几分钟的一段较长的互动过程，现在正在尝试玩一个不同的测验Skill，Quiz Master。肯特家族在回忆技巧的名字时遇到了麻烦，因此苏珊用她的智能手机查看了它（从本抄本中省略）。当我们加入片段时，Emma利用这个开放，而苏珊很忙，要求Echo“恢复音乐”。该指导是儿童试图指导Echo播放父母不一定会欣赏或希望听到的音乐的更广泛的玩笑中的一部分。苏珊试图与Alexa交谈，但音乐开始播放。接着是一些笑声，之后苏珊完成了她的“打开问答大师”的指示。
我们在这里看到Emma和Susan之间的一场“竞争”，以解决Echo问题。正如我们前面提到的那样，Echo被设计为随时可用于地址，这意味着参与者有效地具有“平等访问”。正如我们在这里看到的，这导致出现各种会话方法来管理和管理访问。爱玛在01号线发起她对Echo的指示，这只是部分在飞行中，因为苏珊下一轮指示爱玛“坚持一分钟”插入。尽管艾玛并没有对苏珊说话，但她仍然密切注意她对03行Echo的继续使用，即苏珊的指示并未导致课程变更，苏珊似乎是通过她在04行与艾玛的重叠谈话来分析的Emma的延续涉及重复元素（“简历”）以及在与Susan的指导重叠期间提高音量。管理他人对该设备的话语的参与者的这种感觉进一步举例说明VUI控制如何被调节为在该设置的成员之间并通过相互作用而处于社交中的社会事件。我们的观点是，对Echo的控制与环境并没有什么不同，而是深深地嵌入到它的社会秩序中，就像它的参与者和他们对该社会秩序的分析所产生的那样。

### 互动中的回声会计
我们关于VUI嵌入用户的最后一点是必须将其引入社交环境的问责制中。通过“问责制”我们的意思是说，人们经常试图产生社交行为，使其看起来对其他人和情况负责。对于社会成员来说，这是一个持续不断的问题，因为在社会行为问责制可能存在缺陷的情况下，成员们通常会努力提供他们正在做的事情的记录（可能是“解释”）。

从片段1中可以看出，苏珊如何为后续行动提供一个这样的（未来的）账户，即“我想在01分钟内打一分钟”。苏珊的话语在这里将账户准备为一个“框架”，我们可以说，通过共同出席其他人的方式来使她的后续教学变得有意义。苏珊对自己未来可能采取的行动的陈述表明了对该行为可能如何被家庭其他人所对待的敏感性（她也将其作为一种偏好“我想要”而不是“明确的”我们将“ ）。还有一个更广泛的意义，在这个意义上，与Echo的各种互动被视为对情况负责。例如，在片段2中，Emma对01行（“Alexa”）的指示开始导致Susan快速分析Emma对Echo的地址，作为推定，转折和暂时问题（即“不保留分钟“，第02行）。换句话说，针对Echo的谈话是对正在进行的谈话的一致性负责，同样也是谈话展开的情况。一般而言，处理VUI涉及在经常以其他参与者为特征的情况下产生话语，这意味着这种话语以与所有社交行为被处理的方式类似的方式来对待：对他们所处的情况负责。
VUI交互特征如何在会话的连续组织中提供
我们已经看到Echo如何融入家庭的多重活动，设备控制的组织和管理以及话语的问责。然而，VUI交互的一个重要元素是它如何适应有序，顺序的谈话组织，即如何以逐个转弯的方式完成与VUI设备的交互。我们现在将开始详细解释Echo如何在连续的谈话组织中“在家中”制作。
首先，关于序列性以及会话分析如何处理它的意思。 Schegloff认为，顺序是“任何类型的组织都涉及话语或行为的相对定位[交谈]转向是一种顺序组织，因为它涉及发言者的相对排序”[35]。换句话说，谈话（如涉及寻址和收听VUI输入或输出的谈话）必须将设备的“话语”整合到谈话顺序中。重要的是，顺序性与单纯的时间顺序不同（虽然它可以利用它），不仅因为它包含了暂时发生的行为（如重叠谈话），而且会话的连续一致性是连续的那些正在寻求集合那些经常在基本时间秩序之外的行动的意识的交谈者取得了成就。例如，演讲者可能会在对话中提出几个问题后回答问题（这可能会由演讲者以各种方式解释，例如，在我回答您的问题之前提前发言......）。
在下面的章节中，我们将依次回顾Echo的两个关键方法成就。首先，寻址VUI，即如何实现对设备的输入。其次，我们看看参与者如何处理来自VUI的响应，即交互的“完成”，输出的顺序，甚至输出的缺失。我们故意在这里使用“输入”和“输出”来确保描述人类VUI交互反映了参与者似乎对待设备的方式，以避免拟人化特征或合并。

### 在会话环境中处理回声
寻址Echo涉及产生以这种方式格式化的话语，以便被设备检测为请求。这些请求可能会在几次谈话中出现（例如，参见片段2了解复杂的示例），即使只有一个用户在场时也是如此。请求通常涉及两种公式：作为“问题”（例如“什么是天气？”）或作为指令（例如“打败介绍”）。在处理Echo问题时，我们发现参与者（作为有能力的对话者）以至少三种连接方式（毫无疑问更多）将设备带入到连续的对话组织中。首先，我们看看如何以适合自己的方式产生请求，并自己调整谈话的一些基本转向“机制”[33]。其次，我们看到请求制作如何经常涉及共同产生沉默（即拒绝或暂停轮流）以帮助参与者提出请求。第三，请求有时不是一个参与者的唯一领域，而是坐在谈话序列的协作方面。
为了帮助我们展示这些特征，现在我们在片段1之后的片段中介绍下面的片段3.在这个片段中，Carl接管了Susan迄今为止未能尝试开始游戏Beat the Intro的尝试。苏珊抱怨Echo不适合她，但几秒钟后，卡尔的请求似乎也失败了。艾玛评论说“她不喜欢那样”。艾玛然后产生请求的修改版本，在此期间卡尔质疑游戏是否真的被称为“击败介绍”。 Echo回答不正确，并提出问题，Emma通过回答消极的方式关闭序列。卡尔表达了一种恼怒的感觉，“我们晚上玩了它！”，最后苏珊再次尝试这个指令，通过设备的进一步沉默（4.5秒）来满足。
我们将在下面的部分回到这个片段。
将请求转化为会话转换
就像在任何对话中一样，肯特家族成员也关注对话的持续顺序组织。这种敏感性使他们能够在展开谈话的过程中找到可以进行下一回合的时刻。对话者倾向于的一个关键特征是谈话的转向结构单位（TCU），即一个话语的可持续的情境，“完整”部分，导致可能的过渡相关位置（TRP），另一位发言者可能选择轮到他们[33]。例如，要使用Sacks等人的例子[33：702]，接待台可能会询问一个主叫方“你的姓氏是洛林？”，其中一个TCU是“你叫什么名字”，因为主叫方这部分话语可能是完整的（作为针对唯一另一方'存在'的适当问题）。在这个例子中，TRP位于“name”之后，表示可能的演讲者转换的地点。
对于Echo的用户，我们注意到寻址设备的方式提供了某些会话特定的TCU，因此提供了TRP。例如，考虑卡尔对片段3（第07-08行）中技能名称的询问（“它是否击败了介绍？”），以及他如何将它依次插入到艾玛的话语中。卡尔在艾玛制作唤醒词“Alexa”和随后向设备“播放节目介绍”的请求之间的1.3秒差距中准确地提出了这个问题。还请考虑苏珊在片段1的第03行所发出的请求，她在那里发出“Alexa（1.1）播放击败介绍”，而Carl在1.1秒暂停期间悄悄地说“是”。卡尔的“是啊”提供了一个反对利亚姆拒绝苏珊在01行的预备话语，而且重要的是，这个“耶”被定位在苏珊制作“Alexa”之后的精确时刻 - 卡尔似乎正在定位于这种常规停顿。同样，在片段2中，我们在01-03行中看到苏珊在说出“Alexa”之后是如何从艾玛转过来的。
换句话说，Echo用户的分析工作中的唤醒词“Alexa”似乎常规地被定位为TCU，即可能导致转向过渡的“完整”话语。输入到Echo和其他VUI的输入生成的语法公式性质，即wakeword-gap-request的输入生成，使得有能力的设备用户能够预测这个差距，建设性地减少沉默，并因此提供利用差距的可能性来自我选择并进行谈话。通常这也会导致原始请求者与Echo进行交互，然后选择在交互转向之后恢复交谈[15：301-304,33]。此外，随着要求的提出，在谈话中重叠最小化的偏好[36]似乎也在运作。例如，在第6行的片段3中，Emma继续完成她的要求。在片段1和2中，我们看到类似的例子，包括更紧密锁定的谈话。可能这种恢复的做法是为了尽量减少重叠以提高Echo的转录准确性。

### 在请求期间相互产生沉默
要求生产是以各种微妙的方式协同完成的。一个关键的形式涉及在回应地址时暂停轮换。我们在片段的不同位置看到了这一点，例如片段3中的第18-20行，在此期间Susan提出了一个请求，在该请求中，房间里的笑声显着地消退，因为她产生唤醒词。这种静音制作，这种停止轮流和暂停轮流（在片段3的例子中还有4.5秒），是参与者围绕请求制作进行协作的一种方式。由于VUI设备通常可能难以在自动转录过程中区分不同的声音，因此减少背景噪音（即其他说话）似乎是用户为提高准确性而采用的技术（请注意，我们并不是声称用户了解底层机制甚至不相关）。之前的工作已经建立了类似的偏好，在对VUI的请求执行之后，对话中的群组沉默。[27]。进一步说，我们注意到，随后的这轮轮换暂停也为Echo提供了一个可能的，预期的预计响应的可用性增加空间。

### 请求生产中的其他各种顺序协作
我们发现Echo用户经常执行其他类型的协作操作以产生请求。例如，片段3显示Carl，Emma，然后Susan轮流对该设备进行寻址。期望的结果反复未能实现（即开始击败前奏游戏），所以家庭在随后的转身中改变他们的请求。这里的请求更改似乎以双重方式发生;首先，通过改变韵律，例如唤醒词的发音（例如行06,13和18），其次，通过命令词的语义变化（例如，行01中没有，“行”06行，第18行中的“技能”）。这再次回应了以前的工作，展示了与VUI的合作行为充满了重复和改写[27]。
处理回应
在研究了参与者对Echo的请求之后，我们现在必须转向设备的响应，作为计算综合语音提供。正如请求一样，我们广泛地发现，对话者试图将Alexa产生的回应融入到谈话的顺序组织中。在下一节中，我们将探讨参与者如何在谈话中回应Echo，如何针对设备的响应，并在必要时处理发生问题时的响应。这种'麻烦'通常与VUI相互作用，并且在我们的语料库中的大部分序列中都有很好的表现。接下来，我们只解释参与者参与VUI响应的三种方式（可能更多）：面向沉默回应，回应暗示麻烦，以及修复麻烦的交互。
对沉默的回应
就像在日常谈话中沉默的时刻一样，这种沉默经常被视为麻烦来源（例如，在某人问一个问题之后长时间的停顿可能被认为是一种否定的回应），Echo沉默代替预期的反应时刻由参与者进行类似的分析[41]。考虑片段3，在卡尔（01-04行）和后来的苏珊（18-20行）的请求后，4.5-5秒的沉默随之而来。随后的沉默在这些时刻被视为麻烦，我们可以在艾玛的两段时间之后的“她不喜欢那样”的评论中看到。我们还注意到，参与者对延迟应对的敏感度可能会导致尝试解决麻烦的其他方式。例如，卡尔质疑技能是否被称为“击败介绍”（第07行），提供明确的候选人来解决麻烦来源，即他以前的请求可能使用了不正确的技能名称。
我们注意到，这里的参与者对沉默的敏感度与日常谈话中的不同。由于Echo必须远程计算响应，引起通常至少1秒的延迟（在我们的语料库中），因此该响应时间可能会更短或更长，因此设备的响应中存在预期的时间延迟。但是在这里，我们看到沉默在某种程度上被视为无回应，并且在某种程度上是失败的。这与之前提出的一些观点相联系：参与者经常互相产生沉默以允许VUI请求产生，并且他们经常在预测响应中产生沉默。
作为麻烦暗示的回应
在我们研究参与者如何寻求解决问题之前，我们需要看一个相关的问题：在提示麻烦时如何对待自己的反应。而在触摸屏设备（例如智能手机或平板电脑）上发现的VUI中，语音到文本转录通常显示在屏幕上，而无屏幕设备的用户必须完全依赖听觉响应（尽管他们可能会发现更多线索，在大多数无屏幕设备提供的伴侣应用程序中）。我们发现，Echo的设计反应似乎整合了麻烦形式的指标，以及实际上参与者如何处理这些指标的方式之间存在显着的不匹配。尽管出于简单起见而想要调用某些回声响应的“错误消息”，但这并不正确，因为这些响应并非总是计算错误的结果，例如，它们可能是由于VUI设备错误地转录了请求。不过，这些反应是诊断和解决问题的重要资源。
下面我们的下一个片段提供了一个如何处理来自Alexa的响应的展示。该片段在家庭演奏了Beat the Intro之后开始。艾玛要求苏珊执行这个要求，这是一个“正常的测验”（与Beat the Intro相反）。苏珊然后指示给Alexa：“给我们一个家庭测验”。来自Alexa的第一个回应是“我找不到我听到的问题的答案”，导致艾玛给苏珊的一个类似的指示。 Echo提供了另一个类似的回应，导致Liam加入他自己的指导请求。经过更多的困难和一些笑声，卡尔两次尝试类似的指导（“启用家庭测验”），并从关于启用“尼尔家庭测验”的问题的形式得到Alexa的回应。
有趣的是，第04-05行的设备的初始响应可以被看作暗示问答结构序列（“我无法找到我听到的问题的答案”），尽管参与者似乎将序列定位为一个教学问题：我们可以看到苏珊把艾玛的问题转化为她，即“你能问一个普通的问答吗？”，这就变成了“让我们成为家庭问答”。 VUI将指令误分类为问题（技术上它超出了请求的范围）。这可能会产生问题，因为用户可能会反过来导致Echo的错误分类而不是麻烦来源。然而，这似乎很大程度上被家庭忽略，他们轮流反复地将请求改为第一个的细微变化：省略“我们”（第07行），添加“请”（第12行），并省略命令动词“set”（第19行）。从某种意义上说，该设备对此问题的回应似乎是参与者解决问题并使设备运行的低效资源。
修复麻烦的交互
在最后一节中阐述最后一点，我们在这里考虑更多的参与者在修复与Echo的麻烦交互中实际做的事情。首先，从假设的VUI​​设计者的角度考虑片段4中的交互：Echo可能不会将“set”识别为调用所需技能的命令。 Echo在片段4中产生的每一个反应都是由不同的家庭成员依次重新提出请求来满足的。回声（第04-05行和第09-10行）的前两个回应没有被家庭成员视为需要显着改变他们对设备的指示：相反，他们对苏珊的原始指令进行了很小的变化（第02行），并特别保留“set”一词。 Echo的第三个回应（第15-16行）有些不同，指的是“理解”的问题：“我无法理解”。这导致了Emma1的重叠笑声。卡尔然后产生了早期指令的最小版本（第19行），但他似乎认为这是有问题的，因为他很快发出了另一条指令，他将命令动词更改为“启用”。这最终导致了一个表明进展的反应（第24行），从而纠正了麻烦。这再次表明了重新制定或重新规定请求作为语音交互功能的做法[12,27]。参与者也重复请求，改变语调以尝试让设备工作（在许多情况下，对设备的连续请求都使用更大的动力和重新安排），但我们在这里没有探讨这一点。

讨论
我们的研究结果的介绍侧重于VUI用户的实际成果，因此本身也是本文的主要贡献。然而，在这里，我们继续反思这项研究对于人类基因组学的影响。我们的观点具有广泛的概念性特征 - 我们不愿意确定强大的实际影响，并对随后的设计师和研究人员进行讨论。
“会话界面”的用词不当
虽然我们的片段清楚地显示VUI设备已成为日常对话的一部分，但我们拒绝这样的设备和接口本质上是对话性的概念，并且与接口的交互是对话。我们认为'对话交互'对于这种人机交互是一种误用，并且会在与实际对话的对话中将交互与设备混淆。虽然参与我们数据的参与者当然确实采用了谈话方法来完成Echo的各种活动，但根据我们的数据很难根据设备的情况来设定来自设备的响应与其所嵌入的对话具有类似的状态。
我们认为，'会话交互'这个术语是无用的，因为它没有区分VUI和对话的交互嵌入性。例如，考虑一下邻接对（例如问候，问题解答或提议接受），这是我们许多日常交流中使用的“原子”组织结构[32]。在邻接对中，第二对部分（例如答案）顺序且含蓄地与第一对部分（例如问题）关联。这意味着，第一对部分没有明显的独立特征，确切地说，它确实是一个问题;相反，只有第二对部分对待第一对部分（即我们可以说'答案产生问题'），第一对部分的问题特征才赋予该特征。与VUI的交互可以像对话中的邻接对那样展开，但重要的是，它被预先配置为通过设计以这种方式，而不是如上所述的交互展开的过程。例如，早期McTear将口语对话系统定义为“人与人交互的计算机系统”[19]。虽然我们并不反对这个定义，但所选术语可以很容易地将输入输出与逐轮讲话混淆在一起。然而，转角以及邻接对在截然不同之处在于它们是同时由人与人之间的相互作用形成的并且更新的构件块[10]。我们的数据显示了VUI交互方式与人类交互有着根本性的不同，从设备响应不一定遵循输入的方式来看也是如此。正如我们在片段4中看到的那样，Echo的回应可能会将教学分类为一个问题。虽然在日常会话中可以做到这一点（例如，看起来被指示做某事，人们可以回答“你问我，还是告诉我？”），Echo的用户似乎经常将其视为有问题且麻烦的输出这需要以某种方式或另一种方式进行修复，而不是将自己的话语重现为一个问题（这可能是对话者所做的事）。

如果没有设备能够“理解”谈话的逻辑模型（并且我们不想在这里开始讨论机器是否可以，这样的讨论已经在其他地方被广泛地讨论过，例如[3]），在这里我们只是寻求敏感HCI社区以怀疑的态度对待“对话交互”（及其派生词）这个术语，这与其他人质疑在使用具体行为的界面设计中使用“自然”这样的术语的方式大致相同。奥哈拉等人。 [22]指出，尽管将交互范式定义为允许人们“以自然倾向于的方式进行行为和交流”的叙述可以用于许多目的（例如，市场营销和与更广泛的受众沟通），但他们也发现框架问题。他们继续争辩说，“自然”界面的叙述仅将界面置于界面中，忽略了构成相互作用的基本原位和体现特征。在这项工作中，我们对这些问题的务实回应是阐明成员对“让这件事情起作用”的关注，并且放弃“与计算机交谈”的概念。因此，我们的数据显示与VUI的交互如何嵌入在谈话中，设备本身根本不被视为对话者，并且语音交互具有与对话完全不同的特征。
我们在这里采用的对话的跨学科视角认为，人们之间谈话必须遵循的预定义规则不存在，但是这样的“规则”被建立为对话者在情景和时刻的交互中的成就-时刻。然而，VUI目前在不同的平面上运行，只遵守预定的结构。这可以帮助他们提供用户交互的可预测性，但是当人类对话者对待它时，它显然是非对话的。因此，我们认为这一观点从将VUI的设计任务从对话设计转换为请求/响应设计的转变。

提出请求的责任
我们的第二点涉及请求设计：VUI设计师打算用户对设备说些什么，以及它们如何广泛地概念化交互设计中的必要话语。具体而言，我们认为请求设计从根本上需要考虑请求对设计者希望用户产生的上下文环境的投射责任。与VUI交互的嵌入性可能会让用户做额外的工作来使他们的行为负责。这种围绕他人进行社交交流的基本特征表明，VUI设计人员需要将其视为围绕他人采取并置行动而不是孤立（即请求必须对当前情况负责）的问题。存在各种可能的原因和情况，其中请求可能被视为需要明确的会计，例如当请求不适合于谈话方式或社交情况（例如家庭聚餐）时，或者也许这在某种程度上是令人尴尬的，或许多其他原因。
对于VUI用户来说，这不一定是个问题，因为VUI用户很容易在相关的情况下解决请求。相反，设计师可以从中受益是一种敏感。设计请求责任并不是要求根据请求赋予某些内在特征，使其能够负责，而是考虑如何在可能提出或嵌入设计请求的本地发生的对话中发出请求。换句话说，重要的是要认识到，我们在此讨论的问责制不是行动的属性，而是互动的成果。因此，设计师可能会问自己：“我们为用户设计的要求可能会在某些情况下出现尴尬吗？”，“他们什么时候可能不合适或者不常见？”，“用户需要做大量的会计工作围绕着别人？“。此外，在考虑请求设计的问责性与Dourish和Button [6]对“可观察到的可报告抽象”的反思之间有一个联系，它们提供了“使用户合理化系统活动并因此组织它们周围的行为，随着互动的进行，为了他们自己的实际目的“。

作为进一步互动的资源的回应
我们展示了我们片段中的家庭成员如何将反应（或没有反应）作为发生某种麻烦的指标。成员会根据VUI自身的响应分析其提供的有关VUI设备状态的“帐户”。我们的数据显示，作为提供此分析以便用户进行交互的资源，回应不足。为了提供更多的回应，设计师可能会认为Dourish和Button关于“可观察到可报告的抽象”的建议是有用的，这些建议不仅提供了关于系统正在做什么的线索，而且还提供了为什么它正在完成以及可能会发生什么接下来要做的，特别是针对眼前的情况“[6]。
例如，我们发现，由于参与者修复了与Echo的互动，他们还试图找出麻烦来源，无论是系统问题还是转录问题。只要可以通过VUI实现，设备的响应就是系统状态的主要“账户”和麻烦指示器：无响应（静音）也被视为麻烦的指示器，但它不提供任何机制进一步互动，并没有提供系统的状态，将VUI与“黑匣子”的概念联系起来。
相反，来自VUI的响应提供了设备的活动或其处理的转录以及接下来可能发生或暂时不发生的转录，为其用户提供了可支持和偶然与VUI设备进行进一步交互的资源。在设计响应时，我们可能会建议设计人员考虑如下问题：“这种响应是一种相互作用的死胡同吗？”，“这种响应为可能的下一个请求产生提供了什么资源？”，“这可能是什么？响应？“，”用户可能会在哪些时候中断并采取下一个转向？“，以及”响应设计如何采用静默的时刻？“。因此，我们提出了一个概念性转变，即将响应设计视为用户互动资源的设计，而不是像一个想象中的“脚本”交互的短语。
结论
这里介绍的分析说明了VUI的使用如何被常规考虑并嵌入到谈话交互中。通过从我们从多个家庭收集到的亚马逊Echo使用记录集中抽取一些片段，我们的研究结果揭示了Echo的使用是如何在“家中”进行的，如位于行为，并嵌入在家庭生活中，而不是一个独立的单一孤立事件。我们的数据显示，与VUI交互的初始阶段是通过其现成可用性实现的，但用户仍然可以在给定使用完成的社会背景下有条不紊地解决请求。我们还解压使用VUI，按顺序组织在家中通话。最终，我们确定了使用VUI的两项协作活动：在谈话中处理设备，并处理来自设备的响应。最后，我们转而将我们的研究成果从相互作用问题转移到概念性讨论要点，以便通知和塑造有关使用VUI的未来研究和设计。

## 参考文献
REFERENCES
1. J. Maxwell Atkinson and John Heritage. 1984. Transcript Notation. In Structures of Social Action: Studies in Conversation Analysis. Cambridge University Press, ix–xvi. https://doi.org/10.1017/CBO9780511665868
2. Liam Bannon, John Bowers, Peter Carstensen, John A. Hughes, Kari Kuutii, James Pycock, Tom Rodden, Kjeld Schmidt, Dan Shapiro, Wes Sharrock, and Stephen Viller. 1993. Informing CSCW System Requirements. In COMIC Deliverable 2.1.
3. Graham Button, Jeff Coulter, John R. E. Lee, and Wes Sharrock. 1995. Computers, Minds and Conduct. Polity Press, Cambridge, UK.
4. Andy Crabtree, Steve Benford, Chris Greenhalgh, Paul Tennent, Matthew Chalmers, and Barry Brown. 2006. Supporting Ethnographic Studies of Ubiquitous Computing in the Wild. In Proceedings of the 6th ACM Conference on Designing Interactive Systems (DIS ’06), 60. https://doi.org/10.1145/1142405.1142417
5. David DeVault, Ron Artstein, Grace Benn, Teresa Dey, Ed Fast, Alesia Gainer, Kallirroi Georgila, Jon Gratch, Arno Hartholt, Margaux Lhommet, Gale Lucas, Stacy Marsella, Fabrizio Morbini, Angela Nazarian, Stefan Scherer, Giota Stratou, Apar Suri, David Traum, Rachel Wood, Yuyu Xu, Albert Rizzo, and Louis- philippe Morency. 2014. SimSensei Kiosk: A Virtual Human Interviewer for Healthcare Decision Support. International Conference on Autonomous Agents and Multi-Agent Systems, 1: 1061–1068.
6. Paul Dourish and Graham Button. 1998. On “Technomethodology”: Foundational Relationships Between Ethnomethodology and System Design. Human-Computer Interaction 13, 4: 395–432. https://doi.org/10.1207/s15327051hci1304_2
7. Hasan Shahid Ferdous, Frank Vetere, Hilary Davis, Bernd Ploderer, and Kenton OHara. 2016. Technologies At Mealtime: Collocated Interactions In The Family Home. In CHI ’16 Workshop on Proxemic Mobile Collocated Interactions.
8. Harold Garfinkel. 1967. Studies in Ethnomethodology. Prentice-Hall.
9. Nigel Gilbert, Robin Wooffitt, and Norman Fraser. 1990. Organising Computer Talk. In Computers and Conversation (1st edition), Paul Luff, David Frohlich and Nigel Gilbert (eds.). Academic Press, 235 – 257.
10. Charles Goodwin and John Heritage. 1990. Conversation Analysis. Annual Review of Anthropology 19, 1: 283–307. https://doi.org/10.1146/annurev.an.19.100190.001435
11. Christian Heath, Jon Hindmarsh, and Paul Luff. 2010. Video in Qualitative Research. SAGE.
12. Jiepu Jiang, Wei Jeng, and Daqing He. 2013. How Do Users Respond to Voice Input Errors?: Lexical and Phonetic Query Reformulation in Voice Search. In Proceedings of the 36th International ACM SIGIR Conference on Research and Development in Information Retrieval (SIGIR ’13), 143–152. https://doi.org/10.1145/2484028.2484092
13. Mohammed Waleed Kadous and Claude Sammut. 2004. InCa: A Mobile Conversational Agent. PRICAI 2004: Trends in Artificial Intelligence 3157: 644–653. https://doi.org/10.1007/978-3-540-28633-2_68
14. Stefan Kopp, Lars Gesellensetter, Nicole C. Krämer, and Ipke Wachsmuth. 2005. A Conversational Agent as Museum Guide – Design and Evaluation of a Real- World Application. In Lecture Notes in Computer Science, 329–343. https://doi.org/10.1007/11550617_28
15. Stephen C. Levinson. 1983. Pragmatics. Cambridge University Press.
16. J. C. R. Licklider. 1960. Man-Computer Symbiosis.
IRE Transactions on Human Factors in Electronics
HFE-1, 1: 4–11. https://doi.org/10.1109/THFE2.1960.4503259
17. Ewa Luger and Abigail Sellen. 2016. “Like Having a Really Bad PA”: The Gulf between User Expectation and Experience of Conversational Agents. In Proceedings of the 2016 CHI Conference on Human Factors in Computing Systems (CHI ’16), 5286–5297. https://doi.org/10.1145/2858036.2858288
18. Moira McGregor and John Tang. 2017. More to Meetings: Challenges in Using Speech-Based Technology to Support Meetings. In Proceedings of the 20th ACM Conference on Computer-Supported Cooperative Work & Social Computing (CSCW ’17). https://doi.org/10.1145/2998181.2998335
19. Michael McTear. 2002. Spoken Dialogue Technology: Enabling the Conversational User Interface. ACM Computing Surveys 34, 1: 90–169. https://doi.org/10.1145/505282.505285
20. Michael McTear, Zoraida Callejas, and David Griol. 2016. The Conversational Interface. Springer International Publishing. https://doi.org/10.1007/978-3- 319-32967-3
21. Dong Nguyen, A. Seza Doğruöz, Carolyn P. Rosé, and Franciska de Jong. 2016. Computational Sociolinguistics: A Survey. Computational Linguistics 42, 3: 537–593. https://doi.org/10.1162/COLI
22. Kenton O‘Hara, Richard Harper, Helena Mentis, Abigail Sellen, and Alex Taylor. 2013. On the Naturalness of Touchless : Putting the “Interaction” Back into NUI. ACM Transactions on Computer- Human Interaction 20, 1: 1–25. https://doi.org/10.1145/2442106.2442111
23. Sabine Payr. 2013. Virtual butlers and real people: styles and practices in long-term use of a companion. In Your Virtual Butler, Robert Trappl (ed.). Springer- Verlag Berlin, Heidelberg, 134–178. https://doi.org/10.1007/978-3-642-37346-6_11
24. Hannah R. M. Pelikan and Mathias Broth. 2016. Why That Nao?: How Humans Adapt to a Conventional Humanoid Robot in Taking Turns-at-Talk. In Proceedings of the 2016 CHI Conference on Human Factors in Computing Systems (CHI ’16), 4921–4932. https://doi.org/10.1145/2858036.2858478
25. Stefania Pizza, Barry Brown, Donald McMillan, and Airi Lampinen. 2016. Smartwatch in vivo. In Proceedings of the 2016 CHI Conference on Human Factors in Computing Systems (CHI ’16), 5456–5469. https://doi.org/10.1145/2858036.2858522
26. Martin Porcheron, Joel E. Fischer, Moira McGregor, Barry Brown, Ewa Luger, Heloisa Candello, and Kenton O’Hara. 2017. Talking with Conversational Agents in Collaborative Action. In Companion of the 2017 ACM Conference on Computer Supported Cooperative Work and Social Computing (CSCW ’17 Companion), 431–436. https://doi.org/10.1145/3022198.3022666
27. Martin Porcheron, Joel E. Fischer, and Sarah Sharples. 2017. “Do Animals Have Accents?”: Talking with Agents in Multi-Party Conversation. In Proceedings of the 20th ACM Conference on Computer-Supported Cooperative Work & Social Computing (CSCW ’17). https://doi.org/10.1145/2998181.2998298
28. Stuart Reeves and Barry Brown. 2016. Embeddedness and Sequentiality in Social Media. In Proceedings of the 19th ACM Conference on Computer-Supported Cooperative Work & Social Computing (CSCW ’16), 1050–1062. https://doi.org/10.1145/2818048.2820008
29. Jacob M. Rigby, Duncan P. Brumby, Sandy J. J. Gould, and Anna L Cox. 2017. Media Multitasking at Home. In Proceedings of the 2017 ACM International Conference on Interactive Experiences for TV and Online Video (TVX ’17), 3–10. https://doi.org/10.1145/3077548.3077560
30. Sean Rintel, Richard Harper, and Kenton O'Hara. 2016. The Tyranny of the Everyday in Mobile Video Messaging. In Proceedings of the 2016 CHI Conference on Human Factors in Computing
Systems (CHI '16). ACM, New York, NY, USA, 4781- 4792. https://doi.org/10.1145/2858036.2858042
31. John Rooksby, Timothy E. Smith, Alistair Morrison, Mattias Rost, and Matthew Chalmers. 2015. Configuring Attention in the Multiscreen Living Room. In Proceedings of the 14th European Conference on Computer Supported Cooperative Work (ECSCW ’15), 243–261. https://doi.org/10.1007/978-3-319-20499- 4_13
32. Harvey Sacks. 1992. Harvey Sacks: Lectures on Conversation. Basil Publishing, Oxford.
33. Harvey Sacks, Emanuel A. Schegloff, and Gail Jefferson. 1974. A Simplest Systematics for the Organization of Turn-Taking for Conversation. Language 50, 4: 696–735. https://doi.org/10.1353/lan.1974.0010
34. Emanuel A. Schegloff. 1987. Analyzing Single Episodes of Interaction: An Exercise in Conversation Analysis. Social Psychology Quarterly 50, 2: 101–114.
35. Emanuel A. Schegloff. 2007. Sequence Organization in Interaction. Cambridge University Press, Cambridge. https://doi.org/10.1017/CBO9780511791208
36. Tanya Stivers, N. J. Enfield, Penelope Brown, Christina Englert, Makoto Hayashi, Trine Heinemann, Gertie Hoymann, Federico Rossano, Jan Peter de Ruiter, Kyung-Eun Yoon, and Stephen C Levinson. 2009. Universals and cultural variation in turn-taking in conversation. Proceedings of the National Academy of Sciences of the United States of America 106, 26: 10587–92. https://doi.org/10.1073/pnas.0903616106
37. Peter Tolmie and Andy Crabtree. 2008. Deploying Research Technology in the Home. In Proceedings of the 2008 ACM Conference on Computer Supported Cooperative Work (CSCW ’08), 639–648. https://doi.org/10.1145/1460563.1460662
38. Peter Tolmie, Andy Crabtree, Tom Rodden, and Steve Benford. 2008. “Are You Watching This Film or What?” Interruption and the Juggling of Cohorts. In Proceedings of the ACM 2008 Conference on Computer Supported Cooperative Work (CSCW ’08), 257. https://doi.org/10.1145/1460563.1460605
39. Sherry Turkle. 2011. Alone Together: Why We Expect More from Technology and Less from Each Other. Basic Books.
40. Laura Pfeifer Vardoulakis, Lazlo Ring, Barbara Barry, Candace L. Sidner, and Timothy Bickmore. 2012. Designing Relational Agents as Long Term Social Companions for Older Adults. In Intelligent Virtual Agents. 289–302. https://doi.org/10.1007/978-3-642- 33197-8_30
41. Robin Wooffitt. 1994. Applying Sociology: Conversation Analysis in the Study of Human- (Simulated) Computer Interaction. Bulletin de Méthodologie Sociologique 43, 1: 7–33. https://doi.org/10.1177/075910639404300103
42. Victor Zue, Stephanie Seneff, J. R. Glass, Joseph Polifroni, Christine Pao, T. J. Hazen, and Lee Hetherington. 2000. JUPlTER: a telephone-based conversational interface for weather information. IEEE Transactions on Speech and Audio Processing 8, 1: 85–96. https://doi.org/10.1109/89.817460