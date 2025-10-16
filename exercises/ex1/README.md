# Exercise 1 - Activate a content schema and upload your first document

In this exercise, we will activate a content schema and upload our first document for processing.
A schema describes the structure of the information that we want to extract from a document and contains processing instructions as well as visualization-related configurations.
Document processing is always based on schema, as part of the application, we deliver a number of content schemas, as a way to quickly start using the application for processing of various common document types.

## Exercise 1.1 Activate a content schema 

After completing these steps you will have created...

1. Click here. <br>![](/exercises/ex1/images/ex1_1.png)

2. Click here. <br>![](/exercises/ex1/images/ex1_2.png)

3. Click here. <br>![](/exercises/ex1/images/ex1_3.png)

4. Click here. <br>![](/exercises/ex1/images/ex1_4.png)

5. Click here. <br>![](/exercises/ex1/images/ex1_5.png)



## Exercise 1.2 Sub Exercise 2 Description

After completing these steps you will have...

1.	Enter this code.
```abap
DATA(lt_params) = request->get_form_fields(  ).
READ TABLE lt_params REFERENCE INTO DATA(lr_params) WITH KEY name = 'cmd'.
  IF sy-subrc <> 0.
    response->set_status( i_code = 400
                     i_reason = 'Bad request').
    RETURN.
  ENDIF.

```

2.	Click here.
<br>![](/exercises/ex1/images/01_02_0010.png)


## Summary

You've now ...

Continue to - [Exercise 2 - Exercise 2 Description](../ex2/README.md)

