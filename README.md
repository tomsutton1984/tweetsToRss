#### What it is

A node.js app that periodically reads a Twitter account and generates an RSS feed from it.

#### Overview

Once it's set up, every minute it gets the most recent tweets for one Twitter account, and writes an RSS file with the content of those tweets.

I've included an <a href="https://github.com/scripting/tweetsToRss/blob/master/exampleFeed.xml">example feed</a> in the repo to show you what one looks like.

#### Set up with Twitter

You need to set four environment variables, to connect this app with Twitter. 

twitterConsumerKey and twitterConsumerSecret -- get these by registering an app at apps.twitter.com. 

twitterAccessToken and twitterAccessTokenSecret -- these are the two keys that a user gets when they do the OAuth dance with your app and Twitter. I get these values by logging in with my app, say Happy Friends or Little Card Editor, and grabbing copies of the values from localStorage where they're kept. I don't know a better way to get these values. If you do, please create a page on the wiki here and I'll have a look.

#### Whose feed, where to save it

Two environment variables configure the twitterToRss app. 

twitterScreenName -- the screen_name of the user whose timeline you want to convert to RSS. Examples of screen names: <a href="https://twitter.com/davewiner">davewiner</a>, <a href="twitter.com/nyt">nyt</a>, <a href="https://twitter.com/dsearls">dsearls</a>, <a href="https://twitter.com/nakedjen">nakedjen</a>.

pathRssFile -- this is the local filesystem path for the file we'll maintain. It's optional, if you don't specify it we write the file as rss.xml in the same folder as the app.

#### Questions, comments?

Please use the <a href="https://groups.google.com/forum/?fromgroups#!topic/server-snacks/KGAqhB3g3Ys">server-snacks</a> list for support.

