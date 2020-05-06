# CSC260
CSC260 Object-Oriented Design
CSC 260 Object-Oriented Design
March 2020

#Project Proposal – Automate calculating Healthcare Second Lowest Cost Plan
#Problem Statement
Healthcare plan professionals spend too much time determining the tax credit for qualifying individuals and families receive on the marketplace.  The method used for a health plan in a particular rate area is called a Second Lowest Cost Plan and serves as the benchmark health plan for a particular area.
For example, if a rate area had health plans with rates of [197.3, 201.1, 305.4, 306.7], the SLCP for that rate area would be 201.1 since it's the second lowest rate in that rate area.
A plan shall have a metal level which can be Bronze, Silver, Gold, Platinum, or Catastrophic. The metal level is indicative of the level of coverage the plan provides. 
A plan shall have a rate which is the amount that a consumer pays as a monthly premium in dollars and a plan has a rate area which is a geographic region in a state that determines the plan's rate.  For example: WA 1, SD 2
Historically, the process for calculating the SLCP involves importing comma separated value files into spreadsheet software, typically Excel, to determine the SLCP which is the second lowest rate for a plan in the rate area.
CSV files provided to ftp drop folder locations that change frequently.
•	plans.csv - All health plans on the marketplace
•	rates.csv - map of ZIP code to county/counties and rate area(s)
•	slcp.csv – zip code list used to determine the Second Lowest Cost Plan
Proposal Solution
To create object-oriented real-time Second Lowest Cost Plan site monitor that updates the SLCP values when new file changes are detected.  The Healthcare plan professionals will be able to expedite tax credit determinations for individuals and families. 

Expected output
The order of the rows in slcp.csv must stay the same as how they appeared in the original slcsp.csv. The first row shall be the column headers: [zipcode],[rate] The remaining lines shall output unquoted values with two digits after the decimal place of the rates, for example: 64148,245.20.

Additional information
It may not be possible to determine a SLCP for every ZIP code given; for example, if there is only one silver plan available, then there is no second lowest cost plan. For cases where a definitive answer cannot be found those cells shall be left blank in the output CSV (no quotes or zeroes or other text). For example, 40813,. A ZIP code can potentially be in more than one county. If the county cannot be determined definitively by the ZIP code, it may still be possible to determine the rate area for that ZIP code. A ZIP code can also be in more than one rate area. In that case, the answer is ambiguous and shall be left blank.
