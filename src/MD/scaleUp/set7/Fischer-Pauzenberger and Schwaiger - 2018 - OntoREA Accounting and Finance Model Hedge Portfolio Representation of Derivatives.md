[FIGURE]

## OntoREA © Accounting and Finance Model: Hedge Portfolio Representation of Derivatives

Christian Fischer-Pauzenberger and Walter S. A. Schwaiger ( &amp; )

[FIGURE]

Institute of Management Science, Technische Universit ä t Wien, Theresianumgasse 27, 1040 Vienna, Austria {christian.fischer-pauzenberger, walter.schwaiger}@tuwien.ac.at

Abstract. OntoREA © is a speci fi cation of the Accounting and Finance domain in the OntoUML language [1]. In a previous article [2] the authors use a forward contract fi nancial derivative instrument to demonstrate the validity of the OntoREA © model within the design science research methodology (DSRM) [3]. A forward contract does not change over time and therefore can be modelled as static hedge portfolio composition. However, it is of interest if the OntoREA © model can also hold true for dynamic hedge portfolio compositions, as induced by option contract fi nancial derivative instruments. This article investigates on that and delivers proof that the OntoREA © model is suitable for option contracts as well. Through adequately re fi ning the platform speci fi c database model (PSM) the policy ' s dynamic nature can be demonstrated. Moreover, including a Plan/Do/Check/Act (PDCA) process model for the speci fi cation of the option contract replication also demonstrates the information processing in the REA accounting infrastructure. The proposed approach is implemented into an R/Shiny software prototype where the 3-tier-architecture is used to integrate the database and the PDCA process model at the R/Shiny implementation speci fi c model (ISM) level. The presented hedge portfolio representation of derivatives can be useful for business analysts in the fi nance and accounting domain as well as for teaching fi nancial derivative instruments.

Keywords: OntoREA © Accounting and Finance model Design science research methodology DSRM Model driven development MDD  Conceptual modeling Derivative instruments  Dynamic hedge portfolio

## 1 Introduction

In a preceding article contributing to the OntoREA © Finance and Accounting model research, a forward contract is used to demonstrate validity of the OntoREA © Accounting and Finance Model by specifying a static hedge portfolio representation [2]. The OntoREA © model act as conceptual platform independent model (PIM) for the development of a platform speci fi c PostgreSQL relational database model (PSM) within the model-driven software development context (MDD). The composition of the forward contract does not change over time and that ' s why it is called a static hedge portfolio . Modelling option contracts however result in dynamic hedge portfolio , which comprise the generic research interest of this article: Can the OntoREA © model can also hold true for dynamic hedge portfolio compositions?

The hedge portfolio representation of derivative instruments is one of the core features of the OntoREA © model and it is expressed in the upper left part of Fig. 1 in form of the Collective class Derivative Instrument and its MemberOf relationship to the Kind class Economic Resource. In simple terms the meta-physical stereotypes of the OntoUML language have the following meaning: A derivative instrument is represented as a rigid and identity-providing portfolio collective that consists of two economic resources that are themselves rigid and identity providing kinds .

Fig. 1. OntoREA © Accounting and Finance model - conceptual PIM level

[FIGURE]

The hedge portfolio [4] representation of derivative instruments was originated by the Nobel laureates Black/Scholes [5] and Merton [6] who developed to the no -arbitrage pricing theory . This representation holds true for unconditional derivatives (e.g. forward contracts) as well as for conditional derivatives (e.g. option contracts). Unconditional derivatives include the obligation for the buyer of the contract to buy the underlying asset in the future. Due to this obligation the hedge portfolio composition does not change over time. Conditional derivatives include the right for the buyer of the contract to buy the asset in the future. As the probability of executing the option is changing over time, the hedge portfolio composition changes as well.

The primary research objective of this article lies in delivering the proof that the conceptual OntoREA © PIM model incorporates not only the static but also the dynamic hedge portfolio representation of derivative instruments. The traditional data layer transformation (PIM-PSM-ISM) is enhanced by the inclusion of an additional process model at the PIM and the ISM level to adequately specify the dynamic peculiarities of the dynamic replication policy. This process model extension is shown within the MDD framework in Fig. 2: the dynamic replication policy will be represented as Plan/Do/Check/Act (PDCA) cycle [7] and a PDCA management activity diagram (Fig. 5), respectively.

Fig. 2. Model driven development -extended framework

[FIGURE]

This paper is organized as follows: The next section covers the no-arbitrage pricing theory and its hedge portfolio foundation is presented. Next, the re fi ned relational PSM database model for unand conditional derivative instruments is presented and its applicability to conditional option contracts is demonstrated for a stock call option. Section 4 outlines the software-aided transformation of the PSM- into the ISMdatabase model. Section 5 introduces the PDCA management activity diagram as representation of the dynamic replication policy. The last section concludes the paper.

## 2 No-Arbitrage Pricing: Hedge Portfolio Representation

The no-arbitrage pricing theory was developed by the Nobel laureates Black/Scholes [5] and Merton [6]. They show that there is only one price for the derivative instruments, i.e. the no-arbitrage price that does not allow arbitrage possibilities. They derive the no-arbitrage price for European stock call options. European stock calls have the peculiarity that the right to buy refers to a stock asset, which is the underlying of the contract, and that the right can be exercised by the buyer of the contract only at expiration date (European style). The no-arbitrage price for the European stock call is given by the Black/Scholes formula:

<!-- formula-not-decoded -->

The no-arbitrage price, which is called fair value , corresponds according to the hedge portfolio of two parts: The value of the asset ( asset value ) on the left side (left leg) and the present value of the liability ( loan liability ) on the right side.

The asset weight , i.e. N ( d1,t ) gives the fraction of the underlying stock that is hold in the hedge portfolio. It is calculated by evaluating the standard normal distribution function N () at the value of d1,t . The d1,t -value (for further details see [5]) is a function of the stock Price PA,t and the time to maturity Tt,T . Consequently this value changes over the life cycle of the call option. The asset weight is a probabilistic term that expresses the probability of a stock option execution. It ranges between zero and 100%.

The present value of the loan liability is calculated by weighting the exercise price X0,T with the weighting factor N ( d2,t ) and discounting the resulting product by multiplying it with the discount factor exp (-ln (1+ R0,T ) * Tt,T ). The discount factor is calculated in form of a continuous compounding by inserting the interest rate R0,T over the whole life time of the option, i.e. from 0 to T, and the time to maturity Tt,T into the Euler exponential.

Finally, by using the t variable for the pricing date, the Black/Scholes formula is generically de fi ned so that it can be applied for the initial (i.e. t = 0) and the subsequent (i.e. t &gt; 0) pricing.

Table 1. European stock call (running example) -speci fi cation and pricing

| Contracting date:    | 01.01.   | Initial interest rate:   | 5%        |
|----------------------|----------|--------------------------|-----------|
| Expiration date:     | 31.12.   | Asset weight N(d1):      | 63.68%    |
| Exercise price:      | 100      | Liability weight N(d2):  | 55.96%    |
| Initial stock price: | 100      | Stock Asset:             | 63.68     |
| Volatility:          | 20%      | Loan Liability:          | 53.23     |
|                      |          | Fair value: = A - L      | 10.45 (A) |

Table 1 contains the speci fi cation of a European stock call and its initial pricing at the beginning of the year (01.01.) according to the Black/Scholes formula, which is evaluated at the contracting date, i.e. t = 0. The fair value of the stock option, i.e. its noarbitrage price, amounts to 10.45 and it is calculated by subtracting the present value of the loan liability (53.23) from the value of the stock asset (63.68).

The composition information is of special importance in the case of a dynamic call replication policy , where the call is not bought initially but instead it is synthetically created by implementing and rebalancing the dynamic hedge portfolio over time. In this case the asset weights N ( d1,t ) are of special importance. They indicate the fractions of the underlying stock assets in the hedge portfolio.

For demonstrative purposes a pricing after each quarter is assumed. Furthermore, it is assumed that the stock price from initially 100 does not change after the fi rst and second quarter and then increases to 120. In this constellation -as can be seen in the fi rst column of Table 2 -the asset weights start decreasing from 63.68% (01.01.: 100) to 61.91% (31.03.: 100) and to 59.77% (30.06.: 100) and consequently increase to 97.72% (30.09.: 120). The initial decrease at the stable price of 100 indicates a decreasing execution probability and consequently a smaller stock position is hold in the hedge portfolio. The stock price increase increases the execution probability and consequently the stock position in the hedge portfolio. The changing asset weights over the call ' s life time demonstrate what is meant by saying that the composition of the option ' s hedge portfolio is changing over time. This changing composition in the dynamic hedge portfolio is contrasted to the stable composition in the static hedge portfolio of stock forwards where at each point in time exactly one unit of the underlying stock is held in the hedge portfolio.

## 3 Hedge Portfolio: From PIM- to PSM-Database Models

After having a deeper understanding of the hedge portfolio in the Black/Scholes formula, the transformation of its conceptualization in the OntoREA © Accounting and Finance model -as the Collective class Derivative Instrument with a MemberOf relationship to the Kind class Economic Resource -into a PostgreSQL database model can be addressed. In the MDD context this transformation corresponds to the switch from an abstract conceptual PIM model into a speci fi c database PSM model. Associated with this concretization step is an informational extension that is accomplished by adding additional attributes and tables in the PSM model to capture the more detailed contents at the PSM model level.

Fig. 3. PSM database model -UML data model notation

[FIGURE]

Figure 3 contains the re fi ned PSM database model in the UML data model pro fi le that concretizes the OntoREA © conceptualization of the derivative instruments ' hedge portfolio representation. It covers not only unconditional but also conditional derivative instruments. Compared to the development of the PostgreSQL database (PSM) model related to the static hedge portfolio representation in [2], the dynamic hedge portfolio peculiarities for the stock options are now explicitly incorporated for the:

1. Collective class Derivative Instrument,
2. MemberOf relationship between Collective class Derivative Instrument and Kind class Economic Resource and
3. Formal relationship in-/outflow (out-/inflow) between Kind class Economic Resource and SubKind class Debit Event (Credit Event).
4. Ad 1) The Collective class Derivative Instrument is transformed via the four tables in the right upper corner of Fig. 3. The splitting into four tables allows a clear distinction of information that is stable over time ( master information ) and information that changes ( transactional information ).
- The table Derivative\_Instrument\_Master contains the stable information which speci fi es the derivative instruments. Its attribute Type\_Of\_Stock\_Derivative is of INTEGER type so that un- and conditional derivatives are covered in the PostgreSQL database model.
- The two tables Financial\_Security\_Pricing\_Master and Financial\_Security\_Pri-cing\_Transactional are included in order to allow the separate speci fi cation of the derivative ' s underlying asset (i.e. fi nancial security) which is fully de fi ned by its international security identi fi cation number (ISIN).
- The table Derivative\_Instrument\_Transactional contains the pricing information which is associated to the initial and subsequent pricing dates measured with the Attribut timestamp. In the case of a dynamic replication policy the hedge portfolio composition adjustments are connected with capital market transactions.
8. Ad 2) The MemberOf relationship is transformed via the three tables in the lower left part of Fig. 3 according to the fi nancial categorization of fi nancial instruments into risky income, fi xed income and equity resources. All three tables have a foreign key to the table Derivative\_Instrument\_Transactional. The inclusion of the tables speci fi es the different fi nancial resource types of the hedge portfolio constituents, i.e. the stock asset (risky income) and the loan liability ( fi xed income).

Ad 3) The Formal relationship in-/outflows (out-/inflows) between the Kind class Economic Resource and the SubKind class Debit Event (Credit Event) is transformed by introducing change classes for the asset (A), liability (L) and equity (E) resource types. Furthermore the asset and liability related classes are each equipped with the attribute Debit\_Or\_Credit in order to get the connection with the debit and credit entries in the REA accounting infrastructure of the OntoREA © model.

The introduction of the equity resource type is needed for capturing the revenues and expenses that occur by executing the dynamic replication policy over time.

In Table 2 the calculations for the stock call can be seen in the fi rst column. It is interesting to note the last fair value at the end of the year (31.12.) amounting to 19.23 is close to the intrinsic value of the stock call amounting to 20 which is calculated as difference between the stock asset value of 120 and the exercise price of 100. The resulting fair value at the option ' s expiration date is connected to a self- fi nancing policy. According to this policy the changing asset fractions are either used for redemption of the loan if they decrease or fi nanced by increasing the loan if the increase.

Table 2. European stock call -speci fi cation and subsequent pricing

[FIGURE]

## 4 Hedge Portfolio: From PSM- to ISM-Database Models

After translating the OntoREA © PIM model into the PSM database model the second MDD transformation is performed, i.e. the transformation from the PostgreSQL PSM database model into the Shiny ISM database model. The ISM database model represents the physical database schema of the PostgreSQL relational database.

This second transformation step is partly automated and supported by the UML modeling software Enterprise Architect. With this automated transformation all data storage requirements of the dynamic hedge portfolio are covered in the ISM database model. But the ISM data model does not consider the information of the dynamic replication policy which is modeled in the PDCA management activity diagram (Fig. 5). To include the policy ' s PDCA representation in the R/Shiny application a generic 3-tier-architecture is chosen.

The left side of Fig. 4 shows the 3-tier-architecture and the right side relates to its implementation in the R/Shiny technology. The 3-tier-architecture is built upon a modular layer concept. In R/Shiny the modularity between Tier 3 and Tier 2 is achieved by using R/DBI database interface.

Fig. 4. 3-Tier-architecture -implementation in R/Shiny

[FIGURE]

The traditional data transformation in the extended MDD framework (Fig. 2) relates to Tier 3, i.e. to the Data Access Layer. The PDCA management process representation of the dynamic replication policy relates to Tier 2 and Tier 1. This transformation from the PSM process model into the Shiny PIM process model is given now.

## 5 Hedge Portfolio: PDCA-Process Representation

The R/Shiny Reactivity technology is the key for implementing the PDCA management process representation of the dynamic replication policy.

Fig. 5. PDCA management activity diagram

[FIGURE]

The repeating (iterating) nature of the dynamic replication policy can be seen in Fig. 5 by the arrow that links the gateway before the termination node to the gatewayafter the starting node. After having speci fi ed the PIM process model for the dynamic replication policy in form of the PDCA management activity diagram it can be translated into the R/Shiny ISM process model.

- The &lt;&lt;Do&gt;&gt; prompts the user to enter the present pricing information (stock price and timestamp). The information gets stored in the table Financial\_Security\_-Pricing\_Transactional (see Fig. 3).
- The &lt;&lt;Check&gt;&gt; activity activation compares the actual N(d1) value with the one of the last pricing observations and calculates the difference. The difference indicates the required change in asset weights. The negative value of -0,0177 indicates to sell this quantity of the stock asset (a positive amount would indicate a purchase of stock assets).
- After pressing the &lt;&lt;Plan&gt;&gt; activity button the current asset weight N(d1) is calculated and displayed.
- Pressing the &lt;&lt;Act&gt;&gt; activity button executes this indication in the fi nal step. Connected with this rebalancing execution the according data are inserted into the PostgreSQL database.

The re fi ned PSM database model in Fig. 3 implements the REA accounting infrastructure -that can be seen on top of the OntoREA © PIM model (Fig. 1) via the three Kind classes Economic Resource, Economic Event and Economic Agent -in a special, somehow hidden way.

Table 3. Showing resource chances in T-accounts

Table 3 shows the contents of the attributes Value\_Change (A), Present\_Value\_-Change (L) as well as Debit\_Value (E) and Credit\_Value (E) for the three change classes in a traditional T-account format. Correspondingly, they specify the changes of the asset (A) resource risky income (stock), the liability (L) resource fi xed income (loan) and the equity (E) resource which are associated with each single transactional loop. At the initial pricing date (01.01.) the hedging portfolio is set up. The buying of the risky income stock (A) according to the initial asset weight of 0.6368 causes the debit entry amounting to 63.38. This purchase is partially fi nanced by taking a fi xed income loan (L) amounting to 53.23. As the purchase price is higher than the loan the difference has to be covered by cash. In order to fund the needed cash amount (10.45) an equity position is established by booking a corresponding Credit\_Value entry.

At the subsequent pricing date (31.03.) the stock asset weight declines according to the Black/Scholes formula. The negative difference of the asset weight ( -0.0177) is sold in the stock market at the stock price of 100 (Credit entry of 1.77 in the stock asset). The cash earned (+1.77) is used to pay the interest (Debit\_Value entry of 0.67)

and to pay back part of the loan ' s face value (Debit entry of 1.10). At the following to the next pricing date (10.09.) the same procedure applies. The only difference is the inclusion of a capital gain that results from the stock price increase from 100 to 120. The capital gain (Credit\_Value entry) is calculated by multiplying the asset weight of the previous pricing date (0.5977) with the stock price change (20).

Finally, the balanced duality of the different debit and credit entries can be shown: They correspond to the equal sums of the debit and credit entries at each pricing date.

## 6 Conclusion

The primary research objective of this article is the delivery of the proof that the hedge portfolio representation of derivative instruments speci fi ed in the OntoREA © PIM model covers not only unconditional (forward contracts) but conditional (option contracts) as well. This proof is delivered in the MDD-context by translating the OntoREA © PIM model into a PSM database model which is re fi ned compared to [2]. The re fi nement refers especially to the separation of master and transactional data, which allows the adequate inclusion of the hedge portfolio data representation.

To include the conditional derivatives ' dynamic management processes the MDD framework was extended by including the process representation next to the traditional data representation. Equipped with this view the dynamic replication policy is represented as a PDCA management process model at the PIM level that can be directly transformed into a ISM process model. For demonstrative purposes a European stock call is synthetically constructed by executing the dynamic replication policy. Its software implementation is demonstrated in an R/Shiny application where the 3-tierarchitecture is used to integrate the database and the PDCA process model at the R/Shiny ISM level.

The hedge portfolio representation of (un-)conditional derivative instruments in the extended MDD framework can be useful for business analysts in the fi nance and accounting domain as well as for software engineers by not only explaining derivatives in form of PIM, PSM and ISM data and process models but also by implementing the derivatives ' hedge portfolio representation models in real software application.

## References

1. Fischer-Pauzenberger, C., Schwaiger, W.S.A.: The OntoREA © Accounting and Finance model: ontological conceptualization of the accounting and fi nance domain. In: Mayr, H.C., Guizzardi, G., Ma, H., Pastor, O. (eds.) ER 2017. LNCS, vol. 10650, pp. 506 -519. Springer, Cham (2017). https://doi.org/10.1007/978-3-319-69904-2\_38
2. Fischer-Pauzenberger, C., Schwaiger, W.S.A.: The OntoREA © Accounting and Finance model: a retroactive DSRM demonstration evaluation. In: Poels, G., Gailly, F., Serral Asensio, E., Snoeck, M. (eds.) PoEM 2017. LNBIP, vol. 305, pp. 81 -95. Springer, Cham (2017). https://doi.org/10.1007/978-3-319-70241-4\_6
3. Geerts, G.L.: International journal of accounting information systems a design science research methodology and its application to accounting information systems research. Int. J. Account. Inf. Syst. 12 , 142 -151 (2011)

4. Cox, J.C., Ross, S.A., Rubinstein, M.: Option pricing: a simpli fi ed approach. J. Financ. Econ. 7 , 229 -263 (1979)
5. Black, F., Scholes, M.: The pricing of options and corporate liabilities. J. Polit. Econ. 81 , 637 (1973)
6. Merton, R.C.: Theory of rational theory option pricing. Bell J. Econ. 4 , 141 -183 (1973)
7. Schwaiger, W.S.A., Abmayer, M.: Accounting and management information systems. In: Proceedings of International Conference on Information Integration Web-based Application Services - IIWAS 2013, pp. 346 -352 (2013)
