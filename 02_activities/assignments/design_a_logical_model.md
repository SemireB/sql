# Assignment 1: Design a Logical Model
### Name: Semire Bamikole

## Question 1
Create a logical model for a small bookstore. 📚

At the minimum it should have employee, order, sales, customer, and book entities (tables). Determine sensible column and table design based on what you know about these concepts. Keep it simple, but work out sensible relationships to keep tables reasonably sized. Include a date table. There are several tools online you can use, I'd recommend [_Draw.io_](https://www.drawio.com/) or [_LucidChart_](https://www.lucidchart.com/pages/).

![assignment_1_ERD_1.png](https://github.com/SemireB/sql/blob/Assignment/02_activities/homework/images/assignment_1_ERD_1.png)

## Question 2
We want to create employee shifts, splitting up the day into morning and evening. Add this to the ERD.
![assignment_1_ERD_2.png](https://github.com/SemireB/sql/blob/Assignment/02_activities/homework/images/assignment_1_ERD_2.png)

## Question 3
The store wants to keep customer addresses. Propose two architectures for the CUSTOMER_ADDRESS table, one that will retain changes, and another that will overwrite. Which is type 1, which is type 2?

_Hint, search type 1 vs type 2 slowly changing dimensions._

Bonus: Are there privacy implications to this, why or why not?
```
Type 1 is the architecture that would overwrite changes to the customer address table. Whenever a customer updates their address, the existing address is updated with the new address and the history of the previous address is deleted.

Type 2 is the architecture that would retain changes to the customer address table. Whenever a customer updates their address, a new record is inserted into the table with the new address and the history of the previous adress is kept with the effective date showing inactive for the old record and active for the new record.

With type 2 where changes are retained there are higher privacy implications due to the amount of personal data collected over time in the stored history.
```

## Question 4
Review the AdventureWorks Schema [here](https://i.stack.imgur.com/LMu4W.gif)

Highlight at least two differences between it and your ERD. Would you change anything in yours?
```
Difference 1: the AdventureWorks Schema is very large so to help with readability and comprehension they categorized and colour coded the smaller schemas that interact to create the larger schema.

Difference 2: for each table in the AdventureWorks Schema the primary and foreign keys are identified for further comprehension.

Becasue my model is smaller and less complex I wouldn't categorize and colour code the schemas but I would add the primary and foreign keys for each of the tables.



```

# Criteria

[Assignment Rubric](./assignment_rubric.md)

# Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `September 28, 2024`
* The branch name for your repo should be: `model-design`
* What to submit for this assignment:
    * This markdown (design_a_logical_model.md) should be populated.
    * Two Entity-Relationship Diagrams (preferably in a pdf, jpeg, png format).
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sql/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [x] Create a branch called `model-design`.
- [x] Ensure that the repository is public.
- [x] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [x] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack at `#cohort-4-help`. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
