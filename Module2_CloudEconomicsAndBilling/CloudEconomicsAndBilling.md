# AWS - Cloud Foundation

## Module 2 - Cloud Economics and Billing

### Section 1 - AWS Price Fundamentals

---

#### Three Fundamental Drivers of Cost

1. Compute
2. Store
3. Outbound Data Transfer

At mostly cases, the inbound data transfer is free. Also, data transfer between services in the same region is free too. For all outbound data transfers it is aggregated accross services and then charged at the outbound data transfer rate. This charges appears on a montly statement as AWS data transfers out.

- Reserved Instances

1. AURI - All Upfront Reserved Instances. Early payed early.
2. PURI - Partial Upfront Reserved Instances. Partialy Payed early and partialy monthly.
3. NURI - No Upfront Reserved Instances. Monthly Payed.

#### Cost Strategy

`Pay-as-you-go Strategy`

There are diferent tiers of contract of services, and each tier has diferent price. If your usage increase, you will have more dicounts.

### Section 2 - Total Cost of Ownership

---

`Total Cost of Ownership` is a financial estimate that helps customer determining the direct and indirect costs of even product or system.

`The TCO Calculator` is a smart tool tha helps to compare the on premisse infrastructure and the AWS Services.

### Section 3 - AWS Organizations

---

The `AWS Organizations` is a free account management service that enables you consolidate multiples AWS accounts into your organizational tree with each branch representing a department or team, including consolidated billing and secure management capabilities.

You can manage the organizations by:

- AWS Console (Web browser)
- CLI (local CLI terminal)
- SDK (programmaticly)
- API (HTTPS requests)

### Section 4 - AWS Billing and Cost Management

---

`AWS Billing and Cost Management` is a service that you use to pay your AWS bill. You can monitor the cost of services e plannig ahead.

You can set up a custom time period and determine the details daily or monthly

1. Billing and Payments

- `Bills: `

  This page shows a monthly view of your chargeable costs, along with details of your AWS services and purchases made through AWS Marketplace. Invoices are generated when when a monthly period closes (marked as **Issued** status), or when subscriptions or one-time purchases are made. For monthly billing periods that haven't closed (marked as **Pending** status), this page will show the most recent estimated charges based on your AWS services metered to date.

  If you are a management account of AWS Organizations you can view consolidated charges for all of your member accounts, along with account level details available on the **charges by account** tab.

  Choose **View Billing Period** on the top right to specify you billing period.

- `Payments: `

  - `Payments due: ` You can view amount totals in the **Payments due** summary section of the **Payments due** tab. Use the table to search, filter and select specifc invoices. Select the gear icon to change the default columns and customize other table settings.

    `Statuses shown on table: `

    **Due:** Outstanding invoices with an approaching due date.

    **Past Due:** Outstanding invoices where a payment has not been made by the due date.

    **Scheduled:** Invoices with upcoming scheduled payment.

    **Processing:** Invoices for wich we are currently scheduling a payment.

  - `Unapplied funds: ` You can view amount totals in the **Unapplied funds summary** section of the **Unapplied funds** tab. Use the table to search, filter and select funds that haven't been applie to your AWS account. Choose the gear icon to change the default columns and other table settings.

    `Types of unapplied funds: `

    **Credit memo:** Credits issued as a part of a Saving Plan, or a result of invoide adjustments.

    `Table status: `

    **Unapplied:** Available credit memos to be applied to an invoice.

    **Partially applied:** Credit memos where some amounts have been applied to a previous invoice.

  - `Transactions: `You can view your transactions history with AWS in the transactions table. Use the table to search, filter and select specific transactions. Transactions shown on this page have been completed and applied to your account. Choose the gear icon to change the default columns an other table settings.

- `Credits: ` AWS credits are applied to bills to help cover costs that are associated with eligible services. Credits are applied until they are exhausted or they expire.

- `Purchase Orders: ` AWS Purchase Order Management allows you to easily manage your AWS purchase orders (POs) in a self-service manner. Manage your PO information from the Purchase Orders dashboard in the Billing Console, configure multiple POs, and define the rules of how they map to your invoices. Monitor your PO status and balance on your Purchase Orders dashboard. Stay informed with email notifications when your POs approach expiration or run out of balance.

2. Costs Analysis

- `Cost Explorer: `Cost Explorer is a tool that enables you to visualize, understand and manage your AWS costs and usage over time. With Cost Explorer, you can filter and group by values such as API operation, Availability Zone, AWS service, custom cost allocation tag, Amazon EC2 instance type, purchase option, AWS region, usage type, usage type group and more. If you use consolidated billing, you can also filter by member account. In addition, you can see a forecast of future costs based on your historical cost data.

  After you have achieved your desired results with filters and group-bys, you can either download your results by choosing **Download as CSV** or save the report by clicking **Save to report library**.

- `Cost Explorer Saved Reports: ` The Report page provides default reports. You can also create new report with existing templates. The reports include Cost and usage report, Saving Plans utilization report, Saving Plans coverage report, reservation utilization report and reseration coverage report.

- `Cost Anomaly Detection: ` This section provides key performance indicators (KPIs) to help measure monthly trends such as the total count of anomalies, the total financial impact of anomalies and month over month costs trend.

  - `Detection history: ` This section provides an event log of all anomalies detected in your account, regardless of source monitor and root cause. Each anomaly includes information for the date of occurrence, duration, financial impact, and root cause if it is available. The event log can be customized to your preference based on the available data.

  - `Cost monitors: ` This section provides a list of all monitors that evaluate your account for anomalies. There are four available monitor types that help segment your cost for further granular analysis.

  - `Alert subscriptions: ` This table shows all of the alert subscriptions that are created for this account. Each subscription specifies an alert threshold, frequency, subscribers and attached cost monitors.

- `Free Tier: ` The AWs Free Tier is designed to give you hands-on experience with a range of AWS services at no charge. When you create an AWS account, you are automatically signed up for the AWS Free Tier for 12 months. Your AWS Free Tier elegibility expires at the end of the 12-month period. When your AWS Free Tier expires, AWS starts charging the regular rates for any AWS services and resources that you are using.

- `Data Exports: ` You can use AWS Data Exports to quickly configure exports from multiple AWS cost management and billing datasets. Select only the data you want to process, remove any sensitive cost information, and control the output schema of your exports. You can also create a data export that builds directly to a dashboard in Amazon QuickSight.

3. Cost Organization

- `Cost categories: ` You can use to group your cost and usage information into meaningful categories based on your needs. You can create custom categories based on the rules you define using various dimensions. For example, account, tag, service, charge, type, region and other cos categories. Once cost categories are set up, you can use them across products in the AWS Billing and Cost Management console. This includes Cost Explorer, AWS Budgets, AWS Cost and Usage Reports (AWS CUR) and AWS Cost Anomaly Detection.

- `Cost Allocation Tags: ` A tag is a label that you or AWS assingns to an AWS resource. The tag consists of a key and a value. You can activate tags as cost allocation tags. After you activate cost allocation tags, AWS uses the cost allocation report, to make it easier for you to categorize and track your AWS costs. To retoractively view a cost corresponding to tags from a previous month, you can use the bakcfill tags feature. The current tag status (active or inactive) wil be backfilled to tahc month. This enables you to see costs even if the tag wasn't active before. For example, if you have an active tag `Engeneering`, you can change the month from wich you want to view costs. Inactive tags won't show costs from the month that you choose and will not appear in AWS Cost Explorer or AWS Cost an Usage Report (CUR). You can submit a backfill tag request once every 24 hours if the prior backfill request is complete.

  - `User-defined cost allocation tags: ` User-defined tags are tags that you define, create and apply to resources. To create and apply your tags to resources, use AWS Tag Editor. After you create and apply your user defined tags, use the AWS Billing console to activate your tags for cost allocation tracking. The `awsApplication` tag wil be automatically added to all resources that are associated with applications that are set up in AWS Service Catalog AppRegistry. This tag is automatically activated for you as a cost allocation tag. Tags that are automatically activated don't count towards your cost allocation tag quota.

  - `AWS generated cost allocation tags: ` The AWS generated tags `createdBy` is a tag that AWS defines and applies to supported AWS resources for cost allocation purposes. The AWS generated tags are available only in the AWS Billing and Cost Management console and reports and doewn't appear anywhere else in the AWS console, including the AWS Tag Editor. The `createdBy` tag does not count towards your taggs per resource limit.

- `Billing Conductor: ` AWS Billing Conductor simplifies cost management of your organization by segmenting your account into logical billing groups (for example, by customer or business unit). Each billing group will have an applied price plan, wher eyou can apply a percentage-based markup or discount on top of AWS On-Demand rates to all usage accrued by the billing grop's associated account. Manage your billing groups and pricing plans using a stremlined AWS console interface. Your custom configuration are used to compute cost and usage data is visible on the Bills page and avaliable by Cost and Usage Report, where you can view and inspect each individual billing group's custom-rated cost right in your Billing Dashboard. The billing group's associated accounts can also theirs perspective pro forma costs in AWS Cost Explorer.

4. Budgets and Planning

- `Budgets: ` You can use AWS Budgets To set custom budgets that alert you when your costs and usage, utilization or coverage os Savings Plans and RIs exceed your budget amount.

- `Budget Reports: ` You can use Budget Reports to create and send daily, weekly or montly reports to monitor the performance of your AWS Budgets.

### Section 5 - Technical Support

- `AWS Support Concierge: ` For billing and account helps.

- `AWS Trust Advisor: ` To check the best practicies in your environment. It's an automated service that act like an customize cloud expert.

- `Technical Account Manager (TAM): ` The primary point of contact on Enterprise Suport Plan.

#### Four Suport Levels:

Each on level has a particular SLA.

1. `Basic: ` Free. The default support level.

2. `Developer: ` Not Free. Recommended if you are experimenting or testing AWS.

3. `Business: ` Not Free. Minimum level support for who has AWS production workloads.

4. `Enterprise: ` Not Free. Recommended for who has essential AWS production workload.

auri, nuri puri
