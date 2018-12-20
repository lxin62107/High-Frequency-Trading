High-Frequency-Trading-Strategy

In this project, I explored two execution approaches: Market Taking and Opportunistic Market Making. First, Market Taking (MT) method allows us to send market orders and aggress market immediately with the latest quotes. On the other hand, Opportunistic Market Making (OMM) method is risky, which will send limit orders and wait under the certain time limit for a more beneficial price to fill the order. More specifically, OMM can also be divided into 2 types according to how the limit order prices are set: OMMMid will set the mid-market price as the limit price; OMMSide will set a limit price on your side.

In the first step, I dealt with the Market Taking(MT) method. I calculated the mid-arket prices and calculated PnL under Market Taking(MT) scenario.
In the second step, I dealt with the Opportunistic Market Making(OMMT) method. First, I dealt with OMMMid type. I set a range of the time to execution but would use 10s as the time limit in the analysis. Also, I set 0.0003 as the maximum loss. Then I calculated PnL under 3 scenarios:
(1) In 10s, there is a more beneficial price coming, I would execute the order and aggress the market immediately when the price shows up.
(2) In 10s, there is no beneficial price showing up and do not reach the maximum loss, the Time Limit order would be executed.
(3) If there is no beneficial price showing up but it reaches the maximum loss, the Stop Loss order would be executed. Second, I dealt with OMMSide type using similar analysis.
In the third step, I would analyze the result. I compared the average and median PnL for each order, and the average and median TTE for each order. I counted the number of times when Stop Loss was triggered for OMMMid and OMMSide. I also counted the number of times when Time Limit was triggered for OMMMid and OMMSide. I changed the time to execution(TTE) to see the influence of TTE on the median PnL. I compared differences of three alpha generators: DIS, MAR, SOM.
