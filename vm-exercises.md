# Virtual Machine (VM) Exercises

## :information_source: Read this before getting started
- The two exercises should not replicate the exact actions shown in your screencast. The goal of exercises is for learners to apply what was learned in the screencasts to new problems or situations. This is best pedagogical practice for retaining and building skills. For example, this can be done by using another dataset between screencasts and exercises or focusing on a different portion of the dataset.
- We can only run free versions of BI software in our virtual machine exercises. In the case of Power BI, make sure the exercises can run on [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) without any additional paid products. 
- Unsure what the scope of an exercise should be? Here's an [example](https://campus.datacamp.com/courses/introduction-to-power-bi/getting-started-with-power-bi?ex=14) from Introduction to Power BI. The first chapter of most DataCamp courses are free, so take a look at our [BI courses](https://learn.datacamp.com/courses?technologies=Tableau&technologies=Power%20BI) to get a feel for how we assess and guide learners.

## 1st VM Exercise

#### Dataset

- [ ] Add datasets used to the `datasets/` folder

#### Files

- [ ] **Initial**: Add file to the `exercises/`  folder with the name `ex-1-intial.twbx` or `ex-1-intial.pbix`, depending if you are auditioning for a Tableau or Power BI course.
- [ ] **Solution**: Add file to the `exercises/`  folder with the name `ex-1-sol.twbx` or `ex-1-sol.pbix`

#### Learning Objective

This exercise allows you to practice implementing the DATETRUNC function and combining it with parameters to dynamically switch time frame resolutions on a timeline graph.

#### Context

Being able to change the context of the time frames you are visualizing data is key to ensuring you are zeroing in or data points that are relevant to your stakeholders.
For example, a program owner might need to view more granular information that's on a monthly level, the program owner's manager might need the data on a quarterly basis for performance reviews. Finally, your director might need the data on an annual basis to justify budgets to his or her stakeholder.
Knowing how to crate these types of dynamically responsive visualizations is a great way to empower your stake holders to get the data they need themselves, without having to rely on someone else by create ad-hoc reporting requests.

#### Steps to be executed by the student (max 6)

*Each bulleted instruction is a complete sentence that describes a specific task.*

- Step 1: Create your time resolution parameter. This will be the drop down menu for your end users of the dashboard. Ensure it has a name that makes sense. Ensure the data type is set to "string". Create the string values "month", "quarter", "year".
- Step 2: Modify our previously created calculated fields that we are referencing in "Time Frame Calculation" ("Time Frame Resolution: Comp" and "Time Frame Resolution: Fill Rate") so that they make use of the parameter created in Step 1. Write a simple calculation that makes use of the DATETRUNC function, and references the parameter you created in Step 1  for the "date_part" field of the calculation. For "Time Frame Resolution: Comp", ensure your "date" value field is "completion_date", and for Time Frame Resolution: Fill Rate, ensure that it's set to "session_start_date".
- Step 3: Add the parameter to the view of the worksheet and try the different drop-down option while observing how the visualization changes based on your selections.

#### Exercise question:
Set the following values for your parameters in view:
Program Name: C-Level Engagement
Is Active Filter: Full Historical Performance
Time Measurement Parameter: Fill Rate
Running or Total: Time Frame Specific
Time Resolution: Quarter

What is the percentage value for "Time Period Start: Apr '21"?
ANSWER: 50.4%

#### End goal:

[*Add an image of the final visualization here.*](https://drive.google.com/file/d/1kmHmnw2PiN_tHZlThwsQybUf0zbnPsHC/view?usp=share_link)

## 2nd VM Exercise

#### Dataset

- [ ] Add datasets used to the `datasets/` folder

#### Files

- [ ] **Initial**: Add file to the `exercises/`  folder with the name `ex-2-intial.twbx` or `ex-2-intial.pbix`, depending if you are auditioning for a Tableau or Power BI course.
- [ ] **Solution**: Add file to the `exercises/`  folder with the name `ex-2-sol.twbx` or `ex-2-sol.pbix`

#### Learning Objective

In this exercise will expand on our time frame resolution dropdown by making it responsive to non-standard tableau DATETRUNC values, by combining it with DATEADD calculations.

#### Context

In many lines of work, you will find that stakeholders need reporting done on time frames such as half yearly, or custom month collections based on fiscal years that might not align with calendar years, and so on.
Being able to create solutions for these types of asks in Tableau can be vital depending on your line of work.
This exercise will also help you grasp how you can combine different date functions to create adjusted calculations in general, which is applicably to a wide range of reporting needs you are likely to stumble across in your career.


#### Steps to be executed by the student (max 6)

*Each bulleted instruction is a complete sentence that describes a specific task.*

- Step 1: Edit the parameter you created for the time resolution drop down menu, by adding a string value called ”half” without the quotation marks.
- Step 2: Set the time resolution drop down menu to this newly created value of "half", observe that the visualization breaks
- Step 3: Modify the calculations in fields "Time Frame Resolution: Comp" and "Time Frame Resolution: Fill Rate" to be able to respond to our new custom value. To achieve this, you'll need to re-write the calculations with IF/ELSEIF statements that will treat each value of our time resolution parameter separately. For the custom "half" value, we will need to adjust the calculation to also use the DATEADD function. If you get stuck, just look back at the previous video where I cover this type of calculation.
- Step 4: Test your new calculations by selecting the value "half" again in the time resolution drop down menu. If you've written the calculation correctly, the line graph should now display information correctly again.

#### Exercise question:
Set the following values for your parameters in view:
- Program Name: Accelerating Client Program Spend
- Is Active Filter: Full Historical Performance
- Time Measurement Parameter: Completion Rate
- Running or Total: Running Total
- Time Resolution: Half

What is the percentage value for "Time Period Start: Jan '22"?
ANSWER: 67.5%

#### End goal:
[*Add an image of the final visualization here.*](https://drive.google.com/file/d/1gbnlFu8bLM08zP5yrx9Iu31USWSlmdpH/view?usp=share_link)

