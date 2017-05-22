# Climate tweets, May 2017

This file contains 122,379 tweets about climate change from approximately 5/8–5/18, 2017. The tweets were downloaded using [`rtweet`](https://cran.r-project.org/web/packages/rtweet/index.html) and Twitter's REST API. Specifically, I searched for tweets containing "climate change" or "global warming":

    search_tweets(q = '"climate change" OR "global warming"', n = 1000000, include_rts = FALSE, retryonratelimit = TRUE)

I then deleted some extraneous variables to keep the size of this file reasonable.

## Variables

**screen_name**: The username of the account that sent the tweet.

**user_id**: Twitter's user_ID string for the account that sent the tweet.

**created_at**: The date of the tweet in POSIXct format.

**status_id**: Twitter's status ID for the tweet.

**text**: The text of the tweet.

**retweet_count**: The number of retweets a tweet received.

**favorite_count**: The number of favorites a tweet received.

**in_reply_to_status_screen_name**: The screen name that the tweet is replying to, if any.

**urls_expanded**: The URL mentioned in the tweet, if any

**mentions_screen_name**: The screen name of any accounts @mentioned in the tweet.

**hashtags**: The hashtags used in the tweet, separated by spaces.