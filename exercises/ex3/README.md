# Exercise 3 - Add custom fields to your schema

For our use case, we are missing information in the content schema. On top of the fields available, we also want to know whether the company has international shareholders.
To configure this, we will add a custom field to the schema that will extract this information automatically.

1. Go back to the schema screen, open the version 1 of your schema and click on "Deactivate" to perform the required changes <br>![](/exercises/ex3/images/ex3_1.png)

2. To configure the custom field, go to the "Entities" tab, click on "Add", and select "Add Field". <br>![](/exercises/ex1/images/ex3_2.png)

3. Fill the dialog with the information as shown in the image, and click on "Add". <br>![](/exercises/ex1/images/ex3_3.png)
   
4. Finally, we want to configure dedicated processing instructions so that the field matches our use case. To do this, navigate to the "Processing Settings" tab and click on "Edit".
<br>Then search for our newly added field and fill the "Processing Instructions" of this field with the following text:
> Return "No" if shareholders are from the UK only.
> Return "Yes (Europe)" if shareholders include any European country outside of UK.
> Return "Yes (Global)" if shareholders include countries outside of Europe.
<br>![](/exercises/ex1/images/ex3_4.png)

