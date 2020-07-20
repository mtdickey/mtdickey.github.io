---
layout: post
title: T.J. Warren vs. Jimmy Butler
subtitle: Who's better?
image: /img/Warren_Butler.jpg
gh-repo: mtdickey/mtdickey.github.io
gh-badge: [star, fork, follow]
comments: true
---

The NBA is finally returning this week after taking a break for over 4 months due to the coronavirus pandemic.  One bit of drama to watch in the "Disney bubble" is the [beef between TJ Warren and Jimmy Butler](https://www.sbnation.com/nba/2020/1/8/21057795/jimmy-butler-vs-tj-warren-ejection-miami-heat-indiana-pacers-fight-trash-kisses).  The Pacers and Heat even have neighboring practice courts, so they are bound to clash often.

![Pacers_Heat](https://raw.githubusercontent.com/mtdickey/mtdickey.github.io/master/img/Pacers_Heat.jpg)

In this post, I will be investigating who has the upper-hand in the feud between Warren and Butler.  Butler certainly is the bigger name and has far more accolades to boast: he's a 5-time all-star, 4-time All-Defensive team, 2-time All-NBA player, and Olympic gold-medalist.  However, Warren is a rising star and touts slightly better offensive efficiency metrics.

In this post, I'll be comparing the ["Four Factors"](https://www.basketball-reference.com/about/factors.html) for Butler and Warren:
  1. Shooting (Effective Field Goal Percentage, eFG%)
  2. Turnovers (TOV%)
  3. Rebounding (TRB%)
  4. Free Throws (FT/FGA)

### Shooting

Let's start by comparing their shooting.  We'll use effective field-goal percentage because this accounts for the different values of 2 and 3 point shots.

Warren has a career 53.8% eFG compared to Butler's 49.0% - but is that a significant difference?  We can look at this a question a couple of ways:

 1. Frequentist approach - 2-proportion Z-test:
    
	```
	2-sample test for equality of proportions with continuity correction
	
	data:  c(warren_succ - 2136, butler_succ - 3894) out of c(warren_n - 4012, butler_n - 3894)
	X-squared = 18.284, df = 1, p-value = 1.903e-05
	alternative hypothesis: two.sided
	95 percent confidence interval:
	 0.02245897 0.06074843
	sample estimates:
	 prop 1    prop 2 
	 0.5324028 0.4907991 
	```
	
	This approach shows a highly significant difference.  T.J. has an eFG% that is likely between 2% and 6% greater than Butler's.
	
 2. Bayesian approach - comparing posterior distributions:
	
	In the Bayesian approach, we will start with an open-minded view that Warren and Butler's true eFG% could lie somewhere between 40% and 60% with equal probability of each value in between (this is called the "prior distribution").
	
	We then update this distribution based on the likelihood that we'd observe their career values of eFG%.  The final result are 2 distributions that have almost no overlap, meaning that even if T.J.'s true eFG% was on the low-end of his possible values and Jimmy's was on the high-end, we would still see T.J. as a more efficient scorer.

![efg](https://raw.githubusercontent.com/mtdickey/mtdickey.github.io/master/img/Warren_Butler_efg.png)

We'll chalk this one up to Warren.  This is not super surprising because T.J. is known to be a scorer while Jimmy is more of a defensive/all-around player.  Let's see if the other parts of Jimmy's game make up for his shooting.

### Turnovers

Now let's look at their turnover rates.  This can give a sense of their ball-handling and decision making skills on offense.

Warren has a career 7.0% turnover percentage compared to Jimmy's 9.3%.

This is part of T.J.'s game that doesn't get much credit - but he has spent 3 of the last 4 seasons in the top 10 in the league in TOV%.  We'll chalk this one up to T.J. again.

### Rebounding

We will compare the total-rebounding percentages as a sense of both offensive and defensive rebounding abilities.

The career rebounding percentage for "Jimmy G. Buckets" is 8.5%, Tony Buckets is sitting at 7.8%.  At first glance, this doesn't seem like a huge difference, but let's see if it's statistically significant.

Due to the huge sample size involved with rebounding opportunities throughout their careers, this is signficant.  It's also worth mentioning that Jimmy's rebounding has improved significantly this year, up to 10.9% in his first season with Miami.

Butler takes his first category with an advantage in the rebounding department.

### Free Throws

Finally, we'll use the ratio of free-throws made to field-goals attempted to compare both how often each player gets to the line and how often they make those those free-throws.

On average, Jimmy creates about 0.42 extra points from free-throws for every field goal attempted.  Meanwhile, T.J. is sitting at a much lower 0.16.  This is a significant margin by any test.

This isn't especially surprising: Butler attempts more than twice the number of FTs/game as Warren (6.1 to 2.5).  Jimmy gets the last laugh by taking this category.

### Final Tally

|    Factor   | Warren | Butler |
| :---------- |:------ | :----- |
| Shooting    |   X    |        |
| Turnovers   |   X    |        |
| Rebounding  |        |    X   |
| Free Throws |        |    X   |



So there you have it, T.J. and Jimmy are dead even after comparing the 4 main offensive categories.  They are very different players, each with their unique strengths and weaknesses.  Although I didn't get into the stats here, Butler is absolutely the better defender, but that isn't so clear on the offensive end.

Looking forward, on August 10th the Pacers and Heat will play in one of the final games to determine playoff seeds.  Jimmy has been [talking trash and circled the Pacers game on his calendar](https://twitter.com/SBNation/status/1215112067335774208) so it'll be fun to watch this match-up.  Currently, the Heat are the 4th seed and the Pacers are 2 games back as the 5th seed.