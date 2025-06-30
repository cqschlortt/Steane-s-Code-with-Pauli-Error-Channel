# Steane-s-Code-with-Pauli-Error-Channel
The following code takes a boolean (of size n) and a probability p and encodes the boolean into n quantum registers of size seven using Steane's encoding, then runs the registers through a Pauli error channel where error is introduced with probability p, then uses Steane's code for error detection and correction.

Due to simulator restricions, the maximum boolean size that can be tested in this program is a boolean of size 3 (since each logical bit requires seven quantum bits and at least three ancillas are required to measure syndromes).  

Several examples with different sized booleans and different probabilities are demonstrated at the end of the file.  For each of these examples, the distribution of measurements is graphed and the corrected boolean is outputted.  

To use the program, a boolean of size n and a probability can be inputted into the function steane_code_error_correction, which encodes the boolean, runs it through a Pauli error channel which introduces different errors with probability p, measures the syndromes and error corrects is necessary, then measures the final values of the encoded logical bits.  This function outputs the prepared circuit.

The function decode_Steane_circuit takes a prepared circuit (specifically the one prepared in steane_code_error_correction) and the size of the logical boolean (n) and runs a simulator on the prepared circuit 200 times.  Using the measurements prepared in the final step of steane_code_error_correction, the distribution of solutions as well as the most probable solution are found and returned.

For the examples, the distribution returned from decode_Steane_circuit is graphed (to visualise the distribution of possible solutions) and the most probable solution is returned (this solution may not be the original boolean due to the entered probability and the possibility of more than one most probable solution).
