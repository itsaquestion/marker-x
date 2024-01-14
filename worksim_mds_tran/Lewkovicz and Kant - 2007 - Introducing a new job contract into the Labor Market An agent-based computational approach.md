# Introducing A New Job Contract Into The Labor Market: An Agent-Based Computational Approach



We propose to implement and simulate an economic model that studies the potential effects of the introduction of a new type of a job contract into the French labor market. This transition from a classical economic model to an agent-based simulation allows us to reproduce the same tendencies found in the former one and to observe a new dimension that emerges from the agent-based simulation: an increase of oscillations for the characteristic rates revealing an increase of precariousness (job instability) due to the new type of contract. Keywords: Agent-Based Computational Model, Labor Market, Multi-Agent System, Simulation.

我们提出实施和模拟一个经济模型，研究在法国劳动市场引入一种新型工作合同可能产生的潜在影响。通过从传统经济模型转向基于主体的仿真，我们能够重现前者中发现的相同趋势，并观察到基于主体的仿真中出现的新维度：特征率振荡增加，揭示了由于新型合同而导致的不稳定性（工作不稳定）。关键词：基于主体的计算模型、劳动市场、多主体系统、仿真。

## 1. Introduction



In this paper, we aim to build a computational economic model that imitates the conditions of the French labor market in order to study the possible changes in the market, due to the introduction of a new type of a job contract. We intend to take judicious advantage of the tools provided by multi-agent systems (MAS), i.e. systems made of artificial agents that are autonomous and in strong interaction with each other,1 in order to translate an economic model to an agent-based one. The economic model is mainly described by differential equations, whereas in a multi-agent model each agent is an independent entity, constantly interacting with other agents and the environment. This transposition was elaborated in two phases. We started by identifying the main actors in the model. Each actor has his/her own main role, and his/her own behaviors (methods). These behaviors introduce the dynamics to the simulation. We have afterwards integrated the calculation mechanisms of the economic model, which take part in the decision processes of the agents.

本文旨在构建一个计算经济模型，以模拟法国劳动市场的条件，并研究引入一种新型工作合同可能导致的市场变化。为了将经济模型转化为基于主体的模型，我们将充分利用多主体系统（MAS）提供的工具，即由自治的人工智能主体构成的系统，这些主体之间相互作用紧密。经济模型主要由微分方程描述，而在多主体模型中，每个主体都是一个独立实体，不断与其他主体和环境进行交互。我们通过两个阶段来完成这个转换过程。首先，我们确定了模型中的主要参与者。每个参与者都有自己的角色和行为方式（方法），这些行为方式赋予了仿真过程中的动态性。然后，我们将涉及到决策过程的计算机制整合到经济模型中。

## 2 2. Model Features 2.1. Economic Model



The economic model we adopted was proposed by Cahuc and Carcillo2
in order to model the introduction of a new job contract (CNE) into the French labor market. Coming from a microeconomic approach of Labor Economics,3 they used several systems of differential equations to describe the evolution of productivity, unemployment rate, expected utility, decisionmaking, etc. There are three types of job contracts in the model: CDD (short duration), *CDI* (no duration limit), *CNE* (no duration limit but a trial period of 2 years). The life span of the simulation is divided into two parts: one before the introduction of the new contract and the second one after this introduction. For each part, an independent system of equations defines the thresholds for the various behaviors in the market.

我们采用了Cahuc和Carcillo提出的经济模型，以在法国劳动市场模拟引入一种新的工作合同（CNE）的情景。他们从劳动经济学的微观经济学方法出发，运用了多个微分方程系统来描述生产率、失业率、预期效用、决策等的演变。该模型中包含三种类型的工作合同：CDD（短期）、CDI（无时间限制）、CNE（无时间限制但有2年试用期）。仿真过程的生命周期分为两个阶段：引入新合同之前和之后。每个阶段都有一个独立的方程系统来定义市场上各种行为的阈值。

In the first part of the simulation two types of contracts exist. CDD is a contract of limited duration, which can last several months but cannot exceed two years. When two years are reached, this contract has to be either destroyed or transformed into a CDI contract. The CDI is a contract of unlimited duration. As the productivity of employees change over time, companies prefer to hire with the CDD contract, which is less binding. An upper limit is introduced to the possible number of hires with CDD per company (the case in the real French labor market).

在仿真的第一部分中，存在两种合同类型。CDD是一种有限期限的合同，其持续时间可以长达数月，但不得超过两年。当达到两年时，该合同必须被终止或转为CDI合同。而CDI则是一种无限期的合同。随着员工生产力随时间变化，公司更倾向于采用CDD合同进行雇佣，因为其约束力较小。此外，在可能的CDD雇佣数量方面引入了上限（这在法国实际劳动市场中也是如此）。

In the second part of the simulation the CDD contract is replaced with a CNE contract. During the first two years, the company is allowed to fire an employee at the end of every month upon evaluation, without having to justify the decision. In addition to these evaluations, a general evaluation is made at the end of two years: if the contract is not destroyed, it is transformed into a CDI contract. Hires are made only with the CNE contract.

在仿真的第二部分中，CDD合同被CNE合同所取代。在前两年期间，公司有权根据评估结果，在每个月底解雇员工，无需对决策进行解释。除了这些定期评估外，还会在两年结束时进行一次综合评估：如果合同未被终止，则会转为CDI合同。只有使用CNE合同才能进行新的雇佣。

## 2.2. Main Mas Features



When using MAS, one intends to study a specific problem and therefore, chooses a particular architecture for the model. Nevertheless, certain characteristics are common to all MAS.1 Let us briefly review these main features while referring also to our model: The Agents All existing ACE (Agent-Based Computational Economics) models of the Labor Market use Worker agents and Employer agents; some introduce also a Government agent.4 Many researchers want to have the possibility of obtaining "zero unemployment"4,5 which - in their models –
implies to have the same number of workers and employers. Our simulation allows setting the number of agents freely, just before it is launched. There is no obligation of having the same number of worker agents and employer agents. Moreover, the user can choose the maximal number of jobs that a single company (employer agent) will be able to open. In our simulation we set the number of workers to 400 and the companies' to 40. Heterogeneity In the real labor market it is obvious that actors are not homogeneous. One can consider psychological aspects of people, like the level of their education, their history in the labor market or their cognitive abilities. Heterogeneity of agents in ACE simulations is introduced by using the memory (the history of interactions) of agents,5 by having a reservation wage6 or skill endowments.4
In our model heterogeneity of agents is introduced in several aspects: each agent has its own working-site history, productivity rate and "well-being" (the expected utility thresholds with which it reasons). Interactions between agents The ACE community often uses message sending to implement communication and interaction between agents. The protocols for these message-based interactions are not always defined explicitly in the simulations, although we can get a general idea about their structure from principles like "first applied, first hired" or "an agent can not apply to more than one job". Sometimes the order of message sending is crucial, and sometimes it has no importance, as in the Gale-Shapley algorithm.5
We also use message sending to make the agents interact. However, in our model, the type of communication is closer to reality, as it takes place simultaneously and asynchronously: each agent makes its decisions independently of other agents and communicates information whenever it decides to do so.

使用多主体系统（MAS）时，研究人员旨在解决特定问题，并选择特定的模型架构。然而，所有MAS都具有一些共同的特征。让我们简要回顾一下这些主要特征，同时也参考我们的模型：主体。所有现有的劳动力市场基于主体计算经济学（ACE）模型都使用工人主体和雇主主体；有些还引入了政府主体。许多研究者希望实现“零失业”，这在他们的模型中意味着工人和雇主数量相等。我们的仿真允许在启动之前自由设置主体数量，没有必要使工人主体和雇主主体数量相同。此外，用户可以选择单个公司（雇主主体）能够开放的最大职位数。在我们的仿真中，我们将工人数量设置为400，公司数量为40。

异质性是现实劳动力市场中显而易见的特点，参与者之间存在差异。可以考虑到个体心理因素，如教育水平、劳动力市场历史或认知能力水平等方面进行分析。ACE模拟通过使用主体之间互动历史（记忆）、保留工资或技能禀赋等方式引入主体的异质性。在我们的模型中，主体的异质性体现在多个方面：每个主体都有自己的工作历史、生产率和“幸福感”（其推理时所使用的预期效用阈值）。

主体之间的互动通常使用消息传递来实现。尽管模拟中并不总是明确定义这些基于消息的互动协议，但我们可以从原则上了解它们的结构，比如“先申请先录用”或“一个主体不能同时申请多个职位”。有时候消息发送顺序至关重要，有时候则无关紧要，就像Gale-Shapley算法一样。在我们的模型中，我们也使用消息发送来使主体进行互动。然而，在我们的模型中，通信类型更接近现实情况，因为它是同时且异步进行的：每个主体独立做出决策，并在决定这样做时传递信息。

## 2.3. Agentification 2.3.1. The **Person** Agent (Worker)



The *Person* agent can be in one of *three states*:
worker it fills a job, produces and gets paid. unemployed it has no job, but it is looking for one. In this case it gets unemployment benefits.

**2.3. 主体化 2.3.1. 人员主体（工人）**

**人员**主体可以处于以下*三种状态*之一：
- 就业状态：从事工作，进行生产并获得报酬。
- 失业状态：没有工作，但正在寻找就业机会。在这种情况下，可以获得失业救济金。

non-participant it does not fill a job neither does it look for one. In this case it gets social welfare allowances.

不参与状态：既没有工作，也没有找工作。在这种情况下，可以获得社会福利津贴。

The *Person* agent is characterized by the productivity with which it performs its job. This productivity represents the quantity of work and the investment of the agent in the job it fills.2 This productivity takes its values randomly from a probability distribution every month. We can sum up the Person agent's behaviors in the state transition diagram depicted in Figure
1.

人员主体的特征在于其工作的生产力。这种生产力代表了主体在所从事工作中的工作量和投入。每个月，这种生产力会随机地从一个概率分布中取值。我们可以通过图1中所示的状态转换图总结出人员主体的行为。

The *Person* agent uses its decision mechanism in two situations: in the state of unemployment and in the state of non-participation. The transition between these two states is due to a reasoning process, where it decides which state will be more profitable economically. Thus, if the expected utility u for unemployed person is greater than the expected utility n for non participating person, the Person shifts from non-participant to unemployed state; otherwise, we have the opposite shift. In order to compute these expected utilities, the agent has to solve a system of four equations (a separate system exists for each model), for more details see.2

*人员*主体在两种情况下使用其决策机制：失业状态和非参与状态。这两种状态之间的转换是通过推理过程实现的，其中它决定哪种状态在经济上更具盈利性。因此，如果失业人员的预期效用u大于非参与人员的预期效用n，则个体将从非参与状态转变为失业状态；反之亦然。为了计算这些预期效用，主体必须解决一个包含四个方程组的系统（每个模型都有一个独立的系统），详细信息请参见文献2。

## 2.3.2. The **Company** Agent (Employer)



Two states exist for a job in a Company: vacant the *Company* looks for a *Person* to fill the job.

公司中存在两种状态的工作：空缺和公司正在寻找人员来填补这个职位。

filled the job is populated, and produces a profit.

2.3.2 公司主体（雇主）

公司中的工作有两种状态：空缺和公司正在寻找人员来填补这个职位。

当职位被填补时，该职位将被占据，并产生利润。

A *Company* agent can decide not to look for a *Person* to fill a vacancy if it thinks its chances of succeeding are too low, and that it will loose more money looking for en employee than keeping the job closed. If such decision is made after firing a worker, we will say that the job is destroyed. In this model a *Company* agent has a size, which defines the number of jobs it can offer.

如果公司主体认为成功的机会太低，而且寻找雇员比保持职位关闭更为成本高昂，公司主体可以决定不寻找人员来填补空缺。如果在解雇一个工人之后做出这样的决定，我们将称该职位被废除。在这个模型中，公司主体具有一个规模，该规模定义了其可以提供的工作数量。

The *Company* agent uses its decision mechanism in the beginning of each cycle and after each firing. If a firing takes place or vacancies that have not been published exist in the company, the agent decides whether to open these jobs or not. This decision is made according to a threshold C computed for the profitability of the job. The decision mechanism also intervenes after each productivity report, when evaluating the employee and deciding about his/her future in the company. Figure 2 summarizes the *Company*'s behaviors.

*公司*主体在每个周期开始和每次解雇后都使用决策机制。如果发生解雇或存在未发布的职位空缺，主体将根据工作的盈利能力计算出的阈值C来决定是否开放这些职位。此外，在每次生产力报告后，决策机制还会评估员工并决定其在公司的未来。图2概述了*公司*的行为方式。

## 2.3.3. The **Matching** Agent



In order to integrate the environment of the labor market, we introduce a Matching agent. The role of this agent is to manage the lists containing the states of the agents and the states of the jobs in the labor market. It computes the matching rate m(θ) for each round that defines how many vacancies and unemployed persons will be coupled per unit of time. Following,2 we use the same matching function: m(θ) = M0θ−η , where M0 and η
are constants in [0,1] and θ is the tightness of the labor market. The fact of having simultaneously unemployed persons and vacancies in the real labor market, could explain the necessity of having such a function. Furthermore it is possible that the offer and demand of different types of jobs do not coincide. We use the matching function to integrate this notion of delay and frictions.

为了融合劳动力市场的环境，我们引入了一个匹配主体机构。该主体机构的作用是管理包含劳动力市场中个体状态和职位状态的列表。它计算每一轮的匹配率m(θ)，该率定义了每单位时间内将有多少个空缺职位和失业人员进行匹配。接下来，我们采用相同的匹配函数：m(θ) = M0θ−η，其中M0和η是[0,1]范围内的常数，θ表示劳动力市场的紧缩程度。在实际劳动力市场中同时存在失业人员和空缺职位可能解释了需要这样一个函数的必要性。此外，不同类型工作的供求可能不完全吻合。我们使用匹配函数来整合这种延迟和摩擦概念。

## 3. Results 3.1. The Simulation



We implemented our system using the Cougaar Platform,7 because it is an open source agent-based architecture that emphasizes cognitive agents, groups and organizations. Moreover, it fully supports large-scale applications, and we plan in the future to design a large-scale multi-agent system for the labor market.

我们使用Cougaar平台实现了我们的系统，因为它是一个强调认知主体、群体和组织的开源基于主体的架构。此外，它完全支持大规模应用程序，并且我们计划在未来设计一个大规模多主体系统用于劳动力市场。

## 3.2. Observed Tendencies



Our MAS model reproduces the same average behaviors (tendencies) found in the economic model2 of the labor market.

我们的多主体系统模型重现了劳动力市场经济模型中发现的相同的平均行为（趋势）。

For instance, the evolution of the *unemployment rate* depicted in Figure
3, after the introduction of CNE, the market's average unemployment rate stabilizes on a higher level than before, since it is easier to fire a person with CNE. Overall, with CNE, we have a transition from 7.1% of unemployment to 16% on average. Moreover, as shown in the Figure 4, persons have a tendency to consider the non-participation state with higher expected utility than the unemployment state. More and more workers, who have just lost their jobs, choose to abandon the option of looking for a new job because they consider the market and the jobs in it to be extremely unstable. The fall of the working population rate drops from almost 90% to 64%, on average.

举例来说，引入CNE后，图3所示的失业率演变表明市场的平均失业率稳定在比之前更高的水平上，因为使用CNE使解雇一个人变得更容易。总体而言，使用CNE后，失业率从7.1%过渡到了平均16%。此外，如图4所示，个体更倾向于认为非参与状态比失业状态具有更高的预期效用。越来越多刚刚失去工作的工人选择放弃寻找新工作的机会，因为他们认为市场和其中的工作极其不稳定。劳动力参与率从近90%下降到了平均64%。

## 3.3. The Impact On The Well-Being



The novelty in our approach comes from the fact that MAS simulations enable interactions between agents, whose nature is closer to reality. Although in the economic model we can compute the unemployment rate at any given period, we cannot observe the interactions that led to this rate, while our MAS simulation allows us to gain tractability. For instance, in Figures 3 and 4, we can see the increasing frequency and also the increasing deviations from the mean after the introduction of CNE. This phenomenon shows clearly that the well-being of people decreases: the frequency of these oscillations shows frequent shifts from work to unemployment or non-participation and vice-versa. Thus it measures the precariousness (as job instability) of persons and the volatility of the labor market. All three rates (unemployment, vacancy, working population) show an increasing frequency of oscillations, after the introduction of the CNE contract.

我们的方法的创新之处在于MAS模拟使得主体之间的互动更加贴近现实。尽管在经济模型中我们可以计算任何给定时期的失业率，但我们无法观察到导致该比率的互动过程，而我们的MAS模拟则使得这一过程变得可控。例如，在图3和图4中，我们可以清楚地看到引入CNE后频率增加，并且偏离平均值越来越大。这一现象明确地显示人们的福祉下降：这些波动频繁地从工作转向失业或非参与状态，反之亦然。因此，它衡量了个人就业不稳定性以及劳动力市场的波动性。在引入CNE合同后，失业率、空缺率和就业人口这三个指标都显示出振荡频率增加。

[注：MAS为Multi-Agent Simulation（多主体模拟），CNE为Contrat Nouvelle Embauche（新雇佣合同）]

## 4. Conclusion And Future Directions



In this study, we translate a pure economic model to a MAS simulation. We reproduce the same results as in the economic model and add a supplementary dimension to the results obtained. Most of the reasoning processes take place explicitly at the agents' level and implicitly in the aggregated labor market level. In our study, the precariousness induced by the CNE contract clearly emerges, and can be measured as a dramatic increase of oscillations for all the rates: unemployment, vacancy, and working population.

本研究将一个纯经济模型转化为MAS模拟，并在结果中增加了一个补充维度。我们以主体层面明确地进行大部分推理过程，同时在聚合劳动力市场层面隐含地进行。在我们的研究中，CNE合同引发的不稳定性明显显现，并且可以通过失业率、空缺率和就业人口的剧烈波动来衡量。这些结果与经济模型一致。

Several improvements should help to bring the model closer to reality in the future. First, we could diversify the agents (add more heterogeneity) a little more. By diversity we mean setting a field of expertise for each agent. In that case, an agent will be hired only for jobs, which suit its professional profile. This added feature will make the matching mechanism more realistic and add frictions to the labor market's environment.

未来可以通过几项改进来使模型更贴近现实。首先，我们可以进一步增加主体的多样性，即增加更多的异质性。所谓多样性是指为每个主体设定一个专业领域。在这种情况下，只有与其专业背景相符的工作才会雇佣该主体。这一额外特征将使匹配机制更加真实，并为劳动力市场环境增添摩擦。

Second, the meeting between a worker and an employer may be considered as a bargaining interaction as well, where both sides negotiate the wage, the work conditions and so on. By allowing agents to negotiate, the interactions in the simulation will depend more on the labor market's current situation.

其次，工人和雇主之间的会面也可以被视为一种谈判互动，双方在谈判工资、工作条件等方面进行协商。通过允许主体进行谈判，模拟中的互动将更多地依赖于劳动力市场的当前情况。

Finally, our model allows an employer to fire an employee, but the opposite case where an employee decides to quit is not permitted. This situation is biased and a future version of our model should include this possibility. Acknowledgement This work was supported by grants from Region Ilede-France.


最后，我们的模型允许雇主解雇员工，但不允许员工决定辞职的情况。这种情况存在偏见，我们未来的模型版本应该包括这种可能性。致谢：本研究得到了法兰西岛地区的资助。

