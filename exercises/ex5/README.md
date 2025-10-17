# Exercise 5 - TODO

Now that the schema matches our business expectations, we want to start using it productively. During productive use, our business users 
will review and correct documents in the document object page and confirm them to trigger any kind of downstream process.

1. Go to the document worklist for COMPANY_REGISTRY_EXTRACT_STANDARD. If you still have documents in the list from the previous excercise continue to step 2. Otherwise upload a document first.
2. Once the document is in "Review Needed" state, open it, click on "Edit" to start reviewing the document<br>![](/exercises/ex4/images/ex4_1.png)


| Label               | Name         | Entity Type | Data type |
| ------------------- | ------------ | ----------- | --------- |
| Order Information   | orders       | Table       | String    |
|   Packages           | packages     | Field       | Number    |
|   Weight             | weight       | Field       | String    |
|   Order No           | order_no     | Field       | String    |
| Basic Data          | basic        | Group       | String    |
|   Package Count      | package      | Field       | Number    |
|   Sender Name        | sender_name  | Field       | String    |
|   Bill of Lading No  | bol_no       | Field       | String    |
| Carrier Information | carrier_info | Table       | String    |
|   Description        | description  | Field       | String    |
|   Material No        | material  | Field       | String    |
