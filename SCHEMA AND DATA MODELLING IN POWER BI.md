##Data Modelling and Schema Explained##
This is a way in which raw data is transformed to a clean and logical structure for the sake of analysis. Here is a short breakdown of a data model.
- Importing and transforming data by the help of a power query tool.
- Defining relationships created between tables and key columns in the power bi model view.
- Creating Measures and Calculations using Data analysis expressions (DAX)

Schema on the other hand is the process in which data is structured and connected. For instance being able to organize tables and relating them within a data model
####Types of Schemas in Power Bi Overview####

######1.Star Schema ######
This is the most common design for Power bi. It features a central **fact table** sorrounded by several **dimensional table** in a star like illustration hence the word star is derived from.

> Relationship models are typically one to many in this kind of set up.

A **fact table** is basically the central hub of the analysis that stores quantitative and measurable data`("contains the metric and the key perfomance indicators(KPI)")`. 
**Dimensional table** contains the deeper and detailed attributes that build the context of the facts.

![Star Schema](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/1bw2bcd9vdf249rt5ybu.png)

> The fact table contains the foreign keys that link to the dimensional table whereas the dimensional table contains the primary keys that idetifies each record uniquely

######2.SnowFlake Schema######
This is the further break down variation of the Star Schema. It has additional joins and further normalized a dimensional table into sub sections reducing data redudancy hence the complexity.

> Its useful when the source data is already highly normalized or storage optimization is a critical requirement.

![SnowFlake Schema](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/15v7hogwze8pge6cep8p.png)

######3.Galaxy Schema (Fast Constellation)######
This involves multiple fact tables that share common dimension tables hence ideal for large scale enterprise models requiring broad analysis across multiple business processes.
This kind of model has its own complexities due to the interconnected nature of tables but its somehow flexible.

![Galaxy Schema](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/69313huo519ah8a659h4.png).

######Relationships Explained#######
They define how data flows between tables.
They Comprise of;
- **Cardinality**(Quantity of the link)-defines how many rows in one table relate to how many rows in another.i.e
       1. One-to-Many
       2. Many-to-Many
       3. One-to-One

- **Cross-Filter Direction**-defines which way the `filtering power` goes. In this case it normally flows single(One way) that is the filter flows from the dimensional table to the fact table but not vice-versa.

****Data Modelling**** matters alot in the aspect whereby perfomance,accuracy and usability is considered in order to make the work much easier.
