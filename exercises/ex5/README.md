# Exercise 5 - Create a custom schema

In the following exercise, we want to process Bill of Lading documents. Since this document type is not yet covered by any of the SAP content schemas, we will create our own custom schema.<br>

1. To create the custom schema, go to the schema UI and click on "Create schema"<br>![](/exercises/ex5/images/ex5_1.png)
2. In the dialog, fill out the mandatory information and set the Document Type to "Custom"<br>![](/exercises/ex5/images/ex5_2.png) <br>
3. Once the schema got created, click on it and then click on version 1 to open the schema details.<br>In the details view, go to the "Entities" tab and click on "Add" and "Add Group". In the dialog add name and label as shown below<br>![](/exercises/ex5/images/ex5_3.png)

4. Now click on "Add" again and select "Add Field".<br>Fill out the mandatory information and make sure to set select parent to "Group" and select the previously created group.<br>![](/exercises/ex5/images/ex5_4.png)

5. Now create a table by clicking on "Add" and "Add Table".<br>![](/exercises/ex5/images/ex5_5.png)

6. Following this, add a field to the table by clicking "Add Field" and selecting the table as parent.<br>![](/exercises/ex5/images/ex5_6.png)
7. Repeat this for all the entities shown in the table below, make sure to always select the correct parents (either the group or one of the two tables):
   
| Label               | Name         | Entity Type | Data type |
| ------------------- | ------------ | ----------- | --------- |
| Basic Data          | basic_data       | Group       | String    |
|   Package Count      | package      | Field       | Number    |
|   Sender Name        | sender_name  | Field       | String    |
|   Bill of Lading No  | bol_no       | Field       | String    |
| Order Information   | orders       | Table       | String    |
|   Packages           | packages     | Field       | Number    |
|   Weight             | weight       | Field       | String    |
|   Order No           | order_no     | Field       | String    |
| Carrier Information | carrier_info | Table       | String    |
|   Description        | description  | Field       | String    |
|   Material No        | material  | Field       | String    |

8. Once you maintained all the entities, activate the schema by clicking on "Activate".<br>Then navigate to the Worklist of this schema and upload the document
   [Bill of Lading 1](/exercises/documents/Bill%20of%20Lading%201.pdf)
   
9. Once the document changed its status to "Review Needed", open it and check whether the extracted information matches what you defined in your schema<br>![](/exercises/ex5/images/ex5_7.png)
<br>![](/exercises/ex5/images/ex5_8.png)

---

## Summary

You have learned how to create a custom schema for a new document type.
confidence levels.<br>
Continue to [Exercise 6](../ex6/README.md) to learn how to improve accuracy with Instant Learning.
