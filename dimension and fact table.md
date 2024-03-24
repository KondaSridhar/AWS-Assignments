
Dimension and fact tables are fundamental components of a dimensional model used in data warehousing and business intelligence systems. They play distinct roles in organizing and storing data for analytical purposes. Here's an explanation of each:


**Definition:** A dimension table contains descriptive attributes that provide context and categorization for the data in a data warehouse. These attributes are often used for filtering, grouping, and labeling data during analysis.
**Characteristics:**

**Descriptive Attributes:** Dimension tables typically contain textual or categorical attributes that describe the business entities being analyzed, such as customers, products, time periods, or geographic locations.

**Hierarchical Structure:** Dimension tables may have a hierarchical structure, with attributes organized in levels of granularity. For example, a time dimension might have levels like year, quarter, month, and day.

**Small Size:** Dimension tables tend to be relatively small compared to fact tables since they store descriptive information rather than transactional data.

**Slowly Changing Dimensions (SCDs):** Dimension tables may handle changes in descriptive attributes over time using techniques such as Type 1 (overwrite), Type 2 (add new row), or Type 3 (add new column) slowly changing dimension methodologies.

**Example:** In a sales data warehouse, a dimension table for products might include attributes such as product ID, name, category, brand, and supplier.




**Definition:** A fact table contains quantitative measurements (facts) of a business process or event, typically numeric values that can be aggregated or analyzed. Fact tables are at the center of the star schema or snowflake schema in a dimensional model.



**Quantitative Measures:** Fact tables store numeric data representing business metrics or performance indicators, such as sales revenue, quantity sold, profit, or inventory levels.

**Foreign Keys:** Fact tables often include foreign keys that reference primary keys from dimension tables, establishing relationships between the facts and the descriptive attributes.

**Large Size:** Fact tables tend to be larger than dimension tables since they store detailed transactional data or aggregated values at various levels of granularity.

**Aggregation Levels:** Fact tables may contain data at different aggregation levels to support various analysis requirements, such as daily, weekly, or monthly aggregations.

**Example:** In a sales data warehouse, a fact table might include columns such as date key (foreign key to the time dimension), product key (foreign key to the product dimension), sales amount, quantity sold, discount applied, and profit margin.
In summary, dimension tables provide descriptive context for analytical queries, while fact tables store the measurable facts or metrics associated with business processes. Together, they form the foundation of a dimensional model, enabling efficient and flexible data analysis in data warehousing and business intelligence environments.
