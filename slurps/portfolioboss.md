---
title: "portfolioboss Documentation"
source: "https://portfolioboss.com/documentation/"
scraped: "2026-03-01T02:09:57.346Z"
tokens: 204755
---
# portfolioboss Documentation

> Source: https://portfolioboss.com/documentation/
> Generated: 3/1/2026, 2:09:57 AM

### portfolioboss

#### _documentation_.md

> Source: https://portfolioboss.com/documentation/
> Scraped: 3/1/2026, 2:07:31 AM

EARNINGS DISCLAIMER: I like to provide full transparency and not blow smoke up your behind, so listen up.100% Club members in general are seeing between 91%-100% winning months in back tests just using the Instant Start templates I created for them. These results are out-of-sample (unseen in the optimization phase), so I put a lot of weight into that fact.

I don’t yet have a statistic for the average member as far as gains are concerned. There are a lot of variables because this is not a cookie-cutter program. I do have dozens of brokerage statements on file, and the majority are looking positive.

There were a couple outliers that weren’t good because they went off track. I believe I convinced them of where they went wrong and they are back on track (too much leverage, and some over-fitting to the past). That’s my job :)

There are other factors in play as well such as: Are you actually making the trades? Account size. Is your broker any good or are they fleecing you? Are you using all the leverage available to you, or are you dialing it back like I recommend?

**Simply put, I believe the reason we’re seeing the highest preliminary success rate of any program EVER is because:**

a) you’re selecting from 100+ supercomputer-built strategies, and the odds of them all failing at once are extremely low.

b) the strategies take advantage of highly unusual edges that very few if any know about.

c) Our Meta ML technology is completely unique in the trading world. Very few understand that all strategies have cycles, and that there are opportune times to trade them. This allows you to treat trading more like a business rather than a hobby.

d) The daily instructions are brain-dead simple to follow, and can be accomplished in just a few minutes.

#### _documentation_a-strategy-for-short-selling.md

> Source: https://portfolioboss.com/documentation/a-strategy-for-short-selling
> Scraped: 3/1/2026, 2:08:19 AM

[!](_wp-content_uploads_2019_10_Short-Position-Heading-3336.png.md)

Portfolio Boss is generally used for trading Long Positions, but if you're a short seller, you can still use this Platform to help with your trades.

Note that some licenses do not allow you to create Short Positions.

* * *

### Definition of Short Selling

Short Selling means you're entering Positions by selling instruments (_shorting_ the instruments), in the hope that their prices will decrease. These sold instruments are not yours; they're borrowed from your broker and you have the obligation to return them. So, after you sell them, you close (exit) the _Short Positions_ by buying back these instruments (_covering_ the instruments) at such a low price. You'll profit when you bought the shares (to return to your broker) at a lower price than the selling price.

Short Selling is an advanced trading method that carries a much bigger risk than the usual Long Positions. That's why we don't include any strategies created specifically for Short Selling. You must understand the dangers, and execute such trades at your own risk:

*   Short Selling exposes you to _unlimited_ losses. Here's why: You lose when the _buying_ price is higher than the selling price, and since stock's price can go upward without bounds, there's no limit to your loss. As you already know, stock's price does have a floor, i.e 0 dollar amount. But it doesn't have a ceiling; it can go to heaven and beyond. Compare that to a _Long Position_, in which you buy shares for $1000. At the worst case scenario, when the stock's price plummets to $0, you'll only lose $1000. But if you're entering Short Positions, and the price goes higher than the Empire State, you may as well file for bankruptcy.

*   Since you're essentially borrowing stocks, you have to pay interest to your broker _as long as_ the Positions remain _open_. This could be disastrous if you keep waiting for the right buying price. Some brokers even impose a set _deadline_ for returning the borrowed instruments. A Long Position on the other hand, allows you to ride the market for as long as you want, without any interest.

*   There's a dangerous feedback loop called _Short Squeeze_, in which the stock's price goes up and causes some Short Sellers to _panic_ and buy back these stocks. Since _more people_ are _buying_ these stocks, prices will go up even further (the law of supply and demand), thus prompting other Short Sellers to close their positions (buy back the stocks to limit their losses) and increasing the prices even more. This loop goes on until you have to pay a hefty amount to close your position (_if_ you can still find any leftover stocks).

All that being said, such risks also carry big quick profits. So, let's now cover what Portfolio Boss has to offer regarding Short Selling.

* * *

### Strategy Rules for Trading Short Positions

**1.**  **Position Type (System Settings Panel):** In Portfolio Boss, you can generate Short Positions by changing this rule into “Short”, instead of the usual “Long”. 

!

Setting it to “Short” will change the behavior of some parameters. So, we need to revisit each relevant parameter in the sections below.

If you have a limited license, this parameter will not be available. Therefore, you will be using Long Positions by default. Please contact our [Customer Support](mailto:support@portfolioboss.com) if you wish to upgrade your license.

* * **2.**  **If Position Triggers Cover Filter, Replace With (System Settings Panel):** this is how you want to park your money after closing the Short Position. You can choose either “Cash”, which means your money will be idle, or “Cash Equivalent” so that your money will grow a little. 

!

In other words, after a Short Position is covered (the stocks are bought back) you want to enter cash or cash-equivalent before executing another Short Position at the next [switch day](_documentation_system-settings-panel-guide_.md#monthlyswitch). This rule is only available if the [“System” rule](_documentation_system-settings-panel-guide_.md#systemparameter) is set to “Periodically Switch Positions”.

Keep in mind, during tough recessions (strong bear markets), a cash-equivalent such as bonds may not be attractive at all. With rising interest rate, existing bonds prices tend to fall; not to mention the higher risk of defaults by bond-issuing companies. Therefore “Cash” could be used as safe-haven during such times. You may also want to use “Cash” while creating and backtesting the strategy (spanning multiple tough recessions in the past).

* * **3.**  **If Position Triggers Cover Filter … Replace With (System Settings Panel):** this rule is only available if the “System” rule is set to “Continuously Switch Positions”. 

!

This rule essentially tells you that once a Short Position is covered (the stocks are bought back), the strategy will automatically enter the next Short Position. But if there's no profitable Short Position to be entered, PB will park your money into cash or the cash-equivalent.

* * **4.**  **Short Order Type (System Settings Panel):** with this rule, you can short (sell) the borrowed instruments with either a Market Order or a Limit Order. With Market Order, the instruments are _sold_ at the latest market price when you input the order to your broker. 

!

With “N ATR Limit Order”, the instruments are _sold_ only if the limit price (or _higher_) is met.

The limit price is calculated with the next parameter (“Short Order Limit”), and you input to the broker the resulting limit price.

After giving you the Short Signal, PB will look at the _next day's_ High price to determine if the Limit Order is met. If it is, then your Short Position is considered entered; if it's not, then the Position reverts to a Cash or Cash Equivalent until the next Short Signal is given (or if a switch day arrives).

Note that some licenses can't use Limit Orders, thus defaulting to Market Order. If you wish to upgrade your license, please contact our [Customer Support](mailto:support@portfolioboss.com) team.

* * **5.**  **Short Order Limit (System Settings Panel):** this calculates the short _limit price_ that you'll input to your broker. With this Limit Order, the instruments are sold only if the price is equal or higher than: the previous day's close _plus_ a multiplied ATR. 

!

The reason is that you want to sell these instruments at the highest price possible while anticipating the price to go lower.

The first parameter defines the [ATR](https://www.investopedia.com/terms/a/atr.asp) multiplier; you can set this either greater than 1, or a fraction of 1. But keep in mind, anything _greater_ than 1 means your Limit Order is not likely to be filled, since you're looking for a price movement _beyond_ the _average_.

!

Worse still, if you're looking at a stellar price 3x the ATR, there's a good possibility the instrument will reverse toward an _Uptrend_.

Now, the second parameter defines the number of days to look for the Average True Range.

!

If you use a Short Limit Order, a “Short Limit” indicator will be shown on the instrument's [Price Chart](_documentation_instrument-tab_.md). Look for a price bar whose _High_ is equal or _higher_ than this indicator-line.

!

* * **6.**  **Cover Order Type (System Settings Panel):** with this parameter, you can cover (buy back) the instruments with either a Market Order or a Limit Order. With Market Order, the instruments are bought at the _latest_ market price when you input the order. 

!

With “N ATR Limit Order”, the instruments will be bought only if the limit price (or _lower_) is met.

So essentially, the strategy calculates the limit price with the next parameter (“Cover Order Limit”), and then you input the resulting limit price to the broker.

After giving you the Cover Signal, the strategy will look at the _next day's_ Low price to determine if the Limit Order is met. If it is, then your Short Position is successfully closed; if the Limit isn't met, then the Position _continues_ until another Cover Signal is given (or if a switch day arrives).

If you use a Cover Limit Order, make sure _at least one_ of the Cover Filters is set to “Limit Order” instead of “Market Order”. Go to the Cover Filters Panel (previously known as the [Sell Filters Panel](_documentation_sell-filters-panel-guide_.md)) and change any Cover Filter there to use Limit Order. Cover Filters there that use Limit Order may serve as _profit-taker_ filters, while those with Market Order can serve as stop-loss where you must sell immediately at whatever market price, instead of waiting for a limit price to be met.

!

Note that some licenses can't use Limit Orders, thus defaulting to Market Order. If you wish to upgrade your license, please contact our [Customer Support](mailto:support@portfolioboss.com) team.

* * **7.  Cover Order Limit (System Settings Panel):** this calculates the Limit price that you'll input to your broker. With this Limit Order, the instruments are bought only if the price is equal to or _lower_ than: the previous day's close _minus_ a multiplied ATR. 

!

The reason is that you want to buy these instruments at the lowest price possible before the stock rallies again, so essentially you're looking for a further discount.

The first parameter defines the ATR multiplier, you can set this _greater_ than 1 or a _fraction_ of 1. But keep in mind, if you're looking for a price drop _greater_ than the average, your Limit Order isn't likely to be filled.

!

The second parameter defines the time period to calculate the Average True Range:

!

Note, if you use a Cover Limit Order, a “Cover Limit” indicator will be shown on the instrument's Price Chart (at the [Instrument Tab](_documentation_instrument-tab_.md)). Look for a price-bar whose _Low_ is equal to or _lower_ than this indicator-line.

!

* * **8.**  **Short Filters Panel:** these filters select instruments in your Portfolio that are potentially profitable to be Shorted. In other words, think of these filters as the [Buy Filters](_documentation_buy-filters-panel-guide_.md) that you're already familiar with. 

!

You can craft your own rules on what instruments to look for; but generally you want _downtrending_ instruments whose prices are still high (or instruments that _just_ experienced a _reversal_ from a _peak_). Note, for an instrument to be considered, it must fulfill _all_ the rules listed here.

After these instruments are filtered, they will be ranked according to the [Ranking Rules](_documentation_ranking-panel-guide_.md) you set below this panel. Only the “top n” instruments will be entered as Positions (“n” according to the rule [“Total Positions to Hold”](_documentation_system-settings-panel-guide_.md#totalpositions)).

* * **9.**  **Cover Filters Panel:** these filters define the criteria for _closing_ the Short Positions, so you'll be covering (buying back) the shorted instruments. Think of these as the usual Sell Filters that you're already familiar with. 

!

Generally, you want to close downtrending Positions that are _likely_ to make a rally (or Positions that _have just_ experienced a reversal from a trough).

For a Position to be closed, only _one_ of these filters need to be met, not all of them.

Once the Position is closed, the strategy will recommend you to buy a cash-equivalent to park your profit before entering the new Short Position at switch day (this applies for a Periodically Switching strategy). Or it will recommend you to replace the closed Position immediately with the new Short Position (applies for a Continuously Switching strategy).

* * **10.**  **In a Short Strategy, the [Trade Signals Panel](_documentation_trade-signals-panel-guide_.md)** will show “Short”, “Cover”, “Buy”/”Sell” (cash-equivalent), and “Hold” instead of the usual Buy/Sell signals. You can also see the limit price for each signal (if the strategy uses a Limit Order).

!

* * *

### Note:

A short strategy is best employed in tandem with a long strategy. You can achieve this with [multi-strategy](_documentation_multi-strategy_.md). Therefore the short strategy kicks in during rough times for the long strategy. In the long run, a short strategy by itself rarely gives acceptable return. It may even reduce your original account balance to zero dollar (worse yet, negative balance, because there's no ceiling on stocks prices). The key is to short at the right times, not all the time; then during market turmoil, you may hit a large mother lode _very quickly_.

The reasoning is simple: markets tend to go up in the _long run._ But when they **do** go down, they do it in a mighty drop that's much quicker than they go up.

!

Another way to initiate short positions in Portfolio Boss is by using inverse ETFs, as described **[here](_documentation_system-settings-panel-guide_.md#inverseETF)**.

[**Back to Top**](_documentation_a-strategy-for-short-selling_.md#backtotop)

You have already reported this .

#### _documentation_about-filters-rules.md

> Source: https://portfolioboss.com/documentation/about-filters-rules
> Scraped: 3/1/2026, 2:08:32 AM

[!](_wp-content_uploads_2019_10_Buy-Sell-and-Ranking-Rules-Diagram_00000.png.md)

In Portfolio Boss, Technical Indicators are used for selecting which instruments to be entered as Positions; these are known as the “Buy Filters”, and you can find them on the [Buy Filters Panel](_documentation_buy-filters-panel-guide_.md).

[!](_wp-content_uploads_2019_10_Buy-Filters-About.png.md)

As well, Technical Indicators are used to define the criteria for exiting Positions; these are known as the “Sell Filters”, which you can find on the [Sell Filters Panel](_documentation_sell-filters-panel-guide_.md).

[!](_wp-content_uploads_2019_10_Sell-Filters-Panel-About.png.md)

And then there are “Ranking Rules”, which are Technical Indicators used for ranking the instruments top to bottom. You can find them on the [Ranking Panel](_documentation_ranking-panel-guide_.md).

[!](_wp-content_uploads_2019_10_Ranking-Rule-About.png.md)

So first of all, _instruments_ in your strategy's Portfolio must pass the Buy Filters' criteria. Each instrument must fulfill _all the Buy Filters_ listed on the strategy; if just even one Buy Filter is not satisfied, the instrument will not be considered. 

[!](_wp-content_uploads_2019_10_Passing-the-Buy-Filters_00000.png.md)

For example, to be considered as a Position, an instrument's latest closing price must be above the 200 days SMA **and** its volatility of the past 10 days must fall within 30% and 50%.

Now then, there could be quite a few instruments that passed the first screening; more than the maximum number of Positions you'd like to hold at any given time (set on the parameter [“Total Positions to Hold”](_documentation_system-settings-panel-guide_.md#totalpositions)). So, how does the strategy pick the final instruments to be entered as Positions?

Enter the Ranking Rules, which rank the instruments top to bottom, based on certain criteria. For example, the Ranking Rules prefer instruments with the highest gain (profit) during the past 10 days; thus the topmost ranked instrument is the one with the highest gain, while the lowest ranked instrument has the least gain.

[!](_wp-content_uploads_2019_10_Ranking-the-Instruments_00000.png.md)

Now, let's say the maximum number of Positions you'd like to hold at any given time is 10, then only the _top 10_ ranked instruments (that have also passed the Buy Filters) will be entered as Positions.

[!](_wp-content_uploads_2019_10_Buy-Top-10-Instruments_00000.png.md)

Once the Positions are entered, the strategy watches them like a hawk, whether or not they hit _any of the_ Sell Filters. For a Position to be exited, it only needs to hit _one of the_ Sell Filters. 

[!](_wp-content_uploads_2019_10_Exiting-Positions_00000.png.md)

For example, there are two Sell Filters: one is when a Position's latest closing price goes _below_ the 200 days SMA, while the other looks at the SPX index, whether or not it closes _below_ the _lowest_ closing-price of the past 6 months.

If a Position closes below its 200 days SMA _but_ the SPX index is still safe (above its lowest close), then the Position _will_ be exited. Alternatively, if _all_ Positions closed _above_ their respective 200 days SMA _but_ the SPX index is going downhill (it closes below the lowest close of the past 6 months), then _all Positions_ will be exited, no exception.

In this Chapter 6, we will discuss all the Filters and Ranking Rules in great detail.

We'll see what Technical Indicators are used, the real-life application of the filters, and the description of each parameter. Keep in mind, these are just the _generally accepted_ wisdom for using these indicators, which means they may not hold true _all_ _the time,_ since Technical Analysis can't predict the future 100%.

So use them not as a bible set in stone, but as a general rule of thumb.

* * *

#### Notes:

*   Mostly, filters that exist as Buy Filters also exist as Sell Filters. That is, they're using the same Technical Indicators but with different criteria. Therefore to avoid redundancy, we will only discuss each Filter once (both as a Buy and Sell Filter).

*   It's important to note that the various filters & rules in your strategy must be able to cope with a long period (both in the future and in the past), so the strategy can stand the test of time, weathering various market conditions. It's very tempting to set your strategy to perform very well in the _near_ future, but that's a mistake you want to avoid.

*   Even if a Position doesn't hit any Sell Filters, it may be liquidated due to the instrument's company (or fund) getting delisted from the exchanges (merger, acquisition, or pure fat old bankruptcy).

*   As a side note, Sell Filters are also used when entering Positions. That is, if any of the _would-be_ Positions _also_ hits the Sell Filters, then the strategy will discard it, as it's useless to enter the Position only to be exited at the same time.

*   Please note that some Portfolio Boss licenses only allow you to use specific filters, or filters with limited parameters. If you wish to upgrade your license, please contact our Customer Support team at [support@portfolioboss.com.](mailto:support@portfolioboss.com.)

[**Back to Top**](_documentation_about-filters-rules_.md#backtotop)

You have already reported this .

#### _documentation_all-time-high-low-filter.md

> Source: https://portfolioboss.com/documentation/all-time-high-low-filter
> Scraped: 3/1/2026, 2:08:39 AM

!

!

This filter allows the strategy to enter or exit Positions if an all-time high (or all-time low) has been reached _within_ the specified period. All-time high (ATH) is defined as the highest _adjusted closing_ price _ever reached_ by the instrument; and all-time low (ATL) is the lowest _adjusted closing_ price the instrument ever hit throughout its lifetime.

!

!

*   Generally you can use this as a Buy Filter to look for all-time highs, since these indicate strong bullish sentiment. New highs are usually brought about by some groundbreaking favorable news or circumstances for the company itself, or the market in general, and these will attract droves of greedy investors who will drive up the price even more.
*   You can also use this as a Short Filter that finds all-time lows. Companies (or funds) that post a new low scare off investors, because usually there's something fundamentally wrong with them. And it would be hard for their stock price to recover.

In other words, you use the filter to enter Positions. It's not recommended to use it as a Sell (or Cover) Filter, because by the time the all-time low is reached it would be too late to get out as your account size has gone downhill for the most part. Theoretically you can (use it to exit Positions), but just make sure your _entry_ is also close enough to the all-time low (or high, if shorting).

!

Now, some mavericks out there see all-time highs as an opportunity to short (investors are “scared of the heights” they say), but this is more of a folly than wisdom. You short only when you see weakness, not strength. But just try it and experiment for yourself, maybe this out-of-the box “wisdom” could be the secret sauce for your strategy.

All that being said, it would be prudent for you to set other criteria for entering the Positions. All-time high (or low) by itself is still a very loose criteria, it _may be_ good to wait a little before jumping onto the bandwagon (who knows, maybe the bulls need to take a rest in a shallow creek up ahead). Or to see whether the momentum (and volume!) are still strong indeed to warrant further hikes:

!

Don't be part of the crowds gullible to overhyped news. How many times did investors chase really hot stocks, only to realize later _it's the peak_!

Now, let's discuss its parameters.

* * **1.  The first parameter** (leftmost) lets you define whether the filter should find all-time high, or, all-time low:

!

The general wisdom says to find all-time highs for a Buy Filter, and for the Sell Filter you want to find all-time lows. But you can't go wrong with the opposite too (as our tests indicate, helped by the [**Divine Engine**](_documentation_the-divine-engine-and-the-boss_.md)); that is, set this parameter to “Low” for a Buy Filter, and “High” for a Sell Filter. It all depends on your strategy's rules, filters, and Portfolios.

!

* * **2.  The second parameter** defines the lookback period to find the all-time high or all-time low:

!

This obviously includes today's candle (once the market closed). Let's say you set this parameter to 5 days:

!

then the filter must identify such ATH or ATL _within_ the span of 5 days, including today. Our tests indicate a short period from 20 to 55 days to be generally good, as well as a longer period of 110 to 160 days. Side note, the minimum value you can set here is 2 days, which means you jump into the ATH or ATL (nearly) as soon as it happens. If you want to “wait a bit”, set a longer period here.

With longer periods, sometimes the same ATH (or ATL) can trigger multiple (subsequent) signals.

* * *

#### Notes:

*   The new all-time high does not necessarily be _higher_ than the previous ATH; it can be exactly the _same_ price (but not lower). Ditto all-time low, i.e. it must be equal to, or lower than, the last ATL.
*   The _all-time_ high (or low) is compared to the previous prices all the way from when the instrument was first traded (listed) on the exchanges, not from the [earliest backtest date](_documentation_backtest-panel-guide_.md#datefromparam) of the strategy.
*   Since this filter is all about the instrument's price, you may be wondering why'd we use [adjusted prices](_documentation_instrument-tab_.md#adjustedprice)? For backtesting purposes (which Portfolio Boss is all about), adjusted prices is the most realistic price. Imagine if due to a stock split a company traded from $100 down to $5: while such a low price may be the lowest price it ever traded (and even breached all support and moving averages), it's not an indication there's a huge selling pressure or that the company is about to go bankrupt. It would be wrong to base our technical analysis on that faulty “real price” assumption (as it's simply a stock-split, or dividend payment, or what have you). Now don't worry, because when you finally trade with real money (that is, forward performance as opposed to backtesting), the strategy _will_ definitely use the real price, as adjustments happen after the fact, not _before_ the stock splits happen.
*   Some market technicians advocate the identification of multiple consecutive ATH (or ATL) before placing a trade, as a way of confirmation. Due to the way this filter is calculated, you can't find such consecutive ATH/ATL even if you stack this multiple times as Buy Filters (with different periods). The shorter period will always trump the longer period filter in finding the ATH/ATL.

**[Back to Top](_documentation_all-time-high-low-filter_.md#backtotop)**

You have already reported this .

#### _documentation_appearance-tab.md

> Source: https://portfolioboss.com/documentation/appearance-tab
> Scraped: 3/1/2026, 2:09:22 AM

[!](_wp-content_uploads_2019_10_Appearance-Tab.png.md)

This Tab allows you to change Portfolio Boss's appearance.

* * **1.**  “Colors”: You can pick any colors here to change the color theme. The color will be applied to the various buttons, panels' header, tabs' header, side-menu bar, etc.

[!](_wp-content_uploads_2019_10_Colors-777.png.md)

* * **2.**  “Theme”: Here you can choose whether Portfolio Boss is displayed in a “light” theme (mostly white), or a “dark” theme (mostly black/gray). You can also use the theme that your operating system is set to, by choosing “System Preference” here.

[!](_wp-content_uploads_2019_10_Theme-Light.png.md)

[!](_wp-content_uploads_2019_10_Theme-Dark.png.md)

* * **3.**  “Scale”: Dragging the slider here will scale up or down the interface, for example if you prefer the texts, panels, and buttons to appear larger (zoomed-out).

[!](_wp-content_uploads_2019_10_Scale-Reset.png.md)

Note, you _don't_ actually need to do the scaling here; you can simply hold down Ctrl key while _scrolling_ the mouse wheel _anywhere_ on the PB interface (the scale is applied universally). And to reset the scaling back to normal, hold down Ctrl key while pressing the middle mouse button (press down the scroll wheel). Pressing the “Reset” button here will also reset the _scale_ back to normal (the color & theme are kept).

If you want to reset Portfolio Boss's appearance entirely (including color and theme), use the [“Reset Layout”](_documentation_miscellaneous-tab-guide_.md#resetlayout) button on the Miscellaneous Tab.

[**Back to Top**](_documentation_appearance-tab_.md#backtotop)

You have already reported this .

#### _documentation_application-log-page.md

> Source: https://portfolioboss.com/documentation/application-log-page
> Scraped: 3/1/2026, 2:09:22 AM

You can access this page by clicking the “Application Logs” button at the bottom left of the interface. All Portfolio Boss activities are logged into this page: what pages you looked at, some parameters you changed, whether PB is downloading price data, etc.

[!](_wp-content_uploads_2019_10_Application-Log-Overview_00000.png.md)

But this log is most useful when you're experiencing problems with Portfolio Boss: the red colored text shows you the possible error in an easy to understand language, so you'll know where the problem lies. Sometimes these problems are caused by Portfolio Boss services experiencing troubles, in which case you can check it from the [**Portfolio Boss Status Page**](https://status.portfolioboss.com/):

!

The status page can be divided into six general service-reports:

1.  This is the PB mailing service that sends you the daily email notifications and such things.
2.  [The Boss](_documentation_the-divine-engine-and-the-boss_.md) supercomputer cloud service.
3.  Commitment of Traders reports service used by the [Smart Money Indicator](_documentation_smi-filter_.md).
4.  Dynamic Portfolios synchronization service.
5.  Instruments historical data download & processing service.
6.  Market-indicators (TAP and Grayscale) download service, as used by the [Cyber Code](_documentation_cyber-code-genetic-programming_.md#additionaldata).

If there are errors in any of the services, the PB Dev team is immediately notified and you can check back later (the status page is refreshed every minute):

!

Now let's get back to the Application Log: it's divided into two columns: the “Created At” column shows the time when the activity happened, and the “Message” column shows the detail of the activity.

[!](_wp-content_uploads_2019_10_Application-Log-Columns-Folder.png.md)

You can also click the button “Open Log Folder” (at the top) to take you to the log folder, containing all the log files since you first installed Portfolio Boss. You can open these files with a text editor such as Notepad.

[!](_wp-content_uploads_2019_10_Application-Log-Folder-Notepad.png.md)

You have already reported this .

#### _documentation_aroon-oscillator-filter.md

> Source: https://portfolioboss.com/documentation/aroon-oscillator-filter
> Scraped: 3/1/2026, 2:08:44 AM

[!](_wp-content_uploads_2020_03_ARO-filter-buy.png.md)

[!](_wp-content_uploads_2020_03_ARO-filter-sell.png.md)

This filter looks at an instrument's Aroon Oscillator value (ARO), and if it's above (or below) the threshold ARO value that you specified, that instrument will be considered as a buy (or sell).

Aroon Oscillator is a derivative and summary of the Aroon Indicators (both Aroon Up and Aroon Down). All three of them make up the Aroon System, developed by Tushar Chande in 1995.

Essentially, the Aroon System tells you of two things:

*   whether the instrument is uptrending or downtrending, and
*   how strong such a trend is.

It does this by gauging how long it takes for a new high (price) to appear from the previous high. Or the reverse: how long it takes for a new low to appear from the previous low. In other words, this Oscillator cares only about the frequency with which the new highs (or lows) are forming, not how big the prices are moving. This is based on the assumption that:

*   During an uptrend, new highs are formed more frequently than the new lows.
*   During a downtrend, new lows happen more frequently than the new highs.

As the name suggests, this filter oscillates between a value of -100 to 100:

*   A positive value indicates an uptrend. Values approaching 100 indicate that the new high was formed _much more_ recently than the new low, hence a strong uptrend. On the other hand, values approaching 0, while still indicating an uptrend, shows that the new high happened only slightly more recently than the new low, hence a weak uptrend.
*   A negative value indicates a downtrend. Values nearing -100 indicate a strong downtrending instrument, because the new low formed much more recently than the new high; while values nearing 0 indicate a weak downtrend.
*   Values near 0 (either positive or negative) may indicate a trading range, as the new high and the new low are appearing at about the same period.

* * **1.**  The first parameter defines the ARO period to find the new high and the new low within that period. For example, we'll go with a value of 25 days here: The filter will look at the highest and lowest prices within that 25-day period.

[!](_wp-content_uploads_2020_03_ARO-filter-1st-Param.png.md)

If the highest price was formed 1 day ago, while the lowest price was 24 days ago, we'll have a very high oscillator reading, nearing 100; and vice versa: if the lowest price was formed more recently than the highest price, we'll have a negative reading.

Throughout time, this value “decays” (approaching 0) until a new record price is found. The filter constantly looks at the new high and the new low throughout this moving window of 25 days.

Adjust this period according to your trading duration, whether you're a short-term or long-term trader. If you set this period too short, you'll get many false signals, as the trend can not be clearly established. If you set this too long, you'll be too late to jump on the trend wagon (the trend may be nearing its end).

Generally, for a short term trader, use a value less than 25 days here. While for a longer term trader, set a period greater than 25 days. If you're in doubt, you can look at the [Instrument Tab](_documentation_instrument-tab_.md) for the ARO indicator (below the price chart), and see if the ARO line corresponds to the price chart's clear uptrend and downtrend (within your trading duration). If it's not, adjust this period accordingly until you see clear correlation.

* * **2.**  The second parameter lets you choose whether the instrument's ARO must be “Above” or “Below” the threshold ARO value. Generally, you set this to “Above” for a Buy Filter, and “Below” for a Sell Filter.

[!](_wp-content_uploads_2020_03_ARO-filter-2nd-param.png.md)

* * **3.**  The third parameter defines the threshold ARO value, as already explained before. For example, you can set a Buy Filter that finds instruments whose ARO is “Above” 50, which is generally an uptrend.

[!](_wp-content_uploads_2020_03_ARO-filter-3rd-param.png.md)

Or the reverse, set a Sell Filter that will exit any positions whose ARO is “Below” -50, which is generally a downtrend.

* * *

#### Note:

Once this filter is applied (and the strategy is backtested), you'll see the ARO indicator on the chart below the price chart ([Instrument Tab](_documentation_instrument-tab_.md)). Make sure you select an instrument first before such indicator may appear.

[!](_wp-content_uploads_2020_03_ARO-Indicator-Chart.png.md)

**[Back to Top](_documentation_aroon-oscillator-filter_.md#backtotop)**

You have already reported this .

#### _documentation_atr-distance-below-sma-rule.md

> Source: https://portfolioboss.com/documentation/atr-distance-below-sma-rule
> Scraped: 3/1/2026, 2:09:18 AM

[!](_wp-content_uploads_2019_10_ATR-Distance-Below-SMA-Rule-000.png.md)

This rule ranks your instruments based on _how far_ they have gone _below_ their [SMA](_documentation_simple-moving-average-sma-position-filter_.md).

So, it looks at _how far_ the instrument's _last closing price_ went below its SMA (the distance is measured by the instrument's [Average True Range](_documentation_n-atr-above-below-sma-filter_.md)).

This is useful to rank instruments based on how likely they are to reverse toward the downtrend (good for [Short Selling](_documentation_a-strategy-for-short-selling_.md)).

[!](_wp-content_uploads_2019_10_ATR-Below-SMA-Rule-Overview-Trend-Change_00000.png.md)

Or, if you're a firm believer in the “mean reversion theory”, that suggests price spikes or drops will eventually return to the long-standing average prices, you can use this filter to find those instruments. Thus you're entering positions on big discounts in the hope they'll go up again.

[!](_wp-content_uploads_2019_10_ATR-Below-SMA-Rule-Overview_00000.png.md)

* * **1.**  The first parameter defines how to sort the instruments from top to bottom ranks. You can choose “Highest” or “Lowest” here.

[!](_wp-content_uploads_2019_10_ATR-Distance-Below-SMA-Rule-1st-Param-A.png.md)

“Highest” means the instrument that has gone the _farthest_ below the SMA has the top rank. So essentially, you're looking for instruments that have the biggest discount. But beware, it could also mean you're looking for instruments that will reverse the trend.

“Lowest” means the instrument that has gone the _shortest_ distance below the SMA (or the one that went highest _above_ the SMA) has the top rank. So essentially, you're looking for instruments that are still going strong in the uptrend (or looking for a small discount).

[!](_wp-content_uploads_2019_10_ATR-Distance-Below-SMA-Rule-1st-Param.png.md)

* * **2.**  The second parameter defines how many days (or months) ago to look for the Average True Range.

[!](_wp-content_uploads_2019_10_ATR-Distance-Below-SMA-Rule-2nd-Param.png.md)

* * **3.**  The third parameter defines the period for calculating the Simple Moving Average.

[!](_wp-content_uploads_2019_10_ATR-Distance-Below-SMA-Rule-3rd-Param.png.md)

* * *

#### Note

Regarding “Offset” and “Weight” parameters, please refer to the guide about [Ranking Panel](_documentation_ranking-panel-guide_.md#offsetweight).

[**Back to Top**](_documentation_atr-distance-below-sma-rule_.md#backtotop)

You have already reported this .

#### _documentation_augmenting-a-strategy-with-new-rules.md

> Source: https://portfolioboss.com/documentation/augmenting-a-strategy-with-new-rules
> Scraped: 3/1/2026, 2:08:24 AM

[!](_wp-content_uploads_2020_07_Oh-Genie-Fix-This.png.md)

This scenario assumes you have a strategy in hand (even a partially valid strategy).

For example, you added certain rules and technical indicators that you believe will benefit you (or to “guide” the Divine Engine). But still, you believe this strategy can be improved more. Maybe its performance is a little too underwhelming: despite yielding very good CAGR, it has mindboggling Drawdown.

And yet, you have no idea what rules and technical indicators may spice this strategy up to the next level. Worse yet, you have doubts. A certain rule/filter is dubious, whether it's useful or detrimental to the strategy's performance.

Worry not! The Divine Engine to the rescue!

* * **1.**  Let's continue with the previous strategy we created. You can delete all filters (supplied by the previous Divine Engine run), and add your own filters that you trust.

[https://portfolioboss.com/wp-content/uploads/2020/07/Recreating-a-Strategy-clip.mp4](_wp-content_uploads_2020_07_Recreating-a-Strategy-clip.mp4.md)

Don't worry, the top strategies are already stored (in this [Divine Engine Results Tab](_documentation_backtest-results-tab_.md)). They won't change whatsoever, even if you load them then modify/delete their rules. The only thing that changes is the performance report of an _active strategy_, obviously. That is, as market data is continually updated every day, the strategy's performance is also revised every day.

!

You can also create a strategy from scratch, as described in the previous scenario.

* * **2.**  Now, as you can see, this is the strategy I came up with:

[!](_wp-content_uploads_2020_07_Baseline-Strategy-SMA-ARO.png.md)

I believe the [200 days SMA filter](_documentation_simple-moving-average-sma-position-filter_.md) and the [Impulse ranking rule](_documentation_impulse-score-rule_.md) would be useful, but not so much the [Aroon oscillator](_documentation_aroon-oscillator-filter_.md). And besides, I'd like the Divine Engine to add more filters to beef up this meager strategy:

!

* * **3.**  So we will consult the AI genius. Click the button ! and ensure the “Search Algorithm” is [“Evolutionary”](_documentation_backtest-parameterization-panel.md#Evolutionary) (on the “Backtest Parameterization” Panel).

[https://portfolioboss.com/wp-content/uploads/2021/05/r56hjkfg2t1.mp4](_wp-content_uploads_2021_05_r56hjkfg2t1.mp4.md)

Also, make sure “Rule Set Parameterization” is set to “Random Selection”, with the checkbox “Use Current Rule Set as Baseline” ticked. This is because we have a valid baseline strategy that we want to improve more. With that checkbox ticked, you can ensure the Divine Engine will always give you results that are as least as good as the current strategy. Now, if a baseline is not valid (not complete), let's say you don't know what Ranking Rules to use and rather have the Divine Engine find them for you, you must disable that checkbox, even if you supplied other rules/filters yourself. Ticking on that checkbox only works if you have a valid baseline strategy.

* * **4.**  You can leave the rest of the properties here at their default values. But I will reduce the “Population Size”, “Min. Generations”, and “Max. Generations” so the Divine Engine run won't take too long.

[https://portfolioboss.com/wp-content/uploads/2021/05/9hgkj345fgh23.mp4](_wp-content_uploads_2021_05_9hgkj345fgh23.mp4.md)

As well, I decided to increase “Mutation Rate” to 20% so there's a little more variation in the filters and their values.

* * **5.**  Then, set whatever [“Fitness Function”](_documentation_backtest-parameterization-panel.md#FitnessFunctions) you see fit according to your trading goals. As for me, I choose CAGR, for the greatest profit possible.

[https://portfolioboss.com/wp-content/uploads/2021/07/789ryhdgzs.mp4](_wp-content_uploads_2021_07_789ryhdgzs.mp4.md)

I also added “R²”. That will give me a more consistent strategy, with no big surprises either up or down. As for the “Exit Conditions”, I decided not to use them, because the “Max. Generations” value is already low. I don't want the Evolutionary progression to be truncated even shorter.

* * **6.**  Now let's go back to the rules/filters we supplied before. We'll tell the Divine Engine to keep the filters we believe are useful. While a filter that's dubious for the well-being of the strategy shall be judged by the Divine Engine. If it proves to be useless or detrimental, it will be replaced by a new one.

[!](_wp-content_uploads_2020_07_Replaceable-NotReplaceable-Parameters.png.md)

To do that, look at the left-most parameter of each filter that says [“Not Replaceable”](_documentation_backtest-parameterization-panel.md#NotReplaceable). You can click on that dropdown and choose either “Not Replaceable” or “Replaceable”.

[!](_wp-content_uploads_2020_07_Filters-Replaceable-Flags.png.md)

In my case, I leave the SMA filter (and the ranking rule) as “Not Replaceable”, which means the Divine Engine won't replace them. They will stay no matter what. The Aroon filter though, is set to “Replaceable”. Its fate is up to the Divine Engine to decide, whether it will be replaced by another filter or not.

* * **7.**  Let's now start the Divine Engine backtest. You can run the test locally now, or queue it for later. But we usually recommend running big tests in the cloud: Press the button ! as usual. A [confirmation dialog](_documentation_design-strategies-from-scratch_.md#BossDialog) appears, informing you of the estimated compute credit consumption for this backtest:

!

Simply click OK, and look at the [Divine Engine Results Tab](_documentation_backtest-results-tab_.md): there's another item at the top that's currently “Running”. This is your current Divine Engine backtest. The other item (below it) is the previous Divine Engine run you did.

!

You can click on each [“Backtest Item”](_documentation_backtest-results-tab.md#TheBacktestItemsList) to see its contents. So, each “Backtest Item” contains its own set of top strategies, as well as its own [“Fitness Series Chart”](_documentation_backtest-results-tab.md#TheFitnessSeriesChart).

!

Obviously, the Backtest Item that's currently running is not yet fully populated with top strategies. We'll wait it out to finish. In the meantime, you can use Portfolio Boss as usual. You're not locked out waiting for the Divine Engine to finish.

Even better, you can load one of the top strategies fresh out of the oven, to see what rules and filters it contains, even as the backtest is still running.

[https://portfolioboss.com/wp-content/uploads/2022/11/gyuioi56wh5a.mp4](_wp-content_uploads_2022_11_gyuioi56wh5a.mp4.md)

If after a long time you don't see any better strategies listed at the top, you may cancel the backtest. Simply click the “Cancel” button on the running Backtest Item:

!

You may also cancel a backtest if the Brown, Cyan, and/or Green lines (on the “Fitness Series” chart) drops to very low values. That tells you that the evolutionary progression only yields worse performing strategies, thus you manually kill the process. If you used the Exit Conditions, termination happens automatically.

* * **8.**  Once the cloud backtest is finished, you can load one of the top strategies by clicking the [“Load Parameters”](_documentation_backtest-results-tab.md#LoadParameters) buttons ! . In my case, here's the content of the highest performing strategy:

[!](_wp-content_uploads_2020_07_Resulting-Strategy-Rules-0-00-00-00.png.md)

As you can see, the barebone strategy is now augmented with the new rules/filters. And those filters we set to “Not Replaceable” are still there. Surprisingly, the Divine Engine decided that the Aroon oscillator is actually useful, despite some value changes.

What's once a 50,000-percentage return strategy with 76% Drawdown, has now become a strategy with 50,000,000-percentage return and an acceptable 50% Drawdown, despite a short evolutionary progression.

!

So in summary, the steps are very similar to the previous scenario, where you use the [“Evolutionary”](_documentation_backtest-parameterization-panel.md#Evolutionary) search and the property “Rule Set Parameterization” adjusted to “Random Selection”. Except here you supply your own filters you believe will benefit the strategy. The Divine Engine will then add new filters (or replace existing ones that are dubious), to take your barebone strategy to the next level.

* * **Note:**

If the baseline contains Cyber Code rules (from a top strategy you loaded that used the [Cyber Code engine](_documentation_cyber-code-genetic-programming_.md)), they'll have the flag “Not Replaceable” permanently set (grayed out). These Cyber Code rules will stay no matter what, with its contents (codes) fixed. The idea is that a Cyber Code evolution and a standard evolution (which we discussed in this page) are mutually exclusive: the Divine Engine either adds random built-in rules, or adds/evolves the Cyber Code rules, not both. If you don't want a Cyber Code rule to be part of your baseline, simply delete it. If you want the Cyber Code rule to evolve further, set the property “Rule Set Parameterization” to “Generate Cyber Code” as discussed in the Cyber Code page (which means the new random rules added by the Divine Engine will be of the Cyber Code type exclusively, not of the built-in type).

[!](_wp-content_uploads_2021_05_5r6ydegdst4e3.png.md)

[**Back to Top**](_documentation_augmenting-a-strategy-with-new-rules_.md#backtotop)

You have already reported this .

#### _documentation_automation-tab-guide.md

> Source: https://portfolioboss.com/documentation/automation-tab-guide
> Scraped: 3/1/2026, 2:09:22 AM

[!](_wp-content_uploads_2019_10_Automation-Tab.png.md)

This Tab allows you to define:

*   the email (or text) notification settings,
*   whether Portfolio Boss automatically runs at Windows start-up,
*   and how long to wait for the late price data.

* * **1.**  “Automatically start Portfolio Boss on Windows startup”: Toggling this ON allows Portfolio Boss to run automatically every time you start Windows.

[!](_wp-content_uploads_2019_10_Automatically-Start-PB-on-Startup.png.md)

Generally, it is advisable to run Portfolio Boss at least a few hours after the market closes, since market data and trading signals will be processed during this time. And keep in mind, email/text notifications (about trading signals, current positions, etc) will only be sent to you if Portfolio Boss is _running_. There's _no need_ to backtest the strategy yourself (by pressing the Start button) for those e-mail notifications to be generated; they're automatically backtested provided the End of Day data have finished downloading.

If you trade on _various global exchanges_, it is advisable to keep PB running 24 hours so you don't miss out on any signals.

* * **2.**  “Send email notification for strategies that have notifications enabled”: Toggling this ON allows Portfolio Boss to send you the email (or text) notifications about the activities on your strategies.

[!](_wp-content_uploads_2019_10_Send-Email-Notification-checkbox.png.md)

Now the most important thing is, even though you have enabled this checkbox and fill out your email & phone number, you must still enable the “Notifications” checkbox on the strategy (or strategies) that you want to output notifications from.

The “Notifications” checkbox is located at the [“Strategy Management”](_documentation_strategy-management-page-overview_.md#notifspacer) page, on the far right column of that strategy.

[!](_wp-content_uploads_2019_10_Strategies-Notification-Checkboxes.png.md)

Or, when you go to the “Backtest Strategy” page, there's the [“Enable Notifications”](_documentation_strategy-panel-guide_.md#enablenotif) checkbox.

[!](_wp-content_uploads_2019_10_Backtest-Strategy-Enable-Notifications.png.md)

The notification is sent daily, whether the strategies have trading signals or not; and it contains information about the trading signals (if there's any), your current Positions, as well as the Top Ranked instruments (indication of what might become the next buy signals):

!

Keep in mind, trading signals are sent to you one trading day _before_ the signals are supposed to be executed. So if you receive the signals, enter the orders at the same day, and they will be executed at the next trading day.

* * **3.**  “E-Mail Addresses”: at this field, you can enter your email address where the notifications will be sent. Once you typed it, press Enter on your keyboard (or the little “Plus” button on this field).

[!](_wp-content_uploads_2019_10_E-Mail-Addresses-Field.png.md)

Once you fill this field, another empty field shows up where you can enter another email address, or, your _email-to-text_ number.

[!](_wp-content_uploads_2019_10_Type-Here-to-Add-Another-Email.png.md)

Entering your email-to-text number allows Portfolio Boss to send SMS notifications to your phone; this notification is short and concise, so any details you might want to know can be read on the email notification instead.

For example, Verizon users can enter this text: phonenumber@vtext.com (let's say 5551234567@vtext.com ).

[!](_wp-content_uploads_2019_10_Email-to-Text.png.md)

Other carriers' email-to-text commands are:

*   AT&T = phonenumber@txt.att.net
*   T-Mobile = phonenumber@tmomail.net
*   Sprint = phonenumber@messaging.sprintpcs.com
*   Virgin Mobile = phonenumber@vmobl.com

Please contact your mobile carrier if they provide SMS Gateway.

* * **4.**  “E-Mail Service Provider”: here you can choose from the various email services to receive the notifications from. We recommend using the “Portfolio Boss Mail Service” as it is the most reliable: no login information or technical configurations required.

[!](_wp-content_uploads_2019_10_E-Mail-Service-Provider_00000.png.md)

If you opt to use “Yahoo”, “Google”, or “Windows Live” mail services, two fields appear (below the “E-Mail Service Credentials”) where you can enter your Username and Password to log into those mail services.

[!](_wp-content_uploads_2019_10_E-Mail-Service-Credentialss_00000.png.md)

Now, if your email service is not listed here, you can select “Specify other” and fill out the configuration fields below, such as the mail server address, port, your username, and password. 

[!](_wp-content_uploads_2019_10_Specify-Other-Email_00000.png.md)

The “Use SSL” checkbox defines whether this e-mail provider is secured with the Secure Sockets Layer.

* * **5.**  “Send a test email”: You can press this button to see whether Portfolio Boss can actually send the notification to your email. 

[!](_wp-content_uploads_2019_10_Send-a-Test-Email-Buttonn_00000.png.md)

If it's successful, a test email from Portfolio Boss will reach your inbox; if it's not, you may check whether your e-mail address is typed correctly, or you can contact our [Customer Support](mailto:support@portfolioboss.com) for more details.

Now, there are some cases where Portfolio Boss Mail Service suffered some problems, hence you don't receive the daily notifications. You can check the status of the Mailing Service by visiting the [**Portfolio Boss Status Page**](https://status.portfolioboss.com/):

!

This page shows the status of various Portfolio Boss services, including its Mailing Service, historical price data downloads, The Boss supercomputer service, Smart Money data, and various market indicators e.g. ETF True Asset Prices and Grayscale cryptocurrency ETFs data. Make sure you visit this page if such services are interrupted.

* * **6.**  “Late Data Waiting Limit”: So, Portfolio Boss will send notification as soon as the _End of Day_ price data have finished downloading, but some instruments' price data may become available _late_. Portfolio Boss will _wait_ for these price data before sending you notifications. 

[!](_wp-content_uploads_2019_10_Late-Data-Waiting-Limit_00000.png.md)

With this parameter, you can set how long Portfolio Boss will wait. For example you set it to 2 hours, which means Portfolio Boss will wait _until_ 2 hours _before_ the next market opens; then it will send the notification with or without the late data.

You can check the [status page](https://status.portfolioboss.com/) to see if there are indeed problems with the historical price data services:

!

[**Back to Top**](_documentation_automation-tab-guide_.md#backtotop)

You have already reported this .

#### _documentation_average-currency-volume-filter.md

> Source: https://portfolioboss.com/documentation/average-currency-volume-filter
> Scraped: 3/1/2026, 2:08:35 AM

[!](_wp-content_uploads_2019_10_Average-Currency-Volume-Filter-000.png.md)

[!](_wp-content_uploads_2019_10_Average-Currency-Volume-Sell-555.png.md)

This filter is all about the liquidity of an instrument. It looks at an instrument's “average currency volume” for the past several days/months (that you specified), and if it's greater or less than the “average currency volume” that you you specified, the instrument will be bought (or sold).

“Average currency volume”, also known as “Dollar Volume Liquidity” is not just the number of shares traded (its volume); it is actually the volume multiplied by the share's _unadjusted_ closing price. This is then averaged for the past period of time that you specified (e.g the average of the past 30 days). So, the “Average Currency Volume” is specified in dollars, not volume.

This filter is useful, for example, if you don't want to trade stocks that have low liquidity; such stocks' positions are generally difficult to enter or exit, which may cause huge slippage and loss of unrealized gain. But you can also look for lower volume stocks if you wish so; they may provide faster growth than the larger volume stocks. Of course, what dollar volume you're looking for depends very much on your account size; you don't want to trade on low liquidity instruments if you have a larger account.

* * **1.**  The first Parameter defines the time period to calculate the Average Currency Volume. Let's say you want the average of the past 30 days, then enter 30 days here (type 30 and choose from the dropdown either Days or Months). 

[!](_wp-content_uploads_2019_10_Average-Currency-Volume-Filter-1st-Parameter-000.png.md)

Longer period gives a more accurate estimate, but if you're a short-term trader adjust this accordingly (you don't want outlier liquidity to be considered).

* * **2.**  The second Parameter defines whether the average must be “Greater than” or “Less than” the dollar volume that you specified, for the instrument to be considered. 

[!](_wp-content_uploads_2019_10_Average-Currency-Volume-Filter-2nd-Parameter.png.md)

You can also decide whether the average must fall “Between” or “Not Between” (outside) the maximum and minimum dollar volumes that you specified on the third and fourth parameters that show up.

[!](_wp-content_uploads_2019_10_Average-Currency-Volume-Filter-2nd-Parameter-Between.png.md)

* * **3.**  The third and/or fourth parameters define the threshold dollar volume.

[!](_wp-content_uploads_2019_10_Average-Currency-Volume-Filter-3rd-Parameter.png.md)

[!](_wp-content_uploads_2019_10_Average-Currency-Volume-Filter-3rd-4th-Parameters-000.png.md)

You have already reported this .

#### _documentation_average-percent-range-apr-filter.md

> Source: https://portfolioboss.com/documentation/average-percent-range-apr-filter
> Scraped: 3/1/2026, 2:08:43 AM

[!](_wp-content_uploads_2020_08_APR-Buy-Filter.png.md)
[!](_wp-content_uploads_2020_08_APR-Sell-Filter.png.md)

This filter calculates the volatility of an instrument during a certain period, and if such volatility falls within the set criteria, a Buy (or Sell) signal is given.

Unlike other volatility filters, the volatility here is calculated similar to the Average True Range (ATR). Whereas ATR gives the volatility reading in dollar value (how many dollars a given instrument moves per day, on average), this filter converts that dollar value into percent.

[!](_wp-content_uploads_2020_08_Expensive-Stock-Stable.png.md)

[!](_wp-content_uploads_2020_08_Cheap-Stock-Volatile-333.png.md)

The idea is this: volatility stated in dollar value is very subjective. An average movement of $15 per day might not be much for a stock priced at $1000, but the same $15 movement for a $300 stock is considered very volatile. Therefore, converting such volatility into percent (relative to the instrument's price) allows for a more objective judgment. This is especially true for Portfolio Boss, where hundreds (if not thousands) of instruments with different price range are calculated at once. Even the same instrument could have different prices across different periods. Thus for our purposes, we believe Average Percent Range (APR) gives a fairer volatility reading than the Average True Range.

* * **1.**  The first parameter defines the lookback period for the volatility.

[!](_wp-content_uploads_2020_08_APR-First-Parameter.png.md)

For example with a period of 50 days, the average volatility is calculated from 50 days ago until the latest date (today). If today's APR thus falls within the threshold APR, the buy (or sell) signal is given.

Generally, a longer period is preferable (upward of 50 days), so the volatility reading is more accurate. A shorter period may not smooth the outlier volatility enough (temporary spike in price), hence giving false signals. But there are cases where both a longer period and a shorter period are used at once (with two filters), to exploit a temporary divergence in volatility.

* * **2.**  The second parameter defines where the instrument's APR must fall (in relation to the threshold APR) for the signal to be given.

[!](_wp-content_uploads_2020_08_APR-Second-Param.png.md)

You can choose here, whether the instrument's APR must be “Greater Than”, “Less Than”, “Between”, or “Not Between” the threshold APR. Generally, a Buy Filter is best set to “Greater Than”, while “Less Than” is good for a Sell Filter. The reason is that higher volatility gives higher return, so you buy (but beware of higher risk too). And when volatility is low, it could be that price is trapped in a trading range.

[!](_wp-content_uploads_2020_08_Flash-Crashes.png.md)

But sometimes the reverse is true (in a primary bull market, for example): price tends to drop much more violently & quickly when volatility is high, while the uptrend is a slow grind with lower volatility. So, set this parameter according to your strategy's characteristics.

* * **3.**  The third parameter defines the threshold APR, where instruments' APR are compared against.

[!](_wp-content_uploads_2020_08_APR-Third-Parameter.png.md)

Instruments' APR are usually less than 15%, so set this parameter to such a small value (3, 6, 7, 14, etc). A high APR threshold (like 50% or more) gives too much leeway for the instruments' APR, hence inaccurate signals. Besides, such a high APR is rarely encountered, so the strategy may stay in cash most of the time.

* * *

Sometimes, a volatility indicator by itself is not enough: it doesn't take into account whether price is going up or down. So it's a good idea to supplement this with another filter. For example, aside from the spike in volatility, another filter is used to identify a young uptrend (or the end of a downtrend). Hence the high volatility represents investors' eagerness to take the price even higher, instead of panicked selling:

[!](_wp-content_uploads_2020_08_APR-and-ARO-Buy-Filters.png.md)

In the example above, the [Aroon Oscillator (ARO) Filter](_documentation_aroon-oscillator-filter_.md) is set to identify the end of a downtrend (i.e “Above ARO -60”). Then coupled with the increase in volatility (i.e “APR Greater Than 6%”) we have a confirmation of a strong upward momentum.

You can even use this APR filter twice: one Buy Filter uses a shorter period, while another Buy Filter uses a longer period. As stated somewhere above, this technique is used for exploiting temporary divergences in price volatility:

[!](_wp-content_uploads_2020_08_APR-and-APR-Buy-Filters.png.md)

In summary, you can pair this filter with other filters as you see fit, building upon the general ideas set out in this Chapter 7.

* * **Notes:**   As stated above, the APR calculation is slightly different from ATR (aside from the fact that ATR doesn't yield percentage values). Unlike ATR, APR does not take into account the previous day's close (just the difference between a day's lowest and highest prices). This is the correct way for stock and ETF prices. Because ATR, on the other hand, was originally developed for commodities' futures prices.
*   At the [Instrument Tab](_documentation_instrument-tab_.md), there's an APR indicator below the price chart. Change the APR Filter's period parameter to change this indicator's appearance.

[!](_wp-content_uploads_2020_08_APR-Indicator.png.md)

[**Back to Top**](_documentation_average-percent-range-apr-filter_.md#backtotop)

You have already reported this .

#### _documentation_average-true-range-atr-filter.md

> Source: https://portfolioboss.com/documentation/average-true-range-atr-filter
> Scraped: 3/1/2026, 2:08:44 AM

[!](_wp-content_uploads_2020_07_Dow-Theory-Short-Filter.png.md)

[!](_wp-content_uploads_2020_07_Dow-Theory-Sell-Filter.png.md)

This filter looks for downtrending instruments based on a subset of Dow Theory that states a downtrend happens when there are lower lows and lower highs.

[!](_wp-content_uploads_2020_07_Dow-Theory-Diagram.png.md)

In general terms, this filter looks for a price drop, and then a rebound which peaked **lower** than the previous high, and finally a **breach** of the previous low, thus completing the lower-low and lower-high pattern in a downtrend. In short, this filter is best used a sell filter–or better yet, as a short filter. Although you can add this as a buy filter, the downtrend pattern recognition doesn't make sense to be used as a buy filter.

This filter allows you to define how large of a drop and subsequent rally by utilizing the instrument's Average True Range (ATR). ATR is a price volatility reading, that tells you how much the price **usually** moves per day, during a specified period. You can also define how long such a downtrend pattern should complete, by customizing the period parameters on this filter, to conform with your trading duration.

* * *

Now let's get to the parameters:

**1.**  The first parameter defines the period for calculating the ATR.

[!](_wp-content_uploads_2020_07_Dow-Theory-First-Param-000.png.md)

This ATR, in turn, will be used to define the size of the price drop and subsequently rally (as illustrated by point A and B on the previous diagram). A common ATR period is 14 days, but we found the default of 20 days to be good overall. Obviously you can set this shorter or longer depending on your trading duration. Make sure though, that this ATR period doesn't stray too far from the period parameters explained next–for defining how long the pattern should complete. If you set this ATR period too high or too low, the pattern may not actually be representative of a downtrend, thus giving false signals.

[!](_wp-content_uploads_2020_07_Dow-Theory-Price-Action.png.md)

As a little technicality, this ATR period is calculated not from the latest date–i.e today, but from the second peak. For example, an ATR period of 20 days means the ATR is calculated from that peak all the way to 20 days ago from there. Thus it tells you how many dollars the price usually moves per day, during that 20 days period.

* * **2.**  The second parameter defines the size of the **first** drop.

[!](_wp-content_uploads_2020_07_Dow-Theory-Second-Param.png.md)

For example, a value of 4 here means the first drop is 4 times the ATR. So, if the ATR is 2 dollars, the drop would be 8 dollars. Keep in mind that the drop does not necessarily happen in a single day; it could span many days to reach that bottom. Also, the first drop does not necessarily happen from a perfect peak; it could've been calculated from the middle of a drop.

[!](_wp-content_uploads_2020_07_Dow-Theory-First-Drop-0-00-00-01.png.md)

The default value for this parameter is 4. If you set this at a very high value, you're essentially waiting too long for that drop to happen, thus the downtrend may already be exhausted–in case of short selling–or your long position has suffered too much losses before the sell signal is given. Besides, it's rare for instruments to drop so much, so sell signal may not be given at all. Note, this bottom is the closing price of the lowest candle.

* * **3.**  The third parameter defines the size of the **rebound** after the previous drop.

[!](_wp-content_uploads_2020_07_Dow-Theory-Third-Param.png.md)

So after the price dropped toward that bottom specified previously, it rallied toward a peak whose height is defined in this parameter. Generally, you want to set this parameter at a lower value than the previous parameter, thus essentially you're finding a “lower-high”, i.e a peak lower than the previous peak. You can set this at either half the previous parameter, a third, or two-third, because they're the usual heights for a downtrending lower-peak. For example, with a value of 2 here–which is the default value–the price rebounds 2 ATR after that bottom. If the ATR is 2 dollars, that means a rally of 4 dollars from the previous bottom price.

[!](_wp-content_uploads_2020_07_Dow-Theory-Rebound-0-00-00-00.png.md)

* * **4.**  The fourth and fifth parameters define how long it takes for the price to rally–from the previous bottom–and then drop again breaching that bottom.

[!](_wp-content_uploads_2020_07_Dow-Theory-Fourth-Fifth-Params.png.md)

For example, you set them to 10 and 15 days, which means it will take anywhere from 10 to 15 days–it could be 10, 11, 12, 13, 14, or 15 days–for the price to leave that previous bottom, peaking, and finally breaching the previous bottom level. In other words, the duration for the mountain pattern, from bottom, peak, to bottom again. Once the price **closes** below that bottom, a sell signal will be given, because the lower-low and lower-high pattern has been completed, signalling a downtrend.

[!](_wp-content_uploads_2020_07_Dow-Theory-Mountain-Duration-0-00-00-00.png.md)

Note, you can set these two parameters at the same exact value, which means the duration for the mountain pattern will be exact. Let's say you set them both to 10 days, then it will be exactly 10 days from the bottom, peak, and bottom again. For that reason, it's better to set these two parameters as a “window”, instead of an exact value, because different instruments may complete the pattern at different periods.

Set these two values based on your trading duration, i.e lower value for shorter duration, and higher value for longer duration. Beware if you set this too short, you may only get noise and false signals, and stopped out all the time, where the instrument may not actually be in a downtrend. The maximum you can set here is 30 days.

* * **Notes:**   The tool-tip description says liquidated positions go to cash-equivalent. This is not always the case, depending on whether you use cash or cash-equivalent for the strategy. This filter works just as any normal filters.
*   The drop and rebound do not necessarily happen at exactly the values you set (for example 4 and 2 ATRs respectively), but could be a little off from that. As long as the bottom and peak's candles capture the specified ATR height (within their high and low of the day), then it's fine.
*   The duration for the whole pattern to complete is usually 150% of the last parameter. For example, if the last parameter is set to 20 days, then the whole thing from the first peak, drop, rally, to breach takes about 30 days. In other words, each drop or rally takes about one half of that period parameter–or 33% of the whole thing.

[**Back to Top**](_documentation_average-true-range-atr-filter_.md#backtotop)

You have already reported this .

#### _documentation_backtest-panel-guide.md

> Source: https://portfolioboss.com/documentation/backtest-panel-guide
> Scraped: 3/1/2026, 2:08:11 AM

[!](_wp-content_uploads_2021_05_New-Backtest-Panel_00000.png.md)

This Panel is used for defining the strategy's backtest range (time period), and the index (benchmark) to compare against. You can also define the in-sample and out-of-sample periods for the backtest, so you'll know how the strategy performs in uncharted waters. By comparing its performance between the two different time periods, you'll know whether the strategy stays consistent.

This Panel is located at the bottom of the [Rules Area](_wp-content_uploads_2021_05_gdg56ye5dg_00000_00000.png.md) (on the “Backtest Strategy” page).

* * **1.**  **To define an index (benchmark)** to compare against the strategy's performance, use the property “Compare to Benchmark”. Obviously, the benchmark must be related to the strategy's Portfolios, so that the statistical results are comparable. 

[!](_wp-content_uploads_2021_05_Compare-to-Benchmark-2_00000.png.md)

For example, if you're trading stocks, you don't want to input a commodity index in here. Instead, input something like the SPX (for S&P 500) or RUI (for Russel 1000). The benchmark you set here will be shown on the [“Chart” Tab](_documentation_chart-tab_.md) (the blue graph).

Simply type in the symbol in this parameter (or any search terms); a dropdown menu then shows up listing the instruments that match your search. Look at the Asset-Class column (2nd from the right) to see _whether_ the instrument is an _index_, and choose the one you want. 

[!](_wp-content_uploads_2019_10_SPX-dropdown.png.md)

If you're sure the symbol you typed here is correct, simply press enter on your keyboard without selecting from the dropdown. You can also input an ETF here instead of an actual index (let's say QQQ for representing the Nasdaq 100 index). Note, the longer the benchmark has been around, the longer your backtest range will be, thus yielding a more accurate result.

To view the historical price data of that index, simply click the little “Chart” button ! at this property. You'll be taken to the [“Instrument” Tab](_documentation_instrument-tab_.md) (at the Reports Area) where you can see the price chart.

[!](_wp-content_uploads_2021_05_23293279_00000.png.md)

Note, you can't input a delisted instrument here (a symbol with a number suffix within the _square brackets_). If you do so, there's a warning on this property, and your strategy becomes invalid (it can't be backtested):

!

* * **2.**  **On the “Initial Amount” property,** you can enter your initial account balance in dollar value (it's optional, you can leave it at 0).

[!](_wp-content_uploads_2021_05_353467464_00000.png.md)

You can see how much that initial capital grows during the whole backtest period by looking at the [Metrics Tab](_documentation_metrics-panel-guide_.md) (located at the Reports Area), on the item “Total Amount” . 

[!](_wp-content_uploads_2021_05_3532242_00000_00000.png.md)

This is the total money you'd get if you were to trade with this strategy for the same period.

* * **3.**  **“Date From” property:** here you can set how far back the backtest will be processed. Usually, you want to set this to “Earliest Date Possible”, thus the backtest period will be stretched to the oldest date allowed by the strategy. 

[!](_wp-content_uploads_2021_05_9785453523_00000.png.md)

Look at the _date_ shown on this property to get an idea how far back it can go.

Such oldest date is influenced by some factors:

*   how long the [cash-equivalent](_documentation_system-settings-panel-guide_.md#positionreplacements) instrument has been around (PTSHX is older than SHY, for example);
*   how old the Portfolios' [instruments](_documentation_portfolio-instruments-panel-guide_.md) are;
*   how old the _benchmark_ is;
*   how old the various _indices_ used on the Buy and Sell filters are.

Portfolio Boss looks at the earliest date on each of those items, and the earliest date that's the most recent among them (the lowest common denominator) is selected. It then looks at the strategy's rules (technical indicators), and finds which indicator has the most recent _start-line_; for example between 14-day RSI and 200-day SMA, obviously the SMA indicator-line starts 186 days later (more recent) than the RSI line. And this will be the earliest date for the backtest.

Now, as stated before, instruments (indices) used on filters & rules also affect the earliest date. This can be problematic if they're young, thus cutting short the backtest period even more. You may opt out of them _until_ they become available.

!

To do that, choose the option “Earliest date, ignoring rule instruments”.

!

So that any filter containing an instrument (index) won't be used by the strategy _until_ the instrument becomes available in the market. In the example screenshot above, the ROC Index Filter won't be used to exit any Positions _until after_ 23 days since QQQJ was available on the market (where its 23 days ROC can be calculated). This could be useful if you're curious how the strategy performs if the backtest range is extended to the past; though admittedly it's not _exactly_ the same strategy that treads that extended period (but that'd be fine if only one or two filters were deactivated).

You can also set this property to “Set Manually” if you want to set a certain date yourself. On the date field that shows up, you can _type_ a date and press enter on your keyboard. You can type a long or short date format here, either with spaces or dashes. 

[!](_wp-content_uploads_2021_05_ge5y46t33t_00000.png.md)

For example, type “7 dec 03” (or dec 7 03)  and this field will automatically update to 7-Dec-03.

If you simply want to fine tune one day forward/backward, click this field and press the up/down arrow on your keyboard. Note, this parameter is about trading dates, not calendar dates; thus it automatically skips holidays and weekends.

Or, you can click the little “Calendar” button !   to set the date using a Calendar interface.

[!](_wp-content_uploads_2021_05_sfsf8687_00000.png.md)

Note that once you set a manual date, it will be remembered for that strategy, even if you restarted PB (or reverted back to “Earliest date possible”). Just go back to “Set Manually” and it'll be there.

* * **4.  “Date To” property:** here you can set the end-date of the backtest period. Usually, you want it set to “Latest Date Available”, which means the backtest range ends at your current date (today). But if _today_ is a holiday/weekend, this date is set to the the last time the market opened. 

!

There's a note below, that notifies you how long to wait for the next available price data.

You can also set the date manually by choosing “Set Manually” in this property; which then shows the date field below it. You can set the date either with the “Calendar” button, or type in a date as already explained above.

[!](_wp-content_uploads_2021_05_lkjslgfi98868_00000.png.md)

* * **5.**  **The section “In Sample Periods”** lets you distribute the strategy's historical price data into In Sample (IS) and Out of Sample (OOS) periods.

[!](_wp-content_uploads_2021_05_fghhrf3563647967_00000.png.md)

“In Sample Period” is a portion of the historical data (from the strategy's Portfolio) used for crafting and fine-tuning the strategy; whereas “Out of Sample Period” is the portion used as a proving ground on how the strategy performs in untested _historical data_. They're used to compare the strategy's performance in different market conditions; whether or not it stays generally consistent. The key word here is “consistent” performance.

So we're not talking about the strategy's overall performance (for the whole historical data), but rather its performance split into multiple periods (multiple market conditions). We can see whether it performs generally the same for **each** and **every** period. If it does, then we are definitely confident it will perform similarly once it's put to real use with real money (that is, the forward performance, as opposed to its “back” test with historical data). We won't get any nasty surprises.

Let's discuss the properties here:

*   **Number of In Sample Periods** – This defines the amount of In Sample Periods to use. The historical price data is then divided into this many In Sample periods, and (usually) as many Out of Sample Periods. For each IS Period, there's an OOS period; the historical data is divided alternately this way. Normally, traders use 1 IS Period and 1 OOS Period (if they use OOS Period at all). But with this property, you can have more than 1 IS Period, with the maximum of 10. Imagine if you use but one period, it's like generalizing the strategy's performance over the long term. The first 4 years it goes up, then the last two years it goes down. It's good to know its _overall_ performance, but it would be even better if it is continually consistent for _each short term period_ it goes through, instead of the total _eventual_ performance. Note: a value of 3 or 5 is generally good here, unless you have a much longer historic price data. You don't want each period to be too short; each In Sample Period must contain at least 1 year's worth of data.

*   **Total In Sample Ratio** – This defines the percentage of the historical data that goes toward the In Sample Period. The rest goes toward the Out of Sample Period. For example you set this to 70, that is 70% for the IS and 30% for the OOS. This 70% of the total historical data is then dispersed equally through the many IS periods you have (set in the previous property). If you use one or two IS Periods, generally you want to set this to 70 or 80 percent. But the more IS Periods you have (5 or more), the smaller each period becomes; so you better use the same percentage for both IS and OOS (set this to 50 percent). The reason being, with a small slice of data for each period, you don't want the OOS to become even smaller by assigning it 20 or 30 percent. That would be too short to accurately gauge the OOS performance. The result would be a lopsided performance where the IS is noticeably lower-performing than the OOS (OOS just needs to weather much shorter market conditions than the IS).

*   **First Date Period is In Sample** – Ticking this checkbox assigns the earliest historical data to be a part of the In Sample Periods. Using the oldest data for crafting the strategy, i.e. for the In Sample, is the norm that most traders use.

*   **Last Date Period is In Sample** – Ticking this checkbox assigns the latest historical data to be part of the In Sample Period. This causes one of the In Sample Periods to be adjacent to the _real future_ (the forward performance). Though this is not the norm, it _may_ yield a better strategy, as its rules are more relevant to the present instead of the old past.

*   **The Periods bar** – This bar shows the visual distribution of the IS and OOS periods throughout the entire historical data, based on the percentage and the number of periods you use. White spans are for the In Sample Periods, and gray for the Out of Sample. You can hover your mouse over a certain span, and a tooltip appears showing the exact date range for that span.

[!](_wp-content_uploads_2021_05_adfs97978afs_00000.png.md)

The strategy's equity curve (as shown on the [Chart Tab](_documentation_chart-tab_.md)) is also divided into similar white and gray spans:

[!](_wp-content_uploads_2021_05_3e4t5sgfsfs_00000.png.md)

Each span has its own performance, hence its own metrics score. They're then averaged (from the multiple spans) to yield the final metrics score. For example we have five IS Periods (as shown in the screenshot above), with these CAGR each: 20%, 30%, 30%, 25%, and 35%. The strategy's final CAGR (In Sample) is thus 140% divided by 5 is 28%. The final CAGR for Out of Sample is calculated the same way.

Most metrics are calculated with this average. But some, like Max. Drawdown, use the maximum score of all the spans. Others use the summation of all the spans, such as the Total Trades metric.

You want to make sure the metrics performance for both IS and OOS are generally the same; it says a lot about the strategy's _consistency_. Take a look at the [Metrics Tab](_documentation_metrics-panel-guide_.md) and compare each metric:

[!](_wp-content_uploads_2021_05_853t3edhdgh464_00000.png.md)

Also look at the Efficiency value. You don't want it too low below 100% or too high; if that's the case, there's disparate performance between IS and OOS, and the strategy is inconsistent. Though it's still tolerable to have Efficiency far above 100%, generally it's advisable to get it as close to 100% as possible. The Efficiency value is calculated from dividing the OOS score by the IS. Note: instead of checking each metric one by one, there's one vital metric to rule them all, i.e. “Score”. This metric combines Drawdowns and CAGR all at once. At the very least, make sure this one metric is generally the same between IS vs OOS.

**Note:**

You can get hard-core in defining the strategy's OOS period with the **“Date to”** property. That is, you set it to “Set manually” instead of the “Latest date available”, and then put a date a couple of months (or even years) back from today. That way, the backtest period doesn't cover everything. Once the strategy is created & backtested and you're satisfied with its performance, reveal the rest of the backtest period by setting the “Date to” property to the “Latest date available”. Now do the backtest again to see if its performance stays consistent _even today_. You'll be surprised: some strategies fare worse, while others perform much better. This is Dan's term of “super out-of-sample”, often used for more rigorous [Divine Engine](_documentation_the-divine-engine-and-the-boss_.md) backtests.

You can also use such trick on the “Date from” property (“Set manually” instead of “Earliest date possible”). In essence, some parts of the historical data are hidden even to Portfolio Boss itself.

* * **6.**  Finally, to backtest your strategy, press the “Start” button at the top-left corner of this page.

!

A confirmation dialog appears, allowing you to add a memo for this backtest:

!

If you don't want this dialog to appear each time you start a backtest, tick the checkbox “Don't show again”. Once done, click the button “Continue” to actually start the backtest. A memo is _optional_, as it's simply a description about a backtest _run_. Each run (and its memo) will be seen under the [Manual Results Tab](_documentation_manual-results-tab_.md):

!

Now an “Executing Backtest” dialog shows up to show the backtest progress:

[!](_wp-content_uploads_2019_10_Executing-Backtest-Dialogue.png.md)

Sometimes, the latest price data (on the portfolio) have not been downloaded yet, so you must wait (PB will pop up a dialogue saying such thing). But you can choose to run the backtest anyway with the available data, though the backtest may not be accurate.

[!](_wp-content_uploads_2019_10_Historic-Price-Data-being-downloaded.png.md)

In some cases, the price data is almost entirely not downloaded yet, for example when you just installed Portfolio Boss. In such case, you can't run the backtest until most of the data are downloaded. Sometimes price data couldn't be downloaded because there are troubles with the CSI download & processing service; you can check the [**Portfolio Boss Status Page**](https://status.portfolioboss.com/) if such is the case:

!

* * *

#### Important:

*   You can replicate _previous_ trading signals (shown on the [“Trade Signals” Tab](_documentation_trade-signals-panel-guide_.md)) by assigning the “Date To” parameter at _one day prior_ to the strategy's [switch-day](_documentation_system-settings-panel-guide_.md#monthlyswitch). For example, the strategy's switch-day is the 2nd trading day of the month. 

!

Assuming that day is not a holiday or a weekend, then set the “Date To” parameter at the 1st trading day. If it's a holiday/weekend, look at the next market open, and set the date one day prior to that. 

!

In essence, the “Date To” parameter acts as if you're currently on that date.

!

For trading signals other than the switch-day, you can set the “Date To” parameter at one day prior to the Buy/Sell actions (arrows) as shown on the instrument's price chart ([Instrument Tab](_documentation_instrument-tab_.md)).

!

*   Backtesting does not necessarily mean you're comparing against the benchmark. Doing a backtest yields statistical results that you may use to compare against _another_ _backtested strategy_. This is because inherently, a benchmark is just an index, not a strategy.

*   Don't forget to re-run the backtest once you have modified the strategy's rules, so you can look at the new stats. It's perfectly okay to run the backtest many times.

[**Back to Top**](_documentation_backtest-panel-guide_.md#backtotop)

You have already reported this .

#### _documentation_backtest-parameterization-panel.md

> Source: https://portfolioboss.com/documentation/backtest-parameterization-panel
> Scraped: 3/1/2026, 2:08:12 AM

!

This panel defines how the Divine Engine backtest is performed. But most importantly, it allows you to tell the Divine Engine the criteria you want in the strategies it produced. This panel shows up only when the Divine Engine is enabled.

[https://portfolioboss.com/wp-content/uploads/2021/05/ghkjigh4gjf221.mp4](_wp-content_uploads_2021_05_ghkjigh4gjf221.mp4.md)

Behind the scene, there are so many things going on in this panel. In this guide, we'll explore every concept thoroughly. We'll discuss how exactly the Evolutionary progression is performed, the tournaments, the cross-breeding and mutation, the rotational fitness, the calculation of fitness score, and many more.

This page is divided into four segments:

* [Evolutionary](_documentation_backtest-parameterization-panel.md#Evolutionary)
* [Random](_documentation_backtest-parameterization-panel.md#Random)
* [Fitness Functions](_documentation_backtest-parameterization-panel.md#FitnessFunctions)
* [Other Properties](_documentation_backtest-parameterization-panel.md#OtherProperties)

Here's the full list of properties contained in this panel (top to bottom, based on how they appear):

* [Search Algorithm](_documentation_backtest-parameterization-panel.md#Evolutionary)
* [Population Size](_documentation_backtest-parameterization-panel.md#PopulationSize)
* [Cross-breeding Rate](_documentation_backtest-parameterization-panel.md#Cross-breedingRate)
* [Mutation Rate](_documentation_backtest-parameterization-panel.md#MutationRate)
* [Min. Generations](_documentation_backtest-parameterization-panel.md#Min.Generations)
* [Max. Generations](_documentation_backtest-parameterization-panel.md#Max.Generations)
* [Execute N Random Backtests…](_documentation_backtest-parameterization-panel.md#ExecuteNRandomBacktests...)
* [Number of Parameter Steps](_documentation_backtest-parameterization-panel.md#NumberOfParameterSteps)
* [Number of Parameter Combinations](_documentation_backtest-parameterization-panel.md#NumberOfParameterCombinations)
* [Tournament Type](_documentation_backtest-parameterization-panel.md#TournamentType)
* [Tournament Fitness Function Rotation](_documentation_backtest-parameterization-panel.md#TournamentFitnessFunctionRotation)
* [Rule Set Parameterization](_documentation_backtest-parameterization-panel.md#RandomizeRules)
* [Randomize Ranking Rule Offsets](_documentation_backtest-parameterization-panel.md#RandomizeRankingRuleOffsets)
* [Use Current Rule Set as Baseline](_documentation_backtest-parameterization-panel.md#UseCurrentRuleSetAsBaseline)
* [Fitness Function](_documentation_backtest-parameterization-panel.md#FitnessFunctions)
* [Exit Conditions](_documentation_backtest-parameterization-panel.md#ExitConditions)
* [Average In-Sample Population Fitness Rate of Change Exit Condition](_documentation_backtest-parameterization-panel.md#AverageIn-SamplePopulationFitnessRateOfChange)
* [In-Sample/Out-of-Sample Moving Average Rate of Change Divergence Exit Condition](_documentation_backtest-parameterization-panel.md#In-SampleOut-Of-SampleMovingAverageRateOfChangeDivergence)
* [Moving Average In-Sample Population Fitness Exit Condition](_documentation_backtest-parameterization-panel.md#MovingAverageIn-SamplePopulationFitness)
* [Moving Average Out-of-Sample Population Fitness Exit Condition](_documentation_backtest-parameterization-panel.md#MovingAverageOut-of-samplePopulationFitness)
* [No New High for Out-of-Sample Moving Average Exit Condition](_documentation_backtest-parameterization-panel_.md#NoNewHighOOSexitCond)

It's highly recommended that you familiarize yourself first with the Divine Engine and The Boss by following the tutorials [here](_documentation_the-divine-engine-and-the-boss_.md).

Note this is a huge page, so if some images don't show up, please refresh/reload the page.

* * *

### Evolutionary

**1.**  **Search Algorithm** – This is the most important property, as it defines the search algorithm used by the Divine Engine.

!

This property fundamentally changes how the Divine Engine works in finding the best strategies. With “Evolutionary” algorithm, the Divine Engine utilizes the Evolutionary progression to create higher performing strategies: it builds up from earlier, lower-performing strategies as the foundation. Whereas the [“Random” algorithm](_documentation_backtest-parameterization-panel.md#Random) lets the Divine Engine to employ brute force to achieve its goal.

!

By changing this property you change most properties on the Backtest Parameterization panel, to conform with the search mode you selected. Therefore we'll start with the Evolutionary mode and discuss the properties related to it.

!

Evolutionary mode is best suited to create strategies from scratch, or to augment an existing strategy with new rules and filters.

* * **2.  Population Size** – This property defines the amount of strategies contained within each generation.

!

Let us discuss first what happens at the beginning of the evolution: the Divine Engine populates the 1st Generation with diverse strategies. In the screenshot above, for example, it creates 64 different strategies.

[https://portfolioboss.com/wp-content/uploads/2020/09/First-Generation-Creation-Clip.mp4](_wp-content_uploads_2020_09_First-Generation-Creation-Clip.mp4.md)

There are two ways to do this: if you start from scratch without supplying any rules and filters, the Divine Engine adds random rules and filters (along with their random values) for each one of the 64 strategies. On the other hand, if you have an existing strategy, the Divine Engine creates other strategies as variations of your “baseline” strategy.

Such variations may come from:

*   Your [parameterizations](_documentation_fine-tune-a-strategy-for-the-best-settings.md#Parameterization), thus other strategies contain the same rules you supplied but with different values (specified within your parameterization range).
*   The rules you set to [“Replaceable”](_documentation_backtest-parameterization-panel.md#ReplaceableNotReplaceable) (or [“Random”](_documentation_backtest-parameterization-panel.md#RandomDropdown)), thus some strategies contain those rules, while others don't.
*   And finally, variations may come from the fresh new filters added by the Divine Engine itself. Thus one strategy contains the filters A, B, C, while another strategy contains X, Y, Z.

!

!

!

Notice, the value you set on “Population Size” must be a multiple of 4. This is due to the tournament mechanism that requires 4 strategies to do battle (will be explained later). Also, it's best to set “Population Size” to a smaller value, like 64 or 128, and then do multiple Divine Engine backtests simultaneously.

[https://portfolioboss.com/wp-content/uploads/2022/11/547547es5thawb5.mp4](_wp-content_uploads_2022_11_547547es5thawb5.mp4.md)

We've found that a smaller Population Size may increase the likelihood of finding better performing strategies, in contrast to a large bunch of population at once (like 256). By doing multiple backtests with smaller Population Size, you can simulate [“the island effect”](https://en.wikipedia.org/wiki/Foster%27s_rule): an evolutionary idea where different groups of people (or organisms) develop independently of each other, without being dragged down by the others' “bad gene” or fierce competition.

Then, to find the best 20 strategies from the multiple backtests, take a look at the [Overall Top Results Tab](_documentation_overall-top-results-tab_.md):

!

**Notes:**   The Population Size represents the amount of CPU cores utilized by the Divine Engine. Thus with 64 size, you'll consume 64 CPU cores at any given time, with each strategy consuming 1 CPU core. If you have 3 simultaneous backtests, it follows that 192 cores will be used.
*   Thus a larger Population Size will increase backtest time, if CPU cores in the cloud are currently shared with other users. Therefore a smaller size will get you the best of both worlds.
*   When the Divine Engine adds the new filters, there are limits: the amount of Buy, Ranking, or Sell Filters is each capped at 10 per strategy, including the ones you add yourself. Thus the Divine Engine won't add new filters if there's no room for them. Strategies often contain less than these limits, unless you fill it to the brim with your own filters/rules. If you exceed the limit, the filters set to “Replaceable” may get removed until such a limit is respected again. Those filters you set to “Not Replaceable” will stay no matter what, even if they exceed the limit.

* * **3.  Cross-breeding Rate** – This property defines the percentage of offspring created through cross-breeding (sex between parent strategies). Or put another way, it defines the amount of parent strategies that are willing to marry.

!

But we haven't discussed what happens after the 1st Generation was created. So let's continue our Evolutionary discussion: after the 1st Generation was created, these 64 strategies are backtested to find their [Metrics'](_documentation_metrics-panel-guide_.md) values. Therefore each strategy has their Score, CAGR, Drawdown, MAR, Sharpe, and other Metrics reported.

[https://portfolioboss.com/wp-content/uploads/2020/09/First-Generation-Backtesting-clip.mp4](_wp-content_uploads_2020_09_First-Generation-Backtesting-clip.mp4.md)

Once done, they'll do the tournaments to define the survival of the fittest. Each tournament consists of 4 strategies battling each other. These 4 strategies are pulled randomly from the pool of 64. Therefore with a Population Size of 64, we'll have 16 tournaments.

[https://portfolioboss.com/wp-content/uploads/2020/09/First-Generation-Tournament-clip.mp4](_wp-content_uploads_2020_09_First-Generation-Tournament-clip.mp4.md)

During the tournament, the 4 strategies are sorted top to bottom based on the [Fitness Function](_documentation_backtest-parameterization-panel.md#FitnessFunctions) criteria that you set. For example, if you used CAGR as the Fitness Function, the 4 strategies are sorted based on their CAGR values. The top two strategies with the highest CAGR are kept as survivors, while the bottom two are destroyed. The tournament repeats for other strategies until the pool is empty, and we're left with the 32 survivors. The pair of strategies that survived each tournament will become parents for their offspring.

These 32 survivors are now part of the 2nd Generation. The Divine Engine will then “repopulate” this Generation with their offspring. This is when each pair (the two survivors of each tournament) cross-breed. But not all parents will cross-breed; some choose to simply clone themselves to produce their offspring. This parameter “Cross-Breeding Rate” defines what percentage of parents will cross-breed, and the rest will simply clone themselves.

[https://portfolioboss.com/wp-content/uploads/2020/09/2nd-Generation-CB-Clone-clip.mp4](_wp-content_uploads_2020_09_2nd-Generation-CB-Clone-clip.mp4.md)

For example, with a “Cross-Breeding Rate” of 80%, there will be 80% of survivors to cross-breed, while 20% will clone themselves. Regardless, every pair will create another pair of offspring. Thus 32 survivors will produce exactly 32 offspring, replenishing the Population Size to its original 64 size.

Now, what happens exactly during cross-breeding? Cross-breeding essentially means: the two parent strategies pooled their respective rules together, and the children are given random rules picked from that pool. For more clarity, take a look at these illustrations:

[https://portfolioboss.com/wp-content/uploads/2020/09/CrossBreeding-Detail-clip.mp4](_wp-content_uploads_2020_09_CrossBreeding-Detail-clip.mp4.md)

As you can see above, cross-breeding happens in all System Settings, Buy Filters, Ranking, and Sell Filters panels. For the System Settings panel, children are given random rules (picked from the parents' System Settings pool) until their System Settings panel is entirely populated & valid.

For the Buy Filters panel, children are also given filters picked randomly from the parents' Buy Filters pool. The amount they're given is anywhere from the 1st Parent's amount to the 2nd Parent's amount. Let's say the 1st Parent contains 3 Buy Filters, while the 2nd Parent has 5 Buy Filters. A child therefore may contain 3, 4, or 5 Buy Filters. The Sell Filters and Ranking Rules have the same mechanism. Note, a child is not allowed duplicate rules, i.e two rules with the exact same type and values.

This mechanism is further influenced by the [Mutation Rate](_documentation_backtest-parameterization-panel.md#MutationRate), that is, with a higher mutation, a child is more likely to get a different amount of rules than its parents. Continuing with the example above, instead of a random amount between 3 and 5 filters, the child may be assigned anything from 1 to 10 amount of filters (if you use a high mutation rate, that is). In other words, the range is extended  by decreasing the lower bound (3), and increasing the upper bound (5). It is so, because with higher mutation we want the offspring to be more different than their parents. And since the parents have only 8 _distinct_ rules between them (3 and 5), should the child be given more than 8 slots, it will be capped at 8.

Essentially, cross-breeding is not about modifying the rules' values, but simply plucking random rules from the parents. A lower Cross-Breed rate means cloning is more prevalent. This may negatively affect the Evolutionary progression as strategies have less variations between them, thus little or no performance growth throughout the generations.

**Notes:**   The tournaments do not actually use the Metric's actual value (e.g CAGR's percentage), but rather that Metric's value normalized into a factor of 1. This is the “Fitness Score” that serves as the basis for the tournament. If you have multiple Fitness Functions, the Metrics' values are combined and normalized as well. We'll discuss about this [later](_documentation_backtest-parameterization-panel.md#NormalizingFitness).
*   The Fitness Score is calculated from the Metric's performance during the [In-Sample period](_documentation_backtest-panel-guide.md#insampleratio). This is deliberate so that the Divine Engine is “blind” and does not overfit the Out-of-Sample period as well.
*   During cross-breeding, a user-supplied rule that's set to [“Not Replaceable”](_documentation_backtest-parameterization-panel.md#NotReplaceable) (or [“Enabled”](_documentation_backtest-parameterization-panel.md#RandomDropdown)) will always be part of the children, regardless of its current form due to [Parameterization](_documentation_fine-tune-a-strategy-for-the-best-settings.md#Parameterization).

* * **4.  Mutation Rate** – This property defines the percent chance that a “randomizable thing” will be randomized again.

!

You may wonder, what's a “randomizable thing”? To answer that question, let's continue with our Evolutionary discussion: after the offspring are created (through cross-breeding and cloning), they'll undergo the mutation phase. That is, mutation does not happen for the parent strategies.

[https://portfolioboss.com/wp-content/uploads/2020/09/2nd-Generation-Mutation-clip.mp4](_wp-content_uploads_2020_09_2nd-Generation-Mutation-clip.mp4.md)

During mutation, a strategy's “randomizable things” may become randomized again. Such “randomizable things” include:

*   Parameters which are [parameterized](_documentation_fine-tune-a-strategy-for-the-best-settings.md#Parameterization) by you. For example, you supplied a filter “Simple Moving Average (SMA) Position” and parameterized the period parameter, with a range of 10 to 300 days and a step of 10 days. The Divine Engine may then “randomize” that period parameter again, picking a value that falls within 10 to 300 days with a step of 10 days. If a parameter is not parameterized, it will stay no matter what with the value you set.

!

*   Rules that are set to [“Replaceable”](_documentation_backtest-parameterization-panel.md#ReplaceableNotReplaceable) or [“Random”](_documentation_backtest-parameterization-panel.md#RandomDropdown). For example, you supplied your own “RSI Filter” and flagged it as “Replaceable”. Then it may be replaced with another rule picked randomly by the Divine Engine (with its random values as well).

!

*   Rules added by the Divine Engine (not you!) have the flag “Replaceable” automatically set to it. Thus the entire rule may get replaced by another rule.

!

*   All parameters of a rule added by the Divine Engine. So, a rule added by the Divine Engine not only has the “Replaceable” flag set, but all its parameters may get “randomized” again based on the Divine Engine's own parameterization ranges.

!

So in essence, each of those “randomizable things” takes a dice roll on whether it will be randomized again. A higher “Mutation Rate” means there's a higher chance that it will get mutated to obtain a new value (or a new rule). Hence more variation in the rules & values between strategies (diverse gene).

Be careful if you set the “Mutation Rate” too high: the Evolution may not be able to build from the previous generations, as the “DNA” is wrecked and replaced by new ones completely different from the parents.

* * **5.  Min. Generations** – This property defines the _minimum_ amount of Generations the Divine Engine will create.

!

We're at the full 2nd Generation now, let's continue where we left off: After the offspring are created through cross-breeding, cloning, and subsequently mutated, they will be backtested to find their Metrics' performance. This is similar to what happened previously (in the 1st Generation), except that now only the offspring are backtested. Parent strategies obviously have been backtested in the 1st Generation, so we don't need to check their Metrics' performance again.

[https://portfolioboss.com/wp-content/uploads/2020/09/Backtesting-2nd-Generation-Offspring-clip.mp4](_wp-content_uploads_2020_09_Backtesting-2nd-Generation-Offspring-clip.mp4.md)

Then all strategies within this 2nd Generation, parents and offspring alike, do battle between each other. The tournaments happen again with the exact same mechanism as already described. The survivors then become parents for the 3rd Generation, and these parents cross-breed and clone themselves to produce offspring in the 3rd Generation. Offsprings are then mutated, and the whole 3rd Generation do tournaments all over again. This cycle continues for at least the “Min. Generations” that you set here.

[https://portfolioboss.com/wp-content/uploads/2020/09/Evolutionary-Cycle-Summary-clip.mp4](_wp-content_uploads_2020_09_Evolutionary-Cycle-Summary-clip.mp4.md)

Therefore “Min. Generations” is the absolute minimum amount of generations that the Divine Engine creates, no matter what. Let's say you set it to 20, then 20 Generations it will be.

The larger the “Min. Generations”, the longer the backtest time will be.

* * **6.  Max. Generations** – This property defines the _absolute maximum_ amount of generations (that may or may not be created).

!

After the “Min. Generations” are created (in our example 20 Generations) then the [Exit Conditions](_documentation_backtest-parameterization-panel.md#ExitConditions) kick in. We'll explain about them in a moment. But essentially, they're the criteria for stopping the Evolutionary progression should it only produce lower and lower performing strategies. Like a hawk, they watch each generation's performance, deciding whether or not the Evolution must be stopped. For example, if at the 20th Generation the Exit Conditions are hit, there'll be no more tournaments, no more cross-breeding, cloning, and mutation. There will be no 21st Generation.

[https://portfolioboss.com/wp-content/uploads/2020/10/Exit-Condition-Overview-clip.mp4](_wp-content_uploads_2020_10_Exit-Condition-Overview-clip.mp4.md)

Conversely, if none of the Exit Conditions are hit, the cycle continues until the “Max. Generations”. Let's say you set it to 70, then 70 Generations will be created. That's the absolute maximum. There will be no more after that. The cycle stops no matter what.

[https://portfolioboss.com/wp-content/uploads/2020/09/Exit-Condition-not-Hit-clip.mp4](_wp-content_uploads_2020_09_Exit-Condition-not-Hit-clip.mp4.md)

A higher “Max. Generations” mean a longer backtest time. But the Evolution could mature enough with such a longer “timeline”, and you'll be rewarded with high-performing strategies. But sometimes, a longer “timeline” is a waste of compute power if subsequent generations only yield lower (or at least the same) performing strategies over and over again. That's the reason you use Exit Conditions. If you don't use Exit Conditions at all, the Divine Engine _will always_ create strategies up to the “Max. Generations” that you specified.

* * **7.  Exit Conditions** – This section of the Backtest Parameterization Panel allows you to add and customize the Exit Conditions.

!

So we've touched the general idea of Exit Conditions. We'll get into the details, but first we must finish our Evolutionary discussion. We'll discuss the concept of “Average Fitness Score”, and how the top strategies are picked:

The 1st Generation contains a set of population, let's say 64 strategies; and each strategy has its own [Fitness Score](_documentation_backtest-parameterization-panel.md#NormalizingFitness). If you use CAGR as the Fitness Function, then each strategy's Fitness Score is calculated from the _in-sample_ CAGR. This CAGR value is then normalized into a factor of 1, to yield the final Fitness Score.

[https://portfolioboss.com/wp-content/uploads/2020/09/Fitness-Score-Gen-1-clip.mp4](_wp-content_uploads_2020_09_Fitness-Score-Gen-1-clip.mp4.md)

The Divine Engine then calculates the average of the Fitness Score from those 64 strategies. This is the “Average Fitness Score” of the 1st Generation. In addition, the strategy with the highest Fitness Score is recorded as one of the “Top Strategies”, which you'll eventually see at the [Divine Engine Results Tab](_documentation_backtest-results-tab_.md).

This process (of finding the Average Fitness Score and the Top Strategy) continues for subsequent generations. From the 2nd Generation onward, the top strategy that's picked is the best strategy from each Generation's _offspring_.

That's because the 1st Generation's top strategy, being a survivor and a top parent, will always be the top strategy of the next generations _unless_ there's an offspring strategy that can beat it. So the Divine Engine continually watches (and picks) the best offspring of each Generation, to see if they can beat the old man.

[https://portfolioboss.com/wp-content/uploads/2022/11/t67d57ndre6es.mp4](_wp-content_uploads_2022_11_t67d57ndre6es.mp4.md)

When the Evolution reaches its end, the Divine Engine picks 20 (or less) high-performing strategies from the last Generation, not just the Top Strategy there. It's so that results from the ultimate terminus of the Evolutionary progression are not wasted, based on the idea that the last Generation should benefit from all Generations behind it.

Thus our Evolutionary discussion ends, with the Top Strategies served to you. Now you may wonder, what use is the “Average Fitness Score” then? Well it serves as the input for the Exit Conditions, and we'll get to it as we explain each Exit Condition.

So let's see what types of Exit Condition we have, by clicking the button **Add Exit Condition**:

!

That opens a dialog, where you see we have four different Exit Conditions:

!

*   Average In-Sample Population Fitness Rate of Change
*   In-Sample/Out-of-Sample Moving Average Rate of Change Divergence
*   Moving Average In-Sample Population Fitness
*   Moving Average Out-of-Sample Population Fitness
*   No New High for Out of Sample Moving Average (this is the default Exit Condition)

Select any of those Exit Conditions (by ticking their checkbox), and press OK to add them.

**Average In-Sample Population Fitness Rate of Change:**

!

This Exit Condition stops the evolution if the _Average Fitness Score_ drops (across many generations) below the threshold Rate of Change that you specified here.

[https://portfolioboss.com/wp-content/uploads/2022/09/r567n46ee656a.mp4](_wp-content_uploads_2022_09_r567n46ee656a.mp4.md)

Do you recall the [Average Fitness Score](_documentation_backtest-parameterization-panel.md#AverageFitnessScore) we discussed earlier? This Exit Condition tracks the percentage change (also known as the **Rate of Change**) of the latest Generation's “Average Fitness Score” and the “Average Fitness Score” of N Generations ago. Let's say the Evolutionary progression is currently at Generation 25, and its “Average Fitness Score” is 0.70. We look back ten generations (including the current generation), that's Generation 16, and its “Average Fitness Score” is 1.5. Thus from Generation 16 to 25 we have a drop of -53%. Such a large drop warrants the termination of the Evolutionary progression.

!

The first parameter defines the “period”, so to speak, for the Rate of Change. So if you set it to 10, the Exit Condition looks back “10 generations”, including the latest Generation. Obviously this is a moving window, so if we're currently at Generation 25, then it looks back at Generation 16. And if the Exit Condition is not met, the Divine Engine creates the Generation 26, thus we look back at Generation 17, and so on and so forth.

[https://portfolioboss.com/wp-content/uploads/2022/09/75e674w6hn3w563w.mp4](_wp-content_uploads_2022_09_75e674w6hn3w563w.mp4.md)

It is best to set a longer “period” here, so the Exit Condition is more forgiving (wider tolerance). If you set a shorter period, thus a tighter “window”, you'll get stopped out all the time as extreme fluctuations usually happen in the short term. It may reduce the chance of finding better performing strategies as the Evolutionary progression hasn't matured enough.

!

The second parameter defines the threshold Rate of Change (in percent). If the RoC (Rate of Change) across 10 generations falls below this threshold RoC (the percentage change is less than this threshold), the Exit Condition is hit and the Evolution stopped. Usually, we want to set this parameter at either 0%, or a big negative percentage (let's say -50%). The former indicates that we only want a “generally increasing” Fitness Score to happen instead of a decline; even if there are declines, we hope they happen for only a few generations, not a long term decline. The latter (-50%) is actually more useful, as the Evolution won't be stopped unless there's extreme RoC drop, in which case the next generations are more likely to be losers.

[https://portfolioboss.com/wp-content/uploads/2022/09/785563eb54aw5aq.mp4](_wp-content_uploads_2022_09_785563eb54aw5aq.mp4.md)

We don't want this parameter set to a high RoC, as that means we don't tolerate the little gradual changes (even the little negative changes) inevitable in an Evolutionary progression. High RoC is not sustainable in the long run: as the Evolution can't keep up with such a high standard, it may get stopped prematurely. Remember that this is an Exit Condition, whose sole purpose is to stop a bad Evolution, not as a fitness criteria that you want in a strategy.

**In-Sample/Out-of-Sample Moving Average Rate of Change Divergence:**

!

Quite an intimidating name for this Exit Condition, and rightfully so, as it's a combination of five concepts:

*   the “Average Fitness Score” in-sample,
*   the “Average Fitness Score” out-of-sample,
*   the “N generations Moving Average” for those two “Average Fitness Score” above,
*   the “N generations Rate of Change” for each of the Moving Averages above, and finally
*   the delta (a.k.a divergence) between those two Rates of Change.

[https://portfolioboss.com/wp-content/uploads/2022/09/r467wbah5qvaes.mp4](_wp-content_uploads_2022_09_r467wbah5qvaes.mp4.md)

*   First, the “Average Fitness Score” in-sample, we've already discussed about this extensively.
*   Second, the “Average Fitness Score” out-of-sample, is similar to the previous one, except the Metric's performance is taken during the out-of-sample period.
*   Third, the “N generations Moving Average”, plots a Moving Average line for the “Average Fitness Score” across the generations. It's similar to the Moving Average of stock prices, but here the “price” is replaced with each generation's “Average Fitness Score”. And instead of “N days” as the Moving Average period, we use “N generations”. The Moving Average is plotted for each of the in-sample and out-of-sample “Average Fitness Score” graphs.
*   Fourth, the “N generations Rate of Change”, calculates the percent difference (Rate of Change) between the latest generation's Moving Average value and the Moving Average value N generations back. This is also done for each of the in-sample and out-of-sample “Average Fitness Score” graphs. Thus we have two Moving Average RoCs: one for the in-sample performance, another for the out-of-sample performance.
*   Finally, find the difference (subtract) these two RoCs, to yield the “RoC Divergence”.

The idea here is to stop the Evolutionary search if there's great inconsistency (great divergence) between the in-sample performance and the out-of-sample performance throughout the generations. That is, in-sample “Average Fitness Score” only increases throughout generations, while the out-of-sample “Average Fitness Score” (for the exact same strategies) only decreases throughout the generations. If we continue the Evolution, the Divine Engine may yield top performing strategies indeed, but only for the in-sample period. The out-of-sample performance, on the other hand, is underwhelming. We don't want such inconsistent strategies, as their backtest performance may as well be fake, and you may lose your hard-earned money investing in them. Note, such inconsistency (great divergence) may also apply if the out-of-sample performance is much greater than the in-sample.

!

The first parameter defines the “period” for both the Moving Average and the Rate of Change. If you set it to 10, for example, there are 10 generations' worth of “Average Fitness Score” that will be smoothed-out to produce the Moving Average. Ditto the Rate of Change compares the Moving Average that spans 10 generations.

You may wonder why are we using Moving Average instead of the Average Fitness Score themselves? The answer is that a Moving Average gives you a more objective view for the long term progression, so the Rate of Change won't get whipsawed by outlier Average Fitness Score (spike up/down) that usually happens short-term.

It's recommended to use a longer “period” for this parameter, so the Evolution won't be stopped prematurely due to such extreme outlier values. Remember this is an Exit Condition, and we don't want the Evolution to be stopped, unless there's a chronic (long term) divergence.

!

The second parameter defines the threshold divergence (a.k.a. difference, or delta) between the in-sample RoC and the out-of-sample RoC. Let's say we put this threshold at 50%, and the former RoC is 30% while the latter RoC is -40%, thus a delta of 30% – (-40%) = 70%. That's a large divergence, much greater than our threshold at 50%, so the Evolution is stopped, as future generations may only yield greater inconsistency between the in-sample and out-of-sample performances.

Preferably, set this threshold at a higher percentage, so the Evolution won't get stopped by temporary small divergences that are bound to happen.

**Moving Average In-Sample Population Fitness**

!

With this Exit Condition, the Evolution stops if the _latest_ Generation's “Average Fitness Score” drops below the Moving Average line. You're already familiar with the concept of Moving Average for the “Average Fitness Score”. Similar as in stock prices, the Moving Average acts as a “support line” where the Average Fitness Score may rebound and resume its “uptrend”. Therefore if it breached such a strong support, there's a good chance that later generations will have lower and lower score.

[https://portfolioboss.com/wp-content/uploads/2020/10/Exit-Condition-Moving-Average-IS-Population-Fitness-clip.mp4](_wp-content_uploads_2020_10_Exit-Condition-Moving-Average-IS-Population-Fitness-clip.mp4.md)

Note the “Average Fitness Score” is taken from the in-sample period.

!

The only parameter here defines the “period” for the Moving Average. Similar as in stock prices' Moving Average, the longer the period, the stronger it acts as the support line. Therefore if a breach happens, it's a significant signal that a downtrend is imminent, instead of a false positive.

**Moving Average Out-of-Sample Population Fitness**

!

This is similar to the previous one, in that the Evolution is stopped if the “Average Fitness Score” drops below the Moving Average. But the “Average Fitness Score” is calculated from the out-of-sample period.

[https://portfolioboss.com/wp-content/uploads/2020/10/Exit-Condition-Moving-Average-OOS-Population-Fitness-clip.mp4](_wp-content_uploads_2020_10_Exit-Condition-Moving-Average-OOS-Population-Fitness-clip.mp4.md)

The idea is, we don't want subsequent generations to have lower and lower performance for the out-of-sample period. Remember, the Divine Engine was blind to the out-of-sample performance as it was creating the strategies (to avoid overfitting). Thus, as the Divine Engine creates higher performing strategies based on the in-sample period, this Exit Condition makes sure the out-of-sample performance are not decreasing, at the very least.

But that's just half the story, as the Divine Engine may also create lower and lower performance for the in-sample period. So the best way is to use this Exit Condition in tandem with the previous Exit Condition (Moving Average In-Sample Population Fitness). Thus we make sure that both in-sample and out-of-sample performance are not downtrending.

!

The one and only parameter here defines the “period” for the Moving Average. As you already know, a higher value is preferable for a truer signal.

**No New High for Out-of-Sample Moving Average**

!

This Exit Condition looks at the out-of-sample Average Fitness Score (the green line on [the Fitness Series chart](_documentation_backtest-results-tab.md#TheFitnessSeriesChart)), that is: During the specified “period” (including the latest generation), if **there's no** _new all-time high_ for the OOS Avg. Fitness Score, then the evolution is aborted.

!

It could be that the green line (during the period) is all lower than the previous ATH (which is outside the period), or, it simply reached the _same score_ as the previous ATH; in both cases the evolution will be aborted. The idea is that each new high, provided it's not too far separated from the previous one, usually signifies further improvements for the out-of-sample Avg. Fitness Score.

[https://portfolioboss.com/wp-content/uploads/2022/10/yimt67r6e.mp4](_wp-content_uploads_2022_10_yimt67r6e.mp4.md)

So _at least_ the out-of-sample performance for the strategies created are getting better; if not, abort before it consumes too much of your compute hour credit.

There's only one parameter for this, which defines the “period” (the number of generations) to look back, starting from the latest generation. As usual, you don't want to set a short period here, since this is an Exit Condition and you must give some leeway for the evolution to mature.

!

Now, despite the name “… Moving Average”, this Exit Condition does not actually employ Moving Average at all. Instead, it implies the “moving window of generations” for the _Average_ Fitness Score OOS.

**Notes:**   The very first time a strategy has its Divine Engine enabled, an Exit Condition is already added, that is, the “No New High for Out-of-Sample Moving Average” with the “period” set to 10. If you don't want to use this, delete it with the trash-bin icon.
*   Exit Conditions are only available to the Evolutionary search mode. Random search mode doesn't have them.
*   Always remember that Exit Conditions may reduce your chance of finding the best strategy, as the Evolution gets stopped before it matures. So craft the Exit Conditions to meet its intended purpose, that is to cut short a _potentially_ fruitless search (in order to save those precious compute-hour credits). That means setting a wider tolerance for them. Remember, you don't use Exit Conditions to define the criteria you want in a strategy, you use them to stop the Evolution. If the generation amount is small (as defined in the properties Min. & Max. Generations), you may do away with the Exit Conditions altogether.
*   The random nature of Divine Engine backtests means, each run may yield different strategies from the other, even with the same exact settings. So you can use Exit Conditions to stop a fruitless search, and start over with the same settings. Sometimes you can restart PB in order to refresh the “random seed”, and see if the Evolution improves.
*   It's recommended to use just one Exit Condition, so as not to tighten the tolerance and prematurely end the Evolution. But if you decide to use multiple Exit Conditions, do understand that they work like Sell Filters: for the Evolution to be stopped, only one Exit Condition needs to get triggered, not all of them at once. Exit Conditions use the “OR” operator between them, not “AND”.

* * *

### Random

**1.  Search Algorithm** – We'll now delve into the Random search algorithm. Obviously, we'll set this property to “Random” instead of Evolutionary.

!

So now we have different properties shown on the Backtest Parameterization Panel, to conform with the Random mode:

!

The Random mode is much simpler than Evolutionary. In fact it's the original form of the Divine Engine before Evolution was developed. If you're familiar with this [tutorial](_documentation_fine-tune-a-strategy-for-the-best-settings_.md), then you know a lot about the Random mode. This page is only for those craving the nitty gritty technical details.

The Random mode is best suited for fine-tuning a strategy's values. So you have an existing strategy, and you believe in its rules and filters, but you want to find values (of the parameters) that give the best possible performance. Through brute force, the Divine Engine exhaustively tests all possible values and combinations (within your parameterization ranges) and give you the best ones.

[https://portfolioboss.com/wp-content/uploads/2020/10/Random-Search-Overview-clip.mp4](_wp-content_uploads_2020_10_Random-Search-Overview-clip.mp4.md)

Sometimes this is the most sensible thing to do. You don't want to waste time finding a completely new system. You have a system that you trust for years. Let's say, you were a manual trader who used momentum oscillators, like [RSI](_documentation_rsi-filter_.md) and [CMO](_documentation_chande-momentum-oscillator-cmo-filter_.md), along with [Retracement lines](_documentation_retracement-filter_.md) as support and resistance. So you keep those filters, but let the Divine Engine find the best values. Who knows, maybe the 14-days RSI you've been using is not the optimal period? Or that the RSI levels of 70 and 30 are not the best representation of overbought and oversold conditions?

!

Note that a “Random” backtest can only be executed locally in your computer. You do this by clicking the button “Start Local Test”, not the button “Start the Boss”. A confirmation dialog then shows up, allowing you to add a _memo_ for this backtest, along with a warning that a local test may hog all your computer resources:

!

If you don't want this obtrusive dialog to appear each time you start a local backtest, tick the checkbox “Don't show again”. Once done, click the button “Continue” to actually start the backtest. A memo is _optional_, as it's simply a description of each backtest you did. Each backtest (and its memo) can be seen under the [Divine Engine Results Tab](_documentation_backtest-results-tab_.md):

!

* * **2.  Execute _n_ Random Backtests…** – This property allows you to set the amount of iterations to be backtested.

!

An iteration consists of one strategy: a variant of your strategy with its distinct values and combinations. For example, “Iteration 1” contains the [RSI Filter](_documentation_rsi-filter_.md) with the settings “10 days” and “85 RSI level”. Then “Iteration 2” has the settings “28 days” and “65 RSI level”. And so on and so forth.

[https://portfolioboss.com/wp-content/uploads/2020/10/Random-Search-Iterations-clip.mp4](_wp-content_uploads_2020_10_Random-Search-Iterations-clip.mp4.md)

This property contains three fields (of which, only one is user editable):

!

*   **_n_ Parameter Execution Count** – This field can't be customized. It shows the “multiplier” for the amount of iterations. The multiplier is calculated by: (A). Finding how many parameters, or fields, are parameterized by you. (B). Finding the amount of parameterized values, or steps, on a field with the highest amount of parameterized values. (C). Multiply A by B.

!

!

!

The idea for this calculation is that: even if you backtest only the absolute minimum of iterations, not only all values will be tested (parameterized values across all parameters), but some of their combinations as well.

*   **Next is the only field that you can customize**. A number that you set here will be multiplied by the previous “_n_ Parameter Execution Count” to yield the final amount of iterations to be backtested. As stated earlier, you can set this to a value of 1 (which is the logical minimum), and all the different values that you parameterized are certain to be backtested, along with some of their combinations. The maximum value you can enter here is 100.

!

*   **Finally, a field that shows the final amount of iterations to be backtested**. Let's say this field shows “300”, then there will be 300 iterations (300 different strategies) backtested by the Divine Engine. This field can't be edited by you, as it merely shows the result of multiplying the previous two fields.

!

!

Preferably, the amount shown here matches the [“Number of Parameter Combinations”](_documentation_backtest-parameterization-panel.md#NumberOfParameterCombinations). You do this by adjusting the editable field previously explained.

!

Matching them means all parameterized values and all of their combinations will be backtested. Thus you tell the Divine Engine to do its most exhaustive search; not a single value and not a single combination will be left out. But often this means an impossibly huge iteration amount, thus an impossibly long backtest time. If that's the case, you can set the previous user-editable field to a value of 2, 3, or 5.

!

* * **3.  Number of Parameter Steps** – This property is not editable. It shows you the amount of values (steps) that you parameterized, across all parameters.

!

For example on the “RSI Filter”, you parameterized its period parameter with a range of 5 to 25 days and a step of 5. That means there are 5 values parameterized (5, 10, 15, 20, and 25 days).

!

And then the RSI threshold is also parameterized with a range of 0 to 100 and a step of 10. That means 11 different values are parameterized (0, 10, 20, 30, 40, 50, 60, 70, 80, 90, and 100).

!

The ranking rule “PB Pattern Score” also has its third parameter parameterized to include all values there: “PB Velocity Score”, “PB Pattern Score”, and “PB Velocity\*Pattern Score”. Thus we have 3 values parameterized here.

!

So across three parameters above, we have a total of 19 different values parameterized (5 + 11 + 3). As shown on the “Number of Parameter Steps”:

!

If you recall about the property “Execute _n_ Random Backtests…” earlier, even if you set it to a value of 1, not only the 19 values are backtested, but some of their combinations as well. As attested by the final amount of iterations (33) that well exceeds the value of 19:

!

Note, when a rule is set to [“Replaceable”](_documentation_backtest-parameterization-panel.md#ReplaceableNotReplaceable) (or [“Random”](_documentation_backtest-parameterization-panel.md#RandomDropdown)), that means 2 values are parameterized.

!

* * **4.  Number of Parameter Combinations** – This property is not editable. It shows the total amount of combinations from the parameterized values.

!

So, continuing from the previous example ([no. 3](_documentation_backtest-parameterization-panel.md#No3Example) above), we have a total of 165 combinations. This is calculated by multiplying the amount of parameterized values across all parameters: 5 x 11 x 3 = 165.

One “combination” is a distinct mix of different values. For example, the RSI period of “5 days” is combined with the RSI Threshold of “50” along with the value “PB Velocity Score”. That's one combination. The next combination could be the RSI period of “10 days”, RSI Threshold of “70”, and the value “PB Pattern Score”, for example. And so on and so forth.

!

!

Essentially, 1 combination is 1 iteration (1 distinct strategy). That's why as stated earlier, it's best to set the property “Execute _n_ Random Backtests…” to match this property “Number of Parameter Combinations”, so that each and every combination is tested.

!

* * **5.  Pulling the Top Strategies** – Now that we've set the amount of iterations and start the Divine Engine backtest, Top Strategies will be pulled (recorded) to the [Divine Engine Results Tab](_documentation_backtest-results-tab_.md), even as the Random search is progressing.

!

Note, instead of “Gen.” (Generation) as in the Evolutionary search, Top Strategies are listed based on their “Iteration” number. The Iteration that beats a previously listed Iteration (in terms of its “Fitness IS” score) will then be listed on this Divine Engine Results Tab.

Unlike Evolutionary search where backtests are done in the order of earlier Generations toward the later Generations, Random search backtests lower-numbered Iterations and higher-numbered iterations at the same time. Remember that Random search assigns random values & combinations for each Iteration; there's no such thing that higher-numbered Iterations are building up from the lower-numbered Iterations.

This is how the Random search backtest is performed:

[https://portfolioboss.com/wp-content/uploads/2021/05/gfhj5r67fhw3.mp4](_wp-content_uploads_2021_05_gfhj5r67fhw3.mp4.md)

*   In the beginning, the Baseline strategy is backtested. A Baseline strategy is the original strategy you created yourself, with your own values. It is then listed on the Divine Engine Results Tab, as one of the Top Strategies.

*   Then, the first “batch” of iterations are backtested. The amount of iterations on this first batch corresponds to the amount of CPU cores (threads) on your computer. Let's say you have 24 cores, then 24 iterations will be backtested simultaneously (assuming you set the max amount of RAM for PB). And, as stated earlier, lower-numbered Iterations and higher-numbered Iterations alike will be included in this first batch. For example, if we have 1188 iterations (as set on the property “Execute N Random Backtests”), the first batch consists of Iterations 1, 50, 99, 148, 197, 246, 295, 344, 393, 442, 491, 540, 589, 638, 687, 736, 785, 834, 883, 932, 981, 1030, 1079, and 1128. Those are 24 iterations, and between each iteration there's an interval of 49 iterations. This interval is calculated by dividing the total amount of iterations by the amount of cores you have (1188/24 = 49, rounded down).

*   An Iteration that beats the Baseline strategy is then listed on the Divine Engine Results Tab; let's say Iteration 50. Then another Iteration that beats Iteration 50 is also listed there; let's say Iteration 393. So, we have 3 top strategies listed there: Baseline, Iteration 50, and Iteration 393.

!

*   The backtest then continues for the second batch, which is 1 iteration away from the first batch. So the second batch consists of: Iterations 2, 51, 100, 149, 198, 247, 296, 345, 394, 443, 492, 541, 590, 639, 688, 737, 786, 835, 884, 933, 982, 1031, 1080, and 1129. There are 24 iterations as usual, and the top strategies are pulled (recorded) the same way as in the first batch.

*   This continues for the rest of the batches, until all 1188 iterations are backtested. Thus the third batch: Iterations 3, 52, 101, 150… The fourth batch: Iterations 4, 53, 102, 151… and so on and so forth.

!

So why pull multiple top strategies instead of just the one best strategy, if the idea of Random search is to find the best values & combinations? Remember that the Divine Engine is blind to the out-of-sample performance. Thus it could be that the best of the best strategy, despite performing well on the in-sample period, is actually a loser for the out-of-sample period. Besides, different strategies may have different metrics performance (CAGR, Drawdown, etc). So you're given multiple “flavors” to choose from, to suit your preferences.

**Note:** [Exit Conditions](_documentation_backtest-parameterization-panel.md#ExitConditions) don't exist for the Random search. There's no need to stop the backtest on the assumption that “later” iterations have lower and lower performance, no. That's because all iterations are completely independent of each other, they're not building up from earlier-backtested Iterations.

* * **6.  The Mini Chart** – When the backtest is finished, each parameter (that you parameterized) has a Mini Chart. It shows the parameter's performance across the different values that you parameterized.

!

To open this chart, click on the colorful button beside each parameter. The Mini Chart then pops up. Note that Mini Charts are exclusive for Random search; the Evolutionary search doesn't have them, even if you parameterized the parameters.

Let's now discuss the Mini Chart's components:

*   The horizontal axis represents values that you parameterized. Let's say the parameterization range is 5 to 30 days, with a step of 5 days: the horizontal axis thus represents the values 5, 10, 15, 20, 25, and 30 days. Ditto if you parameterized the values “Above” and “Below” (or “Highest” and “Lowest”), the horizontal axis represents those values you chose.

!

!

If you have so many values parameterized, the horizontal axis will be crowded that some values don't have their own labels. But they're still there, plotted correctly.

*   The vertical axis represents the Fitness Score. Obviously, this Fitness Score comes from whatever [Fitness Functions](_documentation_backtest-parameterization-panel.md#FitnessFunctions) you set.

!

We don't show the axis' labels (the Fitness Score scale) as it would clutter the chart more. Instead, you can hover your mouse on the chart to show a tooltip. The tooltip shows the various Fitness Score of a given value.

!

So, you hover the mouse over a certain value, let's say “25”. That value of “25” has four Fitness Score: “Avg. Fitness IS”, “Avg. Fitness OOS”, “Best Fitness IS”, and “Fitness OOS for Best Fitness IS”. Let's discuss them now:

*   “Avg. Fitness IS” – this is represented by the blue line. It shows the values' “Average Fitness Score” for the In-Sample (IS) period. Unlike the Evolutionary's [“Average Fitness Score”](_documentation_backtest-parameterization-panel.md#AverageFitnessScore), the Fitness Score here is the average of all iterations (strategies) that happened to use the value (that you hovered on).

!

Let's say, of all the strategies that used the value “25”, their Fitness Score (IS), averaged, is 4.1.

*   “Avg. Fitness OOS” – represented by the green line. It's similar to the previous one, except now it's for the Out-of-Sample (OOS) period.

!

For example, strategies that use the value “25” (for this parameter) have the Fitness Score during the out-of-sample period averaged as 3.47.

*   “Best Fitness IS” – represented by the orange line. It shows every value's highest Fitness Score during the in-sample period.

!

For example, of all strategies that used the value “25”, there's one strategy with the highest Fitness Score (IS) of 4.96. Thus 4.96 is the “Best Fitness IS” for the value 25.

!

If you look at a parameter's Mini Chart, a value with the highest “Best Fitness IS” (highest orange line) is the value that's deemed best for that parameter and thus applied for it. Such value is shown outside the parentheses (as seen on the screenshot above).

*   “Fitness OOS for Best Fitness IS” – represented by the brown line. This is the Fitness Score during the out-of-sample period, for the strategy with the “Best Fitness IS” (as explained above).

!

For example, of all strategies that used the value “25”, one strategy has the highest Fitness Score in-sample. And that strategy's Fitness Score out-of-sample is shown in this brown line.

Now, sometimes you may encounter a parameter with multiple Mini Charts:

!

This happens if a parameter with built-in values (such as “Above” and “Below”) is parameterized. Thus another parameter (e.g. period parameter) may show multiple Mini Charts, to show its different performance when “Above” and “Below” are used.

!

Keep in mind, the multiple Mini Charts only account for another parameter within the _same_ filter.

**Notes:**   When a rule/filter is set to “Random”, a Mini Chart is also shown next to that “Random” parameter. This is because “Random” means the entire rule is parameterized on whether it should be enabled or disabled. The Mini Chart for this parameter displays a horizontal axis of 0 to 1 (0 means the rule is disabled, while 1 means it's enabled).
*   Different Top Strategies may have different Mini Chart appearance for the same parameter. For example, Iteration 10 has a different Mini Chart appearance from Iteration 50, despite the same SMA Period parameter. This is because: for a Top Strategy that is backtested later (in the last batch for example), its Mini Chart contains more data due to values that have been backtested earlier. Therefore it shows a different Mini Chart appearance from the earlier-backtested Iteration.
*   The original value that you entered (i.e. before you parameterized the field) outside of the parameterization's range, will also be recorded on the Mini Chart.
*   Some Mini Charts are so large their display is truncated. This is usually the case with complex filters. To view the hidden part, you can drag (move) the PB window and then open the Mini Chart again.

* * *

### Fitness Functions

The “Fitness Function” section allows you to define the criteria you want in the strategies created by the Divine Engine.

!

A **Fitness Function** is essentially a metric, such as CAGR, Max.Drawdown, Avg.Position Gain, Sharpe Ratio, etc, which you can find on the [Metrics Tab](_documentation_metrics-panel-guide_.md). The metric(s) that you choose, then, becomes the basis for measuring the strategies' performance. The Divine Engine will try its best to fulfill the metric's performance that you want.

In achieving that goal, the Divine Engine employs Fitness Function in different areas:

*   They're used in the [tournaments](_documentation_backtest-parameterization-panel.md#TournamentMechanism), for defining the survival of the fittest.
*   They serve as the basis for the Avg. Fitness Score, to see whether the Evolutionary progression is healthy (with [Exit Conditions](_documentation_backtest-parameterization-panel.md#ExitConditions)).
*   They're used for picking [top strategies](_documentation_backtest-parameterization-panel.md#AverageFitnessScore) that will be served to you.
*   Finally, Fitness Function is also used for drawing the [Fitness Series chart](_documentation_backtest-results-tab.md#TheFitnessSeriesChart), or the [Mini Chart](_documentation_backtest-parameterization-panel.md#TheMiniChart).

* * **1.**  The very first time a strategy has its Divine Engine enabled, a Fitness Function is already added, which is “Score”.

!

“Score” is good overall as a Fitness Function, but it isn't specific. You may delete it with the trash-bin icon.

To add the Fitness Function(s), click the button “Add Fitness Function”:

!

A dialog appears, allowing you to choose whichever metric(s) you desire:

!

Once they're selected, press the OK button. They're then listed under the “Fitness Function” section:

!

Note that you must have at least one Fitness Function for the Divine Engine to work. This applies to both Random and Evolutionary search algorithms.

* * **2.**  Now we'll define the criteria. We do this by modifying the Fitness Functions' parameters:

!

Each Fitness Function has three parameters, as shown above. We'll discuss each parameter next.

* * **3.**  The first parameter defines how the metrics' value (score) will be pursued. You can pursue as high as possible a value, as low as possible, or _target_ a certain value as _close_ as possible. You can also set a cap (ceiling or floor) in chasing the metric's score.

!
!

As you can see above, we have five values for this parameter:

*   **Goal:** The metric's score will be maintained as close to a target score as possible.
*   **At Most:** The metric's score will be decreased as low as possible. It's only available in Drawdown metrics.
*   **At Least:** The metric's score will be increased as high as possible.
*   **Minimum:** The metric's score will be increased to a minimum value (floor).
*   **Maximum:** The metric's score will be decreased to a maximum value (ceiling).

For example, if you choose “At Least” on the CAGR Fitness Function, the Divine Engine will try to create strategies with as high a CAGR as possible.

!

If you choose “At Most” for the Max Drawdown, it will create strategies with the lowest possible Max Drawdown, if necessary 0%.

!

If you choose “Goal” for the Avg. Trades Per Year, the Divine Engine will create strategies whose amount of trades average about X trades per year. X is the Avg. Trades Per Year you want, let's say 25 trades per year. So the strategies will have as close to 25 trades per year as possible, nothing more, nothing less.

!

Now, “Minimum” and “Maximum” are a bit more complicated. “Minimum” takes the metric score _higher_ to reach the minimum value that you want, but not _really_ pursuing any higher. It could be useful for some metrics like “Avg. Price”, “Avg. Trades per Year”, “Total Trades”, and “Total Trades/Rule Count”. With “Maximum” it's the opposite: the metric score is suppressed _lower_ to reach the maximum value you want, but anything lower is just a bonus. It could be useful to the drawdown metrics.

In other words, they're a bit like “Goal” except they don't mind a better score. If the Maximum (or Minimum) target is _easy_ to reach, for example a “maximum of 50% Avg. Drawdown”, then the Divine Engine will pick whatever strategies as long as their Avg. Drawdown is less than 50%, be they 30%, 10%, or 49%. It won't go out of the way to suppress the drawdown as low as possible.

**Notes:**   We must warn you about the use of Drawdown metrics (either Max.Drawdown, or Avg.Drawdown). If your Fitness Function consists solely of this metric, and it's set to “At Most”, then your strategies are guaranteed to have 0% drawdown. But with 0% drawdown, they're also guaranteed to have 0% return. It's just the basic principle of investing. Now, if you have an existing strategy with good performance, the Divine Engine will break that performance so well, that you'll have 0% return along with the 0% drawdown. Therefore, it's never a good idea to use only the Drawdown metrics as your Fitness Function. Use other return-enhancing metrics as well, such as CAGR. Or at the very least, set those Drawdown metrics to “Goal” instead of “At Most”.

*   Conversely, it's not a good idea to use just the return-enhancing metric, such as CAGR. With very high CAGR, you are likely to get very high drawdown as well. So to put the drawdown in check, use the Drawdown metrics too. If you decide to use just one Fitness Function, then it's highly recommended to use “Score”. The “Score” metric takes into account both CAGR and Max.Drawdown already. In summary, the final Fitness Functions you craft must consider both the return and the risk (expenses & fees too, if you will). To take in-depth tour of the various metrics, read the documentation for the [Metrics Tab](_documentation_metrics-panel-guide_.md).

* * **4.**  The second parameter defines the metric score that you want. This is the score that the Divine Engine will try at least to achieve.

!

For example, as shown above, the Divine Engine will try to create strategies with at most 30% Max Drawdown. Any strategies with Max Drawdown above 30% will be “punished”. They're less likely to survive in the tournaments. And any strategies with Max Drawdown less than 30% (the smaller the better), are likely to survive and generate offspring.

Ditto the CAGR: the Divine Engine will try to achieve at least that 40% CAGR, but the higher the better. As for the Avg. Trades Per Year, it's already explained before. That is, anything less than or more than 25 trades per year will be punished.

Keep in mind, the “punishment” or “reward” is merely semantics. What happens is that, any strategy that falls short of your metric threshold (let's say 35% CAGR instead of 40%), will have a Fitness Score less than 1. And any strategy that exceeds that threshold will have a Fitness Score greater than 1. It could be the case that your threshold is so high (let's say 200% CAGR), that most strategies fall short of that. In that case, even if they have the Fitness Score of 0.6, for example, they'll still trump those strategies with the Fitness Score of 0.4 (besting them in the tournaments). But generally, try not to find a unicorn with your Fitness Functions.

Later on, we'll discuss the [Fitness Score](_documentation_backtest-parameterization-panel.md#NormalizingFitness), and the how & why the metric score is normalized into 1.

* * **5.**  The third parameter defines the “Weight” for each Fitness Function, a.k.a. its “importance”. You can set each weight anywhere from 0 to 999,999. The _actual weight_ applied is shown inside the parentheses (in relation to other Fitness Functions, which add up to 100%).

!

This is especially true if you're using multiple Fitness Functions, so you can set their importance relative to each other. Essentially, weighting allows you to reduce or magnify a Fitness Function's effect in relation to the others (if you only have one Fitness Function, you can set here any number and its _actual weight_ will always be 100%).

This could be useful if you believe a certain Fitness Function could overwhelm other Fitness Functions, hence a lopsided strategy performance. For example, if you maximize Avg. Trades Per Year, its Fitness Score could be well over 1000 (even after it's normalized into 1), whereas CAGR merely has a Fitness Score of 1.5. Therefore the Divine Engine will pursue more trades per year instead of higher CAGR. So the solution is to decrease the weight on Avg. Trades Per Year into a very small value, like 1%, and increase the CAGR's weight to 150%, for example.

So logically, weighting is used to tell the Divine Engine which Fitness Function you'd like to be emphasized. If you like CAGR to be pursued more, then increase the CAGR's weight, and/or reduce the Drawdown's weight. Because if they both have the same weight, it could be that strategies have good Drawdown but underwhelming CAGR.

Good weighting comes after trial and error. So take a look at the Divine Engine's result, and see which metric has abnormally high score, especially if it's not the primary metric you want. Take a look at the [Divine Engine Results Tab](_documentation_backtest-results-tab_.md):

!

In the case of Drawdown metrics, see if they're not abnormally small. If any metric shows aberration, you can adjust its “Weight”, or at least set it to “Goal”. Then do another Divine Engine backtest.

* * **6.**  Fitness Score: Now we'll discuss how the metric(s) score are normalized into a factor of 1, to yield the final Fitness Score.

!

As stated earlier, Fitness Functions serve as the basis for tournaments, exit conditions, and selection of top strategies. But to do those things, Fitness Functions' performance must be converted into a Fitness Score. So for example, it's not just a strategy's _raw_ CAGR of 28.73%, the Max. Drawdown of 19.94%, and R² of 98.81% that will be used. It's these metrics score combined and normalized into 1, which will serve as the basis for tournaments, exit conditions, and top strategy selection.

And here's how the Fitness Score is calculated:

Take a look at the example below, a Top Strategy from Generation 41:

!

It has a Fitness Score (In-Sample) of 1.17, which comes from a CAGR of 47.59% and the R² of 97.16%. Here are the Fitness Functions used:

!

So how do those percentages translate into a Fitness Score of 1.19?

First we must calculate the Fitness Score for each metric (one by one) before we combine them to yield the _final_ Fitness Score. Understand that, in-sample metric scores become in-sample Fitness Score, whereas out-of-sample metric scores become out-of-sample Fitness Score.

The in-sample Fitness Score will be the one used for most purposes, and that's what we'll calculate. Out-of-sample is only useful for some Exit Conditions (like [Moving Average Out-of-Sample](_documentation_backtest-parameterization-panel.md#MovingAverageOut-of-samplePopulationFitness) and [In-Sample/Out-of-Sample M.A ROC](_documentation_backtest-parameterization-panel.md#In-SampleOut-Of-SampleMovingAverageRateOfChangeDivergence) exit conditions). Hence the Divine Engine is usually blind to the OOS performance.

We'll calculate the CAGR's Fitness Score first. Here's the formula:

*   If the metric score exceeds the threshold: 1 + (Delta / Threshold) \* Weight
*   If the metric score misses the threshold: 1 – (Delta / Threshold) \* Weight
*   If the metric score is _exactly_ the same as the threshold, the Fitness Score is _exactly_ 1.

In our case, the 47.59% CAGR obviously “exceeds” the 35% threshold. Remember that we want a minimum of 35% CAGR, the higher the better. So if the CAGR is 23.52% for example, then it “misses” the threshold, thus we'd be using the second formula. In our case, we'll use the first formula:

!

As you can see above:

*   “Delta” is the difference between the metric's score and the threshold value. So it's the difference between the strategy's 47.59% CAGR and the 35% threshold CAGR. Keep in mind that Delta is an absolute value, i.e. always positive, never negative.
*   “Threshold” is obviously the threshold value as set on the Fitness Function. So it's 35% for the CAGR.
*   “Weight” is the weight value set for the Fitness Function. In our case, it's 100% for the CAGR. But note, we don't use raw percentage value here, instead it's a factor of 1. For example, a weight of 100% becomes 1, 90% becomes 0.9, and 7% becomes 0.07. A value greater than 100%, such as 150% becomes 1.5, you get the idea.

So the Fitness Score for CAGR is:

!

### Other Properties

Last but not least, we'll discuss the rest of the properties in this Backtest Parameterization Panel:

!

We'll discuss them based on their order of importance.

* * **1.**  **Rule Set Parameterization** – This defines whether the Divine Engine is allowed to slap random new rules (filters) to your strategy. There are three values for this property:

!

*   _Manual:_ The Divine Engine won't add new rules. So all strategies contain the exact same rules as your Baseline (original) strategy. This is perfect for [fine-tuning your strategy](_documentation_fine-tune-a-strategy-for-the-best-settings_.md) with Random search algorithm (finding the best parameter values for those existing rules).

!

If you choose this value (Manual), each filter may be assigned these flags (at the leftmost parameter, as shown above):

*   *   Enabled: The filter is kept, and exist in all the strategies the Divine Engine created.
    *   Disabled: The filter is discarded, and won't exist in the strategies it created.
    *   Random: The filter is randomly enabled and disabled, to see whether it's actually useful. Thus in some strategies this filter exists, while in others it doesn't.

*   _Random Selection:_ The Divine Engine is allowed to add rules & filters. This is perfect to [create strategies from scratch](_documentation_design-strategies-from-scratch_.md) with the Evolutionary search algorithm. In other words, your Baseline strategy doesn't have to contain any filters.

!

If you choose this value (Random Selection), any existing filter you have may be assigned these flags (at the leftmost parameter, as shown above):

*   *   Not Replaceable: The filter is kept, and exists in all the strategies the Divine Engine created.
    *   Replaceable: The filter is more likely gone in the strategies it created, replaced by another filter.

Note, the random addition of filters may be affected by the number of [parameters (and the value ranges)](_documentation_backtest-strategy-page-overview_.md#Terminology) of each filter. More complex filters _may have_ a higher chance of being added to the strategies. This is because with the wide and deep array of values, it's more difficult for such filters to find good value combinations. On the other hand, less complex filters may have an easier time getting good value combinations.

*   _Generate Cyber Code:_ This option is only available for those with the Cyber Code-capable licenses. It's similar to “Random Selection”, in that the Divine Engine is allowed to add new rules & filters. But instead of the built-in ones such as, RSI, SMA, Kaufman, or Aroon, it creates brand new technical indicators from scratch, whose internal codes are then evolved throughout the generations to create the ultimate indicators.

!

With this option, the rules & filters added by the Divine Engine are exclusively of this “Cyber Code” type (none of the built-in indicators), as opposed to the option “Random Selection”, which adds rules & filters of the built-in type only. So, they are mutually exclusive; either you want the Cyber Code indicators, or the built-in indicators, not both.

You can define how the new indicators are created through the Cyber Code Configuration window, accessed with the button highlighted in the screenshot above. [Cyber Code Genetic Programming](_documentation_cyber-code-genetic-programming_.md) is a huge new feature by itself, so we'll dive deep into it in its own dedicated help page.

**Note:**

The option “Random Selection” can also be used for the Random Search Algorithm. That is, aside from fine-tuning existing parameters, the Divine Engine will also add random rules/filters (with their random values) to the strategies. There is no natural selection and evolution at play here, simply slapping random rules/filters _for every iteration_, in the hope it may beef up the strategies. Obviously rules/filters will be added for as long as there are iterations, as you see on the property “Execute n Random Backtests…”.

!

Therefore it's highly dependent on your _parameterization_ of the existing parameters.

* * **2.  Use Current Rule Set as Baseline** – This checkbox is used in tandem with the option “Random Selection”, explained above.

!

With this checkbox enabled (along with the option “Random Selection”), the Divine Engine is allowed to add new rules, and weigh whether the existing ones are useful. It's perfect for [augmenting your Baseline strategy with new rules](_documentation_augmenting-a-strategy-with-new-rules_.md), utilizing the Evolutionary search algorithm. Ticking it ensures the Divine Engine will always give you results that are at least as good as the baseline strategy. But you must have a valid baseline strategy (complete, with its required rules; e.g. a Ranking Rule is a must). If you don't have a complete baseline and let the Divine Engine find the rest of the rules for you to complete the strategy, turn this checkbox off.

The existing filters may have the flag “Replaceable” and “Not Replaceable” similar to the previous one. But the difference lies in the “Replaceable” flag: instead of discarding the filter, the Divine Engine will weigh whether it's useful or not. The filter is more likely to be kept, but with parameter values assigned by the Divine Engine itself.

!

When a filter is set to “Replaceable”, you can't [parameterize](_documentation_fine-tune-a-strategy-for-the-best-settings.md#Parameterization) its parameters yourself. It's like saying to the Divine Engine, “You decide whether this filter is useful; and if it is, you decide the best values for it”. It's more efficient than flagging it as “Not Replaceable” and do the parameterization yourself; unless of course you want that filter to stay no matter what.

Such techniques can be used to guide (or kick-start) the Divine Engine to follow a certain path. For example, to avoid hindsight overfitting, the Divine Engine is supplied with a certain filter that prevents it from buying undervalued stocks, when such stocks were not yet part of an Index Portfolio (e.g. S&P 500). Such a filter could be the [“Average Currency Volume Filter”](_documentation_average-currency-volume-filter_.md) set to buy above a certain dollar volume.

* * **3.  Randomize Ranking Rule Offsets** – This checkbox defines whether the Ranking Rules “Offset” parameters will be randomized.

!

The default for these “Offset” parameters is “0 days”. If the checkbox is enabled (ticked), the Divine Engine will apply random days to those parameters. If the checkbox is disabled, they'll be applied 0 days as usual. To understand about the “Offset” parameter, read about it [here](_documentation_ranking-panel-guide.md#offsetweight).

!

Keep in mind, the randomization happens only to the Ranking Rules added by the Divine Engine (or if a rule is set to “Replaceable”). For those Ranking Rules you added yourself, their “Offset” parameters are unaffected by this checkbox. If you wish to randomize their “Offset”, you must parameterize them yourself.

!

* * **4.  Tournament Fitness Function Rotation** – This property defines whether Rotational Fitness is used in the tournaments.

!

Rotational Fitness is a mechanism by which every tournament is given a Fitness Function different from the other tournament. As you may recall [earlier](_documentation_backtest-parameterization-panel.md#TournamentMechanism), each tournament uses Fitness Functions to rank the 4 strategies' performance, thus defining the 2 survivors.

For example we have three Fitness Functions, CAGR, R2, and MAR:

*   Without Rotational Fitness, each tournament uses the three metrics combined. Thus each of the 4 strategies has a Fitness Score from the combination of CAGR, R2, and MAR. This Fitness Score, in turn, defines the upper 2 strategies (survivors), and the bottom 2 (losers).
*   But with Rotational Fitness, one tournament will be assigned CAGR to measure its 4 strategies' performance. Another tournament will be assigned R2. Yet another tournament will be assigned MAR, and so on and so forth.

!

!

The idea for Rotational Fitness is twofold:

*   Each tournament produces survivors with distinct strength from the other tournaments. So one tournament has its survivors specializing in CAGR, while another tournament in R2. Their genes (rules & filters) are specifically designed for their strength. Otherwise, they all become jack of all trades and master of none. It's like different groups of organism: each with different environments and needs, thus each has distinct strength from the other groups. Eventually their offspring will breed, and the result is a more robust next generation.

*   But more importantly, the reason for Rotational Fitness is to introduce noise to the tournaments. It's a revolutionary mechanism to produce robust strategies, with good in-sample and out-of-sample performance. So instead of hindsight overfitting to achieve that goal (which is detrimental), we use random noise.

Obviously, Rotational Fitness is only useful if you have multiple Fitness Functions. If you have but one Fitness Function, you can disable Rotational Fitness:

!

Now, let's examine the technical difference between the two flavors there:

!

**Enabled** – with this, the Divine Engine makes a list of all the Fitness Functions used; in our case, the list would be:

1.  CAGR
2.  R2
3.  MAR

Then: the first tournament gets the first item on that list (CAGR), the second tournament gets the second item (R2), and the third tournament gets the third item (MAR). Now that the list is fully “consumed”, it'll start from the beginning again. So the fourth tournament gets CAGR, the fifth tournament R2, the sixth tournament MAR, and so on and so forth until all tournaments are done.

Note, a Fitness Function's “Weight” also determines the amount it's listed there, in relation to the amount of other Fitness Functions. For example, if all Fitness Functions are weighted equally, each will be listed once; just like what we see in the list above. But if CAGR has a weight of 100%, while R2 is 75%, and MAR is 50%, then the list becomes:

1.  CAGR
2.  MAR
3.  R2
4.  CAGR
5.  MAR
6.  R2
7.  CAGR
8.  CAGR
9.  R2

Notice CAGR is listed 4 times, R2 3 times, and MAR 2 times, to account for their different Weights relative to each other. In other words, the “Weight” parameter defines how often that Fitness Function will be assigned to all tournaments–aside from the fact that “Weight” is also used as a multiplier to the Fitness Score itself. That means, as usual, that lower “Weight” indicates less importance in defining the character of the strategies.

[https://portfolioboss.com/wp-content/uploads/2021/05/dfg56gdq3eqe.mp4](_wp-content_uploads_2021_05_dfg56gdq3eqe.mp4.md)

**Enabled: use permutations** – This is similar to the previous one, except the list now includes the permutations (combinations) of the Fitness Functions, aside from the individual Fitness Functions themselves. Hence the list looks like:

1.  CAGR
2.  MAR
3.  R2
4.  CAGR + MAR
5.  CAGR + R2
6.  MAR + R2
7.  CAGR + MAR + R2

As usual, the “Weight” parameter also affects how the list is constructed.

[https://portfolioboss.com/wp-content/uploads/2021/05/Rotational-Fitness-Permutations.mp4](_wp-content_uploads_2021_05_Rotational-Fitness-Permutations.mp4.md)

Now you may wonder “What's the tangible difference for me, if I choose this or that flavor?”. Here's the answer:

*   With Rotational Fitness “Disabled”, the Divine Engine may yield the highest performing strategies (at least for the Fitness IS score), but without any guarantee on its OOS (Out-of-Sample) performance. In fact, the strategies are more likely to have disparate performance between IS and OOS.

*   With “Rotate Fitness Function”, the top strategies have similar (or a little lower) Fitness IS performance than “Disabled”. But the metrics' IS and OOS performance are improved noticeably, neither very high in favor of either IS or OOS, nor too low.

*   With “Rotate Fitness Function Permutations”, the top strategies' Fitness IS are usually even lower than the previous two, but they have the best consistency (IS vs OOS), that is, the best when compared to “Disabled” or “Rotate Fitness Functions”.

* * **5.  Tournament Type** – This property further modifies the way tournaments are executed.

!

Just like [Rotational Fitness](_documentation_backtest-parameterization-panel.md#TournamentFitnessFunctionRotation) that modifies the tournaments' mechanism, this property also affects how winners are selected. When it's set to “Default”, [tournaments](_documentation_backtest-parameterization-panel.md#TournamentMechanism) are conducted as previously explained so far. But if you choose “Winner Takes All”, similar Fitness Functions are compared against each other (between the 4 strategies). For example, Strategy A's CAGR is compared against Strategy B's CAGR, and R2 against R2, etc.

The losing Fitness Function is then discarded altogether. It won't have any effects on that strategy's final [Fitness Score](_documentation_backtest-parameterization-panel.md#NormalizingFitness). Finally, the 4 strategies are compared again as usual (based on this modified Fitness Score) to define the eventual survivors.

So each strategy doesn't have a fixed Fitness Score, which are then sorted as usual. Instead, their final Fitness Score depends on their opponent (the literal duel). By comparing the Fitness Functions individually, you basically prevent a 2nd best score to add to the final Fitness Score. That in turn, may give your strategies a slight advantage.

**Notes:**   Rotational Fitness (and Winner Takes All mechanism) merely affect how the tournaments are conducted, i.e how the survivors are determined. The general Evolutionary mechanisms are not affected, i.e Cross-Breeding, Mutation, Average Fitness Score, the picking of top strategies, etc.

*   When using Rotational Fitness, the orange line on the [Fitness Series chart](_documentation_backtest-results-tab.md#TheFitnessSeriesChart) may go down. If Rotational Fitness is disabled, that line can either stay flat or go up, never down. The reason for this: the orange line represents [the best strategy of each generation](_documentation_backtest-parameterization-panel.md#AverageFitnessScore) (its Fitness IS score). Normally, the best strategy survives and becomes the next generation's best strategy as well, unless there's an offspring strategy besting it. But with Rotational Fitness, the best strategy could be killed, when in the next gen's tournament that strategy is assigned a Fitness Function different from the previous one, thus losing it; so if the next generation doesn't contain any strategy that's similar or higher in score than that top strategy, the orange line will drop.

!

* * *

#### Notes:

*   Theoretically, Genetic Algorithm (as represented by the Evolutionary Search Mode) _will_ find the strategy you want. Even more so if you utilize Genetic Programming ([**Cyber Code Engine**](_documentation_cyber-code-genetic-programming_.md)). You just need to have a very, _very long_ evolution, along with myriad variables (market data) thrown in, which means _enormous_ amount of computing power spent. Imagine how the human species have evolved from single-celled organisms to space-faring advanced civilizations through _billions_ of years of evolution. But obviously, _something_ that guides the evolution must also be present, to achieve that _goal_ ultimately. That means _you_ must design the Fitness Functions to be faultless: logical, non-contradictory, and above all non-utopian. That is, for example, a 100% straight equity-curve can only exist if nobody is buying and selling through greed or panic.

*   If you have The Boss unlimited license, you have 25,000 compute hour credits given to you freely each month. When you're about to run out of credits, an email notification will be sent to you. Do understand, despite the vast amount of computer core we have, we can't process unlimited number of backtest per month, hence the necessity to cap each user at 25,000 compute hour credits each month. It's also to avoid excessive use of The Boss by some enthusiastic members.

*   It's not a good idea to whip the Divine Engine hundreds of times to find that holy grail. That's called overfitting, and the chance the resulting strategies would work in real life is reduced by 1% for each Divine Engine run. If the same strategy rules, parameters, settings, and Portfolios are subjected to 10 Divine Engine runs, let's say, then there's a 10% chance the resulting strategies won't work in real life, despite showing good in-sample and out-of-sample performances. You can alleviate this overfitting problem somehow, with the use of [**Super Out-of-sample**](_documentation_backtest-panel-guide_.md#superOOS).

*   You can check the Portfolio Boss Status Page at https://status.portfolioboss.com for the current state of The Boss service and TAP data downloads (if you use TAP data on the Cyber Code Engine). See if they're running smoothly:

!

[**Back to Top**](_documentation_backtest-parameterization-panel_.md#backtotop)

You have already reported this .

#### _documentation_backtest-results-tab.md

> Source: https://portfolioboss.com/documentation/backtest-results-tab
> Scraped: 3/1/2026, 2:08:15 AM

!

This tab is the repository of the various [Divine Engine](_documentation_the-divine-engine-and-the-boss_.md) backtests that you did for this strategy (either a local backtest or with The Boss). Here you can see the graphical progression of each backtest, and choose the top strategies to use. In previous versions of Portfolio Boss, this is called the “Backtest Results” Tab. It's located at the bottom-mid of the [Backtest Strategy Page](_documentation_backtest-strategy-page-overview_.md).

This tab is divided into three sections:

* [The Backtest Items list.](_documentation_backtest-results-tab.md#TheBacktestItemsList)
* [The Top Strategies list.](_documentation_backtest-results-tab.md#TheTopStrategiesList)
* [The Fitness Series chart.](_documentation_backtest-results-tab.md#TheFitnessSeriesChart)

!

* * *

### The Backtest Items List

This section lists the Backtest Items for this strategy. A Backtest Item is a single Divine Engine backtest, one created each time you start the Divine Engine backtest (either ! or ! ). So if you did five Divine Engine backtests, for example, there are five Backtest Items shown here:

!

Look at the info-bar on top “Showing all records. (5)”: the number in parentheses shows you the total Backtest Items you have. You can use the scrollbar (or mouse wheel) to see them all.

Each Backtest Item, in turn, contains its own top strategies that you can load and use. Simply click a Backtest Item, and its contents (top strategies) are shown in the section beneath it.

[https://portfolioboss.com/wp-content/uploads/2022/11/ftyxdfynxdts.mp4](_wp-content_uploads_2022_11_ftyxdfynxdts.mp4.md)

There are various columns for this section, explained below:

* * **1\. Favorite** – This column allows you to mark a Backtest Item(s) as favorite.

!

Let's say you did a lot of Divine Engine backtests, and found some of them to be particularly interesting. You can mark them by _clicking_ the _star buttons_ here, so they don't get lost in the myriad items you have. The favorite Backtest Items are highlighted in blue:

!

You can also see just the favorite items (instead of _all_ Backtest Items being shown): simply click the dropdown button (on this column's header), and a pop-up _toggle_ appears:

[https://portfolioboss.com/wp-content/uploads/2022/11/24aw5ebhe56nrer.mp4](_wp-content_uploads_2022_11_24aw5ebhe56nrer.mp4.md)

If it's toggled OFF, all Backtest Items are shown, and the info-bar at the top says “Showing all records”. But if it's toggled ON, only the favorite items are shown, and the info-bar says “Favorites filter enabled”. The info-bar is there so you don't get confused on what you're seeing; there could be a case where the list is empty because you haven't starred an item, yet you set this toggle ON. If you really don't have a single Backtest Item, the info-bar will say “No results yet.”:

!

* * **2.  Type** – This shows the _type_ of Divine Engine backtests that you did.

!

It can be either ! (The Boss) or ! (Local Test).

* * **3.  State** – This shows the status of each Divine Engine backtest.

!

There are seven possible states:

Note, for a cloud backtest, even if there's an error that impedes your backtest process, The Boss will continually update itself for a fix of such problem. If the problem is resolved and The Boss has finished synchronizing with it, your backtest will be continued to the finish.

You might want to check the **[Portfolio Boss Status Page](https://status.portfolioboss.com/)** if there are indeed problems with The Boss service:

!

* * **4.  Date Started** – This shows the date and time the backtest was _started_ (submitted, for cloud backtests).

!

It's the local date & time on your computer. All Backtest Items are sorted by this date & time, with the latest at the top.

* * **5.  Memo** – This column shows the memo (description) for each Backtest Item. It also allows you to add (or edit) such memo.

!

Such memo could be written on the backtest [confirmation dialog](_documentation_design-strategies-from-scratch_.md#BossDialog) (when you started the backtest), or here _post-backtest_ with the ! button as shown above. Click that button and a text field appears:

!

Once done, click “Save Changes”. Note that memos are optional, you can leave them empty.

* * **6.  Cancel Button** – This button is only visible if a Divine Engine backtest is running. It's used to cancel a cloud backtest.

!

There's no confirmation dialog when you press that button. The cloud backtest's status immediately changes to !. You may want to cancel a backtest if you realize its settings are wrong (e.g. wrong Fitness Functions criteria); make sure you cancel it early, before your compute credits are expended much.

If you run a local backtest (Random search) use the cancel button on its progress dialog:

!

Once a backtest is successfully canceled, its state will be ! .

* * **7.  Load Start Parameters** – These buttons let you load the Baseline Strategy.

!

Each Divine Engine backtest has a Baseline Strategy, i.e. the _initial strategy_ (along with its Divine Engine settings) that will spawn populations and generations (or derivative iterations). It's the original strategy created by the user, before the Divine Engine backtest is initiated. Even if you didn't add any rules (i.e. create from scratch), the Baseline was that blank strategy without any rules (but System Setting's rules must still be present).

So, if you initiate a Divine Engine backtest based on a top-strategy you loaded (without customizing it), the Baseline would be exactly the same as that top strategy.

* * **8.  Delete Buttons** – These buttons delete the Backtest Items.

!

Deleting a Backtest Item also erases its top results, essentially erasing that Backtest Item from this strategy's history. This is good if you want to remove trash or faulty backtests. There's a confirmation dialog after you press that button:

!

To remove multiple Backtest Items at once, select them (by ticking their checkboxes) and press the button at top right corner:

!

* * *

### The Top Strategies List

!

This section lists the _top strategies_ (of a Backtest Item you selected). You can also load a top strategy so its rules & contents are applied as the active strategy. This list (and the chart below it) are compiled even as the backtest is still in progress.

Let's go through the columns there:

* * **1.  Rank** – This column shows the rank of each top strategy.

!

The ranking is based on their in-sample [Fitness Score](_documentation_backtest-parameterization-panel_.md#NormalizingFitness), with the highest score given the number 1 rank.

* * **2.  Load Parameters** – These buttons load the parameters of a top strategy.

!

In effect, you load that strategy's rules, filters, parameter values, portfolio, Divine Engine settings (on its [Backtest Parameterization Panel](_documentation_backtest-parameterization-panel_.md)), and even the original name it was backtested with (the Baseline Strategy's original name). Thus it becomes the active strategy.

Note while a cloud backtest is still running, you can load its top strategy and do a standard (manual) backtest to populate its [reports](https://portfolioboss.wpenginepowered.com/wp-content/uploads/2021/05/gdg56ye5dg_00000_00000.png).

* * **3.  Description** – This shows the generation from which the top strategy was pulled.

!

For example you see “Gen. 035”, which means the strategy was pulled from the 35th Generation. If you use Random search instead of Evolution, this column shows “Iteration” instead of Generation:

!

Note, if you have a valid Baseline Strategy, it may show here as “Baseline”, whether it's a winning strategy or not.

* * **4.  Fitness** – These two columns show the Fitness Score of the top strategies, both [in-sample (IS)](_documentation_backtest-panel-guide.md#insampleratio) and out-of-sample (OOS) score.

!

The Fitness Score is based on the [Fitness Functions](_documentation_backtest-parameterization-panel.md#FitnessFunctions) (metrics) you set for each Divine Engine backtest. The score of all metrics are aggregated (and normalized into a factor of 1) to yield this final Fitness Score. With or without the [Rotational Fitness](_documentation_backtest-parameterization-panel.md#TournamentFitnessFunctionRotation), the score displayed here is the aggregate of all Fitness Functions used.

Fitness (IS) comes from the metrics' score during the in-sample period, while Fitness (OOS) comes from the out-of-sample period. _Make sure_ you select a top strategy whose IS and OOS Fitness Score are generally similar.

* * **5.  Metrics Score** – These columns show the _actual_ [metrics'](_documentation_metrics-panel-guide_.md) score of the top strategies.

!

They're useful to see the individual metric's performance, unlike the aggregate Fitness Score. Even if a strategy has a good Fitness Score, some metrics may be lacking, and you may decide to discard it. By default, any metrics listed as Fitness Functions (on the [Backtest Parameterization Panel](_documentation_backtest-parameterization-panel_.md)) will have their columns shown here.

Sometimes you'll see columns of other metrics not part of the Fitness Functions; these are simply residue from the latest Divine Engine backtest. You can use the “Manage Columns” dialog to define which metrics have their columns shown; click the button as shown here:

!

Here you can search & select any metrics, either their in-sample (IS) score, out-of-sample (OOS), or all sample (AS):

!

To hide the columns again, simply deselect them from this dialog and press OK. Note that any metrics you added on the Fitness Function section (of the Backtest Parameterization Panel) are grayed out (with italics).

!

Their columns (IS and OOS) are always shown and can't be removed with this dialog, unless you delete the Fitness Function(s) first.

* * **6.  Test Date** – This column shows the date and time each top strategy was born.

!

The time and date are based on your local computer's, not the cloud.

* * **7.  The Delete Buttons** – These allow you to delete top strategies.

!

Clicking them opens a dialog to confirm deletion:

!

Once removed, it's gone entirely from this strategy's history. But the [Fitness Series Chart](_documentation_backtest-results-tab.md#TheFitnessSeriesChart) stays unchanged, as it's supposed to tell you what _happened during_ the backtest.

This is useful to delete garbage results, so your collection of top strategies stays neat and easy to find.

**Notes:**   Each column is sortable top to bottom (or vice versa). By default the entire list is sorted based on Rank (from the highest Fitness IS to the lowest). But you can click any column's header to sort the entire list based on that column (except Test Date). Also, the _metrics columns_ can be moved around by dragging their headers. Let's say you want to drag the CAGR columns to the left, so their values are readily visible. The columns placement will stay as you put them, even after a restart.

[https://portfolioboss.com/wp-content/uploads/2022/12/hguitf6tguycr6he.mp4](_wp-content_uploads_2022_12_hguitf6tguycr6he.mp4.md)

*   Even when a backtest is cancelled (or has failed), top strategies thus far created may be shown here. So you don't waste your compute hour credits.

*   When you load a top strategy, only the [Metrics Tab](_documentation_metrics-panel-guide_.md) is populated. You must execute a standard (manual) backtest ! to see its [Performance](_documentation_monthly-performance-panel-guide_.md), [Positions](_documentation_positions-panel-guide_.md), [History](_documentation_history-tab_.md), and [Trade Signals](_documentation_trade-signals-panel-guide_.md) Tabs populated.

* * *

### The Fitness Series Chart

!

This chart is the graphical representation of the [evolutionary](_documentation_backtest-parameterization-panel.md#Evolutionary) progression; if you use [Random search](_documentation_fine-tune-a-strategy-for-the-best-settings_.md), this chart won't be populated. Each Backtest Item (cloud) has its own distinct chart, and it's continually updated as the Divine Engine backtest is progressing.

The horizontal axis represents the generations, going from the _earliest_ generation at the _left_, toward the _latest_ generation at the _right_.

!

The maximum generation is dictated by the [Max. Generations property](_documentation_backtest-parameterization-panel.md#Max.Generations) at the Backtest Parameterization Panel. This may not be reached if an [Exit Condition](_documentation_backtest-parameterization-panel.md#ExitConditions) is triggered. If such is the case, the generations shown in this chart may be less than what you specified.

The vertical axis represents the Fitness Score, normalized into a factor of 1.

!

Note, there's an **inset** at the top-left corner. It allows you to see which graph belongs to what color, as well as enabling or disabling certain graphs (by ticking them on/off). You can expand or collapse the inset by clicking its arrow button. The “Generation Strategy Fitness” IS and OOS lines (purple and dark blue) are disabled by default. Let's discuss the six graphs (lines) there:

!

*   **Generation Strategy Fitness IS** – dark-blue colored. This shows the fitness score (in-sample) of the best _offspring_ strategy (i.e. excluding the parents) for each generation. It's what you see on the “Fitness (IS)” column on The Top Strategies List above.

*   **Generation Strategy Fitness OOS** – purple colored. This shows the fitness score (out-of-sample) for the best _offspring_ strategy of each generation (as shown on the previous dark-blue line). It's what you see on the “Fitness (OOS)” column on the Top Strategies List above.

*   **Population Avg. Fitness IS** – cyan colored, this line shows each population's [average fitness score](_documentation_backtest-parameterization-panel.md#AverageFitnessScore) for the in-sample period. The average is calculated from offspring and parents alike (hence the term “population”).

*   **Population Avg. Fitness OOS** – green colored, similar to the above i.e. the average fitness score of the _population_, but for the out-of-sample period.

*   **Population Best Fitness IS** – orange colored, this one shows the best fitness score (in-sample) from each population (both offspring and parents). Each population has a strategy with this Best Fitness score.

*   **Population Fitness OOS For Best Fitness IS** – brown colored, this shows the fitness score during the out-of-sample period, for those best strategies whose fitness score is charted by the orange graph.

Throughout the course of the evolution, the dark-blue line may join the orange line, indicating that a new, offspring strategy, has beaten a parent strategy carried over from previous generations (orange line). It means that the best population strategy (orange line) comes from the best of the offspring (dark-blue).

!

While the evolution is progressing, you may want to take a look at each of these graphs. If they show abnormalities, you should cancel the backtest altogether, even before the Exit Condition is hit. For example, if the brown and orange lines show great divergence (obvious disparate values throughout the generations), you know that the top strategies produced have inconsistent performance. Ditto if the green and cyan lines are separated too much (make sure you look at the vertical scale too, so as not to get confused whether the distance is actually big). Also, if the cyan line does not advance (even declining) throughout the generations, you know the evolution is probably useless.

* * *

#### Notes:

*   This tab doesn't exist on a [multi-strategy](_documentation_multi-strategy_.md) as that strategy-type doesn't have the Divine Engine capabilities ([basic and meta](_documentation_types-of-strategy_.md) strategies have them).

*   The Fitness Series Chart displays the aggregated Fitness Functions' score as usual, regardless of whether [Rotational Fitness](_documentation_backtest-parameterization-panel.md#TournamentFitnessFunctionRotation) is used. Therefore the orange line shows the best strategy of each population based on its aggregated Fitness Score. This orange line may be the best strategy carried over from the previous generation (no current offspring beats it), or it may be the new best strategy from the offspring that beats the old man.

*   If the strategy is currently in [read-only mode](_documentation_strategy-panel-guide_.md#ReadOnly), you can still load any of the top strategies (or the start parameters/baseline of a Backtest Item). Just confirm to override the read-only mode from the dialog that appears:

!

*   You can expand or shrink each _section_ of this tab, by hovering your mouse between two sections until an arrow-shaped cursor appears. Then drag the mouse up or down.

[https://portfolioboss.com/wp-content/uploads/2022/12/gyudr567esh5.mp4](_wp-content_uploads_2022_12_gyudr567esh5.mp4.md)

[**Back to Top**](_documentation_backtest-results-tab_.md#backtotop)

You have already reported this .

#### _documentation_backtest-strategy-page-overview.md

> Source: https://portfolioboss.com/documentation/backtest-strategy-page-overview
> Scraped: 3/1/2026, 2:08:07 AM

The “Backtest Strategy” page is _the heart_ of Portfolio Boss.
To access this page, click on the “Backtest Strategy” button  !    at the left of the interface (provided you have _selected_ a strategy from the [“Strategy Management”](_documentation_strategy-management-page-overview_.md) page).

[https://portfolioboss.com/wp-content/uploads/2021/05/fg456fhjfhd.mp4](_wp-content_uploads_2021_05_fg456fhjfhd.mp4.md)

Or, you can double click a strategy so you're taken immediately to this page:

!

In this page you can define the gears, nuts, and bolts of a strategy:

* [at what date the strategy trades each month,](_documentation_system-settings-panel-guide_.md#monthlyswitch)
* [what's the Cash Equivalent when Positions are liquidated,](_documentation_system-settings-panel-guide_.md#positionreplacements)
* [how many Positions to hold at any given time,](_documentation_system-settings-panel-guide_.md#totalpositions)
* [how to define the Limit Orders,](_documentation_system-settings-panel-guide_.md#BuyOrderType)
* [whether you'll be trading Long or Short Positions,](_documentation_system-settings-panel-guide_.md#PositionType)
* [what Portfolio(s) the strategy will trade,](_documentation_instruments-panel-guide_.md)
* [what Technical Indicators to use for entering and exiting Positions,](_documentation_about-filters-rules_.md)
* [whether it uses the AI-based “Divine Engine” for creating the ultimate strategy,](_documentation_the-divine-engine-and-the-boss_.md)
*   and many more!

In short, you can create an extremely complex (and automated!) trading strategy without the slightest experience in computer programming.

Once you define the strategy's rules, you will then backtest the strategy with this page as well. You'll see how it [performs](_documentation_metrics-panel-guide_.md) in _decades_ of historic market conditions. You can also define the [in-sample](_documentation_backtest-panel-guide_.md#insampleratio) and out-of-sample data to see how the strategy performs in untested waters (or the future).

!

Aside from these things, this page allows you to [automatically calculate](_documentation_trade-plan-calculator_.md) the number of shares to be bought (based on each Position's weight and your account size), and export the Orders' details that you'll enter to your broker.

Note if you're using a restricted license, many of the parameters in this “Backtest Strategy” page will not be available. Please contact our Customer Support at [support@portfolioboss.com](mailto:support@portfolioboss.com) if you wish to upgrade your license.

* * *

!

This page is divided into two _Areas_, each containing its own Panels or Tabs:

*   **The Rules Area** is where you define the strategy's rules, filters (technical indicators), and portfolios; in short, its mechanism.

*   **The Reports Area** shows the strategy's performance in various statistical data. You want to be as scientifically accurate as possible before committing your hard earned money to that strategy. Here you can visualize the data in various charts and graphical Indicators. As well, you can receive trading signals from this area.

* * *

Before we delve further, you must understand the terminology we're using in this page:

[https://portfolioboss.com/wp-content/uploads/2022/11/9iyob7n87bty89.mp4](_wp-content_uploads_2022_11_9iyob7n87bty89.mp4.md)

*   **Area:** As explained above. A region with its own collection of Panels or Tabs.
*   **Panel:** A block that contains its own functions, usually studded with rules, filters, or properties. Panels exist on the Rules Area.
*   **Group:** A collection of Tabs grouped together. Groups exist on the Reports Area.
*   **Tab:** Similar to a Panel, it's a block with its own function, usually a report. Tabs exist in the Reports Area.
*   **Section:** A portion of a Panel (or Tab) that envelopes some properties/reports, which work toward a specific function.
*   **Filter:** A single string of criteria, in the form of a technical indicator used as a Buy or Sell mechanism.
*   **Rule:** Similar to a filter, it's a string of command that defines a certain behavior. Rules exist in the [System Settings](_documentation_system-settings-panel-guide_.md) and [Ranking](_documentation_ranking-panel-guide_.md) panels.
*   **Property:** Similar to a rule, but it exists in the [Backtest](_documentation_backtest-panel-guide_.md) or [Backtest Parameterization](_documentation_backtest-parameterization-panel_.md) panels. Sometimes “rule” or “filter”, and “property” are used interchangeably.
*   **Parameter:** A component of a filter/rule/property where usually you can input a value. It's also known as a “field”.
*   **Value:** The content(s) of a parameter, usually input by you. Built-in values are known as “options” (as opposed to values you typed).

* * *

The layout on this page is customizable to suit your visual needs (and screen space).

You can expand the **Rules Area** to the right, so the Panels there are distributed horizontally too.  This allows you to have a holistic view of the strategy's rules, without much scrolling. Simply hover your mouse at the edge between the Rules Area and the Reports Area. Once the cursor changes into an arrow, drag it to the right as much as you will. The Reports Area will give up space for this expansion.

[https://portfolioboss.com/wp-content/uploads/2021/05/rty56edgxds.mp4](_wp-content_uploads_2021_05_rty56edgxds.mp4.md)

You can also customize the **Reports Area** by moving its Tabs around, and docking it somewhere else (but still within this Reports Area). Simply drag the Tab's header (the Tab's name), and move it toward one of the _landing spots_ (the blue highlighted area):

[https://portfolioboss.com/wp-content/uploads/2021/05/456thdg23.mp4](_wp-content_uploads_2021_05_456thdg23.mp4.md)

There are three types of landing spots:

First is located at the Group's top (that shows the Tabs' names). If you drag the Tab here, you will make it a part of that Group, in relation to the other Tabs there. For example you want this Tab to be dropped in between the Tabs there; simply release the drag between the other tabs. Note, if you simply want to rearrange Tabs _within the same Group_, just drag each Tab header toward another header within that same Group; this doesn't show a blue highlighted landing spot.

[https://portfolioboss.com/wp-content/uploads/2022/11/rdftysrbetyss.mp4](_wp-content_uploads_2022_11_rdftysrbetyss.mp4.md)

The second type of landing spot is located at the four extreme edges of the Reports Area–top, bottom, right, left. There's an indicator at each of the edge, looks like this: ! . When a Tab is dragged toward that indicator, a landing spot is highlighted in blue, indicating the Tab will be placed there on its own. In other words, it is placed at the top, left, bottom, or right edge of the Reports Area standing on its own (displacing other Tabs/Groups to give space).

[https://portfolioboss.com/wp-content/uploads/2021/05/456dgf214bngfhj.mp4](_wp-content_uploads_2021_05_456dgf214bngfhj.mp4.md)

The third type of landing spot is that cross-shaped indicator: !

It appears when you drag a Tab and hover it to a Group. Drag the Tab to one of the arrows–the top, bottom, left, or right arrow in that cross indicator–and a blue landing area is displayed, dividing that Group in two. So if you release the drag at the top arrow, for example, the Tab will be placed at the top half of the Group, standing on its own, i.e. dividing the previous Group in two parts. Now, there's also the middle indicator inside that cross: if you release at the center of the cross, you're placing the Tab as part of this Group, instead of standing on its own. The Tab is put leftmost, side by side with other tabs on that Group.

[https://portfolioboss.com/wp-content/uploads/2021/05/546yrh3t436.mp4](_wp-content_uploads_2021_05_546yrh3t436.mp4.md)

As a side note, when a Tab is being dragged, its prior place will vanish. It does not actually vanish until you release the mouse at _one of the landing spots_. If you release it without the landing spot showing, the docking is cancelled and that Tab reverts to its previous location.

* * *

#### Notes:

*   You can resize any Group/Tab by dragging its edges: hover your cursor over an edge and see that it changes into an arrow cursor, then drag it.

*   Any changes you made to the strategy (through this “Backtest Strategy” page) will be _immediately_ saved. Even after you close Portfolio Boss and restart your computer, these changes are kept. If you want to reset a strategy to its default state (provided it's one of the Licensed Strategies), you can press the “Back” button (at the top-right corner of the interface). That button brings you back to a _previous page_ you have visited, in our case the “Strategy Management” page.

!

      Then, on that page, press the “Reset” button !  to revert the strategy to its default state.

*   You can right click any of the scrollbars (throughout PB), and a context menu appears. “Scroll Here” lets you scroll the content to to the location you right clicked at. “Top” scrolls to the top of the content; while “Bottom” to the bottom. “Page Up” reveals a part of the content upward starting from where it was hidden, while “Page Down” reveals the content downward. “Scroll Up” scrolls upward by a little increment, while “Scroll Down” scrolls downward a little step.

!

      Horizontal scrollbars have different options' name, but the idea is similar.

[**Back to Top**](_documentation_backtest-strategy-page-overview_.md#backtotop)

You have already reported this .

#### _documentation_beta-filter.md

> Source: https://portfolioboss.com/documentation/beta-filter
> Scraped: 3/1/2026, 2:08:46 AM

[!](_wp-content_uploads_2019_10_Beta-Filter-Original.png.md)

[!](_wp-content_uploads_2019_10_Beta-FIlter-Sell.png.md)

This filter looks at an instrument's Beta, whether it is above or below the threshold Beta value, to consider that instrument as a buy or sell.

Beta is a measure of an instrument's volatility (price instability) in relation to an index, and how strongly correlated that instrument is to the index. In short, it is a measure of an instrument's risk. It is measured by calculating the instrument's gain/loss during a certain period, compared with the index's gain/loss during the same period.

The Portfolio must be related to the index for the Beta to be meaningful. So, for example, calculating the Beta of an Oil ETF using the S&P 500 index would be an exercise in futility.

A Beta value less than 1 means the instrument is less volatile than the market (index), thus reducing your portfolio's risk (drawdown); but since it's less volatile, it may yield a smaller return than the index.

A Beta value of 1 means the instrument is perfectly in sync with the market; its volatility exactly follows the market. It can be a good or bad thing: good because the instrument doesn't add extra risks except that from the market condition; bad because it follows exactly the market's movement, which means you can't escape systematic risk from the market, if it's experiencing a downward spiral. As well, it may be bad because your return doesn't exceed that of the index.

A Beta value more than 1 means the instrument is more volatile than the market, thus riskier, but it comes with a possible higher return than the index.

This filter essentially tells Portfolio Boss to “look for instruments whose Beta for the past x days (or months) in relation to a certain index is above or below the threshold Beta value”.

* * **1.**  The first parameter defines how long to look for the Beta.

[!](_wp-content_uploads_2019_10_Beta-Filter-1st-Param.png.md)

* * **2.**  The second parameter defines the index you want to compare against. 

[!](_wp-content_uploads_2019_10_Beta-Filter-2nd-Param.png.md)

You can click the little “chart” icon beside the index to show up that index's Price Chart (at the [Instrument Tab](_documentation_instrument-tab_.md)). Note, you can't enter a delisted instrument here (those indicated by a number suffix inside square brackets). Otherwise a warning appears and you can't backtest the strategy:

!

* * **3.**  The third parameter defines whether the instrument's Beta must be “above” or “below” the threshold Beta value.

[!](_wp-content_uploads_2019_10_Beta-3rd-Param.png.md)

* * **4.**  The fourth parameter defines the threshold Beta value; usually set to 1. Which means you're looking for instruments whose Beta is “above” or “below” the value of 1.

[!](_wp-content_uploads_2019_10_Beta-Filter-4th-Param.png.md)

* * *

#### Note:

If you're using this filter, the “Beta” indicator shows up below the instrument's Price Chart. This is the (selected) instrument's Beta against the index.

[!](_wp-content_uploads_2019_10_Beta-Chart.png.md)

[**Back to Top**](_documentation_beta-filter_.md#backtotop)

You have already reported this .

#### _documentation_bollinger-bands-bbands-filter.md

> Source: https://portfolioboss.com/documentation/bollinger-bands-bbands-filter
> Scraped: 3/1/2026, 2:08:41 AM

[!](_wp-content_uploads_2020_07_BBands-Buy-Filter.png.md)

[!](_wp-content_uploads_2020_07_BBands-Sell-Filter.png.md)

Bollinger Bands help you avoid the mania of buying and the panic of selling, by anticipating price movement before it happens.

This filter is based on the principle that price tends to fluctuate (rebound) at key inflection areas. Such inflection areas (support and resistance) are represented by the “moving average” line and the two parallel lines above and below such moving average.

For example, take a look at an uptrend here:

[!](_wp-content_uploads_2020_07_Walmart-Strong-Uptrend.png.md)

As you can see, despite a strong uptrend, we have undulating moves up and down. Prices seem to rebound on invisible walls. Wouldn't it be nice if we can “see” those walls? Such walls represent not only buying, but also selling opportunities even in an uptrend.

[!](_wp-content_uploads_2020_07_Walmart-BBands.png.md)

The Bollinger Bands filter allows you to see such walls; the three “walls” where prices are most likely to bounce:

*   The upper band
*   The Moving Average line
*   The lower Band

When the price touches the lower band, there's a good chance it will rebound upward, so you go long (buy).

[!](_wp-content_uploads_2020_07_Walmart-BBands-Buy-Signal.png.md)

When the price touches the upper band, it's likely to rebound downward, so you sell short or sell for profit.

[!](_wp-content_uploads_2020_07_Walmart-BBands-Sell-Signal.png.md)

In summary, price tends to bounce around within a channel; a channel defined by the upper and lower Bollinger Bands.

[!](_wp-content_uploads_2020_07_Walmart-BBands-The-Channel.png.md)

Well, at least that's the general principle. Now, let's get to the more specific rules:

[!](_wp-content_uploads_2020_07_Bollinger-Specific-Rule-Uptrend.png.md)

*   During an uptrend, when price overshoots the upper band, it's a confirmation that the uptrend is strong and will likely to continue. But expect the price to drop a little toward the Moving Average line. When it does so, it's a good buying opportunity. Sell when the price nears the upper band again. Under no circumstances should you short an instrument with such strong uptrend.

[!](_wp-content_uploads_2020_07_Bollinger-Specific-Rule-Downtrend.png.md)

*   Conversely during a downtrend, when price drops lower than the lower band, it confirms a strong downtrend. Expect the price to rise a little, toward the Moving Average line. When it does so, it's a good shorting opportunity. Cover when the price nears the lower band again. Under no circumstances should you go long (buy) on such a strong downtrend.

[!](_wp-content_uploads_2020_07_Brighthouse-Choppy-Price.png.md)

*   Now when there is no clear trend, such as in a trading range, it's almost always a good opportunity to buy near the lower band, and sell (or sell short) near the upper band. Price tends to cross the moving average from one band to the other.

[!](_wp-content_uploads_2020_07_Bollinger-Specific-Rule-Narrow-Expand.png.md)

*   When price moves in a narrow channel (narrow relative to the previous action), the subsequent explosion of the channel, along with the price breakout outside of the channel usually signal an explosive new trend forming. For example, the price moved in a trading range with its narrow channel, and subsequently it overshoots the upper band along with the expansion of the channel. This signals a fresh uptrend forming.

* * *

Now let's get to the filter's parameters:

**1.**  The first parameter defines whether the closing price must be “Above” or “Below” one of those walls.

[!](_wp-content_uploads_2020_07_BBands-Sell-Filter-1st-Param.png.md)

For example, it's always a good idea to sell when price is over-exhausted above the upper band. So you set this parameter as “Above”.

[!](_wp-content_uploads_2020_07_BBands-Buy-Filter-1st-Param.png.md)

Conversely, it's also a good idea to buy when price breaches below the lower band. So you set this parameter to “Below”.

[!](_wp-content_uploads_2020_07_Bollinger-ABC-Holdings-Trading-Range.png.md)

* * **2.**  The second parameter defines the period for calculating the Moving Average, hence also the period for the upper and lower bands.

[!](_wp-content_uploads_2020_07_Bollinger-2nd-Param.png.md)

The default period is 20 days, as recommended by John Bollinger (the inventor of the Bollinger Bands). That means we'll have a 20-days Simple Moving Average as the central line. The upper and lower bands are then derived from that 20-days SMA.

But really you can set this period to whatever you find best. I like mine set to 26-days. Longer periods tend to give signals based on long term trends, while shorter periods allow you to exploit smaller trends (pullbacks or corrections).

[!](_wp-content_uploads_2020_07_Bollinger-Long-Term-200-days-Period.png.md)

Exploiting longer trend allows you to enjoy hefty price increase during such long period. But it comes with a price: trades happen much less frequently thus less profit, and that you may experience great drawdowns during that long period.

* * **3.**  The third parameter defines which “wall” you'd like to set as the reference.

[!](_wp-content_uploads_2020_07_Bollinger-3rd-Param.png.md)

You can choose between the “Upper BBand” (upper band), the “Lower BBand” (lower band), or the “SMA” (the Moving Average as the central line).

For example as explained previously, you believe a buy signal is best represented by the lower band, and a sell signal by the upper band. So you set a buy filter to use the “Lower BBand”, and a sell filter to the “Upper BBand”.

[!](_wp-content_uploads_2020_07_BBand-3rd-Param-Buy-Lower-Sell-Upper.png.md)

The “SMA” option can be used during a strong trend, where you enter a position as the price approaches the central line.

[!](_wp-content_uploads_2020_07_Bollinger-3rd-Param-set-SMA.png.md)

This application is rather ambiguous though, as the price may actually close at one of the outer bands. So it's best used with another filter.

* * **4.**  The fourth parameter defines the coefficient for the Standard Deviation.

[!](_wp-content_uploads_2020_07_Bollinger-4th-param.png.md)

In practical terms, this parameter allows you to expand or shrink the channel.

[!](_wp-content_uploads_2020_07_Bollinger-Different-Coefficients.png.md)

But you may wonder, what is Standard Deviation?

In layman's terms, Standard Deviation is how much the price deviates from the average. This allows the Bollinger Bands to automatically expand and contract based on price volatility. The greater the volatility, the wider the channel, and vice versa.

[!](_wp-content_uploads_2020_07_Bollinger-Dynamic-Volatility.png.md)

During a trading range, the channel automatically shrinks to account for the low volatility of price. Imagine if the channel stays wide: price won't touch anywhere near the upper & lower bands during period of low volatility, thus no buy/sell signals are given, and you can't profit during periods of different volatility.

Note that Standard Deviation affects only the upper and lower bands:

[!](_wp-content_uploads_2020_07_Bollinger-Upper-Lower-Bands-Calc.png.md)

This is what separates the Bollinger Bands from the standard “envelope”, in which the channel's width stays the same. As such, Bollinger Bands are perfectly suited for a strategy that aims to cover decades of price action, where volatility changes frequently. Even better, it's automatically adapting to the thousands of different instruments such as contained in Portfolio Boss.

But it happens that the channel could not capture the price action correctly, even with Standard Deviation. And so this parameter allows you to “multiply” the Standard Deviation.

[!](_wp-content_uploads_2020_07_Bollinger-200-days-Filter.png.md)

For example, if you use a longer Bollinger period to capture longer & bigger trend, it's useful to increase this parameter so the channel expands, giving you more correct signals.

A value of 1 means the Standard Deviation is not multiplied whatsoever. A value greater than 1 means the Standard Deviation is increased/multiplied, thus the channel expands. While a value less than 1 means the Standard Deviation is reduced/divided, thus shrinking the channel. We set the default value at 1.5, although John Bollinger also recommended a value of 2 or greater, for a presumably longer period.

* * *

As with any technical analysis, the rules set out above are not a guarantee. In fact, it's best to use this filter with other filter(s), to eliminate any ambiguity.

For example as we discussed previously, during a strong uptrend you want to buy when price “nears” the central line. So you set the filter to trigger when price closes “Above” the “SMA”. But how much is “Above”? Above could mean anywhere near the central line, or far beyond the upper band. So you use another filter, the “SMA Position Filter”, to define where the price must fall:

[!](_wp-content_uploads_2020_07_Bollinger-MA-Buy-Strategy.png.md)

As you can see on the picture above, price must close “Above” the Bollinger's 26-days SMA, and also “Below” the 13-days SMA Position filter. That way, not only you define the price must fall “near” the central line, but also you make sure it's a clear uptrend you're trading, as the 13-days SMA can only be above the 26-days SMA during an uptrend (Moving Average cross-over, where the faster MA is above the slower MA). It's impossible for the price to close below the 13-days SMA **and** above the 26-days SMA, when the 13-days SMA is below the 26-days SMA (a downtrend).

And then as a polishing touch, you set a sell filter to trigger when price breaks above the upper band.

[!](_wp-content_uploads_2020_07_Bollinger-MA-Price-Action.png.md)

Another scenario is to trade an “explosive” new trend, when the Bollinger channel narrowed and subsequently expands, as already explained before. With this filter alone, it's impossible for the strategy to tell whether the Bollinger channel has narrowed and expanded. And so we use other filters to define such criteria:

[!](_wp-content_uploads_2020_07_Bollinger-Narrow-Expand-Filters.png.md)

As you can see above, we use three buy filters. The first, “Volatility Change Filter” sees whether price volatily has been decreasing by 20% during the past 2 months. This makes sure the Bollinger channel was shrinking during the past 2 months. The second filter, “Volatility Range Filter” sees whether price volatility suddenly spikes more than 50% recently (past 5 days). This ensures that, very recently, the Bollinger channel suddenly explodes. But sharp price action could mean both ways, either up, or down. And so the third filter, “Bollinger Bands Filter” ensures not only of an uptrend, but a strong one at that. This is achieved by capturing the closing price **above** the **upper** band.

[!](_wp-content_uploads_2020_07_Bollinger-Narrow-Expand-Price-Action.png.md)

Then add a sprinkle of a sell filter. During strong uptrend, it's not uncommon for price to overshoot the upper band, so obviously we can't use the Bollinger Bands (sell when price closes above the upper band; it's premature). We want to ride the strong uptrend as long as possible. Thus comes the “RSI Filter”.

[!](_wp-content_uploads_2020_07_Bollinger-RSI-Filter.png.md)

That tells the strategy to exit the position once the RSI exceeds 70. That's an overbought condition, so we want to take profit before the bulls are exhausted, not after. Sometimes RSI may shoot upward of 80 during a strong uptrend, but we want to be safe here, not chasing that castle in the air.

* * **Notes:**   The indicators (upper band, central line, and lower band) are overlaid on the price chart when you open the [“Instrument” Tab](_documentation_instrument-tab_.md). Make sure to backtest the strategy first.

[!](_wp-content_uploads_2020_07_Bollinger-Instrument-Tab.png.md)

*   For the buy filters, you can stack multiple Bollinger Bands filters to spawn multiple channels. Make sure they have the same period settings, but different coefficients (different multiplier for the Standard Deviation).

[!](_wp-content_uploads_2020_07_Bollinger-Multichannel-Filters.png.md)

[!](_wp-content_uploads_2020_07_Bollinger-Multichannel.png.md)

You can use this for exotic purposes (if you're a believer in multiple channels). But remember, this only applies for entering a position (buy filters). Sell filters are executed with the “OR” operator, so multiple Bollinger Bands filters won't work together as one.

[**Back to Top**](_documentation_bollinger-bands-bbands-filter_.md#backtotop)

You have already reported this .

#### _documentation_buy-filters-panel-guide.md

> Source: https://portfolioboss.com/documentation/buy-filters-panel-guide
> Scraped: 3/1/2026, 2:08:11 AM

!

This panel contains various technical indicators, that select instruments to be entered as Positions. These technical indicators are known as the “Buy Filters”. So the strategy looks into its portfolios, and determines which instruments pass the Buy Filters' criteria. For a comprehensive guide on each technical indicator provided with Portfolio Boss, read [Chapter 7](_documentation_about-filters-rules_.md).

This panel is located at the [Rules Area](_wp-content_uploads_2021_05_gdg56ye5dg_00000_00000.png.md) of the “Backtest Strategy” page. By default, this panel is collapsed; you can press the button shown below to expand it:

!

When it's collapsed, as shown above there's the info telling you the number of Buy Filters (rules) this panel contains.

* * **1.**  **To add a Buy Filter** (or multiple Buy Filters), click the “Add Buy Filter” button at the top-right corner. 

!

The “Add Buy Filter” dialog shows up. Here you can search, select, and add the Buy Filter(s). Make sure you actually ticked (enabled the checkbox) of the Buy Filters before clicking “OK”.

!

If you're merely adding _one_ filter, you can double-click that filter _without_ pressing the OK button (provided the filter's checkbox isn't ticked yet).

The newly added filter is always placed at the bottom of the list:

!

Note that certain Portfolio Boss licenses restrict you to specific filters, or filters with limited parameters. If you wish to upgrade your license, please contact our Customer Support team at [support@portfolioboss.com.](mailto:support@portfolioboss.com.)

* * **2.**  **Some Filters can be added more than once,** allowing you to stack them. Obviously, you must set their parameters different from each other. 

!

To do that, open the dialog again and add that same Filter. But note, certain Filters can only be added once; you can see this if you open the “Buy Filter” dialog and the Filter is _grayed out_.

!

* * **3.**  **You get the gist of how a Filter works** by reading its parameters. For example, the Buy Filter called “Simple Moving Average (SMA) Position Filter”, has descriptive parameters translated into: “Buy if… the instrument closing price is above its 200 days SMA”:

!

And if you hover the cursor on it, there's also a tooltip that describes the general function.

If you want to dive deep into these Filters, please refer to [Chapter 7](_documentation_about-filters-rules_.md). There we discuss all Filters and Rules in great detail: their various uses, the technical indicator(s) they use, and the mechanism for each _parameter_. Once you understand them, you can begin tweaking and mix and match those Filters.

Keep in mind, each Filter is already given default-sensible values for quick use.

* * **4.**  **There's a checkbox** on each Filter that you can use to enable/disable it. 

!

A disabled Filter won't be used by the strategy, even if it's still listed on this Panel. It's useful if you're still tweaking the strategy and see which Filter may cause lower strategy performance.

Note, you can't manipulate the parameters while the Filter is disabled.

* * **5.**  **To delete a Filter from the list,** simply click the trash-bin icon on its right.

!

* * **6.**  **Most Filters have indicator graphs** overlaid on the instrument's price chart (go to the [Instrument Tab](_documentation_instrument-tab_.md) at the [Reports Area](_wp-content_uploads_2021_05_gdg56ye5dg_00000_00000.png.md)). 

!

!

For example, the second Buy Filter from top (as listed on this panel) is labelled “Buy rule #2” and has two indicators: “50 days SMA” and “200 days SMA” plotted there. But note, this Instrument Tab is initially empty until you clicked a symbol (from the [History Tab](_documentation_history-tab_.md), for example).

Some indicators (those not directly related to the price) are displayed _below_ the price chart:

!

Indicators will immediately change their plotting (appearance) as soon as you change the Filters' values; no need to backtest the strategy again.

* * *

#### Notes:

*   To be eligible as a Position, an instrument must pass the criteria of **all** Filters listed here. The idea is that entering Positions must be difficult; various conditions must be fulfilled, since it'll be your hard earned money put on the line. The order in which these Filters are listed (top-bottom, bottom-up) does not matter. But too many Filters can be a bad thing, as you don't tolerate the _necessary_ _risks_ for profit. Besides, too many Filters may cause _conflict_ between the various technical indicators. 

*   Keep in mind that the various Buy Filters in your strategy must be able to cope with a long period of backtest range, in various market conditions. It's a mistake to fine tune the Buy Filters so the strategy performs well at a specific, short term period.

*   You can show/hide the Filters' header (name) by clicking the button shown below:

!

[**Back to Top**](_documentation_buy-filters-panel-guide_.md#backtotop)

You have already reported this .

#### _documentation_cash-equivalent-score-filter.md

> Source: https://portfolioboss.com/documentation/cash-equivalent-score-filter
> Scraped: 3/1/2026, 2:08:43 AM

!

!

This filter looks at the [ranking](_documentation_ranking-panel-guide_.md) of the cash-equivalent (that you set on the [“Cash Equivalent”](_documentation_system-settings-panel-guide_.md#cashequivalent) rule), as well as the ranking of each of your instruments.

!

If the instrument ranks higher than the cash-equivalent, that instrument will be considered as a Position. The ranking here is based on the Ranking Rules that you added for this strategy.

!

This filter also exists as a [Sell Filter](_documentation_sell-filters-panel-guide_.md), in which the Position's ranking must be lower than the cash-equivalent's ranking for it to be closed.

!

The way to use this filter depends on the Ranking Rules you have set for the strategy.

For example, if the Ranking Rules favor those high-gain and less volatile instruments, then this filter will only select those instruments that have higher gain (as well as being less volatile) than the cash-equivalent, because there's no point investing in something whose volatility is higher than the cash-equivalent Bonds (such as SHY) while the return is also lower; better park that money in the safe-haven of SHY.

In essence, this filter decides whether trading the instruments is more profitable than trading the Cash Equivalent.

* * *

### Note:

Your strategy must use cash-equivalent (as set on the “System Settings” panel), instead of cash, to be able to use this as a **Buy Filter**. Otherwise a warning message is shown there:

!

But you can still use this as a Sell Filter even if a strategy uses “Cash”. The Positions will then exit if their rankings are lower than “cash”:

!

You have already reported this .

#### _documentation_chaikin-oscillator-filter.md

> Source: https://portfolioboss.com/documentation/chaikin-oscillator-filter
> Scraped: 3/1/2026, 2:08:45 AM

!

!

The Chaikin Oscillator is a form of momentum indicator that's (mostly) used without the overbought/oversold interpretations, unlike its siblings the [RSI](_documentation_rsi-filter_.md), [ROC](_documentation_rate-of-change-roc-position-filter_.md), [CMO](_documentation_chande-momentum-oscillator-cmo-filter_.md), and the like. It's one of the rare technical indicators out there that scrutinize the traded _volume_ of an instrument. The Chaikin Oscillator was developed by Marc Chaikin as a further refinement of the Accumulation/Distribution line.

So back in the day, apparently the 1970s, the newspapers stopped publishing the market's opening prices necessary to calculate Larry William's oscillator _based on_ Accumulation/Distribution line. Yes, traders back then _actually_ collected newspaper clippings to backtest their strategies, a far cry from what we have now with Portfolio Boss and its [Artificial Intelligence](_documentation_the-divine-engine-and-the-boss_.md). So Chaikin devised an ingenious way of _simply_ subtracting the 10-day EMA from the 3-day EMA, of the Accumulation/Distribution line, to create the Chaikin Oscillator.

!

The main premise behind Accumulation/Distribution is that a price move is significant if accompanied by an equally significant volume. When the line goes up, the shares are being accumulated (concentrated) to fewer and fewer hands, hence most of the volume is associated with the increase in price. When the line goes down, shares are distributed and most volume is associated with the price depreciation. So if an instrument closes near the high of the day, there's accumulation; and if it closes near the low, there's distribution.

Calculating the Accumulation/Distribution is pretty simple:

!

The resulting value is then subtracted (if today's a red candle) or added (if green candle) from the previous Accumulation/Distribution value. The Chaikin Oscillator is calculated from the EMAs of this line.

There are several interpretations when using the Chaikin Oscillator, but the most important is to look at a divergence between price action and the Chaikin indicator: when the price goes up in a given period while Chaikin indicator goes down, it's usually bearish. And when price goes down while the indicator goes up, it's bullish. This is especially true if the instrument closes above the overbought (bearish) or below the oversold (bullish) of an accompanying RSI filter. An additional confirmation could be given, for example, if the instrument closes above (bullish) or below (bearish) its 90-day Moving Average.

!

Then there's another interpretation that sees whether the indicator crosses above (bullish) or below (bearish) its equilibrium value (0). But as usual, these are just the general wisdom; your application of the filter could be vastly different, depending on your strategy's portfolio, rules, and other filters.

* * **1.  Short Period:** This parameter defines the Short EMA period applied to the Accumulation/Distribution line.

!

The norm is to use a 3-day period here. But our tests showed a longer period of 60 to 165 days _may_ give better results.

* * **2.  Long Period:** This defines the Long EMA period for the Accumulation/Distribution line.

!

So the Long EMA value subtracted from the Short EMA value yields the Chaikin Oscillator. Keep in mind, this Long EMA period does not necessarily be longer than the Short EMA's period. Our tests showed a value from 35 to 85 days here would be good, or something even greater around 200 days. But the norm is a 10-day period.

* * **3.  Mode:** This parameter defines the method (interpretation) in using the Chaikin Oscillator. This should be the first parameter you set when using the filter.

!

There are three modes listed here:

*   Price Divergence – Price Up and Chaikin Oscillator Down
*   Price Divergence – Price Down and Chaikin Oscillator Up
*   Crossing Zero Line

So essentially there are two methods to use the Chaikin Oscillator in PB: divergence, and, crossing the zero line. These methods have their own parameters, so we'll discuss each method in the following sections.

* * **4.  Mode – Price Divergence:** This mode identifies divergence between price and the Chaikin Oscillator. You may choose between positive or negative divergence.

!

Generally, positive divergence (bullish) is taken when the price goes down while the Chaikin indicator goes up in a given period; this indicates that falling prices are about to go upward. Negative divergence (bearish) is when price goes up and Chaikin goes down in a given period; this indicates the rising prices will go down.

As you see in the orange box above, there's only one parameter specific to this divergence mode, that is, “Divergence Period”. It defines the time-frame in which the divergence must happen. We recommend setting a longer period here, from 70 to 110 days.

!

So let's say we set the period to ten days: the closing price today is $15 while ten days ago it was $20, which means the price goes down. If the Chaikin Oscillator today is at 2 million while ten days ago it was -1 million (the Chaikin goes up), then we have a divergence with the price. It's as simple as that, no need to account for higher highs and lower highs between them (though it's inherently possible if you set “Divergence Period” at a greater value).

Our tests yielded a contrarian interpretation from the norm: Buy when price goes up while Chaikin goes down, and sell when price goes down while Chaikin up.

!

* * **5.  Mode – Crossing Zero Line:** This mode simply sees whether the Chaikin Oscillator crosses above or below the equilibrium value (0).

!

There's one parameter (orange box above) specific to this mode, which defines whether the Chaikin Oscillator must “rise above” or “fall below” the value of zero before the instrument shall be bought/sold.

The idea for equilibrium is this: When prices consistently close near their high of the day while volume is increasing in a given period, there is significant accumulation underway (bullish), thus Chaikin Oscillator is positive (above zero). The reverse is true, i.e. when Chaikin Oscillator is below zero, there's distribution underway because prices close near their low of the day with increasing volume (bearish).

!

The Chaikin Oscillator in Portfolio Boss identifies the crossing literally and immediately before a signal is given. So if the oscillator is above zero today, then it must be below zero _yesterday_, before a signal is given to trade at tomorrow's market open. Generally, it's good to buy when the oscillator “Rises Above” the zero line, and sell when it “Falls Below” it:

!

* * *

### Notes:

*   You can apply this filter multiple times, especially as a Buy Filter, to combine both modes (divergence and zero-crossing), for a more restrictive buy criteria.
*   Once this filter is applied (and the strategy backtested), you can see the Chaikin Oscillator line plotted below the price chart (at the [Instrument Tab](_documentation_instrument-tab_.md)).

[**Back to Top**](_documentation_chaikin-oscillator-filter_.md#backtotop)

You have already reported this .

#### _documentation_chande-momentum-oscillator-cmo-filter.md

> Source: https://portfolioboss.com/documentation/chande-momentum-oscillator-cmo-filter
> Scraped: 3/1/2026, 2:08:40 AM

[!](_wp-content_uploads_2020_07_CMO-Buy-Filter.png.md)

[!](_wp-content_uploads_2020_07_CMO-Sell-Filter.png.md)

CMO filter allows you to detect over-bought and over-sold price levels, similar to the [RSI filter](_documentation_rsi-filter_.md). So, you buy when price is oversold (bears are exhausted), and sell when it's overbought (bulls are exhausted).

[!](_wp-content_uploads_2020_07_CMO-Basic-Principle.png.md)

But there are three important differences with the RSI:

*   CMO oscillates between -100 to 100. A wider scale means there's less chance the overbought-oversold readings are truncated. RSI on the other hand, has a narrower scale from 0 to 100. With intraday data, it's not uncommon to see extremely overbought instrument capped at 99 RSI, while actually it could be far more than that.

*   This filter is more sensitive to the price action, since prices are not averaged as in RSI. Hence price will reach over-bought and over-sold levels more often, but not too often to result in false signals.

*   CMO scale is symmetrical, thus more intuitive. The 0 level serves as the equilibrium. CMO reading above 0 means a positive price momentum (overbought at 50), while a reading below 0 means a negative momentum (oversold at -50). With RSI, the equilibrium level is not readily identifiable, thus harder to judge between an uptrend and a downtrend.

[!](_wp-content_uploads_2020_07_CMO-Above-Below-Equilibrium-0-00-00-00.png.md)

Therefore, as the third point tells us, CMO can also be used to identify a trend and its strength. A positive reading above 0 means that price gained during up days is more than the price lost during down days (up or down relative to the previous closing price), thus an uptrend. A negative reading below 0 means more price is lost during the down days, thus a downtrend. The closer the reading is to 0, the weaker the trend strength.

* * *

Now let's get to the filter's parameters:

**1.**  The first parameter defines the CMO period.

[!](_wp-content_uploads_2020_07_CMO-First-Param.png.md)

The usual period is either 14 or 20 days, but we found the default of 10 days to be good overall. Let's say, with a period of 10 days, the filter looks at the price action from today to 10 days ago. It sees the total amount of the price gained during the up days, compared to the total amount lost during the down days, for the past 10 days.

* * **2.**  The second parameter defines where the **instrument's** CMO reading should fall in relation to the threshold CMO level.

[!](_wp-content_uploads_2020_07_CMO-Second-Param.png.md)

For example, you want to buy when the instrument's CMO reading falls below the oversold level of -50, you can set this parameter to “Less Than”. And if you want to sell when it exceeds the overbought level of 50, you set this to “Greater Than”.

[!](_wp-content_uploads_2020_07_CMO-Second-Param-Buy-Sell.png.md)

You can use “Between” to define a CMO zone that's neither too high nor too low. For example, to confirm it's a good uptrend you're buying (neither a weak trading range nor overbought), you set a buy filter to see whether the instrument's CMO level falls between 20 and 40:

[!](_wp-content_uploads_2020_07_CMO-Second-Param-Between.png.md)

* * **3.**  The third parameter defines the threshold CMO level.

[!](_wp-content_uploads_2020_07_CMO-40-Level.png.md)

As stated previously, the overbought CMO threshold is usually at 50, while the oversold threshold is at -50. But any values between 40 to 70 (positive or negative) are good levels as well. Use 40 if you want to be cautious, not riding a trend for too long (exit before it's exhausted). Use 60 or 70 if you're confident the trend is so strong you want to squeeze the last drops of profit. But beware such extreme levels may not happen, and the price reverses deep instead.

* * **Note:**

Once the filter is applied, the CMO indicator graph appears below the price chart (on the [“Instrument” Tab](_documentation_instrument-tab_.md)). Make sure to backtest the strategy first, and select an instrument.

[!](_wp-content_uploads_2020_07_CMO-Instrument-Tab.png.md)

[**Back to Top**](_documentation_chande-momentum-oscillator-cmo-filter_.md#backtotop)

You have already reported this .

#### _documentation_chart-tab.md

> Source: https://portfolioboss.com/documentation/chart-tab
> Scraped: 3/1/2026, 2:08:16 AM

!

The Chart Tab is located at the [Reports Area](_wp-content_uploads_2021_05_gdg56ye5dg_00000_00000.png.md) of the “Backtest Strategy” page.

It shows the _performance_ graph of the strategy against a benchmark. The “performance” here is the capital growth over time. So when you're crafting a strategy, this is the _first thing_ you should see each time you do a backtest. Not only you see the growth of the investment, but the greatest drawdown it has suffered. It's also an easy way to see how the strategy performs when the benchmark (the market in general) suffers bear markets.

* * **1.**  **The light-green graph** shows the strategy's performance, while the blue graph (or darker shade of green) shows the benchmark's performance.

!

* * **2.**  **The horizontal and vertical axes** represent time (daily), and account size (portfolio size) in percent of the initial capital, respectively. These axes will change their interval values once you zoom-in the chart.

!

These equity curves are shown in percentage terms, not the dollar value. And they start at 100% (bottom-left corner), because that's the _original amount_ of your account size. So a value of 200% means it's currently at 2x or twice the original amount, 50% means it's half of that, etc.

But for ease of understanding, you _can simply_ think of the percentage here as the actual dollar value and you'd still be correct. Just remember that your initial capital was at $100, so if the equity graph reads 10,000% for example, it's as if your $100 has grown to $10,000.

* * **3.**  **The red shaded area** shows the deepest drawdown the _strategy_ experienced during the whole backtest period. It goes _from peak to trough,_ and it's what you see as the [Max Drawdown](_documentation_metrics-panel-guide_.md#maxdrawdown) metric.

!

This red area doesn't show the _entire duration_ of such drawdown (from the last highest peak to the new highest peak). Note, the benchmark doesn't have its greatest drawdown shown.

!

You can hide this red area by unticking the “Max. drawdown” checkbox at the top.

* * **4.**  **The grey shaded area** represents the backtest period reserved for _out-of-sample_ testing.

!

You can set the in-sample and out-of-sample ratios with the [“In Sample Periods”](_documentation_backtest-panel-guide_.md#insampleratio) section (at the Backtest Panel).

* * **5.**  **To view the chart around,** click and drag it left or right. You can also zoom in and out with the mouse scroll-wheel. To revert to the default zoom level (general overview), double-click the chart. 

[https://portfolioboss.com/wp-content/uploads/2023/01/frsdyu56se5sg6wV.mp4](_wp-content_uploads_2023_01_frsdyu56se5sg6wV.mp4.md)

Alternatively, you can use the bottom scroll-bar to manipulate the views: drag it left or right to pan the chart, and shrink/expand it (by dragging its tail/head) to zoom in and out. You can also right-click the chart to show a tooltip on your cursor, which shows the date you're hovering at, and the percentage value of both the strategy and the benchmark. When hovered over the red area, the tooltip also shows the percentage drop from the last peak:

!

* * **6.**  **Change the chart appearance** with the “Chart Type” parameter on the top-left corner. “Line” is the preferred type here, as it shows two distinct charts (strategy and benchmark) clearly, without overlapping shades.

!

“Mountain” shows the two charts filled with their respective colors; this is good if the strategy and benchmark performs quite differently, thus the difference in performance seems even more apparent. Otherwise the colors may overlap in and out, and it can get confusing.

!

“Column” shows a bar chart instead of a continuous graph line. If you zoom in closely (which is the intended way to use this chart type), you can see each bar represents a single day, and each contains both the strategy and benchmark's values. 

!

This is good if you want to get precision reading on the chart (the exact values contained in each day). The tooltip also “snaps” to each single day, instead of wandering around.

Now, if you right-click and look closely on any chart types, there are two dots and a line connecting them. You can use these as visual aid when comparing the _curvature_ of the two equity graphs.

!

* * **7.**  **On the parameter “Y Axis”,** you can define how the chart's vertical axis is mapped out. “Logarithmic” is the default mode: it uses _logarithmic scale_ for a fairer presentation of the _changes_ in the equity graphs' value.

!

For example, a change from 100% to 1,000% would appear in the same distance as the change from 100,000% to 1,000,000%. Both changes represent a ten-fold increase of the investment value, hence they're displayed in the same distance for better clarity.

In a “Linear” scale, the change from 100,000% to 1,000,000% would cover _1,000 times_ the distance of 100% to 1,000%, which means small changes can't be seen clearly on the chart as they're too subtle (remember the chart may range from zero percent to millions of percent). But the “Linear” mode is good for understanding the _real_ or actual distances between values; for example, a benchmark that tops out at 1,000% return would appear _completely low_ compared to the backtest that returns 5,000,000%. 

!

“Logarithmic” scale is more suited for equity graphs. It shows the changes accurately: for example, losing $50 on a $100 balance hurts bad, ditto losing $50,000 on a $100,000 balance feels about the same, as it's the same 50% reduction in balance. If you lost $50 on a $100,000 balance, it's a pinprick.

[**Back to Top**](_documentation_chart-tab_.md#backtotop)

You have already reported this .

#### _documentation_combining-all-the-features.md

> Source: https://portfolioboss.com/documentation/combining-all-the-features
> Scraped: 3/1/2026, 2:08:24 AM

[!](_wp-content_uploads_2020_08_Electronic-Human-1010.png.md)

Thus far, you have learned the three scenarios for using the Divine Engine. These are the most common scenarios you'll encounter. But you may combine the various techniques you learned here to suit your purpose.

For example, you can “fine-tune” a strategy with the Evolutionary search, instead of the Random search. Although it may not be as thorough in searching all the values and combinations, an Evolutionary search may benefit from the Evolutionary progression, building up from a lower performing strategy to create higher performing strategy. So possibly it's more efficient.

And not only can you fine-tune the filters/rules, but you can add new filters/rules as well.

Let's see how it goes:

* * **1.**  We'll start with a barebone strategy that we like. It contains some rules and filters, whose values we want to fine tune.

[https://portfolioboss.com/wp-content/uploads/2020/07/Replaceable-NotReplaceable-Param-clip.mp4](_wp-content_uploads_2020_07_Replaceable-NotReplaceable-Param-clip.mp4.md)

As shown in the video above, those filters you deem essential are set to [“Not Replaceable”](_documentation_backtest-parameterization-panel.md#NotReplaceable). These filters will stay no matter what, and _you can_ parameterize their fields. As for a certain filter you have doubts on, you can set it to “Replaceable”. Note, a filter that's set to “Replaceable” can't be parameterized manually by you. It's up to the Divine Engine to define its values, and whether or not it will stay on the strategy.

* * **2.**  If you take a look at the rules “Buy Order Type” and “Sell Order Type” (on the [System Settings Panel](_documentation_system-settings-panel-guide_.md)), they don't have the “parameterization” buttons ! . Instead, we're presented with the “Replaceable/Not Replaceable” dropdown:

[!](_wp-content_uploads_2020_07_Buy-Sell-Order-Type-Replaceable.png.md)

Still you can parameterize these rules, so the Divine Engine will find whether a Market Order or a Limit Order is best for them. To do so, set them to “Replaceable”. If the Divine Engine finds that a Limit Order (N ATR Limit Order) is best, then it will also define how the Limit Order is calculated, by automatically enabling and parameterizing the corresponding “Buy/Sell Order Limit” rule below them:

[!](_wp-content_uploads_2020_07_Divine-Engine-Parameterizing-Sell-Order-Limit.png.md)

If you set them as “Not Replaceable”, any value that you _manually_ set (either a Market or N ATR Limit Order) will stay no matter what.

The same thing also applies to the property “System”; you can set it to “Replaceable” so the Divine Engine finds the best of the two values for it (Continuously Switching or a Periodic system). If it decides on a Periodic system, the two properties below it “Monthly Switch on Open Of” and “Don't Switch if Position is Still in Top” will be automatically parameterized by the Divine Engine to find the best values for them.

[!](_wp-content_uploads_2021_05_fhj567gj235_00000.png.md)

* * **3.**  Because we want to benefit from the evolutionary progression rather than brute-force random search, let's set the “Search Algorithm” to [“Evolutionary”](_documentation_backtest-parameterization-panel.md#Evolutionary):

[https://portfolioboss.com/wp-content/uploads/2021/07/6784tsg.mp4](_wp-content_uploads_2021_07_6784tsg.mp4.md)

Also make sure the property “Rule Set Parameterization” is set to “Random Selection”, with the checkbox “Use Current Rule Set as Baseline” ticked. If you don't tick the checkbox, any “Replaceable” filters are more likely to be replaced. The rest of the properties are set as usual; and as for the Fitness Functions, we use “Score” and “R2”.

Since we have multiple Fitness Functions, it's best to enable [Rotational Fitness](_documentation_backtest-parameterization-panel.md#TournamentFitnessFunctionRotation).

[!](_wp-content_uploads_2021_05_756gj45jfs_00000.png.md)

If you remember in a previous scenario, we simply set this property to “Enabled”. But this time, we set it to “Enabled: Use Permutations”. With permutations, the Divine Engine may yield a more consistent strategy, at the expense of a slightly lower performance. But it's up to you which one to use. You can even set this to “Disabled” if you have but one Fitness Function.

* * **4.**  Start the Boss as usual. And when it's finished, load a top result and see its contents:

[https://portfolioboss.com/wp-content/uploads/2022/11/r7d6esha3ag.mp4](_wp-content_uploads_2022_11_r7d6esha3ag.mp4.md)

As you can see, the filters we supplied (“Not Replaceable”) are still there. They're applied with new better values specified within our parameterization settings. For example if we set parameterization to “10 to 50 days with a step of 10 days”, then the new value will fall within such a range. A parameter that we did not parameterize will retain its original value. As for the “Replaceable” filter, you see that the Divine Engine has applied its own values into it. Ditto the new filters added by the Divine Engine are applied with random values whose parameterization range is defined by the Divine Engine itself.

Keep in mind though, the Evolutionary search merely “picks” a random value within such a range that you specified. It does not test _all_ those values and decide the best one. Random search on the other hand, given enough iterations, will calculate all values _and_ combinations and pick the best one.

[https://portfolioboss.com/wp-content/uploads/2020/07/Evo-vs-Random-clip.mp4](_wp-content_uploads_2020_07_Evo-vs-Random-clip.mp4.md)

* * **5.**  So far we've done numerous Divine Engine backtests, and their results can be browsed by clicking each Backtest Item one by one (on the [Divine Engine Results Tab](_documentation_backtest-results-tab_.md)).

[https://portfolioboss.com/wp-content/uploads/2022/11/8yf67d678u7dr.mp4](_wp-content_uploads_2022_11_8yf67d678u7dr.mp4.md)

It would be difficult to see which one is the best-performing strategy from all these results. So, what if they are pooled together, and you can pick the top 20 strategies?

Take a look at the [Overall Top Results Tab](_documentation_overall-top-results-tab_.md):

[https://portfolioboss.com/wp-content/uploads/2022/11/t7if67dre6he5sw.mp4](_wp-content_uploads_2022_11_t7if67dre6he5sw.mp4.md)

This Tab picks the top 20 from the hundreds of strategies produced by the Divine Engine, based on the highest “Fitness (IS)” score as shown on the Divine Engine Results Tab:

!

Therefore, no matter what Fitness Functions you used for each Backtest Item (each Divine Engine run), for example one Backtest Item uses “CAGR” and “R²”, while another uses “Score” and “Avg. Drawdown”, they are all normalized into a factor of 1 as the final Fitness Score, and the top 20 Fitness Score get selected to be displayed on the “Overall Top Results” Tab.

That's why it is highly recommended that a fresh strategy you created (from the [“Strategy Management”](_documentation_strategy-management-page-overview_.md) page), shall only contain generally similar [Fitness Functions](_documentation_backtest-parameterization-panel.md#FitnessFunctions) for all the Divine Engine runs. If you decide to use wholly different Fitness Functions criteria, it's best to start fresh with a new strategy:

[!](_wp-content_uploads_2020_07_Strategy-Management-New-Strategy.png.md)

Otherwise, the top 20 strategies may not reflect fair comparisons between the different Backtest Items. For example, a Backtest Item that uses “Average Position Gain” may yield Fitness Score upward of 1000, whereas another Backtest Item that simply uses CAGR only yields Fitness Score not far from 1. Thus the top 20 is highly skewed to favor the first Backtest Item.

[https://portfolioboss.com/wp-content/uploads/2022/11/yfudr56e6bhes5.mp4](_wp-content_uploads_2022_11_yfudr56e6bhes5.mp4.md)

You can prevent this by using a sensible _threshold value_ for your Fitness Function(s), but it could be difficult to decide. Either way, don't care too much about the top 20; just experiment and play!

Anyway, this Overall Top Results Tab also shows the actual metrics' values for the top 20 strategies (values on CAGR, R², Score, etc):

[!](_wp-content_uploads_2020_07_Overall-Tops-Metrics-and-Threedots.png.md)

If you wish to see a metric column that's not shown here, you can use the “Manage Columns” dialog:

!

It also lets you load a top strategy by clicking the “Load Parameters” button ! similar to what you did on the [Divine Engine Results Tab](_documentation_backtest-results-tab_.md).

For more in-depth information on this “Overall Top Results” Tab, refer to the help page [here](_documentation_overall-top-results-tab_.md).

* * *

#### Note:

The Overall Top Results Tab actually lists the top 20 strategies from _all backtests_ you did on this strategy, be they manual backtests, or Divine Engine (The Boss or local).

[**Back to Top**](_documentation_combining-all-the-features_.md#backtotop)

You have already reported this .

#### _documentation_correlation-filter.md

> Source: https://portfolioboss.com/documentation/correlation-filter
> Scraped: 3/1/2026, 2:08:47 AM

[!](_wp-content_uploads_2019_10_Correlation-Filter-Buy.png.md)

[!](_wp-content_uploads_2019_10_Correlation-Filter-Sell.png.md)

This filter selects your instruments based on how correlated they are to an index (during a specified period). In other words, if an instrument moves perfectly in line with the index (whether up or down, and by the same amount) then the instrument is highly correlated to an index, and vice versa.

!

This is a good filter to make your portfolio mimic the behavior of a certain profitable index. For example, if S&P 500 is on a strong rally, you want to select instruments that perform the same way as that index. Or the reverse, you will sell Positions whose behavior start deviating from the index (remember that an instrument's correlation with an index continuously changes).

But beware that following an index closely exposes you to the market's systematic risks, that is, if the market suddenly crashes it's certain that you will crash too. Besides, closely following an index means you are not outperforming it, which is the goal for many traders.

Do note you may be tempted to use a stock or an ETF, instead of an index. For example, if you know Stock A's performance is gaining strong, you want to look for other stocks that mimic this behavior. But beware that a stock’s performance is much more _variable_ than an index, so your backtesting result (going back decades past) may not reflect the current good performance of that stock, which means your strategy may be a fluke for the longer term.

* * **1.**  The first parameter defines the lookback period for the instrument's correlation to an index. A longer period means the instrument is consistently correlated that way with the index, and vice versa.

[!](_wp-content_uploads_2019_10_Correlation-Filter-1st-Param.png.md)

* * **2.**  The second parameter defines what index (or another instrument) to compare against.

[!](_wp-content_uploads_2019_10_Correlation-Filter-2nd-Param.png.md)

Keep in mind, you can't enter a delisted instrument here (those indicated by a number suffix inside square brackets). Otherwise a warning appears and you can't backtest the strategy:

!

* * **3.**  The third parameter defines whether the instrument must be “Above” or “Below” the threshold correlation value to be considered as a buy/sell.

[!](_wp-content_uploads_2019_10_Correlation-Filter-3rd-Param.png.md)

* * **4.**  The fourth parameter defines the threshold correlation value for these instruments to be considered. A value of 1 means perfect correlation with the index, 100% mirroring its behavior. A lower value like 0.2 means a price behavior that is much less affected by the market (index). 

[!](_wp-content_uploads_2019_10_Correlation-Filter-4th-Param.png.md)

You can also input a negative value, for example, a value of -1 means a perfect mirroring behavior that is opposite from the index; let's say, if the index moves 100.72 points upward, the instrument will move 100.72 points downward.

Do note, it is not recommended to perfectly mirror the index 100% (if that's actually possible), as explained before. So, if you want to follow an index, set this value at least 0.8; that way your Portfolio may outperform the index and has enough diversification to avoid the systematic risks.

* * *

#### Note:

Once this filter is applied, a correlation indicator appears on the chart _below_ the Price Chart (at the [Instrument Tab](_documentation_instrument-tab_.md)). It shows how correlated the selected instrument is to the index, during the specified period.

[!](_wp-content_uploads_2019_10_Correlation-Chart.png.md)

[**Back to Top**](_documentation_correlation-filter_.md#backtotop)

You have already reported this .

#### _documentation_correlation-rule.md

> Source: https://portfolioboss.com/documentation/correlation-rule
> Scraped: 3/1/2026, 2:09:21 AM

* * * [!](_wp-content_uploads_2019_10_Correlation-Rule-000.png.md)

This rule ranks your instruments based on how correlated they are to an index. In other words, if an instrument moves perfectly in line with the index (whether up or down, and by the same amount) then the instrument has the _highest_ correlation score, and vice versa.

[!](_wp-content_uploads_2019_10_Correlation-Between-INTC-and-SPX-at-85_00000.png.md)

Do note, you can specify not just an index as the yardstick, but another instrument as well. For example, if you know an ETF performance is steadily gaining, and you want to look for stocks that mimic this behavior, you can input that ETF's symbol in this filter.

But beware, ETF or other stocks have a more _variable_ performance than an index, so your strategy _may not_ stay true for the longer term.

* * **1.**  The first parameter defines whether you're looking for instruments that have the “Highest” correlation with an Index, or the “Lowest” correlation.

[!](_wp-content_uploads_2019_10_Correlation-Rule-1st-Param.png.md)

* * **2.**  The second parameter defines the _index_ that you want to compare against. Simply type in the symbol in here. There's also a little “chart” icon next to this parameter, which brings you to the [Price Chart](_documentation_instrument-tab_.md) for that index.

[!](_wp-content_uploads_2019_10_Correlation-Rule-2nd-Param.png.md)

You can actually input instruments other than index here, like an ETF. But make sure that instrument isn't delisted (indicated by square brackets suffix containing a number), otherwise there's a warning and the strategy can't be backtested:

!

* * **3.**  The third parameter defines the period for calculating the correlation score (note, an instrument's correlation with an index continuously changes).

[!](_wp-content_uploads_2019_10_Correlation-Rule-3rd-Param.png.md)

* * *

#### Note

Regarding the “Offset” and “Weight” parameters, please refer to the guide about [Ranking Panel](_documentation_ranking-panel-guide_.md#offsetweight).

[**Back to Top**](_documentation_correlation-rule_.md#backtotop)

Discount Applied Successfully!

Your savings have been added to the cart.

Close

You have already reported this .

Search

#### _documentation_cyber-code-genetic-programming.md

> Source: https://portfolioboss.com/documentation/cyber-code-genetic-programming
> Scraped: 3/1/2026, 2:08:26 AM

[!](_wp-content_uploads_2021_06_Electronic-Bull-Pseudocode_00000.png.md)

The Cyber Code is a new feature for the Divine Engine, as part of the Evolutionary mode. It allows the Divine Engine to create trading indicators from scratch, by writing computer code on its own.

When the rest of the world use well-known indicators such as Moving Average, Relative Strength Index, or Bollinger Bands, here you'll keep your market edge even sharper with completely unique trading indicators. With the help of [Genetic Programming](https://en.wikipedia.org/wiki/Genetic_programming), these codes evolve throughout the generations, **in tandem** with the evolution of strategies we already discussed. So it's an even more dynamic evolutionary progression, in which not only the strategies are evolving, but the codes as well, the nuts and bolts of each trading indicator.

You're not constrained to the rigid set of mathematical formula and specific market data as found in built-in trading indicators. Instead, the Cyber Code engine constructs and de-constructs myriad formulas, mixed in with various market data, to create the ultimate technical indicators.

Note, you need a certain license to access the Cyber Code engine. Please contact our [Customer Support](mailto:support@portfolioboss.com) to upgrade your license.

This page is divided into three sections:

* [Practical Use](_documentation_cyber-code-genetic-programming_.md#PracticalUse)
* [Mechanism](_documentation_cyber-code-genetic-programming_.md#Mechanism)
* [Configuration Window](_documentation_cyber-code-genetic-programming_.md#ConfigurationWindow)

* * *

### Practical Use

The use of Cyber Code is generally similar to the [standard evolutionary](_documentation_design-strategies-from-scratch_.md) backtest we discussed previously. The main difference is that the new rules (indicators) added by the Divine Engine are exclusively Cyber Code _rules_. None of the built-in indicators will be slapped to the strategies it created.

**1.**  First, you must set the “Search Algorithm” property to “Evolutionary”.

[!](_wp-content_uploads_2021_06_kshdf7iyi_00000.png.md)

* * **2.**  Then get to the property “Rule Set Parameterization”, and choose the option “Generate Cyber Code” there. This is the key setting.

[!](_wp-content_uploads_2021_06_5r67dfgh3477_00000.png.md)

* * **3.**  Notice the cogwheel icon ! beside that property. This opens the Cyber Code Configuration window. It allows you to define how the codes are generated.

[!](_wp-content_uploads_2021_06_6rfhf5y_00000.png.md)

You may select any of the default profiles here (and then press “Close”), or leave the window alone. Each profile has its own way of generating the codes; and you can create your own profile by toggling ON the “Advanced Mode”. But for now, we won't concern ourselves with its detail. Should you be ready to tweak the Configuration, you can read about it [here](_documentation_cyber-code-genetic-programming_.md#ConfigurationWindow).

* * **4.**  Now the rest of the properties–on the Backtest Parameterization Panel–can be left to their defaults; or you can tweak them however you wish. Consult the help page for [Backtest Parameterization Panel](_documentation_backtest-parameterization-panel_.md) to understand each of those properties.

[https://portfolioboss.com/wp-content/uploads/2021/07/ktyr67wera.mp4](_wp-content_uploads_2021_07_ktyr67wera.mp4.md)

Don't forget to add the [Fitness Functions](_documentation_backtest-parameterization-panel_.md#FitnessFunctions) according to your goals. We have a new metric called [Total Trades/Cyber Code Expression Count](_documentation_metrics-panel-guide_.md#CyberCodeMetric) which can be useful to reduce the occurrence of useless code (introns).

### Mechanism

This section explains the mechanism (workflow) of the Cyber Code engine.

Each rule/filter is created by applying random blocks of code. These blocks can be found on the Cyber Code Configuration window (the Advanced Mode); look under the columns “Operation Type”.

[!](_wp-content_uploads_2021_06_cgh546ftufh_00000.png.md)

In the beginning, a root block (root node) is created. Imagine an upside down tree: the root is the uppermost expression (operation) that produces the final result of the entire tree. The Cyber Code engine picks a random block for this root node, for example the Addition expression. This expression obviously has two operands (the two components that will be added); so from the root node, the tree branches in two. Thus the engine picks two more random blocks; for example Square Root and Division operations.

[!](_wp-content_uploads_2021_06_Root-Node_00000.png.md)

The Square Root has only one operand, so it does not branch; let's say it picks a constant or an input value to be square-rooted. When the engine picks a block like this, either a constant (for example a Pi 3.1416), or an input value (for example volume, closing, high, or low price), that is, a block that requires no operands, just a value, then this branch of the tree ends at this terminus. The Division branch though, requiring two operands, will branch further in two.

[!](_wp-content_uploads_2021_06_gju5t6rh_00000.png.md)

This process of branching and finding random blocks of code continues until the maximum “depth” of the tree is reached. In which case, the engine picks an input value as the terminus (the “leaves” of the tree). The flow of the code starts from the bottom (leaves) toward the root node at the top. Therefore constants and input values are always the building blocks of any Cyber Code rule; these are processed first and foremost. Note: The maximum depth of the tree can be set from the “Max Operation Chain Length”, in that Configuration window.

[!](_wp-content_uploads_2021_06_Filter-vs-Ranking-Tree_00000.png.md)

There are two types of trees: those for the Filters (Buy & Sell), and those for the Ranking Rules. The Filter trees yield a true or false value once they're fed the historic price data of a given instrument (the inputs and constants); so, true means it's a buy. Therefore the root node of such trees are always logical or relational operators; you can see such operators under the “Conditions” Operation Type on the Configuration window. As for the Ranking trees, they yield a number once they're fed the historic price data of an instrument. This number is then used to rank that instrument among other instruments.

All strategies in a population of 64, for example, are given these Cyber Code rules & filters. The [standard evolution](_documentation_backtest-parameterization-panel.md#Evolutionary) then applies: these strategies are backtested to find their metrics' values, and then tournaments are commenced to define the 32 survivors. After that, the usual cross-breeding: the two offspring strategies are given rules & filters picked randomly from the parents' rules & filters.

[https://portfolioboss.com/wp-content/uploads/2021/06/gj456ge.mp4](_wp-content_uploads_2021_06_gj456ge.mp4.md)

Now, comes the Cyber Code cross-breeding: a Cyber Code rule (from one Child) is randomly paired to another Cyber Code rule (from the sibling), and these two rules swap a node. If a rule doesn't find a pair, it'll be left alone as it is. One subtree (node) is exchanged for another subtree; it could even be the whole tree, or just a certain leaf (terminus). Which node gets picked is random, but the engine takes into account the “depth” of the two nodes, so they're of the same size, generally.

[https://portfolioboss.com/wp-content/uploads/2021/06/fh4e56dt.mp4](_wp-content_uploads_2021_06_fh4e56dt.mp4.md)

The property “Cross-Breeding Rate” defines the _maximum_ depth of the node to be cross-bred. With a low rate, only the leaf/terminus is swapped, whereas a high rate may swap the entire tree. In summary, there are two levels of cross-breeding: first is the usual allocation of rules from the parents, and the second is the exchange of DNA codes between the rules. Note, it is also possible that two identical rules are crossbred; the diversity then comes from the different nodes each rule is swapping.

Once the offspring strategies are created, there's the usual [mutation phase](_documentation_backtest-parameterization-panel.md#MutationRate). But those Cyber Code rules are mutated differently: obviously, a Cyber Code rule doesn't have a customizable parameter. So its code (nodes) are the ones mutated. For every node in the tree, there's a percent chance it gets mutated. Of course, this chance is defined from the “Mutation Rate” property. When a node gets mutated, one of two things may happen:

*   The expression type is changed. That is, for example, an Addition expression becomes a Subtraction expression; or a Square Root becomes a Negation, etc. In essence, the amount of operands must not change. As you see, Addition and Subtraction both require two operands; whereas Square Root and Negation require but one operand. With this type of mutation, the original operand(s) is kept, be it a constant, input, function, or a further branch.

*   The node type is changed. Now, this mutation allows a more radical change to the node. So for example, a unary expression becomes a binary expression (from one operand to two operands), or even changed into a terminus (constant or input). The original operand(s) may be used in the new node, so the code logic further down the tree is not affected too much. If it requires more operands, then the engine may pick a random block as usual.

[https://portfolioboss.com/wp-content/uploads/2021/06/678958rfhfth23.mp4](_wp-content_uploads_2021_06_678958rfhfth23.mp4.md)

Other “randomizable things” are mutated too, such as replacing an entire rule if it's flagged “Replaceable”, or any [parameterized](_documentation_fine-tune-a-strategy-for-the-best-settings.md#Parameterization) fields on a built-in rule you added yourself. But note, a Cyber Code rule has only a slight chance of getting replaced entirely, to avoid truncating the code's evolution prematurely.

Now that the offspring strategies are created through standard & Cyber Code cross-breeding, and standard & Cyber Code mutations, the standard tournaments are conducted again. These strategy-level tournaments hit two birds with one stone: not only they select the fittest strategies, but also the fittest Cyber Code rules (the fittest trees), as these rules are part and parcel of a given strategy. So there's no such thing as Cyber Code tournaments in which the rules battle each other out.

[https://portfolioboss.com/wp-content/uploads/2020/09/Evolutionary-Cycle-Summary-clip.mp4](_wp-content_uploads_2020_09_Evolutionary-Cycle-Summary-clip.mp4.md)

This whole process then repeats for the next generations until the evolution is finished. Thus, as you can see, with the Cyber Code evolution, not only the standard evolution is applied, but the code level cross-breeding and mutations as well. This allows for a more dynamic evolutionary progression to create the ultimate strategies.

Let's now learn how to translate the pseudocode into a tree diagram. This way, you'll get the gist of how the indicators work. Note that the Cyber Code engine is continually being improved, so things explained here may become obsolete and irrelevant. In this example, we have a ranking rule; click on the “curly brackets” icon ! to open the pseudocode:

[!](_wp-content_uploads_2021_06_Tree-Diagram-1_00000.png.md)

To read this code, understand that the upper lines are usually the outer branches, containing the leaves. The root node is usually at the bottom. The computer executes the code from top to bottom, unless there's a “control flow” statement like “if” or a shared node. “var” indicates the declaration (creation) of a variable. “v0” is the name of that variable. Think of a variable as a container with a name. A variable may contain an expression, a mathematical operation, function, constant, input, or any code that needs to be contained. Note: Sometimes, a variable is declared without “var” preceding the name, but the data type associated with that variable, such as “double” or “bool”. “double” means the variable yields numerical value with decimal points, and “bool” means it's a variable that yields a true or false value (1 or 0).

In our case, the variable “v0” contains the function SUM, used for finding the sum total of the data sample. So let's draw a circle with a name “v0”, which contains the SUM function.

!

Now, a variable is usually a node that branches further. In this case, it is a node with two operands. The first operand is the “p.AdjustedClose”, that is, the adjusted closing price of an instrument. The second operand is the period of “121” days. These two operands branch out from the “v0” variable. As they are merely input & constant, they don't branch out more. Thus, they are the terminus (leaves). This “v0” subtree can be understood as “calculate the sum of all adjusted closing prices from the past 121 days”.

Now let's get to the second line. Here we have another function assigned to the variable “v0”.

!

It's common for a variable to have multiple assignments like this. That means, whenever the variable is called later down the line, it uses the latest assignment instead of the prior ones. The expression or function on the previous assignment has been calculated, as it is written earlier (above).

This next assignment of “v0” contains the function “Math.Max”, with two operands: “v0” of the previous assignment, and “p.AdjustedLow” signifying the current/today's adjusted low price of an instrument. Since the previous “v0” is the operand of the latest “v0”, we draw a line upward, connecting the previous circle into this new circle called “v0”. This circle contains the operation “Math.Max”.

!

Another branch of this circle, is the input value “p.AdjustedLow”. Thus, the new “v0” node tells the computer “find which operand has the greatest value: either the previous ‘v0′ (i.e. the sum of 121 days' worth of adjusted closing prices), or, the current adjusted low price of this instrument”. Let's say the “p.AdjustedLow” is the greatest, then this v0 node yields the value of “p.AdjustedLow”.

!

On the third line, we have a new variable declared, “v1”. It simply contains the subtraction operation between “p.Volume” (the amount of shares traded for a given day) and the Pi constant (3.1416). So let's draw a new circle called “v1” with the subtraction operation on it, with two operands: “p.Volume” on the left, and “π” on the right.

!

This subtree is still separated from the rest, as it doesn't contain any previously assigned variables (i.e. “v0”). It connects to the “v0” subtree on the fourth line.

!

Now, on this final line, usually we encounter “return”, indicating the root node, where the final value of the whole tree is calculated. “return” simply means this whole code/function/tree must “yield” or return a final value.

This root node contains the multiplication operation between “v0” and “v1”. Remember, the “v0” used here is the latest assigned, not the previous one. So we draw a line connecting the latest “v0” circle, to this root node, a circle that contains the operator “\*” for multiplication. The “v1” circle is also connected toward this root node.

!

This root node is not a variable, so we don't put any label on the circle. The resulting number (product of multiplication) is then used to rank this instrument, in relation to the other instruments. Thus you get the general idea how the tree diagram is constructed.

Sometimes you may encounter logical or relational operators as shown in these code:

!

These are usually found on the Buy/Sell Filter trees, as they must yield a final true/false value (unlike the Ranking trees, which yield a number). In the first example, the node yields a true if the left operand is “greater than or equal” to the right operand; anything other than that yields a false.

!

In the second example, the node yields a true if both operands are true. As you see, the two operands are themselves nodes with relational operators, and if these nodes both yield true, the parent node yields a true; otherwise it's a false.

!

You may also encounter conditional statements like “if” or “?” :

!

In the first example, the expression after “if” (inside the parentheses) is used to define which path is taken: if the expression yields a true, then the statement after “if” (between the curly brackets) is executed, but if it's false, then the statement after “else” is executed. The second example is similar to “if”, but abbreviated. The expression before “?” defines which path is taken: if it yields a true, then the statement after “?” is executed; but if it's a false, then execute the statement after “:”. Usually, such a conditional statement is used to check/avoid division by zero.

When you draw the tree of a conditional statement you do it like this:

!

_as if_ it's a node with three operands, albeit it's not an actual node signified by the dotted circle. Therefore the “if-then-else” circle and the conditional expression do not actually exist in the tree; they merely serve as a visual aid. The real node (subtree) comes from which path is actually taken (the latter two operands).

The same thing applies if there are nested conditional statements, like in this example here:

!

This is because the conditions merely define which path is taken. Each nested condition, taken individually, does not always alter the value itself; it may or it may not do so. So conditional statements, even if nested, do not increase the tree's depth.

There's also an “if” statement with “double.IsNaN( )” as shown in this pseudocode:

!

Such condition simply checks whether the variable inside the bracket yields a number. If it's a number, it returns false, and the “else” statement is executed (or if there's no “else” statement, the computer simply skips the “if” and continues to the next line). If it's not a number, it returns true, and the expression inside the “if” is executed.

In some cases, code bloat or “introns” are encountered. It's when the code don't make any sense (self-defeating, redundant, or inefficient). This is an inevitable side effect of the evolution's random nature. Our developers are continually finding ways to improve code efficiency and reduce such bloat.

**Note:**   The naming of the variables denotes the expressions they contain, for example “b” means a variable that uses a “boolean” expression (yielding true or false), either through logical or relational operators; “v” denotes a variable that contains mathematical functions, arithmetic expressions, constants, or inputs, thus returning a number; “se” is for a “shared expression” variable, containing mathematical expressions shared by other nodes; and “sc” signifies a “shared condition” variable, containing boolean expressions shared by other nodes.

* * *

### Cyber Code Configuration Window

Now we will explore thoroughly the Cyber Code Configuration window.

This window is used for configuring the way the codes are generated. Open this window by pressing the cogwheel button beside the “Rule Set Parameterization” property. Make sure you set that property to the option “Generate Cyber Code”.

!

When you first opened this window, the “easy mode” is displayed:

!

This mode simply lists all the profiles that you can load, either the “Default Profiles” (built-in profiles), or the custom profiles you saved before (under “My Saved Profiles”). Each profile contains its own settings on how the code will be generated. To load a profile, simply click it, and press “Close”. Now to get to the advanced mode, toggle **ON** the “Advanced Mode” (at the top-right corner). This mode allows you to create your own profiles, by manipulating the myriad controls there. Let us now explore each panel in this Advanced Mode:

!

* * **1.  Available Profiles  –**  This panel lists all the profiles, similar to the “easy mode”.

[https://portfolioboss.com/wp-content/uploads/2021/06/356tgrsdg.mp4](_wp-content_uploads_2021_06_356tgrsdg.mp4.md)

Click on a profile to load it; and you'll see other panels have their settings changed. After you clicked a profile, press the “Close” button and it will be used to generate the code. Note, the active profile has its name displayed on top of this window:

!

Now, take note of the four buttons at the bottom-left of this window:

!

“New” lets you create a new profile. Click on that button, and a new profile is created under “My Saved Profile”. This profile (called “New Cyber Code Profile”) is automatically set with the default values. To rename this profile (or any profile under “My Saved Profile”), click its pencil icon and edit the name; once done, press Enter on your keyboard (or click the checkmark icon).

[https://portfolioboss.com/wp-content/uploads/2021/06/6789rfydst.mp4](_wp-content_uploads_2021_06_6789rfydst.mp4.md)

Since the new profile is created with the default settings, you may want to manipulate other panels as you see fit. Then, to save your customization, press the “Save” button. This “Save” button works on any profile you selected (under “My Saved Profile”); that is, any customization you made will be saved to that selected profile.

[https://portfolioboss.com/wp-content/uploads/2021/06/t78fye5.mp4](_wp-content_uploads_2021_06_t78fye5.mp4.md)

Note that profiles under “Default Profiles” can't be customized. You can copy them instead, so they're listed under “My Saved Profiles”. To do that, select a profile and press the button “Copy”. The duplicate has the suffix ” – Copy” on its name. So select that duplicate, manipulate its settings, and press the “Save” button. The same thing applies for profiles under “My Saved Profiles”.

[https://portfolioboss.com/wp-content/uploads/2021/06/ty5678utygs.mp4](_wp-content_uploads_2021_06_ty5678utygs.mp4.md)

Finally we have the “Delete” button, to remove a useless profile from “My Saved Profiles” (built-in profiles can't be deleted). Simply select a profile, click the “Delete” button, and press “Yes” on the confirmation dialog.

[https://portfolioboss.com/wp-content/uploads/2021/06/jyg79iyiyfg.mp4](_wp-content_uploads_2021_06_jyg79iyiyfg.mp4.md)

**Notes:**   If you manipulated the settings and then click on another profile without saving your customization first, a warning dialog is displayed.
*   It is possible to customize the settings and press the “Close” button, without saving first. When you do a Divine Engine backtest with such customization, it will be automatically saved to the profile (which you customized) and be used to generate the code.
*   Obviously, the profiles are available to any strategy you wish to use the Cyber Code on.
*   If you load a top strategy created through the Cyber Code evolution, you also load its particular Cyber Code configurations. The Configuration window is loaded with the settings used for that top strategy.

* * **2.  Cyber Code Generator Settings  –**  This panel contains the general settings for the Cyber Code engine.

!

**Max Operation Chain Length:** This defines the _maximum_ amount of vertical element (depth) in the tree. The resulting trees are capped at this depth; but it may be less than this. You can see in this tree diagram, it has a depth of 5, with each element highlighted. That is to say, each element is either a node or a terminus:

!

This is highly useful to limit the vertical growth of the trees, thus reducing code bloat and introns. The minimum value you can set here is 3, while the maximum is 50. A smaller value yields simpler trees, whereas larger values create more complex trees with many operations and data considered. Keep in mind, a large value not only increases Divine Engine backtest duration, but it _may_ stop the evolution altogether as it exceeds computational memory (a warning will be shown to reduce this value).

!

**Max Lookback:** This affects the “Moving Values” and “Indicators” operation types, such as the EMA, RSI, Lookback, Standard Deviation S, and Sum:

!

It defines the maximum amount of days that these operations can look back. As you already know, for example, an Exponential Moving Average requires a certain amount of days (a period) to calculate its result. Such period may be less than what you set here, but never more. The longer the period, the more memory (RAM) will be used, thus the longer the Divine Engine backtest will be.

!

**Constant Range:** This defines the range that random numbers are generated from. “Random Number” is part of the “Constants” type:

!

Such random numbers are used in the mathematical expressions. When you edit this property, the right field must be greater than the left field, otherwise there's a warning. For example, a range of -10 to 10 means that the random number generated could be -10, -6, 1, 9, or even precise decimal value such as -9.76898975. Greater range means more variance in the random numbers used.

!

**Shared Expression Reuse Pressure:** This defines the likelihood that a “shared expression” is reused. A “shared expression” is a node with the variable name “se” (like “se0” and “se1”) that contains a mathematical expression. This node is “shared”, that is, it can be used by two or more nodes, by referencing it. That way, it serves to control the flow of the code; you can think of it as a node with multiple parent nodes.

!

**Shared Condition Reuse Pressure:** This defines how likely a “shared condition” is reused by other nodes. “Shared condition” is similar to “shared expression”, except it uses the variable “sc” (such as: “sc0” and “sc1”), and contains logical or relational expressions (that yields true or false) instead of mathematical expressions.

!

**Rule Replacement Rate:** This defines the percentage chance that a Cyber Code rule (the entire tree) gets replaced by a completely new tree during the mutation phase. The default value is 10%, and it's recommended to use such a low value. As stated earlier, the chance a Cyber Code rule gets replaced should be low, otherwise the code inside won't evolve properly.

* * **3.  Operation Weights  –**  This panel contains the various code blocks (a.k.a. “operations”), that will be chained together to form the complex trees. Here you can define the likelihood that each block will be used in the trees.

!

Essentially, there are two columns here: the “Operation Type” (shown in red) contains the name of the blocks, whereas “Weight” (shown in green) defines the probability they will be used. Remember that each “Weight” stands in relation to the other “Weights”; so a value of 1 and 1 are considered similar to 100 and 100. But note, a value of 0 means the block will never be used.

The smallest weight you can input is 0, while the maximum weight is 99999.9.

Now, there are at least 9 types of block here:

!

**Inputs:** These are the historic data of a given instrument (from your portfolio); the “raw” data that will be fed to the tree. They denote the “current” data, that is, whatever date the backtest is currently processing. These blocks form the leaves or terminus of any tree.

*   _Adjusted Open:_ The adjusted opening price of the instrument, represented by “p.AdjustedOpen” in the pseudocode.

*   _Adjusted High:_ The adjusted high price of the instrument, represented by “p.AdjustedHigh” in the pseudocode.

*   _Adjusted Low:_ The adjusted low price of the instrument, represented by “p.AdjustedLow” in the pseudocode.

*   _Adjusted Close:_ The adjusted closing price of the instrument, represented by “p.AdjustedClose” in the pseudocode.

*   _Open:_ The historical opening price of the instrument, represented by “p.Open” in the pseudocode.

*   _High:_ The historical high price of the day for the instrument, represented by “p.High” in the pseudocode.

*   _Low:_ The historical low price of the day for the instrument, represented by “p.Low” in the pseudocode.

*   _Close:_ The historical closing price of the instrument, represented by “p.Close” in the pseudocode.

*   _Volume:_ The number of shares traded for the instrument, for that given day; represented by “p.Volume” in the pseudocode.

*   _Day of The Week:_ The “current” day of the week, converted into a number. As you well know, there are 5 trading days in a week. And “current” means whatever date the backtest is currently processing. For example, the backtest is currently being fed the candle from September 9th, 2014, which happened to be a Tuesday, therefore the second trading-day of the week. In a numerical format, we have the value “2”. This is represented by the code “p.DayOfWeek” in the pseudocode.

*   _Day of The Month:_ The “current” day of the month. Similar to the previous one, but for one month, that is, there are 31 different values for this (non-trading days are also counted). It's represented by the pseudocode “p.DayOfMonth”.

*   _Day of The Year:_ The “current” day of the year. For example January 4th, 2021 is the fourth (4) day of the year (holidays counted); so there are 365 different values for this. It's represented by the pseudocode “p.DayOfYear”.

!

**Constants:** Constants are simply fixed numbers (or a random number) used to modify a mathematical expression (for example, as a multiplier). Constants, just like the previously mentioned “inputs”, make up the leaves (terminus) of a tree.

*   _Random Number:_ In the pseudocode, this block manifests as a random number, which falls anywhere between the lower and upper bounds as set on the property “Constant Range” discussed earlier.

*   _Pi:_ The ratio of a circle's circumference to its diameter, which is the approximate number 3.1416. The pseudocode “_π_” represents the number.

*   _Euler Constant:_ This is the base of the natural logarithm, which is the approximate number 2.7183. It's represented by the pseudocode “_ℇ_“.

*   _Golden Ratio:_ The divine proportion, found in many natural phenomena, represented by the approximate number 1.618. It appears with the pseudocode “_φ_“.

!

**Expressions: Standard Math:** These blocks are the standard arithmetic operators. And as operators, they require operands; so they are nodes in the tree that branch further.

*   _Addition:_ Adds two operands to yield their sum. It's represented by the operator “+” between the two operands.

*   _Subtraction:_ Subtracts the right operand from the left operand, to yield their difference. It's denoted by the operator “-” in the pseudocode.

*   _Multiplication:_ Multiplies two operands to yield their product, represented by the operator “\*”.

*   _Division:_ Divides the left operand by the right operand, to yield the size of each partition. Denoted by the operator “/” between the two operands.

*   _Square Root:_ Finds the square root of an operand, represented by the pseudocode “Math.Sqrt( )”. It's a unary operator, where the one and only operand is put inside the brackets. In the tree diagram, simply draw it like the usual node, but with one operand.

*   _Exponentiation:_ Repeated multiplication of the left operand by the amount of the right operand, denoted by the pseudocode “Math.Pow( , )” where the operands are put inside the brackets and separated by the comma.

*   _Root Extraction:_ Finds the root of a number, by a certain depth (degree). The root of 25 with a depth of 2, for example, is called a “Square Root” of 25. In the pseudocode, root extraction uses the same function as exponentiation, i.e. “Math.Pow( , )”. The left operand will have its root extracted, while the second operand denotes the depth of the root. But note, the second operand is placed as the denominator of a fraction of 1, signifying the inverse of power.

*   _Logarithm:_ Calculates the depth by which a number and its root are related. This is represented by the pseudocode “Math.Log( , )” where the left operand is the number whose root is on the right operand.

*   _Modulus:_ Calculates the remainder of an imperfect division. For example, 7 divided by 3 is an imperfect division that yields 2, with 1 as the leftover crumb. It is represented by the operator “%” between the two operands. For example, 7 % 2 equals 1.

*   _Min:_ Finds which of the two operands has the lowest value. Represented by “Math.Min( , )” in the pseudocode.

*   _Max:_ Finds which of the two operands has the greatest value. Represented by “Math.Max( , )” in the pseudocode.

*   _Absolute:_ Another unary operator represented by the pseudocode “Math.Abs( )”. It yields the absolute value of an operand; in other words, it always yields the positive value of that operand, regardless if it's actually negative.

*   _Negation:_ The opposite of Absolute, i.e. it yields the negative value of an operand. But unlike Absolute, Negation is always the _opposite_ of that operand's original value: if it's positive, then it becomes negative; but if it's negative, then it becomes positive (“Absolute” yields a positive value if the operand is already positive). Negation is represented by the “-” (minus sign) attached in front of a single operand.

!

**Expressions: Trigonometry:** These are trigonometric functions, and they serve as nodes with their own operands.

*   _Sine:_ Calculates the sine of an operand. The operand serves as an angle (in radians). Its pseudocode is “Math.Sin( )”.

*   _Cosine:_ Calculates the cosine from an operand (taken as radians), represented by “Math.Cos( )”.

*   _Tangent:_ Calculates the tangent from an operand (taken as radians), represented by “Math.Tan( )”.

*   _Arcsine:_ Calculates the angle (in radians) from a sine value. The operand is taken as the sine value, whose angle will be calculated. It's represented by “Math.Asin( )”.

*   _Arccosine:_ Calculates the angle (in radians) from a cosine value (which is an operand). It's represented by “Math.Acos( )”.

*   _Arctangent:_ Calculates the angle (in radians) from a tangent value (which is an operand). It's represented by “Math.Atan( )”.

*   _Arctangent2:_ Calculates the angle (in radians) from a tangent value. This tangent value comes from dividing the left operand by the right operand. It's represented by “Math.Atan2( , )”.

*   _Hyperbolic Sine:_ Calculates the hyperbolic sine of an operand (taken as radians). It's represented by “Math.Sinh( )”.

*   _Hyperbolic Cosine:_ Calculates the hyperbolic cosine of an operand (taken as radians), represented by “Math.Cosh( )”.

*   _Hyperbolic Tangent:_ Calculates the hyperbolic tangent of an operand (taken as radians), represented by “Math.Tanh( )”.

!

**Expressions: Moving Values:** These are statistical functions, with a period of days as their _sample range_. As the name suggests, the period is a moving window. That is, the entire range is shifted one day forward if the previous day has been processed.

*   _Max:_ Finds the greatest value out of the sample. It's represented by the pseudocode “MAX( , )” where the left operand defines the type of data to be calculated (e.g. the closing price), and the right operand defines the period of days (e.g. 200 days). So for example, out of the last 200 closing prices, this function finds the highest closing price.

*   _Min:_ Finds the smallest value of the sample. It's represented by the pseudocode “MIN( , )” where the left operand defines the data type, and the right operand the period of days; similar as in Max.

*   _Variance S:_ Calculates the Variance of the sample (how varied the sample is). It's represented by the pseudocode “VARIANCES( , )” where the left operand defines the data type, and the right operand the period of days.

*   _Standard Deviation S:_ Calculates the Standard Deviation of the sample (how spread out its values are from the average). It's represented by the pseudocode function “STDDEVS( , )” where the left operand defines the data type, and the right operand the period of days.

*   _Sum:_ Calculates the total sum of the sample; represented by “SUM( , )” where the left operand defines the data type, and the right operand the period of days.

*   _Lookback:_ Picks the value reported in the beginning of the period (for example, the closing price 200 days ago). It's represented by the pseudocode function “LOOKBACK( , )” where the left operand defines the data type, and the right operand the period of days.

!

**Indicators:** These are technical trading indicators encapsulated as functions. These indicators are widely used as the foundation for other, more complex, modern indicators.

*   _Average Percent Range (APR):_ A measure of instrument's volatility in a period of days (shown in percent of the price). It's represented by the pseudocode “APR( , , )” that requires three operands. The left and middle operands are usually the adjusted high and low prices of the instrument, as they are the main ingredients of APR calculation. The right operand is, as usual, the period of days.

*   _Average True Range (ATR):_ This is another yardstick of instrument's volatility similar to APR, but given as a dollar value instead of percent. It's represented by the pseudocode “ATR( , , , )” that requires four operands. The 1st and 2nd operands are usually the adjusted high and low prices (as in APR), the 3rd is the adjusted closing price, and the 4th the period of days.

*   _Chande Momentum Oscillator (CMO):_ A measure of instrument's overbought and oversold conditions (above 50 and below -50, respectively), as well as trend strength. It is represented by the pseudocode “CMO( , )” where the left operand is usually the adjusted closing price (the only historic data required for CMO), and the right operand is the period of days.

*   _Exponential Moving Average (EMA):_ This calculates the average of the data (e.g. closing price) from the specified period. That is, to smooth them out, with more emphasis on recent data instead of the distant past. EMA is commonly used as a support/resistance line. It's represented by the pseudocode “EMA( , , )” with three operands: the left is usually the adjusted closing price, the middle is the period of days, and the right operand is the smoothing constant (a larger value means more weight for the recent prices).

*   _Kaufman Efficiency Ratio (KER):_ A gauge of instrument's trend strength (0 is a trading range, 0.8 is a strong up or down trend, for example). It's represented by the pseudocode “KER( , )” where the left operand usually takes the adjusted closing price, and the right operand the period of days.

*   _Rate of Change (ROC):_ A measure of an instrument's momentum (overbought & oversold state) and velocity (trend strength). The ROC is stated in percent of the price at the period's start. It's represented by “ROC( , )” where the left operand is usually the adjusted closing price, and the right operand the period of days.

*   _Relative Strength Index (RSI):_ This is another measure of overbought (beyond 70) and oversold (below 30) conditions. It's represented by the pseudocode “RSI( , )” where the left operand is usually the adjusted closing price, and the right operand the period of days.

*   _Simple Moving Average (SMA):_ Similar to EMA, but is the simple averaging of the data, where all the data are weighted equally (old and new). It usually serves as a support/resistance line. And is represented by the pseudocode “SMA( , )” where the left operand is usually the adjusted closing price, and the right operand the period of days.

*   _Correlation Coefficient (COR):_ A measure of relationship (correlation) between two data types, whether they're moving in tandem perfectly (a 1.0 correlation); moving perfectly contrarian to each other (a -1.0 correlation); or anything in between (0.0 indicates no correlation). This is represented by the pseudocode function “COR( , , )” with three operands: the left and the middle operands are the two data types being compared (e.g. the Closing Price of a stock, and, the Closing Price of the SPX index), while the right operand is the period of days.

!

**Conditions:** These are logical and relational operators (and some functions that check a value). Each of them is essentially a condition, that will yield a true or false value (1 or 0), depending on whether the condition is met. They may be used as a conditional expression in “if” statements, or as individual expressions in their own right.

*   _Is Greater Than:_ The “>” relational operator, that will yield a true if the left operand is greater than the right operand; otherwise a false.

*   _Is Greater Than or Equal To:_ The “>=” relational operator, that will yield a true if the left operand is greater than, or equal to, the right operand; otherwise a false.

*   _Is Less Than:_ The “<” relational operator, that will yield a true if the left operand is less than the right operand; otherwise a false.

*   _Is Less Than or Equal To:_ The “<=” relational operator, that will yield a true if the left operand is less than, or equal to, the right operand; otherwise a false.

*   _Is Equal To:_ The “==” relational operator, that will yield a true if the left and right operands are equal in value; otherwise a false. Keep in mind, even if you disable this operator (its weight set to 0), it may still be used in conditional statements that prevent division by 0 (the one that uses ? and : as explained earlier). Such statements are important to prevent program error.

*   _Is Not Equal To:_ The “!=” relational operator, that will yield a true if the left and right operands are _not equal_ in value; if they're equal, it yields a false.

*   _Is Not a Number:_ The “double.IsNaN( )” function, with the single operand inside the brackets. It yields true if the operand is “not a number” (NaN), and false if it's a number. NaN denotes “no value”. For example if an indicator function (such as RSI or EMA) does not _yet_ have the minimum period of days required (at the beginning of the backtest date, for example), then the function returns NaN. Therefore “double.isNaN( )” is commonly used as a condition in “if” statements, to check whether an indicator function is ready to be used (already returns a value); if it's not, then use another value (e.g. closing price) until the minimum required period is met.

*   _Is Positive Infinity:_ The “double.IsPositiveInfinity( )” function, with the single operand inside the brackets. It yields true if the operand is a positive infinity, otherwise a false. Positive infinity is a value that is infinite in the positive direction, exceeding the data type's memory allocation; for example, dividing a positive value by 0.

*   _Is Negative Infinity:_ The “double.IsNegativeInfinity( )” function, with the single operand inside the brackets. It yields true if the operand is a negative infinity, otherwise it yields a false. Negative infinity is a value that is infinite in the negative direction, exceeding the data type's memory allocation; for example, dividing a negative value by 0.

*   _AND:_ The “AND” logical operator, that will yield a true if _both_ the left and right operands are themselves true; otherwise it yields a false. Thus each operand must also be a Condition type, be it logical or relational operator, or the three functions described before.

*   _OR:_ The “OR” logical operator, that will yield a true if _any_ operand (left, or right, or both) is true; it only yields false if both operands are false. So each operand must be a Condition type too, that returns either true or false.

*   _XOR:_ The “XOR” logical operator, that will return true if both operands are unequal; if they're equal, it will return false. Equal means the operands are both “true”, or both “false”. So if they're unequal, e.g. “true” and “false”, this operator yields a true.

!

**Expression Control Flow:** These blocks control the flow of expressions (arithmetic operations, mathematical functions, etc) in the tree.

*   _Conditional Expression:_ This is an “if” statement that controls the flow of expressions. In other words, the actual paths taken (if true, and if false) are mathematical expressions (with variables like “v” or “se”).

*   _Shared Expression:_ This is a node that contains mathematical expressions, which can be shared (referenced) by two or more nodes in the tree. Because it is shared, it controls the flow of the program. It's contained within a variable called “se”.

!

**Condition Control Flow:** These blocks control the flow of conditions in the tree (conditions as represented by logical and relational operators, or the boolean functions).

*   _Conditional Condition:_ This is an “if” statement that controls the flow of conditions. In other words, the actual paths taken (the nodes for if true, and if false) are conditional expressions (with variables like “b” or “sc”). But these nodes may contain sub-nodes that are mathematical expressions as well.

*   _Shared Condition:_ This is a node that contains conditional expressions, which can be shared (referenced) by two or more nodes in the tree. Because it is shared, it controls the flow of the program. It's contained within a variable called “sc”.

* * **4.  Additional Data Sources  –**  This panel allows you to add exotic market data, as additional input to be considered by the Cyber Code engine (that is, in addition to the usual OHLCV data of your Portfolio).

!

Such exotic data are usually compiled by external sources. They serve like the usual inputs or constants in the pseudocode; each being a value (a percentage, for example) that can be used in any expressions.

To add them, click the button “Add Data Source”. A dialog appears, allowing you to select the additional data. Once you ticked them, click “OK” and they're listed on this panel.

[https://portfolioboss.com/wp-content/uploads/2022/11/78tren46w.mp4](_wp-content_uploads_2022_11_78tren46w.mp4.md)

You can set their weights as usual (from 0 to 99,999.9), or delete them with their trash-bin icon. The date column (First Date), shows you the first time the data source (ETF) was traded on the exchanges; and this affects the strategy's backtest range (earliest date possible).

Currently, we have three _types_ of additional data (some of them may require a certain PB license):

*   **TAP Premium**

These are listed with the suffix “Premium” on the Add Data Source dialog:

!

TAP stands for True Asset Price, and it shows you the _true value (price)_ that a fund/ETF _should be_ trading at. It's calculated by _dividing_ all its net assets (i.e. minus the liabilities) _by_ the number of shares in circulation.

!

Then comes the Premium (or Discount) part: most of the time, these ETFs are traded at a price higher (or lower) than their True Asset Price. If they're trading lower than the TAP (i.e. discounted), their price will likely _go up_. If they're trading higher (at premium), their price will _go back down_ to their True Asset Price.

!

This discount/premium is calculated by _dividing_ the ETF's adjusted closing price _by_ its TAP, and this is _subtracted_ by 1. The resulting number is a factor of 1 (as percentage) that shows _how much_ of a premium (positive) or a discount (negative) that the ETF is trading at compared to its TAP.

!

TAP Premium data are represented by the pseudocode “get(‘ETFname Premium')”, for example “get(‘ARKK Premium')”.

*   **Grayscale Holdings/Share:**

These have the “Holdings/Share” suffix on the Add Data Source dialog:

!

These are the amount of cryptocurrency held for each share of a Grayscale crypto ETF (e.g. its Bitcoin or Ethereum ETF). They show the US dollar equivalent of such cryptocurrency amount. And they are represented by the pseudocode “get(‘Bitcoin Trust Holdings/Share')” or “get(‘Ethereum Trust Holdings/Share')”.

*   **QQQ Timebomb:**

There's only one item for it:

!

This comes from a licensed-strategy called QQQ Timebomb, indicating the _percentage_ of normal Positions versus the Cash Equivalent Positions. A value of 0.00 means all Positions are in Cash Equivalent (indicating bear market in the Tech sector), while a value of 1.00 means all are normal Positions (normal market condition). It's represented by the pseudocode “get(‘QQQ Timebomb')”.

**Note:**

These hundreds of ETF represent various indexes, asset classes, sectors, industries, and geopolitical regions. They range from corn to gold, Germany to China, futures and bonds, foreign currencies, cryptocurrencies, major indices, complex derivative indices, and even merger & acquisition index! All this to give you a unique edge on your strategy.

For a more direct effect to the strategy, you may include these ETFs as part of the strategy's Portfolio, Cash Equivalent, or the filters' parameter. Let's say you added SPY Premium, QQQ Premium, SH Premium, and PSQ Premium data sources:

!

You can then include SPY and QQQ on the strategy's Portfolio, while its Cash Equivalent is parameterized between SH or PSQ:

!

In other words, you _may_ want to include the data sources related to your strategy's Portfolio. Use your creativity!

Now, if there are problems with downloading any of these data sources, you can check it from the [**Portfolio Boss Status Page**](https://status.portfolioboss.com/).

* * **5.  Additional Instruments  –**  This panel allows you to add more market data to the Cyber Code engine, in addition to the usual OHLCV of the instruments (from your portfolio). But instead of exotic market indicators, you can add any instruments here (_usually market indexes_).

!

They're then taken as the usual inputs (the OHLCV data), with the ticker symbol preceding the input name. For example, instead of “p.AdjustedClose” it now says “SPX.AdjustedClose”.

To add an instrument, type its name or ticker symbol at the top-right field. From the dropdown that appears, select an instrument that matches your search. Or if you typed the ticker symbol correctly, simply press Enter on your keyboard and the instrument is listed on this panel. You can then set its weight as usual, or delete it with the trash-bin icon.

[https://portfolioboss.com/wp-content/uploads/2021/07/5678rhdsgs.mp4](_wp-content_uploads_2021_07_5678rhdsgs.mp4.md)

The “First Date” column simply shows the earliest date for the instrument's historical price data (which affects the backtest's earliest date).

Now, delisted instruments aren't allowed here (those with square brackets suffix enclosing a number). If you try to input a delisted instrument, a warning dialog shows up:

!

!

* * *

#### **Note:**

Visual indicators are also available for Cyber Code rules. As usual, you can see them under the [Instrument Tab](_documentation_instrument-tab_.md). Make sure you click on an instrument first (from the Positions Tab) so the Instrument Tab is populated.

[https://portfolioboss.com/wp-content/uploads/2021/06/789tydt4e.mp4](_wp-content_uploads_2021_06_789tydt4e.mp4.md)

Here, the Cyber Code visual indicators appear on the 2nd section (the middle chart).

On the “Indicators” dropdown, you'll see which line (visual indicator) belongs to what rule. For example, “Ranking Rule #2” means the Cyber Code Ranking Rule located second from top at the Ranking Panel; “Buy Rule #1” means the topmost Buy Filter at the Buy Filters Panel, and so on.

!

This dropdown lists the Ranking Rules first, then below that the Buy Filters, and at the bottom cluster there are the Sell Filters.

Each Filter may contain more than one visual indicator, depending on how that filter works. To understand how it works, open its pseudocode viewer, and look at the variable referred to in the dropdown list. For example, “Sell Rule #1: Cyber Code (v1)” refers to the variable “v1” in the pseudocode. The values yielded by “v1” (the latest assigned “v1”) is plotted by this visual indicator.

!

Always remember that Buy and Sell Filters, no matter how complex the code is, ultimately yield a true or false value (buy or not buy, sell or not sell). So their root node must contain a relational or logical operator between the variables represented in the chart (if “v1” is higher than “v2”, for example, then it's a buy).

When it comes to Ranking Rules, they have only one visual indicator each. This indicator shows the final value (number) yielded by the entire tree, used for ranking the instrument, in relation to the other instruments. Keep in mind that higher value for the indicator does not necessarily mean it's ranked higher; take a look at the rule's “Highest/Lowest” parameter as well.

Note, if an indicator seems so flat throughout its history, either it's indeed flat (the value doesn't change), or because the scaling of the chart has been taken over by another indicator with huge values. If it's the latter case, simply disable that other indicator (from the dropdown).

[**Back to Top**](_documentation_cyber-code-genetic-programming_.md#backtotop)

You have already reported this .

#### _documentation_database-tab-guide.md

> Source: https://portfolioboss.com/documentation/database-tab-guide
> Scraped: 3/1/2026, 2:09:22 AM

!

This Tab allows you to access PB's database files. Just click the button “Open database folder”, and Windows Explorer will open the folder for you:

[!](_wp-content_uploads_2019_10_Database-Folder-336.png.md)

In the database folder, you'll find three essential files for Portfolio Boss. Note, the extension .db (on those files) may not show up depending on your Windows Explorer settings. It doesn't matter, the files are the same:

*   PortfolioBoss.user.db (contains the interface settings, such as panels' sizes, colors, scale, etc),
*   PortfolioBoss.data.db (contains the historic price data for your instruments), and
*   PortfolioBoss.master.db (contains your Strategies and Portfolios).

In this help page, we'll discuss the most common scenarios in using the database files:

* [Backup the database](_documentation_database-tab-guide-2_.md#backupdatabase)
* [Restore the database](_documentation_database-tab-guide-2_.md#restoredatabase)
* [Restoring the database to another machine](_documentation_database-tab-guide-2_.md#restoreto2ndmachine)
* [Changing the database folder](_documentation_database-tab-guide-2_.md#changedatabase)

* * *

### Backup the Database

[https://portfolioboss.com/wp-content/uploads/2021/05/456ghe54t3t.mp4](_wp-content_uploads_2021_05_456ghe54t3t.mp4.md)

1.  Open the database folder through Portfolio Boss.
2.  Make sure you close Portfolio Boss before doing the backup.
3.  Copy all three files.
4.  Navigate to the backup location (or create a new folder).
5.  Paste all three files into the backup folder.

Note, the file **PortfolioBoss.data.db** is usually very large. It is okay not to backup this file if you don't have enough space. But it is **highly recommended** that you backup that file as well, to prevent a possible synchronization error later down the road.

* * *

### Restore the Database

[https://portfolioboss.com/wp-content/uploads/2021/05/hykui46eygdeg.mp4](_wp-content_uploads_2021_05_hykui46eygdeg.mp4.md)

1.  Open your backup folder.
2.  Copy all three files (the backup files).
3.  Open the database folder through Portfolio Boss.
4.  Close Portfolio Boss.
5.  Delete all three database files (on the database folder).
6.  Paste the three backup files on this database folder.

Note, deleting the _current_ database files is the most important step to avoid synchronization error. For example if you don't backup the **PortfolioBoss.data.db**. That way, Portfolio Boss will automatically re-download all historic price data if that file can't be found. If you simply use the current **PortfolioBoss.data.db**, there's a possible synchronization error between your backup files and the current historic price data.

* * *

### Restoring the Database to Another Machine

[https://portfolioboss.com/wp-content/uploads/2021/05/ty56yreghdgs.mp4](_wp-content_uploads_2021_05_ty56yreghdgs.mp4.md)

**The steps are similar to the previous scenario: as long as you can transfer the backup files from one machine to the other, it's fine.** You can use the USB stick route, as shown above; or you can upload those files to a cloud storage, and download them to the other machine; or use a LAN connection for direct transfer between the machines.

1.  Make sure you have a USB stick on hand. Plug it to your 1st machine.
2.  Open the backup folder.
3.  Right-click the three backup files, choose “Send to”, and click on the name of your USB stick (in the video above, it's called USB\_STICK; yours might be different).
4.  Now unplug the USB stick, walk to your 2nd machine, and plug the USB stick there.
5.  Open Portfolio Boss on that _2nd machine_, and open its database folder.
6.  Once the database folder is opened (for that 2nd machine), close Portfolio Boss.
7.  Delete the _current_ database files on that 2nd machine.
8.  Now copy the files (from that USB stick) and paste them to the 2nd machine's _database folder_.

Note, Portfolio Boss's database are machine independent: you can have all your strategies & portfolios on _both_ machines.

* * *

### Changing the Database Folder

By default, the database folder is located at: `%localappdata%\PortfolioBoss\Data`. But you can change it to another folder, for example if your Drive C is full. To do so:

[https://portfolioboss.com/wp-content/uploads/2020/09/Changing-Database-Folder-clip.mp4](_wp-content_uploads_2020_09_Changing-Database-Folder-clip.mp4.md)

*   First make sure you close Portfolio Boss.
*   Then move the files in `%localappdata%\PortfolioBoss\Data` to where you want to store them. Make sure previous folder is now empty.
*   Create a text file in `%localappdata%\PortfolioBoss\Data` and name it **redirect.txt**   In that text file, write the path to the new location. It's not necessary to use quotation marks (“…”) if the path contains blank space.
*   Start Portfolio Boss. It will read the path from that text file. You're essentially “redirecting” Portfolio Boss to use that path.

* * *

#### Note:

*   Inside that **redirect.txt** file, you can write a hashtag character, that is # to annul any path that comes after that character. For example, you can write `# G:\PortfolioBoss 2nd Database`. Portfolio Boss will ignore anything after that # character. It's useful if you're experimenting with different versions of the database files (for example, different PB layouts & settings, etc). Thus to switch back and forth between the two database folders, you can add or remove the # character in front of the path.

[**Back to Top**](_documentation_database-tab-guide_.md#backtotop)

You have already reported this .

#### _documentation_day-of-the-week-filter.md

> Source: https://portfolioboss.com/documentation/day-of-the-week-filter
> Scraped: 3/1/2026, 2:08:47 AM

!

!

This filter allows you to enter (or exit) positions on certain day(s) of the week. It's well known that certain days have some impact on the equity price; for example the [Monday Effect](https://www.investopedia.com/terms/m/mondayeffect.asp).

* * **1.**  The first parameter defines whether it's a single day, or a range of days, that the instrument will be considered to be bought/sold.

!

For example if you pick “Equal to”, the instrument will be bought/sold on a single certain day (that you set on the next parameter). But if you set this parameter to “Between”, the instrument will be bought/sold on a random day within the set range of days. As shown in the example below, the range is between Monday to Wednesday, so it may fall on Monday, Tuesday, or Wednesday:

!

When you set the range, make sure the left day is earlier than the right day. If you set it in reverse, for example Wednesday to Monday, or Friday to Monday, the filter's logic is broken and no instrument will be bought/sold.

There's also the option “Not between” here, which means the day may fall _outside_ the set range:

!

* * **2.**  The second parameter defines which day the instrument should be bought/sold.

!

Or, as already explained, it defines the range of days.

These are the five trading days, from Monday to Friday, excluding Saturday and Sunday. Now, do understand when the instrument falls into the specified day, the buy or sell signal is given tomorrow (the next trading day). So if this filter exits any positions on a Friday, the actual liquidation will occur at Monday's open.

!

* * *

#### Note:

To use this as an exit filter is rather reckless, especially if you have other exit filters in line. Those other filters may not be used at all (their criteria is harder to meet than this filter), and your positions will be frequently liquidated every single week (they may not even last one week). As you already know, exiting a position will happen _if just one_ exit filter is triggered.

[**Back to Top**](_documentation_day-of-the-week-filter_.md#backtotop)

You have already reported this .

#### _documentation_design-strategies-from-scratch.md

> Source: https://portfolioboss.com/documentation/design-strategies-from-scratch
> Scraped: 3/1/2026, 2:08:21 AM

[!](_wp-content_uploads_2020_07_Oh-Genie-Surprise-Me-3.png.md)

This scenario is the most exciting.

Instead of wondering what rules and technical indicators to use, you let the Divine Engine do the thinking, and design strategies from scratch. You read that right. You don't have to add any filters, at all. Just enough guidelines so the Divine Engine knows what it's looking for.

For example, you can tell the Divine Engine to craft strategies that yield an annual return of 80%, with acceptable Drawdown like 30%, and that each month must be a winning month, so you can laugh all the way to the bank, every month, liquidating your profits instead of losses.

[!](_wp-content_uploads_2020_07_Monthly-Yearly-Performance-Screenshot.png.md)

The Divine Engine will then add, mix, and match various [rules, filters](_documentation_about-filters-rules_.md), and values. They're tested thoroughly, and it will see which ones stick to conform with your trading goals. You may even be surprised at the final form the Divine Engine serves you on a platter.

The way it thinks is very different from the human brain with its cognitive biases. Thus rules, filters, and values that you deem impossible or counter-productive may actually be the key to mind boggling results.

In short, you explore a new world.

[!](_wp-content_uploads_2020_07_I-Was-Blind-But-Now-I-see.png.md)

* * **1.**  The very first thing you do is create a new blank strategy, as shown in the video below:

[https://portfolioboss.com/wp-content/uploads/2020/07/Creating-a-Strategy-Clip.mp4](_wp-content_uploads_2020_07_Creating-a-Strategy-Clip.mp4.md)

* * **2.**  As the blank strategy opens before your eyes, let's go to the “System Settings” Panel. This panel is populated by the default values, so there's nothing for you to change here. But feel free to change the rules here as you see fit, for example the rule “Total Positions to Hold”:

[https://portfolioboss.com/wp-content/uploads/2020/07/Total-Position-Clip.mp4](_wp-content_uploads_2020_07_Total-Position-Clip.mp4.md)

If you have doubts on any of the rules, please consult the help page for the [“System Settings” Panel](_documentation_system-settings-panel-guide_.md). Down the road, we'll also discuss how the Divine Engine can find the best “System Settings” values for you.

* * **3.**  Now, let's get to the “Instruments” panel to add Portfolios to this strategy.

[https://portfolioboss.com/wp-content/uploads/2020/07/Adding-Portfolio-Clip.mp4](_wp-content_uploads_2020_07_Adding-Portfolio-Clip.mp4.md)

Keep in mind, the more instruments you have (the larger your Portfolio), the longer it takes for the Divine Engine to finish. In our case, we'll be using the portfolios “Indices Nasdaq 100” and “Indices Nasdaq 100 Historical Deletions” as they're quite small. If you decide to use bigger Portfolios (for example the S&P 500), you may find exotic and high performing instruments with such a bigger pool. But be warned it will take longer for the Divine Engine to finish. Generally, the Divine Engine can accept 1,000 different instruments in your portfolio. But if you use the “Random” search mode (explained [later](_documentation_fine-tune-a-strategy-for-the-best-settings_.md)), you can go well beyond 1,000 instruments.

If you want lightning fast Divine Engine run, you can put one or two instruments in your Portfolio:

!

Usually it's an ETF instrument, be it an index ETF (like QQQ), or commodities (GLD), etc., along with its _inverse_ counterpart to be put on the Cash Equivalent (e.g. PSQ as inverse of QQQ).

!

As shown above, you can also trade a single stock (instead of ETF), which can then be _shorted_ through the Cash Equivalent rules highlighted above. Obviously this technique may run the risk of not diversifying your trades (very volatile equity curve).

* * **4.**  Take a look at the “Buy Filters”, “Ranking”, and “Sell Filters” Panels. These panels contain the bread and butter technical indicators for the strategy.

[!](_wp-content_uploads_2020_07_Buy-Rank-Sell-Filters-Panels-empty.png.md)

But as you notice, these panels are empty. We'll let them be, as the Divine Engine will decide the best technical indicators for us.

* * **5.**  Now that we added the portfolios, let's turn on the Divine Engine. Nope, we won't be turning a special ignition key (though that would be nice). Simply go to the top of this page, and click a button that says “Enable Divine Engine”.

[!](_wp-content_uploads_2020_07_Enable-Divine-Engine-Location.png.md)

You may be greeted by the “invalid strategy” dialog, which shows you what rules & parameters to set so this strategy becomes “valid” (backtest-able).

!

But don't worry for now, just press OK. We'll learn in the following sections what needs to be set.

* * **6.**  After the Divine Engine is enabled, a new panel appears: the [Backtest Parameterization Panel](_documentation_backtest-parameterization-panel_.md). Let's scroll down to it.

[https://portfolioboss.com/wp-content/uploads/2020/07/Scrolldown-Backtest-Param.mp4](_wp-content_uploads_2020_07_Scrolldown-Backtest-Param.mp4.md)

Now, this is where you order your custom tailored suits; in other words, what you're looking for in a strategy. You may look for the highest CAGR with the lowest Drawdown possible, etc. This panel also defines how the Divine Engine backtest will be performed.

We have a dedicated help page explaining all the features of this panel. But for now, you'll only see what's important to you.

* * **7.**  On this panel, just make sure the “Search Algorithm” is set to “Evolutionary”, instead of “Random”.

[!](_wp-content_uploads_2021_05_gkghj2534647_00000.png.md)

“Evolutionary” means that higher-performing strategies are built on the foundation of its lower-performing predecessors, throughout the generations. Each generation undergoes “crossbreeding” and “mutation”, as well as “tournaments” (survival of the fittest) to find the best performing strategies.

If you want to delve deeper on how exactly the Evolutionary search works, refer to the help page [here](_documentation_backtest-parameterization-panel.md#Evolutionary).

* * **8.**  Also make sure the property “Rule Set Parameterization” is set to “Random Selection”. This way, the Divine Engine is allowed to add random rules and filters, along with their random values.

[!](_wp-content_uploads_2021_05_rtyuhjfgh5747_00000.png.md)

This is the most important setting for the “eureka!” moment. Otherwise, with this set to “Manual”, the Divine Engine will not add any filters (rules). You'll be limited to the filters you added manually (in our case, we don't even have them, so we'll have zero filters with this set to “Manual”).

Keep in mind, the random addition of filters may be affected by the number of [parameters (and the value ranges)](_documentation_backtest-strategy-page-overview_.md#Terminology) of each filter. More complex filters _may have_ a higher chance of being added to the strategies. This is because with the wide and deep array of values, it's more difficult for such filters to find good value combinations.

* * **9.**  Still in Backtest Parameterization Panel, set the property “Tournament Fitness Function Rotation” to “Enabled”.

[!](_wp-content_uploads_2021_05_yhuivj464_00000.png.md)

Thus you have enabled [Rotational Fitness](_documentation_backtest-parameterization-panel.md#TournamentFitnessFunctionRotation), a revolutionary way to introduce noise to the evolutionary progression. With Rotational Fitness, strategies may have better consistency. In other words, you don't have to worry whether its real-life performance will mimic the backtest performance.

* * **10.**  Now comes the fun part, where you can tell the Divine Engine what you want in a strategy, custom tailored to your trading needs and goals. Look at the “Fitness Function” section:

!

The very first time a strategy has its Divine Engine enabled, a Fitness Function (i.e. “Score”) is already added. It's a good overall Fitness Function, but it's not specific. If you wish to delete it, click the trash-bin icon.

[!](_wp-content_uploads_2021_05_yudghd35679_00000.png.md)

Now click on the button “Add Fitness Function”.

[!](_wp-content_uploads_2020_07_Add-Fitness-Function-Dialog.png.md)

A dialog appears, listing the various Fitness Functions.

A [Fitness Function](_documentation_backtest-parameterization-panel.md#FitnessFunctions) is essentially the “metric” that the Divine Engine looks in the various strategies it created. A “metric” is the yardstick of the strategy's performance, as you can find in the [Metrics Tab](_documentation_metrics-panel-guide_.md). So for example, you may choose “Score”, “CAGR”, or “Max Drawdown” as the yardstick for the strategies' performance.

The Divine Engine will try its best to create strategies with as high a metric's value as possible. Or in the case of inverted metric like “Drawdown”, it'll create strategies that have the lowest possible value.

[!](_wp-content_uploads_2021_05_wergdg67893_00000.png.md)

You can choose from the various metrics there. For example “Score” is often used, as it already covers both CAGR and Max Drawdown simultaneously. So the Divine Engine will create and find strategies with as high a CAGR as possible, while minimizing the Max Drawdown as low as possible.

You can add multiple Fitness Functions to further narrow down the criteria, for example:

*   R²: this metric shows how smooth the strategy's equity curve is, thus how consistently it performs.
*   Avg. Drawdown: the average depth of the troughs the strategy's equity curve experiences, thus the lower the better.
*   Winning Positions: in case you want to find strategies with higher chance of winning trades.
*   Winning Months: in case you want to find strategies with more winning months per year.
*   Avg. Position Gain: in case you want to find strategies with greater return per trade.
*   Avg. Trades per Year: in case you don't want too many or too little trades per year.
*   Total Trades/Rule Count: to avoid useless rules & filters that don't generate signals.

* * **11.**  As you can see we have multiple Fitness Functions. Let us now define their criteria:

[!](_wp-content_uploads_2020_07_CAGR-At-Least-30-Weight-125.png.md)

For example, we have “CAGR” here. Naturally, we want the Divine Engine to “maximize” the CAGR value as high as possible. Therefore on the first parameter, we set it to “At Least”. Then on the second parameter we define the threshold CAGR value (the minimum that we want). In this case, we set it to 30%. That means, the Divine Engine will try to create strategies with a minimum CAGR of 30%, and higher. And then we have its “Weight” parameter set to “125%” which means the quest for high CAGR occupies “greater importance” for the Divine Engine.

[!](_wp-content_uploads_2020_07_Max-Drawdown-At-Most-35-Weight-75.png.md)

#### Notes:

*   Theoretically, Genetic Algorithm (as represented by the Evolutionary Search Mode) _will find_ your ultimate strategy that will become the envy of even the biggest and most successful Wall Street firm. Even more so if you utilize Genetic Programming ([**Cyber Code Engine**](_documentation_cyber-code-genetic-programming_.md)). You just need to have a very, _very long_ evolution, along with myriad variables (market data) thrown in, which means _enormous_ amount of computing power spent. Imagine how the human species have evolved from single-celled organisms to space-faring advanced civilizations through _billions_ of years of evolution. But obviously, _something_ that guides the evolution must also be present, to achieve that _goal_ ultimately. That means _you_ must design the Fitness Functions to be faultless: logical, non-contradictory, and above all non-utopian. That is, for example, a 100% straight equity-curve can only exist if nobody is buying and selling through greed or panic.

*   A warning notification may be sent to your e-mail if you're about to run out of compute credits. You can either purchase, or wait for the next month's free compute credits. Do understand, despite the vast amount of computer core we have, we can't process unlimited number of backtest per month, hence the necessity to cap each user at 25,000 compute hour credits each month.

*   It's not a good idea to whip the Divine Engine hundreds of times to find that holy grail. That's called overfitting, and the chance the resulting strategies would work in real life is reduced about 1% for each Divine Engine run. If the same strategy rules, parameters, settings, and Portfolios are subjected to 10 Divine Engine runs, let's say, then there's a 10% chance the resulting strategies won't work in real life, despite showing good in-sample and out-of-sample performances. You can alleviate this overfitting problem somehow, with the use of [**Super Out-of-sample**](_documentation_backtest-panel-guide_.md#superOOS).

*   If you wish to “extract” a top strategy into its own stand-alone strategy, you can use the “Copy” button from the top of the Backtest Strategy Page:

!

So, once a top strategy is loaded as the active strategy, you press that button and give it a name:

!

Then press the “Copy” button on that dialog. Note that any Divine Engine parameterization settings (explained later) contained on that strategy will be carried over to the duplicate strategy (even after you restarted PB or your PC, it's still stored there).

This copy function is very useful so you don't lose a top strategy in a big pile of backtest results. You pull it out of the crowd as a standalone strategy, and do other Divine Engine backtests on this sandbox strategy.

[**Back to Top**](_documentation_design-strategies-from-scratch_.md#backtotop)

You have already reported this .

#### _documentation_discount-filter-guide.md

> Source: https://portfolioboss.com/documentation/discount-filter-guide
> Scraped: 3/1/2026, 2:08:45 AM

*   »
*   »
* [Discount Filter](_documentation_discount-filter-guide.md)

* * * [!](_wp-content_uploads_2019_11_Discount-Filter.png.md)

This filter looks for instruments that are _currently_ experiencing a dip in price, therefore you'll enter the Position at a discount before the price rallies again to your profit.

* * *

#### Note:

There's an advanced version of this filter where you can access more parameters. Please contact our Customer Support at [support@portfolioboss.com,](mailto:support@portfolioboss.com) if you wish to upgrade your license.

Discount Applied Successfully!

Your savings have been added to the cart.

Close

#### Block Member?

Please confirm you want to block this member.

You will no longer be able to:

*   See blocked member's posts
*   Mention this member in posts
*   Invite this member to groups
*   Message this member
*   Add this member as a connection

**Please note:** This action will also remove this member from your connections and send a report to the site admin. Please allow a few minutes for this process to complete.

#### Report

You have already reported this .

#### _documentation_divine-engine-global-queue-for-strategy-testing.md

> Source: https://portfolioboss.com/documentation/divine-engine-global-queue-for-strategy-testing
> Scraped: 3/1/2026, 2:07:47 AM

!

Now with all you've learned, you can begin to queue up and manage all your wonderful strategy tests. This is done through Portfolio Boss's powerful Divine Engine Queue.

We've talked a lot about The Boss and it's cloud-based computing resources that make it quick and easy to analyze thousands of possible strategies in record time. These same tests can be run at a slower pace on your own personal computer, if it's up to the task. Usually local tests may slow down your computer as they run in the background, but they can be just the right thing for small or simple experiments.

Let's take an in-depth look at the Divine Engine Queue and how it works.

## Accessing the Divine Engine Queue

To access the Divine Engine Queue, click on the nested play buttons on the left:

![Divine Engine Queue Icon Menu](https://portfolioboss.com/wp-content/uploads/2024/02/Divine-Engine-Queue-Icon-Menu.jpg)

One great feature of the queue is that, now, while Divine Engine tests are running, you can still use Portfolio Boss for other tasks! Manage your portfolio, review other strategies, and even set up other tests all while your queued Divine Engine tests are running in the background.

## Divine Engine Queue Basics

At the top is the Start Queue button. This is what will let you launch all strategy tests you have lined up.

!

Just below is the list of strategies in your queue. The star icon allows you to tag and filter based on your favorite strategies. Click on the down arrow next to the ‘Favorite' header to apply or remove the filter.

!

You can see where strategy tests will run (either locally, or in the cloud) by viewing the icons under the ‘Type' column. The cloud icon strategies will predictably run in the cloud, and the stacked play buttons indicate the strategies will be run locally.

!

The current status of your Divine Engine runs is tracked under the ‘State' column, and the Date started shows you when that state was entered into.

!

This list of strategy tests is limited to show only your most recent tests. You can adjust the size of the historic window show by clicking on the filter / gear icon next to ‘Date queued.' This will show you more (or less) of the strategy test results.

!

With great power comes great responsibility: keep track of all your great work inside the Divine Engine Queue with succinct memos. The first few words are shown automatically in the list view, and the full memo can be read just by hovering over the memo preview. When you want to add or edit a memo, just click the blue paper and pen icon.

!

To dive right into the details of a strategy, use the magnifying glass icon. This will load that strategy's parameters and immediately open the ‘Backtest Strategy' portion of Portfolio Boss. The trash icons here will let you clean up strategies you are all done with. Just be sure you don't lose any work, as deletion can't be undone.

!

The next section below your list of strategy names is the metrics region. Thanks to the dedicated Queue section, we now have much more room to show all the necessary In-Sample (IS) and Out-of-Sample (OOS) metrics you need to make the right decisions.

Clicking on the graph icon on the far left will load that particular generation's parameters into the Backtest Strategy page. Don't forget to use the scroll bar to see more metrics to the right. And of course, you can scroll up and now as normal to view every generation.

!

And finally, at the bottom of the screen is your Fitness Series graph. You can select and deselect various series, with the most important two being ‘Population Best Fitness IS' and ‘Population Fitness OOS For Best Fitness IS.' Remember, you want both of these to be relatively high and they should be converging together late in the generations (to the right side of the graph).

!

## Running the Queue in the Background

After starting the Queue, you can navigate away and continue using Portfolio Boss. You can't start any other tests when the queue is running, but you can still add new tests to the bottom of the queue. When you are on any other page in Portfolio Boss, you'll see a small double arrow in the top right corner that can be used to expand a Queue status window.

!

This status window lets you keep an eye on your test progress while getting other work done. Maximum productivity!

!

You can even add things to your global queue when you are in the Backtest Strategy screen, by first enabling the Divine Engine, clicking on it's drop down, then selecting ‘Queue local test.' CTRL-F11 is the shortcut for this handy feature.

!

**Back to Top**

You have already reported this .

#### _documentation_exporting-the-backtest-result.md

> Source: https://portfolioboss.com/documentation/exporting-the-backtest-result
> Scraped: 3/1/2026, 2:08:14 AM

* * *

!

It's possible to export the strategy's backtest results (statistical reports) as _spreadsheets_, which can then be viewed with Microsoft Excel, [Google Sheets](https://www.google.com/sheets/about/), and other such program. The resulting reports are usually much more detailed than what's seen in Portfolio Boss, though more confusing.

To export the backtest results, click the “Export” button at the top of the [Backtest Strategy Page](_documentation_backtest-strategy-page-overview_.md).

!

That button is only clickable once the strategy is backtested (press the ! button for manual/standard backtest).

Now, the dialog “Export Backtest Results” shows up, which allows you to choose which report to export. These reports are generally similar to the ones you see on the [Metrics](_documentation_metrics-panel-guide_.md), [Performance](_documentation_monthly-performance-panel-guide_.md), [Positions](_documentation_positions-panel-guide_.md), and [History](_documentation_history-tab_.md) Tabs.

!

As you see above, there are six types of report you can export (each will be discussed in the following sections):

*   In-depth trade history, monthly & yearly performances (Excel file),
*   Trade history (positions),
*   Trade history (trading dates),
*   Monthly performance,
*   Yearly performance, and
*   Backtest vs. benchmark comparison.

Select one type, then press the “Browse” button to define the location you want to save the file into:

!

By default the export folder is at “My Documents”, specifically `%UserProfile%\Documents\PortfolioBoss\Backtests` , though you can define it from the File Explorer window that pops up:

!

You can then give the file any name you wish, and press “Save”. This does not create the file, yet. To actually export the file, press the “Export” button on that dialog:

!

Tick the checkbox “Open file after export” to open the file immediately after it's exported; it'll be opened with Microsoft Excel if you have it installed, or with Windows's Notepad. The resulting file has the format “.CSV” (Comma-Separated Values), except the topmost-type which has the format “.XLSX” (Microsoft Excel):

!

Now about the “Field Delimiter” section, it only appears when you select the CSV types:

!

It allows you to choose the character to separate the values/data. You can choose either semicolon (;), comma (,) or tab (whitespace) here.

!

The separator you choose here isn't that important, as the file looks jumbled anyway (_unless_, you're planning to feed these data into some other programs/script). Even if you have Microsoft Excel, the CSV files don't look good except when you use comma as separator. But there's a perfect solution to view the XLSX or CSV files, and that is the [Google Sheets](https://www.google.com/sheets/about/) (it's free!). Look at the video below on how to view the files with Sheets:

[https://portfolioboss.com/wp-content/uploads/2022/12/ftyes56ges5asw.mp4](_wp-content_uploads_2022_12_ftyes56ges5asw.mp4.md)

Let's now discuss each export (report) type from top to bottom as shown on that “Export Backtest Results” dialog:

* * **1.  In-depth trade history, monthly & yearly performances (Excel file):** this export type has the most _complete_ data. It creates an .XLSX file containing three worksheets:

!

*   **Trade History:** this sheet shows the entire history of the backtest, that is, the Positions held each and every day, complete with their entry & exit prices, weights, and gains. There's also the strategy's percentage profit and total account size each day. Let's discuss the columns on this sheet:

!

*   *   _Trading date_: the date of each trading session, excluding weekends/holidays. Each date contains a number of Positions based on [Total Positions to Hold](_documentation_system-settings-panel-guide_.md#totalpositions), but Positions exited at that date will also be included.
    *   _ID_: the identifier for each Position. Each Position entered has a unique ID, and this ID won't be used by other Positions at other dates.
    *   _Symbol_: the ticker symbol for each Position. Sometimes you see “Cash” here too if your strategy uses Cash and/or Limit Orders.
    *   _Position type_: whether the Position is long (bought) or short (short-selling).
    *   _Position weight @ open_: the Positions' weight at the day's market open. It's also the Position's weight when entered and exited. These are a factor of 1 (raw percentage divided by 100).
    *   _Adjusted close_: the adjusted closing price of the instrument on that date.
    *   _Entry price @ open_: this shows the entry price for each Position (could be the day's opening price or the Buy Limit price). It uses adjusted price. Non-empty cells on this column denote freshly entered Positions.

!

*   *   _Exit price @ open_: the exit price for each Position (could be the day's opening price or the Sell Limit price). It uses adjusted price. Non-empty cells on this column denote Positions exited at this day.
    *   _Position weight @ close_: the Positions' weight at the day's market close. Those Positions exited at this day have a weight of 0. It's a factor of 1, as usual.
    *   _Symbol gain_: the instrument's gain, i.e. the change in the instrument's closing price today vs yesterday. If the Position is exited today, it uses the exit Price.
    *   _Position gain_: this is the amount of money the Position has gained/lost since yesterday's close, in relation to/in _percentage_ of the total account size yesterday. It takes into account the Position's exit price, if it's exited today. Therefore the aggregate “Position gain” for all today's Positions (including those exited), equals the total amount of money your account gained/lost since yesterday, shown in the next column.
    *   _Daily gain_: it's simply the percentage gain/loss of the account size between this day and the previous day.
    *   _Compounded daily gain_: the percent gain of the strategy from the beginning of the backtest period up to this day's close. Put another way, it's the dollar profit up to this day (in percent). It's what you see on the [Chart Tab](_documentation_chart-tab_.md) (backtest's equity curve) but minus 100% (because it's the “gain”, not the current account size).

!

*   *   _Portfolio amount_: this is the current account size (portfolio size) at this day's close, in dollar value. You won't see this column populated unless you set a value to the property [“Initial amount”](_documentation_backtest-panel-guide_.md#initialamount) (on the Backtest Panel) before the backtest is executed.

*   **Monthly Performance:** This sheet shows the gain/loss for every month of the whole backtest period, similar as in the [Performance Tab](_documentation_monthly-performance-panel-guide_.md).

!

*   *   _Month_: this column shows all the months (and their year), from the beginning of the backtest period to the latest date.
    *   _Gain_: the percent gain/loss of each month, calculated from the total account size at the previous month's end (last day's market close) to this month's end. Note, the latest month is usually incomplete (no last day yet), so its end date is the latest available date. Ditto the earliest month doesn't usually start at its first trading day, so it's calculated from the earliest available date (the start of the backtest period).
    *   _Compounded gain_: the total gain of the strategy from the beginning of the backtest period up to the end of each month, in percent of the initial capital. Note, this is the total profit (or loss), not the current account size.

*   **Yearly Performance:** This sheet shows the gain/loss for every year of the whole backtest period, similar as in the [Performance Tab](_documentation_monthly-performance-panel-guide_.md).

!

*   *   _Year_: shows all the years during the whole backtest period.
    *   _Gain_: the percent gain of each year, calculated from the account size at previous year's end to this year's end. The latest and earliest years usually aren't whole years, so their gain is calculated from the dates available to them.
    *   _Compounded gain_: the total gain of the strategy from the beginning of the backtest period up to the end of each year, in percent of the initial capital.

* * **2.  Trade history (positions):** this CSV file lists _all_ the distinct Positions _entered_ by the strategy, instead of the day-by-day Positions history as in the previous export type. Here you'll see the Positions' entry and exit dates, prices, weights, and their total gain.

!

One row here is occupied by one distinct Position. These Positions aren't limited to the usual stock/ETF and Cash Equivalent Positions, but includes the Cash Positions as well (the [“Total Positions”](_documentation_metrics-panel-guide_.md#totalpos) metric, as shown on the Metrics Tab and [Stats Tab](_documentation_stats-tab_.md), excludes the Cash Positions). There are also Positions not yet closed (exited), i.e. those at the latest backtest date. Now let's see what columns we have here:

*   _Position ID_: this is the identifier of each distinct Position. Positions with the same symbol (but entered at different dates) have different IDs. The ID starts from 1, and the later a Position is entered, the bigger its ID. The entire Position list here is sorted by this ID (hence by the date they're entered).
*   _Symbol_: the ticker symbol of each Position, including “Cash”. Those with number-suffix within square brackets indicate currently delisted instruments (the number shows how many times they've been delisted).
*   _Position type_: indicates whether the Position is a long-position (bought) or a short-position (short-selling).
*   _Open_: the entry price for each Position (adjusted price). Usually these are the market's opening prices, but could be Buy (or Short) Limit prices as well, i.e. if the limit price is lower (for buying) or higher (for shorting) than the opening price.
*   _Open date_: the date the Positions were entered.
*   _Open weight_: the weight of the Positions when they were entered.
*   _Close_: the exit price for each Position (adjusted price). Usually these are the market's opening prices, but could be Sell (or Cover) Limit prices as well, i.e. if the limit price is higher (for selling) or lower (for covering) than the opening price. For those Positions not yet exited (those at the latest backtest date), their “Close” price here is the market's closing price.
*   _Close date_: the date the Positions were closed (exited).
*   _Close weight_: the weight of the Positions when they were exited.
*   _Gain_: the gain/loss of each Position from _entry to exit_. Those Positions not yet exited have the latest date's closing price to gauge their gain, since they don't have exit prices yet.

* * **3.  Trade history (trading dates):** this is the simplified version of the “In-depth trade history” sheet we discussed earlier. In this CSV file you'll see the Positions held every day, along with their weight, gain, and the action/signal when they will be closed.

!

*   _TradingDate_: this column shows all the trading dates, for the whole backtest period. Each date usually occupies multiple rows, for multiple Positions held on that date.
*   _Symbol_: the ticker symbol of each Position. Cash and Cash Equivalent symbols (e.g. SHY) are listed only once in a given date, even if there are multiple such Positions on that date; there's no grouping indicator (suffix) whatsoever.
*   _Position type_: whether the Position is long (bought) or short (shorted).
*   _Position weight_: the weight of each Position at the day's close (or when the Position was exited).
*   _Gain_: the instrument's gain/loss, based on yesterday's closing price and today's closing price (or the exit price, if the Position is exited).
*   _Action_: the action the strategy will do for each Position at the next trading day. Mostly it's “Hold”, but sometimes you'll see exit actions as well (Sell, Limit Sell, Cover, Limit Cover, or Exit for Cash Positions). Keep in mind these are not trading signals.

* * **4.  Monthly performance:** this CSV file shows the monthly gain for the whole backtest period. Unlike the “Monthly performance” sheet we discussed earlier, we don't have the “Compounded gain” shown here (percent profit from backtest start-date to each month's end). Instead, we have monthly gain comparison between the strategy and its benchmark.

!

*   _Month_: this column shows all the months in the backtest period; but instead of the months' name, we have the months' last trading date. Each row is occupied by each month. Note, the latest month usually hasn't ended yet, so the latest available date is used as its last trading date.
*   _Backtest_: the percent monthly gain/loss for the strategy, calculated from the total account size at the previous month's end (last day's market close) to this month's end. The earliest month usually has its gain calculated from the earliest available backtest date.
*   _Benchmark_: the benchmark's monthly gain/loss.

Note, the gains are raw percentage, not yet a factor of 1. For example 0.182 is actually 0.182%, so you have to divide it by 100 to yield the factor of 1 (that is, 0.00182).

* * **5.  Yearly performance:** this CSV file shows the yearly gain for both the strategy and its benchmark. So as previously, we don't have the “Compounded gain” here.

!

*   _Year_: this column lists all the years in the backtest period. Each row is occupied by a specific year. Each year has its last trading date written here. Note, the latest year usually hasn't ended yet, so its latest available date is used here instead.
*   _Backtest_: the percent yearly gain for the strategy, calculated from the account size at previous year's end up to this year's end. The earliest year's gain is usually calculated from the earliest date available on that year.
*   _Benchmark_: the benchmark's yearly gain, calculated similarly as the strategy's.

As previously, the gains shown here are the raw percentage.

* * **6.**  **Backtest vs benchmark comparison:** This CSV file shows the _metrics_ report for both the strategy and the benchmark. The metrics listed here are the ones shown on the [Metrics Tab](_documentation_metrics-panel-guide_.md), but only for the All Sample period (the whole backtest period). 

!

*   _Description_: this column lists the metrics' name. Top to bottom, they're exactly the ones you see on the Metrics Tab. Please look at the Metrics Tab's documentation (linked above) for the detailed explanation of each metric.
*   _Backtest_: this shows the strategy's metrics score. Each score is for the entire backtest period. They're accurate up to three decimal places, unlike the two decimal places found in the Metrics Tab.
*   _Benchmark_: this is for the benchmark's metrics score.

* * **7.  Now, when it comes to a [multi-strategy](_documentation_multi-strategy_.md),** the export results are generally similar, but there are some important differences:

*   **In-depth trade history, monthly & yearly performances (Excel file):** the Monthly and Yearly performance sheets are similar to what we described, but the Trade History sheet contains additional information:

!

*   *   _Name_: this column shows the name of the active strategies, of each day. For example ! means it's Strategy C there, which is the child of Strategy B, which in turn is the child of Strategy A. Each strategy contains its own set of Positions for that date. You can check on the “Weight” column next, to make sure whether that strategy is indeed active (greater than 0%). Now, sometimes you'll see “Unassigned cash” here as well, which is not part of any strategy. Unassigned cash is simply a cash set aside to trim the weight of a profitable/overweight stack back to its original weight that you set (that is, if your multi-strategy contains **[multiple strategy stacks](_documentation_multi-strategy_.md#MultipleStacks)**); therefore the leaner stack may be infused with the fund to enter its next Positions.
    *   _Weight_: the percentage of account size occupied by each activated strategy. If a parent strategy is fully in Cash Equivalent Positions, its weight will be 0%; even though it's technically not used, it is still active (in its Cash Equivalent Positions).
    *   _Gain_: this column shows the strategy's instruments _average_ _gain_, i.e. from yesterday's close to today's close (or the exit price, if the Positions are exited today).
    *   _ID_: the identifier of each Position. But keep in mind, in a multi-strategy one symbol can occupy multiple Positions (e.g. child strategy activated multiple times). Hence you may see one cell containing multiple IDs (separated by comma) for the same symbol.

!

*   *   _Position weight @ open_: for Cash Equivalent Positions, these are usually 0, because technically there's no such Positions (child strategy is activated instead).
    *   _Position count_: the number of Positions occupied by each symbol.
    *   _Entry price @ open_: each Cash Equivalent symbol from the parent (e.g. SHY) has a note here, like: ! indicating how many Positions are in Cash Equivalent, the name of the child strategy replacing those Cash Equivalent Positions, and the number of Positions held by a single instance of that child strategy. So the total number of replacement Positions held by the child, in that example, is 2 × 3 = 6 Positions.

!

*   *   _Position gain_: instead of a gain for a single Position, you may see multiple Positions' gain (those with the same symbol).

*   **Trade history (positions):** Everything is exactly the same as what's described earlier, except there's a new column “Strategy”, which tells you the name of the strategy each Position belongs to. As usual, if there are arrows, look at the rightmost strategy name:

!

Unlike the previous export type, you will rarely see Cash Equivalent Positions here (unless they're from the last tier strategy). Because Cash Equivalent Positions don't technically exist in that multi-strategy (usually, they're _immediately_ replaced by the child strategy's Positions).

*   **Trade history (trading dates):** As usual, everything is the same except the “Strategy” column:

!

And on each date, the Positions are sorted alphabetically, instead of based on the strategy they belong to. You may also see “Unassigned cash” here, as already explained earlier.

The remaining export types (Monthly Performance, Yearly Performance, and Backtest vs Benchmark Comparison) are exactly the same as what we've discussed before. But there's one metric type not found on the Backtest vs Benchmark Comparison, i.e. “Total trades/Rule count”, since a multi-strategy doesn't have rules/filters  (its basic strategy components do).

As for [**meta-strategies**](_documentation_meta-strategy_.md), their export results are _exactly_ similar to basic-strategies' export results, except the Positions aren't actual instruments (e.g. AAPL, TSLA, etc.), but the strategy-components (like Atlas Order, DB Transactions, Bitcoin Meme Velocity, etc.). Cash or Cash Equivalent Positions still use the ticker symbol, obviously.

!

Positions' prices are based on the strategies' equity curve as seen on the [Chart Tab](_documentation_chart-tab_.md) (the “Backtest” percentage/total return).

[**Back to Top**](_documentation_exporting-the-backtest-result_.md#backtotop)

Discount Applied Successfully!

Your savings have been added to the cart.

Close

You have already reported this .

Search

#### _documentation_fine-tune-a-strategy-for-the-best-settings.md

> Source: https://portfolioboss.com/documentation/fine-tune-a-strategy-for-the-best-settings
> Scraped: 3/1/2026, 2:08:22 AM

[!](_wp-content_uploads_2020_07_Oh-Genie-Make-it-Perfect.png.md)

This is not about finding new rules and filters. Instead, we focus on what we have in hand, and make it perfect.

For example, you have a strategy that you love so much. It is either crafted by you, or conjured up by the Divine Engine from scratch. It doesn't matter; the point is, you believe in its [rules and filters](_documentation_about-filters-rules_.md). But not so much their “values”.

[!](_wp-content_uploads_2020_07_These-Might-Not-Be-Best-Values.png.md)

You can squeeze out the last drops of performance by tweaking their values: an SMA period of 50 days might not be the best value, so you want to try out all the different SMA periods from 10 to 500 days, for example. Ditto the ATR multiplier from -10 to 10 can all be experimented to find the best one for this strategy.

This is what we call **parameterization**, that is, experimenting with different values to find the best one for the parameter. You can count on the Divine Engine to do that for you.

You wouldn't believe how a simple change of value could transform your strategy into a beast. We had a meager strategy that yielded 27% CAGR. But by letting the Divine Engine find the best values, for example 2 days RSI instead of 14 days, the strategy transformed into this 140% CAGR beast:

[!](_wp-content_uploads_2020_07_Specimen-Abe-Reports.png.md)

* * **1.**  Obviously, this scenario assumes you have a complete strategy already (a valid one). This is an example:

[!](_wp-content_uploads_2021_05_567fhj234j7_00000.png.md)

You can create a strategy by yourself. Or load one of the top strategies provided by the previous Divine Engine runs.

* * **2.**  Now, let's enable the Divine Engine by clicking the button ! at the top. Once it's enabled, some panels are spattered with funny looking buttons ! . These panels are:

[!](_wp-content_uploads_2020_07_S1-0-00-00-00.png.md)

[!](_wp-content_uploads_2020_07_S2-0-00-00-00.png.md)

Those are the “parameterization” buttons. With this button, a parameter can be “parameterized”, i.e experimented with different values to find the best one.

If you click on that button, a pop-up appears. Each type of parameter behaves differently in the way you parameterize it.

[!](_wp-content_uploads_2020_07_Parameterization-Dialog.png.md)

We will discuss the different behaviors next.

* * **3.**  Let's get to the SMA filter, and click the parameterization button ! on its “days” parameter, as shown in this screenshot:

[!](_wp-content_uploads_2020_07_SMA-Period-Parameter-Popup.png.md)

If it's a parameter like this, where you can input an arbitrary number such as “200” days, “98” percent, “1.5” multiplier, “30” dollars, etc, you can set the minimum and maximum values to be experimented:

[!](_wp-content_uploads_2020_07_Test-Range-Parameterization.png.md)

Thus we set the values' “range” for that parameter. In the example above, we'll be experimenting from the value of 10 days to 500 days. But is everything between those values experimented?

[!](_wp-content_uploads_2020_07_Step-Size-Parameterization.png.md)

That's where you set the “Step Size”, which defines the increment (step) between the min and max values.

For example, with a “Step Size” of 5, the Divine Engine will experiment from the value of 10, 15, 20, 25, all the way to 500 days. In short, it's a multiple of 5. If you wish all values to be tested (no skipping) then set the smallest “Step Size”. For example, if it's set to 1, the Divine Engine will test 10, 11, 12, 13, 14, 15, all the way to 498, 499, and 500 days.

A larger range and a smaller step size allow for a broader and more thorough search (to find that exotic and high-performing value), but at the expense of a longer backtest time.

[!](_wp-content_uploads_2020_07_Close-Button-Param.png.md)

Once done, you can click the “Close” button.

* * **4.**  Now if it's a parameter that has a fixed set of values, such as “Above”, “Below”, “Greater Than”, “Less Than”, or other values built-in to that parameter, you can select _any_ or _all_ of those values:

[!](_wp-content_uploads_2020_07_Above-Below-Param.png.md)

[!](_wp-content_uploads_2020_07_PB-Pattern-Param.png.md)

[!](_wp-content_uploads_2020_07_Monthly-Switch-Param.png.md)

The Divine Engine will then experiment with those values you selected. If you decide to select all values at once, instead of picking them one by one, use the “Select All” checkbox:

[!](_wp-content_uploads_2020_07_Select-All-Param.png.md)

Conversely, to deselect all at once, disable that checkbox. Or, press the “Reset” button to revert this popup to its default state (no parameterization).

* * **5.**  If it's a parameter that uses ticker symbol, such as Index or Cash Equivalent symbol, you can search the instrument in the ensuing dialog box:

!

The search result can be seen under “Available Instruments”, where you can pick the instruments that you desire:

!

You can enter another search term, and pick yet another set of instruments. The instruments that will finally be tested by the Divine Engine are then listed under “Selected Instruments”:

!

In the example above, you're telling the Divine Engine to experiment with the NDX and NYA indexes, to see which market indicator may best guide this strategy.

* * **6.**  Now as stated earlier, you can also fine tune the rules at the “System Settings” panel. But you must decide on the most important rules first, as they can't be parameterized:

[!](_wp-content_uploads_2020_07_System-Settings-Non-Parameterizable.png.md)

The most important rules are:

*   “System” (whether the strategy is continually or periodically switching its Positions).
*   “If Position Triggers Sell Filter…” (whether the strategy will park the liquidated position on hard cash, or cash-equivalent).
*   “Position Type” (whether the strategy is trading Long or Short positions).
*   “Buy Order Type” (whether entering a position uses a Market Order or a Limit Order).
*   “Sell Order Type” (whether exiting a position uses a Market Order or a Limit Order).

You can read the help page for the [“System Settings” panel](_documentation_system-settings-panel-guide_.md) for a more thorough explanation.

Then, you can parameterize the rest of the rules so the Divine Engine will find the best values for them:

[https://portfolioboss.com/wp-content/uploads/2020/07/Parameterizing-System-Settings-clip.mp4](_wp-content_uploads_2020_07_Parameterizing-System-Settings-clip.mp4.md)

*   “Monthly Switch on Open of” (the Divine Engine will find the best date to switch your Positions).
*   “Don't Switch if Position is Still in Top” (it will find the appropriate top % rank for existing Positions to be retained).
*   “Cash Equivalent” (it will find the best instrument to park your money).
*   “Total Positions to Hold” (it will find the perfect amount of Positions held at any given time, to spread their risks).
*   “Buy/Sell Order Limit” (it will find the best Limit price on your Buy/Sell orders).

Note, the rules “Buy/Sell Order Limit” are only visible if you set the “Buy/Sell Order Type” to “N ATR Limit Order”.

* * **7.**  Obviously, you don't have to parameterize everything. You can leave alone those values you believe are already correct. Parameters that have been parameterized will have their “parameterization” button highlighted with a color:

[!](_wp-content_uploads_2020_07_Parameterization-Buttons-Color.png.md)

* * **8.**  Now let's go to the “Backtest Parameterization” Panel.

[https://portfolioboss.com/wp-content/uploads/2021/05/567ghj35msw.mp4](_wp-content_uploads_2021_05_567ghj35msw.mp4.md)

Things will be different here than the previous scenarios. First, instead of “Evolutionary” Search, we'll be using the [“Random” Search Algorithm](_documentation_backtest-parameterization-panel.md#Random).

“Random” search is more suited for fine-tuning a strategy. Through brute force, it tests all the different values that you picked, combining one parameter's value to another parameter's value. For example, in one test it combines the “Above” value with the “200 days” value. While in another test it combines the “Below” value with the “20 days” value. And so on and so forth.

[!](_wp-content_uploads_2020_07_Above-Below-200-20-SMA.png.md)

The best combinations will then be pulled as a top strategy.

Another thing is to set “Rule Set Parameterization” to “Manual”, because we trust the existing rules/filters to be perfect for this strategy. We don't want new rules to break it.

[https://portfolioboss.com/wp-content/uploads/2021/07/7u8956ysgs.mp4](_wp-content_uploads_2021_07_7u8956ysgs.mp4.md)

Then you set the [“Fitness Functions”](_documentation_backtest-parameterization-panel.md#FitnessFunctions) as you see fit. For example here, I added the “Score” and “Avg. Drawdown” Fitness Functions.

* * **9.**  Next, we will define the amount of backtests to be executed. Take a look at the parameter “Execute n random backtests” here:

[!](_wp-content_uploads_2021_05_4564dgdg8_00000.png.md)

One backtest is for one strategy with its distinct set of combinations. We call each backtest an “iteration”. Thus if we have 29,850 iterations as shown in the screenshot above, it means the Divine Engine will create and test 29,850 strategies, each with different combinations (of values).

The more iterations you set, the longer it takes for the Divine Engine to finish. But that also means your “search” is more thorough and exhaustive, thus potentially finding that exotic high performing combination. If you set it too low, on the other hand, not all combinations will be tested.

Preferably, you set the amount of tests to match the “Number of Parameter Combinations” as shown here:

[!](_wp-content_uploads_2021_05_fgh456353j_00000.png.md)

That means all possible value combinations are tested. But usually, satisfying that number means an impossibly long backtest time. Therefore, for efficiency reasons, you can set the parameter to a value of 3.

[!](_wp-content_uploads_2021_05_rhw35yhdfh89_00000.png.md)

Even if you set it to a value of 1, all values that you picked will be tested; but not _all_ their different combinations.

* * **10.**  If, for one reason or another, you have doubts on a certain filter, you can let the Divine Engine decide its fate. Very similar to the previous scenario:

[!](_wp-content_uploads_2020_07_Leftmost-Enabled-Params-0-00-00-00.png.md)

Click on the leftmost parameter that says “Enabled”, and a dropdown appears:

[!](_wp-content_uploads_2020_07_Enabled-Disabled-Random.png.md)

If you choose “Random”, the Divine Engine decides whether this filter will be disabled or enabled, depending on its performance. If you're certain the filter is useful, set it to “Enabled”.

You may recall this parameter used to show “Replaceable” or “Not Replaceable”, instead of the “Enabled/Disabled/Random”. Well actually they all function the same way despite the different names.

[!](_wp-content_uploads_2020_07_EDR-RNR.png.md)

The former show up when you set “Rule Set Parameterization” to “Random Selection”. When you set it to “Manual”, the dropdown changed into “Enabled/Disabled/Random”.

[!](_wp-content_uploads_2021_05_57gkjg3f_00000.png.md)

* * **11.**  So let's fire up the Divine Engine backtest. Press the button “Start Local Test” as shown below (or press the shortcut key F6):

[https://portfolioboss.com/wp-content/uploads/2022/11/gyd7u56heds.mp4](_wp-content_uploads_2022_11_gyd7u56heds.mp4.md)

A confirmation dialog shows up, allowing you to write a memo describing this backtest (optional). If you don't want this dialog for future _local_ backtests, tick the checkbox “Don't show again”. If everything's good, click OK or press Enter on your keyboard.

Notice the button “Start the Boss” is grayed out. That's because the “Random” search can only be processed locally in your machine. So you use that button we showed above (a _local_ Divine Engine backtest specifically designed for the “Random” search). The Boss cloud platform on the other hand, is specifically architectured to benefit the “Evolutionary” search.

[!](_wp-content_uploads_2020_07_Random-Search-Progressbox.png.md)

The progress box displays some of the iterations being processed or already completed (the rest may not be shown here). Unlike The Boss where you can still use the software, here you must wait it out to finish. Don't worry, the “Random” search is less compute-intensive than the “Evolutionary” algorithm. Therefore you can wait from a few minutes to a few hours at most, unless you have a titanic amount of iterations.

You may notice there are other buttons there:

!

**Queue Local Test** – This allows you to queue (pend and collect), local Divine Engine backtest(s) to be processed later. Each time you click this button, or press the shortcut key Ctrl + F11, whatever rules you have now i.e. filters, parameters, parameterization settings, and portfolios will be stored as a queued [Backtest Item](_documentation_backtest-results-tab.md#TheBacktestItemsList). So if you click this button multiple times, there will be multiple Backtest Items queued. Queueing allows you to start a local Divine Engine backtest at a later time, without losing your strategy's rules & settings. It's also useful so you can create and store multiple baselines, especially for fine-tuning multiple form of baselines. Otherwise you must wait a baseline to finish its Divine Engine backtest before creating another one; it may cause you to forget what your other baselines are supposed to be. For example, one baseline is used for a Nasdaq 100 with RSI, Impulse ranking, and Retracement filters; while others are S&P 500 with SMA Position, Volatility ranking, and Position Duration filters:

[https://portfolioboss.com/wp-content/uploads/2022/11/gutyudnh6es5ha.mp4](_wp-content_uploads_2022_11_gutyudnh6es5ha.mp4.md)

**Start Local Queue** – Once you're ready to backtest the queued items, click this button. Its shortcut key is F11. They will be backtested one by one, starting with the earlier/older item. Once the first one is finished, it immediately processes the second one, and so on (the backtest progress dialog shows 1/2 toward 2/2, etc). Don't confuse “Start Local Test” with the “Start Local Queue”; you want to use the latter to start processing the queued items. If you use the former, the queue won't be processed but instead another new Divine Engine backtest is immediately processed. Note, if you cancel any of the queued process (e.g. while it's showing 2/3 and you cancel the process), the next queued items will be cancelled, not just that one item you cancelled. So to continue processing them, click the “Start Local Queue” again (the cancelled Backtest Item will stay cancelled, while the one already processed will of course stay “Finished”).

[https://portfolioboss.com/wp-content/uploads/2022/11/8ygdrh56e5sbdt.mp4](_wp-content_uploads_2022_11_8ygdrh56e5sbdt.mp4.md)

Note, pressing the button “Start local queue” brings you a confirmation dialog: that these backtests will hog your computer resources. Tick the checkbox “Don't show again” so it doesn't show up in future backtests, and press “Continue”.

* * **12.**  Once it's finished, you can look at the [Divine Engine Results Tab](_documentation_backtest-results-tab_.md). Where the top strategy was pulled, instead of “Generations” it now shows “Iterations”. For example with “Iteration 065”, that strategy was actually the 65th test/iteration to be done.

!

You can load a top strategy as usual by clicking its “Load Parameters” button ! . Also note there's no “Fitness Series” chart when Random search is used (it uses “Mini Charts” instead, explained next).

The memo you wrote for this backtest will be shown here as well.

* * **13.**  If you look at the strategy's parameters, there's a small colorful icon next to each of them.

[!](_wp-content_uploads_2020_07_Colorful-Mini-Charts.png.md)

These are called the “Mini Charts”. If you click them, a popup chart appears.

[!](_wp-content_uploads_2020_07_Mini-Chart-Content.png.md)

The Mini Chart shows the parameter's performance at different values that you picked. Look at which value has the highest orange line (Best Fitness IS):

[!](_wp-content_uploads_2020_07_Highest-Orange-Line-0-00-00-00.png.md)

The value that has the highest “Best Fitness IS” score is the value applied for this parameter. The “Mini Charts” are not really that important, but if you crave for the detailed explanation, visit the help page [here](_documentation_backtest-parameterization-panel.md#TheMiniChart).

Now if you look at the parameter's value itself, there are values inside the parentheses, and outside of them:

[!](_wp-content_uploads_2020_07_Parantheses-Values.png.md)

The value outside the parentheses is the value _applied_ to that parameter (in the example above, “Total Positions to Hold” is set to “3” by the Divine Engine). Inside the parentheses is your parameterization range. If this view looks confusing, you can simply disable the Divine Engine.

[!](_wp-content_uploads_2020_07_Disable-Divine-Engine-at-Top.png.md)

Don't worry, the value applied by the Divine Engine still remains. And the parameter appears neater now.

[!](_wp-content_uploads_2020_07_Disabled-Divine-Engine-Neat.png.md)

If you re-enable the Divine Engine, the parameterization settings you set are still there. Even if you closed Portfolio Boss, they're still remembered. If you wish to remove all those parameterizations at once, click the “Reset Divine Engine Fields” button at the top:

[https://portfolioboss.com/wp-content/uploads/2021/05/54rhfh23hjj.mp4](_wp-content_uploads_2021_05_54rhfh23hjj.mp4.md)

That way, you can start the parameterizations afresh should you wish to fine-tune the strategy again. But if you wish to reset the parameterization one by one, click the “parameterization” button ! of each parameter, and press “Reset” there:

[!](_wp-content_uploads_2020_07_Reset-Parameterization-Button.png.md)

* * *

#### Notes:

*   While fine-tuning existing parameters, the Random Search Algorithm can also _add random_ rules/filters (with their random values) to the strategies. You do this by selecting the option “Random Selection” on the property “Rule Set Parameterization”. There is no natural selection and evolution at play here, simply slapping random rules/filters _for every iteration_, in the hope it may beef up the strategies. Obviously rules/filters will be added for as long as there are iterations, as you see on the property “Execute n Random Backtests…”. Therefore it's dependent on your _parameterization_ of the _existing rules_.

!

*   A [Meta-strategy](_documentation_meta-strategy_.md) can benefit from this Random Search Algorithm (unlike a [multi-strategy](_documentation_multi-strategy_.md)). So essentially, everything's the same as a basic-strategy we've seen here, except its portfolios are comprised not of actual financial instruments but of basic-strategies (taken as if they're stocks/ETFs). That way, you can have a multi-layered winning system in which not only the “trading system” is perfectly crafted by the artificial intelligence, but its “instruments” as well (component-strategies created by the Divine Engine). It's like you created a bunch of winning ETFs on your own, and on top of that you trade these “ETFs” with a winning system.

*   If you close Portfolio Boss (or it crashed) while a local Divine Engine backtest is underway, the next time you open Portfolio Boss you'll be prompted either to continue or stop that backtest.

!

*   When the local Divine Engine backtest is underway, Portfolio Boss may pause it momentarily to do essential tasks in the background, such as downloading EOD data and sending email notifications for those strategies you use.

*   Obviously, Random Search Algorithm doesn't expend a single compute hour credit as it's processed locally in your computer. You need to be wary of that electricity bill though.

[**Back to Top**](_documentation_fine-tune-a-strategy-for-the-best-settings_.md#backtotop)

You have already reported this .

#### _documentation_fixed-atr-stop-loss-filter.md

> Source: https://portfolioboss.com/documentation/fixed-atr-stop-loss-filter
> Scraped: 3/1/2026, 2:08:47 AM

!

As the name implies, this filter serves as a stop-loss to exit your position (as a Sell Filter if long, or a Cover Filter if short).

It will exit a long position whose _closing price_ drops below a certain distance (line). For a short position, the closing price must break above such a line. This line is plotted by: measuring the instrument's [ATR](_documentation_n-atr-above-below-sma-filter_.md) (for a certain period), which is then multiplied by a certain number. This multiplied ATR is then _subtracted_ from the closing price of the previous day (or _added_, for a short position). Note, the ATR value also comes from the previous day.

In other words, if _today's_ closing price violated such a line (which is based from _yesterday's_ ATR and closing price), the position will be liquidated _tomorrow_. As shown in the illustration below, the line is colored blue:

!

Thus, it's a flexible stop-loss that may go up or down, based on the instrument's closing price and volatility; unlike the [Perfect Stop Filter](_documentation_perfect-stop-filter_.md) where the stop-loss line is trailing continually upward (or downward, for a short position). On one hand, this dynamic behavior may actually expose you to greater losses if the downtrend is slow. On the other hand, it prevents your from getting stopped too early, so you ride your position along unless there's a big one-day drop.

* * **1.**  The first parameter defines the ATR multiplier:

!

The sweet spot is usually 2.5 or 3. So for example, if the price drops greater than 2.5 times the volatility of the past 10 days, it's a good sign of a trend change. Clearly, a bigger value here means a wider stop-loss.

* * **2.**  The second parameter defines the ATR period:

!

For example, “10 days” means the average price change of the past 10 days (in dollar value). Generally, use a shorter period less than 1 month here (10 or 14 days is the sweet spot) so the volatility is representative of the recent price behavior. Longer period _may be_ useful for long-term trading (might as well invest); remember that Portfolio Boss is mainly swing trading based on the daily candles.

* * *

#### Note:

The visual indicator is plotted alongside the price chart (on the [Instrument Tab](_documentation_instrument-tab_.md)). For a long position, it appears below the prices:

!

For a short position, it shows up over the prices:

!

[**Back to Top**](_documentation_fixed-atr-stop-loss-filter_.md#backtotop)

You have already reported this .

#### _documentation_frequently_asked_questions.md

> Source: https://portfolioboss.com/documentation/frequently_asked_questions
> Scraped: 3/1/2026, 2:09:23 AM

[!](_wp-content_uploads_2019_10_FAQ-Tab.png.md)

This Tab contains the list of Frequently Asked Questions. Simply click on a question, and an answer will be expanded below it. Please note, we have listed some more FAQs in this user guide than the one contained on this Tab.

* [_Why didn't I receive an email notification from Portfolio Boss?_](_documentation_frequently_asked_questions_.md#wdiraenfpb)
* [_Instrument X fell below its Y day moving average. Why didn't Portfolio Boss send a notification?_](_documentation_frequently_asked_questions_.md#ixfbiydma)
* [_Instrument X is no longer traded. Should I remove it from Portfolio Boss?_](_documentation_frequently_asked_questions_.md#ixinlt)
* [_Instrument X is no longer part of the Nasdaq 100. Should I remove it from Portfolio Boss?_](_documentation_frequently_asked_questions_.md#ixinlpotn)
* [_Can I import instruments into Portfolio Boss?_](_documentation_frequently_asked_questions_.md#ciiiipb)
* [_I found a better CAGR/MAR/DD, but people are warning me about cherry picking/data snooping. What exactly do they mean?_](_documentation_frequently_asked_questions_.md#ifabcbpawm)
* [_The backtest displayed a warning that there are extreme single day gains in the trade history. What does that mean?_](_documentation_frequently_asked_questions_.md#tbdawttaesdg)
* [_Why do I see a black screen when clicking on a question mark to look at a tutorial?_](_documentation_frequently_asked_questions_.md#wdisabs)
* [_Why does Portfolio Boss disappear after I try to open it?_](_documentation_frequently_asked_questions_.md#wdpbdaittoi)
* [_Can I trade inside an IRA?_](_documentation_frequently_asked_questions_.md#citiai)
* [_Is this legal?_](_documentation_frequently_asked_questions_.md#itlegl)
* [_How many signals will I receive each day?_](_documentation_frequently_asked_questions_.md#hmswired)
* [_What time do I receive trade signals?_](_documentation_frequently_asked_questions_.md#wtdirts)
* [_How do I receive the trade signals?_](_documentation_frequently_asked_questions_.md#hdirtts)
* [_How do I contact Portfolio Boss?_](_documentation_frequently_asked_questions_.md#hdicpb)
* [_What are the Terms of using Portfolio Boss?_](_documentation_frequently_asked_questions_.md#wattoupb)
* [_How does Portfolio Boss deal with data privacy?_](_documentation_frequently_asked_questions_.md#hdpbdwdp)
* [_How will Portfolio Boss software be delivered?_](_documentation_frequently_asked_questions_.md#hwpbsbd)
* [_What if I don’t like Portfolio Boss?_](_documentation_frequently_asked_questions_.md#wiidlpb)
* [_What devices can I use the Portfolio Boss on?_](_documentation_frequently_asked_questions_.md#wdciutpbo)
* [_My anti-virus software flagged Portfolio Boss, what's this?_](_documentation_frequently_asked_questions_.md#wimavsfpb)
*   _[My Drive C is full. How can I change PB database folder to use another drive?](_documentation_frequently_asked_questions_.md#MDCIF)_
* [_Portfolio Boss crashed often lately, what should I do?_](_documentation_frequently_asked_questions_.md#PBcrash)

* * **1.**  **_Why didn't I receive an email notification from Portfolio Boss?_**

In order to receive notifications from Portfolio Boss, all of the following must apply:

*   *   Make sure the automation setting [“Send email notification for strategies that have notifications enabled”](_documentation_automation-tab-guide_.md#sendemailnotif) is enabled.
    *   At least one strategy must have notifications enabled. You can do this in the [“Strategy Management”](_documentation_strategy-management-page-overview_.md#notifspacer) page.
    *   Preferably, Portfolio Boss must be running 24/7. Hibernation/sleep mode should theoretically work, but if you're not getting notifications, try not using it.
    *   Check your spam folder to make sure the notification was not marked as spam.
    *   Check the [log](_documentation_application-log-page_.md) to see if there are any errors that might indicate a problem with sending notifications.

By far the easiest to set up is using the default Portfolio Boss Mail Service, since you only have to enter one or more recipient addresses. Should you for whatever reason want to use any of the other options then:

*   *   Make sure you've entered correct email settings. Verify this by sending a [test email](_documentation_automation-tab-guide_.md#sendtestemail).
    *   In case you're using 2 factor verification for your email account, make sure to create a separate app password for Portfolio Boss, because it doesn't support 2 factor verification.
    *   In case you're not using 2 factor verification and you receive emails that a login attempt has been blocked, consider switching to 2 factor verification and make an app password for Portfolio Boss.

* * **2.**  **_Instrument X fell below its Y day moving average. Why didn't Portfolio Boss send a notification?_**

The following is required for an instrument to trigger a signal:

*   *   Make sure you compare the correct moving average type (SMA, EMA, or whatever type Portfolio Boss might support in the future).
    *   The instrument closed below the moving average. If it falls below the moving average intraday, but closes above, no signal will be triggered.
    *   Portfolio Boss uses the adjusted close Yahoo provides. So if the close is below, but the adjusted close isn't, no signal will be triggered.

* * **3.**  **_Instrument X is no longer traded. Should I remove it from Portfolio Boss?_**

No. You can mark it as [“Suspended”](_documentation_portfolio-instruments-panel-guide_.md#suspendedcheckmark). That way Portfolio Boss will no longer try to download price data for it, but your backtests will stay accurate. It of course won't pick the instrument after its last trading day. Note that an instrument that's no longer traded will eventually be marked as [“Delisted”](_documentation_portfolio-instruments-panel-guide_.md#delistedcheckmark), but it takes time; all the bureaucratic works need to finish before it is marked as such. So instead of waiting, you can mark it as “Suspended”.

* * **4.**  **_Instrument X is no longer part of the Nasdaq 100. Should I remove it from Portfolio Boss?_**

No, because it will change the result of your backtests. You could mark it as [“Suspended”](_documentation_portfolio-instruments-panel-guide_.md#suspendedcheckmark), but no longer being part of the Nasdaq 100 doesn't change the exponential nature of the instrument, which was our initial rule for adding instruments.

* * **5.**  **_Can I import instruments into Portfolio Boss?_**

Currently there's no direct way, but there's a workaround:

*   Open the Windows “Notepad” and type in the symbols top to bottom. The Portfolio's name can be written at the beginning of the file, enclosed by square brackets. Something like this:

\[Name of the portfolio\]
SYMBOL1
SYMBOL2
SYMBOL3

[https://portfolioboss.com/wp-content/uploads/2020/08/Typing-Symbols-in-Notepad-clip.mp4](_wp-content_uploads_2020_08_Typing-Symbols-in-Notepad-clip.mp4.md)

*   Now, save the file with the EBTP extension. To do this, from the dropdown “Save as Type”, choose “All Files”. Then type the file name on the “File Name” field. The name must be followed by the extension .EBTP (with the dot character).

[https://portfolioboss.com/wp-content/uploads/2020/08/Saving-the-EBTP-clip.mp4](_wp-content_uploads_2020_08_Saving-the-EBTP-clip.mp4.md)

*   Once the file is created, you can double-click it to be processed by Portfolio Boss. Or, you can go to the [“Portfolio Management”](_documentation_portfolio-management-page-overview_.md) page and click on the Restore button ! at the top of that page. Select the file you've just created and click the Open button.

[https://portfolioboss.com/wp-content/uploads/2020/08/Loading-the-EBTP-clip.mp4](_wp-content_uploads_2020_08_Loading-the-EBTP-clip.mp4.md)

*   A new portfolio is now created, containing instruments you specified in the file. Portfolio Boss automatically downloads all the necessary data for those symbols. Even if the symbol is now delisted, Portfolio Boss will know accordingly.

If you don't want to type the symbols manually, you can copy the textual symbols from a financial website. Let's say you have hundreds of symbols you want to import into Portfolio Boss. Thus you go to a website that provides such a list, for example [www.marketindex.com.au/all-ordinaries](https://www.marketindex.com.au/all-ordinaries) and copy-paste the symbols toward Notepad. But copy-pasting from a complex website may not be as straightforward as it seems, so here are the steps:

*   Make sure to fully expand the table that lists the instruments. In the case of that website above, press the button “Show All Companies”.

[!](_wp-content_uploads_2020_08_Symbol-Website-Screenshot.png.md)

*   Now, select the entire table from the _outside._ That is, place your cursor at the top left area of the table, but _outside_ of it. Then click-drag your mouse toward the bottom right area of the table, again releasing the mouse outside the table.

[https://portfolioboss.com/wp-content/uploads/2020/08/Selecting-Website-Table-clip.mp4](_wp-content_uploads_2020_08_Selecting-Website-Table-clip.mp4.md)

You can also select it from the bottom-right corner to the upper-left. It doesn't matter. The point is, you select the entire table from the outside.

*   Now that you have the _entire_ table selected,  press Ctrl + C on your keyboard to copy the contents.
*   We will paste them toward a spreadsheet first. So go to [sheets.google.com](https://sheets.google.com/) and create a new spreadsheet. Or you can use Microsoft Excel if you have one.

[https://portfolioboss.com/wp-content/uploads/2020/08/Copy-Pasting-Spreadsheet-clip.mp4](_wp-content_uploads_2020_08_Copy-Pasting-Spreadsheet-clip.mp4.md)

Press Ctrl + A on your keyboard to select all cells, then press Ctrl + V to finally paste the data. If there's a warning dialog, just press OK to proceed.

[!](_wp-content_uploads_2020_08_Excel-Warning.png.md)

*   Now click on any empty cell whose **row** _parallels_ the first symbol. For example here, click on cell L2 as it parallels the symbol “360” at Row 2.

[!](_wp-content_uploads_2020_08_Parallel-Row-Spreadsheet.png.md)

On that cell L2, copy and paste this formula `=CONCAT(B2, ".AX")` and press Enter. That way, the cell L2 now contains the “concatenated” (combined) contents from cell B2 and the text string .AX, therefore it now reads “360.AX”. This is to append the symbol with the .AX extension so Portfolio Boss recognizes it as Yahoo data. If the symbol is located at a different cell, let's say C2, then replace B2 with C2 on that formula.

[https://portfolioboss.com/wp-content/uploads/2020/08/Concatenate-Formula-Spreadsheet-clip.mp4](_wp-content_uploads_2020_08_Concatenate-Formula-Spreadsheet-clip.mp4.md)

*   We'll do that concatenation to all symbols, so select cell L2 and press Ctrl + C. Then click the Column L header, thus all cells within Column L are selected. Then press Ctrl + V to paste. The cells now contain their respective symbols combined with the string .AX. It is these contents that will be used by Portfolio Boss.

[https://portfolioboss.com/wp-content/uploads/2020/08/All-Cells-Pasted-Formula-clip.mp4](_wp-content_uploads_2020_08_All-Cells-Pasted-Formula-clip.mp4.md)

*   Now let's copy the contents of all that Column L, and paste it to the Notepad. But before we do that, click the topmost cell that says Code.AX, and press Delete, we don't want that content because it's not part the symbol. Then, click the Column L header again to select all its cells, and press Ctrl + C.

[https://portfolioboss.com/wp-content/uploads/2020/08/Copy-Cells-Contents-clip.mp4](_wp-content_uploads_2020_08_Copy-Cells-Contents-clip.mp4.md)

*   Then open Notepad as already described, and press Ctrl + V to paste the data. You'll see the symbols are sorted top to bottom; and at the file's beginning you can write the portfolio's name as usual. Note the lower part of the file contains empty symbols (only the extension .AX). It's okay, just leave them be.  Save the file as EBTP, and load it to Portfolio Boss as you already know.

[https://portfolioboss.com/wp-content/uploads/2020/08/Pasted-into-Notepad-clip.mp4](_wp-content_uploads_2020_08_Pasted-into-Notepad-clip.mp4.md)

* * **6.**  **_I found a better [CAGR/MAR/DD](_documentation_metrics-panel-guide_.md), but people are warning me about cherry picking/data snooping. What exactly do they mean?_**

Cherry picking or data snooping in itself is not bad. It's the fact that you're taking advantage of unknowable data that makes it bad. You see, CAGR/MAR/DD are all based on hindsight.

Now, what does this mean?

Suppose you add stock X and run a backtest over the past 10 years. You notice the CAGR/MAR/DD improves and you may think therefore the stock is a keeper. Or the opposite happens and you might believe the stock should be removed from Portfolio Boss. Now turn back the clock 10 years. You now no longer have the data of these 10 years, since they haven't happened yet. And no data means no way of knowing the effect of stock X on the CAGR/MAR. This means an improved CAGR/MAR/DD cannot be a reason to add or remove a stock. Because if you do, you're really expecting the performance of stock X in the next 10 years to be the same as the past 10 years. And past performance (good or bad!) is no guarantee for the short term future (with us [switching](_documentation_system-settings-panel-guide_.md#monthlyswitch) every month).

So what good is the CAGR/MAR/DD then?

These numbers should be interpreted as an indication of whether whatever theory you're testing is worth trading. For instance: the theory behind EGR is that there's an edge in buying exponential stocks above a certain market cap on the 6th trading day that are in the top right corner of the chart and just had a dip. Portfolio Boss shows us that indeed this edge exists. Note that the theory doesn't care which exponential stocks are used. Dan just added all of them (he just left out Biotech to get a more diversified picture). Basically the CAGR says if you had stuck with this theory for the past X years, this would have been your result. (In reality of course a bit lower due to commission and slippage). Because the theory isn't tied to the performance of single stocks, it's reasonably safe to extrapolate the graph into the future. It becomes safer as the backtest period becomes longer. But if you're polishing up the CAGR by taking out bad stocks and putting in good ones, you're undermining the validity of the CAGR, because suddenly the CAGR starts depending on the performance of single stocks.

What then would be a reason to add/remove a stock?

Removing a stock will hardly ever happen, unless a company decides to go do something completely different that no longer matches the theory you're testing (suppose you have a theory about the textile industry and therefore deem a certain Berkshire company no longer fitting because they stopped doing textile stuff; I know, bad example…). If a stock is no longer traded (FIO for instance), you can still leave it in Portfolio Boss for backtesting purposes, since it will give you a more historically accurate picture. It won't be picked by Portfolio Boss again after its last trading date.

Adding a stock should be done because it matches the theory you're testing. Maybe you think that a certain type of industry has more potential than others. Or who knows, maybe you believe there's a market edge in companies that have been founded under a full moon. But whenever you're adding a stock, don't be smarter than the market, instead just add all stocks that match your criteria and then let Portfolio Boss calculate whether your criteria have any tradeable edge in them. Of course, when new companies are founded that match the criteria, you can simply add them as well.

* * **7.**  **_The backtest displayed a warning that there are extreme single day gains in the trade history. What does that mean?_**

It means that somewhere in the backtest, Portfolio Boss held one or more positions that jumped over 300% in a single day. This is caused by errors in the ‘End of day' data we obtain from Yahoo. Since Yahoo has no official channels to report such errors, you have no choice but to remove the instrument from your portfolios.

If you don't, your [CAGR](_documentation_metrics-panel-guide_.md#cagr) will be artificially inflated and future returns will be disappointing.

Even in the extremely unlikely event that a stock really manifested such gains, we advise you to remove the instrument, because having to rely on such impossible gains to happen again makes for a very bad strategy.

* * **8.**  **_Why do I see a black screen when clicking on a question mark to look at a tutorial?_**

Some systems seem to have restrictions in place that prevent the tutorial video from playing within the Portfolio Boss application. Usually installing Adobe Flash Player solves this issue. Or if you prefer to stay away from Flash, you can also go to [https://api.portfolioboss.com/Tutorials/](https://api.portfolioboss.com/Tutorials/) and play the videos from there.

Note that these video tutorials have been superseded by the online User Guide, so unless you're using an old version of Portfolio Boss, when you click the question mark icon you'll be brought to the online documentation pages.

* * **9.**  **_Why did Portfolio Boss disappear after I tried to open it?_**

Portfolio Boss does not actually disappear or close, but its window might be located off the screen. This issue may be encountered if you're using multiple monitors. To reposition the window back to its default location, press Shift + Right-click on the Portfolio Boss taskbar icon, and a pop-up appears:

[!](_wp-content_uploads_2020_08_PB-Shift-Right-Click-101.png.md)

From there, choose “Move”, and press the keyboard arrow buttons until Portfolio Boss window shows up. Or, as soon as you choose “Move”, can click-drag and move the mouse until the window appears).

Alternatively, you can also reset PB user settings (including its appearance and window location) by:

*   *   closing Portfolio Boss. You can do this by choosing “Close” on the taskbar pop-up as shown above.
    *   with File Explorer, go to: `%LocalAppData%\PortfolioBoss\Data`

[!](_wp-content_uploads_2020_03_PB-Appdata-folder-address-888.png.md)

(you can copy and paste that address to the address field as shown above, and press enter.)

*   *   in that folder, delete the file “PortfolioBoss.User”,
    *   now open Portfolio Boss again, and it will be loaded with the default appearance settings, including the window's location.

* * **10.**  **_Can I trade inside an IRA?_**

Yes! Brokers like Interactive Brokers allow you to open a margin IRA so you can trade on unsettled funds. Please consult your tax professional.

* * **11.**  **_Is this legal?_**

Yes, perfectly. While we have an advantage, it’s not an unfair advantage.

* * **12.**  **_How many signals will I receive each day?_**

If you’re trading a maximum of 10 stocks at once, then you’ll receive 1-2 signals per day on average. You can test different settings inside Portfolio Boss.

* * **13.**  **_What time do I receive trade signals?_**

Typically after 5 PM Pacific or 8 PM Eastern when quotes are updated. Simply place your orders with your broker for execution the next morning.

* * **14.**  **_How do I receive the trade signals?_**

You receive the Oracle Orders trade signals inside our trading platform, Portfolio Boss. You can also receive the signals automatically by email.

* * **15.**  **_How do I contact Portfolio Boss?_**

Please [visit our contact page by clicking here](_contact_.md) to reach the Portfolio Boss staff for any questions or support needed with your Portfolio Boss software. Portfolio Boss is a US based company located in the state of California.

* * **16.**  **_What are the Terms of using Portfolio Boss?_**

You can review the entire terms of use for the Portfolio Boss software and Portfolio Boss website by visiting our terms and conditions page by [clicking here](_terms-of-service_.md).

* * **17.**  **_How does Portfolio Boss deal with data privacy?_**

We take data privacy very seriously and respect your right to privacy. For our current privacy policy please visit our privacy policy page by [clicking here](_privacy-policy_.md).

* * **18.**  **_How will Portfolio Boss software be delivered?_**

All Portfolio Boss purchases are delivered online as a download. There is no shipped software disk or other shipped product. You will have instant access to the Portfolio Boss software download after your purchase has been completed.

* * **19.**  **_What if I don’t like Portfolio Boss?_**

Each product/service has its own guarantee. Please refer to the sales material.

* * **20.**  **_What devices can I use the Portfolio Boss on?_**

You can use the Portfolio Boss software on any Windows based computer or on a Mac running Windows through [Apple's boot camp](https://support.apple.com/boot-camp) or using virtualization software tools like [VM Ware Fusion](https://www.vmware.com/products/fusion.html) or [Parallels](https://www.parallels.com/).

* * **21.**  **_What if my anti-virus software flagged Portfolio Boss?_**

Some anti-virus programs tend to be over-cautious and raise false positives on completely legitimate software, such as Portfolio Boss.

Why do they do this? If a program displays behavior that is also commonly found in bad guy’s software, they assume it’s a bad software. Unfortunately this is pretty much the equivalent of going to a hardware store and putting all hammers under lock and key, labeling them as dangerous weapons because they have been used in crimes as well. Only if enough people report the program to be safe, the program gets a good reputation and will no longer be flagged. For big software vendors with millions of users, this is not an issue, but small software companies like ours are out of luck here.

So what can you do about it?

Most anti-virus programs allow you to report a file as being safe or to **exclude** the file from being scanned. Since there are too many different anti-virus programs out there, we can’t give you detailed steps on how to do this. You’ll have to ask Google or consult with the vendor of the anti-virus program.
Also, when you exclude Portfolio Boss, make sure you exclude the path `%LocalAppData%\PortfolioBoss\Application\PortfolioBoss.exe` rather than the path to the quarantined file.

If Windows gives you the message _“__This app can’t run on your PC”_, then most likely the anti-virus program already removed what it thinks is the ‘bad behavior’ from PortfolioBoss.exe. Modifying this file however causes our digital signature to be removed, which causes Windows to start mistrusting the file.
In this case you need to **reinstall** Portfolio Boss and make sure you **exclude** it from your anti-virus program, before it scans and ‘fixes’ the newly installed version.

So, how can you check if PortfolioBoss.exe hasn't been modified by your anti-virus software (or even by a virus)? Here are the steps to check if the **Digital Signatures** (to ensure the software stays pristine, un-modified) have been removed:

[https://portfolioboss.com/wp-content/uploads/2020/08/Checking-Digital-Signatures-clip.mp4](_wp-content_uploads_2020_08_Checking-Digital-Signatures-clip.mp4.md)

*   *   Make sure to do this on a fresh install, not on a quarantined or cleaned file.
    *   Open Windows File Explorer.
    *   Type `%LocalAppData%\PortfolioBoss\Application\` in the address bar (or you can copy-paste that address), followed by Enter.
    *   Right-click on PortfolioBoss.exe (the extension .exe may or may not be visible, depending on your Windows settings).
    *   Select _Properties_ from the dropdown menu.
    *   Click on the tab _Digital Signatures_ (if it’s not there, there’s no signature anymore and the program has already been altered; reinstall Portfolio Boss in this case).
    *   Select the signature and click on _Details._

* * **22.  _My Drive C is full. How can I change PB database folder to use another drive_****_?_**

Please refer to the help page for [“Database Tab”](_documentation_database-tab-guide_.md#changedatabase), we explain exactly how to do this.

**[Back to Top](_documentation_frequently_asked_questions_.md#backtotop)**

You have already reported this .

#### _documentation_goldilocks-filter-guide.md

> Source: https://portfolioboss.com/documentation/goldilocks-filter-guide
> Scraped: 3/1/2026, 2:08:47 AM

[!](_wp-content_uploads_2019_11_Goldilocks-Filter.png.md)

This filter will exit any positions that go out of the “Goldilocks Zone”.

Goldilocks Zone is the price range that's neither too high nor too low. So if you're trading Long Positions, this filter makes sure your Positions do not drop below the Goldilocks Zone. Alternatively, if you're trading Short Positions, it makes sure your Positions do not go above the Zone.

This filter is best used as a [Sell Filter](_documentation_sell-filters-panel-guide_.md) (stop-loss).

* * *

#### Note:

There's an advanced version of this filter, where you can access more parameters. If you wish to upgrade your license, please contact our Customer Support team at [support@portfolioboss.com.](mailto:support@portfolioboss.com)

You have already reported this .

#### _documentation_help-page-overview-guide.md

> Source: https://portfolioboss.com/documentation/help-page-overview-guide
> Scraped: 3/1/2026, 2:07:46 AM

*   »
*   »
* [Help Page Overview](_documentation_help-page-overview-guide.md)

* * *

Discount Applied Successfully!

Your savings have been added to the cart.

Close

#### Block Member?

Please confirm you want to block this member.

You will no longer be able to:

*   See blocked member's posts
*   Mention this member in posts
*   Invite this member to groups
*   Message this member
*   Add this member as a connection

**Please note:** This action will also remove this member from your connections and send a report to the site admin. Please allow a few minutes for this process to complete.

#### Report

You have already reported this .

#### _documentation_hilo-over-time-filter.md

> Source: https://portfolioboss.com/documentation/hilo-over-time-filter
> Scraped: 3/1/2026, 2:08:47 AM

* * *

!

!

This filter sees whether the _last closing price_ is the new high (or the new low) of the specified period, before the instrument can be traded. It can also identify if it's **not** a new high (or **not** a new low) of the period. Keep in mind this is not about all-time high or all-time low, but just what's seen within the period specified. And it simply looks at the closing prices, not the candles' wicks.

!

Common sense suggests that it's bullish if the instrument makes a new high for the specified period, and bearish if it makes a new low. But it's a _very loose_ criteria, so you better use this filter with others that identify trend and momentum.

Note, there's no indicator line plotted for this filter (on the [Instrument Tab](_documentation_instrument-tab_.md)), as it's all about the pure price action.

* * **1.  The first parameter** defines the mode (method) to use this filter.

!

There are four modes:

*   **New High:** The instrument will be traded only if its last closing price is _the highest_ of the period. So all closing prices prior to this last-date (up to the start-date of the period) _must be lower_, no matter what happened be they mountains and valleys; unlike the [ROC](_documentation_rate-of-change-roc-position-filter_.md) which simply sees the change between the start date and the end date. This mode is generally good as a Buy Filter.

*   **New Low:** The instrument will be traded only if its last closing price is _the lowest_ of the period; anything prior to that (up to the start of the period) must be higher. This is usually good as a Sell Filter.

*   **No New High:** This one simply sees whether the last closing price **is not** the highest of the period. It doesn't matter how low, sometimes it can even be the lowest of the period; hence it's a very loose criteria that must be supported with other filters. It may look counterintuitive, but our [Divine Engine](_documentation_the-divine-engine-and-the-boss_.md) tests showed this mode is actually good as a Buy Filter.

*   **No New Low:** This mode identifies if the last closing price is simply **not** the lowest of the period. It doesn't matter how high, as long as it's not the lowest; sometimes it can be the highest of the period.

!

* * **2.  The second parameter** defines the _period_ (timeframe), _in which_ the highest & lowest closing prices are identified (as shown by the pink lines in the screenshot above).

!

So it's not like this filter identifies _all-time_ high and all-time low; there's already [another filter](_documentation_all-time-high-low-filter_.md) for that.

Our tests indicate that:

*   The mode **New High** (as a Buy Filter) generally performs well with a period of 10 to 30 days.
*   The mode **New Low** (as a Sell Filter) generally performs well with a period of 220 to 260 days.
*   The mode **No New High** (as a Buy Filter) generally performs well with a period of 250 to 265 days.
*   The mode **No** **New Low** (as a Sell Filter) generally performs well with a period of 2 to 15 days.

!

!

But as usual, these are just the general values when this filter is used simultaneously as a Buy and a Sell Filter. You _may_ need different periods depending on your strategy's portfolio, rules, and other filters used.

[**Back to Top**](_documentation_hilo-over-time-filter_.md#backtotop)

Discount Applied Successfully!

Your savings have been added to the cart.

Close

You have already reported this .

Search

#### _documentation_history-tab.md

> Source: https://portfolioboss.com/documentation/history-tab
> Scraped: 3/1/2026, 2:08:12 AM

!

This tab shows the day-by-day trading history since the beginning of the backtest period. Here you can see the Positions held _every single day_ (for the past several decades!), as well as the average gain between Positions each day.

This tab is located at the “Backtest Strategy” page's report area:

!

* * **1.**  **The “Date” column** shows the date of each day. It only shows the 5 trading-days of the week, excluding holidays and weekends.

!

* * **2.**  **The “Symbol” column** shows all Positions held during each date. Remember, the maximum number of Positions held at any given day is set on the [“Total Positions to Hold”](_documentation_system-settings-panel-guide_.md#totalpositions) rule. 

!

The Positions on each date are sorted left to right from the highest ranked instrument (due to the [Ranking Rules](_documentation_ranking-panel-guide_.md)). You can click on a symbol to see its price chart on the [Instrument Tab](_documentation_instrument-tab_.md). The chart view is automatically centered to the date that you clicked the symbol from (from the “Date” column).

 !

If you hover your mouse over one Position (symbol), a tooltip appears showing you various information: 

!

The information are (from top to bottom): the company's (or fund's) full name, the portfolios that contain this symbol, its asset-class (stock, ETF, ADR, etc), the market (exchange) it's traded at, the period it's been traded, its historical-price data provider, the gain/loss for that particular date (since the Position was entered), its weight (the percentage of account size occupied by this Position), it's Position type (whether a long or short Position), and the number of days it's been held.

If it's a Cash Equivalent symbol (e.g. SHY), the bottom of the tooltip lists the old Position(s) it replaced:

!

And if it's a Cash Position (and the strategy uses Cash _instead of_ Cash Equivalent) you'll see whether it's a replacement for sold Positions, or a placeholder if none of the instruments passed the Buy (enter) Filters hence no instruments can be ranked and bought:

!

If the strategy uses [Limit Orders](_documentation_system-settings-panel-guide_.md#BuyOrderType), you can see whether the Cash Positions are placeholder for some Limit Buy Orders that weren't filled (thus they're stored as Cash); or a temporary placeholder for those Positions considered sold with the Limit Sell Orders (PB can't know whether such limit orders are filled _until_ the market closes, so cash placeholder is used for that day).

!

Cash or Cash Equivalent Positions may be grouped together with the parentheses indicating the number of sold Positions they replaced:

!

Now, some symbols are enclosed within parentheses. This indicates they're not part of that date's positions, but the previous day's positions that are considered sold (exited) at the day's open.

!

Some symbols also have a number within the square brackets:

!

This indicates currently delisted instruments, with the number showing how many times the delisting happened (an instrument can sink in and out of the OTC market multiple times; ditto with going private and public).

* * **3.**  **The “Gain” column** shows the total gain (or loss) from all positions, for that day, in _comparison_ to the _previous day_. Each position's gain (or loss) is affected by its weight, that is, how much it comprised the entire portfolio.

!

This “Gain” column is like a daily performance for that strategy. This is calculated by finding the difference between yesterday and today's account balance, and then dividing the result by yesterday's balance. But keep in mind, the gains shown here may not accurately mirror your trading account. For one, there's the brokerage commissions and slippage that fall outside PB's [assumptions](_documentation_system-settings-panel-guide_.md#slippagesmioptions). And then there's the possibility that entry and exit prices on your actual trades (especially if using Market Orders) differ slightly from PB's clear-cut opening price.

* * *

### Note:

You can click the header of “Date” or “Gain” column to sort the list, from the latest date (or highest gain) to the oldest date (or lowest gain), and vice versa.

[**Back to Top**](_documentation_history-tab_.md#backtotop)

You have already reported this .

#### _documentation_impulse-score-rule.md

> Source: https://portfolioboss.com/documentation/impulse-score-rule
> Scraped: 3/1/2026, 2:07:43 AM

[!](_wp-content_uploads_2019_10_Impulse-Score-Rule-000.png.md)

This rule ranks your instruments based on their _percentage gain_ during the past certain period.

For example, if you're looking for instruments that have the _highest_ percentage gain in the past 5 days, then set this rule as the “highest” impulse score in the past “5 days”.

* * **1.**  The first parameter, “Lowest/Highest”, defines whether you want to look for instruments that have the lowest or highest impulse score.

[!](_wp-content_uploads_2019_10_Impulse-Score-Rule-1st-Parameter.png.md)

* * **2.**  The second parameter, “x days (or months)”, defines the period to calculate the impulse score. That is, the percentage gain is calculated from the beginning of this period until today.

[!](_wp-content_uploads_2019_10_Impulse-Score-Rule-2nd-Parameter.png.md)

* * *

#### Notes:

*   It is best to employ this rule in different flavors, for example the first rule looks at the _lowest_ impulse score during the past 5 days, while the second rule looks for the _highest_ impulse score during the past 6 months. 

[!](_wp-content_uploads_2019_10_Double-Impulse-Rules.png.md)

That way, you're essentially looking for instruments that are experiencing a dip during a generally upward trend, so hopefully once you enter that Position (at such a discount) it will rebound to your profit.

*   Regarding the “Offset” and “Weight” parameters, please refer to the guide about [Ranking Panel](_documentation_ranking-panel-guide_.md#offsetweight).

You have already reported this .

#### _documentation_index-atr-spread-filter.md

> Source: https://portfolioboss.com/documentation/index-atr-spread-filter
> Scraped: 3/1/2026, 2:08:48 AM

[!](_wp-content_uploads_2019_10_Index-ATR-Spread-Filter-Buy.png.md)

[!](_wp-content_uploads_2019_10_Index-ATR-Spread-Filter-Sell.png.md)

This filter looks at the ATR Spread between an instrument and an index, and if such ATR Spread falls within a certain threshold, the instrument will be considered as a buy/sell.

In practical terms, this filter looks at the current _price gap movement_ between the instrument and index, so you can buy that instrument at a big discount knowing that the instrument will fall in line again with the index (provided the Portfolio is highly correlated with the index).

Higher ATR Spread (either positive or negative) means the price gap movement between them is big (if the Spread is high enough, the instrument and Index might be in different trends). Lower ATR Spread (nearing 0) means the price gap movement is low.

So, this is how this filter works:
(please read [this page](_documentation_n-atr-above-below-sma-filter_.md) to understand ATR and SMA.)

[!](_wp-content_uploads_2019_10_PB-Index-ATR-Spread.png.md)

*   An x days SMA and y days ATR (Average True Range) are calculated for the _instrument_.
*   Then, the filter calculates how far up or down the _last closing price_ deviates from the SMA, that is, how many ATRs in that distance; if the last closing price is below the SMA, the distance would be negative, and vice versa.
*   The same components are also calculated for the _Index_, that is, the Index's ATR, SMA, and the ATR-distance between the last closing price and the SMA.
*   Finally, it subtracts the instrument's ATR-distance from the Index's ATR-distance, which results in the final ATR Spread.

This filter is best used with [another filter](_documentation_lowest-close-index-filter_.md) that confirms whether the index is uptrending or downtrending, so you don't blindly follow that index. [Another filter](_documentation_correlation-filter_.md) may also be used to find instruments that are highly correlated with the index.

* * **1.**  The first parameter defines the ATR period for both the instrument and index.

[!](_wp-content_uploads_2019_10_Index-ATR-Spread-Filter-1st-Param.png.md)

* * **2.**  The second parameter defines the index to use. You can also input other types of instrument here, but usually ETF would do the trick.

[!](_wp-content_uploads_2019_10_Index-ATR-Spread-Filter-2nd-Param.png.md)

Note, you can't enter a delisted instrument here (those with a number suffix inside square brackets). Otherwise a warning shows up, and you can't backtest the strategy:

!

* * **3.**  The third parameter defines the SMA period for both the instrument and index.

[!](_wp-content_uploads_2019_10_Index-ATR-Spread-Filter-3rd-Param.png.md)

* * **4.**  The fourth parameter defines whether the resulting ATR Spread must be “Less than”, “Greater than”, “Between”, or “Not between” the threshold ATR Spread value(s).  

[!](_wp-content_uploads_2019_10_Index-ATR-Spread-Filter-4th-Param.png.md)

Keep in mind, even though a big ATR Spread may mean a big discount for entering a Position, it may also mean the index _or_ the instrument is _reversing_ trend. So preferably instead of using “Greater than”, you use the “Between” (as shown above).

That is, you're still looking for a discount, but not big enough that the instrument (or index) is potentially reversing trend, thus going the opposite direction from each other.

For a Sell Filter though, it's good to use the value “Greater than”, since the price gap movement has gone beyond the threshold (index and instrument are potentially not related anymore), so exit the position.

[!](_wp-content_uploads_2019_10_Index-ATR-Spread-Filter-4th-Param-Sell.png.md)

* * **5.**  The fifth parameter defines the threshold ATR Spread. If you choose “Between” or “Not between” in the previous parameter, you can define the min and max threshold values here.

[!](_wp-content_uploads_2019_10_Index-ATR-Spread-Filter-5th-and-6th-Param.png.md)

* * *

#### Note:

Once this filter is applied, you can see _four_ indicators displayed _below_ the Price Chart (at the [Instrument Tab](_documentation_instrument-tab_.md)):

[!](_wp-content_uploads_2019_10_Index-ATR-Spread-Filter-indicators.png.md)

*   *   *   one indicator shows the x days ATR;
        *   one indicator shows the ATR-Distance of the instrument from its SMA;
        *   one indicator shows the ATR-Distance of the index from its SMA;
        *   and one indicator shows the ATR Spread between the instrument and index.

As well, there's an SMA indicator that you specified through this filter, being overlaid on the Price Chart.

[**Back to Top**](_documentation_index-atr-spread-filter_.md#backtotop)

You have already reported this .

#### _documentation_index-atr-spread-rule.md

> Source: https://portfolioboss.com/documentation/index-atr-spread-rule
> Scraped: 3/1/2026, 2:09:19 AM

[!](_wp-content_uploads_2019_10_Index-ATR-Spread-Rule-000.png.md)

This rule is similar to the [“Index ATR Spread Filter”](_documentation_index-atr-spread-filter_.md), but instead of excluding instruments that don't meet the threshold _ATR Spread_, it ranks the instruments top to bottom based on _how large_ their ATR Spread is.

[!](_wp-content_uploads_2019_10_PB-Index-ATR-Spread.png.md)

So, this rule is good to look for instruments that may give a bigger discount, or, to look for instruments that are closely aligned with an index. If you're trading [Short Positions](_documentation_a-strategy-for-short-selling_.md), this filter is good to find those instruments that are reversing toward the downtrend.

* * **1.**  The first parameter defines how to sort the instruments from top to bottom rank. 

[!](_wp-content_uploads_2019_10_Index-ATR-Spread-Rule-1st-Param.png.md)

“Highest” means the instrument that has the _biggest_ ATR Spread will have the top rank, thus you're looking for instruments that give the biggest discount, or instruments that are deviating more from the index (e.g. the market condition is bad, so you want instruments that deviate from the market).

If you're trading Short Positions, “Highest” can be used to find instruments that are reversing toward the downtrend, provided the Index is in uptrend (use a Short Filter that defines an uptrending Index).

[!](_wp-content_uploads_2019_10_Index-ATR-Rule-Short.png.md)

“Lowest” will give the top rank to the instrument that has the _smallest_ ATR Spread, thus you're essentially looking for instruments that are closely aligned with the index.

[!](_wp-content_uploads_2019_10_Index-ATR-Spread-Rule-1st-Param-B.png.md)

* * **2.**  The second parameter defines the ATR period for _both_ the instrument and the index.

[!](_wp-content_uploads_2019_10_Index-ATR-Spread-Rule-2nd-Param.png.md)

* * **3.**  The third parameter defines what index to use, preferably this index is strongly correlated to your Portfolio; though you can input any instruments here (sometimes ETFs are good too).

[!](_wp-content_uploads_2019_10_Index-ATR-Spread-Rule-3rd-Param.png.md)

Keep in mind, you shouldn't enter a delisted instrument here (that with the square brackets suffix containing a number), otherwise the strategy becomes invalid and you can't backtest it.

!

There's that warning “Instrument cannot be historic”, which actually means it shouldn't be a prehistoric relic a.k.a. delisted.

* * **4.**  The fourth parameter defines the period to calculate the SMA (for both the instrument and index).

[!](_wp-content_uploads_2019_10_Index-ATR-Spread-Rule-4th-Param.png.md)

* * *

#### Note

Regarding the “Offset” and “Weight” parameters, please refer to the guide about [Ranking Panel](_documentation_ranking-panel-guide_.md#offsetweight).

[**Back to Top**](_documentation_index-atr-spread-rule_.md#backtotop)

You have already reported this .

#### _documentation_instrument-chart-panel-guide.md

> Source: https://portfolioboss.com/documentation/instrument-chart-panel-guide
> Scraped: 3/1/2026, 2:08:08 AM

!

Located at the right area of the Portfolio Management page, this panel shows the Price and Volume Charts of an instrument. First you need to select an instrument (from the [Portfolio Instruments Panel](_documentation_portfolio-instruments-panel-guide_.md) at the left) for this chart to show its contents.

* * **1.**  **The top chart is the Price Chart:** it shows the price history for that instrument. At the top of this chart you can see the instrument's symbol, full name, the exchange it's trading at, and the source for the price data. The horizontal axis describes time, while the vertical axis is the dollar price (or value) for that instrument. 

!

You can click and drag to _pan_ around this chart. You can also zoom-in and out with the mouse scroll-wheel. Beware, if you zoom-in too much you may not be able to zoom-out, unless you keep scrolling-out (scroll until the chart is actually zoomed-out). Or you can double-click the chart to reset the zoom level.

[https://portfolioboss.com/wp-content/uploads/2021/08/gfyu4e6w3ghq.mp4](_wp-content_uploads_2021_08_gfyu4e6w3ghq.mp4.md)

Right-clicking the chart shows a tooltip with accurate OHLCV and date information.

* * **2.**  **To change how the price data are displayed,** go to the “Chart Type” dropdown on top. 

!

Here you can choose between:

* [Candlestick](_documentation_instrument-tab_.md#candlestick) (shows Open, High, Low, and Close prices, as well as bearish or bullish colors),
* [OHLC](_documentation_instrument-tab_.md#OHLC), or _Open High Low Close_ bar-chart (similar to Candlestick but more intuitive for seeing where the opening & closing prices are),
* [Line](_documentation_instrument-tab_.md#linechart) (a line connecting the days' _closing_ prices),
* [Mountain](_documentation_instrument-tab_.md#mountainchart) (similar to Line but shaded), and
* [Column](_documentation_instrument-tab_.md#columnchart) (individual bars showing the closing prices).

[!](_wp-content_uploads_2019_10_Chart-Types_00000.png.md)

* * **3.**  **At the top-right corner,** you can choose to view the price in either the [Adjusted value](_documentation_instrument-tab_.md#adjustedprice), or the [Real value](_documentation_instrument-tab_.md#realprice). “Adjusted” means the instrument's price is adjusted for stock-splits, new offering, dividend payments, etc. It is the most accurate representation of the price. 

!

“Real” shows the real, historic price that instrument was traded. But without context, this raw price is misleading. Stock-splits, for example, may halve the price per share, but shareholders get two for every share they own. Ditto dividend effects (the drop in price during ex-dividend, and the fact you got the cash) are all affecting the final “value” of a stock, that can't be shown with the raw price.

* * **4.**  **The bottom chart is the Volume Chart.** It shows the amount of shares traded day-by-day.

!

* * **5.**  **At the very bottom of this panel,** there's a scroll-bar that you can _drag_ to pan around the chart. Shrinking or expanding this scroll-bar (by dragging its ends) is the same as zooming-in or out.

[https://portfolioboss.com/wp-content/uploads/2021/08/67w46hqw345u56.mp4](_wp-content_uploads_2021_08_67w46hqw345u56.mp4.md)

You can see a general overview of the price history overlaid on this scroll-bar (conforming to the price chart above).

* * *

#### Note:

This panel will not show any contents if the instrument's price data is being downloaded.

[**Back to Top**](_documentation_instrument-chart-panel-guide_.md#backtotop)

You have already reported this .

#### _documentation_instrument-public-age-filter.md

> Source: https://portfolioboss.com/documentation/instrument-public-age-filter
> Scraped: 3/1/2026, 2:08:47 AM

[!](_wp-content_uploads_2019_10_Instrument-Public-Age-Fillter-Ori.png.md)

This filter only exists as a [Buy Filter](_documentation_buy-filters-panel-guide_.md). It allows you to select instruments which have been publicly traded within a certain period.

For example, stocks fresh out of the IPO tend to have a stronger rally and greater profit potential, not just because the hype surrounding the launch but also the growth spurt of a new company (but this isn't always the case). Older stocks on the other hand, have a consistent and more predictable performance for longer term trading.

* * **1.**  The first parameter defines whether the instrument's age must be “More Than” or “Less Than” the specified period.

[!](_wp-content_uploads_2019_10_Instrument-Public-Age-Fillter-1st-Param.png.md)

* * **2.**  The second parameter defines the threshold period; you can enter days or months here by typing and selecting the value.

[!](_wp-content_uploads_2019_10_Instrument-Public-Age-Fillter-2nd-Param.png.md)

* * **Note:**

This filter can't be applied if you have but one instrument in the strategy's Portfolio.

[!](_wp-content_uploads_2020_04_Portfolio-1-Instrument-1.png.md)

The filter is grayed out and you can't select to add it:

[!](_wp-content_uploads_2020_04_Instrument-Public-Age-Restricted.png.md)

You have already reported this .

#### _documentation_instrument-tab.md

> Source: https://portfolioboss.com/documentation/instrument-tab
> Scraped: 3/1/2026, 2:08:14 AM

!

The Instrument Tab shows the _historical price chart_ of an instrument, as well as the technical indicators (from [rules and filters](_documentation_about-filters-rules_.md) of the strategy) used to analyze the instrument. This tab also shows the trading actions (Buy, Sell, Short, Cover) experienced by the instrument, and its volume data.

All this information is shown as graph or chart.
This tab is located at the Reports Area of the “Backtest Strategy” page:

!

* * **1.**  **Initially, this tab shows nothing,** so you must select an instrument from any panels (or tabs) in this “Backtest Strategy” page. Any symbols highlighted blue are clickable, bringing you to this Instrument Tab and its contents. 

!

For example you can use the [Stats Tab](_documentation_stats-tab_.md), as it lists the instruments in a sortable manner.

* * **2.**  **At the top of this tab,** you can see the instrument's general information: its ticker, company name, asset class, the exchange it's trading at, and the source used for obtaining the price data.

!

* * **3.**  **There are _three charts_ in this tab,** actually: the top chart being the most important of them all. It shows the _historical_ _price data_ of an instrument along with the technical indicators (lines) used by the strategy. The horizontal axis represents time, while the vertical axis represents the instrument's price (in dollar value).

!

You can also see the various trading actions the instrument experienced during the whole backtest period. Look at the Buy and Sell arrows above, they point to the candle (i.e. the day) the instrument was bought and sold, respectively. Trading signals were given one day before each action (execution).

You can click-drag on the chart to pan it left or right; scroll the mouse-wheel to zoom the chart; double click the chart to reset the zoom level; and right-click to show a tooltip on the cursor (contains the Open, High, Low, and Close prices, as well as the Volume and Date information).

!

If you hover your mouse over a Buy action, a tooltip shows you the opening price that PB assumes you entered the Position at. If the strategy uses Buy [Limit Order](_documentation_system-settings-panel-guide_.md#BuyOrderType), the _Lowest Price_ of the day as well as the _Buy_ _Limit Price_ are shown.

!

If you hover your mouse over a Sell action, the tooltip shows you the opening price (that PB assumes the position's exit was), the position's gain, and holding period. If the Position was exited due to a Sell Limit Order (a Sell Filter that uses Limit Order), the highest-price of the day, as well as the Sell Limit Price, are shown.

!

If you use Limit Orders, the strategy looks at whichever is the _better_ price between the opening price and the limit price, to be considered as the entry & exit price for each Position. If you're buying, the lower the price the better, and if you're selling the higher the price the better.

Now, you can expand or collapse the “Indicators” dropdown menu with its arrow button. There you may choose which technical indicators are shown on this chart. Simply tick/untick the checkbox on each Indicator.

!

You can see which rule (filter) the lines belong to, for example: “Buy rule #1” means it's the topmost Buy Filter as shown on the [Buy Filters Panel](_documentation_buy-filters-panel-guide_.md), “Buy rule #2” means it's the Buy Filter below that, and so on. Ditto the Sell Filters.

!

* * **4.**  **Now, the middle chart**: this chart appears _just below_ the price chart; it may or may not show up depending on the rules/filters you use. Some technical indicators that don't correspond _directly_ to the instrument's price data, such as the RSI or volatility measures (which are _derivative_ of price data) may be shown here. 

!

As usual, you can use the “Indicators” dropdown to show or hide certain indicator. It also shows you which filter/rule the indicator belongs to. You can right click the chart so a tooltip appears, which shows the indicator's value right where you put the cursor. Now, since this chart uses a single vertical scale for multiple indicators, it could be that some indicator lines are shown flat (as shown in the screenshot above, green line). Simply uncheck the other indicator(s), so the scale is used solely by the indicator you want, and the graph now shows clear ups and downs.

!

Note, if this chart does not show up despite using a certain filter, hover your mouse at the _bottom edge_ of the _Price Chart_ until your cursor changes into a vertical arrow, then drag that edge upward to expand this chart.

* * **5.**  **The bottom chart** gives you the volume data for that instrument (amount of shares traded each day). 

!

Volume can be useful, for example, as a _confirmation_ of a trend change: Institutional investors, who often trade _gigantic_ amount of shares, tend to know better when a trend is changing (though it's not often & always the case).

* * **6.**  **The bottom scroll-bar** also allows you to pan and zoom the charts. Drag it left or right to pan the charts left or right. Shrink or stretch the scroll-bar (by dragging its head or tail) to zoom the charts in or out.

 !

This is useful if you want to take a closer look at a certain period: see the general overview of the price history (as overlaid in this scroll-bar), then adjust the scroll-bar to enclose a certain period.

* * **7.**  **At the top-right of this tab,** there's a parameter that says “Adjusted” or “Real”. This concerns the way the instrument's price is displayed. 

!

“Adjusted” is the most realistic way of seeing the prices. It takes into account the _dividends_ paid to shareholders, thus reducing the share's value, as the company is “wasting” that profit into dividend payments instead of re-investing into the company itself. Adjusted price also accounts _stock-splits_ (when the price of each share is too high, thus the company decided to split it into cheaper shares) and _new stock offering_ (when the company needs to raise more capital), both of which increase the amount of shares circulated, thus reducing the value. Note that the adjusted price applies as well to candles prior to the introduction of dividend payments, stock-split, and new offerings (thus for example you don't see a sudden decrease in price at the day the stock was split).

Now, “Real” price is the actual historical price it was trading at; but this is a less accurate presentation of the price. So, in case you're wondering why Adobe's stock traded at $1 in the late 1980s, you should know that it's the adjusted price (the “real” price was actually around $30).

**Note:**

Portfolio Boss uses _adjusted price_ in its calculation of most rules & filters. So if you see _trading actions_ here (Buy & Sell arrows) that don't agree with the instrument's price, you may be looking at its “real price”, hence the perceived “error”. In fact, none of the _indicator lines_ are displayed in this entire tab if you set this to “Real” prices.

* * **8.**  **At the top-left of this tab,** there's the “Chart Type” parameter. This is used for changing how the price data is displayed (candlestick, OHLC bar-chart, line, etc.). “Candlestick” shows each day's price in the candlestick format, as shown in the picture below. 

!

The _High_ and _Low_ as shown above (the tips of the candle's wick) indicate the highest price and lowest price of the day. If there's no wick, the highest (or lowest) price is exactly the same as the opening (or closing) price.

Now, the “OHLC” shows the price in OHLC format (Open High Low Close). It's similar to candlestick but more intuitive, since you can quickly tell the opening vs closing price by which side the extension is located (left or right of the main body).

!

“Line” connects the _closing prices_ in a continuous line. There's no visual indicator of the High, Low, and Open. This is useful if you… well, want to see the closing prices _connected_ together (closing prices are often the most impactful and widely cited price). It gives better clarity on where the troughs and peaks are (candlestick often gives the wrong impression of a lower low, while in reality it's a higher low, for example).

!

“Mountain” shows a _shaded_ price graph, similar to line but filled with color. This is good for seeing the general overview of the instrument's history, as you quickly get a sense of gains & growth (solid color), and losses (empty space). Only closing prices are shown here.

!

“Column” shows _each day's_ closing price in a _single bar_ (only the closing price). It's useful in tandem with the right-click tooltip, so you get accurate reading of the prices (the pointer and tooltip _snap_ to each bar, instead of floating around freely).

!

Note that Portfolio Boss can only show _daily_ price data, which means each bar represents a single day (on all chart types). In the future, we will implement _intraday_ price data.

* * *

### Notes:

*   The trading actions shown here (Buy, Sell, Short, and Cover arrows) are the day the orders are executed. For example, a Buy action is shown at January 11th candle; that means the instrument fulfilled the Buy Filters' criteria at January 10th (after the market closed), and that the order to buy was executed on January 11th.

*   Keep in mind that a Buy action (or Short action) not only looks at the [Buy Filters](_documentation_buy-filters-panel-guide_.md) (or Cover Filters), but the [Ranking Rules](_documentation_ranking-panel-guide_.md) as well. So if an instrument you see here seems to have fulfilled the Buy Filters but gets no Buy action, it could be that the instrument doesn't rank highly to be entered as a Position.

*   Ditto if you see a Sell action (or Cover) despite the Position not hitting any of the Sell Filters (or Cover), it could be that the instrument company (or fund) was delisted from the exchanges (caused by merger & acquisition, bankruptcy, or inadequate market-cap).

[**Back to Top**](_documentation_instrument-tab_.md#backtotop)

You have already reported this .

#### _documentation_instruments-panel-guide.md

> Source: https://portfolioboss.com/documentation/instruments-panel-guide
> Scraped: 3/1/2026, 2:08:13 AM

!

This panel is located at the [Rules Area](_wp-content_uploads_2021_05_gdg56ye5dg_00000_00000.png.md) of the “Backtest Strategy” page.

Here you can add the various _portfolios_ for the strategy. All instruments within these portfolios will be considered to be traded. If any instruments pass the [Buy Filters](_documentation_buy-filters-panel-guide_.md) and rank highly based on the [Ranking Rules](_documentation_ranking-panel-guide_.md), they'll be entered as positions.

By default, this panel is collapsed. There's an arrow button at the top-right corner, to expand and collapse the panel to abbreviate its contents, and save up some space.

[https://portfolioboss.com/wp-content/uploads/2021/10/des56esdstn.mp4](_wp-content_uploads_2021_10_des56esdstn.mp4.md)

Note, if you want to trade certain instruments within a custom portfolio, please refer to [**the guide on creating portfolios**](_documentation_portfolios-panel-guide_.md#createnewportfolio).

* * **1.**  **To add the portfolios,** click the “Add Portfolio” button (at the top-right corner). 

[https://portfolioboss.com/wp-content/uploads/2021/10/tf67dj6sedrm.mp4](_wp-content_uploads_2021_10_tf67dj6sedrm.mp4.md)

The “Add Portfolios” dialog shows up, that lets you search and select the portfolios. Once certain portfolios are ticked (checked), you can enter another search term to find and tick other portfolios. Then press OK to add them all to the strategy. Note, any portfolios already added to the strategy will not show up on this dialogue.

Now, sometimes you only want to trade a single ETF with your strategy (along with the [inverse of that ETF](https://www.investopedia.com/terms/i/inverse-etf.asp) as the Cash Equivalent):

!

In that case, there are some symbols that you can immediately type into that “Add Portfolios” dialog:

*   *   BOIL, DBC, ERX, FAS, GLD, PGOVX, PTSHX, QLD, QQQ, SDS, SLV, SOXL, SPY, SSO, TBT, TECL, TMF, TQQQ, UDOW, UUP.

!

That way, you don't have to create the container Portfolio first (though you must for symbols not listed above).

* * **2.  To view the instruments** contained in each portfolio, click the portfolio name (blue colored). A pop-up appears.

[https://portfolioboss.com/wp-content/uploads/2021/10/dres5yres56nes56.mp4](_wp-content_uploads_2021_10_dres5yres56nes56.mp4.md)

The description of each column (on that pop-up) is similar to the [Portfolio Instruments Panel](_documentation_portfolio-instruments-panel-guide_.md#columnsdescrstart). But here you can only view them; you can't manipulate the instruments in any way (use the aforementioned panel for that).

* * **3.**  **To remove a portfolio from the strategy,** click the trash-bin icon next to the portfolio. 

[https://portfolioboss.com/wp-content/uploads/2021/10/tgf674e6hesw5hnj9.mp4](_wp-content_uploads_2021_10_tgf674e6hesw5hnj9.mp4.md)

Or, you can click the top-most trash-bin icon to delete all portfolios at once.

* * **4.**  **The “Listed” column** shows the amount of actively traded instruments in each portfolio. 

!

Whereas the **“Delisted”** **column** shows the number of instruments that are no longer traded in the exchanges.

* * **5.**  **The “Total” amount** (at the bottom of this panel)**,** shows the _total_ number of “Listed” instruments from _all_ portfolios. “Delisted” instruments have their total too.

!

If _the same_ instrument is contained within _multiple_ Portfolios, PB only counts that instrument as one, disregarding the duplicates. PB does not enter duplicate Positions from the same symbol (unless it's a cash-equivalent).

Note, the “instruments listed” and “instruments delisted” numbers as shown when this panel is collapsed are calculated similarly as in this “Total”.

!

* * *

#### Note:

This panel may show instruments data being downloaded:

!

If that's the case, you must wait it out before you can backtest the strategy:

!

Now sometimes you still can't backtest the strategy despite PB not downloading anything. You can just click “Run anyway”, or restart PB to see if that dialog above won't bother you anymore. Other times, there could be problems with the historical data download and Dynamic Portfolio synchronization services. You may want to check the [**Portfolio Boss Status Page**](https://status.portfolioboss.com/) if such is the case:

!

If there are errors in any of the services, the PB Dev team is immediately notified and you can check back later (the status page is refreshed every minute):

!

[**Back to Top**](_documentation_instruments-panel-guide_.md#backtotop)

You have already reported this .

#### _documentation_interactive-brokers-tab-guide.md

> Source: https://portfolioboss.com/documentation/interactive-brokers-tab-guide
> Scraped: 3/1/2026, 2:09:22 AM

!

This Tab allows Portfolio Boss to connect to [Trader Workstation](https://www.interactivebrokers.com/en/trading/tws.php) (a trading platform by [Interactive Brokers](https://www.interactivebrokers.com/)) and use its price data.

The integrated price data can only be seen from the [Instrument Tab](_documentation_instrument-tab_.md). During market open, any instrument you loaded on that Tab will show its _latest candle_ continually changing, according to your IB market-data subscription (it may update in real-time or delayed). Note that index instruments, like SPX and NDX, don't have this integrated data.

!

The latest candle (as long as the instrument is still listed on the exchange) will be contained within a yellow rectangle, along with a red annotation showing the latest price (it will say “delayed” if you don't have a subscription).

Do understand, that connecting your IB market data to PB _does not_ mean the strategy uses this data for its backtest (and daily notifications). Portfolio Boss still uses the main data sources for that (like CSI and Yahoo). This is simply a visual aid to satisfy your curiosity; the latest candle does not even have volume data shown, and any indicator lines are not plotted for it. After the market closes the candle may still update reflecting after-hour price; but after a few hours, PB will download the usual end-of-day data from the main sources. Then the latest candle returns to the usual state.

In a future update, this integration between PB and IB won't just serve a visual purpose, but allows your strategy to _automatically_ execute the trading signals using Interactive Brokers. This will be especially useful once the intra-day trading feature is implemented in PB.

* * *

### Connecting Portfolio Boss to Trader Workstation

!

To connect the price data, first make sure Trader Workstation _is running_ on your computer. PB can't access the market data unless TWS is open. Then turn **on** the toggle “Enable IB Trader Workstation integration” as shown in the screenshot above.

The first time you connect PB to TWS, you'll need to follow these steps so it will accept incoming connections:

**1.**  In Trader Workstation, open the Global Configuration dialog by clicking the _gear icon_ at the top right corner of TWS interface:

!

You can also go to the File menu ⇒ Global Configuration (if you use Mosaic TWS):

!

Or the Edit menu ⇒ Global Configuration (if you use Classic TWS):

!

The Global Configuration dialog opens. From there, go to API ⇒ Settings:

!

**2.**  Make sure the checkbox “Enable ActiveX and Socket Clients” is ticked (as shown above).

**3.**  Still in that dialog, copy the “Socket port” number (as shown above) and paste it to the “Socket port” field in Portfolio Boss. You just want to make sure the socket port numbers are exactly the same between TWS and PB.

!

**4.**  Click OK on the TWS Global Configuration dialog.

!

Your operating system may throw a Windows Firewall dialog. Just choose “allow” for the public and/or private networks.

Now press the “Connect” button from Portfolio Boss. Wait a while and you'll be using price data from Trader Workstation.

!

**5.**  If there's trouble connecting to Trader Workstation, click the “Reset Connection” button. It will attempt to connect again. If the problem persists, please contact our [Customer Service](mailto:support@portfolioboss.com) or Interactive Broker's.

!

Once connected, there's a button at the top-right area of PB interface. The button is green if connection is good; gray if connection is severed; and red if connection attempt has failed.

!

This button will show up if you have the toggle “Enable IB…” turned **on**, and that you have connected to TWS at least once. Clicking the button will take you to this Interactive Brokers Tab to resolve the connection problem. Usually it's caused by TWS not currently running. But sometimes you need to check its API Settings again.

!

In rare cases you may need to install the latest TWS version.

You may need to press the “Connect” button again if connection attempt had failed.

* * *

### If TWS is Running from Another Computer:

Now, if TWS happened to be installed on a machine different from PB, there are some additional steps. A side note, if it's running on a _virtual machine_ within the same computer, it's still considered running on a _different_ machine.

**1.**  Click the “?” section of this Tab, and take note of this computer's IP (where PB is installed):

!

**2.**  Then go to the other computer, and open the same TWS Global Configuration dialog (API ⇒ Settings). Make sure the checkbox “Allow connections from localhost only” (near the bottom) is **unticked**:

!

Now add the PB computer's IP to the list of “Trusted IPs” (click the “Create” button, and write the IP on the ensuing dialog):

!

Then press “OK” on that _Global Configuration dialog_.

**3.**  Now before we go back to the PB computer, we must know the “name” of this TWS computer (host name). Do that by _typing_ “view your PC name” on the Windows's Start Menu search; then click the corresponding result:

!

**4.**  Back to Portfolio Boss, enter the name (or IP address) of the TWS computer, into the “Host” field here:

!

**5.**  Finally click “Connect” from Portfolio Boss:

!

* * *

### Changing the Active IB Account

At the bottom of this Tab there's a section called “IB Account”:

!

As of now, this section serves no purpose and doesn't interfere with the displaying of IB market data. However in a future update, it will let you choose the Interactive Brokers account that you'll use for _auto-trading_. Most IB clients have at least two accounts: one for the paper-trade (simulated trading), and one is the live (real) account. Let's say you want to _further_ test a strategy with the paper-trading account (to see its [forward performance](https://www.investopedia.com/articles/trading/10/backtesting-walkforward-important-correlation.asp#toc-forward-performance-testing-basics)) and once you're satisfied, you switch to the live account; such account switching can be done here.

To change the account, first log-in to your _preferred_ IB account in TWS. Then open Portfolio Boss (this Interactive Brokers Tab); you _may_ see a warning that the _previous_ account you used is no longer relevant. Simply select the active account from the dropdown below (orange rectangle), then press the button “Change Account”.

!

That dropdown simply lists the account that's currently active in TWS.

Note, the top-right button also shows an orange warning if there's such account mismatch:

!

But this mismatch does not interfere with the market data display.

* * *

#### Notes:

*   You _can't_ simply open two instances of TWS, each with a different account, to switch the account back-and-forth in PB. TWS will throw an API Socket warning.
*   Taking a [price snapshot](https://ibkr.info/node/2830) from TWS is not the same as having a stream of market data; therefore the price update from snapshot won't be reflected in PB.
*   Interactive Brokers _apparently_ delay the market data for instruments you currently hold in your _IB portfolio_ (if you don't have a subscription). If you want to see a real-time candle in action, load any instrument (at the Instrument Tab) that's not part of your IB portfolio.
*   If you switch from IB's paper-trading account to a live one, you _may_ need to re-configure the TWS API Settings again (the socket port number could be different).
*   As long as the toggle “Enable IB…” is **on**, Portfolio Boss will try to connect to TWS it last connected to.

[**Back to Top**](_documentation_interactive-brokers-tab-guide_.md#backtotop)

You have already reported this .

#### _documentation_kaufman-efficiency-ratio-filter.md

> Source: https://portfolioboss.com/documentation/kaufman-efficiency-ratio-filter
> Scraped: 3/1/2026, 2:08:50 AM

* * * [!](_wp-content_uploads_2019_10_Kaufman-Efficiency-Ratio-Filter-Buy.png.md)

[!](_wp-content_uploads_2019_10_Kaufman-Efficiency-Ratio-Filter-Sell.png.md)

This filter looks at an instrument's trend-strength.

An instrument stuck in a trading range (lots of rally and pullbacks, or trading at nearly the same price for an extended period) will have a lower Kaufman Efficiency Ratio, while an instrument that is in a strong uptrend or downtrend (even if the price _increment_ is not smooth, i.e. sometimes a much bigger rally than usual) will have a higher Kaufman Efficiency Ratio. So, this is a good filter to identify a strong trend.

Preferably, you use this filter with another filter that identifies a downtrend or uptrend (for example, the [“Moving Average Cross Over Filter”](_documentation_moving-average-cross-over-filter_.md)).

* * **1.**  The first parameter defines the period to calculate the Kaufman Efficiency Ratio. Adjust this according to your trading time-frame.

[!](_wp-content_uploads_2019_10_Kaufman-Efficiency-Ratio-Filter-1st-Param.png.md)

* * **2.**  The second parameter defines whether the instrument's Kaufman Efficiency Ratio must be “Greater than” or “Less than” than threshold Kaufman Efficiency Ratio (that you'll define next).

[!](_wp-content_uploads_2019_10_Kaufman-Efficiency-Ratio-Filter-2nd-Param.png.md)

* * **3.**  The third parameter defines the threshold Kaufman Efficiency Ratio. The minimum value is 0, while the maximum is 1.

[!](_wp-content_uploads_2019_10_Kaufman-Efficiency-Ratio-Filter-3rd-Param.png.md)

For example, you want to buy instruments whose Kaufman Efficiency Ratio is greater than 0.8 (a generally strong trend), then input 0.8 here and set the previous parameter to “Greater than”.

* * *

#### Note:

Once you applied this filter, you can see the “Efficiency Ratio” indicator displayed below the Price Chart (at the [Instrument Tab](_documentation_instrument-tab_.md)). 

[!](_wp-content_uploads_2019_10_Kaufman-Efficiency-Ratio-Indicator.png.md)

This indicator's appearance depends on the filter's period setting, and if you applied more than one Kaufman Efficiency Ratio Filters, each with a different setting, there will be two indicators displayed on this chart.

[**Back to Top**](_documentation_kaufman-efficiency-ratio-filter_.md#backtotop)

Discount Applied Successfully!

Your savings have been added to the cart.

Close

You have already reported this .

Search

#### _documentation_lowest-close-index-filter.md

> Source: https://portfolioboss.com/documentation/lowest-close-index-filter
> Scraped: 3/1/2026, 2:08:50 AM

[!](_wp-content_uploads_2019_10_Lowest-Close-Index-Filter-Buy.png.md)

[!](_wp-content_uploads_2019_10_Lowest-Close-Index-Filter-Sell.png.md)

This filter looks at an index's _lowest_ closing-value during the past certain period, and if the Index's _latest_ closing-value is _above_ that lowest close, you're allowed to enter Positions. In essence, whether or not you will trade your Portfolio is based on the Index's closing-value, so preferably your Portfolio is related that Index.

For example, if the Index's _last_ closing value is $2147, well above $1829 which was the lowest close of the past 200 days, then the index is likely in an uptrend, thus instruments in your Portfolio will be considered to be bought since they too are likely in an uptrend.

[!](_wp-content_uploads_2019_10_Lowest-Close-of-SPX_00000.png.md)

This filter is good as a last defense mechanism before entering Positions, that is, you're looking at the market condition before you enter the Positions. But since the criteria is too loose for entering a Position, you must use this filter in tandem with other filters to constrict the criteria even more.

With that being said, it actually makes more sense to use this filter as a Sell Filter, i.e. a stop-loss for your Positions. When used as a Sell Filter, it will look whether the Index's last close is _“below”_ the lowest close (instead of “above”), and if it is, then the strategy will exit all your Positions.

This is a good way to be on the safe side, since the Index generally resembles your Portfolio. So if it goes downward you know your Portfolio will go downward too (systematic risk is on the way, so get out of the market). For even better protection, you may add this filter more than once, with each filter covering a different index.

[!](_wp-content_uploads_2019_10_Lowest-Close-Index-Two-Sell-Filters.png.md)

* * **1.**  The first parameter defines what index you'd like to watch for. You can also input other types of instrument here, like ETF.

[!](_wp-content_uploads_2019_10_Lowest-Close-Index-Filter-1st-Param.png.md)

You can click on the little “Chart” button next to it, to show the index's price history (on the [Instrument Tab](_documentation_instrument-tab_.md)). The chart is overlaid with the Lowest Close indicator.

[!](_wp-content_uploads_2019_10_Lowest-Close-Index-Filter-Indicator.png.md)

Now keep in mind, you can't enter a delisted instrument here (those indicated by a number suffix inside square brackets). Otherwise a warning appears and you can't backtest the strategy:

!

* * **2.**  The second parameter defines how many days (or months) to look back for the index's lowest closing value. 

[!](_wp-content_uploads_2019_10_Lowest-Close-Index-Filter-2nd-Param-000.png.md)

Changing this parameter will immediately change the Lowest Close indicator on the chart. 

[!](_wp-content_uploads_2019_10_Lowest-Close-Index-Filter-Period-Too-Short.png.md)

Keep in mind you don't want a very short period set in here, as you'll get stopped-out all the time with false signals (the index just swings up and down its usual daily range). A 6-month period is the norm here.

[**Back to Top**](_documentation_lowest-close-index-filter_.md#backtotop)

You have already reported this .

#### _documentation_lowest-close-position-filter.md

> Source: https://portfolioboss.com/documentation/lowest-close-position-filter
> Scraped: 3/1/2026, 2:08:49 AM

[!](_wp-content_uploads_2019_10_Lowest-Close-Position-Filter-Buy.png.md)

[!](_wp-content_uploads_2019_10_Lowest-Close-Position-Filter-Sell.png.md)

This filter looks at an instrument's _lowest_ closing-price during the past certain days (or months) that you specified, and if the instrument's _last_ closing price is _above_ that lowest close, the instrument will be considered as a buy.

For example, during the past 60 days, the lowest closing-price is $30, so if the current (last) closing price is $15, that instrument _will not_ be considered.

Please note, when considering to enter a Position, this is actually a very loose filter, so use it with caution (or use this filter in tandem with other filters so the criteria is more specific).

This filter is good for confirming whether the instrument is currently in an uptrend: as you already know, uptrending instruments have subsequently higher peaks and higher troughs, so obviously only uptrending instruments have their _last_ closing price _above_ the lowest close (provided you specified a rather long period to look for the lowest close; otherwise, if the period is short, the instrument may just go up and down based on its usual volatility).

Another example, you can use this Buy Filter to signal the _end_ of a recent pullback/correction, thus you may enter a short-term Position (use a shorter period if you're looking at such reversal).

[!](_wp-content_uploads_2019_10_Short-Period-Lowest-Close-Position.png.md)

[!](_wp-content_uploads_2019_10_Lowest-Close-Position-Pullback-End_00000.png.md)

Keep in mind that this filter also exists as a Sell Filter, but with a different criterion: it will exit Positions whose last closing-price is “below” the lowest close. 

[!](_wp-content_uploads_2019_10_Lowest-Close-Position-Filter-Below-param.png.md)

It's actually more useful as a this way, for example during a trading range a stock slips below its Support Line (which is the lowest price of the period), so you know there's possible danger ahead and you must exit that position.

This filter has only one parameter, which defines how many days past (or months) to look for the lowest closing-price.

[!](_wp-content_uploads_2019_10_Lowest-Close-Position-Only-Param.png.md)

* * *

#### Note:

A “Lowest Close” indicator will appear on the Price Chart (at the [Instrument Tab](_documentation_instrument-tab_.md)) once you add this filter to your strategy; you can look whether the latest closing-price is above, below, or _exactly_ at that indicator line (if the last close is also the lowest close). Any changes you made to this filter's parameter will immediately change that indicator's appearance.

You have already reported this .

#### _documentation_lowest-close-rule.md

> Source: https://portfolioboss.com/documentation/lowest-close-rule
> Scraped: 3/1/2026, 2:09:21 AM

[!](_wp-content_uploads_2019_10_Lowest-Close-Rule-000.png.md)

This rule looks at an instrument's _lowest_ closing-price during the specified period, and then calculates how much the instrument has gained _since_ that lowest close. It then ranks the various instruments based on such gain.

This rule is good to find instruments that experience a _strong rally_ after their lowest price, which will give you the lowest entry price, the most profit, and are likely to remain in the uptrend.

Keep in mind, that the lowest closing-price may happen at _different_ times between instruments (within that specified period). So, if an instrument's lowest close happened _most recently_, and it showed the strongest gain after such dip, that instrument will have the highest score.

[!](_wp-content_uploads_2019_10_Lowest-Close-Overview_00000.png.md)

* * **1.**  The first parameter defines how to sort the instruments from top to bottom ranks. “Highest” means the instrument that has gained the most will have the top rank. 

[!](_wp-content_uploads_2019_10_Lowest-Close-Rule-1st-Param.png.md)

While “Lowest” means the instrument that has the least gain (even loss, i.e. the greatest loss) will have the top rank, thus you're finding instruments for Short Positions.

[!](_wp-content_uploads_2019_10_Lowest-Close-Rule-1st-Param-B.png.md)

* * **2.**  The second parameter defines how many days ago (or months) to find the lowest closing price.

[!](_wp-content_uploads_2019_10_Lowest-Close-Rule-2nd-Param.png.md)

* * *

#### Note:

Regarding the “Offset” and “Weight” parameters, please refer to the guide about [Ranking Panel](_documentation_ranking-panel-guide_.md#offsetweight).

[**Back to Top**](_documentation_lowest-close-rule_.md#backtotop)

You have already reported this .

#### _documentation_macd-filter.md

> Source: https://portfolioboss.com/documentation/macd-filter
> Scraped: 3/1/2026, 2:08:49 AM

!

!

One of the most complicated indicators, MACD (Moving Average Convergence Divergence) allows you to coat-tail a trend, or, anticipate a trend change. It's the best of both worlds between moving average and momentum-oscillator indicators.

This indicator has two main components: the MACD line itself, and the Signal line. Trading signals are usually given when the MACD line crosses above or below the Signal line. Sometimes, the activity of the MACD line itself (without the Signal line) gives off trading signals: when the MACD line crosses above/below certain threshold values, or, when the MACD line and the instrument's price go in the same/opposite direction.

!

The MACD line is calculated by _subtracting_ a longer Moving Average from a shorter Moving Average (the Moving Average used is usually [EMA](https://www.investopedia.com/terms/e/ema.asp)). This MACD line is then smoothed out through another EMA to produce the Signal line. In Portfolio Boss, the MACD filter does not have the histogram component (which is just another representation of the MACD line).

The use of MACD _could_ help smooth a strategy's equity curve. Instead of major bulges and cliffs, it _may_ rise in a generally straight line (good [R² metric](_documentation_metrics-panel-guide_.md#rsquared)):

!

But despite its strength, just like any technical indicator, MACD may give false signals. So it's best to use it in tandem with other filters that identify _a larger prevailing_ trend, like the [Moving Average Cross Over](_documentation_moving-average-cross-over-filter_.md), [Rate of Change](_documentation_rate-of-change-roc-position-filter_.md), [Impulse Score Rule](_documentation_impulse-score-rule_.md), or the [Simple Moving Average Index](_documentation_simple-moving-average-sma-index-filter_.md) filter.

Let us now dissect MACD's parameters, starting from the easiest one.

* * **1.  Short MA Period:** This defines the timeframe of the _shorter EMA_, which is an ingredient of the MACD line.

!

Let's say it's set to 12 days, which means the instrument's _prices_ of the last 12 days (12 including today) are smoothed out (averaged) with the exponential method. The resulting number (the average value) is plotted in _today's_ date.

The generally accepted period here is 12 days. Some technicians suggest that if you're using the daily candles (as in PB), it's best to use a period of 8 days for the Buy Filter, and 12 days for the Sell Filter.

* * **2.  Long MA Period:** This defines the period for calculating the _longer EMA,_ which is another ingredient for the MACD line.

!

The resulting number (exponential average of the prices) is then plotted on today's date. This longer EMA is then subtracted from the shorter EMA, to produce the MACD line (value) for today's date.

!

Generally, the Long MA is given the 26 days period, though some market technicians prefer 17 days for the Buy Filter, and 25 days for the Sell Filter. Don't take these as a hard-and-fast rule, as certain filters and parameter values may prompt you to change radically the MAs periods. Sometimes the Long MA can even have a shorter period than the Short MA.

* * **3.  Signal MA Period:** This defines the EMA period for calculating the Signal line.

!

So let's say we set this to 9 days, then the MACD values for the last 9 days are smoothed with the 9-day EMA. Thus creating the Signal line (value) for _today_. This parameter is normally set to 9 days.

!

Note, all these MACD indicator lines as shown above can be seen from the [Instrument Tab](_documentation_instrument-tab_.md). Below the price chart, you'll see two indicators: MACD line (usually brown), and Signal line (usually red). The 12 and 26 days EMAs as overlaid on the price charts above are shown for the purpose of clarity, they're not part of the MACD Filter.

* * **4.  Mode:** This should be the first parameter you set when using the MACD filter. From here, you choose the MACD's mode (method) you want to use, like divergence, convergence, or Signal line crossover, etc.

!

There are four modes in PB's version of the MACD:

*   **High/Low Ranges of MACD Line**   **Crossing MACD and Signal Lines**   **MACD Convergence**   **MACD Divergence**

Changing the modes reveals/hides certain parameters in this filter. So we'll explore each mode in the following sections.

* * **5.  Mode – High/Low Ranges of MACD Line:** This mode lets you use MACD as a momentum oscillator (one that defines oversold and overbought conditions), much like [RSI](_documentation_rsi-filter_.md) predicts a trend change or measures a trend's strength.

!

As shown above in the orange rectangles, there are two parameters specific to this mode: the first defines whether the MACD line should be _above/below_ the threshold MACD value, and the second parameter defines the _threshold_ value itself (either overbought, oversold, or equilibrium). So this mode does not employ the Signal line.

!

For example as a Buy Filter, if an instrument's MACD line “Rises Above” the equilibrium threshold (usually a MACD value of 0), that instrument will be considered to be bought.  Ditto if its MACD “Falls Below” the oversold threshold, it could be bought.

!

As a Sell Filter, you can set it to “Falls Below” a MACD value of 0, or, “Rises Above” the overbought threshold.

!

But keep in mind, if the MACD line stays above the overbought threshold (or stays below the oversold threshold) for an extended period, it could be a sign that the uptrend (or downtrend) is strong. You're better off following such a trend instead of positioning for the trend reversal.

!

Note that such overbought, oversold, and equilibrium threshold values aren't definite. You have to find them yourself to fit your strategy's _portfolio_. In a Nasdaq-100 index for example, the MACD line tends to oscillate within 5 and -5 threshold, but not so much the S&P 500 index, which tends to be less volatile. This second parameter, which defines the threshold value, can be set from -100 to 100.

!

Our experiments with this mode showed that you're much better off with the equilibrium point (0) instead of the overbought & oversold areas. For a Buy Filter, set the first parameter to “Rises Above”; and “Falls Below” for the Sell Filter. The Buy Filter tends to perform well when used with small EMA periods, like 4-day, 6-day, and 26-day periods for the Short MA, Long MA, and Signal MA, respectively. Bigger EMA periods are good for the Sell Filter, like 28-day, 80-day, and 76-day. **But of course, these depend on your strategy's portfolio, and other rules/filters used (along with their parameters' values); so anything can change radically.** * **6.  Mode –** **Crossing MACD and Signal Lines:** This mode is the standard method when using MACD. So instruments are considered to be bought/sold when the MACD line crosses above/below the _Signal line_.

!

There's only one parameter specific to this mode (orange box above), which defines whether the MACD line should “rise above” or “fall below” the Signal line, for the instruments to be considered. The common wisdom says that when the MACD line crosses above the Signal line, it's a bullish signal (Buy Filter); and vice versa, when the MACD line crosses below the Signal line it's a bearish signal (Sell Filter).

!

If you see the instruments' price chart individually, short term price actions more or less conform with this conventional wisdom. But Portfolio Boss does not deal with short term testing. Given enough time, which spans decades of market turbulence, such conventional wisdoms _**may** **be**_ detrimental to a strategy's equity curve. In fact, our testing proves that going _opposite_ the MACD norm boosts your CAGR; that is, _buy_ when MACD crosses _below_ the Signal line, and _sell_ when it crosses _above_.

!

!

But as said before, _everything_ could be turned upside down again given different portfolios, rules & filters, and parameters' values. Take everything with a grain of salt, especially technical indicator values and wisdom. You _must_ discover them through your own trial and error.

* * **7.  Mode –** **MACD Divergence:** This mode “predicts” short term trend reversal by identifying divergence between the MACD line and the instrument's price.

!

So during a specified period, if price increases while the MACD line decreases, it's generally construed as a bearish divergence, thus the current uptrend may soon change. And if price decreases while the MACD line increases, it's usually taken as a bullish divergence, and the current downtrend may soon reverse.

As you see in the screenshot above, there are two parameters specific to this mode (shown in the orange rectangles). **The first parameter** defines the period for comparing the _change_ in price (also the _change_ in MACD line). Let's say this parameter is set to 3 days: if the closing price Friday (today) is $15 and the closing price Wednesday was $20, then we have a price decrease, regardless of what happens in Thursday. Now, if the MACD line today is 3, while Wednesday it was 1, then the MACD increased. Since the price decreased while MACD increased, we have a divergence, and a trading signal given.

!

Generally it's a good idea to set a short period here, like 3 or 4 days.

Unlike the usual MACD where divergence is seen from rising/falling peaks and troughs (between price and MACD), this filter simply sees the _change_ between the start of the period and today, no peaks and troughs involved. But it's still possible if you use a longer period in this first parameter. The idea is still the same, essentially.

**The second parameter** (for this mode) defines the type of divergence; either it's the price going up and MACD going down, or, price going down and MACD going up.

!

Based on conventional wisdom, “Price Down and MACD Up” is supposed to be bullish (Buy Filter), while “Price Up and MACD Down” is supposed to be bearish (Sell Filter). But this is _not always_ the case, as our tests (once again) prove that the opposite are true.

!

As well, this MACD Divergence may require different moving average periods than the usual 12, 26, and 9 days. Try and see which ones work best for you.

* * **8.  Mode –** **MACD Convergence:** The mechanism here is similar to the previous mode, but instead of diverging, the price and MACD line must converge. That is, they must both be going in the same direction before a signal is given.

!

There are two parameters specific to this mode (as shown in the orange rectangles above):

*   The first parameter defines the period for calculating the _change_ (in price and in MACD); and it's _usually_ good to set this at a short period, like 3 days.
*   The second parameter defines the convergence type: either price and MACD must both go down, or, price and MACD must both go up.

!

The type “Price Down and MACD Down” is _generally_ good as a Buy Filter, whereas “Price Up and MACD Up” is likely good for a Sell Filter.

!

As with MACD Divergence, you may want to tweak the Short MA, Long MA, and Signal MA periods away from the norm. And the Buy Filter may need different periods than the Sell Filter.

!

* * *

### Note:

You can stack multiple MACD filters, each with different settings (especially as Buy Filters). This is good so you can constraint the buying criteria with multiple different MACD modes (methods). Let's say one filter is used for predicting short-term trend change, another for confirming the strength of the greater prevailing trend, etc.

[**Back to Top**](_documentation_macd-filter_.md#backtotop)

You have already reported this .

#### _documentation_managing-your-strategies.md

> Source: https://portfolioboss.com/documentation/managing-your-strategies
> Scraped: 3/1/2026, 2:08:05 AM

!

At the top of the “Strategy Management” page, there are buttons for managing your strategies: create a new strategy, create a new group (folder), duplicate a strategy, create a backup file for the strategy, import a strategy, and delete or reset a strategy.

* * **1.**  **To create a new strategy,** click the “New” button (at the top-left corner of this page). From the dropdown menu that appears, choose “Strategy”. You can also press the keyboard shortcut Ctrl + N.

[https://portfolioboss.com/wp-content/uploads/2021/08/78r76hw.mp4](_wp-content_uploads_2021_08_78r76hw.mp4.md)

The “Add Strategy” dialog appears, where you can give a name for that strategy, choose what strategy type it will be, and place it on a certain group. Then press OK. You are immediately taken to the [Backtest Strategy Page](_documentation_backtest-strategy-page-overview_.md) where you can customize the strategy's rules and portfolios.

[https://portfolioboss.com/wp-content/uploads/2021/08/tyu5e67w4jw.mp4](_wp-content_uploads_2021_08_tyu5e67w4jw.mp4.md)

If you also want to create a _new_ _group_ (where the new strategy will be placed into), simply type the group's name _without_ selecting any of the existing groups. 

Note, if you don't give a name to the strategy, it'll be simply named “New Strategy”, or “New Strategy – Copy (2)”, and so on.

!

* * **2.**  **To create a new a group** (_without_ creating a new strategy as well), click the “New” button and choose “Group” from the dropdown. You can also use the keyboard shortcut Ctrl + G.

[https://portfolioboss.com/wp-content/uploads/2021/08/8i5rt67udre6hnsw.mp4](_wp-content_uploads_2021_08_8i5rt67udre6hnsw.mp4.md)

The “Add Group” dialog shows up, where you can give it a name. Simply press OK and the new group is created.

To rename a _group_, click exactly on the group's name, and type the new name; then press Enter. Note you can't rename the “Licensed Strategies” group.

[https://portfolioboss.com/wp-content/uploads/2021/08/89ttr85er7e4674jw67w.mp4](_wp-content_uploads_2021_08_89ttr85er7e4674jw67w.mp4.md)

You can drag and drop any strategy from one group to another. Doing so will move that strategy toward that group. Keep in mind you can't move a strategy _to (and from)_ the “Licensed Strategies” group.

[https://portfolioboss.com/wp-content/uploads/2021/08/256787wj6w.mp4](_wp-content_uploads_2021_08_256787wj6w.mp4.md)

To delete a _group_, first make sure it doesn't contain any strategies (by moving or deleting its strategies). Once it's empty, you'll see a “Delete” button below the group's name. Click that button and the group is gone.

[https://portfolioboss.com/wp-content/uploads/2021/10/6r7s56ybseh4a.mp4](_wp-content_uploads_2021_10_6r7s56ybseh4a.mp4.md)

* * **3.**  **The Backtest button** takes you to the [Backtest Strategy](_documentation_backtest-strategy-page-overview_.md) page. Make sure you have selected a strategy here, so you can customize its parameters on that page. Note, double-clicking a strategy here will also take you there.

[https://portfolioboss.com/wp-content/uploads/2021/10/y8tf6h7er6sw3.mp4](_wp-content_uploads_2021_10_y8tf6h7er6sw3.mp4.md)

* * **4.**  **To duplicate a strategy,** select it and press the “Copy” button. 

[https://portfolioboss.com/wp-content/uploads/2021/10/9u5667s56s.mp4](_wp-content_uploads_2021_10_9u5667s56s.mp4.md)

The duplicate has the suffix ” – Copy” added to the original name, and it's placed on whatever group you copied that strategy from. But if you copied a strategy from the “Licensed Strategies” group, the duplicate is placed at “My Strategies” group.

By default there's the notification dialog after you press the “Copy” button, informing you that the strategy is successfully copied. You can prevent that dialog from showing up again by ticking the checkbox “Don't show this dialog again”:

!

Note, some licenses don't have the ability to duplicate _licensed strategies_ (the “Copy” button is grayed out). Copying licensed strategies lets you modify and improve upon them without affecting the original strategy. If you wish to upgrade your license, please contact our [Customer Support](mailto:support@portfolioboss.com) team.

* * **5.**  **The Backup button creates a backup _file_** for the selected strategy. You can put this file anywhere, or send it to your fellow Portfolio Boss users. 

[https://portfolioboss.com/wp-content/uploads/2021/10/46967e6yew.mp4](_wp-content_uploads_2021_10_46967e6yew.mp4.md)

To backup a strategy: select the strategy, click the “Backup” button, and a save-dialog appears where you can specify the name and address of the backup file. It's saved as an EBTS file (where the “S” stands for Strategy).

Note, you can only backup strategies from your custom groups (not the “Licensed Strategies” group). And when you backup a **[multi-strategy](_documentation_multi-strategy_.md)**, its component strategies (basic strategies) are also included in that EBTS file.

* * **6.**  **To import a strategy,** click the “Restore” button. The File-Explorer opens, where you can select the EBTS file:

[https://portfolioboss.com/wp-content/uploads/2022/12/fysd56tsde54h.mp4](_wp-content_uploads_2022_12_fysd56tsde54h.mp4.md)

Once you opened the file, PB will ask you which _group_ to put the strategy into. Select the group from the dropdown, and press OK (you can put it to any group other than the “Licensed Strategies”). You can also open the strategy immediately after it's restored, by ticking the checkbox “After restoring, open…”. Then you'll be brought to its [Backtest Strategy Page](_documentation_backtest-strategy-page-overview_.md).

Now, if the EBTS file name is different from the strategy's name (as set in PB), another confirmation dialog appears, asking you which name to use:

!

Note, you can only import one strategy at a time. Unless you import a multi-strategy (a single EBTS file containing that multi-strategy), in which case you'll _also_ import its component strategies (its basic strategies) to Portfolio Boss.

* * **7.**  **To delete a strategy,** you must select it and press the “Delete” button at the top of this page. You can't simply press the keyboard's Delete button.

[https://portfolioboss.com/wp-content/uploads/2021/10/dr5t6yw4e56a3whA.mp4](_wp-content_uploads_2021_10_dr5t6yw4e56a3whA.mp4.md)

A confirmation dialog appears; simply press Yes.

If that strategy is used by a [Multi (or Meta)](_documentation_types-of-strategy_.md) strategy, a warning dialog shows up asking for your confirmation.

[!](_wp-content_uploads_2019_10_Confirm-Delete-Strategy.png.md)

Keep in mind you can't delete any of the “Licensed Strategies” (no “Delete” button is present if you select a licensed strategy).

That button is replaced with the “Reset” button for _reverting_ any of the licensed strategies into their _default_ state (if you manipulated its parameters on the “Backtest Strategy” page).

[https://portfolioboss.com/wp-content/uploads/2021/10/e45awgawa.mp4](_wp-content_uploads_2021_10_e45awgawa.mp4.md)

* * *

#### Note:

To unselect a strategy, hold down the Ctrl key while clicking that strategy.

[**Back to Top**](_documentation_managing-your-strategies_.md#backtotop)

You have already reported this .

#### _documentation_manual-results-tab.md

> Source: https://portfolioboss.com/documentation/manual-results-tab
> Scraped: 3/1/2026, 2:07:53 AM

!

This tab contains the history of modifications to the strategy; very much the “undo” feature of Portfolio Boss. Each time you pressed the standard (i.e. manual) backtest button, you created a record of the strategy here (a new _item_ appears in this tab).

!

So whatever rules, filters, parameters, and values you set will be recorded. In short, _anything_ on the [Rules Area](https://portfolioboss.wpenginepowered.com/wp-content/uploads/2021/05/gdg56ye5dg_00000_00000.png) of the strategy will be remembered.

Keep in mind though, by default there's a confirmation dialog when you press the “Start” button. You can tick the checkbox “Don't show again” if it's obtrusive to you (in won't appear next time):

!

Press the “Continue” button, and the standard backtest will be executed.

* * **1.  Favorite:** This column allows you to mark some items as favorite. Let's say you did some changes that resulted in a 700% CAGR (who doesn't want that as a favorite?).

!

Simply click their star buttons, and they will be highlighted in blue to say they're your favorites, distinct from the others.

It can also display just the favorite items here, instead of all items being shown. Click the tiny dropdown next to this column's header:

[https://portfolioboss.com/wp-content/uploads/2022/12/7ygi78udr567dh.mp4](_wp-content_uploads_2022_12_7ygi78udr567dh.mp4.md)

A popup toggle appears: if it's turned ON, you only see favorite items; and if it's turned OFF, you see _all_ items. Note, there's the info-bar on top that says “Favorites filter enabled” if you're viewing just the favorite items (this toggle is ON). If this toggle is OFF, the info-bar says “Showing all records”. And if there's not a single item (you haven't backtested the strategy even once), it says “No results yet”:

!

* * **2.  Date started:** Contrary to its name, this column actually shows the date & time that the backtests were _finished_ at.

!

In other words, these are the timestamp of the items creation. The date & time are based locally (from your computer). All items are sorted top to bottom based on this creation time, with the latest on top.

* * **3.  Metrics Score:** These columns show the [metrics](_documentation_metrics-panel-guide_.md) score for each backtest record (item).

!

They only appear if you specifically select them from the “Manage Columns” dialog:

[https://portfolioboss.com/wp-content/uploads/2022/12/tg67ur56yhswh.mp4](_wp-content_uploads_2022_12_tg67ur56yhswh.mp4.md)

You can select any metrics as shown on the Metrics Tab, be it their all-sample (AS), in-sample (IS), or out-of-sample (OOS) score. Take note of the bottom (horizontal) scrollbar there, it does not move the first metric-column. This could be useful to compare one important metric against the others.

Note, you can't sort the items based on these metrics' column. The items are always sorted based on the latest creation time (“Date Started” column).

* * **4.  Memo:** This column displays the memo (description) of each item. You can also add or edit the memos here (orange-rectangle highlighted):

!

By default when you start a backtest ! you can write a memo on the confirmation dialog:

!

But you can also write memos with the ! buttons highlighted above. Click the button and a text field appears; once you're done writing, click “Save Changes”:

[https://portfolioboss.com/wp-content/uploads/2022/12/fysetesgsew.mp4](_wp-content_uploads_2022_12_fysetesgsew.mp4.md)

Memos are quite important here so you don't go blindly loading & groping each item for its contents; with memos, you immediately know what you're after (the changes you did, the filters you applied, whether it's a holy grail or a piece of… expriment…, etc.).

But technically, memos are optional. At the very least, use that star button ! to mark things of importance.

* * **5.  Load Parameters:** These buttons are used to load the [Rules Area](https://portfolioboss.wpenginepowered.com/wp-content/uploads/2021/05/gdg56ye5dg_00000_00000.png) settings of a backtest item. This is the actual “undo” button that you're looking for: Click it, and it loads the backtest's filters, rules, parameters, portfolios, values, what have you. Even the [strategy name](_documentation_strategy-panel-guide_.md) will be loaded too.

!

Note when you load an item, none of the Reports Area is populated; so you have to do a standard backtest ! for its [Metrics](_documentation_metrics-panel-guide_.md), [Performance](_documentation_monthly-performance-panel-guide_.md), [Positions](_documentation_positions-panel-guide_.md), [History](_documentation_history-tab_.md), [Trade Signals](_documentation_trade-signals-panel-guide_.md), and [Chart](_documentation_chart-tab_.md) tabs to be populated. This backtest obviously will create a new item here; you may want to leave the memo empty just so you know it's only for generating the statistical reports.

Keep in mind if the strategy is currently in [read-only mode](_documentation_strategy-panel-guide_.md#ReadOnly), you can still load an item here after confirming to override the read-only mode from the dialog that appears:

!

You may need to click “Restore read-only mode…” (on the Strategy Panel) or navigate away to another strategy, so the read-only mode is restored.

!

* * **6.  Delete Buttons:** These are used for deleting the backtest items. You press that button and a confirmation dialog appears:

[https://portfolioboss.com/wp-content/uploads/2022/12/ift67udr567hdes6.mp4](_wp-content_uploads_2022_12_ift67udr567hdes6.mp4.md)

Essentially you're removing that “undo point”, or “strategy variation”, from the history.

Now, if you want to delete multiple items at once, select them with their checkboxes, and press the trash-bin icon on top-right corner:

!

* * *

#### Note:

*   This tab does not exist on [multi-strategies](_documentation_multi-strategy_.md), because they truly aren't customizable (rules-wise). What you can customize are the basic-strategy components, not the multi-strategy itself. [Basic and meta-strategies](_documentation_types-of-strategy_.md) have this tab.

[**Back to Top**](_documentation_manual-results-tab_.md#backtotop)

You have already reported this .

#### _documentation_meta-strategy.md

> Source: https://portfolioboss.com/documentation/meta-strategy
> Scraped: 3/1/2026, 2:08:29 AM

#### Introduction to Meta-Strategy

In Portfolio Boss, you can treat each strategy as if it were an Exchange Traded Fund (ETF). That means you can buy or sell an entire strategy as if it were a normal financial instrument.

Just like an ETF, each strategy bought/sold contains a collection of instruments within it. This is the purpose of a Meta-Strategy. So a Meta-Strategy is just like any normal strategies, but instead of individual stocks or bonds in its Portfolio, it contains a list of strategies to be bought or sold.

[!](_wp-content_uploads_2019_10_Meta-Strategy-Overview_00000.png.md)

If a Meta-Strategy enters a Position, it's buying _all positions_ of a Strategy. As long as that Position remains open, Portfolio Boss will give you Buy and Sell signals based on that strategy; in essence you're following that Strategy. Think of it like you're holding an ETF position, _but_ you also buy and sell the individual stocks as well.

If the Meta-Strategy sells a Position, it means you're selling _all Positions_ of that strategy, and the released fund will either be parked on the Meta-Strategy's [Cash Equivalent](_documentation_system-settings-panel-guide_.md#positionreplacements) (you'll buy the Meta-Strategy's Cash Equivalent), or be used to enter another strategy.

Note that if some strategies contain the same instrument, PB _will not_ group them into one trade, just like when you're buying two separate ETFs. So it's preferable that each strategy contains different portfolio from the other strategy. For example, one strategy is about Technology Sector, while the other is about Banking Sector.

Meta-Strategy can only be created with certain licenses. If you wish to upgrade your license, please contact our Customer Support team at [support@portfolioboss.com](mailto:support@portfolioboss.com).

* * *

#### Creating a Meta-Strategy from Scratch

To create a Meta-Strategy, go to the [“Strategy Management”](_documentation_strategy-management-page-overview_.md) page, and click the “New” button on the upper left corner. A dropdown will appear, and select “Strategy” from here.

[!](_wp-content_uploads_2019_10_Create-New-Meta-Strategy.png.md)

On the dialog box that appears, you can give a name to the Meta-Strategy, and select which group it will belong. Most importantly in this dialogue box, the “Strategy Type” parameter must be set to “Meta-Strategy”. 

[!](_wp-content_uploads_2019_10_Add-Meta-Strategy-Dialog.png.md)

Now, press OK and you'll be taken to the [“Backtest Strategy”](_documentation_backtest-strategy-page-overview_.md) page where you can customize the Meta-Strategy's parameters.

* * *

#### Customizing the Meta-Strategy

The “Backtest Strategy” page is perfectly identical to any normal strategies, in which you can add [Buy Filters](_documentation_buy-filters-panel-guide_.md), [Ranking Rules](_documentation_ranking-panel-guide_.md), [Sell Filters](_documentation_sell-filters-panel-guide_.md), and any [System Settings](_documentation_system-settings-panel-guide_.md) for this strategy.

[!](_wp-content_uploads_2019_10_Meta-Strategy-Backtest-page.png.md)

The only difference lies in the [Instruments Panel](_documentation_instruments-panel-guide_.md). As explained before, instead of adding a Portfolio of financial instruments, you add a list of strategies here. To do so, click the “Add Strategy” button on the top-right corner of this panel.

[!](_wp-content_uploads_2019_10_Add-Strategy-button8.png.md)

A dialogue box appears allowing you to select which strategies to buy/sell. Keep in mind, you can only select basic strategies here (either bundled with your license, or the ones you created yourself), not other multi or meta-strategies. 

[!](_wp-content_uploads_2019_10_Add-Strategies-Dialog-for-Meta.png.md)

You can search specific strategies by typing a name on the “Search strategies…” above. Once these strategies are selected (their checkboxes enabled), press the OK button and these strategies are listed on the Instruments Panel.

You can edit any of the listed strategies by clicking their name (highlighted blue). 

[!](_wp-content_uploads_2019_10_Click-to-Edit-A-Strategy.png.md)

A dialog box will appear allowing you to edit the strategy's parameters. Keep in mind, editing a strategy through this dialogue box also changes the actual strategy.

[!](_wp-content_uploads_2019_10_Edit-Strategy-Dialog-for-Meta.png.md)

Now, the most important thing about Meta-Strategy is this: as you already know, the Buy, Rank, and Sell filters _normally_ look at an instrument's _price_ _history_. But when it comes to a Meta-Strategy, these filters look at each _strategy's gain_ (which you can see on the [Chart Tab](_documentation_chart-tab_.md) if the strategy is backtested independently). 

[!](_wp-content_uploads_2019_10_Strategys-Gain-for-Filters_00000.png.md)

So for example, if a strategy is experiencing a drawdown i.e. its equity curve falls below the 200 days SMA Sell Filter, the Meta-Strategy will exit that strategy's entire positions. This way, think of the meta-strategy as _a layer above_ your basic strategies, to improve upon them. Since they're analyzed as financial instruments, you can decide _when_ to trade them, so you can have an even smoother ride.

* * *

#### Backtesting the Meta-Strategy

Now that the _Meta-Strategy's_ various parameters are set, you may backtest it as usual by clicking the “Start” ! button.

!

A confirmation dialog appears, allowing you to write a memo describing this backtest. If you don't want this dialog for future standard (manual) backtests, tick the checkbox “Don't show again”. To actually start the backtest, press “Continue”. The memo you wrote can be seen under the [Manual Results Tab](_documentation_manual-results-tab_.md) (once the backtest is finished):

!

The backtest may take quite a while since we're dealing with many strategies at once. Once finished, the resulting backtest reports are perfectly identical to a normal strategy, but instead of actual instruments, you'll see the _strategies_ listed on the reports. 

[!](_wp-content_uploads_2019_10_Meta-Positions-Panel.png.md)

[!](_wp-content_uploads_2019_10_Meta-History-Tab-22344.png.md)

An exception is the Cash Equivalent for the Meta-Strategy, which is listed as a normal instrument.

[!](_wp-content_uploads_2019_10_Meta-Stats-Tab.png.md)

You can click a strategy's name (from the [Positions Panel](_documentation_positions-panel-guide_.md), for example) and the [Price Chart](_documentation_instrument-tab_.md) for that strategy will show up, showing the candlestick chart as if it were a normal instrument. The candlestick bars represents the percentage gain of that strategy; you can also see the various indicators overlaid in this chart. 

[!](_wp-content_uploads_2019_10_Meta-Instrument-Tab.png.md)

The only thing missing is the Volume Chart data, since this is a strategy, not an actual ETF which actually gets traded on the Exchanges.

There is one particular panel in this Meta-Strategy that you must know: the [Trade Signals Panel](_documentation_trade-signals-panel-guide_.md). As said before, instead of instruments, a Meta-Strategy buys/sells strategies. _But_ the trades that you must do, actually involve buying/selling _actual instruments_. 

[!](_wp-content_uploads_2019_10_Meta-Trade-Signals.png.md)

This is reflected by the various buy/sell signals on this panel. As you can see, it lists _all Positions_ within the strategies that have been selected for a trade. It shows which Positions belong to what Strategies.

* * *

#### Note:

If your license includes the [**Divine Engine**](_documentation_fine-tune-a-strategy-for-the-best-settings_.md) capability, you may be able to use the [**Random Search Algorithm**](_documentation_backtest-parameterization-panel_.md#Random) on your meta-strategy. The Divine Engine takes it like any basic-strategy, except its instruments (portfolios) are its component-strategies. If these component-strategies were also created through the Divine Engine, you're binding these high-performing strategies (“instruments”) into a greater strategy, which is also optimized by the artificial intelligence. Hence it's a multi-layered winning system!

Pay attention to the property “Rule Set Parameterization” (on the Backtest Parameterization Panel, once the Divine Engine is enabled):

!

*   The first option, “Random selection”, allows the Divine Engine to slap random new filters (with random parameter-values) to the strategies it creates. Existing rules & filters will be “fine-tuned” to find the best values for them.
*   The second option, “Manual”, simply fine-tunes the existing rules & filters (based on your parameterization) to find the best values for them.

Please contact our **[customer support](mailto:support@portfolioboss.com)** if you wish to upgrade your license.

[**Back to Top**](_documentation_meta-strategy_.md#backtotop)

You have already reported this .

#### _documentation_metrics-panel-guide.md

> Source: https://portfolioboss.com/documentation/metrics-panel-guide
> Scraped: 3/1/2026, 2:08:04 AM

!

This tab is at the top-middle area of the [Backtest Strategy page](_documentation_backtest-strategy-page-overview_.md), and it shows the performance of a strategy in various statistical data. So instead of eyeballing the graph on the [Chart Tab](_documentation_chart-tab_.md), here you get the detailed scientific stats of your strategy.

This tab is only populated once the strategy is backtested (by clicking the “Start” button ! ).

By understanding the strategy's performance, you'll be confident putting your hard-earned money on the line. You may also realize some areas that are still lacking. But most importantly, you won't be surprised by any losses it will _eventually_ make. A_ny_ strategy will experience losses, the question is whether such losses is within your risk tolerance. That is why, the very first things you _must_ look here are the drawdown metrics (later explained).

* * *

This tab is divided into six columns:

!

**1.**  **Name:** shows the name of each metric, such as the strategy's total Score, CAGR, Maximum Drawdown, Sharpe Ratio, etc.

**2.**  **All Sample:** shows each metric's performance during the entire backtest period ([in-sample](_documentation_backtest-panel-guide_.md#insampleratio) and out-of-sample periods together).

**3.**  **In Sample:** shows each metric's performance during the in-sample period. Note, if you set the “In Sample Periods” parameter to 100% (on the Backtest Panel), this column shows the exact same values as the “All Sample” column.

**4.**  **Out of Sample:** shows each metric's performance during the out-of-sample period.

**5.**  **Efficiency (%):** shows how consistent the metric's performance is, throughout the entire backtest periods. This percentage is the result of dividing the _out-of-sample_ performance by the _in-sample_ performance. This is probably the most valuable report on your strategy, especially if you used [multiple in-sample periods](_documentation_backtest-panel-guide_.md#insampleratio) on your backtest.

The Efficiency value says a lot about the strategy's real life performance. If it weathered various market conditions with consistent performance, you could be sure its real life performance will be similar. Generally you want this as close to 100% as possible, anything much higher or much lower may signify nasty surprises (or tasty, who knows). Note, tweaking the property “Total In Sample Ratio” (on the Backtest Panel), will _immediately_ change the _values_ on the “In Sample”, “Out of Sample”, and “Efficiency” columns here. You don't need to run the backtest again for that.

**6.**  **Benchmark:** shows the benchmark's (for example S&P 500 index) metrics performance.

* * *

Now, let's dig into each metric listed there:

**1.**  **Score:** This is the overall score of your strategy, amalgamated from some _risk_ and _return_ metrics. So it's a good measure of the overall performance. Higher number is preferable.

!

* * **2.**  **Current Drawdown (%):** This is the drawdown that's currently underway (if there's any).

!

Drawdown is the fall of the investment value from the _last_ highest peak, and a drawdown continues to exist as long as a _new highest peak_ has not been reached (a peak whose height is equal or higher than the last highest peak).

!

This value is stated in _percentage_ of the total investment value (including previous losses and profits). For example, the total investment peaked at $120,000 before experiencing a 5% drawdown; that means $6000 has been lost since the beginning of the drawdown.

This _current_ _drawdown_ is affected by the backtest's end-date (set on the [“Date To”](_documentation_backtest-panel-guide_.md#datetoparam) parameter at the Backtest Panel). That is, if at the end-date the strategy doesn't experience a drawdown, this metric will show 0%. But if it experiences a drawdown at the end-date, this metric will show something greater than 0%. Obviously lower value for drawdown is better.

* * **3.**  **Current Drawdown (days):** This shows the duration of the _current_ _drawdown_ (up until today, or the end-date). 

!

A drawdown will not end until a peak that is equal (or higher) than the _last_ highest peak is reached. So if the **equity curve** is making a new peak but it's still _lower_ than the last highest peak, then the drawdown still exists.

But do understand: since following a strategy entails active trading (buying and selling the instruments) instead of holding indefinitely, when a drawdown occurs your buying power might be reduced (after the losses are realized). Hence next time you entered the new positions, your portfolio size will smaller than the pre-drawdown size. Thus gains will be less, and _it'll take longer_ to achieve breakeven. You may work around this problem by utilizing margin accounts (where you borrow from your broker to make up for the realized loss). But margin trading entails its own danger (leveraging goes both ways).

* * **4.**  **Max Drawdown (%):** This is the _deepest_ _drawdown_ that the strategy experienced during the specified period (in-sample, out-of-sample, or all-sample). Lower value is better for this metric. 

!

Max Drawdown is one of the most important metrics you should look upon early. Put it this way: most strategies will gain money no matter how slow or fast. But losing money can be devastating. Add to the fact that your buying power is reduced (as explained earlier), it may take a long time to get out of the hole. So instead of ogling the CAGR, you _should_ first understand the strategy's risks as shown by Max Drawdown (and Avg. Drawdown) metrics. And make sure they have good “Efficiency” value as stated earlier. In comparison, the S&P 500 index has a maximum drawdown of around 50%, and that's a buy and forget approach. Ask yourself, are you willing to lose half of your account balance during nasty times?

Now, the _strategy's_ Max Drawdown (not the benchmark) is shown on the [“Chart” Tab](_documentation_chart-tab_.md) as the red-highlighted area.

!

* * **5.**  **Avg. Drawdown (%):** This is the _average_ depth of the various drawdowns during the specified period (in-sample, out-of-sample, or all-sample). Lower value is better.

!

You must be sure the strategy can get you out in time before much of your account is eaten.

* * **6.**  **Max Drawdown (days):** This is the duration, in days, of the Maximum Drawdown. The duration is not from peak to trough, but to another new peak. Lower value is better.

!

* * **7.**  **Avg. Drawdown (days):** This shows the average _duration_ of the drawdowns, for the specified period (in-sample, out-of-sample, or all-sample). Lower value is better.

!

* * **8.**  **CAGR (%):** This shows the _Compound Annual Growth Rate_ for the specified period. That is, the _average_ yearly growth rate of your investment, _compounding_ from the previous year's losses & gain. 

!

Do understand that all metrics here, including CAGR, disregards the fact that you may add/subtract your account balance, throughout the course of following the strategy (to buy that new sailing boat, for example). So they are the pure, theoretical statistics; and CAGR is an excellent metric to compare _returns_ between strategies. Higher value is better.

For example, a CAGR of 20% on an initial capital of $1000 means:

*   it'll grow into $1200 by the first year ($1000 + ($1000 x 20%));
*   it'll grow into $1440 by the second year ($1200 + ($1200 x 20%));
*   and so on and so forth.

Obviously, since CAGR is just an _average_, it doesn't reflect the “real” investment value year by year; some years may experience losses while other years gained much higher than the CAGR.

* * **9.**  **CAGR/√Avg. DD Ratio:** This tells you the strategy's _return_ adjusted by the _risks_ (drawdowns). It simply divides CAGR by the square root of the Average Drawdown. A higher value lets you sleep better.

!

* * **10.**  **R² (%):** R-squared tells you how close to a straight line–on a log scale–the strategy's equity curve is. A value of 100% would be a perfectly straight line, which means your strategy performs perfectly consistent. 

!

A low value indicates more volatility on your strategy's performance. Obviously, you want a strategy that performs more or less consistently, without any big surprises.

!

* * **11.**  **MAR Ratio:** MAR tells you the risk-adjusted _growth_ _rate_ of the strategy. So, while CAGR only tells you of the absolute growth rate, MAR can tell you of that growth rate adjusted by the _greatest_ drawdown. 

!

It's calculated from dividing the CAGR by the Max Drawdown. A _low_ MAR value tells you of the great drawdowns that you may experience. Generally, a value greater than 1.0 is preferable, which means CAGR can outweigh the possible big drawdown in the future.

But keep in mind, for MAR to be useful, the strategy and the benchmark (or another strategy you're comparing against) must be backtested in _generally_ the same period (or the same backtest length).

* * **12.**  **Sharpe Ratio:** This is another risk-adjusted growth rate of the strategy. Sharpe Ratio takes the _risk-free_ profit out of the equation, so you can see better whether profit is due to excess risk. A higher value on Sharpe Ratio is better. 

!

Higher Sharpe Ratio may mean the strategy's portfolios are well diversified, thus decreasing the risk without sacrificing return too much. Lower Sharpe Ratio may mean you're too conservative, since the risk-free profit is greater, thus your total return is expected to be lower. But it could also mean you're too aggressive since the risk is higher, thus your return _may_ be expected to be low or even a loss. In essence, low Sharpe ratio tells you that you're either indulging in excess risk or being too conservative; a double edged sword for you.

A value greater than 1.0 is considered good (2.0 or 3.0 are excellent). Below 1.0 (or even negative) is not preferable.

* * **13.  Profit Factor:** This is the profitability factor of the strategy. Any values greater than 1 indicate a profitable strategy.

!

It's based from the ratio between winning positions' gains _and_ losing positions' losses. So for example, a ratio of 5 means: for every unit of loss, you gained 5 (which is quite attractive).

* * **14.  Total Trades/Rule Count:** This shows the usefulness of the strategy's rules; whether they sat idle, or generated quite a few trading signals during the specified period.

!

It's calculated from dividing the Total Trades metric (all the buy and sell signals combined) by the number of rules your strategy has (all the buy, ranking, and sell filters combined). For example if it shows a value of 200, each rule roughly yields 200 signals.

* * **15.**  **Total Trades/Cyber Code Expression Count:** This metric shows the usefulness of the [Cyber Code](_documentation_cyber-code-genetic-programming_.md) expressions (blocks).

!

It's calculated from dividing the Total Trades metric _by_ the amount of expressions (blocks) contained in the strategy's Cyber Code rules. For example a value of 800 means each expression is responsible for roughly 800 trades.

This metric is primarily used as a [Fitness Function](_documentation_backtest-parameterization-panel.md#FitnessFunctions), to prevent introns (code bloat) during the Cyber Code evolution. The metric doesn't show up if the strategy contains no Cyber Code rule.

* * **16.**  **Total Return (%):** This tells you the total _compounded gain_ by the end of the period, in percent of the initial capital.

!

This is what you see on [Chart Tab](_documentation_chart-tab_.md)‘s equity curve.

* * **17.**  **Total Amount:** This tells you, in dollar amount, the total _compounded gain_ by the end of the period. In other words, it's the money you'll earn if you use the strategy for the same period. 

!

This metric doesn't show if the [“Initial Amount”](_documentation_backtest-panel-guide_.md#initialamount) parameter (on the Backtest Panel) is at 0.

* * **18.**  **Total Trades:** This shows the amount of trades (the sum of all buy and sell signals) during the specified period.

!

It includes switch-day and stop-loss trades.

* * **19.**  **Total Positions:** This is the amount of positions entered during the specified IS, OOS, or AS period.

!

Obviously, this is _about_ half the amount of buy & sell signals generated.

* * **20.  Avg. Position Gain (%):** This is the _average gain_ (or loss) of all positions during the specified period. 

!

It's shown in percent of the position's entry value. Note, the benchmark column is not populated, simply because a benchmark is a buy-and-forget approach (just 1 position for the entire period).

* * **21.**  **Avg. Position Duration (Days):** This is how long the positions were held, on average. 

!

That is, the average duration between entering a position and exiting it. It could be useful in determining the timeframe of the strategy (short-term active trading, or longer-term).

* * **22.**  **Avg. Trades per Year:** This is the average number of trades (buy and sell) done in a year.

!

This metric is useful as a [Fitness Function](_documentation_backtest-parameterization-panel.md#FitnessFunctions), to control the amount of trades potentially executed by the strategy. Too many trades and you'll suffer considerable slippage and commissions. Too few and you can't capitalize on short term fluctuations.

* * **23.**  **Avg. Price:** This is the average _entry_ price for the positions.

!

With this metric, you'll see whether the strategy likes to enter penny stock positions, for example (which are usually illiquid and highly manipulated). But the main purpose is to use it as a Fitness Function, so that the strategies created by the [Divine Engine](_documentation_the-divine-engine-and-the-boss_.md) are not overfit to the past based on hindsight.

For example in a portfolio of cap-weighted index (such as the S&P 500), it's easy to fall into the trap of picking low priced instruments, knowing they'd eventually boost in price and be part of the vaunted index.

* * **24.  Winning Positions (%):** This shows the number of _profitable positions_ the strategy entered, in percentage of the total positions (during the specified period).

!

This metric could also describe the _winning-rate_ of the strategy.

* * **25.**  **Winning Years (%):** This tells you the number of _profitable years_ the strategy produced, in percentage of the total years (during the specified IS, OOS, or AS period). 

!

For example, a value of 80% could indicate the strategy was profitable 8 years out of every 10 years.

* * **26.**  **Winning Months (%):** This tells you the number of _profitable months_ the strategy produced, in percentage of the total months (during the specified period).

!

This and the previous metric (Winning Years) can be useful to determine the time-risk associated with the strategy (as opposed to the usual value-risk).

* * *

#### Notes:

*   If you harbor some reservations or doubt about Portfolio Boss's backtest result, whether some metrics are rigged, please by all means construct your own strategy mimicking certain indexes, or a strategy that holds a conglomerate stock throughout its lifetime (such as Berkshire Hathaway). You'll see that its resulting metrics (and yearly or monthly performance report) almost _exactly_ mirror the index's or the stock's (or ETF, what have you).
*   Some metrics can not be used as [Fitness Functions](_documentation_backtest-parameterization-panel.md#FitnessFunctions), they are: Total Amount, Current Drawdown (%), and Current Drawdown (Days).

[**Back to Top**](_documentation_metrics-panel-guide_.md#backtotop)

You have already reported this .

#### _documentation_miscellaneous-tab-guide.md

> Source: https://portfolioboss.com/documentation/miscellaneous-tab-guide
> Scraped: 3/1/2026, 2:09:19 AM

!

This Tab allows you to set various miscellaneous settings of Portfolio Boss, such as: the amount of memory (RAM) it uses, whether to show or hide various dialogs & notifications within the app, and to reset the app's interface to its default state.

It's divided into five sections:

*   Caching
*   Interactivity
*   Notifications
*   Tutorials
*   Layout

Each will be discussed next:

* * **1.**  **Caching:** defines the maximum memory (RAM) of your computer that Portfolio Boss is allowed to use, especially during heavy backtesting and caching-intensive operations. Simply set the slider to a value that you want.

!

You may lower this value if you experience general slowdown (or crashes) on your computer while using Portfolio Boss; or when you're using a 32-bit system (in which the total RAM is capped at 4 GB). But normally you don't have to touch this slider at all (default value). Reducing the usable memory obviously increases the backtests' duration (standard and even more so Divine Engine backtests).

A default value of 100% means Portfolio Boss uses 100% of the _free memory available_, not the total memory. 

* * **2.**  **Interactivity:** This section allows you to define interactive behaviors within Portfolio Boss, such as showing/hiding backtest confirmation dialogs, and whether to open a strategy after it's copied or restored:

!

*   “Show confirmation dialog when starting a Divine Engine test”: Toggling this _off_ will hide the confirmation dialog each time you start a _local_ Divine Engine backtest!(Random search algorithm). It's the same as ticking the checkbox “Don't show again” on that dialog:

!

*   “Show confirmation dialog when starting a Manual test”: Toggling this _off_ will hide the confirmation dialog each time you start a manual (standard) backtest ! . It's the same as ticking the checkbox “Don't show again” on that dialog:

!

*   “Automatically open the strategy after copying”: If this is toggled _off_, a strategy you copied (with the “Copy” button ! on top of its [Backtest Strategy Page](_documentation_backtest-strategy-page-overview_.md)) won't be automatically opened. It's the same as _unticking_ the checkbox “After copying, open the copied strategy” from that “Copy strategy” dialog:

!

*   “Automatically open the strategy after restoring”: If this is toggled _off_, a strategy that you restored (with the “Restore” button ! on top of the [Strategy Management Page](_documentation_managing-your-strategies_.md)) won't be automatically opened. It's the same as unticking the checkbox “After restoring, open the restored strategy” on that restore-strategy dialog (even if you press “Cancel” there):

!

* * **3.  Notifications:** These settings will show/hide _messages_ about using [Dynamic Portfolios](_documentation_portfolios-panel-guide_.md#dynamicportfolio) and successfully copying a strategy.

!

*   “Show warning when using unused dynamic portfolios in a strategy”: if this is toggled _ON_, there is a message dialog each time you use a Dynamic Portfolio that's never been used in any of your strategies. Therefore, PB will download the price data for it. If this is toggled _OFF_, there won't be such warning, and it's the same as unticking the checkbox “Don't show this dialog again”:

!

*   “Show success message when copying a strategy”: if this is toggled _OFF_, there won't be a success message each time you copied a strategy (with the ! button, either from the [Backtest Strategy Page](_documentation_backtest-strategy-page-overview_.md) or the [Strategy Management Page](_documentation_managing-your-strategies_.md)). It's the same as unticking the checkbox “Don't show this dialog again” on that dialog:

!

**Note:**

If you copied a strategy from the [Backtest Strategy Page](_documentation_backtest-strategy-page-overview_.md) and you opt to automatically open that duplicate, this copy-success message won't be displayed even if it's toggled ON in here.

* * **4.  Tutorials:** This section allows you to show/hide the tutorial buttons ! throughout the Portfolio Boss app (these buttons direct you to their respective user guide documents). There's only one toggle here, and it works as described:

!

You can do the same function with the F2 keyboard button anywhere within the Portfolio Boss app.

!

* * **5.  Layout:** This section allows you to reset the overall appearance of Portfolio Boss to its default state, including panels size, color scheme and theme, scale, etc. There's only one button here to do the task:

!

The same thing can be achieved by deleting the file “PortfolioBoss.user.db” located in the [database folder](_documentation_database-tab-guide_.md) (`%LocalAppData%\PortfolioBoss\Data`).

!

Make sure you closed Portfolio Boss before deleting that file. Once deleted, open Portfolio Boss and it will recreate the file. All the interface reverts to its default appearance.

[**Back to Top**](_documentation_miscellaneous-tab-guide_.md#backtotop)

You have already reported this .

#### _documentation_monthly-performance-panel-guide.md

> Source: https://portfolioboss.com/documentation/monthly-performance-panel-guide
> Scraped: 3/1/2026, 2:08:11 AM

This tab shows the monthly and yearly performance-history (profit or loss) for the whole backtest period. The tab is located at the [Reports Area](_wp-content_uploads_2021_05_gdg56ye5dg_00000_00000.png.md) of the “Backtest Strategy” page.

It's divided into two sections: Yearly Performance, and Monthly Performance.

!

**The yearly section** shows you the year-by-year gain history (or loss). That is, the strategy's percentage gain (or loss) _at the end_ of each year in relation to the amount at the _beginning_ of the year (therefore, the percentage is compounded from the _previous_ _year's_ total amount due to its loss/gain).

**The monthly section** tells you the percentage gain (or loss) at the end of each month, in relation to the month's _initial_ amount (i.e. compounded from the previous month's total amount due to its loss/gain).

Each section has three self-explanatory columns:

!

**1.**  The “Year” (or “Month”) column shows all the years (or months) that the strategy has gone through.

**2.** The “Test” column shows the _strategy_‘s yearly (or monthly) percent gain/loss.

**2.**  The “Benchmark” column shows the _benchmark_‘s yearly (or monthly) percent gain/loss.

You have already reported this .

#### _documentation_moving-average-cross-over-filter.md

> Source: https://portfolioboss.com/documentation/moving-average-cross-over-filter
> Scraped: 3/1/2026, 2:08:47 AM

[!](_wp-content_uploads_2019_10_Moving-Average-Cross-Over-Filter-Buy.png.md)

[!](_wp-content_uploads_2019_10_Moving-Average-Cross-Over-Filter-Sell.png.md)

This filter looks at two different Moving Averages for considering an instrument as a buy/sell. One Moving Average usually has a shorter duration than the other. If this shorter Moving Average is above (or below) the longer Moving Average, then the instrument will be considered.

The idea is pretty similar to the [“SMA Position filter”](_documentation_simple-moving-average-sma-position-filter_.md), in which you see whether the instrument's closing price is above/below its Simple Moving Average. So, if it closes above, it indicates a potential uptrend (or the uptrend is still strong), thus good for entering that position; if it closes below the SMA, then a potential downtrend, thus a condition to exit.

_But_ with this “MA Cross Over filter”, instead of the instrument's _closing prices_, we're looking at the _shorter Moving Average_. The idea is to generate a more valid trading signal, since a single closing-price could just be noise, while the _averaged_ closing-prices give a better representation of how the price behaves.

[!](_wp-content_uploads_2019_10_SMA-false-signal_00000.png.md)

[!](_wp-content_uploads_2019_10_MA-Crossove-Truer-Signal_00000.png.md)

So, if the shorter MA crosses above the longer MA, then the instrument is likely experiencing an uptrend; good for entering that position. And if the shorter MA crosses below the longer MA, it's likely the position is experiencing a downtrend; a reason to exit that position (or initiate a Short Selling).

These are known as Golden Cross (bullish) and Death Cross (bearish), respectively. Most market professionals see such phenomena (especially for major indices) like teenage girls would see Justin Bieber's latest fad. It's popular, but it's usually not as reliable as they make it sound. Therefore it's best advised to use them with other confirming indicators, like momentum oscillators or the Smart Money Indicator.

* * **1.**  The first parameter defines the period for the shorter MA. 

[!](_wp-content_uploads_2019_10_Moving-Average-Cross-Over-Filter-1st-Param.png.md)

Common values for swing traders are either 14, 23, or 50 days. Major indices' Golden and Death Crosses tend to have 50-day shorter MA against a 200-day longer MA slapped on them.

Obviously, you can enter a longer period here than the longer MA, but that doesn't make sense unless you’re doing [Short Selling](_documentation_a-strategy-for-short-selling_.md).

* * **2.**  The second parameter defines what kind of _shorter_ Moving Average to calculate. You can choose either SMA (Simple Moving Average) or _EMA_ (Exponential Moving Average) here. 

[!](_wp-content_uploads_2019_10_Moving-Average-Cross-Over-Filter-2nd-Param.png.md)

_EMA_ responds quicker to recent price changes, so it's better for short-term traders (or for use in a volatile market). But you can't go wrong when using SMA either.

* * **3.**  The third parameter defines whether the _shorter_ MA must be “Above” or “Below” the _longer_ MA for the instrument to be considered. For a Buy Filter, set this to “Above”, while for a Sell Filter, set it “Below”. 

[!](_wp-content_uploads_2019_10_Moving-Average-Cross-Over-Filter-3rd-Param-000.png.md)

The reverse is true if you plan on trading Short Positions: set this to “Below” to look for downtrending instruments to enter, and set the Sell Filter to “Above” to indicate uptrending Positions you must close.

* * **4.**  The fourth parameter defines the length of the _longer_ MA. 

[!](_wp-content_uploads_2019_10_Moving-Average-Cross-Over-Filter-4th-Param.png.md)

200 days is the norm here (unless you're a short-term swing trader).

* * **5.**  The fifth parameter defines the type of the _longer_ Moving Average, whether SMA or EMA.

[!](_wp-content_uploads_2019_10_Moving-Average-Cross-Over-Filter-5th-Param.png.md)

* * *

#### Note:

Once this filter is applied, two MA indicators appear on the instrument's Price Chart. One indicator is for the shorter MA, and the other indicator is for the longer MA.

[!](_wp-content_uploads_2019_10_Moving-Average-Cross-Over-Filter-Indicators.png.md)

[**Back to Top**](_documentation_moving-average-cross-over-filter_.md#backtotop)

You have already reported this .

#### _documentation_moving-average-persistence-filter.md

> Source: https://portfolioboss.com/documentation/moving-average-persistence-filter
> Scraped: 3/1/2026, 2:08:48 AM

!

!

This filter calculates the persistence that an instrument stays above (or below) its [Moving Average](_documentation_simple-moving-average-sma-position-filter_.md) line. As you well know, the Moving Average (for example the 200-day Simple Moving Average) is an excellent support/resistance line. But a breach of the SMA once or twice is not really a good indicator of a trend change. Quite often, an instrument may take a short trip below the SMA before resuming its powerful bullish stampede.

!

So instead of a tripwire, the Moving Average acts as a separator between two habitats: bearish instruments like to hibernate _below_ the Moving Average _most_ of their time, while bullish instruments call it their home the area above; though _sometimes_, bulls too need to rest and sleep _below_ to regain their strength.

!

!

Even better, this filter allows you to define: how far above the Moving Average the instrument should stay, and, how long it should stay there, before it's considered as a position. Such a distance above the Moving Average is derived from the instrument's volatility (its [Average True Range](_documentation_n-atr-above-below-sma-filter_.md)), thus the habitat is dynamically adjusting to the recent price behaviors instead of a fixed fenced area.

Now, be warned this filter has quite a bit of knobs and levers, so it may get a bit confusing:

* * **1.**  The first parameter dictates whether the instrument should stay above, or below, such a separator line.

!

To find bullish instruments, you want this set to “Above”; and “Below” for bearish instruments, but it's not set in stone. With other parameters customized (later explained), you can find anything given the right settings.

Note that the separator line is _plotted above_ the Moving Average line, by default. As shown in the screenshot below, the line that separates the two habitats is colored blue, while the Moving Average is shown in orange:

!

Later down the page you'll learn a trick, so the separator line is plotted below the Moving Average, to find _deeply_ persistent bear(ish instruments).

There's also the option “Between” here. That means we're looking for persistence in the area between the separator line and the Moving Average. If price _strays_ above or below such an area, the persistence is reduced. It could be useful for finding instruments that are neither hot overbought, nor chronically bearish:

!

**Note:** It's the _closing_ prices that matter here, not the intraday price action (high or low, or open). The instrument is persistent, as long as the closing prices stay in the specified habitat, even if the high, low, or opening prices go wayward.

* * **2.**  The second parameter defines the Moving Average period.

!

This is pretty obvious; the longer the period, the stronger the role of the separator line (since it's derived from the Moving Average). Thus the shorter the period, the harder it is for the instrument to stay persistent, because the separation between the two habitats is made obscure by a volatile/active Moving Average line. But generally, this parameter and the last parameter must be set in a roughly similar value, so it wouldn't be too hard (or too easy) for the instrument to stay persistent.

The usual values for a Moving Average are 26, 50, or 200 days.

* * **3.**  The third parameter defines the type of Moving Average used.

!

Here you may choose between SMA (Simple Moving Average) or EMA (Exponential Moving Average). SMA smooths out (averages) the closing prices equally, old and new; while EMA gives more weight to the most recent closing prices, thus more sensitive to the latest developments. There's nothing wrong with either option, but usually EMA is used for a shorter position duration (frequent trades), while SMA is for longer-term trades (where you use equally long periods in other parameters and filters).

* * **4.**   The fourth parameter defines the ATR multiplier. Practically, it lets you adjust how far the separator line goes from the Moving Average.

!

The number you put here multiplies the ATR (the volatility in US dollar), to create a longer or shorter distance from the Moving Average. Any value above 1 means the volatility measure is widened (thus farther from the Moving Average), while a fraction of 1 means it's reduced (thus a shorter distance). A positive number means the separator line is _above_ the Moving Average, while a negative number plots it _below_ the Moving Average. The latter is the trick to find deeply persistent bearish instruments:

!

The norm is to put a value of 2.5 or 3 here (either positive or negative). If you want the Moving Average itself to act as the separator of the two habitats (which makes sense, without being too restrictive), then put a value of 0 here. But keep in mind, usually with a shorter Moving Average period, the lower the ATR multiplier should be.

* * **5.**  The fifth parameter defines the ATR period.

!

For example, a value of 20 days means we're looking at the average price fluctuations of the last 20 days (denoted in US dollar). The general rule of thumb is to use a period of 9, 10, 14, or 20 days here.

* * **6.**  The sixth parameter defines whether persistence should be “More than” or “Less than” the threshold percentage.

!

For example, as shown in the screenshot above, the instrument must stay in the specified habitat _more than_ 50% of the _last 200 days_. So if it stayed 150 days (75%), that's a buy.

!

You can also set it to “Between” or “Not between” the upper and lower percentage bounds:

!

which can be useful to define a _specific duration_ it must stay on the habitat.

* * **7.**  The seventh parameter defines the threshold percentage in relation to the specified period, as explained above.

!

In other words, the percentage you set here is _the persistence_ that you want from the instrument. You can set any value here, but 50% is a good starting point.

* * **8.**  The eighth parameter defines the period of days _in which_ the instrument must stay persistent.

!

For example with a value of 200 days here, the instrument's persistence comes from: _the amount of days_ it stays in the specified habitat, out of the past 200 days. If it stays 150 out of the past 200 days (not necessarily contiguous), then its persistence is (150/200) \* 100% = **75%**.

* * *

#### Notes:

*   Don't set this filter too restrictive, especially as an exit filter. The wrong values may exit (discard) any buyable instruments before they can even be bought, thus creating constant cash positions for the strategy. For example, if you set the ATR multiplier too high, or the percentage threshold at 99%, none of the instruments may fulfill such criteria.

*   On the [Instrument Tab](_documentation_instrument-tab_.md) there are two visual indicators for this filter. The first one shows the Moving Average line, while the second shows the separator line (a certain ATR distance away from the Moving Average):

!

[**Back to Top**](_documentation_moving-average-persistence-filter_.md#backtotop)

You have already reported this .

#### _documentation_moving-average-persistence-rule.md

> Source: https://portfolioboss.com/documentation/moving-average-persistence-rule
> Scraped: 3/1/2026, 2:09:20 AM

!

This rule ranks the instruments based on their _persistence_ in staying inside the specified zone (habitat), as explained in the [Moving Average Persistence Filter page](_documentation_moving-average-persistence-filter_.md).

* * **1.**  The first parameter defines how the sorting happens.

!

“Highest” means the instruments with greater persistence (percentage) are ranked higher. While “Lowest” means you're looking for the least persistent ones.

* * **2.**  The second parameter defines the period of days where persistence is calculated.

!

For example as shown in the screenshot above, if the instrument stayed 200 days in the specified habitat, out of the 200 days specified here, its persistence would be 100%.

* * **3.**  The third parameter defines the habitat where the instrument must stay.

!

“Above” means the area above the separator line (i.e. above the Moving Average _plus_ the Multiplied ATR). “Below” means the area below the separator line. And “Between” means the area between the Moving Average and the separator line.

* * **4.**  The fourth parameter defines the Moving Average period.

!

The usual values are 26, 50, or 200 days.

* * **5.**  The fifth parameter defines the type of Moving Average used.

!

You may choose either SMA (Simple Moving Average) or EMA (Exponential Moving Average).

* * **6.**  The sixth parameter defines the ATR multiplier.

!

It lets you adjust how far the habitat separator is located from the Moving Average line.

* * **7.**  The seventh parameter defines the ATR period.

!

The usual values are 9, 10, 14, or 20 days.

* * *

#### Note:

The “Offset” and “Weight” parameters are explained in [this page](_documentation_ranking-panel-guide_.md#offsetweight).

[**Back to Top**](_documentation_moving-average-persistence-rule_.md#backtotop)

You have already reported this .

#### _documentation_multi-strategy.md

> Source: https://portfolioboss.com/documentation/multi-strategy
> Scraped: 3/1/2026, 2:08:28 AM

!

In Portfolio Boss, you can _combine_ two or more strategies into a _hierarchy_ contained within a _Multi-Strategy._ In essence, you're stacking the strategies top-to-bottom. So, if the top strategy is on a sell signal, instead of parking that money into the [Cash Equivalent](_documentation_system-settings-panel-guide_.md#positionreplacements), Portfolio Boss will operate the next strategy. If this child strategy also fails, then Portfolio Boss will go into the subsequent grandchild strategy, and so on and so forth.

!

The idea is that the top-most strategy is the riskiest investment (but also the most profitable), and if the market conditions don't favor risky investments, we go to the strategy with lesser risk. But if conditions are so bad that all strategies sell their Positions, then get out of all investments and park our money in cash only. So we limit risks based on market conditions, without sacrificing big profits. You will be consistently profitable; even at worst, you'll avoid that big and deep crash.

You can also combine strategies _without a hierarchy_ between them. It's like using each strategy _separately_, but now you don't need to backtest them one by one. Portfolio Boss divides your total account size between the strategies, based on their “Weight” percentage:

!

This is great for those with enormous account: It's well known that hedge funds performance would revert to the mean (or even negative) if their assets grow too big. So you diversify into different strategies with different asset-classes. Even better, these separate strategies can have _their own_ child strategies as well. So you're combining _multiple strategy-stacks:_

!

Note that some licenses don't have the ability to create Multi-Strategies. If you wish to upgrade your license, please contact our Customer Support team at [support@portfolioboss.com](mailto:support@portfolioboss.com).

* * *

### Create a Multi-Strategy from Scratch

Obviously, you need to create the individual strategies first, which will be combined in a Multi-Strategy. The most common way is to create them with tiered-risk management in mind, as described above. You may also create one Long Strategy and one [Short Strategy](_documentation_a-strategy-for-short-selling_.md): so instead of going flat (or shallow dip) during market break down, your account may shoot up high. Make sure these strategies are performing well before you combine them into a single Multi-Strategy.

In our case, we have created three strategies based on tiered-risk management:

!

*   **Allstock Strategy** is the first tier, the bread and butter strategy, that trades the Nasdaq 100 Portfolio (high return, but high risk).
*   **Dividend Strategy** is the second tier, and it trades stocks with the juiciest dividends. You'll _get paid regularly_ even when the bears come out.
*   **Treasury and Bond Strategy** is the last tier. It trades corporate and government bonds as a last line of defense, being one of the most stable asset classes during black swan events. Not only they're stable, they also pay excellent interests _regularly_ when the Fed decides to wreak havoc on the stock market. This last strategy is best to use Cash (instead of Cash Equivalent), so when all asset classes fail miserably, you revert to cold, hard, idle cash (which _may_ _still_ get you interest payment, depending on your broker).

It's recommended that you _name_ these strategies (from top tier to the bottom) in alphabetical order, so you can easily see their hierarchy later on.

Now, to create the Multi-Strategy, go to the [Strategy Management](_documentation_strategy-management-page-overview_.md) page and click the “New” button. From the dropdown, choose “Strategy”.

![Create a new strategy in Portfolio Boss](https://portfolioboss.com/wp-content/uploads/2024/04/Create-Strategy.jpg)

A dialog box appears where you can give it a name, and select the group to put it. Here, you _must_ set the “Strategy Type” to “Multi-Strategy”. Then press OK. 

![Add and name a multi-strategy in Portfolio Boss](https://portfolioboss.com/wp-content/uploads/2024/04/Add-Strategy-Multi-Type.jpg)

You'll then be brought to the [Backtest Strategy](_documentation_backtest-strategy-page-overview_.md) page where you can customize the new Multi-Strategy.

Note, the “Backtest Strategy” page is slightly different for a Multi-Strategy. The [Rules Area](https://portfolioboss.wpenginepowered.com/wp-content/uploads/2021/05/gdg56ye5dg_00000_00000.png) won't contain filters and rules, but a list of _strategies_ instead. And there's neither the [History Tab](_documentation_history-tab_.md) nor the [Top Ranking Instruments](_documentation_trade-signals-panel-guide_.md#toprankingsection) section (on the Trade Signals Tab).

* * *

### Adding the Various Strategies

Now to add the strategies, click the “Add Strategy” button on the **Strategies Panel:**

!

A dialog box appears to let you search and add the strategies. Note that you can only add [Basic Strategies](_documentation_types-of-strategy_.md) here (either built-in with your license or those you created). 

!

Once the strategies are selected (ticked), press OK and you'll see those strategies listed alphabetically on the Strategies Panel:

!

To remove one strategy from the list, click its trash bin button; to delete _all_ strategies at once, click the top-most trash bin button.

* * *

### Editing Each Listed Strategy

You can edit any of those strategies by clicking the strategy's name (highlighted blue):

!

The “Edit Strategy” dialog appears, representing the [Rules Area](_documentation_backtest-strategy-page-overview_.md#BacktestStrategyAreas) for that strategy. Here you can change the strategy's rules (and Portfolios), just like when you open the strategy on its own. 

!

Keep in mind, this is editing the _actual_ strategy, so to prevent unwanted changes it's set to read-only mode (you can't edit anything). You must click the button “Override read-only mode” to edit the strategy. A dialog shows up to confirm the override; simply click “I understand”.

!

It's better that you only make light changes from the “Edit Strategy” dialog, as you can't backtest the strategy from here. To make big changes and see the resulting performance, better do it from its own [Backtest Strategy Page](_documentation_backtest-strategy-page-overview_.md).

Now, in regard to the hierarchy, the most important change we do here is the Cash Equivalent rules. You want to _make sure_ all strategies (_except_ the lowest tier strategy) use Cash Equivalent _instead of_ Cash. And choose whatever instrument as Cash Equivalent (e.g. SHY, PTSHX, or even inverse/bearish ETF).

!

That way, the strategies are _allowed_ to have a child strategy. The lowest tier strategy (which won't have a child) is set to use Cash, so when all strategies & assets fail, we revert to the final safety of the dollar. Once done with the editing, click the “Close” button (no need to click “Restore read-only mode” as it's automatically done when you close the dialog).

### Creating a Hierarchy between the Strategies

Going back to the Strategies Panel, you see that each strategy has a checkbox. If you want a strategy to have a child, tick the checkbox. And then choose the child strategy from the dropdown menu: 

!

In our case, the Allstock Strategy will have the Dividend Strategy as its child.

This Dividend Strategy, in turn, will have the Treasury & Bond Strategy as its child (which will be a grand-child strategy overall). So do the same thing: tick the Dividend Strategy's checkbox and select its child from the dropdown.

!

The Treasury & Bond Strategy, being the last tier and thus no child, does not have a checkbox, as it uses Cash instead of Cash Equivalent.

!

As a side note, if you want a strategy to have a child but there's a warning “No assignable strategies left”, it means all the listed strategies have been put in the hierarchy; simply add more strategies to the list:

!

Lastly, for this hierarchy to work properly, _make sure_ the first tier strategy (the ultimate parent) has its _actual_ “Weight” set to 100%. You can put any number here so long as the percentage inside the parentheses reads 100%.

!

That means, you're putting 100% of your account size into the ultimate parent. That fund will then _trickle down_ to the child and grand-child strategies, depending on the market conditions.

Thus, you've created a strategy stack. From the first tier to the last (top to bottom), the strategies are listed alphabetically, so _you_ don't get confused. You can now backtest the strategy to see how it performs. If you wish to use it, enable its email notifications:

!

When you press the “Start” button, a Multi-Strategy doesn't show a confirmation dialog, unlike other types of strategy where you can write a memo.

Keep in mind, since we'll be backtesting many strategies, it may take longer than usual.

* * *

### Seeing the Strategy Stack in Action

This section might be a little complex. But in reality, once the Multi-Strategy is put to use, such complex mechanism is taken care of by Portfolio Boss. All you need to do is fire up the [Trade Plan Calculator](_documentation_trade-plan-calculator_.md) whenever trading signals are given, and input the order information to your broker. If you're curious how a stack of strategies works, read on.

Behind the scene, each strategy runs _independently_, regardless of the hierarchy. So each strategy has the usual Buy and Sell [Signals](_documentation_trade-signals-panel-guide_.md), and its _current_ [Positions](_documentation_positions-panel-guide_.md) held. Let's say we put $100,000 into the Multi-Strategy; this amount will be assigned initially to the Allstock Strategy:

!

If we look at the Positions Tab, the Multi-Strategy _fully_ utilizes the 1st tier strategy (Allstock) and _none_ of the child strategy. All its 10 Positions are still in stocks:

!

With the Allstock Strategy's “Current weight” of 100% (as shown above), the whole $100,000 are currently used by it. Its Positions are given different amounts, based on their weights (due to their gains & losses).

Now, if we look at the Trade Signals Tab, _one_ Position of the Allstock Strategy (ADTN) will be sold the next day:

!

Normally, if a Position is sold, it will be replaced by the Cash Equivalent (SHY). But as you see above, instead of a Buy Signal for the SHY, there are signals to _buy all_ the child's Positions (Dividend Strategy). In other words, _every_ sold Position of the parent (which is supposed to go to Cash Equivalent), will be replaced by _the whole_ child strategy. Remember that each strategy runs independently, therefore the child strategy has its own existing Positions.

The weight of the sold Position will be _divided equally_ among the child's Positions. In this case, the ADTN weight of 9% ($9,000) will be divided by the child's 10 Positions, so each will have 0.9% ($900).

!

So let's open the [Trade Plan Calculator](_documentation_trade-plan-calculator_.md), so these trades will be executed tomorrow. We enter $100,000 into this calculator, click the button “Update Suggested Quantities” (or press enter), and don't forget to tick the checkbox “Check this if this is the first time you're entering this strategy”:

!

Essentially we'll be buying 9 stock Positions for the Allstock Strategy (worth about $91,000) because this is the first time we're using the Multi-Strategy. We'll also buy 10 stock Positions of the Dividend Strategy (all worth about $9,000). We'll input all this information to the broker. Note the dollar amount for each Position (orange rectangle above), especially for the child: it's not exactly $900 per Position. This is due to the price-per-share causing imperfect division.

At the next day, if we take a look at the Positions Tab, there are two groups of strategy listed here:

!

One group is for the Allstock Strategy (9 Positions), and the other group for the Dividend Strategy (10 Positions). Note the current weight for the Allstock Strategy is now at 90.6%, whereas the Dividend Strategy is at 9.4% instead of 9%. This is due to the gain/loss that some Positions went through today. Also take note of the green arrow, which shows the Allstock Strategy's Position sold at today's market open.

There are no trade signals for the next market open, so if you look at the Trade Signals Tab there's only a note to hold the current Positions (19 symbols; 9 from Allstock Strategy, 10 from Dividend Strategy):

!

Come the next trading day, the strategy has gained about 4.1%, so our account size is about $104,100 now. This is just an approximation, calculated from the difference between the Multi-Strategy's total return _today_ versus the day we entered the strategy (which can be seen from the [Chart Tab](_documentation_chart-tab_.md)). You may need to check your brokerage account for the exact account size.

If we look at the Positions Tab, the weights for all Positions have also changed, reflecting the dollar amount each holds in relation to the current account size (due to gain/loss):

!

The Trade Signals Tab also shows some signals for tomorrow: the Dividend Strategy will sell one of its Positions (DHI), with a weight of 1% ($1,041):

!

As stated earlier, each sold Position of the parent will be replaced by the whole child strategy. In this case, the Dividend Strategy has the Treasury & Bond Strategy as its child. Therefore we also have the signals to _buy all_ 10 Positions of the Treasury & Bond Strategy, each with a weight of 0.1% ($104).

!

So let's open the Trade Plan Calculator and enter our _current_ account size ($104,100). This time we shouldn't tick the checkbox at the bottom, since this is our _second trade_ with this Multi-Strategy.

!

As usual, each _new_ Position isn't exactly worth $104 as per our theoretical calculation (due to price per share causing imperfect division). As a side note, the dollar amount distributed to the child doesn't come from the sold Position's actual dollar amount (in this case $979.03), but from the theoretical amount (1% of $104,100, i.e. $1,041).

At the next day, we see the Positions Tab is fully populated with the three strategies:

!

We see the Dividend Strategy's weight decreased from 9.5% to 8.4% due to the DHI sale (sold at the market open), hence 1% went to the Treasury & Bond Strategy. The weight change is also due to the overall gain/loss that all strategies went through today. Our account size now sits at $107,430 (3.2% gain eyeballed from the [Chart Tab](_documentation_chart-tab_.md)).

If we see the Trade Signals Tab, we'll _sell all the remaining_ Allstock Strategy tomorrow (apparently there's a market break down of some sort).

!

The Allstock Strategy's weight is currently at 90.6% (out of $107,430), or about $97,331. This will be used to buy _all 10_ of the Dividend Strategy's Positions (including the 1 Position that represents the Treasury & Bond Strategy). So _the new_ Positions for the Dividend Strategy will be worth 9.1% each (rounded up from 9.06%). And _the new_ Positions for the Treasury & Bond Strategy will be worth 0.9% each (rounded from 0.906%).

!

So let's open the Trade Plan Calculator and input $107,430 there:

!

You'll notice that the Buy orders have a percentage-suffix on them (inside the parentheses). It indicates the percent-increase from the existing Position. For example the Position WSM (Dividend Strategy) currently sits at $977 (0.9%), and we'll be buying $9,733 more (9.1%), which is an increase of 996.21% from the current WSM Position. Note that some Buy orders are split (e.g. HYLD), because they exceed the average volume per minute (the percent-suffixes will add up to the total increase).

At the next day, we see the Positions Tab, and none of the Allstock Strategy is present. The Multi-Strategy now fully utilizes the child and grandchild strategies. There's a section showing the Allstock's Positions that were sold at the market open today:

!

But the most interesting are the new Positions, highlighted by the red rectangles. They're separated from the old Positions (those not highlighted), despite comprising the _exact same symbols_. Because, as you see on the blue rectangles, their dollar amounts (weights) are different from the old Positions, not to mention their holding duration is different too (thus different total gain/loss). So they're technically different Positions from the old ones.

You may also notice the “(9)” suffix on those new Positions. It simply shows the _multiplier_ for that Position. As you remember, each sold Position from the parent equals one child strategy. We recently sold 9 Allstock Positions, so we have 9 times the Dividend Strategy, which translates to 9 times of its Positions.

!

Ditto Treasury & Bond Strategy's new Positions have the “(9)” suffix, because: _despite_ its parent (Dividend Strategy) only selling 1 Position, there are actually 9 Dividend Strategies activated (due to Allstock's 9 Positions sold), thus there are actually 9 Positions sold from the Dividend Strategy, which translates to 9 times the Treasury & Bond Strategy. **It sounds complicated but really it's not that important; what counts is the _weight_ of each Position.**

Now, fast forward a couple of days later, we have signals to _sell all_ the remaining Dividend Strategy's Positions:

!

We suffered some losses the past couple of days, so our account size is now at $106,860. All the Dividend Strategy _is_ worth 89.9% (about $96,120) and this will be divided evenly to all 10 Positions of the Treasury & Bond Strategy (thus 9% for each new Position, or about $9,612).

!

As usual, we'll open the Trade Plan Calculator and input our account size of $106,860. And send the information to the broker.

Come the next trading day, the Positions Tab shows the Treasury & Bond Strategy is fully utilized (100% weight). All 20 Positions of the Dividend Strategy were sold at today's market open.

!

And we have 10 _new_ Positions under the Treasury & Bond Strategy (red rectangles), each with a suffix “(90)”. It means that _each_ _new_ Position is multiplied by 90, since there are 90 Treasury & Bond Strategies activated based on the recent sale.

!

For the next few days, the Multi-Strategy fully operates with Treasury & Bond's Positions. Eventually, these bonds too will be sold, so the Multi-Strategy will hide 100% behind the safety of the dollar.

!

Notice when a symbol will be sold, the trade signal doesn't discriminate between the different Positions of that symbol. For example the symbol ICVT is represented by three Positions: ICVT (90), ICVT (9), and ICVT, which will be sold all at once. All three are added together into a total weight of 9.8%.

Our trading account now sits at $106,851, and all this will be converted to cash at tomorrow's market open.

!

So we open the Trade Plan Calculator and input $106,851. All orders are simply sell orders here:

!

Note, when a sell order is split (due to exceeding average volume per minute), there's a percentage suffix on each split-order. For example the ticker PCEF is split into two sell orders, each with a suffix “(50.08%)” and “(49.92%)”, which add up to 100% of the PCEF sale. It's simply a split-percentage, not the percent-addition we saw earlier.

Now, our Multi-Strategy would stay in cash for the next 6 days. If we look at the Positions Tab, there is _only one_ Cash Position, with a multiplier of 1000.

!

This is because there are 100 Treasury & Bond Strategies activated (10 Allstock positions sold × 10 Dividend positions sold), with each Treasury & Bond Strategy containing 10 Cash Positions.

Six days later we'll exit the Cash Position: the Allstock Strategy will enter 5 stock Positions, and coincidentally the Dividend Strategy too will enter 10 stock Positions. So the Allstock Strategy will be assigned 50% of the Cash (10% for each new Position); therefore _the remaining_ 50% will be assigned to the Dividend Strategy (5% for each Position). It's a switch day, so the new Positions will have equal weights.

!

It may be a little confusing to see the Dividend Strategy divided into two groups (green areas); ditto the Treasury & Bond Strategy (red areas). But really it's just _visual_. The total weight for _each symbol_ (Dividend Strategy) would still be 5%. It's still the same as when there's _only one_ Dividend Strategy group, with each Position given a suffix “(5)” and a weight of 5%.

!

Our account size is now $107,300. So we open the Trade Plan Calculator and enter that amount. We have all Buy orders here, for the 15 stocks (5 for Allstock Strategy and 10 for Dividend Strategy).

!

At the next trading day, you see the Positions Tab too shows the Dividend Strategy divided into two groups.

!

Sometimes when using a Multi-Strategy you'd be shown multiple groups this way. Just think of them as one group that we've seen so far.

Thus now you understand how a stack of strategies works, in general. There are some rare scenarios not yet explored here, but as said earlier, you shouldn't concern yourself too much with the nitty gritty mechanics. What you see on the Positions Tab (or the Trade Signals Tab) may be overwhelming, but really what you should do is just open that Trade Plan Calculator and make your trades.

**Notes:**   The same ticker (symbol) can be shown in separate strategy groups; but when it comes to the actual trading, Trade Plan Calculator merges them as usual.
*   In a continuously-switching strategy, the sold Positions won't necessarily activate the child strategy, as by nature it will _immediately_ replace them with new Positions (instead of parking into the Cash Equivalent). Only in rare cases will it enter the Cash Equivalent (thus activating the child strategy), e.g. when none of the instruments passed the Buy Filters.
*   Behind the screen, each sold Position (Cash Equivalent) of a _parent_ equals one child strategy. Portfolio Boss keeps track of this child strategy's weight change (due to gain/loss), so if the parent replaces the said Cash Equivalent Position (into a stock Position), the fund will be pulled from this specific child strategy belonging to that parent Position. The child strategy Positions will be sold even if they don't hit any Sell Filters.

* * *

### Assigning the Minimum Capital for the Child Strategy

As you see from the examples above, the _weight_ of a child strategy becomes quite small if the parent merely sold _a few_ positions. Trading with such small capital on a whole Portfolio may not be desirable, as commission & slippage may offset the gain. You can avoid that by specifying the _minimum number_ of sold positions before the child strategy is activated. For example, the child will only be activated if the parent strategy sells 5 out of the total 10 Positions (50% on Cash Equivalent).

You can set the percentage on the parameter shown below: 

!

A value of 0% means _any_ Cash Equivalent Position (from the parent) will immediately activate the child strategy; while a value of 100% means the parent must be _entirely_ in Cash Equivalent Positions before the child strategy kicks in.

Let's say you set it to 50% (out of 10 Positions), then for the first 4 Positions sold, the parent strategy will buy its Cash Equivalent instrument (SHY, PTSHX, etc.):

!

!

Once the parent contains 5 sold Positions, the child strategy will be activated to replace them (the previous 4 SHY positions are sold, along with the 1 stock Position). 

!

!

Subsequent sold Positions will be immediately converted to the child strategy:

!

But if the parent strategy drops again to 4 Cash Equivalent Positions, it's now below the 50% threshold, thus all child Positions will be _sold_ (child strategy deactivated), and you'll _buy_ the parent's Cash Equivalent instrument (along with the new stock Position). We use a different Multi-Strategy as an example here:

!

!

!

This way, _at least_ 50% of the parent will be transferred to the child strategy, so you're trading the child with decent capital amount. You can also use this method to make sure the child is activated _only if_ there's terrible market breakdown for the parent strategy; so you get the most out of the parent, at the expense of a slightly deeper drawdown.

**Note:**

The percentage will be rounded up if there's no clear division. For example you set this to 51% out of 10 Positions, then the child will only be activated if there are 6 Cash-Equivalent Positions instead of 5.

* * *

### Combining Strategies without Hierarchy

As stated earlier, you can also combine two or more strategies _without a hierarchy_ between them. Even better, each of the strategies can have its own stack (hierarchy). The key here is the top-most strategies; they are the head of the families.

[!](_wp-content_uploads_2019_10_Multi-Strategy-without-Hierarchy_00000.png.md)

Each top-most strategy must have its “Weight” parameter set _greater than_ 0%, which defines the fund size to put into each stack. 

!

Let's say, you have two stacks: the first is comprised of Strategy A, Strategy B, and Strategy C; the second is Strategy X, Y, and Z. The first stack is given a weight of 40%, while the second 60%. We can input anything here (e.g. 4 and 6 instead of 40 and 60), as long as the _actual weight_ (inside the parentheses) reads 40% and 60%.

If you have $100,000 to fund this Multi-Strategy, the first stack will be given $40,000 and the second one will be given $60,000, to fund their respective top-most strategy first:

!

The fund will then trickle down to their respective child and grandchild strategies, as usual. Whatever happens, each stack has (about) 40% and 60% _total_ weight. The strategies are grouped top to bottom based on their respective stack:

!

As already stated, the multi-strategy will try to maintain the weight of each stack as you set. So if there's a stack that exceeds its weight (let's say because it's profitable), the next time its Positions are closed, some of the profits will be set aside as “Unassigned cash” in order to trim that weight back to the one you set. This unassigned cash can then be used to fund the next Positions once there are trades (could be for the other stack), so all stacks go back to the original weight ratio you set for them. If you look at the Positions Tab, you'll see the “Unassigned cash” section if such is the case:

!

It may appear at the top or bottom of that tab, it doesn't matter.

Now, the Trade Signals Tab may look equally complicated for these multiple stacks, but essentially they're ordered top to bottom from parent to child, and each stack is bundled in its own group:

!

You can also see the _limit orders_ and _limit prices_ here (in the example above: “Limit Sell” orders), if any of the strategies uses [Limit Orders](_documentation_system-settings-panel-guide_.md#BuyOrderType). It looks really complex, but simply open the Trade Plan Calculator as usual to create your orders (the limit prices are also displayed there).

**Note:**

You can pick a strategy from the first stack, to become a child for the second stack. For example, we pick Strategy C as the child of Strategy Y. So the stack now becomes: Strategy X → Strategy Y → Strategy C. The other stack (Strategy A → Strategy B → Strategy C) still runs normally. This could be useful so you don't have to create separate strategies for the two stacks, e.g. if both stacks trade treasury & bonds as a last line of defense (as represented by Strategy C).

!

This Strategy C operates from the second stack, and is completely separate from the first stack.

!

!

Even if Strategy C has a child (set on the first stack), the Strategy C and its child will operate fully from the second stack, and are completely separate from the first stack's Strategy C and its child.

* * *

#### Notes:

*   Child strategies normally have their “Weight” set to 0%. If you set it greater than 0%, the child will be divided in two: one will be used normally as part of the parent stack, the other will create a stack of its own (it becomes the topmost parent), with the Weight greater than 0% that you set for it. 

*   As stated earlier, a Multi-Strategy doesn't have the [History Tab](_documentation_history-tab_.md). But you can export an Excel file containing the trade & positions history (more in-depth than the History Tab). To do that, backtest the strategy first then press the “Export” button. A dialog appears; select the topmost option, and press “Export”.

!

For a more thorough explanation about multi-strategy's export results, read [**here**](_documentation_exporting-the-backtest-result_.md#MultiStrategyExport).

[**Back to Top**](_documentation_multi-strategy_.md#backtotop)

You have already reported this .

#### _documentation_n-atr-above-below-sma-filter.md

> Source: https://portfolioboss.com/documentation/n-atr-above-below-sma-filter
> Scraped: 3/1/2026, 2:08:50 AM

[!](_wp-content_uploads_2019_10_N-ATR-Above-Below-SMA-Filter-Buy.png.md)

[!](_wp-content_uploads_2019_10_N-ATR-Above-Below-SMA-Filter-Sell.png.md)

This filter will consider an instrument based on _how far_ the _last_ closing-price of that instrument goes above or below the [Simple Moving Average](_documentation_simple-moving-average-sma-position-filter_.md). It's rather similar to the [Bollinger Bands](_documentation_bollinger-bands-bbands-filter_.md) in that the closing price must fall within or outside the walls (bands), except there's only one wall here, and its distance is measured through ATR instead of Standard Deviation of the prices.

To understand this filter, we must understand what an ATR is: Average True Range measures the instrument's volatility (in dollar value) for the past certain days (or months), and as such, it doesn't give any specific signals on whether to exit or enter positions. ATR only tells you: the instrument _usually_ goes up or down x dollar amount per day, _during_ the past certain period.

Now, the general Technical wisdom says if a _downtrending_ instrument goes _above_ the SMA 3 times the ATR (or greater), then it is likely to reverse direction toward an uptrend. Or if it's an _uptrending_ instrument, then such a price spike above the SMA is a _confirmation_ the uptrend continues.

[!](_wp-content_uploads_2019_10_N-ATR-example-Down-to-Up_00000.png.md)

The reverse is also true: if an _uptrending_ instrument goes _below_ the SMA up to 3 times the ATR, it is likely to reverse toward a trading range (or even a downtrend). This is because SMA acts as a strong support or resistance line for the instrument, so if an instrument breaks that line quite far, there's a strong possibility of a trend change.

[!](_wp-content_uploads_2019_10_N-ATR-example-Up-to-Down_00000.png.md)

In plain language, this filter will buy (or sell) an instrument if the instrument closes “above/below” the SMA-ATR indicator. The SMA-ATR indicator is defined as:

*   the past “x days” SMA “plus/minus” the multiplied-ATR for the past “y days”.

Such indicator will be overlaid on the Price Chart, and will change _immediately_ according to the parameters you set on this filter. There's also the SMA indicator overlaid on the Price Chart (based on the SMA period you specified in this filter).

[!](_wp-content_uploads_2019_10_SMA-ATR-plus_00000.png.md)

As a tip, it's better to use this with [another filter](_documentation_moving-average-cross-over-filter_.md) that defines whether the instrument is uptrending or downtrending.

* * *

So, here's the explanation for the parameters:

**1.**  The first parameter, “above/below”, defines whether the instrument must close above or below the SMA-ATR indicator for it to be bought (or sold). Generally, for a Buy Filter you want to set this to “Above”, while for a Sell Filter set it to “Below”. 

[!](_wp-content_uploads_2019_10_N-ATR-Above-Below-SMA-Filter-1st-Param.png.md)

But again, it all depends on what you want to use this filter for. If you're using this filter to look for _discounts_ when entering positions, then set this parameter to “Below”.

* * **2.**  The second parameter, “x days” SMA, defines the period to look back for the Simple Moving Average of that instrument. For example, if you're a swing trader, this period shouldn't be too long. 

[!](_wp-content_uploads_2019_10_N-ATR-Above-Below-SMA-Filter-2nd-Param.png.md)

But if you're trading longer term, a shorter period usually gives more false signals, thus enter a longer period here.

* * **3.**  The third parameter, i.e. “plus/minus”, defines whether the SMA-ATR indicator should be above the SMA (“plus”) or below the SMA (“minus”). Again, for a Buy Filter this is usually set to “plus”, whereas Sell Filter is usually set to “minus”. 

[!](_wp-content_uploads_2019_10_N-ATR-Above-Below-SMA-Filter-3rd-Param.png.md)

_How far_ that indicator is above/below the SMA is defined on the next ATR parameters.

* * **4.**  The fourth parameter, e.g. “3”, is the multiplier to the ATR value. 

[!](_wp-content_uploads_2019_10_N-ATR-Above-Below-SMA-Filter-4th-Param.png.md)

For example, an exit signal will be given if the instrument's price falls _further_ than the: SMA minus 2x ATR, then set this parameter to “2” (which means the threshold price is 2 times the ATR _below_ the SMA).

Values up to 3 times the ATR are generally used for trend confirmation or reversal. But if you're merely looking for a discount when entering positions, set this at _a fraction_ of the ATR.

* * **5.**  The fifth parameter, i.e. “y days” ATR, defines the length of the ATR period. Again, if you're a short-term trader use a shorter period here to look for the ATR, for example 5 days, and vice versa. For normal trading, set it to 14 days.

[!](_wp-content_uploads_2019_10_N-ATR-Above-Below-SMA-Filter-5th-Param.png.md)

* * *

#### Note:

If you're using this filter to look for discounts, make sure to use this filter the second time (as another Buy Filter). This second filter makes sure that the instrument's price is _above_ the SMA-ATR indicator, and this SMA-ATR indicator is set to 3x ATR _minus_ the SMA.

The first filter on the other hand, looks for instruments that close _below_ the SMA-ATR indicator, and its SMA-ATR indicator is set to _a fraction_ of the ATR _plus_ the SMA. Look at the picture below:

[!](_wp-content_uploads_2019_10_Two-N-ATR-Filters-for-Discounts.png.md)

[**Back to Top**](_documentation_n-atr-above-below-sma-filter_.md#backtotop)

You have already reported this .

#### _documentation_octane-indicator-filter-guide.md

> Source: https://portfolioboss.com/documentation/octane-indicator-filter-guide
> Scraped: 3/1/2026, 2:08:48 AM

[!](_wp-content_uploads_2019_11_Octane-Indicator-Filter.png.md)

[!](_wp-content_uploads_2019_11_Octane-Indicator-Filter-Sell.png.md)

This filter allows you to look for instruments that are more volatile than the market, thus you may have a higher return (but beware of greater drawdowns). Or if you want to be conservative, use this as a Sell Filter, where the strategy will exit any Positions that become _more_ volatile than the market.

* * *

#### Note:

There is an advanced version of this filter where you can have access to more parameters. If you wish to upgrade your license, please contact our Customer Support team at [support@portfolioboss.com.](mailto:support@portfolioboss.com)

You have already reported this .

#### _documentation_overall-top-results-tab.md

> Source: https://portfolioboss.com/documentation/overall-top-results-tab
> Scraped: 3/1/2026, 2:08:15 AM

!

This tab contains the crème de la crème of the top strategies. These are the **best 20** strategies from all backtests you did in this strategy; be they standard (manual) backtests, or Divine Engine backtests (local and cloud). This tab is located at the bottom-middle of the [Backtest Strategy Page](_documentation_backtest-strategy-page-overview_.md). Here you can load the top strategy's parameters and make it the active strategy.

The top 20 are picked based on their final [Fitness Score](_documentation_backtest-parameterization-panel.md#NormalizingFitness) (in-sample), regardless of the criteria they used as [Fitness Functions](_documentation_backtest-parameterization-panel.md#FitnessFunctions). Such Fitness Score (in-sample) can be seen from the Divine Engine Results Tab:

!

If it's a standard backtest, the Fitness Score isn't listed anywhere; you can only guess based on the Fitness Functions criteria you set (on the Backtest Parameterization Panel) _before_ you pressed the ! button. Yes, you may need to ! to display that panel (and adjust the Fitness Functions), despite just doing a standard backtest.

!

Note, if you do another backtest, the result(s) may end up here thus replacing the previous crown holders; as the list is capped at 20 at all times. Now, let's discuss the various columns there:

* * **1.  Type** – This shows the type of backtest that the top strategy was created from.

!

It can be either:

*   ! : cloud Divine Engine (The Boss)
*   ! : local Divine Engine (on your PC)
*   ! : standard (manual) backtest.

* * **2.  Rank** – This shows the rank of each top strategy.

!

The strategy with the highest “Fitness (IS)” score has the top rank, and it goes down from there. By default, the whole 20 strategies are sorted top to bottom based on this Fitness (IS) Score.

* * **3.  Load Parameters** – These buttons load the parameters of the top strategies.

!

The top strategy's rules, filters, parameters, portfolios, and values (in short, anything on the [Rules Area](https://portfolioboss.wpenginepowered.com/wp-content/uploads/2021/05/gdg56ye5dg_00000_00000.png), including the [Backtest Parameterization Panel](_documentation_backtest-parameterization-panel_.md)) are loaded as the active strategy, very similar to [loading a top strategy](_documentation_backtest-results-tab.md#LoadParameters) from the Divine Engine Results Tab. And you can load a top strategy while the cloud backtest is still running.

Note, if your strategy is currently in [read-only mode](_documentation_strategy-panel-guide_.md#ReadOnly), you can still load any of the top strategies here, by confirming to override the read-only mode from the ensuing dialog:

!

Once done loading the top strategy (or even customizing the strategy further), you can restore the read-only mode by clicking “Restore read-only mode…” (on the Strategy Panel) or navigate away to another strategy.

!

* * **4.  Fitness IS/OOS** – These columns show the top strategies' final Fitness Score.

!

“Final” means the metrics score (those used as Fitness Functions, like CAGR, Max Drawdown, etc.) are aggregated & normalized into 1. These columns are for both the [in-sample](_documentation_backtest-panel-guide.md#insampleratio) and out-of-sample Fitness Score.

* * **5.  Metrics Score** – These columns show the _individual_ [metrics'](_documentation_metrics-panel-guide_.md) score of the top strategies.

!

By default, the metrics shown here are those Fitness Functions you listed on the Backtest Parameterization panel:

!

You can add other metrics' column with the “Manage Columns” dialog; click the button shown below:

!

Here you can search and select any metrics, be it their IS (in-sample), OOS (out-of-sample), or AS (all-sample) column:

!

Should you wish to hide any columns, simply deselect them from that dialog and press OK. Those metrics used as Fitness Functions are grayed out (in italics), as their columns must always be shown. If you wish to remove them, delete the Fitness Functions first, then deselect them from this dialog.

* * **6.  Test Date** – This shows the date & time the top strategies were born (backtested).

!

These are the local dates & time on your computer.

* * **7.  Select Backtest Source** – Clicking these buttons selects the [Backtest Item](_documentation_backtest-results-tab.md#TheBacktestItemsList) a top strategy belongs to.

!

If the top strategy comes from a standard (manual) backtest, its backtest record (item) will be selected on the [Manual Results Tab](_documentation_manual-results-tab_.md):

!

But if the top strategy resulted from a Divine Engine backtest, its Backtest Item will be selected (light-gray highlighted) on the [Divine Engine Results Tab](_documentation_backtest-results-tab_.md):

!

This is useful, for example, if you want to check the top strategy's siblings, and decide whether some of them have more convincing performance than the top strategy itself.

* * **8.  Delete Buttons** – These buttons delete top strategies.

!

Once removed, the top strategy exists neither in here nor in its respective Backtest Item; it's gone entirely from history, and another will take its place in the top 20. This is useful to delete garbage strategies; let's say the Fitness Functions used were nonsensical hence it doesn't deserve a top 20 due to inflated Fitness Score. Therefore your collection of top 20 strategies stay neat and easy to find.

* * *

#### Notes:

*   This tab does not exist on [multi-strategies](_documentation_multi-strategy_.md).

*   Remember, the top 20 strategies are picked based on their final [Fitness Score](_documentation_backtest-parameterization-panel.md#NormalizingFitness) (IS), regardless of the [Fitness Functions](_documentation_backtest-parameterization-panel.md#FitnessFunctions) used (between the various Backtest Items). Hence, for each and every backtest, you must craft Fitness Function(s) with sensible [threshold](_documentation_backtest-parameterization-panel.md#FitnessFunctionThreshold), so that one backtest doesn't trump the other backtests due to inflated Fitness Score (after factored into 1). For example, metrics such as “Avg. Position Gain” or “Avg. Trades Per Year” usually yield _very high_ Fitness Score if their _threshold_ is set low. Thus the top 20 will be skewed to favor such strategies, trumping other strategies with sensible Fitness Functions criteria. If such is the case, you can just delete them; this tab will automatically pick the next top strategies previously not included in the top 20.

*   Obviously, if you delete a Backtest Item or a top strategy (from either the [Divine Engine Results Tab](_documentation_backtest-results-tab_.md) or the [Manual Results Tab](_documentation_manual-results-tab_.md)), it will cease to be listed in this Overall Top Results Tab.

*   The whole list is sortable by each column (except the “Type” and “Test Date” columns). The metrics columns can also be moved left/right by dragging the column header; even after a restart, these columns stay where you put them. The sorting though, always defaults back to the “Rank” column.

[https://portfolioboss.com/wp-content/uploads/2022/12/t678r7res56sh.mp4](_wp-content_uploads_2022_12_t678r7res56sh.mp4.md)

[**Back to Top**](_documentation_overall-top-results-tab_.md#backtotop)

You have already reported this .

#### _documentation_pb-pattern-score-rule.md

> Source: https://portfolioboss.com/documentation/pb-pattern-score-rule
> Scraped: 3/1/2026, 2:09:21 AM

* * * [!](_wp-content_uploads_2019_10_PB-Pattern-Score-Rule-000.png.md)

This rule ranks your instruments based on their “PB Velocity” and/or “PB Pattern” scores.

“PB Velocity” is the instrument's percentage return during a specified period. That is, how much an instrument's price has gained during that period. The higher the gain, the higher the score.

[!](_wp-content_uploads_2019_10_1-Month-Velocity_00000.png.md)

“PB Pattern” is how close to a straight line the instrument's price history curve is (during the specified period). That is, the consistency of its price gain, whether it experienced low dips and high peaks. 

[!](_wp-content_uploads_2019_10_PB-Pattern-Examples_00000.png.md)

It is similar to the [R² metric](_documentation_metrics-panel-guide_.md#rsquared) found on the Metrics Panel, but applied on an instrument instead. The closer to a straight line, the higher the score.

* * **1.**  The first parameter defines whether you're looking at the lowest or highest of these scores.

[!](_wp-content_uploads_2019_10_PB-Pattern-Score-Rule-1st-Param.png.md)

* * **2.**  The second parameter defines the period to look for these scores.

[!](_wp-content_uploads_2019_10_PB-Pattern-Score-Rule-2nd-Param.png.md)

* * **3.**  The third parameter defines what kind of score you want to look for: PB Velocity only, PB Pattern only, or _both_ the PB Velocity and PB Pattern scores (which means the sum score is affected by both scores at once; for example, if just one score is low, the sum score will become lower). 

[!](_wp-content_uploads_2019_10_PB-Pattern-Score-Rule-3rd-Param.png.md)

Thus, if _both_ the PB Velocity and PB Pattern score highly, the instrument not only gained much, but at a consistent pace as well (not experiencing much price dips).

* * *

#### Notes

Regarding the “Offset” and “Weight” parameters, please refer to the guide about [Ranking Panel](_documentation_ranking-panel-guide_.md#offsetweight).

[**Back to Top**](_documentation_pb-pattern-score-rule_.md#backtotop)

Discount Applied Successfully!

Your savings have been added to the cart.

Close

You have already reported this .

Search

#### _documentation_perfect-stop-filter.md

> Source: https://portfolioboss.com/documentation/perfect-stop-filter
> Scraped: 3/1/2026, 2:08:49 AM

[!](_wp-content_uploads_2019_10_Perfect-Stop-Filter-Buy.png.md)

[!](_wp-content_uploads_2019_10_Perfect-Stop-Filter-Sell.png.md)

This filter uses the “Chandelier Exit” to consider an instrument as a buy or sell. It is good for spotting trend reversal, and is usually implemented as a Sell or Cover Filter (Stop Loss).

The Chandelier Exit is calculated by finding the _highest_ or _lowest price_ during a specified period, and then subtract/add such price by the multiplied [ATR](_documentation_n-atr-above-below-sma-filter_.md).

During an _uptrend_, the Chandelier Exit will _subtract_ the _highest_ price of the period by the multiplied ATR, thus the Chandelier indicator appears below the prices most of the time. If an instrument's closing-price goes below this indicator, it's a strong sign the trend will reverse toward a downtrend. Such condition is good for exiting a Long Position, or entering a [Short Position](_documentation_a-strategy-for-short-selling_.md).

[!](_wp-content_uploads_2019_10_Perfect-Stop-Filter-Indicator-Uptrend-000.png.md)

Now, during a _downtrend_, the Chandelier Exit will _add_ the _lowest price_ of the period by the multiplied ATR, thus the Chandelier indicator appears above the prices.

If an instrument's closing price goes above the indicator line, it's a good sign the trend will reverse toward an uptrend. Such condition is good for entering a Long Position, or exiting a Short Position.

[!](_wp-content_uploads_2019_10_Perfect-Stop-Filter-Indicator-Downtrend-000.png.md)

It's important to note: due to the way this filter is calculated, the indicator line _never goes down_ during an _uptrend_. Ditto it never goes up during a downtrend.

Such behavior means the filter is good as a stop-loss: The stop-loss line will go higher as the price goes higher, thus locking your profit from a downward movement (if the price hits the indicator, the strategy will exit the position).

It also applies for a Short Position: As the price goes lower, the stop-loss will also go lower; so, your profit is protected from an uptrend (whenever the price goes upward and hits the stop-loss, your Short Position will be exited).

* * **1.**  The first parameter defines whether you're looking for instruments that close “Above” or “Below” the Chandelier indicator.

[!](_wp-content_uploads_2019_10_Perfect-Stop-Filter-1st-Param.png.md)

* * **2.**  The second parameter defines the _period_ to look for the Highest/Lowest price, as well as the ATR duration.

[!](_wp-content_uploads_2019_10_Perfect-Stop-Filter-2nd-Param.png.md)

* * **3.**  The third parameter defines the ATR multiplier. Usually you want to input a value of up to 3 here. Which means if the closing-price breaks that 3x ATR, it's a strong indication of a trend change. 

[!](_wp-content_uploads_2019_10_Perfect-Stop-Filter-3rd-Param-1.png.md)

But if the portfolio's volatility is high, you may want to increase this value, so you don't get false signals due to the ups and downs of the price.

* * **4.**  The fourth parameter, “Dynamic Multiplier”, will _automatically change_ the ATR multiplier if the instrument's volatility changes.  

[!](_wp-content_uploads_2019_10_Perfect-Stop-Filter-4th-Param.png.md)

In other words, you don't set the ATR multiplier manually; the strategy will set it for you, depending on volatility.

* * *

#### Note:

In Portfolio Boss, the Chandelier Exit is called “Perfect Stop”, and if you use this filter, a “Perfect Stop” indicator is shown on the instrument's Price Chart.

[**Back to Top**](_documentation_perfect-stop-filter_.md#backtotop)

You have already reported this .

#### _documentation_portfolio-boss-forum.md

> Source: https://portfolioboss.com/documentation/portfolio-boss-forum
> Scraped: 3/1/2026, 2:07:44 AM

You can visit our forum by clicking the “Globe” button at the top-right corner of the interface. It will take you to [https://portfolioboss.com/forums/](_forums_.md) where you can ask questions about Portfolio Boss or just chill out with your fellow traders.

[!](_wp-content_uploads_2019_10_Globe-Button_00000.png.md)

Please note that some forum _groups_ are locked, depending on your Portfolio Boss license. Some licenses don't even have the “Globe” button (the forum is entirely locked). If you wish to upgrade your license, please contact our [Customer Support](mailto:support@portfolioboss.com) team.

You have already reported this .

#### _documentation_portfolio-instruments-panel-guide.md

> Source: https://portfolioboss.com/documentation/portfolio-instruments-panel-guide
> Scraped: 3/1/2026, 2:08:04 AM

!

As the name suggests, this panel shows the instruments contained within a _selected_ Portfolio (the one you selected from the [Portfolios Panel](_documentation_portfolios-panel-guide_.md) previously). Also, this panel allows you to add, remove, or suspend instruments from the Portfolio.

* * **1.**  **To add an instrument,** use the field “Type here to add a new instrument” at the top of this panel. Type the instrument's ticker symbol there and press enter; the instrument will be added to the list. 

[https://portfolioboss.com/wp-content/uploads/2021/08/78rd67se56sw.mp4](_wp-content_uploads_2021_08_78rd67se56sw.mp4.md)

You can type anything here, either partial or complete description of an instrument. For example you can type its _symbol_ (like AMD) or the _full name_ (Advanced Micro Devices); a dropdown menu will then appear letting you choose the exact instrument that you want. If you're confident the symbol you entered is correct, simply press enter without selecting from the dropdown menu.

!

This dropdown menu shows you the detail of each instrument. From left to right, each column on _that dropdown_ is as follows:

*   The first column shows the symbol of the instrument.
*   The second column shows the full name of the instrument (e.g company name).
*   The third column shows the period that the instrument has been actively traded.
*   The fourth column shows the market/exchange that the instrument is traded.
*   The fifth column shows the _asset-class_ of the instrument (Stock, ADR, Bonds, ETF, Index, etc),
*   and the sixth column shows the data source for that instrument.

Note, if you typed a non-existent instrument, such as ABBA, and pressed enter, a warning dialog will tell you it's not a valid symbol (PB may “hang” a little while processing whether it's a valid symbol).

!

Also, you can't add instruments to a Dynamic Portfolio. The text field shows “Dynamic portfolios can not be modified”.

!

Now, to remove the instrument from the Portfolio, select it and press the keyboard Delete button (a delete confirmation dialog shows up).

!

* * **2.**  **The Symbol column** on _this_ _panel_ shows you the symbol (ticker) for the instruments.

!

* * **3.**  **The Description column** shows the full name of those instruments.

!

* * **4.**  **The Exchange column** shows the market/exchange that the instruments are traded on.

!

* * **5.**  **The Type column** shows the asset-class of the instruments, either Stock, Bond, ADR, ETF, Index, etc.

!

If you don't see this column, simply drag the scrollbar at the bottom of this panel. Or drag the right-edge of the panel to enlarge it.

* * **6.**  **The Delisted column** shows whether an instrument has been _delisted_ (in the form of a checkmark). 

!

You can also tell if an instrument is delisted by its gray inactive appearance on this list. For example a company that went bankrupt (or acquired by another company) will have its symbol delisted; in short, the instrument is no longer traded. 

* * **7.**  **The First Date column** shows the first date that the price data became available. Usually, that also means the date an instrument was first traded on an exchange. 

!

* * **8.**  **The Latest Date column** shows the date of the _latest price data_. Usually, if the date is _far off_ in the past, it means the instrument has been delisted thus no new price data will be downloaded. 

!

Keep in mind that price data won't be available during weekends and holidays (non-trading days), so this date may be off by a few days. If you're trading on a foreign exchange, their holidays may be different than yours.

* * **9.**  **Date Added:** If you've been using this Portfolio for some time and _then_ _add_ a new instrument, it's best to use this parameter to assign the date you added that instrument. That way, no Positions will be entered before that date, and your backtest result will be more accurate. 

!

To do so, click on the little “Calendar” icon ! . A calendar dialog pops up where you can enter the date. This feature can also be used to _mark_ an instrument to be _added later_ (let's say it's going public next week).

Note, to remove the date, simply select (block) the date _text_ and press Delete on your keyboard.

* * **10.**  **Date Removed:** If you've been using this Portfolio for some time _and then_ decided to discard a certain instrument, it's best to mark that instrument with this “Date Removed” parameter. That way, PB will no longer enter its Positions, starting from that date. 

!

You must not _remove_ that instrument from the Portfolio, as it will affect the backtest result and the accuracy of your strategy. This parameter can also be used to _mark_ an instrument that you want to discard at a _later time_.

* * **11.**  **The Data Source column** shows where the price data is sourced from. It may show Csi (Commodity Systems Inc.) or Yahoo.

!

* * **12.**  **The Suspended checkmark:** If you have _insider's information_ that an instrument will no longer be traded on the exchanges (company bankruptcy, acquisition, etc.) you can mark it as “Suspended” instead of deleting it from the list. 

!

That way, PB _will_ no longer enter Positions for that instrument, and your backtest will stay accurate (because the instrument's price history is kept).

Ideally, you don't even need to mark an instrument as “Suspended”, because eventually it will be marked as “Delisted” by the exchanges (see the “Delisted” column above). But being marked as “Delisted” takes time, as all the bureaucratic works need to be finished. So instead of waiting, you can mark it as “Suspended”.

Note, when you mark “Suspended” an instrument, it is suspended in all Portfolios where it resides. If you don't want this to happen, use the “Date Removed” function previously explained.

* * **13.  Show Delisted Instruments:** This toggle is located at the top-right corner of the panel. Toggling it ON lets delisted instruments be shown in the instrument list (along with non-delisted instruments).

!

As you remember, delisted instruments are those with the “Delisted” checkmark ticked (and their appearance grayed out). Toggling it OFF shows only the instruments still actively traded in the exchanges. This is just visual aid, as the delisted instruments are still part of the Portfolio.

* * **14.**  **Show Errors Only:** This toggle is located at the top of the panel, and is only visible if a _selected_ Portfolio contains error. Toggling this ON will only list the _instrument_ that contains error. 

!

Such instrument also has its name marked by a red circle; if you hover your mouse over it, the error detail shows up. Such error may happen if the price data are unavailable from CSI and Yahoo, or if the “Date Added” and “Date Removed” don't make sense.

Now, to show all the instruments again, simply press the same toggle.

* * **15.**  **The Trashbin button** lets you _remove_ the instrument from the Portfolio. 

!

Usually you want to do this when _you're still constructing_ the Portfolio. But if the Portfolio has been used for some time, it's best to remove an instrument with the “Date Removed” parameter explained earlier, so your backtest will stay accurate.

You can also delete an instrument by selecting it and press the keyboard Delete button.

* * *

#### Notes:

*   Dynamic Portfolios can't be manipulated, either adding or removing their instruments, or customizing the “Date Added” and “Date Removed” parameters. But you can still mark their instruments as “Suspended”, just in case you know they'll be delisted in the near future.

*   Even if an instrument is not used in any strategy, clicking it here will automatically download the price data.

*   The instrument list can be sorted. Simply click a column's header to sort based on that column (only the “Symbol” column can't sort the list):

[https://portfolioboss.com/wp-content/uploads/2021/08/uki6r7dhs.mp4](_wp-content_uploads_2021_08_uki6r7dhs.mp4.md)

[**Back to Top**](_documentation_portfolio-instruments-panel-guide_.md#backtotop)

You have already reported this .

#### _documentation_portfolio-management-page-overview-2.md

> Source: https://portfolioboss.com/documentation/portfolio-management-page-overview-2
> Scraped: 3/1/2026, 2:08:05 AM

![Portfolio Boss - Portfolio Page Regions Defined](https://portfolioboss.com/wp-content/uploads/2024/04/Portfolio-Boss-Portfolio-Page-Regions-3-1024x555.jpg)

This page allows you to view and manage various Portfolios (baskets of instruments). Open this page by clicking the “Portfolio Management” button ! at the sidebar.

Each Portfolio contains financial instruments (stocks, bonds, ETFs) from specific industry sectors, market indexes, countries/regions, or any kind of grouping. The strategy will pick from these baskets those instruments that are potentially profitable as Positions. Most Portfolios bundled in the software are crafted by the Portfolio Boss team; you don't have to research and pick financial instruments tediously one by one. But if you wish so, you can [create your own Portfolio](_documentation_portfolios-panel-guide_.md#createnewportfolio) in this page.

There are four panels in this page:

1\. [Portfolios Panel](_documentation_portfolios-panel-guide_.md) (the list of Portfolios).

2\. [Instruments Panel](_documentation_portfolio-instruments-panel-guide_.md) (shows instruments within a Portfolio).

3\. [Instrument Chart Panel](_documentation_instrument-chart-panel-guide_.md) (shows instrument's historic price chart).

4\. [Sync Details/Search Results Panel](_documentation_sync-details-search-results-panel_.md) (hidden by default).

We will explain them in the following pages.

You have already reported this .

#### _documentation_portfolio-management-page-overview.md

> Source: https://portfolioboss.com/documentation/portfolio-management-page-overview
> Scraped: 3/1/2026, 2:07:57 AM

!

This page allows you to view and manage various Portfolios (baskets of instruments). Open this page by clicking the “Portfolio Management” button ! at the sidebar.

Each Portfolio contains financial instruments (stocks, ETFs, etc.) from specific industry sectors, market indexes, countries/regions, or any kind of grouping. The strategy will pick from these baskets those instruments that are potentially profitable as Positions. Most Portfolios bundled in the software are crafted by the Portfolio Boss team; you don't have to research and pick financial instruments tediously one by one. But if you wish so, you can [create your own Portfolio](_documentation_portfolios-panel-guide_.md#createnewportfolio) in this page.

There are four panels in this page:

1\. [Portfolios Panel](_documentation_portfolios-panel-guide_.md) (the list of Portfolios).

2\. [Instruments Panel](_documentation_portfolio-instruments-panel-guide_.md) (shows instruments within a Portfolio).

3\. [Instrument Chart Panel](_documentation_instrument-chart-panel-guide_.md) (shows instrument's historic price chart).

4\. [Sync Details/Search Results Panel](_documentation_sync-details-search-results-panel_.md) (hidden by default).

We will explain them in the following pages.

You have already reported this .

#### _documentation_portfolio-position-limit-filter.md

> Source: https://portfolioboss.com/documentation/portfolio-position-limit-filter
> Scraped: 3/1/2026, 2:08:51 AM

* * * [!](_wp-content_uploads_2019_10_Portfolio-Position-Limit-Filter-Buy.png.md)

This filter only exists as a [Buy Filter](_documentation_buy-filters-panel-guide_.md).
It allows you to _limit_ the number of positions originating from the _same_ Portfolio.

So for example, your strategy contains various Portfolios, each representing a different sector (sectors like financial, industry, technology, commodity, etc.); if you don't want to enter so many Positions within the _same_ sector, you can limit the number of Positions using this filter.

[!](_wp-content_uploads_2019_10_Sector-Limit_00001_00000.png.md)

This is a good way to diversify your Positions, thus reducing risk.

This filter has one parameter only, which defines the _maximum_ _amount_ of Position from within the _same_ Portfolio. For example, with a value of 5 here you can only enter 5 Positions (5 different instruments) from within the same Portfolio at any given time.

If 5 Positions have been entered from that Portfolio, then no more instruments from that Portfolio will be considered as a buy, until any of the previous 5 Positions have been exited (when they hit [Switch Day](_documentation_system-settings-panel-guide_.md#monthlyswitch) or [Sell Filters](_documentation_sell-filters-panel-guide_.md), for example).

[!](_wp-content_uploads_2019_10_Portfolio-Position-Limit-Filter-Param.png.md)

Now, there's a warning on this parameter if you input a value equal to (or greater than) the [Total Positions to Hold](_documentation_system-settings-panel-guide_.md#totalpositions):

!

Obviously, that's because the theoretical maximum from each Portfolio can't exceed the total number of Positions the strategy holds at any given time.

* * *

#### Note:

If this is your first time using the Strategy, obviously no Positions have been entered. But the limited Positions have been _reserved_ for instruments that _rank highly_ from that Portfolio (based on the [Ranking Rules](_documentation_ranking-panel-guide_.md)), so essentially it’s a race toward the top rank for the instruments in that Portfolio. 

Discount Applied Successfully!

Your savings have been added to the cart.

Close

You have already reported this .

Search

#### _documentation_portfolio-threshold-filter.md

> Source: https://portfolioboss.com/documentation/portfolio-threshold-filter
> Scraped: 3/1/2026, 2:08:52 AM

[!](_wp-content_uploads_2019_10_Portfolio-Threshold-Filter-Buy.png.md)

This filter exists only as a [Buy Filter](_documentation_buy-filters-panel-guide_.md). It looks at a [Portfolio](_documentation_instruments-panel-guide_.md), and if _at least_ N percent of the Portfolio is accepted by the Buy Filters (other than this Buy Filter we're talking about), as long as they don't hit the [Sell Filters](_documentation_sell-filters-panel-guide_.md) as well, then the Portfolio is allowed to be traded.

In other words, this filter sets the _minimum_ _number_ of instruments that a Portfolio _must be able_ to trade.

For example, the minimum amount is set to 50%: if a Portfolio is only able to pass 30% of its instruments through the Buy Filters, then that Portfolio will not be traded at all.

But note, if a Portfolio passes this minimum amount, and then a few days later some of its instruments hit the Sell Filters thus the Portfolio is trading at less than the minimum percentage, the existing Positions will still be maintained.

[!](_wp-content_uploads_2019_10_Portfolio-Threshold-Not-Pass_00000.png.md)

Also note that despite passing the minimum percentage, not all of those instruments (that passed the Buy Filters) will be entered as Positions.

The strategy will only allow x amount of Positions at any given time (set through the parameter [“Total Positions to Hold”](_documentation_system-settings-panel-guide_.md#totalpositions)) after they have been ranked by the [Ranking Rules](_documentation_ranking-panel-guide_.md) (only _top x_ instruments will be entered as Positions).

[!](_wp-content_uploads_2019_10_Portfolio-Threshold-Pass_00000.png.md)

The purpose of this filter is to see whether a Portfolio is profitable to be traded before actually committing to it. Let's say the market is at the end of economic recession, and you want to know whether the Technology Sector is profitable to be traded.

If _more than_ 50% of the Technology Portfolio's instruments passed the Buy Filters, then you can be confident this sector is profitable during the market cycle. Because if just one or two instruments passed, it could be just a _fluke_ for the whole Portfolio.

Note that _all Portfolios_ within the strategy will be checked whether they pass this percentage amount.

* * **1.**  The first parameter defines whether the Portfolio must pass “More than” or “Less than” the threshold percentage. Generally, you always want to set this to “More than”. 

[!](_wp-content_uploads_2019_10_Portfolio-Threshold-Filter-1st-Param.png.md)

“Less than” can be useful for example if you want to trade a Portfolio that is highly risky, but only a small percentage of it, as part of diversification.

* * **2.**  The second parameter defines the percentage threshold that these Portfolios must pass.

[!](_wp-content_uploads_2019_10_Portfolio-Threshold-Filter-2nd-Param.png.md)

You have already reported this .

#### _documentation_portfolios-panel-guide.md

> Source: https://portfolioboss.com/documentation/portfolios-panel-guide
> Scraped: 3/1/2026, 2:08:07 AM

!

This panel lists all Portfolios you have; the ones bundled with the software or those Portfolios you created yourself.

* * **1.**  **The “Name” column** shows each Portfolio's name. Looking at the names, you can tell if a Portfolio contains a certain industry sector (financial, technology, commodities, etc.) or if it's trading certain instruments such as stocks, ADRs (foreign stocks), ETFs, etc. 

!

You can also find _index_ Portfolios, which contain the exact instruments as the real indexes they represent (past and present, thus they may include delisted symbols too). An index Portfolio usually has a counterpart called “Historical Deletion” Portfolio. This contains instruments that were ever dropped out of the index.

!

If you use an index Portfolio, it's recommended that you use its counterpart as well. For example, instead of just using the “Nasdaq 100” as part of the strategy, use the “Nasdaq 100 – Historical Deletions” too. It allows for a more objective selection, without overfitting to the present.

!

Now, you can rename these Portfolios by double-clicking any of their names. Or hover your mouse over a name, and click the pencil icon ! that appears. Once renamed, press Enter on your keyboard, or click the the checkmark icon ! .

[https://portfolioboss.com/wp-content/uploads/2021/07/t67d7ndje6swe.mp4](_wp-content_uploads_2021_07_t67d7ndje6swe.mp4.md)

Only “User defined” Portfolios can be renamed, not the “Dynamic” ones.

* * **2.**  **The “Data Source” column** indicates the source of the instruments' price data. 

!

Usually we obtain data from CSI (Commodity Systems Inc.) or Yahoo Finance (deprecated).

* * **3.**  **The “Type” column** indicates whether the Portfolio is “User Defined” or “Dynamic”. A “User Defined” Portfolio is the one that you manage yourself; you can add or remove instruments as you wish. 

!

A “Dynamic” Portfolio is the one automatically managed by Portfolio Boss; we use reliable 3rd party data to manage these Portfolios. The idea is you don't have manually update the Portfolios as the market changes (companies delisted, new companies IPO'd, new entry to an index, etc.). Note, you _can't_ customize “Dynamic” Portfolios.

* * **4.**  **The “Listed” column** shows the number of instruments that are actively traded; that is, instruments that are still listed on the exchanges.

!

* * **5.**  **The “Delisted” column** shows the number of instruments that are no longer listed on the exchanges; either the company went bankrupt, was merged, or it no longer meets the exchange's requirements. 

!

Keep in mind, even though the companies are delisted, Portfolio Boss keeps their historic price data for a more accurate backtest result (past positions). Obviously they won't be traded in the future once delisted.

* * **6.**  **The toggle “Show Errors Only”:** this is located at the top-right corner of the panel. Toggling this ON will only list Portfolios that _contain error_; such Portfolios are labelled with a warning circle ! .

!

Hovering the cursor over the warning details the actual error. For example, the Portfolio contains instruments whose price data are unavailable from CSI and Yahoo, or if its “date removed” is earlier than the “date added” (explained later).

To revert back to the full list of Portfolios, click to toggle it OFF.

**Note:**

The Portfolio list can be sorted by each column. Just click a column's header to sort the list based on that column.

[https://portfolioboss.com/wp-content/uploads/2021/07/789t7ehqw.mp4](_wp-content_uploads_2021_07_789t7ehqw.mp4.md)

* * *

#### Create and Manage the Portfolios

**7.**  **To create a Portfolio,** click the “New” button at the top-left corner of the page. 

[https://portfolioboss.com/wp-content/uploads/2021/07/ftyre6aha.mp4](_wp-content_uploads_2021_07_ftyre6aha.mp4.md)

The “Add Portfolio” dialog appears where you can type the name of the Portfolio. Press “OK”, and you're immediately taken to the Portfolio Instruments Panel to add the instruments. Please refer to the [Portfolio Instruments Panel](_documentation_portfolio-instruments-panel-guide_.md) help, to add or remove instruments from a Portfolio; essentially it's just typing the symbol and press enter.

* * **8.**  **To delete a Portfolio,** you can't just press the _keyboard_ “Delete” button on a selected Portfolio. You must actually tick the checkbox (at the left of the Portfolio's name), and click the “Delete” button at the top of the page. 

[https://portfolioboss.com/wp-content/uploads/2021/07/gyfu4e6es.mp4](_wp-content_uploads_2021_07_gyfu4e6es.mp4.md)

You can also tick multiple Portfolios to be deleted at once (“Dynamic” Portfolios can't be deleted).

Note, if you delete a Portfolio used by a Strategy, a warning dialogue appears asking whether you really want to delete it, thus the Strategy no longer contains that Portfolio. 

[!](_wp-content_uploads_2019_09_Confirm-Delete.png.md)

* * **9.**  **To copy a Portfolio,** first tick it then press the “Copy” button at the top of this page. The duplicate has the suffix “- Copy” and it's a distinct Portfolio whose contents you can manipulate differently from the original. 

[https://portfolioboss.com/wp-content/uploads/2021/08/89dr6sw5haw.mp4](_wp-content_uploads_2021_08_89dr6sw5haw.mp4.md)

Note, if you copy a “Dynamic” Portfolio there's a confirmation dialog. The duplicate becomes a “User Defined” Portfolio (a.k.a. static), thus retaining the original contents but will not be _automatically_ updated.

* * **10.**  **To “Merge” two or more Portfolios,** tick the Portfolios and click the “Merge” button. They'll become _one single_ Portfolio (the originals are gone) that uses one of the Portfolios' name. 

[https://portfolioboss.com/wp-content/uploads/2021/08/67846whq.mp4](_wp-content_uploads_2021_08_67846whq.mp4.md)

Their instruments are _combined_ in that single Portfolio. If the _exact same_ instruments are used between these Portfolios, only one instrument will appear on the merged Portfolio.

* * **11.**  **To “Backup” a Portfolio into a file,** tick the Portfolio and click the “Backup” button. A save-destination dialog appears, defaulting to “My Document” folder at:

`%USERPROFILE%\Documents\PortfolioBoss\Portfolios`

then save the .EBTP file (the P stands for Portfolio). 

[https://portfolioboss.com/wp-content/uploads/2021/08/78eshw5hnq.mp4](_wp-content_uploads_2021_08_78eshw5hnq.mp4.md)

In case of multiple selected Portfolios, they will be contained within a _single_ EBTP file. This file not only acts as a back up, but you can send it to other PB users so they can use the Portfolios.

* * **12.  To “Restore” a.k.a. import a Portfolio** (provided you have the EBTP file), simply click the “Restore” button and navigate to where the EBTP file is located; then click Open. 

[https://portfolioboss.com/wp-content/uploads/2021/08/t67er7wkwm8.mp4](_wp-content_uploads_2021_08_t67er7wkwm8.mp4.md)

You can also double click the EBTP file _directly_ from Windows Explorer (without using PB), and the Portfolio will be added to the Portfolio list.

Note that the EBTP _file_ _name_ does not necessarily become the Portfolio name on the list, as the Portfolio uses the name you created internally in PB.

* * *

#### Notes:

*   If the imported Portfolio already exists inside of PB, then nothing happens.
*   You can't load multiple .EBTP files at once.
*   If the instruments' price data are being downloaded, the Portfolios will show a loading column. And only Portfolios that are used in strategies will have their historic price data downloaded, for efficiency reasons.

!

*   You may want to check the [**Portfolio Boss Status Page**](https://status.portfolioboss.com/) if there are problems with the historical data download (or synchronization of Dynamic Portfolios):

!

**[Back to Top](_documentation_portfolios-panel-guide_.md#backtotop)**

You have already reported this .

#### _documentation_position-duration-filter.md

> Source: https://portfolioboss.com/documentation/position-duration-filter
> Scraped: 3/1/2026, 2:08:55 AM

!

This filter only exists as a Sell Filter.
It will automatically _exit_ any Positions that have been held for a certain period.

This filter is preferably used when the strategy is set to [“Continuously Switch Position”](_documentation_system-settings-panel-guide_.md#systemparameter). The idea is that you don't want to hold on to current positions for too long and miss out on better positions out there (based on the Ranking Rules).

So in essence, applying this filter gives you the best of both worlds between “Continuously Switch Positions” and “Periodically Switch Positions”.

!

This filter has only one parameter, which defines the _maximum_ duration a Position can be held.

!

* * *

#### Note:

You may use this filter on a Periodically Switching strategy. Let's say to avoid an instrument getting selected over and over again (as a Position) through many switch days.

You have already reported this .

#### _documentation_positions-panel-guide.md

> Source: https://portfolioboss.com/documentation/positions-panel-guide
> Scraped: 3/1/2026, 2:08:13 AM

!

This tab shows you the latest Positions held by the strategy (i.e. today's Positions, or any date set with the [“Date to”](_documentation_backtest-panel-guide_.md#datetoparam) property of the Backtest Panel). You must backtest the strategy first (with the standard backtest ! ) before this tab is populated. Here you'll see the instruments you've been holding, their holding duration, their gains/losses, etc. A text at the top tells you the date that these Positions belong to:

!

This tab is located at the [Reports Area](https://portfolioboss.wpenginepowered.com/wp-content/uploads/2021/05/gdg56ye5dg_00000_00000.png) of the “Backtest Strategy” page.

* * **1.**  **Rank:** this column shows the Positions' rank, which is based on the [Ranking Rules](_documentation_ranking-panel-guide_.md).

!

Keep in mind these rankings are taken when the Positions are initiated (entered), and they don't update. So it could be that these instruments no longer rank highly based on their latest data. If you want to see updated ranking (for those instruments that passed the [Buy/](_documentation_buy-filters-panel-guide_.md)[Short Filters](_documentation_a-strategy-for-short-selling_.md)) look at the section [“Top Ranking Instruments”](_documentation_trade-signals-panel-guide_.md#toprankingsection) on the Trade Signals Tab.

* * **2.**  **Symbol:** this column shows the ticker symbol of each Position. 

!

Note that Cash–or Cash Equivalent Positions (e.g. SHY)–can be grouped into a single symbol with a number-suffix inside the parentheses, indicating the number of old Positions it replaced.

You can click a symbol to show its price chart (on the [Instrument Tab](_documentation_instrument-tab_.md)), so you may see its price-action since it was entered (the Buy action/arrow):

!

You can also hover your cursor over a symbol to see a tooltip-description for that Position:

!

From top to bottom, the tooltip describes:

*   the full name of the company (or fund),
*   the [portfolios](_documentation_portfolios-panel-guide_.md) that contain this symbol,
*   the asset class of this symbol (stock, ETF, [ADR](https://www.investopedia.com/terms/a/adr.asp), etc.),
*   the market (exchange) it's traded at,
*   the period it's been traded,
*   its historical-data provider,
*   its gain/loss for today i.e. the change in the instrument's _closing price_ today vs. yesterday.
*   its weight (percentage of account size occupied by this Position),
*   its Position type (either long or short Position),
*   the number of days it's been held,
*   the old Position(s) that it replaced–this only appears for a Cash Equivalent Position (e.g. SHY).

!

As for the Cash Position, the tooltip tells you _whether_ it's a replacement for sold Positions (if your strategy uses [Cash _instead of_ Cash Equivalent](_documentation_system-settings-panel-guide_.md#positionreplacements)):

!

or if it's a placeholder for when instruments don't pass the Buy Filters (thus they're not ranked, and can't be entered):

!

If the strategy uses [Limit Orders](_documentation_system-settings-panel-guide_.md#BuyOrderType), Cash will be used as a placeholder for when a Limit Buy Signal (order) failed to be filled at the next trading day:

!

That Cash Position will continue as long as the Limit Buy Signal remains unfilled (and such signal may jump toward another top-ranked instrument). If it's finally filled, the Cash Position will be replaced with the new stock/ETF Position.

Cash will also be used when a Position is sold with the Limit Sell Signal:

!

This Cash Position stays for _one day after_ such signal, so that PB can determine (after the market closes tomorrow, and all EOD data downloaded) whether its limit price is met. Then at the next day (2 days after the signal), PB will replace such Cash Position with the new stock/ETF Position. If the Limit Sell Signal failed to get filled, there's no Cash Position and the old Position remains; PB will continue to generate the Limit Sell Signal as long as the Position still triggers the [Limit Sell Filter](_documentation_system-settings-panel-guide_.md#SellLimitFilter).

Now, some symbols have a number-suffix enclosed within the square brackets:

!

This indicates a currently delisted instrument, with the number telling you how many times it's been delisted (companies can be delisted from an exchange and then relisted, e.g. due to going private and then public again, or if its market cap goes below the exchange's requirement).

* * **3.**  **Gain:** this column displays the gain/loss of each Position since it's entered. It's stated in percentage of the initial value when the Position was entered.

!

For example, if a Position was initially given $10,000 and then experienced profits totaling $3,000 and losses totaling $1,000, its total gain would be $2,000, or 20% of the initial value. In technical terms, gain is simply the _difference_ _between_ the price you entered the Position with (usually the day's opening price) _and_ the closing price of the instrument _today_. The resulting dollar value is then divided by that entry price, and multiplied by 100, yielding this percentage.

!

Now, if the Position was entered with a Limit Order, whichever is the _better price_ (whether the _limit price_, or the _opening price_) becomes the entry price. “Better” means the lower price between those two (if you're buying), and if you're selling (i.e. shorting) it's the higher price.

!

Now, when the [Slippage Option](_documentation_system-settings-panel-guide_.md#slippagesmioptions) is applied (from the System Settings Panel), the gain/loss calculation is a bit different. Essentially, slippage-simulation will occur at each trade (each Buy/Short and Sell/Cover). For example if you are buying, your entry price will be _higher_ (more expensive) than the opening price. How much higher? Let's say you put the Slippage Option at 10%, and the day the Position was entered the instrument traded at a high of $50 and a low of $40, which means a $10 movement-range for that day. A 10% slippage gives you about $10 × 10%, i.e. $1 actual slippage; therefore your entry price is $1 higher than the opening price of that day. Today's closing price (as the _end price_) won't be influenced by the slippage. Slippage only affects actual trades.

Note, if the trades are executed with the limit prices (instead of the opening prices), slippage won't be applied. In summary, the Slippage Option reduces your gains and amplifies your losses (sounds bad, but that's how real-life trades actually work, so you're not deluded with utopian statistics).

!

Now, Cash Positions, their gain is always 0%, no matter how long you hold them. In reality, _some_ brokers pay interests for your idle cash, especially during high interest-rate by the Fed. Therefore, do understand that the gains/losses you see here are just approximations (though PB tries to make them as accurate as possible). You may need to check your brokerage-account balance/report to see the real, _de facto_ gains/losses (including commissions, slippage, taxes, interests, dividends, account maintenance fee, ETF expense ratio, and all those little things).

* * **4.**  **Days:** this column shows the number of days each Position has been held.

!

This duration includes the day the Position was entered up to the latest backtest date (usually today).

!

Of course it counts only the trading days, without holidays or weekends.

* * **5.**  **Description:** this column displays the Positions' description.

!

Usually, it shows the full name of the company (or fund). When it comes to a Cash Position, its description varies depending on what it represents (as already described earlier about the Cash symbol's tooltip).

But sometimes the Cash description is a little confusing (ditto its tooltip description): sometimes it does not correctly tell you what it represents, other times it's unintelligible, especially if it's the result of multiple replacements (e.g. Limit Sell placeholder and replacement for liquidated Positions).

!

So don't put too much stock into it (no pun intended).

* * **6.**  **Weight:** this column shows the weight of each Position. Weight is the percentage of your account size occupied by a Position.

!

In the beginning, all Positions have the same weight. Let's say the strategy [holds 10 Positions](_documentation_system-settings-panel-guide_.md#totalpositions) at any given time, then each Position holds 10% weight. If you have $100,000 for this strategy, $10,000 would be spent to enter each Position. The moment they're entered, they're subject to the market forces: some Positions gained more than the others, while some Positions lost. 

!

Naturally, those that gained now occupy _more weight_ than those that lost. Still, all those weights add up to 100%, i.e. _the whole_ of your account size (which may have grown or shrunk by now).

Now if some Positions are sold, their liquidated value will be combined (their weights combined) and then distributed _equally_ to enter the same number of _new_ Positions. Let's say 3 Positions are sold, their combined liquidation value will be distributed equally to enter 3 new Positions:

!

If it's a [periodically-switching strategy](_documentation_system-settings-panel-guide_.md#systemparameter), these new Positions are usually its Cash Equivalent (or simply Cash, i.e. nothing bought):

!

When it's a [switch-day](_documentation_system-settings-panel-guide_.md#monthlyswitch), _all_ Positions will be liquidated (including the Cash Equivalent Positions), and all their weights combined (i.e. 100% of your current account size) will be distributed equally to enter the brand new 10 Positions (thus 10% each again):

!

Sometimes at switch day, not all Positions will be replaced, as some still pass the Buy Filters and rank highly (higher than the new replacements). If that's the case (i.e. some old Positions remain), obviously they don't receive any part of the combined liquidated-funds (from the sold Positions).

There are also some rare cases where the Cash Equivalent Positions won't be replaced even at switch day. Usually it's because none of the instruments passed the Buy Filters; or _very few_ of them did, hence [the top ranking instruments](_documentation_trade-signals-panel-guide_.md#toprankingsection) are _all_ _used up_ (as seen on the Trade Signals Tab), either as replacements or as already-existing Positions, leaving the remaining slots to stay with the Cash Equivalent.

**Note:**

When there are [trade signals](_documentation_trade-signals-panel-guide_.md), the number of shares to be traded is automatically calculated with the [Trade Plan Calculator](_documentation_trade-plan-calculator_.md) based on these weights (though they may not match these weights exactly, due to the price-per-share causing imperfect division).

* * **7.**  **Positions sold at the open:** this section shows the Positions _exited_ today (or the latest backtest date). It only appears if there were indeed Positions exited today.

!

So these are _theoretically_ not part of today's Positions; their exit signals were given on the previous trading day, and were executed today. If it's a [short strategy](_documentation_a-strategy-for-short-selling_.md), this section says “Positions covered at the open”.

!

Note, despite the name “sold/covered _at_ _the open_“, some Positions might be exited any time during today's trading session. These are Positions exited with the Limit Orders (Limit Sell/Cover Signals), because Portfolio Boss can't know whether their limit prices are met except after the market's closed and EOD (End of Day) data are all downloaded.

The columns for this section are generally similar to what we've discussed so far, but with a few twists:

!

From left to right:

*   **Rank:** similar to what's discussed before.
*   **Symbol:** the tooltip's “Gain” info is calculated from the instrument's closing price yesterday versus the price it was sold at today (opening price or limit price). And the “Position Weight” is always at 0.0% (as it's already exited, it occupies $0 of your account):

!

*   **Gain:** the calculation is similar to what we discussed earlier (i.e. percentage change between the entry price and the _end price_), but the end price here is not today's closing price; instead it's the price the Position was _exited at_ (today's opening price). In other words, the percentage you see here is the gain/loss of that Position from entry _to exit_. If the strategy uses Limit Sell Orders, the end (exit) price is whichever the _higher_ price between the opening price and the limit price (or if it's a Cover Order, whichever is the _lower_ price between those two). If [Slippage Option](_documentation_system-settings-panel-guide_.md#slippagesmioptions) is used, the end price is today's _opening_ price _minus_ the dollar slippage (if Sell), or _plus_ the dollar slippage (if Cover). Slippage is never applied on limit prices.
*   **Days:** this duration _includes_ the day the Position was entered and the day it was exited.
*   **Description:** similar to what's discussed earlier about this column.
*   **Weight:** here is the Position's weight when it was exited (i.e. based on its total gain from entry to exit, as shown on the “Gain” column here we just described).

* * *

#### Notes:

*   The Positions Tab for a multi-strategy is slightly different from what's shown here. Read about the multi-strategy in action [**here**](_documentation_multi-strategy_.md#SSinAction).
*   The list here is sortable by clicking each column's header (except the “Symbol” column). You can also move each column to the left or right by dragging its header.

[https://portfolioboss.com/wp-content/uploads/2022/12/drtsd5wvgea4g.mp4](_wp-content_uploads_2022_12_drtsd5wvgea4g.mp4.md)

[**Back to Top**](_documentation_positions-panel-guide_.md#backtotop)

You have already reported this .

#### _documentation_price-range-filter.md

> Source: https://portfolioboss.com/documentation/price-range-filter
> Scraped: 3/1/2026, 2:08:56 AM

[!](_wp-content_uploads_2019_10_Price-Range-Filter-Buy.png.md)

This filter is only available as a Buy Filter.
It uses a certain _price_ as a threshold; so if an instrument's _closing price_ is above or below that threshold price, then the instrument will be bought (or sold).

This is a very simple filter to _exclude_ instruments that don't meet a certain price. For example if you don't want to trade “penny” stocks, since they usually have small dollar liquidity thus harder to make regular trades (incurring more slippage), or they may signify bad company reputation, or because their volatility is quite extreme.

Alternatively, you can use this filter to find those penny stocks since you're just beginning to trade and have a smaller account, for example.

Keep in mind, this filter can't be applied if your strategy contains only one instrument as its Portfolio (the filter is grayed out and you can't add it to your strategy). This applies to both Sell and Buy filters.

[!](_wp-content_uploads_2020_04_Portfolio-1-Instrument.png.md)

[!](_wp-content_uploads_2020_04_Price-Range-Filter-Restricted.png.md)

* * **1.**  The first parameter defines whether the instrument must be “Greater than” or “Less than” a certain price to be considered as a buy/sell. 

[!](_wp-content_uploads_2019_10_Price-Range-Filter-1st-Param.png.md)

You can also define whether the instrument must be “Between” (within) the minimum and maximum prices that you set, or “Not between” (outside) the maximum and minimum prices (in other words, you're looking at instruments that have very low or very high prices).

[!](_wp-content_uploads_2019_10_Price-Range-Filter-1nd-Param-B.png.md)

* * **2.**  The second parameter defines the threshold price that you want (in dollar value). Now, if on the previous parameter you set either “Between” or “Not between”, you can define the minimum and maximum prices on this second and third parameters that show up.

[!](_wp-content_uploads_2019_10_Price-Range-Filter-2nd-3rd-Param.png.md)

* * *

#### Note:

The price used here is the “real” closing price of the instrument, as opposed to the “adjusted” closing price (refer to [this page](_documentation_instrument-tab_.md#adjustedprice) to know the difference between “real” and “adjusted”). You can display “real” or “adjusted” price by going to the [Instrument Tab](_documentation_instrument-tab_.md).

[!](_wp-content_uploads_2019_10_Adjusted-vs-Real-Prices.png.md)

[**Back to Top**](_documentation_price-range-filter_.md#backtotop)

You have already reported this .

#### _documentation_price-range-index-filter.md

> Source: https://portfolioboss.com/documentation/price-range-index-filter
> Scraped: 3/1/2026, 2:09:05 AM

* * * [!](_wp-content_uploads_2019_10_Price-Range-Index-Filter-Buy.png.md)

[!](_wp-content_uploads_2019_10_Price-Range-Index-Filter-Sell.png.md)

This filter looks at an index's _last closing value_, and if it falls within the specified threshold value, your strategy is _allowed_ to enter or exit Positions. This is a simple filter to look at the market condition (provided your Portfolio is related to the index).

For example, you’re looking at market’s volatility using VIX (an _index_ that calculates the volatility of the S&P 500). 

[!](_wp-content_uploads_2019_10_VIX-Chart.png.md)

If VIX goes above 30, which indicates a highly volatile market, then exit out of all Positions, and vice versa: when VIX goes below 20 it indicates a generally stable market so your strategy is allowed to enter Positions.

* * **1.**  The first parameter defines what index to use, which is related in some ways to your Portfolio. You can actually enter other types of instrument here, preferably ETFs, representative of your Portfolio:

[!](_wp-content_uploads_2019_10_Price-Range-Index-1st-Param.png.md)

Note, you can't enter a delisted instrument here (those indicated by a number suffix inside square brackets). Otherwise a warning appears and you can't backtest the strategy:

!

* * **2.**  The second parameter defines whether the index must be “Greater than”, “Less than”, “Between”, or “Not between” the threshold value(s). 

[!](_wp-content_uploads_2019_10_Price-Range-Index-Filter-2nd-Param.png.md)

“Not between” might be good if you're [Short Selling](_documentation_a-strategy-for-short-selling_.md), that is, you'll only trade if the market is either very low, or very high (over exhausted) thus you're looking for downtrending market.

* * **3.**  The third parameter defines the _threshold_ value for the index. A negative value is not allowed here, since an index value can’t be negative.

[!](_wp-content_uploads_2019_10_Price-Range-Index-3rd-4th-Param.png.md)

Discount Applied Successfully!

Your savings have been added to the cart.

Close

You have already reported this .

Search

#### _documentation_primitive-pattern-filter.md

> Source: https://portfolioboss.com/documentation/primitive-pattern-filter
> Scraped: 3/1/2026, 2:09:02 AM

[!](_wp-content_uploads_2019_10_Primitive-Pattern-Filter-Buy.png.md)

[!](_wp-content_uploads_2019_10_Primitive-Pattern-Filter-Sell.png.md)

This filter looks at an instrument's high, low, closing, or opening _price_ a certain days/months ago, and if that price is higher/lower than the high, low, closing, or opening price of today (or a few days ago), then consider the instrument as a buy/sell.

The price used here is the [adjusted price](_documentation_instrument-tab_.md#adjustedprice) (after dividends, stock splits, or new shares are adjusted), not the actual price it was trading. Aside from prices, it can also compare the instrument's _volume_ x days ago versus y days ago.

It's quite a simple filter, unlike most Technical Indicators, but it has many uses.

For example, as you know during an uptrend newer prices tend to be higher than the older prices, so only buy the instrument if its closing-price 200 days ago is _less than_ the closing-price 0 day ago (“0 day” means the “latest” closing-price).

Or the reverse, if you're [Short Selling](_documentation_a-strategy-for-short-selling_.md), only buy instruments whose closing-price 200 days ago is _greater than_ the closing-price 0 day ago.

[!](_wp-content_uploads_2019_10_Primitive-Pattern-Filter-Shorting.png.md)

Another example, if you're looking for a “price gap” upward that confirms an uptrend: look for instruments whose high-price 1 day ago is _lower than_ the low-price 0 day ago.

Or the reverse, when you're looking for a “price gap” downward in short selling: look for instruments whose low-price 1 day ago is _higher than_ the high-price 0 day ago.

[!](_wp-content_uploads_2019_10_Upward-Price-Gap_00000.png.md)

Settings for finding the price gap:

[!](_wp-content_uploads_2019_10_Primitive-Pattern-Filter-Price-Gap.png.md)

Now, regarding volume, it can be useful to predict liquidity. So, for example only buy instruments whose volume is increasing from the past 200 days' volume, thus avoiding slippage and making sure your orders are timely filled.

Also, increase in volume may _confirm_ a trend change, as many traders (including big institutional investors) are scrambling to sell (or buy) the shares.

* * **1.**  The first parameter defines the instrument's _older_ property to look for. It can be any one of the “Close”, “Open”, “High”, and “Low” prices, or it can be the “Volume” of that instrument.

[!](_wp-content_uploads_2019_10_Primitive-Pattern-Filter-1st-Param.png.md)

* * **2.**  The second parameter defines how long ago that _older_ price (or volume) is taken from.

[!](_wp-content_uploads_2019_10_Primitive-Pattern-Filter-2nd-Param.png.md)

* * **3.**  The third parameter defines whether the _older_ price (or volume) must be “Greater than” or “Less than” the _newer_ price (or volume).

[!](_wp-content_uploads_2019_10_Primitive-Pattern-Filter-3rd-Param-00.png.md)

* * **4.**  The fourth parameter defines the _newer_ property to look for, whether the price (Close, Open, High, Low) or volume.

[!](_wp-content_uploads_2019_10_Primitive-Pattern-Filter-4th-Param.png.md)

* * **5.**  The fifth parameter defines how long ago to look for that _newer_ price (or volume). Usually you want to set this parameter at “0 day”, so that you have a fresh signal that is still applicable.

[!](_wp-content_uploads_2019_10_Primitive-Pattern-Filter-5th-Param.png.md)

* * *

#### Note:

Once this filter is applied, an indicator appears _below_ the Price Chart (at the [Instrument Tab](_documentation_instrument-tab_.md)) depending on the settings you set for this filter. 

[!](_wp-content_uploads_2019_10_Primitive-Pattern-Filter-Indicator.png.md)

This indicator is calculated by _subtracting_ the newer value from the older value, so you may see this indicator going in the negative values as well. If the indicator is positive it means the _older_ value is greater than the newer value, whereas negative means the _newer_ value is greater than the older value.

[**Back to Top**](_documentation_primitive-pattern-filter_.md#backtotop)

You have already reported this .

#### _documentation_quick-start-guide.md

> Source: https://portfolioboss.com/documentation/quick-start-guide
> Scraped: 3/1/2026, 2:08:01 AM

!Let's learn the essential features, and make money right away without diving too deep! You can click the links scattered throughout this page, and they'll take you to pages with in-depth explanations.

Let the genie do its magic behind the screen.

First you must understand that Portfolio Boss is a _strategy designer_ based on the daily candles, hence what you'll be doing is called [swing trading](https://www.investopedia.com/terms/s/swingtrading.asp). We're currently developing [day trading](https://www.investopedia.com/terms/d/daytrader.asp) capability, but swing trading is the bread and butter of PB. The types of instrument are mainly stocks and ETFs (indexes, commodities, cryptocurrencies, bonds, etc.), and then there are some CEF, UIT, ETN, ADR, Equity Linked Securities, Stapled Securities, and others.

Second, this tutorial uses existing strategies bundled with Portfolio Boss. These are amazing strategies tested through time; but if you wish to create your own strategies, you can start [here](_documentation_managing-your-strategies_.md) based on the knowledge you acquired from this quick start guide.

* * *

### Selecting a strategy:

A strategy is a trading system that contains specific rules and portfolios of stocks to trade. It calculates and gives you the trading signals automatically; when to buy and when to sell. So essentially, the strategy manages most of your trading activity.

**1.**  **The** **very first time** you opened Portfolio Boss, you'll be prompted to enter your log-in credentials. So please do so, and ignore the subsequent confirmation dialogs. 

[https://portfolioboss.com/wp-content/uploads/2021/07/789rtsfzasfs.mp4](_wp-content_uploads_2021_07_789rtsfzasfs.mp4.md)

You're now taken to the [Strategy Management](_documentation_strategy-management-page-overview_.md) page. You can get to this page by clicking the starred-folder icon ! from the sidebar (see the video above).

Note, if you clicked “Yes Please” on the “Interactive Brokers Integration” dialog, you'll be taken to the [Settings Page](_documentation_settings-page-overview-guide_.md) so you can use your market data subscription from [Interactive Brokers](_documentation_interactive-brokers-tab-guide_.md).

!

In a future update, this integration allows you to trade _automatically_ with Interactive Brokers.

* * **2.**  **Choose** **one strategy** from the various strategies listed here. You can read the strategy's description.

!

* * **3.**  **Or use the Search field** (at the top right corner) to find the strategy you want.

!

* * *

### Understand how the strategy operates:

**4.**  **Double click** that strategy to open the [“Backtest Strategy”](_documentation_backtest-strategy-page-overview_.md) page.

[https://portfolioboss.com/wp-content/uploads/2021/07/78tswraswt.mp4](_wp-content_uploads_2021_07_78tswraswt.mp4.md)

Or manually click the “Backtest Strategy” button ! at the sidebar (with the strategy selected).

The _left side_ of this page contains the nuts & bolts of your strategy. We'll focus on this area for a moment (highlighted green in the screenshot below).

!

* * **5.**  **Notice the rule [Monthly Switch on Open of](_documentation_system-settings-panel-guide_.md#monthlyswitch).** It is a day that most of your trading will occur (you enter orders to your broker). 

!

It's not a calendar day, but a trading day of the month when the exchanges are open. So in the screenshot above, it says most trades happen on the 2nd _trading-day_ of the month (or 2nd working day, whichever you prefer).

* * **6.  Look at the rule [Total Positions to Hold](_documentation_system-settings-panel-guide_.md#totalpositions).** This is the number of different instruments (e.g. different company stocks) that you'll hold for any given time. 

!

You'll know the amount of shares to trade (for each company) during the trading day.

* * **7.**  **From the [Instruments Panel](_documentation_instruments-panel-guide_.md)** you can see the baskets of stocks that will be traded. These baskets are called _Portfolios_.

!

Each Portfolio may represent an industry sector, an index, a geopolitical region, or anything. If you wish to create your own Portfolio, take a look at [this page](_documentation_portfolios-panel-guide_.md#createnewportfolio).

* * **8****.  You can see the criteria** for picking the stocks (from the Portfolios) by looking at the [Buy Filters](_documentation_buy-filters-panel-guide_.md) and [Ranking](_documentation_ranking-panel-guide_.md) panels. 

!

These panels contain the _technical indicators_ to select potentially profitable stocks. They'll be entered as positions (bought) based on these technical analysis.

* * **9.**  **As for the criteria to exit the Positions** (i.e. selling the stocks), look at the [Sell Filters panel](_documentation_sell-filters-panel-guide_.md). 

!

For example, if the stock's price starts falling a _certain way_, the strategy will exit that Position, before it eats away much of your _past_ profit.

* * *

### Seeing how the strategy performs:

_Backtest_ is a rigorous test for your strategy, to see how it performs in the decades of _past_ market conditions, as well as its _potential_ performance in the future. If there's anything worse than coin flipping, it's trading blind without testing a system.

**10.**  **Enter your account size** in the [Initial Amount](_documentation_backtest-panel-guide_.md#initialamount) property. This amount will be divided evenly for each Position (each company's stock). 

!

If you have $100,000 put into a strategy that holds 5 Positions at any given time, then each Position will be given $20,000 to buy its shares.

During the course of holding these Positions, some may worth more than $20,000 (when the Positions are profitable), while others may contain less than $20,000 (when the Positions experience loss).

* * **11.**  **Now, to backtest the strategy,** click the “Start” button at the top of this page: 

!

A confirmation dialog appears, allowing you to add a memo for this backtest:

!

If you don't want this obtrusive dialog to appear each time you start a backtest, tick the checkbox “Don't show again”. Once done, click the button “Continue” to actually start the backtest. A memo is _optional_, as it's simply a description about a backtest _run_. Each run (and its memo) will be seen under the [Manual Results Tab](_documentation_manual-results-tab_.md):

!

Now a progress dialog appears. Wait until it's finished, and you'll get the various statistical data, or _metrics_, from this backtest.

!

* * **12.**  **We'll depart the left area now,** and look at the [Metrics Tab.](_documentation_metrics-panel-guide_.md) Here, the performance data are served. Pay attention to the important metrics: CAGR, Max Drawdown (%), and Total Amount. 

[https://portfolioboss.com/wp-content/uploads/2021/07/futr7es54ara.mp4](_wp-content_uploads_2021_07_futr7es54ara.mp4.md)

[CAGR](_documentation_metrics-panel-guide_.md#cagr) (Compound Annual Growth Rate) tells you the average _yearly_ growth rate on your capital (compounded from the previous year's total gain and loss). This value is stated in percent of the capital, higher value is better.

[Max Drawdown (%)](_documentation_metrics-panel-guide_.md#maxdrawdown) tells of the deepest crash the strategy experienced during the backtest, which may indicate a similar occurrence in the future. It's stated in percent of the _peak value_ before the crash.

[Total Amount](_documentation_metrics-panel-guide_.md#totalamount) is the money your capital could've grown into, should you trade with this strategy for the same amount of time as the backtest period.

* * **13.**  **Look at the [Performance Tab](_documentation_monthly-performance-panel-guide_.md).** Here, you see how much the strategy has gained (or lost), every month and every year. It's a _compounded percentage_ from last month's (or last year's) total.

!

It's a rough guideline on what you _may_ earn each month. Note the “Test” column shows the strategy's gains, whereas the “Benchmark” column shows the benchmark's (index) gains. Index is representative of the market, it's something you wanna beat through active trading. Hence the term “beating the market”.

* * **14.**  **Look at the [Chart Tab](_documentation_chart-tab_.md),** located on the right area. This chart shows the strategy's _equity curve_ versus the benchmark's. 

!

Equity curve is just the historic daily return plotted in a graph; green for the strategy, blue for the benchmark.

Thus, you have seen how the strategy performed in the past, which gives you an idea how it may serve you in the future.

* * *

### Deploy the strategy and receive trading signals:

**15.**  **Let's now receive trading signals** (buy/sell signals) automatically from this strategy. At the [Notifications](_documentation_strategy-panel-guide_.md#enablenotif) property, choose the option “Daily email”. 

!

The catch is, you can't customize the strategy (it's set to read-only mode) while you have “Daily email” notifications enabled. Later on you'll learn why & how to override the read-only mode.

* * **16.**  **By default,** trading signals will be sent to the email you registered your license with. To change that, go to the “Settings” page, [Automation tab](_documentation_automation-tab-guide_.md).

[https://portfolioboss.com/wp-content/uploads/2021/07/gfhu5t67es56has.mp4](_wp-content_uploads_2021_07_gfhu5t67es56has.mp4.md)

You can also opt to receive text messages direct to your phone.

* * **17.**  **Make sure** the [Send email notification…](_documentation_automation-tab-guide_.md#sendemailnotif) is toggled ON.

!

Disabling that toggle also disables the notifications.

* * **18.**  **Now write the e-mail address** on the [E-Mail Address field](_documentation_automation-tab-guide_.md#emailaddresses), and press enter. 

[https://portfolioboss.com/wp-content/uploads/2021/07/6789r5nse53s4n.mp4](_wp-content_uploads_2021_07_6789r5nse53s4n.mp4.md)

You can add more e-mail addresses by writing on the field below it. You can have 3 different e-mail addresses set here.

* * **19.**  **For sending trading signals to your phone,** you can type an _email-to-text_ address on any of the e-mail fields. Please refer to your carrier's email-to-text command. 

[https://portfolioboss.com/wp-content/uploads/2021/07/hui6t78ena.mp4](_wp-content_uploads_2021_07_hui6t78ena.mp4.md)

For example, Verizon users can type something like this: 5551234567@vtext.com (change the number to your actual phone number). For AT&T users, you can enter something like this 5551234567@txt.att.net. Press enter (or the plus button) once you're done.

* * **20.**  **To make sure** Portfolio Boss can actually send to such addresses, press the [Send a test email](_documentation_automation-tab-guide_.md#sendtestemail) button. This will send a test notification to you. Check your inbox whether you have received the e-mail.

!

The notification e-mail is sent daily to you, and it contains trading signals (if there's any), the Positions currently held (and their gains/losses), along with the top-ranked instruments (indication of the instruments to be bought next):

!

If you didn't receive the email, you might want to check [**Portfolio Boss Status Page**](https://status.portfolioboss.com/), and see if there are no hiccups on the Mailing Service:

!

That status page shows you the current state of the various Portfolio Boss services, including historical price data downloads, [The Boss supercomputer service](_documentation_the-divine-engine-and-the-boss_.md), and Smart Money data; it's refreshed every minute. Now, if you still have trouble receiving the email, ensure the addresses are typed correctly in the fields above. Or, you can contact our Support Team at [support@portfolioboss.com](mailto:support@portfolioboss.com).

Now you're all set and ready to trade!

* * *

### Let's Trade!

**21.**  **For your first trade,** let's take a look at the [Trade Signals Tab](_documentation_trade-signals-panel-guide_.md) just to the left of the _equity curve chart_. If there are no trading signals, as shown below: 

!

then head over to the [Positions Tab](_documentation_positions-panel-guide_.md) and see what instruments are listed there:

!

As you see we have 5 different positions to enter. We'll calculate the number of shares to buy for each position, based on their “Weight” values. “Weight” is the percentage of your total capital assigned to a particular position.

For example the stock RNWK has a weight of 15%, if you have $100,000 to trade, then it gets $15,000 to buy the shares. Let's say RNWK traded at $1.86 today, that means 15,000 divided by 1.86 equals 8,064 shares. Continue the calculation for other stocks.

Once done, enter the orders to your broker. You can use the broker's mobile app, desktop platform, or the old school way of calling them via telephone. The orders are usually executed next time the market opens, within 30 minutes of the opening bell.

**UPDATE:** With the latest version of Portfolio Boss, it is now possible to calculate automatically the amount of shares to trade, with the Trade Plan Calculator, _even if_ there are **no** trading signals as in the above scenario. **Please read the following section, no. 22.** Remember, you don't need trading signals to use this calculator now; just open it and it will calculate the correct amount of shares even if it's your first time using the strategy.

* * **22.  It is much easier** if your first trade happens when there are trading signals, as shown on the Trade Signals Tab:

!

As you see there are two signals: sell GPRE, and buy PTSHX. But it's your first time trading with this strategy, so you don't have anything to sell, and you got everything to buy. This is where it gets easy: open the [Trade Plan Calculator](_documentation_trade-plan-calculator_.md).

[https://portfolioboss.com/wp-content/uploads/2021/07/fyu567w456hnwj.mp4](_wp-content_uploads_2021_07_fyu567w456hnwj.mp4.md)

This calculator tells you what instruments to trade, and how many shares, based on your account size and the positions weights. All you have to do is put your account size (in US dollar), press enter, and **make sure to tick** the checkbox “Check if this is the first time you're entering this strategy”.

Once done with the calculator, you can just close it. Remember, Portfolio Boss _does not_ enter the orders automatically for you (although it's in the works). **Note:** some licenses don't have access to this Calculator. Please contact our [Customer Support](mailto:support@portfolioboss.com) if you wish to upgrade your license.

* * **23.  Now do understand,** trading signals (via e-mail) are sent one day prior to the execution day; usually the night before. 

!

PB also sends you notifications on a daily basis, informing you of how your Positions perform. 

But keep in mind, PB must _run_ on your Computer so it can send the notifications. It doesn't have to run 24/7; just a few hours after the market (exchanges) close. For example, if you're trading on American stock exchanges (depending on the strategy's Portfolio), trading day usually closes at 4:00 PM Eastern Time. Just let Portfolio Boss run around that time, no need to backtest the strategy yourself. Those strategies with notification enabled are automatically backtested to send you the trading signals and performance reports (provided the End of Day data are already downloaded).

* * **24.  All you have to do now is relax,** wait for the next trading signals. Once you're notified, open Portfolio Boss and click the Start button again ! on that strategy, so PB gets the _latest_ performance reports, and you'll be able to use the Trade Plan Calculator.

[https://portfolioboss.com/wp-content/uploads/2021/07/ftyes6es54has.mp4](_wp-content_uploads_2021_07_ftyes6es54has.mp4.md)

This time is a little different, since it's _not_ your first time using this strategy.

First you must enter your _current_ account size, which has been affected by the ups and downs of the market. You can look for something called “Net Liquidation Value” on your broker's report. That's your investment marked to market value. In the example below, we entered $107,250, assuming our positions were mostly profitable:

!

At the bottom of the dialog box, make sure the checkbox “Check if this is the first time…” is **not** **ticked**. Then as usual, take note of the most important columns: **Action** (whether you'll be buying or selling), **Symbol** (the company ticker), and **Suggested Quantity** (number of shares you'll trade for each company).

Take note of the VLEEY symbol, divided into multiple orders. That's because the number of shares you'll trade for VLEEY exceeds the _average volume per minute_ that VLEEY usually traded for. To pile all shares into a single order means you'll get bad fills (slippage). Besides, dividing such a big order into multiple, smaller orders (with different entry time) may help obfuscate your trading activity from the evil High Frequency Trading firms.

Note, even if it's not a switch day and you're merely selling and buying a few instruments (not replacing all of the old Positions), you must still enter your total account size in this calculator, so the weighting on the new Position(s) will be correct.

* * **25.**  If you use TWS (Trader Workstation) software from [Interactive Brokers](https://www.interactivebrokers.com/en/home.php), you may export this complicated information into a _basket file_ which will be imported into TWS. It will then process the orders for you.

[https://portfolioboss.com/wp-content/uploads/2021/07/746g54wbhw5a.mp4](_wp-content_uploads_2021_07_746g54wbhw5a.mp4.md)

Simply click the button “Create IB Basket File” (at the bottom of this calculator), and choose where you want to save the basket file.

Please refer to the TWS user guide [here](https://www.interactivebrokers.com/en/software/tws/usersguidebook/specializedorderentry/upload_basket.htm) on how to import (upload) the basket file.

* * *

### Seeing how the Positions perform:

**26.**  **It is important that you follow** every trading signals given, as otherwise you'd be deviating from the strategy. PB can only assume that you're actually following it, so any deviation would break the consistency between your actual account and PB's calculation.

!

To see the performance of your positions, you can go back to the [Positions Tab](_documentation_positions-panel-guide_.md) (you must backtest the strategy again ! if you closed Portfolio Boss). It shows you the Positions you're currently holding, and how much they're gaining (or losing) since you entered the Positions.

It's updated a few hours after the market close, but really, the more you look into your positions, the more stressed out you'll be, and the more likely you'll abandon the strategy (or any kind of investing for that matter).  

* * **27.**  **You can click any of the symbols** (highlighted blue) to open up the [Price Chart](_documentation_instrument-tab_.md) for that symbol. Here appears the price history, as well as the Technical Indicators the strategy uses to analyze that instrument. You can also see the Buy and Sell actions the instrument experienced so far with this strategy. 

[https://portfolioboss.com/wp-content/uploads/2021/07/hui6y85e7jw.mp4](_wp-content_uploads_2021_07_hui6y85e7jw.mp4.md)

When viewing the chart, you can:

*   click-drag the chart to pan it around
*   scroll the mouse-wheel to zoom the chart in & out
*   double click the chart to reset the zoom level
*   and right-click to show a tooltip on the cursor (contains the Open, High, Low, and Close prices, as well as Volume and Date information).

* * **28.**  **As stated some time ago,** most of your trading takes place during the [switch day](_documentation_system-settings-panel-guide_.md#monthlyswitch). This is when old positions are replaced (sold) with new positions that are potentially more profitable. 

!

Outside the switch day, a few trading signals will be given, usually sell signals for those instruments that triggered the [Sell Filters](_documentation_sell-filters-panel-guide_.md). A sell signal is usually accompanied by a buy signal, to replace the sold instrument.

* * *

### Congratulations!

Now you know how to let Portfolio Boss manage your trading activities. All you have to do is revel and enjoy those profits! Don't let emotions and cognitive biases ruin your hard earned money.

Some important notes now, if you please:

*   Due to the nature of Portfolio Boss' quick switching (once the old is liquidated you immediately buy a new one), it's highly recommended that you use a [Margin Account](https://www.investopedia.com/terms/m/marginaccount.asp) at your broker. If you use a [Cash Account](https://www.investopedia.com/terms/c/cashaccount.asp), your purchasing power may be limited by the [Trade Settlement Date](https://www.investopedia.com/terms/s/settlementdate.asp), or worse, you may commit Good Faith Violation (or Free Riding Violation) and get your account suspended. If, for whatever reason, you can't get a Margin Account, you must set aside some part of your fund (cash) as reserve. It will be used to enter new positions recommended by PB while waiting for the previous trade's fund to settle.

*   If you want to create your own strategy, we highly recommend that you finish these chapters entirely:

*   * [Chapter 3 – Strategy Management Page](_documentation_strategy-management-page-overview_.md)
    * [Chapter 4 – Backtest Strategy Page](_documentation_backtest-strategy-page-overview_.md)
    * [Chapter 2 – Portfolio Management Page](_documentation_portfolio-management-page-overview_.md)
    * [Chapter 7 – Filters & Rules](_documentation_about-filters-rules_.md)
    * [Chapter 6 – Combine, Stack, and Trade Entire Strategies](_documentation_multi-strategy_.md) (optional).

*   But if you have access to our Divine Engine, you can let the **Artificial Intelligence** design the ultimate strategies **for you** (even writing codes on its own to create technical indicators from scratch). Refer to [Chapter 5](_documentation_the-divine-engine-and-the-boss_.md) for this feature. If you wish to upgrade your license, please contact our [Customer Support](mailto:support@portfolioboss.com) team.

**[Back to Top](_documentation_quick-start-guide_.md#backtotop)**

You have already reported this .

#### _documentation_ranking-panel-guide.md

> Source: https://portfolioboss.com/documentation/ranking-panel-guide
> Scraped: 3/1/2026, 2:08:09 AM

!

This Panel is located at the [Rules Area](_wp-content_uploads_2021_05_gdg56ye5dg_00000_00000.png.md) of the “Backtest Strategy” page.

It contains the Rules used for ranking your instruments. So, once instruments in the strategy's Portfolios pass the [Buy Filters](_documentation_buy-filters-panel-guide_.md), they will be ranked _top to bottom_ (or vice versa) based on these Ranking Rules. The _top_ X instruments are then entered as Positions.

This “top X” is defined by the strategy's [“Total Positions to Hold”](_documentation_system-settings-panel-guide_.md#totalpositions) (at the “System Settings” Panel). So a strategy that holds 10 Positions at any given time will look at the _top_ 10 ranked instruments.

!

This panel is collapsed by default; to expand its contents, simply click the arrow button as shown above. When it's collapsed, you'll see the number of rules added to this panel (e.g. ! ).

**Note:** If you use a restricted license, this panel may not be visible to you. So you can't customize how the instruments are ranked and picked. If you wish to upgrade your license, please contact our Customer Support at [support@portfolioboss.com.](mailto:support@portfolioboss.com)

* * **1.**  **To add the ranking-rules,** simply click the “Add Ranking” button.

!

* * **2.**  **The “Add Ranking” dialog** then shows up, where you can search, select, and add the Ranking Rules. Make sure that you actually ticked (enabled the checkbox) of the Ranking Rules before pressing the “OK” button.

!

If you're merely adding _one_ rule, you can double-click that rule _without_ pressing the OK button (provided the rule's not yet checked).

* * **3.**  **Once a rule is listed,** you get the gist of how it operates by reading its parameters. And if you hover your mouse on the rule, a descriptive tooltip shows up. 

!

Note that newly added rules are placed at the bottom of the list. If you want to dive deep into each Ranking Rule, please refer to [Chapter 7](_documentation_about-filters-rules_.md) where we discuss the Technical Indicator(s) used, the real-life application of each rule, and their parameters. 

* * **4.**  **You can add the same Ranking Rule** more than once in the strategy (preferably each rule has its own distinct settings from the other). 

!

Simply open the “Add Ranking” dialog again and choose the same rule you have added previously.

* * **5.**  **To delete a rule,** click the trash bin button next to it.

!

* * **6.**  **Each listed Rule has “Offset” and “Weight”** parameters. “Offset” will _shift_ the period-span of that rule a certain distance to the past.

!

For example, the rule says “Rank according to… Highest volatility in 5 days”, which means the instruments are ranked from the one with the highest volatility to the lowest, during the past 5 days from _today_. Thus, giving it an offset of 5 days will shift the _current_ date to 5 days ago, i.e. the time range for this Ranking Rule starts from 10 days ago until 5 days ago, instead of 5 days ago from today. That will be the time range where instruments' volatility is calculated.

Most of the time though, you don't need an “Offset” value (i.e. 0 days). This parameter is there to satisfy some esoteric theories on trading.

Now, the **“Weight”** parameter allows you to put more (or less) _importance_ to each rule. That is, if you have but one rule, its “Weight” will be 100% as it is the only rule being used. But if you have multiple rules, you can define their relative importance by defining each of their “Weight”. 

!

For example, you have two Ranking Rules: one looks for the **lowest-volatility** instruments, with a “Weight” of 70%. Another looks for the **highest-return** instruments, with the “Weight” set to 30%. That means, instruments are ranked more on their _lower volatility_ than their higher return, thus instruments that have the highest return but _higher volatility_ may not rank highly. But obviously the two rules are still working in tandem with each other.

!

The numbers you put there can be anything, and don't necessarily add up to 100%. Behind the screen though, they're automatically calculated so they add up to 100%, and you can see the **actual weight** for each rule inside the parentheses. If you simply add rules without changing their weights, they'll have equal weights, thus equal importance to each other.

* * **7.  You may use the checkbox** on each rule to disable/enable it.  An unchecked rule means it's not used by the strategy.

!

You can do this to experiment how the strategy runs with or without the rule, while keeping its parameter settings (instead of deleting the rule and adding it again).

* * *

#### Notes:

*   You can show or hide the Rules' header (name) with this button:

!

*   It's possible for a strategy to not have a single Buy and Sell Filter; but a Ranking Rule is always necessary. If such is the case, the strategy will only buy based on the Ranking Rule (after all your instruments have been ranked), and then it will only sell instruments during switch-day. This is only possible for a Periodically Switching Strategy, as it has a switch-day; if you're using _Continuously Switching Strategy_, at least one Sell Filter is also needed, otherwise PB will throw a warning at the [“System” parameter](_documentation_system-settings-panel-guide_.md#systemparameter) when you choose the option “Continuously Switch Position” there.

*   Exception to the above is when your strategy contains but one instrument (as its Portfolio); then it won't need a single ranking rule. If it originally contained numerous instruments, and then you leave just one on the Portfolio, whatever Ranking Rules you have here will not be shown. You _can't_ even add Ranking Rules to it.

!

     The moment you add more instruments, those Ranking Rules will be shown and used again.

*   Keep in mind, your various Ranking Rules must be able to cope with a long backtest range, in various market conditions. Otherwise your strategy is too fine-tuned to perform well at a specific, short-term period.

[**Back to Top**](_documentation_ranking-panel-guide_.md#backtotop)

You have already reported this .

#### _documentation_rate-of-change-index-filter.md

> Source: https://portfolioboss.com/documentation/rate-of-change-index-filter
> Scraped: 3/1/2026, 2:08:57 AM

[!](https://portfolioboss.wpenginepowered.com/wp-content/uploads/2019/10/Return-Index-Filter-Buy.png)

[!](https://portfolioboss.wpenginepowered.com/wp-content/uploads/2019/10/Return-Index-Filter-Sell.png)

This filter looks at the instrument's _price change_ during a specified period, expressed as _percentage change_ (from the starting price toward the end price). It is then compared to the index's percentage change during the same period. If it's greater (or less than) the index's, the instrument will be considered as a buy (or sell).

In other words, you're looking at the instrument's “Rate of Change” (ROC) versus the index's; how fast that instrument is gaining (or losing), compared to the index, during that period.

This filter is similar to the [Rate of Change (ROC) Position Filter](_documentation_rate-of-change-roc-position-filter_.md), but now with the index as the yardstick. So for example, this filter will find instruments that may potentially beat the index.

* * **1.**  The first parameter defines the _period_ to calculate the ROC of _both_ the instrument and the index.

[!](https://portfolioboss.wpenginepowered.com/wp-content/uploads/2019/10/Return-Index-Filter-1st-Param.png)

* * **2.**  The second parameter defines whether the instrument's ROC must be “Greater than” or “Less than” the index's ROC.

[!](https://portfolioboss.wpenginepowered.com/wp-content/uploads/2019/10/Return-Index-Filter-2nd-Param.png)

* * **3.**  The third parameter defines the index to compare against. You can click the little “Chart” icon beside it to open up the index's Price Chart (at the [Instrument Tab](_documentation_instrument-tab_.md)).

[!](https://portfolioboss.wpenginepowered.com/wp-content/uploads/2019/10/Return-Index-Filter-3rd-Param.png)

You can also put any instrument here that you believe is related to the strategy (usually ETFs). Though do keep in mind, you mustn't enter a delisted instrument (indicated by a number suffix inside square brackets); otherwise there's a warning and you can't backtest the strategy:

!

* * *

#### Note:

Once this filter is applied, two indicators are displayed _below_ the Price Chart. One indicator is for the instrument's ROC during the specified period, and one indicator is for the index's ROC during that same period.

[!](https://portfolioboss.wpenginepowered.com/wp-content/uploads/2019/10/Return-Index-Filter-Indicators.png)

[**Back to Top**](_documentation_rate-of-change-index-filter_.md#backtotop)

You have already reported this .

#### _documentation_rate-of-change-roc-position-filter.md

> Source: https://portfolioboss.com/documentation/rate-of-change-roc-position-filter
> Scraped: 3/1/2026, 2:08:58 AM

!

!

This filter looks at the price change of an instrument from the beginning of the period until today. Such price change is represented as a percentage.

For example, with a period of 25 days: an instrument's closing price today is $30, while 25 days ago (the beginning of the period) it was $25. That translates into a price increase of $5, or 20% increase from the beginning price ($25).

If the price is decreasing, we will have a negative percentage. For example, the price went down from $20 to $10, which means a decrease of $10, or -50% of the beginning price ($20).

In other words, this filter looks at the instrument's price momentum or velocity (its “Rate of Change”, how fast the price is gaining or losing).

*   Positive percentage values may indicate an uptrend. The higher the positive percentage, the stronger the uptrend.
*   Negative percentage values may indicate a downtrend. The lower the negative percentage, the stronger the downtrend.
*   Percentage values near 0% may indicate a trading range.

Note that you can apply this filter multiple times as Buy Filters, to look for discounts:

!

*   The first Buy Filter looks at decreasing price in a short period, let's say 5 days.
*   The second Buy Filter makes sure that such price dip happens in a generally upward trend, thus it looks at increasing price for a longer period, let's say 200 days.

This filter is also great as a stop-loss, to lock your profit from excessive downward movements (for example during bear markets). In such case, you may want to set the strategy to revert to Cash after positions are sold (instead of a Cash Equivalent, because Bonds can also drop deep during financial crisis).

!

Do understand, some manual traders use the RoC as a momentum oscillator. But such use is very subjective for each instrument. There's no definite overbought/oversold zones: some instruments are known for their huge advances and declines, while others are calmer. Therefore it's best to use this in tandem with a more general momentum oscillator such as the RSI.

* * **1.**  The first parameter defines the period to look for the starting and latest price. For example, a period of 10 days means the price 10 days ago is compared to today's price.

!

Adjust this period according to your trading duration. If you're a short term trader, generally you will use values like 5, 9, or 12 days. Intermediate timeframe is best represented by a period of 45 days. If you're a longer term trader, use longer periods such as 200 days. And don't make it too short or too long, in relation to your trading time-frame. If it's too short, you'll get many false signals. Longer periods generally give a truer and more predictable future performance, but it may be too late to enter the Position (the trend may well be underway toward its end).

It's best to have multiple instances of this filter, with differing time periods.

* * **2.**  The second parameter defines whether the instrument's percentage-change must be “Above” or “Below” the threshold percentage-change. Generally, use “Above” to find uptrending instruments, and “Below” for downtrending ones.

!

* * **3.**  The third parameter defines the threshold percentage-change, whose meaning is already explained above.

!

A negative percentage bottoms out at -100%, because that means the instrument price has become $0, the lowest price possible for an instrument. A positive percentage on the other hand, can go 100% and beyond, as there is no limit to the upper price of an instrument.

* * *

#### Notes:

*   You may use a very short period, like 2 days, along with a big percentage change (e.g. beyond 50%, positive or negative) to find potential “gappers”. That is, the price change on mere two days was so great that the two candles may form a gap between them. This, in turn, can be used on any interpretation: either that gaps may get filled sooner or later, or, such huge momentum indicates a changing trend or breakout (or a strong confirmation).

*   Once this filter is applied (and the strategy is backtested), you can see the ROC indicator below the price chart (at the [Instrument Tab](_documentation_instrument-tab_.md)). Make sure you have selected an instrument before you can see this ROC indicator.

!

[**Back to Top**](_documentation_rate-of-change-roc-position-filter_.md#backtotop)

You have already reported this .

#### _documentation_retracement-filter.md

> Source: https://portfolioboss.com/documentation/retracement-filter
> Scraped: 3/1/2026, 2:09:00 AM

[!](_wp-content_uploads_2019_10_Retracement-Filter-Buy.png.md)

[!](_wp-content_uploads_2019_10_Retracement-Filter-Sell.png.md)

This filter utilizes the powerful Retracement Rule that predicts a rally after a recent pullback/correction, and whether or not it's just a pullback (could be a reversal of the trend).

This is useful to time your entry into a Position: so not only you get a big discount during the pullback, but you'll get a much higher profit since the price will advance to a new higher peak.

[!](_wp-content_uploads_2019_10_Retracement-Example-1_00000.png.md)

This filter looks at the highest and lowest _closing-prices_ of an instrument during the past certain days/months, and then divide the _vertical distance_ (between such peak and trough) by a certain percentage.

Let's say for the past 200 days an instrument's _lowest_ price is $25 and the _highest_ price is $35, which means a distance of $10 between the trough and peak. Therefore, a percentage of 50% means $5 _from the highest price_, which equals a price of $30.

This 50% level (i.e. $30 price level) will be your support (or resistance) line, where the price may _bounce back_ again after the pullback. So, you enter the position when the pullback is at that 50% level.

[!](_wp-content_uploads_2019_10_Retracement-Overview_00000.png.md)

Different percentage levels may be used depending on what school of thought you believe: some believe in the Fibonacci ratio, in which 23.6%, 38.2%, or 50% is used.

Others use a simpler (but generally proven) percentage levels of 50% and 66%: prices will generally bounce at that 50% level, and if they don't, look _whether_ it bounces at 66%. If it continues past 66%, then a trend reversal is likely, so get out of that position.

Note that this filter is best used with another filter that confirms you're in a trend (let's say the [“Moving Average Cross Over Filter”](_documentation_moving-average-cross-over-filter_.md)).

And best of all, this Retracement Rule also works when you're in a _downtrend_, for example when you're trading [Short Positions](_documentation_a-strategy-for-short-selling_.md). That is, if a _downtrending_ instrument rallies up, more often than not, it will _bounce back down_ at that 50% line, so you'll get the best price possible for shorting (selling) that instrument before the price goes back down again.

* * **1.**  The first parameter defines whether the instrument's _closing-price_ must be “Greater than”, “Less than”, “Between”, or “Not between” the percentage line(s). “Greater than” means the instrument's price must be “below” the percentage line, that is, it's actually going cheaper than the percentage line. 

[!](_wp-content_uploads_2019_10_Retracement-Percentage-Calculation_00000.png.md)

And vice versa with “Less than”, i.e. the price must be “above” the percentage line.

Let's say during an _uptrend_, you will enter a Position when the instrument's price drops toward 50%; then set a value of “Greater than” “49%” for this filter. Another example, you will _get out_ of a Position if the price drop is “Greater than” “66%”.

[!](_wp-content_uploads_2019_10_Retracement-1st-Param.png.md)

Or another example for entering a Short Position: You will borrow (and then sell) the instrument only if it hits the 50% line, which means the instrument's price must _increase_ toward that 50% line before it bounces back down; so you set this filter to “Less than” “51%”.

[!](_wp-content_uploads_2019_10_Retracement-1st-Param-B-000.png.md)

But note, these “Greater/Less than” values are _not_ the most intuitive:

*   First, if you set “Greater Than”, the price might actually be _far below_ the percentage line (thus indicating a trend reversal instead of bouncing back), but still the strategy will enter that Position anyway.
*   Second, if you use “Less than”, the price may actually be _far above_ the percentage line, thus you don't get as much discount as possible but the strategy will enter that position anyway.

So, the best way to use this filter is by using the “Between” value. Thus, in the above example, you will only enter a Position if the instrument's price falls _between_ 40% and 50%. 

[!](_wp-content_uploads_2019_10_Retracement-Between-Param.png.md)

That way, not only you'll get a good discount, but you also make sure you don't buy instruments that are potentially going toward the downtrend.

With that being said, “Greater/Less than” _may_ make more sense if you use this filter as a Sell Filter (exiting positions). So continuing with the above example, after you make sure you buy instruments that don't breach the 50% level, then you make this Stop-Loss:

*   if any of these Positions start breaking the 66% level, then get out of that Position. So, set this sell-filter as “Greater than” “66%”.

[!](_wp-content_uploads_2019_10_Retracement-Filter-Sell-66.png.md)

* * **2.**  The second parameter defines the percentage line between those highest and lowest prices of the past certain days. 

[!](_wp-content_uploads_2019_10_Retracement-Filter-2nd-Param.png.md)

Remember that this percentage line is always calculated from the highest price, that is, 0% is at the highest price and 100% is at the lowest price.

* * **3.**  The third parameter defines how many days (or months) to look for the highest and lowest prices. 

[!](_wp-content_uploads_2019_10_Retracement-Filter-3rd-Param.png.md)

Remember that this is a moving window; for example, a value of 200 days here means the strategy will find the highest and lowest prices _from today_ until 200 days ago.

* * *

#### Notes:

*   After you applied this filter, some indicators will be overlaid on the [Price Chart](_documentation_instrument-tab_.md): one indicator is for the _highest price_ of x days/months ago, one indicator is for the _lowest price_ of the x days/months ago, and one indicator for the percentage line (or lines, if you use multiple percentage lines with the “Between” value, as explained before).

[!](_wp-content_uploads_2019_10_Retracement-Filter-Indicators.png.md)

*   You may use this filter with another filter that finds _currently_ bearish instruments (instruments that are _currently_ going downhill), such as the [Primitive Pattern filter](_documentation_primitive-pattern-filter_.md) (closing price 1 day ago is higher than the closing price 0 day ago a.k.a today). That's because this Retracement Filter by itself may buy instruments that are already well underway on the rally, so you don't get the best discounts from the beginning.

[**Back to Top**](_documentation_retracement-filter_.md#backtotop)

You have already reported this .

#### _documentation_return-index-filter.md

> Source: https://portfolioboss.com/documentation/return-index-filter
> Scraped: 3/1/2026, 2:09:17 AM

*   »
*   »
* [Return Index Filter](_documentation_return-index-filter.md)

* * *

Discount Applied Successfully!

Your savings have been added to the cart.

Close

#### Block Member?

Please confirm you want to block this member.

You will no longer be able to:

*   See blocked member's posts
*   Mention this member in posts
*   Invite this member to groups
*   Message this member
*   Add this member as a connection

**Please note:** This action will also remove this member from your connections and send a report to the site admin. Please allow a few minutes for this process to complete.

#### Report

You have already reported this .

#### _documentation_rsi-filter.md

> Source: https://portfolioboss.com/documentation/rsi-filter
> Scraped: 3/1/2026, 2:09:16 AM

[!](_wp-content_uploads_2019_10_RSI-Filter-Buy.png.md)

[!](_wp-content_uploads_2019_10_RSI-Filter-Sell.png.md)

This filter looks at an instrument's RSI (Relative Strength Index) during the past certain period, to decide whether that instrument will be bought/sold.

RSI is a momentum oscillator that indicates whether an instrument is being “overbought” (overpriced) or “oversold” (underpriced), thus it can tell you of an impending trend change.

RSI oscillates between 0% and 100%. Generally, an RSI of 70% or higher means the instrument is “overbought”, so it will experience a pullback or correction (however small or quick). An RSI of about 30% or less means the instrument is “oversold”, so it will experience a rally (however small or quick).

But these are just a general rule of thumb, since RSI may also generate false signals. So, it's best to use this filter with another filter, for example a [moving average filter](_documentation_moving-average-cross-over-filter_.md) or the [Primitive Pattern filter](_documentation_primitive-pattern-filter_.md) so you know what trend the instrument is currently at.

[!](_wp-content_uploads_2019_10_AMD-RSI_00000.png.md)

During an _uptrend_, an RSI of 30% or less usually signals a rally (after a pullback); whereas during a _downtrend_, an RSI of 70% or higher usually signals a reversal (after a peak). So, it's best to enter Positions whenever these instruments reach those RSI values.

Another school of thought uses the RSI as a trend confirmation: during an uptrend, the RSI may go above 70% for an extended period of time, whereas during a downtrend the RSI may go below 30% for an extended period.

* * *

The parameters for this filter are:

**1.**  The first parameter, “x days”, defines the period to look for the RSI, usually it is 14 days.

[!](_wp-content_uploads_2019_10_RSI-Filter-1st-Param.png.md)

* * **2.**  The second parameter, “Greater than/Less than/Between/Not between”, defines where the instrument's RSI must fall in relation to the _threshold_ RSI, for that instrument to be considered.

[!](_wp-content_uploads_2019_10_RSI-Filter-2nd-Param.png.md)

* * **3.**  The third parameter, “n percent”, defines the _threshold_ RSI that you want. 

[!](_wp-content_uploads_2019_10_RSI-Filter-3rd-4th-Param.png.md)

Generally, it's set at either 70% or 30%. But you can also set it at a maximum and minimum RSI values that you want, which means the instrument must fall _between_ such RSI values, that is, if you use “Between” in the previous parameter.

If you use “Not Between”, you're looking for instruments whose RSI falls _outside_ the minimum and maximum threshold.

* * *

#### Note:

Using this filter will display an RSI indicator _below_ the instrument's [Price Chart](_documentation_instrument-tab_.md). If it doesn't show up, hover your mouse just below the Price Chart until you see the cursor changes into a vertical arrow, then drag that edge upward so the RSI chart shows up entirely.

[!](_wp-content_uploads_2019_10_RSI-Filter-Indicator.png.md)

[**Back to Top**](_documentation_rsi-filter_.md#backtotop)

You have already reported this .

#### _documentation_sell-filters-panel-guide.md

> Source: https://portfolioboss.com/documentation/sell-filters-panel-guide
> Scraped: 3/1/2026, 2:08:11 AM

!

This panel allows you to add various technical indicators, which determine the conditions to _exit_ a Position. These are known in Portfolio Boss as “Sell Filters”. This panel is located at the [Rules Area](_wp-content_uploads_2021_05_gdg56ye5dg_00000_00000.png.md) of the “Backtest Strategy” page; and by default it's collapsed (with the info telling you the number of filters it contains e.g. ! ). Click the button shown below to expand this panel:

!

So, the strategy looks at the Positions currently open, and if a Position hits **any** of the Sell Filters, you'll be given a Sell Signal to liquidate the Position. Sometimes though, a Position may be liquidated automatically (without triggering a Sell Filter) if its instrument company (or fund) gets delisted from the exchanges (due to merger, acquisition, or bankruptcy).

Keep in mind, _most_ of the Sell Filters use the same technical indicators as the Buy Filters; just with different parameters. Please refer to [Chapter 7](_documentation_about-filters-rules_.md) for a comprehensive explanation of each Filter.

* * **1.**  **To add a Sell Filter** (or multiple Sell Filters), click the “Add Sell Filter” button (at the top-right corner). 

!

The “Add Sell Filter” dialog shows up, where you can search, select, and add the Sell Filters into your strategy. Make sure you actually ticked them (enabled their checkboxes) before clicking the “OK” button.

!

If you're merely adding _one_ Filter, you can double-click it _without_ pressing the OK button (provided the Filter's checkbox isn't ticked yet). The newly added Filters are placed at the bottom of the list.

!

Please note, certain licenses may restrict you to use only a handful of Filters, or Filters with limited parameters. If you wish to upgrade your license, please contact our Customer Support team at [support@portfolioboss.com.](mailto:support@portfolioboss.com.)

* * **2.**  **Some Filters can be applied multiple times**; preferably you set each Filter's parameters differently.

!

Other Filters can be applied only once. If you try to add it again, it will be grayed out (on the “Add Sell Filter” dialog):

!

* * **3.**  **A description tooltip appears** when you hover the mouse over a Filter. It's also easy to understand how the Filter's parameters are phrased.

!

If you want to dive deep into the Filters, refer to [Chapter 7](_documentation_about-filters-rules_.md). There we discuss the technical indicator(s) used, the various parameters of each filter, and its real-life applications. Once you understand their mechanisms, you can tweak, mix, and match those Filters.

Keep in mind each Filter is already given default (but sensible) values the moment you add them.

* * **4.**  **There is a checkbox for each Filter** that you can use to enable/disable it. A disabled Filter won't be used by the strategy, despite being listed on this Panel. 

!

This is useful if you're still tweaking the strategy and seeing which Filter may cause lower performance. Backtest the strategy multiple times to see how it performs with and _without_ the Filter. Note, a disabled Filter has its parameters grayed-out so you can't manipulate them.

* * **5.**  **To delete a Filter,** click the trash-bin icon next to it.

!

* * **6.**  **Some Filters have indicator graphs** overlaid on the price chart (at the [Instrument Tab](_documentation_instrument-tab_.md)).

!

!

For example, a Sell Filter stacked at the top of this Panel is labelled “Sell rule #1”, with its indicator lines “25 days EMA” and “50 days EMA” plotted on the chart. These indicators appear alongside other indicators, so if they look confusing, untick the other indicators to hide them.

Some Sell Filters may have their indicators displayed _below_ the price chart, especially those indicators not directly related to the instrument's price. 

!

Note, this chart is initially empty until you clicked a symbol. You can find plenty of symbols to click from the [History Tab](_documentation_history-tab_.md) and the [Stats Tab](_documentation_stats-tab_.md).

* * **7.**  **If a Position hits a Sell Filter,** PB not only gives you a Sell Signal, but a Buy Signal as well to buy into the [cash-equivalent](_documentation_system-settings-panel-guide_.md#positionreplacements) (that is, if your strategy is set to cash-equivalent instead of cash). 

!

!

But if it's a [Continually Switching Strategy](_documentation_system-settings-panel-guide_.md#systemparameter), usually a Sell Signal is accompanied by a Buy Signal to immediately enter the next Position, instead of parking your money into the cash-equivalent.

!

The strategy buys into the cash-equivalent only in rare occasions where none of the instruments passed the Buy Filters, or if their rankings are dismally low.

* * *

#### Notes:

*   Sell Filters are processed with the “OR” operators between them, unlike the [Buy Filters](_documentation_buy-filters-panel-guide_.md) which use the “AND” operators. That means, a Position needs only to hit _one_ of the Sell Filters to be liquidated (even if there are other Filters whose conditions are not met). The idea is that exiting Positions should be easy, otherwise you're in for greater losses.

*   You may show/hide the Filters' header (name), with the button shown below:

!

*   The various Sell Filters in your strategy must be able to cope with a long period of backtest range, in various market conditions. It's a rookie mistake to fine tune the Sell Filters so the strategy performs well at a specific, short term period.

*   As a little technicality you may want to know, Portfolio Boss actually looks at the Sell Filters too when _entering_ Positions, not just the Buy Filters and [Ranking Rules](_documentation_ranking-panel-guide_.md). That is, if any of those instruments also hit the Sell Filters _at the same time_ that it passed the Buy Filters, then the instrument will not be bought.

[**Back to Top**](_documentation_sell-filters-panel-guide_.md#backtotop)

You have already reported this .

#### _documentation_settings-page-overview-guide.md

> Source: https://portfolioboss.com/documentation/settings-page-overview-guide
> Scraped: 3/1/2026, 2:07:52 AM

*   »
*   »
* [Settings Page Overview](_documentation_settings-page-overview-guide.md)

* * *

Discount Applied Successfully!

Your savings have been added to the cart.

Close

#### Block Member?

Please confirm you want to block this member.

You will no longer be able to:

*   See blocked member's posts
*   Mention this member in posts
*   Invite this member to groups
*   Message this member
*   Add this member as a connection

**Please note:** This action will also remove this member from your connections and send a report to the site admin. Please allow a few minutes for this process to complete.

#### Report

You have already reported this .

#### _documentation_simple-moving-average-sma-index-filter.md

> Source: https://portfolioboss.com/documentation/simple-moving-average-sma-index-filter
> Scraped: 3/1/2026, 2:09:13 AM

* * * [!](_wp-content_uploads_2019_10_Simple-Moving-Average-Index-Filter-Buy.png.md)

[!](_wp-content_uploads_2019_10_Simple-Moving-Average-Index-Filter-Sell.png.md)

This filter is similar to the [“Simple Moving Average (SMA) Position Filter”](_documentation_simple-moving-average-sma-position-filter_.md), but instead of calculating the _instrument's_ SMA, this filter calculates an _index's_ SMA, and then looks whether the last closing-price of that index is above or below the SMA, to decide whether or not to trade your Portfolios.

Preferably, the index in question has good correlation to your Portfolios.

Basing your decision on an index gives you more safety as the index represents the market. If the index crosses below its SMA, for example, there's likelihood your Portfolio will cross its SMA too, thus potentially reversing toward the downtrend.

* * **1.**  The first parameter lets you choose an index that you want to look at. For example, you can type SPX here (for S&P 500 index), or RUI (for Russel 1000 index). A dropdown will appear, allowing you to select from the various indices there.

[!](_wp-content_uploads_2019_10_Simple-Moving-Average-Index-Filter-1st-Param-000.png.md)

You can also put here any instrument that may benefit the strategy one way or another. But keep in mind, you can't input a delisted instrument here (indicated by a number suffix inside square brackets). Otherwise a warning will be given and you can't backtest the strategy:

!

* * **2.**  The second parameter defines whether the index's _last_ closing-value must be “Above” or “Below” its SMA to decide whether you will enter or exit Positions.

[!](_wp-content_uploads_2019_10_Simple-Moving-Average-Index-Filter-2nd-Param.png.md)

* * **3.**  The third parameter defines the _period_ that the index's SMA is calculated. For example, you want to see the 200 days SMA of the Index, input a value of 200 days here (type the value and choose from the dropdown whether Days or Months).

[!](_wp-content_uploads_2019_10_Simple-Moving-Average-Index-Filter-3rd-Param.png.md)

* * *

#### Note:

An SMA indicator is displayed on the Price Chart (at the [Instrument Tab](_documentation_instrument-tab_.md)) once you add this filter to your strategy; just click on the little “Chart” icon next to the index symbol in this filter, and you'll see the index's value history with the SMA overlay. 

[!](_wp-content_uploads_2019_10_Simple-Moving-Average-Index-Filter-Indicator.png.md)

Look whether the _current_ index value is above or below that SMA line. Any changes to the SMA period parameter will immediately change this indicator's appearance.

[**Back to Top**](_documentation_simple-moving-average-sma-index-filter_.md#backtotop)

Discount Applied Successfully!

Your savings have been added to the cart.

Close

You have already reported this .

Search

#### _documentation_simple-moving-average-sma-position-filter.md

> Source: https://portfolioboss.com/documentation/simple-moving-average-sma-position-filter
> Scraped: 3/1/2026, 2:09:18 AM

[!](_wp-content_uploads_2019_10_Simple-Moving-Average-Position-Filter-Buy.png.md)

[!](_wp-content_uploads_2019_10_Simple-Moving-Average-Position-Filter-Sell.png.md)

This filter calculates an instrument's Simple Moving Average, and then looks whether the _last_ closing-price is above or below that SMA, to decide whether the instrument will be bought or sold.

Simple Moving Average is a great indicator for establishing the _support_ or _resistance_ line of an instrument.

During an _uptrend_, if the closing-price is _above_ the SMA, the instrument is in the safe zone (trend continues); while if it crosses _below_ the SMA (the support line) the instrument may experience a reversal toward the downtrend.

[!](_wp-content_uploads_2019_10_SMA-Overview-Uptrend_00001.png.md)

The reverse is true during a _downtrend_, in which the SMA acts as the resistance line. Prices rarely go above this resistance line, and if they do, a trend reversal toward the uptrend may happen. 

 [!](_wp-content_uploads_2019_10_SMA-Overview-Downtrend-01_00000.png.md)

Thus, this filter is useful either for trend confirmation, or, when you're looking at a _discount_ when entering a Position (as long as the price dips not too far away below the SMA, it will eventually return above it).

* * **1.**  The first parameter defines whether the instrument's _last_ closing-price must be “Above” or “Below” the SMA for it to be considered. Generally, for a Buy Filter set this to “Above”, since prices above the SMA may indicate the uptrend continues. 

[!](_wp-content_uploads_2019_10_Simple-Moving-Average-Position-Filter-1st-Param.png.md)

For a Sell Filter, set this to “Below” since prices below the SMA may indicate a downtrending instrument.

* * **2.**  The second parameter defines the time-period that the SMA is calculated.

[!](_wp-content_uploads_2019_10_Simple-Moving-Average-Position-Filter-2nd-Param.png.md)

Let's say you want to see an instrument's SMA of the past 200 days, then input a value of 200 days here (type the value, and then choose from the dropdown).

Common SMA lengths are 10, 20, 50, 100, and 200 days. A 200 days SMA is calculated by adding all the closing-prices of the past 200 days, and the result is then divided by 200. So essentially, SMA _smooths out_ the price noises and generates the average.

Keep in mind, deciding the length of the SMA is usually a tricky one: a longer SMA generates fewer signals but most of them are true, while shorter SMA generates more signals but most of them are false. Decide the length based on your trading duration (short term or long term).

* * *

#### Notes:

*   You can use this filter twice, each with a different value. For example, a stock's closing price must be greater than _both_ the 200 days SMA and 100 days SMA to be considered as a buy. This usually generates a greater return while minimizing drawdowns.

[!](_wp-content_uploads_2019_10_SMA-Position-Filter-Twice.png.md)

*   The SMA indicator that you specified here will be overlaid on the Price Chart (at the [Instrument Tab](_documentation_instrument-tab_.md)). Look whether the _last_ closing-price is above or below that SMA line. Any changes you made to the SMA's period parameter will also change the SMA indicator immediately.

[!](_wp-content_uploads_2019_10_SMA-Position-Filter-Indicator.png.md)

*   You may want to include another filter that _further_ confirms whether you're in a downtrend or an uptrend (e.g. the [“Primitive Pattern Filter”](_documentation_primitive-pattern-filter_.md) or the [“Moving Average Cross Over Filter”](_documentation_moving-average-cross-over-filter_.md)).

[**Back to Top**](_documentation_simple-moving-average-sma-position-filter_.md#backtotop)

You have already reported this .

#### _documentation_smi-filter.md

> Source: https://portfolioboss.com/documentation/smi-filter
> Scraped: 3/1/2026, 2:07:44 AM

* * *

!

This filter allows you to enter or exit positions based on the Smart Money activities, as these activities give a clue whether the market is uptrending or downtrending. The Smart Money activities are based on the weekly Commitment of Traders reports that track “Commercial Positions” (from large institutions) and “Non-reportable Positions” (from small traders). The activities are then processed using the proprietary Smart Money Indicator that you find in this filter.

For technical details on how to use this filter, refer to the SMI training module on your [PortfolioBoss.com](index.md) account. As to the philosophy behind the Smart Money Indicator, you may want to read “The Ultimate Crash Detector” report by Dan Murphy. The report is provided as a PDF [here](https://www.dropbox.com/s/509l2ctdte1ohos/The%20Ultimate%20Crash%20Detector.pdf?dl=1), or an audiobook [here](https://www.dropbox.com/s/testi6vnh7l2gbn/Ultimate%20Crash%20Detector.mp4?dl=0).

Note that with restricted licenses, you may not have access to this filter (or its parameters would be limited). To upgrade your license, please contact our Customer Support at [support@portfolioboss.com.](mailto:support@portfolioboss.com)

* * *

#### Notes:

*   Once this filter is applied, two indicators called “SPX Bear Markets” are overlaid on the instrument's [Price Chart](_documentation_instrument-tab_.md). As well, _below_ the Price Chart there's an SMI Chart that shows you the Smart Money activities. There are two indicators on this chart:

*   *   “Net non-reportable positions” which shows the position amount from small speculators (dumb money, which generally you want to make a contrary move from), and
    *   “Net commercial positions” which shows the amount of positions from the large market players and hedgers (smart money, which generally you want to follow).

*   Smart Money activities are derived from the COT reports, and Portfolio Boss has a dedicated service to download these data. If you have trouble with this filter not allowing you to backtest your strategy, it could be that this download service is experiencing problems. You can check the status of that download service with the [**Portfolio Boss Status Page**](https://status.portfolioboss.com/):

!

Discount Applied Successfully!

Your savings have been added to the cart.

Close

You have already reported this .

Search

#### _documentation_software-version-and-updates.md

> Source: https://portfolioboss.com/documentation/software-version-and-updates
> Scraped: 3/1/2026, 2:07:50 AM

[!](_wp-content_uploads_2019_10_About-Buttonn_00000.png.md)

The “About” screen for Portfolio Boss can be accessed by clicking the “About” button (at the top-right corner of the interface). This shows you what PB license you have, the software version, and the software's change-log (update history).

[!](_wp-content_uploads_2019_10_About-Portfolio-Boss.png.md)

You can also check if a newer version of Portfolio Boss is available, by clicking the button “Check for Updates”. If there's a newer public version (not the experimental version), it will be downloaded and installed automatically.

You have already reported this .

#### _documentation_stats-tab.md

> Source: https://portfolioboss.com/documentation/stats-tab
> Scraped: 3/1/2026, 2:08:13 AM

**THIS PAGE IS BEING RENOVATED**

!

This tab shows the _performance_ of those instruments _traded_ by the strategy during the whole backtest period. It shows the gain and holding-duration statistics for their Positions. So, before we entered them as Positions we could only guess how they would perform. But here you have a 20/20 “hindsight” on the true colors of these instruments, once they're subjected to your trading theory & system. But it's recommended not to cherry-pick them to be part of your future portfolio, that is, sift out the losers and retain the winners.

This tab is located at the Reports Area of the “Backtest Strategy” page:

!

As usual, this tab is only populated once the strategy is backtested (by clicking the “Start” button at the top of this page).

* * **1.**  **Instrument:** this column lists all the instruments that had been entered as Positions. Those instruments (on the strategy's [portfolio](_documentation_instruments-panel-guide_.md)) that were never entered as Positions aren't listed here.

!

This is a good place to click a symbol and load it to the [Instrument Tab](_documentation_instrument-tab_.md), so you can analyze how that instrument reacted to the various indicator lines there. You can then adjust your strategy accordingly. But note, while you're adjusting the strategy (and backtesting it numerous times), reserve a big chunk of the available data to be unseen by Portfolio Boss. You can do this through the [**super out-of-sample method**](_documentation_backtest-panel-guide_.md#superOOS).

As usual, you can hover your mouse over a symbol to see its description tooltip:

!

* * **2.**  **Total Gain:** this shows each instrument's total gain from all its Positions (up to the backtest end-date).

!

Each Position's gain is calculated from the entry price (Buy) to the exit price (Sell). If the latest Position isn't closed yet, the gain for that Position is gauged by the _closing price_ on the latest backtest date. All prices are adjusted price.

!

But keep in mind, the calculation for “Total Gain” is not as simple as adding together each Position's gain or loss. It also takes into account the growth of your investment due to the previous Positions' gain. Hence the “Total Gain” you see here is a percentage for the very first Position's initial fund size (weight).

The calculation for the very first Position is:

`Total Gain = 1 * (1 + Position Gain)`

Then for the subsequent Positions:

`Total Gain = Previous Total Gain * (1 + Position Gain)`

The resulting final value is then subtracted from 1, to give you this “Total Gain” percentage for each symbol.

For example: AAPL had three Positions, each with a gain of 2%, 5%, and 3%. The “Total Gain” in relation to AAPL's initial fund size of, let's say $10,000, would be 10.31% or **$1,031**. If we simply add together 2% + 5% + 3% we'd get 10%, or **$1,000**, which would be incorrect, as it doesn't include the growth of your account (due to previous Positions' gain/loss).

* * **3.  Avg Daily Gain:** this column shows the average daily gain (or loss) for all Positions of the instrument.

!

It's **not simply** the total gain divided by the total duration of those Positions, because that still wouldn't be representative of the average daily gain vis-à-vis your account growth. The calculation is rather complex:

**A.** “Total Gain” is divided by 100, to become a factor of 1. Then add 1 to the result.

**B.** Find the percentage that 1 day represents out of the total duration, so 1 is divided by the total duration.

**C.** Then raise A to the power of B, that is: A ^ B. Then subtract the result by 1.

**D.** Finally to make it a true percentage (not a factor of 1), multiply C by 100.

* * **4.  Total Days Held:** here's the total duration (in days) that each instrument was held as Positions. Obviously it excludes holidays and weekends.

!

If the latest Position isn't closed yet, its duration is from the day it's entered up to today (or the backtest end-date).

* * **5.  Avg Days Held:** this column tells you the average duration of the Positions (in days), for each instrument.

!

It's simply the total days it's held as Positions, divided by the number of Positions.

* * **6.  Winning Positions:** it shows the number of _profitable_ Positions that each instrument yielded.

!

Profitable is when the exit price is higher than the entry price (if going long). Or if it's a short Position, exit is lower than entry. For a Position not yet closed, the closing price today is the gauge whether it's profitable or not.

* * **7.  Losing Positions:** this column shows the number of unprofitable Positions each instrument yielded.

!

* * **8.**  **At the bottom** of this tab there's a section for _total statistics_: 

!

*   **Total instruments:** The number of distinct instruments entered as Positions, including the cash-equivalent instrument.
*   **Total positions:** The number of Positions entered.
*   **Average trading days held:** how long each Position lasts on average, and
*   Average Gain (shows the average gain for all Positions). \[BOOKMARK\]

The “Winners” column shows those statistics for profitable instruments (or Positions), whereas the “Losers” column is for unprofitable instruments (or Positions). 

[!](_wp-content_uploads_2019_10_Winners-and-Losers.png.md)

For example, as shown in the picture, there are 510 profitable instruments v.s. 186 unprofitable instruments, and there are 6,779 profitable Positions v.s. 3,165 losing Positions.

* * *

#### Note:

*   All columns here are sortable by clicking the columns' header. For example, if you want to sort instruments from A to Z or from Z to A, or sort based on the highest returning instruments, etc.

[**Back to Top**](_documentation_stats-tab_.md#backtotop)

You have already reported this .

#### _documentation_stochastic-oscillator-filter.md

> Source: https://portfolioboss.com/documentation/stochastic-oscillator-filter
> Scraped: 3/1/2026, 2:09:07 AM

!

!

The Stochastic Oscillator Filter is a momentum oscillator that attempts to predict turning points in the instruments' price, or to identify a trend's strength. It functions similarly as [RSI](_documentation_rsi-filter_.md); and its value oscillates between 0 and 100. It was developed by George Lane in the late 1950's.

This oscillator is calculated by first identifying the highest and lowest price in a given period. The latest closing price is then expressed as a point within such highest & lowest range; this is the Stochastic's value. A value of about 0 indicates the closing price falls near the bottom of the range, and a value close to 1 indicates it falls near the top of the range. In PB, such highest and lowest prices come from the literal highest & lowest wicks that the daily candles have.

!

As shown in the example above, the latest Stochastic value is calculated by: finding the difference between the latest closing price and the lowest price of the period, and this is divided by the difference between the highest and lowest prices of the period. The resulting value is often referred to as **%K**.

There's a second indicator line, referred to as **%D**, calculated by smoothing the %K with a Moving Average (usually SMA or EMA, of the last 3 days). Both %K and %D are shown below the price chart on the [Instrument Tab](_documentation_instrument-tab_.md).

!

There are various interpretations of the Stochastic indicator. One interpretation calls for the %K (or %D) to cross above/below the overbought or oversold area (usually a value of 0.8 and 0.2, respectively), before a signal is given. Another interpretation looks at the %K and %D crossing above/below each other. And then there are those that combine both, as an advanced form of RSI: Buy when %K goes in the oversold, accompanied by a crossing above the %D; and sell when it goes in the overbought, accompanied by a crossing below the %D. Still there is another interpretation that looks at divergences between the price action and the %K movement: whether the price creates lower _lows_ while %K creates higher _lows_ (bullish), or the price creates higher _highs_ while %K goes lower _highs_ (bearish). Though this divergence method isn't modelled in PB.

Essentially, the main idea is this: The momentum a.k.a. speed of the price (as represented by Stochastic) changes _before_ the price itself changes. Therefore if the momentum is strong: you see the %K (or %D) goes near the extreme (1 or 0) for an extended period. It's best to just follow such a strong trend instead of anticipating its turning point.

Let us now discuss this filter's parameters, starting from the easiest to understand:

* * **1.  %K Period:** This defines the period for calculating the %K.

!

In other words, the filter will identify the highest price and the lowest price within such period, and then the latest closing price falls within such high-low range. Obviously it's a moving period. The typical value here is either 5, 9, or 14 days.

* * **2.  %K Slowing Period:** This parameter modifies the %K into either a Slow Stochastic or a Fast Stochastic.

!

With a value of 1, the %K is calculated the usual way, no slowing. It's what people call the Fast Stochastic. But some technicians swear that it generates less reliable signals, resulting in whipsaws. So they decided to slow it down (usually) by a value of 3 days here; this is the Slow Stochastic, which is smoother than its sibling. So when it's set higher than 1, %K is calculated by averaging the highest-high and the lowest-low over the number of this period before performing the division. The maximum period here is 10 days.

* * **3.  %D Period:** This defines the Moving Average period for smoothing the %K, which results in %D line.

!

So whatever values spit out as %K (either slowed or not), will be smoothed out to yield the %D. Most technicians use a period of 3 days here, which means the %K value of the last 3 days are averaged.

* * **4.  %D MA Type:** This defines the type of Moving Average to produce the %D.

!

Here you can choose either SMA (Simple Moving Average) or EMA (Exponential Moving Average). So the %K of the past certain days will be smoothed by either SMA or EMA to produce the %D. You can't go wrong with one or the other, the difference is miniscule. Though the general wisdom says for a volatile portfolio (like small-cap stocks or the Nasdaq 100), you're better off using EMA, as it puts more weight on the _latest_ %K values.

* * **5.  Mode:** This should be the first parameter you set when you use this filter. It defines the method (interpretation) for using the Stochastic indicator.

!

Changing the mode reveals or hides certain parameters. There are two modes in the PB version of the Stochastic:

*   **High/Low Ranges for %K or %D**   **Crossing %K and %D Lines**

The former utilizes overbought & oversold (or any threshold) values for _either_ %K or %D. The latter identifies crosses/intersections between %K and %D; whether one goes below the other. You can combine both modes by applying the filter multiple times (especially as Buy Filters), each with a different mode and parameters than the other.

We'll explore each mode in the following sections, along with the best parameters' values for them.

* * **6.  Mode – High/Low Ranges for %K or %D:** This mode lets you use Stochastic with the overbought/oversold areas (or any threshold value).

!

It's an advanced version of the RSI: that the %K (_or_ %D) must punch through the overbought/oversold line, and then falls back through the same line within a specified period. As shown in the screenshot above, this mode has **four parameters** specific to it (orange box highlighted). From left to right:

*   The 1st parameter defines whether it's the %K or %D that will cross the threshold value.
*   The 2nd parameter defines whether it (%K or %D) rises above _and then_ falls below the threshold value, or vice versa: it falls below _and then_ rises above the threshold.
*   The 3rd parameters: See there are two parameters set to **20.00** in the screenshot above; if you set one parameter, the other is automatically set with the same value. These define the threshold value. Overbought is usually around 80, while oversold is around 20 (you can set this anywhere from 0 to 100).
*   The 4th parameter defines the period _in which_ the %K (or %D) must _cross-back_ the threshold value. That means, the _first time_ it punched through the threshold does not necessarily happen within such a period.

!

General wisdom says if the indicator goes above the overbought and shortly after falls below it, it's bearish. And if it goes below the oversold and then rises above it, it's bullish. Our tests indicate that for a Buy Filter, it's _generally_ good to use %K (instead of %D), which should fall below then rise above a threshold value of 60 to 90, within 140 to 150 days. As for the Sell Filter, apparently it's best to use %D that rises above then falls below a threshold of 40 to 60, within 130 to 170 days.

!

But again, this is just a rough rule of thumb whenever this Stochastic is used simultaneously as a Buy and a Sell Filter. You must find better values if your strategy contains additional rules & filters.

As a side note, if you want to use Stochastic the way RSI is used, that is, the indicator simply goes in the overbought or oversold zone without falling back, you can set it so the indicator line have its _first cross_ from the outside, that is from beyond the overbought/oversold zone:

!

In the example above, you set the first three parameters (as bounded by the red rectangle) so that the %K rises above the oversold of 0.25. That implies that %K attacks _from below_ the oversold (at any time in the past, not necessarily within the set period). Then, _within_ the set period it must fallback below the oversold, which is the actual trigger for the Buy Signal.

* * **7.  Mode – Crossing %K and %D Lines:** This mode generates trading signals from the crossovers between %K and %D. So this does not utilize overbought & oversold areas.

!

It's similar as in [MACD](_documentation_macd-filter_.md) where signals are given when the MACD line crosses above/below the Signal line, but here you can choose what indicator to cross which line. As shown in the screenshot above, there are two parameters specific to this mode (contained in the orange boxes). From left to right:

*   The first parameter lets you choose the indicator line that actively crosses above/below. If you choose %K, it will cross above/below %D to generate the signals. If you choose %D, it will cross above/below %K for the signals.
*   The second parameter defines whether the active line must “rise above”, or “fall below”, the other line, for the signals to be generated.

!

The general wisdom says it's bullish if %K crosses above %D, and bearish if %K crosses below %D. Our tests showed that it's good to buy if %K _falls below_ %D, and sell if %D _falls below_ the %K. Though once again, this depends on your other rules, filters, parameter values, and portfolio. We used the Stochastic simultaneously as a Buy and Sell Filter:

!

* * *

### Note:

You can combine both modes, so that the indicator line must do two types of crossing before a signal is given: it must cross the overbought/oversold, and, it must also cross the %D (or %K) as a confirmation. Simply apply two Stochastic Buy Filters, one set to use the mode “High/Low Ranges…” and the other set to “Crossing %K and %D…” :

!

Since the criteria are constricted even more, this may reduce drawdown and improve the consistency of your strategy. You can't use this trick as Sell Filters, because they don't combine the criteria for exiting positions. If just one criteria is triggered, the position is sold at the next market open.

[**Back to Top**](_documentation_stochastic-oscillator-filter_.md#backtotop)

You have already reported this .

#### _documentation_strategy-in-market-filter.md

> Source: https://portfolioboss.com/documentation/strategy-in-market-filter
> Scraped: 3/1/2026, 2:07:41 AM

*   »
*   »
* [Strategy in Market Filter](_documentation_strategy-in-market-filter.md)

* * *

This page is currently under construction.

Discount Applied Successfully!

Your savings have been added to the cart.

Close

#### Block Member?

Please confirm you want to block this member.

You will no longer be able to:

*   See blocked member's posts
*   Mention this member in posts
*   Invite this member to groups
*   Message this member
*   Add this member as a connection

**Please note:** This action will also remove this member from your connections and send a report to the site admin. Please allow a few minutes for this process to complete.

#### Report

You have already reported this .

#### _documentation_strategy-management-page-overview.md

> Source: https://portfolioboss.com/documentation/strategy-management-page-overview
> Scraped: 3/1/2026, 2:07:59 AM

!

This page lists all the s_trategies_ you have, either the ones bundled with your license, or those you created yourself. To open this page, click the “Strategy Management” button ! at the left sidebar.

This is where you choose a strategy to be used in your trading. It also allows you to manage your strategies: create and delete a strategy, duplicate it, create a backup file, or _reset_ a strategy to its default settings. Please refer to [this guide for more details](_documentation_managing-your-strategies_.md) on how to manage your strategies.

* * *

All strategies bundled with your license are listed under **Licensed strategies** group. These licensed strategies are created by the Portfolio Boss team. They have been backtested thoroughly, and put to test with real money, so you know you're in the right hands when using these strategies.

!

Any strategies that you created yourself (or if you _duplicated_ any of the licensed strategies) are listed under the **My strategies** folder. You can add or remove folders and subfolders, and collapse or expand them to help you more effectively view and access your strategies.

The ‘Show tree' toggle option ![Show tree toggle switch](https://portfolioboss.com/wp-content/uploads/2024/04/Show-Tree.jpg)allows you to see all your strategies in a single list (when off) or to see them in a nested folder structure (when on).

The strategies are described in five columns:

![Strategy Management Page - Five Columns](https://portfolioboss.com/wp-content/uploads/2024/04/Strategy-Management-Page-Five-Columns-1024x441.jpg)

**1.**  **Name:** shows the strategies' names.

**2.**  **Type:** shows the type of the strategies, either “Basic”, “Multi”, or “Meta”. We will discuss this in a [next page](_documentation_types-of-strategy_.md).

**3.** **Data Source:** shows the data source for the strategy's Portfolios; either CSI or Yahoo.

**4.**  **Notifications:** turn ON any of these toggles to receive trading signals (via e-mail) from that strategy. This is similar to the [Send Notifications](_documentation_strategy-panel-guide_.md#enablenotif) toggle in the Backtest Strategy page.

**5\. Description:** shows the description of each strategy.  

Strategies that contain errors will be highlighted in red text. By hovering over the strategy, you can read a bullet point summary of what needs to be fixed. Also note there is a ‘Show errors only' switch !in the top right corner that will filter all visible strategies so you can focus on the ones that need attention.

Additionally, you can search any strategies by typing in the “Search strategies” field (in the top-right corner) **\[1\]**. By default, the search bar looks at instruments, portfolios, and strategies. Click on Strategies **\[2\]** to expand matches within the search window. The folder structure will also be filtered in real-time based on your search term. To view the _full list_ of strategies again, clear the search term from the search bar.

!

* * *

#### Notes:

*   The strategies can be sorted based on any of the five columns simply by clicking on the column name. When you duplicate or create a new strategy, it may not be sorted in the right order. Simply revisit this page again (after opening the Backtest Strategy Page ! for example), and it will be sorted correctly.

*   You can right click any of the scrollbars (throughout PB), and a context menu appears. “Scroll Here” lets you scroll the content to to the location you right clicked at. “Top” scrolls to the top of the content; while “Bottom” to the bottom. “Page Up” reveals a part of the content upward starting from where it was hidden, while “Page Down” reveals the content downward. “Scroll Up” scrolls upward by a little increment, while “Scroll Down” scrolls downward a little step.

!

     Horizontal scrollbars have different options' name, but the idea is similar.

[**Back to Top**](_documentation_strategy-management-page-overview_.md#backtotop)

You have already reported this .

#### _documentation_strategy-panel-guide.md

> Source: https://portfolioboss.com/documentation/strategy-panel-guide
> Scraped: 3/1/2026, 2:07:55 AM

!

This panel is located at the top-left corner of the [Backtest Strategy page](_documentation_backtest-strategy-page-overview_.md). It's the “identification” panel of the strategy, where you can give it a name and description. Such identifications will be visible on the [Strategy Management](_documentation_strategy-management-page-overview_.md) list.

!

This panel also defines whether the strategy will send email notifications (trading signals) to you. As well, it allows you to override (or reinstate) the strategy's read-only mode.

Note, the panel's heading (name) conforms to the [strategy type](_documentation_types-of-strategy_.md) (multi, basic, or meta strategy):

!

!

!

* * **1.**  **To rename** the strategy, type it on the “Name” field:

!

If you leave the field empty, the strategy will revert to its current name (the next time you open its Backtest Strategy page), though you can still backtest the strategy even if the field is empty.

!

* * **2.**  **Write the strategy's description**, like its mechanism or purpose, on the “Description” field.

!

* * **3.**  **To receive daily emails** from the strategy (containing trade signals & current positions), set the Notifications property to “Daily email”.

!

Keep in mind, if a strategy is set to “Daily email”, its rules are grayed out, and you can't edit them. This is the _read-only_ mode, so users don't accidentally edit an active strategy (to prevent the running Positions and history to change).

Any strategies set to “Daily email” will give you such email notifications. Just let Portfolio Boss run a few hours after the markets close (e.g. until 6 or 7 PM Eastern Time). Once the End of Day data are downloaded, those strategies are automatically backtested to send you the daily email. Here's an example of the email:

!

1.  Clicking the link brings you to the Portfolio Boss forum.
2.  It shows the earliest and latest backtest date (today).
3.  This is the day & date when you should execute the trading signals (if there's any).
4.  This lists the strategies whose notifications are bundled with this email, along with their daily gain/loss (change of account size today vs yesterday). If there are trading signals, it says “New trades!”, otherwise “No trades”. If you enabled daily email for multiple strategies, usually they're bundled in a single email, but sometimes they're sent separately.
5.  It shows the trading signals for the strategy. It's only shown if there are indeed trading signals. [Multi](_documentation_multi-strategy_.md) or [meta](_documentation_meta-strategy_.md)\-strategies also have the component-strategy listed here, of whom the trading signals (symbols) belong to.
6.  Here's the list of the Positions currently held by the strategy, along with their gains and holding duration. For meta-strategies, their component-strategies are listed here instead of the actual instruments.
7.  It's the top ranked instruments list (based on the [Ranking Rules](_documentation_ranking-panel-guide_.md)); it's the instruments you'll enter as Positions should the old ones are closed. Multi-strategies don't have this, obviously. And meta-strategies have their component-strategies listed here instead of the actual instruments. This section isn't shown if none of the instruments passed the [Buy Filters](_documentation_buy-filters-panel-guide_.md).

Now, as stated earlier, the strategy is put to read-only mode if daily email is enabled. If you wish to edit the strategy, click the “Override read-only mode…” (as shown in a previous screenshot, orange rectangle), and a confirmation dialog appears:

!

Simply click “I Understand”, and the rules will be customizable again. Once done with the editing, you can click the button “Restore read-only mode” to reinstate the mode:

!

Though this is done automatically (no need to press that button) once you navigate away to the other strategy.

* * *

#### Notes:

*   If email notifications don't reach you, you may want to check [**Portfolio Boss Status Page**](https://status.portfolioboss.com/). See if the Mailing Service is running smoothly. If it is, you may want to check the help page for [**Automation Tab**](_documentation_automation-tab-guide_.md) before contacting [Customer Support](mailto:support@portfolioboss.com).

!

*   If you're still running (trading) the strategy, instead of overriding the read-only mode it's better to just copy the strategy and only edit the duplicate:

!

To do that, click the “Copy” button at the top of the Backtest Strategy page, and a dialog appears: Give the copy a name, and tick the checkbox “After copying…” (if you want to immediately open the duplicate), then click the “Copy” button.

*   Any strategy that's part of a multi-strategy has the read-only mode set by default. This is to prevent unintended position changes of the parent strategy:

!

[**Back to Top**](_documentation_strategy-panel-guide_.md#backtotop)

You have already reported this .

#### _documentation_surprise-day-filter.md

> Source: https://portfolioboss.com/documentation/surprise-day-filter
> Scraped: 3/1/2026, 2:09:15 AM

[!](_wp-content_uploads_2020_08_Surprise-Day-Buy-Filter.png.md)
[!](_wp-content_uploads_2020_08_Surprise-Day-Sell-Filter.png.md)

Surprise, surprise! There's a gap!

This filter identifies a “breakaway gap” in the instrument's candlestick chart. The day that the gap happens is the “Surprise Day”. Its criteria are as follows:

*   The opening price is higher than the previous day's closing price, thus an upward momentum.
*   The closing price is higher than its opening price, therefore it must be a green candlestick.
*   Its volume (of shares) is more than twice the average volume of 1 month.
*   The distance between its closing price and the previous day's closing price is more than 2 times the average volatility of 1 month. This ensures there's indeed a big gap from the previous day's candle.

[!](_wp-content_uploads_2020_08_Yuge-Gap-Sample.png.md)

Such an upside “breakaway gap” with heavy volume indicates a strong bullish momentum. But keep in mind that most gaps are eventually “filled”. That is, subsequent prices (after a few days or weeks) may drop to close that gap (or at least to approach that gap). The crowd psychology during the gap is one of hysteria; everybody wants to jump on the bandwagon. But eventually common sense prevails and the price corrects itself.

[!](_wp-content_uploads_2020_08_Testing-the-Gap.png.md)

[!](_wp-content_uploads_2020_08_Gap-is-Partially-Filled-123-1.png.md)

[!](_wp-content_uploads_2020_08_Gap-is-Completely-Filled-123.png.md)

Before you jump in to buy, it's better to wait a certain period so you won't get whipsawed by the temporary downdraft that happened after the gap.

The way this filter is constructed, it does not identify “common gaps” (small gaps with small volume) which are technically insignificant. So with this filter, you're more likely to jump into a strong uptrend.

* * **1.**  The first parameter defines whether the Buy/Sell signal should be given in “Less Than” the threshold waiting period, or “More Than” that period.

[!](_wp-content_uploads_2020_08_Surprise-Day-First-Parameter-123.png.md)

For example, as in the screenshot above, “Less Than 20 days” means the signal could be given within 20 days after the Surprise Day happened. It could be 1 day after the Surprise Day, or 3 days, 19 days, etc. “More Than 20 days” means you'll wait 20 days minimum before the signal is given, so it could be 21, 25, or 50 days (after the Surprise Day) before the signal is given.

Generally, “Less Than” is good for a Buy Filter, while “More Than” is good for a Sell Filter.

* * **2.**  The second parameter defines the threshold waiting period.

[!](_wp-content_uploads_2020_08_Surprise-Day-Second-Parameter.png.md)

For a Buy Filter, it's best to set this to a longer period, let's say 100 days (or longer). Thus combined with the parameter “Less Than” (as explained previously), the Buy Filter will give the signal in “Less Than 100 days” after the Surprise Day occurred.

[!](_wp-content_uploads_2020_08_Surprise-Day-Buy-Less-Than-100-Days.png.md)

The idea is this: we don't know how long a gap would be filled (or tested). So with a wider window, that is, within 100 days after the gap (it could be 1 day, 50 days, 70 days, etc) we're giving a bigger leeway for the price to complete the retracement (to test the gap). We patiently wait before we jump in. Otherwise we may get caught in the temporary downtrend, if we use a shorter period.

Thus it follows that a Buy Filter could also be set to “More Than”, paired with a short period, let's say “9 days”:

[!](_wp-content_uploads_2020_08_Surprise-Day-Buy-More-Than-9-Days.png.md)

But this could mean we're waiting too long. Because “More Than 9 Days” is either 11 days, 50 days, or 300 days and more! If it's too long, we're jumping in when the bull trend is already exhausted. So it's still best to use the previous form (“Less Than 100 Days”) for a Buy Filter.

Now if you use this as a Sell Filter, it's best to set “More Than”, paired with a longer period. For example 70 days or longer:

[!](_wp-content_uploads_2020_08_Surprise-Day-Sell-More-Than-77-Days.png.md)

There are two reasons for this form of the Sell Filter:

*   With such a long period (after the Surprise Day happened), the uptrend is more likely exhausted. So we sell.
*   Some chartists believe in the idea of a “Measuring Gap”. That is a gap that happens halfway of an uptrend's length. So by waiting a certain period after the Surprise Day, we can “measure” where the cliff would be.

[!](_wp-content_uploads_2020_08_Surprise-Day-Measuring-Gap_00000.png.md)

* * *

Breakaway-gaps are extraordinary events. But their role should not be overemphasized. Sometimes it's a good idea to use other filters, to confirm that such a gap occurs at a young bull market instead of an old, exhausted one.

A breakaway gap that happens after a trading-range gives a strong confirmation that a new bull market has emerged, with tremendous upside momentum. But such an event may be rare, and a strategy based on it would stay in cash most of the time, yielding underwhelming performance.

Still we can get the next best thing: at least we make sure the Surprise Day does not happen at an exhausted uptrend. For example, instead of using RSI Buy Filter to signify a young bull trend (buy if RSI is less than 40, and there's a Surprise Day recently), we put the RSI as a Sell Filter to signify an exhausted bull trend (do not enter a position if RSI is greater than 70). Remember that an instrument that triggered a Sell Filter in the same time it fulfilled the Buy Filter, won't be entered as a Position.

[!](_wp-content_uploads_2020_08_Surprise-Day-and-RSI.png.md)

* * **Notes:**   The way this filter is constructed, there's no way it could identify multiple-gaps pattern (multiple gaps could signify exhaustion, or the island reversal pattern, etc). In fact, this filter can't be applied more than once (for each Buy or Sell Filters Panel).
*   If you look at the [Instrument Tab](_documentation_instrument-tab_.md), there's an arrow above the candlestick signifying a “Surprise Day”. That's when the gap happens.

[!](_wp-content_uploads_2020_08_Surprise-Day-Indicator.png.md)

[**Back to Top**](_documentation_surprise-day-filter_.md#backtotop)

You have already reported this .

#### _documentation_sync-details-search-results-panel.md

> Source: https://portfolioboss.com/documentation/sync-details-search-results-panel
> Scraped: 3/1/2026, 2:08:10 AM

!

These panels are hidden by default. They're located at the bottom of the Portfolio Management page, both occupying the same space. So if one panel is shown, the other is hidden.

[https://portfolioboss.com/wp-content/uploads/2021/08/g7ui5e6whq677.mp4](_wp-content_uploads_2021_08_g7ui5e6whq677.mp4.md)

**To open the “Search Results” panel,** type anything on the “Search” field (at the top-right corner of this page).

You can type a Portfolio's name to find it quickly, or you can type an instrument's symbol, corporation's name, exchange (market) name, or asset-class, to find instruments that match any of those search terms. The result will be displayed on this “Search Results” panel.

!

This panel always shows five columns populated, regardless of your search term:

**1.**  **The Portfolio column** lists all _Portfolios_ that match your search term. For example, you're searching for a Portfolio called “Cloud Computing”, then that Portfolio will be listed on this column. If you're looking for a specific instrument, like AMZN, this column lists the Portfolios _that contain_ the instrument. Simply click any of the Portfolios listed, and that Portfolio will be selected (on the “Portfolios” panel) with its instruments shown (on the “Portfolio Instruments” panel); this “Search Results” panel then disappears.

**2.**  **The Symbol column** shows the symbols (tickers) that match your search term. Click any of the symbols and it will bring you to the [Instrument Chart panel](_documentation_instrument-chart-panel-guide_.md) for that instrument (you can also click on the little-chart icon !  ). The Portfolio in which that symbol resides will also be selected (at the “Portfolios” panel).

**3.**  **The Description column** shows the description for that instrument (usually the company name).

**4.**  **The Exchange column** shows the market/exchange where the instrument is traded.

**5.**  **The Type column** shows the asset-class for that instrument (stocks, ETF, ADR, etc.).

Note, Portfolios only have the “Portfolio” column showing their name (other columns are empty, or described as “Unknown”).

* * **Now, the Sync Details panel:** it simply lists the synchronization activities, i.e. instruments' price data being downloaded. To access this panel, click the “Sync Details” button at the top-right corner of this page:

!

The number on that balloon tells you the amount of instruments that's _finished_ downloading. And you can see such events on this panel:

!

Usually this panel shows just those download activities that you initiated yourself (by clicking an instrument from the [Portfolios Instruments Panel](_documentation_portfolio-instruments-panel-guide_.md)). These are instruments that PB does not download automatically (behind the scene), as they're not part of any strategy.

If there are problems with the historical price data download (or synchronization of Dynamic Portfolios), you may want to check the [**Portfolio Boss Status Page**](https://status.portfolioboss.com/):

!

[**Back to Top**](_documentation_sync-details-search-results-panel_.md#backtotop)

You have already reported this .

#### _documentation_system-requirements-installation.md

> Source: https://portfolioboss.com/documentation/system-requirements-installation
> Scraped: 3/1/2026, 2:07:56 AM

!

## System Requirements

Portfolio Boss is lightweight, it can even run on the cheapest hardware. But if you plan on trading complicated strategies with huge Portfolios, we recommend a mainstream multi-core system with at least 8 GB of RAM. The more CPU core and memory you have, the merrier.

Portfolio Boss runs natively in Windows operating-system. It also works on Mac with a virtualization app that runs Windows ([Apple's Boot Camp](https://support.apple.com/boot-camp), [VM Ware Fusion](https://www.vmware.com/products/fusion.html), or [Parallels](https://www.parallels.com/)).

* * *

## Installing Portfolio Boss

**1\.** Head over to Portfolio Boss [download page](_download_.md).

**2\.** Choose your plan and fill out the necessary information.

**3.** Download the installer with the download link provided.

**4\.** Once it's downloaded, double-click to start the installation.

**5\.** Follow the installation procedure.

**6\.** When you launch Portfolio Boss for the first time, you need to enter the email and password that you've entered previously.

You're done!

* * *

#### Notes:

*   You have essentially 30 days to try out Portfolio Boss, during which you may request a **full refund.** No questions asked! Please refer to our [Refund Policy](_refunds_.md) page.

*   For any inquiries, please contact our support team at [support@portfolioboss.com](mailto:support@portfolioboss.com).

You have already reported this .

#### _documentation_system-settings-panel-guide.md

> Source: https://portfolioboss.com/documentation/system-settings-panel-guide
> Scraped: 3/1/2026, 2:08:08 AM

!

This panel is located at the [Rules Area](_wp-content_uploads_2021_05_gdg56ye5dg_00000_00000.png.md).
It's used for defining the _general rules_ of the strategy:

*   whether it enters fresh new Positions each month,
*   the number of Positions to hold at any given time,
*   whether it's trading [long or short](https://www.investopedia.com/ask/answers/100314/whats-difference-between-long-and-short-position-market.asp) Positions,
*   the instrument to enter when Positions are closed,
*   calculating the [Limit Order's](https://www.investopedia.com/terms/l/limitorder.asp) prices,
*   and more.

* * **1.**  **System:** this rule defines whether the strategy switches (replaces) Positions _periodically_ at a certain date of the month, or, switch Positions continuously when any of them hits the [Sell Filters](_documentation_sell-filters-panel-guide_.md).

!

If you have a restricted license, you may not see this rule. Thus your strategy will be locked in either Periodic or Continual switching (based on your license). Please contact our Customer Support at [support@](mailto:support@portfolioboss.com)[portfolioboss.com](mailto:support@portfolioboss.com) if you wish to upgrade your license. 

!

The “Periodically Switch Positions” will replace all _old_ Positions with _new_ Positions during the switch-date (each month). So old Positions will be sold during this switch-date (even if they're still safe, not triggering the Sell Filters), and then you buy new instruments to replace them.

[https://portfolioboss.com/wp-content/uploads/2021/10/b7u8d567hsa.mp4](_wp-content_uploads_2021_10_b7u8d567hsa.mp4.md)

If a Position hits a Sell Filter _before_ the switch-date, you'll receive a signal to exit that Position and then buy the [cash-equivalent](_documentation_system-settings-panel-guide_.md#cashequivalent) instrument.

!

These _new_ Positions are selected based on the strategy's [Buy Filters](_documentation_buy-filters-panel-guide_.md) (or Short Filters, if it's a short strategy); instruments that passed the Buy Filters are then ranked with the [Ranking Rules](_documentation_ranking-panel-guide_.md). If the strategy holds open, say, **10** Positions at any given time, then PB will recommend the **top 10** (ranked) instruments for you to buy. Take a look at [this diagram](_wp-content_uploads_2019_10_Buy-Sell-and-Ranking-Rules-Diagram_00000.png.md).

Keep in mind, _all_ instruments within the strategy's Portfolio will be tested by the Buy Filters and then ranked by the Ranking Rules. So if an old Position (the old instrument) passes the Buy Filter again and ranks in the top 10, PB will tell you to _hold_ that Position instead of replacing it.

!

The idea for periodic switching is that you're _not bound_ to your current Positions (unless a Sell Filter is triggered), lest there are more profitable Positions to enter. PB will look for more profitable Positions based on the Buy Filters and Ranking Rules.

In short, you don't want wasted opportunities by clinging onto your current Positions for too long. Another advantage is that your trades _mostly_ happen on a single, certain day of the month, thus reducing commission fees as well as minimizing slippage.

Another reason for periodic switching is that all Positions' weight (the money contained in each of them) will be distributed equally at the switch day. So if a Position wins huge, its gain will be used to fund the other Positions as well, instead of being locked into it in a lopsided weighting (which is the case in a continuously-switching strategy, unless all Positions meet their exit and all are parked into cash/cash-equivalent).

!

Now, if you choose “Continuously Switch Positions”, only Positions that triggered the Sell Filter will be replaced with the new Positions; there's no such thing as a switch-day. It allows you to ride a Position all the way through until the condition to exit is met. It is especially useful if you want to capitalize on short-term price fluctuations (thus a more frequent trading), or, if you firmly believe in a Position's setup for entry and exit (hence riding it through no matter what).

[https://portfolioboss.com/wp-content/uploads/2021/10/gy7ui56r7r4w5h.mp4](_wp-content_uploads_2021_10_gy7ui56r7r4w5h.mp4.md)

If a potentially-profitable new Position is found, PB will recommend you to enter that Position. If no profitable replacement is found, PB will recommend you to buy into the cash-equivalent.

Once a cash-equivalent Position is entered, PB continuously looks whether there is a more profitable position than the cash-equivalent (based on the Buy Filters and Ranking Rules). If that's found, the cash-equivalent will be sold, and you'll buy the new Position. Such potentially-profitable instruments can be found on the [Trade Signals Tab](_documentation_trade-signals-panel-guide_.md) as shown below:

!

Regardless of Periodic or Continually Switching strategies, it is highly recommended that you use a [Margin Account](https://www.investopedia.com/terms/m/marginaccount.asp) at your broker, instead of the [Cash Account](https://www.investopedia.com/terms/c/cashaccount.asp). This is because a trade's liquidated-fund requires a Settlement Date (usually 2 days after the trade is executed). You can use unsettled funds to enter new Positions, but these Positions can't be liquidated before the said funds are settled. Since Portfolio Boss's Positions _may be_ switched in quick successions, you may commit Good Faith Violation (or Free Riding Violation) unknowingly.

A Margin Account solves that problem as you can enter and exit Positions freely without waiting for the funds to settle (by borrowing from your broker). If you _must_ use a Cash Account for whatever reason, set aside some part of your fund (as reserve cash, instead of trading all your cash) to enter and exit Positions recommended by PB while waiting for the previous funds to settle.

**Note:**

A continuously-switching strategy requires that you have _at least_ one [Sell Filter](_documentation_sell-filters-panel-guide_.md). Otherwise there's a red warning and you can't backtest the strategy:

!

* * **2.**  **Total Positions to Hold:** this rule defines the number of Positions the strategy holds at _any_ given time.

!

You set this number based on your account size, risk tolerance, and the Portfolios you're trading. Smaller accounts need only to hold 3 to 6 Positions at any given time. _Increasing_ this number also lets you diversify, thus potentially reducing risk (drawdowns), at the expense of potentially lower returns, and vice versa.

This value also defines the top n instruments ranked by the [Ranking Rules](_documentation_ranking-panel-guide_.md). For example, a value of 5 here means the strategy will enter instruments that passed the Buy Filters _and_ ranked in the _top 5_, based on the Ranking Rules. Thus _increasing_ the total Positions may expose you to trade lower-ranked instruments.

!

This value can not be more than the _distinct_ number of instruments in the strategy's [Portfolios](_documentation_instruments-panel-guide_.md).

!

For example you use two Portfolios totaling 10 instruments, of which 2 instruments are also found in the other Portfolio, then you can only input a value of 8 here, nothing more, but could be less. Otherwise, a warning will appear and you can't backtest the strategy. The maximum number of Position you can hold is 1,000.

Your account size will be divided into this number of Positions. For example, you're putting $100,000 into this strategy and you set this rule to 10 Positions. Then each Position _initially_ will have $10,000 to buy its shares; it may then gain or lose. If it's replaced by another Position (due to hitting a Sell Filter), the new Position will worth about the same as the latest value. At the switch date, the _total_ worth of all Positions will be _divided evenly_ among the 10 new Positions.

* * **3.**  **Position Type:** this rule defines the type of Positions generated by the strategy, either long Positions, or short Positions. Note, this rule may not be available depending on your license, so you'll be using long Positions by default.

!

“Long” is the normal position type, in which you _actually buy_ instruments to enter the Positions (preferably at a low price), and sell them to exit the Positions (preferably at a higher price). “Short” is the exact opposite, where you sell (“sell short”) instruments to enter the Positions, and then you buy back (a.k.a. “cover”) those instruments to exit the Positions.

!

!

To short means to borrow stocks from your broker, and sell them at a price that you deem high enough. Now since you borrow the stocks, you must return them. So you buy back these stocks at a price lower than your selling price. In essence, you'll profit when the price falls, so you pocket the _price difference_ between selling and buying back.

This “Short” mode changes the way the rules behave, so we'll cover it extensively in a [**later page**](_documentation_a-strategy-for-short-selling_.md).

* * **4.**  **Monthly Switch on Open of:** this rule is only available if the previous “System” rule is set to “Periodically Switch Positions”. It defines the switch-day for all your Positions. You can set whatever date you want here.

!

One day _before_ the switch-date, PB generates trading signals (on the [Trade Signals Tab](_documentation_trade-signals-panel-guide_.md)) to sell old Positions and buy new ones. Then at the switch-day, within 30 minutes of the opening bell the old Positions will be closed (as the name implies, “…on Open of”) with Market Orders, _even if_ you have [Limit Sell Order](_documentation_system-settings-panel-guide_.md#sellordertype) set for this strategy. The replacement Positions will also be entered during such time, _unless_ you use [Limit Buy Order](_documentation_system-settings-panel-guide_.md#BuyOrderType).

!

Note, the switch-date is the _trading date_ of the month, not the actual (calendar) day of the month. For example, a value of “6th” here means the 6th day that the market is open since the beginning of the month, i.e. excluding holidays and weekends.

!

The negative dates here represent the “nth trading day before the _next_ month begins”. For example, a value of -1 means the _last_ _trading_ day of the month; and a value of -3 means the third trading day before the next month begins, etc.

!

Changing the switch-date may affect the performance of your strategy, as each phase of the month has its own trading characteristics (more volatile, or trading more volume, etc.).

* * **5.  Don't Switch if Position is Still in Top:** this rule is only available if you use a periodically-switching strategy. It allows you to _keep_ existing Positions if they still rank highly.

!

So at the switch-day, if an existing Position passed the Buy Filters and ranks within the **top n%** as defined in this rule (based on the Ranking Rules, in relation to all instruments that also passed the Buy Filters), that Position will be kept, instead of being replaced with a new position. This is true even if there are other instruments that rank higher.

[https://portfolioboss.com/wp-content/uploads/2021/10/gfyue46hswe.mp4](_wp-content_uploads_2021_10_gfyue46hswe.mp4.md)

The idea is that, as long as existing Positions are still potentially profitable (in the general **top n%** as you defined), you keep riding them out, instead of switching in and out incurring commission fees and slippage. Besides, these existing Positions have shown their colors and performed well; who knows what the replacements will do.

**Notes:**   This rule is not meant to exit Positions _outside_ the top n%. We already have Sell Filters to exit Positions. Those instruments outside the top n% _may still_ be included in the next Positions, especially if the top n% can not fill the Total Positions to Hold.
*   Try a narrow percentage, such as 3%, 5%, or 10%, as you don't want to keep existing Positions that don't rank highly.

* * **6.  If Position Triggers Sell Filter, Replace with:** This rule is only available if the strategy is set to “Periodically Switch Positions”. There's a [counterpart](_documentation_system-settings-panel-guide.md#positionreplacementcontinuous) for a continually-switching strategy, explained later.

!

This defines whether closed Positions (when triggering Sell Filter) are replaced with “Cash” (the liquidated fund sits idle), or “Cash Equivalent” so you may still profit (no matter how little) while waiting for that new Position to enter. 

!

Usually you want to park the money in an instrument more stable than stocks, e.g. government bonds. To define such cash-equivalent instrument, go to the rule just below this (explained [**later**](_documentation_system-settings-panel-guide_.md#cashequivalent)). But “hard cash” can be useful if the market condition is _so bad,_ that you must get out of all trading and investment activities, even in safe government bonds. Besides, some brokers pay interests on your idle cash (not to mention with a cash-based strategy, you don't have to pay those extra commission fees when entering & exiting the cash-equivalent Positions).

Do understand that once a Position hits a Sell Filter, PB not only generates a Sell Signal for that position, but a Buy Signal as well for the cash-equivalent (for cash, it's simply an “enter” signal).

!

Note that some licenses do not allow you to choose the “Cash” option, therefore you're locked to use the “Cash Equivalent” only. If you wish to upgrade your license, please contact our [Customer Support](mailto:support@portfolioboss.com) team.

* * **7.**  **If Position Triggers Sell Filter, It Will be Replaced with the Next Top Position. If There's no Next Top Position, Replace with:** this rule is similar to the previous one, except this is for a strategy that's set to “Continuously Switch Positions”. 

!

Most of the time, a continuously-switching strategy immediately enters a new Position to replace the one exited. But if such replacement can't be found (e.g. no instruments passed the Buy Filters), it will enter the cash or cash-equivalent Position, depending on the option you set here. The “Cash” option can be useful if your strategy does frequent, short-term trading.

If you choose cash-equivalent, the instrument can be defined on the “Cash Equivalent” rule, explained next.

* * **8.**  **Cash Equivalent:** here's where you define the cash-equivalent instrument. This rule applies to both a periodically-switching strategy and the continuously-switching strategy.

!

Let's say you want to park the liquidated fund into an ETF that tracks US government's treasury bonds, then _type_ SHY here (and press _enter_). You can also type anything related to the instrument you're looking for, for example “treasury” or “bond”. Then choose (click) from the dropdown that appears. To view the price chart for that instrument, click the “chart” button ! next to it.

[https://portfolioboss.com/wp-content/uploads/2023/01/frtysdrytdbbth.mp4](_wp-content_uploads_2023_01_frtysdrytdbbth.mp4.md)

As a side note, the strategy's backtest period _may_ be stretched backward with an older cash-equivalent, like PTSHX. That way, the backtest becomes more accurate as it spans a longer period (make sure the strategy's Portfolios are also old enough). Once the strategy is ready to be deployed, type here a commonly traded cash-equivalent like SHY (though it _may_ shrink the strategy's total return a little), as PTSHX can only be traded by institutional investors. You may check if your 401(k) has PTSHX as an option.

Keep in mind, this rule can be used to initiate _bearish_ cash-equivalent Positions. That is, once the old Positions are liquidated, you buy an [inverse ETF](https://www.investopedia.com/terms/i/inverse-etf.asp), instead of going long bonds ETF. That way, during market breakdowns your gain will shoot up high instead of going sideways. Simply type the inverse ETF symbol here:

!

For example your Portfolio consists of S&P 500 stocks, you can use SH (the exact opposite of S&P 500) as the cash-equivalent. But beware as shorting is a dangerous and (often) losing game. It's advisable to do this trick only if the strategy closes its Positions due to general market breakdown.

Now, you can also initiate bearish cash-equivalent Positions by _literally shorting_ the cash-equivalent instrument. You do that with the rule just below this one, i.e. “Cash Equivalent Position Type”, discussed next.

**Notes:**   Cash-equivalent Positions are always entered and closed with market orders, even if your strategy utilizes Limit Orders. The idea is that you want to park your money immediately once the old Positions are liquidated, and to get out of that safe haven immediately once profitable instruments are found.
*   You can't enter a delisted instrument here (those indicated by a number suffix inside square brackets). Otherwise a warning appears and you can't backtest the strategy:

!

* * **9.**  **Cash Equivalent Position Type:** this rule defines whether you're buying the cash-equivalent instrument, or you're literally shorting them.

!

If you just want to be safe, by _buying_ bonds/government treasuries ETF, then make sure this is set to “Long”. Even if you're using an inverse ETF as the cash-equivalent, you must set this to “Long” because essentially you're going long (buying) that bearish instrument.

Now, there are cases where you need to _actually short_ the cash-equivalent instrument. For example if there's not a single ETF representing _the inverse_ of your Portfolio. In that case, you can set this rule to “Short”, while the cash-equivalent instrument is set to a bullish ETF representing your Portfolio.

!

The short cash-equivalent Positions behave the same way as the long ones, except when entering and exiting them you'll receive Short and Cover Signals, respectively (as shown on the [Trade Signals Tab](_documentation_trade-signals-panel-guide_.md)):

!

!

But most of the time you can find such _inverse_ ETFs. In that case it's much better to just go long/buy any of those ETFs (you won't be hit with margin and stock-loan fees like when you go short). Now, the common way to use the “Short” option is when you trade single stocks (the strategy's Portfolio contains but a single stock), because individual stocks don't have the inverse counterpart:

!

In the example above, when TSLA long Position will be closed, you may get two signals: One to sell it, the other to sell-short (initiate the TSLA short Position). Ditto if TSLA long will be entered again: one Cover Signal to exit the TSLA short Position, and another a Buy Signal to enter TSLA long Position. So the two trades will happen on the same day (usually at the market open).

!

This is true unless the strategy entirely uses Limit Orders, in which case, _Cash_ Positions _may become_ the intermediary between the long and the short Positions.

When looking at the **[Positions Tab](_documentation_positions-panel-guide_.md)**, it may not be readily known whether the Position is the normal one (long), or the cash-equivalent (short). You can hover your mouse over the symbol to see its Position type:

[https://portfolioboss.com/wp-content/uploads/2023/01/r56e45awg55.mp4](_wp-content_uploads_2023_01_r56e45awg55.mp4.md)

The section “Positions _sold_ at the open” may also display _covered_ (not sold) cash-equivalent Position.

Now, you can create many of these single-stock strategies (even better with the help of the [**Divine Engine**](_documentation_the-divine-engine-and-the-boss_.md)), then you combine them with a **[multi-strategy](_documentation_multi-strategy_.md)** (or [**meta-strategy**](_documentation_meta-strategy_.md)). That way, despite high volatility (but also high gain), you _may_ smooth out the ride altogether.

* * **10.**  **Buy Order Type:** this rule lets you choose between using Market Order or Limit Order when _entering_ Positions. Note, some licenses don't have the ability to use Limit Orders. Please contact our [Customer Support](mailto:support@portfolioboss.com) to upgrade your license.

!

There are three options for this rule, one is for a Market Order, and the other two are different flavors of the Limit Order (we'll discuss them in detail in the next section):

*   **Market Order:** it's the default order type. PB generates the Buy Signals, and then such signals are input _by you_ to the broker (as orders). The broker in turn, will buy the instruments based on _whatever_ market price _when_ they execute the orders (usually during the market open).
*   **N ATR Limit Order:** instruments are _bought_ with Limit Orders (limit prices) that are calculated based on their ATR (Average True Range).
*   **Percentage Limit Order:** instruments are bought with Limit Orders based on a percentage of the previous day's closing price.

Any Limit Order requires the broker to wait until a certain price (or lower) is met for the Buy Order to be executed. This “limit price” will be calculated using the rule below, called [“Buy Order Limit”](_documentation_system-settings-panel-guide_.md#buyorderlimit) (only visible if you choose anything other than “Market Order” here):

!

When setting up your Buy Order Limit, you'll also see an ‘Exceed Limit' checkbox. This option controls whether the day's low price must be strictly lower than your limit price for Portfolio Boss to consider it a buy. When checked, this feature helps account for potential gaps between the low price and the ask price, particularly important for low-priced stocks and ETFs under $10 where order fulfillment can be more challenging.

For example, if you set a limit price of $7.00 and the ‘Exceed Limit' option is checked, the day's low must fall below $7.00 for PB to consider the order filled. Perhaps 10,000 shares are sitting at that price. Unfortunately, only a couple orders get filled, and yours wasn't one of them and price moves back down. The strategy will think you bought unless you check that box. This is especially useful when building trading strategies for correct modeling.

So it goes like this: You set the limit price calculation with that “Buy Order Limit”. Then the strategy generates Buy Signals as usual. These signals, along with the limit prices (calculated by the strategy based on your setting), are sent to your broker. Such limit prices are shown in dollar value, that is, “buy the instrument at this price or _lower_“. Each buy signal (each instrument) will have its own limit price.

!

Once the market closes at the next trading day (the day after the Buy Signals were given), PB looks for the day's _lowest_ _prices_ (for each instrument to be bought) to decide whether or not the limit prices are met. If they're met (and exceeded if that option is selected), then PB considers those Positions as _already entered_. Once entered, PB can only assume their _entry price_, that is: whichever is the lower price between the opening price, and the limit price itself. In reality, the entry price could be different than either of them, i.e. due to slippage, or some advanced order-algorithm used by your broker.

If some instruments don't meet the limit price, then PB assumes they are not entered as Positions today, thus they're listed as Cash Positions until the next Buy Signals are given (could be for different instruments).

!

Limit Order is good for two things: to look for discounts when entering a position, and, to minimize slippage (difference in price between order entry and execution) which may seem small but will accumulate for all your trades, eating your account.

A Limit Order in PB only lasts for that single day; if you don't get the right price for the day, the order must be cancelled (because PB _may_ generate other signal for a different instrument and/or different limit price). Obviously, PB can only “assume” whether or not the Limit Order is filled; you may want to check with your broker to see if it's actually filled.

* * **11.**  **Buy Order Limit:** this rule calculates the limit price that you'll send to your broker. It's only available if you set the previous rule into any of the Limit Orders there. Each type of Limit Order has its own way of calculating the limit price:

!

!

*   **N ATR Limit Order:** 

Essentially you'll buy the instrument if the price is lower than the _previous_ _day's_ close. But how low? Enter the Average True Range. ATR measures an instrument's volatility (in dollar value) during a certain period. In other words, how much a stock goes up or down _on average_ during the past certain days.

If a stock goes below the previous day's closing price, and such drop _exceeds_ the ATR (but not too much), then the stock is likely to _rebound_ to the general trend. So, not only you enter the position at a _big_ discount, you're also well placed for profit when the price rebounds.

[https://portfolioboss.com/wp-content/uploads/2021/10/45awgdyndty.mp4](_wp-content_uploads_2021_10_45awgdyndty.mp4.md)

Of course you can be on the conservative side as well, for example you'll buy if the drop is just _a fraction_ of the ATR. You may only get a small discount when entering the position, but at least you don't risk the instrument reversing its trend. Besides, such Limit Order is more likely to get filled since it has a shallower entry price. Either way, Limit Order allows you to get an extra discount, and the ATR gives you an idea of how likely the Limit Order will be filled (anything too much beyond that ATR and the order may never get filled).

The formula is pretty self-explanatory: “Buy the instrument if the price is _equal to_ or _lower than_: the previous day's adjusted closing-price _minus_ the multiplied ATR of the past certain days.”

!

The first parameter defines the ATR multiplier. Values _greater_ than 1 mean you're looking at a price-drop greater than the ATR. Fractional values (like 0.33) mean you're looking at a price drop smaller than the ATR (i.e. one-third):

!

The second parameter defines the period for the Average True Range. That is, the number of days for the price-volatility to be calculated. The usual periods are 2, 10, 14, or 20 days:

!

On the [Instrument Tab](_documentation_instrument-tab_.md), an indicator-line (showing the limit prices) is overlaid on the price chart:

!

Look at a Buy candle whose low of the day is lower than (or equal to) this indicator line; it means the Buy Limit Order was filled on that day.

*   **Percentage Limit Order:**

This is the simpler Limit Order type: instead of using price volatility in the past few days, the limit price is simply calculated a certain _percentage_ below yesterday's adjusted closing price.

!

There are two reasons for this: First, yesterday's closing price usually continues _right to_ the next market open (at least not too far off, since [gaps](_documentation_surprise-day-filter_.md) aren't that common), so your order is more likely to get filled, unless you use a big percentage here. Second, stock prices _usually_ reverse a little (from yesterday's closing price) at the opening hour, before resuming the general trend; hence you could get a small discount before the price rallies to your profit later in the day.

The calculation is: multiply yesterday's closing price (adjusted) by the percentage you set here, then subtract the resulting dollar from yesterday's closing price. There is your limit price for today.

[https://portfolioboss.com/wp-content/uploads/2023/01/gfyse546awh5.mp4](_wp-content_uploads_2023_01_gfyse546awh5.mp4.md)

There's only one parameter for it:

!

That defines the percentage below yesterday's close. You don't want to set this at high values, because then _all_ your limit orders won't get filled. Our experiments showed that values between 2.5% and 7% are _generally_ the sweet spot. The maximum value you can set here is 50% while the minimum is -50% (yes, you can put a negative percentage, which means the Buy Limit Price is _higher_ than yesterday's closing price).

On the [Instrument Tab](_documentation_instrument-tab_.md), an indicator-line for this Percentage Limit Order is overlaid on the price chart:

!

Look for a Buy candle whose low of the day is lower than (or equal to) this blue line; it means the Buy Limit Order was filled on that day.

**Note:**

Obviously, “yesterday's closing price” is from the day the Limit Buy Signal is given.

!

* * **12.**  **Sell Order Type:** this rule lets you _exit_ Positions with either Market Order or Limit Order. Note that some licenses can't use Limit Orders (thus defaulting to Market Order); please contact our [Customer Support](mailto:support@portfolioboss.com) if you wish to upgrade your license.

!

There are three types of order you can choose here:

*   **Market Order:** The Sell Signals don't carry limit prices, i.e. you take the Sell Orders to your broker, and they'll execute them based on whatever market prices they're trading at (usually at the market open). Generally, Market Order is best, because you don't want any obstacles when exiting Positions; otherwise you're in for greater losses while waiting for those limit prices.
*   **N ATR Limit Order:** You sell the Positions with Limit Orders calculated based on their Average True Range.
*   **Percentage Limit Order:** The Positions are sold with Limit Orders calculated as an offset from the previous day's closing price.

Limit Sell Orders can be useful _not_ as a stop-loss, but as a way to squeeze that last drop of profit when you sell the Positions. Once you choose any of the Limit Order-types here, another rule appears below this, i.e. [“Sell Order Limit”](_documentation_system-settings-panel-guide_.md#sellorderlimit), which defines how the limit prices are calculated.

!

Limit Sell Order is only applicable for Positions that hit Sell Filters _specifically set_ to use Limit Order (explained later). Positions that hit such Sell Filters will be sold with Limit Orders, stated in dollar value, i.e. sell at this price or higher. Sell Filters that are set to Market Order don't trigger the use of Limit Order, ditto Positions that will be sold due to switch-day won't use Limit Order.

!

So, once the Sell Signals and the limit prices are sent to your broker, at _the end_ of the next day PB looks at the High prices of the day (for all Positions that hit Limit Sell Filters). If such High prices are equal or _greater than_ the limit prices, then PB _assumes_ the Positions exited. These Positions are then replaced with Cash Positions on that day; and you'll receive Buy Signals to be executed the _next day_ (either for entering cash-equivalent or new replacement Positions).

!

!

If they fail to get sold, these Positions remain, and the strategy tries to sell them every single day (with the latest limit prices) provided they still hit the Limit Sell Filters.

Now, as stated before, some Sell Filters must be specifically set to use Limit Order. You can do this by going to the [Sell Filters Panel](_documentation_sell-filters-panel-guide_.md), and set at least one of the filters to “Limit Order” instead of “Market Order”. If no Sell Filter is set to use Limit Order, the “Sell Order Type” rule shows a warning and you can't backtest the strategy:

!

If such Sell Filter triggers a Sell Signal, the Limit Order will be set in place. But if it's triggered by a Sell Filter with a “Market Order”, obviously no Limit Order will be set in place.

It's good to set at least one Sell Filter to “Market Order”, so even if the Limit Order doesn't get executed, you _may_ exit out of that Position with the Market Order (if the price continues to deteriorate).

* * **13.**  **Sell Order Limit:** this rule is only available if you set the previous rule to any of the Limit Order-types. This rule lets you define the way the _sell_ limit price is calculated. Each Limit Order-type has its own way of calculating the limit price.

!

!

*   **N ATR Limit Order:**

In essence, you'll only sell if the price is equal or _higher than_: the previous day's adjusted closing-price _plus_ the multiplied-ATR of the past certain days.

[https://portfolioboss.com/wp-content/uploads/2023/01/5463sehrynxdryj.mp4](_wp-content_uploads_2023_01_5463sehrynxdryj.mp4.md)

The first parameter defines the ATR multiplier. You can set it higher than 1 if you're looking for a greater profit. Or be conservative and set it less than 1 so your order is likely to be filled (since the _average_ price range is not exceeded). 

!

Keep in mind, you may set this multiplier to a negative value, which means the limit price is _below_ the previous day's close _and higher_. This can be useful to lower the selling barrier so your Sell Limit Order is more likely to get filled. If such is the case, set this multiplier to a negative fractional value (for example, -0.33).

!

The second parameter defines the number of days to calculate the Average True Range (which includes today, when the limit signals are given):

!

On the [Instrument Tab](_documentation_instruments-panel-guide_.md), you'll see the Sell Limit indicator (blue line) overlaid on the price chart:

!

Look for a Sell candle whose High is _higher_ than (or equal to) this indicator line, it means the Sell Limit Order was filled on that day.

*   **Percentage Limit Order:**

The sell limit price for this is calculated as a percentage _above_ yesterday's closing price (adjusted).

!

So yesterday's closing price is multiplied by a certain percentage, and the resulting dollar value is then added to yesterday's closing price.

[https://portfolioboss.com/wp-content/uploads/2023/01/yjdr5y6sebg6twe.mp4](_wp-content_uploads_2023_01_yjdr5y6sebg6twe.mp4.md)

There's only one parameter here, which defines the percentage:

!

You can put a negative value here so the sell limit price is actually _lower_ than the previous close, but if there's a better (higher) price than it will be used instead. This way, your Limit Sell Order is more likely to get filled.

Now, on the [Instrument Tab](_documentation_instrument-tab_.md), an indicator-line representing this percentage limit price is overlaid on the price chart:

!

Look for a Sell candle whose high of the day is higher than (or equal to) this blue line; it means the sell limit price was reached on that day (order filled).

* * **14.**  **Add Option:** located at the top-right corner of this System Settings Panel, this button allows you to add a Slippage rule to your strategy.

!

Click the button, and a dialog shows up so you can select and add the additional rule:

!

Once added, it's listed at the bottom of this panel:

!

So a word about slippage: when a broker executes your order, the fill price may actually be different than the price when you entered the order. This is due to micro-second volatility of the market.

In PB, unless you're using Limit Orders, most positions are entered and exited at _market open_ (the most liquid, but also the most volatile). So slippage denotes execution price different from the day's _opening price_. This rule _simulates_ the slippage that'll happen on your _trades_ (Buy, Sell, Cover, and Short), including trades for the cash-equivalent Positions. If you're buying, slippage causes your entry price to be _higher_ (more expensive) than the opening price; and if you're selling, it causes your exit price to be _lower_ than the opening price (less realized profit), etc.

[https://portfolioboss.com/wp-content/uploads/2023/01/ddsfgsvfrdfg.mp4](_wp-content_uploads_2023_01_ddsfgsvfrdfg.mp4.md)

Slippage is calculated as a percentage of the stock's price-range for the day it's traded. For example, a stock moves $10 between the _high_ and _low_ prices of the day (adjusted), then a slippage of 5% will get you an entry price $0.5 more expensive than the market's opening price. The strategy's [metrics](_documentation_metrics-panel-guide_.md) reflect a reduced gain due to slippage. This allows you to have a _more realistic_ _return_ on your strategy.

!

Keep in mind, if you have a larger account, you want to simulate a slippage of about 10% on all your trades. Otherwise, a value of 5% or lower is about right. That's because larger accounts tend to trade larger volumes of shares, hence orders may take a while to be entirely filled, so slippage would be more obvious. Not to mention you may offset the price balance with your large orders (the law of supply and demand).

You can disable this option by unchecking it (disable its checkbox on the left), or simply delete it by clicking the trash-bin icon on the right.

**Notes:**   As stated earlier, slippage normally isn't applied to Limit Orders. But if your Limit Orders are executed with the opening price (because the opening prices are better than the limit prices), then slippage will be applied for those trades.
*   Even if the candle doesn't show a price _higher_ than the opening price, slippage will still be applied when you're _buying_. And vice versa when you're _selling_: even if there's no price lower than the opening price, slippage will cause your exit price to be actually lower than the opening price. It's just a simulation after all; you may want to check your brokerage report for the actual slippage (and other fees like commissions, margins, stock-loan fee, etc.).

[**Back to Top**](_documentation_system-settings-panel-guide_.md#backtotop)

You have already reported this .

#### _documentation_the-divine-engine-and-the-boss.md

> Source: https://portfolioboss.com/documentation/the-divine-engine-and-the-boss
> Scraped: 3/1/2026, 2:08:19 AM

[!](_wp-content_uploads_2020_07_Electronic-Bull-Final-w-Border-Logo.png.md)

The “Divine Engine” is a revolutionary Artificial Intelligence feature that helps you _design_ the ultimate strategy that fits your trading goals, schedule, and risk appetite. But most importantly, it allows you to keep your “edge” on the market, also known as Alpha. Alpha measures the _excess return_ of a strategy compared to a benchmark's return (e.g. the S&P 500 index). And by nature, Alpha is about exploiting anomalies and inefficiencies in the market to generate greater returns. As such, Alpha may decay throughout time once the anomalies are found and corrected by the market forces, or exploited by other traders.

Think of it this way: the total population of traders as a whole generate the exact same return as the market. For every buyer there's always a seller, thus for every winner there's always a loser. Some traders win by sheer luck, others by their edge on the market. The question is, _when_ will you be that loser. If you cling to a strategy for a long enough time, you will eventually become a loser, as the strategy's Alpha decays. The reversion to the mean is no joke.

[!](_wp-content_uploads_2020_07_Mean-Reversion-of-Funds.png.md)

Now with the Divine Engine, it creates unique strategies that you and _only you_ will use. Not even other Divine Engine users have the exact same strategy you have. Therefore it greatly reduces Alpha decay by preventing other traders from using your system. Even at the eventuality that your strategy reverts to the mean, as attested by its _now_ poor [Out-of-Sample performance](_documentation_backtest-panel-guide.md#InSampleRatio) (Out-of-Sample performance that _has passed_ might be good, but _now_ the strategy starts reverting to the mean), you can ask the Divine Engine to craft another Alpha for you, thus keeping your edge sharp. But make sure the strategies you pick perform very well _both_ in the In-Sample period and the Out-of-Sample. That way, you make sure they _actually_ have Alpha, instead of fake Alpha generated by torturing the data hard enough to make it confess.

At Portfolio Boss, we're always innovating to find market anomalies. Not only we introduce new rules, filters, and algorithms, but we also dabble now in crunching intraday data. Intraday prices are notorious for the hysteria and manipulation, thus we hope with such “noise” we can find more anomalies that the Divine Engine can use. There's also the latest breakthrough where the A.I. writes its own technical indicators from scratch through Genetic Programming.

This Divine Engine tutorial is separated into four scenarios:

* [Explore a whole new world of discovery, by letting the AI design strategies from scratch.](_documentation_design-strategies-from-scratch_.md)
* [Supplement your current strategy with new filters and rules advised by the AI.](_documentation_augmenting-a-strategy-with-new-rules_.md)
* [Fine tune your current strategy to squeeze out the most profitable settings.](_documentation_fine-tune-a-strategy-for-the-best-settings_.md)
* [Combining all the features.](_documentation_combining-all-the-features_.md)
* [Cyber Code Genetic Programming.](_documentation_cyber-code-genetic-programming_.md)

In the next pages, we'll discuss each scenario in great detail.

To give you an idea of how powerful the Divine Engine is, we have demo strategies that yield astoundingly high returns compared to the SPX's meagre 1,100%. These strategies come with CAGR well beyond 100%:

[!](_wp-content_uploads_2020_07_Super-Strategies-Reports.png.md)

Do understand, the Divine Engine's powerful analytical skills come at a great processing power demand. Portfolio Boss does have a license-dependent local Divine Engine Queue so you can continue to view and build other strategies while you test your ideas. But if you were to run the Divine Engine backtest on your local computer, it may take weeks or even months keeping your PC alive 24/7.

That is the reason we have developed “The Boss”, a cloud-based strategy designer that allows you to run the Divine Engine with the thousands of CPU cores provided there. Here you'll learn how you can run The Boss, and have the ultimate strategy delivered to you _not_ in weeks or months, but in mere minutes or hours.

Please note, you need a specific Portfolio Boss license to access the Divine Engine (and The Boss). If you wish to upgrade your license, please contact our Customer Support at [support@portfolioboss.com](mailto:support@portfolioboss.com)

[**Back to Top**](_documentation_the-divine-engine-and-the-boss_.md#backtotop)

You have already reported this .

#### _documentation_top-n-threshold-filter.md

> Source: https://portfolioboss.com/documentation/top-n-threshold-filter
> Scraped: 3/1/2026, 2:09:17 AM

[!](_wp-content_uploads_2019_10_Top-N-Threshold-Filter-Sell.png.md)

This filter only exists as a Sell Filter.
It will sell Positions that no longer rank in the top N%, based on the [Ranking Rules](_documentation_ranking-panel-guide_.md).

So, let’s first discuss about instruments’ rank: all instruments that have passed the Buy Filters will be ranked according to the Ranking Rules, and the top X instruments will be entered as Positions (according to the parameter [“Total Positions to Hold”](_documentation_system-settings-panel-guide_.md#totalpositions)).

These top X instruments belong in the top N% of the ranked instruments (which means _not all_ top N% instruments are entered as Positions). So, if during the course of trading a Position's rank _drops_ below the top N%, then this filter will exit that Position as there are more profitable instruments in its place.

[!](_wp-content_uploads_2019_10_Top-N-Threshold-Filter-1st-Param.png.md)

The only parameter for this filter defines the _threshold_ top-percent for the ranked instruments.

Beware, if you set this too low, e.g. 1%, the “Total Positions to Hold” _may_ never be fully filled as the majority of the instruments will hit this Sell Filter (at the same time as they pass the Buy Filters), thus they're excluded from being bought. That's because Portfolio Boss is smart enough to exclude instruments that hit the Sell Filters even before their Positions are entered.

You have already reported this .

#### _documentation_trade-plan-calculator.md

> Source: https://portfolioboss.com/documentation/trade-plan-calculator
> Scraped: 3/1/2026, 2:08:18 AM

[!](_wp-content_uploads_2019_10_Trade-Plan-Calculator-Dialog.png.md)

Trade Plan Calculator helps you calculate the number of shares you need to buy and sell, instead of researching the price and calculating manually. This tool can be used anytime even if there are no trading signals today (or the latest backtest date); for example if you start following a strategy at an arbitrary time when there are no trading signals. You can see trading signals from the [Trade Signals Tab](_documentation_trade-signals-panel-guide_.md) (or the email notification sent to you by Portfolio Boss).

So, once you receive these signals, calculate the amount of shares to buy/sell with this tool, and then enter the orders to your broker so he'll execute them tomorrow. If you have Interactive Brokers as your broker, you can also pile your orders into a basket file so they're automatically executed by IB's Trader Workstation.

Note that some licenses don't have access to this Calculator (there's no “Trade Plan” button). Please contact our [Customer Support](mailto:support@portfolioboss.com) if you wish to upgrade your license.

* * **1.**  To access this tool, click the “Trade Plan” button at the top of the “Backtest Strategy” page.

[!](_wp-content_uploads_2019_10_Trade-Plan-button-1122.png.md)

* * **2.**  The tool shows up empty. So you must enter the amount that you will fund this strategy, by using the parameter “Enter Your Portfolio Amount”. Then click the “Calculate” button.

[!](_wp-content_uploads_2019_10_Enter-Portfolio-Amount-000.png.md)

*   If this is the first time you're trading with this strategy, you can enter whatever amount you like, for example $100,000; this tool will automatically calculate how many shares you'll buy on each instrument.

*   If this is a [switch day](_documentation_system-settings-panel-guide_.md#monthlyswitch), you can also enter whatever amount you'd like to _invest_ _further_ into the strategy. For example, you want the previous profits liquidated into hard cash (to buy a new house, for example), then enter whatever _remaining_ amount you'd like to fund the _next round_. If your account size shrunk due to losses in the previous month, enter whatever _remaining_ amount you have (look at your brokerage account's size).

*   If this is _not_ a switch day, for example a Position hits the Sell Filter and you must buy new shares to replace it, then enter your _current_ account size (look at your brokerage account). The Trade Plan Calculator will automatically calculate how many shares to buy for replacing that sold Position, based on that _current account size_. Ditto if you're trading a [Continuously Switching Strategy](_documentation_system-settings-panel-guide_.md#systemparameter) (one that doesn't have a switch day), you must enter your _current_ Portfolio amount in the calculator.

It's okay if you liquidate all your Positions outside of the switch day, although that means you're no longer following this strategy's suggestions, which makes further calculations and recommendations useless. If that is the case, but you want to trade again using this strategy, simply start over as if it's the first time you're using the strategy (enter whatever amount you like invested).

* * **3.**  Once you clicked the “Calculate” button, the Trade Plan Calculator will be populated with data. On the “Symbol” and “Description” columns, you can see the instruments that you'll buy/sell.

[!](_wp-content_uploads_2019_10_Symbol-Description-columns.png.md)

* * **4.**  On the “Action” column, you can see what trade to take on a particular instrument, either Buy or Sell.

[!](_wp-content_uploads_2019_10_Action-Column.png.md)

* * **5.**  The “Suggested Quantity” column shows the _amount_ of _shares_ you need to buy/sell for each instrument. 

[!](_wp-content_uploads_2019_10_Suggested-Quantity-000.png.md)

Note, the _sell_ quantities are just approximations, you may have more or less of the suggested amount. But since we're liquidating the Position entirely, you need to sell _all shares_ of that instrument.

* * **6.**  The “Last Close” column shows the latest closing price for each instrument (in US dollar).

[!](_wp-content_uploads_2019_10_Last-Close-Column.png.md)

* * **7.**  The “Total” column shows the amount of money involved for trading that instrument (if it's a Buy signal, you'll be expending money; if a Sell Signal, you'll receive money). This is calculated by multiplying the “suggested quantity” by the “last close”.

[!](_wp-content_uploads_2019_10_Total-Column.png.md)

Note, each instrument's total fund conforms to its Position weight as shown in [Positions Tab](_documentation_positions-panel-guide_.md) (relative to the other Positions), even if this is the first time you're using the Strategy at an arbitrary time (either periodic or continually switching Strategy). But, it may not _exactly_ reflect the weight, due to the price per share that doesn't allow exact division. The total fund may be less than the weight, but not more.

* * **8.**  The “Suggested Time” column shows the _suggested_ time that your broker will execute these orders. The times are randomized within 30 minutes of the market open, and you can generate new randomized times by pressing the “Calculate” button again. 

[!](_wp-content_uploads_2019_10_Suggested-Time.png.md)

You don't need to pay special attention to these times, as they're merely suggestions. But if you're trading huge amount of shares, it's better to follow these suggestions, as they're able to obfuscate your trades from the High Frequency Traders, as well as avoiding slippage on your orders (bad fills).

* * **9.**  The “Avg. Volume” shows you the _average_ traded volume (amount of shares traded) per day for each instrument.

[!](_wp-content_uploads_2019_10_Average-Volume-Column.png.md)

* * **10.**  The “Rank” column shows each instrument's rank based on the [Ranking Rules](_documentation_ranking-panel-guide_.md).

[!](_wp-content_uploads_2019_10_Rank-Column-Trade-Calculator.png.md)

* * **11.**  If a Buy or Sell order _exceeds_ the average traded volume _per minute_, the calculator will _split_ that order into multiple _smaller_ orders. 

[!](_wp-content_uploads_2019_10_Kyocera-Corp-000.png.md)

The _average traded volume per minute_ is calculated (automatically) by dividing the “average daily volume” by “390 minutes” (which is how long a stock exchange opens in one day).

For example, you have a huge account and you'll be trading Kyocera Corp shares (KYOCY), which traded at an average of 8,140 shares per day, thus 21 shares per minute. If you were to trade 152 KYOCY shares in a single order, it won't be timely filled and you'll suffer slippage (there's no one to buy those extra shares).

Therefore, the calculator divides that big order into smaller orders with 21 shares each. You can see if your order is too big per minute, by looking at an instrument that's _listed multiple times_, with differently-timed orders.

* * **12.**  Now, if this is the _first time_ you're putting this strategy for real use, you can enable the checkbox “Check this if this is the first time you're entering this strategy”, thus the Trade Plan Calculator will only tell you to _buy_ into the various positions, as obviously you have none of the instruments to sell.

[!](_wp-content_uploads_2019_10_First-Time-Using-the-Strategy-Calc-000.png.md)

_You don't need to wait for the switch day to use the strategy:_ you can use the Trade Plan Calculator to calculate your _first_ Positions at any time, even if there are no trading signals.

Thus the calculator will recommend you to enter _today's Positions_ as shown on the [Positions Tab](_documentation_positions-panel-guide_.md) (as long as those Positions are not on the Sell Signals; if they are, then the calculator will recommend the next profitable Positions that will replace them, a.k.a. the Buy Signals).

[!](_wp-content_uploads_2019_10_First-time-buy-replaced-000.png.md)

As shown in the picture above, a Position will be liquidated today (sold) and then replaced by the Cash Equivalent, but since it's the first time you use the strategy, you don't have that instrument to sell. So the calculator automatically tells you to buy the Cash Equivalent (PTSHX).

* * **13.**  If you're using Interactive Brokers' TWS, it is now possible to enter your orders automatically into TWS (orders generated from this Trade Plan Calculator). To do that, while you're in this calculator, click the button “Create IB Basket File” which saves an IB Basket File. 

[!](_wp-content_uploads_2019_10_IB-Basket-File-Export.png.md)

So no longer do you need to type each order manually into TWS, which is error prone. 

This basket file is then imported into TWS (Trader Workstation platform), and your orders are entered automatically with _all the details_, including the instruments' symbol, the number of shares, the stock exchanges to trade, the Limit Prices (if you're using [Limit Orders](_documentation_system-settings-panel-guide_.md#BuyOrderType) in this strategy), etc. Please refer to the Trader Workstation's user guide [here](https://www.interactivebrokers.com/en/software/tws/usersguidebook/specializedorderentry/upload_basket.htm) on how to import a Basket File.

Please note, this feature is only available in some licenses.

* * *

#### Notes:

*   If you're trading a [Multi-Strategy](_documentation_multi-strategy_.md) (or [Meta-Strategy](_documentation_meta-strategy_.md)), the Trade Plan Calculator will merge trades of the same symbol (a symbol that belongs to different Positions, or even different strategies). For example, Strategy A will buy AAPL with 10% weight, and Strategy B will also buy AAPL but at 5% weight. These two trades will be merged into a single order amounting to 15% of your account size. Don't worry, the Multi-Strategy still keeps track of such different Positions.

*   Due to the nature of Portfolio Boss' quick switching into new positions (once the old is liquidated), it's highly recommended that you use a Margin Account at your broker. If you use a Cash Account, your purchasing power may be limited by the Trade Settlement Date, or worse, you may commit Good Faith Violation (or Free Riding Violation) and get your account suspended. If, for whatever reason, you can't get a Margin Account, you must set aside some part of your fund (cash) as a reserve. It will be used to enter new positions recommended by PB while waiting for the previous trade's fund to settle.

*   During switch day (or if you're using the strategy for the first time), your account size will be _evenly_ divided to all new Positions that you'll buy. During non-switch day (when a Position hits a Sell Filter, or if you're using a continually-switching strategy), the amount of money used for buying the _new_ Position depends on the _old_ Position's “weight” as shown on the [Positions Tab](_documentation_positions-panel-guide_.md).

 [**Back to Top**](_documentation_trade-plan-calculator_.md#backtotop)

You have already reported this .

#### _documentation_trade-signals-panel-guide.md

> Source: https://portfolioboss.com/documentation/trade-signals-panel-guide
> Scraped: 3/1/2026, 2:08:14 AM

!

This tab shows you the _latest_ _trade signals_ generated by the strategy (usually the current date, but can also be set from the [“Date to”](_documentation_backtest-panel-guide_.md#datetoparam) property of the Backtest Panel). These [trade signals](https://www.investopedia.com/terms/t/trade-signal.asp) can be sent to you via email/text if the [strategy's notification](_documentation_strategy-panel-guide_.md#enablenotif) is enabled. 

This tab is located at the [Reports Area](https://portfolioboss.wpenginepowered.com/wp-content/uploads/2021/05/gdg56ye5dg_00000_00000.png) of the “Backtest Strategy” Page, and it's divided into two sections:

*   the Trade Signals Section, and
*   the Top Ranking Instruments Section.

!

* * *

### Trade Signals Section

This is where you see the trade signals. They usually appear:

*   one day before the switch-day (for a [periodically-switching](_documentation_system-settings-panel-guide_.md#systemparameter) strategy),
*   when any Position hits the [Sell Filter](_documentation_sell-filters-panel-guide_.md), and
*   when there are instruments more profitable than the Cash or Cash Equivalent Positions, thus the strategy enters the normal/stock Positions (this is for a [continually-switching](_documentation_system-settings-panel-guide_.md#systemparameter) strategy),

in which case you'll see this section populated, and there's a notification balloon on the tab's header:

!

It tells you the number of trade signals that appear here (excluding Cash Signals). There's an info at the top that says “Trade signals based on data through \[today's\_date\]”. And below that, the reason the signals are generated (in this case it's a switch day). Sometimes they're generated due to triggering some Sell Filter(s):

!

If it's simply replacing the Cash (or Cash-Equivalent) with more profitable instrument Positions, then there's no reason given.

These trade signals are generated _one trading day_ before the orders are supposed to be executed.

!

You'll see the date they must be executed, so you must enter the orders to your broker before such a date.

Now, if there are no trade signals, this section simply tells you to hold the current Positions:

!

Let's now see the actual trade signals and their columns' description:

* * **1.  Rank:** This column shows the ranking (based on the [Ranking Rules](_documentation_ranking-panel-guide_.md)) of those instruments that will be traded.

!

Any Positions that will be sold (exited) may have whatever ranking here (they will be sold after all, triggering a Sell Filter). But those instruments that will be bought (entered), usually have high rankings (as seen from the [Top Ranking Instruments Section](_documentation_trade-signals-panel-guide_.md#toprankingsection)). Portfolio Boss will try to enter the #1 ranked instrument, and go down from there.

* * **2.  Symbol:** This column shows the ticker symbol for those instruments to be traded.

!

You can hover your mouse over a symbol, and a tooltip-description shows up, with information about its asset-class, the market (exchange) it's traded on, the portfolios that contain said symbol, and the period it's been traded. The symbol is also clickable, which will bring you to its price chart (at the [Instrument Tab](_documentation_instrument-tab_.md)); there you can see the trading actions for this symbol so far (and how they were triggered based on the strategy's rules, e.g. if the closing price is above the 200-day SMA):

!

Remember, those are the trading actions, that is order execution, _not_ the trading signals. The trading signals are generated one trading day (candle) prior to such actions.

Aside from the usual stock or ETF symbols (part of the strategy's [portfolio](_documentation_instruments-panel-guide_.md)), you'll also see Cash or Cash Equivalent symbols here. Cash Equivalent (e.g. SHY) will be _bought_ if a Position will be _sold (exited)_–that is if your strategy uses [Cash Equivalent instead of Cash](_documentation_system-settings-panel-guide_.md#positionreplacements):

!

Each Sell (exit) Signal will be accompanied with a Buy Signal to enter the Cash Equivalent. If there are multiple Sell Signals, the Cash Equivalent symbol will have a number suffix within the parentheses indicating the number of Positions that will be replaced. Cash Equivalent Positions will then be _sold_ if the strategy decides to replace them with the usual stocks/ETFs:

!

Now the Cash symbol, will appear here if the strategy uses Cash instead of Cash Equivalent. That is, for each Position that will be sold, there's also a signal to “Enter” the Cash Position.

!

As usual there's the number suffix indicating the number of Positions replaced with the Cash. And once the strategy decides to replace the Cash Position with the usual stock/ETF, there's a signal to “Exit” the Cash Position:

!

These Cash Signals obviously don't require anything on your part, as Cash are automatically _received_ when you exit Positions, and _spent_ when you enter Positions.

Now, _regardless_ if your strategy uses Cash or Cash Equivalent, Cash symbol _will also_ appear if you're using [Limit Orders](_documentation_system-settings-panel-guide_.md#BuyOrderType). For example, if a Limit _Buy Signal_ fails to be executed (filled) at the next trading day, it'll be listed as a Cash Position, and PB will continue to generate the Limit Buy Signal (could be for a different top-ranked instrument) _along with_ a Cash Exit Signal on the following days until the Limit Buy Order is filled and the Cash Position is replaced:

!

There's also the Cash symbol if any Position triggered a [Limit Sell Filter](_documentation_system-settings-panel-guide_.md#SellLimitFilter) (hence causing a Limit Sell Signal). Each Limit Sell Signal is accompanied by a Cash Enter Signal (such Cash Signals could be grouped with a parentheses-suffix if there are multiple Limit Sell Signals):

!

That's because Portfolio Boss can't know whether the Limit Sell Order gets filled at tomorrow's open; hence it _can't simultaneously_ give you a Buy Signal (_to replace_ the sold Position) to be executed at tomorrow's market open. Only after the _market closes_ tomorrow does PB know whether the limit order gets filled. If the order gets filled tomorrow, PB enters a Cash Position for that day. Also at that day, PB gives you a Cash Exit Signal along with a Buy Signal to replace the sold instrument (which will be executed at the next market open):

!

But what if such Limit Sell Signal can't be executed during the course of tomorrow's trading session? Then PB keeps that old Position and there won't be any Cash Position entered for that day (despite the Cash Enter Signal). PB will also continually generate the two signals (Limit Sell and Cash Enter Signals) _as long as_ the Limit Sell Filter is _still triggered_ by that Position.

It all may sound complicated, but just think about how you would execute a Limit Sell Order on your own: you won't really be planning & executing a replacement (Buy Order) _unless_ you already know that the Sell Order got filled. PB only knows whether the Sell Order gets filled after the _market closes_ and it _finishes downloading_ the EOD data for that day; hence the replacement (Buy Order) can only be executed the day after; in the time being, the old Position is stored as Cash.

**Note:**

The replacement instrument can be either a Cash Equivalent like SHY (usually for a periodically-switching strategy), or another stock/ETF (usually for a continuously-switching strategy).

* * **3.  Description:** This column shows the description for those instruments that will be traded.

!

The description is usually the company's (or fund's) full name. Note that the Cash symbol also has its own description, but this is usually misleading. In the example above, the Cash is actually a placeholder for the “would be sold” Position of LVLT (using Limit Sell Signal), but instead the description says “Cash placeholder for unfilled position DG” (which indicates a Limit Buy Order for DG that was unfilled). This could be a carryover from the actual DG Limit Buy Order in the past. Until this quirk is fixed, just ignore the Cash description you see.

* * **4.  Signal:** This column shows the _type_ of trade signals generated.

!

If you use a [Long Strategy](_documentation_system-settings-panel-guide_.md#PositionType), you'll have the usual Buy and Sell Signals. This applies to the strategy's Portfolio(s) and its Cash Equivalent. If it uses Cash _instead_ _of_ Cash Equivalent, you'll also see signals to “Enter” or “Exit” the Cash Position:

!

!

If you use a [Short Strategy](_documentation_a-strategy-for-short-selling_.md), instead of Buy and Sell Signals, you'll have the Short Signal and Cover Signal (to enter and to exit the Positions, respectively). The Cash Equivalent instrument will still have the Buy and Sell Signals though:

!

Now, if you use [Limit Orders](_documentation_system-settings-panel-guide_.md#BuyOrderType) on your strategy, you'll see these signals given the “Limit” prefix:

!

Such prefixes are to prevent you from inadvertently entering Market Orders when you should use Limit Orders. But Cash Equivalent (or Cash) Signals _are_ _never_ Limit Signals for obvious reasons.

**Notes:**   For switch-day Sell (or Cover) Signals, there won't be any limit price applied, as you're supposed to _immediately_ exit all existing positions and replace them with new ones.
*   Those signals to exit Positions (Sell, Cover, Cash Exit) are always placed above those signals to enter Positions (Buy, Short, Cash Enter).

* * **5.  Limit:** This column shows the limit price for each Limit Signal. It only appears if indeed there are Limit Signals (despite your strategy already using Limit Orders).

!

This limit price is calculated from the [Buy Order Limit](_documentation_system-settings-panel-guide_.md#buyorderlimit) rule (or [Sell Order Limit](_documentation_system-settings-panel-guide_.md#sellorderlimit)) you set on the System Settings Panel. After the signals are given, PB will wait until the next trading day's close (and EOD data are all downloaded) to determine whether such limit prices were met.

* * **6.  Hold the following positions:** This is located below all the trade signals, and it lists the _current_ Positions that must be held; just let them run.

!

Obviously these held Positions can't be a Position that will be sold (exited) in the signals above. And if it's a switch-day, _usually_ you must replace all existing Positions, hence none are held.

As usual, you can hover your mouse over a symbol to display its tooltip-description; as well as clicking it to bring up its price chart ([Instrument Tab](_documentation_instrument-tab_.md)).

* * *

### Top Ranking Instruments Section

This section shows you the highest performing instruments at the current date (from the strategy's Portfolio), based on the [Ranking Rules](_documentation_ranking-panel-guide_.md).

These are the most likely candidates to become the new Positions once the old ones are exited (either due to a switch day, or hitting a Sell Filter). Or, if the instrument listed here is already held as a Position, you are more likely to keep it. 

!

It's possible that this list is empty, which could be that _none_ of the instruments passed the Buy Filters. If that's the case, liquidated Positions won't be replaced by new Positions, but still parked into the Cash/Cash Equivalent Positions instead. Once this list is populated again, the Cash/Cash Equivalent Positions will be replaced with the top-ranked instruments from here.

There are three columns in this section:

*   **Rank:** ranks the instruments top to bottom, based on the Ranking Rules. The #1 ranked instrument will be the _first_ to replace any sold (exited) Position, then it goes down from there.
*   **Symbol:** shows the ticker symbol for these top-ranked instruments. As usual, you can hover the mouse over the symbol to show its tooltip-description, or click it to show the price chart (on the [Instrument Tab](_documentation_instrument-tab_.md)).
*   **Description:** shows the description for each instrument (full name of the company or fund).

Keep in mind, this list is updated each trading day: some instruments may no longer rank highly, hence other instruments take their place.

**Note:**

The number of instruments listed here correlates to the [“Total Positions to Hold”](_documentation_system-settings-panel-guide_.md#totalpositions) rule you set on the System Settings Panel. If the strategy has only one instrument in its Portfolio, there's only one instrument listed here, even if it has no Ranking Rules at all.

* * *

#### Notes:

*   Once the trade signals are generated, open the [Trade Plan Calculator](_documentation_trade-plan-calculator_.md) ( ! ) to create your orders, which will be sent (input) to your broker. It allows you to calculate the number of shares to be traded, split the big orders for obfuscation and avoiding bad fills, and dump all these order information into a _basket file_ that you can import to [Interactive Broker's TWS](https://www.interactivebrokers.com/en/trading/tws.php) (if you have it as your broker). You can use this Calculator anytime, even when there are no trade signals. Note you may not have access to this Calculator depending on your license. Please contact our [Customer Support](mailto:support@portfolioboss.com) if you wish to upgrade your license.

*   For multi-strategies, this Trade Signals Tab may be a little different than what you see here. For one, there's an additional column “Weight” displaying the weight (percentage of account size) of each trade signal. Then there's the strategy-grouping for the trade signals; and there's no Top Ranking Instruments Section there. Read about it [here](_documentation_multi-strategy_.md#MultStratTradeSignalsTab). For meta-strategies, this tab's layout is generally the same as multi-strategies.

*   Sometimes you may get a Sell (exit) Signal despite the Position not triggering any of the Sell (or Cover) Filters. This could be due to the instrument company (or fund) being delisted from the exchanges (merger, acquisition, or plain bankruptcy).

*   You can expand this tab if it's too cramped. So instead of tediously scrolling its contents, put your cursor at the edge of this tab until it turns into an arrow cursor. Then drag it to expand (or shrink) this tab. Note, each section of this tab isn't expand-able at the expense of the other section.

[https://portfolioboss.com/wp-content/uploads/2022/12/gyudrfy7sn6.mp4](_wp-content_uploads_2022_12_gyudrfy7sn6.mp4.md)

[**Back to Top**](_documentation_trade-signals-panel-guide_.md#backtotop)

You have already reported this .

#### _documentation_types-of-strategy.md

> Source: https://portfolioboss.com/documentation/types-of-strategy
> Scraped: 3/1/2026, 2:07:55 AM

!

Portfolio Boss has three strategy types:

**1.**  **Basic Strategy:**  this is the default strategy type, the meat of Portfolio Boss. A basic strategy contains Buy Filters, Sell Filters, Ranking Rules, and various parameters to _automatically_ _manage_ your trading activities. It trades _individual_ instruments from certain Portfolio(s).

**2.**  **Meta Strategy:**  this is similar to a basic strategy, but instead of trading actual instruments, it trades _basic_ _strategies_ as the “instruments”. Think of a basic strategy as an ETF: in which you trade that ETF's entire instruments at once. A single Position entered is a whole strategy used, so you may have multiple strategies being traded at once.

**3.**  **Multi Strategy:**  now, this one is a beast on its own. It allows you to stack multiple _basic strategies_ in a hierarchy (top-to-bottom), so you can manage market risks in a tiered format (vertically).

For example, the top strategy is the riskiest (but also the most profitable) where you're trading high-performing volatile stocks. If the market condition doesn't favor trading such stocks, then fall back to the second strategy, in which dividend stocks are traded. If the market condition is even worse, then turn toward the third strategy where you're trading bonds. If all else fails, revert to cash position and park your money safely.

Aside from stacking, a Multi Strategy can also be used to combine multiple _basic strategies_ without hierarchy between them. This is useful so you don't have to operate many strategies one by one; Portfolio Boss will calculate how many shares to buy based on how much you invested for each strategy.

For more in-depth explanation about Meta and Multi types, please refer to [Chapter 6](_documentation_multi-strategy_.md). For now, you just need to know the gist of these strategy types for when you're creating a new strategy (through this “Strategy Management” page). 

#### Note:

In some licenses, you can't create either Multi-Strategy, Meta-Strategy, or both. If you wish to upgrade your license, please contact our [Customer Support](mailto:support@portfolioboss.com) team.

You have already reported this .

#### _documentation_user-guide-overview.md

> Source: https://portfolioboss.com/documentation/user-guide-overview
> Scraped: 3/1/2026, 2:07:37 AM

## !

Welcome to the comprehensive user guide for Portfolio Boss!

The user guide walks you through all the functionalities of Portfolio Boss. We'll begin with the [Quickstart Guide](_documentation_quick-start-guide_.md) so you get up to speed with the fundamental features. Then, we'll explore each functionality in great detail:

* [Create a strategy and customize it to fit your trading goals.](_documentation_backtest-strategy-page-overview_.md)
* [Create and manage the list of securities to trade.](_documentation_portfolios-panel-guide_.md)
* [Explore the Technical Indicators, to enter and exit Positions automatically.](_documentation_about-filters-rules_.md)
* [Backtest your strategy, and get the detailed performance report.](_documentation_metrics-panel-guide_.md)
* [Stack multiple strategies as multi-tiered risk management.](_documentation_multi-strategy_.md)
* [Manage your list of strategies.](_documentation_strategy-management-page-overview_.md)
* [**Harness the power of Artificial Intelligence to design the ultimate strategy.**](_documentation_the-divine-engine-and-the-boss_.md)
* [Trade multiple strategies at once as if they were ETFs.](_documentation_meta-strategy_.md)
* [Receive trading signals automatically](_documentation_automation-tab-guide_.md#sendemailnotif)[.](_documentation_trade-plan-calculator_.md)
* [Easily calculate the amount of shares to trade, across a diverse portfolio of stocks.](_documentation_trade-plan-calculator_.md)
* [Customize how Portfolio Boss appears and performs in your machine,](_documentation_settings-page-overview-guide_.md)
*   and many more!

In short, Portfolio Boss takes all the heavy lifting, so you can sleep well at night and do things that you love. It is a _versatile_ Systematic Trading platform built from the ground up by traders, for traders.

Please note, some features explained in this guide may not be available to you, depending on your license. If you wish to upgrade your license, please contact our Customer Support at [support@portfolioboss.com](mailto:support@portfolioboss.com).

* * *

The user guide is divided into nine chapters.
Use the “Search” button (at the bottom-right of this page) to search for topics, or click any of these pages:

##### Chapter 1: Introduction

* [User Guide Overview](_documentation_user-guide-overview_.md)
* [System Requirements & Installation](_documentation_system-requirements-installation_.md)
* [Quick Start Guide](_documentation_quick-start-guide_.md)

##### Chapter 2: Portfolio Management Page

* [Portfolio Management Page Overview](_documentation_portfolio-management-page-overview_.md)
* [Portfolios Panel](_documentation_portfolios-panel-guide_.md)
* [Portfolio Instruments Panel](_documentation_portfolio-instruments-panel-guide_.md)
* [Instrument Chart Panel](_documentation_instrument-chart-panel-guide_.md)
* [Sync Details/Search Results Panel](_documentation_sync-details-search-results-panel_.md)

##### Chapter 3: Strategy Management Page

* [Strategy Management Page Overview](_documentation_strategy-management-page-overview_.md)
* [Types of Strategy](_documentation_types-of-strategy_.md)
* [Managing Your Strategies](_documentation_managing-your-strategies_.md)

##### Chapter 4: Backtest Strategy Page

* [Backtest Strategy Page Overview](_documentation_backtest-strategy-page-overview_.md)
* [Strategy Panel](_documentation_strategy-panel-guide_.md)
* [System Settings Panel](_documentation_system-settings-panel-guide_.md)
* [Instruments Panel](_documentation_instruments-panel-guide_.md)
* [Buy Filters Panel](_documentation_buy-filters-panel-guide_.md)
* [Ranking Panel](_documentation_ranking-panel-guide_.md)
* [Sell Filters Panel](_documentation_sell-filters-panel-guide_.md)
* [Backtest Panel](_documentation_backtest-panel-guide_.md)
* [Backtest Parameterization Panel](_documentation_backtest-parameterization-panel_.md)
* [Metrics Tab](_documentation_metrics-panel-guide_.md)
* [Performance Tab](_documentation_monthly-performance-panel-guide_.md)
* [Positions Tab](_documentation_positions-panel-guide_.md)
* [History Tab](_documentation_history-tab_.md)
* [Trade Signals Tab](_documentation_trade-signals-panel-guide_.md)
* [Manual Results Tab](_documentation_manual-results-tab_.md)
* [Divine Engine Results Tab](_documentation_backtest-results-tab_.md)
* [Overall Top Results Tab](_documentation_overall-top-results-tab_.md)
* [Chart Tab](_documentation_chart-tab_.md)
* [Instrument Tab](_documentation_instrument-tab_.md)
* [Stats Tab](_documentation_stats-tab_.md)
* [Exporting the Backtest Result](_documentation_exporting-the-backtest-result_.md)
* [Trade Plan Calculator](_documentation_trade-plan-calculator_.md)
* [A Strategy for Short Selling](_documentation_a-strategy-for-short-selling_.md)

##### Chapter 5: The Divine Engine & The Boss

* [Introduction to The Divine Engine & The Boss](_documentation_the-divine-engine-and-the-boss_.md)
* [Design Strategies from Scratch](_documentation_design-strategies-from-scratch_.md)
* [Augmenting a Strategy with New Rules](_documentation_augmenting-a-strategy-with-new-rules_.md)
* [Fine-tune a Strategy for the Best Settings](_documentation_fine-tune-a-strategy-for-the-best-settings_.md)
* [Combining All the Features](_documentation_combining-all-the-features_.md)
* [Cyber Code Genetic Programming](_documentation_cyber-code-genetic-programming_.md)

##### Chapter 6: Combine, Stack, and Trade Entire Strategies

* [Multi-Strategy](_documentation_multi-strategy_.md)
* [Meta-Strategy](_documentation_meta-strategy_.md)

##### Chapter 7: Filters & Rules

* [About Filters & Rules](_documentation_about-filters-rules_.md)
* [All Time High/Low Filter](_documentation_all-time-high-low-filter_.md)
* [Aroon Oscillator (ARO) Filter](_documentation_aroon-oscillator-filter_.md)
* [Average Currency Volume Filter](_documentation_average-currency-volume-filter_.md)
* [Average Percent Range (APR) Filter](_documentation_average-percent-range-apr-filter_.md)
* [Average True Range (ATR) Filter](_documentation_average-true-range-atr-filter_.md)
* [Beta Index Filter](_documentation_beta-filter_.md)
* [Bollinger Bands (BBands) Filter](_documentation_bollinger-bands-bbands-filter_.md)
* [Cash Equivalent Score Filter](_documentation_cash-equivalent-score-filter_.md)
* [Chaikin Oscillator Filter](_documentation_chaikin-oscillator-filter_.md)
* [Chande Momentum Oscillator (CMO) Filter](_documentation_chande-momentum-oscillator-cmo-filter_.md)
* [Correlation Filter](_documentation_correlation-filter_.md)
* [Day of the Week Filter](_documentation_day-of-the-week-filter_.md)
* [Discount Filter](_documentation_discount-filter-guide_.md)
* [Fixed ATR Stop Loss Filter](_documentation_fixed-atr-stop-loss-filter_.md)
* [Goldilocks Filter](_documentation_goldilocks-filter-guide_.md)
* [HiLo Over Time Filter](_documentation_hilo-over-time-filter_.md)
* [Index ATR Spread Filter](_documentation_index-atr-spread-filter_.md)
* [Instrument Public Age Filter](_documentation_instrument-public-age-filter_.md)
* [Kaufman Efficiency Ratio Filter](_documentation_kaufman-efficiency-ratio-filter_.md)
* [Lowest Close Index Filter](_documentation_lowest-close-index-filter_.md)
* [Lowest Close Position Filter](_documentation_lowest-close-position-filter_.md)
* [MACD Filter](_documentation_macd-filter_.md)
* [Moving Average Cross Over Filter](_documentation_moving-average-cross-over-filter_.md)
* [Moving Average Persistence Filter](_documentation_moving-average-persistence-filter_.md)
* [N ATR Above/Below SMA Filter](_documentation_n-atr-above-below-sma-filter_.md)
* [Octane Indicator Filter](_documentation_octane-indicator-filter-guide_.md)
* [Perfect Stop Filter](_documentation_perfect-stop-filter_.md)
* [Portfolio Position Limit Filter](_documentation_portfolio-position-limit-filter_.md)
* [Portfolio Threshold Filter](_documentation_portfolio-threshold-filter_.md)
* [Position Duration Filter](_documentation_position-duration-filter_.md)
* [Price Range Filter](_documentation_price-range-filter_.md)
* [Price Range Index Filter](_documentation_price-range-index-filter_.md)
* [Primitive Pattern Filter](_documentation_primitive-pattern-filter_.md)
* [Rate of Change (ROC) Index Filter](_documentation_rate-of-change-index-filter_.md)
* [Rate of Change (ROC) Filter](_documentation_rate-of-change-roc-position-filter_.md)
* [Retracement Filter](_documentation_retracement-filter_.md)
* [Return Index Filter](_documentation_return-index-filter_.md)
* [RSI Filter](_documentation_rsi-filter_.md)
* [Simple Moving Average (SMA) Index Filter](_documentation_simple-moving-average-sma-index-filter_.md)
* [Simple Moving Average (SMA) Position Filter](_documentation_simple-moving-average-sma-position-filter_.md)
* [SMI Filter](_documentation_smi-filter_.md)
* [Stochastic Oscillator Filter](_documentation_stochastic-oscillator-filter_.md)
* [Surprise Day Filter](_documentation_surprise-day-filter_.md)
* [Top N% Threshold Filter](_documentation_top-n-threshold-filter_.md)
* [Volatility Change Index Filter](_documentation_volatility-change-index-filter_.md)
* [Volatility Change Filter](_documentation_volatility-change-position-filter_.md)
* [Volatility Range Filter](_documentation_volatility-range-filter_.md)
* [Volatility Range Percentile Index Filter](_documentation_volatility-range-percentile-index-filter_.md)
* [Volatility Range Percentile Filter](_documentation_volatility-range-percentile-position-filter_.md)
* [ATR Distance Below SMA Rule](_documentation_atr-distance-below-sma-rule_.md)
* [Correlation Rule](_documentation_correlation-rule_.md)
* [Impulse Score Rule](_documentation_impulse-score-rule_.md)
* [Index ATR Spread Rule](_documentation_index-atr-spread-rule_.md)
* [Lowest Close Rule](_documentation_lowest-close-rule_.md)
* [Moving Average Persistence Rule](_documentation_moving-average-persistence-rule_.md)
* [PB Pattern Score Rule](_documentation_pb-pattern-score-rule_.md)
* [Volatility Rule](_documentation_volatility-rule_.md)

##### Chapter 8: Settings Page

* [Settings Page Overview](_documentation_settings-page-overview-guide_.md)
* [Automation Tab](_documentation_automation-tab-guide_.md)
* [Appearance Tab](_documentation_appearance-tab_.md)
* [Database Tab](_documentation_database-tab-guide_.md)
* [Interactive Brokers Tab](_documentation_interactive-brokers-tab-guide_.md)
* [Miscellaneous Tab](_documentation_miscellaneous-tab-guide_.md)

##### Chapter 9: Help Page

* [Help Page Overview](_documentation_help-page-overview-guide_.md)
* [Frequently Asked Questions](_documentation_frequently_asked_questions_.md)
* [Tutorials](_documentation_video-tutorials-deprecated_.md)

##### Miscellaneous Functions

* [Application Log Page](_documentation_application-log-page_.md)
* [Software Version and Updates](_documentation_software-version-and-updates_.md)
* [Portfolio Boss Forum](_documentation_portfolio-boss-forum_.md)

* * *

## Comprehensive User Guide for Portfolio Boss

**Copyright © 2025 Portfolio Boss, Inc.** [**Back to Top**](_documentation_user-guide-overview_.md#backtotop)

#### _documentation_video-tutorials-deprecated.md

> Source: https://portfolioboss.com/documentation/video-tutorials-deprecated
> Scraped: 3/1/2026, 2:09:23 AM

[!](_wp-content_uploads_2019_10_Video-Tutorials.png.md)

This Tab contains video tutorials for some of Portfolio Boss's features. You can click on one of the topics here, and a video player will show up. You can access this Tab by clicking the “Help” button (at the left bar of the interface), and select the _Tutorials_ Tab.

[!](_wp-content_uploads_2019_10_Tutorials-Tab-with-Video-Player.png.md)

Keep in mind, these tutorials are for Portfolio Boss version 4 and older. As of now, they have been superseded by the User Guide you're reading now.

Please visit [PortfolioBoss.com](index.md) to see the video training modules bundled with your license, where you can learn about your _licensed_ _strategies_ in great detail. This user guide (or the video tutorials in this Tab), does not explain each strategy specifically, whereas in the training modules you'll learn the philosophy behind the strategy, as well as how to use it properly.

* * *

#### Notes:

*   In the near future, we plan to remove these video tutorials entirely, so any links presented in this Tab will direct you to the User Guide.

*   If for some reason you can't access the video tutorials presented in this tab, you can still view them here: [https://api.portfolioboss.com/Tutorials/](https://api.portfolioboss.com/Tutorials/)

You have already reported this .

#### _documentation_volatility-change-index-filter.md

> Source: https://portfolioboss.com/documentation/volatility-change-index-filter
> Scraped: 3/1/2026, 2:09:16 AM

[!](_wp-content_uploads_2019_10_Volatility-Change-Index-Filter-Buy.png.md)

[!](_wp-content_uploads_2019_10_Volatility-Change-Index-Filter-Sell.png.md)

This filter is similar to the [“Volatility Change Position Filter”](_documentation_volatility-change-position-filter_.md), in that it looks for the _percentage change_ in volatility (decreasing or increasing) for the past certain period, but instead of instruments, this filter looks at an _index's_ volatility change.

If the index's volatility increases/decreases more than a certain percentage during the specified period, then you're allowed to enter (or exit) Positions. Essentially, this filter allows you to look at the _implied_ market volatility.

For example, if the market is becoming more volatile, then you may trade your Portfolio as the potential for profit is greater (but beware of risks), and vice versa.

* * **1.**  The first parameter defines the period to look for such _volatility change_ in the index. Let's say you want to see _how much_ the index's volatility has changed in the past one month, then enter “1 month” here.

[!](_wp-content_uploads_2019_10_Volatility-Change-Index-Filter-1st-Param.png.md)

* * **2.**  The second parameter defines the _index_ whose volatility is the yardstick for considering instruments. Obviously, the index must be correlated to your Portfolio.

[!](_wp-content_uploads_2019_10_Volatility-Change-Index-Filter-2nd-Param.png.md)

You can also input any instrument here (usually ETF) that may benefit your strategy. Keep in mind, you shouldn't enter a delisted instrument here (indicated by square brackets suffix containing a number); otherwise a warning is given and you can't backtest the strategy:

!

* * **3.**  The third parameter defines whether the index's volatility must “Increase more than” or “Decrease more than” the threshold _percentage change_ during the specified period.

[!](_wp-content_uploads_2019_10_Volatility-Change-Index-Filter-3rd-Param.png.md)

* * **4.**  The fourth parameter defines the _threshold percentage change_ of the index's volatility.

[!](_wp-content_uploads_2019_10_Volatility-Change-Index-Filter-4th-Param.png.md)

* * *

#### Note:

Two indicators will be applied _below_ the Price Chart once this filter is applied. One indicator shows the index's volatility during the specified period, while the other indicator shows that volatility's _percentage change_.

[!](_wp-content_uploads_2019_10_Volatility-Change-Index-Filter-Indicator.png.md)

[**Back to Top**](_documentation_volatility-change-index-filter_.md#backtotop)

You have already reported this .

#### _documentation_volatility-change-position-filter.md

> Source: https://portfolioboss.com/documentation/volatility-change-position-filter
> Scraped: 3/1/2026, 2:09:09 AM

[!](_wp-content_uploads_2019_10_Volatility-Change-Position-Filter-Buy.png.md)

[!](_wp-content_uploads_2019_10_Volatility-Change-Position-Filter-Sell.png.md)

This filter calculates the _change_ of the instrument's volatility, whether the volatility is increasing or decreasing during the past certain period.

For example, if a Position's volatility _increased_ more than 30% (for the past 3 months), then the strategy will exit out of that Position as it's becoming much riskier. In other words, the Position is more likely to maintain the _implied_ higher volatility than you can tolerate.

[!](_wp-content_uploads_2019_10_Volatility-Change-Overview_00000.png.md)

[!](_wp-content_uploads_2019_10_Implied-Volatility_00000.png.md)

Or the reverse (as a Buy Filter): if an instrument's volatility _decreases_ more than 20% (for the whole past month), then the instrument is likely to maintain the implied lower volatility, thus a more stable trading when you enter its Position.

If an instrument's volatility doesn't change much during the specified period (either _flat high_ volatility or _flat low_ volatility), then its volatility _percentage change_ will be near 0%.

[!](_wp-content_uploads_2019_10_Constant-High-Volatility_00000.png.md)

* * **1.**  The first parameter defines how many days or months to look for the _volatility change_. The longer the period, the more accurate the signal is; that is, the implied volatility is correct.

[!](_wp-content_uploads_2019_10_Volatility-Change-Position-Filter-1st-Param.png.md)

* * **2.**  The second parameter defines whether the volatility must “Increase more than” or “Decrease more than” the specified _percentage change_. “Increase more than” implies a more volatile instrument, whereas “Decrease more than” implies a more stable instrument. 

[!](_wp-content_uploads_2019_10_Volatility-Change-Position-Filter-2nd-Param.png.md)

Do understand that you don't want a perfectly stable instrument as you'll gain nothing (even though you lose nothing as well), as riskier instruments also carry with them a potentially higher return (despite potentially higher losses).

* * **3.**  The third parameter defines the threshold _percentage change_ in volatility. Generally, a value of 20% is useful for generating correct signals.

[!](_wp-content_uploads_2019_10_Volatility-Change-Position-Filter-3rd-Param.png.md)

* * *

#### Note:

Once you applied this filter, two indicators appear _below_ the [Price Chart](_documentation_instrument-tab_.md). One indicator is for the instrument's volatility, while the other is for the _percentage change_ of that volatility during the specified period.

[!](_wp-content_uploads_2019_10_Volatility-Change-Position-Filter-Indicator.png.md)

Keep in mind, the _percentage change_ may go in the negative values; that means a _decrease_ in volatility (an _overall decrease_ from the start of the period to the end). Remember that each point in the indicator is the reading from that point to the start of the specified period (e.g 3 months).

[**Back to Top**](_documentation_volatility-change-position-filter_.md#backtotop)

You have already reported this .

#### _documentation_volatility-range-filter.md

> Source: https://portfolioboss.com/documentation/volatility-range-filter
> Scraped: 3/1/2026, 2:09:21 AM

* * * [!](_wp-content_uploads_2019_10_Volatility-Range-Filter-Buy.png.md)

[!](_wp-content_uploads_2019_10_Volatility-Range-Filter-Sell.png.md)

This filter looks at an instrument's volatility (the ups and downs of its price) to determine whether it will be bought or sold. This is good for example if you want to trade highly volatile, thus risky instruments, in the hope of generating higher returns (but beware of greater drawdowns). 

[!](_wp-content_uploads_2019_10_Both-Sides-of-Volatile-Instrument_00000.png.md)

The reverse is also true, i.e. if you want to trade only stable instruments, thus reducing risk.

[!](_wp-content_uploads_2019_10_Aint-Nothing.png.md)

* * *

Now, about this filter's parameters:

**1.**  The first parameter defines the period of time in which the volatility is calculated. Let's say you want to know a stock's volatility based on a period of 3 months, then input a value of 3 months here (type the value, then choose from the dropdown either Days or Months). 

[!](_wp-content_uploads_2019_10_Volatility-Range-Filter-1st-Param.png.md)

This means you're looking at the instrument's volatility calculated from _today_ until 3 months ago (averaged).

* * **2.**  The second parameter defines whether the instrument's volatility must be “Less than” or “Greater than” the _threshold_ volatility.

[!](_wp-content_uploads_2019_10_Volatility-Range-Filter-2nd-Param.png.md)

You may also choose “Between” or “Not between” the volatility values, thus you must set the minimum and maximum volatility values on the next two parameters that show up. 

[!](_wp-content_uploads_2019_10_Volatility-Range-Filter-3rd-4th-Param.png.md)

“Between” means the instrument's volatility must fall within the Min and Max values, while “Not between” means the instrument's volatility must fall outside the Min and Max values (you're looking at either _very volatile_ or _very stable_ instruments).

* * **3.**  The third parameter defines the _threshold_ volatility value. So for example, an instrument whose 3 months volatility is greater than this value will not be considered as a Buy, etc. This value is stated in percent, from 0 to 100. Higher percentage means higher volatility, and vice versa.

[!](_wp-content_uploads_2019_10_Volatility-Range-Filter-3rd-Param.png.md)

* * *

#### Notes:

*   Once this filter is added to your strategy, a “Volatility” indicator appears just _below_ the Price Chart (on the [Instrument Tab](_documentation_instrument-tab_.md)), that shows the volatility of a particular instrument. 

[!](_wp-content_uploads_2019_10_Volatility-Range-Filter-Indicator.png.md)

A high volatility reading means the price is fluctuating wildly (it goes up or down quite far); whereas low volatility indicates a stable price movement (day-to-day prices are not too different from each other during that period). This indicator immediately changes appearance when you change this filter's period parameter.

*   Keep in mind, just like any indicators that use a period of time, this indicator is a moving window, which means every point on the volatility graph is the volatility reading from that point up to the beginning of the period.

*   If you use this filter with the [SMI filter](_documentation_smi-filter_.md), the Volatility indicator may not show correctly (shows flat line), since the chart has been “taken over” to show the SMI data. So, you must disable the SMI indicators by unchecking them from the indicators list. 

[**Back to Top**](_documentation_volatility-range-filter_.md#backtotop)

Discount Applied Successfully!

Your savings have been added to the cart.

Close

You have already reported this .

Search

#### _documentation_volatility-range-percentile-index-filter.md

> Source: https://portfolioboss.com/documentation/volatility-range-percentile-index-filter
> Scraped: 3/1/2026, 2:09:12 AM

[!](_wp-content_uploads_2019_10_Volatility-Range-Percentile-Index-Filter-Buy.png.md)

[!](_wp-content_uploads_2019_10_Volatility-Range-Percentile-Index-Filter-Sell.png.md)

This filter looks at an _index's_ volatility, and if such volatility is greater (or less) than the volatility of N% instruments within the strategy, then you're allowed to enter or exit Positions.

For example, you are only willing to trade if the SPX's volatility is _greater_ _than_ the volatility of 80% instruments (80% of all instruments within the strategy). So _at least_ there are 80% instruments whose volatility is lower than the SPX.

[!](_wp-content_uploads_2019_10_Percentile-Overview_00000.png.md)

(Note: The diagram above is for illustration purposes only, as SPX rarely reached above 80% volatility)

Another example: You will trade only if there are _at least_ 20% of all instruments whose volatility is greater than the SPX.

This filter has many exotic uses depending on your trading strategy.

For example, if the market is highly unstable, then you want to make sure that at least 80% of your Portfolio is _less_ volatile than the market. Or the reverse, if you want to play high risk trading (thus a greater chance of beating the index), then make sure at least 80% of your Portfolio is _more_ volatile than the index.

You can also use it as a Sell Filter for limiting risks, for example: if 80% or more of your Portfolio is _more_ volatile than the index, then get out of all Positions, etc.

* * **1.**  The first parameter defines the period to look for the volatility of _both_ the index and the instruments.

[!](_wp-content_uploads_2019_10_Volatility-Range-Percentile-Index-Filter-1st-Param.png.md)

* * **2.**  The second parameter defines what index to use. You can also input any instrument here, so long as you believe it may benefit the strategy:

[!](_wp-content_uploads_2019_10_Volatility-Range-Percentile-Index-Filter-2nd-Param.png.md)

You shouldn't input a delisted instrument here (those with square brackets suffix containing a number); otherwise a warning is given and you won't be able to backtest the strategy.

!

* * **3.**  The third parameter defines whether the _index's_ volatility must be “Less than”, “Greater than”, “Between”, or “Not between” the threshold _percentile_ value(s) for the instruments to be considered.

[!](_wp-content_uploads_2019_10_Volatility-Range-Percentile-Index-Filter-3rd-Param.png.md)

[!](_wp-content_uploads_2019_10_Volatility-Range-Percentile-Index-Filter-3rd-Param-B.png.md)

* * **4.**  The fourth parameter defines the threshold _percentile_ value. 

[!](_wp-content_uploads_2019_10_Volatility-Range-Percentile-Index-Filter-4th-Param.png.md)

Remember, this is percentile, not percentage.

So for example, if the index's volatility must be “Greater than” the 80th percentile, then _at least_ 80% of all instruments fall below the index's volatility (could be more than 80%, but not less).

Another example, if the index's volatility must be “Less than” the 80th percentile, then _at least_ 20% of all instruments have _higher_ volatility than the index (could be more than 20%, but not less).

This parameter has a range of value from 0 to 100 (nothing fractional or negative).

* * *

#### Note:

Once this filter is applied, there's a Volatility indicator displayed _below_ the [Price Chart](_documentation_instrument-tab_.md). This is the instrument's Volatility indicator, _not_ the index.

_[!](_wp-content_uploads_2019_10_Volatility-Range-Percentile-Index-Filter-Indicator.png.md)_

**[Back to Top](_documentation_volatility-range-percentile-index-filter_.md#backtotop)**

You have already reported this .

#### _documentation_volatility-range-percentile-position-filter.md

> Source: https://portfolioboss.com/documentation/volatility-range-percentile-position-filter
> Scraped: 3/1/2026, 2:09:21 AM

[!](_wp-content_uploads_2019_10_Volatility-Range-Percentile-Position-Filter-Buy.png.md)

[!](_wp-content_uploads_2019_10_Volatility-Range-Percentile-Position-Filter-Sell.png.md)

This filter looks at an instrument's _volatility_, and if such volatility falls within the specified threshold _percentile_ (in relation to all other instruments within the strategy), that instrument will be considered as a buy/sell.

For example, if an instrument's volatility (for the past 1 month) is _greater_ _than_ the volatility of _at least_ 80% of all instruments, then exit out of that instrument's Position.

[!](_wp-content_uploads_2019_10_Percentile-Overview-Instrument_00000.png.md)

Another example: if you want more risk in your trading (thus potentially higher profits), look for instruments whose volatility is _greater_ _than at least_ 80% of all instruments. In essence, this filter is useful to select instruments whose volatility is _different_ than the majority of the Portfolio.

* * **1.**  The first parameter defines how many days (or months) for calculating the volatility.

[!](_wp-content_uploads_2019_10_Volatility-Range-Percentile-Position-Filter-1st-Param.png.md)

* * **2.**  The second parameter defines whether the instrument's volatility must be “Greater than”, “Less than”, “Between”, or “Not between” the threshold _percentile_, in relation to all other instruments.

[!](_wp-content_uploads_2019_10_Volatility-Range-Percentile-Position-Filter-2nd-Param.png.md)

“Between” is useful if you want at least X% of all instruments to have higher volatility than the instrument, while at least Y% of all instruments have lower volatility. This way you're defining a range, thus the instrument's volatility is not too high and not too low in relation to all instruments.

[!](_wp-content_uploads_2019_10_Volatility-Range-Percentile-Position-Filter-2nd-Param-B.png.md)

“Not between” is the opposite, that is, you're looking for instruments whose volatility is at the extreme end (either too high or too low) in relation to all instruments. It could be useful if you are a no-fuss person: it's either black or white, nothing in between.

[!](_wp-content_uploads_2019_10_Volatility-Range-Percentile-Position-Filter-2nd-Param-C.png.md)

That is, you'll trade either very stable instruments from this Portfolio (no losses and little gain), or trade very risky instruments from this Portfolio (big profit or big losses).

* * **3.**  The third parameter defines the threshold _percentile_.

[!](_wp-content_uploads_2019_10_Volatility-Range-Percentile-Position-Filter-3rd-Param.png.md)

For example, if an instrument's volatility must be “Greater than” the 80th percentile, it means _at least_ 80% of all other instruments are below this instrument's volatility (could be more than 80%, but not less).

Or, if an instrument's volatility must be “Less than” the 80th percentile, it means at least 20% of all other instruments have higher volatility than this instrument (could be more than 20%, but not less).

* * *

#### Note:

Once this filter is applied, there's a Volatility indicator displayed _below_ the [Price Chart](_documentation_instrument-tab_.md) (shows the volatility of a selected instrument during the specified period).

[!](_wp-content_uploads_2019_10_Volatility-Range-Percentile-Position-Filter-Indicator.png.md)

[**Back to Top**](_documentation_volatility-range-percentile-position-filter_.md#backtotop)

You have already reported this .

#### _documentation_volatility-rule.md

> Source: https://portfolioboss.com/documentation/volatility-rule
> Scraped: 3/1/2026, 2:07:54 AM

[!](_wp-content_uploads_2019_10_Volatility-Rule-000.png.md)

This rule ranks your instruments based on their _price volatility_. So, if you want to be safe, look for instruments that have the lowest volatility. If you want to be aggressive (for example buying a dip and selling at a stellar gain), look for instruments that have the highest volatility.

[!](_wp-content_uploads_2019_10_Both-Sides-of-Volatile-Instrument_00000.png.md)

[!](_wp-content_uploads_2019_10_Aint-Nothing.png.md)

* * **1.**  The first parameter, “Highest/Lowest”, lets you pick instruments that have the highest or lowest volatility. If it's set to “Highest”, the most volatile instrument will be ranked at the top. 

[!](_wp-content_uploads_2019_10_Volatility-Rule-1st-Param.png.md)

If it's set to “Lowest”, the least volatile instrument (the most stable) will be ranked at the top.

[!](_wp-content_uploads_2019_10_Volatility-Rule-1st-Param-B.png.md)

* * **2.**  The second parameter defines the period to look for the volatility.

[!](_wp-content_uploads_2019_10_Volatility-Rule-2nd-Param.png.md)

* * *

#### Notes

Regarding the “Offset” and “Weight” parameters, please refer to the guide about [Ranking Panel](_documentation_ranking-panel-guide_.md#offsetweight).

You have already reported this .

