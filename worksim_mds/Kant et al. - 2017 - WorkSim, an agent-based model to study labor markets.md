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

## 1 Introduction

WorkSim is a novel agent-based framework to study labor markets. The multi-agent methodology is the perfect tool for such a research program, since it can model institutions precisely, and account for heterogeneity and individual interactions. Simulation results enable us to compute aggregate variables such as the flows and the stocks, and finally the individual careers and the main types of trajectories.

Agents are autonomous and there is then no need for an auctioneer, an unrealistic fiction in orthodox models, and this is has consequences since the labor market is very decentralized. The agents take decisions based on their information and the calculation of costs and benefits, and the profit (for the firms) or utility (for the individuals) they expect. The environment is very complex because of the institutions and the interactions, and changing, and their rationality is bounded in the sense of Simon (1956). Therefore, when in a given state, they choose the best of a few possible solutions (see below for examples). They make mistakes when deciding, but in WorkSim, they can learn and revise their requirements. The institutions and legal rules that constrain the decisions are modeled precisely. The model allows for non-linear relations between aggregate variables, and notably crowding-out effects, often important in labor markets. The computed effects of the present law will bring a resounding example. These models can be calibrated with a varying degree of sophistication, and when the purpose is to study a policy, as in this paper, it is an essential part of the research.

## 1.1 Extending Search Theory

WorkSim is grounded in the concept of *search* (Phelps, 1970). Search Theory studies how economic actors find a partner for their transactions (here a company with a job)5. In WorkSim the basic concept of search is extended in three directions, in order to build a general theory of mobility :

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

1. First, dynamic programming algorithms used to solve the decision problem in analytical search theory cannot be used in a model in which heterogeneous agents move sequentially into many states over time and compete.
2. Second, according to bounded rationality theory, real agents have limited capacities in
terms of computation and memory. They might therefore use simple rules, but a very important behavioral addition in our approach is that they can revise their decisions or even their rules thanks to **learning** and collecting information. This continuous
learning is in fact very coherent with search theory. However, in order to compute equilibrium, analytical models assume perfect rationality and individuals have a lot of information such as the true distribution of wages, and firms the true distribution
of productivities. By contrast, in WorkSim, we model "simple" decision rules - that
comply with bounded rationality, partial information and learning processes.

## 1.2 Related Agent-Based Models

The contributions to the multi-agent literature on labor markets must also be assessed. This literature is thin but has a long history. Bergmann (1974) has developed a simple search model by both sides of the market and obtained simultaneously vacant jobs and unemployment. Eliasson (1977) built a Keynesian and Schumpeterian micro-to-macro model which treats only firms as individual agents but the number of workers in a firm can vary and unemployment is computed. ARTEMIS (Ballot, 1981, 2002) , the ancestor of WorkSim, is the first multi-agent model to have modeled the gross flows between the three main states of the individuals, with the addition of on-the-job search as a state. This was also done within an institutional framework, notably with a temporary help firm, and firing costs. The model generates a temporary segmentation of the young workers. Then, a negative demand shock affects very differently the categories of labor, precluding the progressive integration of young workers in the internal labor markets. This will lead to a permanent segmentation with serious life cycle consequences.

The years 2000 have mainly seen multi-agents models aiming at theoretical research
(see Neugart et al. (2012) for a recent review), such as introducing networks, a logical way to consider search in some contexts (Tassier and Menczer, 2001). Richiardi (2004) modeled the matching process between workers and firms with on-the- job search, entrepreneurial decisions and endogenous wage determination. Neugart (2008) developed an agent-based labor market model with sector-specific skill requirements. Barlet et al. (2009) simulate the French labor market for year 2006. They distinguish individuals and jobs, but not firms as such although there is labor demand side, with creations and destructions of jobs based on a desired margin and demand.

WorkSim goes beyond the existing multi-agent literature on the labor markets in three directions:

1. It is the only ABM labor model to be grounded in a **double stock-flow accounting**,
one for the individuals, one for the jobs, and most of the important flows are considered. This accounting is the equivalent of the financial stock-flow accounting for ACE macroeconomic models, a guarantee of coherence. It also allows for a easy description
of the labor market dynamics at the aggregate and any disaggregation level of interest, and the highlighting of the competition between categories of labor (young, adults, seniors....).

2. It models the **institutions and the labor law** at their level of direct impact (the
microeconomic level), since they are rules of the game that agents know and take into account in their decisions. The diverse forms of labor contracts, with very extreme differences, are probably the major feature of the French labor market, and they are
at the heart of the model, since they modify the flows 8.
3. As stated above,most of the gross flows are generated by bounded rational decisions based on an enlarged search theory, and the effects of shocks we will study then
integrate the agents responses and interactions within the rules of the game and the accounting constraints. Our multi-agent model then provides a tool to explore rigorously the complex system constituted by the labor market.
The paper is organized as follows. In section 2, we describe the main features of the model. In section 3, we present our validation method - through calibration - and in section 4 some simulation results. We will show how WorkSim could be used to assess labor policies, including the recent "Labor Law" that attracted most of the attention recently in France, and generated vivid debates among policians, and economists. Section 5 will conclude and open the discussion.

Note that if the current version WorkSim is primarily designed to account for the French Labor Market (denoted FLM in this paper), most of its components and mechanisms could be re-used to describe labor markets in other countries. In fact, mainly the elements specific to the French institutions (labor law) must be adapted when dealing with another country.

## 2 Model Description 2.1 The Agents In Worksim

There are two types of agents: *Private Firms* and *Individuals*. At its creation, each firm starts with at least one worker to run the company, representing the *managing director* 9
The *Individuals* are grouped in *households* and the simulation evolves in a closed population. The individuals can marry each other, have children, and therefore the decisions of one member of the household may have an impact on the other members. In WorkSim, the agents are heterogeneous. They have specific attributes determined once and for all at their creation (e.g. gender, amenity, ...) and internal variables (e.g. age, salary, number of employees, ...) that evolve all along the simulation.

The agents under 15 or over 65 years belong to these households but are not instantiated as full agents and do not take decisions in the model. However, these non-instantiated agents indirectly participate through the economic decisions of the other members of the household (eg. the number of dependent children is taken into account in decisions of transition to inactivity, the retirement pension is included in household income). The individuals under 15 years become full agents in the model at the age of 15, and some remain in the school system while others enter the labor market.

## 2.2 Environment

In addition to these agents, the model uses three *artifacts* 10:

- *JobAds*, which receives job offers from the firms and job applications from the job
seekers. Dissemination of information, however, is based on the job search process described in more detail below (see sections 2.8 and 2.9), according to the principles of search theory.
- a *Statistical Institute* that calculates statistics from the simulation and disseminates
some information (e.g. tension on the labor market). The information is imperfect for agents, and we specify what information is being broadcasted.
- a *Public Sector* that recruits (exogenously) employees, collects payroll taxes on businesses.

## 2.3 Institutional Framework

Moreover, it also includes one *institutional module*. One distinctive feature of the WorkSim model is to integrate a fairly complete and flexible institutional framework that includes (1) the necessary elements of the French labor Law, including **two types of contract**:
Fixed-Term contracts (FTC11) and open ended contracts (OEC12), dismissals on personal and on economic grounds, redundancy payments, . . . ). and (2) government decisions (minimum wages, welfare benefits, ...).

## 2.4 Individuals

In WorkSim, the individuals i are characterized by the following attributes :

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

- Human capitals (HC) HCgen i,t , HCocc i,q,t, HCspec i,p,t , respectively for the general, related to the occupational level q, and *specific to the firm* and job p *human capitals*14.

The general HC represents the abilities useful for all jobs, like problem solving or knowledge of a foreign language. It increases with experience (one more unit per tick) and also with training. It decreases at each tick i is unemployed by a percentage Lxp after *Txp* ticks (loss of skills). *Lxp* ∈ [0, 0.1] and *Txp* ∈ [0, 100] are two calibrated parameters. The occupational HC is related to the occupational level, and represents abilities specific to this level: machinery or team leading for instance. Like the general HC, it increases with experience (one more unit per tick) and also with training, and decreases at each tick i is unemployed by a percentage *Lxp* after *Txp* ticks. The specific HC is related to the position and the firm. It represents abilities specific to the job in the firm, like a particular process or a software to use. It equals the number of ticks the employee spends in the job. It is reset to zero when s/he leaves the job.

## 2.5 Demand

The only production factor is the labor, like in many labor market models. There is one good, and each firm produces a certain amount of its own variety of this good. The price P is then unique (horizontal differentiation) and fixed at the arbitrary value of 1. Each firm of the N firms in our model responds to a *quantity demanded* of this good Dj,t, which fluctuates randomly due to variations in consumers preferences. However, the global demand Dtot is held constant because we aim to study our economy in a steady state.

At time t = 0, the *market share* of a firm j is given by Dj,t=0/Dtot. We assume that the distribution of this global demand varies between firms. Then we apply a stochastic shock on this market share for each firm at each period (random walk) using a normal law.

## 2.6 Jobs

Each firm has a managing director and a list of jobs per occupation. A job can be in 3 different states : filled, vacant or *pending*. A *pending* job is typically an *FTC* contract that ended, but cannot be renewed immediately, because of the waiting period15.

Each job p of the occupation q is characterized by specific attributes determined once for all at its creation :

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

## 2.7 Simulation Cycle In The Worksim Model

The **simulation cycle** includes four main steps, as shown in Figure 1 below:

1. Firm decisions: contracts and vacancies management, evaluations, job creation / destruction;
2. Individual decisions: labor market entrances and exits, job search; 3. Firm decisions: applications and promotions management; 4. Demography: household dynamics, retirements, aging.
The length of one period in the simulation cycle corresponds to *one week* in the real world, in order to take into account the many very short term contracts that are found in the French labor market, 46% of all hires are on Fixed-Term Contracts that last one week or less in 2010 (ACOSS, 2011).

## 2.8 Firm Decisions

Before describing the job creation process, we describe the demand anticipation mechanism that is the core of these job creation process and the endogenous choice between the different contracts : *FTC* and *OEC*.

Demand anticipation The central idea that governs job creation relies on the way the firm will estimate the future demand. If the demand is going to increase, a new job might be profitable, but not if there is a decrease in the demand.

Hence, the firm will compute three scenarios - pessimistic, *neutral* and *optimistic*, which are depicted in the Figure 2 below. We see in this Figure that in the pessimistic scenario of demand evolution, the demand of the firm is below its production with the new job after a certain time. As the firm cannot sell more good than its demand, it may result in a loss because the firm has to continue to pay a salary. In this example, we see that it may be more profitable for the firm to choose a contract with a shorter expected duration like a 3 months *FTC*. Indeed, the firm will have the option to end this contract after 3 months in case of a negative scenario or to renew it if it goes well. However with a shorter contract it is more difficult to amortize the cost of hiring and training a new employee. It therefore appears a trade-off depending on the level of uncertainty of future demand and how the firm perceives the risks.

Note that, because of bounded rationality, the firms anticipates with a *finite* horizon only. Moreover, the decision process will combine all the three possible scenario into a multi-criteria weighted utility, and the weight of each scenario is automatically calibrated.

Job creations (step 1 in Figure 1)
The job creation proceeds in three steps:

1. First, the firm checks if there is a sufficient demand margin to create a new job.
Here it considers the actual (not anticipated) demand margin DM*j,q,t* for firm j and
occupation level q at time t: if it exceeds the demand margin threshold DT (calibrated
parameter), then the firm moves to the next step. Otherwise, no job is created.
2. If there is in the firm a *pending* job in the occupation q, the firm considers to hire a
new person for this job (taking into account the eventual waiting period). Therefore the pending job becomes a *vacant* job. Otherwise, it moves to the next step.
3. Here, DMj,q,t *> DT* and there are no pending jobs in occupation q. Hence, the firm
considers to create a new job p of the occupation q. The characteristics of this new
job are randomly drawn. From these job features, the firm must decide which type of contract suits better.

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

Moreover, independently of the demand level, the vacancies that remain unfilled and have a vacancy duration greater than a fixed threshold - a parameter that will differ for FTC and *OEC* - are destroyed.

Economic dismissals An evaluation of the financial viability of the company is performed on a yearly basis (52 periods in the simulation). The first date of the balance sheet is drawn randomly, then this financial reporting occurs every year from this date. The company calculates its yearly return that is computed as the ratio of the yearly profit over the total labor cost16. If this return falls below a certain *profitability threshold* (a fixed parameter PT, that will be calibrated), the firm can justify an economic dismissal procedure:

- All remaining vacancies are removed.
- After all the vacancies being removed, if DM*j,q,t* < −DT still holds, the firm consider
to dismiss employees. It selects one employee, computes the associated profit Φtot
i,j,p,q,c,t
and the firing cost *EFC*. If Φtot
i,j,p,q,c,t < −EFC, the firm dismiss the employee. This
process is repeated until DM*j,q,t* > −DT or if all employees have been evaluated.
If a company has no employee anymore, and if the managing director left alone does not make a sufficient return, the firm is considered to be bankrupt and is removed from the simulation. The managing director becomes unemployed. However, we want to keep the number of firms constant17. Hence, when a bankruptcy has occurred, we randomly select an active agent in the simulation to create a new firm and manage it. S/he will be the only producer in the firm (until s/he starts to recruit). Employee evaluations (step 3 in Figure 1) In each period, the firm examines if some employees have to be evaluated. This individual evaluation may occur:

1. At the end of the probationary period for *FTC* and *OEC* ;
2. Every year, at the anniversary date of the contract, for *OEC* employee. 3. At the end of *FTC* contract to decide if it should be renewed ;
4. At the end of *FTC* contract, if the transformation of FTC to *OEC* is to be considered.
Dismissal for personal reasons The process takes in two steps :

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

This *hiring norm* is the profitability threshold below which it prefers to refuse a candidate.

To do so, it uses the *positive* expected profits Φavg j,p,q,c,t calculated for each of the NPros candidates during the prospecting phase and compute the average ΦMoy, the minimum
ΦMin and the maximum ΦMax values.

The hiring norm of the firm is given by:

$$HNorm_{j,p,q,t=crea}=(\phi_{Moy}^{per}+N_{1}\times(\phi_{Max}^{per}-\phi_{Min}^{per}))\frac{N(d_{c})}{H(TIGH_{q,t=crea})}\tag{4}$$
- N1 will be calibrated in [0, 1]. The hiring norm increases with φper Max −φper Min, so the firm favors a large dispersion of candidates' qualities in order to increase the probability to get better candidates, as prescribed by search theory.

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

Hiring takes place in three steps:

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

## 2.9 Individual Decisions (Step 4-6 In Figure 1)

The individuals take decisions in each period of the simulation. This decision process is modeled with a *state machine*, where one individual will be in one particular state: inactive, unemployed, employed and not searching for another job, employed and seeking a new job , student or retired. The transitions between these states can be caused by individual choices (for example: to look for a job, to quit a job...), by external events (firing, death...), or eventually by a sequence of multiple decisions (e.g. applying for a job, and the firm hires the candidate).

Utility functions Each individual uses a utility function, to decide whether s/he should stay in her/his current state or move to another one. The utility function has the generic form of a Cobb-Douglas function:

$$U=\left(Income+Amentity+Stability\right)^{1-\alpha}\left(Free\ Time\right)^{\alpha}\tag{5}$$
It is a weighted aggregation of four factors:
1. *Income*: weekly income of the household in euros, divided by the number of consumption units (an adult counts for 1, a child 0.5)
2. *Amenity*: non-monetary features perceived by the individual (social recognition, working environment, job hardness...), cf. section 2.6 above.
3. *Stability*: criteria reflecting the preference of the individual for stability, i.e. for a job
with the long contract duration. The maximum value is given for a permanent job (OEC). This stability is converted here into a percentage of salary and is expressed in euros;
4. *Free time*: free time per week available for the individual outside her/his working
hours and search time. Our definition is a broad one since it includes time devoted for instance to sleep, eating, washing, domestic duties, and notably caring for the children.
The parameter αi,t ∈ [0, 1] encodes the preference of the individual for free time or work.

Overview of the individual decisions The decision-making process of individuals is sequential and summed up in the state transition diagram depicted in Figure 3. At each tick, the individual agent computes the utility of its current state and the utilities of each reachable state. Each utility is evaluated using the generic form given by equation 5 above, and instantiated with the relevant values of income, amenity, stability and free time. For some transitions, a factor *ICHANG* ∈ [1, 2] is applied that represent the psychological cost facing change (calibrated parameter). When *ICHANG >* 1, the new state's utility must be even greater to win the decision.

Job search process After describing the different decision mechanisms, let me now detail the overall job search process:

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

The first term of the equation accounts for the diminution with time and the second is driven by a modification of *UTUEM*, that is the utility for the unemployed (for instance a decrease of revenue will lower *UTUEM* and therefore *UTRES*, as the urge to find the job increases).

## 3 Validation Process 3.1 Methodology

The WorkSim methodology uses a validation process at 2 levels :

1. *model building* : the way we design the model, and especially the agents' decision rules is
rooted as much as possible in empirical data and facts. Following the psychomimetism methodology Kant (1999), we ensure that these decision processes do not violate the cognitive principles we build our model from (e.g. bounded rationality).
2. *data reproduction*. We want our simulation to account for most of available data on the
labor market we aim to study. To do so, we use an automatic procedure to calibrate the model parameters for which we don't have an empirical value (see below).

## 3.2 Calibration

Scaling First of all, we must set the number of agents in the simulation. It must be large enough to account sufficiently for real behaviors, but not exceed our computational power20. For the first set of experiments (sections 4.1 and 4.2), we used a reduction factor around 5400 and obtained 7484 individuals and 797 firm agents, for a total of 8281 agents in the simulation. The simulation of the "Labor Law" required 20 000 agents to ensure we have sufficient large firms (see section 4.3 below). Calibration procedure To calibrate the 60 model parameters, we have to minimize a fitness function that is the weighted sum of the relative spreads between the outputs of our model and the real targets of the French labor market in 2011 (source: INSEE/DARES). We have chosen 63 targets grouped in 10 different categories : unemployment rates (7 targets), activity rates (6), salaries (14), job flows (12), FTC (4), long-term unemployment (3), mobility (between occupations; 12), additional (part-time, vacancies, on-the-job,training costs). In most cases, we have a target per occupation or age range.

To minimize this fitness function, we apply the evolutionary algorithm CMA-ES (Hansen and Ostermeier, 2001), which is one of the most powerful algorithms to solve this kind of problem (Auger and Hansen, 2012). CMA-ES means Covariance Matrix Adaptation Evolution Strategy. The principle of this evolutionary algorithm is to test step by step new generations of points in the parameters space. Each new generation of points is drawn stochastically according to the results obtained with the previous generation of points. The mean and the covariance matrix of the distribution of the new randomly drawn points are updated incrementally in order to move towards the best results obtained by previous generations.

At each *iteration*, the CMA-ES algorithm sets the values of all the 60 parameters.

Then, to cope with the stochasticity we have in the model, 48 simulations are run (they are usually called *replications* in a calibration process) with a different seed for the random generator, and the outputs are averaged over these 48 simulations to obtain the fitness value of the iteration. We stop the calibration when the fitness does not improve (same minimum value) for 500 iterations. Computational power needs The calibration process is very costly in terms of computational resources, because the total number of simulations could be very high : it is given by the product of the number of iterations by the number of replications. With Work- Sim, it took 2000 iterations to converge, and as stated above each iteration is made of 48 replications. Each simulation takes about 1-2 minutes overall and the whole calibration process will take a couple of days to be completed. Results of the calibration on the main targets We obtain an average relative spread between all the outputs of our model and the real targets of 7.9 %. This can be deemed satisfactory for such a large non-linear model. We deal with a multi-objective optimization problem with many targets and parameters, and these problems are known to be hard to solve.

## 4 Simulation Analyses And Results

In this section, we summarize the main results from a first set of prior simulations we conducted with WorkSim. In this set, the model was calibrated to account French data in 2011. And then we present results on the most recent labor law reform in France. Note that each simulation result is averaged over 196 simulations.

## 4.1 Characterizing The French Labor Market

The model generates some important specific characteristics of the French Labor Market such as the very important share of FTCs in terms of flows, 81 % and the contrasting fairly low figure of the share of the workers employed in such contracts: only 9 %. The unemployment of the young is also much higher than the unemployment of the older workers. This confirms the dualism in the French Labor Market, which is displayed by the differences in the patterns of gross flows of the categories of workers. The model computes all the simulated flows, but allows for comparison with those which can be measured by the published statistics, and the results fit roughly. Most workers are stable in their OECs, while a minority undergoes short spells of employment in FTCs and spells of unemployment between them. Moreover this dualism persists for part of the young workers when they age while the others obtain more stable OEC. More novel results are obtained but will not be detailed here, since they are not the core of this paper.

## 4.2 Assessment Of Some Labor Public Policies

We conducted several simulation of labor policies, and most of them were new (never implemented). In fact, one of the major purpose of WorkSim is to aid politic decision on employment and labor, by simulating and understanding the effects of one particular policy. Removal of Fixed-Term contracts Because of the strong segmentation in the French Labor market, with a lot of flows between FTC and unemployment and few to enter into a more stable OEC, one might want to permanently remove the FTC and have only OEC contracts. We experimented this removal in WorkSim, where only OEC and few customary FTC contracts remained. We measured the impact after 2 and 4 years. Two years after the removal, there is a significant rise of the unemployment rate (+1.1), especially among young people and employees or workers. After 4 ans, the unemployment rate decreases, and equals the baseline simulation (with FTC), because part of the individuals get hired on a OEC. But the unemployment rate decreases also because of the discouragement of 390 000 that leave the labor market (the activity rate drops by 1 point). More over, the long-term unemployment strongly increases (29 points after 2 ans, and still 24 points more after 4 years). Thus, not only the abolition of FTC failed to reduce the segmentation but it actually increased it21. FTC and OEC are not substitutable but complementary on employment.

Reduction of charges The level of social charges on employment are frequently discussed, especially by employers' syndicates. In fact, in 2003, the minister F. Fillon has passed a law that reduces the charges paid by the firms on employment, for salaries lower than 1.6 times the minimum wage (SMIC). The decrease will be 26 % for firms with 20 employees or more, and 28.1 % for the others. To study the effect of this measure, we compared the results of the baseline simulation22 with a new simulation where these charge reductions are removed. We measured a drop of 0.72 points in unemployment rate, and a gain of 233 000 more jobs, thanks to the charges reduction. The firms also increase their benefits.

However, it might be more efficient to target the policy on lower wages. Therefore, we vary the maximum wage to receive to policy, from 1.2 SMIC to 2.2 SMIC. The results are displayed in the Table 1 below. It appeared that the 1.2 SMIC target gives the most effective policy: smallest unemployment rate (9.55%), 298 000 more jobs, 253 000 less unemployed and also the lowest costs.

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

Firing costs and legal justification Another option to reduce unemployment would be to ease the creation of OEC (instead of FTC). Many firm leaders and employers' syndicate complain about the level of firing costs on one hand, and about the difficulty to fire an employee when the demand becomes insufficient, on the other hand. Therefore we conducted experiments to study these issues.

In a first experiment, we vary the level of firing costs, and multiply them by a factor between 0 and 50. Surprisingly, we found a very small effect on unemployment. The unemployment rate increases only by 1 point when we multiply the firing costs by 50. When the cost increases, the firms replace OEC hirings by FTC hirings. Moreover, when the cost is null, the unemployment remains around 9.5%, because hiring in OEC remain low.

So, maybe this is not about the cost of firing, but about the difficulty to fire someone, when the demand is low. Therefore, we conducted a second experiment, where we remove the legal justification attached to firings. When it is the economic interest for the firm to fire an employee, it does so. Moreover, this possibility is integrated into the anticipation mechanism that is part of the decision process to create an OEC job. The results are shown in Table 2, after 2 years following the variant. With this variant, unemployment rate drops by 1.62 points, and the decrease is particularly important for the youth, with a drop of 10.67 points. However, we observe an increase of 1.64 for the seniors. When we look at the unemployment rate per occupation, we find the variant to be quite beneficial for the blue collars/employees category (-3.26 points) at the detriment of the two other occupations (+0.75 for middle levels and +1.64 for executives). This could partly due to the fact that the firms mainly use OEC to hire: the entry rate in OEC goes from 11.4 % to 27.24 %; while the entry rate in FTC drops from 45.38 % to 7.22 %. The share of FTCs drops from 8.77 to 1.89 %. As a counterpart, the OEC become more precarious: the economic firing rate increases from 0.58 % to 16.74 % and the average seniority in OEC decreases from 5.86 to 3.55 years, and the probability to loose a job increases by 65 % (from 8 % to 10.33 %). There is a also in individual utilities (well-being) of -1.3 points.

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

To sum up, this policy is not yet the ideal solution to improve employment nor wellbeing: even it is costless and created 523 000 jobs in our simulation, that was at the price of a significant higher precariousness. Moreover, in another simulation, we found that this policy shows less resilience when the demand gets weaker.

Finally we present the most recent simulation we performed to evaluate the very recent labor reform law in France.

## 4.3 Evaluation Of The El Khomri Law

The El Khomri law project has been presented in March 2016 by the French government as the major labor law of the F. Hollande's presidency. This law has recently set the war not only on the French political scene, but also between French economists who do not hesitate to take a categorical position in favor or against it. Its final version was voted on July 21, 2016. There are many articles in the law, and several are impossible to model at this stage. Here we focus on the facilitation of the economic dismissals, as it is likely to have a most important impact on the labor market.

Before the law, the economic dismissals are allowed if the firm faces "serious economic problems" which in our understanding of case law we interpret as losses over a period of year which can lead to the failure of the firm. Judges may have their own interpretation over the minimum level of losses which could lead to failure23.

With the ELK law, article 30 (denoted as "ELK law" in the remaining of this paper)), the conditions to allow economic dismissals are explicitly specified. They will be allowed in case of a decline either in firm's demand or its turnover computed over a certain period, which depends on the firm's size. For firms under 11 employees, the period is 1 quarter, for those between 11 and less than 50 the period is 2 quarters, for firms between 50 and less than 300, the delay is 3 quarters, and for firms with 300 employees or more the delay is 4 quarters.

Effects under a stable aggregate demand At first we simulate24 the ELK law for a steady state of the exogenous aggregate demand. ELK law yields effects which change over time after the introduction of the law. They evolve during the first 3 years to stabilize generally after 4 years. The first can be termed short run effects and the latter long run effects. This comes from the fact that it takes time for the firing conditions to be filled even under the new law. The immense majority of French firms are small or very small and it takes time for such firms to face a cumulated change large enough to be willing to fire at least one employee.

The law is favorable to the young (15-24), both in the short and the long run, with a decline in unemployment of 148,000 after 4 years (drop over 5 points). The impact is not significant for the age class (25-49), after 2 years, there is a small decrease in unemployment (-53,000) and an increase in employment (+71,000). However after 4 years the law has no significant effect on this age class. Finally the seniors (50-65) undergo a substantial rise in unemployment (+101,000), rising from 6.6 to 8%, i.e. 1.4 points, and a decrease in employment (-121,000).

Moreover, the mobility on the labor market is found to change very deeply, and the nature of the labor market is transformed. The share of FTCs in the hires falls from 77% to 30%. The OEC becomes the dominant hiring contract. The proportion of FTCs in ongoing contracts falls from 8% to 2.3%, yet with a decrease of the mean duration (renewal not included) from 3.6 weeks to 1.9 weeks, meaning that the FTCs are now used only when future demand forecasts are bad and no training is required. The economic dismissal rate jumps from 0.6% to 19%, a major change in a labor market characterized by a very low and decreasing economic dismissal rate. As a consequence the OECs become shorter (the median duration of OECs falls from 4.8 to 2 years) and more precarious, as the probability to loose one's job within a year jumps from 8.17 to 13.13 (+4.9 points, + 60 % relative increase).

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

Two major conclusions can be drawn. First a significant substitution of the young to the seniors takes place, although it declines with time. Second the new load of adjustment set on the OECs has the logical effect of making the FTCs an almost useless tool of flexibility for the employers except for very short expected durations. The explanation of the opposed effects over the young versus the other categories is clear. The young were much more often than the others in FTCs (22% against 7.6% for the 25-50 and 4.9% for the seniors) and benefit from their fall. The effect then goes much beyond the higher flexibility of OECs. It raises the integration of the young in (more precarious) OECs, and this shows that the screening and experience enhancing roles of FTCs were not sufficient. This mechanism, the substitution of OECs to FTCs, and its consequence, the substitution of young workers to seniors, has been overlooked or greatly underestimated by non quantitative analysis of the law. Sensitivity of adjustment to aggregate demand We now change exogenously aggregate demand in order to compare the effects on the unemployment rate of the firing conditions before the law and after the law. Figure 4 gives values after 2 years. It shows that the adjustment of the labor force is predicted to be more important after the law. When demand declines under its value in the reference simulation, economic dismissals are more important, the suppression of the hoarded labor is more complete, and unemployment rises more under the law El-Khomri (increase between 4 and 12 points). When demand rises above the reference value, the employers hire more easily on OECs, and unemployment decreases more under ELK law (decrease around 2 points). The responses are not symmetric for large (and unrealistic) changes since if demand is very high, there always remains some search unemployment by workers who take the time to find a job which satisfies their reservation utility.

## 5 Discussion

In this paper, we present the WorkSim framework, a comprehensive model of the labor market. It implements numerous mechanisms that were not integrated together before within a single labor market model: both sides of the market, detailed decision processes under bounded rationality, learning and anticipation, endogenous contract choices, human capitals, endogenous salaries and productivities. The stock-flow accounting of individuals, based on gross flows, is complete and endogenous. It can be supplemented by a stockflow accounting of jobs (and even jobs within the company) for further analysis. The institutional environment is modeled and based on labor law, which sets constraints on the possible decisions.

WorkSim is calibrated on a large number of targets of the French labor market, by using a powerful algorithm which has not already been used in economic models. It reproduces well enough these targets to conduct some economic analyses. Moreover, it reproduces well the gross flows measured by different statistical sources and with different types of measures. This gives us an estimation of the model accuracy, and is part of the model's validation process.

We conducted several analyzes and policy evaluations. These helped us to identify core mechanisms in the French Labor Market : segmentation, importance of firms' pessimism, among others. Labor policies appeared to have contrasting results in terms of employment improvements, utilities, benefits and costs. Future directions The model can be extended in several directions : adding temporary employment agencies, social networks, and training (more detailed) for instance. We can also integrate more organizational elements, including skills and tasks.

Second, WorkSim needs to be plugged into an agent-based macro-economical framework, in order to have consumption, production and financial effects as well25 .

Third, tools to help analyzing and explaining the simulations are still to be developed further : visualization (improving the graphical interface in WorkSim), analyses of the agents ' decisions, automatic classification of agents' trajectories to study individuals' careers (cohort analysis). Another issue is the link with econometrics, to improve the agents' micro-foundation and enhance the validation process.
