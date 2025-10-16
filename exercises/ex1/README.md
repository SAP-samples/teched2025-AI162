# Exercise 1 - Activate a content schema and upload your first document

In this exercise, we will activate a content schema and upload our first document for processing.
A schema describes the structure of the information that we want to extract from a document and contains processing instructions as well as visualization-related configurations.
Document processing is always based on schema, as part of the application, we deliver a number of content schemas, as a way to quickly start using the application for processing of various common document types.

## Exercise 1.1 Activate a content schema 

After completing these steps you will have activated your first schema.

1. In the home screen of SAP Document AI, click on "My Schemas". <br>![](/exercises/ex1/images/ex1_1.png)

2. In the Schema overview page, search for "COMPANY_REGISTRY_EXTRACT_STANDARD". Select the checkbox and click on "Enable". <br>![](/exercises/ex1/images/ex1_2.png)

3. In the dialog, select version "1", and mark the checkbox "Activate" and click "Create". This will create a copy of the content and activate it so that you can use the schema afterwards for document processing. <br>![](/exercises/ex1/images/ex1_3.png)


## Exercise 1.2 Upload your first document

After completing these steps you will have uploaded and reviewed your first document.

1. Once you created your own schema in step 3. of the previous exercise, a new menu icon will appear in the navigation pane on the right. Click on it and select "Version 1". <br>![](/exercises/ex1/images/ex1_4.png)


2. Now you reached the worklist of your "COMPANY_REGISTRY_EXTRACT_STANDARD" schema. This list will show all documents that got processed with this schema.<br>
Since we haven't uploaded a document yet, the list is still empty. To start the processing, upload a document by clicking "Upload" or dragging and dropping a file into the worklist. Pick the file "Company Registry Extract House of Companies UK.pdf" and upload it <br>![](/exercises/ex1/images/ex1_5.png)

3. After the upload a new entry should appear in the worklist. Wait a few seconds until the status changes to "Review Needed"
<br>![](/exercises/ex1/images/ex1_6.png)

4. Click on the document in the worklist to review the extracted information
<br>![](/exercises/ex1/images/ex1_7.png)

## Summary

You've now activated a first schema and processed a document with it. If you want to play around more, you can activate some of the other content schemas and upload documents of different types.

If you want to continue, learn how to configure the schema further in exercise 2 - [Exercise 2 - Schema configuration](../ex2/README.md)

