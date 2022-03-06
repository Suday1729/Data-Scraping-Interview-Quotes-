# Data-Scraping-Interview-Quotes-
Scraping of data from (Interview Quotes) website (Contains jupyter file, dataset)
Procedure
•	Imported the necessary libraries
•	Inspected the webpage to locate all the required details to be extracted from the webpage
•	Once each detail was located using “inspect”, it was passed on to corresponding variables using list comprehension or “for loop”
•	Reusable function was defined (interview(soup)) 
•	Using the interview(soup) function, dataframe (intw) was defined which contained the required details
•	”page” variable was defined to extract different pages of the website using .format{}
•	tqdm was imported for checking the status of progress
•	time was imported to assign adequate sleep time for loading each page which enables complete data extraction from each page
•	sleep time of 5 sec was assigned
•	“data” variable was defined to contain the concatenated tables from each of the 5 pages 
•	Shape of the “data” variable was checked to see whether all the details from each page was extracted. The “data” variable contained 25 rows which was the same in the website (each page had 5 data points)
•	“data” dataframe was converted to .csv file as “Interview Quotes.csv” 


Challenges
•	The pattern for Employee, Job position and Company was different for the first employee in the first page ('Aviv Ben-Yosef')
•	The exception case did not have the company detail
•	Had to use “re.split(',| at ',i.text.strip())” to split multiple characters namely “,” and “at” to extract Job position and company
•	Since the exception case did not have company name, list comprehension was throwing an error of “index out of range”. Solved this issue using if condition for length of each element inside for loop. Also assigned “NIL” for whichever case not having company name

