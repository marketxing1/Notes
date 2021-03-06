>Bancor算法让所有参与者都能够随时随地与智能合约系统的资金池进行交易，无需经过中心化交易所，无需撮合交易，也避免的交易深度不足的问题。

![](https://upload-images.jianshu.io/upload_images/10409266-01a9757f90a4de35?imageMogr2/auto-orient/strip%7CimageView2/2/w/900/format/webp)

## 背景
Bancor 算法之所以命名为「Bancor」，是为了纪念 1943 年在布雷顿森林会议上提出「超主权货币 Bancor」的经济学家凯恩斯。二战结束后，世界各国代表于 1943 年在美国布雷顿森林探讨一套新的国际货币机制，凯恩斯提出了「国际清算同盟计划」，美国经济学家怀特提出了另一套计划，即后来的布雷顿森林体系的原型。

在凯恩斯「国际清算同盟计划」中，提出了建立全球中央银行，并发行超主权货币「Bancor」，根据二战前三年各国进出口贸易额的 75% 在各国政府间分配「Bancor」份额。而怀特提出的布雷顿森林体系最核心的几点，即：

1. 美元与黄金挂钩；
2. 其他国家货币与美元挂钩；
3. 实行固定可调整汇率制度；
4. 美元等同黄金，成为各国储备货币等。

无论是凯恩斯计划，还是怀特计划，所解决的问题都是在各国主权分别发行货币与全球经济流通面临的不平衡问题。凯恩斯计划是在美国经济体占全球经济体很高程度下创建超主权「Bancor」，但是只要美国美元不参与，该计划必然无法阻挡具有强势购买力的美元经济强势入侵。后来，布雷顿森林体系锚定黄金价值，1971 年崩溃后世界完全进入美元信用时代，至此美元基本发挥了全球统一货币的作用。

## Bancor算法
IBO，全拼Initial Bancor Offering，翻译过来就是首次基于Bancor协议的token发行。

Bancor最大的特点是，不需要传统数字货币交易需要的对手盘，有效解决了绝大部分小币种流通性不足的问题，相当于以智能合约担当了传统金融市场做市商的角色，实现了价格公开透明、随时随地的人机交易。

Bancor算法背后有一套数学模型，这个模型的重点是纳入了市场需求的因素，根据需求状况的变化来自动计算出Token的价格，随着池子里Token越来越少，价格会越来越高。

简单而言，在Bancor系统中，币价主要的决定因素是代币的供求关系，当代币稀缺时价格上升，反之下降。

![](https://mmbiz.qpic.cn/mmbiz_png/uucS886wJhfM8nYMsMAoaRSno0IA7ZmicB0hibXOnkSBU4JsibegVWuW91hWnjHl2XonialsYgibicejEzDFQqfdUNQA/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![](https://mmbiz.qpic.cn/mmbiz_png/uucS886wJhfM8nYMsMAoaRSno0IA7ZmicNib0aqlRJ3V4n907BFnAmQwsXFibic5eK7JX6nDsBhhQSQ8TBRAibrh50Q/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

在Bancor算法中，有三个重要参数：
*   准备金池 r（或连接器池 connector balance）
*   杠杆率（或 CW connector weight 或连接器比重）
*   以及智能代币供给量 s（supply 或中转代币）
  
另外，储备金增量与智能代币增量存在一个对应的数学关系。通过这两套公式，可以画出类似的下面四个模型。

![](https://mmbiz.qpic.cn/mmbiz_png/uucS886wJhfM8nYMsMAoaRSno0IA7ZmicsvXug0M1KKcRVTwia92qyP4AWxf4voRy5CbjCYuTwc9WOibmVzn0GURA/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

CW取值在0~100%之间，具体由项目团队来设定。CW 值设置的越小，供求关系对币价的影响也就越剧烈。不同的项目CW值差异很大，这也就造成了不同项目价格波动程度的巨大差异。

当CW=100%时，智能Token供应量变化时，其价格稳定不变；

当CW=50%时，价格与供应呈线性相关，价格随着供应增加线性增长；

当CW介于0%-50%之间时，价格随着供应的增加呈类似“指数”式快速增长；

当CW介于50%-100%之间时，价格随着供应的增加只有少许增加。

## Bancor协议


## IBO的优点
以往的I-C-O模式可谓是弊端频现，在项目的初始阶段项目方仅凭白皮书就有可能募集到大量的数字货币，这就导致很多项目方失去了继续把项目做好的动力，很多项目方把更多精力花在市值管理或者操纵币价上，更有不少项目方圈钱之后便放弃了项目的推进，同时行业中也出现了大量仅以融资为目的的空气项目。正是这种种的乱象，I-C-O已经被包括我国在内的很多国家明令禁止或重点监管。

**在一个标准的IBO发行中，项目方需要按照设定的比例，首先抵押一定价值的另一种Token 作为“准备金”，而后就是完全通过智能合约去实现Token的发行和流通，项目的资金被被锁定在了智能合约之中，随时接受着大家的监督**。因此IBO模式也就衍生出了以下诸多的优点。

### 1、资金更加安全和透明

Bancor协议下的交易，**其本质上是在智能合约中进行的地址之间的直接交易**，交易本身是自动进行的无需人为干预，这也就很大程度上摆脱了交易环节中的各种风险。

此外，IBO项目无论是Token的发行环节和交易流通环节都非常透明，任何投资者希望获得Token都需要去合约池中去购买；如果项目方需要向合约池中释放Token，也都会有链上的记录。

这种透明的机制之下，如果项目方想要玩黑幕，私下做手脚难度就大了很多。

### 2、实现了人机交易，保证了足够的交易深度和便捷性。

此前，我们已经习惯去交易所购买数字货币，并不得不忍受着交易所对整个行业的无情盘剥。

而IBO的出现，完全改变了交易的形态，实现了真正的人机自动交易。**这时，我们的交易对象不再是市场中的其他投资者，而是变成了可以自动完成交易的智能合约以及项目资金池。**

因此，我们可以摆脱交易所，在任何时间进行买入或卖出的操作，智能合约可以随时与你进行交易，不用再担心交易深度不足的问题。

### 3、避免了高昂的上币费和市值管理成本

IBO的模式，尤其对区块链项目的初始阶段是非常有帮助的，可以实现快速的项目启动。以往一个区块链项目希望具备很好的流通性，就必须要争取能上到头部交易所进行交易。当然，这也就避免不了高昂的上币费用和市值管理成本，往往要千万以上的资金量，才有可能实现，几千万的费用仅仅是为了能上个大交易所，这钱最终从哪来呢，当然还是投资者，这就难怪很多项目方不去用心搞开发，而是整天想着控制币价割韭菜了。

而IBO的出现，实际上提供了一种新的可能性，让项目方可以完全绕开数字货币交易所，不仅避免了数千万的交易所上币费用，同时也缩短了项目的启动周期。比如最近的TPT，FIBOS等IBO项目，几乎都是瞬间启动并且成功募集大量资金的。项目方节省下了千万级别的开销，对我们投资者而言，当然是件好事了，可以上项目和整个行业都更良性，这就充分的体现了IBO的优势所在。

### 4、交易更公平，更难操作币价

区块链项目中，项目方或者大户拉盘砸盘操纵币价的的情况非常普遍，这种情况在IBO项目中将很难发生。所有交易都是在智能合约中进行的，价格也是根据预设的参数自动计算得出，如果谁想去拉盘或砸盘难度会更大，这也就增加了交易的公平性。因此我们会说，Bancor是一个在制度上更公平的交易机制。

## IBO的弊端和风险
### 1、新发Token需要与母币锚定，对后续发展有所束缚

前文我们提到过，IBO的发行需要锚定某种母币。比如，现阶段大多数的项目是以EOS为母币来发币的，母币本身可能价格波动很大，新发行的币价也自然受到影响。

锚定母币的方式，在项目的初期阶段并不会有太大的问题，而且是很有现实意义的。但从长远上来讲，如果项目发展顺利，独立运行和定价将成为一种必然方向。

目前的IBO项目，还没有成熟的脱钩机制出现，需要未来不断探索找到可行的脱钩方法。

### 2、长期投资收益的不确定性。

在Bancor协议中，只要掌握CW等重要参数，就能预测出价格与供求关系之间的变化曲线。尽管如此，作为投资者你也很难保证确定的盈利，因为未来的需求量将是非常难以预测的变量。

经历过EosRam价格大起大落的的朋友肯定对这点深有体会，最难的是把握公众投资情绪，投机热潮来的猛烈，砸盘来的更猛烈，尤其是项目初期投机情绪浓重之时，投机热潮会在什么时间戛然而止，非常难以预料。无论是EosRam还是FOMO3D都造成了很多追风的投资者高位接盘，损失惨重。

### 3、初期投资者优势明显

Bancor协议中，币价是由供求关系所直接决定，Token的使用量越小时，币价越低。这个机制就衍生出了一个制度性的缺陷：项目初始期的参与者，能用极低的价格买到代币，而后面的参与者成本会被推高很多，这种先入者的低价优势，也就造成不公平。

了解了这个规律后，新项目上线时，很容易会引起投资者哄抢，而之后到达一定高度后，早期低成本进入的人开始套现离场，而后币价开始下跌，更多人恐慌离场。只有在疯狂投机大起大落之后，币价才能趋于理性和稳定。

作为投资者我们需要充分了解这个特点，或者在启动最早期进入，或者就耐心等待币价波澜起伏真正归于平静理性后，再择机出手，建议一定不要在投机热潮之时跟风买入。

IBO模式的这个特点，也将是后续的IBO项目方所需要重点改进的。最近的一些IBO项目，也在尝试用初期超高手续费，后续不断降低手续费的方式来抑制初期的投机行为，相信后续也会有更多好的制度设计涌现。

总之，未来IBO模式的演进中，需要用心设计优化相关规则，才能避免项目初期的投机狂潮，吸引真正长期持有的投资者加入。

### 4、项目方的投机意图比较普遍

即使是真正有内在价值的模式，最初也很容易被投机者用到歪处，尤其在“赚钱才是最大的共识“的数字货币领域更是如此。

任何新模式出现后，都可能成为别有用心者的圈钱工具，项目方的圈钱意图我们不可不防。

目前，还只是IBO模式很初始阶段，我们今天所看到的IBO显然还并非该模式最好的一面，一定会有各种弊端显现，但这并不意味着该模式没有价值和发张空间。

就像最初，公众会误认为区块链等于传销，现在的IBO也很容易被理解为是资金盘属性的项目，主要是因为之前最有热度的几个IBO项目，大多是资金盘或博彩类项目所致，相信未来这种局面会被更多的优质项目出现所改变。但就目前而言，也确实仍有大量圈钱为核心意图的项目方正在利用IBO大作文章，这也是现阶段我们作为投资者不可不警惕的事实。

### 5、智能合约的安全性问题

再完美的代码也有可难免存在漏洞，包括运行了多年的以太坊，也不断有安全漏洞被发现。

Bancor协议是一个自动运行的智能合约，项目的资金池也通常存放在智能合约之中。目前几个IBO项目资金池的规模都很大，它们自然也会成为黑客未来的重要目标，智能合约很可能正在被越来越多的人研究和攻击，对于投资者而言，IBO这个新模式中智能合约的安全性风险也自然是存在的。


todo http://blockgeek.org/t/topic/1552
http://blockgeek.org/t/topic/1593
http://blockgeek.org/t/topic/1610
http://blockgeek.org/t/topic/1612