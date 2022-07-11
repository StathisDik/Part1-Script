#Instructions to run Queries

Set up BigQuery 
We are mainly using the Standard SQL of BigQuery. Once you have logged in to your google-based
account, you can access the BigQuery platform following the Link to BQ.

1. Create a project named efood2022
Click on “Select a project” and Create New.

2. Add a dataset named main_assessment
Click on the 3 bullets next to efood2022
name and select create dataset.
Window like screenshot appears where you
set the dataset name and location in Europe
(eu) and press on the blue button
Add a table named orders

3. Add a table named orders
Click on the 3 bullets next to main_assessment
and select Create table.
WIndow appears like in the screenshot where
you choose to upload the orders.csv you
downloaded before.
Choose to edit as text and paste the schema included in the following gray pane, as shown in
the screenshot.
order_id:INTEGER,
user_id:INTEGER,
order_timestamp:TIMESTAMP,
city:STRING,
cuisine:STRING,
paid_cash:BOOLEAN,
amount:FLOAT
When clicking on Edit as text again you see the table schema as in screenshot
Finally, in Advanced options we set Header Rows to Skip to 1, as CSV has a header that doesn’t
follow table’s schema and that couldn’t allow its creation

4. Once setup finished you are able to query on the table created ( ie. using the following query or
pressing query button from the UI)
SELECT *
FROM `efood2022.main_assessment.orders`
