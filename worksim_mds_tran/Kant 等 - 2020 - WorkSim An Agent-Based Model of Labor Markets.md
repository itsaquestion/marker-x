# Worksim: An Agent-Based Model Of Labor Markets Jean-Daniel Kant1, Gérard Ballot2**, Olivier Goudet**3




## Abstract:



Inthispaper, weprovideanoverviewoftheWorkSimmodel, anagent-basedframeworkdesignedtostudylabor markets. The first objective of this model is to reproduce, within rigorous stock-flow accounting, the gross flows of individuals between important work-states: i.e., employment (distinguishing fixed term contracts and openended contracts), unemployment and inactivity. French legal institutions of the labor market are modelled in some detail and constrain the decisions of the agents on job flows and worker flows. Firms and individuals are heterogeneous and all decisions are taken on the basis of bounded rationality, yet employers as well as workers formimperfectanticipations. Oneimportanttheoreticalnoveltyofthemodelisthatweconsidermulti-jobfirms and shocks on the individual demand of the firms. Employers consider anticipated shocks when they decide on the types of contract. Once the model is calibrated, the secondary objective is to characterize the nature of the labor market under study, and notably the diferentiated roles of the two types of contracts and their impact on unemployment. This is achieved, first by examining the patterns of flows and stocks of labor and secondly by sensitivity experiments, modifying certain exogenous parameters and variables such as total demand. We then use the model as a tool for experimenting labor market policies, including changes in the labor law in France.

本文提供了WorkSim模型的概述，该模型是一个基于主体的框架，旨在研究劳动力市场。该模型的首要目标是通过严格的库存流量核算，在重要工作状态之间重现个体的总流动情况，包括就业（区分固定期限合同和无固定期限合同）、失业和非活动状态。法国劳动市场的法律机构被详细建模，并对主体在工作流和员工流方面做出决策施加约束。企业和个人具有异质性，并且所有决策都是基于有限理性进行的，同时雇主和工人都形成了不完全预期。该模型的一个重要理论创新是考虑到多岗位企业以及对企业个体需求的冲击。雇主在决定合同类型时会考虑到预期冲击。一旦模型校准完成，次要目标是描述所研究劳动力市场的性质，特别是两种类型合同的不同角色及其对失业率的影响。首先通过检查劳动力流动和存量模式来实现这一目标，其次通过敏感性实验来修改某些外生参数和变量（如总需求）。然后我们将该模型用作实验劳动力市场政策的工具，包括对法国劳动法的变更。

Keywords: Agent-Based Model, Agent-Based Simulation, Dual Labor Markets, Anticipations, Calibration, Policy Design

关键词：基于主体的模型，基于主体的模拟，双重劳动市场，预期，校准，政策设计。

## Introduction



1.1
Agent-based methodology ofers a very appropriate tool to model a labor market as a dynamic system of gross flows of workers between the three major states (or stocks) of employment, unemployment and inactivity (also called non participation). It also allows us to study the efects of policies directly on these flows, a much finer analysis than the studies of the efects on the stocks. Such a representation of the labor market has emerged as the most fruitful description to ground an analysis of a labor market since the 1970's and the development of search theory (Phelps et al. 1970), but its implementation remains partial in empirical work because data
on gross flows are only partial1. The move of a worker from one state to another is based on a decision of the
agent or another agent (the employer), not a random process. The agent-based methodology allows us to base heterogeneous agents' decisions on theoretical ground and empirical knowledge about behavior, and then to build bottom up the aggregate flows and the stocks of individuals in diferent states in a natural way. Finally, we simulate all the flows, both measured and unmeasured, to obtain a complete gross flow system. The workers are always in a state of disequilibrium, by at least the efect of experience gained or lost, although they do not move each period. Yet the market as a whole may show an aggregate quasi stability, or on the contrary may display important changes each period in terms of stocks and flows that inform us in the great detail on the labor market outcomes and their changes. In a similar manner to workers, jobs are treated using a stock-flow approach.
1.2
Why can we consider the gross flows approach to labor markets so important as an investigation tool? Firms as agentsmakedecisionsaboutjobcreation, aswellasjobdestruction. Theresultingflowsarethemostimportant
drivers of the labor market. While employers create jobs, these are first vacant and there are further decisions to fill them: workers apply or not, and firms have to decide to select and recruit an applicant, a complex decision. Firms also may cancel an unfilled vacancy, if no adequate workers apply. The gross flows of workers are also an essential element of a labor market. Hires, quits, dismissal for appropriate cause, and dismissals for economic reasons are the sources of employment and unemployment rates. The workers' entry and exit flows determine inactivityrates. Someofthesedecisionsaremadebyworkersalone,andsomedependonthefirms(dismissals), while some require the decisions of two types of agents (hires).2. Using this gross flow methodology, WorkSim has five ofen novel key features.

1.1
基于主体的方法为劳动力市场建模提供了一个非常合适的工具，将其视为就业、失业和非参与（也称为非活跃）这三个主要状态之间的动态流动系统。它还使我们能够直接研究政策对这些流动的影响，这种分析比对状态变化的研究更加精细。自从20世纪70年代以来，这种劳动力市场描述方式已被证明是最有成果的，并且随着搜索理论（Phelps等人，1970年）的发展而得到了广泛应用。然而，由于总体流动数据只是部分可得，实证研究中对此方法的应用仍然存在局限性。工人从一个状态转移到另一个状态是基于个体或其他个体（雇主）的决策，而不是随机过程。基于主体的方法允许我们根据理论和关于行为的经验知识来制定异质主体的决策，并以自然方式自下而上地构建个体在不同状态下的聚合流量和存量。最后，我们通过模拟所有测量和未测量流量来获得完整的总流系统。工人始终处于一种失衡状态，至少受到获得或失去经验的影响，尽管他们并不在每个周期都发生移动。然而，整个市场可能呈现出总体准稳定状态，也可能每个周期都发生重大变化，这些变化以存量和流量的形式详细地告诉我们劳动力市场的结果及其变化情况。类似地，就业岗位也采用了库存-流量方法进行处理。

1.2
为什么我们认为总流方法对劳动力市场的研究工具如此重要？企业作为主体做出了关于创造和销毁就业机会的决策。由此产生的流动是劳动力市场最重要的驱动因素。虽然雇主创造了就业机会，但这些职位首先是空缺的，并且还需要进一步决策来填补它们：工人是否申请，企业是否选择并招聘申请人，这是一个复杂的决策过程。如果没有合适的工人申请，企业也可能取消未填补的职位。工人的总流也是劳动力市场中至关重要的元素。招聘、离职、因适当原因解雇和因经济原因解雇是就业率和失业率的来源。工人的进入和退出流量决定了非活跃率。其中一些决策由工人独自做出，而另一些决策取决于企业（解雇），还有一些需要两种类型的主体（招聘）共同决策。通过采用总流方法，WorkSim具备了五个常见的创新特点。

1.3
A first key feature is the consistency of the gross flows accounting system. The aggregate flows of workers betweendiferentstatesconstituteaconsistentaccountingsystem, whichishoweveropenasyoungworkersenter and older workers retire or die. Similarly, aggregate job flows constitute a consistent accounting system. These two distinct consistent systems of flows are a key and unique feature of WorkSim. A labor market with weak job flows has very diferent implications for workers than a market with high flows, even if unemployment rates are identical. In the former case, workers will stay a long time in their state, so that employed workers will be very stable in their jobs, while the unemployed will have long spells of unemployment. In the second case, unemployment turnover will be high so that the spells of unemployment will be much shorter and job stability lower (but not necessarily low since employment is the dominant stock). The social implications are obvious and policy changes in this paper will show this.
1.4
A second key feature is an elaborate modeling of the creation of jobs by type of contract as an endogenous process. Suchanemphasis, asmentioned, isjustifiedbecausethecreationofjobsisamaindriverofthegrossflows of workers. The decision procedure on this topic will be the most developed of all decisions in this model and includes far more factors and anticipations than has been done until now in the literature. A real labor market contains a mix of long and short term jobs which is crucial to its overall pattern. French firms make an important use of short contracts, Fixed Term Contracts (FTC), beside the permanent contracts, Open Ended Contracts
(OEC)3. The stock of FTC has reached 10% of the employment in 2014. If other non regular employment is included, a ratio of 17% in 2017 is reached, somewhat higher than the EU average4. They also use other contracts,
such as temporary help contracts and apprenticeship contracts, but OEC and FTC are the most important empirically, and FTC can be considered as representing the class of short term contracts, at least as a first step. We
will then only model these two in this version5. The distinction between the two types of employment contracts
is a fundamental extension of the emphasis on job creation as the first driver of the labor market.
1.5
A third key feature is full use of the heterogeneity of agents allowed by the agent-based methodology, by taking into account agents' histories. Agents are endowed with a set of characteristics. As far as individuals are concerned, these characteristics most ofen evolve over a life cycle, such as experience and wage and for a given state in which they are in, influence their decisions, or the employer's decision about them. The heterogeneity allows us to build up flows accounting for diferent levels of aggregation. This yields a better understanding of outcomes of the labor market in terms of status and flows for major interest groups such as gender, age class,
broad occupational level. Moreover, for a cohort with a specific set of characteristics at start, average career trajectories can be computed over the reference experiments and diferent policy experiments. Firms are also heterogeneous agents, notably by size.
1.6
A fourth key feature is the possibility to model institutions which we define in the legal sense, notably labor laws and the minimum wage, which are crucial to the labor market. Institutions influence or even constrain the decisions at the micro level, and agents are heterogeneous in their characteristics or status and afected
diferently. The labor law (*Code du Travail*) is complex in France, yet our emphasis on contracts has allowed us
to be precise on the rules which govern them (without taking into account particular cases unlikely to afect the main outcomes).
1.7
Here, we list these legal rules that govern the two types of labor contracts, to make clear what we mean by modellinginstitutions. FortheOEC, nodurationlimit, longprobationaryperiod, nolegalseverancepayduring the first year, no termination costs if quitting, variable firing costs when firing. The main *FTC* features are the following: maximum total duration of 18 months including the possibility to be renewed once, a grace period afer the termination of the contract during which the employer cannot fill the job, a small probationary period,
an allowance at the end of the contract proportional to the total gross salary over the contract6. It cannot be
broken without heavy penalties (paying the remaining salary part). The firms, in the present and new version of WorkSim, choose the mix of the two contracts on the basis of their anticipated global needs in manpower
under several scenarios and the knowledge of the legal rules mentioned7. The model is therefore a completely
novel theoretical economic analysis of the determinants of the choice between contracts independently of the methodology (analytic or computer based), hence a more comprehensive explanation of dualism in the labor market and a basis for policy.
1.8
In an aggregate model with a representative agent, institutions afect all agents of one type in an identical way. Moreover, agents' responses to institutional change should depend on their present idiosyncratic characteristics, which difer along many dimensions. Heterogeneous agents also interact within their own class (for instance within a household). Aggregate models then do not allow to study the influence of institutions on agents' decisions in a realistic way. The combination of heterogeneous agents' decisions and legal institutions
constitute the specific foundations of WorkSim, which enable us to study the complexity of the labor market as a system, once the choice of a gross flows methodology has been adopted. Those policy experiments which modify institutions can be studied in an adequate way with diferentiated impact at the agent level, and differentiated responses. Non-linear consequences of policy or behavioral changes, and notably crowding-out efects of workers with certain characteristics appear, which are ofen important in labor markets, and are the source of major distributional changes in terms of unemployment. Ex-ante, the study of the efects of the El Khomri law, voted in 2016, a law which has alleviated the justifications for economic dismissals required, will bring a clear example of the important distributional and other non-linear changes in the labor market (see Section 4.21 below).
1.9
A fifh key feature is the calibration of the model on a large set (63) of aggregate or group level target variables, notably stocks and flows of workers, for the most recent year for which we have many data, 2014, and assuming a steady state. The calibration also uses a large number of parameters (56) and a powerful algorithm. This methodology looks as novel in economics.
1.10
The model has some additional important characteristics. Agents are autonomous and there is therefore no need for an auctioneer, in contrast to orthodox models, which use a matching function with the numbers of
vacant jobs and unemployed as inputs8. In WorkSim, agents take decisions based on their own information,
the calculation of expected costs and benefits and the expected profit (for the firms) or expected utility (for the individuals) for each decision they can take. The environment is very complex and dynamic because of the institutions and agents' interactions, and the agents' rationality is bounded in the sense of Simon (1956). Therefore, when in any given state, an agent chooses the best of a few possible discrete solutions (see below for examples) under limited information, and rules simpler than optimization as in analytic search models. Agents make mistakes when deciding, (as they would also do ex-post by optimizing), but in WorkSim, they can learn and improve their decisions in the future, if events have not changed their status.
1.11
As previously mentioned, we have chosen to focus on labor market institutions, but we also wanted to model individual decisions to enter or exit the labor market. In other words, the gross flows between the inactivity state and the employment and unemployment states, since they appear to us as essential to a complete system of flows and a deep understanding of the labor market. Interactions within the household influence such decisions, otherwise members of a household could not choose to be inactive, as they would not obtain any unemployment benefits, and ofen no welfare, because the latter is not universal in France. Individuals' decisions are influenced by the earnings of the partner and the benefits the household may have. To take this into account, we had to implement a full demographic module. Institutions and the demographic module, as well as modelling the many decisions of firms and individuals, are sizable blocks. We therefore limited the model to
the labor market, with an exogenous aggregate demand for the good.
1.12
We then assume that *each firm faces stochastic shocks on its demand share*, which can be seen as fluctuations
of consumers' preferences for its good. The exogeneity of demand means that the model cannot represent the feedback of the distributed wages on the consumption if they change. However, first even if such a macroeconomic loop were added, the specific efects of profits on investment and the macroeconomic consequences would not appear without also adding capital, R&D and innovation, which imply the development of a financial sector. These are major extensions, and it is wise to build such a macroeconomic model by steps. Secondly, the choice of a stable aggregate demand has its own advantage, by allowing us to fit the model to the most recent year for which we have detailed data (2014). New and more complex methods would have to be designed and more data collected to calibrate a dynamic extension of the model because it would imply fitting it on time series. Themodelcapturesthesteady-stateefectsofinstitutionsandagents'behavioralrulesonthelabormarket outcomes, and important variables such as unemployment. Yet, WorkSim in the present version should be seen more as aiming to analyze the structure of the labor market, with an emphasis on the possibly divergent outcomes on some main workers' groups, and distributional policy efects, than as an analysis of the aggregate unemployment changes under behavioral or institutional changes which would require a full agent-based macroeconomic model.

1.3
第一个关键特点是保持总流计算系统的一致性。不同州之间工人的总体流动构成了一个一致的会计系统，但随着年轻工人进入和老年工人退休或去世，这个系统是开放的。同样，总体就业流动也构成了一个一致的会计系统。这两个独立但一致的流动系统是WorkSim的关键和独特特征。即使失业率相同，在就业流动较弱的劳动力市场中，对工人产生的影响与流动较高的市场截然不同。在前一种情况下，工人将在当前状态中停留很长时间，因此就业工人在他们的工作中非常稳定，而失业者将有长时间的失业期。而在后一种情况下，失业率变动较大，因此失业期将更短，并且就业稳定性较低（但并不一定低，因为就业是主导存量）。这些社会影响显而易见，并且本文中所提出的政策变化将证明这一点。

1.4
第二个关键特点是将按合同类型创造就业机会建模为内生过程。正如前面提到的那样，这种强调是有道理的，因为创造就业机会是劳动力总流的主要驱动因素。在这个主题上的决策过程将是模型中所有决策中最复杂的，并且比

## Main Lines Of The Theoretical Framework



1.13
Agents' decisions are grounded on the concept of *search*. However, the latter is extended in important ways and
the formal apparatus uses calculus procedures under bounded rationality, since the heterogeneity of agents and a detailed modelling of firms' anticipations preclude the use of the analytic equilibrium methodology common to the search models (Phelps et al. 1970). Search Theory considers how economic actors find a partner for their transactions (here workers looking for a job in a company, and employers a worker for a vacant job)9. In WorkSim, the basic concept of search is developed in several directions, some new. The rationale is first, to build the complete framework of job and workers' flows that is needed and secondly, to provide a new and detailed explanation of the choice of contracts by the employers, in order to make some policy experiments:

1.13
主体的决策基于“搜索”概念。然而，由于主体的异质性和对企业预期的详细建模，无法使用搜索模型中常见的分析均衡方法（Phelps等，1970），因此在有界理性下采用了微积分程序。搜索理论研究经济行为者如何找到他们交易的合作伙伴（例如工人在公司寻找工作，雇主寻找空缺职位的工人）9。在WorkSim中，对搜索的基本概念进行了多个新方向的发展。首先是为了构建所需的完整就业和劳动力流动框架，其次是为了提供关于雇主选择合同的新而详细的解释，以进行一些政策实验。

1. *Matching emerges from bilateral meetings on a decentralized labor market*. Both sides select and can prefer no match other than a poor one. Employers post vacant jobs with a contract and a wage and workers apply for these jobs (or not). Employers select among those who are high in productivity distribution. However, they would prefer to keep a job vacant than hire a worker with poor productivity, because of hiring and termination costs. A stopping rule in the form of a minimum productivity requirement or hiring standard is computed. Moreover, agents have an imperfect evaluation of the future match value: workers do not know the amenity of the job (conditions of work) before being hired, and the employer has an imperfect information on the worker's productivity. No aggregate matching function is then used, in opposition to the matching models now dominant in search theory (Mortensen & Pissarides 1994). An aggregate matching function introduces a fictitious intermediary on the labor market, and has weaker microeconomic foundations than our sequential double search framework, which can cope with heterogeneity and informational diferentiation10. Moreover, matching function models are not robust to large
changes in the labor market and do not reproduce the crowding out efect afecting some categories of
workers11.
2. *Firms are multi-jobs*. This is new to the search literature and is a major feature key to the contribution of our model to the analysis of the employers' choices between the two types of contracts. We consider that shocks are on the demand of the firm, a realistic assumption, rather than on individual job productivity, as in the search literature. The firm faces a yearly idiosyncratic random trend (on its share of the market), and random weekly variations around that trend. The employer forms anticipations on future demand and, if the present demand rises, takes into account future cost and benefits of each type of contract before deciding to create a job. If employers forecast a demand fall, they prefer to create short FTC, since they will pay the worker only on the fixed term and so not lose much money. On the other hand, economic dismissals of OEC take delays (ofen a year or more) caused by the labor law and jurisprudencegenerating hoardingcostsandalsoinduceseverancepay. HencehiringFTCcanbeagoodchoiceforanemployerwho is uncertain about her future demand. However, FTC have their own problems such as limited renewal under the French law and a partial amortization of training costs. Considering firms with multiple jobs and demand shocks then makes it possible to model the choice by each firm of a profitable mix of the two types of contracts. Productivity changes in each job-worker match are modeled as improvements in workers' productivity, which is based on general experience and on-the-job learning with seniority.

1. *分散劳动力市场中的双边会议导致匹配产生*。双方都可以选择，并且可以偏好除了差劲之外的任何匹配。雇主发布带有合同和工资的空缺职位，工人申请这些职位（或者不申请）。雇主从那些在生产力分布中较高的人中进行选择。然而，由于招聘和解雇成本很高，他们宁愿保持一个空缺职位，也不愿雇佣生产力差的工人。我们计算了一个最低生产力要求或招聘标准作为停止规则。此外，主体对未来匹配价值有着不完善的评估：在被雇佣之前，工人不知道工作环境如何；而雇主对工人的生产力了解也不完善。与现在在搜索理论中占主导地位的匹配模型相反，并没有使用总体匹配函数。总体匹配函数引入了劳动市场上虚构的中介机构，并且其微观经济基础比我们顺序双重搜索框架要弱一些，后者可以处理异质性和信息差异10. 此外，匹配函数模型对劳动市场的大规模变化不具有鲁棒性，并且无法重现影响某些类别工人的挤出效应11。

2. *公司具有多个职位*。这在搜索文献中是新的，也是我们模型对雇主在两种类型合同之间选择进行分析的一个重要特征。我们认为冲击发生在公司需求上，这是一个现实的假设，而不是发生在个体工作生产力上，就像搜索文献中一样。公司面临着年度特异性随机趋势（关于其市场份额），以及围绕该趋势的随机周变动。雇主对未来需求进行预测，并且如果当前需求增加，则在决定创建一个职位之前考虑到每种类型合同的未来成本和收益。如果雇主预测到需求下降，他们更倾向于创建短期合同，因为他们只需要支付固定期限内的工资，因此损失较少。另一方面，经济解雇OEC需要遵守法律和司法程序所导致的延迟（通常为一年或更长时间），从而产生滞留成本，并引起赔偿费用。因此，在对自己未来需求不确定时，雇主选择雇佣FTC可能是一个不错的选择。然而，FTC也有自己的问题，例如在法国法律下续签受限和培训成本的部分摊销。考虑到具有多个职位和需求冲击的公司，可以对每个公司选择两种类型合同的盈利组合进行建模。我们将每个工作-工人匹配中的生产力变化建模为工人生产力的改进，这基于一般经验和在职学习以及资历。

This is a non-random mechanism (as opposed to the standard search model assumption). We add an assumption of (real and nominal) downward wage rigidity to shocks (a known feature of the French labor market), which means that an employer does not solve a demand shock by lowering the wages of the incumbent workers. A justification based on the theory of eficiency wages can be invoked to give microfoundations (Shapiro & Stiglitz 1984).However entry wages are flexible to the labor market conditions, an assumption based on empirical studies such as Martins et al. (2012), which is compatible with the rigidity of incumbents' wages. The individual wage then increases on human capital accumulation. The multijobs feature induces the employer to take into account her stock of FTC when deciding on the creation of a new job, since FTC are a bufer against uncertainty. In the existing models, the firms have one job, it precludes to model in a realistic way the role of uncertainty and other factors on the mix of the two types of contracts. Moreover, the uncertainty concept has lead us to introduce subjectivity in forecasting, in the line of Tversky & Kahneman (1979), and Akerlof & Shiller (2009), a concept which also appears to be very relevant to job creation decisions, since it opens the way to the integration of employers' anticipations on the business cycle (lef for future work).

这是一个非随机机制（与标准搜索模型假设相反）。我们在冲击中增加了（实际和名义）工资下行刚性的假设（这是法国劳动市场的一个已知特征），这意味着雇主不会通过降低现有员工的工资来解决需求冲击。可以引用效率工资理论为此提供微观基础（Shapiro＆Stiglitz 1984）。然而，入职工资根据劳动力市场条件具有灵活性，这是基于Martins等人（2012）等经验研究的假设，与现任员工薪水的刚性相一致。随后，个体工资随着人力资本积累而增加。多职位特征使雇主在决定是否创建新职位时考虑到其FTC库存，因为FTC对不确定性起到了缓冲作用。在现有模型中，公司只有一个职位，无法以真实方式对两种类型合同的组合进行建模以反映不确定性和其他因素的作用。此外，不确定性概念使我们引入了预测中的主观因素，在Tversky＆Kahneman（1979）和Akerlof＆Shiller（2009）等研究的基础上，这个概念在就业创造决策中也非常相关，因为它为雇主对商业周期的预期提供了整合的途径（留待未来工作）。

3. The search concept is extended and integrated in most other decisions on the labor market, which involve
more than search costs. First, workers take other voluntary decisions than applying for a job, such as quits
and on-the-job search (i.e., looking for a new job while remaining employed). Search calculus in terms of utility is also done about decisions of entry and exit of workers, but we have included some elaborate features such as taking into account the psychological cost of starting to search, and the total income of the household. The latter assumption brings non-market interactions between individuals (see below), an important topic in labor economics, yet one which cannot be treated by models based on representative
agents. Secondly, firms also take into account the search costs of replacement when they consider firing a worker for lack of productivity. Demand shocks and workers' productivity changes allow us to explain the disequilibria and flows at the microeoconomic level. Demand shocks explain job creations and hires, part-time, economic dismissals, while productivity changes explain personal dismissals, promotions and transformations of FTC into OEC, since FTC can be also used as screening devices.

3. 在劳动力市场上，搜索概念在大多数其他决策中得到了扩展和整合，这些决策涉及除了搜索成本之外的其他因素。首先，工人会做出一些自愿的决策，比如辞职和在职搜索（即在保持就业状态下寻找新工作），而不仅仅是申请工作。我们还对工人的入职和离职决策进行了效用方面的搜索计算，但我们还考虑了一些复杂的特征，比如考虑开始搜索的心理成本和家庭总收入。后一种假设引入了个体之间的非市场互动（见下文），这是劳动经济学中一个重要的主题，但不能通过基于代表性主体模型来处理。其次，在考虑因为生产力不足而解雇员工时，企业也会考虑到替换的搜索成本。需求冲击和员工生产力变化使我们能够解释微观经济层面上的失衡和流动情况。需求冲击解释了就业创造和招聘、兼职、经济裁员等现象，而生产力变化则解释了个人裁员、晋升以及将FTC转化为OEC的情况，因为FTC也可以用作筛选设备。

## Search Models And The Dual Labor Market



1.14
All these features put together yield a coherent search model which difers very deeply from existing models, andismoreusefultounderstandunemployment,aswellasthemechanismsofdualismonthelabormarketand its persistence. Only recently search theory has started to integrate dualism. The model by Cahuc et al. (2016) appears to be the first, and up to the writing of the present paper, the only one to fully endogenize the choice
between temporary and permanent contracts12. They introduce the cost of paying the total remaining salary in
case of termination of temporary contract before the contracted end date. It yields the needed trade of to the firing costs for permanent jobs, without which employers should always prefer FTC. However, they assume that eachjobisanindependentprojectwithanexpectedduration. ThentheemployerchoosesFTCforshortprojects and OEC for long projects. The duration of FTC contracts is endogenous. The advance termination cost of FTC does not appear to us as substantial enough to explain that most jobs are OEC. If there is a trade-of, it is rather based on the impossibility to amortize substantial training costs on short contracts, to which one could add the building of trust for many jobs, and long on-the-job learning for complex jobs. Moreover, the independence of the expected duration of jobs in the Cahuc et al. (2016) model does not characterize the demand uncertainty that firms undergo in the real world. As mentioned above and modeled in WorkSim, firms anticipate shocks on their total demand for a good. They respond by choosing a mix of the two types of contracts according to a complex trade-of which takes into account dismissals costs on OEC, vacancy costs, training costs, renewal limitations on FTC and associated costs, as well as the current mix of OEC and FTC, with current FTC as a bufer for the current and future OEC. The duration of FTC is endogenous as in Cahuc et al. (2016). This comprehensive framework of the relative costs of the two contracts requires multi-jobs firms and therefore a profound change in search theory that we propose. Moreover it retrieves the spirit of the seminal dual labor markets model of Rebitzer & Taylor (1991) which is based on total demand uncertainty. The employer divides its employment into temporary and permanent jobs, but the model has an aggregate nature, and no search framework (no unemployment in the model). It also assumes among strong assumptions, diferent wages between FTC and OEC as well as the necessity of monitoring workers to deter them from shirking, and these assumptions are not needed in our model.

所有这些特征的综合构成了一个连贯的搜索模型，与现有模型有着深刻的差异，并且更有助于我们理解失业以及劳动力市场的二元性和持久性机制。最近，搜索理论开始融合二元性。Cahuc等人（2016）提出的模型似乎是第一个也是目前唯一一个完全内生化临时合同和永久合同选择的模型。他们引入了在临时合同约定结束日期之前解雇所需支付剩余工资的成本。这为永久工作岗位上的解雇成本提供了必要的交换条件，否则雇主应该总是更倾向于使用固定期限合同（FTC）。然而，他们假设每个工作岗位都是一个独立项目，具有预期持续时间。然后雇主选择短期项目使用FTC，选择长期项目使用永久合同（OEC）。FTC合同的持续时间是内生化的。然而，对我们来说，FTC提前终止成本似乎不足以解释为何大多数工作岗位采用OEC。如果存在权衡考虑因素，则更可能基于无法在短期合同上摊销大量培训成本、许多工作岗位的信任建立以及复杂工作的长期在职学习。此外，Cahuc等人（2016）模型中预期持续时间的独立性并不能刻画企业在现实世界中面临的需求不确定性。正如前面提到并在WorkSim模型中建模，企业预测其对某种商品的总需求会发生冲击。他们通过选择两种类型合同的组合来应对这些冲击，这种组合考虑了OEC上的解雇成本、空缺成本、培训成本、FTC续约限制及相关成本，以及当前OEC和FTC的混合情况，其中当前FTC作为当前和未来OEC的缓冲。与Cahuc等人（2016）一样，FTC合同的持续时间是内生化的。这个关于两种类型合同相对成本的全面框架需要多岗位企业，并因此需要我们提出一个对搜索理论进行深刻改变的框架。此外，它恢复了Rebitzer和Taylor（1991）经典双重劳动市场模型中基于总需求不确定性而建立起来的精神。雇主将其就业分为临时工作和永久工作，但该模型具有整体性质，在模型中没有搜索框架（没有失业）。它还假设了一些强假设，如FTC和OEC之间的不同工资以及监督工人以防止他们偷懒的必要性，而我们的模型不需要这些假设。

## Related Agent-Based Models



1.15
WorkSim takes place in a multi-agent literature on labor markets, which has a long history, but remains underdeveloped compared to other fields in agent-based economics. Bergmann (1974) is probably the first to have developed a simple search model with both sides of the market and obtained simultaneously vacant jobs and unemployment, reproducing the imperfect matching by a labor market. Eliasson (1977) has built a macroeconomic agent-based model, MOSES, which has Keynesian, Schumpeterian and Wicksellian foundations and contains a labor market, even though workers do not appear as individual agents. Entry and exit of firms, and process R&D (incremental and radical) are the Schumpeterian factor and influence unemployment. Entry has an important positive influence on growth. Extensions introduce skills through training investment. Firms can raise wages to poach skilled labor from other firms (Ballot & Taymaz 1997) and competition is then not only on goods markets but also through wages. ARTEMIS (Ballot 1981, 2002), the forerunner of WorkSim, is based on search decisions by individuals and multi-jobs firms. It is the first multi-agent model to have modeled the gross flows of individuals between the three main states (employment, unemployment, and inactivity), with the addition of on-the-job search.
1.16
This is achieved within an institutional framework distinguishing contracts, notably with some workers in OEC in internal labor markets, other workers in OEC without careers, termed secondary, and others in a temporary help firm. The model generates a temporary segmentation of the young workers, which has been since shown to be an important feature of the French labor market (see for instance Le Barbanchon & Malherbet (2013)). Then, anegativedemandshock(thefirstoilshock)afectsonlyslightlythemaleworkersofprimeageinOECbut crowdsouttheothercategoriesoflabor, suchaslowskilledandfemales, and,beyondtemporarysegmentation, precludes the progressive integration of some of the young workers in the internal labor markets. This result
corresponds to the real efects of this oil shock which has strongly influenced the rise of the dualism in France with for individuals lifecycle consequences13.

1.15
WorkSim是在劳动力市场多主体文献中进行的研究，该领域的发展相对于其他基于主体经济学的领域而言尚不充分。Bergmann（1974）可能是最早开发了一个简单的搜索模型，同时考虑了市场两侧，并同时得出了空缺职位和失业情况，从而模拟了劳动力市场上的不完全匹配。Eliasson（1977）构建了一个宏观经济学基于主体的模型MOSES，该模型具有凯恩斯、熊彼特和维克塞尔等理论基础，并包含一个劳动力市场，尽管工人并不以个体主体出现。公司的进入和退出以及过程性研发（增量和根本性）是熊彼特因素，并影响失业率。公司进入对经济增长有重要积极影响。扩展模型通过培训投资引入技能要素。公司可以提高工资来挖走其他公司的技术劳动力（Ballot＆Taymaz 1997），竞争不仅仅存在于商品市场上，还通过工资水平展开。ARTEMIS（Ballot 1981, 2002）是WorkSim的前身，它基于个人和多岗位公司的搜索决策。它是第一个多主体模型，对个体在就业、失业和非活动三种主要状态之间的总流动进行了建模，并引入了在职搜索的概念。

1.16
该模型在一个机构框架内进行，区分了不同类型的合同，特别是一些OEC内部劳动力市场中的工人，其他没有职业生涯的OEC工人（称为次要工人），以及临时劳务公司中的其他工人。该模型产生了年轻工人的临时分割现象，这在法国劳动力市场中被证明是一个重要特征（例如参见Le Barbanchon＆Malherbet（2013））。然后，负面需求冲击（即第一次石油危机）仅对OEC中年龄适中男性工人产生轻微影响，但挤出了其他类别的劳动力，如低技能和女性，并且除了临时分割现象外，还阻碍了一些年轻工人逐步融入内部劳动力市场。这个结果反映了石油危机对法国产生的实际影响，在法国强烈影响双重结构崛起，并对个体产生终身影响13。

1.17
With the 2000's we have seen some multi-agents models of the labor market aiming at theoretical research (see Neugart & Richiardi (2018) for a review). The introduction of networks is a progress compared to random search insomecontexts(Pingle&Tesfatsion2004;Tassier&Menczer2001). Ifmassivemicrodatabecomeavailable,this
approach may give a better understanding of the labor market flows for segments of the workforce. Richiardi (2004) has modeled in more detail than before the matching process between workers and firms with on-thejob search, entrepreneurial decisions and endogenous wage determination. Neugart (2008) has developed an agent-based labor market model with sector-specific skill requirements. Barlet et al. (2009) have simulated the French labor market for the year 2006, appearing as the closest empirical work to ours. They distinguish individuals and jobs, but not firms as such, although there is a labor demand side, with creation and destruction of jobs based on a desired margin and demand. Moreover, calibration by indirect inference is done. However, the most active agent-based field of research is not focused on the development of detailed labor markets models, but on building compact labor market modules in macroeconomic agent-based models, in order to experiment with alternative specifications of a very limited set of institutional and behavioral rules (unemployment benefits, wage flexibility), and examine the aggregate efects on the whole economic system. Then the models are not calibrated to fit data for a specific country, but look for validation through the obtention of stylised facts.
1.18
Fagioloetal.(2004)donotproposeafullmacroeoconomicmodel, butputaloopbetweenwagesandconsumption, and introduce process innovation to allow for GDP growth. The labor market is represented by a simple decentralised process to match workers and jobs, with some bargaining in the wage setting. The authors investigate two alternative behaviors when firms decide to open jobs (with dependence on past profits or not) and two for workers (trying to be reemployed by the same firm in last period or performing a random search). Combinations define two regimes, the Walrasian regime, and an Institutionally shaped regime (dependence of job openings on past profit and loyalty of workers). They show that some main stylised facts as the Beveridge, Wage and Okun Curves appear simultaneously only in the Institutionally shaped regime14. The K+S model by Dosi et al. (2010) emphasizes the interaction of Keynesian demand factors with innovation (the Schumpeterian dimension) modeled as endogenous R&D to understand growth and business cycles. It has been the stepping stone for macroeconomic models which extend to new parts of the economic system and are more and more complete. Dosi et al. (2020) summarized recent work carried out with a labor market module. The labor market isdecentralisedbutremainscenteredonhiresandfiresasfarasflowsareconcerned. Thefocusisagainoncomparing alternative regimes, namely a Fordist and a Competitive regime. In the Fordist regime, fires are allowed only when losses are incurred as is the case in WorkSim (before the El Khomry law studied below) and more flexible firing rules are studied in the Competitive regime. Many stylised facts are obtained at the microeconomic and the aggregate level. However, the list given by the authors (in their Table 3) makes it clear that almost all do not focus on the labor market detailed outcomes, and notably the competition between categories of workers. Finally, theEURACEmodelisamacroeconomicandstock-flowconsistentmodelwhichcontainsadecentralised labor market module. The model displays a number of macroeconomic stylised facts for a prototype European economy. Dawid et al. (2013, 2018) analyze a system of two regions with diferent or identical labor regimes (rigidity versus flexibility) to analyze convergence and inequality.

1.17
随着2000年代的到来，我们见证了一些劳动力市场的多主体模型，旨在进行理论研究（有关综述，请参阅Neugart和Richiardi（2018））。与某些情况下的随机搜索相比，引入网络是一种进步（Pingle和Tesfatsion，2004；Tassier和Menczer，2001）。如果能够获得大规模的微观数据，这种方法可能更好地理解劳动力市场对不同劳动力群体流动的影响。Richiardi（2004）对工人与企业之间的配对过程进行了比以往更详细的建模，并考虑了在职搜索、创业决策和内生工资决定等因素。Neugart（2008）开发了一个基于主体的劳动力市场模型，其中考虑到了特定行业技能要求。Barlet等人（2009）对法国2006年劳动力市场进行了模拟研究，其结果与我们的研究最为接近。他们区分个体和就业岗位，但没有像公司那样区分企业本身，尽管存在一个劳动需求方面，在所需边际和需求基础上创建和销毁就业岗位。此外还进行了间接推断的校准。然而，目前最活跃的基于主体的研究领域并不专注于开发详细的劳动力市场模型，而是在宏观经济基于主体的模型中构建紧凑的劳动力市场模块，以便尝试使用一组非常有限的制度和行为规则（如失业救济、工资灵活性）进行实验，并研究对整个经济系统的总体影响。因此，这些模型并不是通过校准来适应特定国家的数据，而是通过获得程式化事实来验证其有效性。

1.18
Fagiolo等人（2004）没有提出一个完整的宏观经济模型，但他们建立了工资和消费之间的循环关系，并引入了过程创新以实现GDP增长。劳动力市场通过一个简单的分散过程来表示工人和就业岗位之间的匹配，并在工资设置中进行一些讨价还价。作者研究了两种替代行为：企业决定开设职位时是否依赖过去利润以及工人选择尝试被上一期同一公司重新雇佣或进行随机搜索。这些组合定义了两种制度：Walrasian制度和机构塑造制度（职位开放取决于过去利润和员工忠诚度）。他们表明，只有在机构塑造制度下，一些主要的程式化事实，如贝弗里奇曲线、工资曲线和奥肯曲线才会同时出现14。Dosi等人（2010）的K+S模型强调凯恩斯需求因素与创新（熊彼特维尔维尔维尔维尔维尔）的相互作用，并将内生研发建模为理解增长和商业周期的关键。该模型成为了宏观经济模型的基础，逐渐扩展到经济系统的新领域，并变得越来越完善。Dosi等人（2020）总结了最近进行的带有劳动力市场模块的研究工作。劳动力市场是分散的，但在流动方面仍然集中在招聘和解雇上。重点再次是比较不同制度，即福特主义制度和竞争制度。在福特主义制度中，只有在遭受损失时才允许解雇，这也是WorkSim（以下将对其进行研究）中所发生的情况，并且竞争制度中研究了更灵活的解雇规则。可以得到许多微观和宏观层面上的程式化事实。然而，作者给出的列表（在他们的表3中）清楚地表明，几乎所有这些研究都不关注劳动力市场的详细结果，尤其是不同类别工人之间的竞争。最后，EURACE模型是一个宏观经济和库存流量一致性模型，其中包含一个分散式劳动力市场模块。该模型展示了原型欧洲经济的许多宏观经济程式化事实。Dawid等人（2013, 2018）分析了两个具有不同或相同劳动制度（刚性与灵活性）的地区系统，以分析收敛和不平等问题。

1.19
WorkSim and these macroeconomic models are not opposed models of the labor market, and in the future, they may converge. Yet first, they currently have diferent interests. The macroeconomic models formalise some features of the labor market only in order to integrate its interactions with the other parts of the economy to analyze the aggregate outcomes. WorkSim aims at a better understanding of the dynamics of the detailed flows and stocks of the main categories of workers interacting in a fairly precisely defined institutional environment. To give anexample, Dosiet al.(2020)study broadalternatives infiring laws(only FTC,no firing). Although theoretically interesting, these are much too radical alternatives to study historical policy changes in a country and especially in France, where they are ofen marginal for political and sociological reasons. Modifying the French labor law just to make economic dismissals possible afer one, two, three, or four quarters of diminishing turnover instead of losses during one year has meant a semester of major demonstrations and strikes in France in 2016 as well as the dislocation of the socialist majority in parliament. Yet we will show that the "small" changes of the El-Khomri law have large distributional efects since they afect the gross flows in a major way and the age classes in an opposed manner.
1.20
Secondly, our detailed analysis leads us to theoretical developments that are specific to our model. The modelling of a large number of decisions on the labor market for each agent requires a unified treatment of costbenefit outcome for each of these agents. This is why we have adopted a utility function with idiosyncratic weights for each individual in order to aggregate incomes and free time, with search costs and other variables. Individuals have a bounded rationality, yet they know what trade of they accept between income against free
time, when these play a role in their diferent decisions. The utility function acts simply as an aggregator of two needs, and it enables the individual to decide between discrete choices, not to choose the values that maximize the utility. In the same manner, an employer has a unique profit function which applies to all her decisions, but also ofen faces discrete choices such creating a job or not, hiring a candidate or not. The profit criterion then acts as part of a rule of decision.

1.19
WorkSim和这些宏观经济模型并不是劳动力市场的对立模型，未来它们可能会趋于一致。然而，首先，它们目前有不同的利益。宏观经济模型仅仅为了将劳动力市场与经济其他部分的相互作用整合起来，以分析总体结果而形式化了劳动力市场的一些特征。WorkSim旨在更好地理解在一个相当明确定义的制度环境中相互作用的主要工人类别之间详细流动和存量的动态。举个例子，Dosiet等人（2020）研究了解雇法律（仅限固定期限合同、无解雇）。尽管从理论上来说很有趣，但这些选择对于研究一个国家乃至法国历史政策变化来说都太过激进，并且由于政治和社会原因，在法国通常边缘化。修改法国劳动法以使经济性解雇在一年内损失减少一个季度、两个季度、三个季度或四个季度后成为可能，在2016年导致了法国半年时间里大规模示威和罢工，并导致社会党在议会中的分裂。然而，我们将展示El-Khomri法律的“小”变化对分配产生了重大影响，因为它们在很大程度上影响了总流动和年龄类别。

1.20
其次，我们详细的分析导致了特定于我们模型的理论发展。对于每个主体在劳动力市场上做出的大量决策建模需要统一处理每个主体的成本效益结果。这就是为什么我们采用了一个具有各自权重的效用函数来汇总收入和空闲时间，并考虑搜索成本和其他变量。个体具有有限理性，但他们知道在不同决策中收入与空闲时间之间所扮演的角色时可以接受什么样的权衡。效用函数只是两种需求的聚合器，并使个体能够在离散选择之间做出决策，而不是选择最大化效用值。同样地，雇主拥有一个适用于她所有决策的唯一利润函数，但也经常面临离散选择，比如是否创造一个工作岗位、是否雇佣候选人等等。利润准则则作为决策规则的一部分起作用。

1.21
Finally, unlike the models surveyed and in part because the model is detailed, the empirical focus is very different. The validation goes through calibration by an algorithm on a large number of real labor market variables, rather than by obtaining macroeconomic regularities. Some of the latter are not always present in historical time (for instance the Phillips curve, or the Beveridge curve which may be flat or rising through structural change).
1.22
The paper is organized as follows: In Section 2, we describe the main features of the model. In Section 3, we presentourvalidationmethod—throughcalibration—andinSection4abriefcharacterizationofthesimulated French labor market and some simulation experiments. We will show how WorkSim can be used to assess labor
policies*ex-ante*aswellas*ex-post*, includingthe2016"ElKhomrilaw"thatgeneratedveryhotpoliticalandunion
strugglesin Franceaswellasvividdebatesamongeconomists. Section5willconcludeandopenthediscussion.

1.21
最后，与调查的模型不同，该模型因其详细性而具有独特的实证重点。验证过程通过对大量真实劳动力市场变量进行算法校准来完成，而非通过获取宏观经济规律。其中一些规律在历史时间中并不总是存在（例如菲利普斯曲线或贝弗里奇曲线可能会在结构性变化中平坦或上升）。

1.22
本文的结构如下：第2节描述了模型的主要特点。第3节介绍了我们的验证方法-通过校准，并在第4节对模拟的法国劳动力市场进行了简要描述以及一些模拟实验。我们将展示WorkSim如何用于前瞻性和事后性评估劳动政策，包括2016年引发法国政治和工会激烈斗争以及经济学家之间激烈辩论的“El-Khomri法律”。第5节将总结并展开讨论。

## Model Description The Agents In Worksim



2.1
There are two types of agents: *Private Firms* and *Individuals*. At its creation, each firm starts with at least one
worker to run the company, representing the *managing director*15. The *Individuals* are grouped in households
and the simulation evolves in a stationary population. The individuals can marry each other, have children and therefore the decisions of one member of the household may have an impact on the other members. In WorkSim, the agents are heterogeneous. They have specific attributes determined once and for all at their creation (e.g., gender, amenity,...) and internal variables (e.g., age, salary, number of employees,...) that evolve throughout the simulation.
2.2
The agents under 15 or over 65 years belong to the households but are not *instantiated* as full agents and do not take decisions in the model. However, these *non-instantiated agents* indirectly participate through the economic decisions of the other members of the household (e.g., the number of dependent children is taken into account in decisions of transition to inactivity, the retirement pension is included in household income). The individuals under 15 years become full agents in the model at the age of 15, and some remain in the school system
while others enter the labor market. Finally, the *period* corresponds to *a week*, in order to capture very short
spells on many FTC, and be as close as possible to real gross flows. 46% of all hires are on Fixed-Term Contracts
that last one week or less in 2010 (ACOSS 2011).

2.1
主体可以分为两种类型：私营企业和个人。每个企业在创建时至少有一个工人来担任经营者，即董事长。个人被组织成家庭，并且模拟中的人口是稳定的。个人可以结婚、生育子女，因此家庭成员的决策可能会对其他成员产生影响。在WorkSim中，主体是异质的，它们具有一次性确定的特定属性（例如性别、便利设施等），以及随着模拟过程发展而变化的内部变量（例如年龄、工资、雇员数量等）。

2.2
年龄在15岁以下或65岁以上的主体属于家庭，但不作为完整的主体实例化，并且不在模型中做出决策。然而，这些未实例化的主体通过家庭其他成员的经济决策间接参与其中（例如，在转入非活动状态时考虑到了依赖子女数量，在家庭收入中包括退休金）。15岁以下的个人在15岁时成为完整的主体，并且有些人仍然留在学校系统中，而其他人则进入劳动力市场。最后，“周期”对应于“一周”，以捕捉许多短期合同上很短的时间段，并尽可能接近实际的总流量。根据ACOSS（2011）的数据，2010年有46%的新雇佣是持续时间为一周或更短的固定期限合同。

## Environment



2.3
In addition to these agents, the model uses three *artifacts*16:
- *JobAds*, which lists job ofers from the firms and job applications from the job seekers. Dissemination
of information, however, is based on the costly job search process described in more detail below (see Section 2.25, according to the principles of search theory.
- a *Statistical Institute* that calculates statistics from the simulation and disseminates some information
(e.g. tension on the labor market). The information is imperfect for agents, and we specify what information is being broadcasted.
- a *Public Sector* that recruits (exogenously) employees and collects payroll taxes on businesses.

2.3
除了这些主体外，该模型还使用了三个“工具”16：
- “职位广告”，其中列出了企业的职位提供和求职者的求职申请。然而，信息的传播是基于搜索理论中更详细描述的昂贵的求职过程（见第2.25节）。
- 一个“统计研究所”，用于从模拟中计算统计数据并传播一些信息（例如劳动力市场上的紧张情况）。对于主体来说，这些信息是不完全的，并且我们明确指定了正在广播哪些信息。
- 一个“公共部门”，以外生方式招募员工并收取企业的工资税。

## Institutional Framework



2.4
Moreover, it also includes one *institutional module*. One distinctive feature of the WorkSim model is to integrate
a fairly complete and flexible institutional framework that includes (1) the necessary elements of the French
labor Law, featuring two types of contracts - *Fixed-Term contracts* (denoted *FTC*) and open ended contracts
(OEC), but also dismissals on personal and fires on economic grounds, redundancy payments, etc. and (2) government decisions (minimum wages, welfare benefits, etc.). This institutional framework is described in more detail in Appendix B.

2.4
此外，该模型还包括一个“制度模块”。WorkSim模型的一个显著特点是将一个相当完整且灵活的制度框架整合其中。该框架涵盖了法国劳动法的必要要素，包括两种类型的合同 - “固定期限合同”（FTC）和无固定期限合同（OEC），以及个人解雇、经济裁员等情况，还涉及解雇补偿金等内容。此外，该框架还考虑了政府决策（如最低工资、福利待遇等）。有关该制度框架的详细描述可参见附录B。

## Individuals



2.5
In WorkSim, each individual with index i is characterized by the following attributes :
- *Gender* : female or male. - *Age*, counted in weeks (a tick or period represents one week in the simulation). - Preferences for *free time* : see Section 2.29 below.
- *State* in the labor market. The possible states are : inactive, unemployed, employed and not searching for
another job (denoted ENS), *employed and seeking a new job* (denoted OTJS, for On-The-Job Searchers), student or *retired*.
- *Occupation*, denoted q in this paper. The number of possible occupations is denoted nq. In our simulations, we consider 3 levels : 1 = blue collar or employee, 2 = middle level job, 3 = manager. An individual can change his occupation during the simulation (upward or downward).
- Productivity kernel, *kProd*i : it represents the "innate" abilities of the individual i.
$$kP r o d_{i}\,\sim M a x(0,\,{\mathcal{N}}\left(1,\sigma_{k e r n e l P r o d}\right)),$$
where standard deviation σ*kernelP rod* ∈ [0, 1] is an exogenous calibrated parameter17.

2.5
在WorkSim中，每个索引为i的个体具有以下特征：
- *性别*：女性或男性。
- *年龄*：以周为单位计算（模拟中的一个周期代表一周）。
- 对*空闲时间*的偏好：详见下文第2.29节。
- 在劳动力市场中的*状态*。可能的状态包括：非活跃、失业、就业但不寻找其他工作（记为ENS）、就业并寻找新工作（记为OTJS，即在职求职者）、学生或退休。
- *职业*：本文中记为q。可能的职业数量记为nq。在我们的模拟中，我们考虑了3个级别：1 = 蓝领或雇员，2 = 中层岗位，3 = 管理者。个体可以在模拟过程中改变自己的职业（向上或向下）。
- 生产力核心*kProd*i：它代表了个体i的“天赋”能力。
$$kP r o d_{i}\,\sim M a x(0,\,{\mathcal{N}}\left(1,\sigma_{k e r n e l P r o d}\right)),$$
其中标准差σ*kernelP rod* ∈ [0, 1] 是一个外生校准参数17。

- Condition factor condi,t that represents his physical and psychological condition at time t. It evolves with
time following a random walk :
$$cond_{i,t+1}=Max(minC,\ Min(maxC,cond_{i,t}+\mathcal{N}(0,\sigma_{C})))\tag{1}$$
Hence ∀t, condi,t ∈ [minC, maxC]. minC et *maxC* are two exogenous parameters and σC ∈ [0, 0.3] is calibrated.

- 条件因素condi,t代表个体在时刻t的身心状态。它随时间演变，遵循随机游走的规律：
$$cond_{i,t+1}=Max(minC,\ Min(maxC,cond_{i,t}+\mathcal{N}(0,\sigma_{C})))\tag{1}$$
因此，对于任意时刻t，condi,t ∈ [minC, maxC]。其中minC和maxC是两个外生参数，而σC ∈ [0, 0.3]则经过校准确定。

- Human capitals (HC) HCgen
i,t , HCocc
i,q,t, HCspec
i,p,t , respectively for the general, *occupational level* q, and specific to the firm and job p *human capitals*18. The general HC represents the abilities useful for all jobs, like
problem solving or knowledge of a foreign language. It increases with experience (one more unit per period) and also with training. It decreases at each period when the individual is unemployed (or inactive)
by a percentage *Lxp* afer *Txp* periods (loss of skills). *Lxp* ∈ [0, 0.1] and *Txp* ∈ [0, 500] are two calibrated parameters. The occupational HC is related to the occupation, and represents abilities specific to this occupation: engineering field or craf for instance. Like the general HC, it increases with experience (one more unit per period) and also with training, and decreases at each period if the individual is unemployed (or inactive) by a percentage *Lxp* afer *Txp* periods. The specific HC is related to the position and the firm. It represents abilities specific to the job in the firm, like a particular process or a sofware to use. It equals the number of periods the employee spends in the job. It is reset to zero when he exits this job to another job in the firm.

- 人力资本（HC）分为一般性的HCgeni,t、职业层次q的HCocci,q,t和特定于公司和职位p的HCspeci,p,t。一般性的HC代表适用于所有工作的能力，如问题解决或外语知识。它随着经验（每个时期增加一个单位）和培训的增加而提高。当个体失业（或非活动状态）时，它会在每个时期按比例*Lxp*减少（技能损失），其中*Lxp* ∈ [0, 0.1]和*Txp* ∈ [0, 500]是两个校准参数。职业性的HC与职业相关，代表特定职业所需的能力，例如工程领域或手艺。与一般性HC类似，它随着经验（每个时期增加一个单位）和培训的增加而提高，并且如果个体失业（或非活动状态），则在每个时期后按比例*Lxp*减少。特定于公司和职位的HC与岗位和公司相关。它代表了在该岗位上所需的特定能力，如特定流程或软件使用等。它等于员工在该岗位上度过的时间段数，在他从这份工作转到公司内另一份工作时被重置为零。

## Demand



2.6
Labor is the only production factor, a natural simplification in a stationary state model. As mentioned, there is one good, and each firm produces a certain amount of its own variety of this good. The price P is assumed
unique (horizontal diferentiation between firms) and fixed at the arbitrary value of 1. Each firm responds to a
quantity demanded of this good Dj,t, which fluctuates randomly due to variations in consumers preferences.
However, the total demand Dtot is held constant because we aim to study our economy in a steady state.
2.7
At time t = 0, the *market share* of a firm j is given by Dj,t=0/Dtot. We assume that the distribution of this
total demand is diferent in the initializations. We then apply a stochastic shock which defines the trend of this
market share for each firm catch year and another stochastic shock each period (random walk) using a normal law:

2.6
在稳态模型中，劳动力是唯一的生产要素，这是一种自然的简化。正如前文所述，只有一种商品，每家公司生产自己独特的数量。价格P被假定为唯一且固定在任意值1上（公司之间存在水平差异）。每家公司对需求量Dj,t作出回应，该需求量由于消费者偏好的变化而随机波动。然而，总需求Dtot保持恒定，因为我们旨在研究经济在稳态下的情况。

2.7
在t = 0时刻，公司j的市场份额由Dj,t=0/Dtot确定。我们假设初始状态下总需求的分布是不同的。然后我们引入一个随机冲击来定义每个公司每年捕获市场份额的趋势，并且使用正态分布进行每个时期（随机游走）进行另一个随机冲击：

$$\forall t,\ MS_{j,t}=Max(0,MS_{j,t-1}\times(1+\mathcal{N}(\mu_{MS,j,t},\sigma_{MS,j,t})))\tag{2}$$

对于每个时间点t，公司j的市场份额可以通过以下公式计算得出：$$MS_{j,t}=Max(0,MS_{j,t-1}\times(1+\mathcal{N}(\mu_{MS,j,t},\sigma_{MS,j,t})))\tag{2}$$

with $\mu_{MS,j,t},\sigma_{MS,j,t}$ specific trend and volatility factor assumed to be unknown by the firms. These coefficients are randomly reassessed every year for each firm.

根据假设，公司对于$\mu_{MS,j,t},\sigma_{MS,j,t}$的具体趋势和波动因素是未知的。这些系数每年都会被随机重新评估。

## Jobs



2.8
Eachfirmhasamanagingdirectorandalistofjobsperoccupation. Ajobcanbein3diferentstates: filled,vacant
or *pending*. A *pending* job is typically a *FTC* contract that ended, but cannot be renewed immediately, because
of the grace period19.
2.9
Each job p of the occupation q is characterized by specific attributes determined once for all at its creation :
- a vector of required human capitals [HCgen
req,p, HCocc
req,p,q, HCspec
req,p], respectively for the *general*, the occupational level q, and the *specific to the firm* and job p *human capitals*. They represent the minimum skills
required to work on this job and are randomly drawn according to uniform distributions respectively between 0 and MaxHCgen
req , MaxHCocc
reqand MaxHCspec
req . We will see in the next section that an individual
can acquire these skills with experience or training.
- The duration of work *HpW*p, measured by the number of hours required per week for the job p.
- An hourly base production QHbase
j,q
for all jobs in the firm at occupation q. It is randomly drawn at the
creationofthefirmj,toaccountforthediferencesinproductioneficiency(technology,organization*. . .* )
between the firms. The weekly efective production of an individual on a job depends on this hourly base production and the duration of work, but also on the individual characteristics described on Section 2.4. The complementarity between the technological level of the job (related to the physical capital) and the individual skills (the human capital) has been shown in numerous studies starting with Griliches (1969). We assume that this base level of production does not depend on the type of contract assigned to this job. The weekly efective production of an individual i on this job p at time t is given by
$$QH^{eff}_{j,q}=HpW_{p}\times QH^{base}_{j,q}\times kProd_{i}\times cond_{i,t}\times F_{\beta}(HC^{gen}_{i,t},HC^{occ}_{i,q,t})\times F_{\lambda}(HC^{spec}_{i,p,t}),\tag{3}$$
with

2.8
每家公司都有一位总经理和一份职位清单。每个职位可以处于三种不同的状态：已填补、空缺或待定。待定的职位通常指的是全日制合同到期后无法立即续签的情况，因为存在宽限期。

2.9
每个职业q中的职位p由特定属性描述，这些属性在创建时确定：
- 一个人力资本需求向量[HCgen req,p, HCocc req,p,q, HCspec req,p]，分别代表*通用*、职业水平q和*特定于公司*和职位p的人力资本需求。它们表示了在该职位上所需的最低技能，并且根据均匀分布随机抽取，范围分别在0和MaxHCgen req、MaxHCocc req以及MaxHCspec req之间。我们将在下一节中看到，个体可以通过经验或培训获得这些技能。
- 工作持续时间HpWp，以每周所需工作小时数来衡量。
- 公司中所有职业q上工作岗位的每小时基础产出QHbasej,q。它在公司创建时随机抽取，以考虑公司之间生产效率（技术、组织等方面）的差异。个体在该工作岗位上每周的实际产出取决于这个每小时基础产出和工作持续时间，同时还取决于第2.4节中描述的个体特征。从Griliches（1969）开始，许多研究表明了工作岗位的技术水平（与物质资本相关）和个体技能（人力资本）之间的互补性。我们假设这个基础产出水平不依赖于分配给该职位的合同类型。个体i在时间t上对该职位p的每周实际产出由以下公式给出：
$$QH^{eff}_{j,q}=HpW_{p}\times QH^{base}_{j,q}\times kProd_{i}\times cond_{i,t}\times F_{\beta}(HC^{gen}_{i,t},HC^{occ}_{i,q,t})\times F_{\lambda}(HC^{spec}_{i,p,t}),\tag{3}$$
其中

Fβ(HCgen i,t , HCocc i,q,t) = 1 + β × HCgen i,t − β′ × (HCgen i,t )2 + βq × HCocc i,q,t − β′ q × (HCocc i,q,t)2 (4) and Fλ(HCspec i,p,t ) = 1 + λ × HCspec i,p,t − λ′ × (HCspec i,p,t )2. (5)
β,β′,βq,β′
q,λ, λ′ are calibrated parameters greater than 0. The sensitivity functions Fβ and Fλ are concave, in order to introduce diminishing returns of the human capital on the employee productivity. These diminishing returns are observed for example in the study of Kramarz et al. (2006) for France.

根据公式（4）和（5），我们可以得到以下敏感函数：

Fβ(HCgen i,t , HCocc i,q,t) = 1 + β × HCgen i,t − β′ × (HCgen i,t )2 + βq × HCocc i,q,t − β′ q × (HCocc i,q,t)2 

Fλ(HCspec i,p,t ) = 1 + λ × HCspec i,p,t − λ′ × (HCspec i,p,t )2

其中，β、β'、βq、β'q、λ和λ'是大于0的校准参数。为了引入人力资本对员工生产力的递减回报，敏感函数Fβ和Fλ均为凹函数。这种递减回报在Kramarz等人（2006）对法国的研究中得到了观察。

- An *hourly base salary* determined from the base production in the job for all jobs in the firm at occupation q : SHbase j,q = QHbase j,q × P × (1 − ζ) (6) with $P=1$ the exogenous price of the (unique) good and $\zeta\in[0,1]$, an exogenous parameter that represents the share of the base productivity value kept by the firm (in order to pay expenses, taxes, interests, dividends, etc.). It reflects the balance of power between workers' and employers' unions in the country, since the model does not assume perfect competition and free entry, and workers are not paid their marginal productivity. This does not mean that the forces of competition do not play, since employees the only workers've so the portfolio, while the workers's place their reservation waves when given horizons on the market. The weekly effective salary of an individual $i$ on this job at time $t$ is below by :

- 公司中所有职位的每小时基本工资是根据该职位的基本生产量来确定的，表示为SHbase j,q = QHbase j,q × P × (1 − ζ) (6)，其中$P=1$表示（唯一）商品的外生价格，而$\zeta\in[0,1]$则是一个外生参数，代表公司保留的基本生产力价值的份额（用于支付费用、税收、利息、股息等）。这个模型并不假设完全竞争和自由进入，因此工人们并不按照他们的边际生产力得到报酬。然而，这并不意味着竞争力量没有发挥作用，因为员工是唯一拥有该组合的员工，在市场出现波动时会调整他们对薪水的期望。个体i在时间t上从这份工作获得的每周实际薪水如下所示：

$$S_{i,j,p,q,t}=Max(\mathsf{SHC}_{H}+HpW_{p},SH^{base}_{j,q,t}\times HpW_{p}\times F_{ji}(HC^{open}_{i,t},HC^{occ}_{i,q,t})\times F_{\lambda}(HC^{open}_{i,p,t})\times G(U_{q,t=core}))\tag{7}$$
where SMICH is the hourly minimum wage in France (see Appendix B for details about the institutional framework in France), and G(Uq,t=*crea*) = ( Uq,t=crea U*q,ref* )ω, with Uq,t=*crea* the unemployment rate at the occupation level q when creating the job ofer and U*q,ref* the reference unemployment rate during the current year. Estimations of the efect of the unemployment level on the new worker's wages are not directly available in France, and rarely elsewhere (we mentioned Martins et al. (2012) for Portugal). In order to set this elasticity, that we assume constant, we use the wage curve, a relation between the levels of unemployment in diferent local labor market and the wage levels, although the change in the unemployment rate within an occupation over time is not exactly the same phenomenon (Blanchflower & Oswald 1994). ω has been found to be stable over a very large set of studies on the wage curve (Nijkamp & Poot
(2005)), and equal to −0.1 20 The efective salary of an individual does not depend on its unobservable productivity kernel *kProd*i nor on its condition factor condi,t. The only diferentiation is due to measurable and therefore indisputable factors of human capital related to experience in the line of the human capital theory.

$$S_{i,j,p,q,t}=Max(\mathsf{SHC}_{H}+HpW_{p},SH^{base}_{j,q,t}\times HpW_{p}\times F_{ji}(HC^{open}_{i,t},HC^{occ}_{i,q,t})\times F_{\lambda}(HC^{open}_{i,p,t})\times G(U_{q,t=core}))\tag{7}$$
其中，SMICH是法国的最低小时工资（有关法国制度框架的详细信息请参见附录B）。而G(Uq,t=*crea*) = ( Uq,t=crea U*q,ref* )ω，其中Uq,t=*crea*表示在创建职位时职业水平q上的失业率，U*q,ref*表示当前年份的参考失业率。在法国以及其他地方，很少直接提供有关失业水平对新员工工资影响的估计数据（我们提到了Martins等人对葡萄牙的研究）。为了确定这个我们假设为常数的弹性系数，我们使用了工资曲线，即不同地方劳动力市场中失业水平与工资水平之间的关系，尽管职业内随时间变化的失业率变化并不完全相同（Blanchflower和Oswald 1994）。ω在大量关于工资曲线的研究中被发现是稳定的（Nijkamp和Poot(2005)），并且等于-0.1 20。个体的实际薪水不依赖于其不可观测的生产力核心*kProd*i，也不依赖于其条件因子condi,t。唯一的区别是与人力资本理论相关的经验等可衡量且无争议的人力资本因素。

- A level of *amenity*. This represents non-monetary features perceived by the individual on the job (social
recognition, working environment,*. . .* ). An hourly base amenity is randomly drawn at the creation of the
firm as a percentage *PrA* of the base salary for all occupation level q.

- *福利水平*。这代表个体在工作中感知到的非货币特征（社会认可、工作环境等）。在公司创建时，以职业水平q为基础的每小时福利水平将随机抽取，作为基本工资的*PrA*百分比。

## Simulation Cycle In The Worksim Model



2.10
The **simulation cycle** includes four main steps, as shown in Figure 1 below:
Firm decisions : contracts and vacancies management, evaluations, job creation / destruction;
Individual decisions : labor market entrances and exits, job search;
Firm decisions : applications and promotions management;
Demography : household dynamics, retirements, aging.

2.10
模拟周期包括以下四个主要步骤，如图1所示：
企业决策：合同和职位管理、评估、岗位的创建与销毁；
个体决策：劳动力市场的进入和退出、求职活动；
企业决策：申请和晋升管理；
人口统计学：家庭动态、退休、老龄化。

[重写后的中文内容]

## Firm Decisions



2.11
Before describing the job creation process, we present the demand anticipation mechanism that is the core of the job creation process and the endogenous choice between the diferent contracts : *FTC* and *OEC*.

2.11
在描述就业创造过程之前，我们介绍了作为就业创造过程核心的需求预测机制以及不同合同之间的内生选择：*FTC*和*OEC*。

## Demand Anticipation



2.12
The central idea that governs job creation relies on the way the firm will estimate the future demand. If the demand is going to increase, a new job might be profitable, but not if there is a decrease in the demand. Hence,
the firm will compute three scenarios - *bad* (noted θ = −1), *neutral* (θ = 0) and *good* (θ = +1), which are depicted in Figure 2 below. We see in this figure that in the bad scenario, the demand of the firm is below its production with the new job afer a certain time. As the firm cannot sell more than its demand, and the good is perishable, it may result in a loss because the firm has to continue to pay a salary if it is an OEC until economic dismissal is allowed (a year of delay in the reference experiment). In this example, we see that it may be more profitable for the firm to choose a contract with a shorter duration like a 3 months *FTC*. Indeed, the firm will have the option to end this contract afer 3 months in case of a bad scenario or to renew it if it goes well. FTC then act as a bufer against the shocks on demand. However with a shorter contract it is more dificult to amortize the cost of hiring and training a new employee. It therefore appears a trade-of depending on how the employer perceives the risks. A supplementary trade-of comes from the increase of productivity with tenure in a job, that the employer anticipates. Since this productivity increase is shared by the employer, this factor also favors *OEC* and counterweights the risks of a dismissal cost.

2.12
就业创造的核心思想在于企业如何评估未来的需求。如果需求将增加，新的工作可能会带来利润，但如果需求减少，则不会。因此，企业将计算三种情景——“不好”（记为θ = -1）、“中性”（θ = 0）和“好”（θ = +1），如下图所示。从图中可以看出，在不好的情况下，企业的需求低于其生产能力与新工作之间存在一定时间差。由于企业不能销售超过其需求量，并且商品易腐烂，这可能导致亏损，因为企业必须继续支付OEC合同下员工的薪水直到经济解雇被允许（在参考实验中延迟一年）。在这个例子中，我们可以看到对于企业来说选择一个较短期限合同（比如3个月的FTC）可能更有利可图。事实上，如果出现不好的情况，企业将有选择在3个月后结束该合同或者在情况良好时续签合同。FTC因此对需求冲击起到了缓冲作用。然而，较短期限合同更难摊销招聘和培训新员工的成本。因此，这取决于雇主对风险的感知，出现了一种权衡。另一个权衡来自于雇佣期限与工作绩效的增加，这是雇主预期到的。由于这种绩效提升是由雇主共享的，这个因素也有利于OEC并抵消了解雇成本的风险。

2.13
Because of bounded rationality, the firms anticipate with *finite horizons* corresponding to the specifications of
the diferent contract types. For each contract the decision process computes a net profit for each scenario, and then combines the three possible scenarios into a weighted profit. The weight of each scenario is calibrated at the aggregate level. The most profitable contract type and duration are selected (see Appendix A for details).
Job creations (step 1 in Figure 1)

由于有限理性，企业会根据不同合同类型的规定预期有限的时间范围。对于每个合同，决策过程会计算出每种情景下的净利润，并将三种可能情景的利润进行加权组合。每种情景的权重在总体水平上进行校准。最终选择最具盈利性的合同类型和持续时间（详见附录A）。图1中的步骤1代表就业创造。

2.14
The job creation proceeds in three steps:
1. First, thefirmchecksifthereisasuficientdemandmargintocreateanewjob. Hereitconsiderstheactual
(not anticipated) demand margin DM*j,q,t* for firm j and occupation level q at time t: if it exceeds the
demand margin threshold DT (calibrated parameter), then the firm moves to the next step. Otherwise,
no job is created.
2. If there is in the firm a *pending* job in the occupation q, the firm considers to hire a new person for this
job (taking into account the eventual grace period). Therefore the pending job becomes a *vacant* job.
Otherwise, it moves to the next step.
3. Here, DMj,q,t *> DT* and there are no pending jobs in occupation q. Hence, the firm considers to create
a new job p of the occupation q. The characteristics of this new job are randomly drawn (cf. Section 2.7
above). From these job features, the firm must decide which type of contract suits better.
2.15
In order to create a job and choose a contract, the firm proceeds as follow:
1. During a prospecting phase, the firm receives information about *NPros* job seekers of the occupation
q, who have applied to a job with a *FTC* and *NPros* job seekers of the occupation q who have applied
to a job with a *OEC* during the last period. The expected profit per period φper
i,j,p,q,c,t for a candidate i
on a job p with a contract c is then computed for each contract (see Appendix A) : the *OEC* contract is
compared with several *FTC* with diferent fixed terms (1 week, 1 month, 2 months, 6 months, 12 months, 18 months). As described in Appendix A, it takes into account the training costs for the job.

2.14
就业创造分为三个步骤：
1. 首先，企业检查是否存在足够的需求边际来创造新的工作岗位。在时间t，企业考虑到企业j和职位水平q的实际需求边际DM*j,q,t*（而非预期）：如果超过需求边际阈值DT（校准参数），则企业进入下一步。否则，不会创建工作岗位。
2. 如果在职位q中存在一个“待定”工作岗位，企业考虑雇佣新人来担任该岗位（考虑到可能存在的宽限期）。因此，“待定”工作变成了“空缺”工作。否则，进入下一步。
3. 在这种情况下，DMj,q,t *> DT* 并且在职位q中没有“待定”工作。因此，企业考虑创建一个职位q的新工作p。这个新工作的特征是随机抽取的（参见上文第2.7节）。从这些工作特征中，企业必须决定哪种类型的合同更适合。

2.15
为了创造就业机会并选择合同类型, 企业按照以下方式进行：
1. 在勘探阶段, 企业收到关于职位q的*NPros*个求职者的信息，他们在上一个周期内申请了一份带有*FTC*和*NPros*个求职者的职位q的工作，他们在上一个周期内申请了一份带有*OEC*的工作。然后为每种合同计算每期候选人i在合同c下工作p的预期利润φper
i,j,p,q,c,t（详见附录A）：将*OEC*合同与多个具有不同固定期限（1周、1个月、2个月、6个月、12个月、18个月）的*FTC*进行比较。如附录A所述，它还考虑了该工作岗位的培训成本。

2. Then the firm chooses to *create the contract* c with the *best average positive profit*, calculated along a
set of potential candidates. These candidates are job seekers and the employer is informed via JobAds
of their anticipated productivity level corresponding to their occupation, given their human capitals and
the base production in the job (The information is based on equation3 but the productivity kernel and the condition factor are unknown to the firm and set at their average). The employer will choose the contract
c∗ that gives the highest positive expected profit per period φper
i,j,p,q,c,t. If all the profits are negative, no
new job is created.
3. The firm continues to consider creating new jobs as long as DMj,q,t *> DT*.
Job destruction (step 2 in Figure 1)

2. 随后，公司选择与一系列潜在候选人中的*最佳平均正利润*相匹配的合同c。这些候选人是求职者，通过招聘广告(JobAds)向雇主提供了他们预期的生产力水平，该水平与他们的职业、人力资本和工作基础生产力相对应（该信息基于方程3，但生产力核函数和条件因子对公司来说是未知的，并被设定为其平均值）。公司将选择每个周期内给出最高正预期利润φper
i,j,p,q,c,t的合同c∗。如果所有利润都为负，则不会创建新岗位。
3. 只要DMj,q,t *> DT*，公司将继续考虑创建新岗位。
岗位销毁（图1中的步骤2）

2.16
By contrast, when there is a significant reduction in its demand in one occupation (in our model, this is when
DM*j,q,t* < −DT), the firm reacts in the short-term by removing its pending jobs and vacancies. In the medium
run (on a yearly basis), if this low cost adjustment is not suficient, the firm considers the possibility to dismiss workers.
2.17
Moreover, independently of the demand level, pending jobs and the vacancies that remain unfilled and have a duration greater than a fixed threshold - a parameter that will difer for *FTC* and *OEC* - are destroyed since
they have a cost.
2.18
Economic dismissals : an evaluation of the financial viability of the company is performed on a yearly basis (52
periods in the simulation). The first date of the balance sheet is drawn randomly, then this financial reporting occurs every year from this date. The company calculates its yearly return that is computed as the ratio of the
yearlyprofitoverthetotallaborcost21. Ifthisreturnfallsbelowacertain*profitabilitythreshold* (afixedparameter
PT, that will be calibrated, but has to be negative, representing losses), the firm can justify an economic dismissal procedure. This is the formal implementation of our interpretation of the French jurisprudence (before the El-Khomri law) over the serious economic dificulties that allow to dismiss. However, owing to the diversity of judgments when workers appeal for unfair dismissal, an employer, even though she respects the threshold, may be condemned in industrial courts. Therefore she anticipates penalties on the base of the probabilities of litigation and loosing the case, which are added to the severance costs:
- all remaining vacancies are removed. - afer all the vacancies have been removed, if DM*j,q,t* < −DT still holds, the firm considers dismissing employees. It selects one employee randomly, computes the associated profit Φtot
i,j,p,q,c,t and the firing cost *EFC*. If Φtot
i,j,p,q,c,t < −EFC, the firm dismisses the employee. This process is repeated until
DM*j,q,t* > −DT or if all employees have been evaluated.
2.19
In the event that the company has a return below PT and has no employees to dismiss, the managing director "dismisses" himself, which in this case leads to the bankruptcy of the firm that is removed from the simulation.
Themanagingdirectorbecomesunemployed. However, wewantto*keepthenumberoffirmsconstant*22. Hence,
when a bankruptcy has occurred, we randomly select an active agent in the simulation to create a new firm and manage it. He will be the only producer in the firm (until he starts to recruit).

2.16
相比之下，当某个职业的需求显著减少时（在我们的模型中，当DM*j,q,t* < −DT时），公司会短期内采取措施，取消待定岗位和空缺。在中期（每年一次），如果这种低成本调整不足够，公司会考虑解雇员工的可能性。

2.17
此外，无论需求水平如何，在持续时间超过固定阈值（一个参数，在FTC和OEC之间有所不同）的待定岗位和未填补的空缺都会被销毁，因为它们产生成本。

2.18
经济解雇：公司每年进行一次财务可行性评估（模拟中有52个周期）。资产负债表的第一个日期是随机选择的，然后从该日期开始每年进行一次财务报告。公司计算其年度回报率，即年利润与总劳动力成本之比21。如果此回报率低于某个*盈利能力门槛*（一个固定参数PT，将进行校准，但必须为负数表示亏损），公司可以正当地实施经济解雇程序。这是我们对法国法律规定严重经济困难情况下解雇的解释的正式实施（在El-Khomri法之前）。然而，由于工人在不公平解雇时上诉时判决的多样性，即使雇主尊重门槛，也可能被工业法庭判决有罪。因此，她会预测诉讼和败诉的概率，并将其加到赔偿成本中：
- 所有剩余空缺都被移除。
- 在所有空缺被移除后，如果DM*j,q,t* < −DT仍然成立，则公司考虑解雇员工。它随机选择一个员工，计算相关利润Φtot
i,j,p,q,c,t和解雇成本*EFC*。如果Φtot
i,j,p,q,c,t < −EFC，则公司解雇该员工。此过程重复进行，直到DM*j,q,t* > −DT或所有员工都已评估完毕。

2.19
如果公司回报率低于PT并且没有要解雇的员工，则总经理“自己辞职”，这种情况下导致公司破产并从模拟中删除。总经理变得失业。然而，我们希望保持企业数量恒定22。因此，在发生破产时，我们随机选择模拟中的一个活跃主体来创建一家新公司并管理它。他将是该公司的唯一生产者（直到开始招聘为止）。

## Employee Evaluations (Step 3 In Figure 1)



2.20
In each period, the firm examines if some employees have to be evaluated. This individual evaluation may occur:
1. At the end of the probationary period for *FTC* and *OEC*;
2. Every year, at the anniversary date of the contract, for *OEC* employee;
3. At the end of *FTC* contract to decide if it should be renewed;
4. At the end of *FTC* contract, if the transformation of FTC to *OEC* is to be considered.
2.21
Dismissal for personal reasons (insuficient productivity : the process takes two steps :
1. First, the firm evaluates if there is a case for considering the dismissal. That could be the case if the
employee's production is below the firm's requirement. Thus, there is a chance that the firm considers to fire this employee for personal reasons if the annual production of the employee Qeval
i,j,p,q,t satisfies
: Qeval
i,j,p,q,t < ρ × Qrequired
p,q
where Qrequired
p,q
is the required level of production and ρ an exogenous —
calibrated - parameter in [0.7, 0.9]. ρ encodes the tolerance the firm has with underproduction, or the
maximum margin risk it accepts to take23.
2. Then the firm decides whether such a dismissal is more profitable or less costly than keeping him.

2.20
每个时期，公司会审查是否需要对员工进行评估。这种个体评估可能发生在以下情况下：
1. 对于*FTC*和*OEC*员工，在试用期结束时进行评估；
2. 对于*OEC*员工，在合同纪念日时每年进行评估；
3. 在*FTC*合同结束时，决定是否应该续约；
4. 在*FTC*合同结束时，考虑将其转换为*OEC*。

2.21
因个人原因解雇（生产力不足）：该过程分为两步：
1. 首先，公司评估是否有理由考虑解雇。如果员工的产量低于公司要求，则有可能公司会因为个人原因而考虑解雇该员工，条件是员工的年产量Qeval
i,j,p,q,t满足以下条件：
Qeval
i,j,p,q,t < ρ × Qrequired
p,q，
其中Qrequired
p,q是所需的产量水平，ρ是一个外生参数，在[0.7, 0.9]范围内进行校准。ρ编码了公司对低产量的容忍度或接受的最大风险边际23。
2. 然后公司决定是否解雇比保留该员工更具盈利性或成本更低。

## Hiring Phase And Promotions (Step 7-8 In Figure 1)



2.22
Once the firm has chosen which contract c to create, a hiring norm must be computed to evaluate the candidates. This *hiring norm* is the profitability threshold below which it prefers to refuse a candidate. To do so, it
uses the *positive* expected profits Φavg
j,p,q,c,t calculated for each of the *NPros* candidates during the prospecting
phase and computes the average ΦMoy, the minimum ΦMin and the maximum ΦMax values.
2.23
The hiring norm of the firm is given by the main economic factors taken into account in search theory:
$$HNnorm_{j,p,q,t=crea}=(\phi_{Moy}^{per}+N_{1}\times(\phi_{Max}^{per}-\phi_{Min}^{per}))\frac{N(d_{c})}{H(TIGH_{q,t=crea})}\tag{8}$$
- t = *crea* is the time of the creation of the contract.
- N1 is calibrated in [0, 1]. The hiring norm increases with φper
Max − φper
Min, so that the firm favors a large dispersion of candidates' qualities in order to increase the probability to get better candidates, as prescribed by search theory.
- N(dc) = N2 + N3 × dc, an increasing function 24 of the duration of the contract dc proposed for the job.
N2 et N3 are two calibrated parameters in [0, 1]. We assume that the firm will be more demanding for
longer contracts, as they imply to keep the employee for a longer time.
- TIGHq,t=*crea* is the tightness on the labor market at the time of job creation and is given by
TIGHq,t=*crea* =
Vq,t
Uq,t with Vq,t the vacancy rate and Uq,t the unemployment rate at time t for the occupation q. The higher this tension, the more the firm has to lower its requirements if it hopes to find a
candidate. We assume that the impact of the tension to HN is limited to ±20%, because the hiring norm
could be otherwise increased above the profitability of any worker, so H is a logistic function with values
between 0.8 and 1.2 and given by H(x) = 0.8 +
0.4
1+20×e−3x .
2.24
This hiring norm above is then decreased by a percentage N4 in each period until the job is filled, but never
drops below 0.
2.25
Hiring takes place in three steps:
1. *Receiving applications* - The firm receives applications from external and internal applicants.
2. *Selection and potential hiring* - A two-step process takes place:
(a) First, thefirmcomputesascoreforeachcandidate(internalorexternal), givenbytheexpectedprofit
per period Φper
i,j,p,q,c,t. Then the best candidate (highest score) is selected.
(b) Thereafer, the firm checks if this candidate's score exceeds the hiring norm. If this is the case, the
candidate is hired, otherwise, the job remains vacant.
3. Internalpromotion—Ifthebestcandidatehiredisaninternalcandidateofthecompany, itisapromotion.
The employee acquires the occupation level of the job.
2.26
When an individual is hired for the job, he is trained and receives the minimum required human capital for the job if he does not have it yet and the firm pays for it:
$$HC^{gen}_{i,t}\leftarrow\texttt{Max}(HC^{gen}_{i,t},HC^{gen}_{req,p})\tag{9}$$ $$HC^{occ}_{i,q,t}\leftarrow\texttt{Max}(HC^{occ}_{i,q,t},HC^{occ}_{req,q})$$ (10) $$HC^{spec}_{i,p,t}\leftarrow\texttt{Max}(HC^{spec}_{i,p,t},HC^{spec}_{req,p})\tag{11}$$
2.27
The costs are proportional to the weekly base salary in the job and the gaps in human capital to be filled (Appendix A). Yet the cost of training is deducted from the expected profit a candidate provides to the firm, so that a
candidate who needs much training is unlikely to be selected (see Apppendix A)25. This is an assumption which
fits the facts: a worker who would not fit minimal norms of productivity could have a productivity below the minimum wage in the model, and also induce many other problems such as underutilising capital and slowing team work in the real world. The theoretical framework of ranking candidates according to the expected training costs has been developed by Thurow (1975) under the label of job competition, and fits easily as an extension of the search based concept of a hiring norm. The wage has a job specific base, and cannot be lower that this base, which is a component of the hiring norm. The expected profit provided by a candidate, net of the training costs, must be higher than the hiring norm.

2.22
一旦公司确定了要创建的合同c，就需要计算一个招聘标准来评估候选人。这个“招聘标准”是指公司更愿意拒绝候选人的盈利门槛。为此，公司使用在勘探阶段为每个候选人计算的预期利润Φavg
j,p,q,c,t，并计算平均值ΦMoy、最小值ΦMin和最大值ΦMax。
2.23
公司的招聘标准由搜索理论中考虑到的主要经济因素给出：
$$HNnorm_{j,p,q,t=crea}=(\phi_{Moy}^{per}+N_{1}\times(\phi_{Max}^{per}-\phi_{Min}^{per}))\frac{N(d_{c})}{H(TIGH_{q,t=crea})}\tag{8}$$
- t = *crea*表示合同创建的时间。
- N1在[0, 1]范围内进行校准。招聘标准随着φper Max − φper Min 的增加而增加，因此公司偏好候选人质量分散较大，以增加获得更好候选人的概率，这是搜索理论所建议的。
- N(dc) = N2 + N3 × dc，是提供该工作岗位所建议合同持续时间dc的一个递增函数24。
N2和N3是在[0, 1]范围内进行校准的两个参数。我们假设对于较长的合同，公司会更加苛刻，因为这意味着需要将员工保留更长时间。
- TIGHq,t=*crea*是在工作创建时劳动力市场的紧张程度，并由以下公式给出：
TIGHq,t=*crea* =
Vq,t
Uq,t，
其中Vq,t是职业q在时间t的空缺率，Uq,t是失业率。市场紧张程度越高，如果希望找到候选人，公司就必须降低要求。我们假设紧张程度对招聘标准的影响限制在±20%以内，因为否则招聘标准可能会超过任何工人的盈利能力。因此H是一个介于0.8和1.2之间的逻辑函数，并且由H(x) = 0.8 +
0.4
1+20×e−3x 给出。
2.24
然后，在每个周期中，该招聘标准会按照百分比N4递减，直到填补该岗位，但不会低于0。
2.25
招聘分为三个步骤：
1. *接收申请* - 公司接收来自外部和内部申请人的申请。
2. *筛选和潜在招聘* - 这是一个两步过程：
(a) 首先，公司为每个候选人（内部或外部）计算一个分数，该分数由每期预期利润Φper
i,j,p,q,c,t给出。然后选择最佳候选人（最高分）。
(b) 然后，公司检查该候选人的分数是否超过了招聘标准。如果是这样，则雇佣该候选人；否则，岗位将保持空缺。
3. *内部晋升* - 如果被雇佣的最佳候选人是公司内部的员工，则视为晋升。员工获得该岗位的职业水平。
2.26
当某个个体被雇佣时，如果他还没有达到所需的最低人力资本水平，他将接受培训并获得所需的最低人力资本，并由公司支付：
$$HC^{gen}_{i,t}\leftarrow\texttt{Max}(HC^{gen}_{i,t},HC^{gen}_{req,p})\tag{9}$$ $$HC^{occ}_{i,q,t}\leftarrow\texttt{Max}(HC^{occ}_{i,q,t},HC^{occ}_{req,q})$$ (10) $$HC^{spec}_{i,p,t}\leftarrow\texttt{Max}(HC^{spec}_{i,p,t},HC^{spec}_{req,p})\tag{11}$$
2.27
这些成本与岗位的每周基本工资和需要填补

## Individuals' Decisions (Step 4-6 In Figure 1)



2.28
The individuals take decisions in each period of the simulation. This decision process is modeled with a state machine, where one individual, at each tick, will be in one particular state: inactive, unemployed, employed
and not searching for another job, employed and seeking a new job, student or retired. The transitions between these states can be caused by individual choices (for example: to look for a job, to quit a job, *. . .* ), by external
events (firing, death, *. . .* ), or eventually by a sequence of multiple decisions (e.g. applying for a job, and the
firm hires the candidate).

2.28
在模拟的每个时期，个体会做出决策。这一决策过程被建模为一个状态机，在每个时间点，一个个体将处于以下特定状态之一：不活跃、失业、就业但不寻找其他工作、就业且正在寻找新工作、学生或退休。这些状态之间的转换可能是由个体的选择（例如：寻找工作、辞职等）、外部事件（如解雇、死亡等）或者多次决策序列（例如申请工作并被公司录用）引起的。

## Utility Functions



2.29
Each individual uses a utility function, to decide whether he should stay in his current state or move to another one. The utility function has the generic form of a Cobb-Douglas function:
$$U=(Income+Amentity+Stability)^{1-\alpha}(Free\,Time)^{\alpha}\tag{12}$$
2.30
It is a weighted aggregation of four factors26:
1. *Income*: weekly income of the household in euros, divided by the number of consumption units (an adult
counts for 1, a child 0.5, as ofen in consumers'studies). This specification means that we take into account that the partner' earnings afect the participation decision of the individual. The family nature of the decisions is a fundamental element in labor economics and the theory of labor supply has studied the subject in depth. There are diferent theoretical possibilities. Models of joint decisions afer bargaining inside the household rely on heavy assumptions and are uneasy to generalize to all other workers' decisions on flows (such as quits). Our choice is in the line of Leuthold and Pollak as mentioned in the survey of family labor supply approaches by Killingsworth & Heckman (1986). It is a very simple specification but
it predicts some facts which are important both at a microeconomic level and at a macroeconomic level for WorkSim. First non wage incomes of the household afect the individual's decisions, and notably the hours and the participation decision negatively in France, and the specification implies this result (Kabatek et al. 2014). Secondly the partner's earnings decrease in the model the individual's participation probability. Kabatek et al. (2014) also find this result , which however remains debated (see Briard (2017)
for a survey of the empirical knowledge for the French case)27.
2. *Amenity*: non-monetary features perceived by the individual (social recognition, working environment,
job dificulty, *. . .* ). The factor is expressed as a percentage of the salary.
3. *Stability*: criteria reflecting the preference of the individual for stability, i.e. for a job with the long contract duration. The maximum value is given for a permanent job (OEC). This stability is expressed as a percentage of the salary.
4. *Free time*: free time per week available for the individual outside his working hours and search time. According to INSEE statistics28, we deduct 77 hours for sleep, eating, washing, from the total time per week.
Then, the free time covers leisure but also caring for the children, and the model takes into account that the statistics show that women put more value on time for child care.
much more time than men on caring for children, and this is modeled as a higher "preference" for free time. A participation rate decreasing in the number of young children ensues.

2.29
每个个体都使用一个效用函数来决定是否保持当前状态或转移到另一个状态。该效用函数采用了Cobb-Douglas函数的一般形式：
$$U=(收入+福利+稳定性)^{1-\alpha}(空闲时间)^{\alpha}\tag{12}$$

2.30
这是四个因素的加权聚合26：
1. *收入*：家庭每周收入（以欧元计算），除以消费单位的数量（成年人计为1，儿童计为0.5，常见于消费者研究中）。这一规定考虑到了伴侣的收入对个体参与决策的影响。家庭决策在劳动经济学中是一个基本要素，劳动供给理论对此进行了深入研究。有不同的理论可能性。家庭内部协商后共同决策模型依赖于严格的假设，并且很难推广到所有其他工人关于流动性（如辞职）的决策上。我们选择了Leuthold和Pollak在Killingsworth＆Heckman（1986）关于家庭劳动供给方法调查中提到过的方法。这是一个非常简单的规范，但它预测了一些在微观经济水平和宏观经济水平上对WorkSim都很重要的事实。首先，家庭的非工资收入会影响个体的决策，尤其是在法国，而该规范也预示了这一结果（Kabatek等人，2014）。其次，伴侣的收入会降低模型中个体参与的概率。Kabatek等人（2014）也发现了这一结果，但仍存在争议（有关法国情况的实证知识调查，请参见Briard（2017）27。

2. *福利*：个体感知到的非货币特征（社会认可、工作环境、工作难度等）。该因素以薪资百分比表示。
3. *稳定性*：反映个体对稳定性即长期合同工作偏好的标准。最大值对应永久职位（OEC）。该稳定性以薪资百分比表示。
4. *空闲时间*：个体在工作时间和搜索时间之外每周可用于自由活动的时间。根据INSEE统计数据28，我们从每周总时间中减去77小时用于睡眠、进食和洗漱。
然后，空闲时间包括休闲活动以及照顾孩子，并且模型考虑到统计数据显示女性更重视照顾孩子的时间。
女性在照顾孩子方面花费的时间比男性多得多，这被建模为对自由时间的更高“偏好”。随之而来的是，随着年幼子女数量的减少，参与率也会下降。

## Overview Of The Individuals' Decisions



2.32
The decision-making process of individuals is sequential and summed up in the state transition diagram depicted in Figure 3. At each period, the individual agent computes the utility of his current state and the utilities of each reachable state. Each utility is evaluated using the generic form given by Equation 12 above, and instantiatedwiththerelevantvaluesofincome, amenity, stabilityandfreetime. Moreover, afactor*ICHANG* ∈ [1, 2]
is applied to several transitions to account for the psychological cost to do such a change (calibrated parameter). The higher *ICHANG >* 1, the greater the new state utility must be to win the decision.

2.32
个体的决策过程是顺序的，如图3所示的状态转换图所总结。在每个时期，个体主体计算其当前状态的效用以及每个可达状态的效用。每个效用都使用方程12中给出的通用形式进行评估，并根据收入、福利、稳定性和空闲时间等相关值进行实例化。此外，对于某些转换，还应用了一个因子*ICHANG* ∈ [1, 2]来考虑进行此类变化所需的心理成本（校准参数）。当*ICHANG >* 1时，新状态必须具有更高的效用才能赢得决策。

## Job Search Process



2.33
Afer describing the diferent decision mechanisms, we now detail the overall job search process:
1. Each period in the model, a job seeker spends time trying to get information on some jobs (wage, contract). JobAds sends a list of NVi,t vacancies matching his occupation or a level above. We assume
that these incoming job ofers occur at a mean frequency that is known and independent of the time elapsed since the last ofer. Therefore, we model the arrival of new job ofers with a Poisson law: at time
t, this number of vacancies NVi,t is drawn from a Poisson distribution with parameter λt = NSJU ×
H(TIGHq,t), where *NSJ*U is the average number of vacancies received by the unemployed at each period, and H is the same function of tightness as above. It can be the case that a job seeker does not obtain information on a single vacant job during the period.
2. Theindividualsendsanapplicationforthefirstoferwhoseutilityisabovehisreservationutility UTRESi,t29.
If there is no job ofer corresponding to his occupation or if all his applications are rejected, he lowers his
reservation utility UTRESi,t. Thus, at the end of each period, the reservation utility is updated :
$$UTRES_{i,t}=UTRES_{i,t-1}\times(1-Ru_{3})+Ru_{4}\times(UTUEM_{i,t}-UTUEM_{i,t-1})\tag{13}$$
where Ru3 ∈ [0, 0.005] is a calibrated parameter and Ru4 a fixed parameter (0.5). The first term of the equation accounts for the diminution with time in unemployment and the second is driven by a modification of *UTUEM*, which is the utility for the unemployed (for instance a decrease of income will lower UTUEM and therefore *UTRES*, as the urge to find the job increases). We do not set diferent reservation utilities for the two types of contracts since the workers search for the two types of jobs simultaneously. Yet, we take into account the lower return to search provided by the FTC in terms of utility since they ofer shorter contracts, by including the stability parameter. This information is known to the searcher before contracting for an FTC. For an OEC the mean duration is known. This method ensures that searchers prefer OEC *ceteris paribus*, but may accept to apply to FTC when their research does not meet success by lowering their reservation utility30.

2.33
在描述了不同的决策机制之后，我们现在详细介绍整个求职过程：
1. 在模型中的每个时期，求职者会花费时间获取一些工作的信息（工资、合同）。JobAds会发送一个与他的职业或高一级别相匹配的NVi,t空缺职位列表。我们假设这些新到来的工作机会以已知且与上次机会出现时间无关的平均频率发生。因此，我们使用泊松分布来模拟新工作机会的到来：在时间t，空缺职位数NVi,t服从参数为λt = NSJU × H(TIGHq,t) 的泊松分布，其中NSJU是每个时期失业者收到的平均空缺职位数，H是与紧张度相关的函数。可能情况是，在该时期内求职者没有获得任何一个空缺职位的信息。
2. 每个个体都会申请第一个效用高于其保留效用UTRESi,t29 的工作机会。如果没有符合他所从事行业要求或者所有申请都被拒绝，则降低保留效用UTRESi,t。因此，在每个时期结束时，保留效用将进行更新：
$$UTRES_{i,t}=UTRES_{i,t-1}\times(1-Ru_{3})+Ru_{4}\times(UTUEM_{i,t}-UTUEM_{i,t-1})\tag{13}$$
其中Ru3 ∈ [0, 0.005] 是一个校准参数，Ru4是一个固定参数（0.5）。方程的第一项考虑了失业时间的减少，第二项由*UTUEM*的修改驱动，*UTUEM*是失业者的效用（例如收入下降会降低*UTUEM*，因此增加找工作的紧迫感）。我们没有为两种类型的合同设置不同的保留效用，因为工人同时寻找两种类型的工作。然而，我们通过包括稳定性参数来反映FTC在效用方面提供较低搜索回报率这一事实（因为他们提供较短期合同）。搜索者在与FTC签订合同之前就已经知道这些信息。对于OEC来说，平均持续时间是已知的。该方法确保在其他条件不变的情况下搜索者更喜欢OEC，但当他们无法成功找到工作时可能会通过降低其保留效用30来申请FTC。

## Demographic Module (Step 9-11 In Figure 1) Household Dynamics



2.34
In Worksim, an individual can be in three diferent household states:
1. *Child in a household*, meaning that he stays with his parents. He can be in the labor market or not (when
he is a student for example).
2. *Single person* (with or without children).
3. *In couple* (with or without children).
2.35
At each turn, the individuals change their household state according to transition probabilities deriving from
real demographic data31 measured by the French national institute of statistics (INSEE).
2.36
A simulation evolves over time with a stable population, therefore the agents marry each other and have children that can enter later in the labor market. These children can leave their household in order to create a new household.

在Worksim中，个体可以处于三种不同的家庭状态中：
1. *与父母同住的孩子*，意味着他与父母同住。他可以参与劳动市场，也可以不参与（例如当他是学生时）。
2. *单身人士*（有或没有子女）。
3. *夫妻关系*（有或没有子女）。

每一轮中，个体根据法国国家统计局（INSEE）测得的真实人口统计数据31所得到的转移概率改变他们的家庭状态。

模拟随着时间的推移而发展，并且具有稳定的人口。因此，主体之间会结婚，并且会有孩子后来进入劳动力市场。这些孩子可以离开自己的家庭以创建一个新的家庭。

## Retirements



2.37
The standard age of retirement is established to 65 in WorkSim, but an agent aged between 50 and 65 can get early retirement. We reproduce the share of retired individuals by age range according to INSEE statistics. Let us note however that a retired agent does not leave the simulation as he may still be a member of a household.

在WorkSim中，退休的标准年龄设定为65岁，但50岁至65岁之间的个体可以提前退休。我们根据法国国家统计局（INSEE）的数据重现了不同年龄段退休人员的比例。需要注意的是，即使个体退休了，他们仍可能是一个家庭的成员，因此并不会离开模拟。

## Aging



2.38
The age of an individual is increased by one week every tick or period of the simulation (one year corresponds to 52 ticks). The individuals leave definitely the simulation when they die at an age corresponding to the death rate by gender in France in 2014.

2.38
个体的年龄在每个模拟周期（一年对应52个周期）增加一周。当个体达到2014年法国男女性别死亡率所对应的年龄时，他们将永久离开模拟。

## Validation Process



3.1
The WorkSim methodology uses a validation process at two levels:
1. *model building* : the way we design the model, and especially the agents' decision rules is rooted as much
as possible in empirical data and facts. Following the *psychomimetism* methodology (Kant 1999), we ensure that these decision processes do not violate the cognitive principles we build our model on (e.g. bounded rationality).
2. *data reproduction*: we want our simulation to account for most available data on the labor market we aim
to study. To do so, we use an automatic procedure to calibrate the model parameters for which we do not have an empirical value (see Calibration section below).

3.1
WorkSim方法在两个层面上采用验证过程：
1. *模型构建*：我们的模型设计以及主体决策规则的制定尽可能地依据实证数据和事实。遵循*心理模仿*方法（Kant 1999），我们确保这些决策过程不违反我们所构建模型的认知原则（例如有限理性）。
2. *数据再现*：我们希望我们的模拟能够涵盖我们所研究劳动力市场上的大部分可用数据。为此，我们使用自动程序来校准那些没有经验值的模型参数（详见下文中的校准部分）。

## Calibration Scaling



3.2
First of all, we must set the number of agents in the simulation. It must be large enough to account suficiently
for real behaviors, but not exceed our computational power32. For the experiments described below, we initialized the agents population from the real data found for year 2014, at a scale of 1/4700. We obtained 8713
individuals and 808 firm agents, for a total of 9521 agents in the simulation.

3.2
首先，我们需要确定模拟中的主体数量。这个数量必须足够大，以充分考虑真实行为，但又不能超过我们的计算能力32。在下面描述的实验中，我们根据2014年的真实数据以1/4700的比例初始化了主体口。我们得到了8713个个体主体和808个公司主体，总共有9521个主体参与了模拟。

## Calibration Procedure



3.3
In order to calibrate the 56 parameters, we have to minimize a *fitness* function that is the weighted sum of the
relative spreads between the outputs of our model and the real targets of the French labor market in 2014 (from multiple sources given by INSEE and DARES). We have chosen 63 targets grouped in 10 diferent categories :
unemployment rates (7 targets), activity rates (6), salaries (14), job flows (12), FTC (4), long-term unemployment (3), mobility between occupations (12), additional (part-time, vacancies, on-the-job searchers, training costs) (5). In most cases, we have a target per occupation or age range (see Appendix C).
3.4
To minimize this fitness function, we apply the evolutionary algorithm CMA-ES (Hansen & Ostermeier 2001), which is one of the most powerful algorithms to solve this kind of problem (Auger & Hansen 2012). CMA-ES means Covariance Matrix Adaptation Evolution Strategy. The principle of this evolutionary algorithm is to test stepbystepnewgenerationsofpointsintheparametersspace. Eachnewgenerationofpointsisdrawnstochastically according to the results obtained with the previous generation of points. The mean and the covariance matrix of the distribution of the new randomly drawn points are updated incrementally in order to move towards the best results obtained by previous generations.
3.5
At each *iteration*, the CMA-ES algorithm sets the values of all the 56 parameters. Then, to cope with the stochasticity we have in the model, 48 simulations are run (they are usually called *replications* in a calibration process)
withadiferentseedfortherandomgenerator, andtheoutputsareaveragedoverthese48simulationstoobtain the fitness value of the iteration. We stop the calibration when the fitness does not improve (same minimum value) for 500 iterations.

3.3
为了校准这56个参数，我们需要最小化一个“适应度”函数，该函数是我们模型输出与2014年法国劳动力市场真实目标之间的相对差异的加权和（来自INSEE和DARES提供的多个来源）。我们选择了63个目标，分为10个不同的类别：失业率（7个目标）、活动率（6个）、工资（14个）、就业流动（12个）、固定期限合同（4个）、长期失业（3个）、职业间流动性（12个）以及其他附加指标（兼职、空缺、在职搜索者、培训成本）（5个）。在大多数情况下，我们每种职业或年龄段都有一个目标（详见附录C）。

3.4
为了最小化这一适应度函数，我们采用CMA-ES进化算法 (Hansen & Ostermeier 2001)，这是解决此类问题中最强大的算法之一 (Auger & Hansen 2012)。CMA-ES代表协方差矩阵自适应进化策略。该进化算法的原理是在参数空间中逐步测试新一代点。每一代新点都根据前一代点所得到的结果进行随机抽取。新随机抽取点分布的均值和协方差矩阵会逐步更新，以向前几代所得到的最佳结果靠拢。

3.5
在每次迭代中，CMA-ES算法设置所有56个参数的值。然后，为了应对模型中的随机性，在校准过程中运行48次模拟（通常称为“复制”），每次使用不同的随机数种子，并将输出结果在这48次模拟中进行平均，以获得该迭代的适应度值。当适应度在500次迭代中没有改善（达到最小值）时，我们停止校准过程。

## Computational Power Needs



3.6
The calibration process is costly in terms of computational resources, because the total number of simulations can be quite high: it is given by the product of the number of iterations by the number of replications. With WorkSim, it took 2000 iterations to converge, and as stated above each iteration is made of 48 replications. Each replication takes about 1-2 minutes overall and the whole calibration process takes around two days to be completed on a processor with 48 cores.

3.6
从计算资源的角度来看，校准过程非常耗费，因为模拟的总次数可能相当高：即迭代次数乘以复制次数。使用WorkSim进行校准时，需要进行2000次迭代才能达到收敛，正如前文所述，每个迭代包含48个复制。每个复制总共需要大约1-2分钟的时间，整个校准过程在一个拥有48个核心的处理器上大约需要两天才能完成。

## Results Of The Calibration On The Main Targets



3.7
We obtain an averagerelative spreadbetween allthe outputsof ourmodel andthe real targetsof 7.9%. This can be deemed satisfactory for such a large non-linear model. We deal with a multi-objective optimization problem with many targets and parameters, and these problems are known to be hard to solve. The calibrated values of the parameters and the outputs of Worksim are shown in Appendix C (Tables 5 and 6 for the targets and Tables 7 and 8 for the parameters).

3.7
我们的模型输出与真实目标之间的平均相对差异为7.9%，这一结果对于如此庞大的非线性模型来说是令人满意的。我们面临着一个具有多个目标和参数的多目标优化问题，而这些问题被公认为难以解决。附录C中展示了参数的校准值和Worksim的输出结果（目标表格5和6，参数表格7和8）。

## Results And Policy Experiments



4.1
In this section, we summarize the main results from a set of experiments we conducted with WorkSim. In this set, the model was calibrated to account for French data in 2014. Note that each experiment result is averaged over 200 simulations.

4.1
在本节中，我们总结了我们使用WorkSim进行的一系列实验的主要结果。在这个实验集中，模型被校准以考虑2014年法国的数据。请注意，每个实验结果是基于200次模拟的平均值。

## A Brief Characterization Of The French Labor Market



4.2
We first comment on some calibrated parameters. We do it briefly since most of them do not have known empirical counterparts (Tables 7 and 8). Several concern the labor supply and careers. In order to start to search for a job, the expected utility must be at least 26% higher than his present utility, a jump high enough to avoid repetitive moves between unemployment and inactivity. An unemployed starts losing human capital afer 8 months, a delay which makes sense although data are missing. Then the rate of decrease is 0,93% per week,
which appears a very high rate. The decline in reservation utility Ru3 is 20% per year of unemployment, a high
rate, allowing for the acceptance by former OEC workers of FTC jobs afer some time. However they are much more reluctant to look for jobs in the next lower broad occupation since it takes almost 4 years to accept this downgrading. The probability to look for a better occupation is higher at 1.4% per week. The wage careers
are increasing and only slightly concave in general experience, since we do not consider the ceiling efect that obsolescence of human capital and illness or fatigue put on blue collars. However the managers do obtain a steeper career than intermediate level workers and blue-collars. Internal promotions from a broad occupation to another is low since it takes an average of 10 years. These figures are in agreement with the low social mobility in the French society in the XXIth century, compared to the previous century. On the employer's side, a major parameter is the weight of the pessimistic scenario in the anticipation of demand. At 78.9%, it dominates the two other scenarios (neutral and optimistic), and means that the employers have a strong aversion to loss, which will deserve a sensitivity analysis below. Tolerance to a worker's underproduction is fairly large at 80%, but within the bounds we have set. The parameter of the labor share in productivity ζ may look very low at 29%, but the ratio concerns net wages and, if it is computed at the aggregate level in the model, it is higher since the workers at the minimum wage earn a higher share of their productivity, and then it matches the real French figure. Finally the profit threshold under which firms may layof on economic grounds without too much legal risk PT is -22%, a loss, and clear evidence of *serious economic dificulties*.

4.2
首先，我们对一些校准参数进行简要评论。由于大多数参数没有已知的实证对应物（表7和表8），我们将简要概述。其中几个与劳动力供应和职业生涯有关。为了开始寻找工作，预期效用必须至少比目前效用高出26％，这样可以避免在失业和非活动之间反复转换。失业者在8个月后开始丧失人力资本，这个延迟是合理的，尽管缺乏数据支持。然后每周的降低率为0.93％，这似乎是一个非常高的速度。失业期间预留效用Ru3每年下降20％，这是一个较高的速度，使得原OEC工人在一段时间后接受FTC工作成为可能。然而，他们更不愿意寻找下一个较低广义职业的工作，因为接受此种降级需要近4年时间。寻找更好职位的概率每周增加1.4％。薪资生涯通常随着经验增长而增加，并且总体上只是轻微凹曲，因为我们没有考虑蓝领工人所面临的人力资本过时、疾病或疲劳带来的限制效应。然而，经理们的职业生涯比中级工人和蓝领工人更为陡峭。从一个广义职业晋升到另一个广义职业的内部晋升率很低，平均需要10年时间。这些数据与21世纪法国社会的社会流动性较低是一致的，与上个世纪相比。在雇主方面，一个重要参数是对需求预期中悲观情景的权重。在78.9％时，它主导了其他两种情景（中立和乐观），这意味着雇主对损失有很强的厌恶，在下面将进行敏感性分析。对于员工产量不足的容忍度相当大，达到80％，但仍在我们设定的范围内。劳动力份额在生产率中所占比例ζ可能看起来非常低，只有29％，但该比例涉及净工资，并且如果在模型中以总体水平计算，则较高，因为最低工资者获得了更高比例的生产力，并与实际法国数据相匹配。最后，在没有太多法律风险下企业可以基于经济原因裁员的利润阈值PT为-22％，即亏损，这是*严重经济困难*的明确证据。

4.3
The targets in Tables 5 and 6 are reasonably well fitted for our purpose. The unemployment rate and the activity rate are especially important for the model and well fitted. However the long term unemployment is under the targets, but it should be mentioned that the measure of unemployment tenure is given in the French labor force survey by the worker, who may forget very short contracts during a long spell of unemployment. The flows are also essential but dificult to calibrate since in our labor flows comprehensive system, they are interdependent and therefore determined by the complete set of behavioral parameters and legal constraints. The results can be deemed satisfactory. Economic layofs are very low at 0.47% per year, since they are very costly in France before the ELK law, much lower than the layofs for insuficient productivity, the exits at the end of the trial period, or the quit rate.
4.4
The model generates some important specific characteristics of the French Labor Market such as the very important share of FTC in terms of total entry flows, 80 %, and the contrasting fairly low figure of the share of the workers employed in such contracts: only 10%. The unemployment of the young is also much higher than the unemployment of the older workers. These results reproduce the known stylized facts of the French Labor Market, and the targets. These major stylised facts are not imposed by the assumptions of the model but
emerge from the interactions of the agents during the simulation, given the calibration of the parameters on a
large number of targets.
4.5
This confirms the dualism in the French Labor Market, which is displayed by the diferences in the patterns of grossflowsofthecategoriesofworkers. Themodelcomputesallthesimulatedflows, butallowsforcomparison with those which can be measured by the published statistics, and the results fit roughly. Most workers are stable in their OEC, while a minority undergoes short spells of employment in FTC and spells of unemployment between them. Moreover this dualism persists for a small proportion of young workers. The others obtain more stable OEC. It can be in the same firm in which they had an FTC through the experience (human capital) gained in FTC, as well as a screening process since the employers gather more precise information on their
kernel productivity. This is a significant gross flow in the model. It can be through direct recruitment in OEC in other firms as the result of their increased experience.
4.6
Many more results are obtained, some of them novel in the sense that we simulate the entire gross flows matrix of labor while only some of the flows are documented in the statistics. They will not be detailed here, due to lack of space and the focus of the presentation of the results on the sensitivity of the main variables to the parameters, and on policy design.

4.3
表5和表6中的目标对我们的研究目的非常适合。失业率和活动率对于我们的模型来说尤为重要，并且拟合得很好。然而，长期失业率低于目标值，但需要指出的是，在法国劳动力调查中，失业期限是由工人自行提供的，他们可能会在长时间失业期间忽略非常短暂的雇佣合同。流动性也是至关重要的，但由于在我们的劳动力流动综合系统中它们相互依赖，并且受到完整行为参数和法律约束集合的影响，因此很难进行校准。总体而言，我们得到了令人满意的结果。经济裁员率非常低，每年仅为0.47％，这主要归因于在ELK法实施之前，在法国进行经济裁员非常昂贵。相比之下，由于生产力不足、试用期结束后离职或主动辞职等原因导致的离职率要高得多。

4.4
该模型呈现了法国劳动力市场一些重要特征，例如以总入口流量计算FTC所占比例非常高达80％，而从事此类合同工作的工人所占比例相对较低，仅为10％。年轻人的失业率也远高于老年工人。这些结果再现了法国劳动力市场已知的刻板事实和目标。这些主要刻板事实并非是模型假设所强加的，而是在模拟过程中主体之间的相互作用下产生的，通过对大量目标进行参数校准得出。

4.5
这证实了法国劳动力市场存在二元性，表现为不同类别工人流动模式之间的差异。该模型计算了所有模拟流动，但也允许与公布统计数据进行比较，并且结果基本吻合。大多数工人在他们所处的OEC（职业、雇佣和合同）上保持稳定，而少数工人则在FTC（固定期限合同）就业期间经历短暂就业和失业期间。此外，这种二元性在一小部分年轻工人中仍然存在。其他工人通过在FTC中积累经验（即人力资本）以及雇主获取更精确有关其核心生产力信息的筛选过程，在同一家公司中获得更稳定的OEC。这是模型中一个重要的总体流动。此外，他们也可能通过在其他公司获得的经验增加直接进入OEC。

4.6
我们获得了更多结果，其中一些结果是新颖的，因为我们模拟了整个劳动力总体流动矩阵，而统计数据只记录了其中一部分流动。由于篇幅有限，并且本文重点关注主要变量对参数的敏感性和政策设计，因此不会详细介绍这些结果。

## Sensitivity Analysis



4.7
In order to validate the mechanisms at play in the model, we undertake the sensitivity analysis of some important parameters. The sensitivity analysis consists in launching a set of simulations by changing each time the value of a parameter while the others remain at their calibrated value. For each point, we measure the outputs of the model afer 104 periods (2 years) starting with the baseline calibrated model. We examine three types of parameters having a substantial impact on unemployment. First, we study the impact of a major parameter for individual's choice: the base preference for free time. Secondly, we analyze a parameter playing an important role in unemployment theory and relating to workers' behavior, the rate of decrease of the reservation utility with time spent in unemployment. These two parameters, being the workers' choice, may have a considerable responsibility in unemployment. In a simple aggregate model, a preference of the workers for free time or a reluctance to accept jobs which are not so well paid (or not so stable) as the former job as time goes on, yield more unemployment. A systemic model like WorkSim may yield more nuanced results. Finally, we focus on
one parameter afecting employers's choices between the diferent contracts, relating to the formation of anticipations under uncertainty, a neglected topic in labor market models. The results reveal a huge impact on unemployment. This is in line with the focus of anticipations that macroeconomics now displays.

为了验证模型中的机制，我们对一些重要参数进行了敏感性分析。敏感性分析是通过每次改变一个参数的值，而其他参数保持其校准值不变，来进行一系列模拟。对于每个点，我们在基准校准模型的基础上经过104个周期（2年）后测量模型的输出结果。我们研究了三类对失业率有重大影响的参数。首先，我们研究了一个个体选择中重要参数的影响：对自由时间的基本偏好。其次，我们分析了与失业理论和工人行为相关的一个参数，即随着失业时间增加而预留效用下降率。这两个参数作为工人选择可能在失业中承担相当大责任。在简单的总量模型中，工人对自由时间或者不愿意接受薪水较低（或者不太稳定）但与之前工作相比时间推移产生更多失业。像WorkSim这样系统性模型可能会产生更细致入微的结果。最后，我们关注一个影响雇主在不同合同之间选择、与不确定性下预期形成相关联、劳动力市场模型中被忽视主题的一个参数。结果显示这对失业率有巨大影响。这与宏观经济学现在的关注重点一致。

## Preference For Free Time



4.8
The parameter α0 represents the base mean preference for free time in the computation of the free time parameter α (c.f. Section 2.29 above). The higher this parameter is, the more individuals prefer free time to labor
incomes and the non-monetary characteristics of jobs (see Equation 12 of the utility function). As expected, an
increase of α0, starting from the calibrated value, leads to a substantial decrease in the activity rate and the
employment rate since individuals prefer free time (see Figure 4 below). For the unemployment rate, the expected move is less straightforward since it depends on the relative elasticities of the activity and employment rates to the preference for free time. The figure shows that the unemployment rate comes to a standstill. When
α0 decreases from the calibrated value, the activity rate increases, more individuals want to work, but most of
these individuals do not find a job since total demand is fixed, so that we see an increase in the unemployment rate. To summarize the situation, the efects of a change in the preference for free time are asymmetric (starting from the calibrated value) as far as employment is concerned, bad if the change favors free time, and null if the change disfavors free time. This asymmetry shows that agent-based methodology uncovers nonlinear efects that standard aggregate models would not reveal.

参数α0代表在计算自由时间参数α时的基本平均偏好。该参数越高，个体更倾向于选择自由时间而非劳动收入和工作的非货币特征（参见上文第2.29节中的方程12）。预期如此，从校准值开始增加α0会导致活动率和就业率显著下降，因为个体更倾向于选择自由时间（见下图4）。对于失业率来说，预期变化不那么直接，因为它取决于活动率和就业率对自由时间偏好的相对弹性。图表显示失业率趋于稳定。当α0从校准值减小时，活动率增加，更多个体想要工作，但大部分这些个体找不到工作，因为总需求是固定的，所以我们看到失业率增加。总结一下情况，在涉及就业问题时改变对自由时间的偏好具有非对称性效应（从校准值开始），如果改变有利于自由时间，则效果不佳；如果改变不利于自由时间，则效果为零。这种非对称性表明基于主体的方法揭示了标准聚合模型无法揭示的非线性效应。

## Reservation Utility Decline With Seniority In Unemployment



4.9
In a model that embodies search behavior by the workers, the parameter Ru3 - entering in Equation 13 —
plays a crucial role. It corresponds to the percentage of decline of reservation utility each week spent in unemployment. The higher the value of this parameter, the faster the reservation utility of unemployed decreases in the model. It represents the acceptance of unemployed to revise downwards the minimum utility at which they accept to work, as time elapses. Search theory makes two predictions. First, if the distribution of wages is knowntotheworkerenteringunemployment, andtherateofarrivalofvacanciesinwhichhewouldbeselected, he should not lower his reservation wage. Secondly, if his household income falls unexpectedly over the spell of unemployment, he should lower his reservation wage. Concerning the first prediction, the elasticity of the reservation wage to unemployment seniority in Europe appears to be quite low, and in France, not significantly diferent from zero (Addison et al. 2009).
4.10
This study therefore appears to validate the first prediction of search theory. However, many studies show that workers, afer being laid of, and recovering another job, are subject to a wage loss, which requires that they haveloweredtheirreservationwage. Wethenconsideredthatworkersmaybeoveroptimistic,notnecessarilyin terms of wages, but in terms of the possibility for them to access OEC. Since a worker learns about this dificulty overthespellbybeingnotselectedbyemployers, heacceptsFTCmoreeasily, whichprovidelessstability. Since
stability is a factor of the individual's utility in the model, this means that he decreases his reservation utility. We have then let the calibration decide over the rate of decline, which appears finally as non zero.

4.9
在一个体现工人搜索行为的模型中，方程13中的参数Ru3扮演着至关重要的角色。它代表了失业者每周在失业状态下预留效用的下降百分比。该参数的值越高，模型中失业者的预留效用下降得越快。它反映了随着时间推移，失业者愿意调低接受工作的最低效用水平。搜索理论提出了两个预测。首先，如果失业者在进入失业前已经知道工资分布和他可能被选中的职位到达率，他不应该降低自己的预留工资水平。其次，如果他在失业期间家庭收入意外下降，他应该降低自己的预留工资水平。关于第一个预测，在欧洲地区，预留工资对于失业年限的弹性似乎相当低，并且在法国地区与零没有显著差异（Addison等人，2009年）。
4.10
因此，这项研究似乎验证了搜索理论的第一个预测。然而，许多研究表明，在被解雇后重新找到另一份工作时，工人会遭受薪资损失，这要求他们降低自己的预留工资。因此，我们考虑到工人可能过于乐观，不仅仅是在工资方面，而是在他们能够获得OEC（非全日制）的可能性方面。由于工人通过被雇主拒绝来了解到这种困难，他更容易接受FTC（非全日制）工作，这提供了较少的稳定性。由于稳定性是模型中个体效用的一个因素，这意味着他降低了自己的预留效用。因此，我们让校准决定下降率，并最终显示为非零值。

4.11
Figure 5b shows that the higher the decrease rate of the reservation utility, the lower the unemployment rate, since the unemployed revise faster their reservation utility and accept to apply to a higher number of job ofers. When the reservation utility is rigid, search unemployment becomes a major component of total unemployment, the latter reaching 14% in the model. Such search unemployment is caused by the time that workers take to find a job that satisfies their requirements. It decreases when the reservation utility is more flexible with time elapsed in unemployment. The diference of 4 points in unemployment between the case in which reservation utility is rigid and the calibrated case could suggest that the behavior of unemployed is a major factor of unemployment. However we observe here a non linear efect: it would not decrease by more than one point if the rate of decline doubled beyond the calibrated case, so that a policy forcing unemployed to be less choosy would have a some efect. However it would not solve the unemployment problem, caused by a lack of demand and possibly by employers' requirements as well as the minimum wage. Moreover the decrease in unemployment we can see on the right of Figure 5b is also due partly to a greater discouragement of the unemployed, because we observe a small decrease in the activity rate 5a. When the reservation utility declines, at some level, it falls under the utility of inactivity, and triggers exit from unemployment. There are 122,000 discouraged workers for the highest rate of decline of the reservation utility. Finally the directions of the efects are clear but the sensitivity of unemployment to the rigidity (or flexibility) of the reservation utility to the time spent in unemployment should be lower on the real labor market, since the model underestimates the structural mismatches between supply and demand. We have only three broad occupations, hence very large labour segments, inside which only human capital, hiring norms of firms, and reservation utilities of workers matter for matching. Crafs or geography are not obstacles.

4.11
根据图5b显示的情况，预留效用下降率越高，失业率就越低。这是因为失业者更快地修正他们的预留效用，并愿意申请更多的工作机会。当预留效用刚性时，搜索失业成为总失业的主要组成部分，在模型中达到了14%。这种搜索失业是由于工人花费时间来找到满足其要求的工作所导致的。当预留效用随着失业时间的推移变得更加灵活时，搜索失业率会减少。在预留效用刚性和校准情况之间的4个百分点的失业率差异可能表明，失业者的行为是造成失业问题的一个重要因素。然而，我们观察到了一个非线性效应：如果预留效用下降率超过校准情况翻倍，失业率不会下降超过一个百分点。因此，强迫失业者变得不那么挑剔可能会产生一些影响。然而，这并不能解决由需求不足、雇主要求以及最低工资引起的失业问题。此外，在图5b右侧可以看到的减少失业也部分归因于对失业者更大程度上的沮丧，因为我们观察到活动率5a有小幅下降。当预留效用下降到某个水平时，它会低于不活动的效用，并引发退出失业。在预留效用下降率最高的情况下，有122,000名失望的工人。最后，尽管影响方向是明确的，但实际劳动市场上失业对预留效用刚性（或灵活性）和失业时间敏感度应该较低。这是因为模型低估了供需之间的结构性不匹配。在模型中，我们只考虑了三个广泛的职业领域，因此只有人力资本、企业招聘规范和工人预留效用对匹配起作用，而手艺或地理位置并不是障碍。

## Sensitivity To The Pessimistic Scenario Weight In Demand Anticipation



4.12
Employers form anticipations on the future of their own demand, based on past estimated trend and volatility. Bounded rationality leads them to consider only three scenarios, one neutral, meaning the trend remains the same, and two others, one with an upward deviation of 3 standard errors, and one with a downward deviation with 3 standard errors. They give weights to these scenarios which have asymmetric efects on profits since the bad scenario involves possible termination of OEC at a cost. The weights are calibrated and the value of the bad
scenario ω−1 is 78.9%. The domination of this scenario in the anticipations corresponds to an aversion to the
loss (see Equation 23).
4.13
Wethenvarythecoeficientω−1,theothercoeficientsremaintotheircalibratedvalueandthethreeofthemare
re-normalized in order to make them sum to one. When ω−1 increases, the employers reduce their hires on OEC
in favor of more hires in FTC (Fig. 6a). Termination costs of OEC are so much higher than those undergone when having to pay an FTC until the end of his contract while he is producing in excess of demand. The employers also hire increasingly on short FTC of one week (Fig. 6d), because these contracts are the least risky in case of future decline in demand. The role of bufer of the FTC against the uncertainty is then highlighted by this experiment.
4.14
A reduction of this parameter could have a substantial impact on unemployment (Fig. 6c). In a hypothetical scenario, if it is set at the value of 0, the unemployment rate falls to the value of 5.13%. It highlights the importance to take into account psychological factors determining the employers' behaviors in an economic model, as suggested by Keynes and recent Nobel prizes G. Akerlof and R. Shiller (Akerlof & Shiller 2009). These factors have a very strong impact on the choice of contract, FTC or OEC, and then on the functioning of the labor
market.
4.15
Thefactthatcompaniesaresensitivetouncertaintyaboutdemandhelpsexplainhowtheywillreacttoachange in labor market legislation, in particular with the ELK law (see the following section). The aversion to the risk of having to pay significant redundancy costs in the event of a fall in demand can limit part of the job creation with OEC contracts. With a sofening of dismissal conditions, we therefore expect a higher rate of OEC contracts on the labor market.

4.12
雇主根据过去的趋势和波动性来预测自身需求的未来情况。由于有限理性，他们只考虑三种情景：一种是中立的，即趋势保持不变；另外两种是上升偏差和下降偏差，分别为3个标准误差。这些情景对利润产生非对称影响，因为糟糕的情景可能导致OEC终止并带来成本。根据权重进行校准，其中糟糕情景ω−1的权重为78.9%。预期中这种情景的主导反映了对损失的厌恶（见方程23）。

4.13
当变量ω−1增加时，其他系数保持其校准值，并重新归一化这三个系数使它们总和为1。随着ω−1的增加，雇主减少对OEC的招聘，并更多地招聘FTC（图6a）。与在合同结束之前支付FTC所承受的成本相比，在OEC终止时所需支付的成本要高得多，而此时他们正在超出需求进行生产。面对未来需求下降风险时，雇主还会越来越多地招聘一周短期的FTC（图6d），因为这些合同风险最小。这个实验突出了FTC对不确定性的缓冲作用。

4.14
减少该参数可能对失业率产生重大影响（图6c）。在假设情景下，如果将其设置为0，失业率将降至5.13%。这凸显了在经济模型中考虑决定雇主行为的心理因素的重要性，正如凯恩斯和近年来获得诺贝尔奖的G·阿克洛夫和R·希勒所建议的那样（阿克洛夫和希勒2009年）。这些因素对于合同选择（FTC或OEC）以及劳动市场运作具有非常强大的影响。

4.15
公司对需求不确定性敏感有助于解释他们将如何对劳动力市场立法变化做出反应，特别是ELK法律（见下一节）。由于担心需求下降时需要支付巨额裁员成本，可能会限制OEC合同创造就业机会的一部分。通过放宽解雇条件，我们预计劳动力市场上OEC合同比例会更高。

## Assessment Of Some Labor Public Policies



4.16
We have conducted several simulation of labor policies, and since most of them had not been implemented at the time of the study, nothing was known on their efects at the moment of the decisions. In fact, one of the major purpose of WorkSim is to be a prototype for a generation of new models which advice policy decisions on employment and labor, by simulating them ex-ante and understanding the efects of one particular policy, or, better, joint policies. This requires structural model building because complex interactions occur.

4.16
我们进行了几次劳动力政策的模拟研究，然而由于大多数政策在研究进行时尚未实施，因此在决策时对其效果一无所知。实际上，WorkSim的一个主要目标是成为新一代模型的原型，通过对就业和劳动力进行先期模拟，并理解特定政策甚至是联合政策的效果，以为政策决策提供建议。这需要建立结构模型，因为复杂的相互作用会发生。

## Reduction Of Social Charges



4.17
Thelevelofsocialchargesonemploymentisfrequentlydiscussed,especiallybyemployers'syndicates. In2003, French Minister F. Fillon has passed a law that reduces the charges paid by the firms on wages, for salaries lower
than 1.6 times the minimum wage (SMIC)33. The decrease is 26 % for firms with 20 employees or more, and 28.1
% for the others. To study the efect of this policy, we compared the results of the baseline experiment34 with a new experiment in which these reductions of charges are removed. We measured a drop of 0.72 points in the unemployment rate, and a gain of 233,000 jobs, thanks to the reduction of charges. This result sets the gain within the range of the empirical studies on this policy, with between 200,000 to 400,000 jobs created or saved
(Ourliac & Nouveau 2012). This experiment may be compared to ex post results has, beyond its intrinsic interest, the advantage of giving some validation to the model.

4.17
社会保险费对就业的影响经常受到讨论，特别是雇主工会。2003年，法国部长F. Fillon通过一项法律，减少了企业在工资上支付的费用，适用于低于最低工资（SMIC）的1.6倍的薪水。对于拥有20名员工或更多员工的企业，费用减少了26％；对于其他企业，则减少了28.1％。为了研究这项政策的效果，我们将基线实验结果与取消这些费用减免的新实验进行了比较。由于降低社会保险费用，我们测得失业率下降0.72个百分点，并增加23.3万个就业岗位。这个结果使得该政策在经验研究中所取得的成果范围内，在创造或保存20万至40万个就业岗位之间（Ourliac＆Nouveau 2012）。这个实验可以与事后结果进行比较，并且除了其本身具有固有利益外，还具有为模型提供一些验证的优势。

4.18
However, it might be more eficient to target the policy on lower wages. Therefore, we vary the maximum wage which can benefit from the policy, from 1.2 SMIC to 2.2 SMIC. The results are displayed in Table 1 below. It appears that the 1.2 SMIC target gives the most efective policy: the smallest unemployment rate (9.55%), 298,000
more jobs, 253,000 fewer unemployed and also the lowest costs.

然而，将政策针对较低工资可能更为高效。因此，我们对能够从该政策中受益的最高工资进行了变动，范围从1.2倍最低工资（SMIC）到2.2倍SMIC。具体结果如下表1所示。研究结果显示，以1.2倍SMIC为目标的政策效果最佳：失业率最低（9.55%），新增就业岗位29.8万个，减少失业人数25.3万人，并且成本最低。

| Indicators                                   | 1.2 SMIC   | 1.3 SMIC   |
|----------------------------------------------|------------|------------|
| 1.6 SMIC                                     |            |            |
| 2.2 SMIC                                     |            |            |
| Unemployment rate (%)                        | 9.55       | 9.66       |
| 9.78                                         |            |            |
| 9.83                                         |            |            |
| Number of created jobs (in thousands)        | 298        | 266        |
| 233                                          |            |            |
| 217                                          |            |            |
| Number of avoided unemployed (in thousands)  | 253        | 228        |
| 192                                          |            |            |
| 180                                          |            |            |
| Gross cost per created jobs (in euros)       | 86138      | 94361      |
| 110 729                                      |            |            |
| 119 816                                      |            |            |
| Gross cost per avoided unemployed (in euros) | 101 581    | 110 088    |
| 134 375                                      |            |            |
| 144 445                                      |            |            |

| 指标                                       | 1.2倍SMIC   | 1.3倍SMIC   |
|----------------------------------------------|------------|------------|
| 1.6倍SMIC                                     |            |            |
| 2.2倍SMIC                                     |            |            |
| 失业率 (%)                        | 9.55       | 9.66       |
| 9.78                                         |            |            |
| 9.83                                         |            |            |
| 新增就业岗位数量 (千)        | 298        | 266        |
| 233                                          |            |            |
| 217                                          |            |            |
| 减少失业人数数量 (千)                                                                                                                                                                                                                                                                                                                                                                                 
           
           
           
           
           
           
           
           
             (欧元)       \n\n86138      \n\n94361      
\n\n110729                                     
\n\n119816

## Variant With Ftc Renewable Twice



4.19
We ofer here a new experiment, by studying a policy formulated by the French government and adopted in June 2015 (Rebsamen Law, article 55). It relates to the possibility to renew an FTC twice, but always within the cumulative limit of 18 months. We still keep the assumption made in the model that the renewal of an FTC is of the same duration as the initial duration of the contract. In the evaluation of a new contract, it adds a new option to renew the FTC twice. Hence, the FTC has three potential durations: its initial duration, twice this duration (one renewal) and three times this duration (two renewals), always within the cumulative limit of 18 months.
4.20
The results of this variant are presented in Table 2. It appears that this policy raises the unemployment by 0.25 points, due to a stronger turnover efect of the workforce (+6.67 points). There are fewer entries in OEC (-0.66 points) and more entries in FTC (+7.08 points). It can be explained by the supplementary option of renewal making the FTC more attractive for the employers compared to OEC. In the simulation, the individuals in FTC are less likely to be hired in an OEC at the end of their first contract. This probability decreases from 15% to 14%
because it becomes more beneficial for the employers to renew the contract, knowing that another renewal option remains possible in the future. However we observe that this policy lowers the share of long term unemployed (-1.4 points) by increasing the turnover rate on the labor market, hence recruitment. The objective of the government was to increase the flexibility of labor adjustment to demand change, but this seems to be at the cost of raising unemployment, ceteris paribus (aggregate demand being unchanged).

4.19
本文提供了一个新的实验，通过研究法国政府于2015年6月制定并采纳的一项政策（Rebsamen法案第55条）。该政策允许将固定期限合同（FTC）续签两次，但总累计期限不得超过18个月。我们在模型中保持了一个假设，即FTC的续签期与初始合同期限相同。在评估新合同时，我们增加了一项新选项，即将FTC续签两次。因此，FTC有三种潜在期限：初始期限、两倍于此期限（一次续签）和三倍于此期限（两次续签），总累计期限始终不超过18个月。

4.20
表2展示了这种变体的结果。由于劳动力更高的流动性效应（+6.67个百分点），该政策使失业率上升了0.25个百分点。OEC进入人数减少了0.66个百分点，而FTC进入人数增加了7.08个百分点。这可以解释为由于额外的续约选项使得对雇主来说与OEC相比，FTC更具吸引力。在模拟中，FTC中的个体在第一份合同结束后更不太可能被OEC雇佣。这个概率从15%降低到14%，因为对雇主来说，续签合同更有利，而且未来仍然存在另一次续签的可能性。然而，我们观察到这项政策通过增加劳动力市场的流动率和招聘活动，降低了长期失业人口的比例（-1.4个百分点）。政府的目标是增加劳动力适应需求变化的灵活性，但这似乎是以提高失业率为代价的（其他条件不变，总需求保持不变）。

| Indicators                                      | Reference   | FTC renewable twice   | Diference   |
|-------------------------------------------------|-------------|-----------------------|-------------|
| Unemployment rate (%)                           | 9.78        | 10.03                 | +0.25***    |
| Unemployment rate 15-24 yr (%)                  | 20.88       | 21.01                 | +0.13***    |
| Unemployment rate 25-49 yr (%)                  | 8.4         | 8.72                  | +0.32***    |
| Unemployment rate 50-64 yr (%)                  | 6.84        | 6.92                  | +0.08       |
| Activity rate (%)                               | 66.93       | 66.82                 | -0.11***    |
| Number of employed individuals (in thousands)   | 24 629      | 25 519                | -110***     |
| Number of unemployed individuals (in thousands) | 2672        | 2737                  | +65***      |
| Average net monthly wage                        | 2036        | 2041                  | +5**        |
| Long-term unemployment rate (%)                 | 34.6        | 33.2                  | -1.4***     |
| Turnover rate (%)                               | 45.26       | 51.93                 | +6.67***    |
| Average number of FTC spells                    | 1.97        | 2.2                   | +0.23***    |

| 指标                                       | 参考值   | FTC续签两次   | 差异       |
|------------------------------------------|---------|--------------|-----------|
| 失业率 (%)                                | 9.78    | 10.03        | +0.25***  |
| 15-24岁失业率 (%)                          | 20.88   | 21.01        | +0.13***  |
| 25-49岁失业率 (%)                          | 8.4     | 8.72         | +0.32***  |
| 50-64岁失业率 (%)                          | 6.84    | 6.92         | +0.08     |
| 劳动参与率 (%)                            | 66.93   | 66.82        |-0.11***   |
| 就业人数（千人）                          		|24,629   	|25,519       |-110***    |
| 失业人数（千人）                          		|2,672     	|2,737        	 	  	 	  	 	  	 	  	 	          	   	      	   	      	   	      	   	      	     	       	       	       	       	          	     	         	          	         	          	         	          	         	          	         	        	           	        	           	        	           	        	           	        	          	        	          	        	          	        	         	            	            	             	             	             	             	             	              	              	              	              	               	               	               	               	                	                	                	                 	                 	                 	                 	                 	                 	                   	                   	                   	                   	                   	                   	                       	                       	                       	                       	                       	                           	                           	                           	                           	                           	                           	                           	                           	    	    	    	    	    	        	        	        	        	        	        	         	    	    	   	    	    	   	    	    	   	    	   	    	       	    	       	    	       	    	
平均净月工资                              			2036     			2041           		 +5**      |
长期失业率 (%)                           			34.6     			33.2           		 -1.4***   |
劳动力流动率 (%)                         			45.26    			51.93          		 +6.67***  |
平均FTC合同次数                          		  1.97     			 2.2            	  +0.23***  |

## Evaluation Of The Facilitation Of Dismissals In The El Khomri Law



4.21
The El Khomri (name of the Minister of labor) law has been presented in March 2016 by the French government as the major labor law of François Hollande's presidency. This law has set the war not only on the French political scene, but also between groups of highly recognized French economists such as Philippe Aghion, Olivier
Blanchard, Jean Tirole, or Thomas Picketti and many others who have not hesitated to take a categorical position in favor or against it. Its final version was voted on July 21, 2016. There are many articles in the law, and several would be very dificult to implement in the model such as a much higher possibility to bargain within the firms for instance. Here we focus on the facilitation of the economic dismissals, considered as one of the main elements of the law, as it is likely to have an important impact on the labor market. The aim of the government was to encourage the employers to hire on OEC since dismissals would require less stringent but also more precisely defined economic conditions, hence less uncertainty on the industrial courts decisions in case of litigation and lower severance costs.
4.22
In the El Khomri Law (ELK), article 30, the conditions to allow economic dismissals are explicitly specified. The economic conditions and therefore the delay change. Economic dismissals are allowed in case of a decline either in the firm's demand or its turnover, computed over a certain period of time, which depends on the firm's size. For firms under 11 employees, the period is 1 quarter, for those between 11 and under 50 the period is 2 quarters, for firms between 50 and under 300, the period is 3 quarters, and for firms with 300 employees or more the period is 4 quarters. The law therefore sofened the former conditions for economic dismissals, which
implied that firms had to undergo *serious economic dificulties* to be allowed to fire. Let us keep in mind that we
formalised in a simple and rough way the jurisprudence before the law as the requirement for firms to undergo losses during one year. However, even if respecting this condition, the employers could be taken to industrial courts. They could then be ordered to pay a much higher severance pay than computed by applying the regular indemnitiesbyjudges, ifthelatterestimatedthattheeconomicdificultieswerenotseriousenough, orthelegal procedures not perfectly respected (advance notice,...), and the fires unjustified.
4.23
Inthereferenceexperimentwithoutthelaw,wehadintegratedtheanticipatedsupplementarycosts,takinginto account the probabilities to lose in courts, and the mean extra severance pay. For experiment with the ELK law, for the period afer the ELK law was passed, we have modeled the new conditions and we have suppressed the litigation costs. The real data justify ex post this assumption since they show that the legal conflicts over fires have strongly declined since the law was passed. The French controversy indeed focused on the facilitation of dismissals, but more specifically on the decrease of the litigation risks. Aghion et al. (2016) supported the clearer conditions for dismissals and the consequent diminution in the litigation risk and costs as an incentive for the employers to hire on OEC, but did not mention adverse efects such as the increase of unemployment that faster adjustment to a decrease in firm own demand can generate. Both increases in hire and in economic fires are predicted by theoretical models of firing costs (see Bentolila et al. (2019)), with no clear prediction on the net efect on unemployment. The empirical evidence is mixed (Boeri et al. 2011). Askenazy et al. (2016) argued on theses bases that firing costs have not been proved to be a source of unemployment in Europe, that
restrictive fiscal policy was the source of unemployment, and that FTC should be severely restricted to diminish the segmentation on the French labor market. Our model studies the French labor market as a complex system in which the El Khomri law modifies the rules of the game, and the results are more complex than in the quoted
papers which are not based on models35.

4.21
法国政府在2016年3月提出了El Khomri法案，将其视为弗朗索瓦·奥朗德总统任期内的主要劳动法。该法案不仅在法国政治舞台上引起了争议，还在一些备受认可的法国经济学家群体之间引发了争论，如菲利普·阿吉翁、奥利维尔·布兰查德、让·蒂罗尔或托马斯·皮凯蒂等人，他们对该法案毫不犹豫地表明了自己的立场。最终版本于2016年7月21日通过投票通过。该法案中有许多条款，在实践中可能非常困难实施，例如更高程度上允许企业内部进行谈判。我们在这里关注促进经济解雇的便利化措施，因为这被认为是该法律的主要要素之一，并且可能对劳动市场产生重要影响。政府的目标是鼓励雇主从事以经济条件为基础的招聘，因为解雇将需要更宽松但也更明确定义的经济条件，从而在诉讼案件中减少对工业法庭决定的不确定性和降低解雇费用。

4.22
在El Khomri法案（ELK）中，第30条明确规定了允许经济解雇的条件。经济条件和延迟时间发生变化。在公司需求或营业额下降的情况下，可以进行经济解雇，并根据公司规模计算一定时期内的数据。对于员工人数少于11人的企业，该时期为1个季度；对于员工人数在11至50人之间的企业，该时期为2个季度；对于员工人数在50至300人之间的企业，该时期为3个季度；对于员工人数超过300人的企业，该时期为4个季度。因此，该法律放宽了以前关于经济解雇的条件，以前要求企业必须遭受严重经济困难才能被允许进行解雇。请记住，在法律出台之前我们以简单粗略方式将法院判例形式化为企业必须连续一年亏损。然而，即使满足这一条件，雇主仍可能被送上工业法庭。如果后者认为经济困难不够严重或法律程序没有完全遵守（提前通知等），他们可能被要求支付比法官计算的常规赔偿金高得多的解雇费用。

4.23
在没有该法律的参考实验中，我们已经考虑了预期的额外成本，包括在法院败诉的概率和平均额外解雇费用。对于通过ELK法案后的时期，我们模拟了新条件，并取消了诉讼成本。实际数据事后证明了这一假设的合理性，因为它们显示自该法律通过以来，与解雇有关的法律冲突大幅减少。事实上，法国争议主要集中在解雇便利化上，但更具体地是降低诉讼风险。阿吉翁等人（2016年）支持更明确的解雇条件以及由此带来的减少诉讼风险和成本作为鼓励雇主从事以经济条件为基础的招聘的激励措施，但未提及快速调整企业自身需求下降可能带来增加失业率等负面影响。根据解雇成本理论模型（参见Bentolila et al. (2019)），既有对员工的招聘增加，也有经济解雇的增加，对失业率的净影响没有明确预测。经验证据存在不一致（Boeri et al. 2011）。Askenazy等人（2016年）根据这些基础论证称，在欧洲，解雇成本并未被证明是失业的原因，而紧缩财政政策才是失业的原因，并且应该严格限制FTC以减少法国劳动市场上的分割。我们的模型将法国劳动市场视为一个复杂系统，在其中El Khomri法修改了游戏规则，并且结果比引用论文中更为复杂，后者并未基于模型35。

## Efects Under A Stable Aggregate Demand



4.24
To begin with, we simulate the ELK law for a steady state of the exogenous aggregate demand36. The ELK law
yields efects which change over time afer the introduction of the law. They evolve during the first 3 years to stabilize afer 4 years. This comes from the fact that it takes time for the firing conditions to be filled even under the new law. The immense majority of French firms are small or very small, and it takes time for such firms to face a cumulated change large enough to be allowed by the new law to fire at least one employee. The results are displayed in Table 3.
4.25
The law has no aggregate efect on the unemployment rate or the employment rate. Hires on OEC increase to reach 28% but the rate of exit increases in an identical manner. This is in accord to the empirical results as mentioned. However the law has strong distributive efects. It is very favorable to the young (15-24), both in the short and the long run, with a decline in unemployment of 148,000 afer 4 years (it drops over 5 points). The impact is notsignificantfortheprimeageclass(25-49). Afer2years, thereisasmalldecreaseinunemployment (-53,000) and an increase in employment (+71,000). However afer 4 years the law has no significant efect on
this age class. Finally the seniors (50-65) undergo a substantial rise in unemployment (+101,000), rising from 6.6 to 8%, i.e. 1.4 points, and a decrease in employment (-121,000).

4.24
首先，我们对外生总需求稳态下的ELK法进行了模拟。引入该法律后，其效应会随时间变化。在前3年内，这些效应逐渐演变，并在4年后趋于稳定。这是因为即使在新法律下，填补解雇条件也需要时间。绝大多数法国企业都是小型或者非常小型的企业，这些企业需要时间才能面临累积变化足够大以满足新法律允许至少解雇一名员工的要求。结果显示在表3中。

4.25
该法律对失业率或就业率没有整体影响。OEC上的招聘增加到28%，但离职率也以相同方式增加。这与经验证据一致。然而，该法律具有明显的分配效应。它对年轻人（15-24岁）非常有利，在短期和长期内都能减少失业人数14.8万人（降低超过5个百分点）。对于主力年龄群体（25-49岁），影响不明显。2年后，失业人数略微减少（-5.3万），就业人数增加（+7.1万）。然而，在4年后，该法律对该年龄群体没有显著影响。最后，老年人（50-65岁）的失业人数大幅上升（+10.1万），从6.6%上升到8%，即增加了1.4个百分点，并且就业人数减少（-12.1万）。

4.26
Moreover, the mobility on the labor market is found to change very deeply, and the nature of the labor market is then transformed:
1. The share of FTC in the hires falls from 77% to 30%. The OEC becomes the dominant hiring contract.
2. thehiringrateinOECdoubles, aspredictedbyeconomicanalysisasaresultoflowerfiringcosts(Bentolila
& Bertola 1990).
3. The proportion of FTC in ongoing contracts falls from 8% to 2.3%, which makes it a minor contract in
terms of employment share. There is a decrease of the mean duration (renewal not included) from 3.6 weeks to 1.9 weeks. This double change means that FTC are now mainly used by firms having a really bad future demand forecast and no requirement in training for these jobs.
4. The entry rate in FTC falls to a quarter of its value before the law. Hence less training costs for job specific
training are lost.
5. The economic dismissal rate jumps from 0.6% to 19%, a major change in a French labor market which
has been characterized by an extremely low and decreasing economic dismissal rate during the present century. The decreases in the uncertainty of the cost and the delay induce this explosion in the rate. This rise is predicted by economic analysis, but its rate is a surprise. The diminution of hoarding that the high firing delays induced raise the firms' average benefits by 14%.
6. As a consequence of higher dismissals, the OEC become shorter (the median duration of OEC falls from
4.8 to 2 years) and more precarious, as the probability to lose one's job within a year jumps from 8.17 to 13.13 (+4.9 points, +60 % relative increase), and more frequent spells of unemployment for the OEC. This consequence seems to dominate the favourable efects and lead to a small decrease in average utility.
7. The integration of the remaining FTC employees into OEC is improved since the increased turnover on
OEC makes opportunities higher. This result has been also obtained in cross section studies which compare countries with diferent FTC rates (Bentolila et al. 2019).

此外，劳动力市场的流动性发生了深刻的变化，从而改变了劳动力市场的性质：
1. 固定期限合同（FTC）在招聘中所占比例从77%下降至30%。开放式长期雇佣合同（OEC）成为主要的雇佣合同。
2. 预计由于解雇成本降低，OEC的招聘率翻倍（Bentolila和Bertola 1990）。
3. 在正在进行中的合同中，FTC所占比例从8%下降至2.3%，在就业份额方面成为次要合同。平均持续时间（不包括续签）从3.6周减少至1.9周。这种双重变化意味着FTC现在主要被那些未来需求预测非常糟糕且对这些工作没有培训要求的企业使用。
4. FTC的进入率下降至法律实施前值的四分之一。因此，岗位特定培训所需费用减少。
5. 经济解雇率从0.6%上升至19%，这是法国劳动力市场上一个重大变化，在本世纪以来一直以极低且逐渐下降的经济解雇率为特征。成本和延迟的不确定性减少导致了这一率的激增。这种上升是经济分析所预测的，但其速度令人惊讶。高解雇延迟导致储备减少，使企业平均受益增加了14%。
6. 由于解雇增加，OEC变得更短暂（OEC的中位持续时间从4.8年降至2年），更加不稳定，因为在一年内失去工作的概率从8.17上升至13.13（增加4.9个百分点，相对增长60%），OEC出现更频繁的失业情况。这种后果似乎主导了有利影响，并导致平均效用略微下降。
7. 由于OEC上员工流动性的增加，剩余FTC员工融入OEC的机会得到改善。这个结果也在比较具有不同FTC比例国家之间进行横截面研究时得到证实（Bentolila等人2019）。

| Indicators                                       | Reference   |   ELK law | Diference   |
|--------------------------------------------------|-------------|-----------|-------------|
| Unemployment rate (%)                            | 10.37       |     10.26 |             |
| ns                                               |             |           |             |
| Unemployment rate 15-24 yr (%)                   | 27.75       |     21.89 | -5.86***    |
| Unemployment rate 25-49 yr (%)                   | 9.1         |      9.24 |             |
| ns                                               |             |           |             |
| Unemployment rate 50-64 yr (%)                   | 6.62        |      8.03 | +1.41***    |
| Activity rate (%)                                | 70          |     70.16 | +0.16**     |
| Number of employed individuals (in thousands)    | 25 591      |  25681    |             |
| ns                                               |             |           |             |
| Number of unemployed individuals (in thousands)  | 2960        |   2937    |             |
| ns                                               |             |           |             |
| Entry rate in OEC (%)                            | 11.88       |     28.24 | +16.36***   |
| Entry rate in FTC (%)                            | 40.95       |     12.45 | -28.51***   |
| Average individual's utility                     | 229.2       |    222.72 | -6.48***    |
| Average weekly firm benefit (in euros)           | 4133        |   4728    | +595***     |
| Long-term unemployment rate (%)                  | 34.72       |     33.26 | -1.47***    |
| Economic firing rate (%)                         | 0.61        |     19.55 | +18.94***   |
| Probability to loose one's OEC within a year (%) | 8.17        |     13.13 | +4.86***    |

| 指标                                       | 参考值   |   ELK法律 | 差异   |
|--------------------------------------------------|-------------|-----------|-------------|
| 失业率 (%)                            | 10.37       |     10.26 |             |
| ns                                               |             |           |             |
| 15-24岁失业率 (%)                   | 27.75       |     21.89 | -5.86***    |
| 25-49岁失业率 (%)                   | 9.1         |      9.24 |             |
| ns                                               |             |           |             |
| 50-64岁失业率 (%)                   | 6.62        |      8.03***(+1.41)***    |
| 劳动参与率 (%)                                                                                                                                                                            70              70.16(+0.16)**     |
| 就业人数 (千人)                                                25,591          25681        
ns                                              
失业人数 (千人)                                                                         2960            
ns                                               
OEC的进入率 (%)                                                    11.88                                         +16 .36***   
FTC的进入率(%)                                                    40 .95                                         -28 .51***   
平均个体效用                                            229 .2                                         -6 .48***    
平均每周企业福利（以欧元计）                                   4133                                          +595***     
长期失业率 (%)                                          34 .72                                         -1 .47***    
经济解雇率 (%)                                                 0.61                                          +18.94***   
一年内失去OEC的概率 (%) | 8.17                               13.13                              +4.86***

4.27
Two major conclusions can be drawn. First, a significant substitution of the young to the seniors takes place. Secondly the new adjustment rules on the OEC have the logical efect of making the FTC a much less useful flexibility tool for the employers except when demand expectations are very bad and no training required. A main objective of the law is then achieved: the FTC are no longer the mean to get around the dismissal costs of OEC. They serve the legal purpose for which they have been allowed, namely to bufer temporary increases in demand.
4.28
The explanation of the opposed efects over the young versus the other categories is simple. The young were much more ofen than the others in FTC (22% against 7.6% for the 25-49 and 4.9% for the seniors) and benefit from their fall. The efect is enhanced (in the model) by the two efects on the seniors. First these are mainly in
OEC and the latter become much more precarious, so that many seniors are now fired. Second they are then unemployed and employers are reluctant to hire seniors on OEC when training for the job is required since the proximity of retirement makes amortization dificult37. Young compete seniors out. The efects of the ELK
law then go much beyond the higher flexibility of OEC. The law raises the integration of the young into (more precarious) OEC, and this shows that the screening and experience enhancing roles of FTC before the ELK were not a suficient factor of integration for the young. The consequence of the substitution of OEC to FTC, namely the substitution of young workers to seniors, who are penalised, has been overlooked by the non quantitative analysis of the ELK law we mentioned38.

4.27
可以得出两个重要结论。首先，年轻人对老年人的显著替代正在发生。其次，新的临时雇佣合同（FTC）调整规则在除非需求预期非常糟糕且不需要培训的情况下，对雇主来说已经不再是一个有用的灵活性工具。法律的一个主要目标已经实现：FTC不再被用作规避临时雇佣成本的手段。它们正按照其被允许存在的法律目的发挥作用，即缓冲需求暂时增加。

4.28
对于年轻人与其他类别之间相反效应的解释很简单。相比其他人，年轻人更常被雇佣为FTC（22%对25-49岁群体的7.6%，对老年群体则是4.9%），并从其减少中受益。在模型中，这种效应受到了两个影响老年人因素加强。首先，他们主要从事长期就业合同（OEC），而后者变得更加不稳定，导致许多老年人被解雇。其次，在他们失业后，由于退休即将到来使得岗位摊销变得困难，雇主不愿意在需要岗位培训时聘请OEC上的老年员工。年轻人取代了老年人。ELK法律的效应远远超出了OEC更高的灵活性。该法律提高了年轻人（更不稳定）进入OEC的程度，这表明在ELK之前，FTC在筛选和增强经验方面对于年轻人的整合作用并不足够。我们提到过，非定量分析忽视了OEC取代FTC所带来的后果，即对受到惩罚的老年工作者进行年轻工作者替代。

## Sensitivity Of Adjustment To Aggregate Demand



4.29
We now change aggregate demand exogeneously in order to examine if the ELK law influences the efect on unemployment diferently. Figure 7 gives values afer 2 years. It shows that the adjustment of the labor force is predicted to be more important afer the law. First, when demand declines under its value in the reference experiment, economic dismissals are more important, the suppression of the hoarded labor is more complete, and unemployment rises more under El-Khomri's law. The efect reaches 4 points if demand is to fall by 25%. Secondly when demand rises above the reference value, the employers hire more easily on OEC, and unemployment decreases more under ELK law. For a symmetric increase in demand the decrease is 2 points. The responses are not symmetric for large changes since if demand is very high, there always remains some search unemployment caused by workers who raise their reservation utility. This higher sensitivity to demand could be predicted, yet its importance could not be, since FTC were a substantial bufer before the law, but finally less efective than the reduction in dismissal delays for OEC.

4.29
为了研究ELK法对失业的影响是否不同，我们现在通过外生地改变总需求。图7展示了2年后的数值。结果显示，在该法律实施后，劳动力调整变得更加重要。首先，在需求低于参考实验中的值时，经济解雇更为重要，储备劳动力的压制更加完全，ELK法下的失业率上升更多。如果需求下降25%，则效果达到4个百分点。其次，在需求高于参考值时，雇主更容易在OEC上招聘，并且在ELK法下失业率下降更多。对于对称增长的需求增加，减少为2个百分点。由于需求变化较大时反应不对称，因此如果需求非常高，则始终存在一些由提高保留效用的工人引起的搜索失业。这种对需求敏感性较高可以预测到，但其重要性无法预测到，因为在该法律之前FTC是一个相当大的缓冲区域, 但最终比OEC减少解雇延迟效果不明显。

## Discussion



5.1
In this synthetic paper, we present the WorkSim framework, a comprehensive model of the labor market. First thestock-flowaccountingofindividuals, basedongrossflows, iscompleteandendogenous. Itissupplemented by a stock-flow accounting of jobs for further analysis. The institutional environment is modeled and based on labor law, which sets constraints at the agent level on the possible decisions, taking into account the specific characteristics of each agent in his type, worker or employer. Therefore the simultaneous existence of unfavorable characteristics including the agent's history may result in the exclusion of the labor market, a highly non linear efect that cannot be obtained in aggregate models in a realistic manner.
5.2
Secondly it implements numerous essential economic mechanisms that were not integrated before within a single labor market model: search on both sides of the market with multi-jobs firms, inter-temporal decision processes under bounded rationality, anticipations of demand shocks with risk aversion, learning, endogenous contractchoices, endogenoussalariesandproductivities, diferenttypesofhumancapital. Allarefoundtohave major efects on activity, employment and unemployment.
5.3
Thirdly, WorkSim is calibrated on a large number of targets of the French labor market, by using a powerful evolutionary algorithm that has not already been used in economic models. On average and satisfactorily it reproduces these targets to conduct some economic analyses. Moreover, it reproduces the gross flows measured by diferent statistical sources and with diferent types of measures with a fairly satisfactory approximation.
This gives us an estimation of the model accuracy, and is part of the model's *validation process*.
5.4
Fourthly, we have conducted several analyzes and policy evaluations. These helped us to identify some core mechanisms in the French Labor Market: segmentation, screening and bufer roles of FTC, importance of employers' loss aversion, among others. Each labor policy appears to have contrasting results for the diferent categories of workers in terms of employment improvements, benefits and costs. The complexity of the labor markethasnaturallyledustoomitsomemoreorlessimportantinstitutions, andthenumberoftargetsremains small compared to this complexity. The efects of the policies should then be considered with the necessary scientific caution. The results are mainly meant to suggest new mechanisms, and the possibility of some efects
of policies, which has not been highlighted before. One of the main conclusions is that *institutions matter*. Our
agent-based model enabled us to simulate ex-ante efects of various policies, making it a precious tool to help policy design.
5.5
WorkSim in its present state has no equivalent in the agent-based models. These have macroeconomic goals that WorkSim does not have, and set assumptions on the labor market a minima. They mainly play with the wage setting mechanisms, comparing opposed theoretical assumptions such as wage rigidity versus flexibility, as our survey has shown (Dawid et al. 2013, 2018; Dosi et al. 2020), and obtaining the standard macroeconomic stylised relations such as the Beveridge curve, the Phillips curve, and Okun's curve. Devoided of a complete macroeconomic setting, WorkSim has not such goals. Those models who are closer in spirit to WorkSim as they are interested in the structure of the labor market, study specific mechanisms such as networks (Tassier & Menczer 2001; Pingle & Tesfatsion 2004). They have theoretical purposes and do not intend to model the mechanisms of a real labor market. Reproducing the main mechanisms of such a real market and their interactions requires a framework rich enough: an heterogenous population of individuals and households with a demographic module, the 3 main states (employment, unemployment, inactivity), the gross flows system, some main institutions like the diferent contracts, the minimum wage and benefits (and some others), some main constraints that labor law imposes, and finally, a calibration algorithm. The only agent-based models with such an agenda are our own previous models. ARTEMIS (Ballot 1981, 2002) presented such a model but was calibrated by hand. The first version of WorkSim was calibrated by the powerful algorithm CMA-ES that we described. Goudet et al. (2017) present the model, and Goudet et al. (2015); Ballot et al. (2016b) study policy
experiments. In ARTEMIS and the first version of WorkSIm the choice between OEC and FTC was exogeneous39.
The present paper provides a major improvement, by making the choice between permanent jobs (OEC) and temporary jobs (FTC) completely endogeneous.
5.6
Then the meaningful comparison is between WorkSim and the analytical search models of a dual labor market, which have gross flows between the employment and the unemployment states (the inactivity state is missing). Only one, (Cahuc et al. 2016), features a truly endogenous choice between OEC and FTC. The two models have at least two essential diferences. There is first a fundamental conceptual diference between independent expected shocks on individual jobs in Cahuc et al. (2016) and the global demand shock for a multi-jobs firm in WorkSim. The second diference lies in the types of costs when ending a job. In Cahuc et al. (2016), FTC cannot be extremely short because there is a cost of writing a contract. This cost is calibrated as 0.8 hour of production, significant enough to preclude extremely short contracts in the model. These would reduce to almost zero the possibility of a demand shock before they end, and could be repeated to compete out OEC 40. In fine an exogenous Poisson distribution of projects durations must determine the mix of contract types, if one repeats the draw for many jobs (the authors do not do this exercise). Our model considers firms which anticipate diferent evolutions of their total demand, weight them through risk aversion, and choose a mix of the two types of contracts: some FTC to avoid the risk of dismissing many OEC and paying advance notice and firing costs, but also OEC because FTC have also important drawbacks: they cannot amortise training costs on a short FTC, they cannot renew the incumbent more than once and undergo a waiting period before re-creating the job. Moreover the present mix of contracts is important for the choice in the dynamic context of the employer's choice since it provides a low or high bufer according to the proportion of present FTC in the employment of the firm. Some results are common to the two models, namely the large ratio of FTC in hires, the lack of sensitivity of aggregate unemployment to firing costs, and the substitution of OEC to FTC if the firing cost is decreased. Yet WorkSim, which is also calibrated to a much larger number of targets than the Cahuc et al. (2016) model, can study in more depth the microeconomic and aggregate efects of the legal rules, as has been done with the ELK
law, andpreviouslywiththe*generationcontract* inBallotetal.(2016b). Ithasalsomadepossibletoconsiderthe heterogeneity of workers, and the divergent efects that a change in the rules induces on them, a fundamental topic when it comes to assess the efects of a policy on the young. This is not only a medium run phenomenon as it could appear in the present paper. Ballot et al. (2016b) have been able to show that a cohort carries over its lifetime policy shocks undergone early, a result obtained by longitudinal studies (Schwandt & Von Wachter 2019), and a major topic since the Great Recession and the Covid.

5.1
本综合论文介绍了WorkSim框架，这是一个全面的劳动力市场模型。首先，我们完整且内生地基于总流量对个体进行库存流量核算。此外，我们还对工作岗位进行了库存流量核算，以进行进一步分析。我们建立了机构环境模型，并根据劳动法制定了对主体层面上可能决策的约束条件，考虑到每个主体在其类型（工人或雇主）中的特定特征。因此，当不利特征（包括主体历史）同时存在时，可能导致劳动力市场排斥的非线性效应在聚合模型中无法以现实方式获得。

5.2
其次，该模型实现了许多之前未在单一劳动力市场模型中集成的重要经济机制：双边市场上的搜索与多岗位企业、有界理性下的跨期决策过程、带有风险厌恶和学习能力的需求冲击预期、内生合同选择、内生工资和生产率、不同类型人力资本等等。所有这些因素都对活动、就业和失业产生重大影响。

5.3
第三，我们使用

## Future Directions



5.7
The model can be extended in several directions. Firstly we can add more labor market institutions and mechanisms: temporary employment agencies, social networks, and lifelong training for instance. We can also integrate more organizational elements, including more detailed competences and tasks based production functions, as well as the monitoring role of the hierarchy. Secondly, WorkSim would benefit from being plugged into an agent-based macro-economic framework, in order to have consumption, investment and financial efects as well (this is work in process). The outcomes on wages and profits have efects which in turn modify aggregate demand and employment. One way to look at this is to assume, as done in this paper, that they are second order efects, but this might not be true.
5.8
Thirdly, tools to help analyzing and explaining the simulations are still to be developed further: visualization (improving the graphical interface in WorkSim), analyses of the agents' decisions, automatic classification of agents'trajectoriestostudyindividuals'careers(cohortanalysis). Anotherissueisthelinkwithmicro-econometrics, to improve the agents' measures of elasticities and enhance the validation process. Fourthly, if the current version of WorkSim is primarily designed to account for the French Labor Market, most of its components and mechanisms could be re-used to describe labor markets in other countries. The elements specific to the French institutions (labor law) can be adapted when dealing with another country.

5.7
该模型可以在多个方向上进行扩展。首先，我们可以增加更多的劳动力市场机构和机制，例如临时就业机构、社交网络和终身培训。我们还可以整合更多的组织要素，包括更详细的能力和基于任务的生产函数，以及层级结构的监控作用。其次，将WorkSim与基于主体的宏观经济框架相结合将会有益处，以便考虑消费、投资和金融效应（这是正在进行中的工作）。工资和利润的结果会对总需求和就业产生影响。从某种程度上来看，在本文中假设它们是二阶效应，但这可能并非如此。

5.8
第三，需要进一步开发工具来分析和解释模拟结果：可视化（改进WorkSim中的图形界面）、分析主体决策、自动分类主体轨迹以研究个体职业生涯（队列分析）。另一个问题是与微观计量经济学之间的联系，以改进主体对弹性度量并增强验证过程。第四，在当前版本中，WorkSim主要用于描述法国劳动力市场，但其大部分组成部分和机制也可以用于描述其他国家的劳动力市场。处理其他国家时，可以调整法国机构（劳动法）的特定要素。

## Acknowledgments



We are grateful to the reviewers for their useful comments and suggestions which helped us to significantly improve the paper.

我们感谢审稿人的有益评论和建议，这些评论和建议帮助我们显著改进了本文。

## Notes



1The main empirical methodology relies on transition probabilities with a frequency no smaller than at least one month. This deletes short term contracts.

主要的实证方法依赖于至少一个月频率的转移概率。这样可以排除短期合同。

2Figure 3 describes the main transitions processes.

2图3描述了主要的转移过程。

3The OEC correspond to the *Contrats à durée indéterminée (CDI)* and the FTC correspond to the Contrats à durée déterminée (CDD).

3 OEC代表无固定期限合同（CDI），FTC代表有固定期限合同（CDD）。

4FTC and other non regular employment are even more important in Spain, Portugal, and Netherlands, according to OECD data (Bentolila et al. 2019).

根据OECD的数据（Bentolila等，2019），在西班牙、葡萄牙和荷兰，FTC和其他非正规就业形式更加重要。

5Temporary help is the subject of a work in process (Ballot et al. 2017).

5临时劳动力是一项正在进行中的研究课题（Ballot等，2017）。

6The exact rules are in Appendix B.

6. 具体规定详见附录B。

7A previous version by Goudet et al. (2017) used an exogenous mix.

7Goudet等人（2017）的先前版本使用了外生混合物。

8This has consequences since a centralized labor market has diferent outcomes from a decentralized labor market. The real labor markets have some intermediaries such as Employment Agencies and temporary help firms, but they should be introduced in a decentralized environment with their specificities.

8这一点具有重要影响，因为集中化劳动力市场与分散化劳动力市场有不同的结果。真实的劳动力市场存在一些中介机构，如就业机构和临时劳动力公司，但它们应该在分散化环境中引入，并考虑到它们的特殊性。

9The search concept is necessary to distinguish the two states of "unemployed" and "inactive" on the basis of rational (boundedly or not) decisions of agents. The unemployed looks for a job and the inactive does not. There is indeed a flow from unemployment to inactivity, because the value in terms of unemployment utility (expected gains from search minus time foregone) may become lower than the utility of inactivity (non wage income, welfare and free time). In that case, the individual stops search and becomes inactive. The reverse can occur. Search costs and not only non wage income influence the choice between inactivity, unemployment and employment. When an agent has decided to search, while on-the-job or as an unemployed, search concepts define stopping rules to be a candidate for a vacant job or not.

为了根据有限或无限理性决策的基础上区分"失业"和"非活跃"两种状态，搜索概念是必要的。失业者寻找工作，而非活跃者则不寻找。实际上，由于失业效用（预期搜索收益减去放弃时间）可能低于非活跃状态的效用（非工资收入、福利和空闲时间），因此从失业到非活跃存在一种流动。在这种情况下，个体停止搜索并变得非活跃。反之亦然。选择是否选择非活跃、失业或就业受到搜索成本和非工资收入的影响。当一个主体决定进行搜索时，在职或者是失业时，搜索概念定义了成为一个空缺职位候选人与否的停止规则。

10For instance an employer, when hiring on an OEC, has more information on a worker with whom she has a FTC contract than on an external candidate, hence FTC can be a stepping stone for OEC.

例如，雇主在使用固定期限合同（FTC）雇佣员工时，对于与其签订了固定期限合同的员工拥有更多信息，而对于外部候选人则了解较少。因此，固定期限合同可以成为进入长期雇佣关系（OEC）的一个过渡阶段。

11For evidence of the bias introduced by a matching function as a result of an employment policy, see (Neugart 2008).

关于由就业政策引入的匹配函数所引起的偏见的证据，请参见（Neugart 2008）。

12Bentolila et al. (2019) confirm this state of the research. They propose a simpler version of the Cahuc et al.

12 Bentolila等人（2019）证实了这一研究状态。他们提出了Cahuc等人的简化版本。

(2016) paper. Several papers had proposed before models of this choice but either the choice is not fully endogenous, or they make assumptions much too far from the French rules to be useful to discuss here. Cahuc et al. (2016) ofer a survey.

（2016）年的论文。之前有几篇论文提出了这种选择的模型，但要么选择不完全内生，要么做出的假设与法国规定相差太远，无法在此进行讨论。Cahuc等人（2016）提供了一份综述。

13Briard (2007) presents a typology of careers based on a large number of individual trajectories which suggestsapersistentsegmentationoverthelifecycle. Befyetal.(2008)showbyuseofeconometricsontransitions that around 5% of prime age population cannot get a stable job.

Briard（2007）在一项基于大量个体轨迹的研究中，提出了一种基于职业的分类体系，该体系表明在整个生命周期中存在着持久的分割现象。而Befy等人（2008）则通过计量经济学方法对转变进行了研究，并发现约有5%的适龄人口无法获得稳定的就业机会。

14This work has spurred an extension by Silva et al. (2012) to distinguish routine and non routine workers, and in a framework with unbiased technical progress, explain the rise of unemployment with a paradoxical rise in ofered wages in some countries such as the US and Portugal.

这项研究激发了Silva等人（2012）的进一步研究，以区分例行和非例行工作者，并在一个具有无偏技术进步的框架下，解释了某些国家（如美国和葡萄牙）中失业率上升与提供工资上升之间的悖论。

15The managing director works full time for the firm, and at the three occupations. The director never leaves the firm, except to retire or when the firm goes bankrupt.

15该董事总经理全职为公司工作，并担任三个职务。除非退休或公司破产，否则该董事总经理从不离开公司。

16*Artifacts* in multi-agent systems are the passive (non-proactive) entities providing the services and functions that make individual agents work together (Omicini et al. 2008), and must be distinguished from proactive autonomous entities like the individuals or the firms.

在多主体系统中，*工件*是被动的（非主动的）实体，提供使个体主体协同工作的服务和功能（Omicini等人，2008），必须与主动的自治实体如个人或公司区分开来。

17N(*µ, σ*) denotes a normal law distribution, with mean µ and standard deviation σ.

17N（*µ，σ*）表示正态分布，其中µ为均值，σ为标准差。

18Therearenowmanystudiesthatsupportallthesethreetypesofhumancapitals(e.g.Kambourov&Manovskii
2009; Crook et al. 2011). It appears as covering better the heterogeneity of skills types than the traditional Beckerian dichotomy between general and firm specific human capitals, and it has important efects on the evaluation of the workers and their selection. For instance mobility between occupations is much less than between jobs in the same occupation, and promoting workers from one job to another may involve some training costs within a firm.

目前有许多研究支持这三种人力资本类型（例如Kambourov和Manovskii，2009; Crook等，2011）。相较于传统的贝克尔区分一般和公司特定人力资本的二分法，这些研究似乎更好地涵盖了技能类型的异质性，并对工人的评估和选择产生重要影响。例如，在职业之间的流动性远远小于同一职业内部工作之间的流动性，并且将工人从一个职位提升到另一个职位可能会涉及公司内部的一些培训成本。

19The firm does not want to destroy the job, if there is still a potential demand margin for it, so it becomes a pending job. We have here an important feature of WorkSim: unlike other models, we distinguish the job and the contract, several employees (and therefore several contracts) may have occupied the same job since its creation.

19. 如果仍存在潜在的需求边际，公司不愿意废除该职位，因此它将成为一个待定职位。这是WorkSim的一个重要特点：与其他模型不同，我们将工作和合同区分开来，自从其创建以来，可能有多个员工（因此也有多个合同）占据了同一个职位。

20using estimates of Phillips's curves would be inappropriate in the context of an economy with fixed prices, and downward rigid incumbents' wages.

20. 在价格固定、下行僵化的经济环境中，使用菲利普斯曲线的估计是不合适的。

21The labor cost represents here the capital funds the firm has to pay in advance. Hence, the return is the ratio of the profit over this capital.

21. 这里的劳动成本代表了公司需要提前支付的资本资金。因此，回报率是利润与这个资本之间的比率。

22Wekeepthenumberoffirmsconstantfortwomainreasons. First, wedonotaimtomodelthedeterminants of firm creation, way too complex and out of the scope of WorkSim. Secondly, we are looking for a stationary state with a scale-up for year 2014, to apply and assess policies, and this will not be possible if the number of firms evolves constantly.

22. 保持公司数量恒定有两个主要原因。首先，我们不打算对公司创立的决定因素进行建模，因为这一过程过于复杂且超出了WorkSim的范畴。其次，我们追求一个稳定状态，并在2014年实现规模扩大，以便应用和评估政策。然而，如果公司数量不断变化，这一目标将无法实现。

23This tolerance has necessarily a minimum, and a maximum < 1 to ensure a non-zero tolerance. Moreover, if ρ is too high, it will create a lot of dismissals and the firm will run a higher risk to face litigation and a higher risk to lose if it underestimated the real employee's productivity.

23. 这种容忍度必然有一个最小值和一个最大值小于1，以确保非零容忍度。此外，如果ρ过高，将会导致大量解雇，并使公司面临更高的诉讼风险和低估真实员工生产力的风险。

24In absence of empirical data, we assumed this function to be linear.

在缺乏实证数据的情况下，我们假设这个函数是线性的。

25We assume that this training has no duration. One should have in mind that most training in firms is only a few hours.

25. 我们假设这种培训没有时间限制。需要记住的是，大多数公司的培训只有几个小时。

26More precisely amenity and stability are "monetized" for the sake of adding up to income, a fairly standard procedure in economics, which could be justified by enquiries on the "wage reduction" that workers would accept to have more stability or more amenity. Then the "total income " obtained and free time have diferent weights in the utility function.

26. 更为精确地说，为了增加收入，我们将便利和稳定性进行了“货币化”，这是经济学中一个相当常见的做法。通过调查工人愿意接受的工资降低程度以换取更多的稳定性或便利性，我们可以对此进行合理解释。在效用函数中，"总收入"和空闲时间被赋予不同的权重。

27The correlation appears for women in the econometric studies, even if the husband's earnings are made endogenous. In our specification, the man's decisions are also afected by his wife's earnings. These may afect such variables as his reservation utility. Decisions of a partner then depend on the other partner's status by an iterative process which fits well bounded rationality rather than a joint decision as in the game models of family labor supply. A transaction cost ICHANG avoids frequent changes that such an iterative process could induce.

27. 在计量经济学研究中，即使丈夫的收入是内生的，女性之间仍存在相关性。在我们的模型中，男性的决策也受到妻子收入的影响。这可能会影响到他们的保留效用等变量。因此，伴侣之间的决策是通过一个迭代过程来进行的，这更符合有界理性的思维方式，而不是像家庭劳动供给模型中那样进行联合决策。为了避免频繁变化带来的问题，我们引入了一个交易成本ICHANG。

28INSEE Statistics on physiological time in France in 2010 (https://www.insee.fr/fr/statistiques/
1281050#titre-bloc-1)
29The concept of reservation utility (or of reservation wage) is an important concept in labor economics, and more specifically in search theory. It is the equivalent of the hiring norm, for the individual, as it represents the minimum level of utility (or wage) to make it acceptable to an agent. Most models use the reservation wage concept, but then the state *inactive* cannot be endogenous. In WorkSim, if the reservation utility falls below the utility given by the inactivity state, the unemployed stops search.

28. 根据2010年法国INSEE统计数据，对于生理时间的研究显示（https://www.insee.fr/fr/statistiques/1281050#titre-bloc-1）。

29. 在劳动经济学中，保留效用（或保留工资）的概念是一个重要的概念，尤其在搜索理论中。它代表了个体所能接受的最低效用（或工资）水平，相当于雇佣标准。大多数模型都采用了保留工资的概念，但这样一来，“非活跃”状态就不能是内生的。在WorkSim模型中，如果保留效用低于非活跃状态所给出的效用水平，则失业者将停止搜索。

30Ru3 is positive and calibrated on the basis of the French experience. More details are given in the section on the sensitivity experiment on Ru3 . Ru4 is inspired by the evidence of the Addison et al. (2009)'s study that shows that reservation wages in France respond positively and very significantly to unemployment benefits. Since we consider reservation utility, the coeficient 0.5 reflects that its rise is less than the computed change in utilities, as all measures of elasticities show, and based on our ignorance on a precise value between 0 and 1.

30. Ru3是根据法国的经验进行了正向校准。有关Ru3的更多详细信息在对Ru3进行敏感性实验的部分中提供。Ru4受到Addison等人（2009年）研究的证据启发，该研究表明法国的保留工资对失业救济呈现出积极且非常显著的响应。由于我们考虑到保留效用，系数0.5反映出其上升幅度小于计算出来的效用变化，正如所有弹性度指标所示，并且基于我们对0和1之间精确值的不确定性。

31Population in France in 2014 (https://www.insee.fr/fr/statistiques/3137409)
32As we show below, the simulation itself does not take too much time and power to run. The critical point is the calibration as it has to launch thousands of simulations to reach an acceptable solution.

31. 2014年法国的人口数据可参考(https://www.insee.fr/fr/statistiques/3137409)。

32. 如下所示，模拟本身的运行时间和计算资源消耗并不过多。关键在于校准过程，需要进行数千次模拟以达到可接受的解决方案。

33These results are based on a past calibration of the model on year 2011, but there should not be qualitative changes with 2014.

33这些结果是基于对2011年模型的过去校准，但与2014年相比不应有质的变化。

34As noted above, the baseline experiment is performed with parameters set to their calibrated values. One must bear in mind that an experiment result is the average of 200 simulations.

34如上所述，基准实验是使用参数设置为校准值进行的。必须记住，实验结果是200次模拟的平均值。

35Our simulation has been done in April 2016 and presented in newspapers, workshops and working papers shortly afer, and is therefore really ex ante (Ballot et al. 2016a). One could object that in 2019 an econometric study of the efects of the El Khomri law could be undertaken. However the law was only implemented at the beginning of 2017, and the time series would be short. Moreover the main problem would be the elimination of the other shocks and employment policy changes that the economy has undergone since. At the level of the aggregate efects these obstacles may be overcome, but at the level of more disaggregated groups, where we find strong efects, it is more dificult. Finally, given the complexity of the topic, the two methodologies can be regarded as complementary tools when ex post.

我们的模拟研究于2016年4月完成，并随后在报纸、研讨会和工作论文中进行了展示，因此可以说是真正的前瞻性研究（Ballot等人，2016a）。有人可能会提出，在2019年可以进行一项关于埃尔·霍姆里法律影响的计量研究。然而，该法律直到2017年初才开始实施，时间序列较短。此外，主要问题在于消除自那时以来经济所经历的其他冲击和就业政策变化。在总体效应水平上，这些障碍可能可以克服，但在更细分组别水平上发现了强烈效应的情况下，则更加困难。最后，考虑到该主题的复杂性，事后观察和计量方法可以被视为互补工具。

36We used for the ELK experiment in 2016 a scale of 1/2300, half the one in more recent experiments, with a total number of 20,000 agents: 18,300 individuals and 1,700 firms.

我们在2016年的ELK实验中使用了1/2300的比例尺，比最近的实验少一半，总共有2万个主体：其中18300个是个体，1700个是公司。

37The bias against hiring seniors on OEC is very strong in France and statistical discrimination based on alleged risks of health problems, lower motivation, or less ability to cope with change add in employers'decisions to the training problem which is the only one we model.

37在法国，对雇佣年长者的偏见非常严重，基于健康问题风险、动力较低或难以适应变化的统计歧视加剧了雇主对培训问题的决策。

38However a *caveat* on the magnitude of these substitution results is in order. We have assumed that any job can be an FTC or an OEC, even if we take into account that employers should be deterred from FTC when training costs are high. In the real world, some jobs require trust and/or long experience and cannot be FTC, so that substitution is overestimated in the model.

然而，对于这些替代结果的规模需要进行一项重要的限定。我们假设任何工作都可以是临时合同工或外包雇员，即使我们考虑到当培训成本较高时，雇主应该被阻止使用临时合同工。然而，在现实世界中，一些工作需要建立信任和/或具备长期经验，因此无法采用临时合同工的方式进行替代。因此，在模型中对替代效应的估计存在过高的情况。

39However ARTEMIS has an exogeneous choice between primary and secondary jobs, both permanent, and and endogeneous choice between the former jobs and temporary help jobs
40Very short contracts, of a maximum of one day, represent a large part 30% of the FTC contracts in 2017
(DARES 2018). Moreover in some sectors they can be renewed indefinitely without a waiting period or any other cost under the name of customery FTC (*CDD d'usage* in french). We have included these in WorkSim

然而，ARTEMIS在选择主要工作和次要工作之间具有外生选择，并且在前者工作和临时帮助工作之间具有内生选择。

根据DARES（2018）的数据，2017年的临时合同中，非常短期的合同占据了很大比例，达到30%。此外，在某些行业中，这些合同可以无限期地续签，而无需等待期或任何其他费用，这被称为习惯性临时合同（法语中的“CDD d'usage”）。我们已将这些情况纳入WorkSim模型。

## Appendix A: Evaluation Of The Expected Average Profit Per Period Φper I,J,P,Q,C,T Of An Individual On A Job P **With A Contract** C



The weekly profit of a candidate i on a job p, afer d spent periods and for a scenario θ of demand evolution is :
φi,j,p,q,t(*θ, d*) = P × max(0, min (Qi,j,p,q,t(d), ADj,q,t(*θ, d*))) − S*i,j,p,q,t*(d) × SalC
(14)
with

候选人i在职位p上经过d个周期后，在需求演变情景θ下的每周利润为：
φi,j,p,q,t(*θ, d*) = P × max(0, min (Qi,j,p,q,t(d), ADj,q,t(*θ, d*))) − S*i,j,p,q,t*(d) × SalC
(14)

其中，φ表示候选人i在职位p上的每周利润，j表示某个特定的工作，q表示某个特定的需求情景，t表示时间。Qi,j,p,q,t(d)表示候选人i在职位p上在第d个周期时的产量，ADj,q,t(*θ, d*)表示需求情景θ下工作j在第d个周期时的需求量。S*i,j,p,q,t*(d)表示候选人i在职位p上在第d个周期时的供应量调整系数，SalC表示职位p的薪资水平。

以上公式描述了候选人在特定职位上根据供需关系和薪资水平所获得的预期利润。

- Q*i,j,p,q,t*(d) the anticipated productivity of the individual afer d period on the job
- S*i,j,p,q,t*(d) the anticipated salary of the individual afer d period on the job and *SalC* the payroll charges
(in %)
- P is the fixed exogenous price of the good (set to 1 in the simulations)
When summing this profit from the start of period dv (expected vacancy duration) to the end of dc ( expected duration of the contract) and applying the discount rate r, we get the total profit :

- Q*i,j,p,q,t*(d) 表示个体在工作经过d个周期后的预期生产力。
- S*i,j,p,q,t*(d) 表示个体在工作经过d个周期后的预期薪资，*SalC*表示工资单费用（以百分比表示）。
- P是商品的固定外生价格（在模拟中设为1）。
将从dv（预期空缺持续时间）开始到dc（合同预期持续时间）结束的利润求和，并应用贴现率r，得到总利润。

$$\Phi_{i,j,p,q,c,t}(\theta,d_{c})=\left(\sum_{d=1}^{d_{c}}\frac{\phi_{i,j,p,q,t}(\theta,d))}{(1+r)^{d_{v}+d_{c}}}\right)-\frac{EndC_{c}(d_{c})}{(1+r)^{d_{v}+d_{c}}}\tag{15}$$
with *EndC*c(dc), the cost to end the contract (diferent for OEC and FTC).

$$\Phi_{i,j,p,q,c,t}(\theta,d_{c})=\left(\sum_{d=1}^{d_{c}}\frac{\phi_{i,j,p,q,t}(\theta,d))}{(1+r)^{d_{v}+d_{c}}}\right)-\frac{EndC_{c}(d_{c})}{(1+r)^{d_{v}+d_{c}}}\tag{15}$$
其中，*EndC*c(dc)代表终止合同的成本（对于OEC和FTC而言是不同的）。

Then, for a given evaluated contract $c$ the firm chooses the best duration, that is the one that gives the highest profit:

然后，对于给定的评估合同$c$，公司选择最佳的持续时间，即能够获得最高利润的持续时间：

$$\Phi^{*}_{i,j,p,q,c,t}(\theta)=\max_{d_{\text{\tiny{patient}}}\in D^{c,c,c}_{i,j,p,q,c,t}(\theta,d_{\text{\tiny{patient}}})}\Phi_{i,j,p,q,c,t}(\theta,d_{\text{\tiny{patient}}})\tag{16}$$

对于给定的评估合同$c$，我们寻找能够使利润最大化的持续时间$d_{\text{\tiny{patient}}}$，即：

$$\Phi^{*}_{i,j,p,q,c,t}(\theta)=\max_{d_{\text{\tiny{patient}}}\in D^{c,c,c}_{i,j,p,q,c,t}(\theta,d_{\text{\tiny{patient}}})}\Phi_{i,j,p,q,c,t}(\theta,d_{\text{\tiny{patient}}})\tag{16}$$

with Doption
      c,i
            the set of possible durations with the contract c and an employee i. For an FTC with an initial
duration dF T C and renewable once for a maximum period of 18 months (72 periods in our model), Doption
                                                                                           c
                                                                                                =
{dF T C, Min(2 × dF T C, 72)}. For an OEC, we assume that the firm estimates an average potential duration
dlearned by learning. Doption
                    c
                          = {dlearned}. These possible durations Doption
                                                                c
                                                                     may be reduced by an expected
retirement of the new employee. Then Doption
                                    c,i
                                          = {min(d, ageretirement − agei), d ∈ Doption
                                                                               c
                                                                                    }

对于给定的合同$c$，我们寻找能够最大化利润的持续时间$d_{\text{\tiny{patient}}}$，即：

$$\Phi^{*}_{i,j,p,q,c,t}(\theta)=\max_{d_{\text{\tiny{patient}}}\in D^{c,c,c}_{i,j,p,q,c,t}(\theta,d_{\text{\tiny{patient}}})}\Phi_{i,j,p,q,c,t}(\theta,d_{\text{\tiny{patient}}})\tag{16}$$

其中$D^{c,c,c}_{i,j,p,q,c,t}(\theta)$表示在合同$c$和员工$i$下可能的持续时间集合。对于初始持续时间为$dF T C$且可续签一次，最长期限为18个月（在我们的模型中为72个周期）的固定期限合同（FTC），有$Doption_c = \{dF T C, \min(2 \times dF T C, 72)\}$。对于开放期限合同（OEC），我们假设公司通过学习估计了一个平均潜在持续时间$dlearned$。这些可能的持续时间$Doption_c$可能会因新员工预计退休而减少。因此，有 $Doption_{c,i} = \{\min(d, ageretirement - age_i), d \in Doption_c\}$。

[注：重写时进行了适当的调整和补充，以使句子结构更加清晰，表达更加准确。]

The net profit per period for a contract c with a duration dc in scenario θ is :

合同c在情景θ下的每期净利润为：

$$\Phi^{net}_{i,j,p,q,c,t}(\theta)=\Phi^{*}_{i,j,p,q,c,t}(\theta)-VC-TC,\tag{17}$$
with *V C* the vacancy cost required to open this position and TC the training costs, paid afer dv periods. V C
is given by:

$$\Phi^{net}_{i,j,p,q,c,t}(\theta)=\Phi^{*}_{i,j,p,q,c,t}(\theta)-VC-TC,\tag{17}$$

其中，$VC$代表开设该职位所需的空缺成本，$TC$代表在dv个周期后支付的培训成本。空缺成本的计算公式如下：

$$VC=\sum_{d=1}^{d_{v}}\frac{Vac_{c,j,q,p}}{(1+r)^{d}},\tag{18}$$
with V acc,j,q,p = PrV acc × SHbase j,q
× *HpW*p, where *PrV ac*c is the percentage of the vacancy cost for a contract c with respect to the base salary. These percentages, PrV acOEC for OEC and PrV ac*F T C* for FTC, are calibrated parameters The training costs TC is proportional to the amount of human capital that the firm must invest in the employee in order to reach the required levels of the job:

$$VC=\sum_{d=1}^{d_{v}}\frac{Vac_{c,j,q,p}}{(1+r)^{d}},\tag{18}$$
其中，$Vacc_{c,j,q,p}=PrVacc \times SHbase_{j,q} \times HpW_p$，其中$PrVacc$表示合同$c$的空缺成本占基本工资的比例。这些比例分别为$PrVaccOEC$（对于OEC）和$PrVaccFTC$（对于FTC），它们是经过校准的参数。培训成本TC与公司必须投入员工的人力资本数量成正比，以达到所需职位水平。

$$TC=\frac{TC^{spec}+TC^{gen}+TC^{occ}}{(1+r)^{d_{v}}},\tag{19}$$
with

根据方程（19），成本TC与公司投入的员工人力资本数量成正比，以达到所需职位水平。具体而言，成本TC由特定培训成本$TC^{spec}$、一般培训成本$TC^{gen}$和职业培训成本$TC^{occ}$组成。这些成本在经过一定时期$(1+r)^{d_{v}}$后进行折现。

$$TC^{spec}=PTr^{spec}\times SH^{base}_{j,q}\times HpW_{p}\times\mathsf{Max}(0,HC^{spec}_{Re,p}-HC^{spec}_{i,p,t})\tag{20}$$ $$TC^{gen}=PTr^{gen}\times SH^{base}_{j,q}\times HpW_{p}\times\mathsf{Max}(0,HC^{gen}_{Re,p,q}-HC^{gen}_{i,t})$$ (21) $$TC^{occ}=PTr^{occ}\times SH^{base}_{j,q}\times HpW_{p}\times\mathsf{Max}(0,HC^{occ}_{Re,p,q}-HC^{rec}_{i,q,t}).\tag{22}$$
PTrspec, PTrgen and PTrocc are calibrated scale parameters (human capitals are not measured in the same units). Finally, the firm computes the final (total) profit as the weighed average profit for the 3 scenarios of demand
θ *∈ {−*1, 0, 1} :

$$TC^{spec}=PTr^{spec}\times SH^{base}_{j,q}\times HpW_{p}\times\mathsf{Max}(0,HC^{spec}_{Re,p}-HC^{spec}_{i,p,t})\tag{20}$$ 
$$TC^{gen}=PTr^{gen}\times SH^{base}_{j,q}\times HpW_{p}\times\mathsf{Max}(0,HC^{gen}_{Re,p,q}-HC^{gen}_{i,t})\tag{21}$$ 
$$TC^{occ}=PTr^{occ}\times SH^{base}_{j,q}\times HpW_{p}\times\mathsf{Max}(0,HC^{occ}_{Re,p,q}-HC^{rec}_{i,q,t})\tag{22}$$

其中，$PTrspec$、$PTrgen$和$PTrocc$是经过校准的比例参数（人力资本的度量单位不同）。最终，公司以需求情景θ *∈ {−*1, 0, 1}的加权平均利润来计算最终（总）利润。

$$\Phi^{tot}_{i,j,p,q,c,t}=\omega_{-1}\times\Phi^{net}_{i,j,p,q,c,t}(\theta=-1)+\omega_{0}\times\Phi^{net}_{i,j,p,q,c,t}(\theta=0)+\omega_{+1}\times\Phi^{net}_{i,j,p,q,c,t}(\theta=+1),\tag{23}$$
with ω−1, ω0 and ω+1 the weighing coeficients of the firm for each of the 3 scenarios. ω−1 + ω0 + ω+1 = 1.

根据公司在三种情景下的加权系数，公司的总体绩效指标可以表示为公式（23）所示。其中，$\omega_{-1}$、$\omega_{0}$和$\omega_{+1}$分别代表公司在每种情景下的加权系数。需要注意的是，这三个加权系数满足$\omega_{-1} + \omega_{0} + \omega_{+1} = 1$。

The values of these coeficients represent how much the firms are averse to loss during the evaluation process.

这些系数的值代表了公司在评估过程中对损失的厌恶程度。

A profit per period is then computed: φper
                                       i,j,p,q,c,t =
                                                   Φtot
                                                    i,j,p,q,c,t

接下来，我们计算每个时期的利润：φper
                                       i,j,p,q,c,t =
                                                   Φtot
                                                    i,j,p,q,c,t

                                                       dtot
                                                              with dtot the average expected duration of the
contract. When the algorithm is used to compare contracts with diferent duration for the same job, and choose
a type of contract for this new job, it is repeated for a set of potential candidates.

使用算法比较不同工作的不同期限合同，并为新工作选择一种合同类型时，重复进行一组潜在候选人。其中dtot是合同的平均预期持续时间。

## Appendix B: Institutional Framework Main Contracts Of The French Labor Law



TherearetwomaintypesofcontractsinFrancein2014: fixeddurationcontracts(FTC)andopenendedcontracts (OEC). The main FTC features implemented in WorkSim are:

附录B：法国劳动法的机构框架主要合同

2014年，法国有两种主要类型的合同：固定期限合同（FTC）和无固定期限合同（OEC）。WorkSim中实施的主要FTC特点包括：

1. A maximum duration of 18 months, including the possibility to be renewed once.
2. A small probationary period of one day per working week with a limit of 2 weeks, if the expected duration
of the contract is below 6 months, and of a limit of 1 month, if the expected duration of the contract is over 6 months.
3. A special allowance that the employer must pay at the end of the contract and corresponding to 10% of
the total gross salary paid during the contract.
4. An FTC cannot be broken without heavy penalties (paying the remaining salary part).
The main OEC features implemented in WorkSim are:

1. 合同最长持续时间为18个月，可续签一次。
2. 如果合同预计持续时间不超过6个月，则试用期为每周工作日的一天，最长不超过2周；如果合同预计持续时间超过6个月，则试用期最长为1个月。
3. 雇主在合同结束时必须支付特殊津贴，金额相当于合同期间总薪资的10%。
4. 无固定期限合同（FTC）不能随意解除，否则将面临严重处罚（支付剩余薪资部分）。

WorkSim中实施的主要无固定期限合同（OEC）特点包括：

1. No duration limit, except retirement.
2. A probationary period of 2 months for blue collars, 3 months for middle level jobs and 4 months for managers.
3. No termination costs if the employee is quitting.
4. Firing costs depending on employee salary and seniority:
- No firing costs if the employee seniority is below one year, but dismissals must respect the Labor
law.
- Afer one year the firing costs correspond to a fifh of a monthly wage per year of seniority. The firing
costs are increased by two fifeenth of a monthly wage per year of seniority afer ten years (cf. French labor law L.1234 - 9, R.1234 - 2 et R.1234 - 4). The reference salary used to compute these firing costs is the maximum between the average gross salary of the last twelve months and the average salary of the last three months.
5. In case of firing, a legal dismissal advance notice period has to be respected. It corresponds to one month,
if the employee seniority is below two years, and two months otherwise.

1. 除退休外，没有任何工作期限限制。
2. 蓝领工作有2个月的试用期，中层职位有3个月的试用期，管理层有4个月的试用期。
3. 如果员工主动离职，则无需支付解雇费用。
4. 解雇费用根据员工薪资和资历而定：
- 如果员工资历不满一年，则无需支付解雇费用，但解雇必须符合劳动法规定。
- 一年后，解雇费用相当于每年资历的五分之一的月薪。在十年后，解雇费用增加了每年资历的两分之一十五的月薪（参见法国劳动法L.1234 - 9, R.1234 - 2和R.1234 - 4）。计算这些解雇费用所使用的参考薪资是过去十二个月平均总薪资和过去三个月平均总薪资中较高者。
5. 在解雇情况下，必须遵守法定通知期。如果员工资历不满两年，则通知期为一个月；否则为两个月。

## Social Policy



The main parameters of the French social policy in 2014 implemented in WorkSim are the following:
Welfare allowance: people become eligible for the French welfare allowance (RSA) if one of the following conditions is met:

在WorkSim中实施的2014年法国社会政策的主要参数如下：
福利津贴：如果满足以下条件之一，人们就有资格获得法国福利津贴（RSA）：

- to be 25 years old or older. - to be a lone parent with one or more children.

在WorkSim中实施的2014年法国社会政策的主要参数如下：
福利津贴：如果满足以下条件之一，人们就有资格获得法国福利津贴（RSA）：
- 年满25岁或以上。
- 是单亲家庭且有一个或多个子女。

|   Number of children |   Single person |   Couple |
|----------------------|-----------------|----------|
|                    0 |             499 |      764 |
|                    1 |             749 |      917 |
|                    2 |             899 |     1069 |
|                    3 |            1098 |     1248 |
|                    4 |            1298 |     1448 |
|                    5 |            1498 |     1648 |

|   子女数量   |   单身人士   |    夫妻    |
|----------------------|-----------------|----------|
|                    0 |             499 |      764 |
|                    1 |             749 |      917 |
|                    2 |             899 |     1069 |
|                    3 |            1098 |     1248 |
|                    4 |            1298 |     1448 |
|                    5 |            1498 |     1648 |

上述数据呈现了不同子女数量下的单身人士和夫妻的分布情况。

- to be 18 years old or older and have worked at least two years during the last three years.

- 年满18岁或以上，并在过去三年中至少工作了两年。

The monthly amount of the RSA for a household with no activity income depends on the number of children and is given in the Table 4. The children of the household in this evaluation must be 25 years old or lower and be at the actual charge of the individual (children that perceive no income in the model). For a household with an activity income, the welfare allowance is a complement of resources, if the revenues of activity are below a guaranteed minimum amount (not detailed here).

表4列出了没有活动收入的家庭根据子女数量而定的RSA月度金额。在本评估中，家庭的子女必须年龄在25岁以下，并由个人实际承担（即模型中没有收入的子女）。对于有活动收入的家庭，福利津贴是资源的补充，但前提是活动收入低于一定保障最低金额（此处未详细说明）。

Unemployment benefit: an individual becomes eligible for unemployment benefits if all of the following conditions are met:

失业救济金：只有当满足以下所有条件时，个人才有资格获得失业救济金：

- he has been fired or he has completed a fixed duration contract. - he is looking for a new job. - he has worked 112 days (full time) in the 28 months preceding the end of the employment contract, if he
is less than 50 years old, or 36 months before the end of the employment contract, if he is 50 years old or older.
An individual receives the unemployment benefits over a period of time corresponding to his contribution period with a maximum of 24 months, if he is less than 50 years old, or 36 months if he is more than 50 years old. The calculation of the allowance received depends on an average reference salary received in the past twelve months. We refer the reader to the oficial website of the French administration for more details on the allowance evaluation41.

- 他被解雇或完成了一份固定期限的合同。
- 他正在寻找新工作。
- 如果他年龄不满50岁，在就业合同结束前的28个月内，他必须全职工作112天；如果他年龄在50岁或以上，在就业合同结束前的36个月内工作112天。
个人可以在其缴纳期内领取失业救济金，最长期限为24个月（如果年龄不满50岁）或36个月（如果年龄超过50岁）。所领取津贴的计算依赖于过去12个月中获得的平均参考工资。有关津贴评估的更多详细信息，请参阅法国政府官方网站41。

Legal work time: the legal work time per week for a full time job is 35 hours.

法定工作时间：全职工作的法定每周工作时间为35小时。

Retirement pension: in WorkSim the minimum retirement age for a full-rate pension is 65 years. The retirementpensionistakenintoaccountinthehouseholdutilityevaluations. Forthereasonofsimplicityinthiswork, we assume that this retirement pension is the same for all agents and equal to 75% of the average salary of the last 25 years for employees in the private sector and equal to 75% of the average salary of the last 6 months for employees in the public sector.

退休金：在WorkSim中，全额退休金的最低领取年龄为65岁。退休金被纳入家庭效用评估中。为了简化工作，我们假设该退休金对所有个体均相同，并且对私营部门员工而言，相当于过去25年平均工资的75%，对公共部门员工而言，则相当于过去6个月平均工资的75%。

Minimum wage: the monthly net minimum wage for a full-time job (SMIC) is 1128.7 euros in 2014.

最低工资：2014年全职工作的月净最低工资（SMIC）为1128.7欧元。

Social security contributions: employers and employees have to pay social security contributions. In 2014, the percentage of the employer's social security contributions on net wage is 54%. The percentage of the employee's social security contributions on net wage is 28%. There is a reduction of employer's charges at the SMIC level corresponding to 26% of the gross wage for firms with 20 employees or more and 28.1% of the gross wage for firms with less than 20 employees.


社会保险缴费：雇主和雇员均需缴纳社会保险费。2014年，雇主的社会保险费占净工资的比例为54%，而雇员的社会保险费占净工资的比例为28%。对于拥有20名以上员工的企业，其雇主缴费在SMIC水平上享有减免，减免额相当于总工资的26%；而对于拥有少于20名员工的企业，则相当于总工资的28.1%。

