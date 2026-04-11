---
categories:
  - "[[Classes]]"
course: CS341
source:
teacher:
email:
date:
---
# Op-Amp (Integrated Circuit)
* Op-Amps aren't single components. They are tiny circuits built from basic parts like resistors and transistors
* Op-Amps can perform mathematical operations using voltages
## Definition
- Op-Amps are circuits designed to ==do math== with voltage including adding, subtracting, multiplying, dividing, differentiating, and integrating not just amplifying signals
* `Op`: Operational
* `Amp`: Amplifiers
	* A circuit that takes a small electrical signal and make it bigger
	* Multiply the signal strength
* Example:
	* Mic &rarr; Speaker
	* ![[{5FEA489E-E34C-47CF-9B9F-08087133A7D0}.png]]

## Characteristics
1. Op-Amps don't draw current form the input
2. Op-Amps have infinite input [[Impedance]]
3. Op-Amps have 0 output [[Impedance]]
4. Op-Amps can send or receive current from the output
5. ![[{AC12D2F1-8A98-403C-8138-E872ABBAFF2C}.png]]
## Types
1. Op-Amp Gain
	- The gain represents how much larger the output voltage will be compared to the input voltage difference
		1. Input = $V_1 - V_2$
		2. Output = $V_3$
		3. Gain = $\frac{Output}{Input}$
## Configurations
1. Open-loop configuration
	1. No feedback connecting the output to the input
		- Gain is ==extremely high==
		- Gain = $\frac{Output}{Input} > 100,000$
	2.  Used in Voltage Comparators
2. Closed-loop Configuration
	1. Negative feedback helps control the gain
	2. The output is fed back to one of the inputs through a network of resistors
	3. Used in most Op-Amp circuits
		1. Inverting Amplifier
		2. Non-Inverting Amplifier
		3. Voltage Follower (Buffer)
		4. Summing / Difference Amplifier
		5. Integrators and Differentiators
## Rules to Analyze Op-Amps with Negative Feedback
### Golden Rules
1. No current enters or leaves the Op-Amp Inputs
	- An ideal Op-Amp has infinite input impedance
2. With Negative feedback the voltage of its inputs are equal
	- The Op-Amp continuously adjusts its output to keep the voltage difference between its inputs at or every close to zero
	- $$V_1 = V_2$$
	- 