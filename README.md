# Linear-Programming-Example

Practice problem from ALD2305: Business Math course. A cat food company would like to produce their cat food using chicken and beef exclusively. They would like to keep costs at minimum while maintining nutritional requirements. 

Based on given parametres (per gram cost of chicken/beef, required amounts of nutritional elements, amount of nutritional element available in chicken/beef per gram), we can formulate a Linear Program as follows:

**Decision variables:**

$x_1$ = % of chicken used in a can of cat food<br/>
$x_2$ = % of beef used in a can of cat food

**Objective function:**

min $0.013x_1 + 0.008x_2$<br/> <br/>
*(Considering that per gram chicken costs $0.013 and per gram beef costs $0.008)*<br/>

**Constraints:**

$x_1 + x_2 = 100$<br/> <br/>
*(Chicken and beef would consist of 100% content in a can of catfood)*<br/> <br/>
$0.1x_1 + 0.2x_2 >= 8$ <br/> <br/> 
*(A can of catfood should contain at least 8 grams of Protein. Per gram chicken contains 0.1 grams and per gram beef contains 0.2 grams of Protein.)*<br/> <br/>
$0.08x_1 + 0.1x_2 >= 6$<br/> <br/>
*(A can of catfood should contain at least 6 grams of Fat. Per gram chicken contains 0.08 grams and per gram beef contains 0.1 grams of Fat.)*<br/> <br/>
$0.001x_1 + 0.005x_2 <= 2$<br/> <br/>
*(A can of catfood should contain at max 2 grams of Fibre. Per gram chicken contains 0.001 grams and per gram beef contains 0.005 grams of Fibre.)*<br/> <br/>
$0.002x_1 + 0.005x_2 <= 0.4$<br/> <br/>
*(A can of catfood should contain at max 0.4 grams of Salt. Per gram chicken contains 0.002 grams and per gram beef contains 0.005 grams of Salt.)*<br/> <br/>

Problem is solved using Python's PuLP package. Optimal solution dictates each can of cat food should contain 33.33% of chicken and 66.67% of beef, with the minimum possible cost per can of catfood found at $0.96 while meeting all nutritional requirements. 
