**OP-ED: OF POLITICS AND PREDICTABILITY**

Curren A. Iyer

Nov 10, 2014

For predicting the outcomes of elections, we look at polls, as they are seemingly the most accurate metric for viewing public opinion.  But how accurate are these polls?  People are skeptical of what polls say, as there are numerous factors that can potentially skew the results, such as who responds to these polls and how opinions change over time (we will call these *biases*).  I will make the case that polls are in fact very accurate in predicting election results; we just have to make sure we remove the biases in the data.

Let's look at the 2014 elections, where, against all odds, the Republicans won 23 seats (quite a feat!).  In the aftermath of this historic victory, major political buffs and the media were scratching their heads: how could this have happened?  First, let's take a sample of polls from the time period and take the average across their predicted spread (where *spread* refers to the difference in percentage of votes for the Republican vs. Democratic candidate).  If the spread for a state favors a certain party, then we can say that that party is expected to win that state's seat (i.e. if the spread is 15% in favor of the Republicans, they would be expected to win that seat).  After taking the average for the expected spread among various polls across the nation, let us compare that to the actual results of the election.  We can see our model in the figure below. 

![image](images/Senate_Seats.png?raw=true)
Caption: Our results compared to the actual number of seats won (23) - What went wrong?

Not a bad start, but the fact that our expected number of seats (i.e. where the bar graph clusters the most - approximately 20) is off by approximately 3 seats (which, out of 23, is a pretty sizable difference) still leaves something to be desired.  So what went wrong?  By simply taking the average across multiple polls from across 2014 leading up to the election, we are certainly leaving out a lot of key information.  For instance, polls that are taken closer to the election date are *generally* more accurate than polls taken further away.  Furthermore, polls taken across an entire state are also better predictors than polls taken across certain cities or counties (although there are some cases where a major city can accurately represent the state's opinion).  So how do we take these into account?  What we ended up doing was giving different polls different *weights*, such that polls that were more relevant in terms of timeframe or sampling size would play a larger role in calculating the expected number of seats to be won.  We can see our results below.

![image](images/Senate_Seats_Weighted.png?raw=true)
Caption: Our results after giving different polls more weight, compared to the actual number of seats won (23).  Close, but can we do better?

Okay, so we're doing a bit better.  But is this enough?  What other factors could be interfering with our accuracy?  Well, we talked about the timing of the poll, but timing is a bit more complex than simply how opinions shift, as we should also talk about the context in which events happen.  For instance, after the 8 years of Republican leadership, the 2008 elections illustrated a vast shift in the political status quo, as the Democrats beat out their Republican opponents to score many key victories in the election.  Therefore in the years following, people's opinions were a bit biased by the fact that they wanted a change in leadership.  So how do we address this abstract concept?  I will spare you some of the more specific details, but some of our smart statistician friends at the Huffington Post were actually able to "quantify" this bias (i.e. give it a numerical value that makes it relevant to our data), thus allowing us to account for it in our predictions.  Taking this bias factor into account, as well as our previously weighted polls, we plot the data once again.

![image](images/Senate_Seats_Weighted_Unbiased.png?raw=true)
Caption: Our results after giving different polls more weight and removing a bias factor, compared to the actual number of seats won (23).  Not bad!