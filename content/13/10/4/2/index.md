---
linkTitle: "10.4.2 Writing Call Options"
title: "Writing Call Options: Covered and Naked Strategies Explained"
description: "Explore the intricacies of writing call options, including covered and naked strategies, their risks, and practical examples within the Canadian financial landscape."
categories:
- Derivatives
- Options Trading
- Canadian Securities
tags:
- Call Options
- Covered Calls
- Naked Calls
- Risk Management
- Canadian Market
date: 2024-10-25
type: docs
nav_weight: 1042000
---

## 10.4.2 Writing Call Options

Writing call options is a sophisticated strategy used by investors to generate income or hedge against potential price movements in the underlying asset. This section delves into the two primary strategies for writing call options: covered calls and naked calls. We will explore their mechanics, risks, and practical applications, particularly within the Canadian financial context.

### Covered Calls

A covered call strategy involves writing (selling) call options while simultaneously owning the equivalent amount of the underlying asset. This strategy is often employed by investors who seek to generate additional income from their existing stock holdings. By writing a call option, the investor receives a premium, which can enhance overall returns.

#### How Covered Calls Work

When an investor writes a covered call, they agree to sell the underlying asset at a specified price (the strike price) if the option is exercised by the buyer. The ownership of the underlying asset "covers" the obligation to deliver the shares, thereby limiting the risk associated with the strategy.

**Example of Covered Call Writing:**

Consider an investor who owns 100 shares of Royal Bank of Canada (RBC), currently trading at $100 per share. The investor writes a call option with a strike price of $105, expiring in one month, and receives a premium of $2 per share. 

- **Scenario 1:** If RBC's stock price remains below $105, the option will likely expire worthless, and the investor retains the premium of $200 (100 shares x $2).
- **Scenario 2:** If RBC's stock price rises above $105, the option may be exercised. The investor will sell the shares at $105, realizing a gain from the stock appreciation plus the premium received.

In both scenarios, the premium provides a buffer against minor price declines or stagnation, enhancing the investor's overall return.

### Naked Calls

Writing naked calls involves selling call options without owning the underlying asset. This strategy is inherently riskier than covered calls because the writer does not have the asset to deliver if the option is exercised. As a result, the potential for loss is theoretically unlimited if the asset's price rises significantly.

#### Risks of Naked Calls

The primary risk of writing naked calls is the obligation to purchase the underlying asset at the current market price to fulfill the option contract if exercised. This can lead to substantial losses if the asset's price surges beyond the strike price.

**Example of Naked Call Writing:**

Imagine an investor writes a naked call option for 100 shares of Toronto-Dominion Bank (TD), with a strike price of $80, while TD is trading at $75. The investor receives a premium of $1.50 per share.

- **Scenario:** If TD's stock price unexpectedly rises to $90, the option holder will likely exercise the option. The writer must purchase the shares at $90 to sell them at $80, incurring a loss of $8.50 per share ($90 - $80 + $1.50 premium), totaling a $850 loss for 100 shares.

This example illustrates the significant risk associated with naked calls, emphasizing the importance of risk management and market awareness.

### Glossary

- **Covered Call:** Writing a call option while holding an equivalent amount of the underlying security. This strategy limits risk and generates income from premiums.
- **Naked Call:** Writing a call option without holding the underlying security. This strategy carries high risk due to the potential for unlimited losses if the asset's price rises.

### Practical Considerations and Best Practices

When engaging in call writing strategies, investors should consider the following best practices:

- **Risk Assessment:** Evaluate the risk tolerance and financial goals before choosing between covered and naked calls.
- **Market Analysis:** Conduct thorough market analysis to anticipate potential price movements and adjust strategies accordingly.
- **Regulatory Compliance:** Ensure compliance with Canadian financial regulations and understand the tax implications of option trading.
- **Diversification:** Use call writing as part of a diversified investment strategy to mitigate risks.

### Conclusion

Writing call options can be a powerful tool for generating income and managing risk within an investment portfolio. By understanding the mechanics and risks of covered and naked calls, investors can make informed decisions that align with their financial objectives. As with any investment strategy, due diligence and continuous learning are essential to success in the dynamic world of options trading.

## Quiz Time!

{{< quizdown >}}

### What is a covered call?

- [x] Writing a call option while holding the underlying asset
- [ ] Writing a call option without holding the underlying asset
- [ ] Buying a call option while holding the underlying asset
- [ ] Selling a call option without any asset

> **Explanation:** A covered call involves writing a call option while owning the equivalent amount of the underlying security, which covers the obligation to deliver the shares if exercised.

### What is the primary risk of writing naked calls?

- [x] Unlimited potential losses if the asset's price rises
- [ ] Limited gains if the asset's price falls
- [ ] No risk involved
- [ ] Guaranteed profits

> **Explanation:** Writing naked calls carries the risk of unlimited potential losses because the writer does not own the underlying asset and must purchase it at the market price if the option is exercised.

### In a covered call strategy, what happens if the stock price remains below the strike price?

- [x] The option expires worthless, and the writer keeps the premium
- [ ] The writer must sell the stock at a loss
- [ ] The writer incurs a loss equal to the premium
- [ ] The writer must buy more stock

> **Explanation:** If the stock price remains below the strike price, the option will likely expire worthless, allowing the writer to keep the premium received.

### What is the potential loss for a naked call writer if the stock price rises significantly?

- [x] Unlimited
- [ ] Limited to the premium received
- [ ] Zero
- [ ] Limited to the strike price

> **Explanation:** The potential loss for a naked call writer is unlimited because they may have to purchase the underlying asset at a much higher market price to fulfill the option contract.

### Which strategy involves less risk: covered calls or naked calls?

- [x] Covered calls
- [ ] Naked calls
- [ ] Both have the same risk
- [ ] Neither involves risk

> **Explanation:** Covered calls involve less risk because the writer owns the underlying asset, which covers the obligation to deliver shares if the option is exercised.

### What is the primary goal of writing covered calls?

- [x] Generating additional income from premiums
- [ ] Speculating on stock price declines
- [ ] Avoiding taxes
- [ ] Increasing stock holdings

> **Explanation:** The primary goal of writing covered calls is to generate additional income from the premiums received while holding the underlying asset.

### How can an investor mitigate the risks of writing naked calls?

- [x] By conducting thorough market analysis
- [ ] By ignoring market trends
- [ ] By writing more naked calls
- [ ] By avoiding diversification

> **Explanation:** Conducting thorough market analysis helps investors anticipate price movements and adjust strategies to mitigate the risks associated with writing naked calls.

### What happens if a covered call is exercised?

- [x] The writer sells the underlying asset at the strike price
- [ ] The writer buys more of the underlying asset
- [ ] The writer incurs a loss equal to the premium
- [ ] The option expires worthless

> **Explanation:** If a covered call is exercised, the writer sells the underlying asset at the strike price, fulfilling the obligation of the option contract.

### Why is it important to understand Canadian financial regulations when writing call options?

- [x] To ensure compliance and understand tax implications
- [ ] To avoid paying premiums
- [ ] To guarantee profits
- [ ] To increase market volatility

> **Explanation:** Understanding Canadian financial regulations is crucial for ensuring compliance and understanding the tax implications of option trading.

### True or False: Writing call options is a risk-free strategy.

- [ ] True
- [x] False

> **Explanation:** Writing call options is not risk-free. Covered calls involve limited risk, while naked calls carry significant risk due to the potential for unlimited losses.

{{< /quizdown >}}
