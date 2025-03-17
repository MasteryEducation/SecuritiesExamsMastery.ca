---
title: "Adding and Deleting Option Classes"
description: "A practical look at how exchanges determine which underlying securities get listed as option classes, including the listing criteria, the review process, and the steps to remove under-traded options for market efficiency."
linkTitle: "28.3 Adding and Deleting Option Classes"
date: 2025-02-07
type: docs
nav_weight: 28300
license: "© 2024 Tokenizer Inc. CC BY-NC-SA 4.0"
---

## 28.3 Adding and Deleting Option Classes

So, picture this: you’re at the Bourse de Montréal, or any major options exchange, and you’re just itching to see a brand-new stock (or maybe an ETF) hit the options market. There’s always a bit of buzz when a fast-growing or highly anticipated company is about to be listed for option trading—like that time a certain electric car maker got listed and volumes just went through the roof. Exchanges don’t make the decision to list new classes on a whim; they have specific criteria, procedures, and—believe it or not—lots of regulatory checks. And on the flip side, if a once-popular underlying loses its sparkle, the exchange might decide to quietly say, “Okay, folks, we’re delisting these options.” Let’s dive into how this all works and why it matters.

### Understanding the Underlying Security and the Option Class

When we talk about “option classes,” we basically mean all the calls and puts on the same underlying security—be that a stock, ETF, index, or something else. For instance, if we say “options on Maple Leaf Tech Corp,” that entire universe of calls and puts for Maple Leaf Tech is one option class. Exchanges are tasked with evaluating the demand, liquidity, and compliance of that class. If demand is steady and the underlying meets certain benchmarks, that class will likely stay. If demand wanes and the underlying or the class no longer meets the exchange’s listing criteria, well, it might be time for a goodbye.

#### Why Bother with Listing Criteria?

You might wonder: Why don’t exchanges just list every single stock under the sun for options? After all, more products can mean more trading, right? But listing an option class that has no real buyer or seller interest is a bit like opening a coffee shop in the middle of nowhere. You need enough foot traffic—sufficient trading volume, a broad float of shares, a stable share price—something to ensure people actually show up to trade. Market integrity depends in part on maintaining a critical mass of liquidity so that prices remain fair, spreads stay tight, and you can slip in and out of trades without drama.

### Key Listing Criteria

Each exchange has its own guidelines, but broadly speaking, they’ll look at factors such as:

- Minimum Company Market Capitalization: The underlying stock’s market cap is often required to be over a certain threshold.  
- Minimum Share Price: A baseline share price (e.g., often around CAD$2 or $3 on some exchanges) must be maintained for a period of time.  
- Sufficient Float: A meaningful portion of the company’s shares should be freely tradable in the market.  
- Adequate Trading Volume: The underlying typically needs to meet certain average daily trading volumes.  
- Corporate Governance & Regulatory Compliance: The company must be in good standing with relevant regulatory authorities.

For example, the Bourse de Montréal (often abbreviated as “the Bourse”) posts listing requirements on its official website (https://www.m-x.ca/). They evaluate not just the raw data about an underlying’s trading volume but also the nature of that underlying’s volatility profile, public share ownership, and, occasionally, broad market sentiment.

### The Process of Adding a New Option Class

Let’s say a new stock has just rocketed to popularity—maybe it’s a Canadian biotech firm that soared 300% in a month. Unsurprisingly, investors and traders start clamoring: “We want to hedge! We want to speculate with options!” The process might look like this:

1. Initial Review: The exchange’s product management team gets wind of the interest and checks the stock’s metrics (price, volume, float, corporate governance, etc.).  
2. Exchange Listing Decision: If it meets or exceeds each criterion, the exchange can proceed.  
3. Regulatory Approval: Exchanges often have to notify or obtain clearance from CIRO. CIRO, Canada’s current self-regulatory organization, ensures these new products are suitable for the market and that investor protection measures remain solid.  
4. Clearing Corporation Coordination: The Canadian Derivatives Clearing Corporation (CDCC) also has to be looped in. CDCC makes sure that the clearing and settlement mechanics are properly in place.  
5. Market Maker Assignment: Often, the exchange will designate or invite a market maker to provide two-sided quotes for the new class.  
6. Launch and Public Notice: After final checks, the exchange will publicly announce (via bulletins or website notices) the listing of the new options, typically including details like strike prices, expiration cycles, and any special terms.

Below is a simple Mermaid.js diagram illustrating a typical workflow:

```mermaid
graph LR
    A["Potential Underlying Identified <br/> for Option Listing"]
    B["Initial Review by the Exchange"]
    C["Exchange Listing Decision"]
    D["Regulatory Approval (CIRO)"]
    E["Clearing Coordination (CDCC)"]
    F["Assignment of Market Maker"]
    G["Public Notice & Launch"]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G
```

I remember a case in 2018 when a Canadian cannabis stock blew up in popularity—people were practically begging for exchange-traded options for hedging and speculation. The Bourse weighed the hype against their listing criteria. Once it was greenlit (pun intended), the launch was quite the event. But in the end, the real success came from consistent volume and enough interest from both sides of the trade.

### Why Some Option Classes Get Deleted

Now, about delisting: it’s not necessarily as dramatic as it sounds. Occasionally, an underlying just fails to keep momentum. Maybe its share price drops well below the minimum requirement or it gets delisted from the main stock exchange. Or sometimes, after a corporate restructuring or a merger, the original security no longer exists in the same form. If the underlying goes away, the options inevitably must too.

In other instances:

- Consistently Low Trading Volume in the Option Class: If no one’s trading a particular option, it ties up exchange resources, confuses market participants, and offers limited price discovery.  
- Corporate Events: Mergers, acquisitions, or spin-offs can change the underlying dramatically.  
- Failing Listing Standards: If the underlying’s share price or market cap falls below the mandated threshold for an extended period, that can trigger a review.  
- Regulatory Action: Rarely, serious governance or regulatory infractions at the company level can force an option class removal.

### The Delisting Process

While every exchange has its unique approach, here’s a rough outline of how an option class might be delisted:

1. Monitoring and Review: The exchange continuously monitors average daily volume, open interest, underlying share price, and other liquidity measures for each option class.  
2. Warning Notices and Consultation: If the exchange sees that the class is on a downward trajectory of inactivity or no longer meets requirements, they generally notify the issuer (if relevant) or at least publish a notice that they’re considering delisting.  
3. Final Exchange Decision: The exchange decides on an effective date to halt new listings of that class. Existing open positions either continue until expiration or are closed.  
4. Regulatory Confirmation: The exchange may coordinate with CIRO to confirm there are no big concerns about ongoing positions or investor protections.  
5. Clearing Corporation Updates: The CDCC must ensure all open contracts can still be properly cleared. Typically, any in-the-money or open positions remain valid until expiry, but no new series might be created, or trading might freeze after the final notice.  
6. Announcement to the Public: A final bulletin or market notice is released. The class is removed from listing on the date indicated.

This process helps preserve market efficiency by freeing up resources and preventing confusion around stale or rarely traded products.

### Regulatory Approvals and Market Integrity

You won’t be surprised to learn that regulators keep a close watch on all this. In Canada, the newly established CIRO (since 2023) oversees investment dealers, market integrity, and more. The old IIROC and MFDA no longer exist separately—they’ve merged under this single SRO’s umbrella. The same goes for investor protection under CIPF, which merged with the MFDA’s Investor Protection Corporation.

In practice, if an exchange wants to add a flashy new option class or quietly remove a languishing one, CIRO might need to review or at least sign off on the decision. Their main question is always, “Is this in the best interest of market participants? Does this protect the investor and maintain a fair and orderly marketplace?”

### Coordinating with the Clearing Corporation (CDCC)

You can’t talk about listing or delisting without mentioning the Canadian Derivatives Clearing Corporation. The folks at CDCC handle margin requirements, settlement obligations, contract performance guarantees, and more. Whenever a new class is added, the clearing corporation’s systems need to get updated, parameters need to be set for margin calculations, and risk management frameworks need to consider the new product. It’s sort of like adding a new flavor at an ice cream distributorship: all channels have to be prepared and ready to handle it.

On the flip side, when an option class disappears, the clearing corporation updates its rosters. If you’re a participant holding a contract in that soon-to-be-gone class, the CDCC ensures you can still exercise or close your position in an orderly manner. Meanwhile, no new series get introduced. This helps keep the system stable and fair for everyone.

Try not to fret if you’re worried about losing your position when something is delisted—usually, final settlement or exercise terms remain valid through the last expiration cycle that was originally posted. The key is to watch for official bulletins or announcements regarding those final trading days.

### Practical Example: A Hypothetical Delisting

Imagine you have a firm called “Algonquin Microchips Inc.” that soared to stardom a couple of years ago, easily meeting listing requirements. But let’s say a competitor technology rendered microchips from Algonquin obsolete. The stock price tanks, daily volume shrivels, and the exchange sees open interest on the options basically vanish. At this point, the Bourse announces a “delisting review.” They might say, “Look, the average daily volume is below our threshold for three consecutive months, and the share price is now half of the minimum required.” They send out a consultation notice, and after hearing crickets from the marketplace (because nobody is trading these things), they coordinate with the CDCC to set a final trading day. By that date, any open interest has to be closed or exercised. Then the class is removed, never to be seen again unless the company miraculously rebounds and requalifies.

### Market Efficiency and Investor Implications

Delisting might scare some new traders—you might say, “Uh-oh, is the market going under?” Actually, in many cases it’s a sign of a healthy environment. A well-functioning market removes clutter. Illiquid options can lead to large bid-ask spreads and hamper price discovery. Delisting them ensures that most of the exchange’s resources focus on actively traded, robust products where folks can get in and out at fair prices.

When a new class is added, that can expand your opportunity set. Maybe you want to trade a fresh, innovative tech stock or hedge exposure to a brand-new ETF sector. The presence of new option classes can boost dynamism and give you more ways to manage risk or take positions. Meanwhile, the removal of dormant options helps keep things tidy.

### Best Practices and Pitfalls

For practitioners, this means:

• Stay Informed: Check exchange bulletins or subscription-based alert services, because the Bourse frequently posts their new listings or upcoming delistings.  
• Monitor Volume & Open Interest: If you hold an option on a security that’s losing steam, keep an eye on whether it might be delisted. You want to avoid being caught off-guard.  
• Understand Corporate Events: Mergers, spin-offs, or name changes can drastically alter the option listing landscape.  
• Consult Broker Tools or Analysis Platforms: Many open-source tools (R, Python libraries) let you track historical volume and open interest data. This can clue you in if an option you’re trading is about to wither or ramp up in popularity.  
• Communicate with the Clearing Corporation: In large institutional contexts, direct communication with clearing members can help you plan for pending changes.  
• Regulatory Notices: Keep an eye on CIRO’s website (https://www.ciro.ca) for any new derivative product approvals or changes to existing instructions.

### A Quick Glance at the Glossary

• **Underlying Security:** The stock, ETF, index, or other instrument that an option is derived from.  
• **Option Class:** A set of options (all calls and puts) on the same underlying security.  
• **Listing Criteria:** The qualifications (e.g., share price, market cap) a security must meet to have exchange-listed options.  
• **Float:** The number of shares available for public trading (excluding insider-held or restricted shares).  
• **Delisted:** Removed from trading on the exchange.  
• **Clearing Corporation:** The entity that clears trades, guaranteeing contract performance. In Canada, that’s CDCC for most exchange-traded derivatives.  
• **Market Efficiency:** The extent to which market prices reflect all information, facilitating a fair price discovery process.

### References and Further Reading

• Bourse de Montréal Listing Policies:  
  https://www.m-x.ca/  
• Canadian Derivatives Clearing Corporation (CDCC) – Listing and Clearing Procedures:  
  https://www.cdcc.ca/  
• CIRO Notices and Guidance:  
  https://www.ciro.ca  
• Open-Source Financial Tools:  
  – Python’s “pandas” and “NumPy” libraries for analyzing market data  
  – R’s “quantmod” package for charting and time-series analysis  
• Additional Reading on Derivatives Market Structure:  
  – Hull, John. “Options, Futures, and Other Derivatives.”  
  – Official bulletins from Bourse de Montréal for real-time listing changes  

---

Anyway, that’s the broad strokes on how options exchanges decide whether to add or remove an option class. On the addition side, they’re weighing demand, liquidity, and compliance. On the removal side, they’re safeguarding the market from deadweight and inefficiency. Both ensure a more vibrant, relevant market. So the next time you see a press release that your favorite rising star stock (or sector ETF!) is getting new options, you’ll know exactly why it’s happening—and how.

## Sample Exam Questions: Adding and Deleting Option Classes

{{< quizdown >}}

### Which of the following factors is considered by an exchange when deciding to add a new option class?

- [ ] Whether the issuer’s CEO is a celebrity
- [x] The average daily trading volume of the underlying
- [ ] The client’s personal investment history
- [ ] The number of recent short sellers

> **Explanation:** Exchanges look at tangible, market-based metrics (e.g., trading volume, market cap, liquidity) rather than subjective details like personal history or the celebrity status of the CEO.

### What is the primary reason exchanges remove option classes with very low trading volume?

- [x] To streamline market efficiency
- [ ] To protect the company’s reputation
- [ ] To punish short sellers
- [ ] To eliminate arbitrage opportunities

> **Explanation:** Minimal activity in an option class often leads to poor liquidity and widened spreads, harming price discovery. Removing these listings maintains an orderly and efficient market.

### When a merger causes the underlying company to cease to exist, what typically happens to the option class associated with that stock?

- [x] It is delisted or closed out by the exchange
- [ ] It is converted into index options
- [ ] It is automatically assigned new strikes
- [ ] It remains listed indefinitely

> **Explanation:** If the underlying no longer exists, the associated option class cannot continue to trade. Exchanges coordinate with clearing houses to close out or settle existing positions.

### Which entity in Canada is responsible for overseeing new product approvals for options?

- [ ] The former IIROC
- [ ] The former MFDA
- [x] CIRO
- [ ] CIPF

> **Explanation:** Since the amalgamation of IIROC and MFDA, CIRO is now the single self-regulatory organization responsible for approving new derivative products and overseeing market integrity.

### Which of the following best describes “float” in the context of listing criteria for a new option class?

- [x] The number of shares available for public trading 
- [ ] The difference between call and put options
- [ ] The distribution of strike prices
- [ ] The time between stock dividend payments

> **Explanation:** An underlying’s float refers to the total number of shares that are publicly available to trade, which impacts liquidity and eligibility for option listing.

### Which clearing entity in Canada ensures proper settlement of newly listed option classes?

- [ ] CIPF
- [x] CDCC
- [ ] The New York Stock Exchange
- [ ] The Securities and Exchange Commission

> **Explanation:** The Canadian Derivatives Clearing Corporation (CDCC) is the clearing agency that guarantees contract performance, settling all trades executed on Canadian derivatives exchanges.

### What is the impact on open interest when an option class is delisted?

- [x] Existing positions can often be held until they expire
- [ ] All contracts are immediately canceled
- [ ] All existing positions must be exercised immediately
- [ ] The exchange automatically transfers these positions to a similar underlying

> **Explanation:** Typically, no new series are listed after the delisting announcement, but existing open interest remains valid until contract expiration or final settlement.

### Why would a brand-new company with a very low share price be less likely to have option classes listed?

- [ ] Exchanges prefer high volatility underlying
- [ ] Retail investor demand is usually absent
- [x] It may fail minimum share price or market criteria for listing
- [ ] It costs too much to create new symbols

> **Explanation:** Most exchanges require a minimum share price and other liquidity-related benchmarks that low-priced or newly formed companies may fail to meet.

### Which of the following best explains the role of CIRO when an exchange adds new option classes?

- [ ] CIRO executes the trades
- [x] CIRO reviews and oversees regulatory compliance
- [ ] CIRO acts as a counterparty to all trades
- [ ] CIRO sets the share price of the underlying

> **Explanation:** CIRO is Canada’s self-regulatory organization that supervises activities of registered dealers and ensures new derivative products meet investor protection and market integrity standards.

### True or False: When an option class is scheduled to be removed, market participants must close all positions immediately.

- [ ] True
- [x] False

> **Explanation:** Typically, open interest can be maintained until expiration, but no new series or contracts are created. The position holders are usually allowed time to unwind or exercise existing contracts if they remain in effect.

{{< /quizdown >}}
