# Introducing A New Job Contract Into The Labor Market: An Agent-Based Computational Approach

We propose to implement and simulate an economic model that studies the potential effects of the introduction of a new type of a job contract into the French labor market. This transition from a classical economic model to an agent-based simulation allows us to reproduce the same tendencies found in the former one and to observe a new dimension that emerges from the agent-based simulation: an increase of oscillations for the characteristic rates revealing an increase of precariousness (job instability) due to the new type of contract. Keywords: Agent-Based Computational Model, Labor Market, Multi-Agent System, Simulation.

## 1. Introduction

In this paper, we aim to build a computational economic model that imitates the conditions of the French labor market in order to study the possible changes in the market, due to the introduction of a new type of a job contract. We intend to take judicious advantage of the tools provided by multi-agent systems (MAS), i.e. systems made of artificial agents that are autonomous and in strong interaction with each other,1 in order to translate an economic model to an agent-based one. The economic model is mainly described by differential equations, whereas in a multi-agent model each agent is an independent entity, constantly interacting with other agents and the environment. This transposition was elaborated in two phases. We started by identifying the main actors in the model. Each actor has his/her own main role, and his/her own behaviors (methods). These behaviors introduce the dynamics to the simulation. We have afterwards integrated the calculation mechanisms of the economic model, which take part in the decision processes of the agents.

## 2 2. Model Features 2.1. Economic Model

The economic model we adopted was proposed by Cahuc and Carcillo2
in order to model the introduction of a new job contract (CNE) into the French labor market. Coming from a microeconomic approach of Labor Economics,3 they used several systems of differential equations to describe the evolution of productivity, unemployment rate, expected utility, decisionmaking, etc. There are three types of job contracts in the model: CDD (short duration), *CDI* (no duration limit), *CNE* (no duration limit but a trial period of 2 years). The life span of the simulation is divided into two parts: one before the introduction of the new contract and the second one after this introduction. For each part, an independent system of equations defines the thresholds for the various behaviors in the market.

In the first part of the simulation two types of contracts exist. CDD is a contract of limited duration, which can last several months but cannot exceed two years. When two years are reached, this contract has to be either destroyed or transformed into a CDI contract. The CDI is a contract of unlimited duration. As the productivity of employees change over time, companies prefer to hire with the CDD contract, which is less binding. An upper limit is introduced to the possible number of hires with CDD per company (the case in the real French labor market).

In the second part of the simulation the CDD contract is replaced with a CNE contract. During the first two years, the company is allowed to fire an employee at the end of every month upon evaluation, without having to justify the decision. In addition to these evaluations, a general evaluation is made at the end of two years: if the contract is not destroyed, it is transformed into a CDI contract. Hires are made only with the CNE contract.

## 2.2. Main Mas Features

When using MAS, one intends to study a specific problem and therefore, chooses a particular architecture for the model. Nevertheless, certain characteristics are common to all MAS.1 Let us briefly review these main features while referring also to our model: The Agents All existing ACE (Agent-Based Computational Economics) models of the Labor Market use Worker agents and Employer agents; some introduce also a Government agent.4 Many researchers want to have the possibility of obtaining "zero unemployment"4,5 which - in their models –
implies to have the same number of workers and employers. Our simulation allows setting the number of agents freely, just before it is launched. There is no obligation of having the same number of worker agents and employer agents. Moreover, the user can choose the maximal number of jobs that a single company (employer agent) will be able to open. In our simulation we set the number of workers to 400 and the companies' to 40. Heterogeneity In the real labor market it is obvious that actors are not homogeneous. One can consider psychological aspects of people, like the level of their education, their history in the labor market or their cognitive abilities. Heterogeneity of agents in ACE simulations is introduced by using the memory (the history of interactions) of agents,5 by having a reservation wage6 or skill endowments.4
In our model heterogeneity of agents is introduced in several aspects: each agent has its own working-site history, productivity rate and "well-being" (the expected utility thresholds with which it reasons). Interactions between agents The ACE community often uses message sending to implement communication and interaction between agents. The protocols for these message-based interactions are not always defined explicitly in the simulations, although we can get a general idea about their structure from principles like "first applied, first hired" or "an agent can not apply to more than one job". Sometimes the order of message sending is crucial, and sometimes it has no importance, as in the Gale-Shapley algorithm.5
We also use message sending to make the agents interact. However, in our model, the type of communication is closer to reality, as it takes place simultaneously and asynchronously: each agent makes its decisions independently of other agents and communicates information whenever it decides to do so.

## 2.3. Agentification 2.3.1. The **Person** Agent (Worker)

The *Person* agent can be in one of *three states*:
worker it fills a job, produces and gets paid. unemployed it has no job, but it is looking for one. In this case it gets unemployment benefits.

non-participant it does not fill a job neither does it look for one. In this case it gets social welfare allowances.

The *Person* agent is characterized by the productivity with which it performs its job. This productivity represents the quantity of work and the investment of the agent in the job it fills.2 This productivity takes its values randomly from a probability distribution every month. We can sum up the Person agent's behaviors in the state transition diagram depicted in Figure
1.

The *Person* agent uses its decision mechanism in two situations: in the state of unemployment and in the state of non-participation. The transition between these two states is due to a reasoning process, where it decides which state will be more profitable economically. Thus, if the expected utility u for unemployed person is greater than the expected utility n for non participating person, the Person shifts from non-participant to unemployed state; otherwise, we have the opposite shift. In order to compute these expected utilities, the agent has to solve a system of four equations (a separate system exists for each model), for more details see.2

## 2.3.2. The **Company** Agent (Employer)

Two states exist for a job in a Company: vacant the *Company* looks for a *Person* to fill the job.

filled the job is populated, and produces a profit.

A *Company* agent can decide not to look for a *Person* to fill a vacancy if it thinks its chances of succeeding are too low, and that it will loose more money looking for en employee than keeping the job closed. If such decision is made after firing a worker, we will say that the job is destroyed. In this model a *Company* agent has a size, which defines the number of jobs it can offer.

The *Company* agent uses its decision mechanism in the beginning of each cycle and after each firing. If a firing takes place or vacancies that have not been published exist in the company, the agent decides whether to open these jobs or not. This decision is made according to a threshold C computed for the profitability of the job. The decision mechanism also intervenes after each productivity report, when evaluating the employee and deciding about his/her future in the company. Figure 2 summarizes the *Company*'s behaviors.

## 2.3.3. The **Matching** Agent

In order to integrate the environment of the labor market, we introduce a Matching agent. The role of this agent is to manage the lists containing the states of the agents and the states of the jobs in the labor market. It computes the matching rate m(θ) for each round that defines how many vacancies and unemployed persons will be coupled per unit of time. Following,2 we use the same matching function: m(θ) = M0θ−η , where M0 and η
are constants in [0,1] and θ is the tightness of the labor market. The fact of having simultaneously unemployed persons and vacancies in the real labor market, could explain the necessity of having such a function. Furthermore it is possible that the offer and demand of different types of jobs do not coincide. We use the matching function to integrate this notion of delay and frictions.

## 3. Results 3.1. The Simulation

We implemented our system using the Cougaar Platform,7 because it is an open source agent-based architecture that emphasizes cognitive agents, groups and organizations. Moreover, it fully supports large-scale applications, and we plan in the future to design a large-scale multi-agent system for the labor market.

## 3.2. Observed Tendencies

Our MAS model reproduces the same average behaviors (tendencies) found in the economic model2 of the labor market.

For instance, the evolution of the *unemployment rate* depicted in Figure
3, after the introduction of CNE, the market's average unemployment rate stabilizes on a higher level than before, since it is easier to fire a person with CNE. Overall, with CNE, we have a transition from 7.1% of unemployment to 16% on average. Moreover, as shown in the Figure 4, persons have a tendency to consider the non-participation state with higher expected utility than the unemployment state. More and more workers, who have just lost their jobs, choose to abandon the option of looking for a new job because they consider the market and the jobs in it to be extremely unstable. The fall of the working population rate drops from almost 90% to 64%, on average.

## 3.3. The Impact On The Well-Being

The novelty in our approach comes from the fact that MAS simulations enable interactions between agents, whose nature is closer to reality. Although in the economic model we can compute the unemployment rate at any given period, we cannot observe the interactions that led to this rate, while our MAS simulation allows us to gain tractability. For instance, in Figures 3 and 4, we can see the increasing frequency and also the increasing deviations from the mean after the introduction of CNE. This phenomenon shows clearly that the well-being of people decreases: the frequency of these oscillations shows frequent shifts from work to unemployment or non-participation and vice-versa. Thus it measures the precariousness (as job instability) of persons and the volatility of the labor market. All three rates (unemployment, vacancy, working population) show an increasing frequency of oscillations, after the introduction of the CNE contract.

## 4. Conclusion And Future Directions

In this study, we translate a pure economic model to a MAS simulation. We reproduce the same results as in the economic model and add a supplementary dimension to the results obtained. Most of the reasoning processes take place explicitly at the agents' level and implicitly in the aggregated labor market level. In our study, the precariousness induced by the CNE contract clearly emerges, and can be measured as a dramatic increase of oscillations for all the rates: unemployment, vacancy, and working population.

Several improvements should help to bring the model closer to reality in the future. First, we could diversify the agents (add more heterogeneity) a little more. By diversity we mean setting a field of expertise for each agent. In that case, an agent will be hired only for jobs, which suit its professional profile. This added feature will make the matching mechanism more realistic and add frictions to the labor market's environment.

Second, the meeting between a worker and an employer may be considered as a bargaining interaction as well, where both sides negotiate the wage, the work conditions and so on. By allowing agents to negotiate, the interactions in the simulation will depend more on the labor market's current situation.

Finally, our model allows an employer to fire an employee, but the opposite case where an employee decides to quit is not permitted. This situation is biased and a future version of our model should include this possibility. Acknowledgement This work was supported by grants from Region Ilede-France.
