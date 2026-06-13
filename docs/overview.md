# Kusto Query Language (KQL) — Overview

What is KQL
- Kusto Query Language (KQL) is a read-only query language used to explore large datasets in Azure Data Explorer (ADX) and Azure Monitor Logs. It is optimized for time-series and log analytics.

How to test and run queries
- Azure Data Explorer web UI: https://dataexplorer.azure.com/
- Kusto.Explorer (desktop): https://learn.microsoft.com/azure/data-explorer/kusto/tools/kusto-explorer
- Docs and language reference: https://learn.microsoft.com/azure/data-explorer/kusto/query

Quick local testing technique
- Use the datatable operator to create inline test data and run queries in the web UI or Kusto.Explorer. Example:

  datatable(id:int, ts:datetime, value:real)
  [1, datetime(2020-01-01), 10.5,
   2, datetime(2020-01-02), 12.0]
  | take 5

Repository layout
- /docs — conceptual docs and getting-started notes
- /queries — example queries grouped by difficulty
  - /basic — simple selects, take, where, project
  - /medium — aggregations, binning, time-series basics
  - /complex — joins, windowing, series analysis

How to run the samples
1. Open the Kusto web UI or Kusto.Explorer.
2. Copy any `.kql` sample into the query editor and run.
3. For reproducible examples, paste the datatable sections at the top of each file.

Links and further reading
- KQL tutorial: https://learn.microsoft.com/azure/data-explorer/kusto/query/tutorial
- ADX quickstart: https://learn.microsoft.com/azure/data-explorer/quickstart

"Happy querying — start with queries/basic/take_examples.kql."