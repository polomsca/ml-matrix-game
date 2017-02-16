# One-shot games

## Overview

This is a compilation of data from several behavioral economics experiments where people play various games like the [Prisoner's dilemma](https://en.wikipedia.org/wiki/Prisoner's_dilemma) or [Stag Hunt](https://en.wikipedia.org/wiki/Stag_hunt). 

To contribute to this [database](https://github.com/polomsca/one-shot-games/blob/master/gamesmxn.csv), you can submit any experiment with games that are one-shot (no finitely repeated or "second-mover" games) and in matrix form (also known as bimatrix, normal, or strategic). Please use the following format:

`paper` | `game` | `matrixrow` | `matrixcol` | `choicerow` | `choicecol` | `shape` | `symmetric` | `repeats` | `subjects` 
--- | --- | --- | --- | --- | --- | --- | --- | --- | ---
stahlwilson1994 | 1 | 40 10 70; 20 80 0; 30 100 60 | | 11 40; 0 40; 29 40 | | 3 3 | 1 | | 40

A couple notes on formatting:

- `matrixrow` : The payoff matrix for the row player. In each row, separate elements with a space. Separate rows with semicolons. This lets `numpy.matrix()` return a matrix with the correct dimensions.
- `matrixcol` : If the game is symmetric and the player results are pooled, you may leave this field blank.
- `choicerow` : The frequency of each choice for the row player. If frequencies are represented as fractions, separate integers with a space, not a forward slash. Separate choices with a semicolon. 
- `choicecol` : If the game is symmetric, and the player results are pooled, you may leave this field blank.
- `symmetric` : `1` if symmetric, `0` otherwise.
- `repeats` : Entries of other games that have identical payoff matrices.

This is also a collection of [machine learning](https://en.wikipedia.org/wiki/Machine_learning) models that attempt to predict how people make decisions in these games. To contribute to this collection, you can submit any relevant models or papers.

## ML models based on

- Hartford et al (2016) : Deep learning for predicting human strategic behavior
  - [FFNet](https://github.com/polomsca/one-shot-games/blob/master/modelsffnet.ipynb)
  - [GameNet]()

## Games taken from

- Haruvy et al (2001) : Modeling and testing for heterogeneity in observed strategic behavior

- Haruvy and Stahl (2007) : Equilibrium selection and bounded rationality in symmetric normal-form games

- Rogers et al (2009) : Heterogeneous quantal response equilibrium and cognitive hierarchies

- Stahl and Haruvy (2008) : Level-n bounded rationality and dominated strategies in normal-form games <sup>[1](#myfootnote1)</sup>

- Stahl and Wilson (1994) : Experimental evidence on players' models of other players

- Stahl and Wilson (1995) : On players' models of other players, theory and experimental evidence

- Weizsäcker (2000) : Ignoring the rationality of others, evidence from experimental normal-form games (only games taken from Costa-Gomes et al (2001) : Cognition and behavior in normal-form games, an experimental study)

- Goeree and Holt (2001) : Ten little treasures of game theory and ten intuitive contradictions (only games from "A Matching Pennies Game" and "The Kreps Game")

- Rydval and Ortmann (2005) : Loss avoidance as selection principle, evidence from simple stag-hunt games

- Haruvy and Stahl (1998) : An empirical model of equilibrium selection in symmetric normal-form games

## Footnotes

[<a name="myfootnote1">1</a>] Appendix D, Game 10 is printed incorrectly as

`12` | `63` | `22` 
--- | --- | ---
0 | 0 | 38 
55 | 25 | 40 
35 | 35 | 43 

Game 10 should be read instead as

`0` | `12` | `63` 
--- | --- | ---
25 | 0 | 0
0 | 55 | 25 
100 | 35 | 35 
