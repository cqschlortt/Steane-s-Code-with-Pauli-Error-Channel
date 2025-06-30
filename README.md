# Steane-s-Code-with-Pauli-Error-Channel
The following code takes a boolean (of size n) and a probability p and encodes the boolean into n quantum registers of size seven using Steane's encoding, then runs the registers through a Pauli error channel where error is introduced with probability p, then uses Steane's code for error detection and correction.

Due to simulator restricions, the maximum boolean size that can be tested in this program is a boolean of size 3 (since each logical bit requires seven quantum bits and at least three ancillas are required to measure syndromes).  

Several examples with different sized booleans and different probabilities are demonstrated at the end of the file.  For each of these examples, the distribution of measurements is graphed, and we can see that lower probabilities lead to more uniform distributions.
