# Exercise 6: Improve Extraction Accuracy with Instant Learning

In the previous exercises, some extracted information was incorrect and required manual correction. To avoid repeating these corrections, the system can learn from them using the **Instant Learning** feature.
This exercise explains how to enable Instant Learning and train the system through feedback.

## Step 1 - Activate Instant Learning

1. Open the **Settings** menu and select **Manage Configuration**.
<br>![](/exercises/ex6/images/ex6_1.png)
  
2. In the configuration screen, open the **Learning** section, set **Instant Learning** to **Active**, and click **Save**.
<br>![](/exercises/ex6/images/ex6_2.png)


## Step 2 - Train the System with Corrections

1. Open the **Bill of Lading** worklist from the previous exercise.<br>If documents are still in the **Review Needed** state, use one of them. Otherwise, upload a new document and wait until it reaches the **Review Needed** state.

3. Open a document that is in ***Review Needed*** state
<br>![](/exercises/ex6/images/ex6_2_1.png)

4. Click ***Edit***
<br>![](/exercises/ex6/images/ex6_2_2.png)

5. Review the extraction results and identify incorrect or missing fields.
For example, the **Package Count** may be empty but should be extracted from the **Grand Total** section.
<br>![](/exercises/ex6/images/ex6_2_3.png)

7. Correct the field by clicking on the text in the document preview and then select the ***Package Count*** field and apply it.
<br>![](/exercises/ex6/images/ex6_2_4.png)

8. Next go to the ***Carrier Information*** table and notice that the ***Material*** and ***Decription*** are not extracted as expected.
<br>![](/exercises/ex6/images/ex6_2_6a.png)

9. Correct both fields by selecting ***X-1316*** as ***Material*** and ***Printer Ink Catridge*** as ***Description***.
<br>![](/exercises/ex6/images/ex6_2_5.png)

10. Once you are happy with the results, click on ***Confirm*** in the bottom right corner and confirm the dialog. Now you taught the model your first corrections, which will automatically be applied the next time you process a document with this schema.
<br>![](/exercises/ex6/images/ex6_2_6.png)


## Step 3 - Verify Learning Results

1. Upload another document to see how the learning is automatically being applied. You can either upload the same file again or pick another Bill of Lading document from our samples. E.g. [BoL 2 French](/exercises/documents/Bill%20of%20Lading%202%20FR.pdf)

2. In this example, a French Bill of Lading was uploaded.
   Once processed, the extracted data reflects the applied learning. Previously incorrect fields now appear correctly extracted.
<br>![](/exercises/ex6/images/ex6_3_1.png)
