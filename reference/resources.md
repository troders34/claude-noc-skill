**Warning**: use this resources below as guideline to industries' demands not as the only main inputs for generating questions.

**Note**: this resources below are certification-based outlines using most used open-source monitoring tools. By following certification outline from them, a better guideline can be provided in generating test assessment questions.

# Zabbix
## Zabbix Certified User
URL = https://www.zabbix.com/training_user?course=Certified%20User&language=English#program

**Organizational impact outcomes**
- to understand of the Zabbix GUI and the available toolset for viewing and filtering data
- to quickly pinpoint root cause issues
- to understand the additional context information provided by Zabbix
- to track collected metrics over time in a variety of views


**Individual impact outcomes**
- to familiarize with the Zabbix GUI
- to acknowledge, react to, and understand the problems detected by Zabbix while tracking data points and system states in dashboards and maps

**Materials**
- Zabbix overview
- Zabbix user interface
- User profile
- Accessing, viewing, and filtering the collected metrics
- Zabbix inventory features
- Logical host grouping with Host groups
- Viewing and filtering detected problems
- Acknowledging, updating, and suppressing problems
- Cause and symptom problems
- Zabbix alerting feature overview
- Accessing and reading Zabbix graphs
- Displaying environment status on network maps
- Working with Zabbix dashboards and widgets
- Zabbix Application performance monitoring feature overview
- Built-in reports
- Business service monitoring and SLAs
- Zabbix mobile application overview

## Zabbix Certified Specialist
URL = https://www.zabbix.com/training_specialist?course=Certified%20Specialist&language=English#program

**Organizational impact outcomes**
- to implement optimal monitoring workflows
- to design and implement multiple monitoring strategies
- leverage the full Zabbix data collection and problem detection toolset across a wide range of monitoring endpoints

**Individual impact outcomes**
- to understand and familiarize with Zabbix features, general monitoring techniques and protocols used for collecting and analyzing various data types and endpoints from collecting OS-level metrics on servers and SNMP data on network devices to log file monitoring and performing data collection from web applications via HTTP requests

**Materials**
- Zabbix user interface
- Zabbix components and architecture
- Zabbix entities: Hosts
- Zabbix entities: Items
- Historical and trend data
- Data collection intervals
- Agentless ping and port checks
- Making metrics human-readable
- Configuring Zabbix agent passive and active checks
- Zabbix entities: Triggers
- Problem detection
- Configuration management with Templates
- Performing mass configuration updates
- Data transformation with preprocessing
- Performing aggregations and calculations with calculated items
- Bulk data collection with dependent items
- Configuring HTTP checks for web endpoint monitoring
- SNMP endpoint data collection
- Log monitoring
- Low-level discovery feature overview
- Zabbix permission management with User groups and User roles
- Host inventory configuration and management
- Configuring alerting workflows and alert delivery channels
- Defining host maintenance periods
- Built-in reporting features
- Visualization with Zabbix graphs, maps and dashboards
- Zabbix configuration import/export
- Understanding Zabbix item queue

## Zabbix Certified Professional
URL = https://www.zabbix.com/training_professional?course=Certified%20Professional&language=English

**Organizational impact outcomes**
- to scale monitoring infrastructure
- to automate monitoring workflows
- to design a monitoring solution that has automation and scalability baked-in

**Individual impact outcomes**
- to deploy and configure steps for a variety of Zabbix components including the Zabbix server, frontend, and proxies
- to understand of Zabbix low-level discovery features, automation and optimization metric discovery

**Materials**
- Installing and configuring Zabbix components
- Automating Zabbix configuration with Zabbix API
- Deploying Zabbix server in high-availability mode
- Installing and configuring Zabbix proxies
- Configuring Zabbix load balancing with Proxy groups
- Java application monitoring
- Encrypting communication between Zabbix components
- Configuring scheduled reports
- Zabbix MCP server
- Configuring, deploying, and tuning Zabbix agent
- Sending custom data with Zabbix sender
- Agentless monitoring with SSH checks
- Automated resource management with low-level discovery
- Calculated items
- VMWare monitoring
- Database monitoring
- Automated Zabbix agent host onboarding with Autoregistration
- Host discovery with Zabbix Network discovery features
- Zabbix event correlation and complex event processing features
- Application performance monitoring
- Advanced log monitoring
- Understanding Zabbix item queue

## Zabbix Certified Expert
URL = https://www.zabbix.com/training_expert?course=Certified%20Expert&language=English

**Organizational impact outcomes**
- to provide system administrators with the skills required to fully understand the underlying architecture of Zabbix components and inter-component communication
- to design and configure Zabbix environments for a variety of complex use cases, such as application performance monitoring, synthetic browser monitoring, discovery of hierarchical resources, and more

**Individual impact outcomes**
- to gain an in-depth knowledge of Zabbix from deploying, configuring, upgrading, and fine-tuning Zabbix components to designing complex data collection and analysis workflows for real-world use cases
- to implement enterprise-grade security features for Zabbix environments

**Materials**
- Upgrading Zabbix components
- Compiling Zabbix components from sources
- Tuning database backends for enterprise-grade workloads
- Tuning OS and web server backends for enterprise-grade workloads
- Implementing MFA and SAML authentication for Zabbix
- Deploying Zabbix components with Docker containers
- Configuring Elasticsearch and ClickHouse database backends for Zabbix
- Collecting OpenTelemetry data for application monitoring
- Discovering hierarchical resources with nested low-level discovery
- Zabbix inter-component communication workflows
- Zabbix database structure
- Extending Zabbix with external checks
- Zabbix JavaScript data collection and preprocessing
- Synthetic browser monitoring
- Business service monitoring features
- Zabbix troubleshooting and diagnostics tools
- Zabbix internal components
- Creating and importing custom frontend modules
- Data streaming to external systems
- Securing credentials with external vault

# Prometheus
## Prometheus Certified Associate
**URLs**

1. https://www.cncf.io/training/certification/pca/
2. https://github.com/cncf/curriculum/blob/master/PCA_Curriculum.pdf
3. https://training.linuxfoundation.org/training/monitoring-systems-and-services-with-prometheus-lfs241/

**Outcomes validation**
- Foundational knowledge of Prometheus architecture, components, and data flow
- Skills in configuring and using Prometheus to collect metrics from applications and systems via exporters and knowledge of Prometheus metric types
- Ability to query and analyze data using PromQL (Prometheus Query Language) and create  basic and advanced queries to derive actionable insights
- Understanding of how to configure alert rules and use Alertmanager to send notifications via different channels
- Knowledge of monitoring best practices and strategies for effective monitoring in environments like Kubernetes

**Material Domains**
- Observability Concepts: metrics, understanding of logs and events, tracing and spans, push vs pull, service discovery, basics of Service Level Objectives (SLOs), Service Level Agreements (SLAs), and Service Level Indicators (SLIs)
- Prometheus Fundamentals: system architecture, configuration and scraping, understanding Prometheus limitations, data models and labels, exposition format
- PromQL: selecting data, rates and derivatives, aggregating over time, aggregating over dimensions, binary operators, histograms, timestamp metrics
- Instrumentation and Exporters: client libraries, instrumentation, exporters, structuring and naming metrics
- Alerting & Dashboarding: dashboarding basics, configuring alerting rules, understand and use Alertmanager, alerting basics (when, what, why)

**Learning outline**
- introduction to observability
- introduction to Prometheus
- installing and setting up Prometheus
- basics querying
- dashboarding
- monitoring host metrics
- monitoring container metrics
- instrumenting code
- building exporters
- advanced querying
- relabeling
- service discovery
- blackbox monitoring
- pushing data
- alerting
- making Prometheus highly available
- recording rules
- scaling Prometheus deployments
- local storage
- remote storage integrations
- transitioning from and integration with other monitoring systems
- monitoring and debugging Prometheus
- Prometheus and Kubernetes
