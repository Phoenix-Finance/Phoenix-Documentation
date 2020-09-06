
# Jacks's Pot - Decentralized No-Loss Lottery

Jack’s Pot is a Wanchain based no-loss lottery DApp inspired the Ethereum based no-loss lottery DApp, [Pool Together.](https://www.pooltogether.com/) The DApp is a collaboration between the Wanchain and [FinNexus](https://finnexus.io/) dev teams and will be operated by FinNexus. As in Pool Together, Jack’s Pot allows DApp users a chance to win a lottery prize by staking their cryptocurrency (in this case, WAN). The staked WAN is delegated to a Wanchain validator, generating rewards as a part of the consensus process. The rewards are then pooled together in a single pot and awarded to the lottery winners.

![](https://cdn-images-1.medium.com/max/5448/1*Kc_PSjwvfZ4Ru6R65eCm0A.png)


## About Jack's Pot No Loss Lottery

Unlike a typical lottery where you lose the funds spent on tickets, with Jack’s Pot, your initial funds are never at risk. By generating the prize pot through delegation rewards from Wanchain’s consensus mechanism, Jack’s Pot allows for a no-loss lottery. Similar to a [prize-linked savings account](https://en.wikipedia.org/wiki/Prize-linked_savings_account), the DApp is a fun and low risk way to play a game of chance and save your WAN at the same time.

## How to Access Jack's Pot

You can access Jack’s Pot either through the [web interface](https://jackspot.finnexus.app/#/) or through the Wan Wallet DApp store. You can download the wallet from the Wanchain home page at [https://www.wanchain.org/getstarted/](https://www.wanchain.org/getstarted/), and you can find wallet guides at [http://wanchain.guide/](http://wanchain.guide/) and [http://explorewanchain.org/](http://explorewanchain.org/).

<center>See this video guide for how to add a DApp in the Wanchain Wallet DApp store:</center>
<center><iframe width="560" height="315" src="https://www.youtube.com/embed/5gm2Yq_2S1k" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center><center>*Video Guide*</center>

## Game Rules

* To play the game, users stake one or more tickets with a four digit number on each ticket.
* Users may either choose a specific four digit number through “Self Selection”, or they may generate multiple tickets with randomly four chosen four digit numbers using “Machine Selection”.
* In order to stake a ticket, users must supply 10 WAN for each ticket. This WAN will be locked up in a Wanchain validator node during the duration of the game, and users may withdraw this WAN when they are finished playing.
* The WAN used by staking tickets is delegated to Wanchain’s validator nodes, and the accrued consensus rewards are pooled into the Jackpot
* Every Friday a winning four digit number is selected at random using Wanchain’s true random number generation, and the reward will be awarded to any users who are currently staking a winning number. If multiple users have tickets staked with the winning number, the Jackpot will be split proportionally amongst all tickets with the winning number.
* The lottery closes at 24:00 UTC Thursday, lottery results are settled at 23:00 UTC on Friday, and the lottery re-opens at 00:00 UTC on Saturday.
* If there is no winner, the prize pot will automatically accumulate to the next cycle.
* If you do not withdraw your tickets, those tickets will automatically participate in the next cycle with your chosen numbers.


## Step by Step Guide With Pictures

To play Jack’s Pot users start by choosing a series of four digit numbers. Each four digit number represents a ticket in the Jack's Pot Lotter. All users who pick a ticket(s) with the correct four digit number(s) will win a part of the prize pot.

![Lottery number selection](https://cdn-images-1.medium.com/max/2920/1*msivxENMIWrFK11j9E2PAA.png)<center>*Lottery number selection*</center>
<br><br>
You can also choose for your lottery ticket numbers to be randomly generated if you don’t want to choose your own number. Simply choose how many unique random number tickets you wish to generate:

![Random number ticket generator](https://cdn-images-1.medium.com/max/2780/1*dwLSxnH8FZmwuXzfjkrp5A.png)<center>*Random number ticket generator*</center>
<br><br>
![](https://cdn-images-1.medium.com/max/2000/1*gUyz7BNkN5U9hJlLwwNsyQ.png)

Each lottery round lasts a single week and winnings are distributed 23 hours after the end of the round. The lottery closes at 24:00 UTC Thursday, lottery results are settled at 23:00 UTC on Friday, and the lottery re-opens at 00:00 UTC on Saturday. If no player chooses a winning number during a round, the pooled WAN carries over the next round. If you wish to keep playing, simply leave your WAN staked in the game.

You may stop playing the game at any time by selecting the tickets you wish to withdraw and clicking the ‘Withdraw’ button:

![The ‘Withdraw’ button](https://cdn-images-1.medium.com/max/4360/1*mLQ-w6K38Y2T5-Ojv8wkDg.png)<center>*The ‘Withdraw’ button*</center>
<br><br>
Jack’s Pot uses a liquidity pool which allows for instant withdrawal (ordinarily, unstaking WAN can take up to 3 days). Generally speaking, withdrawal will be instant, although in cases of large numbers of withdrawal at one time, there may be a delay up to 3 days.

## Smart Contract
[The Jack's Pot smart contract on GitHub.](https://github.com/wandevs/jackpot-smart-contracts)