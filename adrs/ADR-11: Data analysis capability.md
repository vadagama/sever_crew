## ADR-10: Cloud provider

### Date:
2021-11-14

### Status:
Proposed

### Context:
We propose to choose Amazon data analysis services for Users Engagement Analysis Module. There are two options: Amazon Athena and Amazon Redshift.

Athena is a serverless service and does not need any infrastructure to create, manage, or scale data sets. It works directly on top of Amazon S3 data sets. It creates external tables and therefore does not manipulate S3 data sources, working as a read-only service from an S3 perspective. 

On the other hand, Redshift is a petabyte-scale data warehouse used together with business intelligence tools for modern analytical solutions. Unlike Athena, Redshift requires a cluster for which we need to upload the data extracts and build tables before we can query. 

<table>
  <tr>
   <td>
   </td>
   <td>RedShift
   </td>
   <td>Athena
   </td>
  </tr>
  <tr>
   <td>Partitioning
   </td>
   <td>
<ul>

<li>Does not support direct partitioning by default

<li>Uses predefined distribution keys to optimize tables for parallel processing

<li>Poor manual partition key selection can dramatically impact query performance, so Redshift does it for you
</li>
</ul>
   </td>
   <td>
<ul>

<li>Can partition by any key with up to 20,000 per table

<li>Supports several Serializer/Deserializer (SerDe) libraries for parsing data from different data formats: CSV, JSON, TSV, and Apache logs

<li>Does not support arrays or object identifier types
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>User Defined Functions
   </td>
   <td>
<ul>

<li>Supports UDFs with scalar and aggregate functions
</li>
</ul>
   </td>
   <td>
<ul>

<li>Does not support UDFs
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Data Formats and Types
   </td>
   <td>
<ul>

<li>Supports several Serializer/Deserializer (SerDe) libraries for parsing data from different data formats: CSV, JSON, TSV, and Apache logs

<li>Does not support arrays or object identifier types
</li>
</ul>
   </td>
   <td>
<ul>

<li>Supports several Serializer/Deserializer (SerDe) libraries for parsing data from different data formats: CSV, JSON, TSV, Parquet, and ORC

<li>Beneficial due to Athena’s convenient data to query structure

<li>Supports complex data types like arrays, maps, and structs
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Infrastructure
   </td>
   <td>
<ul>

<li>Requires a cluster to set itself up. A significant amount of time is required to prepare and set up the cluster. Once the cluster is ready to use, we need to load data into the tables. This also comes with a lag time depending on the amount of data being loaded.
</li>
</ul>
   </td>
   <td>
<ul>

<li>Free from all such dependencies as it does not need infrastructure at all. It just creates its own external tables on top of Amazon S3 data sets.
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Pricing
   </td>
   <td>
<ul>

<li>Based on type and number of nodes in a cluster

<li>Hourly rate for both dense compute nodes and dense storage nodes

<li>Predictable price with no penalty on excess queries, but can increase overall cost with fixed compute (SSD) and storage (HDD)
</li>
</ul>
   </td>
   <td>
<ul>

<li>Price is per terabyte of data scanned during a query execution

<li>Minimum of 10 megabytes per query execution

<li>No charge for failed queries

<li>Most cost effective when data is compressed, partitioned, or converted to columnar format
</li>
</ul>
   </td>
  </tr>
</table>


### Decision:
We propose to use AWS Glue with AWS Athena for data analysis capability. Amazon Athena is noteworthy due to its simple yet efficient quality. No initial set up is required which makes ad hoc querying easy. It’s practical for simple read and aggregated queries and is relatively cost effective. Generally, Athena works best for quickly and conveniently running queries at a low cost without needing to set up a complex infrastructure. We don’t need all the possibilities and complexity of the Redshift solution on this step.