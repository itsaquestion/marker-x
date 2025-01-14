# An Agent-Based Simulation Of The French Labour Market : Studying Age Discrimination



Abstract. We present here an agent-based model and simulation of the French labour market - WorkSim. Based on an existing economic model, ARTEMIS, WorkSim is a full multiagent system, where agents (e.g. individuals, firms) possess detailed attributes and elaborated behaviours in order to reflect the real labour market as close as possible. We illustrate our approach with two main simulation results: the reproduction of one peculiar stylized fact, i.e. discrimination against the seniors, and the impact of a new labour contract introduction.

摘要。本文介绍了一个基于主体的模型和模拟工具——WorkSim，用于研究法国劳动力市场。基于现有的经济模型ARTEMIS，WorkSim是一个完整的多主体系统，其中主体（如个人、公司）具有详细属性和复杂行为，以尽可能真实地反映劳动力市场的情况。我们通过两个主要的模拟结果来说明我们的方法：一是对老年人歧视这一特殊事实的再现，二是新劳动合同引入所带来的影响。

## 1 Introduction



Unemployment is a grave social problem that may have negative impacts not only on the unemployed persons, but also on their relatives and friends or on the entire population of a country (recession etc.). The aim of our work is to show how agent-based modelling and simulation could help (i) understanding how labour market works and (ii) designing better policies in order to improve its performance. In a previous paper [1], we have proposed a multiagent model of a stylized French labour market (FLM), and showed how it could be used to measure the impact of institutional change: the introduction of a new form of hiring contract. A closer analysis of the simulation dynamics enabled us to reveal some drawbacks of this new type of contract (i.e. the increase of precariousness), and also to detect some flaws in the original economic model we started from [2].

失业是一个严重的社会问题，不仅对失业者本人产生负面影响，还可能对他们的亲属、朋友或整个国家的人口产生负面影响（如经济衰退等）。我们的研究旨在展示基于主体模型和模拟的应用，如何有助于（i）理解劳动力市场的运作方式和（ii）设计更好的政策以改善其绩效。在我们之前的一篇论文中[1]，我们提出了一个简化版法国劳动力市场（FLM）的多主体模型，并展示了如何利用该模型来衡量制度变革带来的影响：引入一种新形式的雇佣合同。通过对模拟动态进行更详细分析，我们发现了这种新类型合同存在一些缺陷（即不稳定性增加），同时也发现了我们最初使用的经济模型中存在一些问题[2]。

In this paper, we introduce a new agent-based model and simulator, named WorkSim, aimed to be more complete and realistic than our previous one. Work- Sim is based on the ARTEMIS [3] economic model, which models the FLM as an endogenously evolving institution. It is almost individual-based, with firms and individuals making decisions at the microeconomic level, and includes a search process and decentralized setting of hiring standards. In WorkSim, we translated ARTEMIS into a full multiagent system, and added several components and processes to get a more realistic model.

本文介绍了一个名为WorkSim的全新基于主体的模型和模拟器，旨在比我们之前的模型更加完备和真实。WorkSim基于ARTEMIS[3]经济模型，该模型将FLM作为内生演化的制度进行建模。它几乎是以个体为基础的，企业和个人在微观经济层面上做出决策，并包括搜索过程和分散设置招聘标准。在WorkSim中，我们将ARTEMIS转化为一个完整的多主体系统，并添加了多个组件和过程以获得更加真实的模型。

In order to illustrate the interest of our approach, we will show how WorkSim tackles one important stylized fact of the FLM : the fact that the unemployment rate is significantly higher for the senior population (i.e. age greater than 50). Moreover, we will also use WorkSim to study the impact of a new type of contract, the Unified Contract (UC), on this peculiar segmentation against the senior job seekers.

为了展示我们方法的优势，我们将使用WorkSim来解决FLM中一个重要的事实：即年龄超过50岁的老年人群体的失业率显著较高。此外，我们还将利用WorkSim来研究一种新型合同——统一合同（UC），对这种特殊的老年求职者分割现象的影响。

[重写后的中文内容:]

This paper is organized as follows. In section 2, we present our approach against existing agent-based models of labour markets. In section 3, we describe the main features of the WorkSim model and in section 4 we present some experimental results, followed by a discussion.

本文的组织结构如下。第2节介绍了我们对现有劳动力市场基于主体的模型的方法。第3节描述了WorkSim模型的主要特点，第4节呈现了一些实验结果，并进行了讨论。

## 2 Agent-Based Models Of The Labour Market



When analyzing existing agent-based models of the labour market some common properties dominate. All models use the notions of workers and employers, who interact on a regular basis. The complexity of each entity or interactions varies.

在分析现有的劳动力市场基于主体的模型时，一些共同的特点占主导地位。所有模型都使用工人和雇主的概念，他们定期进行互动。每个实体或互动的复杂性各不相同。

In this section, we will give a brief and non-exhaustive inspection of the existing qualities of these models, and compare with our approach.

在本节中，我们将对这些模型的现有特点进行简要而非详尽的检查，并与我们的方法进行比较。

Heterogeneity The various characteristics of the agents contribute to the complexity of the model. One should choose them in the right way, so that they will provide the model with the exact amount of diversity required. Pingle and Tesfatsion [4] introduce heterogeneity by using the memory (the history of interactions) of agents. In that way a persistent relationship between two agents can be studied. Neugart gives agents various reservation wages [5] or different skill endowments [6]. In our model agents' heterogeneity is introduced in several aspects such as the level of professional qualification, past experience in the labour market or the level of productivity. But the most important one is the (physical) age of the agent. Agents enter the simulation at the age of 18 and leave it when they retire from the labour market. In this way, their histories can be studied and the age segmentation in unemployment can be analyzed.

异质性：主体的各种特征为模型的复杂性增添了一层面。正确选择这些特征是至关重要的，以确保模型具备所需的多样性。Pingle和Tesfatsion [4]通过利用主体的记忆（即互动历史）引入了异质性，从而研究了两个主体之间持久的关系。Neugart则通过设定不同的保留工资[5]或不同的技能禀赋[6]来赋予主体多样化。在我们的模型中，我们从多个方面引入了主体的异质性，包括专业资格水平、劳动力市场上的过去经验以及生产力水平等。然而，最重要的是考虑到主体（物理）年龄因素。主体在18岁进入模拟，并在退休时退出劳动力市场。通过这种方式，我们可以研究他们的历史，并分析失业情况中与年龄相关的分段情况。

注意：重写后的文本保留了原文内容和学术风格，并更加流畅易读。

Rationality and information In some models agents are fully rational and have all the needed tools to reach the best decision available. In [6] in order to compute the investment rate of each agent in his own professional training, the average profits of all other agents is taken into account. That means that a full rationality and a full access to other agents' information are possible. This method may facilitate calculations, but it is less realistic when talking about decision making in the real labour market. In our model agents do not have access to all the information they need. Job seekers cannot know all the vacancies that exist in the labour market and they acquire information about new vacancies gradually. Likewise, firms do not know all the job seekers in the labour market. And when they meet a job seeker, they may estimate his productivity, but they get to know its exact value only after the individual agent has started working for them.

在某些模型中，主体被认为是完全理性的，并具备达到最佳决策所需的所有工具。在[6]中，为了计算每个主体在其专业培训中的投资率，考虑了所有其他主体的平均利润。这意味着完全理性和对其他主体信息的完全获取是可能的。尽管这种方法可以简化计算，但在现实劳动市场上进行决策时却不太现实。在我们的模型中，主体无法获得他们所需的所有信息。求职者无法知道劳动力市场上存在的所有职位空缺，并逐渐获取有关新职位空缺的信息。同样，企业也不知道劳动力市场上所有求职者。当他们遇到一名求职者时，他们可以估计其生产力，但只有在个别主体开始为他们工作后才能确切了解其价值。

Everyday life in the company, which captures the interactions employeremployee, is usually treated implicitly in ACE models. In [4] interactions take place explicitly in the company, where the employees and the employers constantly play a game of strategies. Exogenous events may occur in the labour market, like economic shocks [6] or technological progresses [7] that have direct impacts on everyday life. WorkSim endows the agents with a richer interaction mechanism. Agents may be fired, but they may also choose to quit by themselves. And more importantly, agents may be promoted when staying in the same firm for a sufficient time.

在ACE模型中，通常隐含地处理了公司的日常生活，其中包括雇主和雇员之间的互动。然而，在[4]中，公司内部的互动被明确地呈现出来，员工和雇主不断进行策略游戏。劳动市场可能会发生一些外部事件，如经济冲击[6]或技术进步[7]，这些事件直接影响着日常生活。通过WorkSim模型，主体之间的互动机制更加丰富。主体可能会被解雇，但他们也可以选择自行辞职。更重要的是，在同一家公司工作足够长时间后，主体有可能获得晋升机会。

## 3 The Worksim Model



ARTEMIS (Activit´e, Revenus du Travail Et MIcro-Simulation)1 is a model proposed by Ballot in 1980 [3]. Its main objective was to build a simulation that would help to understand the working-class' distribution of revenues in France between 1972 and 1977. The primary units in the model are individuals and jobs, while the decisional units are individuals and firms.

ARTEMIS（Activité, Revenus du Travail Et MIcro-Simulation）是由Ballot于1980年提出的模型[3]。其主要目标是构建一个模拟，以帮助理解1972年至1977年法国工人阶级收入分配情况。该模型的主要参与者为个体和就业岗位，而决策单位则为个体和公司。

In ARTEMIS individual agents compare possible states (inactivity, current job, new job etc.) by associating a calculated expected utility to each one of them, while firm agents were told exogenously what decisions to make concerning jobs' creation and destruction. In WorkSim, we implemented this parallel process inside the firms. We chose to make them reason with a calculation system of expected costs. Thus a firm will keep an unproductive employee until he retires if the expected cost associated with his firing is greater than the salary cost. For doing so, we had to introduce the concept of productivity level for an individual agent. More importantly, job contracts do not exist in ARTEMIS. This is why we paid particular attention to capture all the aspects of a job contract in the decisional mechanisms of the agents.

在ARTEMIS中，个体主体通过为每种可能状态（不活动、当前工作、新工作等）关联一个计算得出的预期效用来进行比较，而公司主体则被告知如何决定有关工作创造和销毁的事项。在WorkSim中，我们在公司内部实施了这个并行过程。我们选择使用预期成本计算系统让公司进行推理。因此，如果解雇某位员工的预期成本大于薪资成本，公司将会保留这位无生产力的员工直到他退休。为了做到这一点，我们不得不引入个体主体的生产力水平概念。更重要的是，在ARTEMIS中不存在就业合同。因此，在主体决策机制中，我们特别注意捕捉就业合同的所有方面。

On the computational level, ARTEMIS was quite advanced for its time, as the approach Ballot adopted was individual-oriented almost in all its levels. However, we had to increase the complexity of the agents' structure, so they would be independent entities with their personal characteristics (age, qualification level, etc.) and behaviours, which are modelled as a set of performance methods. Each agent has its *decision module*, which is made of three components: perception, *cognition* and *choice*. Agents have states, which correspond to real conditions in the labour market (employed, inactive etc.). Agents shift between states due to the proper choices they made or to the action of other agents. In WorkSim, unlike in ARTEMIS, in order to communicate, agents are endowed with a communication mechanism that enables the exchange and the processing of messages.

在计算层面上，ARTEMIS在其时相当先进，因为Ballot采用的方法几乎在所有层面上都以个体为导向。然而，我们必须增加主体结构的复杂性，使其成为具有个人特征（年龄、资格水平等）和行为的独立实体，并将其建模为一组性能方法。每个主体都有一个决策模块，由感知、认知和选择三个组件组成。主体具有状态，这些状态对应于劳动市场中的实际情况（就业、非活动等）。主体根据自己做出的适当选择或其他主体的行动而在状态之间转换。与ARTEMIS不同，在WorkSim中，为了进行通信，主体配备了一种通信机制，使其能够交换和处理消息。

## 3.1 Agents In Worksim



In WorkSim *Individual* agents may be hired by *Employer* agents in order to occupy *Job*s in *Firm*s. A *Job* is filled under a specific *Contract*, which gives a legal trait to the relation employer-employee. The *Government* agent sets the different types of *Contract*s available in the labour market. The *SmallAds* agent proxies the vacancies' market, where *Firm*s publish their vacancies and where Individuals consult job offers for eventual job applications.

在WorkSim中，个体主体可以被雇主主体聘用，以在公司中担任职位。每个职位都是根据特定的合同来填补的，这使得雇主-员工关系具有法律属性。政府主体设定了劳动市场上不同类型的合同。SmallAds主体充当了空缺市场的中介，公司在这里发布空缺信息，而个人则可以查看工作机会以便进行可能的求职申请。

1 activity, revenue of labour and micro-simulation; for a paper in English, see [8]
The Individual agent (worker) is characterized by his age, his professional qualification level and by his productivity rate. He enters the simulation at the age of 18 and gets older until he reaches the retirement age and exits. He may also gain or loose qualification levels. His productivity increases with the experience he accumulates while occupying a job. The Firm agent (employer) is characterized by its size and amenity. The size of a firm is defined by the number of vacancies and filled jobs it possesses. The amenity of a firm is an indicator of the pleasantness of working in it. In our model this amenity is in opposite correlation with the frequency with which a firm evaluates the productivity of its employees. The more employees are evaluated periodically, the less amount of amenity this firm has.

个体主体（工人）的特征包括年龄、职业资格水平和生产率。他在18岁进入模拟，并随着年龄增长直至退休后退出。他还有可能获得或失去职业资格水平。随着在工作中积累的经验，他的生产率也会增加。公司主体（雇主）的特征则包括规模和宜人性。公司的规模由其拥有的空缺和已填补职位数量来定义。公司的宜人性指标反映了在其中工作时的愉快程度。在我们的模型中，这种宜人性与公司定期评估员工生产力的频率呈相反相关关系。员工被定期评估得越多，该公司具有较低的宜人性。

The Government agent is responsible for determining the *play rules* in the labour market. This agent decides, for example, how the amount of unemployment benefits will be calculated.

政府主体负责确定劳动市场的“游戏规则”。例如，该主体决定了失业救济金的计算方式。

## 3.2 Interactions In Worksim: 3 Stages



In our model a whole periodical life cycle takes place in each step (tick), which is equal to one month in the real labour market. During this cycle each agent executes its behavioural methods. Throughout both parts of the simulation the architecture of the agents stays the same and it is just the economic play rules that change. Figure 1 gives a general aspect on a periodical life cycle.

在我们的模型中，每个步骤（滴答声）都代表一个完整的周期性生命周期，在现实劳动市场中相当于一个月。在这个周期内，每个主体执行其行为方法。在整个模拟的两个部分中，主体的架构保持不变，只是经济游戏规则发生变化。图1展示了周期性生命周期的总体概览。

The first stage (A) starts with (1) a personal evaluation of the employees'
productivity. At each period a number of random employees are designated for personal evaluation. If an employee passes a minimal threshold of productivity that is required for a job, the job is maintained, otherwise the employee is fired and the job becomes vacant. After this personal evaluation that may lead to an *individual firing* (see section 3.3), the (2) job management mechanism takes place. During this phase, vacancies that have exceeded the maximal duration threshold are destroyed and in the next step the firm evaluates its economic state (balance). Firms that have a positive balance will open new vacancies hoping to increase their profits. The creation of new vacancies is followed by their publication via the *SmallAds* agent. However, firms that are in deficit have to restrain their economical activities, in order to minimize losses. In this case vacancies are destroyed as well as filled jobs. In the latter case an employee occupying a job will be dismissed, an *economic firing* (see 3.3) will take place and the job will be destroyed. The last decision made by the firms that closes this first stage is (3) promotions. During a promotion, the promoted employee follows a professional training and thus increases his qualification level and his salary.

第一阶段（A）始于对员工生产力的个人评估（1）。每个周期，随机选择一些员工进行个人评估。如果员工的生产力达到了岗位所需的最低阈值，该岗位将被保留；否则，员工将被解雇，岗位变为空缺。在这个可能导致*个体解雇*的个人评估之后（详见第3.3节），就进入了（2）职位管理机制。在这一阶段中，超过最大持续时间阈值的空缺将被取消，并且公司会评估其经济状况（平衡）。具有正面平衡的公司将开设新的职位，以期增加利润。新职位通过*SmallAds*主体发布。然而，处于亏损状态的公司必须限制其经济活动以减少损失。在这种情况下，空缺和已填补职位都会被取消。对于后一种情况，占据职位的员工将被解雇，并发生*经济解雇*（详见第3.3节），该职位也会被取消。第一阶段结束时企业做出的最后决策是（3）晋升。在晋升过程中，晋升的员工将接受专业培训，提高其资格水平和薪资水平。

The second stage (B) is dedicated to the execution of the cognitive and decisional mechanisms of the *Individual* agents. First of all individuals choose (4)
whether or not to participate in the labour market by comparing their current situation with inactivity. If they consider that inactivity has a more profitable

第二阶段（B）旨在执行个体主体的认知和决策机制。首先，个体通过将自身当前情况与非活动状态进行比较来决定是否参与劳动市场（4）。如果他们认为非活动状态更具盈利性，他们将选择不参与劳动市场。否则，他们将进入下一步骤，即确定是否寻找新的就业机会（5）。在这一步骤中，个体将评估自身当前的工资水平和其他潜在就业机会，并根据这些因素做出决策。如果个体决定寻找新的就业机会，他们将进入求职市场，并根据自身技能和经验寻找适合自己的职位（6）。最后，在求职过程中，个体可能会收到雇主的面试邀请，并根据面试结果做出最终是否接受该职位的决策（7）。

## A



FIRMS' DECISIONS :
(1) Individual evaluation
(2) Jobs creation and destruction
(3) Promotions

企业的决策：
（1）个体评估
（2）就业机会的创造和破坏
（3）晋升

          INDIVIDUALS' DECISIONS :
B

个体的决策：
B）旨在执行个体主体的认知和决策机制。首先，个体会通过将自身当前情况与非活动状态进行比较来决定是否参与劳动市场（4）。如果他们认为非活动状态更具盈利性，他们将选择不参与劳动市场。否则，他们将进入下一步骤，即确定是否寻找新的就业机会（5）。在这一步骤中，个体会评估自身当前的工资水平和其他潜在就业机会，并根据这些因素做出决策。如果个体决定寻找新的就业机会，他们将进入求职市场，并根据自身技能和经验寻找适合自己的职位（6）。最后，在求职过程中，个体可能会收到雇主的面试邀请，并根据面试结果做出最终是否接受该职位的决策（7）。

(4) Entries and exists from the labor market
(5) Start or stop to look for a job
(6) Job−search mechanism

（4）劳动力市场的进入和退出
（5）开始或停止寻找工作
（6）求职机制

FIRMS' DECISIONS :
(7) Sorting candidates and eventual hirings

企业的决策：
（7）候选人筛选和最终雇佣

## C



status regarding their well being, they will leave their current state: quit their job if they are employed or stop looking for one if they are unemployed. Next (5), *Individual* agents, who do not look for a job, have to decide whether to start looking for a (new) job. When deciding to look for a job, *Individual* agents fix their reservation salary before the processes of looking for a job begins. The last stage in the *Individual* agents' decisional procedure is the (6) job-search algorithm, where evaluations of job proposals take place. If a vacancy found, offers a higher remuneration than the reservation salary, the search algorithm ends and the agent candidates to the job. When none of the job proposals pass the reservation salary, the individual does not send any applications and stays in his current state.

根据个体的福利状况，他们将离开当前状态：如果就业，则辞职；如果失业，则停止求职。接下来（5），不主动求职的个体需要决定是否开始寻找（新）工作。在决定求职之前，个体会确定他们的保留薪资。个体决策过程中的最后一个阶段是（6）求职算法，其中对工作提议进行评估。如果发现有一个空缺职位提供的薪酬高于保留薪资，搜索算法就会结束，并且该个体成为该职位的候选人。当所有工作提议都未达到保留薪资时，该个体不会发送任何申请，并维持其当前状态。

The last stage (C) includes the hiring procedure implemented in the firms.

最后一个阶段（C）包括企业实施的招聘程序。

All firms with vacancies gather all the applications they received. Each candidate is first (7) evaluated separately. Those who don't pass a hiring norm are eliminated and those who pass it are compared to one another. The candidate with the best evaluation is hired. In this way, it is possible that a vacancy will stay unfilled if it got zero applications or if none of the candidates passed the hiring norm. With these decisions, the period ends, statistical parameters are calculated and a new round begins.

所有有空缺的企业会收集到他们所收到的所有申请。首先，对每个候选人进行单独评估（7）。未能达到招聘标准的候选人将被淘汰，而通过标准的候选人将相互比较。最终，评估得分最高的候选人将被录用。通过这种方式，如果某个职位没有收到任何申请或者没有一个候选人能够达到招聘标准，那么该职位可能会保持空缺状态。随着这些决策的完成，统计参数将被计算，并开始新一轮循环。

## 3.3 Job Contracts In The French Labour Market



In this study, we are interested in the impact of *job contracts* on the FLM. A Job Contract [9] is established from the moment a person (employee) commits himself to work, through remuneration, for and under the indications and supervision of another person (employer) in a firm. A contract entails a certain number of mutual duties (especially at the end of employment). In the FLM two main types of job contracts exist: CDD - definite term contract (short-term) and CDI - indefinite term contract (long-term). Through our simulation, we would like to analyze the eventual impacts on the labour market of the transition from a CDD/CDI regime to a unified form of those contracts, which is proposed by some economists.

本研究旨在探讨*工作合同*对法国劳动力市场的影响。工作合同[9]是指雇员承诺通过报酬为一家公司工作，并在雇主的指示和监督下履行职责的协议。合同涉及一系列相互义务，尤其是在雇佣结束时。法国劳动力市场存在两种主要类型的工作合同：CDD - 定期合同（短期）和CDI - 无限期合同（长期）。通过模拟分析，我们希望研究从CDD/CDI制度过渡到一种统一形式的合同对劳动力市场可能产生的影响，这也是一些经济学家提出的建议。

We chose to implement the Unified Contract (UC) policies that were proposed by Cahuc and Kramarz [10] as they have the fullest description available. In WorkSim, when a firm hires an employee, it attributes instantly a contract to the job he will occupy. The firm chooses the contract according to: (i) the legal contracts available in the labour market, (ii) legal constraints about portions of types of contracts in a firm and (iii) the expected term of the job. Once a contract has been set, the interactions between the employer and the employee have to follow the traits of this contract. In WorkSim, some of the features are simplified or absent, such as the trial period, minimal term of notice or delay for re-hiring. Table 1 gives the contracts' characteristics that were implemented in WorkSim.

我们选择采用Cahuc和Kramarz [10] 提出的统一合同（UC）政策，因为它们提供了最详尽的描述。在WorkSim中，当一个公司雇佣一名员工时，会立即为他所担任的职位分配一个合同。公司选择合同时考虑以下因素：（i）劳动力市场上可用的法律合同、（ii）公司内各种类型合同比例的法律限制以及（iii）工作预期期限。一旦确定了合同，雇主和员工之间的互动必须遵循该合同的规定。在WorkSim中，一些特性被简化或省略，例如试用期、最短通知期或重新雇佣延迟等。表1列出了在WorkSim中实施的各种合同特性。

表1：合同特性

| 合同类型 | 最短通知期 | 试用期 |
|---------|-----------|-------|
| CDD     | 2周        | 无    |
| CDI     | 1个月      | 2个月 |

注：本文所述特性仅适用于模拟程序，并非真实情况。

A firm will have to end a contract reaching its term (as in CDD) or will be able to keep it indefinitely (as in CDI or UC). At term a procedure of firing will take place where the firm will bear a cost of redundancy payments. While occupying a job, an employee accumulates seniority. This seniority is used in the calculation of the redundancy payment. When a CDD contract is transformed into a CDI contract, this seniority is set to zero.

一家公司在合同到期时必须终止其合同（如CDD），或者可以无限期地保留它（如CDI或UC）。到期时，将进行解雇程序，公司将承担遣散费用。在任职期间，员工会积累工龄，该工龄用于计算遣散费。当CDD合同转变为CDI合同时，该工龄将被设为零。

In a CDD contract firing is not permitted. If an employee is laid-off all expected amount of salaries has to be paid to the employee. When firing under a CDI contract two cases are possible. The first one is an *individual firing*, where the firm decides to fire an employee because of poor professional performance. This entails a redundancy payment, which is proportional to the seniority of the employee in the firm. If y is the seniority in months and s is a monthly salary in euros, the calculation of the redundancy payment PAYCDI is given is equation 1, which is defined in the french law *Article L1234-9*: An employee under a CDI contract, who is fired and has two years of continuous seniority in the service of the same employer..., has the right to a redundancy payment, and Article R1234-2: the redundancy payment cannot be lesser than one tenth of a monthly salary per year of seniority, to which is added one fifteenth of a monthly salary per year beyond fifteen years of seniority.

根据CDI合同，不允许解雇员工。如果员工被裁员，公司必须支付其全部预期工资。在CDI合同下进行解雇有两种情况。第一种是个别解雇，即公司因为员工的职业表现不佳而决定解雇员工。这将导致遣散费用，该费用与员工在公司的资历成比例。如果y表示以月为单位的资历，s表示以欧元计算的月薪，则遣散费用PAYCDI的计算如方程1所示，在法国法律《L1234-9条》中有明确规定：在连续服务于同一雇主两年以上的CDI合同下被解雇的员工...有权获得遣散费，并且根据《R1234-2条》规定：遣散费不能少于每年十分之一月薪加上超过十五年资历部分每年十五分之一月薪。

If *y >* 24,

如果*y > 24，

$$PAY_{CDI}=\sum_{y=0}^{180}\frac{1}{120}s+\sum_{y=180}^{\infty}(\frac{1}{120}+\frac{1}{180})s+legJus\tag{1}$$

根据方程式1，当*y > 24时，遣散费用PAYCDI的计算如下：
$$PAY_{CDI}=\sum_{y=0}^{180}\frac{1}{120}s+\sum_{y=180}^{\infty}\left(\frac{1}{120}+\frac{1}{180}\right)s+legJus\tag{1}$$

$PAY_{CDI}=0$ otherwise.

根据方程式1，当*y > 24时，遣散费用PAYCDI的计算如下：
$$PAY_{CDI}=\sum_{y=0}^{180}\frac{1}{120}s+\sum_{y=180}^{\infty}\left(\frac{1}{120}+\frac{1}{180}\right)s+legJus\tag{1}$$

否则，PAYCDI的值为0。

The $legJus$ term is a supplementary expected cost for CDI contracts that firms have to pay due to costly legal justification procedures. The second case 
is *economic firing*, when the firm looses money and has to destroy filled jobs. In this case the redundancy payment is the double of the one in equation 1.

$legJus$项是指企业因为昂贵的法律证明程序而必须支付的CDI合同的额外预期成本。第二种情况是*经济解雇*，即企业亏损并不得不裁减已填补的职位。在这种情况下，遣散费用是方程式1中的两倍。

The redundancy payment for a UC is given is equation 2.

UC的遣散费用由方程式2给出。

$ PAY_{UC}=\sum_{y=0}^{18}\frac{1}{120}s+\sum_{y=18}^{120}(\frac{1}{120}+\frac{2}{120})s+\sum_{y=120}^{\infty}(\frac{1}{120}+\frac{2}{120}+\frac{1}{36})s+solCont\;\;(2)$

根据方程式2，UC的遣散费用可以表示为：

$ PAY_{UC}=\sum_{y=0}^{18}\frac{1}{120}s+\sum_{y=18}^{120}\left(\frac{1}{120}+\frac{2}{120}\right)s+\sum_{y=120}^{\infty}\left(\frac{1}{120}+\frac{2}{120}+\frac{1}{36}\right)s+solCont$

... 
Where the *legJus* term is replaced by *solCont*, which is a solidarity contribution tax. This tax should help the government in finding a new job for a fired employee. In [10] the solidarity contribution is equal to 1.6% of all paid salaries.

其中，*legJus*一项被替换为*solCont*，即团结贡献税。该税应该帮助政府为被解雇的员工找到新的工作。在[10]中，团结贡献税相当于所有薪资总额的1.6%。

| Features                 | CDD                              | CDI        | UC                     |
|--------------------------|----------------------------------|------------|------------------------|
| When hiring              |                                  |            |                        |
| Maximal term             | 18 months                        |            |                        |
| ∞                        | ∞                                |            |                        |
| accumulated              | accumulated                      | Seniority  | not                    |
| when                     | transformed                      |            |                        |
| into CDI                 |                                  |            |                        |
| When firing              |                                  |            |                        |
| unconditioned            | Firing possibility               | impossible | for individual or eco- |
| nomic reasons            |                                  |            |                        |
| Redundancy payment       | All expected salaries equation 1 | equation 2 |                        |
| Legal justification cost | -                                | >          | 0                      |
| Solidarity contribution  | -                                | -          | 1.6%                   |
| salaries                 |                                  |            |                        |

| 特征                     | CDD                              | CDI        | UC                     |
|--------------------------|----------------------------------|------------|------------------------|
| 雇佣时                   |                                  |            |                        |
| 最长期限                 | 18个月                           |            |                        |
| ∞                        | ∞                                |            |                        |
| 累积                     | 累积                             | 资历       | 不适用                   |
| 转为CDI时                |                                  |            |                        |
| 解雇时                   |                                  |            |                        |
| 无条件限制               | 可能解雇                         | 不可能    ｜ 对个人或经济原因     |
| 解雇补偿金               ｜ 所有预期薪资 方程1             　　＼ 方程2      ／                     　　　　　　　|
   法律合理化成本           -                                >          =0
   团结贡献税              -                                -          =1.6% 
   薪资                    -

## 4 Experimentations, Results And Validation



In this section, we present some simulation results in order to show how Work- Sim functions as a FLM simulator. We demonstrate the abilities of the WorkSim model to reproduce the stylized fact described in the introduction: the discrimination against the young within the FLM. We also study through simulation the impact of the UC on the FLM.

在本节中，我们展示了一些模拟结果，以展示Work-Sim作为FLM模拟器的功能。我们通过模型演示了WorkSim模型能够重现引言中描述的特征事实：FLM中对年轻人的歧视。此外，我们还通过模拟研究了UC对FLM的影响。

## 4.1 Model Input: Simulation Parameters



We use two main categories of exogenous simulation parameters. On one hand (Part I of Table 2), statistical and institutional parameters and distributions, which define the population's properties, as well as the normative (legal) boundaries of the targeted labour market. On the other hand (Part II of Table 2), parameters which were not available from statistics and which we needed to calibrate in order to reproduce a realistic model.

我们使用两个主要类别的外生模拟参数。一方面（表2的第一部分），统计和制度参数以及分布，用于定义人口的特征，以及目标劳动力市场的规范（法律）边界。另一方面（表2的第二部分），我们需要校准的参数无法从统计数据中获取，以便重现一个真实的模型。

In order to obtain the results discussed below, we used 1,000 *Individual* agents and 100 *Firm* agents. We tried to increase these figures (up to 10,000 individuals and 1,000 firms), the results did not significantly differ in the average, increasing the number of agents mainly decreases the oscillations in the transient phases.

为了得到下面所讨论的结果，我们采用了1,000个个体主体和100个公司主体。我们曾试图增加这些数字（增至10,000个个体和1,000个公司），然而结果在平均值上并没有显著差异，增加主体数量主要是为了减少瞬态阶段的波动。

## Part I - Fixed Economic And Legal Parameters



Jobs
Work time per month in hours
140.0
Free time per month in hours
320.0
Individuals
Age in years to enter the labour market
18
Age in years to exit the labour market (retire)
65
Firms
Maximal legal duration in months for a CDD
18
Maximal ratio of CDD contracts in a firm
20%
Lawsuit duration in years for firing under a CDI
2
Contracts
Expected average duration CDD in months
18
Expected average duration CDI in months
120
Expected average duration UC in months
120

就业
每月工作时间（小时）
140.0
每月空闲时间（小时）
320.0
个体
进入劳动力市场的年龄（岁）
18
退出劳动力市场的年龄（退休）
65
公司
CDD合同的最长法定期限（月）
18
公司中CDD合同的最大比例
20%
解雇下CDI合同的诉讼期限（年）
2
合同
预计CDD平均持续时间（月）
18
预计CDI平均持续时间（月）
120
预计UC平均持续时间（月）
120

## Part Ii - Calibrated Parameters



Individuals
Time required for job inspection in hours
4
Vacancies inspected by an unemployed/onTheJobSearch per month
16/4
Firms
Maximal duration for a vacancy in months
10
Maximal portion of employees evaluated monthly per firm (amenity)
0.3
Minimal number of jobs to maintain per firm
3
Productivity ratio to added value
0.6
Market tightness threshold for vacancy creation
2.0

个体
工作检查所需时间（小时）
4
每月由失业/在职求职者检查的空缺数目
16/4
公司
空缺的最长持续期限（月）
10
每家公司每月评估的员工比例上限（福利）
0.3
公司需要维持的最小就业岗位数目
3
生产力与增加值之间的比率
0.6
创造空缺所需市场紧张程度阈值 
2.0

## 4.2 Simulation Protocol



The complete simulation protocol can be described in 7 important parts, illutrated in Figure 2:

完整的模拟协议可以分为7个重要部分，如图2所示。

A (initialization and simulation start)
The *Individual* agent's population
is initialized according to age and sex statistical distributions, available from the French National Institute for Statistics and Economic Studies (INSEE) and abroad (OECD). The *Firm* population is initialized homogeneously with
a fixed number of available vacancies for all firms (simulation parameter). All contracts proposed by *Firm* agents from the initialization until the transition to the UC regime are either CDI or *CDD* contracts.
B (transition phase to current labour market state)
The labour market population after initialization does not actually match the state of a labour market, as no agents are employed and firms have only vacancies. The desired state is reached after a first transition phase where Individual
and *Firm* agents interact through the *SmallAds* agent in order to get jobs
and become employed, and when the statistical information indicates equilibrium in the labour market. The data gathered during this transitional phase must be discarded, as its only purpose is to bring the labour market employment to a similar state as in the real FLM.
C (equilibrium phase of CDD/CDI regime)
After equilibrium in the labour
market is obtained, the CDD/CDI contract phase begins. Data gathered during this phase is used to validate agents' behaviours and global labour market behaviour of our model with respect to the CDD/CDI real data.
D (transition to UC regime)
After a specific duration of maintaining the
equilibrium state CDD/CDI mode, where we observed no transitional shock in the labour market, we perform a transition from the CDD/CDI regime to the UC regime. The transition results in all firms considering only UC contracts for hires.
E (progressive transition to UC only regime)
Existing contacts from the
CDD/CDI regime are kept until the employees either quit, retire, or are fired. Those contracts imply another transition phase towards the state of
the labour market in which there only exist UC contracts. This is an interesting transitional period where we can observe the benefits of the transition to UC contracts on employment and labour market dynamics.

A（初始化和模拟开始）
根据法国国家统计与经济研究院（INSEE）和海外（OECD）提供的年龄和性别统计分布，*个体*主体的人口按照这些分布进行初始化。*公司*人口以固定数量的可用职位均匀初始化（模拟参数）。从初始化到转变为UC制度之前，*公司*主体提出的所有合同都是无固定期限或有固定期限合同。

B（过渡到当前劳动力市场状态）
初始化后的劳动力市场人口实际上并不符合劳动力市场的状态，因为没有主体被雇佣，公司只有空缺职位。通过*SmallAds*主体，个体和*公司*主体在第一个过渡阶段中进行互动，以获得工作并就业，并且当统计信息表明劳动力市场达到平衡时，才能达到所需状态。在这个过渡阶段收集到的数据必须被丢弃，因为它只是为了使劳动力市场就业情况与真实FLM中类似。

C（CDD/CDI制度平衡阶段）
在获得劳动力市场平衡后，开始CDD/CDI合同阶段。在此阶段收集到的数据用于验证我们模型中主体的行为以及与CDD/CDI实际数据相比的全局劳动力市场行为。

D（转变为UC制度）
在维持CDD/CDI模式平衡状态的特定持续时间后，我们观察到劳动力市场没有发生过渡性冲击，因此我们将从CDD/CDI制度过渡到UC制度。这个转变导致所有公司只考虑使用UC合同进行招聘。

E（逐渐过渡到仅使用UC制度）
保留来自CDD/CDI制度的现有合同，直到员工辞职、退休或被解雇。这些合同意味着向劳动力市场状态转变的另一个过渡阶段，在该阶段只存在UC合同。这是一个有趣的过渡期，在这个期间我们可以观察到转向UC合同对就业和劳动力市场动态的好处。

F (UC only regime)
After this last transition phase, the simulation is run
for a specific period of time with only UC contracts.
G (end of simulation)

F（仅使用UC制度）
在这最后一个过渡阶段之后，模拟将在一段特定的时间内仅使用UC合同运行。
G（模拟结束）

## 4.3 Studying A Stylized Fact: Age Discrimination In The Labour Market



We used the Repast agent simulation platform [11] to implement WorkSim. As stated above, in the current FLM there is a noticeable difference between the overall unemployment rate and the younger population's unemployment rate. Statistical information from the INSEE reveals that the unemployment rate of the younger part of the population is more than twice the global unemployment rate (see Table 3 below).

我们采用Repast主体模拟平台[11]来实现WorkSim。正如前文所述，在当前的FLM中，整体失业率与年轻人失业率之间存在显著差异。根据INSEE的统计数据显示，年轻人群体的失业率是全球失业率的两倍以上（详见表3）。

Unemployment rate
Overall
8 %
15 to 24
19.3 %
25 to 49
7.3 %
50 and more
5.4 %

失业率
总体
8%
15至24岁
19.3%
25至49岁
7.3%
50岁及以上
5.4%

In our model, two major aspects have an effect on the unemployment rate:
(i) preferences of firms during job applications filtering and selection, (ii) the productivity of the employees, which can lead to personal firing, if the criteria are not met. A selection of statistical parameters and calibration, which were used to reach the desired unemployment levels, are presented in Table 2. The outcomes of the simulation are shown in CDD/CDI column of Table 4 that represent the result of the simulation under the CDD/CDI regime found in the actual FLM. When comparing to Table 3, we can conclude that our model catches pretty closely the age discrimination phenomenon in the unemployment statistics.

在我们的模型中，失业率受到两个主要因素的影响：
(i) 在求职筛选和选拔过程中，企业的偏好；(ii) 员工的生产力，如果不符合标准，则可能导致个人被解雇。我们使用一组统计参数和校准结果来达到期望的失业水平，这些结果列在表2中。模拟结果显示在表4的CDD/CDI列中，该列代表了在实际FLM中发现的CDD/CDI制度下进行模拟的结果。与表3进行比较后，我们可以得出结论：我们的模型相当准确地捕捉到了失业统计数据中年龄歧视现象。

## 4.4 Impacts Of Uc Contract



The model's output after the transition to UC and a running period was weighted against the positive stylized fact mentioned by Cahuc [12], which foresees that the UC favours a higher level of employment due to the decrease in the cost of job destruction.

在转向UC和运行一段时间后，模型的输出与Cahuc [12]提到的积极事实进行了权衡，该事实预示着由于工作破坏成本的降低，UC有利于更高水平的就业。

As shown in Table 4, the transition to UC leads to a transient decrease of the unemployment rate. In the long run, however, this rate lightly increases (by 0.3

如表4所示，转向UC会导致失业率短期内下降。然而，从长远来看，这一比率略微增加（0.3

CDD/CDI UC transition UC long term Relative difference
Overall
8.1
5.6
8.12
0,3 %
15 - 24
18.4
12.4
17,5
-5 %
24 - 49
6.3
3.5
5,4
-14,3 %
50 and more
6.1
6.1
6,3
3,36 %

CDD/CDI UC转变 UC长期 相对差异
总体
8.1
5.6
8.12
0.3%
15 - 24岁
18.4
12.4
17.5
-5%
24 - 49岁
6.3
3.5
5.4
-14.3%
50岁及以上 
6.1 
6.1 
6.3 
3.36%

%). When we have a closer look at the age intervals, we find out that UC actually reduces the unemployment rate for the young and middle aged (respectively by 5 % and 14.3 %). This was foreseen by many economists, who favoured the UC, as stated above. However, we observe an unexpected increase for the seniors (over 50), of 3.36 % that may explain why the overall unemployment increases. We plan to further extend our experiments and investigations in order to explain this peculiarity.

当我们对年龄区间进行更详细的观察时，我们发现UC实际上降低了年轻人和中年人的失业率，分别下降了5%和14.3%。这与许多经济学家的预期一致，正如前文所述。然而，我们观察到对于50岁以上的老年人出现了意外的增加，增幅为3.36%，这可能解释了整体失业率的增加。为了解释这种特殊情况，我们计划进一步扩大实验和调查范围。

## 5 Discussion And Perspectives



In this paper, we presented an extended agent-based model of the French labour market. We described the agents of the model, the dynamics of the model and its structural properties. Not only did we describe our simulation protocol and its validation against existing statistical data on the real FLM, and put forward the capacity of our model to match existing stylized facts, but we also provided additional information against predicted outcomes of the model with a new contract regime.

本文中，我们提出了一个扩展的基于主体的法国劳动力市场模型。我们详细描述了模型中的主体、模型的动态以及其结构特性。我们不仅描述了我们的仿真协议，并通过与实际法国劳动力市场的统计数据进行验证，展示了我们模型匹配现有简化事实的能力，还提供了针对新合同制度预测结果的额外信息。

We explained the emergence of a macro-level behaviour, characterized by statistical information, by first formulating plausible hypotheses in concordance with the model. The hypotheses were then validated by recollecting other statistical information, which correlated them and provided an analysis of the emergence of a macro-level behaviour from a micro-level model. This was a first step in the validation of emergent behaviour in the model, and we specified the different aspects of validation which need to be further addressed.

我们首先根据模型提出了合理的假设，以解释宏观层面行为的出现。随后，我们通过重新收集其他统计信息对这些假设进行验证，并将其与模型进行相关性分析，从而分析了微观层面模型到宏观层面行为的出现。这是验证模型中新兴行为的第一步，我们还明确指出了需要进一步解决的验证不同方面。

On the conceptual side, our model needs to be confronted with supplementary stylized facts from the FLM and calibrated in order to reproduce those multiple stylized facts in a single run. Further work on the *Individual* and *Firm* agents shall be accomplished in order to better approach the real labour market. We also have further study topics using this labour market model, such as the inadequacy between demand and offer on the labour market, and the study of training support to the unemployed population as suggested in the UC propositions.

在概念层面上，我们的模型需要与FLM的补充式样事实进行对比，并进行校准，以在单次运行中重现这些多样化的式样事实。为了更好地接近真实劳动力市场，还需要进一步研究个体和企业主体。此外，我们还可以利用这个劳动力市场模型进行进一步研究，例如探讨劳动力市场上需求和供给之间的不足问题，以及对失业人口提供培训支持的研究，正如UC提议中所建议的那样。

