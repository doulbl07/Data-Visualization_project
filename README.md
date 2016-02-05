Note    -prosperLoanDataSmallold.csv is for use with index1.html through index5.html
	-prosperLoanDataSmall.csv is for use with index_final.html

Summary 

The visualization shows how credit grade can affect your average annual percentage rate as well as the number of credit lines you have open. A lower credit grade will generally mean a higher APR, but perhaps counterintuitively, the lower average monthly payment one will have.  

Design 

I started with a simple bubble plot showing the different credit grades (x-axis) and how they relate to average APR (y-axis). I was interested to see if credit grades do truely affect APRs as we often hear in the media. I chose a bubble plot because I though it would be interesting to add a third encoding of size to represent the average number of credit lines someone with a particular grade has. Each data point represents a credit grade from AA to HR. I modified the x-axis to show the Avg Monthly Payment, since the individual bubbles already represented the different credit Grades. Having these on the X-axis was redundant. My next version, index3.html, added animation and interaction, but it didn't really add any understanding for the reader. After some valuable feedback, detailed below, my final version is easier to understand and I believe  the reader will see the main patterns I attempted to convey. Specifically the addition of a historic bubble with a color and a label, helps the chart pattern stand out much more than in my earlier versions. 

  

Feedback 

The feedback below is shown in a question - solution format.

Feedback on index3.html from Blake:
	What does APR stand for? - Clarified note to help reader understand APR.

	The main pattern is a higher payment means a higher APR. - This is not a proper understanding of the story I'm trying to tell, I'll reconsider the way I have my axis  
laid out.

	Hard to tell what the size of bubbles stand for - Added note, but a circle with the note may help more. 

	Mouseover animation is a little confusing; the outer circle makes the reader think something is changing. - The only way I found to edit this is to edit dimple.js, which is to far outside the scope of this project. 

	When reviewing the "HR" Credit Grade, the mousover animation doesn't show a y intercept line. - Adjusted min xAxis scale. 

	Y axis does not show enough fidelity, i.e. 0.1 is shown 5 times. - Added yAxis.tickFormat = ',.2f';

	"AA" data should be on the top of the selection grid - Modified y.addOrderRule()

	Double check data between "AA" and "A", animation seems different than the static version in index2.html - index3.html shows data correctly. index2.html shows y axis 	data points incorrectly for "A" and "AA".


Feedback on index4.html from Scott:
	Need to fix the note about "select a dropdown" - Changed wording to match chart. 

	The popup on credit grade buttons shows "Credit Grade: 1.0". This is confusing. - Removed with s.addEventHandler("mouseover", onClick);

	Animation moves too quickly to understand. - Modified frame rate: var frame = 2200; 
	Need to be able to pause the animation from the main chart. -The historic bubbles addition makes the chart easier to read.

	May be useful to add the letter grade to the center of the circle to help understand. - Added .afterDraw fuction to put letter grade in bubbles. 
 

Feedback on index5.html from Andrew:

	The way the bubbles move from one position to the next is confusing, maybe use a different color or shape to help differentiate between data points - Added color to each 	data point to help differentiate.

	The bubble size proportions are off, HR is way smaller than E, but it shouldn't be. - Changed zAxis from Log to Measure, removed Zaxis.overrideMin

	What does each grade mean? - Added in Credit Score, which is a more recognizable term.

Resources 

https://github.com/PMSI-AlignAlytics/dimple/wiki
http://app.raw.densitydesign.org/
http://www.nytimes.com/interactive/2009/11/06/business/economy/unemployment-lines.html?_r=0
http://annapawlicka.com/pretty-charts-with-dimple-js/
http://www.w3schools.com/
http://dimplejs.org/
http://stackoverflow.com/
