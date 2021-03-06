---
layout: post
title: 关于四个W和一个H的思考
category: think
---

#{{ page.title }}

<p class="meta">29 Oct 2013</p>

这个题目想了好久，也拖了好久，日后等到工作的时候会继续更新（这个博客的主要作用是用来记录自己的想法，更重要的是变化）

下图是对接下来要描述的五个重要内容的归类：这里我将产品设计分为五个方面（当然不仅仅是这些，例如商业权衡等，这里只是重点说这五点），它们分别为**角色，需求，操作，场景，核心**，而这五个方面共同构成两个最为重要的两个框架：**功能与设计**；

我暂时浅显地讲**角色，需求，操作**划归到功能层次上，而**场景，核心**划归到设计层次上。这样归类的理由在于：*功能层次需要知道为谁设计，设计什么，如何使用；而设计层次显然需要考虑更多，这其中最重要的是替使用者考虑更多，为其提供不可替代或难以超越的体验*

![wwhww](/assets/img/wwhww.png)

无论是大公司产品线开发，还是小团队创业需要，对于互联网相关的产品开发来说，快速高效是首要事宜，所谓的很多`设计`也许很多时候就是大家拍脑袋想出来的所以然，而不断迭代的结果，也可能在功能上徘徊了好久，很多时候我们所说的设计环节，差不离就是功能设计环节，远没有达到`设计`的层次，所以这里我将设计放在功能之上，其实也想说的是：**功能的实现还没有成为产品设计的全部，设计这一环节被说烂了（创新，用户体验什么的），但是在各种障碍面前（资金，排期，人力等），逐渐变为一个个细节的漏洞，不断腐蚀辛苦开发而来的`产品`，到头来果断堤溃蚁孔**

至于使用Who，What，How，Where，Which这五个单词，主要因为便于记忆与理解，同时也显得高端大气一些，没什么特殊原因；五点之间的关系不一定是逐步实施，也可以调整顺序与重要程度，总之还是需要具体情况具体分析，但总体上可以理解为五点之间全部具有**相互关系**

接下来开始细说这五点（仅凭目前经验和阅历总结的，留着以后看，那时可以嘲笑现在的自己）

##Who（角色）

>相比较于`用户`，我更喜欢`使用者`这个词，其实意思上没有差异，但是给我的感觉，它们的区别在于后者的使动作用更强（使产品能够用来完成什么），听起来亲切一些；

**行为模拟：**主要是对使用者的具体因素进行分析，包括**生活环境，学习能力，工作因素，态度，日常习惯，兴趣爱好，消费行为，常用工具，群体现象等**；这些数据的来源包括对现有线上数据的分析整理，用户的访谈和观察，产品人员自身体验式调查等

在这个环节上，开发人员或产品人员很容易因为一些阻碍（尤其是时间排期紧），而自然而然地主观感觉和臆测，这常常表现为`按照常理来说，普遍用户会……`，`他们应该不能……，`我就经常……，我觉得……`等等；对目标使用者的分析上，应该要从多个角度出发，全面综合地考虑问题，就好比和敌人在开展一场战争，对方的情报了解地越多越好，尽可能减少信息不对称所带来的错误判断

**角色建模：**在具备对使用者一定程度的信息了解基础上，需要对其**进行人物角色的建模**；这部分的主要目的是对使用者各种行为模拟的总结与归纳，将众多的问题与细节还原在一个相对容易理解的概念化角色上，起到设计与开发过程中的主干的作用，并由此不断延伸思考路线，进而推进设计；在遇到问题时也便于回归主题，从角色模型本身进行探讨与分析

这个阶段如果没有确定一个或多个相对具有代表性的角色模型，对于后续工作的开展十分不利。当产品设计进入到中后期时，会出现常见的两个问题是：

一方面大家会**逐渐被众多的细节点扰乱思绪，易造成脱离初衷的设计，难以理清思路**，由于离调研阶段已经一段时间了，产品人员对目标使用者的认识本就因没有建立角色模型而不是十分清晰，此时便更无从追溯；而**开发人员也会在开发的过程中，产生较多的“想法”（删减功能，调整结构，优先级变化等；而BOSS也可能参与进来说几句），这时在产品人员与开发人员的沟通中，易于产生思想上的小矛盾，却又不容易调和，往往会脱离使用者的角色内容，而在某个`功能`上`不相上下`，到后来产品开发出来后，都不清楚当初是怎么想的，为什么这么想；**对了，是各方妥协的结果么？**

##What（需求）

>对于需求的发现，研究，解决方案设计等环节，要时刻结合角色模型，对其进行**故事描述**，将使用者的一切需要以故事的形式总结与归纳，不仅是帮助产品人员思考设计方案，也有利于开发人员时刻明确开发目标及重点

**目标需求：**基于之前的角色模型，目标的确定依托于将产品置于角色模型使用条件下，发觉能够帮助他们完成目标的要点，总结并得出核心目标，作为设计阶段的主要解决问题

解决好目标需求才是一个产品真正的存在价值，下面的三种需求或者其他种类的等等，都不是成为你的产品最有价值点，不过这一切的前提就是首先要明确目标需求；

真正的明确目标需求并不是类似于`我知道椅子是用来给人坐的`，`茶杯可以喝茶，哦，或者喝水等`；优秀的需求分析会结合了众多的要素，**用户行为，目标，工具，心理，困难等**，在角色模型的基础上不断深入研究与总结，不断拨开一些**表面现象**；毫无疑问，这离不开对使用者的充分了解，也就是上面Who（角色）中所阐述的。赶排期的产品也许在这一点上就已经开始埋下炸弹，后续不管在总体定位上，还是产品细节上，问题总会随即发生

**衍生需求：**在明确使用者的目标需求的基础上，适时且适当地兼顾考虑到其相关的衍生需求，这些需求的特点是_具备一定的使用频率，但相对小众；碎片化，开发难度不小于核心功能；可复制性高，易于被竞品复制或改进；学习成本不低，易使产品逐渐臃肿复杂_

这一方面也可以理解为产品的`弱化功能`，`附加功能`，`彩蛋`等。从竞品的角度讲，当市场上大部分产品都具备的功能，也应纳入设计范畴中，至少不能少于竞品。但这样一来是否是真的有必要设计这些衍生需求（对应越来越丰富的功能模块），也是一个产品人员值得考究的地方

一方面，市场上的众多产品纷繁的功能会在各个角度满足这些衍生需求，使用户形成一个惯性`其他产品都有的功能，怎么就他家的没有？！`；另一方面，这些越来越丰富的功能会使产品逐渐变得**愈渐臃肿，学习成本增加，操作复杂等**问题接踵而至，更为重要的，产品设计的中心难以取舍，不能做好平衡，容易顾此失彼

**潜在需求：**这是一个开拓的领域，是在角色模型的基础上深入分析的结果，它和衍生需求的界限其实并不是很明确，如果一定要说出区别，最大的便是潜在需求给了产品人员更多的思考空间，更易于创造新的增长点，但同时风险也要更大一些

像前面说到的，在对角色的分析上，我们力图找到其主要矛盾时，也会发现一些`衍生需求`，如果进一步分析与思考，结合众多的因子（心理模型，群体影响等），便会得到更为潜在的结论。这一点在内容产品上较为明显体现在**推荐系统**上，在工具产品上主要体现在**隐藏功能**上

在不影响整体产品简易性的前提上，适当的挖掘使用者的潜在需求，利于为产品营造`彩蛋`，**优秀的用户体验是能够超出用户预期，并做到更好的**，这虽然主要在说目标需求的满足方面，但也同样适用于潜在需求；**当使用者发觉突然而来的问题竟然在产品中已经预设了解决方案**，必然会对产品好感大增；最后话说回来，这样的情况并不多见，更多的是产品`一厢情愿`，功能多到使用者反感

**错误需求：**这点是指使用者认为应该有的功能，而产品却没有提供；产生原因是因为使用者自身对目标的认识不足，对产品的学习热情不高，以较为强烈的主观认识去使用产品，往往会对某些功能的设计理由产生怀疑，甚至抱怨产品设计出错

本着不能指责使用者的原则，最好的解决办法就是将设计优化，不断提高易用性和简洁性，功能越来越`一目了然`，很多误解和误操作便可以尽可能避免

##How（操作）

>好的操作原则非常清晰，但却最难把控；一切要尽可能简单，尽可能短的步长，尽可能明确的导向；总之最快速地帮助使用者完成目标，然后满意地关闭产品

**导向清晰：**产品在不断完善的过程中（想法-原型-模块-成型-优化等），功能越来越多，操作越来越集中，也越复杂，不可忽略的问题就是让使用者时刻明确**现在我在哪，上一步是什么，下一步做什么，如何退出，全局目录，子级目录，还有众多的按钮位置，设置选项等等**，这些都离不开清晰有效的导向设计

无论是软件，网站，APP还是其他产品，都比现实生活中的实体产品要更加让人容易愤怒，烦躁；因为使用者无法真实感受其实体感，只能在GUI界面中不断尝试，这无异于临时进入一个大型商场，你知道里面商品琳琅满目，但是否能够找到目标店铺，买到想要的商品就不那么容易了

在产品操作设计中需要为使用者考虑两点：**控制感，方向感**，提供尽可能清晰的导向，不仅使人能够明确流程，梳理操作流，更能够增强用户使用产品的学习能力，减少很多不必要的错误；

最后，也是最重要的一点：**反馈**，每一个工作流都包含操作和反馈，反馈起到使用过程中`承上启下`的关键作用；如果说我们在使用产品的过程中就是与产品的对话，那么反馈无异于是这次对话中一个个关键的总结话语

**减少干扰：**精简UI控件，避免花哨不适用的设计；删除所有能够去除的指示或说明，好的设计不需要这么多讲解；让关键性反馈在恰当的时候出现，巧妙地融入界面中，形成统一，及时，文案精简的反馈

**主次分明：**产品是一系列功能的集成，这本身也决定了其较为复杂，需要依据需求的优先级，对功能进行相应的突出或者弱化；解决目标需求的功能应该使用最短的路径，放置在最明显的位置，控件的排序也应做相应的调整等等

对功能进行优先级排列的目的，是基于需求的优先级排列，而需求的优先级排列，是基于角色模型的分析；主次分明可以理解为对功能的回溯设计，**分析并归类目标需求，衍生需求，潜在需求，错误需求等**

##Where（场景）

>这是产品设计必须也非常重视的方面，但是从功能层次，往往难以对其深入分析与利用，在角色模型的基础上，场景（情境）模拟与建模也同样重要，很多时候也可以融入到角色建模中，但不建议这样做

**常见情境：**基于角色模型，基于目标需求，常规用户的操作情况；可以将使用流程进行**基于角色的剧本化演绎**，其中包含抽象的内容（情绪干扰，态度转变，学习能力，生活状态等），也包含实体内容（街道，办公室，陌生人，同事，情侣，儿女等），当然最重要的是使动或被动状态（行走中，准备午休，内心困扰，随机查询等）

**突发状况：**更适合于情景化设计，充分不可控的突发事件及状态，对功能进行**预防性设计**，保障操作的无损进行。典型例子为软件下载中掉网，自动暂停；文件编辑过程中软件关闭，保留副本；单机游戏操作过程中不小心退出，保留即时游戏记录或回滚数据等

**切换模式：**进一步的情景化设计，将情境处理方案打包，为使用者提供快速的集中式功能切换；不仅满足了软件的灵活性需求，也为用户提供了清晰的使用选择。典型例子为3G/Wifi环境下载切换；保护者视图/编辑者视图；定时关闭模式/无限播放模式等

**丰富预设：**以`控制欲`为主，满足用户（专业或资深用户）的产品控制感，能够进行更多的**个性化设置**，从而对产品有着一定的调整（字号，背景，主题，信息流顺序，隐私设置等）；这是产品对使用者的`开放`的一种设计

对于基础用户，提供较为完整常规的预设，而对于高级用户，也提供高级设置的`后门`，可以通过适当的**隐藏**来做好在不同层次用户之间的权衡

##Which（核心）

**专注痛点：**简单说就是一心做好某个需求点，真正读懂目标受众，了解他们最需要的，深入长久地解决这些问题，并配备愈加专业的设计；在如今互联网`集体快速`的大环境下，不断地尝试与周全地考虑，往往与专注背道而驰

**保持独特：**产品的设计理念，UI控件，导向设计，操作流程等，在设计的过程中有着产品独有的，或者做的更好的一套`风格`，并不是必须的内容，但是在做好产品的同时，也会为产品赋予一定的特色，**真正好的产品页需要自己的性格**

**有效改动：**随着技术的发展，开发方法的更新等，产品必然会迭代版本，而在不同的版本更新之中，确保每一次的改动是有必要的（有效的功能提升，Bug修复，界面重大调整等）；不要有过多的版本，每一次的更新与改版，都有着非常值得一改的理由，否则容易弄巧成拙






















