# ELK-Stack-Sleuth

 - **Using correlation IDs to link together transactions across multiple services:**
  - This involves the utilization of Spring Cloud Sleuth, which instruments incoming HTTP requests with trace IDs (correlation IDs). These IDs pass through various components to ensure a seamless link across the entire system.

- **Aggregating log data from various services into a single searchable source:**
  - The ELK stack (Elasticsearch, Logstash, and Kibana) facilitates the aggregation of log data from multiple services, providing a centralized and searchable source.

- **Visualizing the flow of a user transaction across multiple services to understand each part of the transaction’s performance characteristics:**
  - Zipkin, an open-source data visualization tool, enables the breakdown of a transaction into its component pieces. This visualization aids in identifying performance hotspots across the various services involved.

- **Analyzing, searching, and visualizing log data in real time using the ELK stack:**
  - Elasticsearch, Logstash, and Kibana (ELK stack) collectively empower the analysis, search, and real-time visualization of log data. Elasticsearch serves as a distributed analytics engine, Logstash processes and ingests data, and Kibana provides visualization tools such as charts, maps, and real-time histograms.

To accomplish this, we will use the following technologies:

- [Spring Cloud Sleuth](https://cloud.spring.io/spring-cloud-sleuth/reference/html/): The Spring Cloud Sleuth project instruments our incoming HTTP requests with trace IDs (aka correlation IDs). It does this by adding filters and interacting with other Spring components to let the generated correlation IDs pass through to all the system calls.

- [Zipkin](https://zipkin.io/): Zipkin is an open source data-visualization tool that shows the flow of a transaction across multiple services. Zipkin allows us to break a transaction down into its component pieces and visually identify where there might be performance hotspots.

- [ELK stack](https://www.elastic.co/what-is/elk-stack): The ELK stack combines three open source tools—Elasticsearch, Logstash, and Kibana—that allow us to analyze, search, and visualize logs in real time.
  - **Elasticsearch:** Elasticsearch is a distributed analytics engine for all types of data (structured and non-structured, numeric, text-based, and so on).
  - **Logstash:** Logstash is a server-side data processing pipeline that allows us to add and ingest data from multiple sources simultaneously and transform it before it is indexed in Elasticsearch.
  - **Kibana:** Kibana is the visualization and data management tool for Elasticsearch. It provides charts, maps, and real-time histograms.
