---
title: "Introduction and Overview"
subtitle: "BUSS386 Futures and Options"
author: "Prof. Ji-Woong Chung"
#date: ""
format: 
  pdf: default
  revealjs:
    theme: simple
    transition: fade
    transition-speed: fast
    scrollable: true
    slide-number: true
    #toc: true
    chalkboard: TRUE
revealjs-plugins:
    - revealjs-text-resizer       # Thanks to https://github.com/gadenbuie/revealjs-text-resizer#readme
execute:
    echo: true
    eval: true
---




## Outline

- Overview of derivatives/markets
- Review: measures of return and risk
- Reading: Hull, Ch. 1.1--1.10 and 22.1--22.3


# Overview


---

## What are derivatives?

- A derivative is a financial security (i.e., instrument, contract, asset) whose value depends on other underlying **variables**.
- Example: A contract to buy 50,000 barrels of crude oil on September 16, 2017, for \$50 per barrel.
- Example: An option contract that gives the holder the right, but not the obligation, to buy 100 shares of a company's stock at \$100 per share within the next three months.


---

## What are the underlying variables?

- Usually, the price of traded assets (e.g., equities, bonds, currencies, commodities)
- Some properties of asset prices (e.g., volatility)
- Certain events (e.g., default)
- Other factors like weather (e.g., temperature, rainfall), inflation, etc.
  
$\Rightarrow$ All variables should be measurable and observable.
	
---

## Type of derivatives

- **Contract Derivatives**
    - Examples: Futures, forwards, swaps, options, warrants, callable bonds (embedded), etc.
    - These contracts bind two counterparties to make a transaction at a future date. All profits and losses result from cash flows between the counterparties, making it a zero-sum game.

- **Securitized or Structured Products**
    - Unlike contract derivatives, securitizations involve a pool or portfolio of underlying securities.
    - Securitization creates new derivative securities that allocate the cash flows from the underlying pool to different classes of investors based on their risk tolerance.
    - Examples: Collateralized mortgage obligations, asset-backed securities, etc.

- **Key Difference**
    - A contract derivative **transfers** risk from one counterparty to the other.
    - A securitized derivative **redistributes** the risk inherent in the underlying assets among different investors.

---

## History of derivatives

::: {style="text-align: center;"}
![](img/intro_dojima.jpg)
:::

<center>
<small>Source: https://professornerdster.com/tag/forward-contracts/</small>
</center>

- Established in the 1690s. Initially, rice exchange
- Futures trading began in 1730 for hedging.

---

## History of derivatives


- Derivatives have been used by farmers and merchants for thousands of years:
    - Around 2000 B.C., derivatives were used in trade between India and the Arab Gulf.
    - In 300 B.C., olive growers in ancient Greece utilized derivatives.

- In the 12th century, European merchants used forward contracts for the future delivery of their goods.
- During Amsterdam's tulip mania in the 1630s, derivatives helped some merchants manage price swings.
- In the 17th century, Japan developed a forward market in rice.

- Modern developments:
    - The Chicago Board of Trade (CBOT) was established in 1848 to trade futures.
    - The Chicago Mercantile Exchange (CME) was founded in 1919. (CBOT and CME later merged to form the CME Group).
    - The Chicago Board Options Exchange (CBOE) introduced call options in 1973 and put options in 1977.
    - In Korea, forex derivatives began trading in 1968, and exchanges were established in 1996.
	


---

## Where to trade derivatives
Derivatives can be traded in two main types of markets:

### Exchange-Traded Market

- **Centralized Trading**: All buy and sell orders are centralized in one place, either physically or electronically.
- **Standardized Contracts**: Contracts are standardized, ensuring uniformity and reducing the risk of counterparty default.
- **Types of Derivatives**: Futures and options are commonly traded.
- **Examples**: Chicago Mercantile Exchange (CME), Chicago Board Options Exchange (CBOE), Hong Kong Exchanges and Clearing (HKEX).
- **Liquidity**: High concentration of trades creates liquidity, which in turn attracts more liquidity.

---

## Where to trade derivatives

### Over-the-Counter (OTC) Market

- **Decentralized Trading**: There is no central place for collecting orders. Participants trade directly with each other or through a network of dealers.
- **Customizable Contracts**: Contracts are not standardized and can be tailored to meet the specific needs of the participants.
- **Main Participants**: Large institutions such as banks, hedge funds, and corporations.
- **Types of Derivatives**: Forwards, swaps, options, and other customized derivatives are traded.

---

## Market Types and Trading Volume

::: {style="text-align: center;"}
![](img/intro_derivative_market_size.png)
:::

<center>
<small>Source: Bank for International Settlement</small>
</center>



---

## What contributed to rapid growth?

"Necessity is the mother of invention" - Plato

- Deregulation, Increased Volatility, and Technological Innovation
    - Key academic contributions: Black and Scholes (1972), Merton (1973)
    - Major events:
        - 1971: Currencies began to free float, leading to the introduction of currency futures in 1972.
        - 1973: The oil shock caused significant volatility in oil prices.
        - 1970s: Inflation and recessions resulted in volatile interest rates.
        - 1978: Deregulation of natural gas.
        - 1990s: Deregulation of electricity markets.

---

## Why are derivatives useful?

- **Derivatives facilitate the transfer of risk** from those who are exposed to it to those more willing to bear it, making them a powerful tool for risk management.  
- While risk management often aims to reduce risk, it can also involve **strategically assuming risks** that offer potential benefits.  
- By effectively redistributing risk, derivatives **enable productive activities** that might otherwise be deemed too risky to pursue.  
- However, derivatives **can be misused**, which is why regulations exist to mitigate potential abuses and ensure market stability.
	
	
<!-- Lucas lecture "0 06 What are derivatives useful" provide some examples. -->
	
---

## Dangers of derivatives trading

- Without proper risk management, derivatives trading can lead to significant losses. Here are some notable examples:

    - **Société Générale (2008)**: Jérôme Kerviel lost over \$7 billion by speculating on the future direction of equity indices. [Source](https://en.wikipedia.org/wiki/2008_Soci%C3%A9t%C3%A9_G%C3%A9n%C3%A9rale_trading_loss)
    - **UBS (2011)**: Kweku Adoboli lost \$2.3 billion by taking unauthorized speculative positions in stock market indices. [Source](https://en.wikipedia.org/wiki/2011_UBS_rogue_trader_scandal)
    - **Shell (1993)**: A single employee in the Japanese subsidiary of Shell lost \$1 billion in unauthorized trading of currency futures. [Source](https://www.nytimes.com/1993/02/26/business/worldbusiness/IHT-shell-gains-despite-currency-fiasco.html)
    - **Barings Bank (1995)**: Nick Leeson lost £827 million, leading to the bank's collapse. [Source](https://en.wikipedia.org/wiki/Barings_Bank)
    - **Long-Term Capital Management (1998)**: The hedge fund lost \$4.6 billion due to high-risk arbitrage trading strategies. [Source](https://en.wikipedia.org/wiki/Long-Term_Capital_Management)
    - **AIG (2008)**: AIG faced a liquidity crisis due to losses on credit default swaps, leading to a \$182 billion government bailout. [Source](https://en.wikipedia.org/wiki/AIG)

- Effective risk management is crucial:
    - Define risk parameters and set risk limits.
    - Conduct various scenario analyses to anticipate potential outcomes and mitigate risks.


---

## The OTC Market Prior to 2008

- The OTC market was largely unregulated.
- Banks acted as market makers, quoting bid and ask prices.
- Transactions between two parties were usually governed by master agreements provided by the International Swaps and Derivatives Association (ISDA).^[The ISDA is a trade organization of participants in the market for over-the-counter derivatives. ISDA has created a standardized contract (the ISDA Master Agreement) to govern derivative transactions, which helps to reduce legal and credit risks.]
- Some transactions were cleared through central counterparties (CCPs), which act as intermediaries between the two sides of a transaction, similar to an exchange.

---

## Changes Since 2008

- The OTC market has become more regulated with the following objectives:
    - Reduce systemic risk.
    - Increase transparency.
- In the U.S. and other countries, collateral and clearing of trades through a central clearing house (CCP) are required for all standard OTC contracts.
- CCPs must be used to clear standardized transactions between financial institutions in most countries.
- All trades must be reported to a central repository.

---

## The Lehman Bankruptcy 

- Lehman Brothers filed for bankruptcy on September 15, 2008, marking the largest bankruptcy in U.S. history.
- Lehman was heavily involved in the OTC derivatives markets and faced financial difficulties due to high-risk activities and an inability to roll over its short-term funding.
- The firm had hundreds of thousands of outstanding transactions with approximately 8,000 counterparties.
- The process of unwinding these transactions has been challenging for both Lehman's liquidators and their counterparties.

---

## Central Clearing

::: {style="text-align: center;"}
![](img/intro_centralclearing.png)
:::

<center>
<small>Source: [Bank for International Settlement](https://www.bis.org/publ/otc_hy2311.htm)</small>
</center>


---


## Who trades derivatives?

Derivatives are traded by various market participants:

- **Corporations**: Hedge future cash flows and manage risks (e.g., fuel futures for airlines).
- **Financial Institutions**: Manage risks and offer risk management solutions (e.g., interest rate swaps).
- **Hedge Funds**: Achieve higher returns through leverage and complex strategies.
- **Market Makers (Dealers)**: Provide liquidity and profit from bid-ask spreads.
- **Financial Engineers**: Design new derivative products to meet specific needs.

Each participant contributes to the market's depth and liquidity.



# Measures of Return and Risk


---


## Simple Return

Suppose a stock price evolves as follows:




::: {.cell}

```{.r .cell-code}
P0 <- 100
P1 <- 110
P2 <- 100

R_t <- P1 / P0
r_t <- (P1 - P0) / P0
log_return <- log(P1 / P0)

list(GrossReturn = R_t, NetReturn = r_t, LogReturn = log_return)
```

::: {.cell-output .cell-output-stdout}

```
$GrossReturn
[1] 1.1

$NetReturn
[1] 0.1

$LogReturn
[1] 0.09531018
```


:::
:::




---

## Compounded Return

If a bond pays 10% semiannually, its compounded return is:

$$
\left( 1+ \frac{r}{k} \right)^k -1 
$$

Continuously compounded return:

$$
\lim_{k \rightarrow \infty} \left( 1+ \frac{r}{k} \right)^k - 1 = e^r -1 
$$

In R:




::: {.cell}

```{.r .cell-code}
r <- 0.10
compounded_return <- (1 + r / 2)^2 - 1
continuously_compounded <- exp(r) - 1
list(CompoundedReturn = compounded_return, ContinuousReturn = continuously_compounded)
```

::: {.cell-output .cell-output-stdout}

```
$CompoundedReturn
[1] 0.1025

$ContinuousReturn
[1] 0.1051709
```


:::
:::




What is the equivalent c.c. return of Bond XYZ?
$$
e^r = \left( 1+ \frac{10\%}{2} \right)^2
$$
$$
r =  \ln \left( 1+ \frac{10\%}{2} \right)^2 = \ln \frac{P_1}{P_0} = 9.758\%
$$

---

## Multi-Period Return

Again, suppose $P_0=100$, $P_1=110,$ and $P_2=100$. 2-year gross return is

$$
R(0,2) = \frac{P_2}{P_0} 
$$ 

2-year gross return using 1-year return:

$$
R(0, 2) = \frac{P_2}{P_0} = \frac{P_1}{P_0} \frac{P_2}{P_1} =  R(0,1)R(1,2)
$$

cf. Log returns


---

## Annualization

Typically, returns are expressed as an annual return for comparison.

Monthly return 1% for 12 months: 

$$
r = (1+ 0.01)^{12} -1
$$ 

A two-year return 10%:
\begin{align*}
&(1+r_1)(1+r_2) = 1.1 \\
&\text{Set  } r_1 = r_2 = r \\
&(1+r)^2 = 1.1 \Rightarrow r= (1.1)^{1/2} -1 = 4.89\%
\end{align*}

In general, an annualized return $=(1+r_c)^{(365/Days)}-1$, where $r_c$ is the cumulative (holding-period) return, i.e., $P_t/P_0-1$.




---

## Arithmetic vs. Geometric Average Return

- Arithmetic Mean Return:

$$
r_{AM} = \frac{(r_1+r_2+\dots+r_T)}{T}
$$

- Geometric Mean Return:

$$
r_{GM} = \left[ (1+r_1)(1+r_2)\dots(1+r_T)\right]^{1/T}-1
$$

In R:




::: {.cell}

```{.r .cell-code}
returns <- c(0.05, 0.10, -0.02, 0.07)
mean_arith <- mean(returns)
mean_geom <- prod(1 + returns)^(1/length(returns)) - 1
list(ArithmeticMean = mean_arith, GeometricMean = mean_geom)
```

::: {.cell-output .cell-output-stdout}

```
$ArithmeticMean
[1] 0.05

$GeometricMean
[1] 0.04905428
```


:::
:::




---

## Arithmetic vs. Geometric Average Return

- Fact 1: $r_{AM} \ge r_{GM}$

- Fact 2: The greater the volatility of returns, the greater $r_{AM} - r_{GM}$

- Typically, use $r_{AM}$ as a proxy for the expected return.

---

## Expected Return

- The probability weighted average return

- In population (when we know the probability function),
  - Discrete: $E(r) = \sum_{i=1}^{n} P(r_i) r_i$ 
  - Continuous: $E(r) = \int_{-\infty}^{+\infty} r f(r) dr$
    - $E(ar_1+br_2) = aE(r_1)+bE(r_2)$

- In sample (when we only observe history),
  - $\overline{X} = \frac{\sum_{i=1}^{N}x_i}{N}$


---

## Expected Return

- The expected return is the probability-weighted average of all possible returns.

- In practice, the true probability distribution of returns is often unknown (i.e., from the future). Therefore, we estimate it using historical data.

- Typically, we use the arithmetic average of historical returns to estimate the expected return.
  - Law of Large Numbers: If $X_i$'s are independent and identically distributed (i.i.d) with mean $\mu$, then $\frac{1}{N}\sum_{i=1}^{N} X_i \rightarrow \mu$ as $N$ approaches infinity.

- The higher the risk, the greater the required rate of return. In equilibrium, the required rate of return should be equal to the expected return.



---

## Risk: Variance/Standard Deviation

- Measures the degree of dispersion of return (around its mean)

**In population**

- $Var(r) = \sigma^2 = E[(r-E(r))^2] = E(r^2)-E(r)^2$
  - $\sigma(r) = \sqrt{var(r)}$
  - $Var(ar) = a^2 Var(r)$
  - $Var(ar_1 + br_2) = a^2 Var(r_1) + b^2 Var(r_2) + 2ab Cov(r_1, r_2)$

**In sample**

- $s^2 = \hat{\sigma}^2 = \frac{\sum_{i=1}^{N}(x_i - \overline{X})^2}{N-1}$

**Note**

- $Cov(X,Y) = E[(X-E(X))(Y-E(Y))] = E(XY) - E(X)E(Y)$
  - Correlation: $\rho = cov(X,Y)/\sigma(X)\sigma(Y)$, $-1 \le \rho \le +1$
  - $Cov(aX+b, eY+f) = ae Cov(X,Y)$
  - $Cov(X+Y, Z) = Cov(X,Z) + Cov(Y,Z)$




---

## The Reward-to-Volatility (Sharpe) Ratio


$$
\frac{E(r) - r_f}{\sigma}
$$

Example in R:




::: {.cell}

```{.r .cell-code}
# Load necessary libraries
library(quantmod)
library(PerformanceAnalytics)

# Load Tesla (TSLA) stock data from Yahoo Finance
getSymbols("TSLA", src = "yahoo", from = "2015-01-01", to = Sys.Date(), auto.assign = TRUE)
```

::: {.cell-output .cell-output-stdout}

```
[1] "TSLA"
```


:::

```{.r .cell-code}
# Compute daily returns and remove missing values
tsla_returns <- na.omit(dailyReturn(Cl(TSLA)))

# Compute annualized return and standard deviation
annualized_return <- Return.annualized(tsla_returns, geometric = TRUE)
annualized_std_dev <- sd(tsla_returns) * sqrt(252)  # Convert daily std to annualized

# Get the latest 3-month Treasury Bill (IRX) as risk-free rate
getSymbols("^IRX", src = "yahoo", from = Sys.Date() - 30, to = Sys.Date(), auto.assign = TRUE)
```

::: {.cell-output .cell-output-stdout}

```
[1] "IRX"
```


:::

```{.r .cell-code}
risk_free_rate <- as.numeric(last(Cl(IRX))) / 100  # Convert from percentage

# Compute Sharpe Ratio (Annualized)
sharpe_ratio <- (annualized_return - risk_free_rate) / annualized_std_dev
sharpe_ratio
```

::: {.cell-output .cell-output-stdout}

```
                  daily.returns
Annualized Return     0.5105525
```


:::
:::




- Risk premium: $E(r) - r_f$ vs. Excess return: $r- r_f$.


---
	
## Normal Distribution

- We commonly assume that returns are normally distributed, $N(\mu, \sigma^2)$





::: {.cell layout-align="center"}
::: {.cell-output-display}
![](chapter_intro_files/figure-revealjs/unnamed-chunk-5-1.png){fig-align='center' width=960}
:::
:::





---

## Normal Distribution

- Probability distribution function, \(N(\mu, \sigma^2)\)

$$
f(x) = \frac{1}{\sqrt{2\pi} \sigma}e^{-\frac{(x-\mu)^2}{2\sigma^2}}
$$

- Standard normal, \(N(0,1) \equiv \phi\)

$$
f(x) = \frac{1}{\sqrt{2\pi} }e^{-\frac{r^2}{2}}
$$

- If $Z \sim \phi(0,1)$, then $X=\mu + \sigma Z \sim N(\mu,\sigma^2)$

- If $X \sim N(\mu_X,\sigma^2_X)$ and $Y \sim N(\mu_Y,\sigma^2_Y)$, then $X+Y \sim N(\mu_X+\mu_Y,\sigma^2_X +\sigma^2_Y +2cov(X,Y))$

---


## Standard Normal Random Variables

- Consider a normal random variable $R$ with  $\mu=0$ and $\sigma=1$. In other words, $R \sim N(0,1)$. We call it a standard normal random variable.
- Suppose that we want to find the probability that $R$ is lower than $x$. Graphically, this probability is the shadowed area in the figure below:




::: {.cell layout-align="center"}
::: {.cell-output-display}
![](chapter_intro_files/figure-revealjs/unnamed-chunk-6-1.png){fig-align='center' width=1920}
:::
:::




---

## Standard Normal Random Variables

- To find this probability, we calculate

    $$
    \text{Prob}(R \leq x) = \int_{-\infty}^x \frac{1}{\sqrt{2\pi}} e^{-\frac{r^2}{2}}dr \equiv \Phi(x).
    $$
    $\Phi(x)$ is called the cumulative probability distribution function for a standard normal random variable.
- For any $x$, the value of $\Phi(x)$ can be found using the excel function, \emph{norm.s.dist}(x, TRUE).

---

## Standard Normal Random Variables

- ***Ex.1*** Suppose that $R_1 \sim \phi (0,1)$. What is the probability that $R_1$ is larger than 1?




::: {.cell}

```{.r .cell-code}
prob_R1 <- 1 - pnorm(1, mean = 0, sd = 1)
cat("P(R1 > 1) =", prob_R1, "\n")
```

::: {.cell-output .cell-output-stdout}

```
P(R1 > 1) = 0.1586553 
```


:::
:::




- ***Ex.2*** Suppose that $R_2 \sim \phi (0.1, 0.2)$. What is the probability that $R_2$ is equal to or smaller than 0.5?




::: {.cell}

```{.r .cell-code}
prob_R2 <- pnorm(0.5, mean = 0.1, sd = 0.2)
cat("P(R2 ≤ 0.5) =", prob_R2, "\n")
```

::: {.cell-output .cell-output-stdout}

```
P(R2 ≤ 0.5) = 0.9772499 
```


:::
:::





---

## Historic vs. Normal Distribution

- Historical returns often deviate from the normal distribution.
- Empirical distributions can exhibit skewness and kurtosis (fat tails).




::: {.cell layout-align="center"}
::: {.cell-output .cell-output-stdout}

```
[1] "TSLA"
```


:::

::: {.cell-output-display}
![](chapter_intro_files/figure-revealjs/unnamed-chunk-9-1.png){fig-align='center' width=960}
:::
:::




---

## Log-Normal Distribution

- $X \sim LN(\mu, \sigma^2)$ if $\ln(X) \sim N(\mu, \sigma^2)$

- If a rate of return is normally distributed, security prices follow lognormal distribution.
  - $\text{log-return}= \ln R_t = \ln \frac{P_t}{P_{t-1}} = \ln P_t - \ln P_{t-1} \sim N(\cdot)$


::: {.aside}
- By the way,
  - $E(X) = e^{\mu + \sigma^2/2}$. In fact $E(X^n) = e^{n\mu + n^2\sigma^2/2}$
  - $Var(X) = E(X^2)- E(X)^2 = e^{2\mu + 2\sigma^2} - e^{2\mu + \sigma^2} = e^{2\mu + \sigma^2}(e^{\sigma^2}-1)$
:::

---

## Risk Measures

- Companies must assess and manage risks to avoid business failures.
- To understand the risk level of a project or business, we can analyze the probability distribution of possible outcomes.
- Several risk measures are commonly used:
    - Standard Deviation
    - Value at Risk (VaR)
    - Expected Shortfall
    - $\cdots$
- Each measure focuses on different aspects of the distribution.


---

## Standard Deviation

- Standard deviation measures the level of uncertainty about the outcomes, or the dispersion of probability distribution.

- The larger standard deviation is, the riskier a project.

- A disadvantage of the standard deviation is that it cannot distinguish between upside and downside movement.

---

## Value at Risk

- Value at Risk (VaR) is intended to focus on downside risk of the distribution.
- VaR is the estimate of the losses that occur with a given probability.
    - ***e.g.*** How much loss we might have on our portfolio such that there is only a 5\% chance that we will do worse?


::: {style="text-align: center;"}
![](img/intro_var1.png){width=50%}
:::

- That is, we want to find $X$ such that
  
$$
\text{Prob}\left( R \leq X \right) = 0.05
$$

---

## Value at Risk

- How can we find $X$ satisfying $\Pr\left(R \leq X \right) = 0.05$, i.e., 95\% VaR? 
- In a special case when $R \sim \phi( \mu,\sigma )$, we can find $X$ using the Excel function  `norm.inv()`.
    - For given $1-p$, `norm.inv(1-p, mean, sigma)` is $X$ that satisfies $\text{Prob}\left(R \leq X \right) = 1-p$.
        - VaR at 5\% =  `norm.inv(0.05,0,1) = -1.645` 

        (R: `qnorm(0.05, mean = 0, sd = 1)`)

        - VaR at 10\% =  `norm.inv(0.1,0,1) = -1.282` 

        (R: `qnorm(0.10, mean = 0, sd = 1)`)


    

---

## Value at Risk - Example I

- Suppose we own a stock whose return is normally distributed with a mean of 15% and a standard deviation of 30%. What is the 5% Value at Risk (VaR) for this stock?

    ***Answer:*** Let $X$ denote the 5% VaR. Then, $\Pr(R \le X) = \texttt{norm.inv}(0.05, 0.15, 0.30) = -34.3\%$
    
    Alternatively,
    \begin{align*}
        \text{Prob}\left(R \leq X \right) = \text{Prob}\left( \frac{R - 0.15}{0.3} \leq \frac{X - 0.15}{0.3} \right) = 0.05
    \end{align*}
    Note that $\frac{R - 0.15}{0.3} \sim \phi(0,1)$, so we can write
    $$
    \frac{X - 0.15}{0.3} = \texttt{norm.s.inv}(0.05) = -1.645.
    $$
    Thus, $X = -34.3\%$.

---

## Value at Risk - Example II

- ***Q.*** A portfolio worth \$10 million has a 1-day standard deviation of \$200,000 and an approximate mean of zero. Assume that the change is normally distributed. What is the 1-day 99% VaR for our portfolio consisting of a \$10 million position in Microsoft? What is the 10-day 99% VaR?
    
    ***Answer:*** $\texttt{norm.s.inv(0.01)} = -2.326$, meaning that there is a 1% probability that a normally distributed variable will decrease in value by more than 2.326 standard deviations.
    
    Hence, the 1-day 99% VaR is $2.326 \times \$200,000 = \$465,300$.
    
    The 10-day 99% VaR is $2.326 \times (\$200,000 \times \sqrt{10}) = \$1,471,300$.
    

---


## Value at Risk - Multiple Stocks

- Consider a portfolio consisting of ***n*** different stocks.
- The return on the portfolio is
    $$
    R_p = \sum_{i=1}^n w_i R_i
    $$
    where $w_i$ is the fraction of wealth invested in stock $i$.
- If each stock return is normally distributed, then the portfolio return is also normally distributed.

---

## Value at Risk - Multiple Stocks

- ***Ex.*** Consider a portfolio consisting of stock A and stock B. In the portfolio, \$5 million are invested in each of stock A and stock B. The return on each stock is normally distributed. Stock A has an expected return of 15% and a standard deviation of 30%. Stock B has an expected return of 18% and a standard deviation of 45%. The correlation between stock A and stock B is 0.4. What is the 10% VaR for the portfolio?
    - \textbf{Note:} When $X \sim \phi(\mu_x, \sigma_x^2)$ and $Y \sim \phi(\mu_y, \sigma_y^2)$, then $X + Y \sim \phi(\mu_x + \mu_y, \sigma_x^2 + \sigma_y^2 + 2\rho\sigma_x\sigma_y)$

    ***Answer:*** 
    - The expected return of the portfolio is:
    $$
    \mu_p = 0.5 \times 0.15 + 0.5 \times 0.18 = 0.165 \text{ or } 16.5\%
    $$
    - The standard deviation of the portfolio is:
    $$
    \sigma_p = \sqrt{(0.5 \times 0.30)^2 + (0.5 \times 0.45)^2 + 2 \times 0.5 \times 0.5 \times 0.4 \times 0.30 \times 0.45} = 0.315 \text{ or } 31.5\%
    $$
    - The 10% VaR for the portfolio is:
    $$
    \text{VaR}_{10\%} = \mu_p + \sigma_p \times \texttt{norm.s.inv}(0.10) = 0.165 + 0.315 \times (-1.282) = -0.239 \text{ or } -23.9\%
    $$
    - Therefore, the 10% VaR for the \$10 million portfolio is:
    $$
    10,000,000 \times 0.239 = \$2,390,000
    $$



---

## Value at Risk - Historical Data

- We can also calculate the VaR using historical data without assuming a specific distribution.
- For example, let's consider 1-year-long historical data of daily returns for a stock price index.
- We aim to estimate the 5% VaR for the next day's return.
- To do this, we assume that the next day's return will be similar to one of the past year's returns.
- The 5% VaR is then the 5th percentile of these historical returns.

---

## Value at Risk - Some Issues I

- VaR estimation is based on the assumption that the distribution of future return is the same as (at least similar to) the distribution of past return.
- This assumption may not hold in the real world.




::: {.cell layout-align="center"}
::: {.cell-output .cell-output-stdout}

```
[1] "KS200"
```


:::

::: {.cell-output-display}
![](chapter_intro_files/figure-revealjs/unnamed-chunk-10-1.png){fig-align='center' width=960}
:::
:::




---

## Value at Risk - Some Issues II

- VaR specifies the ***minimum*** loss that will occur with a given probability.
- VaR tells nothing about the expected magnitude of the loss.
- Which is the better between the following two?

:::: {.columns}
::: {.column width="50%"}
::: {style="text-align: center;"}
![](img/intro_var1.png)
:::
:::
::: {.column width="50%"}
::: {style="text-align: center;"}
![](img/intro_var2.png)
:::
:::
::::


---

## Expected Shortfall

- ***Expected Shortfall*** is another measure to address the shortcoming of VaR.
    - It asks ***"If things get bad, what is the expected loss?"***
- Suppose that we focus on the loss that will happen with 5% probability. Let ***V*** denote the 5% loss (VaR). Then,
    $$
    \text{Expected shortfall} = E\left(R | R \leq V \right)
    $$

- Also known as Conditional Value at Risk (CVaR)


:::{.aside}
- Under normal distribution: $\text{ES} = \mu - \sigma \frac{\phi((V-\mu)/\sigma)}{\Phi((V-\mu)/\sigma)}$
:::

---

## Expected Shortfall

- Once historical data are given, we can compute the expected shortfall.
    - In Excel, use ***"averageif()"***.
- ***Ex.*** Let's use the 1-year-long data of daily returns on a stock index.
    - ***Q1.*** What is the expected shortfall with 5% probability?
    - ***Q2.*** What is the expected shortfall with 10% probability?



## Value at Risk and Expected Shortfall




::: {.cell}
::: {.cell-output .cell-output-stdout}

```
[1] "PLTR"
```


:::

::: {.cell-output .cell-output-stdout}

```
90% Historical VaR: -0.044821 
```


:::

::: {.cell-output .cell-output-stdout}

```
90% Expected Shortfall: -0.069202 
```


:::

::: {.cell-output-display}
![](chapter_intro_files/figure-revealjs/unnamed-chunk-11-1.png){width=960}
:::
:::




---

## Application: Bank Regulation

- VaR and ES are widely used in the financial industry to measure and manage risk.
- The Basel Committee on Banking Supervision (BCBS) provides global banking regulations.
- Key frameworks include:
    - **1996 Amendment**: Required capital = ***k \times VaR (1\%, 10 days)***, where ***k \ge 3***.
    - **Basel II (2007)**: Suggested ***VaR(0.1\%, 1-year)*** for risk assessment.
    - **Basel IV (2021)**: Recommended 97.5% expected shortfall (ES) for a comprehensive risk view.

