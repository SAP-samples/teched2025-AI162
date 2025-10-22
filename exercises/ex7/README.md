# Exercise 7 - Create a document workflow

Workflow
classify a document
and then extract it differently depending on the document type

for this we want to have three steps
1. Classify the incoming document
2. Have a condition based on the classification result
3. Extract information based on the document type

## Step 1 - Create a schema to classify documents

For the classification, we will again create a custom schema with just one field in it, which holds the classification result meaning the document type.

1. Go to the schema UI and create a new schmea with name "classification" and document type "Custom".<br>![](/exercises/ex7/images/ex7_1_1.png)
2. Navigate to the details of the newly created schema by clicking on it and hten clicking on version 1.<br>
Within the schema version details, go to the "Entities" tab and create the following entity structure:<br>

| Label               | Name         | Entity Type | Data type |
| ------------------- | ------------ | ----------- | --------- |
| Basic Data          | basic       | Group       | String    |
|   Document Type      | document_type      | Field       | Number    |
  
<br>![](/exercises/ex7/images/ex7_1_2.png)
<br>![](/exercises/ex7/images/ex7_1_3.png)

3. Next, we want to specify what kind of document types shall be classified by this schema. For this, we go to the "Processing Settings" tab in the schema details.<br>
Then click on "Edit" and maintain the following instructions for our "Document Type" field:

> Classify the document. 
> Return "bol" if the document is a bill of lading document.
> Return "cr" if the document is a company registry extract document.
<br>
Finally, click on save and activate to save your changes and activate the schema.
<br>![](/exercises/ex7/images/ex7_1_4.png)


## Step 2 - Create your first workflow
