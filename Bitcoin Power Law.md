# Definition of The Power Law
- Power laws are mathematical relationships between two quantities, such that one is proportional to a fixed power of the other
- Ubiquitous in nature and social phenomena and in many other parameters 
	- Example
		1. How a city or a nation grows
			- This can be represented mathematically and physically that they emerge anytime there's some kind of process where the output becomes the new input in an iterative process
# Power Law in Bitcoin
1. Power Laws are everywhere in Bitcoin
	1. Price
	2. Hash Rate
	3. Addresses
2. Bitcoin has an interconnected array of power laws that give us the capabilities to predict the future outcome of all properties of Bitcoin

# Giovanni Santostasi
- Bitcoin is similar to natural phenomena and not a common asset.
- Bitcoin is more similar to a city and an organism than a financial asset
- First discovered the Power Law of Bitcoin between price and time
- Over Time, he discovered more and more Power Laws as he delves deeper into the subject
## Theories
### Point 1
- In the beginning, there was nothing &rarr; Nakamoto Satoshi put his intellectual capacity into creating Bitcoin &rarr;
	1. People started mining it
	2. Others invested in it out of curiosity
- As time goes on, people start to invest, mine, trade and participate in Bitcoin more seriously
### Point 2
- Bitcoin's price (The value of the network itself) began increasing with the square of users ($users^2$)
	- Derived from the observation of the Power Law between price and addresses
	- Confirmation of the theoretical result called the Metcalfe's Law
- Satoshi might didn't think about the Power Laws when he created Bitcoin, but he definitely created ingenious mechanisms that ensured the stability of the Bitcoin's system 
	- Example
		1. Mining Difficulties:
			- Change in difficulty is in proportion to the amount of time over or under two weeks the previous 2016 blocks took to find
			- Imagine a car driving up the mountain, the car would need to break quite often because it cannot just keep accelerating all the time without driving off a ledge when it needs to take curves &rarr; The same of when Bitcoin experiences a rapid growth or decline in hash rate
			- A power lies exactly what you would expect as a result of processes similar to this because iterative self-adjusting feedback loops are the result of Power Laws influencing each other

### Point 3
- The increase in Bitcoin's price after the growth of its users base brought in more resources. Particularly Mining Power and Capabilities
	- People came up with increasingly sophisticated machines as they competed for their share
	- Organized mining operations were established to ensure the highest possible efficiency
### Point 4
- &uarr; Price = &darr;Time needed to mine blocks, but because of the autonomous difficulty adjustment mechanism, the hash rate necessary to mine a block has since been constantly changing in an iterative fashion
- Mining is barely profitable &rarr; The compensation mechanism needs to be proportional to the increase in price to compensate for the linearly proportional increase in hash rate but also for the price itself
-  $$\rightarrow \text{Total compensation} = P^2$$
	- This logical derivation is supported by empirical observation of a Power Law in the form of $$P^2 \propto \text{hashrate}$$
- Adaptive mechanisms like these are necessary to ensure the stability of the system and have to be scaled invariant to keep up with Bitcoin's rapid growth
### Point 5
- Increase in hash rate brought more security to the system &rarr; Attracted more users 
### Point 6
- Bitcoin's Users have been growing with the power of 3 in time ($Time^3$)
- Most models of Bitcoin's Adoption invoke models depicting S-curves, which are typical of the adoption of many Technologies like TVs, Refrigerators, etc. However, Bitcoin does not follow an S curve that is initially exponential. Instead, it follows a Power Law of 3 in Time 
- Many phenomena that have an underlying s-curve mechanism of adoption or spread actually becomes Power Laws if they have some sort of curving mechanism
	- In the case of Bitcoin itself, both difficulty adjustment and the risk involved in any type of investment is that curving mechanism  
- &rarr; We can empirically observe that Bitcoin's growth of adoption is a Power Law of 3 in Time
### Point 7
- This Power Law growth of adoption, together with previously explained Power Laws explains why we can observe Bitcoin's various Power Laws in Time
	1. $\text{Addresses} \propto \text{Time}^3$
	2. $\text{Price} \propto \text{Addresses}^2 = \text{Price} \propto \text{Time}^6$
	3. $\text{Hashrate} \propto \text{Price}^2 = \text{Hashrate} \propto \text{Time}^{12}$
## Conclusion
1. There is no certain point in time when these Power Laws all became established. Because it was a continuous process
2. Bitcoin Power Laws are all tied together &rarr; The change in one creates a change in other in a feedback loop
3. These Power Laws protect Bitcoin from dropping too low by creating a Price Floor that is difficult to get through due to incentive structures created by factors such as the cost of mining
4. Bitcoin's halving motivates people to keep increasing the hash rate on their machines in order to continue achieving the profitability before the halving &rarr; Weak Links are eliminated, and security increases as a result 
5. Bitcoin's finite supply, which is different from scarcity amplifies the effects of Bitcoin's Power Laws
### Outliers & Deviations From The Power Law
1. Outliers are points that deviate a lot from the average Trends. In Bitcoin's case, they are the bubbles &rarr; We are left with the bottoms and they seem to align almost perfectly with a Power Law. All of the other Power Laws are backed up system that create robustness in the system
	- Example:
		- Crashes happen when Bitcoin's Price action has gone up too fast relative to other Power Laws such as the overall hashrate. It is an obvious fact that we cannot scale infrastructure such as mining facilities at the same rate as Bitcoin's Price growth during a bubble. &rarr; The system self-corrects itself
## Why Power Laws?
1. Traditional Linear Graph of time and price is chaotic, unordered.
	1. &rarr; Apply scaling (Log function) to get a better understanding. Changing the POV by a factor of 10
	2. BTC from a fraction of a dollar &rarr; 100k per BTC &arr; Many orders of magnitude
2. BTC is not an exponential phenomena because the log(y) is not a straight line
	1. If you dont find an exponential pattern, with log(y) &rarr; take the log(x) if we get a straight line of log(x)+ log(y) &rarr; Power Laws
3. Power Laws of price in time
### Bitcoin Power Law Misconceptions
1. Humans are Special
	1. Thinking that Humanns dont abby to Math 
	2. Just drawing line and stupid technical analysis
		1. This is not applying finance analysis, this is just Science (MATH)
2. Method of using Log-Log graph to reveal Power Law relationships the nature 
	1. Describing the scalability of a phenomena
	2. Regression is mostly used to derive the POWER that often reveals the consequences and insights about the mechanisims that create the underlying Power Law relationship
		1. Exponent of HIber's Laws is 3/4 reveals the isnights about the economy of scale  and metababolism and the fractal nature of the phisological networks
	3. Efficient Market Analysis
		1. Besides from being just an asset
		2. Bitcoin follows the natural process of Power Laws (EVOLUTION in simple terms) &rarr; Efficient Market Analysis doesnt apply 
		3. Scaling Invariant Property of Bitcoin will always adjust to any atempts to gain the system
			1. The only way to make money out of mining is finding the tiny edge of probability by improving the mining opperation efficiency 
## The Math
1. Method:
	1. OLS regression in Log-Log Space
2. $$\text{Price}= \text{A} * \text{days}^n$$
3. Scale it by a factor of 10 on both sides &rarr; $$log_{10}(Price) = log_{10}(A) + \text{n} * log_{10}(days)$$
4. $$\rightarrow y = c + mx$$ Straight line


For example, in economics, the distribution of wealth often follows a power law, with a small number of people holding a large proportion of the wealth. Similarly, in ecology, the size of animal populations may adhere to power laws, influencing how ecosystems balance and evolve.

  

This property makes them particularly useful in modeling complex systems, as they can capture the underlying patterns that govern the behavior of these systems across different scales