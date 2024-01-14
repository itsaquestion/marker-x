# An Agent-Based Simulation Of The French Labour Market : Studying Age Discrimination

Abstract. We present here an agent-based model and simulation of the French labour market - WorkSim. Based on an existing economic model, ARTEMIS, WorkSim is a full multiagent system, where agents (e.g. individuals, firms) possess detailed attributes and elaborated behaviours in order to reflect the real labour market as close as possible. We illustrate our approach with two main simulation results: the reproduction of one peculiar stylized fact, i.e. discrimination against the seniors, and the impact of a new labour contract introduction.

## 1 Introduction

Unemployment is a grave social problem that may have negative impacts not only on the unemployed persons, but also on their relatives and friends or on the entire population of a country (recession etc.). The aim of our work is to show how agent-based modelling and simulation could help (i) understanding how labour market works and (ii) designing better policies in order to improve its performance. In a previous paper [1], we have proposed a multiagent model of a stylized French labour market (FLM), and showed how it could be used to measure the impact of institutional change: the introduction of a new form of hiring contract. A closer analysis of the simulation dynamics enabled us to reveal some drawbacks of this new type of contract (i.e. the increase of precariousness), and also to detect some flaws in the original economic model we started from [2].

In this paper, we introduce a new agent-based model and simulator, named WorkSim, aimed to be more complete and realistic than our previous one. Work- Sim is based on the ARTEMIS [3] economic model, which models the FLM as an endogenously evolving institution. It is almost individual-based, with firms and individuals making decisions at the microeconomic level, and includes a search process and decentralized setting of hiring standards. In WorkSim, we translated ARTEMIS into a full multiagent system, and added several components and processes to get a more realistic model.

In order to illustrate the interest of our approach, we will show how WorkSim tackles one important stylized fact of the FLM : the fact that the unemployment rate is significantly higher for the senior population (i.e. age greater than 50). Moreover, we will also use WorkSim to study the impact of a new type of contract, the Unified Contract (UC), on this peculiar segmentation against the senior job seekers.

This paper is organized as follows. In section 2, we present our approach against existing agent-based models of labour markets. In section 3, we describe the main features of the WorkSim model and in section 4 we present some experimental results, followed by a discussion.

## 2 Agent-Based Models Of The Labour Market

When analyzing existing agent-based models of the labour market some common properties dominate. All models use the notions of workers and employers, who interact on a regular basis. The complexity of each entity or interactions varies.

In this section, we will give a brief and non-exhaustive inspection of the existing qualities of these models, and compare with our approach.

Heterogeneity The various characteristics of the agents contribute to the complexity of the model. One should choose them in the right way, so that they will provide the model with the exact amount of diversity required. Pingle and Tesfatsion [4] introduce heterogeneity by using the memory (the history of interactions) of agents. In that way a persistent relationship between two agents can be studied. Neugart gives agents various reservation wages [5] or different skill endowments [6]. In our model agents' heterogeneity is introduced in several aspects such as the level of professional qualification, past experience in the labour market or the level of productivity. But the most important one is the (physical) age of the agent. Agents enter the simulation at the age of 18 and leave it when they retire from the labour market. In this way, their histories can be studied and the age segmentation in unemployment can be analyzed.

Rationality and information In some models agents are fully rational and have all the needed tools to reach the best decision available. In [6] in order to compute the investment rate of each agent in his own professional training, the average profits of all other agents is taken into account. That means that a full rationality and a full access to other agents' information are possible. This method may facilitate calculations, but it is less realistic when talking about decision making in the real labour market. In our model agents do not have access to all the information they need. Job seekers cannot know all the vacancies that exist in the labour market and they acquire information about new vacancies gradually. Likewise, firms do not know all the job seekers in the labour market. And when they meet a job seeker, they may estimate his productivity, but they get to know its exact value only after the individual agent has started working for them.

Everyday life in the company, which captures the interactions employeremployee, is usually treated implicitly in ACE models. In [4] interactions take place explicitly in the company, where the employees and the employers constantly play a game of strategies. Exogenous events may occur in the labour market, like economic shocks [6] or technological progresses [7] that have direct impacts on everyday life. WorkSim endows the agents with a richer interaction mechanism. Agents may be fired, but they may also choose to quit by themselves. And more importantly, agents may be promoted when staying in the same firm for a sufficient time.

## 3 The Worksim Model

ARTEMIS (Activit´e, Revenus du Travail Et MIcro-Simulation)1 is a model proposed by Ballot in 1980 [3]. Its main objective was to build a simulation that would help to understand the working-class' distribution of revenues in France between 1972 and 1977. The primary units in the model are individuals and jobs, while the decisional units are individuals and firms.

In ARTEMIS individual agents compare possible states (inactivity, current job, new job etc.) by associating a calculated expected utility to each one of them, while firm agents were told exogenously what decisions to make concerning jobs' creation and destruction. In WorkSim, we implemented this parallel process inside the firms. We chose to make them reason with a calculation system of expected costs. Thus a firm will keep an unproductive employee until he retires if the expected cost associated with his firing is greater than the salary cost. For doing so, we had to introduce the concept of productivity level for an individual agent. More importantly, job contracts do not exist in ARTEMIS. This is why we paid particular attention to capture all the aspects of a job contract in the decisional mechanisms of the agents.

On the computational level, ARTEMIS was quite advanced for its time, as the approach Ballot adopted was individual-oriented almost in all its levels. However, we had to increase the complexity of the agents' structure, so they would be independent entities with their personal characteristics (age, qualification level, etc.) and behaviours, which are modelled as a set of performance methods. Each agent has its *decision module*, which is made of three components: perception, *cognition* and *choice*. Agents have states, which correspond to real conditions in the labour market (employed, inactive etc.). Agents shift between states due to the proper choices they made or to the action of other agents. In WorkSim, unlike in ARTEMIS, in order to communicate, agents are endowed with a communication mechanism that enables the exchange and the processing of messages.

## 3.1 Agents In Worksim

In WorkSim *Individual* agents may be hired by *Employer* agents in order to occupy *Job*s in *Firm*s. A *Job* is filled under a specific *Contract*, which gives a legal trait to the relation employer-employee. The *Government* agent sets the different types of *Contract*s available in the labour market. The *SmallAds* agent proxies the vacancies' market, where *Firm*s publish their vacancies and where Individuals consult job offers for eventual job applications.

1 activity, revenue of labour and micro-simulation; for a paper in English, see [8]
The Individual agent (worker) is characterized by his age, his professional qualification level and by his productivity rate. He enters the simulation at the age of 18 and gets older until he reaches the retirement age and exits. He may also gain or loose qualification levels. His productivity increases with the experience he accumulates while occupying a job. The Firm agent (employer) is characterized by its size and amenity. The size of a firm is defined by the number of vacancies and filled jobs it possesses. The amenity of a firm is an indicator of the pleasantness of working in it. In our model this amenity is in opposite correlation with the frequency with which a firm evaluates the productivity of its employees. The more employees are evaluated periodically, the less amount of amenity this firm has.

The Government agent is responsible for determining the *play rules* in the labour market. This agent decides, for example, how the amount of unemployment benefits will be calculated.

## 3.2 Interactions In Worksim: 3 Stages

In our model a whole periodical life cycle takes place in each step (tick), which is equal to one month in the real labour market. During this cycle each agent executes its behavioural methods. Throughout both parts of the simulation the architecture of the agents stays the same and it is just the economic play rules that change. Figure 1 gives a general aspect on a periodical life cycle.

The first stage (A) starts with (1) a personal evaluation of the employees'
productivity. At each period a number of random employees are designated for personal evaluation. If an employee passes a minimal threshold of productivity that is required for a job, the job is maintained, otherwise the employee is fired and the job becomes vacant. After this personal evaluation that may lead to an *individual firing* (see section 3.3), the (2) job management mechanism takes place. During this phase, vacancies that have exceeded the maximal duration threshold are destroyed and in the next step the firm evaluates its economic state (balance). Firms that have a positive balance will open new vacancies hoping to increase their profits. The creation of new vacancies is followed by their publication via the *SmallAds* agent. However, firms that are in deficit have to restrain their economical activities, in order to minimize losses. In this case vacancies are destroyed as well as filled jobs. In the latter case an employee occupying a job will be dismissed, an *economic firing* (see 3.3) will take place and the job will be destroyed. The last decision made by the firms that closes this first stage is (3) promotions. During a promotion, the promoted employee follows a professional training and thus increases his qualification level and his salary.

The second stage (B) is dedicated to the execution of the cognitive and decisional mechanisms of the *Individual* agents. First of all individuals choose (4)
whether or not to participate in the labour market by comparing their current situation with inactivity. If they consider that inactivity has a more profitable

## A

FIRMS' DECISIONS :
(1) Individual evaluation
(2) Jobs creation and destruction
(3) Promotions

          INDIVIDUALS' DECISIONS :
B

(4) Entries and exists from the labor market
(5) Start or stop to look for a job
(6) Job−search mechanism

FIRMS' DECISIONS :
(7) Sorting candidates and eventual hirings

## C

status regarding their well being, they will leave their current state: quit their job if they are employed or stop looking for one if they are unemployed. Next (5), *Individual* agents, who do not look for a job, have to decide whether to start looking for a (new) job. When deciding to look for a job, *Individual* agents fix their reservation salary before the processes of looking for a job begins. The last stage in the *Individual* agents' decisional procedure is the (6) job-search algorithm, where evaluations of job proposals take place. If a vacancy found, offers a higher remuneration than the reservation salary, the search algorithm ends and the agent candidates to the job. When none of the job proposals pass the reservation salary, the individual does not send any applications and stays in his current state.

The last stage (C) includes the hiring procedure implemented in the firms.

All firms with vacancies gather all the applications they received. Each candidate is first (7) evaluated separately. Those who don't pass a hiring norm are eliminated and those who pass it are compared to one another. The candidate with the best evaluation is hired. In this way, it is possible that a vacancy will stay unfilled if it got zero applications or if none of the candidates passed the hiring norm. With these decisions, the period ends, statistical parameters are calculated and a new round begins.

## 3.3 Job Contracts In The French Labour Market

In this study, we are interested in the impact of *job contracts* on the FLM. A Job Contract [9] is established from the moment a person (employee) commits himself to work, through remuneration, for and under the indications and supervision of another person (employer) in a firm. A contract entails a certain number of mutual duties (especially at the end of employment). In the FLM two main types of job contracts exist: CDD - definite term contract (short-term) and CDI - indefinite term contract (long-term). Through our simulation, we would like to analyze the eventual impacts on the labour market of the transition from a CDD/CDI regime to a unified form of those contracts, which is proposed by some economists.

We chose to implement the Unified Contract (UC) policies that were proposed by Cahuc and Kramarz [10] as they have the fullest description available. In WorkSim, when a firm hires an employee, it attributes instantly a contract to the job he will occupy. The firm chooses the contract according to: (i) the legal contracts available in the labour market, (ii) legal constraints about portions of types of contracts in a firm and (iii) the expected term of the job. Once a contract has been set, the interactions between the employer and the employee have to follow the traits of this contract. In WorkSim, some of the features are simplified or absent, such as the trial period, minimal term of notice or delay for re-hiring. Table 1 gives the contracts' characteristics that were implemented in WorkSim.

A firm will have to end a contract reaching its term (as in CDD) or will be able to keep it indefinitely (as in CDI or UC). At term a procedure of firing will take place where the firm will bear a cost of redundancy payments. While occupying a job, an employee accumulates seniority. This seniority is used in the calculation of the redundancy payment. When a CDD contract is transformed into a CDI contract, this seniority is set to zero.

In a CDD contract firing is not permitted. If an employee is laid-off all expected amount of salaries has to be paid to the employee. When firing under a CDI contract two cases are possible. The first one is an *individual firing*, where the firm decides to fire an employee because of poor professional performance. This entails a redundancy payment, which is proportional to the seniority of the employee in the firm. If y is the seniority in months and s is a monthly salary in euros, the calculation of the redundancy payment PAYCDI is given is equation 1, which is defined in the french law *Article L1234-9*: An employee under a CDI contract, who is fired and has two years of continuous seniority in the service of the same employer..., has the right to a redundancy payment, and Article R1234-2: the redundancy payment cannot be lesser than one tenth of a monthly salary per year of seniority, to which is added one fifteenth of a monthly salary per year beyond fifteen years of seniority.

If *y >* 24,

$$PAY_{CDI}=\sum_{y=0}^{180}\frac{1}{120}s+\sum_{y=180}^{\infty}(\frac{1}{120}+\frac{1}{180})s+legJus\tag{1}$$

$PAY_{CDI}=0$ otherwise.

The $legJus$ term is a supplementary expected cost for CDI contracts that firms have to pay due to costly legal justification procedures. The second case 
is *economic firing*, when the firm looses money and has to destroy filled jobs. In this case the redundancy payment is the double of the one in equation 1.

The redundancy payment for a UC is given is equation 2.

$ PAY_{UC}=\sum_{y=0}^{18}\frac{1}{120}s+\sum_{y=18}^{120}(\frac{1}{120}+\frac{2}{120})s+\sum_{y=120}^{\infty}(\frac{1}{120}+\frac{2}{120}+\frac{1}{36})s+solCont\;\;(2)$

... 
Where the *legJus* term is replaced by *solCont*, which is a solidarity contribution tax. This tax should help the government in finding a new job for a fired employee. In [10] the solidarity contribution is equal to 1.6% of all paid salaries.

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

## 4 Experimentations, Results And Validation

In this section, we present some simulation results in order to show how Work- Sim functions as a FLM simulator. We demonstrate the abilities of the WorkSim model to reproduce the stylized fact described in the introduction: the discrimination against the young within the FLM. We also study through simulation the impact of the UC on the FLM.

## 4.1 Model Input: Simulation Parameters

We use two main categories of exogenous simulation parameters. On one hand (Part I of Table 2), statistical and institutional parameters and distributions, which define the population's properties, as well as the normative (legal) boundaries of the targeted labour market. On the other hand (Part II of Table 2), parameters which were not available from statistics and which we needed to calibrate in order to reproduce a realistic model.

In order to obtain the results discussed below, we used 1,000 *Individual* agents and 100 *Firm* agents. We tried to increase these figures (up to 10,000 individuals and 1,000 firms), the results did not significantly differ in the average, increasing the number of agents mainly decreases the oscillations in the transient phases.

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

## 4.2 Simulation Protocol

The complete simulation protocol can be described in 7 important parts, illutrated in Figure 2:

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

F (UC only regime)
After this last transition phase, the simulation is run
for a specific period of time with only UC contracts.
G (end of simulation)

## 4.3 Studying A Stylized Fact: Age Discrimination In The Labour Market

We used the Repast agent simulation platform [11] to implement WorkSim. As stated above, in the current FLM there is a noticeable difference between the overall unemployment rate and the younger population's unemployment rate. Statistical information from the INSEE reveals that the unemployment rate of the younger part of the population is more than twice the global unemployment rate (see Table 3 below).

Unemployment rate
Overall
8 %
15 to 24
19.3 %
25 to 49
7.3 %
50 and more
5.4 %

In our model, two major aspects have an effect on the unemployment rate:
(i) preferences of firms during job applications filtering and selection, (ii) the productivity of the employees, which can lead to personal firing, if the criteria are not met. A selection of statistical parameters and calibration, which were used to reach the desired unemployment levels, are presented in Table 2. The outcomes of the simulation are shown in CDD/CDI column of Table 4 that represent the result of the simulation under the CDD/CDI regime found in the actual FLM. When comparing to Table 3, we can conclude that our model catches pretty closely the age discrimination phenomenon in the unemployment statistics.

## 4.4 Impacts Of Uc Contract

The model's output after the transition to UC and a running period was weighted against the positive stylized fact mentioned by Cahuc [12], which foresees that the UC favours a higher level of employment due to the decrease in the cost of job destruction.

As shown in Table 4, the transition to UC leads to a transient decrease of the unemployment rate. In the long run, however, this rate lightly increases (by 0.3

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

%). When we have a closer look at the age intervals, we find out that UC actually reduces the unemployment rate for the young and middle aged (respectively by 5 % and 14.3 %). This was foreseen by many economists, who favoured the UC, as stated above. However, we observe an unexpected increase for the seniors (over 50), of 3.36 % that may explain why the overall unemployment increases. We plan to further extend our experiments and investigations in order to explain this peculiarity.

## 5 Discussion And Perspectives

In this paper, we presented an extended agent-based model of the French labour market. We described the agents of the model, the dynamics of the model and its structural properties. Not only did we describe our simulation protocol and its validation against existing statistical data on the real FLM, and put forward the capacity of our model to match existing stylized facts, but we also provided additional information against predicted outcomes of the model with a new contract regime.

We explained the emergence of a macro-level behaviour, characterized by statistical information, by first formulating plausible hypotheses in concordance with the model. The hypotheses were then validated by recollecting other statistical information, which correlated them and provided an analysis of the emergence of a macro-level behaviour from a micro-level model. This was a first step in the validation of emergent behaviour in the model, and we specified the different aspects of validation which need to be further addressed.

On the conceptual side, our model needs to be confronted with supplementary stylized facts from the FLM and calibrated in order to reproduce those multiple stylized facts in a single run. Further work on the *Individual* and *Firm* agents shall be accomplished in order to better approach the real labour market. We also have further study topics using this labour market model, such as the inadequacy between demand and offer on the labour market, and the study of training support to the unemployed population as suggested in the UC propositions.