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

Keywords: multi-agent simulation; labor market; emergence.

## 1. Introduction

In this paper, we aim to build a computational economic model that imitates the conditions of the French labor market in order to study the possible changes in the market, due to the introduction of a new job contract. We intend to take advantage judiciously of the tools provided by Multi-Agent Systems (MAS), i.e. systems made of artificial agents that are autonomous and in strong interaction with each other [13], in order to translate an economic model into an agent-based one. This approach is common in the Agent-based Computational Economics (ACE) community [12]. The ACE community captures economic changes and developments, and translates them into dynamic computational models. In these models, entities (agents) interact with each other and with the artificial environment. The meaning of computational entity is a collection of data and behavioral methods.

This transposition from a pure economic model to a multi-agent system was conceived in two phases. We started by identifying the main actors in the model. Each actor has his/her own main role, and his/her own behaviors (methods). These behaviors introduce the dynamics to the simulation. We have afterwards integrated the calculation mechanisms of the economic model that are the decision processes of the agents.

The implementation of the multi-agent mechanisms is sometimes straightforward, like when we encode the individual decision process, which helps the agents to choose their future action. However, some variables, which are computed by equations in the classical economic approach, can be directly set in the MAS simulation from the results of the agents' interactions. This is the case, for instance, of the unemployment rate: in the MAS simulation, depending on the decisions of workers and employers, jobs are created or destroyed, positions are filled or persons are fired, and the unemployment rate fluctuates accordingly during the simulation. Hence, one central issue when we design our MAS model is to decide whether a particular variable can be derived from simulation or had to be computed via equations.

In the long run, the goal of this work is to provide a useful and reliable tool to political deciders. A tool that will allow, through the agent-based simulation, to evaluate and predict the efficiency of particular economic policies for the labor market.

## 2. Model Features 2.1. The Economic Model

The economic model we adopted was proposed by Cahuc and Carcillo [2] in order to model the introduction of a new job contract (CNE) into the French labor market. Coming from a microeconomic approach of Labor Economics [3], they used several systems of equations to describe the evolution of productivity, unemployment rate, expected utility, decision-making, etc. There are three types of job contracts in the model: *CDD* (short and fixed duration), *CDI* (no duration limit), *CNE* (no duration limit but a trial period of 2 years). The model is divided into two parts: one before the introduction of the new contract and the second just after this introduction. For each part, an independent system of equations defines the thresholds for the various behaviors in the market.

In the first part of the simulation two types of contracts exist, namely CDD and CDI. CDD is a contract of limited duration. After two years this contract has to be either destroyed or transformed into a CDI contract. The CDI is a contract of unlimited duration. As the productivity of employees change over time, companies prefer to hire with the CDD contract, which is less binding. An upper limit is introduced to the possible number of hires with CDD per company (the case in the real French labor market).

A worker may loose his/her job in two cases. After two years of work with a CDD
contract, the company assesses the productivity of its employee: if this productivity is insufficient, the contract is not transformed into a CDI contract and the person looses his/her job. In the second case, employees working with a CDI contract, are evaluated every month, and can be fired upon each evaluation. However the company must justify this decision. The productivity thresholds for each type of contract are computed separately.

In the second part of the simulation the CDD contract is replaced with the CNE
contract. During the first two years, the company is allowed to fire an employee at the end of every month upon evaluation, without having to justify its decision. In addition to these evaluations, a general evaluation is made at the end of two years: if the contract is not destroyed, it is transformed into a CDI contract. Hires are made only with CNE contract.

The model defines several thresholds, which take part in the decisional mechanisms in the simulation. Employers decide whether to fire employees or not, concerning their productivity, and also decide whether to open vacancies or not. Employees decide whether to look for a job or not to participate in the labor market.

## 2.2. Main Mas Features

When using MAS, one intends to study a specific problem and therefore chooses a particular architecture for the model. Nevertheless, certain characteristics are common to all MAS [13]. Let us briefly review these main features while referring also to our model:

## 2.2.1. The Agents

All existing ACE models of the Labor Market use Worker agents and Employer agents. Some introduce also a Government agent [7]. The number of agents in the simulation can be an important factor. In [6] we find 100 agents and in [7] we find 200, while [9] uses 24 agents: 12 workers and 12 employers. Many researchers want to have the possibility of obtaining "zero unemployment" ([7], [9]), which - in their models - implies to have the same number of workers and employers. Our simulation allows setting the number of agents freely, just before it is launched. There is no obligation of having the same number of worker agents and employer agents. Moreover, the user can choose the maximal number of jobs that a single company (employer agent) will be able to open. In our simulation we set the number of workers to 400.

## 2.2.2. Heterogeneity

In the real labor market it is obvious that actors, let's say workers, are not homogeneous. One can consider psychological aspects of people, like the level of their education, their history in the labor market or their cognitive abilities. Heterogeneity of agents in ACE simulations is used to study specific aspects of the labor market. For instance, [9] introduces heterogeneity by using the memory (the history of interactions) of agents. In that way a persistent relationship between two agents can be studied. In other models, agents have various reservation wages [6] or skill endowments [7].

In our model agent's heterogeneity is introduced in several aspects: each agent has its own working-site history, productivity rate and "well-being" (the expected utility thresholds with which it reasons).

## 2.2.3. Goals Of The Agents

We can often see that agents do not have an explicit goal. In ACE models the agents may have a reasoning process that allows them to maximize their profit, for example by choosing their next action according to a profit matrix [9]. In [7], agents imitate a winning strategy without knowing what the meaning of the term "winning strategy" is. As in our model agents live and reason constantly, their permanent goal is to improve their situation, by choosing a higher expected utility state.

## 2.2.4. Representations Of Information

The information in the simulations has two main characteristics.

- A *complete* information environment, where everybody knows or may know
everything.
- A *perfect* information environment, where the information, which the participants have, is a 100% exact.
We can find different approaches dealing with information in the simulations. In [7] an assumption of complete and perfect information is made. To compute the investment rate of each agent in his own professional training, the average profits of all other agents is taken in account. This method may facilitate calculations and may also simplify implementation, but it is less realistic when talking about decision making in the real labor market. Incomplete and perfect information is used in [9], where the agents play a strategy game over a profit matrix of a "prisoner's dilemma" type. As both agents choose their strategy simultaneously they ignore the adversary's strategy, the type of information is incomplete. Then again, as both agents know the matrix, and gain exactly what they should, the information is also perfect in this case. [4] uses incomplete information when agents do not know (or have access) to all the vacancies in the labor market. A searching mechanism for the agents is implemented in the simulation, but this mechanism is quite demanding (from a cognitive point of view), so that agents cannot discover all vacancies in the market. Uncertainty is introduced by [7] in form of probability. Shocks hit sectors in the labor market, which oblige employers to close down their companies. Neither companies nor employees can predict these shocks, in this case an imperfect information assumption is made. In our model the nature of information varies according to the types of agents (see section 3 for more details on agents in our system). *Person* agents (i.e. job seekers or employees) are somewhere between complete and incomplete information. On one hand, they use the rate of unemployment to calculate their chances and their expected utility of finding a job, a process that uses complete information. This process is not completely unrealistic, as persons do read the newspaper and can get a general impression of the unemployment situation in the labor market. If a person sees that the unemployment rate is high, he/she may think that his/her chances of finding a job are too small and so, give up and leave the labor market. On the other hand, the *Person* agent cannot know nor estimate the duration of time required to be matched with a job offer: this incertitude is a clear case of incomplete information. This same kind of analysis is valid for *Company* agents (employers) as well. As all reasoning processes in the simulation take place simultaneously for all agents, we can say that the information that agents have is imperfect. At the moment an agent decides about his future (taking in account, let's say a certain unemployment rate), it is possible that many other agents have gone through the same process and have decided to change their state. So the agent has really a quite imperfect image of the situation in the labor market.

## 2.2.5. Interactions Between Agents

The ACE community uses message sending to implement communication and interactions between agents, as it is often done in MAS. The protocols for this messages sending are not always defined explicitly in the simulations, although we can get a general idea about their structure from principles like "first applied, first hired" or "an agent can not apply to more than one job" [9]. Sometimes the order of message sending is crucial to the results obtained, and sometimes it has no importance, as in the Gale-Shapley algorithm [9]. We also use message sending to make the agents interact, like transmitting information to each other. However, in our model, the type of communication is closer to reality, as it takes place simultaneously and asynchronously: each agent makes its decisions independently of other agents and communicates information whenever it decides to do so.

## 2.2.6. The Environment

The most complex environment is dynamic, stochastic, inaccessible, nondeterministic, non-markovian and *continuous*, alas, this is the case of the labor market. To be able to deal with this complexity ACE researchers use various simplifying hypothesis. The environment in previous ACE experiments is usually markovian, deterministic, static and *discrete*.

In our simulation, the environment is *dynamic* - the unemployment rate can change every round, *non-markovian* - the current productivity of an agent does not depend on its previous productivities, *inaccessible* - agents cannot know the decisions of other agents concerning their future, *deterministic* - the actions of agents are executed fully and *discrete* - each agent has its own life cycle.

## 2.2.7. Everyday Life In The Company

Everyday life in the company is usually treated implicitly in ACE models. From the moment when a person has been hired, his/her wage and his/her productivity stay constant over time. Exogenous events may occur in the labor market, like economic shocks [7] or technological progresses [4]. In [9] interactions take place explicitly in the company, where the employees and the employers constantly play a game of strategies. This game is played over a profit matrix by choosing a cooperation strategy or a defection strategy.

Our simulation does not include a bilateral relationship in the company. A
worker performs with certain productivity and it is the employer who decides whether to keep or to fire this worker. The wage of the worker is constant over the time that he/she works, as his/her expected utility. The separation between a worker and an employer can be initiated only by the latter one that means that en employee cannot quit.

## 3. Our Model'S Agentification

The agents participating in the model are:

- The *Person* agent, who produces while working and gets paid a salary. It
can be employed, unemployed or not participating in the labor market.
- The *Company* agent, who hires and fires *Person* agents. It can also decide
whether to open a job or to keep it closed.
- The *Matching* agent, who represents the environment of the labor market.
It matches unemployed *Person* agents with vacant jobs.
- The *Government* agent, who sets economic policies in the labor market.

## 3.1. *The* Person Agent (Worker)

The *Person* agent can be in one of *three states*:
worker it fills a job, produces and gets paid. unemployed it has no job, but it is looking for one. In this case it gets unemployment benefits.

non-participant it does not fill a job neither does it look for one. In this case it gets social welfare allowances.

The *Person* agent has a capital which is the sum of money it earns by filling a job or the allowances it gets. It is characterized by the productivity with which it performs its job. This productivity represents the quantity of work and the investment of the agent in the job it fills [2]. This productivity takes its values randomly from a probability distribution every month. We can sum up the *Person* agent's behaviors in the state transition diagram depicted in Figure 1.

The *Person* agent uses its decision mechanism in two situations: in the state of unemployment and in the state of non-participation. The transition between these two states is due to a reasoning process, where it decides which state will be more profitable economically. Thus, if the expected utility u for an unemployed person is greater than the expected utility n for a non participating person, the *Person* agent shifts from non-participant to unemployed state; otherwise, we have the opposite shift. In order to compute these expected utilities, the agent has to solve a system of four equations (a separate system exists for each model). For more details see [2].

## 3.2. *The* Company Agent (Employer)

In the labor market the *Company* agents offer vacancies, decide whether to hire a person or not and eventually decide whether to keep or to fire this person. Two states exist for a job: vacant the *Company* looks for a *Person* to fill the job.

filled the job is populated, and produces a profit.

A *Company* agent can decide not to look for a person to fill a vacancy if it thinks its chances of succeeding are too low, and that it will loose more money looking for an employee than keeping the job closed. If such decision is made after firing a worker, we will say that the job is destroyed. In this model a *Company* agent has a size, which defines the number of jobs it can offer.

The *Company* agent uses its decision mechanism in the beginning of each cycle and after each firing. If a firing takes place or vacancies that have not been published exist in the company, the agent decides whether to open these jobs or not. This decision is made according to a threshold C computed for the profitability of a job. The decision mechanism also intervenes after each productivity report, when evaluating the employee and deciding about his/her future in the company. Figure 2 summarizes the *Company* agent's behaviors.

## 3.3. *The* Matching Agent

In order to integrate the environment of the labor market, we introduce a Matching agent. The role of this agent is to manage the lists containing the states of the agents and the states of the jobs in the labor market. Moreover, as we know, looking for a job consumes time and money. Furthermore it is possible that the offer and demand of different types of jobs do not coincide. The *matching function M* is used to introduce this notion of delay and frictions. Hence, the matching agent computes at each cycle M(*U, V* ), the number of hires as a function of the number of unemployed persons U and the number of vacant jobs V . Following [2], we use the same matching function and parameters: M(*U, V* ) = *V.m*(θ), where :

$m(\theta)=m_{0}\theta^{-0,5}$
m0 = 0.772 for the best fit to the real French Market data, and θ =
V
U is the tightness of the labor market.T

## 3.4. *The* Government Agent

The main functionality of this agent is to set the economic policies in the labor market. The agent calibrates the model and is responsible for setting the policy wanted, for example which contracts will be available (CDD, CDI, CNE ...). This A multi-agent simulation of a stylized french labor market : emergences at the micro-level.

agent decides the amount of annual salaries for the different types of contracts, unemployment benefits, social welfare allowances etc. It also computes the benefits paid to fired workers.

## 4. Results 4.1. The Simulation

We implemented our system using the Repast Platform [10]. The simulation takes place in two parts, each part corresponds to different types of contracts. In the beginning we can set the number of agents (Persons, *Companies*) and the size of Companies that will take part in the simulation. We can also modify the level of salaries in the model, the amount of the unemployment benefits and the level of social welfare allowances. The new thresholds for the decision mechanisms are computed automatically by the system. The simulation is then launched.

The agents are created and start to interact with the environment of the labor market and with each other. The *Person* agents decide constantly whether to look for a job or not to participate in the labor market, while the *Company* agents decide whether to open jobs or not. The user can observe the unemployment rate, the vacancy rate, the participation rate, the tightness of the labor market and the messages sent between the agents. The user then decides on what moment to introduce the new contract and the simulation adopts automatically the new model. In the results below, we used 11000 agents. The unemployment rates for the two parts of the simulation are depicted in Figure 3.

The graph shows that before the introduction of the CNE contract, the unemployment rate stabilizes and that right after this introduction, there is a decrease in
10
Zach Lewkovicz and Jean-Daniel Kant the rate and a second stabilization in a higher level. These same results are found in the economic model, where the economists explain that in the long term the unemployment rate will restabilize at a superior level.

## 4.2. Detecting Flaws In The Matching Function

However, when looking at the instantaneous data set measured at each cycle in Figure 3, one can see that there are many drops to zero. This is the case for the two parts of the simulation (i.e. before and after the CNE's introduction). . The only differences are the frequency of drops and the amplitudes of these oscillations, they are both higher during the CNE's regime. Because it is unrealistic to obtain a zero-level of unemployment and this was not found in the original simulation from Cahuc and Carcillo, we had to understand the causes of these abnormal oscillations.

In order to answer this question one has to study the matching process in the model. As mentioned above in 3.3, the matching process computes at each round the number of hires, M(*U, V* ) = *V.m*(θ). From Eq.(1) and recalling that θ = *V/U*, we derive :

$$M(U,V)=V.m_{0}.V^{-0,5}.U^{0,5}=m_{0}.U^{0,5}.V^{0,5}\tag{2}$$
This function has the type of the *Cobb-Douglas function* :

$M(U,V)=A.U^{\alpha}V^{1-\alpha}$ (3)
with A = m0 and α = 0, 5.

When analyzing this Cobb-Douglas function, Boyer found that is has a quite restricted definition domain, as depicted in Figure 4 [1]. The function calculates relevant rates only when its arguments take their values in the domain represented by the white cone (EOF). If U and V take their values in the gray area (*V OE*), the number of unemployed U drops to zero because there are too many vacancies and all the jobs are matched. In the gray area (FOU), the number of vacant jobs V drops to zero because there are too many unemployed and all the jobs are matched (see [1] for details).

When it is used with the macro-level economic model, we can ensure at the average to stay within the definition cone (EOF). This is not the case at the microlevel, the agent's interactions can produce any values of (*U, V* ) leading to extreme cases (U = 0 or V = 0) after the matching process being applied. This explains the unrealistic drops of the unemployment rate to zero found in Figure 3.

## 4.3. Correcting The Matching Function

To sum up the results found in the last paragraph above, we could state that in our simulation of the CNE the Cobb-Douglas type of a matching function is microfounded, as it shows an abnormal behavior at the micro level. We proposed to replace it with another matching function, that was proposed by Stevens [11], in the case when search and recruitment effort are exogenous that is the case in the CNE model. The new matching function we introduced into the model is presented in Equation 4.

$$m(u,v)=m_{0}\frac{uv}{u+v}\tag{4}$$
This function fulfills all the requirements stated by Petrongolo and Pissarides [8], and its domain definition is ℜ2. The results obtained with the new function are depicted in Figure 5. One can see that after an oscillatory period the unemployment rate stabilizes and no drops to zero are detected.

12
Zach Lewkovicz and Jean-Daniel Kant

## 4.4. Results' Analysis

The results we found in our simulations using the new matching function resemble to the results found in the economic model: our MAS/ACE model reproduces the same average behaviors in the labor market. We find the same tendencies while looking at the rates of unemployment, participation etc.

For instance, if we take the evolution of the *unemployment rate* (percentage of unemployed persons within the labor force population) depicted in Figure 5, after the introduction of CNE contracts, there is a temporary drop in the unemployment rate, due to the brief rise in the vacancy rate (percentage of vacant jobs) and the decrease of the labor force. After this brief drop, the market's average unemployment rate stabilizes on a higher level than before, since it is easier to fire a person with CNE. Overall, with CNE, we have a transition from 7.1% of unemployment to 16% on average.

Similarly, with the shift to CNE, the vacancy rate (percentage of vacant jobs) is increasing, as shown in Figure 6. The companies decide to open new jobs, because their expected value is higher if filled than if vacant. Regarding individual persons, when fired, the expected utility tends to be higher in the non-participation then in the unemployment state, so they do not look for a new job and the number of vacancies stays high. In our simulations, we measured a shift from 21% to 29% in the vacancy average rate. Finally, as shown in the Figure 7, persons have a higher tendency to consider the non-participation state with higher expected utility than the unemployment state. More and more workers, who have just lost their jobs, choose to abandon the attempt of looking for a new job because they consider the market and the jobs in it to be extremely unstable. The fall of the working population rate drops from almost 90% to 64%, on average.

## 4.5. The Impact On The Well-Being

The novelty in our approach comes from the fact that MAS simulations add the possibility of taking into account more realistically the interactions between agents. Although in the economic model we can compute the unemployment rate at any given period, we cannot observe the interactions that led to this rate - our MAS simulation allows that. For instance, in Figures 5-7, we can see the increasing frequency and also the increasing deviations from the mean after the introduction of CNE contracts. This phenomenon clearly shows that the well-being of persons decreases: the frequency of these oscillations shows frequent shifts from work to unemployment or non-participation, and vice-versa. Thus it measures the precariousness of persons and the volatility of the labor market. All three rates (unemployment, vacancy, working population) show an increasing frequency of oscillations, after the introduction of the CNE contract.

## 5. Conclusion And Future Directions

In this study, we translated a pure economic model into a MAS simulation and reproduced the same results as in the economic model. Moreover, a new dimension emerged that could not be explicitly shown in the original model : the precariousness induced by the CNE contract.

Contrary to most approaches in economics, we adopted a bottom-up approach.

This approach is based on a higher granularity of the model. Most economic models, including models that deal with microeconomic questions, use to average behaviors of agents when reasoning about durations or decision-making. When using an agentbased simulation, we have to look into the agent, and thus to define its architecture. Many types of architectures are possible. In the future, we plan to model the agent's cognition more profoundly, in order to tackle more adequately the human decision
14
Zach Lewkovicz and Jean-Daniel Kant processes involved in the labor market. For such a purpose, we could use and adapt our cognitive architecture CODAGE [5] we already applied for an experimental financial market. The whole idea is to "humanize" more the agents, to provide them with finer and more precise reasoning and decision abilities, something that will hopefully bring them closer to real human agents in the labor market.

We have not so far exploited all the possibilities provided by MAS, and several improvements will help to bring the model closer to reality in the future. First, we could diversify the agents a little more. By diversity we mean setting a field of expertise for each agent. In that case, an agent will be hired only for jobs, which suit its professional profile. This enrichment will make the matching mechanism more realistic and add frictions to the labor market environment.

Second, in the real world, the matching process is not perfect and straightforward. Even if an employee meets with an employer, a matching does not necessarily take place. A selection or sorting phase may be integrated into both sides. An employee may wave away a job offer because he/she finds the work conditions not satisfying enough. An employer may refuse a candidate because of a bad interview, a bad vita or simply because he/she prefers hiring someone else.

Third, the meeting between a worker and an employer may be considered as a bargaining interaction as well, where both sides negotiate the wage, the work conditions and so on. This first meeting may end in separation or in hiring. By allowing agents to negotiate, the interactions in the simulation will depend more on the labor market situation. If the unemployment rate is low an employee should have more power when negotiating his/her work conditions then when there are a lot of unemployed persons and not many vacancies.

Finally, our model allows an employer to fire an employee, but the opposite case where an employee decides to quit is not permitted. This situation is biased and a future version of our model should allow an employee to quit his/her job as well.