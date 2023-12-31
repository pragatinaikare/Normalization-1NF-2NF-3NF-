# Normalization 1NF-2NF-3NF

# Problem Statement  

You are a data scientist responsible for structuring a relational database for a local retailer. This retailer has a physical store location as well as an online store. The following is a table containing information about recent transactions.
<br>
TABLE 
TransactionDate	CustomerID	OrderType	CustomerName	CustomerStatus	StoreCredit	Item1	Item2	Item3	Promotion
2023-09-01 10:00:00	1001	Online	Juan Johnson	Gold	$50	Laptop ($1200)	Smartphone($800)		GoldStatusFreeShipping
2023-09-01 10:00:00	1002	In-store	Ahmed Al-Masri	Silver	$30	Gaming Console($500)			
2023-09-05 12:45:00	1003	Online	David Lee	Bronze	$10	Headphones($100)	Coffee Maker($50)	Scooter ($80	BronzeStatusFreeShipping
2023-09-06 9:15:00	1001	In-store	Juan Johnson	Gold	$45	Tablet ($600)			GoldStatus10Off
2023-09-10 16:45:00	1001	Online	Juan Johnson	Gold	$40	RunningShoes($100)	FitnessTracker ($80)		GoldStatusFreeShipping
2023-09-12 11:30:00	1002	In-store	Ahmed Al-Masri	Silver	$25	Home TheaterSystem ($700)			

<br>
Let’s name this table Transactions. It has the composite primary key (TransactionDate+CustomerID), such that both fields are needed to uniquely identify each row. Here are some
additional details about this retailer:<br>
● Each item is characterized by the type of item (e.g. Smartphone) and price (e.g. $800). These represent two different pieces of information about each item.<br>
● Customers making qualifying purchases are eligible for promotions. All promotions are completely based on order type, customer status, and items purchased. For
example, GoldStatusFreeShipping promotion applies to all Gold status customers making online purchases; GoldStatus10Off promotion applies to all in-store purchases by
Gold status customers; BronzeStatusFreeShipping applies to all online purchases made on by Bronze status customers purchasing 3 items.<br>
● Items in each transaction are listed in no particular order.<br>
● A customer’s name and status do not depend on the time of the transaction (i.e. these fields are the same across all transactions for each customer).<br>

<br>
Below is a data dictionary containing a description of each field.<br>
● TransactionDate - Date and time when the transaction took place.<br>
● CustomerID - ID that uniquely identifies the customer.<br>
● OrderType - Indicates whether the order was made in-store or online.<br>
● CustomerName - Name of the customer.<br>
● CustomerStatus - Status of the customer. Can be either Bronze, Silver, or Gold.<br>
● StoreCredit - Store credit available to the customer at the time of the transaction.<br>

<br>
Address the following questions.<br>
1. The Transactions table violates first, second, and third normal form. For each level of normalization, explain why the Transactions table is in violation. Be
specific.<br>
2. Create a collection of tables representing all of the data in Transactions that satisfies first, second, and third normal form and does not contain redundant or
duplicated information across the collection of tables. All data in the Transactions table should be represented somewhere in your collection of tables, but you can
remove any redundant information. Provide complete tables with all of the rows and columns filled in, not just the names of the columns.<br>
3. For each level of normalization, explain the specific steps you have taken to bring your new collection of tables into compliance with first, second, and third normal
form. Be specific. State any assumptions made regarding the data needed to explain why your new collection of tables satisfies third normal form.<br>
4. Identify the primary keys for each table in your new collection of tables. Composite primary keys are acceptable.<br>
5. Identify the types of relationships (one-to-one, one-to-many, many-to-many) among the fields in your tables. Be specific about which field corresponds to the ‘one’
vs. ‘many’. Use the `primary key’ and `foreign key’ terminology when appropriate.<br>
<br>
