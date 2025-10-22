<img width="578" height="149" alt="image" src="https://github.com/user-attachments/assets/3b416456-f6b5-48e8-b905-2e166c84ec28" /># Exercise 6 - Use Instant Learning to improve extraction accuracy

In the two previous excercises, we saw that some of the information did not get extracted correctly and requires manual correction. To avoid having to do the corrections over and over, we want the system to learn from our corrections, which is possible with the ***Instant Learning*** feature.<br>
In this excercise, we will learn how to activate Instant Learning and how to teach the system with our feedback.

## Step 1 - Activate Instant Learning

1. To activate Instant Learning, go to the Settings menu and chose ***Manage Configuration***.
<br>![](/exercises/ex6/images/ex6_1.png)
  
2. In the configuration screen, go to the ***Learning*** and set ***Instant Learning*** to ***Active***. Afterwards click on ***Save*** to store the changes.
<br>![](/exercises/ex6/images/ex6_2.png)


## Step 2 - Teach the system with our corrections

1. Go to the ***Bill of Lading*** docuemnt worklist created in the previous excercise.<br>
If you still have documents in ***Review Needed*** state, you can use one of them, otherwise upload a new document and wait until it is in  ***Review Needed*** state.

2. Open a document that is in ***Review Needed*** state
<br>![](/exercises/ex6/images/ex6_2_1.png)

3. Click on ***Edit***
<br>![](/exercises/ex6/images/ex6_2_2.png)

4. Review the extraction results and see if anything requires a correction.<br>
E.g. you might notice that the ***Package Count*** is empty, but should be extracted from the ***Grand Total*** part of the document
<br>![](/exercises/ex6/images/ex6_2_3.png)

5. Correct the field by clicking on the text in the document preview and then select the ***Package Count*** field and apply it.
<br>![](/exercises/ex6/images/ex6_2_4.png)

6. Next go to the ***Carrier Information*** table and notice that the ***Material*** and ***Decription*** are not extracted as expected.
<br>![](/exercises/ex6/images/ex6_2_5.png)

7. Correct both fields by selecting ***X-1316*** as ***Material*** and ***Printer Ink Catridge*** as ***Description***.
<br>![](/exercises/ex6/images/ex6_2_6.png)

8. Once you are happy with the results, click on ***Confirm*** in the bottom right corner and confirm the dialog. Now you taught the model your first corrections, which will automatically be applied the next time you process a document with this schema.
<br>![](/exercises/ex6/images/ex6_2_7.png)


## Step 3 - See the Improvements in Action

1. Upload another document to see how the learning is automatically being applied. You can either upload the same file again or pick another Bill of Lading document from our samples.
<br>![](/exercises/ex6/images/ex6_2_1.png)
