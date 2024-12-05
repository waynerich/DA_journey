<b>Data</b> is a collection of facts such as numbers, descriptions, and observations used to record information<br>

<b>Common data formats / Classifications of data:</b><br>
<b>Structured data</b> is typically tabular data that contains rows to represent each instance of the entity and columns to represent the attributes of the entity<br>
<b>Semi-structured data</b> is data that somehow has structure that allows variation such as number of values for a field between entity instances<br>
<b>Unstructured data</b> is raw binary data such as images, audio, and video<br>

<b>File stores:</b><br>
<b>Delimited text files</b> store data in plain text with specific file delimiters (comma, tab, space) and row terminators (carriage return, new line)<br>
<b>JavaScript Object Notation (JSON)</b> is a format in a hierarchical document schema used to define data entities (objects) that have multiple attributes, where an attribute can be an object or a collection of objects<br>
<b>Extensible Markup Language (XML)</b> is a human-readable data format that was superseded by the less verbose JSON format<br>
<b>Binary Large Objects (BLOBs)</b> store data as raw binary to be interpreted by applications and rendered like images, audio, video, and application-specific documents<br>
<b>Optimized file formats</b> are for efficient storage and processing, enabling compression and indexing. Common otimized file formats are:<br>
&emsp;<b>Avro</b> is a row-based format where each record contains a header (stored as JSON document) that describes the structure of the data (stored as binary information)<br>
&emsp;&emsp;-optimized for compressing data, minimizing storage and network bandwidth requirements<br>
&emsp;<b>Optimized Row Columnar format (ORC)</b> is a column-based format that contains stripes of data where each stripe holds the data for a column or set of columns<br>
&emsp;&emsp;-optimized for read and write operations over large datasets in Apache Hive<br>
&emsp;<b>Parquet</b> is a column-based format that contains row groups where data for each column is stored together in the same row group<br>
&emsp;&emsp;-optimized for storing and processing nested data types efficiently, compressing and encoding schemes<br>

<b>Databases:</b><br>
Database is used to define a central system which data can be stored and queried<br>
<b>Relational database</b> is a database management system used to store, manage, and query structured data using Structured Query Language (SQL). Tables are stored in the database (represents as entities), and that each row (represents as entity instance) is assigned a primary key to uniquely identify it and is used to reference the enitity instance in other tables. The usage of keys to reference enables a relational database to be normalized; which in part means the elimination of duplicate data values<br>
<b>Non-relational / NoSQL database</b> is a database management system that does not apply a relational schema to the data. Types of non-relational databases:<br>
&emsp;<b>Key-Value Database</b> is where each record consists of a unique key, and an associated value in any format<br>
&emsp;<b>Document Database</b> is a specific form of key-value database where the value is a JSON document<br>
&emsp;<b>Column Family Database</b> stores tabular data where columns can be divided into groups known as "column-families" where each column-family holds a set of columns that are logically related together<br>
&emsp;<b>Graph Database</b> stores entities as nodes with links to define relationships between them<br>

<b>Transactional Data Processing</b><br>
Transactional data processing system records transactions(a small, discrete, unit of work) of specific events that the organization wants to track. The work being performed by this system is often referred to as <b>Online Transactional Processing (OLTP)</b>. OLTP solutions rely on database system in which data storage is optimized for read and write operations in which data records are Created, Retrieved, Updated, and Deleted (CRUD operations). To ensure the integrity of data, transactional workloads should enforce <b>ACID</b> semantics:<br>
&emsp;<b>Atomicity</b> - each transaction should either succeed completely or fail completely. If either action cannot be completed, the corresponding action must fail<br>
&emsp;<b>Consistency</b> - transactions can only take the data in the database from one valid state to another<br>
&emsp;<b>Isolation</b> - concurrent transactions cannot interfere with one another, and must result in a consistent database state<br>
&emsp;<b>Durability</b> - a transaction that has been committed, must remain committed regardless of the state of the hardware the system resides in<br>
OLTP systems are typically used to support live business / Line of Business (LOB) applications that process business data<br>

<b>Analytical Data Processing</b><br>
Analytical data processing typically uses read-only system that store vast columns of historical or business data optimized for analytical workloads such as producing reports, dashboards, and visualizations<br>
Common architecture for analytical processing system:<br>
&emsp;1 - Operational data is extracted, transformed, and loaded (ETL) into a data lake for analysis<br>
&emsp;2 - Data in the data lake or data warehouse is loaded into a schema of tables<br>
&emsp;3 - Data in the data warehouse may be aggregated and loaded into an OLAP model; which is an aggregated type of data storage that is optimized for analytical workloads<br>
&emsp;4 - Data in the data lake, data warehouse, and OLAP model can be queried to produce reports, visualizations, and dashboards<br>
Data Lakes collect a large volume of file-based data (structured, semi-structured, and unstructured) to be analyzed<br>
Data Warehouses store data in a relational schema that is optimized for read operations - primarily, queries to support reporting and data visualizations<br>
Data Lakehouses combine the flexible and scalable storage of a data lake with the relational querying semantics of a data warehouse
