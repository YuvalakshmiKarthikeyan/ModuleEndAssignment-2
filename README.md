# ModuleEndAssignment-2
# Task 1 – Data Import & Setup
● Load dataset using Pandas - Using pd.read_csv loaded dataset into workspace
● Explore structure: head(), tail(), shape, columns - Used df.head(),tail(),Shape,Columns to find the number of columns and rows
● Convert InvoiceDate to datetime - By Using pd.to_datetime converted the Invoicedate into Datetime format
# Task 2 – Data Cleaning
● Handle missing values (remove null CustomerID) - Using isnull() printed all the missing values in the columns.dropna(subset=['CustomerID']) dropped all the null customerID's.
● Remove duplicates- drop_duplicates() used the remove all the duplicates present in the dataset
● Fix invalid values (negative quantity, invalid price) - Filtered Quantity and Unitprice with > 0 So that it avoids all the negative values,improper valuesetc.After cleaning checked for all missing values.
# Task 3 – Feature Engineering
● Create TotalPrice = Quantity × UnitPrice- Created TotalPrice Column
● Extract time features (Year, Month, Day, Hour) - By using df['InvoiceDate'] Extracted all the day,yeasr,month and hour
● Create categories (Customer Segment, Order Size, Day Type) - By using simple categorical sections created the categories based on TotalPrice, Quantity and InvoiceDate .CustomerSegment['Low' 'High'],OrderSize['Small' 'Large'],Day Type['Weekday' 'Weekend']
# Task 4 – Data Exploration
● Use describe() and dataset overview - Already printed shape,tail,head,column for dataset overview. now printed Describe,datatypes and unique values
● Analyze categories (value_counts(), unique()) - For CustomerSegment,OrderSize,DayType printed valuecounts and unique
● Perform groupby() (country, month, product) - grouped country, month, productby ['Quantity', 'TotalPrice']
# Task 5 – Data Wrangling
● Aggregate data using groupby() -'TotalPrice' Used to display total sales by customer,Total sales by country and 'Quantity' for Total quantity sold by product
● Sort to find the top customers and countries - By above customer_sales sorting in descending found the top customers. By above Country_sales sorting in descending found the top countries.
● Restructure data if needed - Created pivot_best with daytype,month and total price
# Task 6 – Statistical Analysis
● Analyze Quantity, UnitPrice, TotalPrice
● Calculate mean, median, and mode
● Find standard deviation, variance, and percentiles --Analysed mean(),mode(),median(),std(),var() and Quantile for Quantity, UnitPrice, TotalPrice
# Task 7 – Data Visualization (Min 8 Plots)
# Matplotlib:
● Line chart - Plotted Sales over the month 
● Bar chart - plotted Customer segment vs Total price"
● Histogram - Plotted Distribution of Product Prices
● Box plot - plotted weekend and weekday overall price
# Seaborn:
● Count plot - Plotted Count of Total Price by Customer Segment
● Violin plot - Plotted Weekday vs Weekend Sales
● Heatmap - Plotted Sales Correlation Heatmap with Quantity', 'UnitPrice', 'TotalPrice
● Pair plot - Plotted with Corr of Sales
# Task 8 – Business Insights
● Identify:
○ Top country - Country - United Kingdom
○ Best sales month - 11    1156205.61
○ Peak sales time - Hour- 12    1373695.39
● Analyze:
○ Customer behavior - CustomerID
17841.0    7676
14911.0    5670
14096.0    5111
12748.0    4412
14606.0    2677
used Invoiceno to check how many times sales happened from that customer
○ High-value customers
CustomerID
14646.0    280206.02
18102.0    259657.30
17450.0    194390.79
16446.0    168472.50
14911.0    143711.17
12415.0    124914.53
14156.0    117210.08
17511.0     91062.38
16029.0     80850.84
12346.0     77183.60
○ Top products
Description
PAPER CRAFT , LITTLE BIRDIE           80995
MEDIUM CERAMIC TOP STORAGE JAR        77916
WORLD WAR 2 GLIDERS ASSTD DESIGNS     54319
JUMBO BAG RED RETROSPOT               46078
WHITE HANGING HEART T-LIGHT HOLDER    36706
ASSORTED COLOUR BIRD ORNAMENT         35263
PACK OF 72 RETROSPOT CAKE CASES       33670
POPCORN HOLDER                        30919
RABBIT NIGHT LIGHT                    27153
MINI PAINT SET VINTAGE                26076
