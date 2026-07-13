## OntoREA© Accounting and Finance Model: Including Option Contracts in the MDD-Context

```
Christian Fischer-Pauzenberger 1[0000-0002-9071-9523] , Matthias Ondra, Walter S.A. Schwaiger 1[0000-0003-1868-7018] 1  Technische Universität Wien, Institute of Management Science, Theresianumgasse 27, 1040 Wien, Austria {christian.fischer-pauzenberger, matthias.ondra,
```

walter.schwaiger}@tuwien.ac.at

Abstract. OntoREA© is a specification of the Accounting and Finance domain in  the  OntoUML language [1] which includes derivative instruments as  well. The authors use a forward contract as running example to demonstrate the validity of the OntoREA© Accounting and Finance model within the design science resource methodology (DSRM) [2]. They claim but they do not proof that the model not only holds for forward but also for option contracts. In this article the missing proof is given by refining the relational MySQL model. In the model  driven  development (MDD) context [3] this model constitutes the platform specific  model (PSM) which is derived from the platform independent model (PIM) in form of the OntoREA© model. The refined PSM model  adequately represents  European  option  contracts  and  it  should  be  especially  useful  for business analysts as well as for educational purposes.

Keywords: OntoREA© Accounting and Finance Model, Design Science Research  Methodology  DSRM,  Model  Driven  Development  MDD,  Conceptual Modeling, Derivative Instruments, Dynamic Hedge Portfolio

## 1 Introduction

The  no-arbitrage  pricing  theory  also  holds  for  options.  For  options  a  dynamic hedge portfolio exactly replicates (duplicates) the option value over time. In a dynamic replication policy fractions of the stock are bought and they are partially financed by  a  loan  liability.  Over  time  the  investment  and  financing  has  to  be  continuously adjusted  according  to  the  revealing  stock  prices.  At  the  expiration  date  the  hedge portfolio gives the same result as the initial buying of an option contract. [1]

In contrast to options the hedge portfolio composition of a forward contract does not change over time and that's why it is called a static  hedge  portfolio .  The  static hedge  portfolio  representation  was  used  in  [1]  to  demonstrate  the  suitability  of  the OntoREA© Accounting and Finance model as conceptual platform independent model (PIM) for the development of a platform specific MySQL relational database model (PSM) within the model-driven software development context (MDD).

The hedge portfolio representation of derivative instruments is one of the core features of the OntoREA© model and it is expressed in the upper left part of Figure 1 in form of the Collective class  Derivative Instrument and its MemberOf relationship to the Kind class Economic Resource. In simple terms the meta-physical stereotypes of the OntoUML language have the following meaning (for a full description of the conceptual and meta-physical OntoUML details see [4]): A derivative instrument is represented as a rigid and identity-providing portfolio collective that consists of two economic resources that are themselves rigid and identity providing kinds .

Figure 1: OntoREA© Accounting and Finance Model - Conceptual PIM Level

[FIGURE]

The hedge portfolio [5] representation of derivative instruments was originated by the  Nobel  laureates  Black/Scholes  [6]  and  Merton  [7]  who  developed  to  the noarbitrage pricing theory . This representation holds true for unconditional derivatives (e.g. forward contracts) as well as for conditional derivatives (e.g. option contracts). The main difference between un- and conditional derivates lies in the dynamic behavior of the hedge portfolio composition. Unconditional derivatives include the obligation for the buyer of the contract to buy the underlying asset in the future. Due to this obligation  the  hedge  portfolio  composition  does  not  change  over  time.  Conditional derivatives include the right for the buyer of the contract to buy the asset in the future.

As the probability of executing the option is changing over time, the hedge portfolio composition changes as well.

The research objective of this article is to provide the proof that the conceptual OntoREA© PIM model incorporates not only the static but also the dynamic hedge portfolio  representation  of  derivative  instruments.  For  this  purpose  a  refined  MySQL database PSM model is constructed that includes the peculiarities of dynamic hedging portfolios as  well,  so  that  un-  and  conditional  derivative  instruments  are  covered  in the proposed PSM model.

This paper is organized as follows: In the next section the no-arbitrage pricing theory and its hedge portfolio foundation are presented. In following section the refined relational  database  model  (PSM)  for  un-  and  conditional  derivative  instruments  is presented and its applicability to conditional option contracts is demonstrated with a stock call running example. The last section concludes the paper and shows directions for further research.

## 2 No-Arbitrage Pricing: Hedge Portfolio Representation

The no-arbitrage  pricing  theory  was  -  as  already  mentioned  -  developed  by  the Nobel laureates Black/Scholes [6] and Merton [7]. They show that there is only one price  for  the  derivative  instruments,  i.e.  the  no-arbitrage  price  that  does  not  allow arbitrage possibilities. They derive the no-arbitrage price for European stock call options. European stock calls have the peculiarity that the right to buy refers to a stock asset, which is the underlying of the contract, and that the right can be exercised by the  buyer  of  the  contract  only  at  expiration  date  (European  style).  The  no-arbitrage price for the European stock call is given by the Black/Scholes formula:

<!-- formula-not-decoded -->

As can be seen by the annotations in equation 1, the no-arbitrage price, which is called fair value , corresponds according to the hedge portfolio of two parts: The value of the asset ( asset value ) on the left side (left leg) and the present value of the liability ( loan liability ) on the right side.

The asset weight , i.e. N ( d1,t ) gives the fraction of the underlying stock that is hold in the hedge portfolio. It is calculated by evaluating the standard normal distribution function N () at the value of d1,t . The d1,t -value (for further details see [6]) is a function of the stock Price PA,t and the time to maturity Tt,T . Consequently this value changes over the life cycle of the call option. The asset weight is a probabilistic term that expresses the probability of a stock option execution. It ranges between zero and 100 %.

The present value of the loan liability is calculated by weighting the exercise price X0,T with the weighting factor N ( d2,t ) and discounting the resulting product by multiplying it with the discount factor exp (-ln (1+ R0,T )* Tt,T ). The discount factor is calculat- ed in form of a continuous compounding by inserting  the interest rate R0,T over  the whole life time of the option, i.e. from 0 to T, and the time to maturity Tt,T into the Euler exponential.

Finally, by using the t variable for the pricing date, the Black/Scholes formula is generically defined so that it can be applied for the initial (i.e. t = 0) and the subsequent (i.e. t &gt; 0) pricing.

Table 1: European Stock Call (running example) - Specification and Pricing

| Contracting date:       | 01.01.    |
|-------------------------|-----------|
| Expiration date:        | 31.12.    |
| Exercise price:         | 100       |
| Initial stock price:    | 100       |
| Volatility:             | 20%       |
| Initial interest rate:  | 5%        |
| Asset weight N(d1):     | 63.68%    |
| Liability weight N(d2): | 55.96%    |
| Stock Asset:            | 63.68     |
| Loan Liability:         | 53.23     |
| Fair value: = A - L     | 10.45 (A) |

Table 1 contains the specification of a European stock call and its initial pricing at the beginning of the year (01.01.) according to the Black/Scholes formula, which is evaluated at the contracting date, i.e. t = 0. The fair value of the stock option, i.e. its no-arbitrage  price,  amounts  to  10.45  and  it  is  calculated  by  subtracting  the  present value of the loan liability (53.23) from the value of the stock asset (63.68).

Due  to  its  generic  definition  the  Black/Scholes  formula  can  be  used  for  pricing purpose not only at the call's contracting date but also at subsequent dates.  The big advantage of the formula is that it not only gives the call price, but also the composition of the hedge portfolio at all pricing dates.

The composition information is of special importance in the case of a dynamic call replication policy , where the call is not bought initially but instead it is synthetically created by implementing and rebalancing the dynamic hedge portfolio over time. In this  case  the  asset  weights N ( d1,t )  are  of  special  importance. They indicate the fractions of the underlying stock assets in the hedge portfolio.

For demonstrative purposes a pricing after each quarter is assumed. Furthermore it is assumed that the stock price from initially 100 does not change after the first and second quarter and then increases to 120. In this constellation - as can be seen in the first  column  of  Table  2  -  the  asset  weights  start  decreasing  from  63.68  %  (01.01.: 100) to 61.91 % (31.03.: 100) and to 59.77 % (30.06.: 100) and consequently increase to  97.72  % (30.09.: 120). The initial decrease at the stable price of 100 indicates a decreasing execution probability and consequently a smaller stock position is hold in the hedge portfolio. The stock price increase increases the execution probability and consequently  the  stock  position  in  the  hedge  portfolio.  The  changing  asset  weights over the call's life time demonstrate what is meant by saying that the composition of the option's hedge portfolio is changing over time. This changing composition in the dynamic hedge portfolio  is  contrasted  to  the  stable  composition  in  the  static  hedge portfolio of stock forwards where at each point in time exactly one unit of the underlying stock is held in the hedge portfolio.

## 3 Hedge Portfolio: Switching from PIM- to PSM-Level

After  having  a  deeper  understanding  of  the  hedge  portfolio  in  the  Black/Scholes formula,  the  transformation  of  its  conceptualization  in  the  OntoREA©  Accounting and Finance model - as the Collective class Derivative Instrument with a MemberOf relationship to the Kind class  Economic  Resource - into a MySQL database model can be addressed. In the MDD context this transformation corresponds to the switch from an abstract conceptual PIM model into a specific database PSM model. Associated with this concretization step is an informational extension that is accomplished by adding additional attributes and tables in the PSM model in order to capture the more detailed contents at the PSM model level.

Figure 2: MySQL Relational Database Model - Database PSM Level

[FIGURE]

Figure 2 contains the refined database PSM model that concretizes the OntoREA© conceptualization  of  the  derivative  instruments'  hedge  portfolio  representation.  It covers not only unconditional but also conditional derivative instruments. Compared to the development of the MySQL database (PSM) model related to the static hedge portfolio representation in [1], the dynamic hedge portfolio peculiarities for the stock options are now explicitly incorporated for the:

1. Collective class Derivative Instrument,
2. MemberOf relationship between Collective class Derivative Instrument and Kind class Economic Resource and
3. Formal relationship in-/outflow (out-/inflow) between Kind class Economic Resource and SubKind class Debit Event (Credit Event).

Ad 1) The Collective class Derivative Instrument is transformed via the four tables in the right upper corner of Figure 2. The splitting into four tables allows a clear distinction of information that is stable over time ( master information ) and information that changes ( transactional information ).

- The  table  Derivative\_Instrument\_Master  contains  the  stable  information  which specifies the derivative instruments. Its attribute Type\_Of\_Stock\_Derivative is of ENUM type so that un- and conditional derivatives are covered in the MySQL database model. It can be seen that the table also contains all information from Table 1 which are used to specify the stock call.
- The table Derivative\_Instrument\_Transactional contains the pricing information which is associated to the initial and subsequent pricing dates measured with the Attribut timestamp. In the case of a dynamic replication policy the hedge portfolio  composition  adjustments  are  connected  with  capital  market  transactions. That's why the table has the Transactional suffix.
- The  two  tables  Financial\_Security\_Pricing\_Master  and  Financial\_Security\_Pri-cing\_Transactional are included in order to allow the separate specification of the derivative's underlying asset (i.e. financial security) which is fully defined by its international  security  identification  number  (ISIN).  The  usage  of  two  tables  is due to the intended separation of master and transactional information.

Ad 2) The MemberOf relationship  is  transformed  via  the  two  tables  in  the  lower left part of Figure 2 according to the financial categorization of financial instruments into risky income and fixed income resources. Both tables have a foreign key to the table Derivative\_Instrument\_Transactional. The missing NOT NULL CONSTRAINT (*) indicates that not all of these resource types have to be part of a hedge portfolio. The inclusion of the two tables promotes the understanding of the different financial natures of the two hedge portfolio constituents, i.e. the stock asset (risky income) and the loan liability (fixed income).

Ad 3) The Formal relationship in-/outflows (out-/inflows) between the Kind class Economic Resource and the SubKind class Debit Event (Credit Event) is transformed via  the  relationship  between  the  table  Derivative\_Instrument\_Transactional  and  the reflexive table Event at the bottom of Figure 2. This relationship is needed for triggering events that are - as can be seen in Figure 1 - connected to classes Debit Event and Credit Event. At the pricing dates (timestamp) events are triggered in two cases, i.e. either if the Mark\_To\_Model mode is active (see table Derivative\_Instrument\_Mas-ter) or if a dynamic replication policy is in place. By triggering the events the changes in the hedge portfolio compositions are recognized via balanced double-entries in the accounting system.

After having presented the construction of the MySQL database PIM its working is addressed.  The  storage  of  information  starts  at  the  contracting  date  (initial  pricing date).  At  that  date  the  contracts  for  the  derivative  instruments  are  specified  and  the corresponding information is stored in the master tables. As time goes by - that is at runtime - additional information is revealed. Of special importance for the calculations of the hedge portfolio compositions are the revealing asset prices (see table Fi-nancial\_Security\_Pricing\_Transactional). Furthermore the timestap information in the table Derivative\_Instrument\_Transactional is important as it allows the calculation of the remaining time to maturity ( Tt,T ) together with the attribute Expiration\_Date in the table Derivative\_Instrument\_Master. With this information the hedge portfolio compositions are determined and the corresponding information processing activities are triggered.

Table 2: European Stock Call - Specification and Subsequent Pricing

[FIGURE]

In Table 2 the calculations for the stock call running example can be seen in the first column. It is interesting to note the last fair value at the end of the year (31.12.) amounting to 19.23 is close to the intrinsic value of the stock call amounting to 20 which is calculated as difference between the stock asset value of 120 and the exercise price of 100. By executing the subsequent pricings more often the difference can theoretically  be  brought  to  zero.  For  completeness  it  should  be  mentioned  that  the resulting fair value is connected to a self-financing policy. According to this policy the changing asset fractions are either used for redemption of the loan if they decrease or financed by increasing the loan if the increase.

Finally, the middle and the right column show with which attribute of which table this information is captured in the MySQL database PIM model.

## 4 Conclusion

The  main  contribution  of  this  article  is  the  development  of  a  more  advanced MySQL database PSM model compared to [1] that not only covers static hedge portfolio  representations  for  unconditional  derivatives  (e.g.  stock  forward)  but  also  dynamic hedge portfolio representations for conditional derivatives (e.g. stock call). The applicability of the proposed database PSM model was demonstrated for a European stock call running example. According to the put/call parity analogue results hold for European stock puts, so that the PSM model covers call and put options. Next to the applicability demonstration the proposed PSM model fulfills all peculiarities that are related  to  the  dynamic  hedge  portfolio  representation  specified  in  the  OntoREA© PIM model. In this sense the research objective is reached by delivering the missing proof in [1] in form of a refined database PSM that covers unconditional as well as conditional derivatives.

For  further  research  two  considerations  seem  worthwhile.  Firstly,  the  transformation of the database PSM model into an R/Shiny prototype like in [1] in order to complete also the  2-step  in  the  forward  engineering  approach  in  the  MDD  context. Secondly, the explicit policy level specification seems to be a worthwhile endeavor.

This proposed model can be useful for business analysts in the finance domain as well as for teaching purposes by explaining derivative instruments in form of conceptual PIM and database specific PSM models.

## 5 References

1. Fischer-Pauzenberger,  C.,  Schwaiger,  W.S.A.:  The  OntoREA©  Accounting and Finance Model: A Retroactive DSRM Demonstration Evaluation. In: 10th IFIP WG  8.1. Working Conference, PoEM  2017, Leuven, Belgium, November 22-24, 2017, Proceedings. pp. 81-95. Springer, Cham (2017).
2. Geerts,  G.L.:  International  Journal  of  Accounting  Information  Systems  A design science research methodology  and  its  application to  accounting information systems research. Int. J. Account. Inf. Syst. 12, 142-151 (2011).
3. Pastor, O., España, S., Panach, J.I., Aquino, N.: Model-driven development. Informatik-Spektrum. 31, 394-407 (2008).
4. Fischer-Pauzenberger,  C.,  Schwaiger,  W.S.A.:  The  OntoREA©  Accounting and  Finance  Model :  Ontological  Conceptualization  of  the  Accounting  and Finance  Domain.  In:  36th  International  Conference,  ER  2017,  Valencia, Spain,  November  6-9,  2017,  Proceedings.  pp.  506-519.  Springer,  Cham (2017).
5. Cox, J.C., Ross, S.A., Rubinstein, M.: Option pricing: A simplified approach. J. financ. econ. 7, 229-263 (1979).
6. Black,  F.,  Scholes,  M.:  The  Pricing  of  Options  and  Corporate  Liabilities.  J. Polit. Econ. 81, 637 (1973).
7. Merton, R.C.: Theory of rational Theory option pricing. Bell J. Econ. 4, 141183 (1973).
