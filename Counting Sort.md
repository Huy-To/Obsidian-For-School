Linear time O(n + k)
1. How it works
	1. We know about the input
	2. Track the occurrences
	3. Index starts at 1
	4. The value im at + the value before me
	5. &rarr; Last position that can occur in the new array (Occurrences -1)
2. Analysis
	1. Go from index 0 & k - 1
		1. init 0$$\sum_{i=0}^{k - 1}1$$
		2. Get occurrences $$\sum_{i=0}^{n - 1}1$$
		3. Aggregate $$\sum_{i=1}^{k - 1}1$$
		4. Placement $$\sum_{i=0}^{n - 1}1$$
		 5. Total ((Top - Bottom) + 1)
			$$\sum_{i=0}^{k - 1}1 + \sum_{i=0}^{n - 1}1+ \sum_{i=1}^{k - 1}1 + \sum_{i=0}^{n - 1}1 = O(n+k)$$ 