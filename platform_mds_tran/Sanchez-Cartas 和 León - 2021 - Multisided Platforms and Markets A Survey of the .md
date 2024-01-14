# Multisided Platforms And Markets: A Survey Of The Theoretical Literature



Juan Manuel Sanchez-Cartas*
and Gonzalo León Campus de Montegancedo Universidad Politécnica de Madrid Abstract.

Juan Manuel Sanchez-Cartas*和Gonzalo León Campus de Montegancedo马德里理工大学摘要。

Platforms are everywhere. The rise of Uber, Netflix, and Facebook has attracted a lot of attention to this business model. However, despite its relevance and presence in the digital economy, the definition of platforms, their main characteristics, the intuitions about how they set prices, solve coordination issues, or choose their ownership structure seem to be scattered in many papers. This review attempts to organize the last two decades of research on multisided platforms around three essential elements of platforms: price structure, network effects, and control rights. We highlight which definitions are used in the literature, how they are related to the defining characteristics of platforms, and what research has been made on those characteristics. We pay special attention to the research done on pricing, coordination problems, and ownership structure. We conclude by reviewing the theoretical evidence around monopolization and competition policy in multisided markets.

平台无处不在。Uber、Netflix和Facebook的崛起引起了对这种商业模式的广泛关注。然而，尽管在数字经济中具有重要性和存在感，但关于平台的定义、其主要特征、定价方式、解决协调问题或选择所有权结构的直觉似乎散落在许多论文中。本综述旨在整理过去二十年来关于多边平台的研究成果，围绕平台的三个基本要素：价格结构、网络效应和控制权。我们强调了文献中使用的定义，以及它们与平台定义特征之间的关系，并对这些特征进行了详细研究。我们特别关注定价、协调问题和所有权结构方面的研究成果。最后，我们回顾了多边市场中垄断化和竞争政策方面的理论证据。

（*为译者注：Juan Manuel Sanchez-Cartas为主要作者）

Keywords. Industrial organization; Multisided platforms; Network externalities; Two-sided markets

关键词：产业组织；多边平台；网络外部性；双边市场

## 1. Introduction



We live surrounded by platforms. Facebook, Netflix, Uber, and Airbnb are only a few examples of these platforms nowadays. They are everywhere, and they are disrupting businesses, behaviors and even governments. They put in touch people, users and developers, viewers and advertisers, creators of content, and consumers, sellers, and buyers. However, platforms are not a new phenomenon.

我们身处于平台的环绕之中。如今，Facebook、Netflix、Uber和Airbnb等平台只是其中的几个例子。它们无处不在，正在颠覆企业、行为甚至政府。它们将人与人联系起来，连接了用户和开发者、观众和广告商、内容创作者和消费者、卖家和买家。然而，平台并非新现象。

They are based on the idea of putting in touch two or more groups of people who need each other.

它们的基本理念是将互相需要的两个或多个群体联系在一起。

Newspapers, academic journals, and even fairs work in this way. They "connect" readers and advertisers, researchers and readers, and buyers and sellers. However, information and communication technologies (ICTs) have allowed us to scale up this idea. Traditional newspapers or fairs have two shortcomings that digital platforms avoid: To benefit from a fair, you have to be there. To read a paper, you need a copy. In both cases, it is costly to print a newspaper or to set a stand at a fair. However, digital platforms allow us to overcome these two issues: You do not need to be physically in some place, and copies can be made for free. These two features have allowed platforms to reach global relevance and to increase the interest in them. The larger the number of users, the more relevant they become.

报纸、学术期刊甚至展会都以此方式运作。它们将读者与广告商、研究人员与读者、买家与卖家“连接”起来。然而，信息与通信技术（ICT）使我们能够扩大这一理念的规模。传统报纸或展会存在两个缺点，而数字平台则避免了这些问题：参加展会需要亲自到场，阅读一份报纸需要一份副本。在这两种情况下，印刷报纸或设立展位都是成本高昂的。然而，数字平台使我们能够克服这两个问题：你不需要亲自到某个地方，副本可以免费制作。这两个特点使得平台具有全球影响力，并增加了人们对其的兴趣。用户数量越多，其重要性就越突出。

Although in the last decade, there have been scattered contributions that had reviewed different aspects of multisided platforms, such as competition policy—see Filistrucchi *et al*. (2013) or Jullien and Sand-Zantman (2019)—or specific markets, such as media markets, see Foros *et al*. (2015). There has been no contribution in the industrial organization literature focused on analyzing and clarifying the different concepts of platforms, their defining characteristics, and the research on those distinguishing characteristics despite it could be argued that this literature was precisely born because of the need to define what is distinctive about platform markets compared to traditional ones. In this work, we first introduce the concept of multisided platforms, and how this concept has evolved in the literature. Then, we address the literature around each defining feature of multisided platforms: price structure, network effects and coordination, and control rights. Then, we conclude by addressing the possibility of tipping, and competition policy.

尽管过去十年中已有一些零散的研究对多边平台的不同方面进行了回顾，例如竞争政策（参见Filistrucchi等人，2013年或Jullien和Sand-Zantman，2019年）以及特定市场，如媒体市场（参见Foros等人，2015年），但在产业组织文献中尚未有关于分析和澄清平台不同概念、其定义特征以及与之相关研究的贡献。然而，可以认为这些文献的出现正是因为需要界定平台市场与传统市场之间的区别。本文首先介绍了多边平台的概念及其在文献中的演变。随后，我们探讨了围绕多边平台每个定义特征展开的文献：价格结构、网络效应和协调以及控制权。最后，我们讨论了可能出现倾斜和竞争政策的可能性。

## 2. Definitions And Concepts



What is a multisided platform?1 Unfortunately, neither there is an "industry of platforms" in official statistics that we can use as a reference, nor multisided platforms/markets have a clear and widely accepted definition, as it is pointed out by Filistrucchi *et al*. (2010), Evans (2011), or OECD (2009).

多边平台是什么？遗憾的是，官方统计数据中没有所谓的“平台行业”可供参考，而且关于多边平台/市场也没有一个清晰且被广泛接受的定义，正如Filistrucchi等人（2010年）、Evans（2011年）或OECD（2009年）所指出的。

In fact, *you know a [multi-sided] market when you see it*, Rochet and Tirole (2006).2
This identification problem arises because the concept of multisided markets is a refinement of combining other three concepts: *multiproduct firms, network effects, and property rights*. From the multiproduct pricing literature, it borrows the focus on price structure and the idea that price structures are less likely to be distorted by market power than price levels. From the network effects literature, it borrows the idea that there are noninternalized externalities among end-users. And from the property rights literature, it borrows the idea that there is a relationship between prices and rights over essential terms of the interaction.

实际上，当你看到一个多边市场时，你就能够辨认出它的特征（Rochet和Tirole，2006）。这个识别问题的出现是因为多边市场的概念是对其他三个概念的细化：多产品企业、网络效应和产权。它从多产品定价文献中借鉴了对价格结构的关注，并认为价格结构不太可能受到市场力量扭曲，而不是价格水平。从网络效应文献中，它借鉴了最终用户之间存在非内部化外部性的观点。而从产权文献中，则借鉴了价格与互动关键条款的权利之间存在着一种关系的观点。

A heterosexual, singles-oriented club is an illustrative example of a two-sided platform. There are two groups of customers—men and women. Members of each group value the presence of the other group, and normally, they pay different prices to access the club (or they have different access conditions). For example, let us imagine that men pay $10 and women $5. The club (platform) provides a place for them to get together and interact freely. By doing so, it enables members of these two groups to capture the benefits of having access to each other. In terms of the previous characteristics, a man/woman does not internalize the impact of his/her presence in the club on other women's/men's welfare. Therefore, there is a *noninternalized indirect network effect* among men and women that the club (platform) internalizes, but not necessarily perfectly.3 Additionally, if the total price was equally shared ($7.5), probably, the number of women and men in the club would be different. In other words, *price structure* matters. Lastly, both men and women freely choose their partners. The club does not force them to choose specific partners, so *men/women control with whom interact*. Therefore, we can identify three defining features of multisided markets: the presence of noninternalized externalities among men and women, the focus on price structure, and the control over the interaction terms by men and women.

异性单身俱乐部是双边平台的一个典型例子。这个俱乐部有两组顾客，即男性和女性。每组成员都看重另一组的存在，并且通常会支付不同的价格来进入俱乐部（或者有不同的进入条件）。例如，假设男性支付10美元，女性支付5美元。该俱乐部（平台）为他们提供了一个自由相互交流和互动的场所。通过这种方式，它使得这两个群体的成员能够享受到彼此之间互相接触所带来的好处。从前面所述特征来看，男性/女性并没有内化自己在俱乐部中对其他女性/男性福利产生影响的情况。因此，在男性和女性之间存在着一种非内化间接网络效应，而该俱乐部（平台）则将其内化了起来，但并不一定完全如此。此外，如果总价格是均分的（7.5美元），可能会导致俱乐部中男女人数不同。换句话说，“价格结构”很重要。最后，无论是男人还是女人都可以自由选择自己的伴侣。该俱乐部不会强迫他们选择特定伴侣，因此“男性/女性控制与谁互动”。因此，我们可以确定多边市场具有三个定义特征：男性和女性之间存在非内化的外部效应、关注价格结构以及男性和女性对互动条款的控制。

Despite these features were early explicitly (or implicitly) highlighted by Evans (2003a) and Rochet and Tirole (2003), the trend in the literature has been to define multisided markets using an examplebased approach, which has led to the current situation, in which there is not a clear and widely accepted definition. Furthermore, it has also led to ambiguous definitions that partially focus on some of these features.

尽管Evans（2003a）和Rochet和Tirole（2003）早期明确（或隐含地）强调了这些特征，但学术界目前的趋势是采用基于示例的方法来定义多边市场，这导致了当前没有一个清晰且被广泛接受的定义。此外，这也导致了一些模糊的定义，其中部分关注了这些特征。

For instance, when defining multisided markets, some authors have proposed definitions that focus only on the existence of indirect network effects because, in most of the motivating examples, it is by far the more explicit characteristic. Anderson and Coate (2005) uses as motivating example the media industry and define a two-sided market as one where the participants on each side care directly about the number of participants on the other side. Although finding examples in which that condition is true is easy, not all the cases with indirect network effects are multisided markets. Following the club example, a heterosexual but couples-oriented dancing club provides a place for men and women to dance together, but the previous price structure would be neutral as long as couples would be able to bargain the total price.

举例来说，在定义多边市场时，一些作者提出了只关注间接网络效应存在的定义，因为在大多数激励性示例中，这是更为明确的特征。安德森和科特（2005）以媒体行业作为激励性示例，并将双边市场定义为每一方参与者直接关心另一方参与者数量的市场。虽然很容易找到符合该条件的示例，但并非所有具有间接网络效应的情况都属于多边市场。以俱乐部为例，一个面向异性但以夫妻为导向的舞蹈俱乐部提供了男女共同跳舞的场所，但只要夫妻能够协商总价格，之前的价格结构就是中立的。

Other definitions considered the platform as a "trading device" or a "transaction technology" that facilitates the interaction among sides that otherwise would not occur. For example, an early definition was that a platform is a technology that minimizes transaction costs, or a technology that creates a value allowing transactions that otherwise would not occur, see Evans and Schmalensee (2005). Implicitly, these definitions take into account the necessity of having several sides on board that need each other in some way, and therefore, the existence of noninternalized network externalities. However, without explicit or implicit mention to the nonneutrality of the price structure, these definitions may encompass markets in which buyers and sellers can bargain the total price. Therefore, this definition is very broad and, virtually, every market could be studied as a particular case of multisided markets.4
However, the most common pattern in definitions has been to consider the existence of noninternalized externalities and the relevance of the price structure. The latter has been considered in most of the cases implicitly by referring to the platform as a "multi-product firm that serves several sides," see, for example, Ivaldi *et al*. (2011), Affeldt *et al*. (2013), Armstrong and Wright (2007), Filistrucchi *et al*. (2012), Kaiser and Wright (2006), Schiff (2003), Evans (2003b, 2011), or Weisman and Kulick (2010). In this case, these definitions lack the more subtle part of the features: the necessity of control over essential terms of the interaction. For example, a consultancy firm would be a two-sided platform if it intermediates between clients and freelance consultants by allowing them to interact freely, but a consultancy firm is one-sided if it assigns consultants to projects. In other words, it controls that interaction.

其他定义将平台视为“交易设备”或“交易技术”，促进了双方之间本来不会发生的互动。早期的定义认为平台是一种最小化交易成本的技术，或者是一种创造价值、允许本来不会发生的交易的技术。这些定义隐含地考虑到需要有几个方面需要彼此以某种方式合作，并且因此存在非内部化网络外部性。然而，如果没有明确或隐含地提及价格结构的非中立性，这些定义可能包括买家和卖家可以协商总价格的市场。因此，这个定义非常广泛，实际上每个市场都可以被研究为多边市场的一个特例。

然而，在定义中最常见的模式是考虑到非内部化外部性和价格结构的重要性。后者在大多数情况下被隐含地认为是指平台作为“服务于多个方面的多产品公司”。这些定义缺乏更微妙的特征：对互动的基本条款具有控制权的必要性。例如，如果咨询公司在客户和自由职业顾问之间进行中介，并允许他们自由互动，则该咨询公司将是一个双边平台；但如果咨询公司将顾问分配给项目，则它是一个单边平台。换句话说，它控制着这种互动。

It is common that, at first sight, some definitions seem to lack some relevant features, but those features are later highlighted somewhere in the paper. For example, Hagiu (2004) states that a market is said to be a two-sided if firms serve two distinct groups of customers who depend on each other, and whose joint participation makes platforms more valuable to each, or Jullien (2005), who states that platforms provide services that are used by two types of trading partners to interact and operate an exchange. In both cases, they add an explicit reference to price structure or network effects later in the paper. Nonetheless, this lack of precision in defining platforms may lead to misclassifications, which may lead to wrong policies5.

通常情况下，一些定义乍一看似乎缺少一些相关特征，但这些特征在论文的其他部分得到了强调。例如，Hagiu（2004）指出，如果企业为两个相互依赖、共同参与使平台对每个人更有价值的不同客户群体提供服务，则市场被称为双边市场。而Jullien（2005）则指出，平台提供服务供两种类型的交易伙伴进行互动和交易。在这两种情况下，他们在论文后面明确提到了价格结构或网络效应。然而，这种对平台定义的不精确可能导致错误分类，并可能导致错误的政策制定。

Among those definitions that take into account the three elements, Rochet and Tirole (2006) and Evans
(2003a) propose the most interesting ones. Evans (2003a) summarizes the necessary conditions for the existence of a market with two-sided platforms as follows: a two-sided market requires two or more distinct groups of customers, [it] exhibits externalities which are associated with two or more groups of customers being connected or coordinated in some fashion, [and] an intermediary is required in order to internalise the externalities created by one group for the other group(s). This definition considers the presence of network externalities and the multiproduct dimension of platforms by referring to different groups. However, the notion of end-users controlling the interaction is subtle, and it is only considered by stating that they are "coordinated in some fashion," which is quite general.

在考虑到这三个要素的定义中，Rochet和Tirole（2006）以及Evans（2003a）提出了最有趣的定义。Evans（2003a）总结了存在双边平台市场的必要条件：双边市场需要两个或更多不同的客户群体，它展示了与两个或更多客户群体之间的连接或协调相关联的外部性，并且需要一个中介来内部化一个群体为其他群体创造的外部性。该定义考虑到了网络外部性和平台多产品维度，通过引用不同群体来实现。然而，关于最终用户控制交互的概念是微妙的，只是通过陈述他们以某种方式“协调”来考虑，这是相当笼统的。

Rochet and Tirole (2006) define two-sided platforms as: A market with network externalities is a twosided market if platforms can effectively cross-subsidize between different categories of end-users that are parties to a transaction. Therefore, there are *network externalities*. Platforms can effectively crosssubsidize, which implies a *nonneutral price regime*, and end-users that are parties to a transaction, which takes into account the idea of *end-users freely interacting*.6 However, this last term is ill-defined and has been subject to debate in the literature because the term "transaction" can be broadly interpreted as an interaction, or it can literally be interpreted as a transaction, as some authors have done, see Filistrucchi et al. (2013),7 but more importantly, the allocation of control rights is not properly defined, as in Evans
(2003a), which makes those definitions overinclusive. In fact, Rochet and Tirole (2006) recognize that under their definition almost every company would be two-sided, which is a consequence of this lack of proper definition of the allocation of control rights.8
Building upon those definitions, posterior works provided refined definitions that, in some cases, keep having the same limitations. One of those is OECD (2009), which defines a two-sided market as follows:
A two-sided platform is characterized by three elements: (1) There are two distinct groups of consumers who need each other in some way and who rely on platforms to intermediate transactions. A two-sided platform provides goods or services simultaneously to these two groups. (2) The existence of indirect externalities across groups of consumers; (3) nonneutrality of the price structure. Another work that has proposed a similar definition is Evans and Noel (2008). They define multisided markets as follows:
[platforms that] provide goods and services to several distinct groups of customers who need each other in some way, and who rely on platforms to intermediate transactions between them. […] In particular, they facilitate the realization of indirect network effects. They typically reduce transaction costs and thereby permit value-creating exchanges that otherwise would not occur.9
Despite those advances in defining multisided markets, it seems that the idea of end-users controlling essential terms of the interaction is not well delimited. Hagiu (2007) provides a proper delimitation of control rights by highlighting that the difference between "merchants" and "two-sided platforms" relies on the idea that end-users may have control over essential terms of the transactions, for example, the goods/services traded, or the prices for those goods/services. For example, in a buying/selling platform, it is the seller who sets the price for their goods/services, and in a media platform, it is the advertiser who chooses the ads to display.

Rochet和Tirole（2006）将双边平台定义为：如果平台能够有效地在参与交易的不同终端用户类别之间进行交叉补贴，那么具有网络外部性的市场就是一个双边市场。因此，存在网络外部性。平台可以有效地进行交叉补贴，这意味着一个非中立的价格体制，并且参与交易的终端用户可以自由互动。然而，对于"终端用户自由互动"这一术语并没有明确定义，并且在文献中一直存在争议。因为"交易"一词可以广泛解释为互动，也可以字面解释为交易，正如一些作者所做的那样（参见Filistrucchi等人，2013）。但更重要的是，对于控制权分配的定义不够准确，正如Evans（2003a）所指出的那样，这使得这些定义过于宽泛。事实上，Rochet和Tirole（2006）承认根据他们的定义几乎每个公司都会成为双边市场，这是由于对控制权分配缺乏适当定义所导致的。基于这些定义，在后续研究中提供了更精确的定义，但在某些情况下仍存在相同的局限性。OECD（2009）提出了一个类似的定义，将双边市场定义为具有以下三个特点：（1）存在两个不同的消费者群体，他们在某种程度上互相需要，并依赖于平台来进行交易的中介。双边平台同时向这两个群体提供商品或服务；（2）存在跨群体间接外部性；（3）价格结构的非中立性。Evans和Noel（2008）也提出了类似的定义，将多主体市场定义为向几个不同的客户群体提供商品和服务，这些客户群体在某种程度上互相需要，并依赖于平台来进行交易。它们促进了间接网络效应的实现，并通常降低交易成本，从而允许产生价值的交换。尽管在定义多主体市场方面取得了一些进展，但似乎对终端用户控制交互关键条款的概念并没有很好地界定。Hagiu（2007）通过强调终端用户可能对交易关键条款具有控制权来提供了对控制权进行适当界定，“商家”和“双边平台”之间的区别依赖于终端用户对交易的关键条款具有控制权，例如交易的商品/服务或这些商品/服务的价格。例如，在一个买卖平台上，是卖家设定其商品/服务的价格，在媒体平台上，是广告商选择要展示的广告。

Hagiu and Wright (2015) propose a new definition of multisided platforms based on two characteristics that incorporate this idea that the difference between a merchant and a platform relies on the allocation of property rights:

Hagiu和Wright（2015）提出了一个新的多边平台定义，基于两个特征，这些特征融入了商家和平台之间的区别依赖于产权分配的概念：

- multi-sided businesses enable direct interactions between two or more sides. - each side is affiliated with the platform.
By "direct interaction," they mean that two or more sides retain control over the essential terms of the interaction. For example, on the Uber platform, there are two sides, users and drivers. Drivers retain control rights over the car (it is the drivers' car) as opposed to the one-sided intermediaries (taxi companies) that have total control over their fleet. Therefore, this is the main difference between the onesided and the multisided worlds. By "affiliation," they mean that users on each side consciously make platform-specific investments that are necessary for them to be able to interact with each other directly, for example, paying membership fees or registering. In the Uber example, both users and drivers have to invest time in registering in the app. The affiliation helps to distinguish multisided platforms from input suppliers.

- 多边业务使两个或更多方能够直接互动。
- 每一方与平台有关联。

"直接互动"指的是两个或更多方对互动的关键条款保持控制权。例如，在Uber平台上，存在两个方，即用户和司机。司机保留对车辆的控制权（车辆属于司机），而不像单向中介（如出租车公司）对其车队拥有完全控制权。因此，这是单向和多边世界之间的主要区别。"关联"指的是每一方在能够直接互动时都会有意识地进行平台特定的投资，例如支付会员费或注册。以Uber为例，用户和司机都需要投入时间进行应用程序注册。这种关联有助于将多边平台与输入供应商区分开来。

Therefore, this definition apparently makes use of two out of the three essential characteristics of multisided platforms, but the most remarkable contribution of this definition is that it does not require any reference to indirect or cross-network effects. Hagiu and Wright consider that indirect network effects could be a consequence of "affiliation" or "direct interaction." But independently of whether or not network effects are a consequence or a prerequisite, they agree that they are a characteristic of multisided businesses. However, this definition lacks a clear reference to the nonneutral price structure, and this may be the reason behind the lack of use of this definition. Nonetheless, the reference to the nonneutrality is hidden in the notion of "affiliation." Note that the idea that the affiliation generates multisidedness is not new. Rochet and Tirole (2006) highlight that some factors generate multisidedness, such as membership fees, because they could modify the volume of transactions. In fact, Caillaud and Jullien (2003) show that the price structure is neutral without membership fees. More generally, Evans (2011) argues that any transaction cost that prevents the sides from directly solving these externalities generates multisidedness. Therefore, interpreting "affiliation" as a platform-specific investment that generates transaction costs implicitly links this factor to the nonneutrality of the price structure.

因此，这个定义明显利用了多边平台的三个基本特征中的两个，但这个定义最显著的贡献在于它不需要任何对间接或跨网络效应的参考。Hagiu和Wright认为间接网络效应可能是“关联”或“直接互动”的结果。无论网络效应是结果还是前提条件，他们都同意它们是多边业务的特征。然而，这个定义缺乏对非中性价格结构的明确参考，这可能是没有使用该定义的原因。尽管如此，“关联”的概念中隐藏了对非中性价格结构的引用。需要注意的是，“关联”产生多边性的想法并不新鲜。Rochet和Tirole（2006）强调一些因素会产生多边性，例如会员费，因为它们可以改变交易量。实际上，Caillaud和Jullien（2003）表明，在没有会员费的情况下价格结构是中性的。更一般地说，Evans（2011）认为任何阻止各方直接解决这些外部性问题的交易成本都会产生多边性。因此，将“关联”解释为生成交易成本的平台特定投资隐含地将该因素与价格结构非中性联系起来。

Given the complexity of defining a two-sided market, it is normal to find works that consider different definitions. Some authors have shown that reality is very ambiguous, which leads to a multiplicity of definitions, see Filistrucchi and Klein (2013) or Evans *et al*. (2008). That is why it is usual to find works that use versions of the Evans' and Rochet and Tirole's definitions, see Affeldt (2011), Song (2013), Evans (2011), Affeldt *et al*. (2013), Filistrucchi and Klein (2013), Economides and Katsamakas

鉴于双边市场的定义复杂性，不同的研究对此进行了各种不同的定义。一些作者指出现实情况非常模糊，因此存在多种定义，详见Filistrucchi和Klein（2013）以及Evans等人（2008）。因此，在相关研究中经常会使用Evans、Rochet和Tirole提出的定义版本，参考Affeldt（2011）、Song（2013）、Evans（2011）、Affeldt等人（2013）、Filistrucchi和Klein（2013）以及Economides和Katsamakas。

Mentions to:
Price structure
Network
effects
Property rights
Articles
Implicit
Implicit
No mention
Evans and Schmalensee (2005),
Jullien (2005)
Implicit
Implicit
Explicit
Hagiu and Wright (2015)
Implicit
Explicit
No mention
Ivaldi *et al*. (2011), Affeldt *et al*.
(2013), Affeldt (2011), Armstrong and Wright (2007), Schiff (2003), Evans (2003b), Hagiu (2004), Weyl (2010)
Implicit
Explicit
Ill defined
Evans (2003a), Evans and Noel
(2008), Rysman (2009), Weisman and Kulick (2010), Wright (2004)
Explicit
Explicit
No mention
OECD (2009), Filistrucchi *et al*.
(2012), Kaiser and Wright (2006), Song (2013)
Explicit
Explicit
Ill defined
Filistrucchi *et al*. (2013), Evans
(2011), Rochet and Tirole (2006)

涉及到的内容包括：
价格结构
网络效应
产权
文章
隐含的
隐含的
未提及
Evans和Schmalensee（2005年）
Jullien（2005年）
隐含的
隐含的
明确的
Hagiu和Wright（2015年）
隐含的
明确的
未提及
Ivaldi等人（2011年）、Affeldt等人（2013年）、Affeldt（2011年）、Armstrong和Wright（2007年）、Schiff（2003年）、Evans（2003b）、Hagiu（2004年）、Weyl（2010年）
隐含的 
明确的 
定义不清晰 
Evans（2003a）、Evans和Noel（2008年）、Rysman（2009年）、Weisman和Kulick （2010年）、Wright （  2004  ）
明确的 
明确的 
未提及 
OECD （  2009   )、Filistrucchi等人 (   2012   )、Kaiser and Wright (    2006    )、Song (    2013    )
明确的 
明确的 
定义不清晰  
Filistrucchi等人(     2013     )、Evans(      2011      )、Rochet and Tirole(       2006       )

(2006), Filistrucchi *et al*. (2013), Kaiser and Wright (2006), Weisman and Kulick (2010), Weyl (2010), or Filistrucchi and Klein (2013).10
Lastly, another interesting discussion that has surrounded those definitions is whether or not we should talk about multisided platforms, markets, businesses, or strategies. Rysman (2009) points out that the definition of multisided markets is not correct because it is hard to find "pure multi-sided markets" but, it is easier to find "multi-sided businesses/platforms." He uses as an example Amazon that was a one-sided platform in the market of books and a multisided platform in other markets. He argues that multisidedness is an endogenous decision of firms. The main question is not to know if a market is a multisided one, virtually, all markets might be multisided to some extent. What is relevant is to know how important multisided issues are. Other works such as Cabral (2019) or Filistrucchi *et al*. (2013) have argued similarly. For example, Evans (2011) points out that, in the US newspaper industry, there are examples of different business models with high consumer fees and low level of advertising (The Economist), with a high level of advertising and low consumer fees (Vogue), or free for consumers but with the highest level of advertising (online newspapers), see Evans and Noel (2008), Evans *et al*. (2008), and Evans (2011). Those features are common in social networks too, in which some users pay and have low levels of advertising (LinkedIn premium), or there is advertising but it is free (Facebook). In this vein, it makes much more sense to talk about companies that follow different strategies with different degrees of multisidedness.

最后，围绕这些定义还存在一个有趣的讨论，即我们是否应该讨论多边平台、市场、企业或战略。Rysman（2009）指出，多边市场的定义并不准确，因为很难找到“纯粹的多边市场”，但是找到“多边企业/平台”要容易得多。他以亚马逊为例，亚马逊在图书市场上是单一平台，在其他市场上则是多边平台。他认为多边性是企业内部决策的结果。主要问题不在于一个市场是否是多边的，实际上几乎所有市场都可能在某种程度上是多边的。重要的是了解多边问题有多重要。Cabral（2019）或Filistrucchi等人（2013）也提出了类似观点。例如，Evans（2011）指出，在美国报纸行业中存在着不同商业模式的例子：高消费者费用和低广告水平（《经济学家》），高广告水平和低消费者费用（《时尚杂志》），或对消费者免费但广告水平最高（在线报纸），详见Evans和Noel（2008）、Evans等人（2008）和Evans（2011）。这些特点在社交网络中也很常见，其中一些用户付费并且广告水平较低（领英高级版），或者有广告但是免费（Facebook）。因此，更有意义的是讨论采用不同多边性程度的公司。

In all the previous definitions of platforms, the multisidedness is taken for granted, and the focus is on the company that behaves as a platform, but as Rysman (2009) pointed out, what is relevant is to define multisidedness. Following the literature, we can highlight three pillars that determine the boundaries of multisidedness: network effects, property rights, and price structure. In fact, it is possible to summarize all the previous contributions around these three dimensions, as Table 1 shows. Therefore, multisidedness requires the presence of noninternalized externalities among end-users (i.e., indirect network effects), the possibility of cross-subsidizing different categories of end-users (i.e., price structure matters), and prices must reflect that end-users that are parties to a transaction retain control over essential terms of the interaction (i.e., control rights). The failure of any of these conditions makes simpler and better understood other models. For example, if network effects are not found, or the platform is price-taker on one side, or the platform behaves as a reseller, traditional one-sided analysis is better suited.11 Once these three conditions hold simultaneously, the question is to what extent multisidedness is relevant for each market.12In summary, definitions are controversial. There is no consensus. In general, the vast majority of authors and international organisms recognize that there is not a universally accepted definition of multisided markets or platforms yet. There is a consensus on the idea of two or more groups of agents who need each other in some way and who rely on platforms to intermediate transactions between them. There is also consensus on the idea that it is more important to determine the linkages between the sides of the market than the market itself, see OECD (2009), Filistrucchi *et al*. (2013), or Weyl (2010). However, as it is pointed out by Filistrucchi *et al*. (2013), at first sight, it appears to be still some debate on the exact definition of a two-sided market, but the different definitions appear consistent enough to allow the practical identification of two-sided markets. In fact, when we combine the different approaches found in the literature, it seems that a clear concept of multisidedness emerges around price structure, network effects, and control rights.

在以往对平台的定义中，多边性被默认存在，并且重点放在行为为平台的公司上。然而，正如Rysman（2009）所指出的那样，更重要的是定义多边性本身。根据文献，我们可以强调决定多边性范围的三个关键因素：网络效应、产权和价格结构。实际上，我们可以将之前的研究总结为这三个维度，如表1所示。因此，多边性要求终端用户之间存在非内部化的外部性（即间接网络效应），能够跨补贴不同类别的终端用户（即价格结构至关重要），并且价格必须反映参与交易方对交互过程中基本条款保持控制的情况（即控制权）。任何一个条件未能满足都会使其他模型更加简单和易于理解。例如，如果没有发现网络效应，或者平台在一侧是价格接受者，或者平台行为类似于转售商，则传统的单边分析更加适用。当这三个条件同时成立时，问题就是多边性对每个市场有多大影响。

总之，在定义方面存在争议，并没有达成共识。一般来说，大多数作者和国际组织承认多边市场或平台的定义尚未被普遍接受。人们普遍认同的观点是，多边市场涉及两个或更多群体彼此以某种方式互相需要，并依赖平台来进行交易中介。人们也一致认为，更重要的是确定市场各方之间的联系，而不仅仅是市场本身，参见OECD（2009）、Filistrucchi等人（2013）或Weyl（2010）。然而，正如Filistrucchi等人（2013）所指出的，对于双边市场的确切定义似乎仍存在一些争议，但不同的定义似乎足够一致，以便实际上识别出双边市场。事实上，在结合文献中找到的不同方法时，似乎出现了一个关于价格结构、网络效应和控制权的明确概念。

## 2.1 Typologies Of Multisided Models



With the expansion of the multisided literature, some authors realized that neither all the multisided platforms were equal nor all definitions were suitable for all platform. For instance, Filistrucchi *et al*. (2013) point out that Evans' definitions were more suitable to describe media platforms and, on the contrary, Rochet and Tirole's definition was better suited for payment platforms.

随着多边市场文献的不断扩展，一些作者认识到并非所有多边平台都是相同的，也并非所有定义都适用于所有平台。例如，Filistrucchi等人（2013）指出，Evans的定义更适用于描述媒体平台，而Rochet和Tirole的定义则更适合支付平台。

Since the birth of the literature, different authors have tried to classify multisided platforms following different criteria ranging from price policies to sectors or property structures. Those classifications fulfill different purposes, and an exhaustive analysis of them is out of the scope of this work. As it is pointed out by Filistrucchi (2008), antitrust authorities, managers, researchers, and so forth have to have in mind that different typologies of markets should be treated differently.13
The first taxonomy we are aware of is Evans (2003b). He considers three categories:

自从文学诞生以来，不同的作者尝试根据不同的标准对多边平台进行分类，这些标准涵盖了价格政策、行业或产权结构等方面。这些分类的目的各不相同，本文无法对它们进行详尽分析。正如Filistrucchi（2008）所指出的，反垄断机构、管理者、研究人员等必须意识到不同类型的市场应该有不同的处理方式。Evans（2003b）提出了我们所知道的第一个分类体系，包括三个类别。

[输出结果仅为重写后的中文内容]

(1) Market makers. They enable members of distinct groups to transact with each other. Each member
of a group values more the service if there are more members of the other group. The distinguishing feature is the possibility of monitoring transactions.
(2) Audience makers. They are those markets where platforms match advertisers to audiences. (3) Demand coordinators. These platforms do not strictly sell "transactions" like a market maker,
or "messages" like an audience maker. They are a residual category but economically the most interesting for Evans.
However, this classification presents several flaws. On the one hand, the most interesting category is the residual one. On the other hand, the definition of the categories is either quite restrictive or quite lax. In the case of market makers, platforms should be able to monitor transactions, which is a lax requisite. But in the case of audience maker, platforms must be in the business of advertising, if not, they are in the residual category. These flaws make impractical this taxonomy nowadays, but it was a useful one at the beginning of the literature.

（1）市场制造者。它们使不同群体的成员能够相互交易。如果另一个群体的成员更多，每个群体的成员对该服务的价值就更高。其特点是可以监控交易。

（2）观众制造者。这些市场是平台将广告主与观众匹配起来的地方。

（3）需求协调者。这些平台不严格销售像市场制造者那样的“交易”，也不像观众制造者那样销售“信息”。它们属于剩余类别，但从经济学角度来看最有趣。

然而，这种分类存在几个缺陷。一方面，最有趣的类别是剩余类别。另一方面，各个类别的定义要么非常严格，要么非常宽松。在市场制造者的情况下，平台应该能够监控交易，这是一个宽松的要求。但在观众制造者的情况下，平台必须从事广告业务，否则它们就属于剩余类别。这些缺陷使得这种分类在现今变得不实用了, 但在文献初期却很有用处。

Later, Evans observed four types of two-sided platforms: exchanges, advertiser-support media, transaction devices, and software platforms, see Evans and Schmalensee (2005). However, as the literature grew, and the digital sector became more relevant, other sectoral taxonomies appeared. For instance, Evans (2011) recognizes three different digital platforms: web-based, payment platforms, and software platforms. Although these classifications have a value from the sectoral point of view, from a theoretical one, it is not clear the advantage of differentiating between exchange and transaction device platforms instead of thinking in "market-makers" (as it was initially proposed). Additionally, from a theoretical point of view, it makes little sense to consider as software platforms all the digital platforms independently of their characteristics.

随后，Evans观察到了四种双边平台的类型：交易所、广告支持媒体、交易设备和软件平台（Evans和Schmalensee，2005）。然而，随着文献的增加和数字领域的日益重要，出现了其他行业分类。例如，Evans（2011）将数字平台分为三类：基于网络的平台、支付平台和软件平台。尽管从行业角度来看这些分类具有一定价值，但从理论角度来看，与其区分交易所和交易设备平台，不如考虑它们作为"市场制造者"（最初提出的概念）。此外，在理论上将所有数字平台都视为软件平台而不考虑其特征是缺乏意义的。

On the other hand, Filistrucchi (2008) proposes a theoretical taxonomy that is quite relevant nowadays from theoretical and empirical perspectives:

另一方面，Filistrucchi（2008）提出了一个在理论和实证角度上非常相关的理论分类：

(1) Two-sided nontransaction markets, or media type. In these markets, the transaction is not present,
or it is unobservable. These markets only set membership fees. For example, newspapers. Readers read newspapers with ads, but the newspaper does not know if the ads are generating transactions for the advertiser.
(2) Two-sided transaction markets, or payment card type. These markets are characterized by the
observability of transactions between the sides, like payments with credit/debit cards. The platform can monitor the transaction, and it can set both transaction and adoption fees.
In comparison with Evans's (2003a), this classification is more useful for research purposes. It is simple and straightforward. However, the only flaw is that the two-sided transaction markets category may attract all the digital platforms because these markets are characterized by the observability of a transaction between the sides. In almost all digital platforms, that is true. However, many of them prefer to use membership fees instead. In this sense, it would be better to classify them in terms of the actual pricing instead of the potential pricing. However, that may lead us to derive wrong conclusions, because we would be assuming that they do not set other prices because they cannot.

(1) 双边非交易市场，也称为媒体类型。在这些市场中，交易不存在或不可观察，只收取会员费用。例如，报纸是典型的例子。读者通过阅读带有广告的报纸来获取信息，但报纸无法确定广告是否为广告商带来了实际交易。

(2) 双边交易市场，也称为支付卡类型。这些市场的特点是双方之间的交易可以被观察到，比如使用信用卡或借记卡进行支付。平台可以监控交易，并且可以设置交易费和采用费。

与Evans（2011）相比，这种分类更适合于研究目的。它简单明了。然而唯一的缺点是双边交易市场类别可能包含所有数字平台，因为这些市场的特点是双方之间的交易可观察到。几乎所有数字平台都属于这个类别。然而，许多平台更倾向于使用会员费而不是其他定价策略。从这个意义上说，更好地根据实际定价而不是潜在定价对其进行分类。然而，这样可能导致我们得出错误结论，因为我们会假设它们没有设置其他价格是因为它们无法设置其他价格。

As a summary, in comparison with other lines of research, the classification of two-sided platforms has not been so well studied as other features of these markets. This is also because of the lack of a standard definition of multisided platforms. As a consequence, in all the works we have highlighted, those classifications were developed by the authors' necessity to achieve a specific objective (describe some styled facts, develop an antitrust analysis, etc). However, the relevance of such classifications depends on how useful they are for practitioners or researchers. In Section 6.2, we focus on the practical use of those classifications by highlighting the current debate about the use of multisided platform models in antitrust analysis, and the use of the Filistrucchi's classification as discriminating taxonomy among the different techniques.

综上所述，与其他研究领域相比，对于双边平台的分类研究并不像对这些市场的其他特征那样深入。这主要是因为缺乏对多边平台的标准定义。因此，在我们所强调的所有作品中，这些分类都是作者为了实现特定目标（如描述某些事实、开展反垄断分析等）而制定的。然而，这些分类的重要性取决于它们对从业者或研究人员的实际用途。在第6.2节中，我们将重点关注这些分类的实际应用，并强调当前关于在反垄断分析中使用多边平台模型以及使用Filistrucchi的分类作为区分不同技术之间差异性税务学说的讨论。

## 2.2 Special Features Of Multisided Platforms



Multisided platforms defy many of our preconceived intuitions about firms' behavior. This is a consequence of the interrelationship among the three defining concepts highlighted previously. For instance, Wright (2004) explores eight common statements in the industrial organization literature that do not apply to multisided platforms. Those eight statements (or fallacies as he calls them) are:

多边平台的独特特征

多边平台挑战了我们对企业行为的许多先入之见，这是前文所强调的三个定义概念之间相互关系的结果。例如，Wright（2004）在工业组织文献中探讨了八个常见观点，这些观点在多边平台上并不适用。他将这八个观点称为谬论。

(1) An efficient price structure should be set to reflect relative costs (user-pays). (2) A high price–cost margin indicates market power. (3) A price below marginal cost indicates predation. (4) An increase in competition necessarily results in a more efficient structure of prices. (5) An increase in competition necessarily results in a more balanced price structure. (6) In mature markets, price structures that do not reflect costs are no longer justified. (7) Where one side of a two-sided market receives services below marginal cost, it must be receiving
a cross-subsidy from users on the other side.
(8) Regulating prices set by a platform in a two-sided market is competitively neutral.
Despite that all of them refer to price structure, the interrelationship between independent sides is the reason why some traditional insights do not apply. Additionally, recent evidence has shown that there may be more of those "fallacies," for example, taxes on one side may not disincentivize participation on that side, or compatibility between platforms may reduce competition. Thus, many of our traditional insights may be wrong in multisided markets. In fact, Evans and Schmalensee (2013) argue that one-sided tools often do not apply, at least not without substantial changes, to multisided platforms.

（1）应当建立一个有效的价格结构，以反映相对成本（用户付费）。
（2）高价格-成本差额表明市场力量。
（3）低于边际成本的价格表明掠夺行为。
（4）竞争的增加必然导致更为高效的价格结构。
（5）竞争的增加必然导致更为平衡的价格结构。
（6）在成熟市场中，不反映成本的价格结构不再合理。
（7）在双边市场中，如果一方获得低于边际成本的服务，则必定是从另一方用户那里获得交叉补贴。
（8）对于两边市场中平台设定的价格进行监管是具有竞争中性的。

尽管所有这些观点都涉及到价格结构，但独立双方之间的相互关系是一些传统观点不适用的原因。此外，最近有证据显示可能存在更多这样的“谬论”，例如，在某一方面征税可能并不能减少该方面参与度，或者平台之间兼容性可能会减少竞争。因此，在多边市场中我们许多传统观点可能是错误的。事实上，Evans和Schmalensee (2013)认为单向工具通常不适用，至少在没有实质性变化的情况下不适用于多边平台。

The difference in pricing between multisided and one-sided markets is the most notable characteristic.

多边市场和单边市场之间的定价差异是最显著的特征。

Multisided platforms tend to set an asymmetric price structure in which there are profitable and loss sides. But the differences in pricing behavior are not limited to the asymmetric balance. The prices can be disconnected from marginal costs, as it is pointed out by Evans (2003b).14 Because of the interrelationship between the sides, a platform may respond to an increase in costs on one side with an increase in prices on the other side. Jullien (2005) argues that it is common in multisided markets that the welfare-maximizing prices will not coincide with marginal costs, and Rysman (2009) points out that:
theoretically, it is often hard to establish whether a given price in a two-sided market is higher or lower than socially optimal, or even whether greater competition would make the existing price rise or fall. All these contraintuitive results have led to a vast literature focused on pricing. During the last decade, many of the long-grounded intuitions about prices and market structure have been revised, and this trend continues as new evidence appears.

多边平台往往会采用不对称的价格结构，其中存在盈利和亏损的一方。然而，定价行为的差异并不仅限于不对称平衡。正如Evans（2003b）所指出的，价格可能与边际成本脱节。由于各方之间的相互关系，平台可能会对一方成本上升作出反应，并在另一方面提高价格。Jullien（2005）认为，在多边市场中，最大化福利的价格通常与边际成本不一致，而Rysman（2009）指出：
从理论上来说，很难确定两边市场中给定价格是高于还是低于社会最优价格，甚至更大竞争是否会使现有价格上升或下降。所有这些违背直觉的结果导致了大量关注定价问题的文献。在过去十年中，许多关于价格和市场结构长期以来根深蒂固的直觉已经被修正，并且随着新证据出现这一趋势仍在继续。

On the other hand, grounded on the second pillar of the defining factors of multisidedness, the literature has also focused on the coordination problems that arise as a consequence of the indirect network effects. In network economics and multisided platforms, companies have to solve a coordination problem, in which the role of expectations is essential. In contrast with the canonical network effect model, in which if users believe no one will adopt the platform, the equilibrium is zero adoption (Belleflamme and Peitz, 2015, chapter 20). In multisided platforms, even if one side believes no one is going to enter the platform (pessimistic beliefs), it can get a positive market share if the platform subsidizes one group to attract the other group—divide-and-conquer (DC) strategy—see Caillaud and Jullien (2003) or Jullien (2005).15
Both pricing and coordination problems account for most of the early contributions, but in contrast with the pricing, the expansion of this branch has been smaller.

另一方面，基于多边性定义因素的第二支柱，文献也关注由间接网络效应引起的协调问题。在网络经济学和多边平台中，公司必须解决协调问题，其中期望的作用至关重要。与典型的网络效应模型相反，在该模型中，如果用户认为没有人会采用该平台，则均衡为零采用（Belleflamme和Peitz, 2015, 第20章）。在多边平台中，即使一方持有悲观信念认为没有人会进入该平台，通过对一组进行补贴以吸引另一组 - 分而治之（DC）策略 - 可以获得积极的市场份额，请参见Caillaud和Jullien（2003）或Jullien（2005）。定价和协调问题都是早期研究的重点内容，但与定价相比，这个领域的扩展规模较小。

Despite the differences with one-sided companies, some intuitions prevail between multisided and one-sided companies. For instance, Reisinger (2004) is among the first ones in proving that the greater the differentiation, the greater the profits for at least one platform. Hagiu (2004) or Evans (2002) also find that differentiation guarantees the existence of several platforms in the same market. Rysman (2009) summarizes this feature as follows: If [platforms] can differentiate from each other, they may be able to successfully coexist.16 Also, another common point is that multisided platforms have an excessive incentive to serve the marginal user, which also leads to an imperfect internalization of externalities, see Kind *et al*. (2008) and Weyl (2010).

尽管多边平台公司与单边公司存在差异，但它们之间仍存在一些共同的特征。例如，Reisinger（2004）是最早证明了差异化程度与至少一个平台的利润成正比关系的研究之一。Hagiu（2004）和Evans（2002）也发现差异化确保了同一市场上存在多个平台。Rysman（2009）总结道：如果[平台]能够相互区分开来，它们就有可能成功共存。此外，另一个共同点是多边平台对于服务于边际用户有过度激励，这也导致了对外部性的不完全内部化，详见Kind *et al*.（2008）和Weyl（2010）。

## 3. Pricing In Multisided Markets



Pricing is the most studied topic in the multisided literature by far because the "unusual pricing scheme" of multisided platforms was the focus of many early works, such as Rochet and Tirole (2003), Caillaud and Jullien (2003), or Armstrong (2006). In fact, the eight Wright's (2004) fallacies refer to the price structure in some way.

在多边平台的文献中，定价是最为广泛研究的主题，因为多边平台的“非常规定价方案”成为早期研究的重点，如Rochet和Tirole（2003），Caillaud和Jullien（2003），以及Armstrong（2006）。实际上，Wright（2004）提出的八个谬论在某种程度上都涉及到价格结构。

In the case of two sides, this pricing scheme is characterized by an asymmetric structure in which one side "pays" while the other side is subsidized, for example, free newspapers for readers. Rochet and Tirole highlight that this behavior is the consequence of "the Seesaw principle," and they define it as follows. A factor that is conducive to a high price on one side, to the extent that it raises the platform's margin on that side, also tends to call for a low price on the other side as attracting members on that other side becomes more profitable.17
However, this price scheme does not imply that pricing in multisided markets is disconnected from traditional insights. In the seminal work of Armstrong (2006), a two-sided platform differentiated á la Hotelling sets prices as in the classical Hotelling model but adjusted by the externalities. Armstrong also provides evidence of the Seesaw principle, and he argues that a platform will compete for one group more aggressively than for the other, either if that group is on the more competitive side of the market, or if it causes a larger benefit to the other group. Following the nightclub example, it is usual to find nightclubs where women have free access, but men have to pay. In Armstrong (2006)'s model, this price scheme is explained because men value more the presence of women than the other way around. The externality created by women is larger. However, the key insight of Armstrong is to show that indirect network effects increase the elasticity of demand on both sides. Thus, any price cut induces a larger increase in sales on both sides.

在双边市场中，这种定价方案具有不对称的结构，其中一方“支付”，而另一方则得到补贴，例如向读者提供免费报纸。Rochet和Tirole强调这种行为是“跷跷板原理”的结果，并将其定义如下：在某一方面有利于高价格的因素，通过提高该方面平台的利润，也倾向于要求另一方面降低价格，因为吸引该另一方面的成员变得更加有利可图。

然而，这种定价方案并不意味着多边市场中的定价与传统见解脱节。在Armstrong（2006）的开创性工作中，一个以Hotelling方式区分自己的两边平台设置价格，就像经典Hotelling模型中那样，但通过外部性进行调整。Armstrong还提供了“跷跷板原理”的证据，并认为平台将对其中一个群体进行比其他群体更激烈地竞争，无论是如果该群体处于市场上竞争力更强的一侧还是如果它给其他群体带来更大好处。以夜总会为例，在Armstrong（2006）的模型中解释了这种定价方式：男性比女性更重视女性存在。女性所创造的外部性更大。然而，Armstrong的关键观点是显示间接网络效应增加了两个方面的需求弹性。因此，任何价格下调都会导致两个方面销售量的更大增长。

After those seminal works, pricing on multisided platforms has become a hot topic in the literature. In this sense, we can recognize two different approaches. On the one hand, those works that have focused on factors that influence the price structure of platforms, and on the other hand, those works that have studied the different pricing policies that platforms can implement. For example, membership or pay-byuse (transaction) fees. The former refers to the price that a user pays for entering the market, for example, the price paid by readers to access a digital newspaper. The latter refers to the price paid each time that a transaction occurs. For example, the commission paid by a vendor when a buyer paid by credit card. They are not exclusive, and they can be found together in some markets. For example, a digital streaming platform that has a monthly subscription but, to access specific content, you have to pay an additional fee.

在这些开创性的研究之后，多边平台定价成为文献中备受关注的话题。在这方面，我们可以看到两种不同的方法。一方面，有些研究关注影响平台价格结构的因素；另一方面，有些研究则探讨了平台可以实施的不同定价策略，例如会员费或按使用次数收费（交易费）。前者指用户进入市场时支付的价格，例如读者为访问数字报纸而支付的价格；后者指每次交易发生时支付的价格，例如买家使用信用卡付款时卖家支付的佣金。这两种定价方式并不互斥，在某些市场中可以同时存在。例如，一个数字流媒体平台每月收取订阅费用，但要访问特定内容，则需要额外付费。

Although the vast majority of works consider only membership fees, transaction fees represent an additional instrument to extract profit, but also an instrument that makes multisided markets more contestable. More importantly, when transaction fees are not feasible, inefficient market configurations can emerge in equilibrium, for example, "dominant-firm equilibria," because transaction fees are an additional instrument for deviation that increases the available set of strategies for platforms, see Caillaud and Jullien (2003) or Hagiu and Wright (2015).

尽管大多数研究仅考虑会员费，但交易费不仅是一种额外的利润提取工具，也是使多边市场更具竞争性的一种手段。更重要的是，在无法实施交易费时，均衡状态下可能出现低效的市场配置，例如“主导企业均衡”，因为交易费是一种增加平台可用策略集合的偏离工具。有关详细信息，请参阅Caillaud和Jullien（2003）或Hagiu和Wright（2015）的研究。

At first sight, it may be surprising that given such relevance, the literature has not focused more on the combined role of membership and transaction fees. However, Rochet and Tirole (2006) prove that what matters is the "per-interaction price," which depends on both fees, and both pricing structures obey the standard Lerner principles with a reinterpretation of the marginal cost as an opportunity cost. Similarly, Ambrus *et al*. (2016) show that it does not matter if platforms charge per-unit prices plus an entrance fee or fixed payment, platforms face the same optimization problem. This result does not imply that we should treat both fees equally. In fact, several authors have pointed out that we should not ignore the difference between membership and transaction fees. Armstrong (2006) argues that the possibility of setting transaction fees is the main determinant of the structure of prices offered to the groups in two-sided markets, and according to Filistrucchi (2008), this feature is crucial for the development of econometric models and tests like the SSNIP (small significant nontransitory increase in price). The key insight is to highlight that, independently of which kind of fee we pay attention to, the Lerner principles hold. Therefore, the interesting question to ask is what factors influence the price structure or elasticities on a given side.

乍一看，令人惊讶的是，尽管会员费和交易费的综合作用如此重要，但文献对此并没有更多的关注。然而，Rochet和Tirole（2006）证明了“每次互动价格”才是关键，它取决于两种费用，并且两种定价结构都遵循标准的Lerner原则，将边际成本重新解释为机会成本。类似地，Ambrus等人（2016）表明，平台收取每单位价格加入费用或固定付款并不重要，因为平台面临相同的优化问题。然而这并不意味着我们应该同等对待这两种费用。事实上，一些作者指出我们不应忽视会员费和交易费之间的差异。Armstrong（2006）认为设置交易费是双边市场中向群体提供价格结构的主要决定因素，并且根据Filistrucchi（2008）所说，这个特点对于发展计量模型和SSNIP（小幅度、显著、非暂时性价格增加）等测试至关重要。关键洞察力在于强调无论我们关注哪种类型的费用, Lerner原则都适用. 因此, 有趣的问题是什么因素影响给定方面的价格结构或弹性。

As the classical market literature shows, many factors may influence the market structure, and multisided markets are not an exception. In the next sections, we focus on some of those factors that influence elasticities or price structure, such as the possibility of consuming more than one platform at a time (multihoming), taxation, switching costs, information, or expectations. In this sense, an exhaustive review of all the works that address multisided pricing is beyond the scope of this work. Instead, we narrow the scope to address theoretical works in areas in which the evidence is well-established.18

正如经典市场文献所述，市场结构受多种因素影响，多边市场也不例外。在接下来的章节中，我们将重点关注一些影响弹性或价格结构的因素，例如多重归属（即同时使用多个平台）、税收、转换成本、信息和预期。鉴于对所有涉及多边定价的研究进行详尽回顾超出了本文的范围，我们将范围缩小到处理那些在已有充分证据支持下的理论工作。

## 3.1 Exclusivity In Platforms. Singlehoming, And Multihoming



A common feature that we observe in multisided markets is that some agents tend to use several platforms at the same time. For example, drivers that use both Uber and Lyft. Couriers that use Glovo and Deliveroo. Several works have paid attention to the incentive to be on more than one platform at the same time, also known as multihoming. Multihoming is a natural part of a lot of markets. For example, in the newspaper industry, there is no way to prevent readers from reading two or more newspapers, and the same is also true for advertisers.19 Multihoming is also common in the payment card industry, where many merchants accept both Mastercard and Visa, and consumers have several payment cards. Or, in the digital economy, in which developers may support Android, iOS, or Windows Phone.

在多边市场中，我们观察到一个常见特征是一些参与者倾向于同时使用多个平台。例如，既使用Uber又使用Lyft的司机，同时使用Glovo和Deliveroo的快递员。已有研究关注了在同一时间内在多个平台上活动的激励因素，也被称为多重归属。多重归属在许多市场中都是自然而然的现象。例如，在报纸行业中，无法阻止读者阅读两份或更多份报纸，广告商也是如此。19 在支付卡行业中，接受Mastercard和Visa的商家很常见，并且消费者拥有几张支付卡。或者，在数字经济中，开发人员可能支持Android、iOS或Windows Phone等不同平台。

The reasons to multihome are diverse. For instance, Rochet and Tirole (2006) point out that multihoming stems from the users' desire to reap the benefits of network externalities in an environment of noninterconnected platforms. In a similar vein, Caillaud and Jullien (2001) and Caillaud and Jullien (2003) highlight that multihoming increases the probability of matching, and it allows consumers to save on transaction fees because they can adopt the cheaper platform.20 On the other hand, Choi (2010) points out that when there is exclusive content on platforms, there is also an incentive to multihome. However, this incentive to multihome depends on the degree of multihoming on the other side negatively. In other words, the incentives to join more than one platform decrease with the number of users on the other side that are common to several platforms, see Gabszewicz and Wauthy (2014). Rysman (2009) also observes that two-sided markets seem to evolve toward a situation in which members of one side use a single platform (singlehoming), and the other side uses several platforms (multihoming).

多重归属的原因是多种多样的。例如，Rochet和Tirole（2006）指出，多重归属源于用户在非互联平台环境中追求网络外部性效益的愿望。类似地，Caillaud和Jullien（2001）以及Caillaud和Jullien（2003）强调，多重归属增加了匹配的概率，并且它允许消费者通过选择更便宜的平台来节省交易费用。然而，Choi（2010）指出，在平台上存在独家内容时，也存在多重归属的动机。然而，这种动机取决于另一方面进行多重归属程度的负面影响。换句话说，随着共同使用几个平台的用户数量增加，加入超过一个平台的动机会减少（参见Gabszewicz和Wauthy，2014）。Rysman（2009）还观察到两边市场似乎向着一边成员使用单一平台（单一归属），而另一边使用多个平台（多重归属）发展。

It seems that multihoming is a great advantage because users can benefit from the network externalities of several platforms. But multihoming may not be as good as it seems. The maximal price multihoming consumers are willing to pay is the incremental value of having access to an extra platform, see Ambrus *et al*. (2016) and Anderson *et al*. (2019). Other things equal, multihoming consumers are thus less valuable than singlehoming consumers. Thus, the singlehoming side is usually subsidized by the multihoming side. So, their desire to reap the benefits of different network externalities leads platforms to increase prices on the multihoming side. In other words, multihoming influences the price structure by increasing competition on the singlehoming side but relaxing it on the multihoming one, see Rochet and Tirole (2003), Armstrong and Wright (2007), and Armstrong (2006). While there is competition for singlehoming customers, there is no direct competition for multihoming ones, even when they are homogeneous, see Armstrong and Wright (2007). This situation gives rise to so-called competitive bottlenecks, see Armstrong (2006). This is a consequence of platforms having monopoly power over providing access to their singlehoming customers. This difference between singlehoming and multihoming sides also leads to an asymmetric price structure, but this time, it is not motivated by the strength of network effects, but by the decisions of consuming one or more platforms.21
From a social point of view, because there is no direct competition for multihoming consumers, their interests are ignored, and there are too few multihoming customers.22 This market failure does not imply larger profits, as Armstrong (2006) argues: the excessive prices faced by the multi-homing side do not necessarily result in excess profits for platforms, since platforms might be forced by competitive pressure to transfer their monopoly revenues to the single-homing agents. In other words, factors that induce more multihoming may also induce more competition. For example, if more buyers are attracted by both platforms, platforms may compete harder for their positions.

多重归属似乎是一个巨大的优势，因为用户可以从多个平台的网络外部性中获益。然而，多重归属可能并不如表面看起来的那么好。多重归属消费者愿意支付的最高价格是额外获得一个平台访问权的增量价值（Ambrus等人，2016年；Anderson等人，2019年）。其他条件相同，因此多重归属消费者的价值低于单一归属消费者。因此，通常情况下，单一归属方面会得到多重归属方面的补贴。为了实现不同网络外部性的利益，平台会提高多重归属方面的价格。换句话说，多重归属通过增加单一归属方面的竞争程度而减少了多重归属方面的竞争（Rochet和Tirole，2003年；Armstrong和Wright，2007年；Armstrong，2006年）。尽管存在对单一归属客户的竟争，但即使是同质化用户也没有直接竟争（Armstrong和Wright, 2007) 。这种情况导致了所谓的竟争瓶颈（Armstrong, 2006年）。这是由于平台对其单一归属客户提供访问权的垄断力量。单一归属和多重归属方面之间的这种差异也导致了不对称的价格结构，但这次不是由网络效应的强度所驱动，而是由消费一个或多个平台的决策所驱动（21）。从社会角度来看，由于多重归属消费者没有直接竟争，他们的利益被忽视，并且多重归属客户数量较少（22）。正如Armstrong（2006年）所指出的那样，这种市场失灵并不意味着更高的利润：多重归属方面面临的过高价格并不一定导致平台获得超额利润，因为平台可能受到竞争压力而将其垄断收入转移给单一归属主体。换句话说，促使更多多重归属可能也会引起更多竟争。例如, 如果吸引了更多买家同时使用两个平台, 平台可能会为争夺位置而进行更激烈地竟争。

Nevertheless, some works challenge conventional wisdom according to which multihoming leads to monopoly prices on that side. Jeitschko and Tremblay (2014) show that when the homing decision is endogenous, prices will not converge to monopoly prices on the multihoming side, although those would be larger than without multihoming. But more surprising are the Belleflamme and Peitz (2019a)'s results. They show that it is not necessarily the case that multihoming users pay a higher fee, and singlehoming ones a lower fee. Although we may expect higher prices on the multihoming side because of the
"bottleneck effect," the multihoming side may end paying less than the singlehoming one. The reason for this counterintuitive result is that the platform faces a more elastic demand when the consumers' outside option is quitting the market rather than the competitor's offer. In other words, a fee reduction on the multihoming side may be more effective expanding the demand on that side. Therefore, two economic effects are at work: the market share effect that drives competing platforms to set a lower price than a monopolist and the price sensitivity effect that works in the opposite direction. Belleflamme and Peitz (2019a) conclude that it is impossible to state whether prices would be higher/lower on either side, but we can state that prices on both sides of the market always move in opposite directions. Other authors have also found this flipping behavior between singlehoming and multihoming. Anderson *et al*. (2019) find that multihoming flips the side of the market on which platforms compete. But this effect is not only limited to prices. They also found that multihoming may flip the side that it is impacted the most by a merger or an entry of a new firm.

然而，一些研究对传统观点提出了质疑，即多重归属会导致该方面的垄断价格。Jeitschko和Tremblay（2014）的研究表明，当归属决策是内生的时候，价格不会收敛到多重归属方面的垄断价格，尽管这些价格会比没有多重归属时更高。但更令人惊讶的是Belleflamme和Peitz（2019a）的研究结果。他们发现，多重归属用户支付较高费用、单一归属用户支付较低费用并不一定成立。尽管我们可能预期由于“瓶颈效应”，多重归属方面会有较高的价格，但实际上多重归属方面可能支付的费用比单一归属方面还要低。这种违反直觉的结果是因为当消费者选择退出市场而不是选择竞争对手提供的选项时，平台面临着更弹性的需求。换句话说，在多重归属方面降低费用可能更有效地扩大该方面的需求。因此，两种经济效应同时起作用：市场份额效应推动竟争平台设定比垄断者更低的价格；而价格敏感性效应则起到相反的作用。Belleflamme和Peitz（2019a）得出结论，无法确定价格在哪一方面会更高/更低，但可以确定市场两侧的价格总是朝着相反的方向变动。其他作者也发现了单一归属和多重归属之间的这种翻转行为。Anderson等人（2019）发现，多重归属会改变平台竞争的市场方面。但这种影响不仅仅局限于价格上。他们还发现，多重归属可能会改变对并购或新公司进入产生最大影响的市场方面。

Lastly, the conventional wisdom by which multihoming leads to monopoly prices has also sparked the literature around those factors that may mitigate multihoming, such as exclusivity contracts or compatibility among networks. For instance, with exclusive contracts, platforms force multihoming consumers to singlehome regardless of competitor's offers. This behavior also breaks competitive bottleneck equilibria. However, by forcing one side to choose one of the platforms, a platform may instead induce consumers to choose the rival one, see Armstrong and Wright (2007). Additionally, exclusivity contracts may create new damages that were unintended because when platforms prefer to impose exclusivity, they hurt at least one group of participants, see Belleflamme and Peitz (2019a).

最后，传统观点认为多重归属会导致垄断价格，这也引发了关于减轻多重归属的因素的文献讨论，如排他性合同或网络之间的兼容性。举例来说，通过排他性合同，平台强制多重归属的消费者无论竞争对手提供何种优惠都只选择一个平台。这种行为也打破了竞争瓶颈均衡。然而，通过迫使一方选择其中一个平台，该平台可能反而诱使消费者选择竞争对手的平台（参见Armstrong和Wright，2007）。此外，排他性合同可能会产生意外损害，因为当平台更倾向于实施排他性时，至少会伤害到一组参与者（参见Belleflamme和Peitz，2019a）。

Instead of making exclusive contracts, another way to disincentive multihoming is by becoming compatible. If platforms are compatible, there is no incentive to multihome because users will benefit from the network externalities of all the compatible platforms. Doganoglu and Wright (2006) find that compatibility mitigates the incentives to multihome, and because profits are increasing with respect to multihoming, platforms are less prone to compatibility. So, platforms have excessive incentives for incompatibility when customers multihome. But more interestingly, compatibility may mitigate price competition in two-sided markets by increasing the market imperfection, see Doganoglu and Wright (2006), Salim (2009), or Sanchez-Cartas and Leon (2017). When platforms are fully compatible, they do not internalize the network effects, and the subsidizing incentives disappear. This is an interesting result because it contrasts with the traditional one-sided literature in which the opposite is true, see Farrell and Saloner (1985) or Katz and Shapiro (1985).23

与采用独家合同不同，另一种减少多重归属的方法是通过兼容性。如果平台之间兼容，用户将从所有兼容平台的网络外部性中受益，因此没有多重归属的动机。Doganoglu和Wright（2006）发现，兼容性减轻了多重归属的激励，并且由于多重归属而增加了利润，平台对兼容性的倾向较小。因此，在客户进行多重归属时，平台对不兼容性有过度激励。但更有趣的是，在两边市场上，通过增加市场缺陷来减轻价格竞争可能会导致兼容性问题（Doganoglu和Wright，2006；Salim，2009；Sanchez-Cartas和Leon，2017）。当平台完全兼容时，它们不内部化网络效应，并且补贴激励消失。这一结果与传统单边文献相反，在传统单边文献中相反情况成立（Farrell和Saloner，1985；Katz和Shapiro，1985）。

## 3.2 The Role Of Information



A critical factor that influences price structure in classical markets is the degree of available information. Should platforms disclose their prices? How do platforms infere the size of network effects? Despite its relevance, the research on this topic is scarce, but the current evidence provides striking results. For instance, Hagiu and Hałaburda (2014) propose a model in which they analyze the impact on the price structure of price disclosure on one side. They prove that a monopoly has incentives to avoid asymmetries in information, but the opposite is true in a duopolistic framework. In other words, the larger the market power, the more likely platforms would inform about prices on all sides. This result is a consequence of network effects, when agents are informed, the effect of a price reduction is amplified. Platforms with more market power benefit because this leads to demand increases. In terms of prices, platforms tend to set higher prices when agents are less informed because demands are less reactive to price changes. Thus, any estimation of network effects based on observed prices would be different depending on the level of agent information. Belleflamme and Peitz (2019b) address the same issue, but they consider partial strategic disclosure on both sides instead of total coordinated disclosure on one side. They find that Hagiu and Hałaburda (2014)'s results are robust to partial disclosure. Interestingly, if platforms could coordinate their decisions, they would not inform any users, as shown by Hagiu and Hałaburda (2014). Following Hagiu and Halaburda's work, Sun (2018) addresses the same issue, but she considers a market with bundling/tying strategies. She finds that bundling is more effective in stimulating consumer demand when there are more informed consumers, which may amplify Hagiu and Halaburda's insights.24
On the other hand, sometimes is the platform that is uncertain about the externalities that each side exerts on the other. In this situation, platforms can use their fees to gradually learn about those externalities by observing participation. But how should the platform set prices under such uncertainty? Lowering fees increases the quantity of information, but it reduces current revenues. By extending Armstrong (2006)'s model, Peitz *et al*. (2017) find that, when there are only externalities/uncertainty on one side, it is optimal to set a fee lower than the myopic model (the price set by a monopolist when maximizing current revenues only) on the side that profit from the externality, and a higher one on the other side. But in a case with two uncertain externalities, the correlation between the direct and indirect effects of lowering fees across the states of the world play an essential role in defining the price structure. The intuitive direction of experimentation is to lower prices, which holds when uncertainty is high, but if this is moderate, it may be profitable to set higher prices than myopic ones on one side. This result implies that the casual chain from lower prices to higher participation levels to more informative outcomes can be overturned by the incentive to extract surplus (on the side that benefits more from the lower experimentation fee on the other side). Nevertheless, their results provide a rationale for introductory prices because the platform starts by charging lower prices on both sides then increase them over time. And more importantly, these results highlight that platforms can alter the intensity of competition by manipulating the information flow to consumers.

3.2 信息的作用

在经典市场中，影响价格结构的一个关键因素是可获得的信息程度。平台是否应该披露其价格？平台如何推断网络效应的规模？尽管这个问题非常重要，但对于这个主题的研究却很少，但目前的证据提供了令人震惊的结果。例如，Hagiu和Hałaburda（2014）提出了一个模型，在该模型中他们分析了价格披露对价格结构的影响。他们证明，在垄断框架下，垄断者有动机避免信息不对称，但在双头寡头框架下则相反。换句话说，市场力量越大，平台越有可能在所有方面都公开价格。这一结果是网络效应导致的，当主体被告知时，降价效果会被放大。拥有更多市场力量的平台会从中受益，因为这会导致需求增加。就价格而言，在主体信息较少时平台倾向于设定较高价格，因为需求对于价格变化反应较弱。因此，在基于观察到的价格进行网络效应估计时, 结果将取决于主体信息水平不同。

Belleflamme和Peitz（2019b）也讨论了同样的问题，但他们考虑了双方的部分策略性披露，而不是单方面的全面协调披露。他们发现Hagiu和Hałaburda（2014）的结果对于部分披露是稳健的。有趣的是，如果平台能够协调他们的决策，根据Hagiu和Hałaburda（2014）所示，他们将不会向任何用户提供信息。在Hagiu和Halaburda工作之后，Sun（2018）也讨论了同样的问题，但她考虑了一个具有捆绑/绑定策略的市场。她发现，在存在更多知情消费者时，捆绑更有效地刺激消费者需求, 这可能会放大Hagiu和Hałaburda的观点。

另一方面, 有时平台对于每一方对其他方产生外部性感到不确定。在这种情况下, 平台可以通过观察参与来逐渐了解这些外部性。但在这种不确定性下, 平台应该如何设定价格？降低费用可以增加信息量, 但会减少当前收入。通过扩展Armstrong（2006）模型, Peitz等人(2017)发现当只有一方存在外部性/不确定性时, 在从外部性中获益的一方设定低于短视模型（仅最大化当前收入时垄断者设定的价格）的费用是最优的, 而在另一方面则设定较高费用。但在存在两个不确定外部性的情况下，降低费用对世界状态之间降低费用的直接和间接影响之间的相关性起着至关重要的作用来定义价格结构。直观上，实验方向是降低价格，在不确定性较高时成立，但如果这种不确定性适度，则可能会将价格设置为高于短视模型在一方面上设置的价格。这个结果意味着从更低价格到更高参与水平再到更多信息化结果这个因果链条可以被提取剩余价值（对于从另一方面获得更多实验费用减少所产生效益）所推翻。尽管如此，他们的结果为引入期初价格提供了合理解释，因为平台开始通过向两个方面收取较低价格然后随时间增加它们来进行收费。而且更重要地是, 这些结果强调了平台可以通过操纵向消费者传递信息流来改变竞争强度。

## 3.3 Taxation And Customers' Behavior



Taxes are a fundamental factor that alters price structure in classical markets, and they influence multisided markets too, but the way they do it is different.25 Taxation on digital platforms is more complex than in one-sided markets, and in some cases, it requires a completely new design. The innate characteristics of digital products and digital platforms modify the effects and the optimal design of taxes in potentially unexpected ways, see Kind and Koethenbuerger (2018). For example, it is possible that taxing a two-sided platform may increase the number of affiliates on both sides, see Kind *et al*. (2008). They find that a higher value-added tax on one side may be profitable for the platform to shift revenue from that side to the other one (from the heavily taxed to the untaxed side). Because of this balance, the output on both sides may increase. In a similar vein, Kind *et al*. (2013) point out that, in media platforms, even if consumers dislike ads, a tax aimed to reduce ad levels may affect consumers negatively. The cross-relationships among the sides implies that the impact of taxation cannot be limited to consider the side upon which such tax is levied only, because of the network effects, platforms will react by shifting revenues from the sides, which may go against the motivations of the tax.

税收是经典市场中改变价格结构的基本因素，同时也对多边市场产生影响，但其方式有所不同。数字平台上的税收问题比单边市场更为复杂，在某些情况下，需要进行全新的设计。数字产品和数字平台的固有特性会以意想不到的方式改变税收的效果和最优设计，详见Kind和Koethenbuerger（2018）。例如，对双边平台征税可能会增加两个方面的关联方数量，参见Kind等人（2008）。他们发现，在一方面增加增值税可能对平台有利，将收入从受重税一方转移到未征税一方。由于这种平衡，两个方面的产出可能会增加。类似地，Kind等人（2013）指出，在媒体平台上，即使消费者不喜欢广告，旨在减少广告水平的税收也可能对消费者产生负面影响。各个方面之间的相互关系意味着不能仅仅考虑征收该项税收所涉及到的那一方面来限制其影响力量, 因为由于网络效应, 平台将通过从各个方面转移营收来做出反应, 这可能与征税动机相悖。

Up to now, the literature has focused on comparing the effects of value-added and unit taxes on price structure, where effects are quite different. Kind *et al*. (2009) find that a higher specific tax on one side leads to a lower affiliation, as in one-sided markets, but the opposite may be true with ad valorem taxes. Similarly, Belleflamme and Toulemonde (2018) find that transaction taxes hurt agents on both sides and benefit platforms. On the other hand, they also confirm the result found by Kind *et al*. (2008) that ad valorem taxes may benefit users that are taxed, but it may hurt agents on the other side of the market. In terms of welfare, the dominance of ad valorem taxes, which is common in one-sided markets, does not hold in two-sided markets. In fact, unit taxes may yield higher welfare than ad valorem taxes.26
Interestingly, taxes do not influence the prices only. Kind *et al*. (2013) prove that taxes may affect the optimal location of horizontally differentiated platforms. In other words, taxes may affect the political views of newspapers too.

迄今为止，文献主要关注于比较增值税和单位税对价格结构的影响，而这些影响是相当不同的。Kind等人（2009）发现，在单边市场中，对一方征收更高的特定税会导致附属关系降低，但按比例征收的情况可能恰恰相反。类似地，Belleflamme和Toulemonde（2018）发现交易税会损害双方主体并使平台受益。然而，他们也证实了Kind等人（2008）的研究结果：按比例征收的税可能使纳税用户受益，但可能损害市场另一侧的主体。在福利方面，在单边市场中普遍适用的按比例征收税并不适用于双边市场。事实上，单位税可能产生比按比例征收更高的福利效果。

有趣的是，税收不仅仅影响价格。Kind等人（2013）证明了税收可能影响水平差异化平台的最优位置选择。换言之，税收也可能影响报纸媒体的政治观点。

Lastly, customers' heterogeneity is a wide branch that has attracted many efforts in the last decades.

最后，顾客的异质性是一个广泛的领域，在过去几十年中吸引了许多研究努力。

Heterogeneity may appear in many forms and can be modeled in many ways. One kind of heterogeneity that has a big impact on multisided platforms is the one related to beliefs, either about the participation or about the transaction.

异质性可以以多种形式出现，并可以用多种方式进行建模。对于多边平台而言，与参与或交易相关的信念相关的异质性具有重大影响。

In certain situations, consumers have different beliefs about how many people will join the platforms.

在某些情况下，消费者对于有多少人会加入平台持有不同的信念。

This situation implies that consumers have different beliefs about other consumers' preferences. Jullien and Pavan (2019) study this case and find that although the Armstrong (2006) price structure still holds, it is necessary to consider a new term that accounts for agents' beliefs, which can lead to either higher or lower prices depending on whether the preferences on both sides are positively or negatively correlated. Contrary to the complete information framework, prices under dispersed information increase with the intensity of the own-side network effects if preferences are aligned, or decrease if they are misaligned. Intuitively, if preferences are positively correlated, and consumers are optimistic about the participation on the other side, they will expect high participation on the other side, which implies that only the pessimistic consumers are excluded. Therefore, an increase in price on, say, side A drops side-A's demands less than when all consumers have the same beliefs, in other words, demand elasticity is lower, and prices are higher.

这种情况表明消费者对其他消费者的偏好持有不同的信念。Jullien和Pavan（2019）对此进行了研究，并发现尽管Armstrong（2006）的价格结构仍然适用，但需要考虑一个新的因素来考虑主体的信念，这可能导致价格上升或下降，具体取决于双方偏好是正相关还是负相关。与完全信息框架相反，在信息分散的情况下，如果偏好一致，则价格随着自身网络效应的强度增加而增加；如果偏好不一致，则价格下降。直观地说，如果偏好是正相关的，并且消费者对于在另一方面参与持乐观态度，他们将预期在另一方面有很高的参与度，这意味着只有悲观主义者被排除在外。因此，在A方面提高价格时，A方面需求减少得比所有消费者都持有相同信念时要少，换句话说，需求弹性较低，价格较高。

Instead of having different beliefs, customers may be different. Not all consumers create the same externality on the other side, some of them are more relevant. Influencers are a clear example of these consumers, and their presence in multisided platforms also influence pricing. Rochet and Tirole (2003) and Hogendorn and Ka Yat Yuen (2009) show that "marquee buyers" or "must-have" components increase prices on the opposite side, and Carroni *et al*. (2019), who coined the term "superstar" to mention those consumers, find that, if only one platform has those superstars, their prices are higher than competitors, and via network effects, the content variety and the number of other consumers on the same side increases. Intuitively, the presence of a superstar in a playlist may make indie artists more likely to be discovered, thus their opportunity costs are lowered, and their expected profits increased. However, this "expansion" effect implies that the superstar should be compensated, and Carroni *et al*. (2019) find that such compensation can be more than two-thirds of the total surplus created. Hogendorn and Ka Yat Yuen (2009) show that, in some cases, a negative price on those special customers could be optimal for the smallest platform.

与拥有不同信念的情况不同，消费者可能存在差异。并非所有消费者对另一方面产生相同的外部性，其中一些更为相关。影响者是这些消费者的明显例子，在多边平台上的存在也会对定价产生影响。Rochet和Tirole（2003）以及Hogendorn和Ka Yat Yuen（2009）指出，“招牌买家”或“必备”组件会提高对立方面的价格，而Carroni等人（2019）则将这些消费者称为“超级巨星”，发现如果只有一个平台拥有这些超级巨星，其价格将高于竞争对手，并通过网络效应增加了内容的多样性以及相同方面其他消费者的数量。直观来看，在播放列表中出现一个超级巨星可能会增加独立艺术家被发现的机会，从而降低他们的机会成本并增加预期利润。然而，这种“扩张”效应意味着应该对超级巨星进行补偿，Carroni等人（2019）发现此类补偿可能超过总剩余价值的三分之二以上。Hogendorn和Ka Yat Yuen（2009）表明，在某些情况下，对那些特殊客户实施负价格可能对最小的平台是最优的。

Nonetheles, customers may be heterogeneous in more than one dimension. Weyl (2010) shows that when consumers have different transaction and membership values, this bidimensional heterogeneity generates two distortions in the prices. First, the classical markup of the market power, and second, the Spence distortion.27 He points out that the Spence distortion may increase (reduce) prices, but it depends on the source of heterogeneity, transaction, and membership values. An interesting result derived from the sign of the Spence distortion is that it exists the possibility of mitigating the market power distortion with an opposite Spence distortion. Thus, the harm of market power depends on the source of heterogeneity. For example, in the case of newspapers, it may be the case that, if heterogeneity in willingness to pay for content dominates and is correlated with willingness to pay to avoid advertising, then average readers dislike advertising more than marginals, and the Spence distortion is downward, which mitigates the market power distortion.28
A common assumption of the literature is to consider that consumers are preassigned to different sides. However, it may be the case that some consumers may choose on which side they want to be. For example, a user today may prefer to be an Uber driver, but maybe tomorrow she would be a user. Choi and Zennyo (2019) address this case by extending Armstrong (2006)'s model, and they find that asymmetric price structures may arise because some sides may be less favored. Users may prefer to be on one side despite large network effects, and that may lead platforms to offer discounts on the other side to convince users of changing sides. This source of asymmetry in prices may lead to the first best social welfare with competing platforms. Profit-maximizing platforms adjust their prices to enhance the number of transactions, and in the process, they increase consumers' welfare.

然而，消费者可能在多个维度上存在异质性。Weyl（2010）指出，当消费者在交易和会员价值上存在差异时，这种双重异质性会对价格产生两个扭曲。首先是市场力量的经典加价，其次是Spence扭曲。他指出，Spence扭曲可能会增加（减少）价格，但这取决于异质性的来源，即交易和会员价值。有趣的是，根据Spence扭曲的符号，可以通过相反的Spence扭曲来减轻市场力量的扭曲。因此，市场力量的危害取决于异质性的来源。例如，在报纸业务中，如果愿意为内容付费的异质性主导，并且与愿意避免广告付费相关，则平均读者对广告的厌恶程度超过边际读者，并且Spence扭曲向下减轻了市场力量的扭曲。

文献中常见假设是将消费者预先分配到不同方面。然而，并非所有消费者都必须被分配到特定方面。例如，今天用户可能更喜欢成为Uber司机，但明天她可能成为用户。Choi和Zennyo（2019）通过扩展Armstrong（2006）的模型来解决这种情况，并发现不对称的价格结构可能会出现，因为某些方面可能不受青睐。尽管存在较大的网络效应，用户可能更喜欢选择一方面，这可能导致平台在另一方面提供折扣以说服用户改变立场。价格上的这种不对称性来源可能导致具有竞争平台的最佳社会福利。利润最大化的平台调整其价格以增加交易数量，并在此过程中增加消费者福利。

As a summary, customers can be heterogeneous in different ways, which have different implications on the price structure. However, up to now, the study of such heterogeneities has been mainly influenced by classical heterogeneities, but there are open questions regarding new kinds of heterogeneities that are unique to digital platforms that may influence the price structure as well, such as privacy policies or digital literacy. Finally, to outline the key works regarding price structure, Table 2 highlights the essential works.

总结起来，消费者在不同方面可能存在异质性，这对价格结构有不同的影响。然而，目前对这种异质性的研究主要受到经典异质性的影响，但是关于数字平台独特的新型异质性对价格结构可能产生影响的问题仍然存在。例如隐私政策或数字素养等。最后，在价格结构方面概述关键作品时，表2突出了重要作品。

## 4. Coordination Problems: Chicken And Egg Problem



A key feature of two-sided markets is that platforms have to be able to attract two or more different types of users that need each other in some way. Thus, the market outcome is shaped by consumers' beliefs about participation on each platform. A digital platform with users but without developers has no future, and the opposite is also true. The demand on each side tends to vanish if there is no demand on the other side … regardless of what the price is. […] The businesses that participate in these industries have to figure out ways to get both sides on board, see Evans (2003b). This problem is known as "the chicken & egg problem" in the literature, and it broadly refers to any coordination issue arising from network effects, see Caillaud and Jullien (2001).

两边市场的一个重要特征是平台必须能够吸引两种或更多不同类型的用户，这些用户在某种程度上需要彼此。因此，市场结果受到消费者对每个平台参与的信念的影响。一个没有开发者但有用户的数字平台没有未来，反之亦然。如果一方没有需求，另一方的需求往往会消失，无论价格如何。参与这些行业的企业必须找到方法让双方都加入进来（Evans，2003b）。这个问题在文献中被称为“鸡和蛋问题”，它广泛指任何由网络效应引起的协调问题（Caillaud和Jullien，2001）。

The coordination problem appears in the simplest equilibrium definitions. In fact, Caillaud and Jullien
(2003) state that the uniqueness of equilibrium is hard to justify in many contexts. In the same vein, White and Weyl (2016) point out that if platforms charge "flat prices" that are not contingent on opposite-side participation levels, then there is a possibility of multiple equilibria. Thus, one interesting complication of setting prices in multisided markets is that it is not so easy as setting a mark-up over costs. The price structure has to take into account the participation of all sides. But one side only participates if the other sides do, and vice versa. This feedback loop may create a multiple equilibria problem because consumers' decisions (users) are not isolated from other consumers' decisions (developers). If there are multiple equilibria, and we cannot discriminate among them, we cannot make predictions about the success/failure of platforms. Nonetheless, not all modeling approaches suffer this issue, in many cases, such multiplicity never occurs. For example, when horizontal or vertical differentiation is stronger than network effects. Basically, if network effects are not too large, the coordination game has a unique solution, see Filistrucchi and Klein (2013) and Weyl (2010). On the other hand, when network effects are the dominant force, we may need to face a coordination problem.

协调问题在最简单的均衡定义中出现。实际上，Caillaud和Jullien（2003）指出，在许多情况下很难证明均衡的唯一性。同样，White和Weyl（2016）指出，如果平台收取不依赖于对立方参与水平的“固定价格”，那么存在多个均衡的可能性。因此，在多边市场中设定价格并不像简单地加价那样容易。价格结构必须考虑到所有方面的参与。但是只有当其他方面参与时，一方才会参与，反之亦然。这种反馈循环可能会导致多个均衡问题，因为消费者（用户）的决策不是孤立于其他消费者（开发者）的决策之外。如果存在多个均衡，并且我们无法区分它们，则无法对平台的成功/失败进行预测。尽管如此，并非所有建模方法都存在这个问题，在许多情况下，这种多样性从未发生过。例如，在水平或垂直差异比网络效应更强烈时。基本上，如果网络效应并不太大，则协调博弈有唯一解决方案，请参见Filistrucchi和Klein（2013）以及Weyl（2010）。另一方面，当网络效应成为主导力量时，我们可能需要面对协调问题。

There is no universal way to deal with the chicken and egg problem in the multisided literature. There have been proposed different approaches, the earliest one was based on expectations or beliefs. If the participation of one group depends on the participation of another group, an intuitive and direct way to solve the problem is by paying attention to how those groups believe the other group would behave.

在多边文献中，处理“先有鸡还是先有蛋”的问题并没有一种普遍适用的方法。已经提出了不同的方法，其中最早的一种基于期望或信念。如果一个群体的参与取决于另一个群体的参与，解决这个问题的直观且直接的方式是关注这些群体对另一个群体行为的信念。

Whether agents will coordinate on the positive participation level or not depends on their beliefs about what the other side is doing. Thus, beliefs matter and agents only participate if they are confident in the participation of the others, see Jullien (2005). Intuitively, given a price and expectations, customers in one group can perfectly forecast what other customers in other groups will do, and they will coordinate themselves in the equilibrium that is the best for them. This approach is used to discriminate among equilibria in many works, such as Caillaud and Jullien (2001), Caillaud and Jullien (2003), Doganoglu and Wright (2006), Hagiu (2006), Bakos and Katsamakas (2008), Chao and Derdenger (2013), and Economides and Tåg (2012). However, White and Weyl (2016) point out that it is a risky bet to focus only on consumers' ability to coordinate among themselves. In their vision, although this solution to the coordination problem is a satisfactory one because it allows us to discriminate among equilibria, it implies that consumers can coordinate among themselves almost perfectly, which is not realistic.

参与者是否在积极参与的水平上进行协调取决于他们对对方行为的信念。因此，信念是重要的，只有当参与者对其他人的参与充满信心时，他们才会加入。Jullien（2005）提出了这一观点。从直觉上讲，给定一个价格和期望值，一个群体中的顾客可以完美地预测其他群体中的顾客将会采取什么行动，并且他们将在对自己最有利的均衡点上进行协调。这种方法被用于区分多个作品中的均衡点，如Caillaud和Jullien（2001），Caillaud和Jullien（2003），Doganoglu和Wright（2006），Hagiu（2006），Bakos和Katsamakas（2008），Chao和Derdenger（2013）以及Economides and Tåg (2012)。然而，White和Weyl (2016)指出仅关注消费者之间协调能力是一种冒险。根据他们的观点，尽管这种解决协调问题的方法是令人满意的，因为它使我们能够区分不同均衡点，但它意味着消费者几乎可以完美地相互协调，在现实中并不现实。

Multisided dimensions
Topics
Articles
Price structure
General pricing rules
Rochet and Tirole (2003), Rochet and Tirole (2006), Armstrong
(2006), Caillaud and Jullien (2001), Caillaud and Jullien (2003),
Weyl (2010)
Multihoming and
Armstrong (2006), Armstrong and Wright (2007), Belleflamme
bottleneck competition
and Peitz (2019a), Doganoglu and Wright (2006), Jeitschko and Tremblay (2014)
Imperfect information
Hagiu and Hałaburda (2014), Belleflamme and Peitz (2019b),
Peitz *et al*. (2017), Sun (2018)
Taxation
Kind *et al*. (2010), Kind *et al*. (2008), Kind *et al*. (2009), Kind
et al. (2013), Kind and Koethenbuerger (2018), Belleflamme and Toulemonde (2004)
Heterogenity
Weyl (2010), Jullien and Pavan (2019), Carroni *et al*. (2019),
Rochet and Tirole (2003)
Network effects
Expectation-based
Caillaud and Jullien (2001), Caillaud and Jullien (2003), Jullien
approach
(2005), Doganoglu and Wright (2006), Hagiu (2006), Bakos
and Katsamakas (2008), Chao and Derdenger (2013), Economides and Tåg (2012)
Focality approach
Halaburda and Yehezkel (2019), Jullien (2011)
Divide-and-conquer
Caillaud and Jullien (2001), Caillaud and Jullien (2003), Amelio
and Jullien (2012), Jullien (2011), Jullien (2005), Parker and Van Alstyne (2005), Evans (2003b)
Insulating tariffs
Weyl (2010), White and Weyl (2016), Cabral (2019)
Coalitional razionability
Ambrus and Argenziano (2009)
Ownership structure
Rysman (2009), Evans *et al*. (2008), Evans (2011)
Property rights
Merchants vs platforms
Hagiu (2007), Hagiu and Wright (2015), Hagiu and Wright (2019)
Open source and
Rochet and Tirole (2003), Hagiu (2004), Choi and Zennyo (2019),
not-for-profit platforms
Economides and Katsamakas (2006)
Optimal ownership
Bakos and Katsamakas (2008), Ambrus and Argenziano (2009)
Partial/total integration
Kind *et al*. (2016), Nocke *et al*. (2007), De Corniere and Taylor
(2014), Jullien and Sand-Zantman (2019)

多维度
主题
文章
价格结构
一般定价规则
Rochet和Tirole（2003年），Rochet和Tirole（2006年），Armstrong（2006年），Caillaud和Jullien（2001年），Caillaud和Jullien（2003年），Weyl（2010年）
多重归属和瓶颈竞争
Armstrong（2006年），Armstrong和Wright（2007年），Belleflamme和Peitz（2019a），Doganoglu和Wright（2006年），Jeitschko and Tremblay (2014)
信息不完全
Hagiu and Hałaburda (2014年)，Belleflamme and Peitz (2019b)，Peitz *et al*. (2017年)，Sun (2018年)
税收
Kind *et al*. (2010年)，Kind *et al*. (2008年)，Kind *et al*. (2009年)，Kind et al. (2013年)，Kind and Koethenbuerger (2018年)，Belleflamme and Toulemonde (2004)
异质性
Weyl （ ） ，Jullien 和 Pavan （ ） ，Carroni * et al *. （ ） ，Rochet 和 Tirole （ ）
网络效应 
基于期望的方法 
Caillaud 和 Jullien （   )，Caillaud 和 Jullien （   )，Jullien(   )，Doganoglu 和 Wright(   )，Hagiu(   )，Bakos 和 Katsamakas(   )，Chao 和 Derdenger(   )，Economides and Tåg(   )
焦点方法 
Halaburda 和 Yehezkel(   )，Jullien(   )
分而治之 
Caillaud 和 Jullien （  ） ，Caillaud 和 Jullien （  ） ，Amelio and Jullien （  ） ，Jullien（   )，Parker and Van Alstyne（   )，Evans (2003b)
隔离关税 
Weyl (2010)，White and Weyl (2016)，Cabral (2019)
联合合理性 
Ambrus 和 Argenziano(   )
所有权结构
Rysman (2009)，Evans *et al*. (2008)，Evans (2011)
产权
商家 vs 平台
Hagiu (2007)，Hagiu and Wright (2015)，Hagiu and Wright (2019)
开源和非营利平台
Rochet 和 Tirole （    )，Hagiu（    )，Choi and Zennyo（    )，
Economides and Katsamakas（    )
最优所有权
Bakos 和 Katsamakas(    )，Ambrus和Argenziano(    )
部分/完全整合
Kind *et al*. （     ), Nocke *et al*. （     ), De Corniere和Taylor（     ), Jullien和Sand-Zantman（     )

多维度
主题
文章
价格结构
一般定价规则
Rochet和Tirole（2003年、2006年），Armstrong（2006年），Caillaud和Jullien（2001年、2003年），Weyl（2010年）
多重归属和瓶颈竞争
Armstrong（2006年），Armstrong和Wright（2007年），Belleflamme和Peitz（2019a），Doganoglu和Wright（2006年），Jeitschko和Tremblay（2014年）
信息不完全
Hagiu和Hałaburda（2014年），Belleflamme和Peitz（2019b），Peitz等人（2017年），Sun（2018年）
税收
Kind等人（2010年、2008年、2009年、2013年），Kind and Koethenbuerger（2018年），Belleflamme and Toulemonde（2004）
异质性
Weyl，Jullien and Pavan，Carroni等人，Rochet和Tirole
网络效应
基于期望的方法
Caillaud和Jullien，Jullien，Doganoglu和Wright，Hagiu，Bakos和Katsamakas，Chao和Derdenger，Economides and Tåg
焦点方法
Halaburda and Yehezkel，Jullien
分而治之
Caillaud和Jullien，Amelio and Jullien，Parker and Van Alstyne，Evans (2003b)
隔离关税
Weyl，White and Weyl，Cabral
联合合理性
Ambrus and Argenziano
所有权结构
Rysman，Evans等人，Evans
产权
商家 vs 平台
Hagiu，Hagiu and Wright，Hagiu and Wright
开源和非营利平台
Rochet和Tirole，Hagiu，Choi and Zennyo，Economides and Katsamakas
最优所有权
Bakos和Katsamakas，Ambrus和Argenziano
部分/完全整合
Kind等人，Nocke等人，De Corniere and Taylor，Jullien和Sand-Zantman

Ambrus and Argenziano (2009) state that if there are lots of small consumers in the market, then it is practically impossible for them to get together and make explicit agreements on network choices. They propose a way to overcome the coordination problem without assuming the consumers' ability to coordinate themselves. A noncooperative solution concept that assumes players can coordinate to restrict their play to a subset of the original strategy set if it is in the interest of every participant to do so, they called it: "coalitional rationalizability." However, this solution still requires assuming that consumers can coordinate their decisions to some degree and, in the case of small consumers, that is not realistic.

根据Ambrus和Argenziano（2009）的研究，如果市场上存在大量的小型消费者，那么他们几乎不可能集结起来就网络选择达成明确的协议。为了克服这种协调问题，他们提出了一种方法，该方法不需要假设消费者能够自行协调。他们称之为“联合合理性”，这是一种非合作解概念，假设玩家可以协调以限制他们的策略选择为原始策略集合的子集，如果这对每个参与者都有利。然而，这种解决方案仍然需要假设消费者在某种程度上能够协调他们的决策，在小型消费者的情况下是不现实的。

Other authors have considered that the multiplicity problem relies on timing. If the problem is to attract both sides at the same time, platforms may be interested in changing the timing. That is the proposal to overcome the coordination problem developed by Hagiu (2006). He proposes a model in which software developers arrive before consumers. This asymmetry in timing mitigates the coordination problem on the consumers' side, but it does not mitigate it on the developers' side. However, because it relies on customers' expectations, it suffers the same drawbacks that we described before.

其他作者认为多样性问题与时间有关。如果问题是同时吸引双方，平台可能会有兴趣改变时间。这就是Hagiu（2006）提出的克服协调问题的建议。他提出了一个模型，其中软件开发者先于消费者到达。这种时间上的不对称性减轻了消费者一侧的协调问题，但并没有减轻开发者一侧的协调问题。然而，由于它依赖于客户的期望，因此遭受了我们之前所描述的相同缺点。

On the other hand, White and Weyl (2016) point out that pricing policies may solve this problem even among heterogeneous consumer groups. Their idea is based on preliminary results of Rochet and Tirole (2003) and Armstrong (2006), in which platforms commit to offering consumers a particular level of utility, thus giving them a dominant strategy. The coordination arises because platforms adjust their price in response to changes in the number of users on the other side, fully insuring users against any change in their utility. Thus, coordination emerges not because consumers have some intrinsic ability to coordinate themselves but because platforms give them a dominant strategy. But both cases have two limitations. First, they rely on a particular preference structure. Second, users are unidimensionally heterogeneous. If users are heterogeneous in more than one dimension, it is not possible to give all consumers a dominant strategy with a uniform price.

然而，White和Weyl（2016）指出，即使在消费者群体异质的情况下，定价政策也可能解决这个问题。他们的观点基于Rochet和Tirole（2003）以及Armstrong（2006）的初步研究结果，这些研究表明平台承诺向消费者提供特定水平的效用，从而给予他们一种占优势的策略。协调是因为平台根据另一方用户数量的变化调整价格，完全确保用户不受其效用变化的影响。因此，协调并非因为消费者具有某种固有的协调能力，而是因为平台给予他们一种占优势的策略。然而，这两种情况都存在两个限制。首先，它们依赖于特定的偏好结构。其次，在用户在多个维度上具有异质性时，并不能通过统一价格给所有消费者提供一个占优势策略。

Weyl (2010) proposes a model in which users on one side can be heterogeneous along two dimensions, interaction and membership values.29 To address the coordination problem, Weyl proposes the "insulating tariffs" concept. The basic idea to overcome the coordination problem is to assume that platforms choose user allocations (and not prices) to maximize some objective function. In that way, prices are an insurance instrument of utilities. Platforms charge a price on each side, fixing a utility level, which gives users a dominant strategy. In this way, prices are a function of the number of participants so, from the consumers' point of view, they are isolated from participation on the other side. Following the previous works, White and Weyl (2016) propose the "residual insulating tariffs" as a solution to the coordination problem that is a generalization of Insulating Tariff to environments with rich preference heterogeneity. Despite being a formal and elegant solution, there are not many works in which insulating tariffs are applied. One reason is that the results cannot be compared with works based on other frameworks—see Belleflamme and Toulemonde (2018)—and, in contrast, in the vast majority of models in this literature, platforms set prices and assume a specific allocation of users.30
Cabral (2019) criticizes this approach by pointing out that platforms cannot fix a utility level on one side that is independent of the size of the other side because the platform does not "insure" agents, rather the platform "subsidizes" early adopters to compensate for the low utility of joining the platform at that stage. However, White and Weyl (2016) argue that there is an exact correspondence between equilibrium prices in the [Cabral's] dynamic model, and insulating prices in the static [White and Weyl's] model. However, the idea proposed by Cabral is intuitively closer to the actual managerial practices. In fact, subsidizing early adopters could be understood as the dynamic equivalent of the Weyl's insulating tariffs. Cabral argues that the platform has to subsidize early adopters to compensate them for the low utility of joining the platform at an early stage, or in other words, to compensate them for the low number of other customers on the platform. Therefore, the nature of the coordination problem is independent of the static/dynamic approach. However, the dynamic approach opens new questions that cannot be addressed with static models.

Weyl（2010）提出了一个模型，其中一方的用户在交互和成员价值两个维度上具有异质性。为了解决协调问题，Weyl提出了“隔离关税”的概念。其基本思想是假设平台选择用户分配（而非价格）以最大化某个目标函数。这样一来，价格就成为效用的保险工具。平台对每一方收取价格，确定一个效用水平，从而给用户提供占优势策略。因此，价格是参与者数量的函数，从消费者角度看，他们与另一方的参与是相互隔离的。White和Weyl（2016）在之前的研究基础上提出了“剩余隔离关税”，将其推广到具有丰富偏好异质性的环境中作为协调问题的解决方案。然而，尽管这是一个形式优雅的解决方案，但应用隔离关税的研究并不多见。其中一个原因是无法将结果与其他基于不同框架的研究进行比较（参见Belleflamme和Toulemonde，2018）。Cabral（2019）对这种方法提出批评，并指出平台无法在一方规模独立于另一方的情况下确定一个效用水平，因为平台并非“保险”主体，而是通过对早期采用者进行“补贴”来弥补他们在该阶段加入平台时效用较低的情况。然而，White和Weyl（2016）认为，在[Cabral的]动态模型中均衡价格与静态[White和Weyl的]模型中的隔离价格存在确切对应关系。然而，Cabral提出的想法在直观上更接近实际管理实践。事实上，对早期采用者进行补贴可以被理解为Weyl隔离关税的动态等价物。Cabral认为，平台必须对早期采用者进行补贴，以弥补他们在早期阶段加入平台时效用较低（或者换句话说，弥补他们在平台上其他客户数量较少）的情况。因此，协调问题的性质与静态/动态方法无关。然而，动态方法引发了一些无法通过静态模型解决的新问题。

On the one hand, dynamic models allow us to address the growth over time, and therefore, to consider which are the best strategies to get customers on board. In this sense, a usual pattern of platform growth is when the number of users on both sides increases in tandem, see Cabral (2019). In that sense, Filistrucchi et al. (2013) state that it is also fundamental for the platform to attract the different sides in the right proportion. On the other hand, dynamic models allow us to address the critical mass problem. Evans and Schmalensee (2010) study this issue, and they find that when the critical mass is reached, the positive feedback between the sides drives the market to equilibrium. Nevertheless, the critical mass depends on prices charged, platform features, agent's tastes, etc. These characteristics can modify the critical mass and the stability of the platform.

一方面，动态模型使我们能够考虑随时间推移的增长，并因此思考如何制定最佳策略来吸引客户。在这方面，平台增长的常见模式是双方用户数量同步增加（Cabral，2019）。Filistrucchi等人（2013）指出，平台以正确的比例吸引不同方面的用户也是至关重要的。另一方面，动态模型使我们能够解决关键质量问题。Evans和Schmalensee（2010）研究了这个问题，并发现当达到关键质量时，双方之间的正反馈推动市场达到均衡。然而，关键质量取决于收费价格、平台特性、主体偏好等因素。这些特征可以改变关键质量和平台的稳定性。

Nonetheless, instead of focusing on consumers' ability to coordinate, we can focus on platforms'
ability to influence beliefs. This is the starting point of focality advantage, which is attracting attention recently. In a broad sense, focality is an incumbency advantage based on consumers' expectations. Intuitively, the idea is that platforms can "influence" customers into thinking that only some equilibria are possible. This advantage implies that, in some unspecified way, a platform can signal consumers that other consumers will join the platform as well, see Halaburda and Yehezkel (2019).31 However, this concept is rather general, and its definition does not identify how and why this focality emerges. It could be a consequence of branding, reputation, advertising, or other investments. From a practical point of view, the matching technology of the platform could constitute a focality advantage too. Currently, this is the main limitation of this approach because it relies on assuming an exogenous and ill-defined effect to limit the set of potential equilibria. For example, Halaburda and Yehezkel (2019) argue that the success (failure) of Apple (Windows Phone) could be attributed to focality. Apple succeeded because users were buying new and expensive phones even though developers had not developed apps to support all the new features, but users anticipated all those potential benefits. On the other hand, users and developers were skeptical about whether Windows phone could attract consumers from Google or Apple and developers to a platform not different from the others. How those users anticipated all those potential benefits, or how developers became skeptical is not explained. This approach simply assumes that Apple had an exogenous advantage with respect to Windows.32 At first glance, this approach seems to be similar to the "coalitional rationalizability" in the sense that both reduce the set of equilibria. However, focality relies on assuming that some equilibria are unfeasible because of some exogenous features of platforms, while "coalitional rationalizability" relies on customers' ability to coordinate themselves. The appealing feature of this approach is its simplicity. In contrast with coalitional rationalizability, focality does not require defining a new noncooperative solution concept but just to exclude some equilibria based on an exogenous criteria. Hitherto, this is a promising approach that provides satisfactory answers to why low-quality platforms end being the market winner, even when a high-quality platform is present, see Jullien (2011) or Halaburda and Yehezkel (2019). However, it is necessary to address how and why this advantage arises. Only addressing these questions we can understand the role of platforms' characteristics in cases like the example of iPhone and Windows Phone.

然而，我们可以将注意力集中在平台对信念的影响力上，而不是消费者的协调能力。这是最近引起关注的焦点优势的起点。从广义上讲，焦点是基于消费者期望的现有优势。直观地说，平台可以通过"影响"客户使其认为只有某些均衡是可能的。这种优势意味着平台以某种未明确方式向消费者传递信号，表明其他消费者也会加入该平台（参见Halaburda和Yehezkel，2019）。然而，这个概念相当普遍，并且其定义并没有解释焦点是如何以及为什么出现的。它可能是品牌、声誉、广告或其他投资的结果。从实际角度来看，平台的匹配技术也可能构成一种焦点优势。目前，这种方法的主要局限性在于它依赖于假设一个外生且模糊定义的效应来限制潜在均衡集合。例如，Halaburda和Yehezkel（2019）认为苹果（Windows Phone）之所以成功（失败）可以归因于焦点性质。苹果之所以成功，在于用户购买了新款昂贵手机即使开发者尚未开发出支持所有新功能的应用程序，但用户预期到了所有这些潜在好处。另一方面，用户和开发者对Windows手机能否吸引来自谷歌或苹果的消费者以及开发者到一个与其他平台无异的平台持怀疑态度。这种用户如何预期到所有这些潜在好处，或者开发者为什么变得怀疑并没有解释。该方法只是假设苹果相对于Windows具有外生优势。乍一看，这种方法似乎类似于"联合理性化"，因为两者都减少了均衡集合。然而，焦点依赖于假设由于平台的某些外生特征，某些均衡是不可行的，而"联合理性化"则依赖于消费者协调自己的能力。这种方法具有简单性的吸引力特点。与联合理性化相比，焦点不需要定义一个新的非合作解概念，只需根据外生标准排除一些均衡即可。迄今为止，这是一种有前途的方法，在像iPhone和Windows Phone之类的案例中提供了令人满意的答案（参见Jullien, 2011或Halaburda和Yehezkel, 2019）。然而，有必要解决这种优势是如何以及为什么产生的问题。只有回答这些问题，我们才能理解平台特征在像iPhone和Windows Phone的例子中的作用。

Another intuitively appealing way to overcome the coordination problem is the "Divide and Conquer
(DC)" strategy, which was also proposed by Caillaud and Jullien (2001) and Evans (2003b). […] [One way to get both sides on board is] to obtain a critical mass of users on one side of the market by giving them the service for free or even paying them to take it, Evans (2003b). This strategy requires dividing the market between a profit side and a loss side to "conquer" the market. It creates an incentive to join the platform on the loss side, and given the network effects, it creates an incentive on the other side to join the platform. Nonetheless, this strategy has two immediate consequences in markets: It helps reduce barriers to entry, and it increases competition and forces one of the platforms to renounce exploiting network effects, thereby not serving one side, see Jullien (2011). Although this strategy does not completely remove the possibility of multiple equilibria, it can limit the cases in which it appears.

另一种直观而吸引人的克服协调问题的方法是"分而治之"（Divide and Conquer）策略，该策略也由Caillaud和Jullien（2001）以及Evans（2003b）提出。[一个让双方都参与其中的方法是]通过向一方提供免费服务甚至支付他们来获得市场上的关键用户群体，如Evans（2003b）所述。这种策略需要将市场分为盈利方和亏损方以"征服"市场。它创造了加入亏损方平台的动力，并且由于网络效应，它也创造了加入另一方平台的动力。然而，在市场中，这种策略有两个直接后果：它有助于降低进入壁垒，并增加竞争并迫使其中一个平台放弃利用网络效应，从而不为一方提供服务，详见Jullien（2011）。尽管这种策略并不能完全消除多重均衡的可能性，但可以限制其出现的情况。

Despite the theoretical discussion about the different ways to discriminate among equilibria, this strategy seems to be closer to real managerial practices like social networks (Facebook, Twitter, Instagram, etc.), sport apps (MyFitnessPal, Endomondo, etc.), or real state platforms. Some users have the service for free, while others pay for the service. Although intuitively appealing as a way to solve the coordination problem, there are also other problems when giving a product for free. Jullien (2005) argues that the coordination problem is mitigated but, sometimes, it is difficult or dangerous to subsidize users because it can attract users without their commitment to using the platform. This possibility creates both the adverse selection and moral hazard problems that are studied by several works, such as Armstrong and Wright (2007) and Parker and Van Alstyne (2005). In fact, Parker and Van Alstyne find that there is another problem because, sometimes, it is not clear on what side a platform should charge positive prices, which may be risky in environments with demand uncertainty, and accounting for that risk may reduce the effectiveness of the DC strategy, Jullien (2011). Therefore, the consequences can be critical because we can attract a mass of users only because there is a subsidy. One way to overcome this problem is by offering a free complementary product instead of a negative price. One example is Microsoft, it subsidizes developers by giving them the Microsoft Application Programming Interfaces (APIs) for free, which only developers value. So, there is no adverse selection problem because it attracts developers only. In that way, platforms may avoid attracting undesirable customers (free-riders that only want the subsidy), see Amelio and Jullien (2012). Therefore, bundling/tying plays a role as a coordinating device that may mitigate the multiple equilibria problem, see Jullien (2005), Parker and Van Alstyne (2005), Choi (2010), or Chao and Derdenger (2013).33
Finally, other authors argue that it is more natural to observe firms begin with a one-sided model and switch to a two-sided model as they become more established. Doing so allows potential platforms to overcome the "chicken-and-egg" problem, see Rysman (2009). Evans *et al*. (2008) argue that expectations about the ownership of control rights are essential. If users believe that a platform is going to change its strategy toward integration, it sends a message that the market is not going to fail in providing that good/service. But also, it sends a message that competition will be more aggressive on one side and, therefore, profits will be lower. Additionally, this problem is not the same for all firms, […]. The start-up problem is particularly difficult for firms that are based on multisided platforms. In addition to the usual problems faced by new firms they often must contend with the well-known chicken-and-egg problem. […] Little attention has been given to critical issues that entrepreneurs must solve to create a viable platform business, Evans (2011).

尽管有关区分均衡的不同方法的理论讨论，这种策略似乎更接近于实际的管理实践，如社交网络（Facebook、Twitter、Instagram等）、运动应用程序（MyFitnessPal、Endomondo等）或房地产平台。一些用户可以免费使用服务，而其他用户则需要付费。虽然这种解决协调问题的方式在直观上很吸引人，但提供免费产品也存在其他问题。Jullien（2005）认为，协调问题得到缓解，但有时对用户进行补贴可能是困难或危险的，因为它可能吸引没有承诺使用平台的用户。这种可能性会引发逆向选择和道德风险问题，在Armstrong和Wright（2007）以及Parker和Van Alstyne（2005）等多个研究中进行了研究。事实上，Parker和Van Alstyne发现还存在另一个问题，因为有时候不清楚平台应该在哪一方收取正价格，在需求不确定性环境中可能具有风险，并且考虑到该风险可能会减少分而治之策略的有效性[Jullien, 2011]。因此，后果可能是关键的，因为我们只是因为有补贴才能吸引大量用户。克服这个问题的一种方法是提供一个免费的补充产品，而不是负价格。一个例子是微软，它通过向开发人员提供免费的Microsoft应用程序编程接口（API），来对开发人员进行补贴，这只有开发人员才会重视。因此，没有逆向选择问题，因为它只吸引了开发人员。通过这种方式，平台可以避免吸引不受欢迎的客户（只想要补贴的搭便车者），参见Amelio和Jullien（2012）。因此，捆绑销售/绑定作为一种协调设备可能会缓解多重均衡问题[Jullien, 2005] [Parker和Van Alstyne, 2005] [Choi, 2010] [Chao和Derdenger, 2013]。
最后，其他作者认为，在企业开始采用单边模式并在成熟后转向双边模式更为自然。这样做可以让潜在平台克服“先有鸡还是先有蛋”的问题[Jullien, 2005] [Parker和Van Alstyne, 2005] [Choi, 2010] [Chao和Derdenger, 2013].33
对于基于多主体平台的企业来说，创业问题尤其困难。除了新企业通常面临的问题外，它们还必须应对众所周知的先有鸡还是先有蛋的问题[Evans, 2011]。

Additionally, in the case of digital platforms, intellectual property (IP) policies and openness of platforms have become a new promising field in which the literature can make significant contributions because the coordination problem may arise as a consequence of how IP rights are allocated. But up to the date, no work has yet analyzed the multiplicity of equilibria under this approach. Only Parker and Van Alstyne (2018) have addressed these issues but in a monopolistic framework. Finally, to outline the key works regarding network effects and coordination, Table 2 highlights the essential works.

此外，在数字平台的情况下，知识产权（IP）政策和平台的开放性已成为一个新的有前景的领域，文献可以在其中做出重要贡献，因为知识产权的分配可能导致协调问题。然而，迄今为止，还没有研究分析了这种方法下多重均衡的存在。只有Parker和Van Alstyne（2018）在垄断框架下讨论了这些问题。最后，为了概述关于网络效应和协调方面的关键作品，《表2》突出了重要作品。

## 5. Control Rights And Ownership Structure



One of the three pillars that define multisided markets are the control rights. If a company takes control of the sellers' goods to resell them to buyers, that firm is a merchant. On the contrary, if the company leaves that control to sellers and simply allows buyer and seller access to a common marketplace, that may constitute a platform. Although this differentiation between these two schemes is (more or less) clear, it gives rise to other questions: When is optimal to be a merchant or a platform? Is there something between these two schemes?

多边市场的三个支柱之一是控制权。如果一家公司掌控卖方的商品并将其转售给买方，那么该公司可以被视为商家。相反地，如果该公司将这种控制权留给卖方，并仅仅提供一个共同市场供买方和卖方进行交易，那么这可能构成一个平台。尽管这两种模式之间的区别（或多或少）是清晰的，但它引发了其他问题：何时最适合选择成为商家或平台？是否存在介于这两种模式之间的折衷方案？

A priori, it is not clear whether a company has to provide only the platform, or it has to control the intermediation too. Nonetheless, companies are living entities that can change their organization/ownership over time. Hagiu and Wright (2015) use as an example the case of Amazon and Zappos. Amazon started off as a one-sided retailer platform but, it has moved to a two-sided platform scheme. On the other hand, Zappos has gone in the opposite direction. Therefore, those structures are not immutable, and if the market conditions change, the ownership structure may change as well.

事先并不清楚一家公司是只需提供平台，还是也需要控制中介。然而，公司是活的实体，其组织/所有权随时间可变。Hagiu和Wright（2015）以亚马逊和Zappos为例。亚马逊最初是一个单边零售平台，但后来转向了双边平台模式。而Zappos则朝相反的方向发展。因此，这些结构并非固定不变的，如果市场条件发生变化，所有权结构也可能会随之改变。

In this regard, Hagiu (2007) states that the merchant mode is strictly preferred to the two-sided platform mode whenever there is a positive probability that seller expectations are unfavorable [about the platform adoption]. It is easier (cheaper) to convince sellers to sell their products outright than to affiliate to a platform and sell the products to consumers themselves, because the first option eliminates coordination issues […] there is a trade-off between the merchant mode and the two-sided platform mode […] between higher costs of managing more products and higher costs of convincing sellers to affiliate. This suggests that intermediaries, especially for new goods, will generally start under a merchant format and, as sufficient sellers become affiliated, move towards a more "open," platform mode, which is cheaper per seller and thus allows intermediaries to offer a broader variety of products, see Hagiu (2007).

据Hagiu（2007）的观点，只要存在卖家对平台采用持不利态度的积极概率，商家模式就明显优于双边平台模式。相比于让卖家加入平台并自行向消费者销售产品，直接说服卖家直接销售产品更容易（更便宜），因为前者消除了协调问题[...]商家模式和双边平台模式之间存在权衡[...]管理更多产品的成本与说服卖家加入的成本之间的权衡。这意味着中介机构，尤其是对于新商品而言，通常会以商家形式开始，并随着足够多的卖家加入而转向更“开放”的平台模式，这样每个卖家的成本更低，从而使中介机构能够提供更广泛的产品种类，请参见Hagiu（2007）。

On the other hand, from the workers' point of view, Hagiu and Wright (2015) compare the incentives of some workers to be employed by a platform as freelancers or as regular employees. They find that there is no a first-best solution. There is not a better structure than the other. There is always a trade-off between the incentives (and the risk) that people have when their salary depends only on their performance and the safety of a fixed salary. And this trade-off also impacts on the performance of the platform because the incentives to work when you have a fixed salary are different from those based on the day-to-day performance. In other words, there is no an "always better" ownership structure, either from the workers' point of view or the platforms' point of view. Recently, Hagiu and Wright (2019) consider this issue from the regulators' point of view. They address the consequences of misclassificating workers as employees when they are independent contractors, and vice versa. They find that any misclassification leads to a loss of welfare. Therefore, a nonrigorous regulator may inflict a welfare loss because of a wrong misclassification. On top of that, an additional complication is that between pure merchants and twosided markets, there is a continuum of ownership structures that depend on the allocation of control rights over the decision variables.

然而，从工人的角度来看，Hagiu和Wright（2015）对比了作为自由职业者或正式雇员被平台雇佣的一些工人的激励机制。他们得出结论，没有一个最佳解决方案。没有一种结构比另一种更好。当薪水仅依赖于绩效时，人们所面临的激励（和风险）与固定薪水的安全性之间总是存在权衡。而这种权衡也会影响到平台的表现，因为拥有固定薪水时工作的激励与基于日常绩效的激励是不同的。换句话说，无论从工人还是平台的角度来看，都不存在一个“始终更好”的所有权结构。最近，Hagiu和Wright（2019）从监管者的角度考虑了这个问题。他们探讨了将独立承包商错误分类为雇员以及将雇员错误分类为独立承包商所带来的后果。他们发现任何错误分类都会导致福利损失。因此，一个不严谨的监管者可能因错误分类而造成福利损失。此外，另一个复杂性在于，在纯商家和双边市场之间，存在一系列依赖于决策变量控制权分配的所有权结构。

As well as there are profits and non–for-profits merchants, there is a similar distinction for platforms too. In this sense, Rochet and Tirole (2003) find that non–for-profits platforms need not generate an efficient outcome because the non–for-profits platforms do not internalize the end-users' surpluses. In a similar vein, Hagiu (2004) analyzes the case of open source and proprietary platforms, and his results suggest there is a welfare trade-off between open source and proprietary platforms. A proprietary platform creates a dead-weight loss as a consequence of monopoly pricing, but an open-source platform does not internalize indirect network effects, so there is no obvious way to determine which ownership structure creates a higher level of product variety, adoption, or welfare. The preference for one or another is not justified economically in his model. In other words, there is no unambiguously superior ownership structure. There are economic trade-offs that need to be taken into account. On the contrary, Choi and Zennyo (2019) find that profit-maximizing platforms may yield a higher social surplus than open platforms with free access because proprietary platforms can use price mechanisms to incentivize consumers to change sides. Nonetheless, they argue that such a result relies heavily on their Hotelling specification.34 Economides and Katsamakas (2006) argue that, when proprietary and open-source platforms compete, the proprietary ones tend to dominate in terms of market share and profitability, a point that is also shared by Cabral (2019), but who argues that depends on the assumed homogeneity. This is a consequence of the fact that an open-source platform cannot adopt two-sided strategies because this ownership structure imposes a null price on at least one side and a nonprofit behavior, which could always be replicated by a proprietary platform.

除了盈利和非盈利商家之外，平台也存在类似的区别。Rochet和Tirole（2003）发现，非盈利平台不需要产生有效结果，因为它们无法内部化最终用户的剩余价值。Hagiu（2004）分析了开源和专有平台的情况，并得出结论：开源和专有平台之间存在福利权衡。专有平台由于垄断定价而产生死损失，但开源平台无法内部化间接网络效应，因此很难确定哪种所有权结构能够创造更高水平的产品多样性、采用率或福利。在经济模型中，并不存在一个明确优越的所有权结构。换句话说，并没有一个明确优越的所有权结构。我们需要考虑经济上的权衡。相反，Choi和Zennyo（2019）发现以盈利为目标的平台可能会产生比免费访问开放式平台更高社会剩余价值，因为专有平台可以使用价格机制来激励消费者改变立场。然而，他们认为这样的结果在很大程度上依赖于他们Hotelling规范模型。Economides和Katsamakas（2006）认为，在专有和开源平台竞争时，专有平台在市场份额和盈利能力方面往往占据主导地位，这一观点也得到了Cabral（2019）的支持，但他认为这取决于假设的同质性。这是因为开源平台无法采用双边策略，因为这种所有权结构对至少一方施加了零价格和非盈利行为的限制，而这种行为总是可以由专有平台复制。

Additionally, proprietary platforms can be organized in different ways depending on how the value created is allocated, in other words, it depends on who owns the platform. Bakos and Katsamakas (2008) study the optimal ownership structure of multisided platforms, and find that the optimal ownership is always ownership by the side that enjoys the strongest network effect from the participation of the other side. In a similar vein, Ambrus and Argenziano (2009) highlight that, sometimes, it is optimal to split monopolies into two platforms but under common ownership. The idea is to adopt second-degree price discrimination because, in that way, users coordinate by themselves (higher and lower quality lovers). However, a monopoly network without price discrimination is the most profitable strategy when there is no differentiation among agents.

此外，根据价值分配的方式，专有平台可以以不同的组织形式呈现，也就是说，这取决于平台的所有者是谁。Bakos和Katsamakas（2008）对多边平台的最佳所有权结构进行了研究，并发现最佳所有权结构始终是由享受其他一方参与所带来的最强网络效应的一方拥有。在类似的观点中，Ambrus和Argenziano（2009）指出，有时将垄断分割为两个共同拥有的平台是最优选择。其理念在于采用二度价格歧视，因为这样用户可以自行协调（高质量和低质量爱好者）。然而，在没有主体之间差异化时，没有价格歧视的垄断网络是最具盈利能力的策略。

Finally, it is common to assume that providers and clients are the two sides that the platform is linked to. However, sometimes the platform does not interact with one of those sides directly, and in other cases, one of those sides could be integrated in the platform totally or partially. The first case implies a disconnection with the network effects on one side, which raises a new concern, the interfirm price coordination. Kind *et al*. (2016) address this issue and find that platforms face two conflicting needs: the need for intrafirm coordination (internalization of network effects) and the need for interfirm price coordination (internalization of the competitive pressure). When products become more homogeneous, competition raises because the interfirm price coordination dominates intrafirm coordination. Thus, platforms prefer letting an independent firm set prices on one side to reduce competition between platforms on that side. Although this situation could lead to a cartel-like outcome in one-sided markets, it may not be the case in two-sided ones because the interfirm coordination prevents intrafirm price coordination. However, their model is rather specific, and it focuses on the TV distribution schema. It is still unknown whether or not those results hold in more general settings.

最后，我们通常认为提供者和客户是平台所连接的两个方面。然而，有时平台并不直接与其中一方互动，而在其他情况下，其中一方可能完全或部分地融入平台。第一种情况意味着与网络效应的一方断开连接，这引发了一个新问题：企业间价格协调。Kind等人（2016）解决了这个问题，并发现平台面临两种相互冲突的需求：企业内部协调的需求（内部化网络效应）和企业间价格协调的需求（内部化竞争压力）。当产品变得更加同质化时，竞争加剧，因为企业间价格协调主导了企业内部协调。因此，平台更倾向于让独立公司在一方设定价格，以减少平台之间在该方面的竞争。尽管这种情况可能导致单边市场上类似卡特尔的结果，在双边市场上可能并非如此，因为企业间协调阻止了企业内部价格协调。然而，他们的模型比较具体，并且专注于电视分销模式。目前还不清楚这些结果是否适用于更普遍的设置中。

The second case represents an example of vertical integration, which is quite common in digital markets. For example, Netflix offers both own films and series along with a platform for third-party films and series. Vertical integration eliminates the double marginalization problem, as it happens in one-sided markets, and it may also lead to a better internalization of externalities, see Jullien and Sand- Zantman (2019). However, integration may lead to own content bias, but the internalization of consumers' decisions on the other side generates a countervailing effect that promotes a larger variety. For instance, Nocke *et al*. (2007) find that if the platform integrates some agents on one side and later excludes some potential entrants on that side, that is detrimental to welfare when network effects are weak, but welfareenhancing if network effects are strong. Therefore, the effect of vertical integration is ambiguous in two-sided markets, see De Corniere and Taylor (2014). In the end, platforms face a trade-off between maximizing its long-run value and short-run profits through the integration, see Jullien and Sand-Zantman (2019).

第二个案例是数字市场中垂直整合的一个典型例子。例如，Netflix既提供自家制作的电影和系列剧，又提供第三方电影和系列剧的平台。垂直整合消除了单边市场中的双重边际化问题，并可能更好地内部化外部性（参见Jullien和Sand-Zantman，2019）。然而，整合可能导致自身内容偏见，但消费者决策的内部化产生了一个相抵消的效应，促进了更大的多样性。例如，Nocke等人（2007）发现，在网络效应较弱时，如果平台在一方面整合了一些主体，并在后来排除了该方面的一些潜在进入者，则对福利有害；但在网络效应较强时，则有益于福利。因此，在双边市场上，垂直整合的效果是不确定的（参见De Corniere和Taylor，2014）。最终，平台面临着通过整合来最大化其长期价值和短期利润之间的权衡（参见Jullien和Sand-Zantman，2019）。

As a summary, there is a continuum of ownership structures between platforms and merchants that are underexplored. The literature has focused on extreme cases, and it has shown that there is a lot of ambiguity. Nonetheless, there is a lot of work to be done in this area, especially, on the allocation of IP, and the different integrated/disintegrated structures that may be plausible. Finally, to outline the key works regarding property rights, Table 2 highlights the essential works.

总结起来，平台和商家之间存在着一系列的所有权结构，这方面的研究还未得到充分探索。现有文献主要关注极端情况，并且显示出存在很多模糊性。然而，在这个领域还有很多工作需要完成，特别是在知识产权的分配以及可能合理的不同整合/解体结构方面。最后，为了概述与产权相关的关键作品，表2突出了重要作品。

## 6. Market Structure And Competition Policy



Do platforms tend to become natural monopolies over time? Should platforms be left under current regulation and ex post antitrust scrutiny, or they require new regulations and procedures? Currently, these two questions have attracted the attention of both scholars and practitioners alike. This open debate has given rise to a rich body of literature but an exhaustive analysis of the whole literature around these two topics deserves a specific literature review. However, in the following sections, we provide a general view of the current debate on these issues. In the first section, we address the incumbententrant relationship and the practices that have raised the concern of public authorities, such as exclusive contracts. In the second section, we make a quick review of the common and specific areas of literature in multisided markets regarding competition policy, and we illustrate the current debate on the application of competition policy in multisided markets.

随着时间的推移，平台是否趋向于形成自然垄断？对于平台，是应该继续受到现行监管和事后反垄断审查的限制，还是需要制定新的规定和程序？这两个问题目前引起了学者和从业者的广泛关注。这场公开辩论已经产生了大量文献，但对于围绕这两个主题的整体文献进行详尽分析是必要的。然而，在接下来的章节中，我们将提供对当前关于这些问题辩论的总体观点。在第一节中，我们将探讨现有企业与新进入者之间的关系以及引起公共机构担忧的做法，例如独家合同。在第二节中，我们将快速回顾多边市场竞争政策领域中普遍存在和特定领域内文献，并阐述当前关于在多边市场应用竞争政策方面进行辩论情况。

[重写后的译文:]

## 6.1 Entry The Market And Tipping. The Winner Takes All?



A common myth about multisided platforms is that markets tend to become monopolies as a consequence of the network effects. Nowadays, this thought has become popular because of the rise of social networks, such as Facebook, Twitter, or LinkedIn. However, there is no clear evidence supporting this line of thought. In fact, there are examples in the opposite direction, such as Uber versus Lyft, Uber Eats versus Just Eat, or Deliveroo versus Glovo. A general perception is that, because of network effects, incumbency advantage creates some barriers to entry that make monopolies more likely. Jullien and Sand-Zantman (2019) point out that three elements prevent a market with network effects from being a natural monopoly: the existence of stand-alone value, the possibility of multihoming, and the existence of compatibility. On top of that, they highlight that dynamic competition considerations may contribute to weakening incumbency advantage. The prospective benefits of gaining future incumbency advantage for a superior quality entrant are larger than the prospective benefits of the lower quality incumbent. Hence, a forward-looking entrant may be willing to sacrifice more in the current competition, thus, forcing the incumbent to sacrifice all their profits to keep its position, see Caillaud and Jullien (2003).

多主体平台存在一个常见的误解，即由于网络效应的影响，市场往往会形成垄断。如今，随着社交网络（如Facebook、Twitter或LinkedIn）的兴起，这种观点变得流行起来。然而，并没有明确的证据支持这一观点。事实上，存在相反的例子，比如Uber与Lyft、Uber Eats与Just Eat以及Deliveroo与Glovo之间的竞争。一般认为，由于网络效应的存在，现有企业具有优势地位，在进入市场方面存在一些壁垒，从而使垄断更有可能发生。Jullien和Sand-Zantman（2019）指出了三个因素阻止了具有网络效应的市场成为自然垄断：独立价值的存在、多重归属性和兼容性的存在。此外，他们强调动态竞争考虑因素可能有助于削弱现有企业优势地位。对于一个质量更高的新进入者来说，获得未来优势地位所带来的潜在利益大于现有低质量企业所带来的潜在利益。因此，一个具有前瞻性眼光的新进入者可能愿意在当前竞争中做出更多牺牲，从而迫使现有企业牺牲所有利润来保持其地位（Caillaud和Jullien，2003）。

In this sense, White and Weyl (2016) state that the owner of a better technology must have two preconditions to replace an incumbent and to avoid a failure in the launching. First, the platform must be sufficiently well capitalized to finance subsidies to consumers. Second, it must be sophisticated enough to manage consumers' coordination. In that sense, three elements that create incentives to enter and isolate the influence of competitors are differentiation, compatibility, and segmentation, see Jullien (2005) and Belleflamme and Toulemonde (2004). Additionally, Jullien (2011) highlights that market typology also matters. In pure intermediation markets, barriers to entry are more likely than when platforms offer some value beyond the connectivity to a network. In this respect, Caillaud and Jullien (2003) raise an interesting question: To what extent will established firms use exclusivity to deter entry?

根据White和Weyl（2016）的观点，拥有更先进技术的企业要想取代现有企业并避免失败，必须满足两个前提条件。首先，平台必须具备足够的资本来为消费者提供补贴。其次，平台必须足够复杂以管理消费者的协调。在这方面，差异化、兼容性和分割是创造进入市场并隔离竞争影响的三个关键因素（参见Jullien，2005；Belleflamme和Toulemonde，2004）。此外，Jullien（2011）强调市场类型也是重要因素。在纯粹的中介市场中，进入壁垒比平台除了连接网络之外还提供其他价值时更有可能存在。在这方面，Caillaud和Jullien（2003）提出了一个有趣的问题：已建立企业将何以利用独家权来阻止竞争对手进入？

[注意：重写后的文本保留了原文内容，并进行了适当修改以使其更流畅，并符合学术风格。]

Exclusive dealing has long been a controversial practice under the antitrust law, and multisided literature is not an exception. Intuitively, exclusive contracts may be used to protect monopoly power and exclude potential competitors, see Doganoglu and Wright (2006). For example, it may be used to mitigate multihoming by forcing customers to choose one platform, which may lead to monopolization, see Armstrong and Wright (2007). Jullien and Sand-Zantman (2019) conclude that, although exclusivity could be exclusionary, it raises less concern in the case of platforms. Even without efficiency gains, exclusivity may not be motivated by the exclusion of competitors but rather by the maximization of profits. But exclusive contracts also have implications for consumers on all sides. Belleflamme *et al*. (2020) review recent works on exclusivity, and they highlight that when platforms find profitable to impose exclusivity, it damages at least one side.

独家交易长期以来一直是反垄断法下备受争议的做法，多边文献也不例外。从直观上看，独家合同可能被用来保护垄断权力并排斥潜在竞争对手（Doganoglu和Wright，2006）。例如，通过强迫客户选择一个平台来减轻多重归属问题，这可能导致垄断化（Armstrong和Wright，2007）。Jullien和Sand-Zantman（2019）得出结论，在平台的情况下，尽管独家权可能具有排斥性质，但引起的担忧较少。即使没有效率收益，独家合同也可能不是为了排除竞争对手而是为了利润最大化。然而，独家合同对所有方面的消费者也有影响。Belleflamme等人（2020）回顾了关于独家性的最新作品，并强调当平台发现强制实行独占性有利可图时，至少会损害一方。

In a similar vein, Carroni *et al*. (2019) study whether the presence of an agent that generates large externalities on the other side (a superstar) may also convince agents on the same side to stop multihoming and join the platform exclusively. Because more agents singlehome on the superstar side, that attracts more demand, which attracts more agents on the superstar side, and so on. But gaining exclusivity with the superstar is costly, and they find that platforms only consider exclusivity when the competition is strong on the opposite side of the superstar. Surprisingly, this exclusivity may benefit agents despite that it may lead to a monopoly market. Although superstar exclusivity increases welfare relative to its absence, some agents are worse-off, for example, singlehoming consumers on the platform without the superstar. Nonetheless, the overall effect is an increase in welfare because the superstar induces some agents to enter the market.

在同样的思路下，Carroni等人（2019）研究了一个产生巨大外部性影响的主体（超级明星）是否能够说服同一方的主体停止多重归属并独家加入平台。由于更多的主体选择在超级明星一侧进行单一归属，这吸引了更多需求，进而吸引了更多超级明星一侧的主体，如此循环。然而，与超级明星达成独家合作是有成本的。他们发现只有在超级明星相反一侧竞争激烈时，平台才会考虑独家合作。令人惊讶的是，尽管这种独占可能导致垄断市场，但它可能使主体受益。虽然相对于没有超级明星时，超级明星的独占性增加了福利，但某些主体变得更差劲，例如没有超级明星的平台上进行单一归属消费者。然而总体效果是福利增加，因为超级明星促使某些主体进入市场。

But, under which circumstances can we expect exclusive contracts? Caillaud and Jullien (2003)
provide the first answer by pointing out that such contracts depend on the quality of the matching technology of the incumbent w.r.t. the entrant. Hogendorn and Ka Yat Yuen (2009) use a Cournot model and highlight that the must-have component providers will prefer to sign an exclusivity contract when compatibility is low, and the size assymetry in terms of market share between platforms is high, and Carroni *et al*. (2019) expect such exclusivity when differentiation is low.

然而，在哪些情况下我们可以预期出现独家合同呢？Caillaud和Jullien（2003）通过指出这样的合同取决于现有者与新进者之间的匹配技术质量，给出了第一个答案。Hogendorn和Ka Yat Yuen（2009）使用了Cournot模型，并强调当兼容性较低、平台之间市场份额的大小不对称较高时，必备组件供应商将更倾向于签订独家合同。Carroni等人（2019）预计在差异化较低的情况下会出现这种独占性。

More generally, platforms can make strategic investments to deter entry, exclusive dealing could be a specific case in which platforms invest in creating lock-in, but there may other potential deterring investments. Farhi and Hagiu (2008) adapt Fudenberg and Tirole's typology of strategic interactions to multisided markets to study how those interactions may influence the market structure. We can have four strategies based on the effects of investment on the strategic variable (prices or quantities) and the relationship among these strategic variables (whether they are strategic complements or substitutes). Intuitively, an investment that reduces an incumbent's marginal cost can only hurt the entrant and benefit the incumbent. But what the authors prove is that, in a multisided market, a cost-reducing investment by one firm can both increase the profits of its rivals and be desirable for the firm undertaking the investment
[…]. The set of strategic configurations in a two-sided market is strictly larger than in a one-sided market, Farhi and Hagiu (2008). Therefore, other strategies that deter entry in one-sided markets may not have the same effects on multisided markets, which opens the door to the careful application of traditional insights.

更一般地说，平台可以通过战略性投资来阻止竞争对手进入市场。独家交易可能是平台投资于创建锁定效应的一个特例，但也可能存在其他潜在的阻止投资。Farhi和Hagiu（2008）将Fudenberg和Tirole关于战略互动的分类方法应用于多边市场，以研究这些互动如何影响市场结构。根据投资对战略变量（价格或数量）的影响以及这些战略变量之间的关系（它们是战略互补还是替代品），我们可以有四种策略。直观地说，降低现有者边际成本的投资只会损害新进者并使现有者受益。但作者证明了，在多边市场中，一个公司通过降低成本进行的投资既可以增加其竞争对手的利润，也对承担该投资的公司有利[...]. 在双边市场中，战略配置集合严格大于单边市场中的集合（Farhi和Hagiu, 2008）。因此，在单边市场上阻止进入所采取的其他策略可能不会对多边市场产生相同效果，这为传统观点的谨慎应用打开了大门。

Nonetheless, most of the analysis so far comes from the difficulty for a newcomer to overcome the incumbent position in "traditional cases." But there are other factors to take into account, for example, backward compatibility or data usage. Many digital platforms are built on top of other previous platforms or technologies. In this sense, a critical question is to what extent backward compatibility may influence the market equilibrium. To the best of our knowledge, there is only one work that addresses this topic despite its relevance. Tremblay (2017) finds that when an entrant and the incumbent with backward compatibility have the same technology, the incumbent will drive the entrant out of the market. However, if the entrant has a technology advantage, three scenarios are possible. Either the incumbent sets low prices to deter entry, or the entrant has superior technology and sets prices with mark-up, or the incumbent is expelled from the market. Concerning data usage, past consumption may allow platforms to reduce search costs for consumers, creating a new incumbency advantage.35 Therefore, policies aiming at data portability may influence incumbency advantage and competition, but so far, the impact of data portability on platform competition is an open question that is starting to be addressed. To the best of our knowledge, the closest work in addressing this issue is Lam (2017). She finds that the strategy of lowering prices on one side is not only due to network externalities or consumer's characteristics but also due to switching costs and the dynamic nature of the model. She argues that switching costs could be procompetitive in some circumstances. Therefore, policies aimed at facilitating switching, such as data portability, may end up limiting competition.

然而，迄今为止的大部分分析都集中在新进入者在“传统案例”中克服现有地位的困难上。然而，还有其他因素需要考虑，例如向后兼容性或数据使用。许多数字平台是建立在其他先前平台或技术之上的。在这个意义上，一个关键问题是向后兼容性对市场均衡的影响程度。据我们所知，尽管与其相关性相比只有一项研究涉及这个主题。Tremblay（2017）发现当新进入者和具有向后兼容性的现有者拥有相同技术时，现有者将驱逐新进入者离开市场。然而，如果新进入者具备技术优势，则可能出现三种情况。要么现有者降低价格以阻止进入，要么新进入者拥有更优越的技术并设置带溢价的价格，要么现有者被驱逐出市场。关于数据使用方面，过去的消费可能使平台能够降低消费者搜索成本，并创造一种新的地位优势。因此，旨在实现数据可移植性的政策可能会影响地位优势和竞争力, 但迄今为止，数据可移植性对平台竞争的影响是一个尚未解决的问题。据我们所知，最接近解决这个问题的工作是Lam（2017）的研究。她发现，在某些情况下，降低一方价格的策略不仅取决于网络外部性或消费者特征，还取决于转换成本和模型的动态性质。她认为，在某些情况下，转换成本可能具有促进竞争的作用。因此，旨在促进转换（如数据可移植性）的政策可能最终限制竞争。

## 6.2 Competition Policy And Antitrust Literature Of Multisided Markets



A fundamental issue for competition policy nowadays comes from the lack of proper competitive benchmark for activities involving large demand externalities, such as network effects. Without demand externalities, the perfect competition provides the normative benchmark, but with demand externalities, prices may not reflect costs, and costs may not internalize the effect on other consumers' decisions. For instance, Kind *et al*. (2008) show that platforms might over- or underinternalize indirect network effects, which depends on the relation between the average indirect network effect and the marginal indirect network effect, and the platform only accounts for the latter in its pricing decision. This does not mean that traditional analysis never applies to platforms, but that we should be cautious, see Jullien and Sand- Zantman (2019).

如今，竞争政策面临一个根本性问题，即在涉及大规模需求外部性（如网络效应）的活动中缺乏适当的竞争基准。在没有需求外部性的情况下，完全竞争提供了规范性基准；然而，在存在需求外部性的情况下，价格可能无法反映成本，成本也可能无法内化对其他消费者决策的影响。例如，Kind等人（2008）指出平台可能会过度或不足地内化间接网络效应，这取决于平均间接网络效应与边际间接网络效应之间的关系；而平台在定价决策中仅考虑了后者。这并不意味着传统分析从不适用于平台，而是我们需要谨慎对待（参见Jullien和Sand-Zantman，2019）。

There is a growing interest in how competition authorities have to address multisided platforms because, in some cases, it is possible to find optimal prices below marginal costs, socially optimal monopolies, competitive tying/bundling, etc, see Filistrucchi *et al*. (2013). In this section, we do not try to make an exhaustive analysis of the development of the antitrust policies regarding multisided markets, but to present another field that is attracting the attention of researchers. More exhaustive analyses can be found in some of the cited papers.36
Evans (2002) points out that it is essential to consider network effects in the antitrust analysis because they create externalities that make the one-sided analysis no longer suitable. This is a broadly shared opinion among scholars who consider that relying on one-sided logic may lead to mistakes, see Filistrucchi *et al*. (2013), Goos *et al*. (2011), or Lam (2017). For example, the identification of market power may not be related to the markup over cost. In the traditional analysis of oligopoly, market power is identified by a large markup over cost. But […] platforms may exhibit strong price skewness with some sides being charged low or zero prices and others being charged relatively high prices. That implies that observing a high markup on one side […] need not reflect strong market power, see Jullien and Sand- Zantman (2019). Additionally, market power is a capacity and not a behavior. Platforms have multiple sources of revenue and may choose not to exploit their market power on one side. Thus, authorities have to choose between defining a common market for both sides, or separate markets for each side. Depending on the choice made, the consequences for antitrust enforcement may differ significantly, as we explain later in this section.

由于多边平台存在一些情况下可能出现低于边际成本的最优价格、社会最优垄断、竞争性捆绑等现象，因此竞争当局如何应对这些问题引起了越来越多的关注（Filistrucchi等人，2013）。本节中，我们并不试图对多边市场的反垄断政策发展进行详尽分析，而是介绍另一个吸引研究者注意的领域。更详尽的分析可以在一些引用文献中找到（36）。

Evans（2002）指出，在反垄断分析中考虑网络效应是至关重要的，因为它们产生了使单边分析不再适用的外部性。这是学者们广泛共享的观点之一，他们认为依赖单边逻辑可能会导致错误（Filistrucchi等人，2013；Goos等人，2011；Lam，2017）。例如，在传统寡头市场分析中，通过大幅超过成本来确定市场力量。然而[...]平台可能表现出价格严重倾斜, 一些方面收取低价或零价, 而其他方面则收取相对较高价格。这意味着观察到一方面的高溢价[...]不一定反映出强大的市场力量（Jullien和Sand-Zantman，2019）。此外，市场力量是一种能力而不是行为。平台有多个收入来源，并可能选择不在一方面利用其市场力量。因此，当局必须在为双方定义一个共同市场或为每一方定义单独的市场之间做出选择。根据所做的选择，反垄断执法的后果可能会有很大差异，我们将在本节后面解释。

Following those ideas, the first contributions in the literature developed extensions of traditional one-sided tests to address the multisided nature of platforms. One of the first is Filistrucchi (2008), who proposes a modification of the SSNIP test to identify the relevant market in two-sided markets. Filistrucchi highlights the complexity of adapting this one-sided tool to two-sided markets. In a two-sided market, the profits of the hypothetical monopolist are determined by both, the price level and the price structure. It is not a priori clear whether the hypothetical monopolist should be thought of as raising:

在这些理念的基础上，文献中的首批贡献是对传统单边测试进行扩展，以应对平台多边性的特点。其中一项最早的贡献是Filistrucchi（2008）提出了一种修改SSNIP测试的方法，以确定双边市场中相关的市场。Filistrucchi强调了将这种单边工具适应于双边市场的复杂性。在双边市场中，假设垄断者的利润由价格水平和价格结构共同决定。目前尚不清楚是否应该将假设垄断者视为提高价格：

(1) *the price level while optimally adjusting the price structure*.
(2) *both prices together keeping fixed the price structure*. (3) *each of the two prices separately allowing the other price to be adjusted optimally*.
(4) *each of the two prices while keeping the other price fixed*.
Answering these questions requires using Filistrucchi's taxonomy of two-sided markets (see Section 2.1). In a "payment card" market, the hypothetical monopolist would increase the price level and optimally adjust the price structure. In a "media" market, that is not true, and the hypothetical monopolist would increase each one of the two prices separately while optimally adjusting the price structure. However, Evans and Noel (2008) also distinguish between short- and long-term effects of the price increase, but Filistrucchi does not think in that way, who states: the distinction is probably useless from a practical point of view in the case of SSNIP test, see Filistrucchi (2008).

回答这些问题需要使用Filistrucchi对双边市场的分类（详见第2.1节）。在“支付卡”市场中，假设垄断者将提高价格水平，并对价格结构进行最优调整。而在“媒体”市场中，情况则不同，假设垄断者将分别提高两种价格，并对价格结构进行最优调整。然而，Evans和Noel（2008）还区分了价格增加的短期和长期效应，但Filistrucchi认为这种区分在SSNIP测试中可能是无用的（参见Filistrucchi，2008年）。

Filistrucchi also highlights that nontransaction markets tend to be more complicated than transaction markets. Nontransaction markets require a more extensive analysis of which feedbacks we should take into account. On the other hand, the profits in transaction markets come from the transactions, in which all the externalities are included. Following this idea, Filistrucchi and Klein (2013) point out that, if we study a nontransaction market, it has to be considered as two interrelated markets. Whereas in payment card markets, we have to define only one market because in these markets there is a basic service (the transaction) that is linking both markets.37 Contemporaneously to Filistrucchi's work, Evans and Noel
(2008) propose a two-sided framework for the Critical Loss Analysis and SSNIP test, and they find that:

Filistrucchi还指出，非交易市场比交易市场更为复杂。对于非交易市场，我们需要进行更加全面的分析，以确定应考虑哪些反馈因素。而交易市场的利润来自于交易本身，其中包含了所有的外部性。基于这一观点，Filistrucchi和Klein（2013）指出，如果我们研究一个非交易市场，就必须将其视为两个相互关联的市场。而在支付卡市场中，我们只需要定义一个市场，因为这些市场中存在着一个基本服务（即交易），它将两个市场联系在一起。与Filistrucchi的研究同时进行的Evans和Noel（2008）提出了一个双边框架用于关键损失分析和SSNIP测试，并得出以下结论：

(1) the bigger the network effects, the larger the biases.
(2) one-sided approaches underestimate merger effects.38
Other interesting works that have contributed to extending traditional one-sided tests are Weyl (2010), that proposes an extension of his model to measure the market power and to evaluate predation; Behringer and Filistrucchi (2015) that extend the Areeda-Turner rule to two-sided markets; and White and Weyl (2016), who make recommendations about estimating discrete choice models and upward pricing pressure (UPP) tests.

（1）网络效应越大，偏差就越明显。
（2）单边方法低估了合并效应。38
其他有趣的研究对传统的单边测试进行了扩展。例如，Weyl（2010）提出了对其模型的扩展，以衡量市场力量和评估掠夺行为；Behringer和Filistrucchi（2015）将Areeda-Turner规则扩展到双边市场；White和Weyl（2016）则提出了关于离散选择模型和上升定价压力（UPP）测试的估计建议。

Apart from modifying one-sided tests to address the multisided nature of platforms, another two topics that have attracted the attention of scholars are market collusion and bundling/tying.39 With regard to market collusion, only a few works have explicitly addressed it, such as Ruhmer (2010). Collusion in two-sided markets is more complex and harder to detect because collusion may occur on all prices, but sometimes only on prices on one side, and the characteristic price skewness may favor colluding on one side only. However, network effects make collusion harder to sustain too. For example, Ruhmer (2010) finds that the higher the network effect, the harder to collude in repeated games with a grim trigger strategy. But when collusion is possible, its consequences vary depending on whether or not some consumers multihome. With singlehoming, all consumers are hurt, but when multihoming on one side leads to monopoly prices on that side, collusion has no effect on them; or if collusion occurs on only one side, prices on both sides react in opposite directions, which imply that some consumers may benefit from collusion, see also Correia-da Silva *et al*. (2019). Another interesting related work is Boffa and Filistrucchi (2014). They argue that there is a similarity between collusion in two-sided markets and collusion in one-sided markets with complementarities. They find that in some cases, it may be profitable for the cartel to set quantity levels lower than monopoly levels. When platforms cannot coordinate on the monopoly outcome, the cartel can coordinate on pseudo-competitive outcomes, thus, raising the cost of deviation from the equilibrium. More recently, Lefouili and Pinho (2020) have shown that collusion in two-sided markets may harm some consumers but benefit others.

除了修改单边测试以应对平台的多边性质之外，还有两个引起学者关注的主题是市场勾结和捆绑销售。关于市场勾结，只有少数几项研究明确涉及到，例如Ruhmer（2010）。双边市场中的勾结更加复杂且更难检测，因为勾结可能发生在所有价格上，但有时只发生在一方的价格上，并且特征性的价格偏斜可能会偏向于仅在一方进行勾结。然而，网络效应也使得勾结更难维持。例如，Ruhmer（2010）发现，在采用严厉触发策略的重复博弈中，网络效应越大，则越难以进行勾结。但是当存在可能进行勾结时，其后果取决于消费者是否同时使用多个平台。如果只使用一个平台，则所有消费者都会受到伤害；但是当一方同时使用多个平台导致该方面出现垄断定价时，则勾结对其没有影响；或者如果只在一方面发生了勾结，则两个方面的价格会呈相反方向变化，这意味着某些消费者可能从中受益（参见Correia-da Silva等人，2019）。另一个有趣的相关研究是Boffa和Filistrucchi（2014）。他们认为，在双边市场中的勾结与具有互补性的单边市场中的勾结存在相似之处。他们发现，在某些情况下，对于卡特尔来说，将数量水平设定为低于垄断水平可能是有利可图的。当平台无法在垄断结果上进行协调时，卡特尔可以在伪竞争结果上进行协调，从而提高偏离均衡状态的成本。最近，Lefouili和Pinho（2020）表明，在双边市场中进行勾结可能会对一些消费者造成损害，但对其他消费者造成利益。

Concerning bundling/tying, the motivations for bundling/tying in multisided markets differ from the usual ones in classical markets, and also the consequences. For example, in classical markets, these strategies have been used as a tool to price discriminate and hence extract consumer surplus more efficiently; or to deter entry in both the tied and the tying good's market, see Affeldt (2011). In contrast, Farhi and Hagiu (2008) and Affeldt (2011) find that tying is unlikely a barrier to entry because tying platforms in multisided markets have an incentive to compete *softly*. After all, it could be profitable for both incumbent and entrant. In multisided markets, tying allows platforms to perform a better balancing between sides, which may increase social welfare, Rochet and Tirole (2008). In this regard, Choi (2010) studies the tying strategy and finds that the effect on welfare depends on the relative strength of externalities and the level of differentiation. This ambiguous result in terms of welfare is also found by Amelio and Jullien (2012). In general, in welfare terms, tying has ambiguous effects, and it depends on parameter values and whether or not some customers multihome. Lastly, another common intuition from classical markets is that bundling/tying can serve as price discrimination tools and thus help firms to extract more consumer surplus. The welfare effects of bundling and tying in classical markets as a price discrimination tool are ambiguous. They increase producer surplus as they are adopted as a profitmaximizing strategy, but the effects on consumers are not a priori clear though. Chao and Derdenger (2013) find that, in multisided markets, the motivation to price discriminate is consistent in both market structures, but the consequences are different. For instance, it is also true that bundling provides the platform an additional instrument to extract consumer surplus, but the overall welfare increases because prices on both sides of the market are lower.

关于捆绑销售/捆绑销售，在多边市场中的动机和后果与传统市场有所不同。在传统市场中，这些策略被用作定价歧视的工具，以更有效地提取消费者剩余；或者用于阻止捆绑商品和被捆绑商品市场的进入（Affeldt，2011）。相比之下，Farhi和Hagiu（2008）以及Affeldt（2011）发现，在多边市场中，捆绑销售不太可能成为进入壁垒，因为多边市场中的平台有竞争“软性”的激励。毕竟，对于现有企业和新进企业来说都可能是有利可图的。在多边市场上，捆绑销售使平台能够更好地平衡各方利益，从而增加社会福利（Rochet and Tirole, 2008）。在这方面, Choi (2010) 研究了捆绑策略并发现其对福利的影响取决于外部性和差异化水平之间相对强度。Amelio 和 Jullien (2012) 也发现了关于福利方面模糊的结果。总体而言，在福利方面，捆绑销售的效果是模糊的，这取决于参数值和消费者是否同时使用多个平台。最后，从传统市场中得出的另一个常见观点是，捆绑销售可以作为定价歧视工具，并帮助企业提取更多的消费者剩余。在传统市场中，捆绑销售和捆绑销售作为定价歧视工具对福利的影响是模糊的。它们作为一种利润最大化策略而增加了生产者剩余，但对消费者的影响不明确（Chao and Derdenger, 2013）。在多边市场中，定价歧视动机在两种市场结构中都是一致的，但后果却不同。例如, 捆绑销售也提供了平台提取消费者剩余的额外手段, 但整体福利增加了因为市场两侧价格都降低了。

Jullien and Sand-Zantman (2019) point out that we should also pay attention to new concerns that are specific to platforms, for example, the net neutrality debate.40 The evidence is unclear, and different authors have found a rationale for both regimes. For example, Njoroge *et al*. (2013) argue that the nonneutral regime is the best option for consumers and content providers, and it also leads to higher social welfare. On the other hand, Economides and Tåg (2012) find that indirect network effects provide a rationale for network neutrality regulation, but only for some parameter values. In the duopoly case, they find that platforms prefer the neutrality regime, but the opposite is true in the monopoly case. From a theoretical point of view, it is not clear whether or not the neutral regime is better than the nonneutral regime. Therefore, there is room for further research. Additionally, given the FCC's decision of revoking net neutrality in the United States, there is an opportunity to empirically address the consequences of such a decision.

Jullien和Sand-Zantman（2019）指出，我们还应关注特定于平台的新问题，例如网络中立性辩论。然而，对于这一问题的证据并不明确，不同的研究者对于两种制度都找到了合理性。例如，Njoroge等人（2013）认为非中立制度是消费者和内容提供商的最佳选择，并且还导致更高的社会福利。然而，Economides和Tåg（2012）发现间接网络效应为网络中立性监管提供了合理性，但仅适用于某些参数值。在垄断情况下，他们发现平台更倾向于采用中立制度，但在寡头垄断情况下则相反。从理论角度来看，目前尚不清楚中立制度是否比非中立制度更优。因此，有必要进行进一步研究。此外，鉴于美国联邦通信委员会废除网络中立性的决定，我们有机会从实证角度探讨这一决定所带来的后果。

Nonetheless, the use of multisided literature in antitrust cases and public policy is not exempt from critics. There are two open issues already: the definition of multisided platforms and the role of nonprice competition. As we have pointed out in Section 2, there is no consensus on how to define a multisided platform. Therefore, there is no consensus on how to address the relevant market or how to evaluate competitive harm. Although our proposal of Section 2 may be a first step in identifying multisidedness and addressing these issues, it relies on relevant implicit assumptions that limit its use. In this regard, it is important to realize that "multi-sidedness," as described in this work, is a static, demand-side view of platform competition, which fulfills a specific need in competition policy but that falls short if we want to define platforms for other purposes, such as for innovation policy. In this case, it would be relevant to take into account the governance of the ecosystem. For example, the governance influences the effective competition within the sides, which, if excessive, may lead to further contractualizing the relationship moving away from the canonical platform market to a supply-chain one.41 Concerning nonprice competition, a common feature of multisided markets is gratuity, which generates difficulty for antitrust analysis. Gratuity raises the level of complexity because of the locus of competition shifts from prices to the nonprice competition, an area in which no well-established measure of quality is available, which implies a need to go case-by-case. On top of that, such a gratuity tends to raise privacy concerns, which adds a further complexity because, in some instances, privacy may be a strategic variable that public authorities must take into account, see Casadesus-Masanell and Hervas-Drane (2015).

然而，多主体文献在反垄断案件和公共政策中的应用并未得到全面认可。目前存在两个尚未解决的问题：多主体平台的定义和非价格竞争的作用。正如我们在第2节中所指出的，对于如何定义多主体平台并没有达成一致意见。因此，在确定相关市场或评估竞争危害方面也没有共识。尽管我们在第2节提出的建议可能是确定多主体性和解决这些问题的第一步，但它依赖于相关隐含假设，从而限制了其适用范围。在这方面，需要认识到本研究所描述的“多主体性”是从静态、需求端视角来看待平台竞争，并且仅适用于竞争政策中特定需求的描述，但如果我们想要为创新政策等其他目标来定义平台，则存在局限性。在这种情况下，考虑到生态系统治理是非常重要的。例如，治理方式会影响各方之间有效竞争的程度，在某些情况下可能会过度合约化关系，并将其从典型的平台市场转变为供应链市场41. 关于非价格竞争，多边市场的一个共同特征是免费赠送，这给反垄断分析带来了困难。免费赠送提高了复杂性，因为竞争的焦点从价格转向非价格竞争，而在这个领域中没有确立的质量衡量标准可用，这意味着需要根据具体情况进行逐案处理。此外，这种免费赠送往往引发隐私问题，这增加了进一步的复杂性，因为在某些情况下，隐私可能是公共当局必须考虑的战略变量，请参见Casadesus-Masanell和Hervas-Drane（2015）。

Another interesting question that has attracted attention recently is the interrelationship between the sides. Could it be that the interrelationship is not different than the importance of complementarities in a simple single-sided market? As Wright and Yun (2019) point out, these concerns lead to a competition between two schools of thought. The first school claims that platforms should be addressed in a similar way as traditional single-sided markets. The core justification is that the two sides are not interchangeable, and they do not include the same participants sometimes. Therefore, each side of the market should be considered as a separate market but interrelated with the other markets or sides by complementarities. The other school of thought claims that platforms cannot be considered without taking into account all sides. This school argues that "the relevant market must be sufficiently broad that, if it were monopolized, the monopolist would be able to exercise market power profitably." They use Google as an example. It would be an error to consider the online search tool in isolation because Google is not profit maximizing with respect to the online search tool only.

最近引起关注的另一个有趣问题是各方之间的相互关系。这种相互关系是否与简单的单边市场中互补性的重要性没有区别？正如Wright和Yun（2019）所指出的，这些问题引发了两种思想流派之间的竞争。第一种观点认为，应该像处理传统单边市场一样来处理平台。其核心理由是两个方面不可替代，并且有时并不包括相同的参与者。因此，市场的每一方面都应被视为一个独立市场，但通过互补性与其他市场或方面相关联。另一种思想流派认为，在考虑平台时不能忽视所有方面。这个学派认为，“相关市场必须足够广泛，以至于如果垄断了该市场，垄断者将能够有利可图地行使市场权力。”他们以谷歌为例进行论证。仅仅考虑在线搜索工具是错误的，因为谷歌在利润最大化上并不仅限于在线搜索工具。

The recent decision on the Ohio versus American Express case in the United States has pointed out how vivid this debate is because of the divergences between the criteria of the district court and the Second Circuit. Two essential works to understand this conflict are Wright and Yun (2019) and Katz (2019b). The first work supports a more flexible use of multisided theory, and the second one supports a more limited use.

美国最近关于俄亥俄州诉美国运通案的裁决，凸显了地方法院和第二巡回法院之间标准的分歧，这使得这场辩论变得更加激烈。要深入理解这一冲突，有两部重要著作值得参考：Wright和Yun（2019）以及Katz（2019b）。前者支持对多边理论进行更灵活的运用，而后者则主张对其使用进行更为有限制。

Wright and Yun (2019) argue that we cannot justify paying attention to the prices on one side of the transaction only. However, Katz (2019b) argues that we cannot consider the "transaction" as the unit over which competition occurs because relevant markets are defined as a collection of products that are sufficiently close substitutes. The services offered to each side are not substitutes. Nonetheless, other authors argue that the complementarities between both sides are akin to the left and right shoes. Katz (2019b) argues that this argument lacks to point out that both sides have different interests that may not be aligned.

Wright和Yun（2019）认为，仅关注交易一方的价格是不合理的。然而，Katz（2019b）指出，我们不能将“交易”作为竞争发生的单位，因为相关市场被定义为一系列足够接近替代品的产品。提供给双方的服务并非替代品。尽管如此，其他学者认为双方之间的互补性就像左右鞋子一样。Katz（2019b）认为这个论点没有指出双方有不同的利益可能不会保持一致。

The practical implication of this debate is that it affects the allocation of the burdens of proof between the plaintiff and the defendant. The first school that claims that the indirect network effects should not be considered out-of-market efficiencies, and therefore, any "prima facie" antitrust assessment of competitive harm must incorporate the impact on all sides. The second school does not support this view.

这场辩论的实际影响在于它对原告和被告之间的证明责任分配产生了影响。第一派认为间接网络效应不应被视为市场外效益，因此，在对竞争伤害进行“初步”反垄断评估时，必须考虑其对各方的影响。然而，第二派对此观点持不支持态度。

## 7. Future Directions



We acknowledge that this is a vibrating and fast-pacing field that generates new evidence each year. However, there are areas in which the multisided literature has open questions. For example, a relevant issue that deserves exploration is competition in nonprice features, as Jullien and Sand-Zantman (2019)
or Foros *et al*. (2015) point out. This is a relatively unexplored area that deserves more attention given its potential impact on how we understand platform competition. One recent example is Parker and Van Alstyne (2018). They focus on studying how a monopolist platform should set its IP policies. They consider that such policies depend on two parameters: the openness degree and the length of the exclusivity period awarded to developers to exploit their innovations. This nonprice approach is promising, and the first results point out that non-price features play an essential role in how platforms set their control rights. However, the evidence is quite scarce when we consider oligopolistic settings, and it can be considered unexplored yet.42 Privacy is another notorious nonprice dimension that is relevant in the competition analysis on the Internet. Casadesus-Masanell and Hervas-Drane (2015) analyze this case by considering the privacy policy as a quality parameter used by homogeneous platforms to compete. They find a rationale for a vertical differentiation scheme in which platforms set different levels of privacy disclosure. In general, the research on nonprice competition is currently an unexplored area that deserves more attention given that it influences from prices to coordinating issues, as Veiga *et al*. (2017) show.

我们承认这是一个充满活力且快节奏的领域，每年都会产生新的证据。然而，在多边文献中存在一些未解决的问题。例如，Jullien和Sand-Zantman（2019）或Foros等人（2015）指出了一个值得探索的相关问题，即非价格特征上的竞争。这是一个相对未被开发的领域，在我们理解平台竞争方式方面具有潜在影响，因此值得更多关注。Parker和Van Alstyne（2018）提供了一个最近的例子。他们专注于研究垄断平台应该如何制定其知识产权政策。他们认为这些政策取决于两个参数：开放程度和授予开发者利用其创新进行独占期限的长度。这种非价格方法很有前景，并且初步结果表明非价格特征在平台设定其控制权方面起着重要作用。然而，在考虑寡头垄断设置时，证据相当有限，可以说尚未被充分开发[42]。隐私是互联网竞争分析中另一个显著的非价格维度。Casadesus-Masanell和Hervas-Drane（2015）通过将隐私政策视为同质平台用于竞争的质量参数来分析这个案例。他们发现垂直差异方案的合理性，其中平台设置不同水平的隐私披露。总体而言，非价格竞争研究目前是一个未被充分开发的领域，值得更多关注，因为它影响从价格到协调问题，正如Veiga等人（2017）所展示的那样。

Two other areas of great relevance for public authorities that are yet underexplored are acquisitions of start-up technologies by big companies and the impact of Big Data. On the one hand, these acquisitions normally do not meet the requirements to lead to traditional merger analysis, and the frequent acquisitions by the "Big Five" (Amazon, Apple, Facebook, Google, and Microsoft) have raised concerns about the persistent and increasing market power of some of those firms. To this date, there is some early theoretical evidence that calls for more intervention of antitrust authorities, but this evidence is scarce and does not take a multisided approach.

公共机构尚未充分开发的两个与其相关性极高的领域是大公司对初创技术的收购和大数据的影响。一方面，这些收购通常不符合传统合并分析的要求，而“五巨头”（亚马逊、苹果、Facebook、谷歌和微软）频繁进行的收购引发了人们对其中一些公司持续增长的市场力量的担忧。迄今为止，虽然有一些早期理论证据呼吁反垄断机构更多地介入，但这些证据仍然稀缺，并且没有采用多边方法。

Motta and Peitz (2020) propose a simple model with two companies in which one company is the big incumbent, and the other one is a small start-up that has an innovative but risky project. They find that mergers are only procompetitive if, without the acquisition, the start-up is unable to pursue its project. As a recommendation, the authors suggest that the burden of proof that the merger is procompetitive should be placed on the merging firms in contrast with current practice. In the same spirit, Bryan and Hovenkamp (2020) show that, given the prospects of acquisition, startups incentive to innovate would be based on the leaders' agenda, which may be inefficient and leads to monopolies. They argue in favor of interventions (compulsory licensing) in situations where a highly dominant incumbent acquires a startup whose technology could plausibly influence competition if rivals are excluded from using it. Although interesting, these results rely on one-sided approaches, and it is yet unknown to what extent these results hold if, for example, the start-up operates on several platforms. In this regard, a new wave of works on multisided platforms focused on the effects of the strategic behavior of agents on the sides is needed. How will a likely-to-be-acquired start-up invest resources when multihoming? How that influences platform competition? Will start-ups compete to be acquired? How? To this date, all those questions are open.

Motta和Peitz（2020）提出了一个简单的模型，其中包括两家公司，一家是大型现有企业，另一家是具有创新但风险较高项目的小型初创企业。他们的研究发现，只有在没有收购的情况下，初创企业无法推进其项目时，合并才能促进竞争。作者建议将证明合并对竞争有促进作用的责任放在合并公司身上，与当前做法相反。在同样的精神下，Bryan和Hovenkamp（2020）表明，在考虑到收购前景的情况下，初创企业创新动力将基于领导者的议程，这可能是低效且导致垄断的。他们主张在高度占主导地位的现有企业收购一家技术可能对竞争产生影响（如果排除竞争对手使用该技术）的初创企业时进行干预（强制许可）。尽管这些结果很有趣，但它们依赖于单方面方法，并且尚不清楚如果例如初创企业在多个平台上运营时这些结果能够得以保持到什么程度。因此需要进行新一轮关于多边平台上主体战略行为对各方影响的研究。当初创企业可能被收购时，它们将如何投资资源？这将如何影响平台竞争？初创企业会竞相被收购吗？如何竞争？迄今为止，所有这些问题都没有答案。

On the other hand, a related issue is the use of data on digital platforms. Some authors have raised concerns because of the idea that the amount of data that platforms gather can create market power beyond the market they operate. Katz (2019a) reviews the literature on big data and antitrust policy and highlights five potential areas that raise concerns: the impact on rivals' costs, predatory conducts, mergers, price discrimination, and privacy. In general, Katz concludes that with the current tools, many of the potential negative effects of data cannot be detected. For example, is a platform limiting their APIs because data are key to the competitor's success, or is it because of privacy concerns? Privacy is a part of the product offering, and therefore, part of the nonprice competition dimension. A related work is Condorelli and Padilla (2020). They analyze the risks of privacy policy tying. This policy requests users to grant consent so that the platform can combine the data users generate when using multiple services.

另一方面，与此相关的问题是数字平台上数据的使用。一些作者对此表示担忧，因为他们认为平台收集的大量数据可能会在其所经营的市场之外创造超越市场的市场力量。Katz（2019a）对大数据和反垄断政策的文献进行了回顾，并强调了引发担忧的五个潜在领域：对竞争对手成本的影响、掠夺行为、合并、价格歧视和隐私。总体而言，Katz得出结论称，在当前工具下，许多数据潜在负面影响无法被检测到。例如，一个平台限制其API是否是因为数据对竞争对手的成功至关重要，还是因为隐私问题？隐私是产品提供中的一部分，因此也是非价格竞争维度的一部分。Condorelli和Padilla（2020）进行了相关研究，他们分析了隐私政策捆绑带来的风险。该政策要求用户授权以便平台可以将用户在使用多个服务时生成的数据进行组合。

They identify both procompetitive and anticompetitive effects, but it is not clear which one dominates and when, and it is a topic that is currently open in the multisided literature.

他们确定了既有促进竞争又有反竞争效应，但目前尚不清楚哪种效应占主导地位以及何时出现，这是多边文献中一个当前尚未解决的课题。

Lastly, an interesting area that is yet to explore is the interrelation between IP and competition laws.

最后，一个有趣且尚未探索的领域是知识产权和竞争法之间的相互关系。

Antitrust law aims to promote competition and static welfare. In contrast, IP law permits static welfare losses in exchange for dynamic welfare gains, see Blair *et al*. (2020). Thus, there is an apparent trade-off between both approaches that is of key relevance for public authorities. In recent years, the European Commission has devoted significant resources to The European Digital Strategy,43 which aims for fostering *a trusting, lawful, and innovation-driven online platforms' environment in the EU*. Thus, there is an urgent need to take into account both approaches because innovation policies influence competition, which is also influenced by competition policy. To avoid unnecessary conflicts between policy objectives, it is necessary an integrative framework.

反垄断法的目标是促进竞争和静态福利。相比之下，知识产权法则允许在获得动态福利的同时产生静态福利损失（Blair等人，2020）。因此，这两种方法之间存在明显的权衡，对于公共当局来说具有重要意义。近年来，欧洲委员会已经投入了大量资源到《欧洲数字战略》中，该战略旨在在欧盟内部营造一个信任、合法和创新驱动的在线平台环境。因此，迫切需要考虑这两种方法，因为创新政策影响竞争，而竞争政策也受到竞争的影响。为了避免政策目标之间的不必要冲突，需要一个综合框架。

## 8. Conclusions



In the last decade, multisided platforms have become a popular topic as a consequence of the emergence of platforms, such as Facebook or Google. However, since the early 2000s, this business model has attracted the attention of many scholars because it seems to defy some of the cornerstone intuitions about markets, such as price below marginal costs denoting predation. In this work, we provide an introduction to the theoretical literature to new readers and an overall view of the current state of this literature to experienced researchers. In that sense, the first question we address is what characteristics these multisided platforms have. We discuss the most relevant contributions in defining a multisided platform, and we identify three essential elements: multiproduct nature, presence of network effects, a specific allocation of control rights. We review how the literature has evolved in considering each one of these features, and how the vast majority of the definitions lacks some essential element, which has led to the current situation in which there is no standard definition. Their identification can be tricky because there is no industry of platforms that allow us to group them all. In this regard, several taxonomies have been proposed depending on specific interests (managerial, competition policy, etc.) but it is a relatively underxplored area. Once we characterized platforms and their typologies, we address why platforms are relevant by pointing out differences with respect to traditional market models.

在过去的十年中，由于Facebook或Google等平台的出现，多边平台已成为一个热门话题。然而，自2000年代初以来，这种商业模式吸引了许多学者的关注，因为它似乎违背了市场的一些基本直觉，比如价格低于边际成本意味着掠夺。在本文中，我们向新读者介绍理论文献，并向经验丰富的研究人员提供对当前文献状况的整体观点。在这方面，我们首先探讨了多边平台具有哪些特征。我们讨论了定义多边平台最相关的贡献，并确定了三个基本要素：多产品性质、网络效应存在和特定控制权分配。我们回顾了文献是如何在考虑每一个特征方面发展的，并且发现大部分定义都缺少一些基本要素，导致目前没有标准定义。由于没有一个平台产业可以将所有平台归类起来，因此它们的识别可能会有难度。在这方面，根据具体利益（管理、竞争政策等），提出了几种分类法，但这是一个相对未被充分开发的领域。一旦我们对平台及其类型进行了描述，我们将解释为什么平台是相关的，并指出与传统市场模型相比的差异。

One of the most recurrent differences is the price structure of multisided platforms, which have attracted the vast majority of the attention. In Section 3, we address the source of those differences. We start by describing the most robust result on comparative statics in the literature, the "Seesaw principle." In other words, factors leading the platform to choose higher participation on side "i" lead it to choose lower participation on side "j," see Weyl (2010). This principle is the source of many divergences with respect to traditional price structure. Nonetheless, the Lerner principles also hold, which leads us to study which other factors that influence price elasticities have been considered in the literature, such as multihoming, information management, taxation, or beliefs. With respect to multihoming, we first address the incentive to do it, and we show recent evidence that highlights that prices on both sides move in opposite directions.

多边平台的价格结构是最常见的差异之一，也是受到广泛关注的方面。在第三部分中，我们探讨了这些差异的根源。我们首先介绍了文献中最为稳健的比较静态结果，即“跷跷板原理”。简而言之，导致平台在一侧选择更高参与度的因素会导致其在另一侧选择较低参与度，详见Weyl（2010）。这个原理是许多与传统价格结构不同之处的根源。尽管如此，Lerner原则仍然适用，这促使我们研究了文献中考虑到的其他影响价格弹性的因素，例如多重归属、信息管理、税收或信念。关于多重归属，我们首先探讨了其动机，并展示了最近的证据表明两侧价格呈相反方向变动。

Another essential factor that influences price structure is the available information for both, platforms and customers. On the one hand, platforms set different prices depending on how customers form their beliefs. The larger the market power, the more likely platforms prefer facing informed agents. On the other hand, sometimes is the platform, which is uncertain about the externalities that each side exerts on the other. In this case, current literature provides a rationale for introductory prices. There are two external factors that have been widely studied that also influence price structure: taxation and customers' behavior. Taxation in multisided markets creates quite surprising effects, such as increasing the number of affiliates on both sides, or inverting the asymmetric price structure, or even changing the political views of newspapers. Lastly, customer's behavior is quite an increasing research branch that little by little is gaining the attention of economists because provides different explanations for the asymmetric price structure.

另一个影响价格结构的重要因素是平台和客户之间可获得的信息。一方面，平台根据客户形成信念的方式设定不同的价格。市场力量越大，平台越倾向于面对了解情况的主体。另一方面，有时平台对每一方对另一方施加的外部性存在不确定性。在这种情况下，现有文献提供了介绍性价格的理由。此外，还有两个广泛研究并且也影响价格结构的外部因素：税收和客户行为。多边市场中的税收会产生令人惊讶的效果，例如增加两侧关联方数量、颠倒非对称价格结构，甚至改变报纸政治观点。最后，客户行为是一个逐渐引起经济学家关注并且不断发展研究领域，因为它提供了关于非对称价格结构不同解释的可能性。

In Section 4, we address one of the main concerns in the literature: the coordination problem of attracting two or more different types of users that need each other in some way, also known as "the chicken & egg problem." This coordination issue derives from the presence of indirect network effects, which create a feedback loop. Consumers' decisions about whether or not joining a platform are not isolated from other consumers' decisions. This situation leads to the possibility of multiple equilibria, which implies uncertainty about the market outcome. There is no universal way to deal with the chicken and egg problem in the multisided literature, and there have been proposed different approaches. One of the earliest and most popular is based on expectations or beliefs. If the participation of one group depends on the participation of another group, an intuitive and direct way to solve the problem is by paying attention to how those groups believe the other group will behave. However, it is a risky bet to focus on consumers' ability to coordinate among themselves only. Different timings have been proposed as a way of mitigating those coordination problems, but it only mitigates the problem partially. A more satisfactory way of dealing with this problem is the "insulating tariff" proposed by Weyl (2010). The intuitive idea is that coordination emerges not because of consumers having some intrinsic ability to coordinate themselves, but because platforms give them a dominant strategy to do so. These tariffs "insulate" consumers from participation on the other side by providing them a "fixed" utility level. Another way of dealing with the coordination problem is the idea that platforms can influence consumers' beliefs by creating "focal platforms." Focality broadly refers to an incumbency advantage based on consumers' expectations. This advantage implies that when several equilibria are possible, platforms have some kind of advantage that signals consumers that those platforms will attract other consumers, which reduces the potential set of equilibria. Although promising, this approach still does not explain how or why such an advantage emerges.

在第4节中，我们解决了文献中的一个主要问题：吸引两种或更多不同类型的相互需要的用户之间的协调问题，也被称为“鸡和蛋问题”。这个协调问题源于间接网络效应的存在，它创建了一个反馈循环。消费者对是否加入平台的决策并不是孤立于其他消费者的决策。这种情况导致可能存在多个均衡点，这意味着市场结果存在不确定性。在多边文献中，并没有一种通用方法来处理鸡和蛋问题，并且已经提出了不同的方法。最早和最流行的方法之一是基于期望或信念。如果一个群体参与取决于另一个群体的参与，解决该问题直观而直接的方式是关注这些群体如何相信另一个群体会行动。然而，仅仅关注消费者之间协调能力是一种有风险的赌注。已经提出了不同时间安排作为缓解这些协调问题的方式，但只能部分缓解该问题。更令人满意地处理此问题的方式是Weyl（2010）提出的“隔离关税”概念。直观地说，协调的出现不是因为消费者具有某种固有的协调能力，而是因为平台给予他们一种主导策略来实现协调。这些关税通过提供“固定”的效用水平来“隔离”消费者免于参与另一方。处理协调问题的另一种方式是平台可以通过创建“焦点平台”来影响消费者的信念。焦点广泛指基于消费者期望的优势地位。这种优势意味着当存在多个均衡点时，平台具有某种优势，向消费者传递信号表明这些平台将吸引其他消费者，从而减少潜在均衡集合。尽管有希望，但这种方法仍然无法解释此类优势如何或为何出现。

However, many of the current multisided platforms that we know today were born as one-sided platforms, and they evolved toward multisided platforms over time. This may be another way of dealing with the chicken and egg problem, but it relates to a fundamental point to describe multisided platforms: the allocation of control rights. In Section 5, we analyze the branch of the literature that has focused on comparing different allocations of control rights in multisided platforms, for example, between merchants and platforms, or between open source and proprietary platforms. In the first case, the literature agrees that the merchant mode is strictly preferred to the two-sided platform mode whenever there is a positive probability that seller expectations are unfavorable about the platform adoption. It is easier to convince sellers to sell their products outright than to affiliate with a platform. However, a key conclusion is that there is no an "always better" ownership structure. With regard to open or proprietary platforms, the current evidence shows that a proprietary platform creates a dead-weight loss as a consequence of monopoly pricing, but an open-source platform does not internalize indirect network effects, which implies that there is always a trade-off between the ownership structures. Lastly, the literature has also addressed whether or not one of the sides should control the platform, or whether or not the platform should directly interact with one of the sides. Nowadays, the evidence supports the idea that platforms have to be created by those who benefit the most from attracting the other side, but the evidence in this area is scarce. Similarly, the current and scarce evidence highlights that vertical integration has ambiguous effects in multisided markets, but also that there is a trade-off between the need for intrafirm coordination (internalization of network effects) and interfirm price coordination (internalization of the competitive pressure).

然而，我们今天所熟知的许多多边平台最初都是单边平台，随着时间的推移逐渐演变成为多边平台。这可能是解决鸡生蛋问题的另一种方式，但它涉及到描述多边平台的一个基本观点：控制权的分配。在第5节中，我们对专注于比较多边平台中不同控制权分配的文献进行了分析，例如商家和平台之间、开源和专有平台之间的比较。在第一种情况下，文献普遍认为只要存在卖方对于采用该平台持不利预期的正概率，商家模式严格优于双边平台模式。说服卖方直接销售产品比加入一个平台更容易。然而，一个关键结论是没有一种“总是更好”的所有权结构。关于开放或专有平台，目前的证据显示专有平台由于垄断定价而产生死损失，但开源平台没有内部化间接网络效应，这意味着在所有权结构之间总是存在权衡。最后，文献还讨论了其中一方是否应该控制该平台以及该平台是否应直接与其中一方互动等问题。目前的证据支持这样一个观点：那些从吸引另一方获益最多的人必须创建平台，但在这个领域的证据很少。同样，目前和稀缺的证据强调垂直整合在多边市场中具有模糊的影响，但也存在着内部化网络效应（企业内协调）和内部化竞争压力（企业间价格协调）之间的权衡。

In Section 6, we address two topics: the possibility of monopolization or tipping by platforms, and the main lines of the research in competition policy and antitrust in multisided markets. In the first case, the idea that multisided platforms tend to monopolization is more a myth than a reality. In general, three elements prevent a market with network effects from being a natural monopoly: the existence of standalone value, the possibility of multihoming, and the existence of compatibility. Another common myth is related to exclusive dealing, which has long been a controversial practice under the antitrust law, and multisided literature is not an exception. Intuitively, exclusive contracts may be used to protect monopoly power, but the current evidence highlights that, in multisided markets, it raises fewer concerns. In the second case, we address the current issues of addressing antitrust policies from a multisided perspective. We continue highlighting some areas in which the evidence is scarce, such as collusion or mergers, and we conclude by presenting the current debate on how to address the relevant market or how to evaluate competitive harm. Finally, we conclude in Section 7 by describing some of the most promising areas of research, such as nonprice competition or the new challenges of competition policy in the digital economy. These areas represent the forefront of the multisided platforms literature, and the results so far show that this literature has yet a lot to offer, and many questions remain open.

在第6节中，我们探讨了两个主题：平台的垄断或倾斜可能性，以及多边市场中竞争政策和反垄断研究的主要方向。就第一种情况而言，多边平台倾向于垄断的观点更多是一种神话而非现实。总体而言，有三个因素阻止具有网络效应的市场成为自然垄断：独立价值的存在、多重归属的可能性和兼容性的存在。另一个常见的神话与排他交易有关，在反托拉斯法下长期存在争议，而多边文献也不例外。直观上看，排他合同可能被用来保护垄断权力，但目前的证据表明，在多边市场中引起的担忧较少。在第二种情况下，我们从多边视角探讨了解决反托拉斯政策当前问题。我们继续强调一些证据稀缺的领域，如勾结或合并，并最后介绍了关于如何解决相关市场或如何评估竞争伤害的当前辩论。最后，在第7节中描述了一些最具潜力的研究领域，例如非价格竞争或数字经济中竞争政策的新挑战。这些领域代表了多边平台文献的前沿，迄今为止的结果显示，这个领域仍有很多可以探索的内容，许多问题仍然待解决。

## Acknowledgments



We are grateful to the editor, Iris Claus, and two anonymous reviewers for their careful reading and providing numerous suggestions that have significantly improved the paper.

我们感谢编辑Iris Claus以及两位匿名审稿人的仔细阅读和提供了许多建议，这些建议极大地改进了本文。

## Notes



1. In this work, we refer to two-sided platforms, two-sided markets, multisided markets, and multisided
platforms as synonyms. We know that this is not true. However, for simplicity's sake, we keep the same language from the original authors.
2. This term was first used in Rochet and Tirole (2003). However, these models had been studied before
by Parker and Van Alstyne (2000), Caillaud and Jullien (2001), and Caillaud and Jullien (2003). In the last two works, they refer to the platforms as "cibermediaries." For some authors, the literature was born when the term "two-sided market" is coined. To others, it is when the first paper with interdependent demands between two markets was published. In this regard, the birth is attributed to Parker and Van Alstyne.
3. It depends on the relation between the average indirect network effect and the marginal indirect
network effect, see Kind *et al*. (2008).
4. Other examples of these definitions are those of Kumar *et al*. (2010) and Amelio and Jullien (2012). 5. Other similar cases are Wright (2004), Cabral (2019), or Affeldt (2011). 6. What is even more interesting is the link between their definition and the Coase Theorem. In the
previous example, couples can negotiate how to divide the price of the tickets. A nightclub in which only couples go would be a one-sided platform. In the credit card market, sellers and buyers cannot coordinate themselves to reallocate their prices, so the Coase Theorem fails. Therefore, the failure of the Coase Theorem is a necessary condition.
7. This literal interpretation has sparked a fruitful discussion about the difference among multisided
markets that we address in Section 2.1.
8. Weyl (2010) argues similarly to Rochet and Tirole (2006). He highlights three conditions that must
be met to consider adopting a two-sided approach. The failure of any of these conditions makes simpler and better understood other models: There is a multiproduct firm, there are network effects, and there is bilateral market power. However, as it has been previously stated, these conditions miss the one regarding the control of essential terms of the interaction by the end-users.
9. Other authors have considered similar definitions, such as Song (2013) or Filistrucchi *et al*. (2013).
The latter also makes an interesting comparison between the Rochet and Tirole's (2006) and Evans's (2003a) definitions.
10. In Filistrucchi *et al*. (2010), we find an example of ambiguity between Evans' and Rochet and
Tirole's definitions.
11. See Rochet and Tirole (2006) or Weyl (2010) for other specific cases that break the multisidedness. 12. The current debate about public intervention in this context is symptomatic of this. As Jullien and

## 致谢

我们衷心感谢Iris Claus编辑以及两位匿名审稿人的仔细阅读和宝贵建议，这些建议极大地改进了本文。

## 注释

1. 在本研究中，我们将双边平台、双边市场、多边市场和多边平台视为同义词。尽管我们知道这并不准确，但出于简单起见，我们保留了原始作者使用的相同语言。
2. 这个术语最早出现在Rochet和Tirole（2003）的论文中。然而，在此之前，Parker和Van Alstyne（2000）、Caillaud和Jullien（2001）以及Caillaud和Jullien（2003）已经对这些模型进行了研究。在后两篇论文中，他们将平台称为“网络媒介”。对于一些作者来说，当术语“双边市场”被创造出来时，该领域的文献才开始产生。而对于其他人来说，则是当第一篇涉及两个市场之间相互依赖需求的论文发表时。在这方面，归功于Parker和Van Alstyne。
3. 这取决于平均间接网络效应与边际间接网络效应之间的关系，请参见Kind等人（2008）的研究。
4. 其他对这些定义的例子包括Kumar等人（2010）和Amelio和Jullien（2012）的研究。
5. 其他类似的案例包括Wright（2004）、Cabral（2019）或Affeldt（2011）的研究。
6. 更有趣的是，这些定义与科斯定理之间存在联系。在前面的例子中，夫妻可以协商如何分配门票价格。只有夫妻去的夜总会是一个单边平台。在信用卡市场上，卖家和买家无法协调自己来重新分配价格，因此科斯定理失效了。因此，科斯定理失效是一个必要条件。
7. 这种字面解释引发了关于多边市场之间差异的富有成果的讨论，我们将在第2.1节中进行详细探讨。
8. Weyl（2010）与Rochet和Tirole（2006）提出了类似观点。他们强调采用双边方法必须满足三个条件：存在多产品公司、存在网络效应以及存在双边市场力量。然而，正如前面所述，这些条件忽略了关于最终用户对交互关键条款控制权的重要条件。
9. 其他作者也提出了类似定义，例如Song（2013）或Filistrucchi等人（2013）的研究。后者还对Rochet和Tirole（2006）与Evans（2003a）的定义进行了有趣的比较。
10. 在Filistrucchi等人（2010）的研究中，我们可以找到Evans和Rochet与Tirole定义之间存在歧义的例子。
11. 请参见Rochet和Tirole（2006）或Weyl（2010）的研究，以了解其他打破多边性的具体案例。
12. 当前关于公共干预在这一背景下的讨论正是这种情况的症结所在。正如Jullien和

Sand-Zantman (2019) point out, the mere presence of network effects does not call for specific interventions, but it is its relative strength, which calls for different approaches. In the same spirit, Hagiu and Wright (2015) highlight that between multisided platforms and resellers, there is a
continuum of potential business models, which further emphasizes that, in reality, we could observe several degrees of multisidedness that may require different interventions. Thus, an open question is to determine which degree of multisidedness is necessary to call for specific public intervention.
13. In Section 6.2, we address the relevance and current discussion around this topic. 14. Even a monopoly may set prices under marginal costs, see Caillaud and Jullien (2001), Caillaud and
Jullien (2003), or Schiff (2003).
15. Optimality will call for subsidies, […] and one should subsidize more the less profitable side of the
market, Jullien (2005).
16. A wider and more general view of platform differentiation from an empirical point of view can be
found in Cennamo and Santalo (2013).
17. Later, Weyl (2010) states that the Seesaw principle was the most robust result on comparative statics
of two-sided markets, but he argues that the notion of "price" is unclear, and he reformulates it as follows. Factors leading the platform to choose higher participation on side "i" lead it to choose
lower participation on side "j."
18. That does not imply that other areas have not been addressed or their insights are not trustful,
but that there have not attracted the same level of attention. Many other factors influence price structure, as Wright (2004) pointed out, intuitions derived from classical models may not apply to multisided markets, which implies that those factors that influence pricing on classical models should be reviewed under a multisided perspective. In this sense, the multisided market literature progresses steadily, and an exhaustive analysis of all those works is as unattainable as an exhaustive review of all the industrial organization literature.
19. Evans (2011) considers that it is common to find singlehoming consumers and multihoming advertisers.
20. In this case, Jullien (2005) warns that multihoming drives competition toward transaction fees. With
multihoming, agents try to concentrate their activity on the low transaction fee platforms.
21. Although we focus on pricing in this section, multihoming also influences other variables. Ambrus
et al. (2016) show that advertising levels do not depend on whether the market is a monopoly or a duopoly when viewers multihome.
22. This market failure is unambiguous only if there are no intragroup externalities on the multihoming side.
23. Lastly, another possible strategy to deal with the supposed monopoly prices of multihoming is to
commit a certain level of prices in advance. That is the case addressed by Hagiu (2006). He analyzes four market structures with combinations of multihoming and price commitments, and he finds that price commitment is always a dominant strategy for platforms.
24. Belleflamme *et al*. (forthcoming) review recent works on price transparency, and they highlight
that competing platforms prefer opaqueness. In fact, tipping becomes more likely when competing platforms disclose information.
25. See Belleflamme and Toulemonde (2018) for a short review of this topic. 26. Other interesting works in this area are Bourreau *et al*. (2018), Kind *et al*. (2010), and Tremblay
(2018).
27. The Spence distortion arises because the platform internalizes network effects to marginal rather than
average participating agents. This distortion was pointed out for the first time by Wright (2004), and it was also analyzed by Kind *et al*. (2008), but it is Weyl (2010) who coined the term.
28. This same idea can be found in Kind *et al*. (2008). Although the models are different, the basic
feature of that the incomplete internalization of indirect network effects (Spence distortion) may counteract the market power distortion (possibly even leading to too high quantities in equilibrium) is already part of their work.
29. When there are two dimensions of heterogeneity, even fixing the size on the other side and the price
on the side considered, many types of users could be just on the margin between participating and not. Some may have high interaction benefits but large membership costs, and others may have low interaction benefits and no membership cost.
30. Other examples of models in which we find that platforms set allocations of users are Kind *et al*.
(2008), Kind *et al*. (2009), or Kind and Koethenbuerger (2018).
31. The notion of focality is equivalent to "favorable beliefs" as Caillaud and Jullien (2001) and Caillaud
and Jullien (2003) coined. See Halaburda and Yehezkel (2019) for an introduction to several degrees of focality.
32. We would like to thank one of the anonymous reviewers for pointing out this limiting feature. 33. Or it may also lead to more efficient outcomes, see Affeldt (2011). 34. The Hotelling model assumes a perfect negative correlation between tastes. This assumption heavily
influences some results, see Ambrus *et al*. (2016).
35. This idea is found in Halaburda and Yehezkel (2019), who use this example to motivate the focality
advantage. See Section 4.
36. Some interesting reviews about the antitrust issues in two-sided markets are Filistrucchi *et al*. (2013),
Filistrucchi *et al*. (2012), Filistrucchi and Klein (2013), and Jullien and Sand-Zantman (2019).
37. From a theoretical point of view, it is worth mentioning Alexandrov *et al*. (2011). Their model has
no network effects. However, there are cross-side effects that arise from shortages, so both sides are interdependent as we expect in two-sided markets, but they are not truly two-sided platforms. What is interesting about this work is that it is necessary to take into account the relationship between both sides, even in markets beyond the canonical definition of two-sided markets/platforms. Some of their results are common to those found by Filistrucchi.
38. It is worth mentioning that this result is not found by Chandra and Collard-Wexler (2009) when
analyzing the Canadian newspaper industry.
39. We acknowledge that there are other interesting topics for public authorities, such as mergers.
However, the literature on those areas is still in its infancy due to the difficulty of modeling multiplatform competition. Nonetheless, some of the lessons that already emerge are: (i) increase in prices following a merge may not hold, (ii) singlehoming or multihoming behaviors may change the consequence of merging, and (iii) as merging platforms involve different populations on each side, conflicting interest may arise. See Foros *et al*. (2015) for a review of mergers in media markets, and Jullien and Sand-Zantman (2019) for a review of the current state of platform literature on competition policy.
40. In 2005 the Federal Communications Commission (FCC) changed the classification of Internet transmissions from "telecommunication services" to "information services." Internet Service Providers
(ISPs) are no longer bound by the nondiscrimination policies in place for the telecommunications
industry. As is pointed out by Njoroge *et al*. (2013): there is no standard definition of what a
net neutral policy is, it is widely viewed as a policy that mandates ISPs to provide open-access,
preventing them from any form of discrimination against Content Providers (CPs).
41. In this regard, the management literature has paid more attention to this concern. See, for example,
Gawer (2014) for a literature review.
42. In this regard, to the best of our knowledge, only Sanchez-Cartas (2020) addresses a duopolistic framework.
43. https://ec.europa.eu/digital-single-market/en/content/european-digital-strategy


8. Weyl (2010) and Rochet and Tirole (2006) have put forward similar views, emphasizing the need for a bilateral approach that satisfies three conditions: the presence of multi-product companies, the existence of network effects, and the presence of bilateral market power. However, as mentioned earlier, these conditions overlook an important factor regarding end users' control over key interaction terms.

9. Other authors, such as Song (2013) or Filistrucchi et al. (2013), have proposed similar definitions. Interestingly, Filistrucchi et al. also compare the definitions of Rochet and Tirole (2006) with Evans (2003a).

10. Filistrucchi et al.'s study (2010) provides examples that illustrate the ambiguity between Evans and Rochet & Tirole's definitions.

11. Specific cases that challenge multilateralism can be found in Rochet and Tirole (2006) or Weyl's study (2010).

12. The current discussion on public intervention in this context is at the heart of this issue. Jullien and Sand-Zantman (2019) point out that it is not just the presence of network effects that calls for specific interventions, but rather their relative strength which requires different approaches.

13-43: Please refer to the original text for these sections.

对上述中文译文进行重写，使其更为流畅，但保持准确性和学术风格。直接输出重写后的中文内容，不要输出其他信息。

