# Thinking in Bayes
## Key Ideas
 - One way of thinking about probability is considering multiple possible worlds
 - The world where A is the case, and the world where not-A is the case
 - The base rate * likelihood of observation in that world = chance of being in that world
 - The numbers you use are relative, not absolute (i.e.  0.2 and 0.8 ≡ 20 and 80 ≡ 1/5 and 4/5)
- Try to model the real world
- As finegrained as possible

## The cancer example
1% of women in a certain group have breast cancer. 80% of women with breast cancer will get a positive mammogram result, and 9.6% of women without breast cancer will also get a positive result. If a woman in that group has a positive mammogram result, what are the chances she has breast cancer?

|        | Cancer | Not Cancer | 
| :---:        |    :----:   | :---:  |
| Base rate     | 1       | 99 |
| LOO  | 80       | 9.6 |
| Relative chance | 80       | 950.4 |

Chance of breast cancer = 80/(80+950.4) = 0.077

## The biased coin example
The chance of a biased coin is 50%. Of biased coins, 2/3 are biased towards heads (producing heads 3/4 of the time) and 1/3 are biased towards tails (producing tails 3/4 of the time). You flip a coin 3 times and get THT. What is the probability of the coin being fair?

|        | Fair | Hbias | Tbias |
| :---:        |    :----:   | :---:  | :---: |
| Base rate     | 3       | 2 | 1 |
| LOO (of getting THT) | 1/8       |3/64 |6/64 |
| Relative chance | 3/8       | 6/64 |6/64 |

Chance of a fair coin = (1/8)/(1/8+3/64+6/64) = 8/17

## The dresser example
You have a dresser with 8 drawers. You think the probability of your socks being in your dresser is 4/5. You have checked 6 drawers, and haven't found your socks. What are the chances your socks are in the next drawer you check?

|        | in  d1 | d2 | d3 | d4 | d5 | d6 | d7 | d8 | outside of dresser |
| :---:  |  :----:   | :---:  | :---: | :---: | :---:  |  :----:   | :---:  | :---: | :---: |
| Base rate     | 1       | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 2 |
| LOO (not in drawer 1) | 0 |1 |1 | 1 |1 |1 | 1 |1 | 1 |
| LOO (not in drawer 2) | 1 |0 |1 | 1 |1 |1 | 1 |1 | 1 |
| LOO (not in drawer 3) | 1 |1 |0 | 1 |1 |1 | 1 |1 | 1 |
| LOO (not in drawer 4) | 1 |1 |1 | 0 |1 |1 | 1 |1 | 1 |
| LOO (not in drawer 5) | 1 |1 |1 | 1 |0 |1 | 1 |1 | 1 |
| LOO (not in drawer 6) | 1 |1 |1 | 1 |1 |0 | 1 |1 | 1 |
| Relative chance | 0 | 0 | 0 | 0| 0| 0| 1 | 1 | 2 |

Chance of socks in next drawer = 1/(1+1+2) = 1/4

