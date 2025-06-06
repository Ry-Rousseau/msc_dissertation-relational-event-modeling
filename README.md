### MSc Dissertation: A Relational Event Model Approach to Online Collective Action: Reddit’s r/amcstock

#### Abstract:
This paper investigates the Reddit-driven AMC short squeeze of 2021 as a casestudy of online collective action. It leverages unique features of the movement to conduct a novel analysis of longitudinal interaction patterns among Reddit users, relating these to the movement’s growth, climax, and decline over a 17-month period. Relational event models are adapted to accommodate large-scale dynamic interaction data using case-control sampling and partial likelihood estimation, developing an approach that can be broadly applied to Internet networks. A sliding window process is used to estimate the temporal variations in the model coefficients. The study finds evidence supporting the staying power of activity and popularity effects throughout the short squeeze life-cycle. It also finds that interaction predictors fluctuate substantially in short-term trends, suggesting that the underlying social formations in the network are highly temporary. The study utilizes an ‘organizational agent’ framework of networked collective action and explores a range of possibilities in an underdeveloped area of study. It examines interaction predictors related to clustering, activity, popularity, and other dyadic effects, advancing empirical knowledge on cases of collective action, and providing a methodological foundation for further studies in this area, particularly in analyzing dynamic network behavior.

All data is derived from the push shift data dump at academic torrents, includes all 2021 comments and submissions, here is the [link](https://academictorrents.com/details/9c263fc85366c1ef8f5bb9da0203f4c8c8db75f4).

The _eventnet_ software used to run relational event model statistics is courtesy of Jeurgen Lerner, and can be downloaded from its [Github]([https://academictorrents.com/details/9c263fc85366c1ef8f5bb9da0203f4c8c8db75f4](https://github.com/juergenlerner/eventnet)). 

All models and visualizations are run in R and raw data parsing is run in Python.

See the pdf of the final dissertation in the parent directory. 

#### Research Extension

The methods used here can be extended for future investigations of Reddit and social media networks. I invite any collaboration on this area, in particular, methods for the analysis of large-N dynamic networks. 

## Replication

### eventnet_configs
XML configuration files for the _eventnet_ java program specifying to the baseline, event-type and weighted REM statistic calculations.

### modeling
The Cox Proportional Hazard models for 3-stage estimations of the relational event models. These correspond to: baseline, time-varying, and event type and weighted (both in stage 3). 

### network construction 
The data filtering and raw data collection steps. Note that raw Reddit data comes in the form of zst compressed files, so a script to handle this data and extract comments and submission related to a specific subreddit is provided.
See paper pdf for network topography. 

#### raw_parsing_scripts
- zst_to_csv.py - module for zst to csv conversion function - decompresses the zst compressed push shift file - courtesy of [u/ramnamsatyahai](https://www.reddit.com/r/pushshift/comments/1cptl87/trouble_with_zst_to_csv/) 
- combine_folder_multiprocess.py - script to filter raw zst files from pushshift dump to get subreddit specific data without full decompression - courtesy of [Watchful1](https://github.com/Watchful1/PushshiftDumps)

### visualization 
Code for all visuals: missing data, time-series and network structure.

