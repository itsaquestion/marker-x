# Worksim, An Agent-Based Model To Study Labor Markets



Abstract. In this paper, we introduce the WorkSim model, a novel agent-based framework to study
labor markets. The first objective of the model is to reproduce the gross flows between the important
states: employment (distinguishing fixed term contracts and open ended contracts), unemployment
and inactivity, and the ratios of individuals in these states. The novelty of the model is that it
simulates the flows on the basis of the rational decisions of individual heterogeneous agents. Once
the model is calibrated, the second objective is to characterize the nature of the labor market
under study. This is done, first by examining the patterns of flows and stocks at the aggregate level
and at the levels of different categories of labor, and second by sensitivity experiments, modifying
some exogenous parameters and variables such as the demand for the good. Finally the model once
calibrated is a tool for experimenting labor market policies, including changes in the labor law in
France.

摘要。本文介绍了WorkSim模型，这是一个新颖的基于主体的框架，用于研究劳动力市场。该模型的首要目标是通过个体异质主体的理性决策来模拟重要状态之间的总流动，包括就业（区分固定期限合同和无固定期限合同）、失业和非活动，并且研究这些状态中个体的比例。该模型的创新之处在于它能够根据个体异质主体的决策行为来模拟流动情况。一旦模型被校准，第二个目标是描述所研究劳动力市场的性质。首先，在整体水平和不同劳工类别水平上检查流动和存量的模式，其次通过敏感性实验修改一些外生参数和变量（如对商品需求）来进行分析。最后，经过校准后的模型可用作实验劳动力市场政策工具，包括法国劳动法的变更。

## 1 Introduction



WorkSim is a novel agent-based framework to study labor markets. The multi-agent methodology is the perfect tool for such a research program, since it can model institutions precisely, and account for heterogeneity and individual interactions. Simulation results enable us to compute aggregate variables such as the flows and the stocks, and finally the individual careers and the main types of trajectories.

WorkSim是一个创新的基于主体的框架，用于研究劳动力市场。多主体方法是研究这一领域的理想工具，因为它能够准确地模拟机构，并考虑到异质性和个体之间的相互作用。通过模拟结果，我们可以计算出诸如流动和存量等聚合变量，最终得出个体职业生涯和主要轨迹类型。

Agents are autonomous and there is then no need for an auctioneer, an unrealistic fiction in orthodox models, and this is has consequences since the labor market is very decentralized. The agents take decisions based on their information and the calculation of costs and benefits, and the profit (for the firms) or utility (for the individuals) they expect. The environment is very complex because of the institutions and the interactions, and changing, and their rationality is bounded in the sense of Simon (1956). Therefore, when in a given state, they choose the best of a few possible solutions (see below for examples). They make mistakes when deciding, but in WorkSim, they can learn and revise their requirements. The institutions and legal rules that constrain the decisions are modeled precisely. The model allows for non-linear relations between aggregate variables, and notably crowding-out effects, often important in labor markets. The computed effects of the present law will bring a resounding example. These models can be calibrated with a varying degree of sophistication, and when the purpose is to study a policy, as in this paper, it is an essential part of the research.

主体是自治的，因此在传统模型中无需拍卖人，这种设想在实际中是不现实的。这一点对于劳动力市场的分散性具有重要影响。主体根据他们的信息、成本和效益计算以及预期的利润（对于企业）或效用（对于个人）做出决策。由于机构和相互作用以及其变化，环境非常复杂，并且他们的理性受到Simon (1956) 的有限制约束。因此，在给定状态下，他们从几种可能解决方案中选择最佳解决方案（请参见下面的示例）。他们在做决策时可能会犯错误，但在WorkSim中，他们可以学习并修订自己的要求。精确地建模了约束决策的机构和法律规则。该模型允许聚合变量之间存在非线性关系，尤其是在劳动力市场中经常出现重叠效应。目前法律计算出来的影响将提供一个引人注目的例子。这些模型可以根据不同程度上进行校准，并且当研究政策时（如本文），它是研究中必不可少的一部分。

## 1.1 Extending Search Theory



WorkSim is grounded in the concept of *search* (Phelps, 1970). Search Theory studies how economic actors find a partner for their transactions (here a company with a job)5. In WorkSim the basic concept of search is extended in three directions, in order to build a general theory of mobility :

WorkSim以“搜索”（Phelps, 1970）的概念为基础。搜索理论研究经济行为者如何寻找他们交易的合作伙伴（在这里是公司与工作）。在WorkSim中，搜索的基本概念在三个方向上得到了扩展，以建立一个关于流动性的普遍理论。

1. *Search is done also by firms* that symmetrically look for workers who are high in
the productivity distribution. They prefer to keep a job vacant than hire a worker with a poor productivity. A stopping rule taking the form of a minimum productivity
requirement or hiring standard follows. Moreover, the addition of the costs of search
may render the job unprofitable (and then it will be suppressed).
2. *The search calculus is extended to all voluntary decisions by workers* such as quits and
on-the-job search (i.e. looking for a new job while remaining employed). The firms take into account the search costs of replacement when they consider firing a worker, for lack of productivity. Finally the hiring decision is the result of the sequential decisions of the worker who applies and the firm which selects and hires. Moreover, unlike matching models, *we do not use any matching function* - like in the canonical model of Mortensen
and Pissarides (1994) - as it is an aggregate artifact, likely not to be robust to large changes in the labor market, and with weaker microeconomic foundations than our
double search decision6.
3. Our model integrates *wage rigidities*7 with the realistic assumption that firms have
often several jobs. It allows for the differentiation between demand shocks and productivity shocks, while existing search models do not often deal with this topic.The model then contains some Keynesian features. Demand shocks explain part-time, dismissals, and job creations in the model, while productivity changes explain dismissals, promotions and some hires. This distinction has also some importance since the model deals only with the labor market, with no feedback on the goods market. The demand for
the goods is exogenous. To make things simple and coherent, we assume that each firm
produces a variety of a unique good with horizontal differentiation, and hence a unique exogenous price. However, *Each firm faces stochastic shocks on its demand*, which can
be seen as fluctuations of consumers' preferences.
However a major difference between WorkSim and the analytical search models relies on our utilization of the concept of Simon's **bounded rationality** to model the decisions
(Simon, 1955). Two major arguments can be given:

1. *公司也会进行搜索*，寻找生产力分布较高的工人。他们更倾向于保持职位空缺，而不是雇佣生产力较低的工人。这种停止规则采取了最低生产力要求或招聘标准的形式。此外，搜索成本的增加可能导致工作无利可图（从而被取消）。

2. *搜索计算扩展到了工人所有自愿决策*，例如辞职和在职搜索（即在保持就业状态下寻找新工作）。当公司考虑解雇一名因为缺乏生产力而需要替换的员工时，他们会考虑到替换的搜索成本。最终的招聘决策是申请者和选择并雇佣员工的公司顺序决策的结果。此外，与匹配模型不同，*我们没有使用任何匹配函数* - 就像Mortensen和Pissarides（1994）经典模型中那样 - 因为它是一个总体构件，在劳动市场发生大变化时可能不稳定，并且比我们双重搜索决策具有更弱微观经济基础。

3. 我们的模型将*工资刚性*与现实假设相结合，即公司通常有多个职位。它允许区分需求冲击和生产力冲击，而现有的搜索模型往往不涉及这个问题。该模型具有一些凯恩斯主义特征。需求冲击解释了兼职、解雇和就业创造，而生产力变化解释了解雇、晋升和一些招聘。这种区分也具有一定的重要性，因为该模型仅涉及劳动市场，对商品市场没有反馈。商品的需求是外生的。为了简化和保持连贯性，我们假设每家公司都生产一种具有水平差异化的独特商品，并且存在唯一的外生价格。然而，*每家公司都面临其需求的随机冲击*，可以看作是消费者偏好的波动。

然而，WorkSim与分析性搜索模型之间一个重要区别在于我们利用Simon提出的**有限理性**概念来建模决策（Simon, 1955）。可以给出两个主要论点：

1. First, dynamic programming algorithms used to solve the decision problem in analytical search theory cannot be used in a model in which heterogeneous agents move sequentially into many states over time and compete.
2. Second, according to bounded rationality theory, real agents have limited capacities in
terms of computation and memory. They might therefore use simple rules, but a very important behavioral addition in our approach is that they can revise their decisions or even their rules thanks to **learning** and collecting information. This continuous
learning is in fact very coherent with search theory. However, in order to compute equilibrium, analytical models assume perfect rationality and individuals have a lot of information such as the true distribution of wages, and firms the true distribution
of productivities. By contrast, in WorkSim, we model "simple" decision rules - that
comply with bounded rationality, partial information and learning processes.

1. 首先，在分析性搜索理论中用于解决决策问题的动态规划算法无法应用于一个模型中，该模型涉及异质个体随时间顺序进入多个状态并进行竞争。

2. 其次，根据有限理性理论，实际个体在计算和记忆方面具有有限能力。因此，他们可能采用简单的规则。然而，在我们的方法中，一个非常重要的行为补充是他们可以通过学习和收集信息来修正他们的决策甚至规则。这种持续学习实际上与搜索理论非常一致。然而，在计算均衡时，分析模型假设完全理性，并且个体拥有大量信息，如工资的真实分布以及企业生产力的真实分布。相比之下，在WorkSim中，我们建模“简单”的决策规则 - 符合有限理性、部分信息和学习过程。

## 1.2 Related Agent-Based Models



The contributions to the multi-agent literature on labor markets must also be assessed. This literature is thin but has a long history. Bergmann (1974) has developed a simple search model by both sides of the market and obtained simultaneously vacant jobs and unemployment. Eliasson (1977) built a Keynesian and Schumpeterian micro-to-macro model which treats only firms as individual agents but the number of workers in a firm can vary and unemployment is computed. ARTEMIS (Ballot, 1981, 2002) , the ancestor of WorkSim, is the first multi-agent model to have modeled the gross flows between the three main states of the individuals, with the addition of on-the-job search as a state. This was also done within an institutional framework, notably with a temporary help firm, and firing costs. The model generates a temporary segmentation of the young workers. Then, a negative demand shock affects very differently the categories of labor, precluding the progressive integration of young workers in the internal labor markets. This will lead to a permanent segmentation with serious life cycle consequences.

对于劳动力市场的多主体文献的贡献也需要进行评估。尽管这方面的文献数量不多，但其历史悠久。Bergmann（1974）提出了一个简单的搜索模型，同时考虑了市场两侧，并得出了空缺职位和失业率的结果。Eliasson（1977）构建了一个凯恩斯和熊彼特式的微观到宏观模型，将企业视为个体主体，但允许企业中工人数量的变化，并计算了失业率。ARTEMIS（Ballot, 1981, 2002），即WorkSim的前身，是第一个模拟个体之间三种主要状态总流动性质的多主体模型，并引入在职搜索作为一种状态。该模型还在制度框架内进行了建模，特别是考虑到临时劳务公司和解雇成本等因素。该模型生成了年轻工人临时分割现象。然后，负面需求冲击对不同类别劳动力产生了截然不同的影响，阻碍了年轻工人逐步融入内部劳动力市场。这将导致永久性分割，并带来严重的生命周期后果。

The years 2000 have mainly seen multi-agents models aiming at theoretical research
(see Neugart et al. (2012) for a recent review), such as introducing networks, a logical way to consider search in some contexts (Tassier and Menczer, 2001). Richiardi (2004) modeled the matching process between workers and firms with on-the- job search, entrepreneurial decisions and endogenous wage determination. Neugart (2008) developed an agent-based labor market model with sector-specific skill requirements. Barlet et al. (2009) simulate the French labor market for year 2006. They distinguish individuals and jobs, but not firms as such although there is labor demand side, with creations and destructions of jobs based on a desired margin and demand.

2000年以来，主要出现了以多主体模型为目标的理论研究（最近的综述可参见Neugart等人，2012年），其中包括引入网络作为在某些情境下考虑搜索的一种逻辑方式（Tassier和Menczer，2001年）。Richiardi（2004年）对工人和企业之间的配对过程进行了建模，包括在职搜索、创业决策和内生工资确定。Neugart（2008年）开发了一个基于主体的劳动力市场模型，具有特定行业技能要求。Barlet等人（2009年）对法国劳动力市场进行了2006年的模拟。他们区分个体和就业岗位，但没有将企业作为独立实体考虑进去，尽管存在劳动需求方面的因素，根据所需利润和需求创建和销毁就业岗位。

[重写后的中文内容:]

WorkSim goes beyond the existing multi-agent literature on the labor markets in three directions:

WorkSim在劳动力市场的多主体文献中有三个方面的创新。

1. It is the only ABM labor model to be grounded in a **double stock-flow accounting**,
one for the individuals, one for the jobs, and most of the important flows are considered. This accounting is the equivalent of the financial stock-flow accounting for ACE macroeconomic models, a guarantee of coherence. It also allows for a easy description
of the labor market dynamics at the aggregate and any disaggregation level of interest, and the highlighting of the competition between categories of labor (young, adults, seniors....).

1. 这是唯一一个以**双重库存流量核算**为基础的ABM劳动力模型，其中一个用于个体，另一个用于就业岗位，并且考虑了大部分重要的流动。这种核算方法类似于ACE宏观经济模型中的金融库存流量核算，确保了模型的一致性。同时，它还能够轻松描述劳动力市场在整体和任何感兴趣的细分水平上的动态，并突出不同劳动力类别之间的竞争（如年轻人、成年人、老年人等）。

2. It models the **institutions and the labor law** at their level of direct impact (the
microeconomic level), since they are rules of the game that agents know and take into account in their decisions. The diverse forms of labor contracts, with very extreme differences, are probably the major feature of the French labor market, and they are
at the heart of the model, since they modify the flows 8.
3. As stated above,most of the gross flows are generated by bounded rational decisions based on an enlarged search theory, and the effects of shocks we will study then
integrate the agents responses and interactions within the rules of the game and the accounting constraints. Our multi-agent model then provides a tool to explore rigorously the complex system constituted by the labor market.
The paper is organized as follows. In section 2, we describe the main features of the model. In section 3, we present our validation method - through calibration - and in section 4 some simulation results. We will show how WorkSim could be used to assess labor policies, including the recent "Labor Law" that attracted most of the attention recently in France, and generated vivid debates among policians, and economists. Section 5 will conclude and open the discussion.

2. 该模型在直接影响层面（即微观经济层面）对机构和劳动法进行建模，因为它们是参与者在决策中了解和考虑的游戏规则。法国劳动市场的主要特征可能是各种形式的劳动合同，其差异极大，并且这些合同是模型的核心，因为它们改变了流动情况。

3. 如前所述，大部分总流量是由有界理性决策基于扩展搜索理论产生的，并且我们将研究的冲击效应将融入参与者对游戏规则和会计约束的反应和互动中。因此，我们的多主体模型为探索由劳动市场构成的复杂系统提供了一种严谨的工具。
本文结构如下：第2节描述了模型的主要特点。第3节介绍了我们通过校准进行验证方法，第4节呈现了一些仿真结果。我们将展示WorkSim如何用于评估劳动政策，包括最近在法国引起广泛关注并引发政治家和经济学家激烈辩论的“劳动法”。第5节将做出结论并开启讨论。

Note that if the current version WorkSim is primarily designed to account for the French Labor Market (denoted FLM in this paper), most of its components and mechanisms could be re-used to describe labor markets in other countries. In fact, mainly the elements specific to the French institutions (labor law) must be adapted when dealing with another country.

需要注意的是，尽管当前版本的WorkSim主要是为了描述法国劳动市场（在本文中标记为FLM），但它的大部分组成部分和机制可以被重新利用来描述其他国家的劳动市场。实际上，在处理其他国家时，只需对与法国机构（劳动法）相关的特定元素进行适应性调整即可。

## 2 Model Description 2.1 The Agents In Worksim



There are two types of agents: *Private Firms* and *Individuals*. At its creation, each firm starts with at least one worker to run the company, representing the *managing director* 9
The *Individuals* are grouped in *households* and the simulation evolves in a closed population. The individuals can marry each other, have children, and therefore the decisions of one member of the household may have an impact on the other members. In WorkSim, the agents are heterogeneous. They have specific attributes determined once and for all at their creation (e.g. gender, amenity, ...) and internal variables (e.g. age, salary, number of employees, ...) that evolve all along the simulation.

2 模型描述 2.1 WorkSim中的主体机构

WorkSim中存在两种类型的主体机构：*私营企业*和*个人*。在创建时，每家企业至少有一名工人来经营公司，代表着*总经理*9。
个人被分组成*家庭*，模拟发生在一个封闭的人口中。个人可以结婚、生育孩子，因此家庭成员的决策可能会对其他成员产生影响。在WorkSim中，主体机构是异质的。他们具有在创建时确定的特定属性（例如性别、便利设施等）和内部变量（例如年龄、薪水、雇员数量等），这些变量在整个模拟过程中不断演化。

The agents under 15 or over 65 years belong to these households but are not instantiated as full agents and do not take decisions in the model. However, these non-instantiated agents indirectly participate through the economic decisions of the other members of the household (eg. the number of dependent children is taken into account in decisions of transition to inactivity, the retirement pension is included in household income). The individuals under 15 years become full agents in the model at the age of 15, and some remain in the school system while others enter the labor market.

这些家庭中的年龄在15岁以下或65岁以上的成员被视为非完整个体，不参与模型中的决策过程。然而，这些非完整个体通过家庭其他成员的经济决策间接参与其中（例如，在转入非活动状态的决策中考虑了依赖子女的数量，退休金计入家庭收入）。当个体年满15岁时，他们将成为模型中的完整个体，并且有些人会继续在学校系统中学习，而其他人则进入劳动力市场。

## 2.2 Environment



In addition to these agents, the model uses three *artifacts* 10:

除了这些主体外，该模型还使用了三个*工具*10：

- *JobAds*, which receives job offers from the firms and job applications from the job
seekers. Dissemination of information, however, is based on the job search process described in more detail below (see sections 2.8 and 2.9), according to the principles of search theory.
- a *Statistical Institute* that calculates statistics from the simulation and disseminates
some information (e.g. tension on the labor market). The information is imperfect for agents, and we specify what information is being broadcasted.
- a *Public Sector* that recruits (exogenously) employees, collects payroll taxes on businesses.

- *职位广告*是一个接收企业职位提供和求职者求职申请的平台。然而，根据搜索理论的原则，信息的传播是基于下文详细描述的求职过程（见第2.8节和第2.9节）。
- *统计研究所*负责从模拟中计算统计数据并传播一些信息（例如劳动力市场上的紧张情况）。对于主体来说，这些信息是不完全的，并且我们会明确指定正在广播哪些信息。
- *公共部门*通过外部招募员工，并对企业征收工资税。

## 2.3 Institutional Framework



Moreover, it also includes one *institutional module*. One distinctive feature of the WorkSim model is to integrate a fairly complete and flexible institutional framework that includes (1) the necessary elements of the French labor Law, including **two types of contract**:
Fixed-Term contracts (FTC11) and open ended contracts (OEC12), dismissals on personal and on economic grounds, redundancy payments, . . . ). and (2) government decisions (minimum wages, welfare benefits, ...).

此外，该模型还包括一个“制度模块”。WorkSim模型的一个显著特点是将一个相当完整且灵活的制度框架整合其中，包括法国劳动法的必要要素，如**两种类型的合同**：固定期限合同（FTC11）和无固定期限合同（OEC12），以及个人和经济原因的解雇、遣散费等。此外，还考虑了政府决策（如最低工资、福利待遇等）。

## 2.4 Individuals



In WorkSim, the individuals i are characterized by the following attributes :

在WorkSim模型中，个体i的特征由以下属性来描述：

- *Gender* : female or male.
- *Age*, denoted *age*i and counted in weeks (a tick represents one week in the simulation).
- Preferences for *free time* : see section 2.9 below. - *State* in the labor market. The possible states are : inactive, unemployed, employed
and not searching for another job (denoted ENS), employed and seeking a new job (denoted OTJS, for On-The-Job Searchers), student or retired.
without heavy penalties (paying the remaining salary part).
12 Main *OEC* (CDI) Features: no duration limit, probationary period, no firing costs for the first year, no termination costs if quitting, variable firing costs when firing.
- *Occupation*, denoted q in this chapter. The number of possible occupations is denoted
nq. In our simulations, we consider 3 levels : 1=blue collar or employee, 2 = middle level job, 3 = executive. Of course, an individual can change his/her occupation during the simulation (upward or downward).
- Productivity kernel *kProd*i : it represents the "innate" abilities of the individual i.
kProdi ∼ Max(0, N (1, σ*coreProd*))13 with standard deviation σ*coreProd* ∈ [0, 1] is an
exogenous calibrated parameter.
- Condition factor condi, t that represents the physical condition, the motivation and
satisfaction for i. It evolves with time following a random walk :
$$cond_{i,t+1}=Max(minC,\ Min(maxC,cond_{i,t}+{\cal N}(1,\sigma_{C})))\tag{1}$$
Hence ∀t, condi,t ∈ [minC, maxC]. minC et *maxC* are two exogenous parameters and σC ∈ [0, 0.3] is calibrated.

2.4 个体

在WorkSim模型中，个体i的特征由以下属性来描述：

- *性别*：女性或男性。
- *年龄*，表示为*age*i，以周计算（模拟中的一个时刻代表一周）。
- 对*空闲时间*的偏好：详见下文第2.9节。
- 在劳动市场上的*状态*。可能的状态有：不活跃、失业、就业但不寻找其他工作（记为ENS）、就业并寻找新工作（记为OTJS，即在职求职者）、学生或退休。没有重大惩罚（支付剩余薪水部分）。
- 主要的无固定期限合同（CDI）特征：没有期限限制、试用期、第一年没有解雇成本、如果辞职则没有终止成本、解雇时变动的解雇成本。
- *职业*，在本章中表示为q。可能的职业数量表示为nq。在我们的模拟中，我们考虑了3个级别：1=蓝领或员工，2=中层岗位，3=高管。当然，在模拟过程中个体可以改变他/她的职业（向上或向下）。
- 生产力核心*kProd*i：它代表了个体i的“天赋”能力。kProdi服从Max(0, N (1, σ*coreProd*))13的分布，其中标准差σ*coreProd* ∈ [0, 1]是一个外生校准参数。
- 条件因子condi,t表示个体i的身体状况、动机和满意度。它随时间按照随机游走的方式演变：
$$cond_{i,t+1}=Max(minC,\ Min(maxC,cond_{i,t}+{\cal N}(1,\sigma_{C})))\tag{1}$$
因此，对于所有t，condi,t ∈ [minC, maxC]。minC和maxC是两个外生参数，σC ∈ [0, 0.3]经过校准。

- Human capitals (HC) HCgen i,t , HCocc i,q,t, HCspec i,p,t , respectively for the general, related to the occupational level q, and *specific to the firm* and job p *human capitals*14.

- 人力资本（HC）可分为三个部分：HCgen i,t，代表个体i在一般领域的人力资本；HCocc i,q,t，代表与职业水平q相关的人力资本；HCspec i,p,t，代表特定于公司和工作p的人力资本14。

The general HC represents the abilities useful for all jobs, like problem solving or knowledge of a foreign language. It increases with experience (one more unit per tick) and also with training. It decreases at each tick i is unemployed by a percentage Lxp after *Txp* ticks (loss of skills). *Lxp* ∈ [0, 0.1] and *Txp* ∈ [0, 100] are two calibrated parameters. The occupational HC is related to the occupational level, and represents abilities specific to this level: machinery or team leading for instance. Like the general HC, it increases with experience (one more unit per tick) and also with training, and decreases at each tick i is unemployed by a percentage *Lxp* after *Txp* ticks. The specific HC is related to the position and the firm. It represents abilities specific to the job in the firm, like a particular process or a software to use. It equals the number of ticks the employee spends in the job. It is reset to zero when s/he leaves the job.

一般人力资本代表了适用于所有工作的能力，如问题解决能力或外语知识。它随着经验的积累（每个时间单位增加一个单位）和培训的进行而增加。当个体i在某个时间单位内失业时，其会以Lxp的百分比减少（技能损失）。其中Lxp ∈ [0, 0.1]和Txp ∈ [0, 100]为两个经过校准的参数。职业人力资本与职业水平相关，代表了特定于该水平的能力，如机械操作或团队领导等。与一般人力资本类似，它随着经验的积累（每个时间单位增加一个单位）和培训的进行而增加，并且当个体i在某个时间单位内失业时，其会以Lxp的百分比减少（技能损失）。特定人力资本与职位和公司相关。它代表了在公司中从事该工作所需具备的特定能力，如特定流程或软件使用等。其数值等于员工在该工作岗位上度过的时间单位数。当员工离开该岗位时，其将被重置为零。

## 2.5 Demand



The only production factor is the labor, like in many labor market models. There is one good, and each firm produces a certain amount of its own variety of this good. The price P is then unique (horizontal differentiation) and fixed at the arbitrary value of 1. Each firm of the N firms in our model responds to a *quantity demanded* of this good Dj,t, which fluctuates randomly due to variations in consumers preferences. However, the global demand Dtot is held constant because we aim to study our economy in a steady state.

在许多劳动力市场模型中，唯一的生产要素是劳动力。我们的模型中存在一个商品，每家公司生产自己特定数量的该商品。价格P是唯一的（水平差异），并被固定为任意值1。在我们的模型中，N家公司中的每家公司都对该商品的需求量Dj,t做出反应，该需求量由于消费者偏好变化而随机波动。然而，全球需求Dtot保持恒定，因为我们旨在研究经济稳态下的情况。

At time t = 0, the *market share* of a firm j is given by Dj,t=0/Dtot. We assume that the distribution of this global demand varies between firms. Then we apply a stochastic shock on this market share for each firm at each period (random walk) using a normal law.

在时间t = 0时，公司j的市场份额由Dj,t=0/Dtot给出。我们假设全球需求的分布在公司之间有所不同。然后，我们对每个公司在每个时期的市场份额施加随机冲击（随机漫步），使用正态分布进行模拟。

## 2.6 Jobs



Each firm has a managing director and a list of jobs per occupation. A job can be in 3 different states : filled, vacant or *pending*. A *pending* job is typically an *FTC* contract that ended, but cannot be renewed immediately, because of the waiting period15.

每个公司都有一个总经理和一份职位列表。一个职位可以处于3种不同的状态：已填充、空缺或待定。待定的职位通常是一份FTC合同结束后无法立即续签的情况，因为需要等待期15。

Each job p of the occupation q is characterized by specific attributes determined once for all at its creation :

每个职位 q 的 p 都具有特定属性，这些属性在其创建时一次性确定：

- a vector of required human capitals [HCgen
req,p, HCocc
req,p,q, HCspec
req,p], respectively for the
general, *related to the occupational level* q, and *specific to the firm* and job p human capitals. They represent the minimum skills required to work on this job and
are randomly drawn according to uniform distributions respectively between 0 and
MaxHCgen
req , MaxHCocc
reqand MaxHCspec
req . We will see in the next section that an individual can acquire these skills with experience and training.
- The duration of work *HpW*p, measured by the number of hours required per week for
the job p.
- A hourly base production QHbase
j,q
that equals to the hourly base production for all
jobs in the firm at occupation q. It is randomly drawn at the creation of the firm j, to account for the differences in production efficiency (technology, organization...) between the firms.
* A _hourly base salary_ determined from the base production in the job for all jobs in the firm at occupation $q$ : $$SH_{j,q}^{base}=QH_{j,q}^{base}\times P\times(1-\zeta)$$ (2) with $P=1$ the exogenous price of the (unique) good and $\zeta\in[0,1]$, an exogenous parameter that represents the share of the base productivity value kept by the firm (in order to pay expenses, taxes, interests, dividends, etc.). The weekly base salary will be simply given by $$S_{j,p,q}^{base}=SH_{j,q}^{base}\times Hp_{p}$$ (3)
* A level of _amenity_. This represents non-monetary features perceived by the individual on the job (social recognition, working environment,...). A hourly base annuity randomly drawn at the creation of the firm as a percentage $PrA$ of the base salary for all occupation level $q$.

- 人力资本要求向量包括一般的（HCgenreq,p）、与职业水平 q 相关的（HCoccreq,p,q）以及特定于公司和职位 p 的（HCspecreq,p）人力资本。它们代表了在该职位上工作所需的最低技能，并根据均匀分布在 0 和 MaxHCgenreq、MaxHCoccreq、MaxHCspecreq 之间进行随机抽取。我们将在下一节中看到，个体可以通过经验和培训来获得这些技能。
- 工作持续时间 HpWp 以每周所需小时数衡量。
- 每小时基础产量 QHbasej,q 表示公司在职业 q 上所有工作的每小时基础产量。它在公司 j 创建时进行随机抽取，以考虑公司之间生产效率（技术、组织等）的差异。
- 基于工作中所有工作的基础产值确定的每小时基础薪水 SHj,q^base：$$SH_{j,q}^{base}=QH_{j,q}^{base}\times P\times(1-\zeta)$$ (2)，其中 $P=1$ 是商品的外生价格（唯一商品），$\zeta\in[0,1]$ 是一个外生参数，表示公司保留的基础生产力价值的份额（用于支付费用、税收、利息、股息等）。每周基础薪水将简单地由以下公式给出：$$S_{j,p,q}^{base}=SH_{j,q}^{base}\times Hp_{p}$$ (3)
- 福利水平表示个体在工作中感知到的非货币特征（社会认可、工作环境等）。每小时基础年金在公司创建时随机抽取，作为所有职业水平 q 的基本工资的百分比 $PrA$。

## 2.7 Simulation Cycle In The Worksim Model



The **simulation cycle** includes four main steps, as shown in Figure 1 below:

**模拟周期**包括以下四个主要步骤，如下图1所示：

1. Firm decisions: contracts and vacancies management, evaluations, job creation / destruction;
2. Individual decisions: labor market entrances and exits, job search; 3. Firm decisions: applications and promotions management; 4. Demography: household dynamics, retirements, aging.
The length of one period in the simulation cycle corresponds to *one week* in the real world, in order to take into account the many very short term contracts that are found in the French labor market, 46% of all hires are on Fixed-Term Contracts that last one week or less in 2010 (ACOSS, 2011).

1. 公司决策：合同和职位管理、评估、就业创造/破坏；
2. 个体决策：劳动力市场的进入和退出、求职；
3. 公司决策：申请和晋升管理；
4. 人口统计学：家庭动态、退休、老龄化。
模拟周期的长度相当于现实世界中的一周，以考虑法国劳动力市场上存在的许多非常短期的合同。根据ACOSS（2011）的数据，2010年法国46%的新雇佣是持续时间为一周或更短的固定期限合同。

## 2.8 Firm Decisions



Before describing the job creation process, we describe the demand anticipation mechanism that is the core of these job creation process and the endogenous choice between the different contracts : *FTC* and *OEC*.

在描述就业创造过程之前，我们将描述需求预期机制，这是就业创造过程的核心，并且对不同合同（FTC和OEC）之间的内生选择进行了描述。

Demand anticipation The central idea that governs job creation relies on the way the firm will estimate the future demand. If the demand is going to increase, a new job might be profitable, but not if there is a decrease in the demand.

需求预期  就业创造的核心思想在于企业如何估计未来的需求。如果需求将增加，新增一个职位可能是有利可图的，但如果需求减少，则不是。

Hence, the firm will compute three scenarios - pessimistic, *neutral* and *optimistic*, which are depicted in the Figure 2 below. We see in this Figure that in the pessimistic scenario of demand evolution, the demand of the firm is below its production with the new job after a certain time. As the firm cannot sell more good than its demand, it may result in a loss because the firm has to continue to pay a salary. In this example, we see that it may be more profitable for the firm to choose a contract with a shorter expected duration like a 3 months *FTC*. Indeed, the firm will have the option to end this contract after 3 months in case of a negative scenario or to renew it if it goes well. However with a shorter contract it is more difficult to amortize the cost of hiring and training a new employee. It therefore appears a trade-off depending on the level of uncertainty of future demand and how the firm perceives the risks.

因此，该公司将计算三种情景——悲观、中立和乐观，如下图所示。从图中可以看出，在需求演变的悲观情景中，该公司的需求低于其新增职位后的生产。由于该公司无法销售超过需求量的产品，这可能导致亏损，因为该公司必须继续支付工资。在这个例子中，我们可以看到对于该公司来说选择一个预期持续时间较短的合同（如3个月的FTC）可能更有利可图。实际上，如果出现负面情况，该公司将有选择在3个月后结束该合同或者在表现良好时进行续签。然而，较短的合同更难以摊销雇佣和培训新员工的成本。因此，在未来需求不确定性水平和企业对风险感知程度之间存在权衡关系。

Note that, because of bounded rationality, the firms anticipates with a *finite* horizon only. Moreover, the decision process will combine all the three possible scenario into a multi-criteria weighted utility, and the weight of each scenario is automatically calibrated.

需要注意的是，由于有限理性，该公司只能预测有限的时间范围。此外，决策过程将把所有三种可能的情景结合起来形成一个多准则加权效用，并自动校准每种情景的权重。

Job creations (step 1 in Figure 1)
The job creation proceeds in three steps:

工作岗位的创造（图1中的第一步）
工作岗位的创造分为三个步骤：

1. First, the firm checks if there is a sufficient demand margin to create a new job.
Here it considers the actual (not anticipated) demand margin DM*j,q,t* for firm j and
occupation level q at time t: if it exceeds the demand margin threshold DT (calibrated
parameter), then the firm moves to the next step. Otherwise, no job is created.
2. If there is in the firm a *pending* job in the occupation q, the firm considers to hire a
new person for this job (taking into account the eventual waiting period). Therefore the pending job becomes a *vacant* job. Otherwise, it moves to the next step.
3. Here, DMj,q,t *> DT* and there are no pending jobs in occupation q. Hence, the firm
considers to create a new job p of the occupation q. The characteristics of this new
job are randomly drawn. From these job features, the firm must decide which type of contract suits better.

1. 首先，公司会检查是否存在足够的需求余量来新增一个工作岗位。在此过程中，公司会考虑实际的需求余量DM*j,q,t*，而非预期值，以及公司j和职位水平q在时间t的情况。如果需求余量超过了设定的阈值DT（校准参数），则公司将进入下一步。否则，将不会创建新的工作岗位。

2. 如果公司在职位q中有一个待定的工作岗位，则公司会考虑招聘一名新员工来填补该职位（同时考虑可能存在的等待期）。因此，待定的工作岗位将变为空缺岗位。如果没有待定的工作岗位，则公司将进入下一步。

3. 在这种情况下，需求余量DMj,q,t*大于阈值DT，并且职位q中没有待定的工作岗位。因此，公司考虑新增一个职业为q、编号为p的新工作岗位。这个新工作岗位的特征是随机确定的。基于这些特征，公司需要决定哪种类型合同更适合。

注意：重写后文本保留了原文内容，并对表达进行了优化和调整以符合学术风格。

## Evaluation Of A Contract



1. During a prospecting phase, the firm receives information about *NPros* job seekers of
the occupation q , who have applied to a job with a *FTC* and *NPros* job seekers of
the occupation q who have applied to a job with a *OEC* during the last period. The
expected profit per period φper
i,j,p,q,c,t for a candidate i on a job p with a contract c is then
computed for each contract : the *OEC* contract is compared with several *FTC* with
different fixed terms : 1 week, 1 month, 2 months, 6 months, 12 months, 18 months.
2. Then the firm chooses to *create the contract* c with the *best average positive profit*,
calculated along a set of potential candidates. These candidates are unemployed job
seekers and *JobAds* sends to the firm their productivity level and human capitals. The
firm will choose the contract c∗ that give the highest positive profit φavg. If all the
profits are negative, no new job is created.
3. The firm continues to consider creating new job as long as DMj,q,t *> DT*.
Job destruction (step 2 in Figure 1) By contrast, when there is a significant reduction in its demand in one occupation (in our model, this is when DM*j,q,t* < −DT), the firm reacts in the short-term by trying to remove its vacancies. In the medium run (on a yearly basis), if this low cost adjustment is not sufficient, the firm considers the possibility to dismiss workers.

1. 在勘探阶段，公司会收到关于职业q的*NPros*求职者对带有*FTC*的工作和对带有*OEC*的工作的申请信息。针对每种合同，将计算候选人i在合同c上与工作p每期的预期利润φper
i,j,p,q,c,t。通过将*OEC*合同与不同固定期限的多个*FTC*进行比较（如1周、1个月、2个月、6个月、12个月、18个月），来确定最佳合同。
2. 公司会选择与一组潜在候选人中具有最佳平均正利润φavg的合同c，并获取这些候选人的生产力水平和人力资本信息。如果所有利润都为负，则不会创建新工作岗位。
3. 只要DMj,q,t *> DT*, 公司将继续考虑创建新工作岗位。
    工作销毁（图1中第2步）相反，当某一职业需求显著减少时（在我们的模型中，当DM*j,q,t < -DT时），公司会试图短期内减少空缺岗位。从中长期来看（按年计算），如果这种低成本调整不足够，公司会考虑解雇员工。

Moreover, independently of the demand level, the vacancies that remain unfilled and have a vacancy duration greater than a fixed threshold - a parameter that will differ for FTC and *OEC* - are destroyed.

此外，与需求水平无关，那些未填补的职位空缺且持续时间超过一个固定阈值（该阈值对于FTC和OEC将有所不同）的职位将被销毁。

Economic dismissals An evaluation of the financial viability of the company is performed on a yearly basis (52 periods in the simulation). The first date of the balance sheet is drawn randomly, then this financial reporting occurs every year from this date. The company calculates its yearly return that is computed as the ratio of the yearly profit over the total labor cost16. If this return falls below a certain *profitability threshold* (a fixed parameter PT, that will be calibrated), the firm can justify an economic dismissal procedure:

经济性解雇：每年（模拟中的52个周期）都会对公司的财务可行性进行评估。首次资产负债表日期是随机选择的，然后从该日期开始，每年都会进行一次财务报告。公司计算其年度回报率，即年度利润与总劳动成本之比16。如果该回报率低于特定的“盈利能力阈值”（一个固定参数PT，将进行校准），公司可以合理地启动经济性解雇程序。

- All remaining vacancies are removed.
- After all the vacancies being removed, if DM*j,q,t* < −DT still holds, the firm consider
to dismiss employees. It selects one employee, computes the associated profit Φtot
i,j,p,q,c,t
and the firing cost *EFC*. If Φtot
i,j,p,q,c,t < −EFC, the firm dismiss the employee. This
process is repeated until DM*j,q,t* > −DT or if all employees have been evaluated.
If a company has no employee anymore, and if the managing director left alone does not make a sufficient return, the firm is considered to be bankrupt and is removed from the simulation. The managing director becomes unemployed. However, we want to keep the number of firms constant17. Hence, when a bankruptcy has occurred, we randomly select an active agent in the simulation to create a new firm and manage it. S/he will be the only producer in the firm (until s/he starts to recruit). Employee evaluations (step 3 in Figure 1) In each period, the firm examines if some employees have to be evaluated. This individual evaluation may occur:

- 所有尚未填补的职位已被撤销。
- 在所有职位被撤销后，如果DM*j,q,t* < −DT仍然成立，公司将考虑解雇员工。公司会选择一名员工，计算其所带来的利润Φtot
i,j,p,q,c,t以及解雇成本*EFC*。如果Φtot
i,j,p,q,c,t < −EFC，则公司将解雇该员工。这个过程会重复进行，直到DM*j,q,t* > −DT或者所有员工都被评估完毕。
- 如果一家公司没有员工了，并且仅剩下的董事总经理无法获得足够的回报，那么该公司将被视为破产并从模拟中移除。董事总经理将失业。然而，我们希望保持公司数量不变17.因此，在发生破产时，我们会随机选择一个在模拟中活跃的参与者来创建一家新公司并进行管理。该参与者将成为该公司唯一的生产者（直到开始招聘）。员工评估（图1中的步骤3）每个周期内，公司会检查是否需要对某些员工进行评估。这种个体评估可能发生：

1. At the end of the probationary period for *FTC* and *OEC* ;
2. Every year, at the anniversary date of the contract, for *OEC* employee. 3. At the end of *FTC* contract to decide if it should be renewed ;
4. At the end of *FTC* contract, if the transformation of FTC to *OEC* is to be considered.
Dismissal for personal reasons The process takes in two steps :

1. *FTC*和*OEC*的试用期结束时；
2. 每年合同纪念日时，对于*OEC*员工；
3. 在*FTC*合同到期时决定是否应该续签；
4. 在*FTC*合同到期时，考虑是否将其转为*OEC*。
个人原因解雇的流程分为两个步骤：

1. First, the firm evaluates if there is a case for considering the dismissal. That could
be the case if the employee's production is below the firm's requirement. Thus, there is a chance that the firm considers to fire this employee for personal reasons if the annual production of the employee Qeval
i,j,p,q,t satisfies : Qeval
i,j,p,q,t < ρ × Qrequired
p,q
where
Qrequired
p,q
is the required level of production and ρ an exogenous parameter in [0.7, 0.9].
ρ encodes the tolerance the firm has with underproduction, or the maximum margin
risk it accepts to take18.
2. Then the firm decides whether such a dismissal is profitable (on economic grounds).
Hiring phase and promotions (step 7-8 in Figure 1)
Once the firm has chosen which contract c to create, a hiring norm must be computed to evaluate the candidates.

1. 首先，公司会评估是否有必要考虑解雇员工。如果员工的产量低于公司的要求，那么可能会考虑解雇该员工。因此，当员工的年产量Qeval i,j,p,q,t满足以下条件时：Qeval i,j,p,q,t < ρ × Qrequired p,q，公司有可能因个人原因解雇该员工。其中，Qrequired p,q表示所需生产水平，而ρ是一个外生参数，取值范围在0.7至0.9之间。ρ代表了公司对于低产量的容忍度或者接受的最大风险边界。

2. 接着，公司会根据经济原因来判断这样的解雇是否具有盈利性。
招聘阶段和晋升（图1中第7-8步）
一旦公司确定了要创建哪种合同c，就需要计算一个招聘规范来评估候选人。

注意：上述内容仅为重写后的中文翻译结果，并非原文内容。

This *hiring norm* is the profitability threshold below which it prefers to refuse a candidate.

这个“招聘规范”是指公司的盈利门槛，低于该门槛的情况下，公司更倾向于拒绝候选人。

To do so, it uses the *positive* expected profits Φavg j,p,q,c,t calculated for each of the NPros candidates during the prospecting phase and compute the average ΦMoy, the minimum
ΦMin and the maximum ΦMax values.

为了做到这一点，公司使用了在勘探阶段计算出的每个NPros候选人的预期正利润Φavg j,p,q,c,t，并计算出平均值ΦMoy、最小值ΦMin和最大值ΦMax。

The hiring norm of the firm is given by:

公司的招聘规范如下：

$$HNorm_{j,p,q,t=crea}=(\phi_{Moy}^{per}+N_{1}\times(\phi_{Max}^{per}-\phi_{Min}^{per}))\frac{N(d_{c})}{H(TIGH_{q,t=crea})}\tag{4}$$
- N1 will be calibrated in [0, 1]. The hiring norm increases with φper Max −φper Min, so the firm favors a large dispersion of candidates' qualities in order to increase the probability to get better candidates, as prescribed by search theory.

$$HNorm_{j,p,q,t=crea}=(\phi_{Moy}^{per}+N_{1}\times(\phi_{Max}^{per}-\phi_{Min}^{per}))\frac{N(d_{c})}{H(TIGH_{q,t=crea})}\tag{4}$$
- N1将在[0, 1]范围内进行校准。招聘规范随着φper Max −φper Min的增加而增加，因此公司倾向于候选人素质的较大差异，以提高获得更优秀候选人的概率，符合搜索理论的要求。

- N(dc) = N2+N3×dc, an increasing function of the duration of the contract dc proposed
for the job. N2 et N3 are two calibrated parameters in [0, 1]. We assume that the firm
will be more demanding for longer contracts, as they imply to keep the employee for a longer time.
- TIGHq, t = *crea* is the tightness on the labor market at the time of job creation and
is given by TIGHq, t = Vq,t
Uq,t with Vq,t the vacancy rate and Uq,t the unemployment rate
at time t for the occupation q. The higher this tension, the more the firms have to lower their requirements if they hope to find a candidate. H is a logistic function with values between 0.8 and 1.2 and given by H(x) = 0.8 +
0.4
1+20×e−3x.
This hiring norm is then decreased by a percentage N4 in each period until the job is filled, but never drops below 0.

- N(dc)是一个关于工作合同持续时间dc的递增函数，表示为N(dc) = N2 + N3×dc。其中N2和N3是两个在[0, 1]范围内校准的参数。我们假设随着合同时间的延长，公司对于员工的要求会更高。
- TIGHq, t = *crea*表示岗位创建时劳动力市场的紧张程度，由TIGHq, t = Vq,t
Uq,t计算得出。其中Vq,t表示职业q在时间t的空缺率，Uq,t表示失业率。当劳动力市场紧张程度较高时，公司需要降低要求才能找到合适的候选人。H是一个逻辑函数，取值介于0.8和1.2之间，定义为H(x) = 0.8 +
0.4
1+20×e−3x。
此外，在每个周期中招聘规范会以百分比N4递减，直到职位被填补，但不会低于0。

注意：以上内容仅供参考，请根据具体情况进行修改和调整。

Hiring takes place in three steps:

招聘分为三个步骤：

1. *Receiving applications* - The firm receives applications from external and internal
applicants.
2. *Selection and potential hiring* - A two-steps process takes place:
(a) First, the firm computes a score for each candidate (internal or external), given by
the expected profit per period Φper
i,j,p,q,c,t. Then the best candidate (highest score) is
selected.
(b) Thereafter, the firm checks if this candidate exceeds the hiring norm. If this is the
case, the candidate is hired, otherwise, the job remains vacant.
3. Internal promotion - If the best candidate hired is an internal candidate of the company, it is a promotion. The employee acquires the occupation level of the job.

1. *申请接收* - 公司接收来自内外部申请人的申请。
2. *筛选和潜在雇佣* - 这是一个两步骤的过程：
(a) 首先，公司根据预期每期利润Φper
i,j,p,q,c,t为每个候选人（内部或外部）计算得分。然后选择得分最高的候选人。
(b) 随后，公司检查该候选人是否符合招聘标准。如果符合，则雇佣该候选人；否则，职位将保持空缺。
3. 内部晋升 - 如果被雇佣的最佳候选人是公司内部员工，则属于晋升。员工将获得该职位的职业水平。

## 2.9 Individual Decisions (Step 4-6 In Figure 1)



The individuals take decisions in each period of the simulation. This decision process is modeled with a *state machine*, where one individual will be in one particular state: inactive, unemployed, employed and not searching for another job, employed and seeking a new job , student or retired. The transitions between these states can be caused by individual choices (for example: to look for a job, to quit a job...), by external events (firing, death...), or eventually by a sequence of multiple decisions (e.g. applying for a job, and the firm hires the candidate).

在模拟的每个时期，个体会做出决策。这一决策过程被建模为一个状态机，其中每个个体将处于以下特定状态之一：不活动、失业、就业但不寻找其他工作、就业并寻找新工作、学生或退休。这些状态之间的转换可以由个体的选择引发（例如：寻找工作、辞职...），也可以由外部事件引发（如解雇、死亡...），或者最终由多个决策序列引发（例如申请工作，公司雇佣候选人）。

Utility functions Each individual uses a utility function, to decide whether s/he should stay in her/his current state or move to another one. The utility function has the generic form of a Cobb-Douglas function:

效用函数 每个个体都使用一个效用函数来决定是否应该保持当前状态还是转移到另一个状态。效用函数具有Cobb-Douglas函数的一般形式：

$$U=\left(Income+Amentity+Stability\right)^{1-\alpha}\left(Free\ Time\right)^{\alpha}\tag{5}$$
It is a weighted aggregation of four factors:
1. *Income*: weekly income of the household in euros, divided by the number of consumption units (an adult counts for 1, a child 0.5)
2. *Amenity*: non-monetary features perceived by the individual (social recognition, working environment, job hardness...), cf. section 2.6 above.
3. *Stability*: criteria reflecting the preference of the individual for stability, i.e. for a job
with the long contract duration. The maximum value is given for a permanent job (OEC). This stability is converted here into a percentage of salary and is expressed in euros;
4. *Free time*: free time per week available for the individual outside her/his working
hours and search time. Our definition is a broad one since it includes time devoted for instance to sleep, eating, washing, domestic duties, and notably caring for the children.
The parameter αi,t ∈ [0, 1] encodes the preference of the individual for free time or work.

该公式是对四个因素进行加权聚合：
1. *收入*：家庭每周以欧元计算的收入，除以消费单位的数量（成年人计为1，儿童计为0.5）。
2. *便利设施*：个体感知到的非货币特征（社会认可、工作环境、工作难度等）。
3. *稳定性*：反映个体对稳定性的偏好，即对长期合同工作的偏好。最大值对应于永久性工作（OEC）。这里将稳定性转化为薪水百分比，并用欧元表示。
4. *空闲时间*：个体在工作时间和寻找工作时间之外每周可用的空闲时间。我们的定义很广泛，因为它包括例如睡觉、吃饭、洗漱、家务事，尤其是照顾孩子所需的时间。
参数αi,t ∈ [0, 1]编码了个体对空闲时间或工作的偏好。

Overview of the individual decisions The decision-making process of individuals is sequential and summed up in the state transition diagram depicted in Figure 3. At each tick, the individual agent computes the utility of its current state and the utilities of each reachable state. Each utility is evaluated using the generic form given by equation 5 above, and instantiated with the relevant values of income, amenity, stability and free time. For some transitions, a factor *ICHANG* ∈ [1, 2] is applied that represent the psychological cost facing change (calibrated parameter). When *ICHANG >* 1, the new state's utility must be even greater to win the decision.

个体决策概述 个体的决策过程是顺序进行的，如图3所示的状态转换图所总结。在每个时间点，个体主体计算其当前状态的效用以及每个可达状态的效用。每个效用都使用方程5中给出的通用形式进行评估，并使用相应的收入、便利设施、稳定性和空闲时间值进行实例化。对于某些转换，应用了一个表示面临变化心理成本（校准参数）的因子*ICHANG* ∈ [1, 2]。当*ICHANG >* 1时，新状态的效用必须更大才能赢得决策。

Job search process After describing the different decision mechanisms, let me now detail the overall job search process:

就业搜索过程 在描述了不同的决策机制之后，现在让我详细介绍整个就业搜索过程：

1. Each period in the model (one week in the reality), a job seeker receives from JobAds
a list of NVi,t vacancies matching her occupation or a level above. We assume that
these incoming job offers occur at a mean frequency that is known and independent of the time elapsed since the last offer. Therefore, we model the incoming of new job
offers with a Poisson law : at time t, this number of vacancies NVi,t is drawn from a
Poisson distribution with parameter λt = NSJU × H(TIGHq,t), where *NSJ*U is the
average number of vacancies received by the unemployed at each period, and H is the
same function of tightness as above.
2. The individual sends an application for the first offer whose utility is above his/her
reservation utility UTRESi,t19. If theres is no job offer corresponding to her/his occupation or if all of her/his applications are rejected, s/he lowers her/his reservation utility UTRESi,t. Thus, at the end of each period, the reservation utility is updated :
$$UTRES_{i,t}=UTRES_{i,t-1}\times(1-Ru_{3})+Ru_{4}\times(UTUEM_{i,t}-UTUEM_{i,t-1})\tag{6}$$
where Ru3 ∈ [0, 0.005] is a calibrated parameter and Ru4 a fixed parameter (0.5).

1. 在模型中的每个时期（现实中为一周），求职者会收到一份与其职业或更高级别相匹配的空缺岗位列表，这些信息来自于招聘广告。我们假设这些新工作机会以已知频率出现，且与上次提供机会的时间无关。因此，我们使用泊松分布来模拟新工作机会的到来：在时间t，空缺岗位的数量NVi,t服从参数为λt = NSJU × H(TIGHq,t) 的泊松分布。其中，NSJU表示每个时期失业者平均收到的空缺岗位数量，H是与紧张程度相关的函数。

2. 求职者会对第一个效用高于其保留效用UTRESi,t19 的工作机会进行申请。如果没有符合其职业要求的工作机会，或者所有申请都被拒绝，则求职者会降低其保留效用UTRESi,t。因此，在每个时期结束时，保留效用将根据以下公式进行更新：
$$UTRES_{i,t}=UTRES_{i,t-1}\times(1-Ru_{3})+Ru_{4}\times(UTUEM_{i,t}-UTUEM_{i,t-1})\tag{6}$$
其中Ru3 ∈ [0, 0.005] 是一个经过校准的参数，Ru4 是一个固定参数（0.5）。

The first term of the equation accounts for the diminution with time and the second is driven by a modification of *UTUEM*, that is the utility for the unemployed (for instance a decrease of revenue will lower *UTUEM* and therefore *UTRES*, as the urge to find the job increases).

该方程的第一项考虑了随时间的减少，第二项则是由*UTUEM*的修改驱动，即失业者的效用（例如，收入减少会降低*UTUEM*和因此*UTRES*，因为找工作的紧迫感增加）。

## 3 Validation Process 3.1 Methodology



The WorkSim methodology uses a validation process at 2 levels :

3 验证过程 3.1 方法论

WorkSim 方法论在两个层面上使用验证过程：

1. *model building* : the way we design the model, and especially the agents' decision rules is
rooted as much as possible in empirical data and facts. Following the psychomimetism methodology Kant (1999), we ensure that these decision processes do not violate the cognitive principles we build our model from (e.g. bounded rationality).
2. *data reproduction*. We want our simulation to account for most of available data on the
labor market we aim to study. To do so, we use an automatic procedure to calibrate the model parameters for which we don't have an empirical value (see below).

3 验证过程 3.1 方法论

WorkSim 方法论在两个层面上使用验证过程：

1. *模型构建*：我们以尽可能多的实证数据和事实为基础，设计模型，特别是主体的决策规则。遵循康德（1999）的心理模仿方法，我们确保这些决策过程不违反我们从中建立模型的认知原则（例如有限理性）。
2. *数据再现*：我们希望我们的模拟能够涵盖我们所研究劳动市场上大部分可用的数据。为了实现这一目标，对于那些没有经验值的模型参数，我们采用自动程序进行校准（见下文）。

## 3.2 Calibration



Scaling First of all, we must set the number of agents in the simulation. It must be large enough to account sufficiently for real behaviors, but not exceed our computational power20. For the first set of experiments (sections 4.1 and 4.2), we used a reduction factor around 5400 and obtained 7484 individuals and 797 firm agents, for a total of 8281 agents in the simulation. The simulation of the "Labor Law" required 20 000 agents to ensure we have sufficient large firms (see section 4.3 below). Calibration procedure To calibrate the 60 model parameters, we have to minimize a fitness function that is the weighted sum of the relative spreads between the outputs of our model and the real targets of the French labor market in 2011 (source: INSEE/DARES). We have chosen 63 targets grouped in 10 different categories : unemployment rates (7 targets), activity rates (6), salaries (14), job flows (12), FTC (4), long-term unemployment (3), mobility (between occupations; 12), additional (part-time, vacancies, on-the-job,training costs). In most cases, we have a target per occupation or age range.

3.2 校准

首先，我们需要确定模拟中的主体数量。这个数量必须足够大，以充分考虑真实行为，但不能超过我们的计算能力20。对于第一组实验（第4.1节和第4.2节），我们采用了一个约为5400的缩小因子，得到了7484个个体和797个公司主体，总共有8281个主体参与了模拟。而对于"劳动法"的模拟，则需要20000个主体，以确保我们有足够多的大型企业（详见下文第4.3节）。

校准过程中，我们需要调整60个模型参数。为此，我们需要最小化一个适应度函数，该函数是我们模型输出与2011年法国劳动市场真实目标（来源：INSEE/DARES）之间相对差距的加权和。我们选择了63个目标，并将其分为10个不同的类别：失业率（7个目标）、活动率（6个）、工资（14个）、就业流动性（12个）、固定期限合同（4个）、长期失业率（3 ），流动性（职业间；12），附加信息（兼职、空缺、在职培训成本）。在大多数情况下，每种职业或年龄段都有一个目标值。

To minimize this fitness function, we apply the evolutionary algorithm CMA-ES (Hansen and Ostermeier, 2001), which is one of the most powerful algorithms to solve this kind of problem (Auger and Hansen, 2012). CMA-ES means Covariance Matrix Adaptation Evolution Strategy. The principle of this evolutionary algorithm is to test step by step new generations of points in the parameters space. Each new generation of points is drawn stochastically according to the results obtained with the previous generation of points. The mean and the covariance matrix of the distribution of the new randomly drawn points are updated incrementally in order to move towards the best results obtained by previous generations.

为了最小化这个适应度函数，我们采用了CMA-ES（Hansen和Ostermeier，2001）这一进化算法，它是解决这类问题中最强大的算法之一（Auger和Hansen，2012）。CMA-ES代表协方差矩阵适应进化策略。该进化算法的原理是在参数空间中逐步测试新一代点。每个新一代点根据前一代点的结果以随机方式绘制。通过增量更新新绘制点的分布的均值和协方差矩阵，以朝着前几代获得的最佳结果移动。

At each *iteration*, the CMA-ES algorithm sets the values of all the 60 parameters.

在每次迭代中，CMA-ES算法设置了所有60个参数的值。

Then, to cope with the stochasticity we have in the model, 48 simulations are run (they are usually called *replications* in a calibration process) with a different seed for the random generator, and the outputs are averaged over these 48 simulations to obtain the fitness value of the iteration. We stop the calibration when the fitness does not improve (same minimum value) for 500 iterations. Computational power needs The calibration process is very costly in terms of computational resources, because the total number of simulations could be very high : it is given by the product of the number of iterations by the number of replications. With Work- Sim, it took 2000 iterations to converge, and as stated above each iteration is made of 48 replications. Each simulation takes about 1-2 minutes overall and the whole calibration process will take a couple of days to be completed. Results of the calibration on the main targets We obtain an average relative spread between all the outputs of our model and the real targets of 7.9 %. This can be deemed satisfactory for such a large non-linear model. We deal with a multi-objective optimization problem with many targets and parameters, and these problems are known to be hard to solve.

为了应对模型中的随机性，我们进行了48次模拟（在校准过程中通常称为“复制”），每次使用不同的随机生成器种子。然后将这48次模拟的输出取平均，以获得迭代的适应度值。当适应度在500次迭代中不再改善（达到相同的最小值）时，我们停止校准。从计算资源角度来看，校准过程非常耗费资源，因为总模拟次数可能非常高：它由迭代次数乘以复制数量得出。使用Work-Sim进行收敛需要2000次迭代，并且如上所述，每个迭代由48个复制组成。每个模拟总共需要1-2分钟时间，整个校准过程将需要几天才能完成。

我们得到了模型输出与真实目标之间的平均相对差异为7.9%。对于如此庞大的非线性模型来说，这可以认为是令人满意的结果。我们处理一个具有许多目标和参数的多目标优化问题，而这些问题被认为很难解决。

## 4 Simulation Analyses And Results



In this section, we summarize the main results from a first set of prior simulations we conducted with WorkSim. In this set, the model was calibrated to account French data in 2011. And then we present results on the most recent labor law reform in France. Note that each simulation result is averaged over 196 simulations.

在本节中，我们对我们使用WorkSim进行的第一组模拟进行了主要结果的总结。在这组模拟中，我们校准了模型以考虑2011年的法国数据。随后，我们展示了关于法国最新劳动法改革的结果。需要注意的是，每个模拟结果都是基于196次模拟的平均值。

## 4.1 Characterizing The French Labor Market



The model generates some important specific characteristics of the French Labor Market such as the very important share of FTCs in terms of flows, 81 % and the contrasting fairly low figure of the share of the workers employed in such contracts: only 9 %. The unemployment of the young is also much higher than the unemployment of the older workers. This confirms the dualism in the French Labor Market, which is displayed by the differences in the patterns of gross flows of the categories of workers. The model computes all the simulated flows, but allows for comparison with those which can be measured by the published statistics, and the results fit roughly. Most workers are stable in their OECs, while a minority undergoes short spells of employment in FTCs and spells of unemployment between them. Moreover this dualism persists for part of the young workers when they age while the others obtain more stable OEC. More novel results are obtained but will not be detailed here, since they are not the core of this paper.

该模型呈现了法国劳动力市场的一些重要特征。例如，在流动性方面，固定期限合同（FTCs）在流动中所占比例非常高，达到81％，而从事此类合同的工人所占比例相对较低，仅为9％。年轻人的失业率也远高于老年工人的失业率。这证实了法国劳动力市场的二元性，即不同类别工人之间存在着差异。该模型计算了所有模拟流动情况，并与公布统计数据进行了大致比较。大多数工人在他们的现有雇佣契约（OECs）中保持稳定，而少数工人则在FTCs中短暂就业，并在其间经历失业期间。此外，在部分年轻工人变老时，这种二元性仍然存在，而其他一些年轻工人则获得更稳定的OEC。虽然还有其他新颖结果可得到，但本文核心不涉及详细介绍。

## 4.2 Assessment Of Some Labor Public Policies



We conducted several simulation of labor policies, and most of them were new (never implemented). In fact, one of the major purpose of WorkSim is to aid politic decision on employment and labor, by simulating and understanding the effects of one particular policy. Removal of Fixed-Term contracts Because of the strong segmentation in the French Labor market, with a lot of flows between FTC and unemployment and few to enter into a more stable OEC, one might want to permanently remove the FTC and have only OEC contracts. We experimented this removal in WorkSim, where only OEC and few customary FTC contracts remained. We measured the impact after 2 and 4 years. Two years after the removal, there is a significant rise of the unemployment rate (+1.1), especially among young people and employees or workers. After 4 ans, the unemployment rate decreases, and equals the baseline simulation (with FTC), because part of the individuals get hired on a OEC. But the unemployment rate decreases also because of the discouragement of 390 000 that leave the labor market (the activity rate drops by 1 point). More over, the long-term unemployment strongly increases (29 points after 2 ans, and still 24 points more after 4 years). Thus, not only the abolition of FTC failed to reduce the segmentation but it actually increased it21. FTC and OEC are not substitutable but complementary on employment.

我们进行了几次劳动力政策的模拟，其中大部分是新的（从未实施过）。事实上，WorkSim的一个主要目标就是通过模拟和理解特定政策的影响，以帮助决策者制定就业和劳动力政策。在法国劳动力市场存在严重分割现象，许多人在固定期限合同和失业之间流动，而很少有人进入更稳定的长期雇佣契约。因此，有人可能希望永久取消固定期限合同，只保留长期雇佣契约。我们在WorkSim中进行了这种取消实验，只保留了长期雇佣契约和少量惯例性固定期限合同。我们在2年和4年后测量了其影响。取消后的2年内，失业率显著上升（+1.1），尤其是年轻人和员工或工人中失业率上升较多。4年后，失业率下降，并与基准模拟（包含固定期限合同）相等，因为部分个体得到了长期雇佣契约。但是失业率也下降是因为有39万人离开劳动力市场（活跃率下降了1个百分点）。此外，长期失业人数大幅增加（2年后增加29个百分点，4年后再增加24个百分点）。因此，取消固定期限合同不仅未能减少劳动力市场的分割现象，反而使其增加。固定期限合同和长期雇佣契约在就业方面不是可替代的，而是互补的。

Reduction of charges The level of social charges on employment are frequently discussed, especially by employers' syndicates. In fact, in 2003, the minister F. Fillon has passed a law that reduces the charges paid by the firms on employment, for salaries lower than 1.6 times the minimum wage (SMIC). The decrease will be 26 % for firms with 20 employees or more, and 28.1 % for the others. To study the effect of this measure, we compared the results of the baseline simulation22 with a new simulation where these charge reductions are removed. We measured a drop of 0.72 points in unemployment rate, and a gain of 233 000 more jobs, thanks to the charges reduction. The firms also increase their benefits.

费用减免
就业方面的社会费用水平经常受到讨论，尤其是雇主工会。事实上，2003年，菲利昂部长通过了一项法律，降低了企业在低于最低工资（SMIC）1.6倍的薪资上支付的费用。对于拥有20名以上员工的企业，费用降幅为26％，其他企业为28.1％。为了研究这一措施的影响，我们将基准模拟结果与取消这些费用减免的新模拟进行了比较。我们发现失业率下降了0.72个百分点，并创造了23.3万个就业机会，这要归功于费用减免。此外，企业也增加了他们的利润。

However, it might be more efficient to target the policy on lower wages. Therefore, we vary the maximum wage to receive to policy, from 1.2 SMIC to 2.2 SMIC. The results are displayed in the Table 1 below. It appeared that the 1.2 SMIC target gives the most effective policy: smallest unemployment rate (9.55%), 298 000 more jobs, 253 000 less unemployed and also the lowest costs.

然而，将政策的目标定位于较低工资可能更为有效。因此，我们对政策的最高工资标准进行了变动，从1.2倍最低工资（SMIC）调整至2.2倍SMIC。具体结果如下表1所示。研究结果显示，以1.2倍SMIC为目标的政策效果最佳：失业率最低（9.55%），新增就业机会达到29.8万个，失业人数减少了25.3万人，并且成本也相对较低。

| Indicators                                   | 1.2 SMIC 1.3 SMIC   |
|----------------------------------------------|---------------------|
| 1.6 SMIC                                     |                     |
| 2.2 SMIC                                     |                     |
| Unemployment rate (%)                        | 9.55                |
| 9.78                                         |                     |
| 9.83                                         |                     |
| Number of created jobs (in thousands)        | 298                 |
| 233                                          |                     |
| 217                                          |                     |
| Number of avoided unemployed (in thousands)  | 253                 |
| 192                                          |                     |
| 180                                          |                     |
| Gross cost per created jobs (in euros)       | 86138               |
| 110 729                                      |                     |
| 119 816                                      |                     |
| Gross cost per avoided unemployed (in euros) | 101 581             |
| 134 375                                      |                     |
| 144 445                                      |                     |

| 指标                                       | 1.2倍SMIC  | 1.3倍SMIC |
|----------------------------------------------|---------------------|
| 1.6倍SMIC                                    |                     |
| 2.2倍SMIC                                    |                     |
| 失业率（%）                                  | 9.55                |
| 9.78                                         |                     |
| 9.83                                         |                     |
| 新增就业机会数量（千）                      | 298                 |
| 233                                          |                     |
| 217                                          |                     |
| 避免失业人数数量（千）                      | 253                 |
| 192                                          |                     |
| 180                                          |                     |
| 每个新增就业机会的总成本（欧元）          | 86,138               |
|110,729                                      || 
119,816                                      || 
每个避免失业人员的总成本（欧元）          ||101,581               ||
134,375                                      || 
144,445                                      ||

Firing costs and legal justification Another option to reduce unemployment would be to ease the creation of OEC (instead of FTC). Many firm leaders and employers' syndicate complain about the level of firing costs on one hand, and about the difficulty to fire an employee when the demand becomes insufficient, on the other hand. Therefore we conducted experiments to study these issues.

降低失业的另一种选择是简化OEC（而不是FTC）的设立。许多企业领导和雇主联合会既对高昂的解雇成本表示不满，又对需求不足时解雇员工的困难感到抱怨。因此，我们进行了实验来研究这些问题。

In a first experiment, we vary the level of firing costs, and multiply them by a factor between 0 and 50. Surprisingly, we found a very small effect on unemployment. The unemployment rate increases only by 1 point when we multiply the firing costs by 50. When the cost increases, the firms replace OEC hirings by FTC hirings. Moreover, when the cost is null, the unemployment remains around 9.5%, because hiring in OEC remain low.

在第一个实验中，我们对解雇成本的水平进行了变动，并将其乘以0至50之间的倍数。令人惊讶的是，我们发现对失业率的影响非常微小。当我们将解雇成本乘以50时，失业率仅增加了1个百分点。随着成本的增加，企业开始用FTC雇佣替代OEC雇佣。此外，当成本为零时，失业率仍然维持在约9.5%左右，因为OEC的招聘数量较少。

[重写后的中文内容]

So, maybe this is not about the cost of firing, but about the difficulty to fire someone, when the demand is low. Therefore, we conducted a second experiment, where we remove the legal justification attached to firings. When it is the economic interest for the firm to fire an employee, it does so. Moreover, this possibility is integrated into the anticipation mechanism that is part of the decision process to create an OEC job. The results are shown in Table 2, after 2 years following the variant. With this variant, unemployment rate drops by 1.62 points, and the decrease is particularly important for the youth, with a drop of 10.67 points. However, we observe an increase of 1.64 for the seniors. When we look at the unemployment rate per occupation, we find the variant to be quite beneficial for the blue collars/employees category (-3.26 points) at the detriment of the two other occupations (+0.75 for middle levels and +1.64 for executives). This could partly due to the fact that the firms mainly use OEC to hire: the entry rate in OEC goes from 11.4 % to 27.24 %; while the entry rate in FTC drops from 45.38 % to 7.22 %. The share of FTCs drops from 8.77 to 1.89 %. As a counterpart, the OEC become more precarious: the economic firing rate increases from 0.58 % to 16.74 % and the average seniority in OEC decreases from 5.86 to 3.55 years, and the probability to loose a job increases by 65 % (from 8 % to 10.33 %). There is a also in individual utilities (well-being) of -1.3 points.

因此，也许这并不是关于解雇成本的问题，而是关于在需求低迷时解雇某人的困难。因此，我们进行了第二个实验，去除了与解雇相关的法律理由。当企业有经济利益需要解雇员工时，它会采取行动。此外，这种可能性已纳入决策过程中的预期机制中，以创建OEC工作岗位。结果显示在变体后2年的表2中。通过这个变体，失业率下降了1.62个百分点，并且对青年人来说下降幅度尤为重要，下降了10.67个百分点。然而，我们观察到老年人增加了1.64个百分点。当我们观察各职业的失业率时，我们发现该变体对蓝领/员工类别（-3.26个百分点）非常有益, 而其他两种职业则受损（中层+0.75, 高管+1.64）。部分原因可能是企业主要使用OEC进行招聘：OEC进入率从11.4%增加到27.24%；而FTC进入率从45.38%下降到7.22%。FTC占比从8.77减少到1.89%。作为对应，OEC变得更加不稳定：经济解雇率从0.58%增加到16.74%，OEC的平均资历从5.86年减少到3.55年，失业风险增加了65%（从8%增加到10.33%）。个人福利也下降了1.3个百分点。

|                                                  | Indicators   | Reference Variante   | Impact    |
|--------------------------------------------------|--------------|----------------------|-----------|
| Unemployment rate (%)                            | 9.81         | 8.19                 | -1.62***  |
| Unemployment rate 15-24 ans (%)                  | 24.66        | 13.99                | -10.67*** |
| Unemployment rate 25-49 ans (%)                  | 8.89         | 7.65                 | -1.24***  |
| Unemployment rate 50-64 ans (%)                  | 5.42         | 7.06                 | +1.64***  |
| Activity rate (%)                                | 69.84        | 70.01                | +0.17***  |
| Number of employed individuals (in thousands)    | 25 694       | 26 1218              | +523***   |
| Number of unemployed individuals (in thousands)  | 2794         | 2340                 | -454***   |
| Entry rate in OEC (%)                            | 11.4         | 27.24                | +15.84*** |
| Entry rate in FTC (%)                            | 45.38        | 7.22                 | -38.16*** |
| Average individual's utility                     | 226.5        | 225.2                | -1.3***   |
| Average weekly firm benefit (in euros)           | 4133         | 4728                 | +595***   |
| Long-term unemployment rate (%)                  | 32.12        | 41.94                | +9.81***  |
| Economic firing rate (%)                         | 0.58         | 16.74                | +16.16*** |
| Probability to loose one's job within a year (%) | 8            | 10.33                | +2.33***  |

|                                                  | 指标           | 参考变体               | 影响       |
|--------------------------------------------------|--------------|----------------------|-----------|
| 失业率 (%)                                        | 9.81         | 8.19                 | -1.62***  |
| 15-24岁失业率 (%)                                 | 24.66        | 13.99                | -10.67*** |
| 25-49岁失业率 (%)                                 | 8.89         | 7.65                 | -1.24***  |
| 50-64岁失业率 (%)                                 | 5.42         | 7.06                 | +1.64***  |
| 动态参与率 (%)                                    | 69.84        | 70.01                | +0.17***   |
| 就业人数 (千人)                                                                                                                                                                                                                   
25,694                                                                                                                                                                                 
26,218                                                                                                                                            
                                                     
                                                     
                                                     
                                                     
                                                     
                                                     
                                                       
                                                       
                                                       
                                                       
                                                       
                                                       

                                                                                         

                                                                                         

                                                                                         

                                                                                         

                                                                                         

                                                                                         


                                                    


                                                    


                                                    


                                                    


                                                    


                                                    



                                                   



                                                   



                                                   



                                                   



                                                   




                                                  




                                                  




                                                  




                                                  




                                                  
                                                  
                                                  
                                                  
                                                 





                                                 





                                                 





                                                 





                                                 





                                                 





                                                 




                                                




                                                




                                                




                                                




                                                  
| 失业人数 (千人)                                   | 2,794        | 2,340                | -454***   |
| 进入OEC的概率 (%)                                | 11.4         | 27.24                | +15.84*** |
| 进入FTC的概率 (%)                                | 45.38        | 7.22                 | -38.16*** |
| 平均个人效用                                                                                                                                                                                                               
226.5                                                                                                                                                                                 
225.2                                                                                                                                            
                                                     
                                                     
                                                     
                                                     
                                                     
                                                     
                                                       
                                                       
                                                       
                                                       
                                                       
                                                       

                                                                                         

                                                                                         

                                                                                         

                                                                                         

                                                                                         

                                                                                         


                                                    


                                                    


                                                    


                                                    


                                                    


                                                    



                                                   



                                                   



                                                   



                                                   



                                                   




                                                  




                                                  




                                                  




                                                  




                                                  
                                                  
                                                  
                                                  
                                                 





                                                 





                                                 





                                                 





                                                 





                                                 





                                                 






平均每周企业福利（以欧元计）                                                                                                                                                                                               
4,133                                                                                                                                                                                  
4,728

To sum up, this policy is not yet the ideal solution to improve employment nor wellbeing: even it is costless and created 523 000 jobs in our simulation, that was at the price of a significant higher precariousness. Moreover, in another simulation, we found that this policy shows less resilience when the demand gets weaker.

综上所述，这项政策并非改善就业和福祉的理想解决方案：尽管在我们的模拟中它是无成本的，并创造了52.3万个就业岗位，但这是以更高的不稳定性为代价。此外，在另一个模拟中，我们发现当需求减弱时，这项政策表现出较低的韧性。

Finally we present the most recent simulation we performed to evaluate the very recent labor reform law in France.

最后，我们呈现了我们最近进行的一项模拟，以评估法国最新的劳动改革法。

## 4.3 Evaluation Of The El Khomri Law



The El Khomri law project has been presented in March 2016 by the French government as the major labor law of the F. Hollande's presidency. This law has recently set the war not only on the French political scene, but also between French economists who do not hesitate to take a categorical position in favor or against it. Its final version was voted on July 21, 2016. There are many articles in the law, and several are impossible to model at this stage. Here we focus on the facilitation of the economic dismissals, as it is likely to have a most important impact on the labor market.

2016年3月，法国政府提出了El Khomri法案，作为F. Hollande总统任期内的主要劳动法。这项法律最近在法国政治舞台上引起了激烈争议，并在法国经济学家之间引发了赞成或反对的明确立场。该法案的最终版本于2016年7月21日通过投票获得通过。该法律中包含许多条款，其中有几个目前无法进行建模。本文重点关注经济解雇的便利化措施，因为它可能对劳动市场产生最重要的影响。

Before the law, the economic dismissals are allowed if the firm faces "serious economic problems" which in our understanding of case law we interpret as losses over a period of year which can lead to the failure of the firm. Judges may have their own interpretation over the minimum level of losses which could lead to failure23.

在该法律出台之前，只有在公司面临“严重经济问题”的情况下才允许进行经济解雇。根据我们对案例法的理解，我们将其解释为一年内的亏损可能导致公司破产。法官可能对可能导致破产的最低亏损水平有自己的解释。

With the ELK law, article 30 (denoted as "ELK law" in the remaining of this paper)), the conditions to allow economic dismissals are explicitly specified. They will be allowed in case of a decline either in firm's demand or its turnover computed over a certain period, which depends on the firm's size. For firms under 11 employees, the period is 1 quarter, for those between 11 and less than 50 the period is 2 quarters, for firms between 50 and less than 300, the delay is 3 quarters, and for firms with 300 employees or more the delay is 4 quarters.

根据《ELK法》第30条（以下简称为“ELK法”），明确规定了允许进行经济解雇的条件。当公司需求或营业额在一定期限内出现下降时，根据公司规模的不同，将允许进行经济解雇。对于员工少于11人的公司，期限为1个季度；对于员工在11至50人之间的公司，期限为2个季度；对于员工在50至300人之间的公司，期限为3个季度；对于员工300人或更多的公司，期限为4个季度。

Effects under a stable aggregate demand At first we simulate24 the ELK law for a steady state of the exogenous aggregate demand. ELK law yields effects which change over time after the introduction of the law. They evolve during the first 3 years to stabilize generally after 4 years. The first can be termed short run effects and the latter long run effects. This comes from the fact that it takes time for the firing conditions to be filled even under the new law. The immense majority of French firms are small or very small and it takes time for such firms to face a cumulated change large enough to be willing to fire at least one employee.

在总需求稳定的情况下，我们首先对外生总需求稳定状态下的ELK法进行了模拟。ELK法在引入后会产生随时间变化的效应，这些效应在前3年内逐渐演变，并在4年后通常趋于稳定。我们将前者称为短期效应，而后者称为长期效应。这是因为即使在新法律下，填补解雇条件也需要时间。考虑到绝大多数法国企业都是小型或非常小型企业，这些企业需要时间才能面对累积变化足够大以至于愿意解雇至少一名员工的情况。

The law is favorable to the young (15-24), both in the short and the long run, with a decline in unemployment of 148,000 after 4 years (drop over 5 points). The impact is not significant for the age class (25-49), after 2 years, there is a small decrease in unemployment (-53,000) and an increase in employment (+71,000). However after 4 years the law has no significant effect on this age class. Finally the seniors (50-65) undergo a substantial rise in unemployment (+101,000), rising from 6.6 to 8%, i.e. 1.4 points, and a decrease in employment (-121,000).

在短期和长期内，该法律对年轻人（15-24岁）是有利的。经过4年的时间，失业人数减少了148,000人，降幅超过5个百分点。然而，对于25-49岁的年龄段来说，该法律的影响并不显著。在2年后，失业人数略有减少（-53,000人），就业人数增加（+71,000人）。然而，在4年后，该法律对这个年龄段没有明显的影响。最后，50-65岁的老年人面临着失业率大幅上升（+101,000人），从6.6%上升到8%，即1.4个百分点，并且就业人数减少了（-121,000人）。

Moreover, the mobility on the labor market is found to change very deeply, and the nature of the labor market is transformed. The share of FTCs in the hires falls from 77% to 30%. The OEC becomes the dominant hiring contract. The proportion of FTCs in ongoing contracts falls from 8% to 2.3%, yet with a decrease of the mean duration (renewal not included) from 3.6 weeks to 1.9 weeks, meaning that the FTCs are now used only when future demand forecasts are bad and no training is required. The economic dismissal rate jumps from 0.6% to 19%, a major change in a labor market characterized by a very low and decreasing economic dismissal rate. As a consequence the OECs become shorter (the median duration of OECs falls from 4.8 to 2 years) and more precarious, as the probability to loose one's job within a year jumps from 8.17 to 13.13 (+4.9 points, + 60 % relative increase).

此外，劳动力市场的流动性发生了深刻变化，劳动力市场的本质也发生了转变。固定期限合同（FTCs）在招聘中所占比例从77%下降至30%。开放式长期雇佣合同（OEC）成为主导的雇佣合同。FTCs在持续合同中所占比例从8%下降至2.3%，然而平均持续时间（不包括续签）从3.6周减少至1.9周，这意味着现在只有在未来需求预测不佳且无需培训时才会使用FTCs。经济解雇率从0.6%上升至19%，这是劳动力市场中经济解雇率非常低且逐渐下降的重大变化。因此，OECs变得更短暂（OECs的中位数持续时间从4.8年减少至2年），更加不稳定，因为一年内失去工作的概率增加了4.9个百分点，相对增长了60%。

| Indicators                                       | Reference Variante   |   Impact |
|--------------------------------------------------|----------------------|----------|
| Unemployment rate (%)                            | 10.37                |    10.26 |
| ns                                               |                      |          |
| Unemployment rate 15-24 yr (%)                   | 27.75                |    21.89 |
| Unemployment rate 25-49 yr (%)                   | 9.1                  |     9.24 |
| ns                                               |                      |          |
| Unemployment rate 50-64 yr (%)                   | 6.62                 |     8.03 |
| Activity rate (%)                                | 59.29                |    59.09 |
| Number of employed individuals (in thousands)    | 25 591               | 25681    |
| ns                                               |                      |          |
| Number of unemployed individuals (in thousands)  | 2960                 |  2937    |
| ns                                               |                      |          |
| Entry rate in OEC (%)                            | 11.88                |    28.24 |
| Entry rate in FTC (%)                            | 40.95                |    12.45 |
| Average individual's utility                     | 229.2                |   222.72 |
| Average weekly firm benefit (in euros)           | 4133                 |  4728    |
| Long-term unemployment rate (%)                  | 34.72                |    33.26 |
| Economic firing rate (%)                         | 0.61                 |    19.55 |
| Probability to loose one's OEC within a year (%) | 8.17                 |    13.13 |

| 指标                                               | 参考值                 | 影响     |
|--------------------------------------------------|----------------------|----------|
| 失业率 (%)                                          | 10.37                |    10.26 |
| ns                                               |                      |          |
| 15至24岁失业率 (%)                                   | 27.75                |    21.89 |
| 25至49岁失业率 (%)                                   | 9.1                  |     9.24 |
| ns                                               |                      |          |
| 50至64岁失业率 (%)                                   | 6.62                 |     8.03 |
| 劳动参与率 (%)                                       | 59.29                |    59.09 |
| 就业人数 (千人)                                      | 25,591               |   25,681   |
| ns                                               ||||
||失业人数 (千人)                                      ||2,960                 ||2,937    ||
||ns                                               ||                      ||          ||
||进入OEC的比例 (%)                                    ||11.88                ||28.24     ||
||进入FTC的比例 (%)                                    ||40.95                ||12.45     ||
||平均个体效用                                        ||229.2                ||222。72   ||
||平均每周企业福利（以欧元计）                          ||4,133                 ||4,728      ||
||长期失业率(%)                                       ||34。72               ||33。26      ||
||经济解雇率(%)                                       ||0。61                 ||19。55      ||
||一年内失去OEC的概率(%)                               ||=8。17                 ||=13。13       |

Two major conclusions can be drawn. First a significant substitution of the young to the seniors takes place, although it declines with time. Second the new load of adjustment set on the OECs has the logical effect of making the FTCs an almost useless tool of flexibility for the employers except for very short expected durations. The explanation of the opposed effects over the young versus the other categories is clear. The young were much more often than the others in FTCs (22% against 7.6% for the 25-50 and 4.9% for the seniors) and benefit from their fall. The effect then goes much beyond the higher flexibility of OECs. It raises the integration of the young in (more precarious) OECs, and this shows that the screening and experience enhancing roles of FTCs were not sufficient. This mechanism, the substitution of OECs to FTCs, and its consequence, the substitution of young workers to seniors, has been overlooked or greatly underestimated by non quantitative analysis of the law. Sensitivity of adjustment to aggregate demand We now change exogenously aggregate demand in order to compare the effects on the unemployment rate of the firing conditions before the law and after the law. Figure 4 gives values after 2 years. It shows that the adjustment of the labor force is predicted to be more important after the law. When demand declines under its value in the reference simulation, economic dismissals are more important, the suppression of the hoarded labor is more complete, and unemployment rises more under the law El-Khomri (increase between 4 and 12 points). When demand rises above the reference value, the employers hire more easily on OECs, and unemployment decreases more under ELK law (decrease around 2 points). The responses are not symmetric for large (and unrealistic) changes since if demand is very high, there always remains some search unemployment by workers who take the time to find a job which satisfies their reservation utility.

可以得出两个重要结论。首先，年轻人对老年人的显著替代正在发生，尽管随着时间的推移有所下降。其次，新的调整负担使得临时合同雇员在除非预期持续时间非常短之外几乎成为雇主灵活性的无用工具。对于年轻人与其他类别之间相反效应的解释是清楚的。相比其他人，年轻人更经常处于临时合同雇佣关系中（22%对25-50岁群体的7.6%，对老年人则为4.9%），并从中受益。这种效应远远超出了临时合同雇佣关系更高灵活性的范畴。它提高了年轻人在（更不稳定）临时合同雇佣关系中的融入程度，并表明临时合同雇佣关系在筛选和增强经验方面并不足够。被忽视或被非定量分析大大低估了这种机制——将临时合同雇员替换为长期劳动者，并由此导致将年轻劳动者替换为老年劳动者。

调整对总需求敏感性
我们现在通过外生地改变总需求，以比较法律实施前后解雇条件对失业率的影响。图4给出了2年后的数值。它显示，在法律实施后，劳动力调整预计会更加重要。当需求低于参考模拟中的值时，经济解雇更为重要，扫除囤积劳动力更为彻底，并且失业率在埃尔-霍姆里法案下上升得更多（增加4到12个百分点）。当需求高于参考值时，雇主更容易在临时合同雇佣关系中招聘员工，并且失业率在埃尔-霍姆里法案下降得更多（减少约2个百分点）。对于大幅度（不切实际）的变化，这些响应并不对称，因为如果需求非常高，则仍然存在一些搜索失业情况，即工人花时间找到满足其保留效用的工作。

## 5 Discussion



In this paper, we present the WorkSim framework, a comprehensive model of the labor market. It implements numerous mechanisms that were not integrated together before within a single labor market model: both sides of the market, detailed decision processes under bounded rationality, learning and anticipation, endogenous contract choices, human capitals, endogenous salaries and productivities. The stock-flow accounting of individuals, based on gross flows, is complete and endogenous. It can be supplemented by a stockflow accounting of jobs (and even jobs within the company) for further analysis. The institutional environment is modeled and based on labor law, which sets constraints on the possible decisions.

本文介绍了WorkSim框架，这是一个全面的劳动力市场模型。该模型整合了以往单一劳动力市场模型中未曾集成的多种机制：包括市场的双方、有限理性下的详细决策过程、学习和预期、内生合同选择、人力资本、内生工资和生产力。个体的库存流量核算基于总流量，具备完整且内生的特点。此外，还可以通过对职位（甚至公司内部职位）进行库存流量核算，以进行进一步分析。该模型还考虑了制度环境，并基于劳动法设定了决策的约束条件。

WorkSim is calibrated on a large number of targets of the French labor market, by using a powerful algorithm which has not already been used in economic models. It reproduces well enough these targets to conduct some economic analyses. Moreover, it reproduces well the gross flows measured by different statistical sources and with different types of measures. This gives us an estimation of the model accuracy, and is part of the model's validation process.

WorkSim框架通过使用一种在经济模型中尚未使用过的强大算法，对法国劳动力市场的大量目标进行了校准。它能够很好地复制这些目标，以进行一些经济分析。此外，它还能够准确地复制不同统计来源和不同类型的测量所得到的总流量。这为我们提供了对模型准确性的估计，并且是模型验证过程中的重要组成部分。

We conducted several analyzes and policy evaluations. These helped us to identify core mechanisms in the French Labor Market : segmentation, importance of firms' pessimism, among others. Labor policies appeared to have contrasting results in terms of employment improvements, utilities, benefits and costs. Future directions The model can be extended in several directions : adding temporary employment agencies, social networks, and training (more detailed) for instance. We can also integrate more organizational elements, including skills and tasks.

我们进行了多项分析和政策评估，以帮助我们识别法国劳动力市场的核心机制，包括分割和企业悲观情绪等。在就业改善、效用、利益和成本方面，劳动力政策呈现出截然不同的结果。未来的研究方向可以在多个方面进行扩展，例如添加临时就业机构、社交网络以及更详细的培训内容。此外，我们还可以整合更多组织要素，包括技能和任务。

Second, WorkSim needs to be plugged into an agent-based macro-economical framework, in order to have consumption, production and financial effects as well25 .

其次，为了实现消费、生产和金融效应，WorkSim需要嵌入一个基于主体的宏观经济框架。

Third, tools to help analyzing and explaining the simulations are still to be developed further : visualization (improving the graphical interface in WorkSim), analyses of the agents ' decisions, automatic classification of agents' trajectories to study individuals' careers (cohort analysis). Another issue is the link with econometrics, to improve the agents' micro-foundation and enhance the validation process.


其次，需要进一步发展工具来帮助分析和解释模拟结果。这些工具包括改进WorkSim的图形界面以提升可视化效果，分析主体的决策过程，自动分类主体轨迹以研究个体职业生涯（进行队列分析）。此外，与计量经济学的结合也是一个问题，旨在改善主体的微观基础并加强验证过程。

