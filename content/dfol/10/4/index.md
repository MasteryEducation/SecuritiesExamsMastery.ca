---
title: "Pricing an Interest Rate Swap"
description: "A comprehensive guide to interest rate swap valuation in Canada, exploring fundamental concepts, discounting cash flows, and real-world applications under the CIRO regulatory landscape."
linkTitle: "10.4 Pricing an Interest Rate Swap"
date: 2025-02-07
type: docs
nav_weight: 10400
license: "© 2024 Tokenizer Inc. CC BY-NC-SA 4.0"
---

## 10.4 Pricing an Interest Rate Swap

When I first encountered interest rate swaps, I’ll admit—I was totally baffled. My friend and I spent hours discussing how on earth traders nailed down that magical “fixed rate” so the initial value of the swap came out to zero. We were tossing around phrases like “discount factors,” “forward curves,” and "zero-coupon yields" and half the time I felt like we were speaking Martian. But after a while, it started to make sense, and I realized how practical and powerful these contracts could be in managing risk. Let’s pull back the curtain and take a thorough (but slightly relaxed) look at how a plain vanilla interest rate swap is priced, from building up the cash flows to applying discount rates from the appropriate yield curve.

### Why Does Swap Pricing Even Matter?

At its core, an interest rate swap lets two parties exchange sets of cash flows, usually a fixed rate for a floating rate. The reason we even bother “pricing” a swap is that swaps are contracts with future obligations, and each side has value—positive, negative, or zero—depending on current and expected future interest rates. At inception, a plain vanilla interest rate swap is typically set so that its initial value is close to zero. This is crucial for fairness: no one wants to start out in the hole or with an unfair advantage.

But over time, interest rates change, credit spreads change, even regulatory fees might change. All of this can push the swap’s value into positive or negative territory. Traders, hedge funds, corporations, and banks need to understand this value for things like daily margin calls, collateral requirements, or simple risk management decisions.

### Foundations of Swap Cash Flows

A vanilla interest rate swap typically consists of two legs:

• A fixed leg: one party pays a fixed interest rate (the “swap fixed rate”) on a notional principal.  
• A floating leg: the other party pays a floating interest rate (for example, CORRA in Canada, or sometimes LIBOR in older swaps, but that’s winding down globally).  

No principal amounts actually exchange hands at the start—they’re “notional.” Instead, each leg’s interest payment is calculated on the same notional. At each payment date (which might be quarterly, semi-annually, or annually), the difference between the two legs is exchanged.

Below is a simplified diagram to show the basic flow of payments between two counterparties—the fixed-rate payer and the floating-rate payer:

```mermaid
flowchart LR
    A["Fixed Rate Payer <br/>(Company ABC)"] -->|Pays Fixed Rate| B["Floating Rate Payer <br/>(Bank XYZ)"]
    B -->|Pays Floating Rate <br/>(e.g. CORRA+Spread)| A
```

Even though each side is “paying” an amount, in practice, often just the net difference in cash flow changes hands on the scheduled payment date.

### Setting the Swap’s Fixed Rate

At inception (swap start), the fixed rate is set so that the present value (PV) of the expected floating leg payments equals the PV of the fixed leg. When these values are equal, the swap has zero initial market value. If the fixed rate is set too high, the fixed-rate payer is likely to be at a disadvantage and the contract would actually have positive initial value for the fixed-rate receiver (and vice versa).

Professionals typically rely on a forward rate curve to project the floating rate. This forward rate curve is a series of implied future interest rates—often derived from the current yield curve for the appropriate benchmark (e.g. Government of Canada bonds, BA futures, or forward CORRA rates). Once those future floating rates are projected, each future cash flow is discounted back to present value using discount factors from the zero-coupon yield curve. Meanwhile, the fixed-rate leg is simpler: it’s just a fixed rate multiplied by the notional, times the day-count fraction for each payment period, also discounted back to the present.

If the notional is N and the term of the swap is T years with suitable payment intervals j, an illustrative approach to finding the “par swap rate” r_fixed is:

1. Project floating leg cash flows based on the forward curve for each interval j.  
2. Compute the PV of each floating leg payment by discounting each at its appropriate discount factor DF_j.  
3. Sum all discounted floating payments to get PV(Floating).  
4. Compute the PV of a fixed rate r_fixed paid at each interval j. The discounted value can be expressed as:  
   PV(Fixed) = r_fixed × (N × Σ_j [τ_j × DF_j]) + (N × [DF_final - 1]) if there is some notional exchange at maturity, but usually, for an interest-only swap, it’s just the interest part.  
5. Equate PV(Fixed) and PV(Floating), and solve for r_fixed.  

The big picture:  

Present Value (Fixed Leg) = Present Value (Floating Leg)  

Hence, r_fixed is set so these match. That’s why it’s called the “par swap rate” because you’re essentially getting a “fair” deal at the start.

### But Let’s Be Real: Market Fluctuations

Interest rates rarely stand still. If short-term rates rise a month into the swap, it might suddenly tip the existing swap’s market value, turning it into a gain (or loss) for one side. Credit risk can also cause that fair value to shift if one counterparty has a higher perceived risk of default—this can lead to bigger haircuts on collateral or modifications to discount rates.

Daily valuations matter too. Under Canadian regulatory regimes (e.g., guidance from the Canadian Securities Administrators (CSA) and oversight by CIRO), banks and other market participants often mark-to-market these swaps daily. When the value moves, collateral might need to move along with it so that each side remains protected. Collateral is typically posted in cash or sometimes in high-quality government securities.

### Basic Example of Pricing a 3-Year Plain Vanilla Swap

Let’s take a bite-size approach. Suppose Company ABC enters a 3-year swap to pay fixed and receive floating (linked to CORRA) on a notional of CAD 10 million, with quarterly payment frequency. Let’s assume we have a forward CORRA curve telling us the expected future rates for each 3-month period, and a discount curve which gives us discount factors for each of these same payment dates.

Let’s lay out what the floating rates might look like for each quarter (simplifying heavily):

• Quarter 1: 4.10%  
• Quarter 2: 4.15%  
• Quarter 3: 4.20%  
• ... (we continue for all 12 quarters stretching 3 years)  

For each quarter j, the expected floating payment is:

Floating Payment_j = (Projected Rate_j × Notional × Day-Count Fraction).  

We discount that back to the present using discount factor DF_j. Summing them up, we get:

PV(Floating) = Σ(Floating Payment_j × DF_j).  

Let’s say, after we do that math, we find the total PV of the floating leg is approximately CAD 920,000. That means, for everything we see in the forward curve, receiving floating payments over the next 3 years is “worth” $920,000 in today’s money.

Then, we guess a fixed rate, say 4.15%, to see how the value of the fixed leg would stack up. We do:

Fixed Payment_j = (4.15% × Notional × Day-Count Fraction).  

We discount each of these fixed payments by the same discount factor (or a relevant discount factor for each time period). Summing them up, we might get CAD 920,000 as well, or not. If the sum is more or less, we tweak the fixed rate until they match. Once they match, that 4.15% is our par swap rate, and the swap has a fair (zero) initial value for both parties.

This is obviously a simplified example. In practice, you might have slightly different discount factors for each quarter—some might be 0.98, 0.95, 0.92, etc. You sum them all up, multiply them by the cash flows, and aim for equivalence. If you want to see more advanced references that load the real math in detail, I’d point you to “Fixed Income Securities” by Pietro Veronesi, which goes deeply into how yield curves are derived and how that influences the swap rate.

### A Note on Discount Factors

Discount factors effectively convert a future dollar amount into a present value. If a discount factor for a certain date is 0.95, it means that CAD 1 in that future quarter is worth 95 cents in today’s money. You get them from the zero-coupon yield curve for government bonds or from swap curves themselves. Since the credit risk and market conditions might differ, participants sometimes use an Overnight Indexed Swap (OIS) curve for discounting, especially when referencing CORRA. This is a big shift from older LIBOR-based discounting. In Canada, CORRA-based discounting is a best-practice standard for collateralized swaps.

### Valuing the Floating Leg

One of the more intuitive aspects of a plain vanilla swap is that, at the start of each payment period, the floating leg resets to a “fair” rate. In many textbook examples, you’ll see that the floating leg is worth par (i.e., notional) at the immediate reset date, because it just reset to the then-current forward rate. Between resets, the floating leg’s value can fluctuate with interest rates. In the big scope, though, practitioners project each floating rate using forward rates. If you want to see how complicated or simple that is, you can check out open-source libraries like [QuantLib](https://www.quantlib.org/) (yes, it’s free!) and punch in your yield and forward curves to get a precise floating leg valuation.

### Real-World Tools and Techniques

Major players in the market typically rely on powerful data systems:

• Bloomberg: well-known functions that model swaps in real-time; you click in your floating index (like CORRA), notional, start date, end date, fixed frequency, etc.  
• Refinitiv Eikon: robust swap pricing modules for real-time quotes.  
• In-house systems at banks and large fund managers.  
• Open-source libraries (e.g., QuantLib), which are super flexible if you like coding in C++ or Python.

These platforms connect to real-time or near real-time market data. They’ll retrieve yield curves, forward CORRA or forward CDOR rates (though post-CDOR environment in Canada is heavily shifting to CORRA), and discount factors. Then the software automatically calculates the net present value (NPV) of both the fixed and floating legs.

### Common Pitfalls and Best Practices

I can’t tell you how many times I forgot to align day-count conventions or made a slight mismatch in payment frequency assumptions. Seemingly small details—like whether you use Actual/365 or 30/360—can create differences in the final swap valuation. Another pitfall is ignoring credit risk. If you’re dealing with a lower-rated counterparty, even if you decided a fair fixed rate on day one, the risk-based discounting might change the effective value midstream. Also, ignoring the effect of compounding for daily overnight rates can lead to mispricing.

One best practice is to keep a robust schedule of dates and payments, each with an accurate discount factor. Ensure your yield curve data is up to date (and consistent!) for both discounting and projecting the floating rate. For corporate treasurers or smaller fund managers, it might help to do a high-level check—like verifying if the fixed rate is roughly in line with market swap quotes for that tenor.

### Daily Valuations and Collateral

Swaps, especially those governed by the International Swaps and Derivatives Association (ISDA) Master Agreement, often require daily margin or collateral postings. If the market moves and your swap is now “in the money” to you, your counterparty might have to post collateral, like cash or treasury bills, to offset that risk. On the flip side, if your trade has moved against you, you might need to post collateral. Under CIRO’s oversight, these margin processes must be consistent with regulations to protect all parties. So continuous or at least frequent valuation is key.

### CORRA and the Transition from CDOR

In Canada, we’ve seen a shift away from the Canadian Dollar Offered Rate (CDOR) to the Canadian Overnight Repo Rate Average (CORRA). If your swap references CORRA, you’ll need the forward CORRA curve instead of a forward CDOR curve to project the floating payments. Practitioners typically forecast overnight rates plus any relevant spread. The discounting is also done with the same or similar OIS curve to maintain consistency. 

### Regulatory Context in Canada

In the Canadian market, the CSA has published guidance on how derivatives, including swaps, ought to be valued. These guidelines emphasize consistency, prudence, and the need to use market-based data. CIRO (the Canadian Investment Regulatory Organization) supervises investment dealers and can impose margin or capital requirements, especially if you’re an authorized participant. For daily valuations or collateral calls, you’re expected to rely on accepted industry practices. The golden rule is: the more accurate and consistent your data inputs, the more accurate your valuation.

### Example of Marking a Swap to Market

Imagine that 6 months have passed since you entered a 3-year swap to pay fixed at 4% and receive a floating CORRA-based rate. In those 6 months, short-term rates jumped 50 basis points. Now your fixed payment might be relatively low compared to new, higher floating benchmarks. Your swap position (where you pay fixed) could be worth more because new payers would have to pay maybe 4.50% if they opened a swap today. You’d do a fresh set of calculations—project out the new expected floating rates for the next 2.5 years, discount them, and compare them to your 4% fixed payments. The difference is your mark-to-market gain or loss.

### Using QuantLib for a Quick Demo

Though we’re definitely not diving into code here, I have personally used QuantLib in Python to price hypothetical interest rate swaps. It’s a neat exercise: you instantiate a yield term structure, define the swap schedule (i.e., how often it pays, the day-count convention, etc.), and then ask the library to compute the fair swap rate. The code might look a little complicated first time around, but after a while, it’s an amazing tool to learn the nitty-gritty details. If you’re curious, [QuantLib](https://www.quantlib.org/) has extensive documentation and examples that walk you through building yield curves, bootstrapping forward rates, and discounting swap cash flows.

### Putting It All Together

Pricing an interest rate swap boils down to comparing the net present value of two streams of cash flows. The fixed leg is straightforward: a constant rate times the notional, discounted to present. The floating leg is where the fun begins: you use a forward rate curve (like a forward CORRA curve) to project each future payment, then discount it. If you’re pricing at inception, you solve for the fixed rate that sets the swap’s value to zero. If you’re re-valuing mid-swap, you recalculate with the updated interest rate environment. This is crucial for understanding your swap’s gain or loss. Keep track of day-count conventions, payment frequencies, and discount rates. 

### Additional Resources

• CSA Regulatory Guidance on Valuation of Derivatives  
• Bloomberg Swap Pricing Functions / Refinitiv Eikon Tools  
• [QuantLib Website](https://www.quantlib.org/) for open-source pricing examples  
• “Fixed Income Securities” by Pietro Veronesi (advanced deep-dive on yield curves and complex swap valuation)  
• CIRO (https://www.ciro.ca) for current rules and oversight updates around margin, collateral, and daily mark-to-market  

Feel free to tinker with real data and practice building your own yield curves. Yes, it’s a bit of work to gather all the rates and do the discount factor math, but once you get the hang of it, you’ll see it’s not as intimidating as it might have seemed. Plus, being able to speak confidently about swap pricing is a sure way to impress the folks in your next treasury or risk management meeting. 

---

## Sample Exam Questions: Pricing an Interest Rate Swap

{{< quizdown >}}

### In a plain vanilla interest rate swap, what is the primary reason the swap’s initial value is typically set to zero?

- [ ] Each leg has no payments.
- [x] The present value of the fixed leg equals the present value of the floating leg at inception.
- [ ] No collateral is required by either party.
- [ ] The transaction is cleared by a central counterparty.

> **Explanation:** The fair value for both the fixed and floating legs is equated so that at inception neither party has an initial advantage, resulting in a swap value of zero.

### Which of the following best describes the function of discount factors in swap pricing?

- [ ] They convert floating rates into fixed rates.
- [ ] They eliminate day-count conventions for future payments.
- [ ] They assume credit risk is zero over the life of the swap.
- [x] They convert future cash flows into their present value.

> **Explanation:** Discount factors are used to derive the present value of a future cash flow by accounting for the time value of money.

### If the floating rate index for a Canadian interest rate swap changes from CDOR to CORRA, how might this affect the pricing approach?

- [ ] Pricing no longer requires discounting future cash flows.
- [ ] Fixed leg computation remains identical but the notional is halved.
- [x] Practitioners use a forward CORRA curve instead of a forward CDOR curve to project future floating rates.
- [ ] No difference at all, as the swap fixed rate remains unchanged.

> **Explanation:** CORRA-based swaps need to reflect the new underlying rates. Thus, the floating leg is projected using a forward CORRA curve rather than a forward CDOR curve.

### Why is daily mark-to-market of a swap necessary in many institutional or dealer settings?

- [ ] Swaps rarely change in value, so daily checks confirm no movement.
- [ ] Regulatory bodies forbid posting collateral based on monthly valuations.
- [x] Market interest rates change, causing gains or losses that need to be collateralized.
- [ ] It ensures both parties remain in a fixed payment arrangement.

> **Explanation:** As the interest rate environment shifts, the value of each leg can fluctuate. Daily valuations help determine if additional collateral is required under CIRO or CSA regulations.

### What role do forward rate curves play in pricing the floating leg of a swap?

- [x] They provide projected future floating rates that determine cash flows.
- [ ] They replace discount factors for the fixed leg.
- [x] They help forecast interest payments at each payment interval.
- [ ] They set the fixed rate on the swap to a guaranteed profit.

> **Explanation:** The forward rate curve gives a snapshot of expected future rates, which is essential in forecasting the floating payments and measuring the present value of those cash flows.

### Which statement is most accurate about the par swap rate in a vanilla interest rate swap?

- [x] It is the fixed rate that makes the swap’s initial value zero.
- [ ] It equals the spread between the overnight rate and prime rate.
- [ ] It is always below current market interest rates.
- [ ] It is fixed by the central bank.

> **Explanation:** The par swap rate is the fixed rate that ensures the initial net present value of the fixed leg equals that of the floating leg, resulting in zero initial market value.

### Which is a common pitfall in swap pricing?

- [ ] Using discount factors from the swap curve only.
- [x] Misalignment of day-count conventions or payment frequencies.
- [ ] Incorporating forward rates into both legs.
- [ ] Failing to assume any credit risk between parties.

> **Explanation:** Day-count conventions (e.g., Actual/365, 30/360) can differ and cause inaccurate present value calculations if not aligned properly across the swap schedule.

### What is the effect of rising short-term interest rates on an existing swap where you pay fixed and receive floating?

- [ ] The value of your swap falls because you are paying a higher rate.
- [x] The value of your swap likely increases as your floating receipts rise.
- [ ] Your swap remains neutral; no change occurs.
- [ ] The fixed rate you pay adjusts higher automatically.

> **Explanation:** If short-term rates rise, the floating leg you receive becomes more valuable relative to the fixed rate you pay, so your position tends to gain value.

### Under CIRO’s regulatory environment, why might a swap participant be required to post additional collateral?

- [ ] Swaps are illegal without full collateralization initially posted.
- [ ] CIRO doesn’t require collateral for interest rate swaps.
- [x] A change in market interest rates might push a swap’s value in one side’s favor, triggering margin requirements.
- [ ] The CSA mandates daily transaction fees to national clearinghouses.

> **Explanation:** Market fluctuations alter a swap’s market value, and if the exposure grows beyond a set threshold, additional collateral is posted under regulatory guidelines.

### True or False: Using the same OIS (Overnight Indexed Swap) curve for discounting both fixed and floating legs ensures consistency in a CORRA-based swap’s valuation.

- [x] True
- [ ] False

> **Explanation:** A CORRA-based swap typically uses an OIS curve for discounting both legs. This alignment reflects real market risk-free funding conditions and promotes accurate pricing.

{{< /quizdown >}}
