# Dự án CNN1

## Mở Đầu

### Lý do chọn đề tài

### Mục tiêu

### Đối tượng và phạm vi nghiên cứu

### Ý nghĩa đề tài

## Giới thiệu về Công ty TNHH Hoàng Thành Capital & Partners

## Thiết kế và xây dựng Hệ Thống Cào Dữ Liệu Bất Động Sản

### Cơ sở lý thuyết

#### Web Scraping

##### What is Web Scraping?

Web scraping is an automated technique used to extract large volumes of data from websites. The data obtained through web scraping is often unstructured and in HTML format, but it can be converted into structured data, such as spreadsheets or databases, for use in various applications. There are several methods for performing web scraping, including using online services, APIs, or creating custom web scraping code.
Some websites, like Google, Twitter, and Facebook, offer APIs that provide access to their data in a structured format, making it the preferred option for data extraction. However, many other websites do not offer this capability, necessitating the use of web scraping to extract data from them.
Web scraping involves two main components: the crawler and the scraper. The crawler is an AI algorithm that navigates the web to locate the required data by following links across the internet. On the other hand, the scraper is a specialized tool designed to extract data from websites. The design of the scraper can vary significantly depending on the complexity and scope of the project, ensuring efficient and accurate data extraction.

##### How do Web Scraping works?

Web Scrapers operate by gathering specific data from websites, allowing users to extract the information they need efficiently. It is advisable to specify the desired data to ensure accurate extraction. For instance, if someone wants to scrape an Amazon page for juicer models, they may only want details about the products rather than customer reviews.

When initiating a web scraping process, the scraper first receives the URLs of the target sites. Subsequently, it retrieves the HTML code of the websites, and in more advanced cases, it may also extract CSS and Javascript elements. Afterward, the web scraper identifies and collects the necessary data from the HTML code and presents it in the format specified by the user. Typically, this output is in the form of an Excel spreadsheet or a CSV file, although other formats such as JSON are also feasible.

In summary, the process of web scraping involves the following key steps:

- Specifying the desired data for extraction
- Providing the URLs of the target websites
- Retrieving and parsing the HTML code, including CSS and Javascript elements if necessary
- Extracting and formatting the required data based on user specifications
- Generating the output in the preferred format, such as Excel, CSV, or JSON files.

#### ETL

##### What is ETL?

The process of ETL, which stands for extract, transform, load, involves integrating data by gathering, formatting, and consolidating it from various origins into a unified and coherent dataset, which is then stored in a data warehouse, data lake, or another designated system.

##### How ELT works?

![ETL](https://www.informatica.com/content/dam/informatica-com/en/images/misc/etl-process-explained-diagram.png)

- Extraction: The initial phase of the ETL process involves extracting raw data from various source locations and transferring it to a staging area. This raw data can originate from diverse sources such as SQL or NoSQL servers, CRM and ERP systems, JSON and XML formats, flat-file databases, email, and web pages.
- Transformation: Once the data is in the staging area, it undergoes a series of transformations to prepare it for analytical use. This phase includes activities such as filtering, cleansing, aggregating, de-duplicating, validating, and authenticating the data. It includes carrying out computations, translations, summarizations, and reviews to guarantee the accuracy and adherence of data.
- Loading: The final step in the ETL process is the loading phase, where the transformed data is moved from the staging area into a target data warehouse. This step typically involves the initial loading of all data, followed by periodic loading of incremental data changes, and occasionally, full refreshes to replace data in the warehouse. Organizations often automate this process, implementing well-defined, continuous, and batch-driven loading procedures. It is common for the ETL load process to occur during off-peak hours to minimize disruption to source systems and the data warehouse.

#### Apache Airflow

##### What is Apache Airflow?

Airflow is an open-source platform designed for creating, scheduling, and monitoring batch-oriented workflows. It provides an extensible Python framework that allows users to develop workflows connecting with almost any technology. The platform offers a web interface for managing workflow states and is deployable in various configurations, from a single process on a personal laptop to a distributed setup for supporting large workflows.

##### Workflows as code

![Apache Airflow Basic Flow](https://airflow.apache.org/docs/apache-airflow/stable/_images/diagram_basic_airflow_architecture.png)

One of the key features of Airflow is that all workflows are defined in Python code, which brings several benefits:

- Dynamic: Airflow pipelines are configured as Python code, enabling dynamic pipeline generation.
- Extensible: The Airflow framework includes operators to interact with a wide range of technologies, and all components are designed to be easily adaptable to different environments.
- Flexible: Workflow parameterization is built-in, leveraging the Jinja templating engine for enhanced flexibility and customization.

##### Why Apache Airflow?

Apache Airflow serves as a platform for orchestrating batch workflows. It features a wide range of operators for connecting with various technologies and can be easily extended to integrate with new technologies. Workflows with clear start and end points that run at regular intervals can be programmed as Directed Acyclic Graphs (DAGs) in Airflow.
For those who prefer coding over clicking, Airflow is an ideal tool, as workflows are defined as Python code. This allows for version control, simultaneous development by multiple team members, and the ability to write tests to validate functionality. The framework's extensible components provide the flexibility to build on existing components and create complex pipelines with rich scheduling and execution semantics. Additionally, the backfilling feature enables the re-execution of pipelines on historical data after making logic changes, while the ability to rerun partial pipelines after resolving errors maximizes efficiency.
Airflow’s user interface offers in-depth views of pipelines and tasks, providing an overview of pipeline performance over time. Users can inspect logs, manage tasks, and retry tasks in case of failure directly from the interface.
Being an open-source platform, Airflow allows users to benefit from components developed, tested, and used by companies worldwide. Engaging with the active community provides access to valuable resources such as blog posts, articles, conferences, and books, as well as opportunities to connect with peers through channels like Slack and mailing lists.
Furthermore, Airflow's high customizability as a platform allows users to extend and customize nearly every aspect of the framework through its Public Interface.

#### Docker

##### What is Docker?

Docker is a versatile software platform designed to facilitate the swift building, testing, and deployment of applications. It operates by encapsulating software into standard units known as containers, which encompass all the necessary components for the software to function, including libraries, system tools, code, and runtime. This approach ensures that applications can be easily deployed and scaled across various environments, with the assurance that the code will run as intended.

##### How does Docker work?

![Docker](https://d1.awsstatic.com/Developer%20Marketing/containers/monolith_2-VM-vs-Containers.78f841efba175556d82f64d1779eb8b725de398d.png)

Docker simplifies the process of running code by offering a consistent method for its execution. Acting as an operating system for containers, Docker operates similarly to a virtual machine by virtualizing the server's operating system. It can be installed on each server and offers straightforward commands for container building, launching, and termination.

##### Why use Docker?

Docker provides the capability to expedite code deployment, standardize application operations, facilitate seamless code migration, and optimize resource usage, leading to cost savings. With Docker, you receive a unified entity that ensures consistent execution across diverse environments. Its uncomplicated and transparent syntax empowers users with comprehensive control, while its widespread adoption fosters a robust ecosystem of tools and readily available applications compatible with Docker.
Enhanced Software Deployment Velocity: Docker users, on average, achieve a 7-fold increase in software deployment frequency compared to non-Docker users, allowing for the frequent shipment of isolated services as required.
Standardized Operational Procedures: The encapsulation of applications into small, containerized units simplifies deployment and facilitates the identification and resolution of issues, as well as rollback processes for remediation purposes.
Seamless Code Migration: Docker-based applications can be effortlessly transferred from local development environments to production deployments on AWS, ensuring consistency and reliability throughout the migration process.
Cost Optimization: Docker containers streamline the execution of larger volumes of code on individual servers, thereby enhancing resource utilization and resulting in substantial cost savings.

##### When use Docker?

Docker containers can be utilized as a fundamental element in the development of modern applications and platforms.
Docker simplifies the process of building and running distributed microservices architectures, deploying code through standardized continuous integration and delivery pipelines, creating highly-scalable data processing systems, and establishing fully-managed platforms for developers.
When it comes to microservices, Docker containers enable the construction and expansion of distributed application architectures by leveraging standardized code deployments. This approach allows for the seamless scaling of applications to meet varying demands.
In terms of continuous integration and delivery, Docker facilitates the acceleration of application delivery by standardizing environments and eliminating conflicts between language stacks and versions. This ensures a smoother and more efficient development process, ultimately enhancing the overall productivity and quality of the delivered applications.
For data processing, Docker offers the ability to provide big data processing as a service. By packaging data and analytics packages into portable containers, Docker empowers non-technical users to execute these tasks with ease, thereby democratizing access to advanced data processing capabilities.
Lastly, the concept of containers as a service involves building and shipping distributed applications with content and infrastructure that is IT-managed and secured. This approach ensures that the content and infrastructure of distributed applications are well-maintained and protected, contributing to a more robust and secure operational environment.

#### Data Warehouse

##### What is Data Warehouse?

A data warehouse is a specialized data management system designed to facilitate business intelligence activities, particularly analytics. It is primarily used for querying and analyzing large volumes of historical data sourced from various systems such as application log files and transaction applications. The main purpose of a data warehouse is to centralize and consolidate data from multiple sources, enabling organizations to derive valuable business insights and improve decision-making based on a historical record of data. In essence, a data warehouse serves as an organization's "single source of truth."
Key components of a typical data warehouse include:

- A relational database for storing and managing data
- An extraction, loading, and transformation (ELT) solution to prepare data for analysis
- Statistical analysis, reporting, and data mining capabilities
- Client analysis tools for visualizing and presenting data to business users
- Advanced analytical applications leveraging data science, artificial intelligence (AI) algorithms, graph, and spatial features for scalable data analysis
Furthermore, organizations can opt for a solution that integrates transaction processing, real-time analytics, data warehouses, data lakes, and machine learning into a single MySQL Database service, eliminating the complexities, latencies, costs, and risks associated with extract, transform, and load (ETL) duplication.

##### Benefits of a Data Warehouse

Data warehouses provide significant advantages for organizations, allowing them to analyze vast and diverse data and derive substantial value from it, while also maintaining a historical record. Computer scientist William Inmon, known as the father of the data warehouse, outlined four key characteristics that enable data warehouses to deliver these benefits:

- Subject-oriented: Data warehouses can analyze data related to specific subjects or functional areas, such as sales.
- Integrated: They establish consistency among different data types from various sources.
- Nonvolatile: Once data is in a data warehouse, it remains stable and does not change.
- Time-variant: Data warehouse analysis focuses on changes over time.

A well-designed data warehouse can execute queries rapidly, handle high data throughput, and offer the flexibility for users to analyze data in various ways, catering to different demands at both high and detailed levels. Additionally, data warehouses serve as the foundational support for middleware BI environments, providing users with reports, dashboards, and other interfaces.

##### Data Warehouse Architecture

The design of a data warehouse is tailored to fit the specific needs of the organization. There are several common architectures that are typically employed:

- Basic design: All data warehouses follow a fundamental structure where metadata, summary data, and raw data are stored within the central repository of the warehouse. Data is collected from various sources and made accessible to end users for analysis, reporting, and mining.
- Basic design with staging area: Operational data undergoes a cleaning and processing phase before being loaded into the warehouse. Many data warehouses include a staging area to simplify data preparation before it enters the central repository.
- Hub and spoke: Data marts are integrated between the central repository and end users, allowing organizations to customize their data warehouse to cater to different lines of business. Once the data is ready for use, it is moved to the relevant data mart.
- Sandboxes: These are secure, private areas that enable companies to explore new datasets or analyze data informally without adhering to the formal rules and protocols of the data warehouse. Sandboxes provide a space for quick and flexible data exploration.

## Citiations

<https://www.ibm.com/topics/etl>
<https://www.informatica.com/resources/articles/what-is-etl.html>
<https://airflow.apache.org>
<https://www.geeksforgeeks.org/what-is-web-scraping-and-how-to-use-it/>
<https://aws.amazon.com/docker/>
