# AECO Option Valuation


AECO options are Asian style options whose underlying are natural gas futures prices.  This model prices a call or put on a commodity whose underlying price is based on a futures contract.  The buyer has the option, but not the obligation to receive the difference calculated as the average rate less the strike, in the case of a call, or the strike less the average rate, in the case of a put, as applied against a notional amount.  The average rate is the arithmetic average of the closing rates of the futures contract observed over a designated period of time.  The style of exercise is European, i.e., there is no early exercise feature.

The expected average rate in the Foreign Exchange Model is the average of the rates projected for the observation period.  The expected average rate in the Commodity Model is the rate for the underlying futures contract.  This model is not intended for cases where the observation period spans more than one futures contract.

The Asian volatility in the Foreign Exchange Model is determined from a forward volatility curve.  In the case of the Commodity Model, the volatility is the volatility of the underlying futures contract. Sometimes, an AECO option may have a callable feature.

Let   be a price process of a natural gas futures contract.  Let   be a set of average dates and   be a payoff settlement date.  The price of the underlying is recorded on the set of average dates to obtain the price arithmetic average of A, where

	 .

The payoff of this Asian-European type option at the settlement date is given by

	 ,

where N is the notional principal, and K is the option strike, and   (1 or –1) is the call/put indicator.

Let t be the current value date, then the current value of this derivative security can be written as

	 

where   is the discount factor at the value date.  The governing price dynamics of this underlying asset in the risk-neutral world should be written as

	 

where r is the risk-free interest rate, q is the equivalent dividend yield of the underlying,   is the volatility of the underlying price.  For a futures option like an AECO option, q should be set to r, since the futures price is considered a martingale.
Detailed derivation of the analytical closed-form solution to the general Arithmetic Average derivative securities using the Curran’s method can be found in Ritchie He (2001).  This derivation is based on two Michael Curran’s papers (1992, 1994).
It is assumed that the input “AverageSoFar” is applied from the beginning date of the month to the immediate preceding date prior to the value date if applicable.  The spot price is used as the price for the value date.  

The Greeks of the AECO options can be computed by using numerical differentiation.

(1)	Delta: The Delta value is calculated by shifting the stock price up and down 2.5%.

	 

where   and   are option prices corresponding to shifting the spot price   2.5% up and down, respectively.

(2)	Gamma: The Gamma value is calculated by

	 

where   is the option value corresponding to the spot stock price  .

(3)	Vega: The Vega value is calculated by

	 

where   is the option price corresponding to an upper 1% shift of stock price volatility.

(4)	Theta: The Vega value that measure the rate of change of the option value with respect to the passage of time is given by

	 

where   is the option value assuming one-day shift of value time while all else remains the same.  When   is calculated, if “AverageSoFar” is applicable, this value is applied from the beginning date of the month to the value date, and the spot price is used as the price for the next date. 

Reference:

https://finpricing.com/product.html

