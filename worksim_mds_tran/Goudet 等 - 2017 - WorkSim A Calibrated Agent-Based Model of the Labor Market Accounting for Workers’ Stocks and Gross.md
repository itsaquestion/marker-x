# Worksim - A Calibrated Agent-Based Model Of The Labor Market Accounting For Workers' Stocks And Gross Flows



## Abstract



This paper presents an agent-based model of the labor market. It simulates the market in the recent period at the aggregate level and at the level of the principal categories of labor, on the basis of the decisions of heterogeneous agents, firms and individuals, who interact. These decisions rely on individual computations of profits and utilities, although rationality is bounded in such a complex environment. The theoretical structure that underlies the decisions is the search concept. We apply this framework to the case of France in 2011. The model is at a scale of 1/4700. It is fairly detailed on the institutions of the labor market that constrain the agents' decisions. Finally it is calibrated by a powerful algorithm to reproduce a large number of variables of interest. The calibrated model presents a consistent accounting system of the gross flows of the individuals between the main states, employment, distinguishing open ended contracts and fixed duration contracts, unemployment and inactivity. The simulation of the gross flows accounts enables us to analyze the patterns of mobility in a way that the observed statistics on gross flows, which are partial, cannot do. The model then characterizes the nature of the labor market under study, reproducing the high proportion of the fixed duration contracts in the hiring flows, and it points to a dualism of the French labor market.

本文提出了一个基于主体的劳动力市场模型。该模型在总体水平和劳动力的主要类别水平上模拟了最近时期的市场，基于异质主体（企业和个人）之间的互动决策。这些决策依赖于个体对利润和效用的计算，尽管在如此复杂的环境中理性是有限制的。决策背后的理论结构是搜索概念。我们将这个框架应用到2011年法国的情况中。该模型按照1/4700比例进行缩放，并对约束主体决策的劳动力市场机构进行了相当详细地描述。最后，通过强大算法进行校准，以重现大量感兴趣变量。校准后的模型提供了一个一致性账户系统，记录了个体在就业、区分无固定期限合同和固定期限合同、失业和非活跃状态之间流动情况。通过对总流量进行模拟分析，我们能够以观察到但不完整统计数据所不能做到的方式来分析流动性模式。该模型进一步揭示了所研究劳动力市场特征，并重现了雇佣流程中固定期限合同的高比例，指出了法国劳动力市场的二元性质。

## 1 Introduction



The model WorkSim is a novel tool of analysis for labor markets. The first objective of the model is to reproduce the gross flows between the important states: employment (distinguishing fixed term contracts and open ended contracts), unemployment and inactivity, and the ratios of individuals in these states. The novelty of the model is that it simulates the gross flows on the basis of the rational decisions of individual heterogeneous agents. The gross flow concept is crucial because each flow unit is caused by a decision that involves comparing idiosyncratic expected benefits and costs for the agent, and a flow unit will yield idiosyncratic benefits and costs for the agent and possibly other agent. It is not the case for transition based models that imply some time aggregation. Once the model is calibrated, the second objective is to characterize the nature of the labor market under study. This is done, first by examining the patterns of flows and stocks at the aggregate level and at the levels of different categories of labor, second by sensitivity experiments, modifying some exogenous parameters and variables such as the demand for the good. Finally the model once calibrated is a tool for experimenting labor market policies, including changes in the labor law. The multi-agent methodology is the perfect tool for such a research program, since it can model institutions precisely, and account for heterogeneity and individual interactions. Simulation results enable us to compute aggregate variables such as the flows and the stocks, and finally the individual careers and the main types of trajectories.

WorkSim模型是劳动力市场分析的一种创新工具。该模型的首要目标是重现重要状态之间的总流量，包括就业（区分固定期限合同和无固定期限合同）、失业和非活跃状态，以及这些状态中个体的比例。该模型的创新之处在于，它基于个体异质主体的理性决策来模拟总流量。总流量概念至关重要，因为每个流动单位都是由涉及主体独特预期收益和成本比较的决策引起的，并且一个流动单位将为主体本身以及可能其他主体带来独特收益和成本。与基于转换的模型不同，它不涉及时间聚合。一旦模型被校准，第二个目标是表征所研究劳动力市场的性质。首先，在整体水平上以及不同劳动力类别水平上检查流量和存量模式；其次，通过敏感性实验修改某些外生参数和变量（如商品需求）。最后，经过校准后的模型可用于实验劳动力市场政策，包括劳动法变更。多主体方法论是进行此类研究计划的理想工具，因为它可以精确地建模机构，并考虑到异质性和个体间的相互作用。模拟结果使我们能够计算出总体变量，如流量和存量，最终还可以计算出个体职业生涯和主要轨迹类型。

However, the labor market is complex and this means that the modeling progresses only by steps. The present version is consistent as a stock-flow model and more detailed than other existing stock-flow models of the labor market, analytic, econometric, or multi-agent. The model builds on the experience of model ARTEMIS proposed by Ballot ((Ballot, 1981, 1988, 2002)) and a preliminary version of WorkSim by Lewkovicz and Kant (Lewkovicz & Kant, 2008). ARTEMIS
is the first multi-agent model to have modeled the gross flows between the three main states of the individuals, with the addition of on-the-job search as a state. This was also done within an institutional framework, notably with a temporary help firm, and firing costs. The accounting framework of stocks and flows allowed for a rigorous analysis of the competition between the different categories of labor. It threw some light on the effects of aggregate shocks or institutional change on the displacement or integration in open ended contracts of such categories as the young workers, female workers, low educated workers. The underlying hypothesis, that results confirm, is that these effects on the gross flows and stocks are highly non linear, or even non monotonic, and difficult to obtain through available econometric methods. For instance, a negative demand shock could possibly lower the unemployment rate of young non educated workers who would abandon participation, but raise unemployment for the other workers.

然而，劳动力市场的复杂性意味着建模只能逐步进行。目前的版本是一个存量-流量模型，比其他现有的劳动力市场模型（分析、计量或多主体）更加详细。该模型基于Ballot提出的ARTEMIS模型（Ballot, 1981, 1988, 2002）和Lewkovicz和Kant提出的WorkSim初步版本（Lewkovicz & Kant, 2008）的经验。ARTEMIS是第一个多主体模型，对个体之间三种主要状态之间的总流量进行了建模，并增加了在职搜索作为一种状态。这也是在一个机构框架内完成的，特别是与临时劳务公司和解雇成本相关。股份和流动性会计框架使得对不同劳动力类别之间竞争情况进行严格分析成为可能。它揭示了总需求冲击或制度变革对年轻工人、女性工人、低教育程度工人等类别在无固定期限合同中流动或融入方面产生的影响。结果证实了底层假设，即这些对总流量和存量产生影响的非线性或甚至非单调效应很难通过现有计量方法获得。例如，负的需求冲击可能会降低年轻非受教育工人的失业率，他们可能会放弃参与，但却会提高其他工人的失业率。

The version of WorkSim presented in this artical aims to analyze the French labor market in
2011. However the methodology we have developed will enable researchers to use it for other countries as well. WorkSim puts emphasis on one of the most important features of the French labor market that is the major role of the fixed term contracts, about 80% of the hires in 2011. The present version is mainly devoted to the reproduction of the flows on the basis of our modeling of rational decisions. It then provides a first characterization of the patterns of flows of the different categories of workers, which is key for understanding the nature of a labor market, letting policy design for future work. Due to lack of space, we mainly restrict our economic analysis to the observation of a segmentation, and then throw a first light on the fundamental question: is the segmentation of a temporary or permanent nature for a generation of individuals?

本文介绍的WorkSim版本旨在分析2011年法国劳动力市场。然而，我们开发的方法使研究人员能够将其应用于其他国家。WorkSim强调了法国劳动力市场最重要的特点之一，即固定期限合同的重要角色，该合同在2011年约占雇佣比例的80%。目前版本主要致力于基于我们对理性决策建模的流量再现。它提供了对不同类别工人流动模式的初步描述，这对于理解劳动力市场的性质以及为未来工作制定政策至关重要。由于篇幅有限，我们主要将经济分析局限于观察分割情况，并首次探讨一个基本问题：临时或永久性质是否适用于一代人？

This paper is organized as follows. Section 2 will present the theoretical framework and related models, section 3 will develop the model. Section 4 will deal with the calibration procedure, and section 5 the first characterization of the French labor market on the basis of the results. Section 6 concludes.

本文的组织结构如下。第2节将介绍理论框架和相关模型，第3节将发展模型。第4节将处理校准程序，第5节将基于结果对法国劳动力市场进行初步描述。第6节总结。

## 2 Theoretical Framework And State Of The Art 2.1 Extending Search Theory



WorkSim like ARTEMIS is grounded in the concept of search (Phelps, 1970). It gives its intellectual coherence to the model, and the foundations for many of the decision rules. The search concept is necessary to distinguish the two states of "unemployed" and "inactive" on the basis of rational decisions of agents. There is indeed a flow from unemployment to inactivity, because the unemployment utility (expected gains from search minus time foregone) may become lower than the utility of inactivity (including welfare and free time). In that case, the individual stops search and becomes inactive. This is distinct from the fact that part of the inactive persons do not want to work because they have some other resources and value non-working time (caring for children). When the cost of search is introduced, the concept of search then also explains - and it was the seminal idea of Stigler (1962) - that workers will sometimes prefer not to apply for a job and spend some more time unemployed to try to obtain a better job. They adopt a stopping rule that sets the minimum utility a job must offer to induce them to apply. These formalizations follow the definition of unemployment as a state in which workers act actively to find a job. This is a definition adopted by the International Labor Office (ILO), and the French National Statistical Institute (INSEE) in the *Employement Survey*, an enquiry that measures some of the variables the model wants to reproduce. In WorkSim the basic concept of search is extended in three directions, in order to build a general theory of mobility :

WorkSim与ARTEMIS一样，基于搜索理论（Phelps, 1970）。这一概念为模型提供了智力上的一致性，并为许多决策规则奠定了基础。搜索概念的引入是为了根据个体的理性决策来区分"失业"和"非活动"两种状态。实际上，由于失业效用（搜索预期收益减去时间损失）可能低于非活动效用（包括福利和空闲时间），从失业到非活动存在一种流动。在这种情况下，个体会停止搜索并转为非活动状态。这与部分非活动人员之所以不愿意工作是因为他们拥有其他资源并且重视非工作时间（例如照顾孩子）是不同的。当引入搜索成本时，搜索概念也解释了工人有时会选择不申请工作并花更多时间失业以试图获得更好的工作 - 这正是Stigler (1962) 的开创性思想。他们采取一个停止规则来设定必须提供给他们的工作的最低效用，以诱使他们申请该工作。这些形式化定义遵循国际劳工组织（ILO）和法国国家统计研究所（INSEE）在《就业调查》中采用的将失业定义为积极寻找工作状态的定义。该调查测量了模型试图复制的一些变量。在WorkSim中，搜索的基本概念在三个方向上得到了扩展，以建立一个关于流动性的通用理论。

1. *Search is done also by firms* that symmetrically look for workers who are high in the productivity distribution. They prefer to keep a job vacant than hire a worker with a poor productivity. An optimal stopping rule taking the form of a minimum productivity requirement or hiring norm follows. A further possibility is that the addition of the costs of search and other costs (wages, expected firing costs...) makes the job unprofitable and it is suppressed.
2. *The search calculus is extended to all voluntary decisions by workers* such as quits to search
and on-the-job search. Symmetrically, the firms take into account the search costs of replacement when they consider firing a worker, for insufficient productivity. Other relevant
costs and benefits are also taken into account for firing, not renewing a fixed duration contract.... Finally the hiring decision is the result of the sequential decisions of the worker who applies and the firm which selects and hires. Moreover we do not use any matching function - unlike in the matching models such as the canonical model of Mortensen and Pissarides (Mortensen & Pissarides, 1994) - as it is an aggregate artefact, likely not to be robust to large changes in the labor market, and with weaker microeconomic foundations than our double search decisions. The model definitely belongs to the pure search models,
fully taking into account the heterogeneity of jobs and workers1.
(a) Our model integrates *wage rigidities* based on the realistic assumption that firms have
often several jobs, which is not the case in the searchor matching models. Then equity requires a fixed wage structure between insiders'jobs. The model then allows for the differentiation between demand shocks and productivity shocks, while existing search models do not usually deal with this topic. WorkSim then contains some Keynesian features. Demand shocks explain part-time, economic dismissals, job creations and promotions in the model, while productivity changes explain dismissals on personal grounds, and some hires. This distinction has also some importance since the model deals only with the labor market, with no feedback on the goods market. The quantity demanded for the goods is exogenous.
However a major difference between WorkSim and the analytical search models relies on our utilization of the concept of Simon's *bounded rationality* to model the decisions (Simon, 1955).

1. *企业也会进行搜索*，寻找在生产力分布中处于较高水平的工人。他们更愿意保持职位空缺，而不是雇佣生产力较低的工人。采用最低生产力要求或招聘规范的最优停止规则。另一种可能性是，搜索成本和其他成本（工资、预期解雇成本等）的增加使得该职位无利可图，并被取消。

2. *搜索计算扩展到了工人所有自愿决策*，例如离职寻找新工作和在职搜索。同样地，企业在考虑解雇生产力不足的员工时也会考虑到替换的搜索成本。对于解雇、不续签固定期限合同等情况，还会考虑其他相关成本和收益。最终的招聘决策是申请者和企业连续决策的结果。此外，我们没有使用任何匹配函数 - 不像Mortensen和Pissarides（Mortensen＆Pissarides, 1994）等匹配模型中那样 - 因为它是一个整体性构件，在劳动市场发生大变化时可能不稳健，并且比我们双重搜索决策具有较弱的微观经济基础。该模型明确属于纯搜索模型，充分考虑了工作和工人的异质性1。
(a) 我们的模型结合了基于现实假设的*工资刚性*，即企业通常拥有多个职位，而这在搜索或匹配模型中并不成立。然后，公平要求内部职位之间存在固定的工资结构。该模型还允许区分需求冲击和生产力冲击，而现有的搜索模型通常不涉及此问题。因此，《WorkSim》具有一些凯恩斯主义特征。需求冲击解释了兼职、经济解雇、岗位创造和晋升等情况，在该模型中生产力变化解释了出于个人原因的解雇和一些新员工招聘。这种区分也很重要，因为该模型仅涉及劳动市场，并没有对商品市场产生反馈作用。商品需求量是外生确定的。
然而，《WorkSim》与分析性搜索模型之间一个重要差别在于我们利用Simon提出的*有限理性*概念来建立决策过程（Simon, 1955）。

Two major arguments can be given:

有两个主要的论点可以提出：

1. First, dynamic programming algorithms used to solve the decision problem in analytical
search theory cannot be used in a model in which heterogeneous agents move sequentially into many states over time and compete.
2. Second, according to bounded rationality theory, real agents have limited capacities in
terms of computation and memory. They might therefore use simple rules, but a very important behavioral addition in our approach is that they can revise their decisions or even their rules thanks to *learning* and collecting information. This continuous learning is in fact very coherent with search theory. However, in order to compute equilibrium, analytical models assume perfect rationality and individuals have a lot of information such as the
true distribution of wages, and firms know the true distribution of productivities. By contrast, in WorkSim, we model "simple" decision rules - that comply with bounded rationality - and the learning processes.

有两个主要论点需要提出：

1. 首先，在分析性搜索理论中用于解决决策问题的动态规划算法无法应用于一个模型中，其中异质主体随时间顺序移动到许多状态并进行竞争。

2. 其次，根据有限理性理论，真实的主体在计算和记忆方面具有有限能力。因此，他们可能使用简单的规则。然而，在我们的方法中，一个非常重要的行为补充是他们可以通过学习和收集信息来修正他们的决策甚至是规则。这种持续学习实际上与搜索理论非常一致。然而，在计算均衡时，分析模型假设完全合理性，并且个体拥有大量信息，如工资的真实分布以及企业知道生产力的真实分布。相比之下，在《WorkSim》中，我们建模了符合有限理性要求的“简单”决策规则，并考虑了学习过程。

## 2.2 Related Agent-Based Models



The contributions to the multi-agent literature on labor markets must also be assessed. This literature is thin but has a long history. Bergmann (2002) has developed a simple model of search by both sides of the market and obtained simultaneously vacant jobs and unemployment. Eliasson (1977) has built a Keynesian and Schumpeterian micro-to-macro model that treats only firms as individual agents but the number of workers in a firm can vary and unemployment is computed. It stresses poaching of labor by firms that grow and the wage competition that eliminates the firms that are not profitable. An extension by Ballot and Taymaz (2000) added human capital and the growing firms poach the more educated workers, enhancing a virtuous cycle of innovation and profit. ARTEMIS, the ancestor of WorkSim, stressed the different personnel management types to study segmentation. Some firms offer internal labor markets with a high selection at entry, but also training and promotion, and others offer lower wages, less selection, no promotion ("secondary jobs"). Moreover firms can recur to temporary help work, with very short contracts, but less selection than for internal labor markets. The model generates a temporary segmentation of the young workers. Then, a negative demand shock affects very differently the categories of labor, precluding the progressive integration of young workers in the internal labor markets. This leads to a permanent segmentation with serious life cycle consequences. WorkSim brings many improvements over ARTEMIS. It replaces the "secondary" jobs by the fixed duration contract with the main legal specificities that apply to them in 2011. It also models the accumulation of several types of human capital, and considers that workers have an idiosyncratic component in productivity so that the employers learn - but never know perfectly - the productivity of their employees. This is a source of personal dismissals, while in ARTEMIS the workers when hired became equally productive through an adapted training. Moreover the model is calibrated by a powerful algorithm to fit year 2011, while ARTEMIS was calibrated by hand to fit the evolution 1972-75. In WorkSim, a simulation is repeated 200 times to average out the stochastic effects while ARTEMIS could not - for computational cost reasons - be tested with more that a few runs. In order to focus precisely on the role of fixed duration contracts, we do not integrate - at this time - the temporary help jobs modeled in ARTEMIS.

还需要评估对于劳动力市场的多主体文献的贡献。尽管这方面的文献数量有限，但其历史悠久。Bergmann（2002）提出了一个简单的模型，同时考虑市场两侧的搜索行为，并同时得出了空缺职位和失业情况。Eliasson（1977）构建了一个凯恩斯和熊彼特式的微观到宏观模型，将企业视为个体主体，但允许企业中工人数量的变化，并计算失业率。该模型强调了成长中企业对劳动力的挖角以及通过工资竞争淘汰无利可图企业。Ballot和Taymaz（2000）在此基础上增加了人力资本，并考虑到成长中企业更倾向于挖角受教育程度较高的工人，从而形成创新和利润之间良性循环。ARTEMIS是WorkSim的前身，着重研究不同类型的人事管理以探讨分割现象。一些公司提供内部劳动力市场，通过严格筛选、培训和晋升机制来吸引员工；而其他公司则提供较低工资、较少筛选和无晋升机会的“次要职位”。此外，公司还可以利用临时劳动力，签订短期合同，但筛选程度低于内部劳动力市场。该模型生成了年轻工人的临时分割现象。然后，负面需求冲击对不同类别的劳动力产生了不同的影响，阻碍了年轻工人逐步融入内部劳动力市场。这导致了严重的生命周期后果和永久性分割现象。相比ARTEMIS，WorkSim在多个方面进行了改进。它将“次要职位”替换为具有固定期限合同的职位，并考虑到2011年相关法律特点。此外，该模型还考虑到多种类型人力资本的积累，并认为工人在生产率方面存在个体差异性，使得雇主能够学习员工的生产率情况（尽管无法完全掌握）。这也是个人解雇发生的原因。与ARTEMIS不同，在ARTEMIS中，员工在受雇时通过培训达到相同的生产率水平。此外，WorkSim通过强大算法进行校准以适应2011年情况，而ARTEMIS则是手动校准以适应1972-75年的演变情况。在WorkSim中，模拟实验重复进行200次以平均随机效应，而由于计算成本原因，ARTEMIS无法进行多次测试。为了更加准确地研究固定期限合同的作用，我们目前不会将ARTEMIS中建模的临时助理工作纳入考虑范围。

The years 2000 have mainly seen the construction of multi-agents models aiming at theoretical research, such as introducing networks on the labor market, i.e. the role of social relations in the hiring process, a way to go beyond random search that is relevant in some contexts (Tassier & Menczer, 2001), and the study of the robustness of aggregate relations such as the Beveridge curve that describes the negative relationship between vacancies and unemployment, if one starts bottom up by modeling the firms and individuals decisions (Richiardi, 2006). However, one model has tried to model the French labor markets with some of its specificities. Barlet et al. (2009) simulate the French labor market for year 2006. They distinguish individuals and jobs but not firms as such although there is a labor demand side, with creations and destructions of jobs based on a desired margin and demand. Fixed duration and open ended contracts are also distinguished. The flows are obtained from transition rates, often exogenous, and the dismissals are determined by the destruction of jobs exclusively (and not by insufficient productivity). The model is calibrated using an indirect inference method to fit a set of real data, and is then used to study the effects of the rise of the minimum wage and a lowering of the social charges on the firms. However, there are no inactive individuals in their model, hiring is performed through an aggregated matching function, quits are exogenous, and the terminations of fixed duration contracts are random. One another important difference with ARTEMIS and WorkSim is that the period is the year and therefore the gross flows are not reproduced, which prevents a fine analysis of fixed duration contracts and unemployment spell durations.

2000年以来，主要出现了一些旨在进行理论研究的多主体模型的构建。其中包括引入劳动力市场网络，即社会关系在招聘过程中的作用，这是一种超越随机搜索的方式，在某些情况下具有相关性（Tassier＆Menczer，2001）。另外还有对贝弗里奇曲线进行建模，该曲线描述了空缺与失业之间的负相关关系。通过从底层开始建模企业和个人决策，研究了这种聚合关系的稳健性（Richiardi, 2006）。

然而，只有一个模型尝试模拟法国劳动力市场及其特定性。Barlet等人（2009）对2006年法国劳动力市场进行了模拟。他们区分个体和工作岗位，但没有将企业本身作为区分对象。尽管存在劳动需求方面的问题，并且基于期望边际和需求创建和销毁工作岗位，但并未明确区分企业。此外，他们还区分了固定期限合同和无固定期限合同，并通过转换率获得流量数据（通常是外生变量）。解雇仅由工作岗位销毁确定，并不是由于生产力不足。该模型使用间接推断方法进行校准，以适应一组真实数据，并用于研究最低工资的上涨以及降低社会费用对企业的影响。

然而，在他们的模型中没有考虑非活跃个体，招聘是通过聚合匹配函数进行的，离职是外生的，固定期限合同的终止是随机的。与ARTEMIS和WorkSim模型相比，该模型还有一个重要区别，即周期为年，因此无法再现总流量，这限制了对固定期限合同和失业持续时间进行详细分析的能力。

The version of WorkSim (in the line of ARTEMIS) presented here then goes beyond the existing multi-agent literature on the labor markets in three directions, as the following sections will show:

这里介绍的WorkSim版本（与ARTEMIS相似）在劳动力市场的多主体文献中有三个方面的突破，如下节所示：

1. It is the only model to be grounded in a double stock-flow accounting, one for the individuals, one for the jobs, and all the flows between the stocks considered are simulated. This accounting is the equivalent of the financial stock-flow accounting for ACE macroeconomic models, a guarantee of consistency. It also allows for a easy description of the labor market dynamics at the aggregate and at any disaggregation level of interest, and the
highlighting of the competition between categories of labor (young, adults, seniors....) with possible crowding out effects.
2. It models the institutions and the labor law at their level of direct impact (the microeconomic level), since they are rules of the game that agents know and take into account in their decisions. The diverse forms of labor contracts, with very important differences, are probably the major feature of the French labor market, and they are at the heart of the
model, since they modify the flows 2.
3. Most of the gross flows are generated by rational decisions based on an enlarged search
theory, and the effects of shocks we will study then integrate the agents responses and interactions within the rules of the game and the accounting constraints. Our multi-agent model then provides a tool to explore rigorously the complex system constituted by the labor market.

1. 该模型是唯一一个基于双重库存流量核算的模型，其中一个用于个体，另一个用于工作岗位，并且考虑了两者之间的所有流动。这种核算方法类似于ACE宏观经济模型中的金融库存流量核算，确保了一致性。同时，它还能够轻松描述劳动力市场在总体和任何感兴趣的细分水平上的动态，并突出了不同劳动力类别（年轻人、成年人、老年人等）之间可能存在的竞争和排挤效应。

2. 该模型在直接影响层面（即微观经济层面）对机构和劳动法进行建模，因为它们是主体所知道并在决策中考虑到的游戏规则。法国劳动力市场具有多种形式的劳动合同，这些合同之间存在着非常重要的差异，而这也是该模型的核心内容，因为它们会改变流动情况。

3. 大部分毛流量都是基于扩展搜索理论做出理性决策产生的，并且我们将研究到的冲击效应将与主体对游戏规则和会计约束作出反应和互动相结合。因此，我们的多主体模型为深入探索劳动力市场所构成的复杂系统提供了一个严谨的工具。

## 3 Model Description 3.1 The Agents In Worksim



In WorkSim, the agents are heterogeneous. They have specific attributes determined once and for all at their creation and internal variables which evolve all along the simulation. The agents attributes and variables are shown in Appendix A. There are two types of agents: Private Firms and *Individuals*. At its creation, each firm starts with at least one worker to run the company, denoted in this paper as the managing director. The *Individuals* are grouped in households and the simulation evolves in a closed population. The individuals can marry each other, have children, break up, and therefore the decisions of one member of the household may have an impact on the other members.

在WorkSim中，主体是异质的。它们在创建时具有确定的特定属性，并且在整个模拟过程中会不断演变的内部变量。主体的属性和变量详见附录A。这里有两种类型的主体：私营企业和个人。每个企业在创建时至少有一名工人来经营公司，本文将其称为总经理。个人被分组成家庭，而模拟过程则发生在一个封闭的人口中。个人可以结婚、生育、分手，因此家庭成员的决策可能会对其他成员产生影响。

The agents under 15 or over 65 years belong to these household but are not *instantiated* as full agents and do not take decisions in the model. However, these *non-instantiated agents* indirectly participate through the economic decisions of the other members of the household (eg. the number of dependent children is taken into account in decisions of transition to inactivity, the retirement pension is included in household income). The individuals under 15 years become full agents in the model at the age of 15, and some remain in the school system while others enter the labor market.

年龄在15岁以下或65岁以上的个体属于这些家庭，但不被视为完整的主体并且在模型中不参与决策。然而，这些非实例化的主体通过家庭其他成员的经济决策间接参与其中（例如，在决定转入非活动状态时考虑了依赖子女的数量，退休金被计入家庭收入）。15岁以下的个体在15岁时成为完整的主体，并且有些人继续留在学校系统，而其他人则进入劳动力市场。

## 3.2 Environment



In addition to these agents. the model uses three *artifacts* 3:

除了这些主体外，该模型还使用了三个“工具”3：

- *JobAds*, which receives job offers from the firms and job applications from the job seekers.
Dissemination of information, however, is based on the job search process described in more detail below (see sections 3.6.4 and 3.7), according to the principles of the theory of search.
- a "*statistical institute*" that calculates all the statistics from a simulation model. and disseminates some information (e.g. tension on the labor market). The information is imperfect for agents, and we specify what information is being broadcasted.
- a *Public Sector* that recruits (exogenously) employees, collects payroll taxes on businesses.

- *招聘广告*是一个接收企业职位提供和求职者求职申请的平台。然而，根据搜索理论的原则，信息的传播是基于下文中更详细描述的求职过程（参见第3.6.4节和第3.7节）。
- *统计机构*通过模拟模型计算所有统计数据，并传播一些信息（例如劳动力市场上的紧张局势）。这些信息对经济主体来说并不完全，我们会明确指出正在广播哪些信息。
- *公共部门*以外生方式招募员工，并向企业征收工资税。

## 3.3 Institutional Framework



Moreover, it also includes one *institutional module*. One distinctive feature of the WorkSim model is to integrate a fairly complete and flexible institutional framework that includes (1) the necessary elements of the French labor Law, including **two types of contract**: fixed duration contracts (FDC)4 and open ended contracts (OEC),5 dismissals on personal and on economic grounds, redundancy payments, ... ). and (2) government decisions (minimum wages, welfare benefits, ...). The parameters of the institutional framework are shown in Appendix B.

此外，该模型还包括一个*制度模块*。WorkSim模型的一个显著特点是将一个相当完整且灵活的制度框架整合其中，该框架包括（1）法国劳动法的必要要素，包括**两种类型的合同**：固定期限合同（FDC）4和无固定期限合同（OEC）5、个人和经济原因解雇、遣散费等；以及（2）政府决策（最低工资、福利待遇等）。制度框架的参数详见附录B。

## 3.4 Key Economical Computations In The Worksim Model



Before detailing the behaviors of the our agents in the model, let us describe some key economic computations in WorkSim.

在详细描述模型中我们的主体行为之前，让我们先介绍一些WorkSim中的关键经济计算。

## 3.4.1 Benefit Of The Firm



Firm Income -
The only production factor is the labor, like in many labor market models.

公司收入 -
唯一的生产要素是劳动力，就像许多劳动力市场模型一样。

There is one non-storable good, and each firm produces a certain amount of its own variety of this good. Each firm responds to a quantity demanded of this good Dj,t, defined as its share of the total quantity of the good demanded, share that fluctuates randomly according to a random walk. Total quantity demanded Dtot is held constant because we aim to study our labor market in a steady state. Exogenous shocks on this total demand will be introduced in a sensitivity analysis to study the response of the main variables. In order to illustrate the coherence of a constant total demand with stochastic shocks on firms own demand, we can for instance look at a goods market with horizontal differentiation, where firms undergo stochastic variations of consumers' preferences for their own variety. Price adjustments have a cost, and then firms dare not modify the price. Since the unit costs are not too dissimilar, we can then set a unique exogenous price
(Salop, 1979). Firms that make losses for some time fail. The firm production is linear additive in terms of the productions of the different workers, given that employees work either full time or part time.

存在一种不可储存的商品，每个公司生产其自身品种的一定数量。每个公司对该商品的需求量Dj,t做出响应，该需求量被定义为其所占总需求量的份额，并且会根据随机游走而随机波动。为了研究劳动力市场的稳态，我们将保持总需求量Dtot恒定。在敏感性分析中，我们将引入对总需求的外部冲击，以研究主要变量的响应。为了说明恒定总需求与公司自身需求上的随机冲击之间的一致性，我们可以考虑一个具有水平差异化的商品市场，在这个市场中，公司会面临消费者对其自身品种偏好的随机变化。由于价格调整是有成本的，因此公司不敢轻易修改价格。鉴于单位成本相差不大，我们可以设定一个唯一外生价格（Salop, 1979）。那些在某段时间内亏损的公司将会失败。公司生产是线性可加性质地由不同工人进行生产，而员工则要么全职工作要么兼职工作。

A firm is composed of a manager and employees of 3 different occupation levels (1 = blue collar or employee, 2 = middle level job, 3 = executive ).

一个公司由一个经理和三个不同职业级别的员工组成（1 = 蓝领或员工，2 = 中层职位，3 = 高管）。

Each firm has a specific organization and needs labor for each occupation level q :
Dj,q,t = Dj,t × ψj,q with ψj,q the share of demand of the firm j allocated to the occupation level q. At the creation of a firm, these shares are randomly drawn from a standard normal distribution with a mean µΨq, which depends on the occupation level of the job, and a standard deviation σψ.

每个公司都有其独特的组织结构，并且对于每个职业级别 q，都需要相应的劳动力：
Dj,q,t = Dj,t × ψj,q，其中 ψj,q 表示分配给公司 j 的职业级别 q 的需求份额。在公司成立时，这些份额是从具有均值 µΨq（取决于工作的职业级别）和标准差 σψ 的标准正态分布中随机抽取的。

At each step of our simulation - one week in the reality6, we assume that each occupation q in the firm j cannot contribute more than its demand D*j,q,t* or its production capacity Qeff j,q,t
(computed as the sum of the production of all these nj,q employees). The income of the firm j at time t is given by:

在我们的模拟中的每一步，即现实中的一周时间，我们假设公司j中的每个职位q不能超过其需求D*j,q,t*或其生产能力Qeff j,q,t（计算为所有这些nj,q员工的生产总和）所能贡献的数量。公司j在时间t的收入由以下公式给出：

$$R^{eff}_{j,t}=P\times\sum_{q=1}^{3}min(Q^{eff}_{j,q,t},D_{j,q,t})\tag{1}$$
Firm costs -
The regular global cost of the firm is:

公司成本 -
公司的常规全球成本为：

$$C_{j,t}^{eff}=\sum_{i=1}^{n_{j}}C_{i,j,t}^{eff}\tag{2}$$
where Ceff i,j,t is the effective salary cost of the employee i in the firm j at time t and nj the total number of employees. There are additional costs Cadd j,t that include training costs, firing costs and vacancy costs.

公司成本 -
公司的有效薪资成本为：
$$C_{j,t}^{eff}=\sum_{i=1}^{n_{j}}C_{i,j,t}^{eff}\tag{2}$$
其中，Ceff i,j,t表示时间t时公司j中员工i的有效薪资成本，nj表示员工总数。此外还有其他费用Cadd j,t，包括培训费用、解雇费用和空缺费用。

Benefit -
The profit of the firm at time t is given by:

利润 -
公司在时间t的利润为：

$$\Phi^{eff}_{j,t}=R^{eff}_{j,t}-C^{eff}_{j,t}-C^{add}_{j,t}\tag{3}$$
This profit is stored in the history of the firm in order to perform a quarterly balance (cf. section 3.6.2).

为了进行季度平衡，公司将这笔利润记录在历史中。具体而言，在时间t，公司的利润可以表示为：
$$\Phi^{eff}_{j,t}=R^{eff}_{j,t}-C^{eff}_{j,t}-C^{add}_{j,t}\tag{3}$$

## 3.4.2 Determination Of Firm Production Qeff J,Q,T



There is a base production attached to each job, and the employee's characteristics will modulate its value to determine the effective production. Moreover, the employer has only an imperfect and evolving information on individual production 7.

每个工作岗位都有一个基本产量，员工的特征将调节其值以确定有效产量。此外，雇主对个人产量只有不完善且不断发展的信息。

Base production per occupation level -
In the firm an employee occupies an individualized job p, notably characterized by a occupation level q, but also by the nature of the job contract, the expected duration of this contract, the work time per period (full-time or part-time job). The weekly base production for a job p at occupation level q in firm j is randomly drawn within bounds from a normal distribution with a mean µq, which depends on the occupation level of the job, and a standard deviation σq. The base production of a worker (for full time) reflects the technology embodied in the equipment used by the workers in the occupation q. The technology is not explicitly modeled and it is assumed to be different between firms but identical for all jobs in the same occupation in a given firm. Moreover there is presently no technical progress in the model so that the base technologies are fixed variables for a firm, and the base production is drawn from a distribution when the firm is created :

在公司中，员工担任个性化的职位p，其特征包括职业水平q、工作合同的性质、预期合同期限以及每个周期的工作时间（全职或兼职）。公司j中岗位p在职业水平q上的每周基本产量是从一个正态分布中随机抽取的，该分布的均值µq取决于岗位的职业水平，标准差σq。员工（全职）的基本产量反映了岗位q所使用设备中蕴含的技术。尽管技术并未被明确建模，但假设不同公司之间存在差异，而对于同一公司内相同职业的所有岗位来说是相同的。此外，在模型中目前没有技术进步，因此对于一家公司而言，基础技术是固定变量，并且在创建公司时从分布中抽取基本产量值。

$$Q_{jq}^{base}=Max(0,\,(\mu_{q}\times\mathcal{N}\left(1,\sigma_{q}\right)))\times NbHoursPerWeekRatio(contract_{p})\tag{4}$$
where NbHoursPerWeekRatio(*contract*p) is a coefficient equals to 1 if the contract of the job is a full-time job (35 hours per week) and equals to 1
2 if the contract is a part-time job.

$$Q_{jq}^{base}=Max(0,\,(\mu_{q}\times\mathcal{N}\left(1,\sigma_{q}\right)))\times NbHoursPerWeekRatio(contract_{p})\tag{4}$$
其中，NbHoursPerWeekRatio(*contract*p)是一个系数。如果工作合同为全职（每周35小时），该系数为1；如果工作合同为兼职，则该系数为1/2。

Effective production -
The effective production of an individual i at job p in firm j is given by :

有效生产力 -
个体i在公司j的工作p中的有效生产力由以下公式给出：

$$Q_{i,j,\alpha t}^{eff}=Q_{j,\alpha}^{base}\times Corroid_{i}\times F_{\beta_{i}}(CH_{i,t}^{general}+CH_{i,\alpha t}^{soc})\times F_{\lambda}(CH_{i,j,t}^{spe})\tag{5}$$

有效生产力 -
个体i在公司j的工作p中的有效生产力可以通过以下公式计算：

$$Q_{i,j,\alpha t}^{eff}=Q_{j,\alpha}^{base}\times Corroid_{i}\times F_{\beta_{i}}(CH_{i,t}^{general}+CH_{i,\alpha t}^{soc})\times F_{\lambda}(CH_{i,j,t}^{spe})\tag{5}$$

请注意，上述公式描述了个体在特定工作环境下的有效生产力，并考虑了不同因素的影响。

The $F_{y}$ functions are given by: $F_{y}(x)=1+y\times x$, and $\beta_{i}$ a positive exogenous parameter.

$F_{y}$函数的定义如下：$F_{y}(x)=1+y\times x$，其中$\beta_{i}$是一个正的外生参数。

The effective production is based on four complementary factors : (1) the base production in the job, (2) the core productivity of the employee, (3) the general human capital of the employee, and (4) the specific human capital in the job she holds's.

有效生产力基于四个互补因素：(1) 工作中的基础生产力，(2) 员工的核心生产力，(3) 员工的一般人力资本，以及 (4) 她所担任职位的特定人力资本。

1. The base production Qbase
j,q,t for the job p in occupation q is given above by equation 4
2. *CProd*i is the core productivity of the individual i. CProdi ∼ Max(0, N (1, σ*Prod*)) with
standard deviation σ*Prod*. It encodes the initial skills and motivations of the individual.
3. CHgeneral
i,t
is the general human capital production factor,
CHgeneral
i,t
is the stock of general human capital detained by individual i at time t, and equals
the general work experience Experiencei,t .
4. CHocc
i,q,t is the occupational human capital production factor, with βq a positive exogenous
parameter.
CHocc
i,q,t is the stock of human capital related to occupation level q and detained by individual
i at time t. It equals the work experience obtained in the occupational level Experience*i,q,t* .
5. $F_{\lambda}(CH^{\rm spec}_{i,q,t})$ is the job-specific production factor. $\lambda$ an exogenous parameter. $CH^{\rm spec}_{i,p,t}$ is the specific human capital of an individual i in the occupation q at the job p in the firm j and is given by: $$CH^{\rm spec}_{i,p,t}=Senior^{\rm spec}_{i,p,t}$$ (6)
where Seniorspec i,p,t is the seniority in number of periods of individual i at job p in firm j. Notice that if the individual receives a promotion and changes her occupation level in the company, the seniority will be reset to 0. The specific human capital in the original definition of Becker (1975) represents the skills acquired by an individual in a firm and only useful in this firm. However, the seniority factor in a firm appears to have little impact (at least on wages) in France since the 90s (Beffy et al., 2006). In our model, we distinguish jobs by occupation and each occupation allows to acquire skills (technological and social)
specific to this occupation but transferable between firms9
Each period spent in employment, Experiencei,t and Experience*i,q,t* increase 10 by 1 but are reduced by a percentage - respectively *PrLossXP* and *PrLossXP*q - in each period spent out of employment 11. This decrease will start only after 6 months after leaving employment.

1. 方程4给出了职业q中岗位p的基础生产力Qbasej,q,t。
2. *CProdi*表示个体i的核心生产力。CProdi ∼ Max(0, N (1, σProd*))，其中σProd*为标准差。它反映了个体的初始技能和动机。
3. CHgenerali,t是一般人力资本生产因子，表示个体i在时间t所持有的一般人力资本存量，等于一般工作经验Experiencei,t。
4. CHocci,q,t是职业人力资本生产因子，βq为正的外生参数。CHocci,q,t表示个体i在时间t所持有的与职业水平q相关的人力资本存量，等于在该职业水平上获得的工作经验Experience*i,q,t*。
5. $F_{\lambda}(CH^{\rm spec}_{i,q,t})$ 是岗位特定生产因子，其中$\lambda$为外生参数。$CH^{\rm spec}_{i,p,t}$表示个体i在公司j中职业q、岗位p上所具备的特定人力资本，并由以下公式给出：$$CH^{\rm spec}_{i,p,t}=Senior^{\rm spec}_{i,p,t}$$ (6)
其中Seniorspec i,p,t表示个体i在公司j中岗位p上任期数。需要注意的是，如果个体晋升并更换公司内部的职业水平，资历将被重置为0。贝克尔（1975）的原始定义中，特定人力资本代表个体在一家公司中获得的技能，仅在该公司中有用。然而，自90年代以来，在法国，公司内部的资历因素似乎对工资影响不大（Beffy等，2006）。在我们的模型中，我们通过职业来区分工作，并且每个职业都可以获得与该职业相关的技能（技术和社交），但这些技能可以在不同公司之间转移9。
就业期间，Experiencei,t和Experience*i,q,t*每经过一个周期增加1，但在失业期间每个周期分别减少一定比例-*PrLossXP*和-*PrLossXP*q-。这种减少只会在离开就业后6个月后开始生效。

Employee production estimation -One key theoretical options of WorkSim model is that an employee never knows perfectly the production of an employee. This hypothesis is in the line of loanovic (Iovanovic, October 1979), and was the basis of important developments in labor economics. This hypothesis has multiple potential effects on the functioning of the labor market. We assume that the company does not have any _a priori_ knowledge about the precise levels of real productivity for each of its employees. Therefore, it is only able to assess a level of _estimated productivity_:

员工产量估计- WorkSim模型的一个关键理论选项是员工无法完全了解其他员工的产量。这一假设与Iovanovic（1979年10月）的观点一致，并为劳动经济学领域的重要发展奠定了基础。该假设对劳动市场的运作产生了多种潜在影响。我们假设公司对于每位员工的实际生产力水平没有任何先验知识。因此，公司只能评估出一个“预估生产力”的水平。

$$Q_{i,j,d}^{estimated}\sim Max(0,\,\mathcal{N}(Q_{i,j,d+1}^{eff},\sigma_{i,j,d+1}))\tag{7}$$
This amount Qestimated i,j,q,t is drawn from this distribution when the employee is hired, and also at each employee evaluation. σ*i,j,q,t* represents the degree of uncertainty of the company in the evaluation of its employees. It decreases in the seniority of the employee in the firm at her level of occupation (informal learning by the employer) and in the number of times she has been evaluated by the firm (formal learning that takes place on specific occasion such as the end of probationary period, or the end of a FDC if a transformation into an OEC is considered):

在员工入职时以及每次员工评估时，我们从该分布中抽取出Qestimated i,j,q,t这个数值。σ*i,j,q,t*代表公司对于评估员工的不确定程度。这个不确定程度会随着员工在公司的资历（雇主的非正式学习）以及公司对其进行评估的次数（特定场合如试用期结束或FDC结束时进行的正式学习）而减少。

$$\sigma_{i,j,q,t}=Max(0,\;\sigma_{0}\times(1-\delta_{\sigma}\times\mbox{\it Seni}or_{i,j,q,t}^{spec}-\eta_{\sigma}\times\#Eval_{i,j,q,t}))\tag{8}$$
with σ0, δσ and ησ, three exogenous parameters12.

$$\sigma_{i,j,q,t}=Max(0,\;\sigma_{0}\times(1-\delta_{\sigma}\times\mbox{\it Seni}or_{i,j,q,t}^{spec}-\eta_{\sigma}\times\#Eval_{i,j,q,t}))\tag{8}$$
其中，σ0、δσ和ησ是三个外生参数12。

## 3.4.3 Determination Of Firm Costs Ceff I,J,T



Base salary The weekly base salary for a job p at occupation level q in firm j is written Sbase j,q . It is determined from the base production in the job:

基本工资：在公司j中，职位级别为q的职位p的每周基本工资记作Sbase j,q。它是根据该职位的基本生产力确定的。

$$S^{base}_{j,q}=Q^{base}_{j,q}\times P\times(1-\zeta_{j})\tag{9}$$
9We have made the choice to discard the notion of firm human specific capital by creating instead two new types of human capitals. The first is the occupation human capital, which corresponds to the professional skills acquired in the educational system and subsequent experience acquired in a given occupation level. This type of human capital is obviously important and distinct from work experience since entering the labor market in the model (see Gibbons et al. (Gibbons et al., 2005), Kambourov & Manovskii (Kambourov & Manovskii, 2009) for evidence). In the model it is specific to a broad aggregate of occupations q, but it could be extended to more finely defined professions or crafts.

我们选择放弃公司特定人力资本的概念，而是引入了两种新的人力资本类型。第一种是职业人力资本，它代表了在教育系统中获得的专业技能以及在特定职位级别上积累的经验。这种人力资本类型在模型中具有重要意义，并且与工作经验有所区别（参见Gibbons等人，2005年；Kambourov和Manovskii，2009年的研究结果）。在模型中，职业人力资本是针对广泛的职业群体q进行定义的，但也可以进一步细分为更具体的专业或手艺。

The second is the job specific human capital. It covers possibly some required training given when entering the job but in any case the experience by learning on the job. It is assumed to be so specific that it will not have any use in other jobs. It notably contains some social skills specific to the job.

第二种是工作特定的人力资本。它可能涵盖了进入工作时所需的一些培训，但无论如何都包括在工作中学习的经验。它被认为是如此特定，以至于在其他工作中没有任何用途。特别是它包含了与该工作相关的一些社交技能。

with P the exogenous price of the (unique) good and ∀*j, ζ* = ζ, an exogenous parameter that represents the share of the sales revenue (of base production here but also of the sales of effective production below) kept by the firm in order to pay intermediate consumptions, payroll charges, taxes, interests, investments, dividends, etc.. It reflects the balance of power between workers and employers, the size of public services in the society and the technology among the principal determinants. Although it differs in the real world between firms because the expenditures differ between firms, we will assume it is uniform since the model does not focus on the determinants not related to the human resources management.

假设P为外生价格（唯一商品），对于所有j，ζ* = ζ是一个外生参数，代表公司保留的销售收入份额（包括基础生产和实际生产的销售收入），用于支付中间消费、工资税、税收、利息、投资、股息等。这一参数反映了劳动者和雇主之间的力量平衡、社会中公共服务的规模以及技术等主要决定因素。尽管在现实世界中，不同公司之间的支出存在差异，但由于该模型不关注与人力资源管理无关的决定因素，我们将假设其是均匀的。

Weekly starting salary The starting net salary Seff i,j,q,t=*hiring* of an employee i in firm j at level of occupation q at time t = *hiring* is given by:

每周起始工资，即员工i在公司j的职位q上的净起始工资Seff i,j,q,t=*hiring*，由以下公式给出：

$$S^{eff}_{i,j,q,t=hiring}=Max(SMIC,\,S^{base}_{j,q}\times F_{\beta_{q}}(CH^{general}_{i,t=hiring}+CH^{occ}_{i,qt-hiring})\times G(U_{t=publish}))\tag{10}$$
SMIC 13 is the minimum hourly wage in France, net of the employee's contribution to social security, multiplied by the number of hours worked on the job. The starting salary is the base salary of the job modulated by the general and occupational human capitals of the employee. Due to important considerations of equity in terms of human resource management (e.g. (Adams, 1963)), the employer cannot discriminate between employees who have the same experience. A feeling of unfairness could generate decreases in effort and productivity for the employees who feel unequally treated (efficiency wage concept)14.

根据公式（10），在招聘时刻（$t=hiring$），有效薪资$S^{eff}_{i,j,q}$取最大值，即与法定最低工资（SMIC）相比较。SMIC 13是法国的最低小时工资，扣除员工对社会保障的贡献后，乘以在职工作的小时数。起始工资$S^{base}_{j,q}$是基于员工的一般人力资本（$CH^{general}_{i,t=hiring}$）和职业人力资本（$CH^{occ}_{i,qt-hiring}$）进行调整的。由于在人力资源管理方面存在重要的公平考虑（例如(Adams, 1963)），雇主不能歧视具有相同经验的员工。不公平感可能会导致感到不公平对待的员工努力和生产力下降（效率工资概念）14。同时，薪资还受到发布时刻($t=publish$)的失业率($U_{t=publish}$)影响，通过函数$G(U_{t=publish})$进行调节。

A final factor affecting wages is the global unemployment rate U t=*publish* at the time of publication of the job offer by the firm. We consider that the relation G is isoelastic, according to the literature on the wage curve (Blanchflower & Oswald, 1994), and take G(x) = k × xω, where ω is an exogenous parameter, set at its standard value of -0.1, and k = (
1
Uref )ω. Uref is set as the global unemployment rate for the reference year we study (Uref = 0.092 in 2011).

工资的最后一个影响因素是公司发布职位时的全球失业率$U_{t=publish}$。根据有关工资曲线的文献（Blanchflower＆Oswald，1994），我们假设关系函数$G$是等弹性的，并采用形式为$G(x) = k × x^ω$的函数，其中$ω$是外生参数，被设定为标准值-0.1，而$k = (1/U_{ref})^ω$。我们将全球失业率设定为我们研究的参考年份（2011年）的参考失业率($U_{ref} = 0.092$)。

Annual increase of the weekly wage The weekly salary of employee i in firm j is reviewed annually at her birthday date of her arrival in the company according to the equation:

每年的周薪增长 员工i在公司j的周薪根据以下方程式在她入职公司的生日日期进行年度审查：

$$S^{eff}_{i,j,q,t}=Max(SMIC,\,S^{base}_{j,q}\times F_{\beta_{q}}(CH^{general}_{i,t}+CH^{occ}_{i,q,t})\times F_{\lambda_{q}^{*}}(CH^{spec}_{i,j,q,t})\times G(U_{t=publish}))\tag{11}$$
with Fλ∗q(CHspec i,j,q,t), the productivity gains factor related to her experience in the job that affects her salary. It is assumed here that, following the consensual principals of specific human capital theory, the company gives to the worker only a part of the productivity gains related to specific human capital , hence λ∗
q < λq. However, according to the insiders-outsiders theory, the employee's salary is not affected by changes in the state of the labor market after hiring (the factor G(U) remains the same as it was at the time of publishing the vacancy). Some rigidity in search models is necessary to obtain variations in unemployment during the cycle and Pissarides (Pissarides, 2009) has argued that hiring wages are flexible and current contracts rigid, a double hypothesis which fits the wage curve and the insiders-outsiders theory, and that we can implement easily since the wages are individualized 15.

$$S^{eff}_{i,j,q,t}=Max(SMIC,\,S^{base}_{j,q}\times F_{\beta_{q}}(CH^{general}_{i,t}+CH^{occ}_{i,q,t})\times F_{\lambda_{q}^{*}}(CH^{spec}_{i,j,q,t})\times G(U_{t=publish}))\tag{11}$$

其中，Fλ∗q(CHspec i,j,q,t)是与员工在工作中的经验相关的生产力增益因子，影响其薪资。根据特定人力资本理论的共识原则，公司仅向员工提供与特定人力资本相关的生产力增益的一部分，因此λ∗q < λq。然而，根据内外部理论，在雇佣后劳动市场状况的变化不会影响员工的薪资（因素G(U)保持与发布职位时相同）。为了在周期中获得失业率变化，搜索模型中需要一定程度的刚性。Pissarides（2009）认为招聘工资是灵活的、当前合同是刚性的，并提出了这个双重假设既符合薪酬曲线又符合内外部理论，并且我们可以很容易地实施它，因为薪酬是个体化的15。

Effective cost of an employee Ceff i,j,q,t The effective cost of an employee Ceff i,j,q,t include her salary Seff i,j,q,t and payroll charges .

员工的有效成本Ceff i,j,q,t包括她的薪资Seff i,j,q,t和社会保险费用。

$$C^{eff}_{i,j,\mu t}=S^{eff}_{i,j,\mu t}\times(1+PrCharge)\tag{12}$$

员工的有效成本Ceff i,j,q,t等于她的薪资Seff i,j,q,t乘以（1+PrCharge）。

_PrCharge_ is the ratio of payroll charges to net salary. It includes both the employee's and the employee's charges.

_PrCharge_是社会保险费用与净薪资的比率。它包括员工和雇主的费用。

## 3.5 Simulation Cycle In The Worsim Model



The **simulation cycle** includes four main steps, as shown in Figure 1 below:

**模拟周期**包括以下四个主要步骤，如下图1所示：

1. Firm decisions: contracts and vacancies management, evaluations, job creation / destruction
2. Individual decisions: labor market entrances and exits, job search 3. Firm decisions: applications and promotions management 4. Demography: household dynamics, retirements, aging
The length of one period in the simulation cycle corresponds to *one week* in the real world, in order to take into account the many very short term contracts that are found in the French labor market, 46% of all hires are on FDC that last one week or less in 2010 (Berche et al., 2011). Moreover, when statistics are needed, we took as a reference year 2011, the most recent year for which we could find the complete statistical data and sources.

3.5 Worsim模型中的模拟周期

**模拟周期**包括以下四个主要步骤，如图1所示：

1. 公司决策：合同和职位管理、评估、岗位创设/销毁
2. 个人决策：劳动力市场进入和退出、求职
3. 公司决策：申请和晋升管理
4. 人口统计学：家庭动态、退休、老龄化

为了考虑法国劳动市场上存在的许多非常短期的合同，模拟周期的长度与现实世界中的一周相对应。根据2010年的数据（Berche等，2011），46%的新雇佣是持续一周或更短时间的固定期限合同。此外，在需要统计数据时，我们选择了参考年份2011年，这是我们能够找到完整统计数据和来源的最近一年。

## 3.6 Firm Decisions



In each period and for each occupation level, each firm has to create new jobs or destroy existing
ones, depending on an exogenous demand. Then, it manages its employees through evaluation,
possibly dismissals, and manages the fixed duration contracts. For each occupation level q, we
define the demand margin Gj,q,t = Dj,q,t − (Qeff
                                              j,q,t + Q∗
                                                      j,q,t), as the difference between:

在每个时期和每个职位级别下，每家公司都必须根据外部需求情况创造新的工作岗位或销毁现有岗位。随后，通过评估、可能的解雇以及管理固定期限合同来管理其员工。对于每个职位级别q，我们定义需求边际Gj,q,t为Dj,q,t与(Qeff j,q,t + Q∗ j,q,t)之间的差异。

- the amount of good demanded to the firm D*j,q,t*, which varies stochastically among firms,
and
- the sum of the current total effective production of the firm Q*j,q,t* and the current expected
production of vacant jobs (to be filled) of the firm Q∗
j,q,t

- 公司所需的商品数量D*j,q,t*，在公司之间随机变化，
和
- 公司当前总有效生产量Q*j,q,t*与公司当前预期的空缺职位生产量（待填补）Q∗j,q,t的总和。

## 3.6.1 Job Creations (Step 1 In Figure 1)



When Gj,q,t *> DTh*, where *DTh* ≥ 0 is a fixed parameter, the firm considers whether to create a new job to be filled. The characteristics of the job to be created are based on two exogenous probabilities (calibrated, see values in Appendix C) :

当Gj,q,t*>DTh*时，其中*DTh*≥0是一个固定参数，公司会考虑是否创建一个待填补的新职位。待创建的职位的特征基于两个外生概率（校准后，请参见附录C中的数值）:

1. The first sets the choice between creating a FDC and an OEC. This decision is based on
exogenous probabilities identical for all firms. If a FDC is drawn, its duration will be set by another drawing. The durations considered for the FDC are: 1 week, 1, 2, 6, 12 or 24 months.
2. The second one decidess whether the job should be full-time or part time.
Before definitely creating job p of occupation q, the company estimates its expected profit per period from the expected revenue Rexpected q,j,t and costs Cexpected q,j,t
: Φexpected q,j,t
= Rexpected q,j,t
− Cexpected q,j,t
.

1. 第一个决策涉及选择创建FDC（全日制职位）还是OEC（兼职职位）。这个选择是基于对所有公司相同的外生概率的考虑。如果选择了FDC，其持续时间将通过另一次抽取来确定。可供选择的FDC持续时间为：1周、1个月、2个月、6个月、12个月或24个月。
2. 第二个决策确定该职位应该是全职还是兼职。
在最终创建占据q的p号工作之前，公司会估计从预期收入Rexpected q,j,t和成本Cexpected q,j,t中每期预期利润Φexpected q,j,t。

The expected revenue from this productivity is given by :

这种生产力的预期收入由以下方式给出：

$$R_{q,j,t}^{expected}=P\times min\;(G_{j,q,t},Q_{d,j,q,t}^{dist(m)})\tag{13}$$

1. 第一个决策涉及选择创建全日制职位（FDC）还是兼职职位（OEC）。这个选择是基于对所有公司相同的外生概率的考虑。如果选择了FDC，其持续时间将通过另一次抽取来确定。可供选择的FDC持续时间为：1周、1个月、2个月、6个月、12个月或24个月。

2. 第二个决策确定该职位应该是全职还是兼职。在最终创建占据q的p号工作之前，公司会估计每期预期利润Φexpected q,j,t，该利润由预期收入Rexpected q,j,t和成本Cexpected q,j,t计算而得。

预期收入Rexpected q,j,t的计算方式如下：
$$R_{q,j,t}^{expected}=P\times min\;(G_{j,q,t},Q_{d,j,q,t}^{dist(m)})\tag{13}$$

with $G_{j,q,t}$ the demand margin and $Q_{d,j,t}^{est(m)}$ is the average of all the productivity estimates for the individuals that will be evaluated during the prospective phase.

其中，$G_{j,q,t}$代表需求边际，$Q_{d,j,t}^{est(m)}$是在前瞻阶段评估的所有个体的生产力估计的平均值。

The cost per period is a function of the wage but also includes a potential cost of a contract breach. This cost will differ with the nature of the contract (FDC or OFC) :

每个时期的成本是工资的函数，但也包括合同违约的潜在成本。这个成本将根据合同的性质（FDC或OFC）而有所不同：

$$C_{q,j,t}^{expected}=S_{d,j}^{estim}\times(1+PrCharge)+C\,PoS\,Va_{q,t}^{expected}+CE\,End_{q,t}^{expected}\tag{14}$$
where Sestim Avg is the average of all the net wage estimates for the individuals that will be evaluated during the prospecting phase. CPosV acexpected q and CEndexpected q,t are respectively the expected total cost of a vacancy and the expected total end cost of the contract (short-term contract bonus, firing cost,...) amortized over the expected duration of the contract. These costs are estimated by learning. As generally found in search theory, the vacancy cost will impact the hiring norm (though the expected profit, see section 3.6.4 below).

式（14）中，$C_{q,j,t}^{expected}$表示预期的成本，$S_{d,j}^{estim}$表示前瞻阶段评估的所有个体净工资估计的平均值。$C\,PoS\,Va_{q,t}^{expected}$和$CE\,End_{q,t}^{expected}$分别表示空缺的预期总成本和合同的预期总终止成本（包括短期合同奖金、解雇成本等），并按合同预期持续时间进行摊销。这些成本通过学习进行估计。根据搜索理论的一般发现，空缺成本将影响招聘规范（尽管通过预期利润，见第3.6.4节）。

Thus, if its current expected profit Φexpected q,j,t
> 0, the company publishes a job offer at the wage Sbase j,q,t .

因此，如果当前预期利润Φexpected q,j,t大于0，公司将以基本工资Sbase j,q,t发布招聘信息。

## 3.6.2 Job Destruction (Step 2 In Figure 1)



By contrast, when there is a significant reduction in its demand in one occupation level (in our model, this is when Gj,q,t < −DTh), the firm reacts in the short term by removing its vacancies.

相比之下，当某个职业层次的需求显著减少时（在我们的模型中，当Gj,q,t < -DTh时），公司会短期内通过取消空缺来做出反应。

In the medium run (on a quarterly basis), if this low cost adjustment is not sufficient, the firm considers the possibility to dismiss workers (see 3.6.3 below).

在中期（按季度计算），如果这种低成本调整不足够，公司会考虑解雇员工的可能性（见下文3.6.3）。

Moreover, independently of the demand level, the vacancies that remain unfilled and have a vacancy duration greater than a fixed threshold - a parameter that will differ for FDC and OEC - are destroyed.

此外，无论需求水平如何，那些仍未填补且空缺持续时间超过固定阈值的职位将被取消。这个阈值参数在FDC和OEC之间会有所不同。

Short-term adjustment: vacancy removals In each period, when Gj,q,t < −DTh. the company randomly draws one of its vacancies and evaluates the interest to keep it or not. To do this, the company recalculates the demand margin G
′
j,q,t it would have without this vacancy, and reassesses its interest it would have to create the job now. If this time Φexpected q,j,t
< 0, the company removes the vacancy and G*j,q,t* is increased by Qexpected j,q,t
. This process is repeated for all the remaining vacancies as long as overproduction remains (i.e. as long as Gj,q,t < −DTh and there are still vacancies to be removed).

短期调整：职位取消。在每个时期，当Gj,q,t < −DTh时，公司会随机选择一个职位，并对其进行评估以确定是否保留。为了做出决策，公司会重新计算没有该职位的需求边际G'j,q,t，并重新评估现在创建该工作的兴趣。如果此时Φexpected q,j,t < 0，则公司会取消该职位，并将G*j,q,t*增加Qexpected j,q,t。只要存在过剩（即Gj,q,t < −DTh且仍有待取消的职位），则会对所有剩余的职位重复此过程。

Medium-term adjustments: economic dismissals An evaluation of the financial viability of the company is performed on a quarterly basis (12 periods in the simulation). The first date of the balance sheet is drawn randomly, then this financial reporting occurs every three months from this date. The company calculates its quarterly return that is computed as the ratio of the quarterly profit over the total labor cost16. If this return falls below a certain profitability threshold
(a fixed parameter PT, that will be calibrated and can be negative), the firm engages an economic dismissal procedure:

中期调整：经济解雇。公司每季度（模拟中的12个时期）对其财务可行性进行评估。资产负债表的首个日期是随机选择的，随后每三个月进行一次财务报告。公司计算季度回报率，即季度利润与总劳动成本之比16。如果该回报率低于一定的盈利能力阈值（一个固定参数PT，将进行校准且可以为负），公司将启动经济解雇程序。

- All remaining vacancies are removed. - The company dismisses a number of employees, drawn randomly. The company cannot
set the ranking according to the estimation of the profit of the individual employees, even though it has some estimate, since the French labor law and collective agreements set several criteria of ranking that must be respected first. Moreover, the criteria differ between collective agreements, and we considered this ranking process to be too complex to be modeled. The number of employees dismissed is chosen as the minimum number of persons to fire in order to get a return above the profitability threshold.
If a company has no employee anymore, and if the managing director left alone does not make a sufficient return, the firm is considered to be bankrupt and is removed from the simulation. The managing director becomes unemployed. However, we want to keep the number of firms constant since we aim for a steady state. Hence, when a bankruptcy has occurred, we randomly select an active agent in the simulation to create a new firm and manage it. To keep the number of contracts types low, we assume that she will work under an OEC contract and be the only producer in the firm (until she starts to recruit).

- 所有剩余职位已被取消。公司随机解雇了一部分员工。尽管公司对个体员工的利润估计有一些参考，但根据法国劳动法和集体协议的规定，排名必须遵守多个标准。此外，不同的集体协议之间的标准也存在差异，我们认为这个排名过程过于复杂而无法建模。解雇的员工人数被选择为使回报率超过盈利能力阈值所需解雇的最少人数。

如果一家公司没有员工，并且独自留下的总经理无法获得足够的回报，则该公司被视为破产并从模拟中移除。总经理将失业。然而，为了保持公司数量恒定，因为我们追求稳态，当发生破产时，我们会随机选择一个活跃主体来创建并管理一个新公司。为了减少合同类型数量，我们假设该主体将在OEC合同下工作，并且成为该公司唯一的生产者（直到开始招聘）。

## 3.6.3 Employee Evaluations (Step 3 In Figure 1)



In each period, the firm examines if some employees have to be evaluated. This individual evaluation may occur:

在每个时期，公司会检查是否需要对一些员工进行评估。这种个体评估可能发生：

- At the end of the probationary period for FDC and OEC ; - At the end of FDC contract to decide if it should be renewed ; - At the end of FDC contract, if the transformation of FDC to OEC is to be considered ;
- Every year, at the anniversary date of the contract, for each FDC or OEC employee.
In order to decide whether the employee should be kept, the firm calculates a profit for each scenario:

- 在FDC和OEC试用期结束时；
- 在FDC合同到期时决定是否续约；
- 在FDC合同到期时，考虑将其转换为OEC；
- 每年，在合同的周年纪念日，对每位FDC或OEC员工进行评估。

为了确定是否保留员工，公司会针对每种情况计算利润。

- First scenario: the firm keeps the employee. The company computes the demand margin it
gets without this employee, and evaluates as in section 3.6.1 the interest it would now have to create this job. Thanks to learning, the firm knows better this time the employee's actual productivity.
- Second scenario: the firm does not keep the employee (dismissal on personal ground):
1. If the employee is under OEC, the firm evaluates the dismissal costs (specific to a dismissal on personal ground) ;
2. The company computes the potential profit given by a new employee, who would be
recruited to replace the fired employee (with the same contract and the same level of occupation).
The firm compares the total profits associated with each scenario. If the firm chooses to dismiss the employee (end of probationary period, end of FDC contract, OEC firing on personal ground), it publishes a new job add to recruit a new employee at the same level of occupation.

- 第一种情况：公司选择保留该员工。公司计算了在没有该员工的情况下所获得的需求边际，并按照3.6.1节的方法评估了现在需要创建这个职位所带来的利益。通过学习，公司这次更加准确地了解到了员工的实际生产力。
- 第二种情况：公司选择不保留该员工（因个人原因解雇）：
1. 如果员工处于OEC合同下，公司会评估解雇成本（特定于因个人原因解雇的成本）；
2. 公司计算了由一名新员工带来的潜在利润，该新员工将被招募来替代被解雇的员工（具有相同合同和相同职位水平）。
公司比较了与每种情景相关联的总利润。如果公司选择解雇该员工（试用期结束、FDC合同到期、OEC因个人原因解雇），则会发布一份新的招聘广告，以招募一个具有相同职位水平的新员工。

[重写后的中文内容]

## 3.6.4 Hiring Phase And Promotions (Step 7-8 In Figure 1)



If workers are distributed according to productivity, search theory shows that the firm should set an optimal reservation productivity or profit, under which it rejects the candidates. This reservation profit is based on the probability to attract candidates, the distribution of the discounted values of the productivities of these candidates over the expected duration of the job, and the cost of the vacancy per period, but this list is not exhaustive. A firm will prefer to wait one more period than recruiting if all current candidates are below this reservation productivity. The determination of the optimal reservation profit is symmetric to the worker's search recursive model under fixed wages. 17 Since rationality is bounded, and the productivity distribution unknown, we define a hiring norm that replicates the main results from search theory. The hiring norm of the firm is given by:

如果员工的分布符合生产力，搜索理论表明公司应该设定一个最优的保留生产力或利润水平，在此水平下拒绝候选人。这个保留利润是基于吸引候选人的概率、这些候选人生产力的贴现价值分布以及每个期间的空缺成本等因素进行计算的，但这个列表并不详尽。如果所有当前候选人都低于这个保留生产力水平，公司会更愿意等待一个周期而不是招聘。确定最优保留利润与固定工资下员工搜索递归模型对称。鉴于有限理性和未知的生产力分布，我们定义了一个招聘规范来复制搜索理论的主要结果。公司的招聘规范如下所示：

$$\text{HirringNorm}_{j,q,p,t}=\text{N}_{1}\Phi_{j,q,t}^{Avg}(1+\text{N}_{2}\frac{\Phi_{j,q,t}^{Max}}{\Phi_{j,q,t}^{Min}})\frac{N(d_{p})}{H(ITENS_{t})}\tag{15}$$
with N1, N2 two exogenous parameters. The firm is assumed to know a small sample of candidates without cost (by its former presence on the labor market), but not large enough to estimate the parameters of the productivity distribution, a demanding and complex process. It calculates the expected profits, and for the positive ones, the company stores the average ΦAvg j,q,t , the maximum of these profits, ΦMax j,q,t and the minimum ΦMin j,q,t . A first result of search theory is that firms prefer distributions with a higher profit mean and ΦAvg j,q,t raises their hiring norm. A second result of search theory is that firms prefer more variance in the distribution since there are more high productivity workers. An increase in the mean preserving variance raises the hiring norm (Pissarides, 1990, p.97). We formalize this result by a bounded rationality rule in which the relative range of the productivities N2 ΦMax
ΦMin raises the hiring norm. A third result is that the norm is an increasing function of the duration of the contract dp proposed for the job through the factor N(dp):
it has a minimum of N3 for a very short FDC (duration of one week) and a maximum at 100% for an OEC contract. A fourth result is that firms lower their norm when there are few unemployed and many vacancies. *ITENS*t is the tension on the labor market and is given by ITENSt = Vt Ut with Vt the vacancy rate and Ut the unemployment rate at time t. The higher this tension, the more the firms have to lower their requirements if they want to find a candidate. H is a logistic function with values between 0.8 and 1.2 and given by H(x) = 0.8 +
0.4
1+20×e−3x .

$$\text{招聘规范}_{j,q,p,t}=\text{N}_{1}\Phi_{j,q,t}^{Avg}(1+\text{N}_{2}\frac{\Phi_{j,q,t}^{Max}}{\Phi_{j,q,t}^{Min}})\frac{N(d_{p})}{H(ITENS_{t})}\tag{15}$$
其中，N1和N2是两个外生参数。假设公司了解一小部分候选人的信息（通过其在劳动力市场上的先前存在），但数量不足以估计生产力分布的参数，这是一个要求且复杂的过程。公司计算预期利润，并对正值利润进行存储，包括平均利润ΦAvg j,q,t、最大利润ΦMax j,q,t和最小利润ΦMin j,q,t。搜索理论的第一个结果表明，公司更倾向于选择具有更高平均利润的分布，而ΦAvg j,q,t则会提高其招聘规范。搜索理论的第二个结果表明，公司更倾向于选择具有更大差异性的分布，因为这样可以获得更多高生产力员工。保持均值不变而增加方差会提高招聘规范（Pissarides, 1990, p.97）。我们通过有界理性规则来形式化这个结果，在该规则中，生产力范围相对于ΦMax
ΦMin的比例N2会提高招聘规范。第三个结果表明，规范是合同持续时间dp的增函数，通过因子N(dp)来提出工作。当固定期限合同非常短（一周）时，规范达到最小值N3；而对于OEC合同，则达到100%的最大值。第四个结果表明，在失业人数较少且空缺职位较多时，公司会降低其规范。*ITENS*t表示劳动力市场上的紧张程度，由ITENSt = Vt Ut给出，其中Vt表示时间t时的空缺率，Ut表示失业率。紧张程度越高，如果公司想要找到候选人，则必须降低要求。H是一个逻辑函数，取值介于0.8和1.2之间，并由H(x) = 0.8 +
0.4
1+20×e−3x给出。

This hiring norm is then decreased by a percentage N4 in each period until the job is filled, but never drops below 0. This decrease is justified by the limited duration of a job that lowers the expected profit as time to fill this job increases (Pissarides, 1976, p.50). A rising cost from holding the job vacant would have the same effect.

然后，每个周期中的招聘标准会以N4的百分比递减，直到职位被填补，但永远不会降至0以下。这种减少是基于工作的有限期限，随着填补该工作所需时间的增加而降低了预期利润（Pissarides, 1976, p.50）。保持职位空缺所带来的成本上升将产生相同的效果。

Hiring takes place in three steps:

招聘分为三个步骤：

1. *Receiving applications* - Firstly the firm receives applications from external applicants. and
applications of internal candidates18.
2. *Selection and potential hiring* - A two-steps process takes place:
(a) First, the firm computes a score for each candidate (internal or external). The score for
each candidate i is computed as the expected profit Φestimated
i,j,q,t
if the candidate is hired
for the job. Then the best candidate (highest score) is selected.
(b) Thereafter, the firm checks if this candidate exceeds the hiring norm. If this is the case,
the candidate is hired, otherwise, the job remains vacant.
3. Internal promotion - If the best candidate hired is an internal candidate of the company, it
is a promotion. The employee acquires the occupation level of the job.

1. *申请接收* - 首先，公司接收来自外部申请者和内部候选人的申请18。
2. *筛选和潜在雇佣* - 这是一个两步骤的过程：
(a) 首先，公司为每个候选人（无论是内部还是外部）计算一个分数。候选人i的分数是根据预期利润Φestimated
i,j,q,t
计算得出的，即如果该候选人被聘用担任该工作的话。然后选择最佳候选人（即分数最高者）。
(b) 随后，公司检查该候选人是否超过了招聘标准。如果是这样，则雇佣该候选人；否则，职位将保持空缺。
3. 内部晋升 - 如果被雇佣的最佳候选人是公司内部员工，则属于晋升。员工获得该工作的职业水平。

## 3.7 Individual Decisions (Step 4-6 In Figure 1)



The individuals take decisions in each period of the simulation. This decision process is modelled with a *state machine*, where one individual will be in one particular state: inactive, unemployed, employed and not searching for another job (denoted *ENS*), employed and seeking a new job (denoted *OTJS*, for On-The-Job Searchers), student or retired. The transitions between these states can be caused by individual choices (for example: to start studying, to quit a job...), by external events (firing, death...), or by a sequence of two decisions (applying for a job, and the firm hires the candidate).

在模拟的每个时期，个体会做出决策。这个决策过程被建模为一个状态机，其中每个个体处于特定的状态之一：不活动、失业、就业但不寻找其他工作（简称为ENS）、就业并寻找新工作（简称为OTJS，即在职求职者）、学生或退休。这些状态之间的转换可以由个体的选择引起（例如：开始学习、辞职...），也可以由外部事件引发（如解雇、死亡...），或者是两次决策的序列导致（申请工作，公司雇佣候选人）。

## 3.7.1 Utility Functions



Each individual uses a utility function, to decide whether she should stay in her current state or move to another one. The utility function has the generic form of a Cobb-Douglas function:

每个个体都使用一个效用函数来决定是否应该保持当前状态还是转移到另一个状态。效用函数的一般形式为Cobb-Douglas函数：

$$U=(Income+Amentity+Stability)^{1-\alpha}(Free\,Time)^{\alpha}\tag{16}$$
It is a weighted aggregation of two groups of factor, the income including the value of the characteristics of the job, and free time. The detailed factors are:

3.7.1 效用函数

每个个体都使用一个效用函数来决定是保持当前状态还是转移到另一个状态。效用函数采用Cobb-Douglas函数的一般形式：

$$U=(收入+便利性+稳定性)^{1-\alpha}(空闲时间)^{\alpha}\tag{16}$$

该函数是对两组因素进行加权聚合，其中一组因素包括工作特征价值在内的收入，另一组因素是空闲时间。具体因素如下所示：

1. *Income*: weekly income of the household in euros, divided by the number of consumption
units (an adult counts for 1, a child 0.5)
2. *Amenity*: non-monetary features perceived by the individual (social recognition, working
environment, work hardness...)19. It is converted into a percentage of salary and is expressed in euros.
3. *Stability*: criteria reflecting the preference of the individual for stability, i.e. for a job with
the longest possible remaining contract duration. The maximum value is given for a permanent job (OEC). This stability is converted here into a percentage of salary and is expressed in euros;
4. *Free time*: free time per week available for the individual outside her working hours and
her search time. Our definition is a broad one since it includes time devoted for instance to sleep, eating, washing, domestic duties, and notably caring for the children.
The parameter α ∈ [0, 1] encodes the preference of the individual for free time or work. First, there is an effect of age, which increases the disutility of time spent at work. Hence α will evolve according to the following equation :

1. *收入*：家庭每周以欧元计算的收入，按消费单位数量进行平均（成年人计为1，儿童计为0.5）。
2. *便利性*：个体感知到的非货币特征（社会认可度、工作环境、工作强度等）。将其转化为薪水的百分比，并以欧元表示。
3. *稳定性*：反映个体对稳定性的偏好，即对剩余合同期限最长的工作的偏好。永久职位（OEC）给出最大值。这里将稳定性转化为薪水的百分比，并以欧元表示。
4. *空闲时间*：个体在工作时间和搜索时间之外每周可用于自由活动的时间。我们对空闲时间进行了广义定义，包括睡眠、进食、洗漱、家务事务，尤其是照顾孩子等方面所需的时间。

参数α ∈ [0, 1]编码了个体对空闲时间或工作的偏好。首先，年龄会产生影响，增加在工作中花费时间所带来的不便之处。因此，α将根据以下方程进行调整：

$$\alpha=\alpha_{base}*(1+\alpha_{old}*(age-15))\tag{17}$$

根据方程（17），参数α的值将根据年龄进行调整。其中，α_base是基础值，α_old是与年龄相关的调整系数，age表示个体的年龄。

With $\alpha_{base}$ drawn at the creation of the agent according to a normal distribution with mean $\alpha_{0}$ and standard deviation $\sigma_{all\alpha}$ (and with a minimum of zero).

根据正态分布，以均值为$\alpha_{0}$，标准差为$\sigma_{all\alpha}$（最小值为零），在创建主体时绘制$\alpha_{base}$。

Moreover. as in the ARTEMIS model (Ballot, 2002), α is different between men and women with children, because gender roles in the household has some impact20. We model this difference by multiplying the woman's alpha by a factor Fw depending on the number of children in
19The amenity is a proxy for all the factors that make the work pleasant or painful. We consider the work time per period when we calculate this amenity to avoid a bias, and above all, the amenity is fully revealed to the employee only after hiring. This amenity discovery could cause some early quitting, as it is happening in reality. Thus, in terms of imperfect information, there is a symmetric process between amenity discovery for the employee and employee's productivity discovery for the employer. The main difference is that we assume the employee to be promptly informed of the amenity, while the productivity is measured only very gradually (the probationary period is too short to reveal the real productivity).

此外，根据ARTEMIS模型（Ballot, 2002），α在有孩子的男性和女性之间存在差异，因为家庭中的性别角色对此有一定影响。我们通过将女性的α乘以一个与孩子数量相关的因子Fw来建模这种差异。

19福利是衡量工作愉快或痛苦等各种因素的主体变量。在计算这个福利时，我们考虑每个时期的工作时间，以避免偏差。尤其重要的是，员工只有在雇佣后才能完全了解到这个福利。这种福利发现可能导致一些早期辞职，就像现实中正在发生的那样。因此，在信息不完全方面，员工对福利进行发现和雇主对员工生产力进行发现之间存在对称过程。主要区别在于我们假设员工能够迅速了解到福利情况，而生产力只能逐渐测量（试用期太短无法揭示真实生产力）。

20In fact, and even if societies are constantly evolving on that issue. French women in 2011 have devoted more time than men to housework and the education of children. According to INSEE's enquiry on time use (2010), on average (including persons withot children), women devote 45mn daily to care for children, while men spend only 19 mn on such an activity. Indeed, in 2011, the employment rate of French women working full-time and living in a couple with three children or more was 39.8% against 87% for men in the same situation (INSEE, 2011b)
the household : Fw = 1+α*child*1∗(1+#children)α*child*2. For women under 25 and having children, this alpha is further multiplied by a factor (1 + α*youngWomen*).

实际上，尽管社会在这个问题上不断演变。根据INSEE关于时间利用的调查（2010年），2011年法国女性在家务和子女教育方面投入的时间比男性多。平均而言（包括没有孩子的人），女性每天花费45分钟照顾孩子，而男性只花费19分钟。事实上，在2011年，有三个或更多孩子的法国夫妇中，全职工作且生活在一起的女性就业率为39.8%，而男性则为87%（INSEE, 2011b）。
家庭：Fw = 1 + α * child * 1 * (1 + #children)α * child * 2。对于年龄在25岁以下且有孩子的女性，这个α还要乘以一个因素（1 + α * youngWomen）。

## 3.7.2 Overview Of The Decision-Making Process



The decision-making process of individuals is sequential. The transition from one state to another is done by comparing the utility level of the current state with the expected utility level in a new state.21 Each reachable state will be evaluated using the relevant values of income, amenity, stability and free time in the utility function, the difficulty to reach it, and the psychological cost of starting to search (ICHANG). The agent can then decide whether it is better for her to stay in his current state or to move to another one, as we see on Figure 2. In this case, the individual stops her decision process and changes state, as prescribed by Simon's satisficing heuristics (Simon, 1956).

个体的决策过程是顺序进行的。通过将当前状态的效用水平与新状态中预期效用水平进行比较，个体进行状态转移。每个可达到的状态都会使用收入、便利性、稳定性和空闲时间等相关价值在效用函数中进行评估，同时考虑到达该状态的难度以及开始搜索的心理成本（ICHANG）。然后，个体可以决定是继续保持当前状态还是转移到另一个状态，如图2所示。在这种情况下，个体会停止决策过程并根据西蒙的满足启发式规则（Simon, 1956）改变其状态。

注：图2未提供，请参考原文。

Every month, an individual in the inactive or *the employed* state receives information about NPros new jobs p prospected. This list of known jobs is obtained by randomly drawing a list of jobs among all job vacancies of JobAds that match the current occupation of the individual. On the basis of these informations she receives on these jobs, she evaluates *UTNEW*, which represents the interest to start looking for another job .

每个月，处于非活跃或已就业状态的个体会收到关于NPros新工作的信息。这些已知工作的列表是通过在所有与个体当前职业相匹配的职位广告中随机抽取一份工作列表来获得的。根据她对这些工作所获得的信息，她评估了UTNEW，即开始寻找另一份工作的兴趣程度。

Reservation utility calculation for the unemployed and On-The-Job-search states The reservation utility of the unemployed evolves according to the following equation :

对于失业和在职搜索状态的个体，预留效用的计算如下所示：

$$UTRES_{i,t}=UTRES_{i,t-1}\times(1-Param3_{UTRES})+Param4_{UTRES}\times(UTEM_{i,t}-UTEM_{i,t-1})\tag{18}$$

根据以下方程式，失业者的预留效用在时间 t 演化为：

$$UTRES_{i,t}=UTRES_{i,t-1}\times(1-Param3_{UTRES})+Param4_{UTRES}\times(UTEM_{i,t}-UTEM_{i,t-1})\tag{18}$$

If a worker becomes unemployed by putting, or has a job but considers looking for and job, the initial reservation utility of the individual $UTRES_{i,0}$ is computed from the list of all the jobs known during the free search: If an employee becomes unemployed because she is fired, $UTRES_{i,0}$ is initialized at $UTEM_{i,t}$, the utility of the job lost: the individual has no higher requirement. The reservation utility decreases at the rate of $1-Param3_{UTRES}$ with the seniority in unemployment. $Param3_{UTRES}$ is a calibrated parameter. $UTRE_{i,t}$ depends also on the changes in the movie utility $UTEM_{i,t}$ with a sensitivity coefficient $Param4_{UTRES_{i,t}}$, a calibrated parameter. This movie utility reflects the income per unit in the period (unemployment benefit, $S$A$). [20] The free time related by the memory content of each 20 by every week. This means that this myopic utility can rise for fall) and $UTRE_{i,t}$ accordingly.[20]
In the case of an On-the-Job-Search (OTJS) worker, her reservation utility is given by :
UTRESi,t = UTRESi,t−1 × (1 − Param3*UTRES*).

如果一个工人因为辞职而失业，或者有一份工作但考虑寻找新的工作，个体的初始预留效用$UTRES_{i,0}$是根据自由搜索期间所了解到的所有工作来计算的。如果一个员工因为被解雇而失业，$UTRES_{i,0}$初始化为失去的那份工作的效用$UTEM_{i,t}$，因为个体没有更高要求。随着失业时间的增长，预留效用以速率$1-Param3_{UTRES}$递减。其中$Param3_{UTRES}$是一个经过校准的参数。此外，$UTRE_{i,t}$还受到电影效用$UTEM_{i,t}$变化的影响，其敏感系数为$Param4_{UTRES_{i,t}}$，这也是一个经过校准的参数。电影效用反映了每单位时间内的收入（如失业救济金、SA）[20]。与每周相关联的空闲时间由每20周内存内容确定。这意味着这种短视效用可以上升或下降，并相应地改变$UTRE_{i,t}$[20]。
在职搜索（OTJS）状态下的员工，其预留效用由以下公式给出：
$$ UTRES_i,t = UTRES_i,t−1 × (1 − Param3* UTRES*)$$

## 3.7.3 Decision Of Student And Public Servant Agent



Given the variety of possible situations, we found difficult to model the behavior of students in this first version of WorkSim. We took a "black box" approach, simply aiming to reproduce the flow of students towards activity on the labor market in 2011.

鉴于可能出现的各种情况，我们发现在WorkSim的第一个版本中很难对学生的行为进行建模。我们采取了“黑盒子”方法，只是简单地试图在2011年再现学生进入劳动力市场的流动。

Furthermore, the public servant agents (21.3% of the agents) do not take decisions and are just present in order to reproduce demographic and employment statistics. When they retire, they are replaced according to a rate 1:1 (to be in a steady state) by young people who are finishing their studies and are randomly drawn in their cohort.

此外，公务员主体（占总主体数的21.3%）不做决策，只是为了再现人口统计和就业统计数据。当他们退休时，会按照1:1的比例（以保持稳定状态）由即将毕业并随机选取自己同龄群体的年轻人来替代他们。

## 3.7.4 Job Search Process



After describing the different decision mechanisms, let us now detail the overall job search process:
ITENSref .

在描述了不同的决策机制之后，现在让我们详细介绍整个就业搜索过程：ITENSref。

1. Each period in the model (one week in the reality), a job seeker receives from JobAds a list
of NPros vacancies matching its occupation level or a level above. At time t, this number
of vacancies NPros is determined according to a Poisson distribution with parameter λt =
NProsAvg ×
ITENSt
(a) NProsAvg is the average number of vacancies received by the unemployed each week
and set at the value of 3.
(b) *ITENS*tis the tension on the labor market at time t and ITENSref is the tension on
the labor market for the reference year we study (ITENSref = Vref
Uref = 0.044
0.092 = 0.48 in
2011). The higher the vacancy rate and the lower the unemployment rate, the more the job seekers receive vacancies each period.
2. The individual applies each period for the first offer she receives with a utility at least as
high as her reservation utility UTRESi,t.
3. At each step, if the individual looking for a job does not receive any job offer corresponding
to her occupation level or if all of her applications are rejected, she lowers her reservation
utility UTRESi,t.

3.7.4 就业搜索过程

在介绍了不同的决策机制后，我们现在详细描述整个就业搜索过程：

1. 在模型中的每个时期（现实中为一周），求职者从招聘广告中收到一个与其职业水平匹配或高于其水平的NPros空缺列表。在时间t，这个空缺数量NPros根据参数λt的泊松分布确定，其中λt = NProsAvg × ITENSt。
   (a) NProsAvg是每周失业者平均收到的空缺数，设定为3。
   (b) ITENSt是时间t上劳动力市场的紧张程度，而ITENSref是我们研究的参考年份劳动力市场的紧张程度（ITENSref = Vref / Uref = 0.044 / 0.092 = 0.48，在2011年）。空缺率越高、失业率越低，求职者每个时期收到的空缺就越多。

2. 每个时期，个体会申请她所接收到的第一个效用至少达到她保留效用UTRESi,t 的工作机会。

3. 在每一步中，如果正在找工作的个体没有收到与她职业水平相对应的工作机会或者她所有申请都被拒绝，她会降低她的保留效用UTRESi,t。

## 4 Model Calibration 4.1 Scaling



In order not to exceed our computation power, we limit the total number of agents to 10 000. To do so we first scale down the number of firms to reproduce the distribution of firms by size in France in 2011 (INSEE, 2011a). This gives a reduction factor of 1/4700 and a total of 808 firms.

为了不超过我们的计算能力，我们将主体的总数限制在10,000个。为此，我们首先按照2011年法国公司规模分布对公司数量进行缩减（INSEE，2011a）。这样得到了一个缩减系数为1/4700和总共808家公司。

From this firm distribution we derive the number of employees, 4411 in our case. Then, we add public servants in a proportion of 21.3% (INSEE Source (INSEE, 2013b)), and the numbers of "inactive", "unemployed", "retired" and "student" agents corresponding to 2011 statistics (INSEE, 2011d). We obtain a total of 8713 individual agents and it corresponds to the 40.79 million individuals in the age range 15-64 with a reduction factor of 4 682 (which is well in line with the reduction factor for the firms). Finally, we have then a total of 9521 agents in the simulation.

根据公司分布，我们得出了员工人数，本例中为4411人。然后，根据INSEE的数据来源（INSEE, 2013b），我们以21.3%的比例增加了公务员，并根据2011年的统计数据（INSEE, 2011d）确定了“非活动人口”，“失业人口”，“退休人口”和“学生”主体的数量。我们总共有8713个个体主体，并且这对应于1545-64岁年龄段的4079万个人，缩减系数为4682（与公司缩减系数相符）。最后，在模拟中我们总共有9521个主体。

## 4.2 Minimization Of A Fitness Function



To calibrate the model parameters (37) we minimize a *fitness* function that is the weighted sum of the relative spreads between the outputs of our model and the real targets of the French labor market in 2011 (source INSEE/DARES). We have chosen 49 main targets grouped in 7 different categories:

为了校准模型参数(37)，我们采用一个“适应度”函数进行最小化，该函数是我们的模型输出与2011年法国劳动力市场真实目标之间相对差距的加权和（数据来源：INSEE/DARES）。我们选择了49个主要目标，这些目标被分为7个不同的类别。

- 7 targets on unemployment rate by age group and by occupation level (INSEE, 2011c) - 6 targets on activity rate by age group and by gender (INSEE, 2011b)
- 20 targets on wages by age group and by occupation levels, and annual wages distribution
per decile on the global population (INSEE, 2013a)
- 9 targets on labor flows (DARES, Octobre 2012) (the global column values in Table 1 below)
- 9 targets on annual transition rate (Jauneau & Nouel de Buzonniere, 2011)24.
- 3 targets on share of long term unemployment in unemployment by age group (INSEE,
2011d)
- 4 additional targets on part-time job proportion in employment (INSEE, 2011d), vacancy
rate (Conseil d'Orientation pour l'Emploi (COE), 2013), the ratio of employed "looking for a new job" (OTJS) (INSEE, 2008) and the share of FDC in total employment (INSEE, 2011d).

- 根据INSEE（2011c）的数据，针对不同年龄组和职业水平，设定了7个失业率目标。
- INSEE（2011b）提出了6个关于不同年龄组和性别的活动率目标。
- 根据INSEE（2013a）的研究，共有20个关于不同年龄组和职业水平的工资目标，并对全球人口按十分位数进行了年工资分布分析。
- DARES（2012年10月）提出了9个劳动力流动目标（见表1中全局列值）。
- Jauneau和Nouel de Buzonniere（2011年）研究了9个关于年度转移率的目标。
- INSEE（2011d）提供了3个关于长期失业在不同年龄组失业人数中所占比例的目标。
- 此外，还有4个额外指标：就业中兼职比例、空缺率、"寻找新工作"就业者比例（OTJS）以及FDC在总就业中所占比例，这些指标由INSEE（2011d）、COE（2013年）提供。

## 4.3 Calibration Method



This fitness function is minimized at a horizon of 200 periods (each period corresponds to one week). To minimize our fitness function, we choose the evolutionary algorithm CMA-ES (Hansen & Ostermeier, 2001), which is one of the most powerful algorithms to solve this kind of problem (Auger & Hansen, 2012). CMA-ES means Covariance Matrix Adaptation Evolution Strategy. The principle of this evolutionary algorithm, inspired by biology, is to test step by step new generations of points in the parameters space. Each new generation of points is drawn stochastically according to the results obtained with the previous generation of points. The mean and the covariance matrix of the distribution of the new randomly drawn points is updated incrementally in order to move towards the best results obtained by previous generations.

该适应度函数在200个周期（每个周期对应一周）的时间范围内达到最小值。为了最小化该适应度函数，我们选择了CMA-ES进化算法（Hansen＆Ostermeier，2001），这是解决此类问题中最强大的算法之一（Auger＆Hansen，2012）。CMA-ES代表协方差矩阵自适应进化策略。这种受生物学启发的进化算法的原则是在参数空间中逐步测试新一代点。根据先前一代点获得的结果，每个新一代点的分布均值和协方差矩阵会逐步更新，以朝着先前一代获得的最佳结果移动。

Once the fitness function is minimized at the horizon of 200 periods in a steady state, we verify that a steady state is actually reached. This steady state is not devoid of a drift : however, on average, the simulated outputs for the targets have changed by less than 5% after 200 periods.

一旦适应度函数在稳态的200个周期内达到最小值，我们验证实际上已经达到了稳态。这个稳态并不是没有漂移的：然而，平均而言，在200个周期后，模拟输出的目标变化不超过5%。

## 4.4 Results Of The Calibration On The Main Targets



We obtain the results shown in Appendix C for the main targets of our calibration in a steady state
(the different rates are expressed in %), the outputs are averaged over 200 simulations. The values of the calibrated parameters are shown in Appendix D. We obtain an average relative spread between all the outputs of our model and the real targets of 12.9%. The average spread can be deemed satisfactory for such a large non-linear model.

我们在稳态下对我们校准的主要目标进行了模拟，结果如附录C所示（不同比率以百分比表示），输出是基于200次模拟的平均值。校准参数的数值显示在附录D中。我们发现，我们的模型输出与真实目标之间的平均相对差异为12.9%。考虑到这是一个庞大的非线性模型，这个平均差异可以被认为是令人满意的。

## 4.4.1 Comparison Of Simulated Flows With Dmmo Survey



The DMMO *(D´eclarations mensuelles des Mouvements de Main-d'Oeuvre*) is the only French source that measures several types of gross flows, yet only a small part of all types of gross flows, and therefore does not provide full accounts of labor flows. Yet it is of interest to verify whether other types of flows, which were not in our fitness function, are accurate or not. Therefore, we compare the workforce flows by age group calculated by WorkSim with the same variables calculated by DARES and based on DMMO (DARES, Octobre 2012). These entry and exit rates are ratios between gross entry or exit numbers during the 2011 year over the number of employed persons at the beginning of the year (they are not probabilities to move from a state to another).

DMMO（D´eclarations mensuelles des Mouvements de Main-d'Oeuvre）是法国唯一一个测量多种类型总流动的数据源，尽管只涵盖了所有总流动中的一小部分，因此无法提供完整的劳动力流动账户。然而，验证其他未包含在我们的适应函数中的流动类型是否准确仍具有重要意义。因此，我们将使用WorkSim计算得出的按年龄组划分的劳动力流动与DARES根据DMMO（DARES, 2012年10月）计算得出的相同变量进行比较。这些进入和退出率是指2011年期间净进入或净退出人数与年初就业人数之间的比率（它们并非表示从一个状态转移到另一个状态的概率）。

We note that most work flows calculated by WorkSim are close to DMMO, or at least the hierarchies of magnitudes by age groups are consistent. (cf. Table 1). Improvements require the introduction of more detailed institutions and behavior, and are left to future developments of the model.

我们注意到，WorkSim计算得出的大多数劳动力流动与DMMO接近，或者至少按年龄组划分的数量级层次是一致的（参见表1）。改进需要引入更详细的机构和行为，并留待模型未来发展。

| WorkSim outputs                  |   Source: Dares. DMMO/EMMO |
|----------------------------------|----------------------------|
| Global                           |                            |
| <                                |                       30   |
| 30 to 49                         |                            |
| >                                |                       50   |
| Global                           |                            |
| <                                |                       30   |
| 30 `a 49                         |                            |
| >                                |                       50   |
| Entry rate                       |                            |
| 49.1                             |                       88   |
| 51.0                             |                      115   |
| Entry in FDC rate                |                            |
| 39.8                             |                       75   |
| 40.0                             |                       92.1 |
| Entry in OEC rate                |                            |
| 9.3                              |                       13.1 |
| 11.1                             |                       23   |
| Exit rate                        |                            |
| 46.4                             |                       75.4 |
| 49.4                             |                      104.3 |
| Exit for FDC end                 |                            |
| 31.7                             |                       56.6 |
| 35.2                             |                       79.2 |
| Quit rate                        |                            |
| 5.9                              |                       11.9 |
| 6.5                              |                       13.9 |
| end of probationary period rate  |                            |
| 3.1                              |                        3.8 |
| 2.0                              |                        4.9 |
| dismissal for eco. reasons rate  |                            |
| 0.24                             |                        0.3 |
| 0.5                              |                        0.4 |
| dismissal for other reasons rate |                            |
| 4.1                              |                        2.7 |
| 3.2                              |                        4.3 |

| WorkSim输出结果                  |   数据来源: Dares. DMMO/EMMO |
|----------------------------------|----------------------------|
| 全球                             |                            |
| <30                              |                       30   |
| 30到49岁                        |                            |
| >50                              |                       50   |
| 全球                             |                            |
| <30                              |                       30   |
| 30到49岁                        |                            |
| >50                              |                       50   |
| 进入率                           |                            |
| 49.1                             |                       88   |
| 51.0                             |                      115   |
| FDC进入率                        |                            |
| 39.8                             |                       75   |
| 40.0                             |                       92.1 |
| OEC进入率                        |                            |
| 9.3                              |                       13.1 |
| 11.1                             |                       23   |
| 离职率                           |                            |

[参考原文，对上述中文译文进行重写:]

## 4.4.2 Comparison Of Simulated Annual Transition Rates With The Employment Survey



We now compare the annual transition rate of individuals calculated by the model with those obtained empirically from the Employment Survey *2007* (Jauneau & Nouel de Buzonniere, 2011), last year for that we have found the annual transition matrix. For 2011 we found only 3 transition rates in (INSEE, 2014). The transitions are based on questionnaires by comparing individual states at a certain date in year n and the same date in year n+1 (with a 12 months distance). A number in a state X in year n+1 comes from state Y in year n. The ratio of (number in X)/ (number in Y) gives the annual transition rate There are two interests in doing this comparison. First most of the empirical flow studies use these data. Second the Employment Survey defines unemployment as we do, according to the ILO norms, implying that only workers without a job and actively searching are labelled as unemployed.

我们现在将模型计算得出的个体年度转移率与从就业调查中获得的经验数据进行比较（Jauneau＆Nouel de Buzonniere，2011）。我们找到了去年的年度转移矩阵。对于2011年，我们在(INSEE, 2014)中只找到了3个转移率。这些转移是基于问卷调查，通过比较n年和n+1年同一日期时个体状态的变化（相隔12个月）。n+1年中状态X的数量来自n年中状态Y。 (X数量)/(Y数量) 的比值给出了年度转移率。进行这种比较有两个目的。首先，大多数经验流动研究使用这些数据。其次，就业调查像我们一样根据ILO标准定义失业，意味着只有没有工作并积极寻找工作的工人被标记为失业者。

We only aim to obtain a rough fit since the transition rates have been affected by the crisis between 2007 and 2011. The transition rates between the employment and unemployment obtained with our model are quite similar to the 2007 rate obtained from the Employment Survey (cf. Table 2). The lower transition rate of unemployment to employment (36.26%) fits well the 2011 Employment Survey figure (37.6%) and the higher stability into unemployment (56.8%) fits better the new INSEE figure (44% in 2011). Finally the transition from employment to unemployment (2.79%) fits better the the new INSEE figure (2.9%). These evolutions in our simulated data and the real data fit the effect of the 2008 crisis. The transition rates between inactivity and unemployment are however not well matched, but as Jauneau et al. (Jauneau & Nouel de Buzonniere, 2011) show, measuring the inactivity and the flows it entertains with unemployment is a difficult endeavor because of statistical biases in the data.

由于2007年至2011年的危机影响了转移率，我们只追求一个粗略的拟合。我们的模型计算得出的就业和失业之间的转移率与就业调查中获得的2007年转移率非常相似（参见表2）。失业到就业的较低转移率（36.26%）很好地匹配了2011年就业调查数据（37.6%），而更高的稳定性进入失业状态（56.8%）则更好地适应了新的INSEE数据（2011年为44%）。最后，从就业到失业的转移率（2.79%）更好地匹配了新的INSEE数据（2.9%）。我们模拟数据和实际数据中这些变化符合2008年危机的影响。然而，不活动和失业之间的转移率并不完全匹配，但正如Jauneau et al. (Jauneau & Nouel de Buzonniere, 2011)所指出，由于数据中存在统计偏差，测量不活动和其与失业之间流动关系是一项困难任务。

| Simulated by WorkSim transitions   |
|------------------------------------|
| Unemployment into Employment       |
| 36.26%                             |
| 42.1 % (37.6% in 2011)             |
| Unemployment into Inactivity       |
| 6.98%                              |
| 17.5 %                             |
| Unemployment into Unemployment     |
| 56.8%                              |
| 40.4 % (44.0% in 2011)             |
| Employment into Unemployment       |
| 2.79%                              |
| 2.5 % (2.9% in 2011)               |
| Employment into Inactivity         |
| 3.16%                              |
| 3.3 %                              |
| Employment into Employment         |
| 94.06%                             |
| 94.3 %                             |
| Inactivity into Employment         |
| 3.83%                              |
| 9.7 %                              |
| Inactivity into Unemployment       |
| 2.02%                              |
| 4.7 %                              |
| Inactivity into Inactivity         |
| 94.15%                             |
| 85.6 %                             |

由于2007年至2011年的危机对转移率产生了影响，我们只追求了一个粗略的拟合。我们的模型计算出的失业到就业的转移率与2007年就业调查数据非常相似（参见表2）。失业到就业的较低转移率（36.26%）很好地匹配了2011年就业调查数据（37.6%），而更高的失业到失业的稳定性转移率（56.8%）则更好地适应了新的INSEE数据（2011年为44%）。最后，从就业到失业的转移率（2.79%）更好地匹配了新的INSEE数据（2.9%）。我们模拟数据和实际数据中这些变化符合2008年危机的影响。然而，不活动和失业之间的转移率并不完全匹配，但正如Jauneau et al. (Jauneau & Nouel de Buzonniere, 2011)所指出，由于数据中存在统计偏差，测量不活动和其与失业之间流动关系是一项困难任务。

## 4.4.3 Transition Rates And The Underestimation Of Gross Flows



One very important methodological point must be made here. One can notice that these figures capture the transitions between two dates separated by a full year, but do not capture the intermediate transitions that have taken place during the year, unlike those calculated from DMMO rates. A state such as unemployment is transitory for part of the workers concerned since the majority of unemployment spells (60%) last less than a year. Thus, the annual transitions rates considerably underestimate mobility. The following computations illustrate this statement. The DUE (D´eclarations Uniques d'Embauche) is another source than DMMO for the hires (but only covers the hires), and give an exhaustive account of these. It should be however mentioned that the DUE are intentions to hire, and that it is acknowledged that they overestimate hires by 5 to 10%. We have taken from (Berche & Vong, 2012) a figure for 2011 of 20.6 Millions of hires in OEC and FDC, which can be dispatched between 3.4 Millions OEC and 17.2 Millions FDC, and among these 13.1 Millions FDC of less than one month. If we compute the number of hires of unemployed by applying the transition rate of 37.6% in the Employment Survey, to the unemployed in our simulation (2.2 Millions - see our figure 16), we obtain 826 448 hires. The DUE also include hires from employment as many workers change jobs. If we compute quits from the DMMO, we find 1.3 Millions moves that we will assume to be rehired. The hires in DUE without these quits are 19.3 Millions. The annual transition rates in the Employment Survey are then 4% of the DUE. The immense majority of hires on short run contracts are not captured by the annual Employment Survey, and this shows that the underestimation of gross flows is huge.

在这里需要强调一个非常重要的方法论观点。需要注意的是，这些数据捕捉到了相隔一整年的两个日期之间的转变，但没有捕捉到在这一年期间发生的中间转变，与从DMMO率计算得出的情况不同。对于部分受影响工人来说，失业等状态是暂时性的，因为大多数失业时段（60%）持续时间不超过一年。因此，年度转变率严重低估了流动性。以下计算说明了这一观点。DUE（D´eclarations Uniques d'Embauche）是除了DMMO之外的另一个招聘来源（但仅涵盖招聘），并提供了对其进行全面记录。然而需要指出的是，DUE是意向招聘，并且公认它们高估了5%至10%的招聘数量。我们从（Berche＆Vong, 2012）中获得2011年OEC和FDC中2060万次招聘数量，在3.4万次OEC和1720万次FDC之间分配，并且其中有1310万次FDC持续时间不足一个月。如果我们根据就业调查中37.6% 的转移率将模拟中失业人数（220万 - 见图16）应用于失业人数，则获得了826,448次招聘。DUE还包括来自就业的招聘，因为许多工人会换工作。如果我们根据DMMO计算辞职人数，我们发现有130万次变动，我们将假设这些人被重新雇佣。没有这些辞职的DUE招聘数量为1930万次。就业调查中的年度转变率占DUE的4%。绝大多数短期合同的招聘并未被年度就业调查捕捉到，这表明对总流量的低估是巨大的。

The Employment Survey has been made continuous since 2003, and transitions over short periods could in principal be computed. However the persons are interviewed once a quarter so that transitions under a quarter cannot be computed (Deroyon et al., 2013). A questionnaire on the preceding month allows to compute monthly transitions, but there is a retrospective memory bias. Morevover, these data have not been published. (Dubois et al., 2011) have treated the transitions between unemployment and employment under the assumption of homogeneity of the workers, and they find that the monthly transition from unemployment to employment is around 11% in 2010 (figure 1 in their paper), which yields a flow of 241,780 moves per month. The DUE yields a monthly figure of 1.6 Million hires in 2011 (as we mentioned overestimating hires by 5% to 10%). The ratio of transitions to the gross flows rises from 4% to 15% only. Our model captures 56% of the hires in the DUE, an underestimation that we have to accept if we want the other flows to fit the DMMO, which underestimate considerably the FDC of less than one month. However we capture the dominance of short FDC well enough since we simulate that 63% of FDC spells last one week, and 21% more than one week and less than one month25.

自2003年以来，就业调查一直持续进行，理论上可以计算短期转变。然而，被访者每个季度只接受一次采访，因此无法计算不到一个季度的转变（Deroyon等人，2013）。通过对上个月的问卷进行调查，可以计算每月的转变情况，但存在回顾性记忆偏差。此外，这些数据尚未公开发布。（Dubois等人，2011）在假设工人同质性的情况下研究了失业和就业之间的转变，并发现2010年失业到就业的月度转变率约为11%（他们论文中的图1），相当于每月241,780次流动。根据DUE数据，在2011年每月招聘数量为160万次（我们提到过高估招聘量5%至10%）。从总流量来看，转换率仅从4%上升至15%。我们的模型捕捉到了DUE中56% 的招聘数量，这是一个低估值，但为了使其他流动与DMMO相吻合（DMMO明显低估不足一个月时间段的FDC），我们必须接受这种低估值。然而，在模拟中我们很好地捕捉到了短期FDC占主导地位的情况，因为我们模拟了63%的FDC持续一周，21%持续一周以上但不足一个月25。

Another way to look at the underestimation problem is to look at the duration of FDC and unemployment spells. Barlet et al. (2014) measure a median spell for the FDC of 2 weeks in 2012.

另一种看待低估问题的方法是观察FDC和失业期间的持续时间。Barlet等人（2014）在2012年测量了FDC的中位数持续时间为2周。

These statistics mean that most of FDC could not captured by any enquiry that has a step of one month or more, and hence the flows between FDC and unemployment (and the other way) lead to a huge underestimation of gross flows even if computing monthly transitions. Data on (completed) unemployment spells by duration are not available, but they would certainly confirm that many short spells are underestimated by transitions matrices. In our model, 27% of the spells of unemployment among those completed during the year last at most two weeks and 50% last at most one month26.

这些统计数据表明，大多数FDC无法通过一个月或更长时间的调查来捕捉到，因此FDC和失业之间的流动（以及反过来）会导致总流动量被严重低估，即使计算每月转换率也是如此。关于（完成的）失业期间持续时间的数据不可得，但它们肯定会证实许多短期期间在转换矩阵中被低估。根据我们的模型，在完成的失业期间中，27% 的持续时间最多为两周，50% 的持续时间最多为一个月。

## 4.4.4 Unemployment By Age And Occupation Group



The WorkSim model allows to compute detailed data on the characteristics of unemployment by age group and occupation level, shown in Table 3 below. First we note that the average duration of unemployment spells is much lower than the average unemployment seniority. This reflects a composition effect (the most employable of the unemployed individuals find a job quickly) and possibly a *duration dependance effect* (a decrease of the exit rate when unemployment seniority increases). The latter effect is however a controversial issue in the empirical studies (OECD, 2011), and since the evolution of the reservation utility with the unemployment seniority is an important factor of exit intensity in the model, we formalize three effects :

WorkSim模型可以计算不同年龄组和职业水平的失业特征的详细数据，如下表3所示。首先需要注意的是，失业期间的平均持续时间远低于失业资历的平均值。这反映了一个组成效应（最易就业的失业者很快找到工作）和可能存在的“持续时间依赖效应”（当失业资历增加时，退出率下降）。然而，后一种效应在实证研究中存在争议（OECD, 2011）。由于模型中失业资历对退出强度起到重要作用，我们对这三种影响进行了形式化处理。

- the seniority of unemployment has a negative effect on the reservation utility, since the
unemployed understands she cannot succeed to obtain the good jobs she has applied to, and this raises the hiring rate
- the decrease in the replacement rate when the unemployment redundancy is replaced by
welfare reinforces this reservation utility decrease, and this has a positive effect on the hiring rate
- finally the decrease in the reservation utility may induce some unemployed to exit to inactivity
All these effects decrease unemployment. However, the seniority of unemployment induces a progressive loss of human capital after six month that decreases the hiring rate and increases unemployment. The net effect of these opposed factors is the existence of a very substantial proportion of long term unemployed. The long-term unemployment is well reproduced as a proportion of total unemployed persons. On average, in our model, 34.5% of the unemployed persons have been unemployed for more than 1 year and 26% for more than 2 years (which is not very far from the 40.5% and 19% rate respectively obtained with the Employment Survey (INSEE, 2011d).

- 失业的资历对预留效用产生负面影响，因为失业者意识到她无法成功获得所申请的优质工作，从而提高了招聘率。
- 当失业补偿被福利取代时，替代率的下降加剧了预留效用的减少，进而对招聘率产生积极影响。
- 最后，预留效用的减少可能导致一些失业者选择退出劳动力市场。

所有这些因素共同减少了失业率。然而，失业时间的增长会导致人力资本逐渐流失，在六个月后降低了招聘率并增加了失业率。这些相互对立的因素综合作用下，长期失业者占据相当大比例。在我们的模型中，平均有34.5%的失业者已经超过1年处于失业状态，并且26%超过2年（与就业调查（INSEE, 2011d）得出的分别为40.5%和19%相差不远）。

|                                                     | Global        | 15 24 years   | 25 49 years   | 50 64 years   |
|-----------------------------------------------------|---------------|---------------|---------------|---------------|
| Share of long-term unemployed - more than 1 year    | 34.5% (3.4%)* | 26.3% (3.6%)  | 38.5% (2.8%)  | 34.8% (3.4%)  |
| Share of long-term unemployed - more than 2 years   | 26.0% (2.1%)  | 16.0% (2.2%)  | 30.3% (3.1%)  | 27.7% (3.7%)  |
| Average unemployement seniority (in month)          | 13.9 (0.90)   | 10.4 (0.69)   | 15.4 (0.97)   | 14.4 (1.21)   |
| Average duration of unemployment spells (in months) | 2.59 (0.71)   | 3.14 (0.19)   | 2.28 (0.22)   | 2.51 (0.25)   |

|                                                     | 全球          | 15-24岁       | 25-49岁       | 50-64岁       |
|-----------------------------------------------------|---------------|---------------|---------------|---------------|
| 长期失业比例 - 超过1年                                | 34.5% (3.4%)* | 26.3% (3.6%)  | 38.5% (2.8%)  | 34.8% (3.4%)  |
| 长期失业比例 - 超过2年                                | 26.0% (2.1%)  | 16.0% (2.2%)  | 30.3% (3.1%)  |27 .7%(3 .7 %) |
| 平均失业时长（月）                                    |13 .9(0 .90)   |10 .4(0 .69)   |-15 .4(0 .97)   |-14 .4(1 .21)   |
| 失业时期的平均持续时间（月）                          |-2。59(0。71)   |-3。14(0。19)   |-2。28(0。22)    |-2。51(0。25)|

*The Figures in brackets are the standard deviations on the results

*括号中的数字表示结果的标准差。

## 5 Simulation Analyzes And Results



We first undertake a sensitivity analysis on some important parameters in order to explore the model outputs, showing that the results can be interpreted through economic mechanisms that make sense. We then use the model to offer a first characterization of the nature of the French labor market.

为了探索模型的输出结果，我们首先对一些重要参数进行了敏感性分析，结果显示可以通过具有经济意义的机制来解释。然后，我们使用该模型对法国劳动力市场的性质进行了初步描述。

## 5.1 Sensitivity Analysis



In order to perform the sensitivity analyzes, we run a set of simulations by changing the value of a given parameter step by step, the others remaining at their calibrated values. For each consecutive point, we measure the outputs of the model after 200 periods (4 years in reality) and average these results over 200 simulations in order to eliminate the stochastic effects. The results enable us to uncover if a parameter has a significant, null, or overwhelming role on the main features of the labor market. We analyze the effects of changing two different types of parameters. First we look at some of those which play a potentially important role in the behavior of the agents, namely the preference for free time, the cost of change to a new state, the speed of the decline of the reservation utility with the seniority of unemployment, and the change in the level of uncertainty of the employer on a newly hired worker. Second we submit the model to two types of aggregate shocks, one on demand, and the other on the parameter which influences the share of the wages in the total value.

为了进行敏感性分析，我们通过逐步改变给定参数的值来运行一系列模拟，其他参数保持其校准值不变。对于每个连续点，我们在经过200个周期（实际上相当于4年）后测量模型的输出，并在200次模拟中对这些结果进行平均，以消除随机效应。这些结果使我们能够揭示一个参数对劳动力市场的主要特征是否具有显著、无效或压倒性的作用。我们分析了改变两种不同类型参数的影响。首先，我们关注那些在主体行为中可能起到重要作用的参数，包括对自由时间的偏好、转换到新状态的成本、失业资历随着资历增长而预留效用下降速度以及雇主对新雇员存在不确定性水平的变化。其次，我们将模型置于两种类型的总量冲击之下，一种是需求冲击，另一种是影响工资占总价值比例的参数冲击。

## 5.1.1 Preference For Free Time



The parameter α0 represents the basic mean preference for free time in the computation of the free time parameter α (c.f. section 3.7.1 above). The higher α0, the higher is the preference for free time compared to wages and non-monetary job characteristics. An increase in α0 leads to greater valuation of free time that leads to a substantial decrease in activity (cf. Figure 3).

参数α0代表在计算自由时间参数α时的基本平均偏好。α0越高，相对于工资和非货币工作特征，对自由时间的偏好就越高。增加α0会导致对自由时间的估值增加，从而导致活动量大幅减少（参见图3）。

For the unemployment rate, when α raises and is below 0.23, some unemployed stop to search and then the unemployment rate decreases. When α becomes somewhat higher than the calibrated value, the number of unemployed remain constant while the number of active persons decreases, which leads to an increase of the unemployment rate. Therefore the unemployment rate has a U-Shape (non monotonic).

对于失业率而言，当α提高并且低于0.23时，一些失业者停止求职，从而导致失业率下降。当α略高于校准值时，失业人数保持不变，而活跃人数减少，这导致失业率增加。因此，失业率呈现出U形曲线（非单调）。

## 5.1.2 Cost Of Change To A New State



Mobility, and its inverse, stability in a state, is one of the crucial features to characterize a given aggregate labor market or the situation of some categories of labor when there is no homogeneity. The individuals will be less mobile when the cost of changing one's state rises. This cost is measured by the *ICHANG* parameter, which reflects psychological and economic transition costs (cf. section 3.7.2). When *ICHANG* is equal to 1, there is no cost of entering the labor market and the activity rate is then higher as shown on Figure 4. When *ICHANG* decreases from its calibrated value 1.2 to become close to 1, we see on Figure 6 that the quit rate increases considerably, because more employed workers are looking for another job and quit their own job. This *individual instability* leads to a high turnover rate on the labor market and increases the unemployment rate (cf. Figure 5).

在描述一个总体劳动力市场或某些劳动力类别情况时，流动性和稳定性是两个关键特征。当存在非均质性时，个体的流动性会受到改变状态成本的影响。这个成本由参数ICHANG衡量，它反映了心理和经济转换成本（参见第3.7.2节）。当ICHANG等于1时，进入劳动力市场没有成本，并且活跃率较高（如图4所示）。当ICHANG从校准值1.2减小至接近1时，我们可以从图6中看到离职率显著增加，因为更多的就业者正在寻找新工作并辞去原有工作。这种“个体不稳定性”导致劳动力市场高周转率，并增加失业率（参见图5）。

## 5.1.3 Reservation Utility Decline With Seniority In Unemployment



We now study the effect of the labor supply attitude of workers, and more precisely, in a search framework, one of the main parameters that determines it: the rate at which the workers decrease their reservation utility when their unemployment seniority increases. This rate is Param3UTRES
in our model, the reservation utility reduction parameter in equation 18. We see in Figure 8 that the higher the reservation utility reduction parameter, the lower is the unemployment rate, because the unemployed revise faster their reservation utility in their job search process and then accept a high number of job offers. The same happens for the longterm unemployment rate (more than one year) and the effect is considerably more pronounced. This experiment highlights the *existence of some search unemployment* in the model, Finally the faster reduction of the reservation utility induces some discouragement of unemployed persons, and the activity rate decreases (cf. Figure 7).

我们现在研究劳动者的劳动力供给态度的影响，更具体地说，在一个搜索框架中，有一个主要参数决定了这种态度：即当劳动者的失业资历增加时，他们降低保留效用的速率。在我们的模型中，这个速率被称为Param3UTRES，即方程式18中的保留效用减少参数。从图8中可以看出，保留效用减少参数越高，失业率就越低，因为失业者在求职过程中更快地修正他们的保留效用，并接受更多的工作机会。对于长期失业率（超过一年），情况也是如此，并且效果明显更加显著。这个实验突出了模型中存在某种搜索失业现象。最后，保留效用减少速度较快导致部分失业人员感到沮丧，并且活跃率下降（参见图7）。

## 5.1.4 Uncertainty On Workers'Productivity



The parameter σ0 represents the basic uncertainty of the firm when it evaluates the productions of its employees (equation 8).

参数σ0代表了企业在评估其员工的生产力时的基本不确定性（方程式8）。

This uncertainty reflects the organization of the production and its management. For instance, the tayloristic firm, in which the management decides the production process in minute detail, yields a low uncertainty while more modern organizations, that allow for more autonomy, lead to higher uncertainty. We see that an increase of uncertainty in the firm evaluation leads to higher entry and exit rates (cf. Figure 10). The firm makes more mistakes in its recruitment process and is more likely to fire on personal ground afterwards. We notice in Figure 9 that when uncertainty increases, the long-term unemployment decreases strongly, because the chance to get a job even with a weak core productivity is higher. This leads to a slight decrease of the global unemployment rate (from 10.3% to 9%).

这种不确定性反映了生产组织和其管理方式。例如，泰勒制企业通过管理层对生产过程进行详细决策，从而降低了不确定性；而更现代化的组织则允许更多的自主权，导致不确定性增加。我们可以观察到，企业评估中不确定性的增加会导致进入和退出率的提高（参见图10）。企业在招聘过程中会犯更多错误，并且更有可能因个人原因解雇员工。从图9中我们可以看到，随着不确定性的增加，长期失业率大幅下降，因为即使核心生产力较弱，也有更高的就业机会。这导致全球失业率略微下降（从10.3%降至9%）。

## 5.2 Response To Aggregate Changes



In this section, we aim to study the effects of some macroeconomic exogenous changes. Namely, we first analyze how the share of sales revenue between firms and workers impacts the main aggregates on the labor market, and then the market response to some aggregate demand shocks.

在本节中，我们旨在研究一些宏观经济外生变化的影响。具体而言，我们首先分析销售收入在企业和工人之间的分配比例对劳动力市场主要聚合指标的影响，然后研究市场对一些总需求冲击的反应。

## 5.2.1 Share Of Net Wages In Sales Revenue



The share of the sales revenue kept by the firm ζ determines the share of the workers (1 − ζ), and more precisely the share of the net (real) wages, since the payroll charges are not included in the workers' wages (cf. equation 11). Because ζ is homogeneous over firms, changing ζ corresponds to a change in the balance of power between firms and workers. Results are shown in Figure 11. We observe a U-shape, and opposite effects on unemployment and employment rates, with a minimum unemployment rate of 9% for the calibrated value (cf. Figure 11b). If the share of firms is smaller and decreases (ζ < 0.74), the unemployment increases because firms create fewer jobs. Jobs have indeed less chances to be profitable. Conversely, if the share of firms is higher and increases (ζ > 0.74), the wages proposed to individuals decrease and the jobs become less and less attractive, which results in an increase in the unemployment rate, since participation does not decline much. Two factors explain this mild decline. First, when ζ approaches 1 (i.e.

企业保留的销售收入比例ζ决定了工人所占的比例（1-ζ），更准确地说是净工资的比例，因为工资中不包括薪资费用（参见方程11）。由于ζ在企业间是均匀的，改变ζ相当于改变企业和工人之间的权力平衡。结果如图11所示。我们观察到一个U形曲线，并且对失业率和就业率产生相反的影响，校准值下失业率最低为9%（参见图11b）。如果企业份额较小且减少（ζ < 0.74），则失业率增加，因为企业创造的就业机会较少。事实上，就业机会更难盈利。相反地，如果企业份额较高且增加（ζ > 0.74），向个人提供的工资降低，岗位变得越来越不具吸引力，这导致失业率上升，因为参与度没有大幅下降。有两个因素解释了这种轻微下降。首先，在ζ接近1时（即

when the firm share is close to 100%), wages will not drop to 0 since they must remain equal to the minimum legal net wage (1 072 euros per month in France in 2011), as displayed in Figure 12. Second the model does not offer to the individuals the possibility to become self-employed or undertake illegal activities to support themselves. Most of them then keep searching a job.

当企业份额接近100%时，工资不会降至0，因为它们必须保持等于法定最低净工资（2011年法国每月1072欧元），如图12所示。其次，该模型不提供个人成为自雇或从事非法活动以维持生计的可能性。因此，大多数人会继续寻找就业机会。

## 5.2.2 Demand Shocks



Finally, we study a macroeconomic shock on global demand. To do so, we apply a multiplicative factor on the demand and observe the response of the model after 200 periods (4 years in the model).

最后，我们研究了对全球需求的宏观经济冲击。为此，我们在需求上应用一个乘法因子，并观察模型在200个周期（模型中的4年）之后的响应。

If the demand shock is negative (aggregate demand factor falling under 1), the unemployment rate increases dramatically, which highlights an unemployment by lack of demand. When the demand factor is greater than 1 (demand increase), the unemployment rate decreases, but it does not decrease to zero, while the vacancy rate becomes very important. As found in real labor markets, there is a persistent unemployment caused by search on both sides, workers and employers. It can be characterized as a frictional unemployment, the level of which however depends also on the institutions of the labor market. This means that such factors (institutional or behavioral) as the firing costs, the level of unemployment benefits and welfare, the preference for free time and the rate of decrease of the reservation utility among others affect it (see Figure 13).

如果需求冲击为负（总需求因子低于1），失业率将大幅增加，凸显出由需求不足引起的失业问题。当需求因子大于1（需求增加）时，失业率会下降，但不会降至零，而职位空缺率变得非常重要。实际劳动力市场研究发现，双方都存在搜索引起的持续性失业问题，即工人和雇主。这可以被描述为摩擦性失业，其水平也取决于劳动力市场的制度。这意味着解雇成本、失业救济和福利水平、对休闲时间的偏好以及预留效用减少速度等因素都会对其产生影响（见图13）。

## 5.3 Use Of The Model To Characterize The French Labor Market: Flows And Segmentation



Finally, we study the weekly gross flows diagrams we derive directly from our simulations. Since the unit period is the week, no flow between two states is left unmeasured. Intra week flows are however theoretically possible and not taken into account, because the ILO and Employment Survey definition of unemployment makes it impossible to measure since it is enough to have worked one hour in the week to be considered as being employed during that whole week. The gross flows constitute a stock-flow consistent accounting system that no institution in France or elsewhere can build with the real data since the latter are not complete. The simulation model is thus a unique tool to obtain a complete and consistent description of the French flows, after calibration, and building this consistent accounting is the preliminary step to analysis. On practical grounds, as we have shown, it is less subject to the underestimation of flows that we find in the monthly or annual transition rates calculated from the *Employment Survey*. Thus we are ready to characterize our labor market and we will see how an important aggregate feature emerges: segmentation, and more precisely *dualism*. The model contains an institutional segmentation by the mere fact that at a point of time 90% of the workers are on an OEC job, while the other 10% are on a FDC job. The two types of jobs differ at least by the legal features of the contract and the unknown duration in the first case (but with the protection against a fast termination) and the fixed duration in the second case, duration that has a median value of 2 weeks in France. However a dualism implies more, and namely that some workers are stable in OEC while others move back and forth between unemployment and FDC, for a significant length of time or for most of their professional life.

最后，我们研究了从模拟中直接得出的每周总流动图。由于单位周期为一周，因此没有两个状态之间的流动被遗漏。然而，在一周内的流动在理论上是可能的，但由于国际劳工组织和就业调查对失业的定义使其无法测量，因为只要在一周内工作了一个小时就被认为在整个周内都是就业状态。总流动构成了一个库存-流量一致的会计系统，在法国或其他地方没有任何机构可以使用真实数据建立这样完整的系统，因为后者并不完整。因此，模拟模型是获得法国流动完整且一致描述的独特工具，在校准之后建立这种一致性会计是分析的初步步骤。从实际角度来看，正如我们所展示的那样，它不太容易低估从“就业调查”计算出来的月度或年度转换率中发现的流动。因此，我们已经准备好对劳动力市场进行描述，并将看到一个重要的总体特征出现：分割和更确切地说是“二元性”。该模型通过事实上90% 的工人在OEC（长期雇佣合同）职位上工作而另外10% 的工人在FDC（固定期限合同）职位上工作，包含了一种制度性的分割。这两种类型的工作至少在合同的法律特征和第一种情况下未知的持续时间（但有快速解雇保护）以及第二种情况下固定的持续时间方面有所不同，在法国，这个持续时间的中位数为2周。然而，二元性意味着更多，即一些工人在OEC上稳定就业，而其他人则在失业和FDC之间来回移动，在相当长的时间内或者他们职业生涯中大部分时间都是如此。

We present the flow diagrams for all individuals and by age group (15-24, 25-49 and 50-64
years old), translated at the national level scale. Each type of flow is measured in two ways. First the numbers associated with the arrows indicate the number of agents in thousands who move from one state to another during the basic period, a week. The thickness of an arrow in the diagram shows the strength of a flow compared to the other flows. Second the percentage in brackets indicates the proportion of agents of a group who change state. This is computed as the ratio of the gross flow between two states on the number of the agents in the a state of origin. It can be labeled as the probability of transition from a state to another from a period to the next. These probabilities are very low because they are calculated on a weekly basis but exit probabilities from the same state can be compared and the relative probabilities can be interpreted in economic terms.

我们在全国范围内以年龄组（15-24岁、25-49岁和50-64岁）为尺度呈现了所有个体和流动图表。每种流动方式都有两种测量方法。首先，箭头上的数字表示在基本期间（一周）内从一个状态转移到另一个状态的主体数量，以千为单位。图表中箭头的粗细显示了与其他流动相比的流量强度。其次，括号中的百分比表示改变状态的群体中主体的比例。这是通过将两个状态之间的总流量与原始状态下主体数量之比计算得出的。它可以被标记为从一个时期到下一个时期从一个状态转换到另一个状态的概率。由于这些概率是基于每周计算的，所以非常低，但可以比较相同状态下的退出概率，并且可以用经济术语解释相对概率。

In the diagram for all individuals (Figure 14), the labor market is characterized by high rates of turnover between the states of "unemployed" and "Employed under FDC". The entry flow in FDC from unemployment is the largest of all flows with 162 00027 persons per week and about five times greater than the flow of direct entry in OEC from unemployment, 31 000 that is the third flow by order of importance28. Exit to unemployment from FDC, is also a major stream amounting to 137 000, the second in size. Exit from OEC to unemployment are much lower and constitutes the fourth flow with 26 000 persons. The conversions of FDC into OEC represent only the fifth flow, 12 600 with 8.4% of the exits from FDC (leaving aside the flows to inactivity and retirement), the other persons going into unemployment. It is an indicator of the stepping stone effect, since FDC offers potentially a chance for workers to obtain an integration in OEC in the same firm. However, this integration is a partial measure of the stepping stone effect as there is also a longer term effect, by which experience acquired in FDC may favor later integration into OEC in an other firm. In our simulation, we find that 22 % of individuals in FDC are working in OEC one year later.

在所有个体的图表中（图14），劳动力市场的特点是“失业”和“FDC下就业”之间的高流动率。从失业到FDC的进入流量是所有流量中最大的，每周有162,00027人，约为直接从失业到OEC的进入流量的五倍，即31,000，这是按重要性排序的第三个流量28。退出FDC进入失业也是一个重要的流量，总数为137,000，排名第二。相比之下，从OEC到失业的退出要低得多，仅有26,000人，并且排名第四。将FDC转换为OEC仅占据了第五个流量位置，共计12,600人，占FDC退出总数（不考虑转向非活动和退休）的8.4％，其余人员则进入失业状态。这一指标显示了跳板效应，因为FDC潜在地为工人提供了在同一公司获得OEC整合机会。然而，这种整合只是跳板效应的部分衡量指标，因为还存在长期效应，在其中在FDC获得经验可能有利于以后在其他公司获得OEC整合。根据我们进行的模拟结果，在FDC中有22％的个体一年后正在OEC中工作。

Therefore, a first and important observation is that FDC generate important flows towards unemployment and from unemployment to FDC, but at this stage we cannot say whether this mobility is concentrated or not on a rather small fraction of the agents, and consequently if there is segmentation, or not. There are two extreme stories to interpret the data. A first story is segmentation: some workers alternate precarious FDC, which are generally short as mentioned, and periods of unemployment. The other workers are employed in very stable OEC, even if some of these workers can lose their jobs because they are fired for personal or economic motives. The second story is integration with a delay: it tells that FDC is mainly a stepping stone to obtain an OEC later, but one that might require a significant number of spells in FDC to accumulate experience. In the latter case, the flow from unemployment to FDC should not be overwhelmingly large compared to the flow from unemployment to OEC, and the one from FDC to OEC. In the Figure 14, we see that the move from unemployment to FDC is 3.7 times larger than the sum of the moves from FDC to OEC and from unemployment to OEC. Thus, we infer that a segmentation between workers occurs in the sense that many workers on FDC are moving back and forth between FDC and unemployment (very few chose inactivity, only 2750), while other workers have long spells of employment on OEC (28 months in the model). Some are fired from OEC - the flow amounts to 12 000- and spend some time unemployed to find another OEC.

因此，首要且重要的观察是，FDC对失业和从失业到FDC之间产生了重要的流动，但目前我们无法确定这种流动是否集中在一小部分个体上，以及是否存在分割现象。对于这些数据，有两种极端的解释。第一种解释是分割现象：一些工人在不稳定的FDC岗位和失业期间交替工作。而其他工人则在非常稳定的OEC岗位上就业，尽管其中一些工人可能因个人或经济原因而失去工作。第二种解释是延迟整合：它认为FDC主要是为了以后获得OEC而进行的一个跳板，但可能需要经历相当数量的FDC周期来积累经验。在后一种情况下，从失业到FDC的流动量不应该比从失业到OEC和从FDC到OEC之间的流动量大得多。根据图14所示，在从失业到FDC的转移中，其规模比从FDC到OEC和从失业到OEC之间的转移总和大3.7倍。因此，我们推断出劳动者之间存在分割现象，即许多处于FDC状态下的劳动者来回穿梭于FDC和失业之间（只有2750人选择不活动），而其他劳动者在OEC上有长时间的就业周期（模型中为28个月）。其中一些人被OEC解雇，流动量达到12,000，并花费一些时间失业以寻找另一个OEC岗位。

This is not the end of the story. If there is segmentation, the next issue is whether this segmentation is temporary for individuals or durable over the working life. The frontier between the two is not a precise figure, but an integration of young workers that would go beyond a period of 5 to 8 years after entry or say beyond being 30 years old, could be termed durable. Durable segmentation has very serious effects in terms of well-being on the cycle of life such as the difficulty to rent an accommodation and to obtain a loan to buy an accommodation, and brings the risk of exclusion. A temporary segmentation is an integration in an OEC after a difficult period in FDC and unmployment for those youths who have not obtained an OEC straightaway after their studies 29. In order to give some elements of answer on the durable character of the segmentation for a worker, we need to split the diagram by age groups, as depicted in the following Figures 15 and 16 below.

这并非故事的终结。如果存在分割现象，下一个问题是这种分割是个体暂时性的还是在职业生涯中持久存在的。两者之间的界限并非确定的数字，而是指年轻工人在入职后5至8年或30岁之后超过一段时间内进行整合，可以称之为持久性分割。持久性分割对生命周期中的幸福感产生严重影响，例如租房和购房贷款难度增加，并带来排斥风险。暂时性分割指那些在完成学业后未能立即获得稳定就业(OEC)的年轻人经历了FDC和失业困境后才得以融入OEC。为了对劳动者分割现象是否具有持久性提供一些答案，我们需要按年龄组划分图表，如下图15和16所示。

The flow diagrams appear persistent between the 15-24 and the 25-49 age groups. The flows between unemployment and OEC remain fairly of the same order of magnitude in probabilities to move. The probability to move from unemployment into OEC is 1.47% per week for the 25-49 age group, while it it is 1.04% for the 15-24 age group, indicating that experience matters. The probability from OEC to unemployment is 0.13% for the 25-49 age group while it is 0.09% for the 15-24 age group. It shows that the OEC are not life time jobs and that the 25-49 age group is not immune to contract termination. The conversions of FDC in OEC rate are not very high since they amount to 0.67% per week against 0.8% for the 15-24 age group, nor is the recruitment in OEC, so that precariousness does not disappear.

15-24岁和25-49岁年龄组之间的流程图显示出持续性。失业与OEC之间的流动概率在相同数量级上保持相对稳定。25-49岁年龄组从失业转向OEC的每周概率为1.47%，而15-24岁年龄组为1.04%，这表明经验对于转换至关重要。从OEC转向失业的概率为25-49岁年龄组为0.13%，而15-24岁年龄组为0.09%。这表明OEC并非终身职位，同时25-49岁年龄组也不免于合同终止的风险。FDC转化为OEC的比例并不高，每周仅占0.67%，而15-24岁年龄组则为0.8%，招聘进入OEC的比例也不高，因此不稳定性并未消失。

The market for seniors (Figure 17) is similar to the market for the 25 - 49 age group except for the retirement flow. The flow rates between unemployment and FDC remain similar and substantial, as well as the hiring rate of unemployed into OEC (1.76%), the exit rate from OEC to unemployment (0,15%). The main new flow, which increases the total exit from OEC is the transition to retirement (0.002% per week). Persistence of segmentation seems to occur.

与25-49岁年龄组市场相比，老年人市场（图17）在退休流动方面存在差异。失业和FDC之间的流动率保持相对稳定且显著，失业者进入OEC的招聘率为1.76%，从OEC转向失业的退出率为0.15%。主要的新流动是转向退休（每周增长0.002%）。这种分割性的持续存在似乎是不可避免的。

A disaggregated analysis of the workforce by occupation levels will not be detailed here because of the lack of space. Its main conclusion is that the flows between FDC and unemployment are concentrated on blue collar workers and employees without disappearing in the other categories. The observations we made for the age groups point to a durable segmentation for a fraction of the young workers, while another fraction stabilizes into OEC. The Employee/blue collar occupation is specially concerned. Yet a precise assessment would require cohort analysis over the life cycle and a typology of the careers, as well as a comparison with the rare empirical studies that are available and cover only part of the life cycle. While the ABM tool is very fit for this analysis, which we have started to undertake, it will require a full paper to present it properly. The present paper analysis should be considered as a first step in our research program as far as this topic is concerned.

由于篇幅有限，本文不会详细探讨职业层次的劳动力分析。然而，主要结论是FDC和失业之间的流动主要集中在蓝领工人和其他类别中的雇员身上，并没有在其他类别中消失。对于年龄组的观察表明，一部分年轻工人存在持久的分割现象，而另一部分则稳定地进入OEC。特别需要关注雇员/蓝领职业。然而，要进行准确评估需要进行整个生命周期的队列分析和职业生涯分类，并与少数可用且仅涵盖生命周期部分的实证研究进行比较。虽然ABM工具非常适合这种分析（我们已经开始进行），但需要一篇完整的论文来全面展示。因此，本文应被视为我们研究计划在这个主题上的第一步。

## 6 Conclusion



In the version presented here, the WorkSim model provides a comprehensive theoretical framework of the labor market. Following ARTEMIS, WorkSim is the first to bring together a number of elements, which we consider jointly essential to characterize precisely the nature of a specific labor market, in order to have a tool for employment policies analysis:

在这个版本中，WorkSim模型提供了一个全面的劳动力市场的理论框架。作为ARTEMIS之后的继任者，WorkSim首次将多个要素结合在一起，我们认为这些要素共同对于准确描述特定劳动力市场的性质至关重要，以便提供一种就业政策分析工具。

1. the **stock-flow accounting** of individuals, based on gross flows, is complete and endogenous. It can be supplemented by a stock-flow accounting of jobs (and even jobs within the company) for further analysis. This is a preliminary step for a thorough analysis of a labor market.
2. the **institutional environment** is modeled and based on labor law, which sets constraints
on the possible decisions.
3. the mobility is modeled through decision-making based on bounded rationality with learning. These decisions are made by the firms **and** the individuals, both heterogeneous. They
are based on a *search theory framework*, which is rooted in the consideration of the cost
of state change (search costs, mobility costs) in a decentralized market, and extended to a general theory of mobility. This theoretical framework provides an intellectual coherence to the many decisions modeled, and the many gross flows simulated. It also appears to have a higher analysis potential for the analysis of competition between categories of workers (for instance) both in the short run and over the life cycle than the matching model that assumes homogeneity. The results, for instance the emergence of segmentation, are however not the results of standard search theory and reflect the role of institutions that impinge at the micro level but have aggregate and possibly unexpected effects coming from the multiple interactions.
WorkSim is calibrated on a large number of targets of the French labor market in 2011, by implementing a powerful algorithm that has not already been used in economic models. It reproduces well enough these targets to conduct some economic analyzes. Moreover, it reproduces often well and sometimes very well the gross flows measured by different statistical sources and with different types of measures. It reproduces well gross flows of labor of the DMMO and many of the annual transitions calculated by the Employment Survey (*Enquˆete Emploi*). These statistics are widely used in analyzes and debates on the French labor market. The DMMO however gives an information on only some of the flows, which precludes a stock-flow accounting. WorkSim, by simultaneously fitting the gross flows of the DMMO and the annual transitions rates of the Employment Survey, uncovers the massive underestimation of mobility if these transitions are considered as a proxy of the gross flow rates. We also show that the monthly transitions measured by the Employment Survey (only for hires) diminish the underestimation of flows only in a marginal way.

1. 个体的存量-流量核算是基于总流量的，它是完整和内生的。为了进一步分析，可以通过对工作岗位（甚至公司内部的工作岗位）进行存量-流量核算来补充。这是对劳动力市场进行全面分析的初步步骤。
2. 制度环境是通过建模并基于劳动法来设定可能决策的限制。
3. 移动性通过基于有限理性和学习的决策进行建模。这些决策由企业和个体（都是异质的）做出。它们基于搜索理论框架，该框架根植于考虑去中心化市场中状态变化成本（搜索成本、移动成本），并扩展为一般移动性理论。这个理论框架为建模的许多决策和模拟的许多总流提供了智力上的连贯性。与假设同质性的匹配模型相比，它似乎在短期和生命周期内对不同类别工人之间竞争等方面具有更高的分析潜力。然而，例如分割现象等结果并非标准搜索理论得出，并反映了微观层面上影响但具有聚合效应和可能产生意想不到效果的制度的作用。

WorkSim使用一种在经济模型中尚未使用过的强大算法对2011年法国劳动力市场的许多目标进行了校准。它能够很好地复制这些目标以进行一些经济分析。此外，它通常能够很好地甚至非常好地复制不同统计来源和不同类型的测量所测得的总流量。它很好地复制了DMMO（劳动力市场动态观察）所测得的劳动力总流量以及就业调查（Enquête Emploi）计算得出的许多年度转换率。这些统计数据广泛应用于对法国劳动力市场进行分析和辩论。然而，DMMO只提供了一部分流量信息，无法进行存量-流量核算。通过同时拟合DMMO的总流和就业调查的年度转换率，WorkSim揭示了如果将这些转换视为总流速率主体时对移动性估计存在巨大低估问题。我们还表明，就业调查所测得的月度转换（仅适用于新雇佣）仅以边际方式减少了对流量估计值的低估问题。

This article presents a number of preliminary analyzes to characterize the French labor market, on the basis of complete individuals' stock-flow accounts, micro-decisions of heterogeneous agents, and institutions.We have studied several behavioral changes and aggregate shocks through sensitivity variants of some parameters. We show reactions of unemployment which we are able to explain by detailing the economic mechanisms at work in the model. The results may be sometimes unexpected *ex-ante* because of complex interactions. For example, the mean preference for free time and the share of sales revenue retained by the firms before the payment of salaries have a non-monotonic effect on unemployment. The latter has a slight U-shape.

本文通过对完整个体的存量-流量账户、异质主体的微观决策和制度进行分析，对法国劳动力市场进行了初步刻画。我们通过对一些参数的敏感性变化进行研究，探讨了几种行为变化和总量冲击。我们详细说明了模型中起作用的经济机制，以解释失业率的反应。由于复杂的相互作用，结果有时可能出乎意料。例如，对自由时间的平均偏好和企业在支付工资之前保留销售收入的份额对失业率产生非单调效应。后者呈现轻微的U形曲线。

Our results also suggest a **segmentation or dualism between workers**, since some are stable in OEC because the number of dismissals is low, and some are rotating between FDC and unemployment. This dualism persists between the 15-24 years age group and the 25-49 years age group, and even the 50-65 group, so that the paper suggests it is permanent or at least durable, for a fraction of the workers. A fraction of young people do not seem to switch from FDC to OEC
when they get older, contrary to the assumption of a gradual integration mechanism of young people involved by a temporary dualism.

我们的研究结果还表明，工人之间存在一种分割或二元性，因为有些工人在经济活动中保持稳定，解雇人数较少，而有些工人则在非经济活动和失业之间轮换。这种二元性在15-24岁年龄组、25-49岁年龄组甚至50-65岁年龄组之间仍然存在，因此本文认为它是永久的或至少是持久的，适用于部分工人。与假设的年轻人逐渐融入机制相反，一部分年轻人似乎在变老后并不从非经济活动转向经济活动。

Naturally, the key factor is the job creation, and the model reproduces well the massive effect of a sharp increase in aggregate demand on the reduction of unemployment. However, the primary objective of a model of the labor market is to study the effects of structural policies at a given aggregate demand level, although *in fine* some structural policies could influence demand and require to model some feedback mechanism.

当然，关键因素是就业创造，该模型很好地展示了总需求的急剧增加对减少失业的巨大影响。然而，劳动力市场模型的主要目标是研究在特定总需求水平下结构政策的影响，尽管最终一些结构政策可能会影响需求，并需要建立一些反馈机制来进行建模。

## Future Work



Our research program is currently focused on a number of modules (extensions) to be integrated. The first aims to model (endogenously) the choice between FDC and OEC openings made by the firms. This is a complex issue that has not been solved to our sense in a formalized framework. This module will integrate the need for a required minimum level in human capital and training in some jobs and uncertainty on future demand that are fundamental elements in the labor market. Secondly, the choice of contracts will be extended to the temporary help contracts which have become empirically important and are presently included in the FDC, in order to bring into the scene the role of an intermediary in a decentralized market. Thirdly we might need a more detailed analysis of retirement to better analyze the seniors' market. A fourth module will focus on the analysis of careers. The characterization of the labor market requires an understanding of careers notably but not only in order to distinguish temporary segmentation and permanent segmentation. Existing empirical analyzes can serve as a benchmark, but are not able to reproduce full careers in a cohort, due to the lack of individual data over such a long period, and are biased by the changes in the economic environment during the lifetime. The multi-agent modeling seems to be an essential tool in this area, and this is a key reason for their construction, if one want to really understand the nature of the labor markets.

我们目前的研究计划专注于整合多个模块（扩展）。首先，我们旨在通过内生建模来解决企业在FDC和OEC开放之间的选择问题。这是一个复杂的问题，在一个形式化框架中尚未得到解决。该模块将综合考虑劳动力市场中人力资本和培训水平的最低要求以及对未来需求的不确定性等基本因素。其次，我们将扩展合同选择范围，包括临时劳动合同，这在实证上变得越来越重要，并且目前已纳入FDC中，以便在分散市场中引入中介机构的角色。第三，我们可能需要对退休问题进行更详细的分析，以更好地了解老年人市场。第四个模块将专注于职业生涯分析。了解职业生涯对于揭示劳动力市场特征至关重要，尤其是为了区分临时性和永久性分割。现有的实证分析可以作为基准，但由于缺乏长期个体数据并受到经济环境变化的影响，在一个群体中无法完全再现完整职业生涯。多主体建模似乎是这个领域中不可或缺的工具，这也是我们进行构建的一个关键原因，如果我们真正想要理解劳动力市场的本质。

