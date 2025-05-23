# Conga Platform Chrome Extension

The Conga Platform Extension is a Chrome Extension designed to enhance productivity for developers working with the Conga Platform. It provides quick utilities for auth token copy, quick redirection and easy data handling (import/export).

**Features:**

> 1) Copy user authentication token

* The option is available on conga platform page by hovering over the org name displayed via extension
  
  ![](assets/20250428_175141_CopyAuthToken.gif)

> 2) Generate GUID

* Clicking this will prompt you to provide salesforce Id, helping you find the Platform ID of any master data synced from Salesforce to Conga Platform. This eliminates the need to query the platform using External IDs just to retrieve the Platform Id of the record.
  
  ![](assets/20250428_180258_GenerateGUID.gif)

> 3) Compare Salesforce record

* You can compare record from salesforce page in a split view to compare the record details between salesforce and Conga platform. This will help see values on same page from both platforms and records can be updated during testing.
* Once the split view is open it will automatically try to detect the record change on the tab and open the record details in split view as the user navigates through records.
  
  <video width="600px" controls>
  <source src="assets/20250428_181725_CompareRecord.mp4" type="video/mp4"></video>


> 4) Conga Platform Query

* You can write query in text box and get suggestion for object name or object fields based on the query user enters.
* You can press `CNTRL + SPACE` to select all fields of the selected object
* User can enter relational fields in where clause of query to apply filter based on relation fields

```
SELECT ID From LineItem WHERE Configuration.ParentProposal.ExternalId = 'a1ran000000o9qMAAQ'
```

* User can also use relation fields in select clause

```
SELECT id,PriceRule.Ruleset.Type FROM PriceRuleEntry WHERE PriceRule.Name = 'Test'
```

* You can apply filter on multiple columns after the data is fetched by clicking on filter icon

![](assets/20250428_220341_queryfilter.png)

* Below is demo showing how you can query using related fields in query


  https://github.com/user-attachments/assets/3ad785ef-03a8-4717-9336-f1cd18d4d783


    <video width="600px" controls>
  <source src="assets/QueryDemo1.mp4" type="video/mp4"></video>
