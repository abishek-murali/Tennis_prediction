# Tennis prediction

I have always been fascinated by sports and stats. The hardest bit of prediciting results for games is discounting for luck. Luck probably has the least impact on the game of tennis as it is played between 2 individuals and one can rely on talent to win the game unlike other sports such as soccer where you are only as good as your time. Given the fact that we know luck plays minimal role in tennis can we predict the outcome of games based on player stats?

## Dataset

UCI has an amazing collection of datasets. For this analysis I've chosen the dataset about 2013 grand slam [tennis dataset](https://archive.ics.uci.edu/ml/datasets/Tennis+Major+Tournament+Match+Statistics).

The dataset consists of men's and women's data from grand slams that took place in 2013. Tennis has 4 grand slams in a year, and it is considered the biggest event in the tennis circuit. The data is split into men's and women's results.

The dataset has 42 attributes -
```
Player 1 Name of Player 1
Player 2 Name of Player 2
Result Result of the match (0/1) - Referenced on Player 1 is Result = 1 if Player 1 wins (FNL.1>FNL.2)
FSP.1 First Serve Percentage for player 1 (Real Number)
FSW.1 First Serve Won by player 1 (Real Number)
SSP.1 Second Serve Percentage for player 1 (Real Number)
SSW.1 Second Serve Won by player 1 (Real Number)
ACE.1 Aces won by player 1 (Numeric-Integer)
DBF.1 Double Faults committed by player 1 (Numeric-Integer)
WNR.1 Winners earned by player 1 (Numeric)
UFE.1 Unforced Errors committed by player 1 (Numeric)
BPC.1 Break Points Created by player 1 (Numeric)
BPW.1 Break Points Won by player 1 (Numeric)
NPA.1 Net Points Attempted by player 1 (Numeric)
NPW.1 Net Points Won by player 1 (Numeric)
TPW.1 Total Points Won by player 1 (Numeric)
ST1.1 Set 1 result for Player 1 (Numeric-Integer)
ST2.1 Set 2 Result for Player 1 (Numeric-Integer)
ST3.1 Set 3 Result for Player 1 (Numeric-Integer)
ST4.1 Set 4 Result for Player 1 (Numeric-Integer)
ST5.1 Set 5 Result for Player 1 (Numeric-Integer)
FNL.1 Final Number of Games Won by Player 1 (Numeric-Integer)
FSP.2 First Serve Percentage for player 2 (Real Number)
FSW.2 First Serve Won by player 2 (Real Number)
SSP.2 Second Serve Percentage for player 2 (Real Number)
SSW.2 Second Serve Won by player 2 (Real Number)
ACE.2 Aces won by player 2 (Numeric-Integer)
DBF.2 Double Faults committed by player 2 (Numeric-Integer)
WNR.2 Winners earned by player 2 (Numeric)
UFE.2 Unforced Errors committed by player 2 (Numeric)
BPC.2 Break Points Created by player 2 (Numeric)
BPW.2 Break Points Won by player 2 (Numeric)
NPA.2 Net Points Attempted by player 2 (Numeric)
NPW.2 Net Points Won by player 2 (Numeric)
TPW.2 Total Points Won by player 2 (Numeric)
ST1.2 Set 1 result for Player 2 (Numeric-Integer)
ST2.2 Set 2 Result for Player 2 (Numeric-Integer)
ST3.2 Set 3 Result for Player 2 (Numeric-Integer)
ST4.2 Set 4 Result for Player 2 (Numeric-Integer)
ST5.2 Set 5 Result for Player 2 (Numeric-Integer)
FNL.2 Final Number of Games Won by Player 2 (Numeric-Integer)
Round Round of the tournament at which game is played (Numeric-Integer)
```

## Methodology

I will be treating this as a classification problem where the results are predicted based on the in-game statistics. I have noticed a lot of sports recently have the odds of a team winning displayed during the game. This is something I haven't noticed in tennis yet.

I have used 3 models for the purpose of my analysis -
1. k-nearest neighbours
2. Regression tree classifier and
3. Logistic regression

I also look at the importance of features at the end of the analysis to see which factors influence the outcome of the game.

## How to run the analysis

1. Clone the repository to your local system
2. Open the Complete_analysis.ipynb file from Jupyter notebook
3. Select the `Run all` option from the in the `Cell` menu. This imports, cleanses, plots and runs analysis on the data.
