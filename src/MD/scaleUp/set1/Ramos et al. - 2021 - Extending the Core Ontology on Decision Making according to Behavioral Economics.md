## Extending the Core Ontology on Decision Making according to Behavioral Economics

Eduardo C. Ramos 1 , Maria Luiza M. Campos 1 , Fernanda Baião 2 , Renata Guizzardi 3

1 Graduate Program in Informatics Universidade Federal do Rio de Janeiro, Rio de Janeiro - RJ - Brazil

Pontifical Catholic University of Rio de Janeiro (PUC-Rio), Rio de Janeiro - RJ -

2 Department of Industrial Engineering Brazil

3 Department of Industrial Engineering and Business Information Systems University of Twente, Enschede - The Netherlands

ramoseduardoc@gmail.com, mluiza@ufrj.br, fbaiao@puc-rio.br, r.guizzardi@utwente.nl

Abstract. Decisions are constantly made and some of them may be extremely critical. However, most decision makers are unaware that their decisions may be  biased.  We  used  Behavioral  Economics  as  a  foundation  to  propose  an ontology that shows how decision makers' preferences are set and the situation in which they occur in an intuitive decision under risk and uncertainty. Our aim is that this ontology be used to improve their decisions by allowing them a better understanding of how they decide. In addition, this ontology can be used as part of a strategy to reduce biases.

## 1. Introduction

Organizations' success depends on their decisions and decision-making processes are key to make good decisions (SIMON, 1997). An important part of human decision making processes is the use of intuition, i.e. not all decisions are taken rationally or based on logical  reasoning.  Intuition  is  supposed  to  help  decision  makers  address  complex problems,  especially  in  risky  and  uncertain  situations  as  in  dynamic  and  turbulent environments and when little information is available (KAHNEMAN, 2011; VAN RIEL &amp; HORVÁRTH, 2014). The Intuitive decision and its biases are studied by behavioral economics (BE) theory (descriptive theory) that is a theory about how decisions are made (KAHNEMAN, 2011) (THALER, 2015) (OVE HANSSON, 2005) (ARNOTT &amp; GAO, 2019). An indication of the successful field's standing is that three Nobel Prizes have been awarded to BE (ARNOTT &amp; GAO, 2019): to Herbert A. Simon in 1978, to Daniel Kahneman in 2002, and to Richard Thaler in 2017.

On the other hand, decisions can be negatively impacted by psychological biases, such as the loss aversion , risk seeking and framing effects. Psychological biases, also known  as  cognitive  biases,  are  systematic  errors  that  recur  predictably  in  particular circumstances, such as decision making under uncertainty. The errors resulting from a biased process prevent us from making sound decisions. Even when we have gathered abundant work experience and knowledge, we are still subject to those biases. Avoiding bias is a challenge, and one of the reasons is that people are incapable of recognizing their own biases. Therefore, to improve decision making, it is important to better understand how these biases occur and how to reduce their negative consequences (KAHNEMAN, 2011).

[FIGURE]

In  this  sense,  a  considerable  number  of  studies  have  been  done  in  strategic decision making (e.g. KAHNEMAN et al., 2011; KAHNEMAN, 2011; BAZERMAN &amp;MOORE, 2013; THALER &amp; GANSER, 2015; CRISTOFARO, 2017; ABATECOLA et  al.,  2018;  TSIPURSKY,  2019).  Psychological  and  behavioral  studies,  for  example, bounded rationality  (SIMON,  1997),  fast-and-frugal  heuristics  (GIGERENZER  et  al., 1999) and cognitive biases (TVERSKY &amp; KAHNEMAN, 1974; KAHNEMAN, 2011) have suggested that there are contexts in which people consistently violate the axioms of utility  theory  based  on  the  maximization  of  utility,  but  Cumulative  Prospect  Theory (CPT) can accommodate most of these violations (LEWANDOWSKI, 2017). CPT can predict and explain the ways in which people actually make decisions and may allow a better understanding of cognitive biases (KAHNEMAN, 2011) (FRENCH et al., 2009).

In  this  paper,  we  present  an  ontological  analysis  of  the  process  of  intuitive decision  making  according  to  CPT,  and  formalize  it  by  means  of  a  well-founded ontology. We build on the Core Ontology on Decision Making (GUIZZARDI et al., 2020) and consider the fourfold pattern of risk attitudes, one of the core achievements of CPT. This pattern models the following four behavior types: risk aversion for gains and risk seeking for losses of medium and high probability ; risk seeking for gains and risk aversion for losses of low probability .  The proposed ontology accounts for these four behavior types, allowing decision makers to understand how their preferences can be biased in comparison with rational decision making, and how such biases may occur.

The remainder of this paper is structured as follows. Section 2 presents Behavioral Economics and the Cumulative Prospect Theory. Section 3 shows the Core Ontology on Decision  Making.  Section  4  presents  our  proposed  ontology,  and  Section  5  points  to Related Work. Finally, Section 6 concludes this work.

## 2. Behavioral Economics

Behavioral Economics is a descriptive theory about how decisions are made. It shows our actual behavior and does not assume that people generally know what is best for them and  make  decisions  consistent  with  it  (THALER  &amp;  GANSER,  2015),  as  the  rational (normative) decision making theories do.

One of the main foundations of BE is the dual process theory of human cognition. It  reflects  a  fundamental  distinction  in  human  thinking  known  as  System  1  (intuitive system)  and  System  2  (rational  system),  from  the  perspective  of  decision  makers. Decision making can be described as a function of both Systems (KAHNEMAN, 2011). System 1 operates involuntarily, automatically, unconsciously, and quickly with little or no effort, and is also emotional, while system 2 operates voluntarily, consciously, and slowly with high effort (KAHNEMAN, 2011; KAHNEMAN &amp; KLEIN, 2009). The latter is logical, based on controlled operations, and allocates attention to the effortful mental activities that demand it, including complex computations. System 2 can follow rules, compare objects on several attributes, and make deliberate choices between alternatives. On the other hand, System 1 does not have these capabilities.   Systems 1 and 2 are both active whenever we are awake and operate in parallel and interactively

[FIGURE]

(KAHNEMAN, 2011; KAHNEMAN and KLEIN, 2009). In this Section, we present Cumulative Prospect Theory, which is the most famous theory of Behavioral Economics.

## 2.1. Cumulative Prospect Theory

CPT  is  a  descriptive  theory  of  decision  making  in  risky  and  uncertain  situations (TVERSKY &amp; KAHNEMAN, 1992). It considers the fact that, in general, people tend to measure uncertainty and risk badly (SHARDA et al., 2014). To understand it, we here compare it to the Expected Utility (EU) theory, which is a rational decision making theory (FRENCH et al., 2009).

Expected Utility (EU) theory assumes that decision makers optimize by choosing the alternative with the highest Expected Utility among all the alternatives (FRENCH et al, 2009). The Expected Utility of an alternative is calculated by multiplying the value of each outcome by the probability of that occurring outcome and, lastly, summing those numbers (PALMER, 2016).

EU is the right way to make decisions while Cumulative Prospect Theory gives a good prediction of the actual choices people make (THALER, 2015). The EU theory and CPT predict differently the decision maker´s choice between Gamble A and Gamble B in the following example. Gamble A represents a sure loss of $1000, and Gamble B, 50% chance of losing $2500 or 50% chance of losing nothing. The EU of Gamble A is -$1000, and the EU for Gamble B is -$1250. According to EU, Gamble A would be selected as the  final  decision  because  s/he  loses  less  (-$1000)  than  selecting  the  other  option  ($1250).  However,  CPT  argues  the  decision  maker  chooses  Gamble  B.  The  key  to understanding this example is that CPT considers the notion of reference point and loss aversion  in  decision  making,  while  EU  does  not.  We  show  this  example  in  detail  in Section 4, but first we explain the main characteristics of Cumulative Prospect Theory.

CPT is based on the aforementioned dual process theory (KAHNEMAN, 2011; KAHNEMAN and KLEIN, 2009). The following three cognitive features, all operating characteristics of System 1 (Intuitive), are the foundation of CPT and are illustrated as the CPT value function in Figure 1: (i) Reference dependence : evaluation is relative to a neutral reference point. Outcomes that are better than the reference point are seen as gains, and are seen as losses when they are below the reference point. A reference point may be the status quo, but it can also be the outcome to which you feel entitled to, or the outcome you expect, or a goal in the future, for instance. In the aforementioned example, the reference point was 'losing nothing' in the Gamble B. So, not achieving the goal is a loss. Receiving a bonus smaller than you expected is also a loss (KAHNEMAN, 2011). The reference point people use to compute gains and losses is their 'beliefs . . . held in the  recent  past  about  outcomes  (KŐSZEGI  and  RABIN  2006,  2007,  2009  apud BARBERIS, 2013)'; (ii) Loss aversion : a loss hurts more than an equivalent gain gives pleasure (THALER, 2015). We tend to avoid losses more strongly than to have gains (KAHNEMAN, 2011), that is why Gamble A is perceived as  a loss. The thought  of accepting the sure large loss is too painful. It has become the most powerful tool in the behavioral economist's arsenal (THALER, 2015); (iii) We feel diminishing sensitivity to  gains  and  losses  (THALER,  2015). We perceive the subjective difference between $1100  and  $1200  as  much  smaller  than  the  difference  between  $100  and  $200 (KAHNEMAN, 2011).

[FIGURE]

Figure 1 shows the psychological value , yield to a decision maker, of gains and losses  from  a  reference  point,  in  the  vertical  axis.  The  monetary  gains  or  losses  of  a decision are represented in the horizontal axis. The choice process of Cumulative Prospect Theory has two phases: framing and valuation. In the framing phase, the decision maker builds a mental representation of the problem, representing the acts, contingencies, and outcomes that are relevant to the decision. Then, in the valuation phase, s/he assesses the value of each prospect and chooses accordingly (TVERSKY &amp; KAHNEMAN, 1992). One of the core achievements of CPT is the fourfold pattern of risk attitudes.

Figure 1. The form of the value function in CPT representing the psychological value of gains and losses - adapted from (KAHNEMAN 2011)

[FIGURE]

## 2.2. The fourfold pattern of risk attitudes

As already seen, according to CPT, 'people attach values to gains and losses rather than to  wealth,  and  the  decision  weights  that  they  assign  to  outcomes  are  different  from probabilities' (KAHNEMAN, 2011, p. 317). This is the basis to explain the distinctive pattern of decision makers' preferences presented in the fourfold pattern (Table 1) of risk attitudes  as: risk  aversion  for  gains and risk  seeking  for  losses  of  medium  and  high probability ; risk seeking for gains and risk aversion for losses of low probability . Decision makers are 'risk seeking' if the gamble is preferred, and 'risk averse' if the sure thing is preferred (KAHNEMAN, 2011).

In the top right cell, the pattern of decision makers' preference is Risk seeking for losses of medium and high probability . When they face very bad options, i.e. when offered a choice between a sure large loss and a gamble for a larger loss of medium and high probability, they hope to avoid the sure loss and become risk seeking. They reject the favorable settlement of losing $9,500 with certainty and choose 95% chance to lose $10,000. This was new and unexpected and is where many unfortunate human situations unfold. Decision makers tend to 'accept a high probability of making things worse in exchange for a small hope of avoiding a large loss' (KAHNEMAN, 2011, p. 319).

In the top left cell, the pattern of decision makers' preference is risk aversion for gains of medium and high probability . When they face very good options, i.e. when offered a choice between a sure large gain and a gamble for a greater gain of medium and high  probability,  they  fear  disappointment  and  become  risk  averse.  They  accept  the unfavorable settlement of getting $9,500 with certainty, instead of 95% chance to get $10,000.

[FIGURE]

In the bottom left cell, the pattern of decision makers' preference is risk seeking for gains of low probability . When they face options like '5% chance to win $10,000' or '$500 with certainty', i.e. when offered a choice between a possible large gain of low probability and a small sure gain, they hope to get the large gain and become risk seeking. They  reject  the  favorable  settlement  of  getting  $500  with  certainty  and  choose  a  5% chance to win $10,000. This effect explains why lotteries are popular.

In  the  bottom  right  cell,  the  pattern  of  decision  makers'  preference  is risk aversion for losses of low probability . When they face options like '5% chance to lose $10,000' or '$500 with certainty', i.e. when offered a choice between a possible large loss of low probability and a small sure loss, they fear the large loss and become risk averse. They accept the unfavorable settlement of 100% chance to lose $500. Here is where insurance is bought because people are risk averse for losses of low probability and prefer paying much more for insurance than expected value.

Table 1. The fourfold pattern of risk attitudes. Adapted from Kahneman (2011).

|                                      | GAINS                                                                                                                                                     | LOSSES                                                                                                                                                      |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HIGH PROBABILITY (Certainty effect)  | '95% chance to win $10,000' or '$9,500 with certainty' Fear of disappointment. RISK AVERSE. Accept unfavorable settlement of 100% chance to obtain $9,500 | '95% chance to lose $10,000' or '$9,500 with certainty' Hope to avoid loss. RISK SEEKING. Reject favorable settlement and choose 95% chance to lose $10,000 |
| LOW PROBABILITY (Possibility effect) | '5% chance to win $10,000' or '$500 with certainty' Hope of large gain. RISK SEEKING. Reject favorable settlement and choose 5% chance to win $10,000     | '5% chance to lose $10,000' or '$500 with certainty' Fear of large loss. RISK AVERSE. Accept unfavorable settlement of 100% chance to lose $500             |

For each of the cells of the fourfold pattern, systematic deviations from expected value are costly in the long run and this rule applies to both risk aversion and risk seeking (KAHNEMAN, 2011). However, most decision makers are unaware that their decisions are  influenced  by  risk  preferences  as  shown  in  the  CPT,  so  they  are  likely  to  decide without realizing how it can bias their choice of action (FRENCH et al., 2009).

The  true  semantics  of  what  is  value  and  how  the  cognitive  biases  sometimes negatively  affect  decision  making  are  sometimes  not  well  understood.  The  semantic notions involving these concepts, and their relations with decision making can be better explored  and  represented,  mainly  by  showing  the  differences  between intuitive and rational decision .

## 3. The Core Ontology on Decision Making

Guizzardi et al. (2020) argue that for providing better support to decision making, it is paramount to understand, first of all, the nature of decisions and of the decision making process. For that, these authors propose the Core Ontology on Decision Making, founded on  the  Unified  Foundational  Ontology  (UFO),  on  the  ontology  of  Value  Proposition

[FIGURE]

(SALES et al. 2017) and on the ontological analysis of Economic Preference (PORELLO &amp; GUIZZARDI 2018)(PORELLO et al. 2020).

According  to  the  ontology  foundations,  an  agent  termed  VALUE  BEHOLDER ascribes  VALUE to VALUE OBJECTS or VALUE EXPERIENCES, the latter being past, present or future experiences of an agent (i.e., kinds of mental simulations, or mental models). Hence, VALUE OBJECT and VALUE EXPERIENCE are two types of VALUE BEARERS.  The  AGENT  makes  VALUE  ASCRIPTIONS  (i.e.,  assesses  a  VALUE BEARER) to assign it with VALUE. So, the AGENT starts simulating possible scenarios, e.g., imagining herself in experiences, in which she interacts with other AGENTS and OBJECTS. This is what Sales et al. ( 2017) call VALUE EXPERIENCE. In this sense, value is goal dependent, context dependent, uncertain, and subjective.

Furthermore,  Guizzardi  et  al.  (2020)  defined  an  AGENT'S  PREFERENCE  by comparing  the  VALUE  that  the  VALUE  BEHOLDER  assigns  to  two  VALUE BEARERS,  following  Porello  and  Guizzardi  (2018)  and  Porello  et  al.  (2020).  The preferred  bearer  is  then  called  the  PREFERRED  VALUE  BEARER,  while  the  other DEPRECATED VALUE BEARER.

PREFERENCE is the truthmaker of the ternary "has preference" relation, the latter connecting a PREFERRED BEARER and the DEPRECATED BEARER (non-preferred bearer).  PREFERENCE  is  a  COMPLEX  MODE,  which  aggregates  two  VALUE ASCRIPTIONS, each one associated to one of the VALUE BEARERS (GUIZZARDI et al.,  2020).  A  VALUE  ASCRIPTION  is  also  a  COMPLEX  MODE  associated  to  a VALUATION event, performed by the AGENT when ascribing value to the VALUE BEARER. Here, VALUE is an emerging quality that inheres in a VALUE ASCRIPTION that takes a magnitude in a given conceptual space (PORELLO and GUIZZARDI 2018) (GUIZZARDI et al., 2020).

Finally, a DECISION is associated with two ACTIONS, one that creates it, i.e., the DELIBERATION, and one that is associated with the decision result, the DECISION RESULTING ACTION. The DECISION RESULTING ACTION brings about a SITUATION termed CONSEQUENCE. By analysing the decision CONSEQUENCE, the  AGENT  develops  other  MENTAL  MOMENTS  (i.e.  BELIEFS,  DESIRES  and INTENTIONS) that will then influence his future DECISIONS. CONSEQUENCE and DECISION  RESULTING  ACTION  help  in  the  cycle  of  assessing  the  result  of  the decision before taking the next one.

## 4. Proposed Ontology

In this paper, we extend the ontology of Guizzardi et al. (2020) by including intuitive decision  making according  to  CPT  and,  consequently,  we  defined  the  concepts  of INTUITION, REFERENCE POINT, COGNITIVE BIAS, LOSS AVERSION, GAIN, LOSS, RISK AVERSE, RISK SEEKING, PSYCHOLOGICAL VALUE ASCRIPTION and PSYCHOLOGICAL VALUE. CPT considers decisions under risk and uncertainty , and so does our proposed ontology.

EU theory (aforementioned on Section 2.1) is based on elementary rules (axioms) of  rationality  (KAHNEMAN,  2011)  and  it  represents value as  final  states  of  wealth

[FIGURE]

(FRENCH et al., 2009). In this sense, value (or use value ) is a composition of benefits (which  emerge  from  goal  satisfaction),  and  sacrifices  (which  emerge  from  goal dissatisfaction) (LANNING &amp; MICHAELS, 1998). This is the value considered in the ontology  of  Guizzardi  et  al.  (2020),  which  allows  one  to  determine  what  are  the alternatives (value bearers) to be chosen from, how they are valued, what are the applied criteria, who can execute the action resulting from the decision, and so on.  In our proposed ontology, we call this value as RATIONAL VALUE to make the difference with PSYCHOLOGICAL VALUE explicit.

According to CPT, people attach values to gains and losses rather than to wealth (KAHNEMAN, 2011). Depending on how a decision maker frames the decision problem (mental representation of the problem), she represents the value of the possible outcomes that may  occur  as gains and losses from a reference point . To  account for PSYCHOLOGICAL VALUE, our ontology reuses the concepts proposed by Guizzardi et al. (2020), but specializes them from VALUE ASCRIPTION to RATIONAL VALUE ASCRIPTION and PSYCHOLOGICAL  VALUE  ASCRIPTION, from VALUE ASCRIPTION COMPONENT to RATIONAL VALUE ASCRIPTION COMPONENT and  PSYCHOLOGICAL  VALUE  ASCRIPTION  COMPONENT,  from  VALUE COMPONENT  to  RATIONAL  VALUE  COMPONENT  and  PSYCHOLOGICAL VALUE COMPONENT.

Suppose that an AGENT A is in a given SITUATION S1 , i.e., her actual state of affairs. Suppose that S1 does not satisfy A's INTENTIONS (GOALS). Thus, A desires a different  SITUATION S2 . Given her  PREFERENCES  and  resources (including capacities)  and  the  context  surrounding S1 (such  as  risk  and  uncertainty,  quantity  of available information, time and pressure to make the decision), A can decide to selfcommit to a particular way of pursuing her GOALS. Agent A does that by deliberately assessing her options (rational decision making) or by using intuition (intuitive decision making) to form a new INTENTION 1  according to the dual process theory explained in Section  2.  In  other  words,  an  INTENTION  can  result  from  an intuitive  or  rational decision making process (KAHNEMAN, 2011).

Figure 2 shows that an AGENT performs a CHOICE between alternatives due to a certain (motivating) INTENTION. Choice is a critical step of decision making in which 'the actual decision and the commitment to follow a certain course of action are made' (SHARDA et al., 2014, p. 85).

The  Choice  is  performed  by  DELIBERATION  and/or  by  performing  an INTUITIVE CHOICE. These sub-classes of Choice are not disjoint.  An  INTUITIVE CHOICE  applies  an  INTUITION  (reasons  intuitively)  which,  in  turn,  creates  a  new INTENTION termed a DECISION (as the result from the decision making process). In other words, a DECISION is an INTENTION created by a DELIBERATION or by an INTUITIVE CHOICE. An INTUITIVE CHOICE can be influenced by COGNITIVE BIASES, such as loss aversion. As an INTENTION, that DECISION can eventually be manifested  by  performing  another  ACTION  termed  a  DECISION  RESULTING ACTION, whose resulting situation is termed a CONSEQUENCE. If that is a successful action, a CONSEQUENCE satisfies the PROPOSITIONAL CONTENT (GOAL) of the original DECISION (GUIZZARDI et al., 2020).

1   Remember that according to the foundation ontology we adopt (i.e. UFO), a GOAL is a propositional content of an INTENTION. And an INTENTION is adopted by an agent having in mind a particularly aimed SITUATION.

[FIGURE]

Figure 2. Deliberation, Intuition and Decision

[FIGURE]

The  next  figure  (Figure  3)  illustrates  how  the  RATIONAL  and  INTUITIVE DECISIONS are made and how the concepts of VALUE and PREFERENCE are related. Consider a SITUATION in which an AGENT must decide between two alternatives A and B. Each alternative is a VALUE BEARER (either a VALUE OBJECT or a VALUE EXPERIENCE).  When  an  AGENT  decides  something,  she  can  decide  rationally  or intuitively (KAHNEMAN, 2011) (KORNYSHOVA and DENECKERE, 2012). During the  decision  making  process,  she  takes  into  consideration  her  own  PREFERENCES regarding two possible VALUE BEARERS.

Let us now consider in more detail what happens when an agent makes a decision. When s/he decides rationally (i.e., performs a DELIBERATION ) or intuitively (e.g., performs an INTUITIVE CHOICE ). DELIBERATION (GUIZZARDI et al., 2020) and INTUITIVE  CHOICE  are  manifestations  of  that  agent's  PREFERENCES  over  two VALUE BEARERS.

Based  on  the dual process theory explained  in  Section  2,  the  VALUE ASCRIPTION 2  can be PSYCHOLOGICAL or RATIONAL. If the AGENT deliberately assesses her/his options, then s/he is using System 2, i.e. s/he is reasoning logically (a DELIBERATION  is  hence  happening).  This  results  in  a  RATIONAL  VALUE ASCRIPTION (RVA). On the other hand, if the AGENT uses her/his intuition to decide, then s/he is using System 1, i.e. intuitive thinking. So, it is a PSYCHOLOGICAL VALUE ASCRIPTION (PVA). Note that Systems 1 and 2 operate in parallel and interactively (KAHNEMAN, 2011; KAHNEMAN &amp; KLEIN, 2009). To account for both systems, we incorporated the notion of a PVA in addition to a RVA, as described in the following paragraphs.

2 According to Kahneman (2011), in an intuitive decision making there is psychological value and in a rational decision making there is a 'value', that we renamed here to 'rational value'.

[FIGURE]

Each  RATIONAL  VALUE  ASCRIPTION  is  composed  of  several  smaller 'comparisons' (or 'judgements'), named RATIONAL VALUE ASCRIPTION (RVA) COMPONENTS, which aggregate an INTENTION and INTRINSIC MOMENTS that are  taken  into  consideration  by  the  AGENT  when  ascribing  VALUE  to  a  VALUE BEARER. Each RVA COMPONENT is in its turn associated to a RATIONAL VALUE COMPONENT, defined as either a BENEFIT or a SACRIFICE.

Each  PSYCHOLOGICAL  VALUE  ASCRIPTION  is  composed  of  several smaller 'comparisons' (or 'judgements'),  named  PSYCHOLOGICAL  VALUE ASCRIPTION (PVA) COMPONENTS,  which aggregate an INTENTION and INTRINSIC MOMENTS that are taken into consideration by the AGENT when ascribing VALUE to a VALUE BEARER. Each PVA COMPONENT is in its turn associated to a PSYCHOLOGICAL  VALUE  COMPONENT,  defined  as  either  a  GAIN  or  a  LOSS according  to  a  REFERENCE  POINT,  which  is  ontologically  a  BELIEF.  A  reference point is highly determined by the objective status quo, but is also affected by social and expectations comparisons. When an employee receives a smaller raise than everyone else in  the  office,  s/he  experiences  this  objective  improvement  as  a  loss.  Moreover,  the PSYCHOLOGICAL  VALUE  COMPONENTS  are  influenced  by  the  COGNITIVE BIASES, such as LOSS AVERSION, that is the DESIRE to avoid losses. For example, in many decisions, decision makers must choose between retaining the status quo and accepting an alternative to it. Because losses loom larger than gains, they tend to be biased in  favor  of  keeping  the  status  quo,  considering  the  status  quo  as  the  reference  point (KAHNEMAN, 2011).

It  is  important  to  note  that  when  instantiating  this  ontology  for  a  particular decision making case, we may not be able to account for all involved PSYCHOLOGICAL VALUE ASCRIPTION COMPONENTS because PVA is done by the intuitive thinking, which  is  unconscious  and  holistic.  On  the  other  hand,  all  the  RATIONAL  VALUE ASCRIPTION COMPONENTS should always be represented, because RVA is done by logical reasoning, which is conscious.

As seen before, the core premise of conventional economic theory is that people choose  by  optimizing  (THALER,  2015).  Hence,  considering  a  RATIONAL  VALUE ASCRIPTION, a VALUE BEARER is preferred in a has preference relation if and only if the value magnitude of its RATIONAL VALUE ASCRIPTION bearer is greater than the  one  of  the  compared  alternatives  (GUIZZARDI  et  al.,  2020).  However,  the PSYCHOLOGICAL VALUE ASCRIPTION works differently. As shown by CPT, a VALUE BEARER that is preferred in a RVA may be the deprecated in a PVA because the PSYCHOLOGICAL VALUE is represented as gains and losses from a reference point rather than as final states of wealth, as assumed by EU theory (FRENCH et al, 2009). This will set the PREFERENCE mode for most of the decision makers as RISK SEEKING  PREFERENCE  or  RISK  AVERSE  PREFERENCE.  They  tend  to  be  risk averse for gains and risk seeking for losses of medium and high probability; risk seeking for gains and risk aversion for losses of low probability (KAHNEMAN, 2011).

To facilitate the understanding of the concepts and as a preliminary evaluation of the proposed ontology, Figure 4 illustrates a possible instantiation of a situation.

Suppose  the  example  in  which  someone  named  Fred  needs  to  make  a  choice between Gamble A (a sure loss of $1000) and Gamble B (50% chance of losing $2500 and 50% chance of losing nothing). The Expected Utility (EU) of Gamble A is -$1000, and the EU for Gamble B is -$1250. The EU is calculated by the probability multiplied with the expected win/loss. The EU theory says that people tend to choose Gamble A, because it has the highest Expected Utility. However, CPT shows that most people select Gamble B, despite having the lower Expected  Utility.  We explain  how it  happens  as follows.

[FIGURE]

Figure 3. Deliberation, Intuition, Value and Preference

[FIGURE]

Fred  starts  evaluating  these  two  alternatives,  thus  ascribing  value  (VALUE ASCRIPTION) to each alternative. The VALUE ASCRIPTION can be PSYCHOLOGICAL  (PSYCHOLOGICAL  VALUE  ASCRIPTION)  or  RATIONAL (RATIONAL VALUE ASCRIPTION). Each VALUE ASCRIPTION may be composed by one or more components. In this example, we only consider one component (Cost).

For instance, illustrating rational decision, Fred may rationally value Gamble A as -$1000 while Gamble B is valued as -$1250, according to the EU theory (RATIONAL VALUE ASCRIPTION). There are BENEFITS and SACRIFICES inhering in each of these RATIONAL VALUE ASCRIPTION COMPONENTS, for instance, Gamble B is a SACRIFICE and Gamble A is a lower sacrifice that we represent here as a BENEFIT just to simplify the understanding. So, Fred chooses Gamble A, the PREFERRED BEARER, while Gamble B is the DEPRECATED ONE.

On the other hand, Fred may intuitively value Gamble A as a LOSS and Gamble B as a GAIN, according to CPT (see Figure 4). These PSYCHOLOGICAL VALUES are represented as gains and losses from a REFERENCE POINT that set the PREFERENCE mode  for  RISK  SEEKING  PREFERENCE  because  the  alternatives  were losses  of medium and high probability . In this context, as stated by CPT, decision makers hope to avoid the sure loss and become risk seeking by choosing the riskier alternative with high chance to lose even more. The thought of accepting the large sure loss (Gamble A) is too painful for Fred. This is the effect of loss aversion. He has the desire to avoid the large sure loss and he believes the outcome of Gamble B will be losing nothing. His reference point is to lose nothing.

[FIGURE]

Figure 4. Instantiation of the PVA and its related concepts, illustrating how an intuitive decision is taken

[FIGURE]

Figure 4 shows that Fred chooses Gamble B, the PREFERRED BEARER, while Gamble  A  is  the  DEPRECATED  ONE.  Based  on  his  set  PREFERENCE  (RISK SEEKING PREFERENCE), Fred uses INTUITION to decide between Gambles, which leads to the creation of the 'Chooses Gamble B DECISION'. And finally, Fred chooses 'Gamble B DECISION RESULTING ACTION'.

## 5. Related Work

In the literature review, we found no ontology representing the fourfold pattern of risk attitudes of the CPT. However, we found a few proposals of ontologies (KORNYSHOVA and  DENECKERE, 2010; NOWARA, 2017) that consider intuitive  decision  making, which are the source of cognitive biases and risk preferences, but they do not consider the cognitive biases neither the risk preferences.

Brodaric and Neuhaus (2020) provided a conceptual and formal foundation for an ontology  of  beliefs,  desires,  and  intentions,  and  discussed  how  their  theory  can  be extended to some major philosophical accounts of desires, and cognitive biases such as wishful thinking. However, the cognitive biases concerned by Tversky and Kahneman (1974)  stem  from  the  reliance  on  judgmental  heuristics  and  are  not  attributable  to motivational effects such as wishful thinking or the distortion of judgments by payoffs and penalties.

So, to the best of our knowledge, there are no ontologies considering relevant concepts to model the fourfold pattern of risk attitudes of the CPT for decision making under uncertainty.

[FIGURE]

## 6. Conclusion

Our proposed ontology makes explicit what is involved in a decision making whether it is a rational or intuitive decision. Our main contribution is considering intuitive decision making  under  risk  and  uncertainty.  Most  decision  makers  are  unaware  that  they  use reference points, so they are likely to decide 'without realizing how it can bias their choice of action' (FRENCH et al, 2009, p. 38). Our proposed ontology allows the decision maker to improve his decision making by understanding how his preferences are influenced by his reference point and cognitive biases in an intuitive decision. It can be achieved by improving the understanding of the risk preferences and the situation in which they occur. Future work includes the evaluation of the ontology w.r.t. its completeness and perceived usefulness. Moreover, the ontology may be used as part of a strategy to reduce the biases, and  contribute  to  improving  the  development  of  Decision  Support  Systems  (DSS) considering intuitive decision making. This may allow a joint decision making between human and DSS that can ultimately help human decision makers reach better decisions (TINTAREV et al., 2016) by allowing them to understand how their preferences can be biased in comparison with rational decision making, and how such biases may occur.

## References

- ABATECOLA,  Gianpaolo;  CAPUTO,  Andrea;  CRISTOFARO,  Matteo.  Reviewing cognitive distortions in managerial decision making.  Journal  of  Management Development, 2018.
- ARNOTT, D., &amp; GAO, S. (2019). Behavioral economics for decision support systems researchers. Decision Support Systems, 122, 113063.
- BARBERIS, Nicholas C. Thirty years of prospect theory in economics: A review and assessment. Journal of Economic Perspectives, 2013, 27.1: 173-96.
- BAZERMAN, M. H., &amp; MOORE, D. A. (2013). Judgement in Managerial Decision 8th edition edn.
- BRODARIC, B.; NEUHAUS, F. Foundations  for  an  Ontology  of  Belief,  Desire  and Intention.  In:  Formal  Ontology  in  Information  Systems:  Proceedings  of  the  11th International Conference (FOIS 2020). IOS Press, 2020. p. 140.
- CRISTOFARO, M. (2017). Reducing biases of decision-making processes in complex organizations. Management Research Review.
- FRENCH, S., MAULE, J., &amp; PAPAMICHAIL, N. (2009). Decision behaviour, analysis and support. Cambridge University Press.
- GIGERENZER, G. (1999). Simple heuristics that make us smart. New York, NY: Oxford University.
- GUIZZARDI, Renata SS, et al. A Core Ontology on Decision Making. In: ONTOBRAS. 2020. p. 9-21.
- KAHNEMAN, D. (2011) Thinking, Fast and Slow, first ed. Farrar, Straus and Giroux, New York.
- KAHNEMAN, D.; KLEIN, G. Conditions for intuitive expertise: a failure to disagree. American psychologist, 2009, 64.6: 515.

[FIGURE]

- KAHNEMAN, D., LOVALLO, D., &amp; SIBONY, O. (2011). Before you make that big decision. Harvard business review, 89(6), 50-60.
- KORNYSHOVA,  E.;  DENECKERE,  R.  Decision-Making  Ontology  for  Information System Engineering. ER 2010 29th International Conference on Conceptual Modeling, Nov 2010, Vancouver, Canada. Springer, 6412/2010, pp.104-117, 2010, Lecture Notes in Computer Science. &lt;10.1007/978-3-642- 16373-9\_8&gt;.
- LANNING, M.J.; MICHAELS, E.G. A business is a value delivery system. McKinsey staff paper, 1988.
- LEWANDOWSKI, Michał. Prospect theory versus expected utility theory: Assumptions, predictions,  intuition  and  modelling  of  risk  attitudes.  Central  European  Journal  of Economic Modelling and Econometrics, 2017, 275-321-275-321.
- OVE HANSSON, S. Decision Theory. A Brief Introduction. Stockholm: Royal Institute of Technology, pristupano, 2005, 2: 2020.
- PALMER,  Daniel  E..  "Expected  utility".  Encyclopedia  Britannica,  18  May.  2016, https://www.britannica.com/topic/expected-utility. Accessed 13 August 2021.
- PORELLO, D., GUIZZARDI, G., Sales, T., and Amaral, G. (2020). A core ontology for economic exchanges. In 39th International Conference on Conceptual Modeling.
- PORELLO, D., GUIZZARDI, G. (2018). Towards an ontological modeling of preference relations.  In  17th  International  Conference  of  the  Italian  Association  for  Artificial Intelligence, pages 152-165.
- SALES, T. P., BAIÃO, F., GUIZZARDI, G., ALMEIDA, J. P. A., GUARINO, N., &amp; Mylopoulos, J. (2018, October). The common ontology of value and risk. In International Conference on Conceptual Modeling (pp. 121-135). Springer, Cham.
- SHARDA,  R.,  DELEN,  D.,  and  TURBAN,  E.  Business  Intelligence  and  Analytics: Systems  for  Decision  Support.  Pearson  Education,  10th  edition,  ISBN  978-0-13305090-5, 2014
- SIMON, Herbert A. (1997) Administrative behavior: a study of decision-making process in administrative organizations. The Free Press. Fourth edition.
- THALER, R. H., &amp; GANSER, L. J. (2015). Misbehaving: The making of behavioral economics. New York: WW Norton.
- TSIPURSKY, Gleb. (2019) Never Go With Your Gut: How Pioneering Leaders Make the Best Decisions and Avoid Business Disasters. Kindle.
- TVERSKY, A., &amp; KAHNEMAN, D. (1974). Judgment under uncertainty: Heuristics and biases. Science, 185(4157), 1124-1131.
- TVERSKY,  A.,  &amp;  KAHNEMAN,  D.  Advances  in  prospect  theory:  Cumulative representation of uncertainty. Journal of Risk and uncertainty, v. 5, n. 4, p. 297-323, 1992.
- VAN  RIEL,  Allard  CR;  HORVÁTH,  Csilla.  Conceptualizing  intuition  as  a  mental faculty: Toward a 'critique of intuitive reason'and a process model of intuition. In: Handbook of research methods on intuition. Edward Elgar Publishing, 2014.

[FIGURE]
