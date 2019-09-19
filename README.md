## Module 4 - Probability Theory

```
table = matrix(c(10,20,20,40),ncol=2,byrow=TRUE)

colnames(table) = c("B","B1")
rownames(table) = c("A","A1")

table = as.table(table)
table
```

```
probA = sum(table[1,])/sum(table)
probA

probB = sum(table[,1])/sum(table)
probB

probAB = probA + probB
probAB
```

![table](https://i.gyazo.com/832b4ac53c97010ba2d53c5084542adc.png

Based on the table, the probability of landing on Event 'A' is .3333 or 1/3. The probability for landing on Event 'B' is also 1/3, and the probability for landing on either event A or B is .5511, or 55.11%.

# Bayes Theorem

"Jane is getting married tomorrow, at an outdoor ceremony in the desert. In recent years, it has rained only 5 days each year. Unfortunately, the weatherman has predicted rain for tomorrow. When it actually rains, the weatherman correctly forecasts rain 90% of the time. When it doesn't rain, he incorrectly forecasts rain 10% of the time. What is the probability that it will rain on the day of Jane's wedding?"

"Notation for these events appears below.

Event A1. It rains on Jane's wedding.
Event A2. It does not rain on Marie's wedding.
Event B. The weatherman predicts rain.

In terms of probabilities, we know the following:
P( A1 ) = 5/365 =0.0136985 [It rains 5 days out of the year.]
P( A2 ) = 360/365 = 0.9863014 [It does not rain 360 days out of the year.]
P( B | A1 ) = 0.9 [When it rains, the weatherman predicts rain 90% of the time.]
P( B | A2 ) = 0.1 [When it does not rain, the weatherman predicts rain 10% of the time.]"

```
pA1 = .0136
pA2 = .9863

pBgivenA1 = .9
pBgivenA2 = .1

pA1givenB = pA1*pBgivenA1/(pA1*pBgivenA1+pA2*pBgivenA2)
pA1givenB
```

Although one might, myself included, expect the probability of rain to be fairly high given the weatherman is correct 90% of the time, we can see that using the given probabilities alongside Baye's theorem, the probability of it raining on Jane's wedding is only 11.04%. This can be mathematically verified by plugging each probability and conditional probaility into Baye's equation. Since it only rains 5 days out of 365, this means that even though the weatherman has been considerably accurate in the past, it is still very likely that he is incorrect on his prediction because of how small the initial chance of it raining is. For example, if someone were to win a raffle out of one-thousand people, their "success rate" would be 100%, however this does not change the fact that for the next raffle, their odds are still one to one-thousand. 

[Visit my GitHub Profile](https://github.com/adamwk97)
