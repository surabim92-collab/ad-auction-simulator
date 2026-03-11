# Ad Auction Simulator

A research-oriented simulation of online advertisement auctions demonstrating the economic and algorithmic principles behind digital advertising marketplaces.
This project models how advertising platforms allocate ad slots and determine pricing using auction-based mechanisms widely used in modern ad exchanges.
he simulator implements and analyzes two important auction mechanisms:
• Second Price (Vickrey) Auction  
• Ad Rank Auction with Quality Score  
These mechanisms form the foundation of ad allocation systems used by platforms such as Google Ads, Facebook Ads, and Amazon Sponsored Ads.

## Motivation

Digital advertising platforms must solve three fundamental problems:

1. Which advertiser should display their ad?
2. In what order should ads appear?
3. How much should the advertiser pay?

To solve these problems, modern platforms use auction algorithms that combine ideas from:

• Game Theory  
• Algorithm Design  
• Market Economics  
• Machine Learning

This project simulates these auction mechanisms to understand how bids, competition, and quality signals influence platform revenue and advertiser outcomes.

## Background: Online Ad Auctions

Search engines and social media platforms allocate advertising slots through real-time auctions.
When a user performs a search or opens a feed, advertisers compete for the opportunity to display their ad
These auctions typically occur within milliseconds.

Key goals of the system include:
• Efficient allocation of ad slots  
• Incentivizing truthful bidding  
• Maximizing platform revenue  
• Maintaining user experience

## Auction Mechanisms Implemented

### 1. Second Price Auction (Vickrey Auction)

In a second price auction:

• The highest bidder wins the auction  
• The winner pays the second highest bid

Example:

Advertiser A bids: 80  
Advertiser B bids: 70  
Advertiser C bids: 60  

Winner: A  
Price Paid: 70

This mechanism encourages **truthful bidding** because bidders gain no advantage by misreporting their true valuation.
Second price auctions are a fundamental concept in **mechanism design and algorithmic game theory**.


### 2. Ad Rank Auction with Quality Score

Modern advertising systems incorporate additional signals beyond bids.

Platforms calculate an **Ad Rank**:

Ad Rank = Bid × Quality Score

Quality score represents:

• Ad relevance  
• Click-through rate (CTR)  
• Landing page quality  
• User experience

This ensures that advertisers with better user experience can win even with lower bids.

Example:

Advertiser A: Bid = 10, Quality = 9 → Rank = 90  
Advertiser B: Bid = 15, Quality = 3 → Rank = 45

Advertiser A wins despite bidding less.



## Pricing Rule

The simulator approximates the **Generalized Second Price (GSP) Auction** used in many advertising systems.
Winner price:
Price = (Ad Rank of next advertiser) / (Winner Quality Score)
This ensures the winning advertiser pays just enough to maintain their ranking position.


## Monte Carlo Simulation

The simulator runs multiple auction rounds with randomly generated bids to analyze:

• Expected platform revenue  
• Revenue distribution across auctions  
• Effects of competition among bidders

This helps estimate auction behavior under different market conditions.

## Visualization

The notebook generates visualizations such as:
• Revenue distribution histogram  
• Ad Rank comparison plots  
These visualizations help interpret the economic behavior of the simulated auction environment.

## Technologies Used

Python  
NumPy  
Pandas  
Matplotlib  
Seaborn  
Jupyter Notebook

## Applications

Understanding auction-based allocation mechanisms is important in many industries:

Digital Advertising  
Online Marketplaces  
Ride-sharing platforms  
E-commerce ranking systems  
Cloud resource allocation

Auction theory is widely applied in real-world platforms such as:

Google Ads  
Facebook Ads  
Amazon Sponsored Products  
Uber Surge Pricing Systems


## Limitations
This simulator simplifies many aspects of real ad exchanges.

Missing components include:

• Click-through rate prediction  
• User targeting models  
• Multiple ad slot auctions  
• Budget constraints for advertisers  
• Strategic bidder behavior

Future work could extend the simulator by incorporating these elements.

## Future Improvements

Possible extensions of the project include:

• Multi-slot auction simulation  
• CTR prediction models  
• Budget constrained advertisers  
• Reinforcement learning bidding strategies  
• Large scale advertiser simulations

## Academic Relevance

This project relates to topics studied in:

Algorithmic Game Theory  
Mechanism Design  
Market Design  
Computational Economics

These areas explore how algorithms interact with strategic human behavior in digital marketplaces.


## Author
Surabi Mondal

Computer Science Student  
Indian Institute of Engineering Science and Technology (IIEST), Shibpur
