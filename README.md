# ✍️ Product Inventory Expiry Alert Automation Workflow

A Power Automate and Excel project built to track product expiry records, monitor decision status and send reminder emails to the PIC when action is required.

This project shows how a manual product tracking sheet can be converted into a structured automation workflow. The flow checks each product record, refreshes the reminder stage, updates the tracker and prepares email reminders for the responsible PIC.

## Dashboard Preview

[![Dashboard Preview](Dashboard_Preview.png)](Product_Expiry_Tracker.xlsx)

## 🎯 Project Objective

The goal was to create a simple control system for product expiry follow up.

The tracker needed to help operations answer five practical questions:

| Question                            | Why it matters                                                    |
| ----------------------------------- | ----------------------------------------------------------------- |
| Which products are being tracked?   | Gives operations a single view of active product records          |
| Which products are close to expiry? | Helps the team see which items need attention first               |
| Has a decision been made?           | Separates completed items from items still waiting for PIC action |
| Who is responsible?                 | Connects each product to the right PIC for follow up              |
| Should an email be sent?            | Ensures reminders are only sent when action is still required     |


## ⚙️ Workflow Logic

The automation was built in Power Automate and connected to an Excel tracker.

The flow checks the product tracker on a regular schedule, reviews each product record and refreshes the reminder status based on the expiry and action logic.

| Workflow step      | What it does                                                       |
| ------------------ | ------------------------------------------------------------------ |
| Recurrence trigger | Runs the workflow on a scheduled basis                             |
| List rows          | Reads product records from the Excel tracker                       |
| Apply to each      | Loops through each product record one by one                       |
| Nested conditions  | Checks whether the product has reached the relevant reminder stage |
| String variables   | Stores products that need to be included in the reminder email     |
| Update row         | Refreshes reminder status directly in Excel tracker                |
| Compose message    | Builds the reminder email content                                  |
| Send email         | Sends an Outlook reminder only when action is required             |

## 📊 Excel Tracker Design

The Excel file was modelled as both a working tracker and a reporting template.

It includes:

| Area                | Purpose                                                                        |
| ------------------- | ------------------------------------------------------------------------------ |
| Product records     | Stores product name, expiry date, PIC, decision and reminder information       |
| Decision fields     | Tracks whether the item has been reviewed or completed                         |
| Reminder stage      | Shows the current follow up stage for each product                             |
| PIC ownership       | Assigns each product record to the responsible person                          |
| Email required flag | Identifies whether the product should be included in the reminder email        |
| Dashboard summary   | Gives a quick management view of expiry risk, reminder stage and action status |
| User guide          | Explains how the tracker should be used and how the flow logic works           |

## 🧮 Excel Logic Used

The tracker was designed with structured tables and rule based fields so that Power Automate could read and update the records cleanly.

| Excel feature          | How it was used                                                                        |
| ---------------------- | -------------------------------------------------------------------------------------- |
| Structured tables      | Created a stable data source for Power Automate row retrieval                          |
| IF and IFS logic       | Classified reminder stage, action status and decision outcome                          |
| AND and OR logic       | Checked multiple conditions before marking records as requiring action                 |
| Lookup fields          | Connected product records with PIC, reminder and decision information                  |
| Conditional formatting | Highlighted products requiring attention                                               |
| Pivot summaries        | Summarised products by reminder stage, PIC ownership and action status                 |
| Dashboard cards        | Displayed key figures such as total products, active reminders and completed decisions |

## 📈 Dashboard Output

The dashboard was designed for quick operations review.

It shows:

1. Total products tracked
2. Products by expiry risk
3. Active reminder stage
4. Email required items
5. PIC follow up ownership
6. Completed decisions
7. Action status breakdown
8. Reminder progress summary

The dashboard helps the reviewer understand the status of the tracker without checking every product row manually.

## 🛠️ Tools and Skills Demonstrated

| Tool or method           | How it was used                                                                                                 |
| ------------------------ | --------------------------------------------------------------------------------------------------------------- |
| Microsoft Power Automate | Scheduled the workflow, checked product rows, applied reminder rules and triggered email logic                  |
| Excel                    | Built the tracker, formula logic, structured tables, conditional formatting, pivot summaries and dashboard view |
| Outlook                  | Sent reminder emails when product records required follow up                                                    |
| Workflow automation      | Converted manual expiry checking into a repeatable reminder process                                             |
| Exception monitoring     | Flagged products requiring action rather than reviewing all records equally                                     |
| Reporting design         | Turned product level data into dashboard level summaries for operations review                                  |

## 📁 Repository Files

| File                          | Description                                                             |
| ----------------------------- | ----------------------------------------------------------------------- |
| `Product_Expiry_Tracker.xlsx` | Excel tracker and dashboard template used for product expiry monitoring |
| `Power_Automate_Flow.pdf`     | Exported workflow screenshots showing the Power Automate logic          |
| `Dashboard_Preview.png`       | Preview image of the dashboard summary                                  |

## ✅ What This Project Demonstrates

This project demonstrates my ability to:

1. Build a scheduled workflow using Power Automate
2. Connect automation logic with an Excel based tracker
3. Use structured tables so records can be read and updated reliably
4. Apply conditional logic to classify reminder status
5. Use Excel formulas, lookup fields, conditional formatting and pivot summaries
6. Create a dashboard view for operations monitoring
7. Automate email reminders based on action required logic
8. Document the process clearly for portfolio review

## 🔗 Relevance to Data Analyst and Operations Roles

This project is relevant to roles involving reporting automation, exception monitoring and operations control.

The same logic can be applied to areas such as:

1. Payment exception tracking
2. Invoice follow up
3. Stock or product monitoring
4. Compliance reminders
5. Customer account review
6. Weekly reporting workflows
7. Manual process automation

The project shows how Excel and Power Automate can work together to create a simple control process that is easier to monitor, update and explain.

## 🔐 Public Repository Notes

This is a public portfolio version.

The tracker uses sample product records and does not include confidential company data, real supplier details or internal email addresses.
