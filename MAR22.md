\newpage

# Standardised approach: default risk capital requirement {#MAR22}

This chapter sets out the calculation of the default risk capital requirement under the standardised approach for market
risk.

## Main concepts of default risk capital requirements {#MAR22.1}

The default risk capital (DRC) requirement is intended to capture jump-to-default (JTD) risk that may not be captured by
credit spread shocks under the sensitivities-based method. DRC requirements provide some limited hedging recognition. In
this chapter offsetting refers to the netting of exposures to the same obligor (where a short exposure may be subtracted
in full from a long exposure) and hedging refers to the application of a partial hedge benefit from the short
exposures (where the risk of long and short exposures in distinct obligors do not fully offset due to basis or
correlation risks).

## Instruments subject to the default risk capital requirement {#MAR22.2}

The DRC requirement must be calculated for instruments subject to default risk:

1. Non-securitisation portfolios
   
2. Securitisation portfolio (non-correlation trading portfolio, or non-CTP)
   
3. Securitisation (correlation trading portfolio, or CTP)

## Overview of DRC requirement calculation {#MAR22.3}

The following step-by-step approach must be followed for each risk class subject to default risk. The specific
definition of gross JTD risk, net JTD risk, bucket, risk weight and the method for aggregation of DRC requirement across
buckets are separately set out per each risk class in subsections in [MAR22.9] to [MAR22.26].

1. The gross JTD risk of each exposure is computed separately.
   
2. With respect to the same obligator, the JTD amounts of long and short exposures are offset (where permissible) to
   produce net long and/or net short exposure amounts per distinct obligor.
   
3. Net JTD risk positions are then allocated to buckets.
   
4. Within a bucket, a hedge benefit ratio is calculated using net long and short JTD risk positions. This acts as a
   discount factor that reduces the amount of net short positions to be netted against net long positions within a
   bucket. A prescribed risk weight is applied to the net positions which are then aggregated.
   
5. Bucket level DRC requirements are aggregated as a simple sum across buckets to give the overall DRC requirement.

No diversification benefit is recognised between the DRC requirements for:

1. non-securitisations;
   
2. securitisations (non-CTP); and
   
3. securitisations (CTP).

For traded non-securitisation credit and equity derivatives, JTD risk positions by individual constituent issuer legal
entity should be determined by applying a look-through approach.

For the CTP, the capital requirement calculation includes the default risk for non-securitisation hedges. These hedges
must be removed from the calculation of default risk non-securitisation.

Claims on sovereigns, public sector entities and multilateral development banks may, at national discretion, be subject
to a zero default risk weight in line with paragraphs 7 through 15 in the Basel III credit risk framework. National
authorities may apply a non-zero risk weight to securities issued by certain foreign governments, including to
securities denominated in a currency other than that of the issuing government.

For claims on an equity investment in a fund that is subject to the treatment specified in [MAR21.36](3) (ie treated as
an unrated “other sector” equity), the equity investment in the fund shall be treated as an unrated equity instrument.
Where the mandate of that fund allows the fund to invest in primarily high-yield or distressed names, banks shall apply
the maximum risk weight per Table 2 in [MAR 22.24] that is achievable under the fund's mandate (by calculating the
effective average risk weight of the fund when assuming that the fund invests first in defaulted instruments to the
maximum possible extent allowed under its mandate, and then in CCC-rated names to the maximum possible extent, and then
B-rated, and then BB-rated). Neither offsetting nor diversification between these generated exposures and other
exposures is allowed.

## Default risk capital requirement for non-securitisations

### Gross jump-to-default risk positions (gross JTD)

The gross JTD risk position is computed exposure by exposure. For instance, if a bank has a long position on a bond
issued by Apple, and another short position on a bond issued by Apple, it must compute two separate JTD exposures.

For the purpose of DRC requirements, the determination of the long/short direction of positions must be on the basis of
long or short with respect to whether the credit exposure results in a loss or gain in the case of a default.

1. Specifically, a long exposure is defined as a credit exposure that results in a loss in the case of a default.
   
2. For derivative contracts, the long/short direction is also determined by whether the contract will result in a loss
   in the case of a default (ie long or short position is not determined by whether the option or credit default swap (
   CDS), is bought or sold). Thus, for the purpose of DRC requirements, a sold put option on a bond is a long credit
   exposure, since a default results in a loss to the seller of the option.

The gross JTD is a function of the loss given default (LGD), notional amount (or face value) and the cumulative profit
and loss (P&L) already realised on the position, where:

1. notional is the bond-equivalent notional amount (or face value) of the position; and
   
2. P&L is the cumulative mark-to-market loss (or gain) already taken on the exposure. P&L is equal to the market value
   minus the notional amount, where the market value is the current market value of the position.

$$
\begin{aligned}[t] 
   JTD_{long}  &= \max(LGD \times notional + P\&L, 0)\\ 
   JTD_{short} &= \min(LGD \times notional + P\&L, 0)   
\end{aligned}
$$

For calculating the gross JTD, LGD is set as follows:

1. Equity instruments and non-senior debt instruments are assigned an LGD of 100%.
   
2. Senior debt instruments are assigned an LGD of 75%.
   
3. Covered bonds, as defined within [MAR21.51], are assigned an LGD of 25%.
   
4. When the price of the instrument is not linked to the recovery rate of the defaulter (eg a foreign exchange-credit
   hybrid option where the cash flows are swap of cash flows, long EUR coupons and short USD coupons with a knockout
   feature that ends cash flows on an event of default of a particular obligor), there should be no multiplication of
   the notional by the LGD.

In calculating the JTD as set out in [MAR22.11], the notional amount of an instrument that gives rise to a long (short)
exposure is recorded as a positive (negative) value, while the P&L loss (gain) is recorded as a negative (positive)
value. If the contractual or legal terms of the derivative allow for the unwinding of the instrument with no exposure to
default risk, then the JTD is equal to zero.

The notional amount is used to determine the loss of principal at default, and the mark-to-market loss is used to
determine the net loss so as to not double-count the mark-to-market loss already recorded in the market value of the
position.

1. For all instruments, the notional amount is the notional amount of the instrument relative to which the loss of
   principal is determined. Examples are as follows:

    * For a bond, the notional amount is the face value.
      
    * For credit derivatives, the notional amount of a CDS contract or a put option on a bond is the notional amount of
      the derivative contract.
      
    * In the case of a call option on a bond, the notional amount to be used in the JTD calculation is zero (since, in
      the event of default, the call option will not be exercised). In this case, a JTD would extinguish the call
      option's value and this loss would be captured through the mark-to-market P&L term in the JTD calculation.

2. Table 1 illustrates examples of the notional amounts and market values for a long credit position with a
   mark-to-market loss to be used in the JTD calculation, where:

    * the bond-equivalent market value is an intermediate step in determining the P&L for derivative instruments;
      
    * the mark-to-market value of CDS or an option takes an absolute value; and
      
    * the strike amount of the bond option is expressed in terms of the bond price (not the yield).

| Instrument         | Notional           | Bond-equivalent market value            | P&L                                |
|--------------------+--------------------+-----------------------------------------+------------------------------------|
| Bond               | Face value of bond | Market value of bond                    | Market value – face value          |
| CDS                | Notional of CDS    | Notional of CDS                         | – \|MtM value of CDS\|             |
|                    |                    | – \|mark-to-market (MtM) value of CDS\| |                                    |
| Sold put option    | Notional of option | Strike amount                           | (Strike – \|MtM value of option\|) |
| on a bond          |                    | – \|MtM value of option\|               | – Notional                         |
| Bought call option |                    | MtM value of option                     | MtM value of option                |
| on a bond          | 0                  |                                         |                                    |
 
:Examples of components for a long credit position in the JTD calculation

To account for defaults within the one-year capital horizon, the JTD for all exposures of maturity less than one year
and their hedges are scaled by a fraction of a year. No scaling is applied to the JTD for exposures of one year or
greater.^[Note that this paragraph refers to the scaling of gross JTD (ie not net JTD)] For example, the JTD for a
position with a six month maturity would be weighted by one-half, while the JTD for a position with a one year maturity
would have no scaling applied to the JTD.

Cash equity positions (ie stocks) are assigned to a maturity of either more than one year or three months, at banks'
discretion.

For derivative exposures, the maturity of the derivative contract is considered in determining the offsetting criterion,
not the maturity of the underlying instrument.

The maturity weighting applied to the JTD for any sort of product with a maturity of less than three months (such as
short term lending) is floored at a weighting factor of one-fourth or, equivalently, three months (that means that the
positions having shorter-than-three months remaining maturity would be regarded as having a remaining maturity of three
months for the purpose of the DRC requirement).

### Net jump-to-default risk positions (net JTD)

Exposures to the same obligator may be offset as follows:

1. The gross JTD risk positions of long and short exposures to the same obligor may be offset where the short exposure
   has the same or lower seniority relative to the long exposure. For example, a short exposure in an equity may offset
   a long exposure in a bond, but a short exposure in a bond cannot offset a long exposure in the equity.
   
2. For the purposes of determining whether a guaranteed bond is an exposure to the underlying obligor or an exposure to
   the guarantor, the credit risk mitigation requirements set out in paragraphs 189 and 190 of the Basel II framework
   apply.
   
3. Exposures of different maturities that meet this offsetting criterion may be offset as follows.

    * Exposures with maturities longer than the capital horizon (one year) may be fully offset.
      
    * An exposure to an obligor comprising a mix of long and short exposures with a maturity less than the capital
      horizon (equal to one year) must be weighted by the ratio of the exposure's maturity relative to the capital
      horizon. For example, with the one-year capital horizon, a three-month short exposure would be weighted so that
      its benefit against long exposures of longer-than-one-year maturity would be reduced to one quarter of the
      exposure size.^[Basel Committee on Banking Supervision, Revisions to the securitisation framework, December 2014, 2016 and 2018]

In the case of long and short offsetting exposures where both have a maturity under one year, the scaling can be applied
to both the long and short exposures.

Finally, the offsetting may result in net long JTD risk positions and net short JTD risk positions. The net long and net
short JTD risk positions are aggregated separately as described below.

### Calculation of default risk capital requirement for non-securitisation

For the default risk of non-securitisations, three buckets are defined as:

1. corporates;
   
2. sovereigns; and
   
3. local governments and municipalities.

In order to recognise hedging relationship between net long and net short positions within a bucket, a hedge benefit
ratio is computed as follows.

1. A simple sum of the net long JTD risk positions (not risk-weighted) must be calculated, where the summation is across
   the credit quality categories (ie rating bands). The aggregated amount is used in the numerator and denominator of
   the expression of the hedge benefit ratio (HBR) below.
   
2. A simple sum of the net (not risk-weighted) short JTD risk positions must be calculated, where the summation is
   across the credit quality categories (ie rating bands). The aggregated amount is used in the denominator of the
   expression of the HBR below.
   
3. The HBR is the ratio of net long JTD risk positions to the sum of net long JTD and absolute value of net short JTD
   risk positions:
   
   $$ HBR = \frac{ \sum{net JTD_{long}} }{\sum{net JTD_{long}} + \sum{|net JTD_{short}|}} $$

For calculating the weighted net JTD, default risk weights are set depending on the credit quality categories (ie rating
bands) for all three buckets (ie irrespective of the type of counterparty), as set out in Table 2:

| Credit quality category | Default risk weight | 
|-------------------------+---------------------|
| AAA                     | 0.5%                | 
| AA                      | 2%                  | 
| A                       | 3%                  | 
| BBB                     | 6%                  | 
| BB                      | 15%                 | 
| B                       | 30%                 | 
| CCC                     | 50%                 |
| Unrated                 | 15%                 | 
| Defaulted               | 100%                |

: Default risk weights for non-securitisations by credit quality category

The capital requirement for each bucket is to be calculated as the combination of the sum of the risk-weighted long net
JTD, the HBR, and the sum of the risk-weighted short net JTD, where the summation for each long net JTD and short net
JTD is across the credit quality categories (ie rating bands). In the following formula, DRC stands for DRC requirement;
and i refers to an instrument belonging to bucket b.

$$
   DRC_b = \max \left[ \left( \sum_i{RW_i \times net JTD_i} \right) - HBR \times \left( \sum{RW_i \times |net JTD_i|} \right); 0 \right]
$$

No hedging is recognised between different buckets - the total DRC requirement for non-securitisations must be
calculated as a simple sum of the bucket level capital requirements.

## Default risk capital requirement for securitisations (non-CTP)

### Gross jump-to-default risk positions (gross JTD)

For the computation of gross JTD on securitisations, the same approach must be followed as for default risk (
non-securitisations), except that an LGD ratio is not applied to the exposure. Because the LGD is already included in
the default risk weights for securitisations to be applied to the securitisation exposure (see below), to avoid double
counting of LGD the JTD for securitisations is simply the market value of the securitisation exposure (ie the JTD for
tranche positions is their market value).

For the purposes of offsetting and hedging recognition for securitisations (non-CTP), positions in underlying names or a
non-tranched index position may be decomposed proportionately into the equivalent replicating tranches that span the
entire tranche structure. When underlying names are treated in this way, they must be removed from the
non-securitisation default risk treatment.

### Net jump-to-default risk positions (net JTD)

For default risk of securitisations (non-CTP), offsetting is limited to a specific securitisation exposure (ie tranches
with the same underlying asset pool). This means that:

1. no offsetting is permitted between securitisation exposures with different underlying securitised portfolio (ie
   underlying asset pools), even if the attachment and detachment points are the same; and
   
2. no offsetting is permitted between securitisation exposures arising from different tranches with the same securitised
   portfolio.

Securitisation exposures that are otherwise identical except for maturity may be offset. The same offsetting rules for
non-securitisations including scaling down positions of less than one year as set out in [MAR22.15] through [MAR22.18]
apply to JTD risk positions for securitisations (non-CTP). Offsetting within a specific securitisation exposure is
allowed as follows.

1. Securitisation exposures that can be perfectly replicated through decomposition may be offset. Specifically, if a
   collection of long securitisation exposures can be replicated by a collection of short securitisation exposures, then
   the securitisation exposures may be offset.
   
2. Furthermore, when a long securitisation exposure can be replicated by a collection of short securitisation exposures
   with different securitised portfolios, then the securitisation exposure with the “mixed” securitisation portfolio may
   be offset by the combination of replicating securitisation exposures.
   
3. After the decomposition, the offsetting rules would apply as in any other case. As in the case of default risk (
   non-securitisations), long and short securitisation exposures should be determined from the perspective of long or
   short the underlying credit, eg the bank making losses on a long securitisation exposure in the event of a default in
   the securitised portfolio.
   
### Calculation of default risk capital requirement for securitisations (non-CTP)

For default risk of securitisations (non-CTP), the buckets are defined as follows:

1. Corporates (excluding small and medium enterprises) – this bucket takes into account all regions.
   
2. Other buckets – these are defined along two dimensions:
   
   * Asset classes: the 11 asset classes are defined as asset-backed commercial paper; auto Loans/Leases; residential
     mortgage-backed securities (MBS); credit cards; commercial MBS; collateralised loan obligations; collateralised
     debt obligation (CDO)-squared; small and medium enterprises; student loans, other retail; and other wholesale.
   * Regions: the four regions are defined as Asia, Europe, North America and all other.

To assign a securitisation exposure to a bucket, banks must rely on a classification that is commonly used in the market
for grouping securitisation exposures by type and region of underlying.

1. The bank must assign each securitisation exposure to one and only one of the buckets above and it must assign all
   securitisations with the same type and region of underlying to the same bucket.
   
2. Any securitisation exposure that a bank cannot assign to a type or region of underlying in this fashion must be
   assigned to the “other bucket”.

The capital requirement for default risk of securitisations (non-CTP) is determined using a similar approach to that for
non-securitisations. The DRC requirement within a bucket is calculated as follows:

1. The hedge benefit discount HBR, as defined in [MAR22.23], is applied to net short securitisation exposures in that
   bucket.
   
2. The capital requirement is calculated as in [MAR22.25].

For calculating the weighted net JTD, the risk weights of securitisation exposures are defined by the tranche instead of
the credit quality. The risk weight for securitisations (non-CTP) is applied as follows:

1. The default risk weights for securitisation exposures are based on the corresponding risk weights for banking book
   instruments, which is defined in a separate Basel Committee publication - Revisions to the Securitisations framework
   of 2014, 2016 and 2018 (securitisation transactions that are assessed as simple, transparent and comparable-compliant
   for capital purposes are subject to alternative capital treatment requirements outlined in [the same documents]) with
   the following modification: the maturity component in the banking book securitisation framework is set to zero (ie a
   one-year maturity is assumed) to avoid double-counting of risks in the maturity adjustment (of the banking book
   approach) since migration risk in the trading book will be captured in the credit spread capital requirement.
   
2. Following the corresponding treatment in the banking book, the hierarchy of approaches in determining the risk
   weights should be applied at the underlying pool level.
   
3. The capital requirement under the standardised approach for an individual cash securitisation position can be capped
   at the fair value of the transaction.

No hedging is recognised between different buckets. Therefore, the total capital requirement for default risk
securitisations must be calculated as a simple sum of the bucket-level capital requirements.

## Default risk capital requirement for securitisations (CTP)

### Gross jump-to-default risk positions (gross JTD)

For the computation of gross JTD on securitisations (CTP), the same approach must be followed as for default
risk-securitisations (non-CTP) as described in [MAR22.27].

The gross JTD for non-securitisations (CTP) (ie single-name and index hedges) positions is defined as their market
value.

Nth-to-default products should be treated as tranched products with attachment and detachment points defined below,
where “Total names” is the total number of names in the underlying basket or pool:

1. Attachment point = (N – 1) / Total names
   
2. Detachment point = N / Total names

### Net jump-to-default risk positions (net JTD)

Exposures that are otherwise identical except for maturity may be offset. The same concept of long and short positions
from a perspective of loss or gain in the event of a default as set out in [MAR22.10] and offsetting rules for
non-securitisations including scaling down positions of less than one year as set out in [MAR22.15] to [MAR22.18] apply
to JTD risk positions for securitisations (non-CTP).

1. For index products, for the exact same index family (eg CDX.NA.IG), series (eg series 18) and tranche (eg 0–3%),
   securitisation exposures should be offset (netted) across maturities (subject to the offsetting allowance as
   described above).
   
2. Long and short exposures that are perfect replications through decomposition may be offset as follows. When the
   offsetting involves decomposing single name equivalent exposures, decomposition using a valuation model would be
   allowed in certain cases as follows. Such decomposition is the sensitivity of the security's value to the default of
   the underlying single name obligor. Decomposition with a valuation model is defined as follows: a single name
   equivalent constituent of a securitisation (eg tranched position) is the difference between the unconditional value
   of the securitisation and the conditional value of the securitisation assuming that the single name defaults, with
   zero recovery, where the value is determined by a valuation model. In such cases, the decomposition into single-name
   equivalent exposures must account for the effect of marginal defaults of the single names in the securitisation,
   where in particular the sum of the decomposed single name amounts must be consistent with the undecomposed value of
   the securitisation. Further, such decomposition is restricted to vanilla securitisations (eg vanilla CDOs, index
   tranches or bespokes); while the decomposition of exotic securitisations (eg CDO squared) is prohibited.
   
3. Moreover, for long and short positions in index tranches, and indices (non-tranched), if the exposures are to the
   exact same series of the index, then offsetting is allowed by replication and decomposition. For instance, a long
   securitisation exposure in a 10–15% tranche vs combined short securitisation exposures in 10–12% and 12–15% tranches
   on the same index/series can be offset against each other. Similarly, long securitisation exposures in the various
   tranches that, when combined perfectly, replicate a position in the index series (non-tranched) can be offset against
   a short securitisation exposure in the index series if all the positions are to the exact same index and series (eg
   CDX.NA.IG series 18). Long and short positions in indices and single-name constituents in the index may also be
   offset by decomposition. For instance, single-name long securitisation exposures that perfectly replicate an index
   may be offset against a short securitisation exposure in the index. When a perfect replication is not possible, then
   offsetting is not allowed except as indicated in the next sentence. Where the long and short securitisation exposures
   are otherwise equivalent except for a residual component, the net amount must show the residual exposure. For
   instance, a long securitisation exposure in an index of 125 names, and short securitisation exposures of the
   appropriate replicating amounts in 124 of the names, would result in a net long securitisation exposure in the
   missing 125th name of the index.
   
4. Different tranches of the same index or series may not be offset (netted), different series of the same index may not
   be offset, and different index families may not be offset.

### Calculation of default risk capital requirement for securitisations (CTP)

For default risk of securitisations (CTP), each index is defined as a bucket of its own. A non-exhaustive list of
indices include: CDX North America IG, iTraxx Europe IG, CDX HY, iTraxx XO, LCDX (loan index), iTraxx LevX (loan index),
Asia Corp, Latin America Corp, Other Regions Corp, Major Sovereign (G7 and Western Europe) and Other Sovereign.

Bespoke securitisation exposures should be allocated to the index bucket of the index they are a bespoke tranche of. For
instance, the bespoke tranche 5% - 8% of a given index should be allocated to the bucket of that index.

The default risk weights for securitisations applied to tranches are based on the corresponding risk weights for the
banking book instruments, which is defined in a separate Basel Committee publication - Revisions to the Securitisations
framework of 2014, 2016 and 2018, with the following modification: the maturity component in the banking book
securitisation framework is set to zero, ie a one-year maturity is assumed to avoid double-counting of risks in the
maturity adjustment (of the banking book approach) since migration risk in the trading book will be captured in the
credit spread capital requirement.

For the non-tranched products, the same risk weights for non-securitisations as set out in [MAR22.24] apply. For the
tranched products, banks must derive the risk weight using the banking book treatment as set out in [MAR22.42].

Within a bucket (ie for each index) at an index level, the capital requirement for default risk of securitisations (CTP)
is determined in a similar approach to that for non-securitisations.

1. The hedge benefit ratio (HBR), as defined in [MAR22.23], is modified and applied to net short positions in that
   bucket as in the formula below, where the subscript ctp for the term $HBR_{ctp}$ indicates that the HBR is determined
   using the combined long and short positions across all indices in the CTP (ie not only the long and short positions
   of the bucket by itself). The summation of risk-weighted amounts in the formula spans all exposures relating to the
   index (ie index tranche, bespoke, non-tranche index or single name).
   
2. A deviation from the approach for non-securitisations is that no floor at zero applies at the bucket level, and
   consequently, the DRC requirement at the index level $DRC_b$ can be negative.
   $$
      DRC_b = \left( \sum{RW_i \times net JTD_i} \right) - HBR_{ctp} \times \left( \sum{RW_i \times |net JTD_i|} \right)
   $$

The total DRC requirement for securitisations (CTP) is calculated by aggregating bucket level capital amounts as
follows. For instance, if the DRC requirement for the index CDX North America IG is $+100$ and the DRC requirement for
the index Major Sovereign (G7 and Western Europe) is $-100$, the total DRC requirement for the CTP is $100-0.5 \times
100=50$.^[The procedure for the $DRC_b$ and $DRC_{ctp}$ terms accounts for the basis risk in cross index hedges, as the 
hedge benefit from cross-index short positions is discounted twice, first by the hedge benefit ratio HBR in $DRC_b$,and 
again by the term 0.5 in the $DRC_{ctp}$ equation]

$$ DRC_{ctp} = \max \left[ \sum_b{(\max[DRC_b, 0] + 0.5 \times \min[DRC_b, 0])}, 0 \right] $$

