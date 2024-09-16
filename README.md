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
  * to display the first five rows I used the .head() code and for the last 5 rows I used .tail() code
  ![image](https://github.com/user-attachments/assets/68274d32-5831-4198-863a-d7137e450e0a)
  # The output:
  ![image](https://github.com/user-attachments/assets/651d7b35-ec16-4632-8ba4-e4d38f414676)


  # Problem 2:
  ## Tasks:
  a. Display the first five rows with odd-numbered columns
  b. Display the row that constains the 'Model' of 'Mazda RX4'
  c. How many cylinders does the car model 'Camaro Z28' have?
  d. Determine how many cylinders and what gear type tha car models 'Mazda RX4 Wag', 'Ford Pantera L', and 'Honda Civic' have
  ## Approach
  * for part a I used iloc to slice the first five rows and to increment the the columns by 2 so only odd columns are printed.
    # The code to display the first 5 rows and odd-number columns
    ![image](https://github.com/user-attachments/assets/b199108f-3e55-4d2b-907c-5c0124700246)
    # The output:
    ![image](https://github.com/user-attachments/assets/632c656e-9868-4d8b-a3ab-a4e997328928)
  * to locate 'Mazda RX4' I used .loc which specifically contains the 'Model' to filter the DataFrame
     # The Code:
    ![image](https://github.com/user-attachments/assets/6ddc92d8-6764-4438-9d85-f48ac5b672a1)
    # The output:
    ![image](https://github.com/user-attachments/assets/2e992e28-b6c4-485a-b7c2-91dffd83c476)
  * To find the cylinder number of the Camaro I used .loc() to and input the row of the Camaro and input the 'cyl' to filter the column and get the value for the Camaro.
   # The code:
  ![image](https://github.com/user-attachments/assets/12318d20-0be7-4904-b16d-8dfadde57f85)
  # The output:
  ![image](https://github.com/user-attachments/assets/cd0ee9e6-5b29-44d4-a41c-6fd283df95d1)
  * To find the following car models I used .loc to locate the rows where the cars are located and use the name of the columns to filter the output.
  # The code:
  ![image](https://github.com/user-attachments/assets/a37c8fdc-9d85-4fc3-8a82-1057e536d990)
  # The output:
  ![image](https://github.com/user-attachments/assets/07f21486-6cee-441d-83f6-3f349ad33dcb)


