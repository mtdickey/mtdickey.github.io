---
layout: post
title: How will Philip Rivers fit in with the Colts?
subtitle: A preview of what's to come for the Indianapolis offense.
image: /img/Rivers_Colts.jpg
gh-repo: mtdickey/mtdickey.github.io
gh-badge: [star, fork, follow]
comments: true
---

Philip Rivers is heading to Indy.  The 38-year-old veteran signed a one-year, $25 million deal which some are calling an ["all-in"](https://www.theringer.com/nfl/2020/3/18/21184726/philip-rivers-indianapolis-colts-jacoby-brissett-nfl-free-agency) move from the Colts.  Rivers joins fellow NC State alums Jacoby Brissett and Nyheim Hines with hopes to improve on the Colts 7-9 record from last season.  The question is: how will Rivers fit in with this offense?  There is hope that with the Colts' [superior offensive line](https://www.colts.com/news/offensive-line-third-best-nfl-pro-football-focus-2019) Rivers will be able to return to form after a disappointing season resulting in the worst touchdown-to-interception ratio of his career and a 5-11 record.

We can get some answers by looking to the past.  Frank Reich, the Colts' head coach, was the Chargers' Offensive Coordinator for the 2014 and 2015 seasons.  [Reich's bond with Rivers](https://www.colts.com/news/frank-reich-philip-rivers-los-angeles-chargers-san-diego-interview) is a major reason the Colts chose to sign Rivers.  Although, Rivers' statistics from those seasons are not a good sign for what's to come.

First, according to [Pro-Football Reference](https://www.pro-football-reference.com/players/R/RivePh00.htm) Rivers has posted his 2nd and 3rd worst approximate values in the seasons with Reich leading the offense.

![Rivers_Reich_AV](https://raw.githubusercontent.com/mtdickey/mtdickey.github.io/master/img/Rivers_Reich_AV.png)
  - Note: Approximate value (AV) is a metric built by Pro-Football reference to quantify a value for each player-season in order to roughly compare across years and across positions. See [here](https://www.pro-football-reference.com/blog/index6b92.html?p=465) for more information.
  
Rivers actually had a couple of pretty good seasons in terms of yards, including his career high.

![Rivers_Reich_Yards](https://raw.githubusercontent.com/mtdickey/mtdickey.github.io/master/img/Rivers_Reich_Yards.png)

The problem is that he was not efficient on these passes, he was attempting the most passes in the league due to an imbalance on offense caused by an inept rushing game led by Ryan Mathews. 

![Rivers_Reich_YPA](https://raw.githubusercontent.com/mtdickey/mtdickey.github.io/master/img/Rivers_Reich_YPA.png)

Reich and Rivers' years together in 2014 and 2015 are not the whole story though.  There are myriad factors that contribute to an offense's success.  After being fired from the Chargers, Reich went on to show that he can design a [Super Bowl Champion caliber offense](https://www.pro-football-reference.com/teams/phi/2017.htm) with the right players.

Certainly, the Chargers and Colts offensive personnel are quite different.  The Colts have an offensive line that was ranked [3rd by Pro Football Focus](https://www.colts.com/news/offensive-line-third-best-nfl-pro-football-focus-2019) while the Chargers were ranked just 29th.  Although, the Chargers have [receiving corps ranked top-10 by some](https://www.sbnation.com/nfl/2019/5/30/18635928/nfl-wide-receiver-corps-power-rankings-team-2019), while the Colts are thin at the position behind T.Y. Hilton.

This leads the question: what effect has offensive-line and receiver quality had on Rivers in his past seasons?

Let's start with offensive-line quality.  How has Rivers' approximate value changed as his offensive line's approximate value changes?  Luckily approximate value is available for O-linemen too, so we can calculate the average AV for the linemen who played each season with Rivers.  There is a pretty strong correlation (R-squared of 71.4%) between Rivers play and the play of his O-line.

![Rivers_Oline_Corr](https://raw.githubusercontent.com/mtdickey/mtdickey.github.io/master/img/Rivers_OLine_AV_Corr.png)

Now to look at the relationship with receiver quality.  This is an even stronger linear relationship (R-squared of 82.8%) between receivers and Rivers' performance.  This correlation is a classic case of "correlation doesn't imply causation" though.  Does Rivers good play elevate the value of his receivers?  Or do receivers make Rivers play better?  It's not easy to separate these factors in football, so it's worth remembering these caveats for the rest of the analysis.

![Rivers_Receivers_Corr](https://raw.githubusercontent.com/mtdickey/mtdickey.github.io/master/img/Rivers_Receiver_AV_Corr.png)

Combining these two relationships into a simple linear regression model, we find coefficients of 0.65 and 1.55 for offensive-line and receiver value respectively.  You can't beat linear regression when it comes to interpretability.  It's clear now that as the average value of Rivers' receivers increases by 1 his own approximate value increases by 1.55 on average while holding offensive-line value constant.

Extending this, we can apply the model with a "what-if" scenario to predict Rivers' performance with the 2019 Colts roster.

Plugging in the Colts average AVs for offensive line (9.75) and receivers (2.18), we find that his expected approximate value is around 15.  Working backwards, we can expect traditional stats in the realm of 4,300 to 4,500 yards, ~30-34 TDs, and 10-12 INTs with this AV.  This is close to Rivers' average season historically.

To see how this compares with all of his past seasons, see the table below:

| Season | Average O-Line Value | Average Receiver Value | Approximate Value |
| :--- |:--- | :--- | :--- |
| 2009 | 6.375 | 5.11 | 19 |
| 2006 | 8.0|5.25| 18 |
| 2008 | 8.29 | 3.78 | 17 |
| 2010 | 6.25|3.45 | 17 |
| 2011 | 4.5 |5.43 | 17 |
| 2013 | 6.43 | 3.89 | 16 |
| **2020 Predicted** | **9.75** | **2.18** | **15.14** |
| 2018 | 7.2 | 3.88 | 14 |
| 2007 | 5.0 | 3.67 | 13 |
| 2016 | 4.86 | 2.67| 13 |
| 2017 | 4.5 | 3.27 | 13 |
| 2019 | 4.67 | 2.27 |13 |
| 2014 | 3.625| 3.0 | 12 |
| 2015| 3.75 | 2.0 | 12 |
| 2012 | 4.29 | 2.5 | 10 |

Since the draft is coming up, the Colts roster is still in flux.  Let's say they pick up a couple of receivers (hopefully Michael Pittman Jr., as this [mock draft](https://coltswire.usatoday.com/2020/04/20/2020-nfl-mock-draft-indianapolis-colts-final-7-round-projections-trades/) predicts, or Tee Higgins) and T.Y. Hilton can avoid injuries this year.  If the Colts average receiver value increases by 2, we can expect a value of 17 out of Rivers, tied for his 3rd best season of his career.

In conclusion, it's tough to say how Rivers will play with the Colts this year.  While he will have the best collective offensive line of his career, the receiving corps are currently not up-to-par with the Chargers, and his past results with Frank Reich are not encouraging.  Based on a simplistic analysis, we can expect a relatively average year from Rivers if the offensive line and receivers stay where they are.  Although, the Colts would be smart to pick a receiver early in this year's draft to set Philip up for success.

##### Update 2/18/2021:

Rivers had a decent final season of his career after joining the Colts.  Although Pro-Football Reference's Approximate Value for his season was only 12 (below the 15 predicted above), he led the Colts to a 11-5 record and a Wildcard playoff appearance.  For the 8th season in a row and 12th season in his career, he passed for over 4000 yards.  This has him currently tied for 2nd with Brady and Brees for most all-time (behind only Peyton Manning).  

I will make a post about his career and legacy, both in college and the NFL, in due time.  For now I'll just say thanks for all the memories, 17.  You will be missed.
