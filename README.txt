The following steps are to set up a Qualtrics survey for the line study using the multiple choice style question:
1. Create the Survey
* Log into your Qualtrics account.

* Click “Create a new survey.”

* Under “From Scratch,” select “Survey” and then click “Get Started.”

* Name your project (any name is fine).

* Leave “Create a blank survey project” selected.
2. Set Up Your First Block
   * Delete the default question by clicking the three dots on the question and selecting “Delete.”

   * Rename the block to “Block 1” or another name that fits your study design.
3. Add the Multiple-Choice Question
      * Click “Add new question.”

      * Select “Multiple Choice.”
      * This can be used for the instructions question to have an I agree statement for participants consent as well as the questions for the line sets. 
      * When you click on the question a panel will appear on the left side of the screen, there you will find a lot of useful tools that are needed to create the study. For right now we will just pay attention to the number of choices and response requirements. You can change the number of answer choices you need for any question. For the response requirements in the consent statement, you need to have it set to force response because the participant needs to agree before taking the study. 
      * When making the questions for the line sets, you first need to have the images you are going to use saved on your computer. Then go to the Qualtrics library and import the images as graphics in qualtrics. 
      * Then go back to the survey builder and go to your multiple choice question for your line set. To make the answer choices images you need to click on the choice, delete the automatic text, and then there will be a dropdown menu, from there click “insert graphic” and choose an image from the library. If you need to change the image size you can click on the choice and open the drop down menu and click graphic size and then select the size you want. 

****ONLY IF THE QUESTION PART HAS AN IMAGE NOT THE ANSWERS****
4. Insert the HTML to Display the Random Image
Paste the HTML code in the file named: qualtricsHTMLCode.rtf  into the question text area under html view only for the multiple choice questions with the line sets.
5. Add the JavaScript for Random Images and Question Order Tracking
Open the question options → click the gear icon → select “Add JavaScript.”
Copy the code from the file named: qualtricsJSCode.rtf and paste it into the add JavaScript area. (more instructions in the file)
6. Add the Free-Response Comment Question
         * Add another question to the block and select “Text Entry.”

         * This question allows participants to comment on the multiple-choice question they just answered.
7. Set Up Randomization
            * Use block randomization if you have multiple blocks in the survey flow.
            * Click Survey Flow at the top.

            * In Survey Flow, click “+ Add Below.”

            * Select "Randomizer." This creates a Randomizer element in your flow.

            * Drag your blocks INTO the Randomizer.

               * Click on the move option on the left of the block in the survey flow. 

               * Drag it into the Randomizer box

               * Repeat for each block you want randomized

                  * In the Randomizer settings, choose:
                  * “Randomly present X of the following elements.”
 (Use this if you want to show only some of the blocks.)

                     * Click Apply in the bottom right.

                     * Go back to Survey to double-check that nothing moved out of order outside the Randomizer.

                        * Inside each multiple-choice question, use the Randomization settings to randomize the choices and choose “display answers in a random order”.

                        * Use “Recode Values” to rename the options using your preferred variable labels.
8. Improve the Survey Appearance
                           * Go to “Look & Feel.”

                           * Under the Layout tab, select the Modern theme to improve appearance.
9. Outputting the Data from Qualtrics to Excel 
                              * Go to the “data & analysis" tab 
                              * There should be a dropdown menu that says “export and import”, click on it then choose “export data”.
                              * You will see different formats that the data can be outputted to, choose excel.
                              * Leave download all fields checked and make sure that under “values and labels”, “export labels” is the only one marked. Then click download.


10. JS Code
                              * To change the layout of the page you need to go to each individual question, click on the question to edit it, and find the javascript link on the left side menu bar then paste the code given: “Qualtrics Code.” This changes the layout of the page to have the question on the bottom and the answers on the top, makes the answers horizontal, and moves the text only answer to the bottom, and tracks the order of sets a user is  given since it has to be randomized. 


11. Embedded Data for Question Tracking 
To ensure the JavaScript correctly logs the randomized order of your questions into your final data export, you need to define the variable in the Survey Flow.
                              * Click on Survey Flow at the top of the survey builder.
                              * Click + Add a New Element Here (it is best to place this at the very top of the flow).
                              * Select Embedded Data.
                              * In the box that says "Create New Field or Choose From Dropdown," type exactly: QuestionOrder.
Note: The name must match the JavaScript code exactly (case-sensitive) for the tracking to work.
                              * Leave the value as "Value will be set from Panel or URL" (blank).
                              * Click Apply at the bottom right.
                              * This should make it so that when you go to data & analytics it shows up as embedded data