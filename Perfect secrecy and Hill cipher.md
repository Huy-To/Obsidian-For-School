# 1. Explain Perfect Secrecy (1 point) and show an example of encryption scheme that achieves Perfect Secrecy (2 point).
 - An encryption scheme is perfectly secure when
	 - Observing the ciphertext does not change the probability of any plaintext
	 - The ciphertext and plaintext are statistically independent
	 - The number of message bits that one can encrypt cannot exceed the number of key bits. 
- Example:
	- One Time Pad $$P = C = K = (Z_2)^n \quad | \quad x = (x_1,...,x_n) \quad | \quad  y= (y_1,...,y_n) \quad | \quad K = (K_1,...,K_n)$$
		- Encryption $$e_k(x) = (x_1 + K_1,..., x_n + K_n) \text{ mod } 2$$
		- Decryption $$d_k(y) = (y_1 + K_1,..., y_n + K_n) \text{ mod } 2$$
		- Bayes' theorem $$Pr[x|y] = \frac{Pr[x]Pr[y|x]}{Pr[y]}$$
		- Joint and Conditional Probability $$Pr[x,y]=Pr[x|y]Pr[y] = Pr[y|x]Pr[x]$$
		- Probability is the same for every plaintext
# 2. The plaintext is “theplaintext” and the ciphertext is “XPUVLACBRAHN”. We are assuming that the plaintext was enciphered using a 2X2 Hill cipher. Calculate the key K and inverse key $K^{-1}$. (2 point) Show the calculation process (2 point)
1. 2X2
	- Plaintext: [th, ep, la, in, te, xt]
	- Cipher: [XP, UV, LA, CB, RA, HN]
2. Using the alphabet to convert these letters into numbers to create 2x2 matrixes $$\text{P} = \begin{bmatrix} 19 & 4 \\ 7 & 5 \end{bmatrix} = \begin{bmatrix} t & e \\ h & p \end{bmatrix}  \quad | \quad C = \begin{bmatrix} 23 & 20 \\ 15 & 21 \end{bmatrix} = \begin{bmatrix} X & U \\ P & V \end{bmatrix}$$

3. Compute $P^{-1}$
	1. $$det(P) = 19* 15 - 4*7 = 257 \text{ mod } 26 = 23$$
	2. $$23^{-1} \text{ mod } 26 =  17$$
	3. $$P^{-1} = 17 \begin{bmatrix}15 & 4 \\ -7 & 19 \end{bmatrix} \text{ mod } 26 = \begin{bmatrix} 21 & 10 \\ 11 & 11 \end{bmatrix}$$
4. Hill Cipher Rule: $$C = KP \text{ mod } 26 \quad | \quad K = CP^{-1} \text{ mod } 26$$
	1. $$K = (\begin{bmatrix} 23 & 20 \\ 15 & 21 \end{bmatrix}\begin{bmatrix} 21 & 10 \\ 11 & 11 \end{bmatrix}) \text{ mod } 26 = \begin{bmatrix} 1 & 8 \\ 0 & 17\end{bmatrix}$$
	2. $$K^{-1} = det(K^{-1}) * K^{T} = 23* \begin{bmatrix}17 & -8 \\ 0& 1\end{bmatrix} = \begin{bmatrix}1 & 24 \\ 0 & 23 \end{bmatrix}$$
# 3. What is the name of the above attack of question 2. (1 point) List at least two other types of attacks introduced in the class. 
1. The name of the above attack in question 2 is Known-Plaintext Attack
2. Other attacks
	1. Chosen Plaintext
	2. Chosen Ciphertext
	3. CHosen text
	4. CiphertextOnly