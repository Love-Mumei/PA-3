# ECE2112-PA-3
* Kyle Nathaniel Dimalanta
* September 16,2024
  # Libraries Used:
  * Pandas
  # Problem 1:
  ## Tasks:
  a. Load the .csv file
  b. Display the first and last five rows of the table of data
  # The code to have an output of the first and last five rows of the table of data
  ## Approach
  * to load a .csv file can be loaded by using the .read syntax
  # Code to load the csv file
```
import pandas as pd
data = pd.read_csv('cars.csv')
data
```
  * to display the first five rows I used the .head() code and for the last 5 rows I used .tail() code
  # Code to output the rows
``` python
print ("The first 5 rows of data are: \n", data.head()) #print the first five rows of the table
print ("The last 5 rows of data are: \n", data.tail()) #print the last five rows of the table
```
# The output
```
The first 5 rows of data are: 
                Model   mpg  cyl   disp   hp  drat     wt   qsec  vs  am  gear  \
0          Mazda RX4  21.0    6  160.0  110  3.90  2.620  16.46   0   1     4   
1      Mazda RX4 Wag  21.0    6  160.0  110  3.90  2.875  17.02   0   1     4   
2         Datsun 710  22.8    4  108.0   93  3.85  2.320  18.61   1   1     4   
3     Hornet 4 Drive  21.4    6  258.0  110  3.08  3.215  19.44   1   0     3   
4  Hornet Sportabout  18.7    8  360.0  175  3.15  3.440  17.02   0   0     3   

   carb  
0     4  
1     4  
2     1  
3     1  
4     2  
The last 5 rows of data are: 
              Model   mpg  cyl   disp   hp  drat     wt  qsec  vs  am  gear  \
27    Lotus Europa  30.4    4   95.1  113  3.77  1.513  16.9   1   1     5   
28  Ford Pantera L  15.8    8  351.0  264  4.22  3.170  14.5   0   1     5   
29    Ferrari Dino  19.7    6  145.0  175  3.62  2.770  15.5   0   1     5   
30   Maserati Bora  15.0    8  301.0  335  3.54  3.570  14.6   0   1     5   
31      Volvo 142E  21.4    4  121.0  109  4.11  2.780  18.6   1   1     4   

    carb  
27     2  
28     4  
29     6  
30     8  
31     2  
```
  # Problem 2:
  ## Tasks:
  a. Display the first five rows with odd-numbered columns
  b. Display the row that constains the 'Model' of 'Mazda RX4'
  c. How many cylinders does the car model 'Camaro Z28' have?
  d. Determine how many cylinders and what gear type tha car models 'Mazda RX4 Wag', 'Ford Pantera L', and 'Honda Civic' have
  ## Approach
  * for part a, I used iloc to slice the first five rows and to increment the the columns by 2 so only odd columns are printed. The code to help the explanation.
```
data.iloc[:5, ::2]
```
  * to locate 'Mazda RX4' I used .loc which specifically contains the 'Model' to filter the DataFrame. The code to help the explanation.
```
data.loc[data['Model'] == 'Mazda RX4'
```  
  * To find the cylinder number of the Camaro, I used .loc() to input the row of the Camaro and input the 'cyl' to filter the column and get the value for the Camaro. The code to help the explanation.
```
data.loc[[23], ['cyl']
```  
  * To find the following car models I used .loc to locate the rows where the cars are located and use the name of the columns to filter the output. The code to help the explanation.
```
data.loc[[1, 28, 18], ['Model', 'cyl', 'gear']
```
  # The code
  ```
print("The odd numbered columns are: \n", data.iloc[:5, ::2]) #using iloc to locate the position of the columns.
print("\n The Data for Mazada RX4 is: \n", data.loc[data['Model'] == 'Mazda RX4']) #using .loc to find the word "Mazda RX4" in the Model columns
print("\n The number of cylinders in Camaro is: \n", data.loc[[23], ['cyl']]) ##using the .loc to find the data needed for row 23 and look for the 'model' and 'cyl' for specification)
print("\n The data for the following cars are: \n", data.loc[[1, 28, 18], ['Model', 'cyl', 'gear']]) #using .loc rows: 1, 18 and 28 will look for the data that is contained in 'Model', 'cyl', and 'gear
  ```
  # The output:
  ```
The odd numbered columns are: 
                Model  cyl   hp     wt  vs  gear
0          Mazda RX4    6  110  2.620   0     4
1      Mazda RX4 Wag    6  110  2.875   0     4
2         Datsun 710    4   93  2.320   1     4
3     Hornet 4 Drive    6  110  3.215   1     3
4  Hornet Sportabout    8  175  3.440   0     3

 The Data for Mazada RX4 is: 
        Model   mpg  cyl   disp   hp  drat    wt   qsec  vs  am  gear  carb
0  Mazda RX4  21.0    6  160.0  110   3.9  2.62  16.46   0   1     4     4

 The number of cylinders in Camaro is: 
     cyl
23    8

 The data for the following cars are: 
              Model  cyl  gear
1    Mazda RX4 Wag    6     4
28  Ford Pantera L    8     5
18     Honda Civic    4     4
  ```



