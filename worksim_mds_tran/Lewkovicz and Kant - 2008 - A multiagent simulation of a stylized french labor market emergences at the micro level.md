# A Multi-Agent Simulation Of A Stylized French Labor Market : Emergences At The Micro-Level.



The aim of this work is to design a Multi-Agent System (MAS) simulation to model the
French labor market. We departed from an economic model proposed by Cahuc and Car-
cillo to model the introduction of a new job contract into the labor market. We designed
a specific methodology to convert this equation-based model to an agent-based model,
and calibrated our MAS to reproduce the data found in the economic simulations. As
we observed the same tendencies found in the former one, a new dimension emerged
from the agent-based simulation: an increase of oscillations for the characteristic rates,
revealing an increase of precariousness (job instability) due to the new type of contract.
Moreover, our simulation enabled to detect and correct some flaws of the Cobb-Douglas
type of matching function. These encouraging results lead us to pursue into that direc-
tion, where several extensions of our model can be proposed, including the move to a
large-scale simulation framework.

本研究的目标是设计一个多主体系统（MAS）模拟，以对法国劳动力市场进行建模。我们基于Cahuc和Carcillo提出的经济模型，对引入新的工作合同到劳动力市场进行建模。我们采用了一种特定的方法，将基于方程的模型转化为基于主体的模型，并通过校准我们的MAS来重现经济模拟中的数据。与之前的研究相比，我们观察到了相同的趋势，但基于主体的模拟中出现了一个新维度：特征率振荡增加，揭示了由于新类型合同而导致不稳定性（工作不稳定）。此外，我们的模拟还能够检测和纠正柯布-道格拉斯类型匹配函数的一些缺陷。这些令人鼓舞的结果使我们决定继续深入研究这个方向，并提出了几个扩展我们模型的可能性，包括转向大规模仿真框架。

Keywords: multi-agent simulation; labor market; emergence.

关键词：多主体模拟；劳动力市场；出现。

## 1. Introduction



In this paper, we aim to build a computational economic model that imitates the conditions of the French labor market in order to study the possible changes in the market, due to the introduction of a new job contract. We intend to take advantage judiciously of the tools provided by Multi-Agent Systems (MAS), i.e. systems made of artificial agents that are autonomous and in strong interaction with each other [13], in order to translate an economic model into an agent-based one. This approach is common in the Agent-based Computational Economics (ACE) community [12]. The ACE community captures economic changes and developments, and translates them into dynamic computational models. In these models, entities (agents) interact with each other and with the artificial environment. The meaning of computational entity is a collection of data and behavioral methods.

本文旨在构建一个计算经济模型，以模拟法国劳动力市场的条件，并研究引入新的工作合同可能导致的市场变化。为了实现这一目标，我们将巧妙地利用多主体系统（MAS）提供的工具，即由自主人工智能主体构成的系统[13]，将经济模型转化为基于主体的模型。这种方法在基于主体计算经济学（ACE）社区中非常常见[12]。ACE社区通过捕捉经济变化和发展，并将其转化为动态计算模型来进行研究。在这些模型中，实体（主体）相互交互，并与人工环境进行交互。计算实体指的是一组数据和行为方法。

重写后的中文内容如上所示。

This transposition from a pure economic model to a multi-agent system was conceived in two phases. We started by identifying the main actors in the model. Each actor has his/her own main role, and his/her own behaviors (methods). These behaviors introduce the dynamics to the simulation. We have afterwards integrated the calculation mechanisms of the economic model that are the decision processes of the agents.

这一从纯经济模型向多主体系统的转变分为两个阶段。首先，我们确定了模型中的主要参与者，每个参与者都扮演着独特的角色，并具有各自的行为方式（方法）。这些行为方式赋予了模拟过程以动态性。随后，我们将经济模型的计算机制——即主体的决策过程——进行了整合。

The implementation of the multi-agent mechanisms is sometimes straightforward, like when we encode the individual decision process, which helps the agents to choose their future action. However, some variables, which are computed by equations in the classical economic approach, can be directly set in the MAS simulation from the results of the agents' interactions. This is the case, for instance, of the unemployment rate: in the MAS simulation, depending on the decisions of workers and employers, jobs are created or destroyed, positions are filled or persons are fired, and the unemployment rate fluctuates accordingly during the simulation. Hence, one central issue when we design our MAS model is to decide whether a particular variable can be derived from simulation or had to be computed via equations.

多主体机制的实施有时是直接的，例如当我们对个体决策过程进行编码时，这有助于主体选择其未来的行动。然而，在经典经济方法中，一些变量可以通过方程计算得出，而在MAS模拟中可以直接从主体相互作用的结果中设置。例如，失业率就是这样一个情况：在MAS模拟中，根据工人和雇主的决策，就业岗位会被创造或销毁，职位会被填补或者人员会被解雇，并且失业率在模拟过程中相应地波动。因此，在设计我们的MAS模型时一个核心问题是决定特定变量是否可以通过模拟推导出来还是必须通过方程计算得到。

In the long run, the goal of this work is to provide a useful and reliable tool to political deciders. A tool that will allow, through the agent-based simulation, to evaluate and predict the efficiency of particular economic policies for the labor market.

从长远来看，这项工作的目标是为政策决策者提供一个有用且可靠的工具。通过基于主体的模拟，这个工具将能够评估和预测劳动力市场特定经济政策的效果。

## 2. Model Features 2.1. The Economic Model



The economic model we adopted was proposed by Cahuc and Carcillo [2] in order to model the introduction of a new job contract (CNE) into the French labor market. Coming from a microeconomic approach of Labor Economics [3], they used several systems of equations to describe the evolution of productivity, unemployment rate, expected utility, decision-making, etc. There are three types of job contracts in the model: *CDD* (short and fixed duration), *CDI* (no duration limit), *CNE* (no duration limit but a trial period of 2 years). The model is divided into two parts: one before the introduction of the new contract and the second just after this introduction. For each part, an independent system of equations defines the thresholds for the various behaviors in the market.

我们采用的经济模型是Cahuc和Carcillo [2]提出的，旨在对法国劳动力市场引入新的工作合同（CNE）进行建模。他们采用了劳动经济学的微观经济学方法，利用多个方程系统描述了生产率、失业率、预期效用、决策等因素的演变。该模型中包含三种类型的工作合同：*CDD*（短期固定期限）、*CDI*（无期限限制）、*CNE*（无期限限制但有2年试用期）。模型分为两部分：引入新合同之前和引入后。每个部分都有一个独立的方程系统来定义市场上各种行为的阈值。

In the first part of the simulation two types of contracts exist, namely CDD and CDI. CDD is a contract of limited duration. After two years this contract has to be either destroyed or transformed into a CDI contract. The CDI is a contract of unlimited duration. As the productivity of employees change over time, companies prefer to hire with the CDD contract, which is less binding. An upper limit is introduced to the possible number of hires with CDD per company (the case in the real French labor market).

在模拟的第一部分中，存在两种合同类型，即CDD和CDI。CDD是一种有限期限的合同。在两年后，该合同必须被终止或转为CDI合同。CDI是一种无限期限的合同。随着员工生产力随时间变化，公司更倾向于雇佣CDD合同，因为这种合同的约束力较小。为了限制每家公司可以雇佣的CDD人数（这是法国实际劳动力市场中的情况），引入了一个上限。

A worker may loose his/her job in two cases. After two years of work with a CDD
contract, the company assesses the productivity of its employee: if this productivity is insufficient, the contract is not transformed into a CDI contract and the person looses his/her job. In the second case, employees working with a CDI contract, are evaluated every month, and can be fired upon each evaluation. However the company must justify this decision. The productivity thresholds for each type of contract are computed separately.

一个工人可能在两种情况下失去工作。在与CDD合同工作两年后，公司会评估员工的生产力：如果生产力不达标，合同将不会转为CDI合同，该员工将失去工作。而对于与CDI合同工作的员工，每月都会进行评估，并且根据每次评估的结果可能被解雇。然而，公司必须对这一决定进行合理的解释。每种类型合同的生产力门槛是分别计算的。

In the second part of the simulation the CDD contract is replaced with the CNE
contract. During the first two years, the company is allowed to fire an employee at the end of every month upon evaluation, without having to justify its decision. In addition to these evaluations, a general evaluation is made at the end of two years: if the contract is not destroyed, it is transformed into a CDI contract. Hires are made only with CNE contract.

在模拟的第二部分中，CDD合同被CNE合同所取代。在前两年，公司有权在每个月底根据评估结果解雇员工，无需对其决定进行解释。除了这些定期评估外，还将在两年结束时进行一次综合评估：若合同未被终止，则转为CDI合同。只有使用CNE合同才能进行新员工的招聘。

The model defines several thresholds, which take part in the decisional mechanisms in the simulation. Employers decide whether to fire employees or not, concerning their productivity, and also decide whether to open vacancies or not. Employees decide whether to look for a job or not to participate in the labor market.

该模型定义了几个阈值，这些阈值参与了模拟中的决策机制。雇主根据员工的生产力决定是否解雇他们，并决定是否开放职位。员工决定是否寻找工作，是否参与劳动市场。

## 2.2. Main Mas Features



When using MAS, one intends to study a specific problem and therefore chooses a particular architecture for the model. Nevertheless, certain characteristics are common to all MAS [13]. Let us briefly review these main features while referring also to our model:

当使用多主体系统时，人们意图研究特定问题，并因此选择了特定的模型架构。然而，所有多主体系统都具有一些共同的特征[13]。让我们简要回顾一下这些主要特点，同时也参考我们的模型：

## 2.2.1. The Agents



All existing ACE models of the Labor Market use Worker agents and Employer agents. Some introduce also a Government agent [7]. The number of agents in the simulation can be an important factor. In [6] we find 100 agents and in [7] we find 200, while [9] uses 24 agents: 12 workers and 12 employers. Many researchers want to have the possibility of obtaining "zero unemployment" ([7], [9]), which - in their models - implies to have the same number of workers and employers. Our simulation allows setting the number of agents freely, just before it is launched. There is no obligation of having the same number of worker agents and employer agents. Moreover, the user can choose the maximal number of jobs that a single company (employer agent) will be able to open. In our simulation we set the number of workers to 400.

所有现有的劳动力市场ACE模型都采用了工人主体和雇主主体。一些模型还引入了政府主体[7]。仿真中的主体数量可能是一个重要因素。在[6]中，我们发现有100个主体，在[7]中有200个主体，而[9]使用了24个主体：12个工人和12个雇主。许多研究人员希望能够实现“零失业”（[7]，[9]），这在他们的模型中意味着工人和雇主的数量相同。我们的仿真允许在启动之前自由设置主体数量，没有必要强制要求工人主体和雇主主体的数量相同。此外，用户还可以选择单个公司（雇主主体）能够开放的最大职位数。在我们的仿真中，我们将工人数量设置为400名。

## 2.2.2. Heterogeneity



In the real labor market it is obvious that actors, let's say workers, are not homogeneous. One can consider psychological aspects of people, like the level of their education, their history in the labor market or their cognitive abilities. Heterogeneity of agents in ACE simulations is used to study specific aspects of the labor market. For instance, [9] introduces heterogeneity by using the memory (the history of interactions) of agents. In that way a persistent relationship between two agents can be studied. In other models, agents have various reservation wages [6] or skill endowments [7].

在实际劳动力市场中，很明显，行为者，例如工人，并非同质的。可以考虑人们的心理因素，如他们的教育水平、在劳动力市场上的历史或认知能力。ACE模拟中主体的异质性被用来研究劳动力市场的特定方面。例如，[9]通过利用主体之间的记忆（互动历史）引入了异质性。这样可以研究两个主体之间持久关系。在其他模型中，主体具有不同的保留工资[6]或技能禀赋[7]。

In our model agent's heterogeneity is introduced in several aspects: each agent has its own working-site history, productivity rate and "well-being" (the expected utility thresholds with which it reasons).

在我们的模型中，主体的异质性在几个方面被引入：每个主体都有自己的工作地点历史、生产率和“幸福感”（它用来推理的预期效用阈值）。

## 2.2.3. Goals Of The Agents



We can often see that agents do not have an explicit goal. In ACE models the agents may have a reasoning process that allows them to maximize their profit, for example by choosing their next action according to a profit matrix [9]. In [7], agents imitate a winning strategy without knowing what the meaning of the term "winning strategy" is. As in our model agents live and reason constantly, their permanent goal is to improve their situation, by choosing a higher expected utility state.

我们经常发现，主体并没有明确的目标。在ACE模型中，主体可能通过一个推理过程来最大化他们的利润，例如根据利润矩阵选择下一步行动[9]。在[7]中，主体模仿了一个获胜策略，却不知道“获胜策略”这个术语的含义。与我们的模型类似，主体不断生活和推理，他们永远的目标是通过选择更高预期效用状态来改善自己的情况。

## 2.2.4. Representations Of Information



The information in the simulations has two main characteristics.

模拟中的信息具有两个主要特征。

- A *complete* information environment, where everybody knows or may know
everything.
- A *perfect* information environment, where the information, which the participants have, is a 100% exact.
We can find different approaches dealing with information in the simulations. In [7] an assumption of complete and perfect information is made. To compute the investment rate of each agent in his own professional training, the average profits of all other agents is taken in account. This method may facilitate calculations and may also simplify implementation, but it is less realistic when talking about decision making in the real labor market. Incomplete and perfect information is used in [9], where the agents play a strategy game over a profit matrix of a "prisoner's dilemma" type. As both agents choose their strategy simultaneously they ignore the adversary's strategy, the type of information is incomplete. Then again, as both agents know the matrix, and gain exactly what they should, the information is also perfect in this case. [4] uses incomplete information when agents do not know (or have access) to all the vacancies in the labor market. A searching mechanism for the agents is implemented in the simulation, but this mechanism is quite demanding (from a cognitive point of view), so that agents cannot discover all vacancies in the market. Uncertainty is introduced by [7] in form of probability. Shocks hit sectors in the labor market, which oblige employers to close down their companies. Neither companies nor employees can predict these shocks, in this case an imperfect information assumption is made. In our model the nature of information varies according to the types of agents (see section 3 for more details on agents in our system). *Person* agents (i.e. job seekers or employees) are somewhere between complete and incomplete information. On one hand, they use the rate of unemployment to calculate their chances and their expected utility of finding a job, a process that uses complete information. This process is not completely unrealistic, as persons do read the newspaper and can get a general impression of the unemployment situation in the labor market. If a person sees that the unemployment rate is high, he/she may think that his/her chances of finding a job are too small and so, give up and leave the labor market. On the other hand, the *Person* agent cannot know nor estimate the duration of time required to be matched with a job offer: this incertitude is a clear case of incomplete information. This same kind of analysis is valid for *Company* agents (employers) as well. As all reasoning processes in the simulation take place simultaneously for all agents, we can say that the information that agents have is imperfect. At the moment an agent decides about his future (taking in account, let's say a certain unemployment rate), it is possible that many other agents have gone through the same process and have decided to change their state. So the agent has really a quite imperfect image of the situation in the labor market.

2.2.4 信息表示

在模拟中，信息具有两个主要特征：

- 完全信息环境，每个人都知道或可能知道一切。
- 完美信息环境，参与者所拥有的信息是100%准确的。

我们可以找到不同的方法来处理模拟中的信息。在[7]中，假设了完全和完美的信息。为了计算每个主体在其专业培训中的投资率，考虑了所有其他主体的平均利润。这种方法可能会简化计算和实施过程，但在真实劳动市场上做决策时却不太现实。[9]使用了不完全和完美的信息，在该模型中主体通过一个类似于“囚徒困境”的利润矩阵进行策略游戏。由于两个主体同时选择策略，他们忽视对手的策略，因此这种类型的信息是不完整的。然而，在这种情况下，由于两个主体都知道矩阵并且获得了应得利益，因此可以说这种情况下也是完美信息。[4]使用了不完全信息，在该模型中主体并不知道（或无法获得）劳动市场上所有职位空缺情况。模拟中实施了主体的搜索机制，但这种机制在认知上要求较高，因此主体无法发现市场上的所有职位空缺。[7]引入了概率形式的不确定性。冲击打击劳动市场中的部门，迫使雇主关闭公司。在这种情况下，既没有公司也没有员工能够预测到这些冲击，因此假设信息是不完美的。在我们的模型中，信息的性质根据主体类型而异（有关我们系统中主体更多细节，请参见第3节）。个体主体（即求职者或雇员）处于完全和不完全信息之间。一方面，他们使用失业率来计算自己找到工作的机会和预期效用，这个过程使用了完全信息。这个过程并不完全不现实，因为个体确实会阅读报纸，并对劳动市场上的失业情况有一个大致印象。如果一个人看到失业率很高，他/她可能会认为自己找到工作的机会太小了，所以放弃并离开劳动市场。另一方面，“个体”主体无法知道或估计与工作机会匹配所需时间的持续时间：这种不确定性是明显的不完全信息情况。对于“公司”主体（雇主）也适用同样的分析。由于模拟中所有推理过程同时进行，我们可以说主体所拥有的信息是不完美的。当一个主体决定自己的未来时（考虑到某个失业率），可能有很多其他主体经历了相同的过程，并决定改变自己的状态。因此，主体对劳动市场情况有一个相当不完善的认识。

## 2.2.5. Interactions Between Agents



The ACE community uses message sending to implement communication and interactions between agents, as it is often done in MAS. The protocols for this messages sending are not always defined explicitly in the simulations, although we can get a general idea about their structure from principles like "first applied, first hired" or "an agent can not apply to more than one job" [9]. Sometimes the order of message sending is crucial to the results obtained, and sometimes it has no importance, as in the Gale-Shapley algorithm [9]. We also use message sending to make the agents interact, like transmitting information to each other. However, in our model, the type of communication is closer to reality, as it takes place simultaneously and asynchronously: each agent makes its decisions independently of other agents and communicates information whenever it decides to do so.

ACE社区使用消息发送来实现主体之间的通信和互动，这在多主体系统中经常采用。尽管模拟中并未明确定义这些消息发送的协议，但我们可以从原则上对其结构有一个大致的了解，比如“先申请先录用”或“一个主体不能同时申请多个工作”[9]。有时，消息发送的顺序对于所得结果至关重要，而有时则无关紧要，就像Gale-Shapley算法中一样[9]。我们还利用消息发送使主体相互交互，例如相互传递信息。然而，在我们的模型中，通信类型更接近现实情况，因为它是同时进行且异步进行的：每个主体独立做出决策，并在决定这样做时传达信息。

注意：重写后的内容保留了原文的所有信息和结构，并且更加流畅和准确。

## 2.2.6. The Environment



The most complex environment is dynamic, stochastic, inaccessible, nondeterministic, non-markovian and *continuous*, alas, this is the case of the labor market. To be able to deal with this complexity ACE researchers use various simplifying hypothesis. The environment in previous ACE experiments is usually markovian, deterministic, static and *discrete*.

劳动力市场是一个动态、随机、不可预测、非马尔可夫、连续的复杂环境。为了应对这种复杂性，ACE研究人员采用了多种简化假设。先前的ACE实验中，环境通常是马尔可夫、确定性、静态和离散的。

In our simulation, the environment is *dynamic* - the unemployment rate can change every round, *non-markovian* - the current productivity of an agent does not depend on its previous productivities, *inaccessible* - agents cannot know the decisions of other agents concerning their future, *deterministic* - the actions of agents are executed fully and *discrete* - each agent has its own life cycle.

在我们的模拟中，环境是动态的，意味着失业率每一轮都有可能发生变化；非马尔可夫的，即一个主体当前的生产力不受其之前生产力的影响；不可预测的，因为主体无法了解其他主体关于未来决策的信息；确定性的，即主体的行动完全执行；离散的，每个主体都有自己独立的生命周期。

## 2.2.7. Everyday Life In The Company



Everyday life in the company is usually treated implicitly in ACE models. From the moment when a person has been hired, his/her wage and his/her productivity stay constant over time. Exogenous events may occur in the labor market, like economic shocks [7] or technological progresses [4]. In [9] interactions take place explicitly in the company, where the employees and the employers constantly play a game of strategies. This game is played over a profit matrix by choosing a cooperation strategy or a defection strategy.

在ACE模型中，通常隐含地处理公司的日常生活。一旦一个人被雇佣，他/她的工资和生产力就会在时间上保持恒定。劳动市场可能发生外部事件，如经济冲击[7]或技术进步[4]。在[9]中，公司内部明确进行互动，雇员和雇主不断进行策略博弈。通过在利润矩阵中选择合作策略或背叛策略来进行这个游戏。

Our simulation does not include a bilateral relationship in the company. A
worker performs with certain productivity and it is the employer who decides whether to keep or to fire this worker. The wage of the worker is constant over the time that he/she works, as his/her expected utility. The separation between a worker and an employer can be initiated only by the latter one that means that en employee cannot quit.

我们的模拟中不考虑公司内部的双边关系。每个工人都有一定的生产力，而雇主则决定是否保留或解雇该工人。工人的工资在其工作期间保持不变，作为其预期效用。只有雇主才能发起雇员和雇主之间的分离，这意味着雇员无法自行辞职。

## 3. Our Model'S Agentification



The agents participating in the model are:

参与模型的主体有：

- The *Person* agent, who produces while working and gets paid a salary. It
can be employed, unemployed or not participating in the labor market.
- The *Company* agent, who hires and fires *Person* agents. It can also decide
whether to open a job or to keep it closed.
- The *Matching* agent, who represents the environment of the labor market.
It matches unemployed *Person* agents with vacant jobs.
- The *Government* agent, who sets economic policies in the labor market.

在我们的模型中，涉及到以下主体：

- *个人* 主体，他们在工作时进行生产并获得工资。他们可以是就业、失业或不参与劳动市场。
- *公司* 主体，雇佣和解雇 *个人* 主体。它还可以决定是否开放职位或保持关闭状态。
- *匹配* 主体，代表劳动市场的环境。它将失业的 *个人* 主体与空缺职位进行匹配。
- *政府* 主体，在劳动市场制定经济政策。

## 3.1. *The* Person Agent (Worker)



The *Person* agent can be in one of *three states*:
worker it fills a job, produces and gets paid. unemployed it has no job, but it is looking for one. In this case it gets unemployment benefits.

*个人* 主体可以处于以下三种状态之一：
- 就业状态：填补职位，进行生产并获得工资。
- 失业状态：没有工作，但正在寻找工作。在这种情况下，可以获得失业救济金。

non-participant it does not fill a job neither does it look for one. In this case it gets social welfare allowances.

不参与状态：既没有填补职位，也没有寻找工作。在这种情况下，可以获得社会福利津贴。

The *Person* agent has a capital which is the sum of money it earns by filling a job or the allowances it gets. It is characterized by the productivity with which it performs its job. This productivity represents the quantity of work and the investment of the agent in the job it fills [2]. This productivity takes its values randomly from a probability distribution every month. We can sum up the *Person* agent's behaviors in the state transition diagram depicted in Figure 1.

*个人* 主体的资本是通过填补职位或获得津贴所赚取的金钱总和。其特征在于其工作的生产力，即代表了个人主体在填补职位时所投入的工作量和投资[2]。每个月，这种生产力会从一个概率分布中随机选择其值。我们可以通过图1中所示的状态转换图来概括*个人* 主体的行为。

The *Person* agent uses its decision mechanism in two situations: in the state of unemployment and in the state of non-participation. The transition between these two states is due to a reasoning process, where it decides which state will be more profitable economically. Thus, if the expected utility u for an unemployed person is greater than the expected utility n for a non participating person, the *Person* agent shifts from non-participant to unemployed state; otherwise, we have the opposite shift. In order to compute these expected utilities, the agent has to solve a system of four equations (a separate system exists for each model). For more details see [2].

*个人* 主体在两种情况下使用其决策机制：失业状态和非参与状态。这两种状态之间的转换是通过推理过程实现的，其中它会决定哪种状态在经济上更具有利润性。因此，如果对于一个失业者来说，预期效用 u 大于非参与者的预期效用 n，那么 *个人* 主体将从非参与状态转变为失业状态；否则，将发生相反的转变。为了计算这些预期效用，主体必须解决一个包含四个方程的系统（每个模型都有一个单独的系统）。更多详细信息请参见[2]。

## 3.2. *The* Company Agent (Employer)



In the labor market the *Company* agents offer vacancies, decide whether to hire a person or not and eventually decide whether to keep or to fire this person. Two states exist for a job: vacant the *Company* looks for a *Person* to fill the job.

在劳动市场上，*公司*主体提供职位空缺，决定是否雇佣某人，并最终决定是否保留或解雇该人。对于一份工作，存在两种状态：空缺状态下，*公司*正在寻找一个*个人*来填补这个职位。

filled the job is populated, and produces a profit.

填补职位后，工作岗位被填满，并产生利润。

A *Company* agent can decide not to look for a person to fill a vacancy if it thinks its chances of succeeding are too low, and that it will loose more money looking for an employee than keeping the job closed. If such decision is made after firing a worker, we will say that the job is destroyed. In this model a *Company* agent has a size, which defines the number of jobs it can offer.

如果*公司*主体认为成功的机会太低，而且寻找雇员比保持职位关闭更为成本高昂，它可以决定不再寻找人来填补空缺。如果在解雇一个工人后做出这样的决定，我们将称该职位被废除。在这个模型中，*公司*主体具有一个规模，该规模定义了它可以提供的工作数量。

The *Company* agent uses its decision mechanism in the beginning of each cycle and after each firing. If a firing takes place or vacancies that have not been published exist in the company, the agent decides whether to open these jobs or not. This decision is made according to a threshold C computed for the profitability of a job. The decision mechanism also intervenes after each productivity report, when evaluating the employee and deciding about his/her future in the company. Figure 2 summarizes the *Company* agent's behaviors.

*公司*主体在每个周期开始和每次解雇后都使用决策机制。如果发生解雇或公司存在未发布的职位空缺，主体会决定是否开放这些职位。该决策是基于计算出的职位盈利能力阈值C进行的。在每次生产力报告后，决策机制还会介入，评估员工并决定其在公司的未来。图2总结了*公司*主体的行为方式。

## 3.3. *The* Matching Agent



In order to integrate the environment of the labor market, we introduce a Matching agent. The role of this agent is to manage the lists containing the states of the agents and the states of the jobs in the labor market. Moreover, as we know, looking for a job consumes time and money. Furthermore it is possible that the offer and demand of different types of jobs do not coincide. The *matching function M* is used to introduce this notion of delay and frictions. Hence, the matching agent computes at each cycle M(*U, V* ), the number of hires as a function of the number of unemployed persons U and the number of vacant jobs V . Following [2], we use the same matching function and parameters: M(*U, V* ) = *V.m*(θ), where :

为了使劳动力市场环境更加协调，我们引入了一个匹配机构。该机构的职责是管理包含劳动力市场中个体状态和职位状态的列表。此外，我们知道找工作需要时间和金钱。而且不同类型的工作需求和供给可能不完全匹配。为了解决这种延迟和摩擦问题，我们使用匹配函数M来衡量招聘数量与失业人数U和空缺职位数V之间的关系。根据[2]的研究，我们采用相同的匹配函数和参数：M(U, V) = V.m(θ)，其中：

$m(\theta)=m_{0}\theta^{-0,5}$
m0 = 0.772 for the best fit to the real French Market data, and θ =
V
U is the tightness of the labor market.T

$m(\theta)=m_{0}\theta^{-0.5}$，其中$m_0$为最适合法国实际市场数据的值，$\theta = \frac{V}{U}$表示劳动力市场的紧张程度。

## 3.4. *The* Government Agent



The main functionality of this agent is to set the economic policies in the labor market. The agent calibrates the model and is responsible for setting the policy wanted, for example which contracts will be available (CDD, CDI, CNE ...). This A multi-agent simulation of a stylized french labor market : emergences at the micro-level.

政府主体的主要功能是制定劳动力市场的经济政策。该主体校准模型，并负责设定所需的政策，例如可用的合同类型（CDD、CDI、CNE等）。这是一个关于法国劳动力市场的多主体仿真模拟：微观层面上的新兴问题。

agent decides the amount of annual salaries for the different types of contracts, unemployment benefits, social welfare allowances etc. It also computes the benefits paid to fired workers.

主体决定不同类型合同的年薪、失业救济金、社会福利津贴等。它还计算解雇工人的福利支付。

## 4. Results 4.1. The Simulation



We implemented our system using the Repast Platform [10]. The simulation takes place in two parts, each part corresponds to different types of contracts. In the beginning we can set the number of agents (Persons, *Companies*) and the size of Companies that will take part in the simulation. We can also modify the level of salaries in the model, the amount of the unemployment benefits and the level of social welfare allowances. The new thresholds for the decision mechanisms are computed automatically by the system. The simulation is then launched.

我们采用Repast平台[10]来实现我们的系统。仿真分为两个部分，每个部分对应不同类型的合同。在开始时，我们可以设定参与仿真的主体（个人、公司）的数量以及参与仿真的公司规模。我们还可以调整模型中的薪资水平、失业救济金金额和社会福利津贴水平。系统会自动计算决策机制的新阈值。然后启动仿真过程。

The agents are created and start to interact with the environment of the labor market and with each other. The *Person* agents decide constantly whether to look for a job or not to participate in the labor market, while the *Company* agents decide whether to open jobs or not. The user can observe the unemployment rate, the vacancy rate, the participation rate, the tightness of the labor market and the messages sent between the agents. The user then decides on what moment to introduce the new contract and the simulation adopts automatically the new model. In the results below, we used 11000 agents. The unemployment rates for the two parts of the simulation are depicted in Figure 3.

主体被创造并开始与劳动力市场及彼此进行互动。个人主体不断决策是否寻找工作或参与劳动力市场，而公司主体则决策是否开放职位。用户可以观察失业率、空缺率、参与率、劳动力市场的紧张程度以及主体之间的信息传递。用户随后决定何时引入新合同，仿真系统会自动采用新模型。在下面的结果中，我们使用了11000个主体。两个部分仿真的失业率如图3所示。

The graph shows that before the introduction of the CNE contract, the unemployment rate stabilizes and that right after this introduction, there is a decrease in
10
Zach Lewkovicz and Jean-Daniel Kant the rate and a second stabilization in a higher level. These same results are found in the economic model, where the economists explain that in the long term the unemployment rate will restabilize at a superior level.

图表显示，在引入CNE合同之前，失业率稳定，并且在引入后立即出现了下降，然后在一个较高水平上再次稳定。经济学家在经济模型中也得出了相同的结果，他们解释说从长期来看，失业率将在一个更高的水平上重新稳定。

## 4.2. Detecting Flaws In The Matching Function



However, when looking at the instantaneous data set measured at each cycle in Figure 3, one can see that there are many drops to zero. This is the case for the two parts of the simulation (i.e. before and after the CNE's introduction). . The only differences are the frequency of drops and the amplitudes of these oscillations, they are both higher during the CNE's regime. Because it is unrealistic to obtain a zero-level of unemployment and this was not found in the original simulation from Cahuc and Carcillo, we had to understand the causes of these abnormal oscillations.

然而，在观察图3中每个周期测量的瞬时数据集时，可以发现存在许多降至零的情况。这种情况在模拟的两个部分（即引入CNE之前和之后）中都存在。唯一的区别在于降至零的频率和这些振荡的幅度，在CNE制度期间均较高。由于实现零失业率是不现实的，并且在Cahuc和Carcillo原始模拟中也未出现此情况，因此我们必须理解这些异常振荡的原因。

In order to answer this question one has to study the matching process in the model. As mentioned above in 3.3, the matching process computes at each round the number of hires, M(*U, V* ) = *V.m*(θ). From Eq.(1) and recalling that θ = *V/U*, we derive :

为了回答这个问题，我们必须研究模型中的匹配过程。如上所述，在3.3节中，匹配过程在每一轮计算雇佣人数M(*U, V*) = *V.m*(θ)。根据公式（1）和记住θ = *V/U*，我们推导出：

$$M(U,V)=V.m_{0}.V^{-0,5}.U^{0,5}=m_{0}.U^{0,5}.V^{0,5}\tag{2}$$
This function has the type of the *Cobb-Douglas function* :

这个函数具有*Cobb-Douglas函数*的形式：

$M(U,V)=A.U^{\alpha}V^{1-\alpha}$ (3)
with A = m0 and α = 0, 5.

$$M(U,V)=A.U^{\alpha}V^{1-\alpha}\tag{3}$$
其中，A = m0，α = 0.5。

When analyzing this Cobb-Douglas function, Boyer found that is has a quite restricted definition domain, as depicted in Figure 4 [1]. The function calculates relevant rates only when its arguments take their values in the domain represented by the white cone (EOF). If U and V take their values in the gray area (*V OE*), the number of unemployed U drops to zero because there are too many vacancies and all the jobs are matched. In the gray area (FOU), the number of vacant jobs V drops to zero because there are too many unemployed and all the jobs are matched (see [1] for details).

在对这个Cobb-Douglas函数进行分析时，Boyer发现它的定义域相当受限，如图4所示[1]。只有当其参数取值在白色锥体（EOF）所代表的域内时，该函数才能计算相关比率。如果U和V取值在灰色区域（*V OE*）内，失业人数U将降至零，因为存在过多的职位空缺并且所有工作都得到匹配。而在灰色区域（FOU）内，职位空缺数V降至零，因为存在过多的失业人员并且所有工作都得到匹配（详见[1]）。

When it is used with the macro-level economic model, we can ensure at the average to stay within the definition cone (EOF). This is not the case at the microlevel, the agent's interactions can produce any values of (*U, V* ) leading to extreme cases (U = 0 or V = 0) after the matching process being applied. This explains the unrealistic drops of the unemployment rate to zero found in Figure 3.

当与宏观经济模型结合使用时，我们可以确保平均保持在定义锥体（EOF）内。然而，在微观层面上，个体之间的相互作用可能会产生任意的(*U, V*)值，在应用匹配过程后导致极端情况（U = 0或V = 0）。这解释了图3中发现的失业率下降至零的不现实情况。

## 4.3. Correcting The Matching Function



To sum up the results found in the last paragraph above, we could state that in our simulation of the CNE the Cobb-Douglas type of a matching function is microfounded, as it shows an abnormal behavior at the micro level. We proposed to replace it with another matching function, that was proposed by Stevens [11], in the case when search and recruitment effort are exogenous that is the case in the CNE model. The new matching function we introduced into the model is presented in Equation 4.

综上所述，根据上文所述的结果，我们可以得出结论，在我们对CNE进行的模拟中，我们发现Cobb-Douglas类型的匹配函数在微观层面表现出异常行为，因此我们建议在CNE模型中将其替换为Stevens [11]提出的另一个匹配函数。我们引入的新匹配函数如方程4所示。

$$m(u,v)=m_{0}\frac{uv}{u+v}\tag{4}$$
This function fulfills all the requirements stated by Petrongolo and Pissarides [8], and its domain definition is ℜ2. The results obtained with the new function are depicted in Figure 5. One can see that after an oscillatory period the unemployment rate stabilizes and no drops to zero are detected.

该函数满足Petrongolo和Pissarides [8]提出的所有要求，并且其定义域为ℜ2。使用新函数得到的结果如图5所示。可以看到，在一段振荡期之后，失业率稳定下降，并且没有观察到降至零的情况。

12
Zach Lewkovicz and Jean-Daniel Kant

Zach Lewkovicz和Jean-Daniel Kant

## 4.4. Results' Analysis



The results we found in our simulations using the new matching function resemble to the results found in the economic model: our MAS/ACE model reproduces the same average behaviors in the labor market. We find the same tendencies while looking at the rates of unemployment, participation etc.

我们在使用新的匹配函数进行模拟时得到的结果与经济模型中的结果相似：我们的MAS/ACE模型在劳动力市场上复制了相同的平均行为。当观察失业率、参与率等指标时，我们发现了相同的趋势。

For instance, if we take the evolution of the *unemployment rate* (percentage of unemployed persons within the labor force population) depicted in Figure 5, after the introduction of CNE contracts, there is a temporary drop in the unemployment rate, due to the brief rise in the vacancy rate (percentage of vacant jobs) and the decrease of the labor force. After this brief drop, the market's average unemployment rate stabilizes on a higher level than before, since it is easier to fire a person with CNE. Overall, with CNE, we have a transition from 7.1% of unemployment to 16% on average.

举例来说，如果我们观察图5所示的失业率（劳动力人口中失业人数的百分比）的变化情况，在引入CNE合同后，由于职位空缺率（空缺职位的百分比）短暂上升和劳动力减少，导致失业率暂时下降。然而，这次短暂下降之后，市场的平均失业率稳定在比之前更高的水平上，因为使用CNE合同可以更容易地解雇员工。总体而言，在采用CNE合同后，我们将平均失业率从7.1%过渡到16%。

Similarly, with the shift to CNE, the vacancy rate (percentage of vacant jobs) is increasing, as shown in Figure 6. The companies decide to open new jobs, because their expected value is higher if filled than if vacant. Regarding individual persons, when fired, the expected utility tends to be higher in the non-participation then in the unemployment state, so they do not look for a new job and the number of vacancies stays high. In our simulations, we measured a shift from 21% to 29% in the vacancy average rate. Finally, as shown in the Figure 7, persons have a higher tendency to consider the non-participation state with higher expected utility than the unemployment state. More and more workers, who have just lost their jobs, choose to abandon the attempt of looking for a new job because they consider the market and the jobs in it to be extremely unstable. The fall of the working population rate drops from almost 90% to 64%, on average.

同样地，随着转向CNE合同，空缺率（即空缺职位的百分比）正在增加，如图6所示。公司决定开设新的职位，因为如果填补职位而不是保持空缺，其预期价值更高。就个人而言，在被解雇时，非参与状态下的预期效用往往比失业状态下更高，因此他们不会寻找新工作，导致空缺数量保持较高水平。在我们的模拟中，我们测得了空缺平均率从21%上升到29%的变化。最后，如图7所示，在非参与状态下具有较高预期效用的人们倾向于选择非参与状态而不是失业状态。越来越多刚刚失去工作的工人选择放弃寻找新工作的尝试，因为他们认为市场和其中的工作极其不稳定。劳动力人口比例从近90%平均下降到64%左右。

## 4.5. The Impact On The Well-Being



The novelty in our approach comes from the fact that MAS simulations add the possibility of taking into account more realistically the interactions between agents. Although in the economic model we can compute the unemployment rate at any given period, we cannot observe the interactions that led to this rate - our MAS simulation allows that. For instance, in Figures 5-7, we can see the increasing frequency and also the increasing deviations from the mean after the introduction of CNE contracts. This phenomenon clearly shows that the well-being of persons decreases: the frequency of these oscillations shows frequent shifts from work to unemployment or non-participation, and vice-versa. Thus it measures the precariousness of persons and the volatility of the labor market. All three rates (unemployment, vacancy, working population) show an increasing frequency of oscillations, after the introduction of the CNE contract.

我们的方法的创新之处在于MAS模拟增加了更真实地考虑主体之间相互作用的可能性。尽管在经济模型中我们可以计算任何给定时期的失业率，但我们无法观察到导致这一比率的相互作用 - 我们的MAS模拟允许这样做。例如，在图5-7中，我们可以看到引入CNE合同后频率增加以及与平均值的偏离增加。这一现象清楚地显示出个人福祉下降：这些波动频繁地从工作转向失业或非参与状态，反之亦然。因此，它衡量了个人的不稳定性和劳动力市场的波动性。在引入CNE合同后，三个比率（失业、空缺、劳动力人口）都显示出振荡频率增加。

## 5. Conclusion And Future Directions



In this study, we translated a pure economic model into a MAS simulation and reproduced the same results as in the economic model. Moreover, a new dimension emerged that could not be explicitly shown in the original model : the precariousness induced by the CNE contract.

在这项研究中，我们将一个纯经济模型转化为MAS模拟，并重现了与经济模型相同的结果。此外，还出现了一个新的维度，在原始模型中无法明确显示：CNE合同引发的不稳定性。

Contrary to most approaches in economics, we adopted a bottom-up approach.

与经济学中大多数方法相反，我们采用了自下而上的方法。

This approach is based on a higher granularity of the model. Most economic models, including models that deal with microeconomic questions, use to average behaviors of agents when reasoning about durations or decision-making. When using an agentbased simulation, we have to look into the agent, and thus to define its architecture. Many types of architectures are possible. In the future, we plan to model the agent's cognition more profoundly, in order to tackle more adequately the human decision
14
Zach Lewkovicz and Jean-Daniel Kant processes involved in the labor market. For such a purpose, we could use and adapt our cognitive architecture CODAGE [5] we already applied for an experimental financial market. The whole idea is to "humanize" more the agents, to provide them with finer and more precise reasoning and decision abilities, something that will hopefully bring them closer to real human agents in the labor market.

这种方法基于模型的更高粒度。大多数经济模型，包括处理微观经济问题的模型，在推理持续时间或决策时使用主体的平均行为。而在使用基于主体的模拟时，我们需要深入研究主体，并因此定义其架构。有许多可能的架构类型可供选择。未来，我们计划更深入地建模主体的认知能力，以更充分地应对劳动市场中涉及的人类决策过程。为此，我们可以借鉴并调整我们已经应用于实验金融市场的认知架构CODAGE [5]。总体思路是使主体更加“人性化”，赋予他们更精细和准确的推理和决策能力，希望这将使他们在劳动市场中更接近真实的人类主体。

We have not so far exploited all the possibilities provided by MAS, and several improvements will help to bring the model closer to reality in the future. First, we could diversify the agents a little more. By diversity we mean setting a field of expertise for each agent. In that case, an agent will be hired only for jobs, which suit its professional profile. This enrichment will make the matching mechanism more realistic and add frictions to the labor market environment.

迄今为止，我们尚未充分利用多主体系统（MAS）所提供的全部潜力，未来的若干改进将有助于使该模型更贴近现实。首先，我们可以进一步增加主体的多样性。所谓多样性是指为每个主体设定专业领域。在这种情况下，只有与其专业背景相符的工作才会雇佣该主体。这种丰富将使匹配机制更加真实，并为劳动市场环境引入摩擦力。

Second, in the real world, the matching process is not perfect and straightforward. Even if an employee meets with an employer, a matching does not necessarily take place. A selection or sorting phase may be integrated into both sides. An employee may wave away a job offer because he/she finds the work conditions not satisfying enough. An employer may refuse a candidate because of a bad interview, a bad vita or simply because he/she prefers hiring someone else.

其次，在现实世界中，匹配过程并非完美和直接。即使员工与雇主见面，也不一定会发生匹配。双方可能会进行选择或筛选阶段。员工可能因为对工作条件不够满意而拒绝一份工作邀约。雇主可能因为糟糕的面试、简历或仅仅是因为更倾向于雇佣其他人而拒绝候选人。

Third, the meeting between a worker and an employer may be considered as a bargaining interaction as well, where both sides negotiate the wage, the work conditions and so on. This first meeting may end in separation or in hiring. By allowing agents to negotiate, the interactions in the simulation will depend more on the labor market situation. If the unemployment rate is low an employee should have more power when negotiating his/her work conditions then when there are a lot of unemployed persons and not many vacancies.

其次，员工与雇主之间的会面也可被视为一种谈判互动，双方在工资、工作条件等方面进行协商。这次初次会面可能以分道扬镳或录用结束。通过允许主体进行谈判，模拟中的互动将更加依赖于劳动力市场的情况。当失业率较低时，员工在谈判工作条件时应该拥有更多的议价权，而当失业人数众多而职位空缺不多时，则相对较弱。

Finally, our model allows an employer to fire an employee, but the opposite case where an employee decides to quit is not permitted. This situation is biased and a future version of our model should allow an employee to quit his/her job as well.

最后，我们的模型允许雇主解雇员工，但不允许员工决定辞职的情况。这种情况是有偏见的，我们未来的模型版本应该允许员工辞职。

