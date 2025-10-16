# Exercise 2 - Exercise 2 Description

In this exercise, we will create...

## Exercise 2.1 Configure Workslist and Object Page Header Entities

Schemas allow configuring which information shall be shown in the worklist of documents and in the object page header of each document.<br>
This can be used to customize the UI to the requirements of your business, e.g. when processing invoices, it might help to see the supplier name and total amount on the worklist to find the right invoice more quickly.
<br>
<br>
We will now configure this for our Company Registry Extract schema.

1. Navigate back to the schema UI by clicking on the schema icon in the navigation bar. <br>![](/exercises/ex2/images/ex2_1.png)

2. Select version 1 to open the details of the schema. <br>![](/exercises/ex2/images/ex2_2.png)

3. On the schema configuration screen, navigate to the second tab "Display Entities". <br>![](/exercises/ex2/images/ex2_3.png)

4. Configure which information to show on the worklist by clicking on "Add to Worksist" and select some of the schema fields in the dialog. Once you are done, close the dialog by clicking "Add". <br>![](/exercises/ex2/images/ex2_4.png)

5. Configure which information to show on the object page by clicking on "Add to Object Header" and select some of the schema fields in the dialog. Ideally select different fields to step 4 so that you can see the impact more clearly. Once you are done, close the dialog by clicking "Add". <br>![](/exercises/ex2/images/ex2_5.png)

6. Confirm the changes by clicking "Save". <br>![](/exercises/ex2/images/ex2_6.png)

7. Now see how this impacted the visualization of the documents by navigating back to the worklist.<br>Here you should see the fields that you selected for the worklist. In case they are not shown, try refreshing the browser window. <br>![](/exercises/ex2/images/ex2_7.png)

8. To see the object header fields you configured, click on the document and check the header section of the screen. <br>![](/exercises/ex2/images/ex2_8.png)



## Exercise 2.2 Sub Exercise 2 Description

After completing these steps you will have...

1.	Enter this code.
```abap
DATA(lt_params) = request->get_form_fields(  ).
READ TABLE lt_params REFERENCE INTO DATA(lr_params) WITH KEY name = 'cmd'.
  IF sy-subrc = 0.
    response->set_status( i_code = 200
                     i_reason = 'Everything is fine').
    RETURN.
  ENDIF.

```

2.	Click here.
<br>![](/exercises/ex2/images/02_02_0010.png)

## Summary

You've now ...

Continue to - [Exercise 3 - Excercise 3 ](../ex3/README.md)
