## Einstein Language
* [Einstein Bot Cookbook](https://developer.salesforce.com/docs/atlas.en-us.bot_cookbook.meta/bot_cookbook/bot_cookbook_beginner_section.htm)

Language contains two NLP services: Einstein Intent and Einstein Sentiment.

The Einstein Language APIs support data in these file formats:
.csv (comma-separated values)
.tsv (tab-separated values)
.json

### Einstein Intent—
The Einstein Intent API categorizes unstructured text into user-defined labels to better understand what users are trying to accomplish. Use this API to analyze text from emails, chats, or web forms to:
* Determine which products prospects are interested in, and send customer inquiries to the appropriate sales person.
* Route service cases to the correct agents or departments, or provide self-service options.
* Understand customer posts to provide personalized self-service in your communities.

### Einstein Sentiment—
The Einstein Sentiment API classifies text into positive, negative, and neutral classes to understand what the words people use can tell us about how they’re feeling. Use this API to analyze emails, social media, and text from chat to:
* Identify the sentiment or emotion in a prospect’s emails to trend a lead or opportunity up or down.
* Provide proactive service by helping dissatisfied customers first or extending promotional offers to satisfied customers.
* Monitor how people perceive your brand across social media channels, identify brand evangelists, and note customer satisfaction.

### Resources
* [Einstein API Signup](https://api.einstein.ai/signup)
* [Einstein Platform Developer Guide](https://metamind.readme.io/docs/intro-to-einstein-language)
* [Einstein Private Key](https://api.einstein.ai/reset/confirm?tenantToken=64EPOE3MAARSCO7ASQ3HJR6H2NWO6RLMADADPXXALEYPVBTBVS5LVIVEDIGBJ2B34GN2FCUUB2HTE45FDI2A47XXG4XGIAJZ2MQX5YY)
* [Algorithmia](https://algorithmia.com/users/anablock)
* [Analytics Extended Metadata (XMD) Reference](https://developer.salesforce.com/docs/atlas.en-us.222.0.bi_dev_guide_xmd.meta/bi_dev_guide_xmd/bi_xmd_intro.htm)
* [Chart Suggestions](https://s3.amazonaws.com/extremepresentations/extremepresentations/wp-content/uploads/6a00d8341bfd2e53ef0148c699cc96970c.jpg)
* [Einstein Analytics Glossary](https://help.salesforce.com/articleView?id=bi_glossary.htm&type=5)
* [Visualize Data With Charts](https://help.salesforce.com/articleView?id=bi_visualize.htm)
* [Einstein Token](https://api.einstein.ai/token)

## CPU_TIME
 CPU time is calculated for all executions on the Salesforce application servers occurring in one Apex transaction. CPU time is calculated for the executing Apex code, and for any processes that are called from this code, such as package code and workflows. CPU time is private for a transaction and is isolated from other transactions. Operations that don’t consume application server CPU time aren’t counted toward CPU time. For example, the portion of execution time spent in the database for DML, SOQL, and SOSL isn’t counted, nor is waiting time for Apex callouts.

```sql
q = load "ApexExecutionWithUsers";
q = group q by 'TIMESTAMP_DERIVED_Month';
q = foreach q generate 'TIMESTAMP_DERIVED_Month' as 'TIMESTAMP_DERIVED_Month', sum('RUN_TIME') as 'sum_RUN_TIME', sum('CPU_TIME') as 'sum_CPU_TIME';
q = order q by 'TIMESTAMP_DERIVED_Month' asc;
q = limit q 2000;
```

```sql
result = load dataset;
result = filter rows by predicate;
// for 
q = foreach q generate expression as alias[, expression as alias ...];
