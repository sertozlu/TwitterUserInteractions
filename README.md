# Twitter User Interactions

## **Overview**
Collect twitter trend data and build network graph per user interactions. Dataset was fetched using Twitter API and Python [Tweepy](http://docs.tweepy.org/en/latest/) module. Recursive calls were made on API to get tweets, friends/followers/retweeters list starting with tweets from a trend search. Pandas Dataframes are used to process and filter the collected user/tweet data. Finally, [networkx](https://networkx.org/) package is used for graph creation.  

## Project Files

```twitter_credentials.cfg``` -> Contains Twitter credentials - to be filled by user.

```TrendDataCollect.ipynb``` -> Jupyter notebook to authenticate to Twitter, collect tweet/user data, and save them into CSV files.

```ObtainNodesEdges.ipynb``` -> Jupyter notebook to process CSV files containing tweet/user data, identify users as nodes and interactions between users as edges of the social network graph, and save them into CSV files.

```SocialNetworkGraph.ipynb``` -> Jupyter notebook to import node/edge CSV files into networkx, provide some stats and produce the social network graph.

## Limitations

* <b>[Twitter rate limits](https://developer.twitter.com/en/docs/rate-limits)</b>: Twitter allows certain number of requests/API calls to the standard API endpoints.

* <b>Handling large networks</b>: Number of vertices and edges can get pretty large with Twitter data. Processing a graph with thousands of nodes and edges can take very long time. For large graphs, more appropriate tools should be used.