# Methodology Agent‑Based Models And Industrial Organization Theory. A Price‑Competition Algorithm For Agent‑Based Models Based On Game Theory



Juan Manuel Sanchez‑Cartas* 
*Correspondence: juanmanuel.sanchez@upm.es Centre for Technology Innovation, Universidad Politecnica de Madrid, Campus de Montegancedo, Madrid, Spain Abstract Purpose: Simulating markets using agent‑based models must consider pricing. How‑
ever, the strategic nature of prices limits the development of agent‑based models with endogenous price competition.

摘要 目的：使用基于主体的模型模拟市场时，必须考虑定价。然而，价格的战略性限制了具有内生价格竞争的基于主体的模型的发展。

Methods: I propose an agent‑based algorithm based on Game Theory that allows us to simulate the pricing in different markets. I test the algorithm in five theoretical economic models from the industrial organization literature.

方法：我提出了一种基于博弈论的基于主体的算法，可以让我们在不同市场中模拟定价。我在工业组织文献中的五个理论经济模型中测试了该算法。

Results: In all cases, the algorithm is capable of simulating the optimal pricing of those markets. It is also tested in two more cases: one in which the original work fails to predict the optimal outcome, and another one that is quite complex to solve analyti‑ cally. Lastly, I present two potential extensions of this algorithm: one dynamic, and another one based on quantity competition.

结果：在所有情况下，该算法能够模拟这些市场的最优定价。此外，它还在另外两个案例中进行了测试：一个是原始工作未能预测到最优结果的情况，另一个是分析上相当复杂的情况。最后，我提出了该算法的两个潜在扩展：一个是动态扩展，另一个是基于数量竞争的扩展。

Conclusions: This algorithm opens the door to the extensive inclusion of pricing in agent‑based models, but also, it helps to establish a link between the industrial organi‑ zation literature and the agent‑based modeling.

结论：该算法为基于主体的模型中广泛引入定价提供了可能性，同时也有助于建立产业组织文献与基于主体建模之间的联系。

Keywords: Agent‑based models, Algorithmic game theory, Price optimization, Industrial organization Background Prices play an essential role in any market and understanding how they are fixed is a fundamental part of the Economic Science. However, complex problems such as social networks or the launching of new digital platforms can set new challenges in understanding how those prices are fixed.

关键词：基于主体的模型、算法博弈论、价格优化、产业组织背景
在任何市场中，价格起着至关重要的作用，而了解价格是如何确定的则是经济科学的基本组成部分。然而，复杂问题，如社交网络或新数字平台的推出，可能会对我们理解价格确定机制提出新的挑战。

To tackle these complex problems, some researchers have adopted the agent-based modeling approach. But, there is a lack of integration between this approach and the industrial organization literature. This lack of integration is clearly depicted by the absence of works that address prices in agent-based models (ABM), despite being considered an essential variable in markets.1
To address this issue, I propose an algorithm for agent-based models that simulates price competition among companies. This algorithm establishes a new link between the industrial organization literature and the agent-based modeling. It is based on Game Theory, and it guarantees the optimality of consumers' and companies' behavior without needing to use the equilibrium equations of any theoretical model, nor relying on maximizing (minimizing) any real function.2 Intuitively, this algorithm resembles the best response map but without assuming any particular theoretical model or function. The algorithm encompasses two sub-algorithms, one for consumers and another one for companies. Both sub-algorithms encompass several behavioral rules that are combined to simulate the behavior predicted by Game Theory. In this sense, it is possible to address markets with heterogeneous decisions-makers, asymmetric information flows and levels, continuous or discontinuous behaviors, etc. and without assuming that decisionmakers carried out complicated mathematical manipulations, and at the same time, it is also possible to guarantee the optimality and rationality of our results.3
We test the algorithm in five different theoretical models, and we prove that the algorithm reproduces the Nash equilibria of those models. We also consider two extended versions of two theoretical models that are quite complex to solve. We prove that the algorithm also works in those cases. Lastly, we consider two more cases. The first one is dynamic, and the second one is based on quantity competition. In those two cases, we show that the algorithm is easily adaptable to other frameworks that are not static price-competition games.

为了应对这些复杂问题，一些研究人员采用了基于主体建模的方法。然而，这种方法与产业组织文献之间缺乏整合。尽管价格在市场中被认为是一个重要变量，但基于主体模型的研究中几乎没有涉及价格的作品。

为了解决这个问题，我提出了一种基于主体模型的算法，用于模拟公司之间的价格竞争。该算法在产业组织文献和基于主体建模之间建立了新的联系。它基于博弈论，并且可以保证消费者和公司行为的最优性，而无需使用任何理论模型的均衡方程或最大化（最小化）任何实际函数。直观地说，该算法类似于最佳反应映射，但不假设任何特定的理论模型或函数。该算法包括两个子算法，一个用于消费者，另一个用于公司。两个子算法都包含多个行为规则，并结合起来模拟博弈论预测的行为。因此，在处理具有异质决策者、信息流和水平不对称、连续或不连续行为等特征的市场时是可行的，并且无需假设决策者进行复杂的数学运算，同时也可以保证结果的最优性和合理性。

我们在五个不同的理论模型中测试了该算法，并证明了该算法能够重现这些模型的纳什均衡。我们还考虑了两个较复杂的理论模型的扩展版本。我们证明了该算法在这些情况下也适用。最后，我们考虑了另外两种情况。第一种是动态情况，第二种是基于数量竞争。在这两种情况下，我们展示了该算法可以轻松适应其他非静态价格竞争博弈框架。

This work does not pretend to provide groundbreaking evidence that agent-based models are better than other alternatives. We only try to establish a bridge between agent-based modeling and the mainstream industrial organization literature. And to do so, we apply the agent-base modeling to well-known theoretical models.

这项工作并不意味着提供了关于基于主体模型优于其他替代方案的突破性证据。我们只是试图在基于主体建模和主流产业组织文献之间建立一座桥梁。为了做到这一点，我们将基于主体建模应用到众所周知的理论模型中。

Agent‑based models and economic theory. An ongoing issue The situation of agent-based models in Economics can be summarized as follows: Despite the power of ABM, widespread acceptance and publication of this method in the highest-level journals has been slow. This is due in large part to the lack of commonly accepted standards of how to use ABM rigorously, Rand and Rust (2011). This problem is not new, but although some advances are taking place, there is plenty of room for improvement.

基于主体模型与经济理论：一个持续存在的问题
基于主体模型在经济学中的现状可以概括如下：尽管基于主体模型具有强大的能力，但该方法在顶级期刊上的广泛接受和发表进展缓慢。这主要是因为缺乏如何严格运用基于主体模型的共同认可标准（Rand和Rust，2011）。虽然这个问题并非新鲜事物，但尽管已经取得了一些进展，仍有很大改进空间。

Rand and Rust (2011) argues that, a common perception of agent-based models is that they are "toys" because of the lack of documentation, proper testing or theoretical background. Although some attempts have been made, theoretical economic models are rarely considered in the agent-based model literature.4 Those works which consider a theoretical framework are a minority, and we only can highlight some examples such as Rixen and Weigand (2014), Hamill and Gilbert (2016), Barr and Saraceno (2005) and Chang (2011). Nonetheless, they present two shortcomings:

根据Rand和Rust（2011）的观点，人们普遍认为基于主体模型的模型被视为“玩具”，因为缺乏文档、适当的测试或理论背景。尽管已经有一些尝试，但在基于主体模型的文献中很少考虑到理论经济模型。只有少数作品考虑了理论框架，我们可以举几个例子，如Rixen和Weigand（2014）、Hamill和Gilbert（2016）、Barr和Saraceno（2005）以及Chang（2011）。然而，这些作品存在两个缺点：

  •
They rely on the equilibrium equations of the theoretical models, so the simulated markets are constrained by the theoretical assumptions.
  •
They tend to assume other interactions among the agents even when the equilibrium of the theoretical model does not consider such interactions, which if taken into account, may change the equilibrium. Therefore, there is no standard rule or procedure to consider how to implement such theoretical frameworks.
Finally, another relevant shortcoming is that they tend to consider competition in quantities, particularly, the Cournot model. For instance, Barr and Saraceno (2005) investigates how environmental and organizational factors affect the equilibrium outcome of a repeated Cournot model. Chang (2011) analyzes entry and exit in an industrial market characterized by turbulent technological processes and by quantity competition.

• 这些模拟市场依赖于理论模型的均衡方程，因此受到理论假设的限制。
• 即使在理论模型的均衡不考虑这些相互作用的情况下，它们倾向于假设主体之间存在其他相互作用，而考虑这些相互作用可能会改变均衡。因此，在如何实施这样的理论框架方面没有标准规则或程序。
最后，另一个相关缺点是它们倾向于考虑数量上的竞争，尤其是Cournot模型。例如，Barr和Saraceno（2005）研究了环境和组织因素对重复Cournot模型均衡结果的影响。Chang（2011）分析了在技术过程动荡和数量竞争特征下产业市场中的进入和退出情况。

Rixen and Weigand (2014) analyzes the diffusion of smart meters and, although they try to relax some assumptions, they remain constrained by the Cournot model. Lastly, Hamill and Gilbert (2016) shows how Cournot models can be simulated using agentbased models, but it relies on the equilibrium outcomes of the basic Cournot model as in the previous works. There are also other works which do not assume theoretical frameworks, but assume exogenous and non-optimal prices such as Fuks and Kawa (2009), Zhang and Brorsen (2011) or Diao et al. (2011). To the best of our knowledge, only Leeuwen and Lijesen (2016) has considered a market with endogenous price competition but, it is limited to a Hotelling model, it is designed *ad-hoc*, it cannot be applied to other cases, it makes small but systematic errors when predicting prices, and it is not efficient when there are many consumers or companies.

Rixen和Weigand（2014）对智能电表的扩散进行了分析，尽管他们试图放松一些假设，但仍受到Cournot模型的限制。Hamill和Gilbert（2016）展示了如何使用基于主体的模型来模拟Cournot模型，但它依赖于基本Cournot模型的均衡结果，与之前的研究相似。还有其他一些研究不假设理论框架，而是假设外生和非最优价格，例如Fuks和Kawa（2009），Zhang和Brorsen（2011）或Diao等人（2011）。据我们所知，只有Leeuwen和Lijesen（2016）考虑了具有内生价格竞争的市场，但它局限于Hotelling模型，并且是特定目标设计，不能应用于其他情况，在预测价格时存在小而系统性错误，并且在存在许多消费者或公司时效率不高。

Given this situation, two questions arise:

鉴于这种情况，出现了两个问题：

  •
Can theoretical models be simulated following a set of standard rules?
  •
Can price competition be implemented in agent-based models following a set of common rules in concordance with Game Theory and economic intuitions?
The first question represents the common problem that each economist faces when dealing with agent-based models and, probably, it will take some decades to achieve a convergence in standards and criteria. On the other hand, the second question is the one we are going to answer in this work. We analyze an agent-based algorithm that simulates the pricing behavior that is assumed in theoretical economic models. This algorithm allows us to identify each component individually and to test its validity against the theory. The relevant contribution of the algorithm is twofold: First, it does not rely on the differentiability of an aggregate equation, but on the optimization of the agents' decisions. Second, it guarantees the optimality of the users' and companies' decisions (buying decisions and prices respectively) in ABM.

在处理基于主体的模型时，经济学家面临着一个常见问题：是否可以按照一套标准规则来模拟理论模型？这个问题可能需要几十年的时间才能达成标准和准则上的一致。另一个问题是我们将在本文中回答的重点。我们对一个基于主体算法进行了分析，该算法模拟了理论经济模型中所假设的定价行为。通过这个算法，我们能够单独识别每个组成部分，并对其与理论之间的有效性进行测试。该算法的重要贡献有两个方面：首先，它不依赖于聚合方程式的可微性，而是依赖于主体决策的优化。其次，在基于主体模型中保证用户和公司决策（购买决策和价格）的最优性。

[参考原文，对上述中文译文进行重写:]

## Experimental: The Price‑Competition Algorithm. Applications To Theoretical Models



The algorithm The algorithm is designed in a modular way. In this sense, each part of it can be used in different contexts and for different purposes. It consists in two sub-algorithms: The consumers' and the companies' algorithm. The consumers' reproduces the buying decisions of consumers and allows us to generate demands. The companies' sub-algorithm reproduces the process by which companies choose the price levels. The continuous interaction of both leads us to the equilibrium (or equilibria).

实验：价格竞争算法——对理论模型的应用

该算法采用模块化设计，使得其各个部分可以在不同的背景和目的下灵活应用。它由两个子算法组成：消费者算法和公司算法。消费者算法模拟了消费者的购买决策过程，从而生成需求。而公司算法则模拟了公司选择价格水平的过程。通过这两个子算法之间的持续互动，我们能够达到均衡状态（或多个均衡状态）。

The consumers' algorithm Our framework considers that each consumer at each moment of time t has an utility function U(·). Each consumer considers the utility he/she obtains from each company he/she knows. If no company offers a worthy product, U(·) < 0, the consumer abandons the market; but if there is a company which offers a valuable product, U(·) ≥ 0, the consumer will compare those products and will buy the one that maximizes its utility. All the consumers who buy the same product from the same company form the demand addressed to that company. In Fig. 1 is depicted a schematic version of the algorithm. Up to this point, this algorithm is not new, and similar algorithms can be found in other works. However, this algorithm is scalable. It presents four features that differentiate it from other proposals:5 

消费者算法
我们的框架假设在每个时间点t，每个消费者都有一个效用函数U(·)。每个消费者考虑从他/她所了解的每家公司获得的效用。如果没有公司提供有价值的产品，即U(·) < 0，消费者将放弃市场；但如果存在一家公司提供有价值的产品，即U(·) ≥ 0，消费者将比较这些产品，并购买能够最大化其效用的那一个。所有从同一家公司购买同一种产品的消费者构成了针对该公司的需求。图1展示了该算法的简化版本。尽管这个算法并非全新之物，在其他研究中也可以找到类似算法。然而，该算法具备可扩展性，并且具备以下四个与其他提案不同之处：5

  •Its modularity. This algorithm can be used independently of the price competition. •We do not impose any demand function, the demands are the emergent result of the consumers' decisions. It only matters how consumers make decisions.
  •Consumers make decisions based on their utility functions, which can be discrete or 
continuous and have as many parameters as necessary. However, those functions are flexible, and each consumer has its own utility function. That implies the possibility of introducing multi-dimensional heterogeneity, externalities, etc. Also, we do not impose fixed utility functions, those utilities can be dynamic.
  •Although we assume perfect information throughout the paper, the algorithm can be 
adapted to deal with those cases in which information is not perfect. For example, we can assume there is a network that connects consumers and by which information flows.
The companies' algorithm This sub-algorithm (Fig. 2) is composed of four sub-sub-algorithms.6 

• 模块化：该算法可独立于价格竞争使用。
• 我们不强加任何需求函数，需求是消费者决策的结果。重要的是消费者的决策方式。
• 消费者根据其效用函数做出决策，该函数可以是离散或连续的，并且可以具有所需的参数数量。然而，这些函数具有灵活性，每个消费者都有自己的效用函数。这意味着可以引入多维异质性、外部性等因素。此外，我们不限制使用固定的效用函数，这些效用函数可以是动态的。
• 尽管我们在整篇论文中假设信息完全无误，但该算法可适应信息不完全的情况。例如，我们可以假设存在一个连接消费者并传递信息的网络。

公司算法：
该子算法（图2）由四个子子算法组成。6

1. In the first algorithm, each company considers a change in prices (increase or 
decrease). The parameter ǫ controls this change (iteration parameter). The algorithm 
requires a starting price that can be any real number.7
2. In the second, each company considers how that change in prices will affect the 
demands. To estimate the impact of that change in the demands, they estimate the change in the utilities taking other companies' prices as given. Because all consumers compare the utility that each company's product provides them, the price decisions of companies influence the other companies. If we assume that all companies are 
rational and fully-informed. They will perfectly forecast the decision of consumers.8 
Nonetheless, the algorithm can consider other assumptions about how companies make their decisions.
3. The third algorithm is an optional one. It is designed to control externalities such 
as direct and indirect network effects. It addresses the case in which the change in prices affects the decisions of other consumers that, at the same time, influences other consumers and so on. In some cases, when a company changes their prices, 
that decision attracts other consumers that, at the same time, attract more consumers and so on. This algorithm simulates these feedback loops until this effect disappears (convergent feedback loops or the attraction of all the consumers).
4. Companies compare the three actions: increase, decrease or maintain the prices, and 
they choose the most profitable one.
As it was stated before, the algorithm resembles the best response map, so the convergence towards the price equilibria depends on the initial price and the size of the changes in prices (ǫ).9 Once the algorithm has reached an equilibrium, the algorithm will be continuously testing if any deviation is profitable. This algorithm can be considered as a helpful tool to look for local optima. To find global ones, we need to consider different ǫ -values and different suitable starting prices.

1. 在第一个算法中，每家公司考虑价格的变动（增加或减少）。参数ǫ用于控制这种变动（迭代参数）。该算法需要一个起始价格，可以是任意实数。7
2. 在第二个算法中，每家公司考虑价格变动对需求的影响。为了估计这种需求变动的影响，他们估计在其他公司的价格保持不变的情况下效用的变化。因为所有消费者都会比较每家公司产品所提供给他们的效用，所以公司的定价决策会影响其他公司。如果我们假设所有公司都是理性和充分了解情况的，它们将能够完美地预测消费者的决策。8然而，该算法可以考虑关于公司如何做出决策的其他假设。
3. 第三个算法是可选项。它旨在控制直接和间接网络效应等外部性。它处理这样一种情况：价格变动影响其他消费者的决策，而这些消费者同时又会影响其他消费者，依此类推。在某些情况下，当一家公司改变其价格时，该决策吸引了其他消费者，并进一步吸引更多消费者等等。该算法模拟这些反馈循环，直到这种效应消失（收敛的反馈循环或吸引所有消费者）。
4. 公司比较三种行动：增加、减少或保持价格，并选择最有利可图的行动。
正如前面所述，该算法类似于最佳响应映射，因此向价格均衡的收敛取决于初始价格和价格变动的大小（ǫ）。9一旦算法达到平衡状态，算法将不断测试是否存在有利可图的偏离。该算法可以被视为寻找局部最优解的有用工具。要找到全局最优解，我们需要考虑不同的ǫ值和不同合适的起始价格。

Theoretical frameworks To prove that the proposed algorithm is capable of reproducing theoretical models, we need to apply it in several frameworks. We choose five theoretical economic models. All of them share only one feature: companies compete in prices for consumers. This framework only requires knowing the utility functions, so we will not solve those models analytically. However, we provide references to those theoretical models. All the assumptions made in the following sections are the original assumptions of the models. Some of them are very restrictive, but those models are very well known in Economics, and it is easier to prove the algorithm in an environment that is well-known. Later, we will show how the algorithm is capable of dealing with those models but relaxing some of their assumptions.

理论框架
为了证明所提出的算法能够复现理论模型，我们需要在几个框架中应用它。我们选择了五个理论经济模型，它们都只有一个共同特征：公司之间为了争夺消费者而在价格上竞争。这个框架只需要了解效用函数，因此我们不会通过解析方法来解决这些模型。然而，我们提供了对这些理论模型的参考文献。以下各节中所做的所有假设都是这些模型的原始假设。尽管其中一些假设非常严格，但这些模型在经济学领域非常著名，在一个众所周知的环境中证明算法更加容易。稍后，我们将展示算法如何能够处理这些模型，并放宽其中一些假设。

Horizontal differentiation: the Hotelling framework This model10 assumes there is a large pool of small consumers that are uniformly distributed in a line. At the extreme of that line, there are two companies that compete in prices to attract consumers. Each consumer has to move from his/her position to the company's position he/she prefers. In Economics, this heterogeneity among consumers is called "horizontal differentiation". At the same level of prices, some consumers prefer one company but other consumers prefer the competitor. For example, at the same price, some consumers prefer Coke over Pepsi. In the classical version of this model, the utility of a consumer i buying the product of company j, j ∈ 1, 2 is

水平差异化：Hotelling框架
该模型假设存在一大批均匀分布在一条线上的小消费者。在该线的两个极端，有两家公司通过价格竞争来吸引消费者。每个消费者都需要从自己的位置移动到他/她更偏好的公司位置。在经济学中，这种消费者之间的异质性被称为“水平差异化”。在相同价格水平下，一些消费者更喜欢其中一家公司，而其他消费者则更喜欢竞争对手。例如，在相同价格下，一些消费者更倾向于选择可口可乐而不是百事可乐。在这个模型的经典版本中，消费者i购买第j家公司产品时所获得的效用为j ∈ 1, 2。

[注：根据原文内容进行了重写，以保持准确性和学术风格，并使句子结构更加流畅。]

$$U_{i,j}=c^{u}+q_{j}-t*|l_{j}-x_{i}|-p_{j}\tag{1}$$
All consumers are identical with the exception that they are uniformly located (xi) 
between 0 and 1. Consumers face a transportation cost (t) for reaching companies which are located at the extremes of the interval (lj ∈ [0, 1]). The intuition of this parameter is the following: The distance between products and consumers in that interval can be interpreted as a "cost" because consumers have to go from their position (that represents their ideal product) to companies' position (that represents the position of the real product). Therefore, the term that controls the differentiation is t ∗ |lj − xi|.

$$U_{i,j}=c^{u}+q_{j}-t*|l_{j}-x_{i}|-p_{j}\tag{1}$$

除了位置均匀分布在0和1之间的消费者(xi)外，所有消费者都是相同的。消费者面临着到达位于区间两端的公司的运输成本(t)。(lj ∈ [0, 1])。这个参数的直觉是：该区间内产品与消费者之间的距离可以解释为一种“成本”，因为消费者必须从他们所在的位置（代表他们理想产品的位置）到达公司所在位置（代表真实产品的位置）。因此，控制差异化程度的项是t * |lj − xi|。

To guarantee that all consumers buy at least one platform, the theoretical model assumes that all consumers have an identical (and sufficiently high) reservation value, cu . 

为了确保所有消费者至少购买一个平台，理论模型假设所有消费者具有相同（且足够高）的保留价值cu。

Lastly, we assume each company sells a product that has an exogenous quality level qj , and they fix a price pj.

最后，我们假设每家公司销售的产品具有外生的质量水平qj，并且他们确定了一个价格pj。

Vertical differentiation model In this case11, consumers' preferences are

垂直差异化模型 在这种情况下11，消费者的偏好是

$$U_{i,j}=\theta_{i}*q_{j}-p_{j}\tag{2}$$
All consumers pay a price pj when consuming the product j, j ∈ 1, 2, which has a quality qj. Without loss of generality, we assume q1 > q2. The parameter θ represents the taste for quality. It is uniformly distributed across the population of consumers between θ ≥ 0 
and θ = θ + 1 with density 1.

在消费产品j时，所有消费者都需要支付价格pj，其中j ∈ 1, 2。这些产品具有不同的质量水平，我们假设q1 > q2以简化问题。参数θ代表了对质量的偏好程度，它在消费者群体中均匀分布于θ ≥ 0和θ = θ + 1之间，密度为1。

根据公式(2)，消费者i在购买产品j时的效用可以表示为$$U_{i,j}=\theta_{i}*q_{j}-p_{j}$$

We make two extra assumptions that are common in literature to guarantee enough differentiated consumers and a covered market respectively:
Assumption 1 θ ≥ 2θ

我们做出两个额外的假设，这在文献中很常见，以确保有足够多的不同消费者和一个覆盖市场：
假设1：θ ≥ 2θ

#### Assumption 2



$\frac{(\overline{\theta}-2\theta)}{3}(q_1-q_2)\leq\underline{\theta}q_1$.

假设2：存在一个下界值$\underline{\theta}$，使得$(\overline{\theta}-2\theta)(q_1-q_2)/3\leq\underline{\theta}q_1$。

The intuition of the vertical differentiation is the following: at the same level of prices, all consumers prefer one company over the rest. For example, at the same price, all consumers prefer a Ferrari over a Fiat.

垂直差异化的直觉如下：在相同价格水平下，所有消费者都更喜欢某一家公司而不是其他公司。例如，在相同价格下，所有消费者都更喜欢法拉利而不是菲亚特。

Externalities: two‑sided markets We consider two cases. Both of them are extensions of the previous models. In the first case, we consider the two-sided market proposed by Hagiu and Hałaburda (2014) in which two platforms compete in prices for users and developers. This model can be considered an extension of the Hotelling's in which there are indirect network externalities between two independent groups of consumers: users and developers. Following the original work, we assume all consumers are rational and buy one and only one platform. 

外部性：双边市场
我们考虑两种情况，它们是对之前模型的扩展。在第一种情况下，我们研究了Hagiu和Hałaburda（2014）提出的双边市场，其中两个平台通过价格竞争来吸引用户和开发者。这个模型可以被视为Hotelling模型的扩展，其中存在着两个独立消费者群体之间的间接网络外部性：用户和开发者。根据原始研究，我们假设所有消费者都是理性的，并且只购买一个平台。

In this case, the utility of a user i consuming the platform j, j ∈ 1, 2 is given by12

在这种情况下，用户i消费平台j（其中j∈1,2）的效用由以下公式给出12。

$$U_{i,j}=c_{i}^{u}-t*|l_{j}-x_{i}|-p_{j}+\delta n_{-j}\tag{3}$$
Users are uniformly located in the interval [0,1], and they suffer a cost when going from their position to the platforms', like in the Hotelling model. However, instead of valuing exogenous qualities, users (developers) value the number of developers (users) they can meet in the platform (n−j). We assume all users (developers) value the presence of the other group in the same way (δ).

用户在区间[0,1]上均匀分布，并且当他们从自己的位置移动到平台时会产生成本，类似于Hotelling模型。然而，与其评估外部品质不同，用户（开发者）评估他们在平台上可以遇到的开发者（用户）的数量（n−j）。我们假设所有用户（开发者）以相同的方式看待同一群体的存在（δ）。

The second model is proposed by Gabszewicz and Wauthy (2004), which is another example of two-sided markets. However, it has two interesting features: first, it presents vertical differentiation. This characteristic is unusual among the two-sided market literature, mainly because it generates multiple equilibria. Second, there is no information about the stability of the equilibria, so we have the opportunity to test the algorithm in an environment in which several potential equilibria are possible.

Gabszewicz和Wauthy（2004）提出的第二个模型是另一个双边市场的典型案例。然而，该模型具有两个引人注目的特点：首先，它呈现出垂直差异化。这一特征在双边市场文献中并不常见，主要是因为它会导致多个均衡状态的存在。其次，关于这些均衡状态的稳定性没有提供任何信息，因此我们有机会在可能存在多个潜在均衡状态的环境中测试算法。

It consists of two platforms that represent exhibition centers that compete for visitors and exhibitors. In this case, visitors' preferences are described by

该模型由两个代表展览中心的平台组成，它们竞争吸引游客和参展商。在这种情况下，游客的偏好通过...（待续）

$$U_{i,j}=\theta x_{j}^{e}-p_{j}\tag{4}$$
And exhibitors' preferences are

$$U_{i,j}=\theta x_{j}^{e}-p_{j}\tag{4}$$
参展商的偏好是...（待续）

$$U_{l^{\prime}j}=\gamma v_{j}^{\epsilon}-\pi_{j}\tag{5}$$
Parameters θ and γ are best understood as a measure of how each visitor (exhibitor) values an additional exhibitor (visitor) in the exhibition centers. The intuition underlying the model is the following. From an exhibitor's point of view,13 the willingness to rent a stand in the exhibition center depends on his personal value of an additional visitor (γ), on the number of additional sales this exhibitor may expect (that depends on the number of visitors, v e j),14 and on the rental fee, πj. At the same price, all exhibitors will prefer the exhibition center with more visitors.

参数θ和γ可被视为衡量每位参观者（展商）对于展览中心中增加一个展商（参观者）的价值的度量。该模型的基本思想是：从展商的角度来看，是否愿意租用展位取决于其对于额外参观者的个人价值（γ），以及该展商可能预期到的额外销售数量（取决于参观者数量v_ej），还有租金费用πj。在相同价格下，所有展商都更倾向选择游客更多的展览中心。

In the original work, the authors assume that θ, γ , v e j , x e j ∈ [0, 1], in other words, they assume a normalized market.

在原始研究中，作者假设θ、γ、v_ej和x_ej都属于[0, 1]的范围，换句话说，他们假设市场是标准化的。

Warranties model This model is taken from [Belleflamme and Peitz (2015), Chapter 13]. In this model, we suppose that a firm offers a product that breaks down with probability 1 − , and consumers are willing to pay for a product that works a quantity r > 0. The authors make four assumptions:

保修模型
这个模型源自于[Belleflamme和Peitz（2015），第13章]。在该模型中，我们假设一家公司提供的产品有1-的概率出现故障，而消费者愿意为一个能够正常工作的产品支付数量r > 0。作者对此做出了四个假设：

  •
There is a unit mass of homogeneous consumers
  •
There are two firms. A high-quality one (1) and a low-quality one (2). Therefore, 
1 > 2
  •
Consumers do not know the quality of each company
  •
Both companies have constant marginal costs, c.
From consumers' point of view, a firm can be the high-quality one with probability ρ and the low-quality one with probability 1 − ρ. Thus, the expected utility of consumers is

• 存在一群同质化的消费者，其总质量为单位质量。
• 存在两家公司，一家是高质量公司（1），另一家是低质量公司（2）。因此，有1 > 2。
• 消费者对每家公司的质量一无所知。
• 两家公司均具有恒定的边际成本c。
从消费者的角度来看，一家公司以概率ρ成为高质量公司，以概率1-ρ成为低质量公司。因此，消费者的预期效用为。

$$U_{i}=(\rho\dot{\lambda}_{1}+(1-\rho)\dot{\lambda}_{2})r-p\tag{6}$$
Up to now, the model does not consider warranties. Let's introduce full warranties (the company replaces the broken product by a new one). The expected cost of introducing a warranty is c/1 for the high-quality one, and c/2 for the low-quality one. The interesting point about this model is that consumers only observe prices and warranties. Warranties can play a decisive role in shaping prices and market shares because they provide information about which company could be the high-quality one. Companies can use warranties to "prove" users that its product is the high-quality one.15 To guarantee the stability of the equilibrium, the authors assume 2r < c.

$$U_{i}=(\rho\dot{\lambda}_{1}+(1-\rho)\dot{\lambda}_{2})r-p\tag{6}$$

迄今为止，该模型未考虑保修。现在我们引入全面保修（公司将损坏的产品更换为新产品）。引入保修的预期成本为高质量产品为c/1，低质量产品为c/2。这个模型的有趣之处在于消费者只观察到价格和保修。保修可以在塑造价格和市场份额方面起到决定性作用，因为它们提供了哪家公司可能是高质量公司的信息。公司可以利用保修来“证明”用户其产品是高质量的。为了确保均衡的稳定性，作者假设2r < c。

Results and simulation tests We create a world with 314 consumers (in the case of the market with two-sided platforms, there are 628 consumers divided into two groups: users and developers, or visitors and exhibitors) and two companies. We run one thousand simulations for each case in NetLogo. In all those cases, we compare the theoretical and the simulated equilibria. 

结果和模拟测试：我们在NetLogo中创建了一个世界，其中包含314名消费者（在双边平台市场的情况下，分为两组：用户和开发者，或访客和展商），以及两家公司。我们对每种情况进行了一千次模拟，并比较了理论均衡和模拟均衡的结果。

We consider two ε-values, 0.1 and 0.05. For each case, we only consider a set of parameters values, for example, different transportation costs or quality levels, etc. to show how the algorithm is capable of reaching the theoretical equilibria. We can consider other cases with other parameters but, for simplicity's sake and without loss of generality, they are not included (although they are available upon request).16
Horizontal differentiation: the Hotelling framework We run the simulations considering different transportation costs and with symmetric quality levels (q1 = q2). As depicted in Fig. 3, depending on what ε-values we assume, we obtain different simulated prices that reproduce the theoretical prices properly.17
To test if simulated prices are able to reproduce the theoretical prices accurately, we run a linear regression in which the dependent variable is the theoretical price, and the explanatory variable is the simulated one. In Table 1, we observe that the r-squared is close to 99% 
in both cases. So, the simulated prices explain 99% of the variations in theoretical prices.

我们考虑了两个ε值，分别为0.1和0.05。针对每种情况，我们仅考虑一组参数值，例如不同的运输成本或质量水平等，以展示算法如何能够达到理论均衡。尽管我们可以考虑其他具有不同参数的情况，但为了简化问题并且不失一般性，我们在此未加以考虑（尽管可以根据要求提供）。16
在Hotelling框架下进行模拟时，我们考虑了不同的运输成本，并且假设质量水平是对称的（q1 = q2）。如图3所示，根据所假设的ε值不同，我们得到了能够准确复现理论价格的不同模拟价格。17
为了验证模拟价格是否能够准确复现理论价格，我们进行了线性回归分析。其中因变量是理论价格，自变量是模拟价格。从表1中可以观察到，在两种情况下R方接近99%。因此，模拟价格能够解释理论价格变动中99%的差异。

Let's consider the difference between theoretical and simulated prices. We test if those errors are normally distributed. To do so, we consider three normality test, all of them assume the null hypothesis of normality.

让我们考虑理论价格和模拟价格之间的差异。我们测试这些误差是否服从正态分布。为此，我们考虑了三种正态性检验，它们都假设正态性的零假设。

The first one is the D'Agostino's K-squared test, or the Skewness and Kurtosis test. This test is based on the kurtosis and skewness measures, it can be considered a default normality test. We also consider the Shapiro–Wilk test, which is another traditional normality test. Lastly, we consider the Shapiro–Francia test, which is indicated as the best test to detect deviation from normality in a recent work, Mbah and Paothong (2015).

首先是D'Agostino的K平方检验，也称为偏度和峰度检验。该检验基于峰度和偏度的测量，可被视为默认的正态性检验。其次，我们考虑了Shapiro-Wilk检验，这是另一种传统的正态性检验方法。最后，我们考虑了Shapiro-Francia检验，在最近的研究中被认为是最佳用于检测偏离正态分布的测试方法（Mbah和Paothong，2015）。

In Table  2, we observe the p-values associated with those tests. Let's consider first the case in which ε = 0.1. In this case, at 95% confidence level, only in the D'Agostino's K-squared test we can reject the null hypothesis of normality. It is reasonable to think that errors are normally distributed and therefore, the average (− 0.036) is a good representation of the simulations errors. In this case, it is an underestimation of 3.6%. However, given that the algorithm works considering 10% of change in prices (ε = 0.1), this error is negligible.

在表2中，我们观察到与这些检验相关的p值。首先考虑ε = 0.1的情况。在这种情况下，在95%的置信水平下，只有在D'Agostino的K平方检验中我们可以拒绝正态性的零假设。我们合理地认为误差是正态分布的，因此平均值（-0.036）很好地代表了模拟误差。尽管它低估了3.6%，但考虑到算法是基于价格变化10%（ε = 0.1）进行工作的，这个误差可以忽略不计。

On the other hand, when ε = 0.05, all the tests suggest that the difference between simulated and theoretical prices is not normal. We run a variance-comparison test, and we find that, at 99% confidence level, the standard deviations between the cases with transportation costs in the interval [0.1;0.59] and in the interval [0.60;0.99] have different variances. Given that each simulation for each parameter is independent of the rest, we can analyze both sub-samples separately. The first one considers transportation costs between 0.1 and 0.59 and the other one between 0.60 and 0.99. In those intervals, at 95% confidence level, we cannot reject the null hypothesis of equal variance.

然而，当ε = 0.05时，所有的检验结果表明模拟价格与理论价格之间的差异不服从正态分布。我们进行了方差比较测试，并发现在99%的置信水平下，运输成本在[0.1;0.59]和[0.60;0.99]区间内的标准差具有显著不同的方差。由于每个参数的每次模拟都是相互独立的，我们可以对这两个子样本进行单独分析。第一个子样本考虑了运输成本在0.1到0.59之间，另一个子样本考虑了运输成本在0.60到0.99之间。在这些区间内，在95%的置信水平下，我们无法拒绝等方差的零假设。

If we run the normality tests again, we cannot reject the null hypothesis of normality at 95% confidence level, Table  3. Therefore, the average error in simulated prices is an underestimation of 1.3% in the first part (− 0.013), and an overestimation of 2% in the second part (0.02). But given that the algorithm works considering changes of 5% in prices, in this case, those errors are also negligible.

重新进行正态性检验后，我们无法以95%的置信水平拒绝正态性的零假设（见表3）。因此，在第一部分中，模拟价格的平均误差被低估了1.3%（-0.013），而在第二部分中被高估了2%（0.02）。然而，考虑到该算法在价格变动5%时的工作表现，这些误差可以被视为可忽略的。

| Variable                      | Coefficient (std. err.)   |
|-------------------------------|---------------------------|
| (a) Hotelling, Iteration 0.1  |                           |
| Simulated price               | 1.0459** (0.0073)         |
| N                             | 90                        |
| R                             |                           |
| 2                             |                           |
| 0.9957                        |                           |
| F                             |                           |
| (                             |                           |
| 1,89                          |                           |
| )                             |                           |
| 20,558.99                     |                           |
| (b) Hotelling, Iteration 0.05 |                           |
| Simulated price               | 0.9821** (0.005)          |
| N                             | 90                        |
| R                             |                           |
| 2                             |                           |
| 0.9977                        |                           |
| F                             |                           |
| (                             |                           |
| 1,89                          |                           |
| )                             |                           |
| 38,519.85                     |                           |
ε/p‑values
Skewness and kurtosis test
Shapiro–Wilk test
Shapiro–Francia test
0.10
0.0205
0.09909
0.60196
0.05
0.0000
0.0000
0.001
| Intervals   |   Skewness and kurtosis test |   Shapiro–Wilk test |   Shapiro–Francia test |
|-------------|------------------------------|---------------------|------------------------|
| [0.1;0.59]  |                       0.5595 |             0.23156 |                0.86565 |
| [0.60;0.99] |                       0.2468 |             0.67779 |                0.68322 |

| 变量                          | 系数（标准误差）    |
|-------------------------------|---------------------------|
| (a) Hotelling, 迭代0.1       |                           |
| 模拟价格                      | 1.0459** (0.0073)         |
| N                             | 90                        |
| R                             |                           |
| 2                             |                           |
| 0.9957                        |                           |
| F                             |                           |
| (                             |                           |
| 1,89                          |                           |
| )                             |                           |
| 20,558.99                     |                           |
| (b) Hotelling, 迭代0.05      |                           |
| 模拟价格                      | 0.9821** (0.005)          |
| N                             | 90                        |
| R                             |                           |
| 2                             |                           |
| 0.9977                        |                           |
F                            ||
(                            ||
1,89                         ||
)                            ||
38,519.85                    ||

ε/p-值
偏度和峰度检验
Shapiro-Wilk检验
Shapiro-Francia检验
0.10
0.0205
0.09909
0.60196
0.05
0.00000
0.00000
0。001

区间        偏度和峰度检验     Shapiro-Wilk检验   Shapiro-Francia检验 
[0。1; 059]  	05595 	          	23156 	             	86565 
[060;099]  	02468 	          	67779 	             	68322

Vertical differentiation model In this case, we run the simulations by considering different quality levels for company 2. 

垂直差异化模型。在这种情况下，我们通过考虑公司2的不同质量水平来运行模拟。

Nonetheless, we maintain q1 = 1. In Fig.  4, we observe the simulated and the theoretical equilibrium prices considering different quality levels (company 2). As in the previous case, the simulated prices reproduce the theoretical ones accurately.18
We run a linear regression for each ε. The dependent variable is the theoretical price, and the explanatory variable is the simulated price. We find the algorithm reproduces the behavior of the theoretical companies properly.

尽管如此，我们仍然保持q1 = 1。在图4中，我们观察到考虑不同质量水平（公司2）时的模拟和理论均衡价格。与之前的情况一样，模拟价格准确地再现了理论价格。对于每个ε，我们进行了线性回归分析。其中，理论价格作为因变量，模拟价格作为自变量。我们发现该算法能够准确地再现理论公司的行为。

In Table  4, we observe that the r-squared is close to 99% in all cases. The simulated prices are able to explain 99% of the variations in the theoretical prices. As in the Hotelling model, simulations reproduce the optimizing behavior of companies accurately. Let's consider the differences between the theoretical and simulated prices. As before, we consider three normality tests.

在表4中，我们可以观察到在所有情况下，R平方接近99%。模拟价格能够解释理论价格变动的99%。与Hotelling模型相似，模拟结果准确地再现了公司的优化行为。现在我们来考虑一下理论价格和模拟价格之间的差异。与之前一样，我们进行了三个正态性检验。

In Table  5, we observe that all the normality tests point out that, at 95% confidence level, we cannot reject the null hypothesis of normality. Therefore, the average of the errors can be interpreted as the average error of the algorithm in this model. In this case, the algorithm yields an average error of − 1.5% (− 0.015) when ε = 0.1 and 1% (0.01) 
when ε = 0.05. Nonetheless, the algorithm considers changes in prices of 10 and 5% 
respectively, so these errors are negligible.

在表5中，我们可以观察到所有的正态性检验结果表明，在95%的置信水平下，我们无法拒绝正态性的零假设。因此，可以将误差的平均值解释为该模型中算法的平均误差。在这种情况下，当ε = 0.1时，算法产生了一个平均误差为-1.5%（-0.015），当ε = 0.05时，算法产生了一个平均误差为1%（0.01）。然而，考虑到价格变化分别为10%和5%，所以这些误差可以忽略不计。

In this model, demands are not equal. In contrast with the rest of the models, companies will not equally share the market. Nonetheless, the algorithm is also capable of simulating demands. In Fig.  5, we observe demands are well reproduced at the beginning, but there are divergences at high-quality levels. This effect depends on the ε we assume, and it is exclusive of vertically differentiated models.

在这个模型中，需求是不均衡的。与其他模型相比，公司不会平均分享市场份额。然而，该算法也能够模拟需求。在图5中，我们观察到需求在开始时被很好地再现，但在高质量水平上存在差异。这种效应取决于我们所假设的ε，并且它只存在于垂直差异化模型中。

When both qualities are similar, prices tend to be similar too but, because the algorithm works in "discrete jumps (ε)", when both qualities are similar, little increments of quality may not change the simulated prices but may change utilities, which leads to 

当两种质量相似时，价格也倾向于相似，但是由于算法以“离散跳跃（ε）”的方式工作，当两种质量相似时，质量的微小增加可能不会改变模拟价格，但可能会改变效用，从而导致...

| Variable           | Coefficient (std. err.)   |
|--------------------|---------------------------|
| (a) Iteration 0.1  |                           |
| Simulated price    | 1.0385** (0.0104)         |
| N                  | 85                        |
| R                  |                           |
| 2                  |                           |
| 0.9917             |                           |
| F                  |                           |
| (                  |                           |
| 1,84               |                           |
| )                  |                           |
| 10066.75           |                           |
| (b) Iteration 0.05 |                           |
| Simulated price    | 1.0314 ** (0.0054)        |
| N                  | 85                        |
| R                  |                           |
| 2                  |                           |
| 0.9977             |                           |
| F                  |                           |
| (                  |                           |
| 1,84               |                           |
| )                  |                           |
| 36883.17           |                           |
ε
Skewness and kurtosis test
Shapiro–Wilk test
Shapiro–Francia test
0.1
0.3097
0.77471
0.94308
0.05
0.2197
0.22636
0.24974

| 变量               | 系数 (标准误差)       |
|--------------------|---------------------------|
| (a) 迭代 0.1       |                           |
| 模拟价格           | 1.0385** (0.0104)         |
| 样本量             | 85                        |
| R方                |                           |
| 2                  |                           |
| 0.9917             |                           |
| F统计量             |                           |
| (                  |                           |
| 1,84               |                           |
| )                  |                           |
| 10066.75           |                           |
| (b) 迭代 0.05      |                           |
| 模拟价格           | 1.0314 ** (0.0054)        |
| 样本量             | 85                        |
| R方                |                           |
| 2                  |                           |
| 0.9977             |                           |
F统计量
(                  
1,84               
)
36883.17           
ε
偏度和峰度检验
Shapiro-Wilk检验
Shapiro-Francia检验
0.1
0.3097
0.77471
0.94308
0.05
0.2197
0.22636
0。24974

changes in demands. The more similar the platforms are, the more relevant are these changes. For that reason, those unusual behaviors are concentrated in the region where platforms are less differentiated. If we omit that region, we observe that the difference between theoretical and simulated demands (hereinafter, the errors) are normally distributed and, on average, the algorithm predicts without errors the demand level. However, we cannot omit the fact that some errors arise. To prove that those errors come from the ε-value assumed, we also consider the case in which ε = 0.01.

需求的变化与平台的相似程度密切相关。当平台差异较小时，这些变化表现得更为显著。如果我们排除这个地区，我们会发现理论需求和模拟需求之间的差异（以下简称误差）呈正态分布，并且算法在预测需求水平时平均没有误差。然而，我们不能忽视一些误差的存在。为了证明这些误差是由于假设的ε值引起的，我们还考虑了ε = 0.01的情况。

In Table 6, the  represents the difference between companies' quality levels at which the errors are normal. For instance, when ε = 0.01, only if the difference in quality is bigger than 0.05, the errors are normal. In parenthesis, there are the p-values that correspond to those cases in which we remove the observations with a differentiation less than . In Table  7, we observe the case in which ε = 0.01 is the best one in reproducing demands because prices are more sensitive to differences in qualities.

在表6中，我们使用符号  来表示公司质量水平之间的差异，该差异下的误差是正常的。例如，当ε = 0.01时，只有当质量差异大于0.05时，误差才被认为是正常的。括号中的p值对应于那些我们删除了质量差异小于 的观察值的情况。在表7中，我们观察到当ε = 0.01时，在再现需求方面是最好的选择，因为价格对质量差异更为敏感。

In contrast with the previous case, the lower the ε, the more accurate are the simulated prices and demands in all cases. Figure 6 depicts the comparison between the cases in which ε = 0.05, ε = 0.1 and ε = 0.01.

与前一个案例相比，ε越低，在所有情况下模拟的价格和需求越准确。图6显示了ε = 0.05、ε = 0.1和ε = 0.01的情况之间的比较。

## Externalities: Two‑Sided Markets



Hagiu and Halaburda's model This model considers that two platforms compete in prices for consumers (users and developers). Consumers value the presence of the other group so, the more, the better. For simplicity's sake and without loss of generality, we assume both sides are 

Hagiu和Halaburda的模型考虑了两个平台在消费者（用户和开发者）方面的价格竞争。消费者对另一组的存在感兴趣，因此越多越好。为了简化问题并且不失一般性，我们假设两个方面都是竞争性的。

[参考原文，对上述中文译文进行重写:]

ε ()
Skewness and kurtosis test
Shapiro–Wilk test
Shapiro–Francia test
0.1(0.14)
0.0037 (0.0674)
0.00000 (0.13764)
0.00001 (0.07698)
0.05(0.09)
0.0009 (0.0396)
0.00001 (0.09888)
0.00002 (0.04154)
0.01 (0.05)
0.000 (0.6848)
0.00000 (0.69446)
0.00001 (0.55921)
| Variable           | Coefficient (std. err.)   |
|--------------------|---------------------------|
| (a) Iteration 0.1  |                           |
| Simulated demand   | 0.9556** (0.0231)         |
| N                  | 85                        |
| R                  |                           |
| 2                  |                           |
| 0.9534             |                           |
| F                  |                           |
| (                  |                           |
| 1,84               |                           |
| )                  |                           |
| 1717.66            |                           |
| (b) Iteration 0.05 |                           |
| Simulated demand   | 0.9850** (0.0165)         |
| N                  | 85                        |
| R                  |                           |
| 2                  |                           |
| 0.9771             |                           |
| F                  |                           |
| (                  |                           |
| 1,84               |                           |
| )                  |                           |
| 3585.43            |                           |
| (c) Iteration 0.01 |                           |
| Simulated demand   | 0.9987** (0.0067)         |
| N                  | 85                        |
| R                  |                           |
| 2                  |                           |
| 0.9962             |                           |
| F                  |                           |
| (                  |                           |
| 1,84               |                           |
| )                  |                           |
| 22024.81           |                           |

ε ()
偏度和峰度检验
Shapiro-Wilk检验
Shapiro-Francia检验
0.1(0.14)
0.0037 (0.0674)
0.00000 (0.13764)
0.00001 (0.07698)
0.05(0.09)
0.0009 (0.0396)
0.00001 (0.09888)
0.00002 (0.04154)
0。01（ ）。
（a）迭代  。
模拟需求   。9556** （   ）。
N                  | 85                        |
R                  |                           |
2                  |                           |
。9534             |                           |
F                  |                           |
（                  |                           |
1,84               |                           |
）                  |                           |
1717。66            |                           |
（b）迭代  。05 
模拟需求   。985** （   ）。
N                  | 85                        |
R                  |                           |
2                  |                           |
。9771             ||                          ||
F                 ||                          ||
（                 ||                          ||
1,84              ||                          ||
)                 ||                          ||
3585。43           ||                          ||
(c) 迭代    .01 
模拟需求   .9987** （    )。
N                   .85                       )|
R                   .                         )|
2                   .                         )|
9962                .                         )|
F                   .                         )|
(                   .                         )|
1,84                .                         )|
)                   .                         )
22024。81           。

symmetrical, and we only analyze one of them, in this case, we focus on users. We run simulations considering different transportation costs. In Fig.  7, we observe that the simulated and theoretical prices behave in a similar way. As in the previous cases, the simulated prices reproduce the theoretical ones properly.19
If we regress the theoretical prices with the simulated ones, we find that, in all cases, the r-squared is superior to 99%, which shows that simulated prices predict quite well the theoretical prices, Table 8.

在这种情况下，我们只分析了其中一个对称的方面，即用户。我们进行了考虑不同运输成本的模拟实验。从图7可以看出，模拟价格和理论价格的行为方式相似。与之前的情况一样，模拟价格很好地复制了理论价格。通过将模拟价格与理论价格进行回归分析，我们发现在所有情况下，R平方值均超过99%，这表明模拟价格很好地预测了理论价格（见表8）。

In Table   9, we analyze the differences between the simulated and the theoretical prices. We observe that when ε = 0.1 and at 95% confidence level, we cannot reject the null hypothesis of normality. On the other hand, given that the average is approximately 

在表9中，我们分析了模拟价格和理论价格之间的差异。我们观察到当ε = 0.1且在95%的置信水平下时，我们无法拒绝正态性的零假设。另一方面，考虑到平均值约为...

| Variable                      | Coefficient (std. err.)   |
|-------------------------------|---------------------------|
| (a) Two‑sided, Iteration 0.1  |                           |
| Simulated price               | 0.9924** (0.0068)         |
| N                             | 90                        |
| R                             |                           |
| 2                             |                           |
| 0.9959                        |                           |
| F                             |                           |
| (                             |                           |
| 1,88                          |                           |
| )                             |                           |
| 21,373.90                     |                           |
| (b) Two‑sided, Iteration 0.05 |                           |
| Simulated price               | 0.9201** (0.0055)         |
| N                             | 90                        |
| R                             |                           |
| 2                             |                           |
| 0.9968                        |                           |
| F                             |                           |
| (                             |                           |
| 1,88                          |                           |
| )                             |                           |
| 27,492.02                     |                           |
ε
Skewness and kurtosis test
Shapiro–Wilk test
Shapiro–Francia test
0.1
0.2179
0.14804
0.77307
0.05
0.0000 (0.2568)
0.0000 (0.3255)
0.0000 (0.4511)

| 变量                          | 系数（标准误差）     |
|-------------------------------|---------------------------|
| (a) 双边, 迭代 0.1             |                           |
| 模拟价格                      | 0.9924** (0.0068)         |
| N                             | 90                        |
| R                             |                           |
| 2                             |                           |
| 0.9959                        |                           |
| F                             |                           |
| (                             |                           |
| 1,88                          |                           |
| )                             |                           |
| 21,373.90                     |                           |
| (b) 双边, 迭代 0.05            |                           |
| 模拟价格                      | 0.9201** (0.0055)         |
| N                             | 90                        |
| R                             |                           |
| 2                             |                           |
| 0.9968                        |                           |
F
(                             
1,88                          
)                             
27,492.02                     
ε
偏度和峰度检验
Shapiro-Wilk检验
Shapiro-Francia检验
0.1
0.2179
0.14804
0.77307
0.05
p < 0.001 (偏度: 0.2568)
p < 0.001 (偏度: 03255)
p < 0.001 (偏度:04511)

zero, we can state that, in this case, the algorithm makes no error. However, when we consider ε = 0.05, we can reject the null hypothesis of normality at 99% confidence level. 

在这种情况下，当ε = 0.05时，我们可以以99%的置信水平拒绝正态性的零假设。

However, this rejection is a consequence of an unusual behavior at high transportation costs. When transportation costs are higher than 0.9, simulated prices show great differences with theoretical prices as depicted in Fig.  7.

然而，这种拒绝是由于在高运输成本下的异常行为所导致的。当运输成本高于0.9时，模拟价格与理论价格之间存在很大差异，如图7所示。

If we omit that interval, in all normality tests, the null hypothesis cannot be rejected at 95% confidence level. The average is approximately equal to 0.03. So, we can state that when ε = 0.05, the algorithm makes an average error of 3% (3.8% if that interval is not omitted). As in previous cases, given that the algorithm works with percentages bigger than the average errors, those errors are negligible.

如果我们排除该区间，在所有正态性检验中，无法以95%的置信水平拒绝零假设。平均值约为0.03。因此，我们可以得出结论，当ε = 0.05时，该算法的平均误差为3%（如果不排除该区间，则为3.8%）。与之前的情况一样，鉴于该算法处理的百分比大于平均误差，这些误差可以忽略不计。

| Equilibria              |
|-------------------------|
|                         |
| 1                       |
| =                       |
| 0.0233                  |
|                         |
| 2                       |
| =                       |
| 0.1866                  |
| Duopolistic equilibrium |
| p                       |
| 1                       |
| =                       |
| π                       |
| 1                       |
| =                       |
| 2                       |
| /                       |
| 49                      |
| p                       |
| 2                       |
| =                       |
| π                       |
| 2                       |
| =                       |
| 8                       |
| /                       |
| 49                      |
| x                       |
| 1                       |
| =                       |
| v                       |
| 1                       |
| =                       |
| 2                       |
| /                       |
| 7                       |
| x                       |
| 2                       |
| =                       |
| v                       |
| 2                       |
| =                       |
| 4                       |
| /                       |
| 7                       |
| Monopoly corner eq.     |
| p                       |
| 1                       |
| =                       |
| 0,                      |
| π                       |
| 1                       |
| =                       |
| 1                       |
| /                       |
| 2                       |
| x                       |
| 1                       |
| =                       |
| 1,                      |
| v                       |
| 1                       |
| =                       |
| 1                       |
| /                       |
| 2                       |
|                         |
| =                       |
| 1                       |
| /                       |
| 4                       |
| Monopoly equilibrium    |
| p                       |
| 1                       |
| =                       |
| π                       |
| 1                       |
| =                       |
| 1                       |
| /                       |
| 2                       |
| x                       |
| 1                       |
| =                       |
| v                       |
| 1                       |
| =                       |
| 1                       |
| /                       |
| 2                       |
|                         |
| =                       |
| 1                       |
| /                       |
| 4                       |
| Equilibria   |
|--------------|
| ǫ            |
| =            |
| 0.1          |
| P            |
| =            |
| x            |
| =            |
|              |
| =            |
| 0            |
| P            |
| =            |
| 0.21         |
|              |
| x            |
| =            |
| 0.698        |
|              |
|              |
| =            |
| 0.293        |
| ǫ            |
| =            |
| 0.05         |
| P            |
| =            |
| x            |
| =            |
|              |
| =            |
| 0            |
| P            |
| =            |
| 0.21         |
|              |
| x            |
| =            |
| 0.647        |
|              |
|              |
| =            |
| 0.291        |
| ǫ            |
| =            |
| 0.01         |
| P            |
| =            |
| x            |
| =            |
|              |
| =            |
| 0            |
| P            |
| =            |
| 0.24         |
|              |
| x            |
| =            |
| 0.599        |
|              |
|              |
| =            |
| 0.287        |
| ǫ            |
| =            |
| 0.005        |
| P            |
| =            |
| x            |
| =            |
|              |
| =            |
| 0            |
| P            |
| =            |
| 0.22         |
|              |
| x            |
| =            |
| 0.672        |
|              |
|              |
| =            |
| 0.296        |
| P            |
| =            |
| 0.136        |
|              |
| x            |
| =            |
| 0.8375       |
|              |
|              |
| =            |
| 0.228        |
| ǫ            |
| =            |
| 0.001        |
| P            |
| =            |
| 0.215        |
| x            |
| =            |
| 0.685        |
|              |
| =            |
| 0.294        |

| 平衡点       |
|--------------|
|              |
| 1            |
| =            |
| 0.0233       |
|              |
| 2            |
| =            |
| 0.1866       |
| 垄断竞争均衡   |
| p            |
| 1            |
| =            |
| π            |
| 1            |
| =            |
| 2/49         | 
...
（以下省略）

Gabszewicz and Wauthy's model In contrast with the previous model, the Gabszewicz and Wauthy's model20 considers vertical differentiation between the platforms. However, this is not the only difference. The essential difference is that this model presents three different equilibria in the duopolistic framework. These equilibria are also different than the previous ones. They do not depend on parameters values. Each price-equilibrium is defined by constant prices and demands. Table 10 shows the different equilibria found by Gabszewicz and Wauthy. However, some of those equilibria are not stable, and the simulations are affected by this feature.

与之前的模型相比，Gabszewicz和Wauthy的模型考虑了平台之间的垂直差异。然而，这并不是唯一的区别。该模型在寡头竞争框架下呈现出三种不同的均衡状态，与之前的模型也有所不同。这些均衡状态不依赖于参数值，而是由恒定的价格和需求来定义。Gabszewicz和Wauthy发现了不同的均衡状态，并在表10中进行了展示。然而，其中一些均衡状态并不稳定，并且模拟结果受到此特征的影响。

Let's prove that some of those equilibria are not stable. On the one hand, the duopolistic equilibrium is not stable. If any company fixes a zero price on one side and the monopoly price on the other side, this deviation is profitable. If any company deviates, the other one will abandon the market.21 If we analyze the other equilibria, only the 
"Monopoly equilibrium" is stable.22 This happens because Gabszewicz and Wauthy assume "passive beliefs". That implies that when a platform changes prices on one side, the other side does not change their expectations immediately. So, it is always profitable a deviation from the zero price because, given the passive beliefs, the platforms earn an extra profit from deviating. And once they have moved from that equilibrium and the expectations have changed, they will move to the "Monopoly equilibrium" to keep their profits.

让我们证明其中一些均衡状态是不稳定的。首先，寡头垄断的均衡状态是不稳定的。如果任何一家公司在一侧设定零价格，在另一侧设定垄断价格，这种偏离将带来利润。如果任何一家公司偏离，另一家将退出市场。21 对于其他均衡状态的分析表明，只有“垄断均衡”是稳定的。22 这是因为Gabszewicz和Wauthy假设了“被动信念”。这意味着当一个平台在一侧改变价格时，另一侧不会立即改变他们的期望。因此，从零价格偏离总是有利可图的，因为根据被动信念，平台可以从偏离中获得额外利润。而且一旦他们从那个均衡状态移开并且期望发生了变化，他们将转向“垄断均衡”以保持他们的利润。

In this case, the theoretical equilibrium is a constant value, so we present in Table 11 
the simulation results with different ǫ-values and the theoretical equilibrium values. As we stated in the "Vertical differentiation model" section, the vertical differentiation can have dramatic effects on the equilibrium because it may lead to big changes. In the case of indirect network effects and vertical differentiation, those changes can be even more dramatic. For example, when ǫ = 0.01 or ǫ = 0.005 the model collapses to the Bertrand equilibrium (which is another possibility considered by the authors). This result is a consequence of the extreme sensitivity of the model to changes, and the existence of several equilibria.

在这种情况下，理论均衡是一个恒定值。因此，我们在表11中呈现了不同ε值的模拟结果和理论均衡值。正如我们在“垂直差异化模型”部分所述，垂直差异化可能对均衡产生重大影响，因为它可能导致巨大变化。而在间接网络效应和垂直差异化的情况下，这些变化甚至更加剧烈。例如，当ε = 0.01或ε = 0.005时，模型将崩溃至Bertrand均衡（这也是作者考虑的另一种可能性）。这一结果源于模型对变化极其敏感以及存在多个均衡的特点。

As we move towards small ǫ-values, the monopoly equilibrium becomes the predominant outcome. However, in comparison with other models, it seems that there is a big divergence in demands but not in prices. This characteristic is a consequence of the simulation model. While the theoretical model considers an infinite amount of consumers uniformly distributed, our model only considers 314. That implies that one percent change in the γ and θ parameters represents 1% of population in the theoretical model, but 1.3% of population in the simulated model. This small difference leads to a huge difference between the demands of the theoretical and the simulated model because the vertical differentiation. Again, these results show the relevance of testing different ǫ-values. In comparison with previous models, testing different ǫ-values does not change the equilibrium pointed out by the simulations. But in this case, different equilibria appear when choosing different ǫ-values. All of them are equilibria of the theoretical model. So, testing different ǫ-values helps us to identify global equilibria as it was argued before.

随着我们逐渐接近较小的ε值，垄断均衡成为主要结果。然而，与其他模型相比，需求存在很大的分歧，但价格没有。这一特点是由于我们的模拟模型所导致的。理论模型假设有一个均匀分布的无限数量消费者，而我们的模型只考虑了314个消费者。这意味着在理论模型中，γ和θ参数的1%变化代表人口的1%，而在模拟模型中则代表人口的1.3%。由于垂直差异化，这种微小差异导致了理论和模拟模型之间需求巨大差异。再次强调测试不同ε值的重要性。与先前的模型相比，测试不同ε值并不改变仿真所指出的均衡状态。但在这种情况下，在选择不同ε值时会出现不同均衡状态。它们都是理论模型中的均衡状态。因此，测试不同ε值有助于我们确定全局均衡状态，正如之前所提到的那样。

Warranties model In this case, the theoretical model predicts two different equilibria when there are warranties and when there is no warranty. If there is no warranty, both companies fix the same price (p = (ρ1 + (1 − ρ)2)r), but if warranties are used, consumers can identify the quality of each company and prices will be different (p1 ≤ r, p2 = 2r). However, in the last case, only the high-quality company remains in the market. For simplicity's sake and without loss of generality, we analyze the former case.23
In Fig. 8, we depict the theoretical prices and the average simulated ones with different values of 1. In Fig. 9, we observe the theoretical price and two simulated prices during the first 50 iterations. In this model, prices are not always stable at a specific point, but they oscillate around that point. This oscillating pattern is due to the discrete nature of the algorithm, that is applied in a continuous environment that is quite sensitive to small changes.

在这种情况下，理论模型预测当存在保修和不存在保修时会出现两种不同的均衡状态。如果没有保修，两家公司会设定相同的价格（p = (ρ1 + (1 − ρ)2)r），但如果使用了保修，消费者可以识别出每家公司的质量，价格将会有所不同（p1 ≤ r, p2 = 2r）。然而，在后一种情况下，只有高质量的公司能够留在市场上。为了简化问题并且不失一般性，我们将分析前一种情况。

在图8中，我们展示了理论价格和不同值下的平均模拟价格。在图9中，我们观察到了理论价格和前50个迭代期间的两个模拟价格。在这个模型中，价格并不总是稳定在一个特定点上，而是围绕该点波动。这种波动模式是由于算法离散性质在连续环境中对微小变化非常敏感所致。

To test if simulated prices are able to reproduce the theoretical prices accurately, we run a linear regression in which the dependent variable is the theoretical price, and the explanatory variable is the simulated one. In Table 1, we observe that, in both cases, the r-squared is around 99%, so our simulated prices are able to explain 99% of the variations in theoretical prices. Nonetheless, in this case, we have seven observations only, so we cannot test the normality of these cases properly.24 However, Figs. 8 and 9 leave little room for doubt that the algorithm is capable of simulating the theoretical optimal prices.

为了准确复现理论价格，我们进行了一项线性回归分析，将理论价格作为因变量，模拟价格作为自变量。从表1中可以看出，在两种情况下，R平方约为99%，说明我们的模拟价格能够解释理论价格变动的99%。然而，由于观测值仅有七个，我们无法对这些情况进行正态性检验。尽管如此，图8和图9几乎毫无疑问地证明了该算法能够成功模拟出理论上的最优价格。

However, the algorithm presents two limitations in this model. First, sometimes the algorithm is not capable of reaching the equilibrium and predicts a situation in which all companies abandon the market. This happens because of the discrete nature of the algorithm, small changes in the parameters correct this situation, e.g. instead of using 
1 = 0.89, use 1 = 0.9. Second, extreme cases such as ρ = 0 or ρ = 1 will not work. This is a limitation of the current model because it is not programmed to consider the cases in which the model converges to others with full information.

然而，在该模型中，该算法存在两个限制。首先，有时候算法无法达到均衡状态，并预测所有公司都退出市场的情况。这是由于算法的离散性质所导致的。通过微小的参数变化可以纠正这种情况，例如将1设为0.9而不是0.89。其次，极端情况如ρ = 0或ρ = 1将无法奏效。这是当前模型的一个局限性，因为它没有编程考虑到模型收敛到具有完全信息的其他情况。

Relaxation of assumptions and extensions. New directions in agent‑based modeling Up to now, we have considered the theoretical models under their original assumptions. However, we can use the algorithm to address cases in which some assumptions are relaxed or even cases that are out of the reach of theoretical models. For instance, we can consider the market is not covered, utility functions are not linear, users are distributed following a normal, an exponential, or any other distribution, etc. In all of those cases, the algorithm works properly. We can even include new layers of complexity by 

放宽假设和扩展：基于主体建模的新方向
迄今为止，我们一直在考虑在其原始假设下的理论模型。然而，我们可以利用算法来处理一些放宽了某些假设甚至超出了理论模型范围的情况。例如，我们可以考虑市场未覆盖、效用函数非线性、用户按照正态分布、指数分布或其他任何分布进行分布等等。在所有这些情况下，算法都能正常运行。我们甚至可以通过引入新的复杂性层次来进一步扩展模型。

| Variable                       |   Coefficient (std. err.) |
|--------------------------------|---------------------------|
| (a) Warranties, Iteration 0.1  |                           |
| Simulated price                |                           |
| 0.9756                         |                           |
| ∗∗                             |                           |
| (0.0111)                       |                           |
| N                              |                         7 |
| R                              |                           |
| 2                              |                           |
| 0.9992                         |                           |
| F                              |                           |
| (                              |                           |
| 1,6                            |                           |
| )                              |                           |
| 7621.27                        |                           |
| (b) Warranties, Iteration 0.05 |                           |
| Simulated price                |                           |
| 0.9304                         |                           |
| ∗∗                             |                           |
| (0.008)                        |                           |
| N                              |                         7 |
| R                              |                           |
| 2                              |                           |
| 0.9996                         |                           |
| F                              |                           |
| (                              |                           |
| 1,6                            |                           |
| )                              |                           |
| 14,831.19                      |                           |

| 变量                           | 系数 (标准误差) |
|--------------------------------|-----------------|
| (a) 保修, 迭代 0.1              |                 |
| 模拟价格                       |                 |
| 0.9756                         |                 |
| ∗∗                             |                 |
| (0.0111)                       |                 |
| N                              |               7 |
| R                              |                 |
| 2                              |                 |
| 0.9992                         |                 |
| F                              |                 |
|(                               |                 |
| 1,6                            |                 |
|(                               )                ||
|(b) 保修, 迭代 0.05             ||                ||
||模拟价格                      ||                ||
||0.9304                        ||                ||
||∗∗                            ||                ||
||(0.008)                       ||                ||
||N                             ||              7||
||R                             ||                ||
||2                             ||                ||
||0.9996                        ||                ||
||F                             ||                ||
||(                               )               ||
||(1,6                            )               ||
||(                               )               ||
||(14,831.19                      )               ||

assuming more than two companies, or by assuming that users are heterogeneous in several dimensions. In this section, we consider two different cases in which we relax such assumptions.

在这一部分中，我们考虑了两种不同的情况，其中我们放宽了这些假设，即假设有两个以上的公司，或者假设用户在几个维度上是异质的。

First, we simulate the Hagiu and Halaburda's model presented in "Hagiu and Halaburda's model" section, but this time we test the model outside of the parameter region defined by the authors. What is relevant about that region is that the theoretical model predicts negative profits, which is not realistic because platforms will prefer to fix zero prices in both sides than to lose money.

首先，我们对Hagiu和Halaburda在“Hagiu和Halaburda的模型”部分中提出的模型进行了仿真，但这次我们在作者定义的参数区域之外进行了模型测试。该区域的重要性在于理论模型预测了负利润，然而这并不现实，因为平台更倾向于在两个方面都设定零价格，而不是亏本经营。

Second, we simulate the Hoteling's model presented in "Horizontal differentiation: the Hotelling framework" section, but this time we assume that not all the consumers enter the market at the same time. In fact, we assume that there is diffusion of information process that determines who enters the market and when.

其次，我们对“水平差异化：Hotelling框架”部分中提出的Hoteling模型进行了仿真，但这次我们假设并非所有消费者同时进入市场。实际上，我们假设存在一种信息扩散过程来确定谁何时进入市场。

Lastly, we briefly show how this algorithm can address other theoretical models in the industrial organization literature that are based on quantity competition or consider a two-stage competition (dynamic frameworks). I consider those models as extensions of the price competition algorithm, but not as extensions of the other theoretical frameworks.

最后，我们简要展示了这个算法如何应用于工业组织文献中基于数量竞争或考虑两阶段竞争（动态框架）的其他理论模型。我认为这些模型是价格竞争算法的扩展，而不是其他理论框架的扩展。

Relaxed assumptions: Hagiu and Halaburda's model One of the assumptions of this model to guarantee that "all optimization problems with competing platforms are well-behaved" is t2 > δ2, Eq. 3. If we assume this condition does not hold, the theoretical model predicts negative profits. Obviously, this is not optimal because a better option is to fix zero prices or to abandon the market, which guarantees zero profits.

放宽的假设：Hagiu和Halaburda的模型
该模型假设中的一个条件是确保“所有具有竞争平台的优化问题都是良好行为”，即t2 > δ2，见方程3。若我们假设此条件不成立，理论模型将预测出负利润。显然，这并非最佳选择，因为更好的选项是将价格定为零或者退出市场，以确保利润为零。

If we consider that such assumption does not hold and we run the algorithm, platforms always find that prices near zero are an equilibrium.25 In Table 13, we consider two different starting prices for the algorithm (− 0.05 and 0.25) and two different scenarios.26 We find that simulated profits make more sense than their counterparts, the theoretical ones. The algorithm is capable of finding the best outcome in those cases in 

如果我们不考虑这种假设并运行算法，平台总是会发现接近零的价格是一个均衡点。在表13中，我们考虑了两个不同的算法起始价格（-0.05和0.25）以及两种不同的情景。我们发现，模拟利润比理论利润更具意义。在这些情况下，算法能够找到最佳结果。

| Variables/cases     |   Starting price |   Deltas | Transportation    |
|---------------------|------------------|----------|-------------------|
| costs               |                  |          |                   |
| Equilibrium prices  |                  |          |                   |
| users (developers)  |                  |          |                   |
| Equilibrium profits |                  |          |                   |
| Simulated case      |             0.25 |     0.65 | 0.15              |
| −                   |                  |          |                   |
| 0.05 (0.15)         |             0.05 |          |                   |
| −                   |                  |          |                   |
| 0.05                |             0.65 |     0.15 | 0.05              |
| −                   |                  |          |                   |
| 0.05                |             0.8  |     0.4  | 0.05 (            |
| −                   |                  |          |                   |
| 0.05)               |             0    |          |                   |
| Theoretical case    |                  |          |                   |
| 0.65                |             0.15 |          |                   |
| −                   |                  |          |                   |
| 0.5                 |                  |          |                   |
| −                   |                  |          |                   |
| 0.5                 |                  |          |                   |
| 0.8                 |             0.4  |          |                   |
| −                   |                  |          |                   |
| 0.4                 |                  |          |                   |
| −                   |                  |          |                   |
| 0.4                 |                  |          |                   |

| 变量/情景         | 起始价格 | 增量 | 运输费用 |
|-----------------|----------|------|---------|
| 成本              |          |      |         |
| 均衡价格         |          |      |         |
| 用户（开发者）   |          |      |         |
| 均衡利润         |          |      |         |
| 模拟情景         | 0.25     | 0.65 | 0.15    |
|-                |-         |-     |-        |
|-                |-         |-     |-        |
|-                |-         |-     |-        |
|-                |-         |-     |-        |
|-                |-         |-     |-        |
|-                |-         |-     |-        |
|-                |-         |-     |-        |
|-                |-         |-     |-        |
|-                |-         |-     |-        |
|--               |--        |--    |--       |
|--               |--        |--    |--       |
|--               |--        |--    |--       |

注意：为了保持准确性和学术风格，我保留了原文中的空行和破折号。

which the theoretical model provides unsatisfactory results. This result implies the algorithm can be used as a verification tool for theoretical models but also, it can be used to deal with cases that are theoretically complex or non-tractable.

这一结果意味着该算法可以作为理论模型的验证工具，并且还可以用于处理在理论上复杂或难以处理的情况。

Relaxed assumptions: Hotelling's model This case represents a Hotelling model in which consumers are entering the market in a non-random way. We assume that only a small percentage of consumers can enter the market in the first iteration (all of them are less than one node away from one another). Then, those consumers can transmit the information about the product they consume to others neighbors in their networks in the following iterations.27 For simplicity's sake, we assume that users are linked in a random network. We assume there are two companies, and consumers can be in one of these states: uninformed, totally informed or partly informed about one company. In other words, this case mixes the spread of information in a network with two price-competing companies trying to attract consumers.28
On the left side of Fig. 10, simulations show that prices are more volatile. This behavior is normal because new users are entering the market at each moment. Companies try to adjust prices to the expansion of the market, but companies are also competing, so they try to reduce prices. Prices only reach a stable position in the case with low differentiation because the competition is stronger than the expansion effect (new users).

放宽的假设：Hotelling模型
本案例代表了Hotelling模型，其中消费者以非随机方式进入市场。我们假设在第一次迭代中只有少部分消费者能够进入市场（它们之间相距不到一个节点）。随后，这些消费者可以在后续迭代中向其网络中的其他邻居传递他们所消费产品的信息。为简化起见，我们假设用户之间是通过随机网络连接的。我们假设存在两家公司，消费者可以处于以下状态之一：未知、完全知晓或部分知晓其中一家公司。换言之，本案例将网络中信息传播与两家价格竞争的公司吸引消费者相结合。
图10左侧的模拟结果显示价格更加波动。这种行为是正常的，因为新用户每时每刻都在进入市场。公司试图根据市场扩张来调整价格，但它们也在竞争，因此试图降低价格。只有在差异化较低的情况下，价格才能达到稳定位置，因为竞争力大于市场扩张效应（新用户）。

On the right side of Fig. 10, simulations show the case with low differentiation is the only one that reaches a point where adoption is not growing anymore (the expansion effect is over, almost all the potential consumers are attracted). However, the other two cases are so volatile because the spread of information is less regular and slower than before.

在图10的右侧，模拟结果显示差异化较低的情况是唯一一个达到不再增长的采纳点（扩张效应结束，几乎吸引了所有潜在消费者）。然而，其他两种情况非常不稳定，因为信息传播比之前更加不规律和缓慢。

We can observe too that high prices are a barrier that blocks other users from becoming consumers, which limits the adoption. When prices are high, some users do not consume the products although they know them. This limit the spread of information which leads to stopping the diffusion. On the other hand, users only know about the individual products, so there are cases in which users are only aware of one product and, because information initially spreads from clusters, there will be clusters that will never know about the existence of other companies. In this situation, there is volatility in prices and adoption because there is a trade-off between rising prices (because of the differentiation levels and larger profits) and reducing prices (because of the competition between platforms and the boosting effect that it has on the demands).

我们还可以观察到，高价格成为了其他用户成为消费者的障碍，从而限制了采纳的范围。当价格居高不下时，尽管一些用户对产品有所了解，却选择不消费。这种情况限制了信息的传播，导致扩散停滞。另一方面，用户只能了解到个别产品，因此存在一些情况下用户只知道某一家公司的存在，并且由于信息最初是从集群中传播的，会有一些集群永远不会知道其他公司的存在。在这种情况下，价格和采纳率存在波动，因为需要在差异化水平和更大利润之间进行权衡，并且在平台之间的竞争以及对需求的推动效应上降低价格。

Extension 1: the perfect competition framework. Competition in quantities Although we assume the algorithm can be applied to simulate price competition, it can also simulate quantity competition. To prove this point, we test a small modification of the algorithm. This is the simplest model of quantity competition. It assumes there is a large number of companies and consumers, all of them are so small with respect to the market that no one can influence the market. So, every participant is a price taker. In that sense, consumers have to choose how many products they want to buy (given a fixed level of rent), and companies have to choose how many products they will produce at given prices. For simplicity's sake, we consider only two companies (but we can consider any other number). In this case, we consider the utility functions defined by [Belleflamme and Peitz (2015), Page 65]. In particular, the utility function takes the form

扩展1：完全竞争框架。数量竞争尽管我们假设该算法可用于模拟价格竞争，但它也可以模拟数量竞争。为了证明这一点，我们对算法进行了小的修改测试。这是数量竞争的最简单模型，假设存在大量的公司和消费者，它们相对于市场来说都非常小，没有人能够影响市场。因此，每个参与者都是价格接受者。在这种情况下，消费者必须根据固定租金水平选择购买多少产品，而公司必须根据给定的价格选择生产多少产品。为简化起见，我们只考虑两家公司（但我们可以考虑任意其他数量）。在这种情况下，我们采用由Belleflamme和Peitz（2015）在第65页定义的效用函数形式。

$$U(q_{1},q_{2})=1+a q_{1}+a q_{2}-(b q_{1}^{2}+2d q_{1}q_{2}+b q_{2}^{2})/2$$
We consider companies can produce natural quantities of each product (1,2,3,..), and they sell their products at a fixed price.29 Depending on the values of b and d, we can address several cases considering complements or substitutes. In Table 14, we compare different cases. In all of them, the algorithm points out that the consumers' decisions about their quantities are the optimal ones.30
For example, when d = 0 and b = 1, it is optimal for consumers to buy products from both companies. So, both companies will produce enough products for all the 

我们假设公司可以按照自然数量（1、2、3等）生产各种产品，并以固定价格销售。根据参数b和d的不同取值，我们可以考虑几种情况，包括互补或替代关系。在表14中，我们对不同情况进行了比较。在所有这些情况下，算法指出消费者关于产品数量的决策是最优的。

举例来说，当d = 0且b = 1时，对于消费者来说从两家公司购买产品是最佳选择。因此，两家公司将生产足够的产品以满足所有消费者的需求。

Parameter values at a = 1
Quantities consumed
Parameter values at a = 1
Quantities consumed
d = 0; b = 1
q1 = q2 = 1
d = 0.7; b = 1
q1 = 1 or q1 = 0
q2 = 0 or q2 = 1
d = 0.7; b = 0
q1 = q2 = 1
d = b
q1 = 1 or q1 = 0 q2 = 0 or q2 = 1
d = − 1; b = 0
q1 = q2 = 1
d = 0.1; b = 1
q1 = q2 = 1
d = − 1; b = 1
q1 = q2 = 1
d = 0.2; b = 1
q1 = q2 = 1

在a = 1的参数值下，
消费数量
在a = 1的参数值下，
消费数量
当d = 0；b = 1时，
q1 = q2 = 1
当d = 0.7；b = 1时，
q1可以等于1或者等于0
q2可以等于0或者等于1
当d=0.7；b=0时，
q1=q2=1 
当d=b时，
q1可以等于1或者等于0，q2可以等于0或者等于1
当d=-l;b=O时，
q, q, l=l 
当d=l; b=l时，
q, q, l=l 
当d=O.2;b=l时，
q, q, l=l

consumers. But when d = b, consumers only demand one product, and only one company will produce it.

消费者。但是当d = b时，消费者只需求一种产品，只有一家公司会生产它。

Extension 2: Milgrom–Roberts Models of barriers to entry The algorithm is flexible, and it can deal with dynamic frameworks. To test this statement, we chose the Milgrom–Roberts model.31 The model assumes two stages: At the first stage, there is a monopoly that produces a good with a marginal cost that may be high ch or low cl. The information about the cost is not available outside of the monopoly. 

扩展2：米尔格罗姆-罗伯茨模型对进入壁垒的研究
该算法具有灵活性，能够应对动态框架。为了验证该论断，我们选择了米尔格罗姆-罗伯茨模型。该模型假设存在两个阶段：第一阶段是一个垄断市场，生产一种商品，其边际成本可能是高ch或低cl。关于成本的信息在垄断市场之外是不可得知的。

At the second stage, an entrant has the opportunity to enter the market. However, his/ her decision of entering depends on the marginal cost of the incumbent and on its own marginal costs ce. If the cost of the incumbent is high, the entrant will have positive profits; if the cost is low, the entrant will have negative profits.

第二阶段，一个新进入者有机会进入市场。然而，他/她的决策是否进入取决于现有企业的边际成本以及自身的边际成本ce。如果现有企业的成本很高，新进入者将获得正利润；如果成本很低，新进入者将获得负利润。

The original model considers two different equilibria: the separating one and the pooling one. For simplicity's sake and without loss of generality, we focus on the pooling one.32 This equilibrium predicts that the incumbent will block the market forever. Independently of the high or low marginal costs. This happens if the Eq. 7 holds. This equation states that the duopoly profits of the entrant when the incumbent has high costs must be larger than zero. But they must be negative with low costs, [Tirole and Matutes (1990), Condition 9.8]

该原始模型考虑了两种不同的均衡状态：分离均衡和汇聚均衡。为了简化问题并不失一般性，我们将重点关注汇聚均衡。根据该均衡，现有企业将永远阻止市场进入，无论边际成本高低。这一结果是在等式7成立的情况下得出的。等式7表明，在现有企业成本较高时，新进入者的垄断利润必须大于零；而在成本较低时，这些利润必须为负值[Tirole and Matutes (1990), Condition 9.8]。

$$c_{l}<c_{e}<c_{h}\tag{7}$$
If this equation does not hold, for example, if the entrant has lower marginal costs than the incumbent with low marginal cost. The entrant will always enter the market, and two outcomes are possible:

如果等式不成立，例如，如果新进入者的边际成本低于现有企业的边际成本。那么新进入者将始终进入市场，并且可能出现两种结果：

  •
Competition: if both have low costs and profits are non-negative.
  •
Expulsion: the incumbent will be expelled from the market
In Table 15, we observe the outcome of the simulated model. The idea is to have an intuition of how works the algorithm in this model. We consider two cases. One in which the incumbent has high marginal costs. And another one in which it has low marginal costs. In all those cases, the result predicted by the agent-based model is the same than the one predicted by theory.

在表15中，我们观察到了模拟模型的结果。这个模型旨在让我们对算法在该模型中的工作方式有一个直观的理解。我们考虑了两种情况：一种是现有企业具有较高的边际成本，另一种是具有较低边际成本。在所有这些情况下，基于主体的模型预测的结果与理论预测的结果相同。

| Market outcome        | Parameters values    |
|-----------------------|----------------------|
| when                  |                      |
| c                     |                      |
| incumbent             |                      |
| =                     |                      |
| c                     |                      |
| h                     |                      |
| Market outcome        | Parameters values    |
| when                  |                      |
| c                     |                      |
| incumbent             |                      |
| =                     |                      |
| c                     |                      |
| l                     |                      |
| Duopoly competition   |                      |
| c                     |                      |
| l                     |                      |
| =                     |                      |
| 0.1                   |                      |
| ;                     |                      |
| c                     |                      |
| h                     |                      |
| =                     |                      |
| 0.84                  |                      |
| c                     |                      |
| e                     |                      |
| =                     |                      |
| 0.1                   |                      |
| Incumbent is expelled |                      |
| c                     |                      |
| l                     |                      |
| =                     |                      |
| 0.1                   |                      |
| ;                     |                      |
| c                     |                      |
| h                     |                      |
| =                     |                      |
| 0.84                  |                      |
| c                     |                      |
| e                     |                      |
| =                     |                      |
| 0.1                   |                      |
| Incumbent is expelled |                      |
| c                     |                      |
| l                     |                      |
| =                     |                      |
| 0.1                   |                      |
| ;                     |                      |
| c                     |                      |
| h                     |                      |
| =                     |                      |
| 0.84                  |                      |
| c                     |                      |
| e                     |                      |
| =                     |                      |
| 0.2                   |                      |
| Incumbent is expelled |                      |
| c                     |                      |
| l                     |                      |
| =                     |                      |
| 0.3                   |                      |
| ;                     |                      |
| c                     |                      |
| h                     |                      |
| =                     |                      |
| 0.84                  |                      |
| c                     |                      |
| e                     |                      |
| =                     |                      |
| 0.1                   |                      |
| Block to entry        |                      |
| c                     |                      |
| l                     |                      |
| =                     |                      |
| 0.1                   |                      |
| ;                     |                      |
| c                     |                      |
| h                     |                      |
| =                     |                      |
| 0.84                  |                      |
| c                     |                      |
| e                     |                      |
| >                     |                      |
| 0.2                   |                      |
| Block to entry        |                      |
| c                     |                      |
| l                     |                      |
| =                     |                      |
| 0.1                   |                      |
| ;                     |                      |
| c                     |                      |
| h                     |                      |
| =                     |                      |
| 0.84                  |                      |
| c                     |                      |
| e                     |                      |
| >                     |                      |
| 0.2                   |                      |

市场结果 | 参数值
-----------------------|----------------------
当 | c
现有企业 | = 
c | h
市场结果 | 参数值
当 | c
现有企业 | = 
c | l
双头垄断竞争 |
c | l
= |
0.1 |
; |
c |
h |
= |
0.84 |
c |
e |
= |
0.1 |

现有企业被驱逐| 
c|
l|
=|
0.1|
;|
c|
h|
=|
0.84|
c|
e|
=|
0.1|

现有企业被驱逐| 
c| 
l| 
=| 
0.1| 
;| 
c| 
h| 
=| 
0.84|  
c|  
e  |=  
  0.2   |

现有企业被驱逐   |   
 c    |   
 l    |=   
  0.3   ||                     
 ;     ||                     
 c     ||                     
 h     ||=                    
  0.84   ||                    
 c     ||                     
 e     ||=                    
  0.1   ||
进入受阻止||
 c    ||
 l    ||=   
  0.1   ||
 ;     ||
 c     ||
 h     ||=    
  0.84   ||
 c      ||
 e      |>    
   0.2    ||
进入受阻止||
 c    ||     
 l    ||=    
   0..1||     
 ;      ||     
 c      ||     
 h      ||=    
   o..84||     
 ce       |>    
    o..2||

Discussion. Similarities and dissimilarities between the algorithm and other approaches The proposed algorithm resembles the optimization programs that are used in Economic Theory or Game Theory. In these cases, it is common to compute an optimization program from which the first and second order conditions are derived to identify the reaction functions and the equilibria. The algorithm is closely related to the idea of reaction functions. However, there are relevant similarities and differences. On the one hand, the algorithm acts in a similar way than reaction functions; the output of both is the best reply to a specific situation, and the continuous interaction of reaction functions or agents with the algorithm leads to the Nash equilibria. If it does not exist, the algorithm can find corner solutions or second best equilibria.33
On the other hand, there are three relevant differences in comparison with the classical optimization programs used in Economics:

讨论。算法与其他方法的相似性和差异性。所提出的算法类似于经济理论或博弈论中使用的优化程序。在这些情况下，通常会计算一个优化程序，从中导出一阶和二阶条件以确定反应函数和均衡点。该算法与反应函数的思想密切相关。然而，存在相关的相似性和差异性。一方面，该算法与反应函数类似；两者的输出都是对特定情况的最佳回应，并且反应函数或主体与算法之间的持续交互导致纳什均衡点。如果不存在纳什均衡点，则该算法可以找到边界解或次优解33。
另一方面，与经济学中使用的传统优化程序相比，存在三个重要差异：

  •
First, the algorithm does not provide a stylized expression that represents the equilibria. It computes a numerical one.
  •
Second, tractability is not an issue. Traditionally, researchers assume some assumptions like linear demands, constant values, continuity of functions, concave profits functions, etc. that may not be realistic. This is done to guarantee tractability and well-behaved equilibria. However, that is not necessary with the algorithm. If there is no equilibrium, the algorithm chooses a second-best solution (one which produces the most favorable outcome for the agent, taking other agents' strategies as given). In some cases, several second-best solutions can be found, in such cases, the algorithm may pivot from one to another. But, if the equilibrium is global, the algorithm will prove that by showing always the same outcome.
  •
Third, we do not assume continuity or differentiability. The algorithm is discrete, and it approximates a continuous environment.
There are other features that make the algorithm interesting. For example, the algorithm puts emphasis in the process of reaching the equilibrium, and not in the equilibrium itself. This allows us to study the impact of shocks not only in the equilibrium but also, in the process of reaching it. Nonetheless, the most important contribution is the possibility of relaxing assumptions and guarantying the optimality of results at the same time. In this way, we can introduce new dimensions that were quite complicated in theoretical models, such as introducing a network structure among the consumers.

首先，该算法并不提供一个能够代表均衡的简化表达式，而是计算出一个数值解。

其次，可行性并不是一个问题。传统上，研究人员会假设一些条件，如线性需求、恒定值、函数连续性、凹利润函数等等，尽管这些假设可能并不现实。这样做是为了保证模型的可行性和均衡结果的良好性质。然而，在该算法中，并不需要这样做。如果不存在均衡点，该算法会选择次优解（即在其他参与者策略给定的情况下产生最有利结果的解）。在某些情况下，可能存在多个次优解，在这种情况下，算法可以从一个解转移到另一个解。但是，如果存在全局均衡，则该算法将始终显示相同的结果来证明全局均衡。

第三，我们并不假设连续性或可微性。该算法是离散的，并且对连续环境进行了近似。

该算法还具有其他有趣的特点。例如，该算法强调达到均衡的过程而非均衡本身。这使得我们能够研究冲击对达到均衡过程以及均衡本身的影响。然而，最重要的贡献是能够在放松假设的同时保证结果的最优性。通过这种方式，我们可以引入在理论模型中相当复杂的新维度，例如在消费者之间引入网络结构。

Nonetheless, some researchers may argue that the algorithm is not different than solving the model numerically. However, this is not true. To solve a model numerically requires solving the theoretical model analytically in advance in most of the cases,34 but with this algorithm, that is not necessary. The algorithm does not assume that agents make complicated mathematical manipulations. It consists of simple actions (consumers make their best decision, the one that maximizes their utility: buy one of the product or not; and companies increase, decrease or maintain prices, what it is more profitable at each time), and we prove that, with those simple actions, the theoretical equilibria predicted by many theoretical models can be reached.

然而，一些研究人员可能会争辩说，该算法与数值求解模型没有区别。然而，这种观点是不正确的。在大多数情况下，通过数值方法解决一个模型需要事先在理论上进行解析求解34，但是使用这个算法则不需要。该算法并不假设主体进行复杂的数学运算。它由简单的行动组成（消费者做出最佳决策，即最大化他们的效用：购买产品或不购买；公司根据每个时间点的利润情况来增加、减少或保持价格），我们证明了通过这些简单的行动可以达到许多理论模型预测的理论均衡状态。

I am not the first one in considering theoretical models for agent-based simulations. 

我并不是第一个考虑基于主体模拟的理论模型的人。

But this is the first time that an algorithm reproduces the optimizing behavior of agents like in theoretical economic models. So, it is possible to build agent-based models that are closely linked to traditional economics by using economic intuitions. I do not pretend to present the agent-based modeling as an alternative to the traditional industrial organization literature. Instead, this work presents the agent-based modeling as a complement of that literature. If we can agree that the rules presented in "The algorithm" 
section represent the same rules that we take as given (or we assume) in the consumer's and company's decision problems. Then, we can agree that the algorithm is a representation of the process of maximization of utility (profits) of users (and companies).

然而，这是第一次有一个算法能够模拟出像理论经济模型中那样的主体优化行为。因此，通过运用经济直觉，我们可以构建与传统经济学密切相关的基于主体的模型。我并不打算将基于主体模拟作为传统产业组织文献的替代品来呈现。相反，本研究将基于主体模拟作为该文献的补充。如果我们可以认同在“算法”部分中提出的规则代表了我们在消费者和公司决策问题中所假设或认定的规则，那么我们可以认为该算法是用户（和公司）效用（利润）最大化过程的一种表征。

Nonetheless, the algorithm I propose is also criticizable. It is a tool designed to look for local equilibria. So, to address global equilibria, it requires different starting points, different number of iterations or even different discrete "jumps (ε)" in prices. If not, we are at risk of identifying local optima that are not the global ones.

然而，我所提出的算法也存在批评的空间。它是一种旨在寻找局部均衡的工具。因此，为了解决全局均衡问题，它需要采用不同的起始点、不同数量的迭代甚至不同离散“跳跃（ε）”价格。如果没有这样做，我们有可能仅识别出局部最优解而非全局最优解。

Conclusions We develop an algorithm for agent-based models that simulates the behavior of pricecompeting companies. This algorithm considers two sub-algorithms: one for consumers, and another one for companies. The consumers' algorithm specifies that all users will choose that product that provides them with the highest utility. The companies' algorithm specifies that each company will change its prices by a small quantity if they believe that such change is profitable.

结论：我们提出了一种基于主体模型的算法，用于模拟价格竞争公司的行为。该算法包括两个子算法：一个用于消费者，另一个用于公司。消费者的算法规定所有用户将选择能够提供最高效用的产品。公司的算法规定每家公司在认为这样做有利可图时，通过微小调整价格。

We test the price-competition algorithm in several theoretical frameworks such as the Hotelling model, a vertical differentiation model or a two-sided market. In all of them, we prove the algorithm is capable of reaching the equilibria predicted by theory. We also prove that the algorithm works in cases that were not considered by theory, or in parameter regions where the theoretical model was not suitable to be analyzed. These results open the door to implementing endogenous pricing in agent-based models but also, to test theoretical models in a new environment or even to teach theoretical models in a new way.

我们在多个理论框架中对价格竞争算法进行了测试，包括Hotelling模型、垂直差异化模型和双边市场模型。在所有这些框架中，我们证明了该算法能够达到理论预测的均衡状态。此外，我们还证明了该算法适用于理论未考虑的情况，或者在参数区域内，理论模型不适合进行分析的情况下。这些结果为在基于主体的模型中实施内生定价提供了可能性，并且还为在新环境下测试理论模型甚至以新方式教授理论模型提供了机会。

We conclude with a discussion of the current limitations of this research, and how this line of research is related to other approaches used in the Economic literature.


我们最后讨论了这项研究的当前限制，并探讨了这一研究领域与经济学文献中使用的其他方法之间的关系。

