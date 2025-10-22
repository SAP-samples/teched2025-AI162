# Exercise 7 - Create a document workflow

Workflow
classify a document
and then extract it differently depending on the document type

for this we want to have three steps
1. Classify the incoming document
2. Have a condition based on the classification result
3. Extract information based on the document type with document type specific schemas

## Step 1 - Create a schema to classify documents

For the classification, we will again create a custom schema with just one field in it, which holds the classification result (in our case the document type).

1. To create the schema, go to the schema UI and create a new schmea with name "classification" and document type "Custom".<br>![](/exercises/ex7/images/ex7_1_1.png)

3. Navigate to the details of the newly created schema by clicking on it and then clicking on version 1.<br>
Within the schema version details, go to the "Entities" tab and create the following entity structure:<br>

| Label               | Name         | Entity Type | Data type |
| ------------------- | ------------ | ----------- | --------- |
| Basic Data          | basic       | Group       | String    |
|   Document Type      | document_type      | Field       | Number    |
  
<br>![](/exercises/ex7/images/ex7_1_3.png)

3. Next, we want to specify what kind of document types shall be classified by this schema. For this, we go to the "Processing Settings" tab in the schema details.<br>
Then click on "Edit" and maintain the following instructions for our "Document Type" field:

> Classify the document. 
> Return "bol" if the document is a bill of lading document.
> Return "cr" if the document is a company registry extract document.

<br>
Finally, click on save and activate to save your changes and activate the schema.

<br>![](/exercises/ex7/images/ex7_1_4.png)

4. When we define the workflow, we want to reference this schema via its version ID. Therefore, store this to have it ready for the next excercise. You can find the ID in the browser URL while you have the schema details open. Check the URL, find the last part starting with "SchemaVersions(" and save the ID that is in the brackets.

<br>![](/exercises/ex7/images/ex7_1_5.png)

5. (Optional) Before creating the workflow, you can test the newly created schema with some of the sample documents to see if it works as intended.

## Step 2 - Create your first workflow

Now that we have all prerequisites ready, we will create and design our workflow.

1. Navigate to the "Workflow" UI via the navigation bar on the left and click on "Create".<br>![](/exercises/ex7/images/ex7_2_1.png)
2. Specify a name and label for the workflow and click on "Create".<br>![](/exercises/ex7/images/ex7_2_2.png)
3. After creation, the new workflow appears in the list of workflows. Click on it to navigate to the workflow.
4. On the workflow page, you can find the design area on the bottom half of the page. The "+" element in the workflow between "Start" and "End" allows you to add additional steps to the workflow. Let us start by adding an "Extraction" step by clicking on "+" and "Extraction".<br>![](/exercises/ex7/images/ex7_2_3.png)
5. Now you can click on the new extraction step to configure the details. An extraction step always references a schema version and processes the incoming document with this schema.<br>
Specify identifier as "classify", this is crucial since we will reference this identifier later in the workflow.<br>
Finally fill the schema version ID, with the value you stored in the previous excercise (step 4.).
<br>![](/exercises/ex7/images/ex7_2_4.png)

6. After this classification, we would to have a condition with different branches depending on the classification result.<br Click on the "+" after the "Extraction" step you added earlier and select "Condition" here.
<br>![](/exercises/ex7/images/ex7_2_5.png)

7. Click on the condition to configure it. Specify the identifier as "document_type". Then click on the edit icon on the first branch to configure the branch.
<br>![](/exercises/ex7/images/ex7_2_6.png)

8. Click on "Edit"
<br>![](/exercises/ex7/images/ex7_2_6.png)

9. In the branch edit dialog. Specify a label and add the following expression and click on "Apply":
> classify.fetchValue("document_type") == "bol"

"classify" here references the previous workflow step. "document_type" references the field from the schema and "bol" the value of this field. Therefore, it is crucial to follow the exact naming in this excercise.
<br>![](/exercises/ex7/images/ex7_2_7.png)


10. To add the second branch for the second document type, click on "Add branch".
<br>![](/exercises/ex7/images/ex7_2_9.png)
      
11. Now follow the steps from 9. just replace the condition with:
> classify.fetchValue("document_type") == "cr"
<br>![](/exercises/ex7/images/ex7_2_8.png)

12. The worflow should show show three branches, two for our document types and one "default" which you can ignore.<br>
For each of the branches that reference one of our document types, add an "Extraction" step.
<br>![](/exercises/ex7/images/ex7_2_10.png)

14. Fill each of these extraction steps with a schema version ID that matches a schema corresponding to the document type.<br>If you followed all excercises you should have one schema created for each document type.<br>
To get the version IDs, use a second browser tab, navigate to the schema UI and copy the version ID from the URL of each schema as done in the previous section of this excercise.
<br>![](/exercises/ex7/images/ex7_2_11.png)
