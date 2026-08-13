# VIXY
The VIXY (ProShares VIX Short-Term Futures ETF) is a fund that tracks market volatility. It is designed to surge in value
during periods of sudden macroeconomic stress or market uncertainty. To maintain a constant one-month maturity, the fund
must roll its futures contracts on a daily basis. Since VIXY is heavily impacted by contango (market state where longer-dated
VIX futures are more expensive than near-term ones), VIXY must sell cheaper, expiring futures, and buy more expensive
next-month contracts. As a result, this negative roll yield (selling low and buying high) causes the fund’s net asset value to
consistently decay over time.
Due to VIXY’s structural downward drift, VIXY has become a big target for short sellers. However, high demand to
short the ETN leads to limited availability. Brokers classify VIXY as hard to borrow and charge high daily borrow fees that
often neutralize profitability of the trade. To bypass the brutal broker fees, institutional traders go to the options market.
Our project backtests a three year trading strategy that utilizes synthetic shorting. To create a synthetic short, we pair
two options together that mimic a normal short. By buying a put and selling a call at the same strike price, we build a trade
that makes money when VIXY drops and loses money when it climbs. This allows for the same results as a traditional short,
without the struggle of finding a broker that has shares to lend.
On another note, the options market is highly efficient. Since many people want to buy ”insurance” against a market
crash, the price of VIXY options gets pushed higher. This creates a hidden fee inside the price of the options. By looking at
three years of historical data, our project uses the Put-Call Parity to figure out exactly how much the borrow cost is. Our
goal is to see if VIXY’s natural decay is big enough to actually make a profit, or if the borrow cost is so high that it makes
the trade a waste of time.
