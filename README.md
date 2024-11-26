# RTB_Optimization_with_AI_RL

### Abstract

Real-Time Bidding (RTB) is a programmatic advertising technique that enables advertisers to bid on individual ad impressions in real time as they become available. This project presents a reinforcement learning framework using Q-learning and exploration-exploitation technique to optimize bids in RTB. The results demonstrate the ability of Q-learning to adaptively learn optimal bidding strategies that maximize reward based on clicks and conversions.

### Research Questions

- How can Q-learning be applied to optimize RTB bidding strategies?
- What is the impact of user demographics and ad-specific features on bidding outcomes?
- How effective is the learned bidding strategy in maximizing rewards?
- How can the challenges of large-scale data and state spaces be addressed in RTB bid optimization?

### Dataset

The 10,000 row-dataset “Online Advertisements Click-Through Rates” [by Mendeley Data, 2024](https://data.mendeley.com/datasets/wrvjmdtjd9/1) includes user demographics like age, gender, income, location; ad characteristics like types, topics, placements; and behavior metrics like clicks, click time, conversion rate. To simulate RTB  and RL environment, I also added synthetic data columns like Bid and Reward (Click + 3×Conversion).

### Methodology & Experiments

The preprocessing step involved simulating data with encoded categorical and scaled numerical variables for user and ad features. State spaces were defined by these features, while actions represented bid levels. Q-learning was employed to iteratively update Q-values for state-action pairs using a reward function integrating clicks and conversions to measure campaign effectiveness. The model was trained over 500 episodes using an ε-greedy policy to balance exploration and exploitation, and its performance was evaluated on unseen data to compute average rewards.
Q-values formula with α learning rate, γ discount factor, s state, a action:
![image](https://github.com/user-attachments/assets/2a4baba5-2bf1-4732-b6cb-b39d08fba1bd)



### References
- [iPinYou Global RTB Bidding Algorithm Competition Dataset](https://contest.ipinyou.com/ipinyou-dataset.pdf) by Hairen Liao, Lingxiao Peng, Zhenchuan Liu, Xuehua Shen, iPinYou Inc., 2013
- Efficient Bid Optimization Method for Budget Constraint Bidding in Online Advertising by Ke Fang1, Junfeng Wu2, Hao Liu3, Qingyu Cao, IEEE 2024
- [Real-Time Bidding (RTB) seen through the lens of machine learning research](https://numberly.com/en/real-time-bidding-rtb-seen-through-the-lens-of-machine-learning-research/) by Numberly
- ~~[Optimal Real-Time Bidding Strategies](https://arxiv.org/abs/1511.08409) by Junqi Jin et al. ArXiv 2018~~
- ~~[Bidding Machine: Learning to Bid for Directly Optimizing Profits in Display Advertising](https://arxiv.org/abs/1803.02194) by Kan Ren et al. TKDE 2018~~
- OR [Real-Time Bidding by Reinforcement Learning in Display Advertising](https://arxiv.org/pdf/1701.02490) by Han Cai et al. WSDM 2017
- ~~[Real-Time Bidding with Multi-Agent Reinforcement Learning in Display Advertising](https://arxiv.org/pdf/1802.09756) by by Junqi Jin et al. ArXiv 2018~~
- ~~[Real-Time Bidding rules of thumb: analytically optimizing the programmatic buying of ad-inventory](https://wnzhang.net/share/rtb-papers/opt-prog-buy.pdf) by Joaquin Fernandez-Tapia. SSRN 2015~~
- [Real-Time Bidding Algorithms for Performance-Based Display Ad Allocation](https://wnzhang.net/share/rtb-papers/rtb-perf-bid.pdf) by Ye Chen et al. KDD 2011
- [Offline Evaluation of Response Prediction in Online Advertising Auctions](https://wnzhang.net/share/rtb-papers/ctr-bid.pdf) by Olivier Chapelle. WWW 2015.
- [Estimating Conversion Rate in Display Advertising from Past Performance Data](http://wnzhang.net/share/rtb-papers/cvr-est.pdf) by Kuang-chih Lee et al. KDD 2012.
- 
