# ECE2112-PA-3
* Kyle Nathaniel Dimalanta
* September 16,2024
  # Libraries Used:
  * Pandas
  # Problem 1:
  ## Tasks:
  a. Load the .csv file
  b. Display the first and last five rows of the table of data
  ## Approach
  * to load a .csv file can be loaded by using the .read syntax
  * to display the first five rows I used the .head() code and for the last 5 rows I used .tail() code

  # Problem 2:
  ## Tasks:
  a. Display the first five rows with odd-numbered columns
  b. Display the row that constains the 'Model' of 'Mazda RX4'
  c. How many cylinders does the car model 'Camaro Z28' have?
  d. Determine how many cylinders and what gear type tha car models 'Mazda RX4 Wag', 'Ford Pantera L', and 'Honda Civic' have
  ## Approach
  * for part a I used iloc to slice the first five rows and to increment the the columns by 2 so only odd columns are printed.
  * to locate 'Mazda RX4' I used .loc which specifically contains the 'Model' to filter the DataFrame
  * To find the cylinder number of the Camaro I used .loc() to and input the row of the Camaro and input the 'cul' to filter the column and get the value for the Camaro.
  * To find the following car models I used .loc to locate the rows where the cars are located and use the name of the columns to filter the output.
