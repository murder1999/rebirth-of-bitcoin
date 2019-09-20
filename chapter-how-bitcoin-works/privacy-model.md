# 比特币隐私模型

比特币拥有一个非常简单，但相当强大的规模化隐私模型。通过 UTXO 和找零机制，可以让人们能够在交易记录有迹可寻的情况下，尽力保护好自己的隐私。其中最重要的一点是：不要重复使用地址。

白皮书第 10 节以非常简单的方式描述了隐私模型的细节。但是，大多数人似乎并不理解它。

![](https://miro.medium.com/max/2666/1*SJ5XfjYfgG0qt5h-jOs9AA.png)

图片的左边，是系统的隐私部分。右边，是开放的，可以看到的。这是大多数人没有理解比特币的地方。Core 团队首先提出了比特币类似于银行业的概念，并开始移除使比特币成为点对点隐私系统的大部分元素。

## 传统模式

在传统的隐私模型中，用户需要与第三方 (如银行) 一起完成 AML/ KYC 流程。第三方处在所有交易的中间，拥有账户资金内外流动的全部信息。不向公众提供任何信息，但任何漏洞都是灾难性的 --- 需要一个系统长期维护安全。

其结果, 这一个设计脆弱的系统。

银行离免疫非法的信息泄露还有很长的路要走。更重要的是，[PII(个人身份信息, Personally Identifiable Information)](https://www.investopedia.com/terms/p/personally-identifiable-information-pii.asp)允许更广泛的信任违反。该模型中的信息泄露不仅泄露了相关直接各方的活动，而且允许攻击者 (犯罪分子) 利用这些信息从事诸如身份型型盗窃犯罪等。

比特币通过创造一个真正的点对点环境，解决了这个问题。 P2P 不是节点，也不是挖矿。P2P 是个人对个人。你这个点就是交易中的另一方。理想情况下，使用 IP-2-IP 就是这样，甚至允许从 [客户到商家](https://medium.com/@craig_10243/instant-transactions-a11f391fbd57) 的直接交换。矿工仅在双方协商完成，**接受方** 将交易广播给区块链时才参与进来。

**发送**交易的人根本不需要在线。它们不需要节点，甚至不需要 IP 地址。使用 NFC，他们可以登录，下载区块头，并在以后更新他们的地址变化(或者甚至可以在一个完全独立的系统上拥有这个密钥)。

在传统模型中，可信任的第三方知道你所做的一切。银行或信贷机构保存着所有取款、取款地点和交易细节的记录 --- 包括你与谁打交道以及如何打交道。他们不希望这种情况发生改变，因为这些数据实际上是有价值的信息。

在这个模型中，银行 (或者其他 TTP) 会记录你的每一个行动，每一笔交易，并且可以建模你的所有消费行为。在 Visa 和万事达看来，这些信息可以让他们知道需要把消费者推向何方，从而欠下更多债务。它允许 TTPs 持有足够的信息来控制市场，操纵消费者。

这些 [数据是价值](https://www.ey.com/Publication/vwLUAssets/EY_-_The_upside_of_compliance/%2524FILE/EY-The-upside-of-compliance-Steven-Lewis.pdf)，也是信息。作为信息，他们可以直接做广告，并高价出售。这就是陈旧的、不安全的、可操纵的、前隐私模式的结果。比特币 core, 还有其他如闪电、Plasma 等复制了这个模式。现在，[你的信息是这家银行拥有的最有价值的东西，](https://www.globalbankingandfinance.com/why-data-has-become-banks-most-important-commodity/) 这就是他们反对比特币的原因。他们不想失去它。这就是为什么我们看到比特币被劫持，为什么他们试图告诉你它不安全，不是隐私的，以及你听到的所有其他谎言的原因。这些人希望保留你的数据，因为这些数据有价值。

传统的银行模式通过限制相关方和可信第三方对信息的访问来保护隐私。这也是今天的 Bitpay、 Coinbase 和大多数比特币公司系统。

这不是比特币要设计的。

## 比特币的新模式

新的隐私模式非常简单。交易都是公开的，因为它们不与你的身份相连，也与任何特定的商家无关。重要的是，商家也希望保持隐私。竞争对手分析公司的能力导致商家建立多个地址，就像用户一样。

因此，如果一个商家不想公布他们的销售量和每笔销售额，他们需要确保他们不重复使用地址，而且这些地址不会以公众或竞争对手可以知晓的方式相互联系起来。

**核心概念是，我们不重复使用密钥**

### 币的分割

关于孩子购物和找零总有一些麻烦。像比特币中的许多事物一样，人们总把事情搞得比应有的复杂得多。为了拥有一大堆可以随意快速花掉的币，我们可以把这些币分割，在需要再把它们组合起来。有时，购物者可能需要在短时间内走很多地方。如果能够分割比特币，他们这样做便很安全。

提前分割币，所花矿工费不到一分钱。

![](https://miro.medium.com/max/962/1*Exh4c6qJv1vOgJEPZqQ8cA.png)

像 Core 之流团体之所以反对比特币白皮书第 9 节的结构，是因为他们反对比特币扩容。随着交易的增加，系统变得更大，也更隐私。比特币有如下事实，即允许创建、分割和重新组合大量 in-out 交易，从而使得系统可以在没有大量未验证交易链的情况下使用，并允许 SPV 良好运行。

比如，我们有 2 个 BSV 币, 当我们逛一家旅行商店时，可以分裂它。预计通常在 5-20 分钟内，这些币可以分解到一个区块里。从一个 UTXO 币，现在我们在一个区块里有了多个可以花费的币。这样, 如果我们担心交易中的任何隐私问题，就已经创造了一种更深层次的不透明。商家无法确定我们是在 Tx 1 级支付, 还是在 Tx 0 级支付。

![](https://miro.medium.com/max/1798/1*qeHJhwwcRLs2G3u-1jLctQ.png)

在单个区块中，我们现在有许多分割的交易。这些币中的每一枚都与 Tx 的 0 级币相关联，但只有一条通道。 一个商人不能讲在某个时刻已把这些币分割给另一个商人了，也不能说正在分割你的币。

如果你稍微随机地分割这些币，可以变得更隐私。此时，你可以使用多个 input 和 output，如果这些分割没有再次连接，也就没有简单的方法将各种花费联接起来。

使用此方法时，任何时候花掉的币都在 UTXO 集里，作为一个区块的已验证交易。 在这里没有必要立即花掉零钱。

当我们看到比特币被设计成一个商业系统，而不是一堆简单的树莓派机器时，我们方能理解它有多么强大，又多么简单。

### 商户地址

比特币被引入的一个主要缺陷是重复使用地址。人们在静态页面上公布地址。比特币的真实设计是，用户和商家只能使用一次密钥。

这样就能充当安全和隐私的防火墙，并阻止交易连接到一个地址的共同所有者。没有任何实际理由保留密钥对。一旦密钥已签署和使用，就可以删除和抛弃。通常发送一、两个 satoshi 金额的微小 "垃圾交易"，是不删除旧密钥的直接后果。

如果不保存密钥又希望从一个旧地址中获得钱，是没有动机向这些旧地址发送少量比特币的。这等同于向一个从未见过的随机公私密钥对发送比特币，对任何人都没有价值。

一个为每次、每笔交易创建新地址的商人可以提高他们的隐私。如果使用一个单一的公共钱包和地址结构，那么企业收集情报就很简单。而变换地址时，商家不会留下任何可供分析的东西，对他们自己和客户都更加隐私。

如果我去沃尔玛或者乐购超市购物并收到零钱，这些币现在是分割的。来自沃尔玛找零的一组交易的价值是无法分析的。单单沃尔玛每天就有超过 1500 万笔交易。 也就是在运营时，大约每秒超过 400 次交易。

有趣的是，没有一台现存的超级计算机能够通过分析比特币区块链来匹配未知来源的比特币，但同时，该系统在最短的搜索时间内又是可追踪的(例如税务审计)。

让比特币运行良好的关键不是增加复杂性，而是像最初设计的那样使用它。

随机分割增加更多的隐私。

比特币的一切都是基于经济激励。如果愿意，我们可以通过模拟使用，采用一种方式在钱包和分裂币之间发送，使我们的钱包更安全和更隐私。现在，没有钱包可以做到这一点，用户需要完全靠手动才能完成整个过程。这在代码中很容易实现，但是还没有部署，因为困扰比特币的概念仍然偏向于滥用。

在下面的例子中，我们以两个设备上的币(等级 2 对等级 3) 结束，产生许多币。如果币保持分离，我们保持颜色组分离，我们现在可以看到如何使分析来源变得越来越困难。

![](https://miro.medium.com/max/1958/1*VJlKy23kMLARRG3d4IOTjg.png)

随着我们保持这种分割，分析出用户连接习惯的概率呈指数级减少。

### 隐私与匿名

比特币的隐私与匿名,一度是比特币发展中的焦点问题。尤其是丝绸之路等非法网站被打击之后，如何增加交易中的匿名性更成了部分开发者的目标，比如隐藏交易者地址与身份的闪电网络，比如隐藏交易者钱币来源与去向的混币技术等等，甚至出现了许多以匿名为直接目标的数字货币，如门罗币与Z-cash等。随着欧盟、美国及世界诸国相继将数字货币纳入金钱处理监管，纳入反洗钱法监管，隐私与匿名的争议将越来越激烈。那么法律上如何看待隐私与匿名？

为了正确理解隐私与匿名，我们首先思考一下隐私与匿名所要保护的对象是什么？对，个人信息，无论是自然人的还是法人的不愿公开的私人信息。进一步，哪些私人信息可纳入隐私或匿名范畴？这个 非常复杂了，不同国家、不同民族，甚至不同人群，都有各自独特的对个人不愿公开信息的理解，比如有人认为电话号码不宜公布，而有人则直接在网上公布自己的电话号码，住所也一样，即使比较隐私的疾病信息，是否归入隐私，不同人也有不同理解，所以何为隐私或匿名需要保护的内容，千人千不同，那么法律上有最低的保护水准或保护内容么？仔细想想，除了不愿公开的主观意愿，客观内容真不易确定。但是，为了分析比特币的隐私与匿名，我们可以采用一种光谱分析法。

对于个人信息的披露，我们可以分成两个极端，位于光谱两端，一个是绝对不公开，即完全匿名，即一切个人信息均不作任何公开；一个极端是绝对公开，即完全透明，即一切个人信息在主观或客观上不做任何保护，任何第三人均可轻易得到或被给予他的包括身份、财产等隐私在内的全部个人信息。凭常识可以判断，对于绝大多数人，不可能做到或愿意完全匿名或完全透明，而是处在两个极端光谱之间，有些人、在有些场景可能愿意披露的个人信息多一些，更靠近完全透明一侧；有些人、在有些场景可能不愿披露的个人信息更多一些，更靠近完全匿名一侧。

总有一些人或者政府希望获得或窥伺他人更多的个人信息，也总有人尽量保护自己的个人信息不被他人侦测或获取。故整个人类社会，隐私的获取与保护是处在一个动态平衡之中的，平衡点就在上述两个极端光谱之间移动。当平衡点大致稳定而不经常移动时，我们可以说这个社会的秩序是稳定的，如果平衡点经常在移动，可以说这个社会是处于剧烈动荡之中，比如战争状态、动乱状态或紧急状态，此时个人信息常被不自愿披露。

所以，比特币作为一种前所未有的发明，作为一种以全球通用货币为目标的发明，作为与未来整个人类、每个人、每个政府可能息息相关的发明，其必须在隐私保护方面找到一个最佳平衡点，以使社会秩序大致稳定，而不发生重大偏移。

完全匿名的比特币显然不可取，以完全匿名为目标的数字货币显然也不可取。这里的完全匿名与上面提到的光谱一侧的完全匿名在货币场景下是同一个含义，意即这种货币的转移和存储完全对其他所有人、所有机构屏蔽身份信息，也就是这个人完全在黑暗中交易，甚至连交易对手也不知情。就人类生活与法律经验，完全匿名的数字货币处在处在光谱的极端一侧，不可能为绝大多数人选择，不可能成为通用货币，至少法律就第一个不允许。比如已经生效的美国金融犯罪执法网络的条例以及欧盟反洗钱指令均要求数字货币的传递与托管机构必须符合反洗钱法，意味着它们必须执行KYC和大金额的报告制度.仅凭法律这一条,完全匿名的数字货币已难以生存,更遑论人类几千年来基于诚实的生活经验。

但同样，比特币也不能处在完全透明的光谱一侧，否则无人敢进行比特币交易，因为一旦交易，个人身份便被锁定，毫无隐私可言。所以，比特币必须在完全透明与完全匿名之间找到一种保护隐私的方法，以满足不同地区、不同人群的隐私保护需求。比特币的发明人非常天才，他找到了人类货币的可追踪性这一本质特征，将光谱的平衡点建立在比特币的可追踪性这一特征之上。

比特币的可追踪性包括两个重要特征，缺一不可。一、任何比特币交易包括与之相关的发票、合同等，均记录于链上，实现货币和交易的可追踪性。二、任何比特币交易包括与之相关的发票、合同等信息数据均以特定算法以私钥加密，除非特定人，其他任何人均无法访问，从而实现隐私性。更进一步，为了防止大数据追踪，采用一次交易一次地址的算法，隐私得到更强保护；又为了适应不同主权国家、不同地区的要求，采用区块的双哈希算法，据此可以过滤特定交易，实现了隐私与现实法律的平衡。

故，比特币在最底层的协议层面，实现了隐私与匿名之间的最基础平衡，可以确保社会秩序不致大幅波动。但正如前文所说，隐私在本质上是个人保护意愿及能力与他人或政府窥伺意愿及能力之间的一种动态平衡，当比特币在技术层面实现了最基础的平衡之后，至于现实中的真实平衡点。则有赖于在应用层面各方之间的博弈平衡，比如仅KYC一条，不同国家、不同地区甚至不同交易机构就可能有不同规定，有的可能只要身份证认证，有的则需要视频认证，有的则可能需要生物学认证等等，这些属于不同人群、不同国家在比特币最基础平衡基础上形成的各个现实法律下的新平衡。