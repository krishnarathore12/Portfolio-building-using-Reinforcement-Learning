# Portfolio-building-using-Reinforcement-Learning
Reinforcement learning algorithms, with the ability to decide the policy on their own are strong models for performing portfolio allocation in an automated manner without the need for continuous supervision. Automation of the manual steps involved in portfolio allocation can prove to be immensely useful, specifically for robo-advisors.

Within the framework of reinforcement learning outlined for this case study, the algorithm undertakes actions, specifically optimal portfolio allocation, contingent upon the current state of the portfolio. Employing a deep Q-learning framework, the components of the model are delineated as follows:

- Agent: Represented by either a portfolio manager, a robo-advisor, or an individual investor.
- Action: Involves the assignment and rebalancing of portfolio weights. The DQN model furnishes Q-values, subsequently translated into portfolio weights.
- Reward function: Predicated on the Sharpe ratio. While various intricate reward functions exist, striking a balance between profit and risk, alternatives encompass percentage return or maximum drawdown.
- State: Characterized by the correlation matrix of instruments over a specified time window. The correlation matrix serves as a pertinent state variable for portfolio allocation, encapsulating information on the relationships between diverse instruments and facilitating portfolio allocation.
- Environment: Manifests as the cryptocurrency exchange.

The dataset utilized for this study is sourced from the Kaggle platform, encompassing daily cryptocurrency prices observed throughout 2018. Notable cryptocurrencies featured in the dataset include Bitcoin, Ethereum, Ripple, Litecoin, and Dash.

## DQN Training for portfolio optimization
![image](https://github.com/krishnarathore12/Portfolio-building-using-Reinforcement-Learning/assets/86671142/13c35ded-ed7f-4d93-a729-1817edbf98a9)


## Training Results 
![image](https://github.com/krishnarathore12/Portfolio-building-using-Reinforcement-Learning/assets/86671142/bfa0cd22-6eb9-4a88-a545-c18ba9479afe)

As shown in the following charts, the code produces the final results along with two charts for each episode. The first chart shows the total cumulative return over time, while the second chart shows the percentage of each cryptocurrency in the portfolio.

## Testing Results
![image](https://github.com/krishnarathore12/Portfolio-building-using-Reinforcement-Learning/assets/86671142/84f2606c-7537-4fe2-a6e5-71aefcb9eabd)

The black line shows the performance of the portfolio, and the dotted grey line is that of an equally weighted portfolio of cryptocurrencies. Despite underperforming during the initial period, the model performance was better overall, primarily due to avoiding the steep decline that the benchmark portfolio experienced in the latter part of the test window. The returns appear very stable, perhaps due to rotating away from the most volatile cryptocurrencies.

## Conclusion
In this case study, we transcended the conventional efficient frontier for portfolio optimization, instead focusing on acquiring a policy for dynamically adjusting portfolio weights. We achieved this by training an RL-based model within a standardized simulation environment. This methodology streamlined the training process and offers potential for further exploration in the realm of general RL-based model training.

