# Exercise 4 - Review documents and automate the review

Now that the schema matches our business expectations, we want to start using it productively. During productive use, our business users 
will review and correct documents in the document object page and confirm them to trigger any kind of downstream process.

1. Go to the document worklist for COMPANY_REGISTRY_EXTRACT_STANDARD. If you still have documents in the list from the previous excercise continue to step 2. Otherwise upload a document first.
2. Once the document is in "Review Needed" state, open it, click on "Edit" to start reviewing the document<br>![](/exercises/ex4/images/ex4_1.png)
3. Now go through the document and see whether you find any errors that require correction. E.g. in the example below, the incorporation date was incorrectly extracted and requires correction.<br>
To correct a value, you can either type in the correct value or draw a box around the correct value in the document and then select the field that should be filled with this value in the dialog and apply it.<br>
<br>![](/exercises/ex4/images/ex4_2.png)
4. Once the document got reviewed and corrected, you can confirm it by clicking on the "Confirm" button. Confirming will mark the document as ready for downstream processes and will block furter editing.
<br>![](/exercises/ex4/images/ex4_3.png)

6. After a while, you have enonugh trust in the processing, that you do not want to review every document manually. Instead, you want to configure an automation based on the confidence value of the AI.<br>
This is possible in the schema. Go back to the schema screen and edit the COMPANY_REGISTRY_EXTRACT_STANDARD schema again.

7. Go to the "Automation" tab, activate "auto-confirmation" and select "65%" as confidence threshold. Before saving and activating the schema again.<br>
You can also play around with the confidence values or define confidence values only for some of the schema fields.<br>
![](/exercises/ex4/images/ex4_4.png)

8. Now back to the document worklist and upload the document again. You will see that the document does not go to "Review Needed" anymore but instead directly goes to "Confirmed" since all fields are above the confidence threshold.
<br>![](/exercises/ex4/images/ex4_5.png)


## Summary

You've now learned how to automatically confirm documents based on their confidence.<br>

Continue to - [Exercise 5](../ex5/README.md)
