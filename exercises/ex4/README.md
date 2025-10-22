# Exercise 4 - Review Documents and Automate the Review

With the schema aligned to business requirements, it can now be used in production. During productive use, business users review extracted data, correct errors, and confirm documents to trigger downstream processes.

---

1. Open the **COMPANY_REGISTRY_EXTRACT_STANDARD** worklist.
   If no documents are available, upload one before proceeding.
2. Once the document is in ***Review Needed*** state, open it, click on ***Edit*** to start reviewing the document<br>![](/exercises/ex4/images/ex4_1.png)
3. Review the extracted fields and identify any incorrect values.
   For example, the incorporation date may have been extracted incorrectly.
   To correct a value, either type it manually or click on the correct value in the document preview, select the corresponding field, and apply it.
<br>![](/exercises/ex4/images/ex4_2.png)
4. Once the document got reviewed and corrected, you can confirm it by clicking on the ***Confirm*** button. Confirming will mark the document as ready for downstream processes and will block furter editing.
<br>![](/exercises/ex4/images/ex4_3.png)

6. After consistent use, once extraction results are reliable, manual review can be reduced. This is done by configuring automatic confirmation based on AI confidence scores.
   Open the schema configuration for **COMPANY_REGISTRY_EXTRACT_STANDARD**.

7. Go to the ***Automation*** tab, activate ***auto-confirmation*** and select ***65%*** as confidence threshold. Before saving and activating the schema again.<br>
You can also play around with the confidence values or define confidence values only for some of the schema fields.<br>
![](/exercises/ex4/images/ex4_4.png)

8. Now back to the document worklist and upload the document again. You will see that the document does not go to ***Review Needed*** anymore but instead directly goes to ***Confirmed*** since all fields are above the confidence threshold.
<br>![](/exercises/ex4/images/ex4_5.png)

---

## Summary

You have learned how to review documents, correct extraction errors, and configure automated confirmation based on AI confidence levels.
Continue to - [Exercise 5](../ex5/README.md)
