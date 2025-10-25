# Exercise 3: Add Custom Fields to the Schema

The current content schema lacks a field indicating whether a company has international shareholders.
In this exercise, a custom field will be added to extract that information automatically.

---

1. Open the schema screen, select **Version 1**, and click **Deactivate** to allow editing. <br>![](/exercises/ex3/images/ex3_1.png)

2. To configure the custom field, go to the ***Entities*** tab, click on ***Add***, and select ***Add Field***. <br>![](/exercises/ex3/images/ex3_2.png)

3. Fill the dialog with the information as shown in the image, and click on ***Add***. <br>![](/exercises/ex3/images/ex3_3.png)
   
4. Finally, we want to configure dedicated processing instructions so that the field matches our use case. To do this, navigate to the ***Processing Settings*** tab and click on ***Edit***.
<br>Then search for our newly added field and fill the ***Processing Instructions*** of this field with the following text:

> Return ***No*** if shareholders are from the UK only.<br>
> Return ***Yes (Europe)*** if shareholders include any European country outside of UK.<br>
> Return ***Yes (Global)*** if shareholders include countries outside of Europe.

<br>![](/exercises/ex3/images/ex3_4.png)

5. Once you are done, activate the schema again, navigate back to the Worklist and upload the document again. In the extraction results, search for the newly added field and validate if the value matches your expectation.
<br>![](/exercises/ex3/images/ex3_5.png)


## Summary

You have added a custom field to the schema and configured it with tailored processing instructions.
You can either continue adding more fields or continue to - [Exercise 4](../ex4/README.md) to learn how to review documents and automate the review.
