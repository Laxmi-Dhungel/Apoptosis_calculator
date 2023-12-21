Apoptosis Calculator

This code works like a calculator to analyze apoptosis results obtained from flowcytometry. One of the ways to determine apoptosis is by staining with propidium iodide and annexin V. However, no matter which dye is used if the information on total, late and early apoptosis is provided then this code works well to analyze the apoptosis results.
This code generates bar graphs with statistical analysis. However, the file should be in csv format. Below, there is a sample image of flow cytometry results on apoptosis (image generated using biorender).

<img width="360" alt="flowcytometry_biorender_paint" src="https://github.com/Laxmi-Dhungel/Apoptosis_calculator/assets/154451345/4d1f19c5-1a54-4dd7-aa0d-f1bbfe3cdc7c">

In the figure, x-axis represent cells stained by annexin V and y axis represent cells stained by propidium iodide (PI). 
Annexin V can bind to phospholipid exposed outside of cells that are present in apoptotic cells whereas PI binds to nucleic acids of dead cells.
Hence, cells statined by annexin V represent apoptosis whereas cells stained by propidium iodide represent dead cells.
In the figure shown above, quadrant Q1 is annexin V- negative but PI-positive(A-P+). Hence they represent dead cells (necrosis).
Quandrant Q2 is positive for both annexin V and PI (A+P+) hence represent both apoptotic and dead cells (i.e late apoptosis)
Quandrant Q3 is negative for both annexin V and PI (A-P-) hence represent healthy cells.
Quadrant Q4 is positive for annexin V but negative for PI (A+P-) hence represent apoptotic cells only (early apoptosis).

The number in each quadrant represent percentage of cells in those quadrants. Depending on the instrument and software used, these information on percentages of cells in each quadrant can be obtained as a csv file.
Now, this calculator based code comes into play to analyze these results and create graphs from it. This code can be used to analyze data from single or multiple experiments. Hence, saving hours of work.
The csv file should be in the following format. 

<img width="317" alt="csv_file" src="https://github.com/Laxmi-Dhungel/Apoptosis_calculator/assets/154451345/18d7e5c6-ea41-4a65-9f7e-d434bf6336ec">

The first column should consist of sample names. If experiment is repeated multiple times then each experiment results can be added on subsequent rows.
The other columns should have information on total, late and early apoptosis (the order doesn't matter).

The user will be then asked to input file name to be analyzed. Important: if the data has % sign on it then it needs to be removed. The numbers can be multiplied by 100 to get the actual percentage before saving it as a csv file. 
The user will be then asked to input the column header name for treatment groups (which is sample here). Further, they will be asked to input title, x and y label for the image.

<img width="476" alt="file_name" src="https://github.com/Laxmi-Dhungel/Apoptosis_calculator/assets/154451345/b7c61cca-907d-45a7-8f0a-dbf8d63342f2">

Then the user will be provided with options to choose the type of graphs they want. The options include grouped bar plot including all types of apoptois, separate bar plot of each type of apoptosis, separate bar plot with statistics, grouped and separate bar plot or all types of graphs.
For barplot with statistical analysis, it is important that you have atleast 3 replicates. The code doesn't throw an error if you have less replicates, however, statistical analysis is not representative if used to analyze data with less then 3 replicates. 
Here, I typed 5 so that I get all types of graphs.

<img width="456" alt="graphs_options" src="https://github.com/Laxmi-Dhungel/Apoptosis_calculator/assets/154451345/efb5231b-9aa6-4d2a-8ff9-a505bc01a040">

At first, it gives the grouped barplot.

![grouped_bar_chart](https://github.com/Laxmi-Dhungel/Apoptosis_calculator/assets/154451345/ecd78b1b-041a-4166-a2e7-8ab5bf63ccc9)

Then it will ask for column headers that you want to analyze.

<img width="465" alt="column_headers_apoptosis" src="https://github.com/Laxmi-Dhungel/Apoptosis_calculator/assets/154451345/5b982aa0-2c6e-4115-a68f-8438b9e66282">

Then it generates separate graphs for each type of apoptosis with and without statistical analysis. Type of statistical analysis used is provided (Tukey hsd).

![Total_apoptosis](https://github.com/Laxmi-Dhungel/Apoptosis_calculator/assets/154451345/be33a634-d671-42bf-b404-ff3c4f5bcc8b)


![late apoptosis](https://github.com/Laxmi-Dhungel/Apoptosis_calculator/assets/154451345/fa18279d-b958-40be-9ba8-7aadaa84c306)


![Early apoptosis](https://github.com/Laxmi-Dhungel/Apoptosis_calculator/assets/154451345/09d87468-79fb-4d41-bc1c-576c64b3a40b)


![Total_apoptosis_with_stat](https://github.com/Laxmi-Dhungel/Apoptosis_calculator/assets/154451345/fb47f569-2a78-457e-8a76-9479676c171b)


![late_apoptosis_with_stat](https://github.com/Laxmi-Dhungel/Apoptosis_calculator/assets/154451345/cc44fc1f-dc44-4ac3-9341-3a289107131d)


![early_apoptosis_with_stat](https://github.com/Laxmi-Dhungel/Apoptosis_calculator/assets/154451345/3eea361c-7030-4d2b-bae5-9677b364de8f)


However, if the user don't want all of these type of graphs then they always have options to choose the type of graphs they want as said earlier.
At the end, user will be asked if they want to analyze any other set of data so they don't have to run the code again.

Happy graph creating!!
