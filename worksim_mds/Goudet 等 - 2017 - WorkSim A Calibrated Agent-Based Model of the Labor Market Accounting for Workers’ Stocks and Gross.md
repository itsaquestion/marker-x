# Worksim - A Calibrated Agent-Based Model Of The Labor Market Accounting For Workers' Stocks And Gross Flows

## Abstract

This paper presents an agent-based model of the labor market. It simulates the market in the recent period at the aggregate level and at the level of the principal categories of labor, on the basis of the decisions of heterogeneous agents, firms and individuals, who interact. These decisions rely on individual computations of profits and utilities, although rationality is bounded in such a complex environment. The theoretical structure that underlies the decisions is the search concept. We apply this framework to the case of France in 2011. The model is at a scale of 1/4700. It is fairly detailed on the institutions of the labor market that constrain the agents' decisions. Finally it is calibrated by a powerful algorithm to reproduce a large number of variables of interest. The calibrated model presents a consistent accounting system of the gross flows of the individuals between the main states, employment, distinguishing open ended contracts and fixed duration contracts, unemployment and inactivity. The simulation of the gross flows accounts enables us to analyze the patterns of mobility in a way that the observed statistics on gross flows, which are partial, cannot do. The model then characterizes the nature of the labor market under study, reproducing the high proportion of the fixed duration contracts in the hiring flows, and it points to a dualism of the French labor market.

## 1 Introduction

The model WorkSim is a novel tool of analysis for labor markets. The first objective of the model is to reproduce the gross flows between the important states: employment (distinguishing fixed term contracts and open ended contracts), unemployment and inactivity, and the ratios of individuals in these states. The novelty of the model is that it simulates the gross flows on the basis of the rational decisions of individual heterogeneous agents. The gross flow concept is crucial because each flow unit is caused by a decision that involves comparing idiosyncratic expected benefits and costs for the agent, and a flow unit will yield idiosyncratic benefits and costs for the agent and possibly other agent. It is not the case for transition based models that imply some time aggregation. Once the model is calibrated, the second objective is to characterize the nature of the labor market under study. This is done, first by examining the patterns of flows and stocks at the aggregate level and at the levels of different categories of labor, second by sensitivity experiments, modifying some exogenous parameters and variables such as the demand for the good. Finally the model once calibrated is a tool for experimenting labor market policies, including changes in the labor law. The multi-agent methodology is the perfect tool for such a research program, since it can model institutions precisely, and account for heterogeneity and individual interactions. Simulation results enable us to compute aggregate variables such as the flows and the stocks, and finally the individual careers and the main types of trajectories.

However, the labor market is complex and this means that the modeling progresses only by steps. The present version is consistent as a stock-flow model and more detailed than other existing stock-flow models of the labor market, analytic, econometric, or multi-agent. The model builds on the experience of model ARTEMIS proposed by Ballot ((Ballot, 1981, 1988, 2002)) and a preliminary version of WorkSim by Lewkovicz and Kant (Lewkovicz & Kant, 2008). ARTEMIS
is the first multi-agent model to have modeled the gross flows between the three main states of the individuals, with the addition of on-the-job search as a state. This was also done within an institutional framework, notably with a temporary help firm, and firing costs. The accounting framework of stocks and flows allowed for a rigorous analysis of the competition between the different categories of labor. It threw some light on the effects of aggregate shocks or institutional change on the displacement or integration in open ended contracts of such categories as the young workers, female workers, low educated workers. The underlying hypothesis, that results confirm, is that these effects on the gross flows and stocks are highly non linear, or even non monotonic, and difficult to obtain through available econometric methods. For instance, a negative demand shock could possibly lower the unemployment rate of young non educated workers who would abandon participation, but raise unemployment for the other workers.

The version of WorkSim presented in this artical aims to analyze the French labor market in
2011. However the methodology we have developed will enable researchers to use it for other countries as well. WorkSim puts emphasis on one of the most important features of the French labor market that is the major role of the fixed term contracts, about 80% of the hires in 2011. The present version is mainly devoted to the reproduction of the flows on the basis of our modeling of rational decisions. It then provides a first characterization of the patterns of flows of the different categories of workers, which is key for understanding the nature of a labor market, letting policy design for future work. Due to lack of space, we mainly restrict our economic analysis to the observation of a segmentation, and then throw a first light on the fundamental question: is the segmentation of a temporary or permanent nature for a generation of individuals?

This paper is organized as follows. Section 2 will present the theoretical framework and related models, section 3 will develop the model. Section 4 will deal with the calibration procedure, and section 5 the first characterization of the French labor market on the basis of the results. Section 6 concludes.

## 2 Theoretical Framework And State Of The Art 2.1 Extending Search Theory

WorkSim like ARTEMIS is grounded in the concept of search (Phelps, 1970). It gives its intellectual coherence to the model, and the foundations for many of the decision rules. The search concept is necessary to distinguish the two states of "unemployed" and "inactive" on the basis of rational decisions of agents. There is indeed a flow from unemployment to inactivity, because the unemployment utility (expected gains from search minus time foregone) may become lower than the utility of inactivity (including welfare and free time). In that case, the individual stops search and becomes inactive. This is distinct from the fact that part of the inactive persons do not want to work because they have some other resources and value non-working time (caring for children). When the cost of search is introduced, the concept of search then also explains - and it was the seminal idea of Stigler (1962) - that workers will sometimes prefer not to apply for a job and spend some more time unemployed to try to obtain a better job. They adopt a stopping rule that sets the minimum utility a job must offer to induce them to apply. These formalizations follow the definition of unemployment as a state in which workers act actively to find a job. This is a definition adopted by the International Labor Office (ILO), and the French National Statistical Institute (INSEE) in the *Employement Survey*, an enquiry that measures some of the variables the model wants to reproduce. In WorkSim the basic concept of search is extended in three directions, in order to build a general theory of mobility :

1. *Search is done also by firms* that symmetrically look for workers who are high in the productivity distribution. They prefer to keep a job vacant than hire a worker with a poor productivity. An optimal stopping rule taking the form of a minimum productivity requirement or hiring norm follows. A further possibility is that the addition of the costs of search and other costs (wages, expected firing costs...) makes the job unprofitable and it is suppressed.
2. *The search calculus is extended to all voluntary decisions by workers* such as quits to search
and on-the-job search. Symmetrically, the firms take into account the search costs of replacement when they consider firing a worker, for insufficient productivity. Other relevant
costs and benefits are also taken into account for firing, not renewing a fixed duration contract.... Finally the hiring decision is the result of the sequential decisions of the worker who applies and the firm which selects and hires. Moreover we do not use any matching function - unlike in the matching models such as the canonical model of Mortensen and Pissarides (Mortensen & Pissarides, 1994) - as it is an aggregate artefact, likely not to be robust to large changes in the labor market, and with weaker microeconomic foundations than our double search decisions. The model definitely belongs to the pure search models,
fully taking into account the heterogeneity of jobs and workers1.
(a) Our model integrates *wage rigidities* based on the realistic assumption that firms have
often several jobs, which is not the case in the searchor matching models. Then equity requires a fixed wage structure between insiders'jobs. The model then allows for the differentiation between demand shocks and productivity shocks, while existing search models do not usually deal with this topic. WorkSim then contains some Keynesian features. Demand shocks explain part-time, economic dismissals, job creations and promotions in the model, while productivity changes explain dismissals on personal grounds, and some hires. This distinction has also some importance since the model deals only with the labor market, with no feedback on the goods market. The quantity demanded for the goods is exogenous.
However a major difference between WorkSim and the analytical search models relies on our utilization of the concept of Simon's *bounded rationality* to model the decisions (Simon, 1955).

Two major arguments can be given:

1. First, dynamic programming algorithms used to solve the decision problem in analytical
search theory cannot be used in a model in which heterogeneous agents move sequentially into many states over time and compete.
2. Second, according to bounded rationality theory, real agents have limited capacities in
terms of computation and memory. They might therefore use simple rules, but a very important behavioral addition in our approach is that they can revise their decisions or even their rules thanks to *learning* and collecting information. This continuous learning is in fact very coherent with search theory. However, in order to compute equilibrium, analytical models assume perfect rationality and individuals have a lot of information such as the
true distribution of wages, and firms know the true distribution of productivities. By contrast, in WorkSim, we model "simple" decision rules - that comply with bounded rationality - and the learning processes.

## 2.2 Related Agent-Based Models

The contributions to the multi-agent literature on labor markets must also be assessed. This literature is thin but has a long history. Bergmann (2002) has developed a simple model of search by both sides of the market and obtained simultaneously vacant jobs and unemployment. Eliasson (1977) has built a Keynesian and Schumpeterian micro-to-macro model that treats only firms as individual agents but the number of workers in a firm can vary and unemployment is computed. It stresses poaching of labor by firms that grow and the wage competition that eliminates the firms that are not profitable. An extension by Ballot and Taymaz (2000) added human capital and the growing firms poach the more educated workers, enhancing a virtuous cycle of innovation and profit. ARTEMIS, the ancestor of WorkSim, stressed the different personnel management types to study segmentation. Some firms offer internal labor markets with a high selection at entry, but also training and promotion, and others offer lower wages, less selection, no promotion ("secondary jobs"). Moreover firms can recur to temporary help work, with very short contracts, but less selection than for internal labor markets. The model generates a temporary segmentation of the young workers. Then, a negative demand shock affects very differently the categories of labor, precluding the progressive integration of young workers in the internal labor markets. This leads to a permanent segmentation with serious life cycle consequences. WorkSim brings many improvements over ARTEMIS. It replaces the "secondary" jobs by the fixed duration contract with the main legal specificities that apply to them in 2011. It also models the accumulation of several types of human capital, and considers that workers have an idiosyncratic component in productivity so that the employers learn - but never know perfectly - the productivity of their employees. This is a source of personal dismissals, while in ARTEMIS the workers when hired became equally productive through an adapted training. Moreover the model is calibrated by a powerful algorithm to fit year 2011, while ARTEMIS was calibrated by hand to fit the evolution 1972-75. In WorkSim, a simulation is repeated 200 times to average out the stochastic effects while ARTEMIS could not - for computational cost reasons - be tested with more that a few runs. In order to focus precisely on the role of fixed duration contracts, we do not integrate - at this time - the temporary help jobs modeled in ARTEMIS.

The years 2000 have mainly seen the construction of multi-agents models aiming at theoretical research, such as introducing networks on the labor market, i.e. the role of social relations in the hiring process, a way to go beyond random search that is relevant in some contexts (Tassier & Menczer, 2001), and the study of the robustness of aggregate relations such as the Beveridge curve that describes the negative relationship between vacancies and unemployment, if one starts bottom up by modeling the firms and individuals decisions (Richiardi, 2006). However, one model has tried to model the French labor markets with some of its specificities. Barlet et al. (2009) simulate the French labor market for year 2006. They distinguish individuals and jobs but not firms as such although there is a labor demand side, with creations and destructions of jobs based on a desired margin and demand. Fixed duration and open ended contracts are also distinguished. The flows are obtained from transition rates, often exogenous, and the dismissals are determined by the destruction of jobs exclusively (and not by insufficient productivity). The model is calibrated using an indirect inference method to fit a set of real data, and is then used to study the effects of the rise of the minimum wage and a lowering of the social charges on the firms. However, there are no inactive individuals in their model, hiring is performed through an aggregated matching function, quits are exogenous, and the terminations of fixed duration contracts are random. One another important difference with ARTEMIS and WorkSim is that the period is the year and therefore the gross flows are not reproduced, which prevents a fine analysis of fixed duration contracts and unemployment spell durations.

The version of WorkSim (in the line of ARTEMIS) presented here then goes beyond the existing multi-agent literature on the labor markets in three directions, as the following sections will show:

1. It is the only model to be grounded in a double stock-flow accounting, one for the individuals, one for the jobs, and all the flows between the stocks considered are simulated. This accounting is the equivalent of the financial stock-flow accounting for ACE macroeconomic models, a guarantee of consistency. It also allows for a easy description of the labor market dynamics at the aggregate and at any disaggregation level of interest, and the
highlighting of the competition between categories of labor (young, adults, seniors....) with possible crowding out effects.
2. It models the institutions and the labor law at their level of direct impact (the microeconomic level), since they are rules of the game that agents know and take into account in their decisions. The diverse forms of labor contracts, with very important differences, are probably the major feature of the French labor market, and they are at the heart of the
model, since they modify the flows 2.
3. Most of the gross flows are generated by rational decisions based on an enlarged search
theory, and the effects of shocks we will study then integrate the agents responses and interactions within the rules of the game and the accounting constraints. Our multi-agent model then provides a tool to explore rigorously the complex system constituted by the labor market.

## 3 Model Description 3.1 The Agents In Worksim

In WorkSim, the agents are heterogeneous. They have specific attributes determined once and for all at their creation and internal variables which evolve all along the simulation. The agents attributes and variables are shown in Appendix A. There are two types of agents: Private Firms and *Individuals*. At its creation, each firm starts with at least one worker to run the company, denoted in this paper as the managing director. The *Individuals* are grouped in households and the simulation evolves in a closed population. The individuals can marry each other, have children, break up, and therefore the decisions of one member of the household may have an impact on the other members.

The agents under 15 or over 65 years belong to these household but are not *instantiated* as full agents and do not take decisions in the model. However, these *non-instantiated agents* indirectly participate through the economic decisions of the other members of the household (eg. the number of dependent children is taken into account in decisions of transition to inactivity, the retirement pension is included in household income). The individuals under 15 years become full agents in the model at the age of 15, and some remain in the school system while others enter the labor market.

## 3.2 Environment

In addition to these agents. the model uses three *artifacts* 3:

- *JobAds*, which receives job offers from the firms and job applications from the job seekers.
Dissemination of information, however, is based on the job search process described in more detail below (see sections 3.6.4 and 3.7), according to the principles of the theory of search.
- a "*statistical institute*" that calculates all the statistics from a simulation model. and disseminates some information (e.g. tension on the labor market). The information is imperfect for agents, and we specify what information is being broadcasted.
- a *Public Sector* that recruits (exogenously) employees, collects payroll taxes on businesses.

## 3.3 Institutional Framework

Moreover, it also includes one *institutional module*. One distinctive feature of the WorkSim model is to integrate a fairly complete and flexible institutional framework that includes (1) the necessary elements of the French labor Law, including **two types of contract**: fixed duration contracts (FDC)4 and open ended contracts (OEC),5 dismissals on personal and on economic grounds, redundancy payments, ... ). and (2) government decisions (minimum wages, welfare benefits, ...). The parameters of the institutional framework are shown in Appendix B.

## 3.4 Key Economical Computations In The Worksim Model

Before detailing the behaviors of the our agents in the model, let us describe some key economic computations in WorkSim.

## 3.4.1 Benefit Of The Firm

Firm Income -
The only production factor is the labor, like in many labor market models.

There is one non-storable good, and each firm produces a certain amount of its own variety of this good. Each firm responds to a quantity demanded of this good Dj,t, defined as its share of the total quantity of the good demanded, share that fluctuates randomly according to a random walk. Total quantity demanded Dtot is held constant because we aim to study our labor market in a steady state. Exogenous shocks on this total demand will be introduced in a sensitivity analysis to study the response of the main variables. In order to illustrate the coherence of a constant total demand with stochastic shocks on firms own demand, we can for instance look at a goods market with horizontal differentiation, where firms undergo stochastic variations of consumers' preferences for their own variety. Price adjustments have a cost, and then firms dare not modify the price. Since the unit costs are not too dissimilar, we can then set a unique exogenous price
(Salop, 1979). Firms that make losses for some time fail. The firm production is linear additive in terms of the productions of the different workers, given that employees work either full time or part time.

A firm is composed of a manager and employees of 3 different occupation levels (1 = blue collar or employee, 2 = middle level job, 3 = executive ).

Each firm has a specific organization and needs labor for each occupation level q :
Dj,q,t = Dj,t × ψj,q with ψj,q the share of demand of the firm j allocated to the occupation level q. At the creation of a firm, these shares are randomly drawn from a standard normal distribution with a mean µΨq, which depends on the occupation level of the job, and a standard deviation σψ.

At each step of our simulation - one week in the reality6, we assume that each occupation q in the firm j cannot contribute more than its demand D*j,q,t* or its production capacity Qeff j,q,t
(computed as the sum of the production of all these nj,q employees). The income of the firm j at time t is given by:

$$R^{eff}_{j,t}=P\times\sum_{q=1}^{3}min(Q^{eff}_{j,q,t},D_{j,q,t})\tag{1}$$
Firm costs -
The regular global cost of the firm is:

$$C_{j,t}^{eff}=\sum_{i=1}^{n_{j}}C_{i,j,t}^{eff}\tag{2}$$
where Ceff i,j,t is the effective salary cost of the employee i in the firm j at time t and nj the total number of employees. There are additional costs Cadd j,t that include training costs, firing costs and vacancy costs.

Benefit -
The profit of the firm at time t is given by:

$$\Phi^{eff}_{j,t}=R^{eff}_{j,t}-C^{eff}_{j,t}-C^{add}_{j,t}\tag{3}$$
This profit is stored in the history of the firm in order to perform a quarterly balance (cf. section 3.6.2).

## 3.4.2 Determination Of Firm Production Qeff J,Q,T

There is a base production attached to each job, and the employee's characteristics will modulate its value to determine the effective production. Moreover, the employer has only an imperfect and evolving information on individual production 7.

Base production per occupation level -
In the firm an employee occupies an individualized job p, notably characterized by a occupation level q, but also by the nature of the job contract, the expected duration of this contract, the work time per period (full-time or part-time job). The weekly base production for a job p at occupation level q in firm j is randomly drawn within bounds from a normal distribution with a mean µq, which depends on the occupation level of the job, and a standard deviation σq. The base production of a worker (for full time) reflects the technology embodied in the equipment used by the workers in the occupation q. The technology is not explicitly modeled and it is assumed to be different between firms but identical for all jobs in the same occupation in a given firm. Moreover there is presently no technical progress in the model so that the base technologies are fixed variables for a firm, and the base production is drawn from a distribution when the firm is created :

$$Q_{jq}^{base}=Max(0,\,(\mu_{q}\times\mathcal{N}\left(1,\sigma_{q}\right)))\times NbHoursPerWeekRatio(contract_{p})\tag{4}$$
where NbHoursPerWeekRatio(*contract*p) is a coefficient equals to 1 if the contract of the job is a full-time job (35 hours per week) and equals to 1
2 if the contract is a part-time job.

Effective production -
The effective production of an individual i at job p in firm j is given by :

$$Q_{i,j,\alpha t}^{eff}=Q_{j,\alpha}^{base}\times Corroid_{i}\times F_{\beta_{i}}(CH_{i,t}^{general}+CH_{i,\alpha t}^{soc})\times F_{\lambda}(CH_{i,j,t}^{spe})\tag{5}$$

The $F_{y}$ functions are given by: $F_{y}(x)=1+y\times x$, and $\beta_{i}$ a positive exogenous parameter.

The effective production is based on four complementary factors : (1) the base production in the job, (2) the core productivity of the employee, (3) the general human capital of the employee, and (4) the specific human capital in the job she holds's.

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

Employee production estimation -One key theoretical options of WorkSim model is that an employee never knows perfectly the production of an employee. This hypothesis is in the line of loanovic (Iovanovic, October 1979), and was the basis of important developments in labor economics. This hypothesis has multiple potential effects on the functioning of the labor market. We assume that the company does not have any _a priori_ knowledge about the precise levels of real productivity for each of its employees. Therefore, it is only able to assess a level of _estimated productivity_:

$$Q_{i,j,d}^{estimated}\sim Max(0,\,\mathcal{N}(Q_{i,j,d+1}^{eff},\sigma_{i,j,d+1}))\tag{7}$$
This amount Qestimated i,j,q,t is drawn from this distribution when the employee is hired, and also at each employee evaluation. σ*i,j,q,t* represents the degree of uncertainty of the company in the evaluation of its employees. It decreases in the seniority of the employee in the firm at her level of occupation (informal learning by the employer) and in the number of times she has been evaluated by the firm (formal learning that takes place on specific occasion such as the end of probationary period, or the end of a FDC if a transformation into an OEC is considered):

$$\sigma_{i,j,q,t}=Max(0,\;\sigma_{0}\times(1-\delta_{\sigma}\times\mbox{\it Seni}or_{i,j,q,t}^{spec}-\eta_{\sigma}\times\#Eval_{i,j,q,t}))\tag{8}$$
with σ0, δσ and ησ, three exogenous parameters12.

## 3.4.3 Determination Of Firm Costs Ceff I,J,T

Base salary The weekly base salary for a job p at occupation level q in firm j is written Sbase j,q . It is determined from the base production in the job:

$$S^{base}_{j,q}=Q^{base}_{j,q}\times P\times(1-\zeta_{j})\tag{9}$$
9We have made the choice to discard the notion of firm human specific capital by creating instead two new types of human capitals. The first is the occupation human capital, which corresponds to the professional skills acquired in the educational system and subsequent experience acquired in a given occupation level. This type of human capital is obviously important and distinct from work experience since entering the labor market in the model (see Gibbons et al. (Gibbons et al., 2005), Kambourov & Manovskii (Kambourov & Manovskii, 2009) for evidence). In the model it is specific to a broad aggregate of occupations q, but it could be extended to more finely defined professions or crafts.

The second is the job specific human capital. It covers possibly some required training given when entering the job but in any case the experience by learning on the job. It is assumed to be so specific that it will not have any use in other jobs. It notably contains some social skills specific to the job.

with P the exogenous price of the (unique) good and ∀*j, ζ* = ζ, an exogenous parameter that represents the share of the sales revenue (of base production here but also of the sales of effective production below) kept by the firm in order to pay intermediate consumptions, payroll charges, taxes, interests, investments, dividends, etc.. It reflects the balance of power between workers and employers, the size of public services in the society and the technology among the principal determinants. Although it differs in the real world between firms because the expenditures differ between firms, we will assume it is uniform since the model does not focus on the determinants not related to the human resources management.

Weekly starting salary The starting net salary Seff i,j,q,t=*hiring* of an employee i in firm j at level of occupation q at time t = *hiring* is given by:

$$S^{eff}_{i,j,q,t=hiring}=Max(SMIC,\,S^{base}_{j,q}\times F_{\beta_{q}}(CH^{general}_{i,t=hiring}+CH^{occ}_{i,qt-hiring})\times G(U_{t=publish}))\tag{10}$$
SMIC 13 is the minimum hourly wage in France, net of the employee's contribution to social security, multiplied by the number of hours worked on the job. The starting salary is the base salary of the job modulated by the general and occupational human capitals of the employee. Due to important considerations of equity in terms of human resource management (e.g. (Adams, 1963)), the employer cannot discriminate between employees who have the same experience. A feeling of unfairness could generate decreases in effort and productivity for the employees who feel unequally treated (efficiency wage concept)14.

A final factor affecting wages is the global unemployment rate U t=*publish* at the time of publication of the job offer by the firm. We consider that the relation G is isoelastic, according to the literature on the wage curve (Blanchflower & Oswald, 1994), and take G(x) = k × xω, where ω is an exogenous parameter, set at its standard value of -0.1, and k = (
1
Uref )ω. Uref is set as the global unemployment rate for the reference year we study (Uref = 0.092 in 2011).

Annual increase of the weekly wage The weekly salary of employee i in firm j is reviewed annually at her birthday date of her arrival in the company according to the equation:

$$S^{eff}_{i,j,q,t}=Max(SMIC,\,S^{base}_{j,q}\times F_{\beta_{q}}(CH^{general}_{i,t}+CH^{occ}_{i,q,t})\times F_{\lambda_{q}^{*}}(CH^{spec}_{i,j,q,t})\times G(U_{t=publish}))\tag{11}$$
with Fλ∗q(CHspec i,j,q,t), the productivity gains factor related to her experience in the job that affects her salary. It is assumed here that, following the consensual principals of specific human capital theory, the company gives to the worker only a part of the productivity gains related to specific human capital , hence λ∗
q < λq. However, according to the insiders-outsiders theory, the employee's salary is not affected by changes in the state of the labor market after hiring (the factor G(U) remains the same as it was at the time of publishing the vacancy). Some rigidity in search models is necessary to obtain variations in unemployment during the cycle and Pissarides (Pissarides, 2009) has argued that hiring wages are flexible and current contracts rigid, a double hypothesis which fits the wage curve and the insiders-outsiders theory, and that we can implement easily since the wages are individualized 15.

Effective cost of an employee Ceff i,j,q,t The effective cost of an employee Ceff i,j,q,t include her salary Seff i,j,q,t and payroll charges .

$$C^{eff}_{i,j,\mu t}=S^{eff}_{i,j,\mu t}\times(1+PrCharge)\tag{12}$$

_PrCharge_ is the ratio of payroll charges to net salary. It includes both the employee's and the employee's charges.

## 3.5 Simulation Cycle In The Worsim Model

The **simulation cycle** includes four main steps, as shown in Figure 1 below:

1. Firm decisions: contracts and vacancies management, evaluations, job creation / destruction
2. Individual decisions: labor market entrances and exits, job search 3. Firm decisions: applications and promotions management 4. Demography: household dynamics, retirements, aging
The length of one period in the simulation cycle corresponds to *one week* in the real world, in order to take into account the many very short term contracts that are found in the French labor market, 46% of all hires are on FDC that last one week or less in 2010 (Berche et al., 2011). Moreover, when statistics are needed, we took as a reference year 2011, the most recent year for which we could find the complete statistical data and sources.

## 3.6 Firm Decisions

In each period and for each occupation level, each firm has to create new jobs or destroy existing
ones, depending on an exogenous demand. Then, it manages its employees through evaluation,
possibly dismissals, and manages the fixed duration contracts. For each occupation level q, we
define the demand margin Gj,q,t = Dj,q,t − (Qeff
                                              j,q,t + Q∗
                                                      j,q,t), as the difference between:

- the amount of good demanded to the firm D*j,q,t*, which varies stochastically among firms,
and
- the sum of the current total effective production of the firm Q*j,q,t* and the current expected
production of vacant jobs (to be filled) of the firm Q∗
j,q,t

## 3.6.1 Job Creations (Step 1 In Figure 1)

When Gj,q,t *> DTh*, where *DTh* ≥ 0 is a fixed parameter, the firm considers whether to create a new job to be filled. The characteristics of the job to be created are based on two exogenous probabilities (calibrated, see values in Appendix C) :

1. The first sets the choice between creating a FDC and an OEC. This decision is based on
exogenous probabilities identical for all firms. If a FDC is drawn, its duration will be set by another drawing. The durations considered for the FDC are: 1 week, 1, 2, 6, 12 or 24 months.
2. The second one decidess whether the job should be full-time or part time.
Before definitely creating job p of occupation q, the company estimates its expected profit per period from the expected revenue Rexpected q,j,t and costs Cexpected q,j,t
: Φexpected q,j,t
= Rexpected q,j,t
− Cexpected q,j,t
.

The expected revenue from this productivity is given by :

$$R_{q,j,t}^{expected}=P\times min\;(G_{j,q,t},Q_{d,j,q,t}^{dist(m)})\tag{13}$$

with $G_{j,q,t}$ the demand margin and $Q_{d,j,t}^{est(m)}$ is the average of all the productivity estimates for the individuals that will be evaluated during the prospective phase.

The cost per period is a function of the wage but also includes a potential cost of a contract breach. This cost will differ with the nature of the contract (FDC or OFC) :

$$C_{q,j,t}^{expected}=S_{d,j}^{estim}\times(1+PrCharge)+C\,PoS\,Va_{q,t}^{expected}+CE\,End_{q,t}^{expected}\tag{14}$$
where Sestim Avg is the average of all the net wage estimates for the individuals that will be evaluated during the prospecting phase. CPosV acexpected q and CEndexpected q,t are respectively the expected total cost of a vacancy and the expected total end cost of the contract (short-term contract bonus, firing cost,...) amortized over the expected duration of the contract. These costs are estimated by learning. As generally found in search theory, the vacancy cost will impact the hiring norm (though the expected profit, see section 3.6.4 below).

Thus, if its current expected profit Φexpected q,j,t
> 0, the company publishes a job offer at the wage Sbase j,q,t .

## 3.6.2 Job Destruction (Step 2 In Figure 1)

By contrast, when there is a significant reduction in its demand in one occupation level (in our model, this is when Gj,q,t < −DTh), the firm reacts in the short term by removing its vacancies.

In the medium run (on a quarterly basis), if this low cost adjustment is not sufficient, the firm considers the possibility to dismiss workers (see 3.6.3 below).

Moreover, independently of the demand level, the vacancies that remain unfilled and have a vacancy duration greater than a fixed threshold - a parameter that will differ for FDC and OEC - are destroyed.

Short-term adjustment: vacancy removals In each period, when Gj,q,t < −DTh. the company randomly draws one of its vacancies and evaluates the interest to keep it or not. To do this, the company recalculates the demand margin G
′
j,q,t it would have without this vacancy, and reassesses its interest it would have to create the job now. If this time Φexpected q,j,t
< 0, the company removes the vacancy and G*j,q,t* is increased by Qexpected j,q,t
. This process is repeated for all the remaining vacancies as long as overproduction remains (i.e. as long as Gj,q,t < −DTh and there are still vacancies to be removed).

Medium-term adjustments: economic dismissals An evaluation of the financial viability of the company is performed on a quarterly basis (12 periods in the simulation). The first date of the balance sheet is drawn randomly, then this financial reporting occurs every three months from this date. The company calculates its quarterly return that is computed as the ratio of the quarterly profit over the total labor cost16. If this return falls below a certain profitability threshold
(a fixed parameter PT, that will be calibrated and can be negative), the firm engages an economic dismissal procedure:

- All remaining vacancies are removed. - The company dismisses a number of employees, drawn randomly. The company cannot
set the ranking according to the estimation of the profit of the individual employees, even though it has some estimate, since the French labor law and collective agreements set several criteria of ranking that must be respected first. Moreover, the criteria differ between collective agreements, and we considered this ranking process to be too complex to be modeled. The number of employees dismissed is chosen as the minimum number of persons to fire in order to get a return above the profitability threshold.
If a company has no employee anymore, and if the managing director left alone does not make a sufficient return, the firm is considered to be bankrupt and is removed from the simulation. The managing director becomes unemployed. However, we want to keep the number of firms constant since we aim for a steady state. Hence, when a bankruptcy has occurred, we randomly select an active agent in the simulation to create a new firm and manage it. To keep the number of contracts types low, we assume that she will work under an OEC contract and be the only producer in the firm (until she starts to recruit).

## 3.6.3 Employee Evaluations (Step 3 In Figure 1)

In each period, the firm examines if some employees have to be evaluated. This individual evaluation may occur:

- At the end of the probationary period for FDC and OEC ; - At the end of FDC contract to decide if it should be renewed ; - At the end of FDC contract, if the transformation of FDC to OEC is to be considered ;
- Every year, at the anniversary date of the contract, for each FDC or OEC employee.
In order to decide whether the employee should be kept, the firm calculates a profit for each scenario:

- First scenario: the firm keeps the employee. The company computes the demand margin it
gets without this employee, and evaluates as in section 3.6.1 the interest it would now have to create this job. Thanks to learning, the firm knows better this time the employee's actual productivity.
- Second scenario: the firm does not keep the employee (dismissal on personal ground):
1. If the employee is under OEC, the firm evaluates the dismissal costs (specific to a dismissal on personal ground) ;
2. The company computes the potential profit given by a new employee, who would be
recruited to replace the fired employee (with the same contract and the same level of occupation).
The firm compares the total profits associated with each scenario. If the firm chooses to dismiss the employee (end of probationary period, end of FDC contract, OEC firing on personal ground), it publishes a new job add to recruit a new employee at the same level of occupation.

## 3.6.4 Hiring Phase And Promotions (Step 7-8 In Figure 1)

If workers are distributed according to productivity, search theory shows that the firm should set an optimal reservation productivity or profit, under which it rejects the candidates. This reservation profit is based on the probability to attract candidates, the distribution of the discounted values of the productivities of these candidates over the expected duration of the job, and the cost of the vacancy per period, but this list is not exhaustive. A firm will prefer to wait one more period than recruiting if all current candidates are below this reservation productivity. The determination of the optimal reservation profit is symmetric to the worker's search recursive model under fixed wages. 17 Since rationality is bounded, and the productivity distribution unknown, we define a hiring norm that replicates the main results from search theory. The hiring norm of the firm is given by:

$$\text{HirringNorm}_{j,q,p,t}=\text{N}_{1}\Phi_{j,q,t}^{Avg}(1+\text{N}_{2}\frac{\Phi_{j,q,t}^{Max}}{\Phi_{j,q,t}^{Min}})\frac{N(d_{p})}{H(ITENS_{t})}\tag{15}$$
with N1, N2 two exogenous parameters. The firm is assumed to know a small sample of candidates without cost (by its former presence on the labor market), but not large enough to estimate the parameters of the productivity distribution, a demanding and complex process. It calculates the expected profits, and for the positive ones, the company stores the average ΦAvg j,q,t , the maximum of these profits, ΦMax j,q,t and the minimum ΦMin j,q,t . A first result of search theory is that firms prefer distributions with a higher profit mean and ΦAvg j,q,t raises their hiring norm. A second result of search theory is that firms prefer more variance in the distribution since there are more high productivity workers. An increase in the mean preserving variance raises the hiring norm (Pissarides, 1990, p.97). We formalize this result by a bounded rationality rule in which the relative range of the productivities N2 ΦMax
ΦMin raises the hiring norm. A third result is that the norm is an increasing function of the duration of the contract dp proposed for the job through the factor N(dp):
it has a minimum of N3 for a very short FDC (duration of one week) and a maximum at 100% for an OEC contract. A fourth result is that firms lower their norm when there are few unemployed and many vacancies. *ITENS*t is the tension on the labor market and is given by ITENSt = Vt Ut with Vt the vacancy rate and Ut the unemployment rate at time t. The higher this tension, the more the firms have to lower their requirements if they want to find a candidate. H is a logistic function with values between 0.8 and 1.2 and given by H(x) = 0.8 +
0.4
1+20×e−3x .

This hiring norm is then decreased by a percentage N4 in each period until the job is filled, but never drops below 0. This decrease is justified by the limited duration of a job that lowers the expected profit as time to fill this job increases (Pissarides, 1976, p.50). A rising cost from holding the job vacant would have the same effect.

Hiring takes place in three steps:

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

## 3.7 Individual Decisions (Step 4-6 In Figure 1)

The individuals take decisions in each period of the simulation. This decision process is modelled with a *state machine*, where one individual will be in one particular state: inactive, unemployed, employed and not searching for another job (denoted *ENS*), employed and seeking a new job (denoted *OTJS*, for On-The-Job Searchers), student or retired. The transitions between these states can be caused by individual choices (for example: to start studying, to quit a job...), by external events (firing, death...), or by a sequence of two decisions (applying for a job, and the firm hires the candidate).

## 3.7.1 Utility Functions

Each individual uses a utility function, to decide whether she should stay in her current state or move to another one. The utility function has the generic form of a Cobb-Douglas function:

$$U=(Income+Amentity+Stability)^{1-\alpha}(Free\,Time)^{\alpha}\tag{16}$$
It is a weighted aggregation of two groups of factor, the income including the value of the characteristics of the job, and free time. The detailed factors are:

1. *Income*: weekly income of the household in euros, divided by the number of consumption
units (an adult counts for 1, a child 0.5)
2. *Amenity*: non-monetary features perceived by the individual (social recognition, working
environment, work hardness...)19. It is converted into a percentage of salary and is expressed in euros.
3. *Stability*: criteria reflecting the preference of the individual for stability, i.e. for a job with
the longest possible remaining contract duration. The maximum value is given for a permanent job (OEC). This stability is converted here into a percentage of salary and is expressed in euros;
4. *Free time*: free time per week available for the individual outside her working hours and
her search time. Our definition is a broad one since it includes time devoted for instance to sleep, eating, washing, domestic duties, and notably caring for the children.
The parameter α ∈ [0, 1] encodes the preference of the individual for free time or work. First, there is an effect of age, which increases the disutility of time spent at work. Hence α will evolve according to the following equation :

$$\alpha=\alpha_{base}*(1+\alpha_{old}*(age-15))\tag{17}$$

With $\alpha_{base}$ drawn at the creation of the agent according to a normal distribution with mean $\alpha_{0}$ and standard deviation $\sigma_{all\alpha}$ (and with a minimum of zero).

Moreover. as in the ARTEMIS model (Ballot, 2002), α is different between men and women with children, because gender roles in the household has some impact20. We model this difference by multiplying the woman's alpha by a factor Fw depending on the number of children in
19The amenity is a proxy for all the factors that make the work pleasant or painful. We consider the work time per period when we calculate this amenity to avoid a bias, and above all, the amenity is fully revealed to the employee only after hiring. This amenity discovery could cause some early quitting, as it is happening in reality. Thus, in terms of imperfect information, there is a symmetric process between amenity discovery for the employee and employee's productivity discovery for the employer. The main difference is that we assume the employee to be promptly informed of the amenity, while the productivity is measured only very gradually (the probationary period is too short to reveal the real productivity).

20In fact, and even if societies are constantly evolving on that issue. French women in 2011 have devoted more time than men to housework and the education of children. According to INSEE's enquiry on time use (2010), on average (including persons withot children), women devote 45mn daily to care for children, while men spend only 19 mn on such an activity. Indeed, in 2011, the employment rate of French women working full-time and living in a couple with three children or more was 39.8% against 87% for men in the same situation (INSEE, 2011b)
the household : Fw = 1+α*child*1∗(1+#children)α*child*2. For women under 25 and having children, this alpha is further multiplied by a factor (1 + α*youngWomen*).

## 3.7.2 Overview Of The Decision-Making Process

The decision-making process of individuals is sequential. The transition from one state to another is done by comparing the utility level of the current state with the expected utility level in a new state.21 Each reachable state will be evaluated using the relevant values of income, amenity, stability and free time in the utility function, the difficulty to reach it, and the psychological cost of starting to search (ICHANG). The agent can then decide whether it is better for her to stay in his current state or to move to another one, as we see on Figure 2. In this case, the individual stops her decision process and changes state, as prescribed by Simon's satisficing heuristics (Simon, 1956).

Every month, an individual in the inactive or *the employed* state receives information about NPros new jobs p prospected. This list of known jobs is obtained by randomly drawing a list of jobs among all job vacancies of JobAds that match the current occupation of the individual. On the basis of these informations she receives on these jobs, she evaluates *UTNEW*, which represents the interest to start looking for another job .

Reservation utility calculation for the unemployed and On-The-Job-search states The reservation utility of the unemployed evolves according to the following equation :

$$UTRES_{i,t}=UTRES_{i,t-1}\times(1-Param3_{UTRES})+Param4_{UTRES}\times(UTEM_{i,t}-UTEM_{i,t-1})\tag{18}$$

If a worker becomes unemployed by putting, or has a job but considers looking for and job, the initial reservation utility of the individual $UTRES_{i,0}$ is computed from the list of all the jobs known during the free search: If an employee becomes unemployed because she is fired, $UTRES_{i,0}$ is initialized at $UTEM_{i,t}$, the utility of the job lost: the individual has no higher requirement. The reservation utility decreases at the rate of $1-Param3_{UTRES}$ with the seniority in unemployment. $Param3_{UTRES}$ is a calibrated parameter. $UTRE_{i,t}$ depends also on the changes in the movie utility $UTEM_{i,t}$ with a sensitivity coefficient $Param4_{UTRES_{i,t}}$, a calibrated parameter. This movie utility reflects the income per unit in the period (unemployment benefit, $S$A$). [20] The free time related by the memory content of each 20 by every week. This means that this myopic utility can rise for fall) and $UTRE_{i,t}$ accordingly.[20]
In the case of an On-the-Job-Search (OTJS) worker, her reservation utility is given by :
UTRESi,t = UTRESi,t−1 × (1 − Param3*UTRES*).

## 3.7.3 Decision Of Student And Public Servant Agent

Given the variety of possible situations, we found difficult to model the behavior of students in this first version of WorkSim. We took a "black box" approach, simply aiming to reproduce the flow of students towards activity on the labor market in 2011.

Furthermore, the public servant agents (21.3% of the agents) do not take decisions and are just present in order to reproduce demographic and employment statistics. When they retire, they are replaced according to a rate 1:1 (to be in a steady state) by young people who are finishing their studies and are randomly drawn in their cohort.

## 3.7.4 Job Search Process

After describing the different decision mechanisms, let us now detail the overall job search process:
ITENSref .

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

## 4 Model Calibration 4.1 Scaling

In order not to exceed our computation power, we limit the total number of agents to 10 000. To do so we first scale down the number of firms to reproduce the distribution of firms by size in France in 2011 (INSEE, 2011a). This gives a reduction factor of 1/4700 and a total of 808 firms.

From this firm distribution we derive the number of employees, 4411 in our case. Then, we add public servants in a proportion of 21.3% (INSEE Source (INSEE, 2013b)), and the numbers of "inactive", "unemployed", "retired" and "student" agents corresponding to 2011 statistics (INSEE, 2011d). We obtain a total of 8713 individual agents and it corresponds to the 40.79 million individuals in the age range 15-64 with a reduction factor of 4 682 (which is well in line with the reduction factor for the firms). Finally, we have then a total of 9521 agents in the simulation.

## 4.2 Minimization Of A Fitness Function

To calibrate the model parameters (37) we minimize a *fitness* function that is the weighted sum of the relative spreads between the outputs of our model and the real targets of the French labor market in 2011 (source INSEE/DARES). We have chosen 49 main targets grouped in 7 different categories:

- 7 targets on unemployment rate by age group and by occupation level (INSEE, 2011c) - 6 targets on activity rate by age group and by gender (INSEE, 2011b)
- 20 targets on wages by age group and by occupation levels, and annual wages distribution
per decile on the global population (INSEE, 2013a)
- 9 targets on labor flows (DARES, Octobre 2012) (the global column values in Table 1 below)
- 9 targets on annual transition rate (Jauneau & Nouel de Buzonniere, 2011)24.
- 3 targets on share of long term unemployment in unemployment by age group (INSEE,
2011d)
- 4 additional targets on part-time job proportion in employment (INSEE, 2011d), vacancy
rate (Conseil d'Orientation pour l'Emploi (COE), 2013), the ratio of employed "looking for a new job" (OTJS) (INSEE, 2008) and the share of FDC in total employment (INSEE, 2011d).

## 4.3 Calibration Method

This fitness function is minimized at a horizon of 200 periods (each period corresponds to one week). To minimize our fitness function, we choose the evolutionary algorithm CMA-ES (Hansen & Ostermeier, 2001), which is one of the most powerful algorithms to solve this kind of problem (Auger & Hansen, 2012). CMA-ES means Covariance Matrix Adaptation Evolution Strategy. The principle of this evolutionary algorithm, inspired by biology, is to test step by step new generations of points in the parameters space. Each new generation of points is drawn stochastically according to the results obtained with the previous generation of points. The mean and the covariance matrix of the distribution of the new randomly drawn points is updated incrementally in order to move towards the best results obtained by previous generations.

Once the fitness function is minimized at the horizon of 200 periods in a steady state, we verify that a steady state is actually reached. This steady state is not devoid of a drift : however, on average, the simulated outputs for the targets have changed by less than 5% after 200 periods.

## 4.4 Results Of The Calibration On The Main Targets

We obtain the results shown in Appendix C for the main targets of our calibration in a steady state
(the different rates are expressed in %), the outputs are averaged over 200 simulations. The values of the calibrated parameters are shown in Appendix D. We obtain an average relative spread between all the outputs of our model and the real targets of 12.9%. The average spread can be deemed satisfactory for such a large non-linear model.

## 4.4.1 Comparison Of Simulated Flows With Dmmo Survey

The DMMO *(D´eclarations mensuelles des Mouvements de Main-d'Oeuvre*) is the only French source that measures several types of gross flows, yet only a small part of all types of gross flows, and therefore does not provide full accounts of labor flows. Yet it is of interest to verify whether other types of flows, which were not in our fitness function, are accurate or not. Therefore, we compare the workforce flows by age group calculated by WorkSim with the same variables calculated by DARES and based on DMMO (DARES, Octobre 2012). These entry and exit rates are ratios between gross entry or exit numbers during the 2011 year over the number of employed persons at the beginning of the year (they are not probabilities to move from a state to another).

We note that most work flows calculated by WorkSim are close to DMMO, or at least the hierarchies of magnitudes by age groups are consistent. (cf. Table 1). Improvements require the introduction of more detailed institutions and behavior, and are left to future developments of the model.

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

## 4.4.2 Comparison Of Simulated Annual Transition Rates With The Employment Survey

We now compare the annual transition rate of individuals calculated by the model with those obtained empirically from the Employment Survey *2007* (Jauneau & Nouel de Buzonniere, 2011), last year for that we have found the annual transition matrix. For 2011 we found only 3 transition rates in (INSEE, 2014). The transitions are based on questionnaires by comparing individual states at a certain date in year n and the same date in year n+1 (with a 12 months distance). A number in a state X in year n+1 comes from state Y in year n. The ratio of (number in X)/ (number in Y) gives the annual transition rate There are two interests in doing this comparison. First most of the empirical flow studies use these data. Second the Employment Survey defines unemployment as we do, according to the ILO norms, implying that only workers without a job and actively searching are labelled as unemployed.

We only aim to obtain a rough fit since the transition rates have been affected by the crisis between 2007 and 2011. The transition rates between the employment and unemployment obtained with our model are quite similar to the 2007 rate obtained from the Employment Survey (cf. Table 2). The lower transition rate of unemployment to employment (36.26%) fits well the 2011 Employment Survey figure (37.6%) and the higher stability into unemployment (56.8%) fits better the new INSEE figure (44% in 2011). Finally the transition from employment to unemployment (2.79%) fits better the the new INSEE figure (2.9%). These evolutions in our simulated data and the real data fit the effect of the 2008 crisis. The transition rates between inactivity and unemployment are however not well matched, but as Jauneau et al. (Jauneau & Nouel de Buzonniere, 2011) show, measuring the inactivity and the flows it entertains with unemployment is a difficult endeavor because of statistical biases in the data.

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

## 4.4.3 Transition Rates And The Underestimation Of Gross Flows

One very important methodological point must be made here. One can notice that these figures capture the transitions between two dates separated by a full year, but do not capture the intermediate transitions that have taken place during the year, unlike those calculated from DMMO rates. A state such as unemployment is transitory for part of the workers concerned since the majority of unemployment spells (60%) last less than a year. Thus, the annual transitions rates considerably underestimate mobility. The following computations illustrate this statement. The DUE (D´eclarations Uniques d'Embauche) is another source than DMMO for the hires (but only covers the hires), and give an exhaustive account of these. It should be however mentioned that the DUE are intentions to hire, and that it is acknowledged that they overestimate hires by 5 to 10%. We have taken from (Berche & Vong, 2012) a figure for 2011 of 20.6 Millions of hires in OEC and FDC, which can be dispatched between 3.4 Millions OEC and 17.2 Millions FDC, and among these 13.1 Millions FDC of less than one month. If we compute the number of hires of unemployed by applying the transition rate of 37.6% in the Employment Survey, to the unemployed in our simulation (2.2 Millions - see our figure 16), we obtain 826 448 hires. The DUE also include hires from employment as many workers change jobs. If we compute quits from the DMMO, we find 1.3 Millions moves that we will assume to be rehired. The hires in DUE without these quits are 19.3 Millions. The annual transition rates in the Employment Survey are then 4% of the DUE. The immense majority of hires on short run contracts are not captured by the annual Employment Survey, and this shows that the underestimation of gross flows is huge.

The Employment Survey has been made continuous since 2003, and transitions over short periods could in principal be computed. However the persons are interviewed once a quarter so that transitions under a quarter cannot be computed (Deroyon et al., 2013). A questionnaire on the preceding month allows to compute monthly transitions, but there is a retrospective memory bias. Morevover, these data have not been published. (Dubois et al., 2011) have treated the transitions between unemployment and employment under the assumption of homogeneity of the workers, and they find that the monthly transition from unemployment to employment is around 11% in 2010 (figure 1 in their paper), which yields a flow of 241,780 moves per month. The DUE yields a monthly figure of 1.6 Million hires in 2011 (as we mentioned overestimating hires by 5% to 10%). The ratio of transitions to the gross flows rises from 4% to 15% only. Our model captures 56% of the hires in the DUE, an underestimation that we have to accept if we want the other flows to fit the DMMO, which underestimate considerably the FDC of less than one month. However we capture the dominance of short FDC well enough since we simulate that 63% of FDC spells last one week, and 21% more than one week and less than one month25.

Another way to look at the underestimation problem is to look at the duration of FDC and unemployment spells. Barlet et al. (2014) measure a median spell for the FDC of 2 weeks in 2012.

These statistics mean that most of FDC could not captured by any enquiry that has a step of one month or more, and hence the flows between FDC and unemployment (and the other way) lead to a huge underestimation of gross flows even if computing monthly transitions. Data on (completed) unemployment spells by duration are not available, but they would certainly confirm that many short spells are underestimated by transitions matrices. In our model, 27% of the spells of unemployment among those completed during the year last at most two weeks and 50% last at most one month26.

## 4.4.4 Unemployment By Age And Occupation Group

The WorkSim model allows to compute detailed data on the characteristics of unemployment by age group and occupation level, shown in Table 3 below. First we note that the average duration of unemployment spells is much lower than the average unemployment seniority. This reflects a composition effect (the most employable of the unemployed individuals find a job quickly) and possibly a *duration dependance effect* (a decrease of the exit rate when unemployment seniority increases). The latter effect is however a controversial issue in the empirical studies (OECD, 2011), and since the evolution of the reservation utility with the unemployment seniority is an important factor of exit intensity in the model, we formalize three effects :

- the seniority of unemployment has a negative effect on the reservation utility, since the
unemployed understands she cannot succeed to obtain the good jobs she has applied to, and this raises the hiring rate
- the decrease in the replacement rate when the unemployment redundancy is replaced by
welfare reinforces this reservation utility decrease, and this has a positive effect on the hiring rate
- finally the decrease in the reservation utility may induce some unemployed to exit to inactivity
All these effects decrease unemployment. However, the seniority of unemployment induces a progressive loss of human capital after six month that decreases the hiring rate and increases unemployment. The net effect of these opposed factors is the existence of a very substantial proportion of long term unemployed. The long-term unemployment is well reproduced as a proportion of total unemployed persons. On average, in our model, 34.5% of the unemployed persons have been unemployed for more than 1 year and 26% for more than 2 years (which is not very far from the 40.5% and 19% rate respectively obtained with the Employment Survey (INSEE, 2011d).

|                                                     | Global        | 15 24 years   | 25 49 years   | 50 64 years   |
|-----------------------------------------------------|---------------|---------------|---------------|---------------|
| Share of long-term unemployed - more than 1 year    | 34.5% (3.4%)* | 26.3% (3.6%)  | 38.5% (2.8%)  | 34.8% (3.4%)  |
| Share of long-term unemployed - more than 2 years   | 26.0% (2.1%)  | 16.0% (2.2%)  | 30.3% (3.1%)  | 27.7% (3.7%)  |
| Average unemployement seniority (in month)          | 13.9 (0.90)   | 10.4 (0.69)   | 15.4 (0.97)   | 14.4 (1.21)   |
| Average duration of unemployment spells (in months) | 2.59 (0.71)   | 3.14 (0.19)   | 2.28 (0.22)   | 2.51 (0.25)   |

*The Figures in brackets are the standard deviations on the results

## 5 Simulation Analyzes And Results

We first undertake a sensitivity analysis on some important parameters in order to explore the model outputs, showing that the results can be interpreted through economic mechanisms that make sense. We then use the model to offer a first characterization of the nature of the French labor market.

## 5.1 Sensitivity Analysis

In order to perform the sensitivity analyzes, we run a set of simulations by changing the value of a given parameter step by step, the others remaining at their calibrated values. For each consecutive point, we measure the outputs of the model after 200 periods (4 years in reality) and average these results over 200 simulations in order to eliminate the stochastic effects. The results enable us to uncover if a parameter has a significant, null, or overwhelming role on the main features of the labor market. We analyze the effects of changing two different types of parameters. First we look at some of those which play a potentially important role in the behavior of the agents, namely the preference for free time, the cost of change to a new state, the speed of the decline of the reservation utility with the seniority of unemployment, and the change in the level of uncertainty of the employer on a newly hired worker. Second we submit the model to two types of aggregate shocks, one on demand, and the other on the parameter which influences the share of the wages in the total value.

## 5.1.1 Preference For Free Time

The parameter α0 represents the basic mean preference for free time in the computation of the free time parameter α (c.f. section 3.7.1 above). The higher α0, the higher is the preference for free time compared to wages and non-monetary job characteristics. An increase in α0 leads to greater valuation of free time that leads to a substantial decrease in activity (cf. Figure 3).

For the unemployment rate, when α raises and is below 0.23, some unemployed stop to search and then the unemployment rate decreases. When α becomes somewhat higher than the calibrated value, the number of unemployed remain constant while the number of active persons decreases, which leads to an increase of the unemployment rate. Therefore the unemployment rate has a U-Shape (non monotonic).

## 5.1.2 Cost Of Change To A New State

Mobility, and its inverse, stability in a state, is one of the crucial features to characterize a given aggregate labor market or the situation of some categories of labor when there is no homogeneity. The individuals will be less mobile when the cost of changing one's state rises. This cost is measured by the *ICHANG* parameter, which reflects psychological and economic transition costs (cf. section 3.7.2). When *ICHANG* is equal to 1, there is no cost of entering the labor market and the activity rate is then higher as shown on Figure 4. When *ICHANG* decreases from its calibrated value 1.2 to become close to 1, we see on Figure 6 that the quit rate increases considerably, because more employed workers are looking for another job and quit their own job. This *individual instability* leads to a high turnover rate on the labor market and increases the unemployment rate (cf. Figure 5).

## 5.1.3 Reservation Utility Decline With Seniority In Unemployment

We now study the effect of the labor supply attitude of workers, and more precisely, in a search framework, one of the main parameters that determines it: the rate at which the workers decrease their reservation utility when their unemployment seniority increases. This rate is Param3UTRES
in our model, the reservation utility reduction parameter in equation 18. We see in Figure 8 that the higher the reservation utility reduction parameter, the lower is the unemployment rate, because the unemployed revise faster their reservation utility in their job search process and then accept a high number of job offers. The same happens for the longterm unemployment rate (more than one year) and the effect is considerably more pronounced. This experiment highlights the *existence of some search unemployment* in the model, Finally the faster reduction of the reservation utility induces some discouragement of unemployed persons, and the activity rate decreases (cf. Figure 7).

## 5.1.4 Uncertainty On Workers'Productivity

The parameter σ0 represents the basic uncertainty of the firm when it evaluates the productions of its employees (equation 8).

This uncertainty reflects the organization of the production and its management. For instance, the tayloristic firm, in which the management decides the production process in minute detail, yields a low uncertainty while more modern organizations, that allow for more autonomy, lead to higher uncertainty. We see that an increase of uncertainty in the firm evaluation leads to higher entry and exit rates (cf. Figure 10). The firm makes more mistakes in its recruitment process and is more likely to fire on personal ground afterwards. We notice in Figure 9 that when uncertainty increases, the long-term unemployment decreases strongly, because the chance to get a job even with a weak core productivity is higher. This leads to a slight decrease of the global unemployment rate (from 10.3% to 9%).

## 5.2 Response To Aggregate Changes

In this section, we aim to study the effects of some macroeconomic exogenous changes. Namely, we first analyze how the share of sales revenue between firms and workers impacts the main aggregates on the labor market, and then the market response to some aggregate demand shocks.

## 5.2.1 Share Of Net Wages In Sales Revenue

The share of the sales revenue kept by the firm ζ determines the share of the workers (1 − ζ), and more precisely the share of the net (real) wages, since the payroll charges are not included in the workers' wages (cf. equation 11). Because ζ is homogeneous over firms, changing ζ corresponds to a change in the balance of power between firms and workers. Results are shown in Figure 11. We observe a U-shape, and opposite effects on unemployment and employment rates, with a minimum unemployment rate of 9% for the calibrated value (cf. Figure 11b). If the share of firms is smaller and decreases (ζ < 0.74), the unemployment increases because firms create fewer jobs. Jobs have indeed less chances to be profitable. Conversely, if the share of firms is higher and increases (ζ > 0.74), the wages proposed to individuals decrease and the jobs become less and less attractive, which results in an increase in the unemployment rate, since participation does not decline much. Two factors explain this mild decline. First, when ζ approaches 1 (i.e.

when the firm share is close to 100%), wages will not drop to 0 since they must remain equal to the minimum legal net wage (1 072 euros per month in France in 2011), as displayed in Figure 12. Second the model does not offer to the individuals the possibility to become self-employed or undertake illegal activities to support themselves. Most of them then keep searching a job.

## 5.2.2 Demand Shocks

Finally, we study a macroeconomic shock on global demand. To do so, we apply a multiplicative factor on the demand and observe the response of the model after 200 periods (4 years in the model).

If the demand shock is negative (aggregate demand factor falling under 1), the unemployment rate increases dramatically, which highlights an unemployment by lack of demand. When the demand factor is greater than 1 (demand increase), the unemployment rate decreases, but it does not decrease to zero, while the vacancy rate becomes very important. As found in real labor markets, there is a persistent unemployment caused by search on both sides, workers and employers. It can be characterized as a frictional unemployment, the level of which however depends also on the institutions of the labor market. This means that such factors (institutional or behavioral) as the firing costs, the level of unemployment benefits and welfare, the preference for free time and the rate of decrease of the reservation utility among others affect it (see Figure 13).

## 5.3 Use Of The Model To Characterize The French Labor Market: Flows And Segmentation

Finally, we study the weekly gross flows diagrams we derive directly from our simulations. Since the unit period is the week, no flow between two states is left unmeasured. Intra week flows are however theoretically possible and not taken into account, because the ILO and Employment Survey definition of unemployment makes it impossible to measure since it is enough to have worked one hour in the week to be considered as being employed during that whole week. The gross flows constitute a stock-flow consistent accounting system that no institution in France or elsewhere can build with the real data since the latter are not complete. The simulation model is thus a unique tool to obtain a complete and consistent description of the French flows, after calibration, and building this consistent accounting is the preliminary step to analysis. On practical grounds, as we have shown, it is less subject to the underestimation of flows that we find in the monthly or annual transition rates calculated from the *Employment Survey*. Thus we are ready to characterize our labor market and we will see how an important aggregate feature emerges: segmentation, and more precisely *dualism*. The model contains an institutional segmentation by the mere fact that at a point of time 90% of the workers are on an OEC job, while the other 10% are on a FDC job. The two types of jobs differ at least by the legal features of the contract and the unknown duration in the first case (but with the protection against a fast termination) and the fixed duration in the second case, duration that has a median value of 2 weeks in France. However a dualism implies more, and namely that some workers are stable in OEC while others move back and forth between unemployment and FDC, for a significant length of time or for most of their professional life.

We present the flow diagrams for all individuals and by age group (15-24, 25-49 and 50-64
years old), translated at the national level scale. Each type of flow is measured in two ways. First the numbers associated with the arrows indicate the number of agents in thousands who move from one state to another during the basic period, a week. The thickness of an arrow in the diagram shows the strength of a flow compared to the other flows. Second the percentage in brackets indicates the proportion of agents of a group who change state. This is computed as the ratio of the gross flow between two states on the number of the agents in the a state of origin. It can be labeled as the probability of transition from a state to another from a period to the next. These probabilities are very low because they are calculated on a weekly basis but exit probabilities from the same state can be compared and the relative probabilities can be interpreted in economic terms.

In the diagram for all individuals (Figure 14), the labor market is characterized by high rates of turnover between the states of "unemployed" and "Employed under FDC". The entry flow in FDC from unemployment is the largest of all flows with 162 00027 persons per week and about five times greater than the flow of direct entry in OEC from unemployment, 31 000 that is the third flow by order of importance28. Exit to unemployment from FDC, is also a major stream amounting to 137 000, the second in size. Exit from OEC to unemployment are much lower and constitutes the fourth flow with 26 000 persons. The conversions of FDC into OEC represent only the fifth flow, 12 600 with 8.4% of the exits from FDC (leaving aside the flows to inactivity and retirement), the other persons going into unemployment. It is an indicator of the stepping stone effect, since FDC offers potentially a chance for workers to obtain an integration in OEC in the same firm. However, this integration is a partial measure of the stepping stone effect as there is also a longer term effect, by which experience acquired in FDC may favor later integration into OEC in an other firm. In our simulation, we find that 22 % of individuals in FDC are working in OEC one year later.

Therefore, a first and important observation is that FDC generate important flows towards unemployment and from unemployment to FDC, but at this stage we cannot say whether this mobility is concentrated or not on a rather small fraction of the agents, and consequently if there is segmentation, or not. There are two extreme stories to interpret the data. A first story is segmentation: some workers alternate precarious FDC, which are generally short as mentioned, and periods of unemployment. The other workers are employed in very stable OEC, even if some of these workers can lose their jobs because they are fired for personal or economic motives. The second story is integration with a delay: it tells that FDC is mainly a stepping stone to obtain an OEC later, but one that might require a significant number of spells in FDC to accumulate experience. In the latter case, the flow from unemployment to FDC should not be overwhelmingly large compared to the flow from unemployment to OEC, and the one from FDC to OEC. In the Figure 14, we see that the move from unemployment to FDC is 3.7 times larger than the sum of the moves from FDC to OEC and from unemployment to OEC. Thus, we infer that a segmentation between workers occurs in the sense that many workers on FDC are moving back and forth between FDC and unemployment (very few chose inactivity, only 2750), while other workers have long spells of employment on OEC (28 months in the model). Some are fired from OEC - the flow amounts to 12 000- and spend some time unemployed to find another OEC.

This is not the end of the story. If there is segmentation, the next issue is whether this segmentation is temporary for individuals or durable over the working life. The frontier between the two is not a precise figure, but an integration of young workers that would go beyond a period of 5 to 8 years after entry or say beyond being 30 years old, could be termed durable. Durable segmentation has very serious effects in terms of well-being on the cycle of life such as the difficulty to rent an accommodation and to obtain a loan to buy an accommodation, and brings the risk of exclusion. A temporary segmentation is an integration in an OEC after a difficult period in FDC and unmployment for those youths who have not obtained an OEC straightaway after their studies 29. In order to give some elements of answer on the durable character of the segmentation for a worker, we need to split the diagram by age groups, as depicted in the following Figures 15 and 16 below.

The flow diagrams appear persistent between the 15-24 and the 25-49 age groups. The flows between unemployment and OEC remain fairly of the same order of magnitude in probabilities to move. The probability to move from unemployment into OEC is 1.47% per week for the 25-49 age group, while it it is 1.04% for the 15-24 age group, indicating that experience matters. The probability from OEC to unemployment is 0.13% for the 25-49 age group while it is 0.09% for the 15-24 age group. It shows that the OEC are not life time jobs and that the 25-49 age group is not immune to contract termination. The conversions of FDC in OEC rate are not very high since they amount to 0.67% per week against 0.8% for the 15-24 age group, nor is the recruitment in OEC, so that precariousness does not disappear.

The market for seniors (Figure 17) is similar to the market for the 25 - 49 age group except for the retirement flow. The flow rates between unemployment and FDC remain similar and substantial, as well as the hiring rate of unemployed into OEC (1.76%), the exit rate from OEC to unemployment (0,15%). The main new flow, which increases the total exit from OEC is the transition to retirement (0.002% per week). Persistence of segmentation seems to occur.

A disaggregated analysis of the workforce by occupation levels will not be detailed here because of the lack of space. Its main conclusion is that the flows between FDC and unemployment are concentrated on blue collar workers and employees without disappearing in the other categories. The observations we made for the age groups point to a durable segmentation for a fraction of the young workers, while another fraction stabilizes into OEC. The Employee/blue collar occupation is specially concerned. Yet a precise assessment would require cohort analysis over the life cycle and a typology of the careers, as well as a comparison with the rare empirical studies that are available and cover only part of the life cycle. While the ABM tool is very fit for this analysis, which we have started to undertake, it will require a full paper to present it properly. The present paper analysis should be considered as a first step in our research program as far as this topic is concerned.

## 6 Conclusion

In the version presented here, the WorkSim model provides a comprehensive theoretical framework of the labor market. Following ARTEMIS, WorkSim is the first to bring together a number of elements, which we consider jointly essential to characterize precisely the nature of a specific labor market, in order to have a tool for employment policies analysis:

1. the **stock-flow accounting** of individuals, based on gross flows, is complete and endogenous. It can be supplemented by a stock-flow accounting of jobs (and even jobs within the company) for further analysis. This is a preliminary step for a thorough analysis of a labor market.
2. the **institutional environment** is modeled and based on labor law, which sets constraints
on the possible decisions.
3. the mobility is modeled through decision-making based on bounded rationality with learning. These decisions are made by the firms **and** the individuals, both heterogeneous. They
are based on a *search theory framework*, which is rooted in the consideration of the cost
of state change (search costs, mobility costs) in a decentralized market, and extended to a general theory of mobility. This theoretical framework provides an intellectual coherence to the many decisions modeled, and the many gross flows simulated. It also appears to have a higher analysis potential for the analysis of competition between categories of workers (for instance) both in the short run and over the life cycle than the matching model that assumes homogeneity. The results, for instance the emergence of segmentation, are however not the results of standard search theory and reflect the role of institutions that impinge at the micro level but have aggregate and possibly unexpected effects coming from the multiple interactions.
WorkSim is calibrated on a large number of targets of the French labor market in 2011, by implementing a powerful algorithm that has not already been used in economic models. It reproduces well enough these targets to conduct some economic analyzes. Moreover, it reproduces often well and sometimes very well the gross flows measured by different statistical sources and with different types of measures. It reproduces well gross flows of labor of the DMMO and many of the annual transitions calculated by the Employment Survey (*Enquˆete Emploi*). These statistics are widely used in analyzes and debates on the French labor market. The DMMO however gives an information on only some of the flows, which precludes a stock-flow accounting. WorkSim, by simultaneously fitting the gross flows of the DMMO and the annual transitions rates of the Employment Survey, uncovers the massive underestimation of mobility if these transitions are considered as a proxy of the gross flow rates. We also show that the monthly transitions measured by the Employment Survey (only for hires) diminish the underestimation of flows only in a marginal way.

This article presents a number of preliminary analyzes to characterize the French labor market, on the basis of complete individuals' stock-flow accounts, micro-decisions of heterogeneous agents, and institutions.We have studied several behavioral changes and aggregate shocks through sensitivity variants of some parameters. We show reactions of unemployment which we are able to explain by detailing the economic mechanisms at work in the model. The results may be sometimes unexpected *ex-ante* because of complex interactions. For example, the mean preference for free time and the share of sales revenue retained by the firms before the payment of salaries have a non-monotonic effect on unemployment. The latter has a slight U-shape.

Our results also suggest a **segmentation or dualism between workers**, since some are stable in OEC because the number of dismissals is low, and some are rotating between FDC and unemployment. This dualism persists between the 15-24 years age group and the 25-49 years age group, and even the 50-65 group, so that the paper suggests it is permanent or at least durable, for a fraction of the workers. A fraction of young people do not seem to switch from FDC to OEC
when they get older, contrary to the assumption of a gradual integration mechanism of young people involved by a temporary dualism.

Naturally, the key factor is the job creation, and the model reproduces well the massive effect of a sharp increase in aggregate demand on the reduction of unemployment. However, the primary objective of a model of the labor market is to study the effects of structural policies at a given aggregate demand level, although *in fine* some structural policies could influence demand and require to model some feedback mechanism.

## Future Work

Our research program is currently focused on a number of modules (extensions) to be integrated. The first aims to model (endogenously) the choice between FDC and OEC openings made by the firms. This is a complex issue that has not been solved to our sense in a formalized framework. This module will integrate the need for a required minimum level in human capital and training in some jobs and uncertainty on future demand that are fundamental elements in the labor market. Secondly, the choice of contracts will be extended to the temporary help contracts which have become empirically important and are presently included in the FDC, in order to bring into the scene the role of an intermediary in a decentralized market. Thirdly we might need a more detailed analysis of retirement to better analyze the seniors' market. A fourth module will focus on the analysis of careers. The characterization of the labor market requires an understanding of careers notably but not only in order to distinguish temporary segmentation and permanent segmentation. Existing empirical analyzes can serve as a benchmark, but are not able to reproduce full careers in a cohort, due to the lack of individual data over such a long period, and are biased by the changes in the economic environment during the lifetime. The multi-agent modeling seems to be an essential tool in this area, and this is a key reason for their construction, if one want to really understand the nature of the labor markets.