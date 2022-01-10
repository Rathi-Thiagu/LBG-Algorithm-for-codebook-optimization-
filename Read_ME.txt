Algorithm Description:
	1. Initialized the code book
	2. Training vector generation by sliding the 2x2 convolution window over the input image (16 training
	vectors where obtained)
	3. Computing distance between each point and the value in the code vectors to determine the error. Code
	value for which has minimum error is chosen.
	Error = sqrt(summation(x-y) ^2),
	 where x is the training vector value and y is the code vector value
	4. Calculate the distortion by taking the average of the minimum distance of training vectors obtained in
	the previous step.
	5. Updating the codebook
	 If [Distortion (0) – Distortion (1)]/ Distortion (0) <= Threshold
	Stop:
	Else:
	Update the codebook by taking the average of the training vector having the same code
	vector mapping. Repeat the steps till the condition is met.
	Threshold value = 0.001 is considered.