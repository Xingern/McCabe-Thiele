# McCabe-Thiele
Code showing how to plot McCabe-Thiele diagrams and also calculating the steps. This code is based on laboratory experiments in TKP4105 - Separation Technology which measures top composition and draws a McCabe-Thiele diagram using Python. 

Explanation of code:
1. Initating the constants used for this experiment. This includes densities and such. 
2. get_VLEregresion() takes a CSV-file of equilibrium-data and returns the 9th order regression. 
3. calc_y() simply calculates y given x, while calc_x() does the reverse. The problem her is to solve the 9th order polynomial, which I in this case just used and iterative method. In retrospect, other methods like using Scipy may be more efficient. 
4. The function vol_to_molerac() uses the given constants to convert volume percent to molefraction.
5. draw_mccabe() is a big function and may seem complicated. What happens is i drew the McCabe-Thiele by hand and systematically wrote down each operation i did and generalized it in code. 
6. The rest is data from the experiments
