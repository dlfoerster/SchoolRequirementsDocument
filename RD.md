# Requirements Document - Business Analytics Improvement Plan

### (January 30, 2024)

# Revision History

| Name   | Date       | Reason for Changes | Version |
| ------ | ---------- | ------------------ | ------- |
| Team 6 | 2024-01-30 | Initial Drafting   | 1.0     |
| Team 6 | 2024-01-31 | Continued Drafting | 1.1     |
| Team 6 | 2024-02-03 | Final Revisions    | 2.0     |

## Table of Contents

1.0 Overview

2.0 Business Requirements

&nbsp; i. Background

&nbsp; ii. Business Opportunity

&nbsp; iii. Business Objectives

&nbsp; iv. Success Metrics

&nbsp; v. Product Vision Statement

3.0 Scope and Limitations

&nbsp; i. Major Features

&nbsp; ii. Project Scope

&nbsp; iii. Limitations and Exclusions

4.0 Context Description

&nbsp; i. User Classes and Characteristics

&nbsp; ii. Operating Environment

&nbsp; iii. Design and Implementation Constraints

&nbsp; iv. Assumptions and Dependencies

&nbsp; v. Glossary of Terms

&nbsp; vi. References

5.0 System Features

&nbsp; i. System Feature 1

&nbsp; ii. System Feature 2

&nbsp; iii. System Feature 3

&nbsp; iv. System Feature 4

6.0 Data Requirements

&nbsp; i. Logical Data Model

&nbsp; ii. Data Dictionary

&nbsp; iii. Report Layout

&nbsp; iv. Data Acquisition, Integrity, Retention, and Disposal

7.0 External Interface Requirements

&nbsp; i. User Interfaces

&nbsp; ii. Hardware Interfaces

&nbsp; iii. Software Interfaces

&nbsp; iv. Communication Interfaces

8.0 Software Quality Attributes (Non-Functional Requirements)

&nbsp; i. Interoperability

&nbsp; ii. Security

&nbsp; iii. Integrity

&nbsp; iv. Usability

9.0 Analysis Models (Data Flow Diagrams)

10.0 Appendices

&nbsp; i. Appendix A - Logical Data Model

&nbsp; ii. Appendix B - Data Flow Diagrams

&nbsp; iii. Appendix C - Swimlane Diagrams

&nbsp; iv. Appendix D - Sequence Diagrams

&nbsp; v. Appendix E - Dialog Maps

&nbsp; vi. Appendix F - State Diagrams

&nbsp; vi. Appendix G - Decision Trees & Decision Tables

## 1.0 Overview

This document represents the top-level requirements and scope specification for the Business Analytics Improvement Plan, as negotiated between our team of developers and our client, Real Time Networks.

We begin by specifying the necessary background and justification for the project, then go on to state the overall requirements of the project. Following this, technical scope and further context are provided. Implementation details, success metrics, external interface requirements, and other necessary criteria conclude the document.

## 2.0 Business Requirements

### i. Background 

Real Time Networks is a small, British Columbia based enterprise that manufactures and administrates physical asset lockers, marketed to other businesses. Real Time Networks comprises numerous departments: marketing, manufacturing, accounting, and installation; and each department manages its own data footprint independently. While one department might use QuickBooks to track sales, another may be using Excel to track inventory. Decentralization of the client’s data footprint has made it difficult for their Executive Management team to make decisions, and oversee the running of their business.

The Business Analytics Improvement Plan aims to implement a centralized, real time, functionally empowered data analytics dashboard in order to better concentrate the client’s data footprint.

### ii. Business Opportunity

The client’s existing system requires interfacing with numerous applications, platforms, and other tools to assemble a complete picture of their business data footprint.

The opportunity that this project aims to leverage is that centralized and modern data gathering and visualization tools will lead to better and faster decision-making for the Executive Management team.

Specifically, the business opportunities include:

- Faster, more informed executive decision-making
- Centralized, less error-prone report generation
- Advanced business data analytics

The Business Analytics Improvement Plan aims to implement a centralized real-time data analytics dashboard to concentrate the client’s data footprint and allow for easier report generation.

### iii. Business Objectives

The main business objectives are:

- Reduce time between customer inquiry and locker installation from 90 to 60 days
- Decision making by the executive team is made easier and more informed
- Increase the total number of lockers purchased by 20%
- Achieve a 50% reduction in the Executive Management team's time spent on data analysis

### iv. Success Metrics 

The main success metrics of the project are:

- Minimize report creation time by 25%
- Achieve a 50% reduction in the Executive Management team's time spent on data analysis
- Reduce the number of systems needed to view the client’s data footprint to one

### v. Product Vision Statement

For C-Suite Executives, Managers, and Administrators, who need to make important decisions, the Business Analytics Improvement Plan is a new information system that will provide a centralized interface for compiling and visualizing company metrics. The system will automatically import data from the third-party platforms used across all departments, featuring customizability to accommodate the unique data utilization needs of each department. It enables users to create charts for data visualization, incorporates permission settings for access control, and supports manual importing for additional flexibility. Additionally, the system facilitates the exporting of detailed reports, enabling users to communicate their unique data insights. Unlike the current manual process of gathering and analyzing company metrics, our product automates these tasks so that users can focus on making informed decisions.

## 3.0 Scope and Limitations

### i. Major Features

The major features can be broken down into three main categories:

1.  **Visualized Graphical Data Interface**

    The client is asking for an easier way to visualize their data and metrics, meaning that the GUI is where a majority of their key features will fall. The data displayed on the GUI must be easily visible, understandable, and customizable.

    1.  **Customizability**

        The customizability of the visual aspects is necessary since each department will need to view and utilize different data from one another. Each user should have the ability to customize their viewport; specify which data is being shown, and arrange the layout of the data according to their preferences.

    2.  **Visualization**

        The dashboard must have the ability to display graphs, numerical data, and tables.

    3.  **Database**

        This data must be read from a secure database that contains the data imported from the third-party platforms (Hubspot, QuickBooks, etc).

    4.  **Permissions**

        Accessibility permissions must be implemented for security reasons. Administrators and the executive team have full access to everything by default. Additionally, they both have the power to assign and remove permissions as necessary from all other users. Department managers should have their own set of default permissions, giving them full access to their department’s data. All other employees that are not described by other categories must have read only access to their department’s data.

2.  **Data Importing**

    The client has a requirement to migrate data from seven external systems called the third-party platforms – namely Hubspot, QuickBooks, Excel, Access Database, Jira, TeamSupport, and ServiceNow – to the new centralized system.

    1. **Manual Importing**

       The system must facilitate manual data imports, enabling users to upload files into the new platform and its associated database.

    2. **Automatic Importing**

       The system must have the capability to autonomously extract and import data from the existing third-party platforms into the new system and its associated database.

    3. **Data Synchronization**

       Additionally, the system should have automated capabilities to synchronize, connect with, and extract the requisite information from the existing third-party platforms.

    4. **Formatting**

       The pipeline is necessary to filter, validate, clean up, normalize, and format imported data into a usable format. Ultimately, the imported data will be stored in a centralized database for subsequent utilization.

3.  **Data Exporting**

    The system must support exporting data that is displayed on the dashboard. This export feature includes downloading graphs, tables, charts and numerical statistics presented on the dashboard to generate formal reports.

    1. **Individual Data Export**

       The system must support the ability to export an individual graph, table, chart, or numerical statistic in a photo, CSV, or Excel format.

    2. **Custom Report Export**

       The system must support the ability to export multiple graphs, tables, charts, or numerical statistics in a PDF file with a custom title.

       1. **Templates**
          The sytem must support the ability to save the selected graphs, tables, charts, or numerical statistics that are included in order to recreate the same report on a regular basis and look at the same metrics over time.

4.  **Permissions**

    Accessibility permissions must be implemented for security reasons. Each Administrator and C-Suite Executive have full access to everything by default. Additionally, they both have the power to assign and remove permissions as necessary from all other users excluding themselves. Each Manager should have their own set of default permissions, giving them full access to their department’s data.

### ii. Project Scope

The proposed system is a web-based application to centralize company metrics and streamline the processing of data research. It will integrate data from the third-party platforms including Hubspot, QuickBooks, Excel, Access Database, Jira, TeamSupport, and ServiceNow. The primary purpose of this system is to empower C-suite executives, managers, and administrators to make faster, more informed decisions. The additional benefit of identifying bottlenecks and inefficiencies by viewing these metrics will help enhance the overall business efficiency, which aligns with their goal of accelerating the marketing-to-sale pipeline.

### iii. Limitations and Exclusions

The system will not include advanced AI analysis to interpret data. It will still include graphs with trend lines and the ability to create charts, but no AI tools or other methods of interpreting data will be possible. The system is purely meant to visualize data in a centralized dashboard, not to perform advanced analysis on its own. That may be included in some future iteration if it is deemed high priority.

## 4.0 Context Description

### i. User Classes and Characteristics

Three distinct user classes will interact with the product, which are summarized in Table 1 below.

<br />

Table 1: User classes for Business Analytics Improvement Plan

| Name               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| C-Suite Executives | The client’s highest authority – the Executive Management team as it might be stated. This user class is responsible for the client company’s overall direction: which investments to make, which products to research, and other key decisions. This user class is also responsible for the running of the client company’s day-to-day operations, albeit from a macro perspective. They are most likely to use the product before important meetings involving decisions about company or department direction.<br><br> <br><br>These users will consume the system in two ways. Firstly, these users will consume reports provided to them by administrators to make decisions on behalf of the company. Here, the importance of accurate and current data is key. Secondly, these users will employ the system’s real-time visualization tools to direct day-to-day operations and stay abreast of the state of the company. This class of users will likely have moderate technical skills and a positive attitude towards the project’s goals. These users will have total access to all views and all data as well as the ability to modify user permissions and context views. |
| Managers           | This user class is made up of department heads of key operations. These users are essentially middle management and are in charge of day-to-day operations from an on-the-ground perspective. These users will make use of real-time visualization tools to stay abreast of the state of their operations. These users are unlikely to make use of formal reports, though they may employ them from time to time.<br><br> <br><br>These users should have access only to their own department’s data. Each department should be given its own context view and suite of visualizations to suit their needs. Each manager views the dashboard around once a day to reference the overall status of their department in their meetings. This set of users is a lower priority as they can already see the data related to their departments.                                                                                                                                                                                                                                                                         |
| Administrators     | Not technically a position so much as a role that any of the client’s employees might take on. Administrators are those entrusted by the client to maintain their data footprint. Their duties include the assembly of reports for use by the executive team, manual data entry, and maintenance of permission and context views.<br><br> <br><br>These users will make use of all the system’s features, from report generation to advanced data visualization, and from manual data entry to maintenance of permissions and context views. They will interact with the system regularly and have a wide range of technical abilities.                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |

### ii. Operating Environment

The system will be restricted to a web-based application that supports consistent behavior across all major browsers, as well as support for mobile devices, including Microsoft Edge, Google Chrome, Safari, and Firefox. As such, responsive design will be required. On the back end, a server will facilitate communication between users on the front end and the system’s core software.

### iii. Design and Implementation Constraints

The system is a data aggregation tool that takes in existing data from other systems and therefore must be able to automatically retrieve data and also support manually importing data from the following third-party platforms:

- QuickBooks
- Hubspot
- Excel
- Access Database
- Jira
- TeamSupport
- ServiceNow

The following is a list of constraints the system must meet in order for the project to be considered an acceptable solution:

1.  **Solution Delivery**

    The client requires the initial project delivery within six months from the elicitation date. Additional time is allowed for subsequent feature deliveries in later iterations. Additionally, the system input format must be easily modifiable to account for format changes from the third-party platforms mentioned above.

2.  **Communication**

    The client is familiar with software utilizing REST API communication. They specifically request the adoption of REST API methodology for network communication among services. The system must perform real time data updates and retrievals. The application must also support instantaneous updates to a central database whenever a user imports new data manually.

3.  **Development Approach**

    The client needs to centralize all of the data being gathered into one reliable system. This system must be a real-time web-based application. Further, the primary development language must be an objective-oriented programming language.

4.  **Budget**

    The system is requested to remain within the proposed budget of $100,000 as stated in the client’s RFP [1].

5.  **Language Support**

    The company primarily operates in Canada. The client needs the system to support two official languages including English and French.

### iv. Assumptions and Dependencies

Assumptions and dependencies made by the development team that are likely to affect requirements include:

- The company uses the latest versions of third-party platforms to maintain consistent import formats. It is easier to maintain the correct import format if we always follow the new standard export
- All browsers will remain updated. This may affect how the application is running
- Users must update the data manually if data cannot be retrieved from an application via the REST API. Should this not be followed, the data will quickly become out of date
- Current third-party platforms will always support a CSV or Excel export
- All currently used third-party platforms support an interface to have their data automatically retrieved
- Export formats from source software will be standard

### v. Glossary of Terms

| Term                                                                         | Definition                                                                                                                                                                             |
| ---------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Real Time Networks                                                           | A company that manufactures software-driven lockers for physical assets.                                                                                                               |
| CSV (Comma-Separated Values)                                                 | A file format used to store tabular data, where each line of the file represents a row in the table, and commas are used to separate individual values within each row.                |
| The client                                                                   | The entity commissioning the project as a whole, which is Real Time Networks.                                                                                                          |
| GUI (Graphical User Interface)                                               | A type of user interface that allows users to interact with electronic devices through graphical icons and visual indicators.                                                          |
| REST API (Representational State Transfer Application Programming Interface) | A set of rules and standards used for building and interacting with web services, allowing different computer systems to communicate over the internet using stateless operations [2]. |
| AI (Artificial Intelligence)                                                 | A field within computer science focused on studying systems capable of performing tasks that normally require human intelligence.                                                      |
| Database                                                                     | A structured collection of data that software applications use for efficient storage, retrieval, and management of information.                                                        |
| Administrator                                                                | Those employed by the client to maintain their data footprint and its integrity as well as the system itself.                                                                          |
| Executive Management                                                         | Those employed by the client to make business altering decisions, as well as to oversee the running of the company.                                                                    |
| The system                                                                   | The end result of the development process, the actual software being developed, and the software that users will actually use.                                                         |
| Web-Based Application                                                        | A software application that is accessed and used through a web browser over the internet network [3].                                                                                  |
| The Third-Party Platforms                                                    | The websites as specified by the client in section 3 of their RFP, namely, Hubspot, QuickBooks, Excel, Access Database, Jira, TeamSupport, and ServiceNow.                             |

### vi. References

[1] Team 2, “Business Analytics Improvement Request for Proposal,” (accessed Jan. 30, 2024).

[2] L. Gupta, “What is REST?,” REST API Tutorial, https://restfulapi.net (accessed Feb. 2, 2024).

[3] M. Rouse, “Web-Based Application,” Techopedia, “https://www.techopedia.com/definition/26002/web-based-application” (accessed Feb. 2, 2024).

## 5.0 System Features

![](https://lh7-us.googleusercontent.com/4vwSqBKneEkexQaXPPsOKMl3SiaiEJ1uqN79ouoyDokncmzqi93VcwTSXKk0SpStrofunsD0w6Ed0ef3NlsJpMwF8mSo086Ewl3a0_EDs_2exddT404DJtuL06SWdGbucFqSLRoyA_vbdU3IDhz4I9Q)

### i. System Feature 1

Visualized Graphical Data Interface

1. **Description and Priority**

   Priority Level [High]

   Each C-suite Executive, Manager, and Administrator must be able to view and customize data relevant to their position within the company.

2. **Functional Requirements**

   1. **REQ-1**
      Each user must have access to company data tailored to their permissions, ensuring that they only view information within the bounds of their authorized access levels.

      1. **Error Conditions / Invalid Inputs**

      - Missing data fields when attempting to generate a plot

      - Overlapping data displays

      - Data field is too narrow to display value in full

      2. **Backward Traceability**
         Defined within the Requirements Document Major Features section under “Visualized Graphical Data Interface”.

      3. **Forward Traceability**
         Each user who uses the system can view data relevant to them.
      4. **Acceptance test 1**
          Given a user is a Manager, when the user logs in to the system, then they can only view their department's data by default
      5. **Acceptance test 2**
         Given a user is a C-Suite Executive or an Administrator, when they log in to the system, then they can view all department's data and access the modify permissions page.
      6. **Acceptance test 3**
          Given a user is a Manager and has been given extra viewing permissions, when they log in to the system, then they can view their own department's data as well as the data corresponding to their added viewing permissions

   3. **REQ-2**
      The graphical user interface must allow for customizable data displays allowing users to select which infographics and statistics to be displayed.
      
      1. **Error Conditions / Invalid Inputs**

      - The user tries to customize data but has no data visible to them.

      2. **Backward Traceability** 
         Defined within the Requirements Document Major Features section under “Visualized Graphical Data Interface”.

      3. **Forward Traceability**
         Each user who uses the system can customize the dashboard to suit their preferences.

   5. **Use cases associated with the feature or functional requirement**

| User Story                                                                                                                                                                                                                       | Acceptance Criteria & Test                                                                                                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| As a C-Suite Executive, I want to be able to view any department’s data so that I can more easily make business decisions and manage day to day operations.                                                                           | Given a C-suite Executive has access to the data visualization tool, when the C-suite Executive tries to view data, then the relevant data is displayed.                                                            |
| As a Manager, I want to be able to view the data for my department, so that I can identify bottlenecks and inefficiencies in our day-to-day operations.                                                                          | Given that a Manager has access to the data visualization tool, when the Manager tries to view the data for their department, then the data is displayed on the dashboard.  |
| As any user class, I want to be able to customize what and how I view my data through widgets of graphs, charts and relevant numerical data, so that I can identify bottlenecks and inefficiencies in our day-to-day operations. | Given that a user can view data and has access to the data visualization tool, when they select a widget, then a pop-up window displays a wizard with a prompt to select data fields.                               |

### ii. System Feature 2

Import Data

1. **Description and Priority**

   Priority Level [High]

   The system must import the data from each website as specified by the client in section 3 of their RFP, namely, Hubspot, QuickBooks, Excel, Access Database, Jira, TeamSupport, and ServiceNow, via the REST API (The third-party platforms).

   Each user class must be able to manually import data into the system.

2. **Functional Requirements**

   1. **REQ-3**
      Each user class must be able to import data to a location for which they have permission to view.

      1. **Error Conditions / Invalid Inputs**

      - If the [Administrator, C-Suite Executive, Manager] tries to upload a file not supported by the system, then an error message must be displayed.

      2. **Backward Traceability**
         Defined within the Requirements Document Major Features section under “Manual Importing”.

      3. **Forward Traceability**
         [Administrator, C-Suite Executive, or Manager] imports the data directly from their dashboard and is then able to view it on the system. Each other user with permission to access the imported data can also now view the imported data on their dashboard.
      4. **Acceptance test 4**
          Given that the user class has permission to view some dashboard, when the user imports a file, then the data will be visible on the system.

   2. **REQ-4**
      When one of the third-party platforms is updated with new data, the system shall import the data to the system's database.

      1. **Error Conditions / Invalid Inputs**

      - If information is unable to be automatically imported from the third party system, then an error message is displayed to the user.

      2. **Backward Traceability** 
         Defined within the Requirements Document Major Features section, under “Automatic Importing”.

      3. **Forward Traceability**
         One of the several third-party platforms is updated, and the updates are displayed on each member's dashboard with access to that data.
      4. **Acceptance test 5**
          Given that a user has permission to view the data, when a third-party platform is updated with new data, then the updates are displayed onto the user's dashboard.

   3. **Use cases associated with the feature or functional requirement**

| ID and Name       | UC-2 Import Data                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Primary Actor     | C-suite Executives, Administrators, Managers                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Secondary Actor   |   None                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Description       | The requester informs the system that he/she would like to update information in the system’s database and dashboard (through a method TBD by the designer). The system autonomously imports data by fetching data from third-party platforms to update its database and dashboard. Otherwise, the C-suite Executive, Administrator, or Manager updates information in the system’s database and dashboard by uploading a file to the system.    <br><br> <br><br>A C-suite Executive, Administrator, or Manager updates information in the system database and dashboard by uploading a file to the system. If the system accepts the file, the system must make this file available in the database, and display a new set of information on the dashboard of each user who has permission to view the file. Otherwise, the system rejects the uploaded file and displays an error message until the user acknowledges the message. |
| Trigger           | A data update request arises.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Preconditions     | PRE-1: The third-party platforms synchronize and link with the system or a C-suite Executive, Administrator, or Manager has a file to upload into the system.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Postconditions    | POST-1: Data in the system’s database updates based on uploaded data.<br><br> <br><br>POST-2: The dashboard reflects updated data.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Normal Flow       | 2.0 Import data autonomously to the system<br><br> <br><br>1. The third-party platforms send an update signal to the system.<br> <br>2. The system receives the update signal<br> <br>3. The system fetches the updated data from the third-party platform.<br> <br>4. The system validates and formats the updated data.<br> <br>5. The system stores and updates the database record with the updated data.<br> <br>6. The system applies the changes in the database to the dashboard reflecting the updates.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Alternative Flows | 2.1 Import data manually to the system<br><br> <br><br>1. A C-Suite Executive, Administrator, or Manager authenticates the permission to access the system. <br> <br>2. User uploads the selected file to the system.<br> <br>3. The system accepts the format of the updated data.<br> <br>4. The system stores and updates the database record with the updated data.<br> <br>5. The system applies the changes in the database to each dashboard of each user affected by the update. <br> <br>6. The system displays a confirmation message on the dashboard of the user who had imported the data.<br> <br>7. The confirmation message remains there until the user acknowledges it.                                                                                                                                                                                                                                             |
| Exceptions        | 2.1.E1 The uploaded data contains errors or invalid<br><br>1. The system displays an error message: ERROR - Fail to import data [reason] until the user acknowledges the message.<br> <br>2. After being acknowledged, the system then displays a message asking the uploader if he/she wants to request another upload (3a) or to exit (4a).<br> <br><be> 3a. The uploader asks to request another upload.<br> <br> 3b. The system starts an alternative flow over<br> <br> 4a. The uploader asks to exit.<br> <br> 4b. The system terminates this use case.                                                                                                                                                                                                                                                                                                                                                                         |
| Priority          | High                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Frequency of Use  | Every time one of the third-party platforms updates its data. The system must allow any number of imports per day.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Business Rules    | 1. C-Suite Executives, Administrators, and Managers have full access to this data import feature.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Assumptions       | 1. The system is available and has access to the internet throughout the process.<br> <br>2. The data imported from third-party platforms is assumed to be error-free and valid.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |

### iii. System Feature 3

Data Exporting

1. **Description and Priority**

Priority Level [Medium]

Administrators must have the ability to export data displayed through infographics and statistics in the form of a report or individual file. This generator will allow Administrators to choose which specific tables, statistics, charts, or graphs will be included. Administrators must also have the ability to create custom report templates that can be used to automatically populate a report.

2. **Functional Requirements**

   1. **REQ-5**
      Each Administrator must be able to download both raw and visualized data (graph, numerical statistics, charts) relevant to their position through the system.

      1. **Error Conditions / Invalid Inputs**

      - If a user tries to download any infographic or statistic that is currently unavailable due to missing or insufficient data, then an error message should be displayed indicating that there is missing or insufficient data for the specific infographic or statistic.

      2. **Backward Traceability**
         Defined within Requirements Document Major Features section

      3. **Forward Traceability**
         Administrator downloads infographic or statistic through the system and the download appears on the Administrator’s device
      4. **Acceptance test 6**
          Given that the administrator has selected at least one infographic or statistic, when they click the download button, then a local file is downloaded to their device.

   2. **REQ-6**
      Each Administrator must be able to create custom template reports of their desired infographic and statistics which can be used to generate reports based on the template.

      1. **Error Conditions / Invalid Inputs**

      - If a user tries to create a template with the same name as another created template, an error message must be displayed to the user. If a user tries to generate a report using a custom template and an infographic or statistic in the template is unable to be shown, an error message must be displayed to the user.

      2. **Backward Traceability** 
         Defined within Requirements Document Major Features section.

      3. **Forward Traceability**
         Administrator creates a custom report template and is able to see this custom report template when trying to generate a report.

   3. **Use cases associated with the feature or functional requirement**

| User Story                                                                                                                                                                                                                          | Acceptance Criteria & Test                                                                                                                                                                                                                                                             |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| As an Administrator, I want to be able to download grouped data infographics and statistics in the form of graphs, numerical stats and charts in the form of a report to provide key departmental information to C-Suite Executives | Given an Administrator wants to generate a report when the Administrator generates a report and selects their desired infographics and statistics to be displayed with a title, then a PDF is generated with the selected infographics and statistics with the custom title.           |
| As an Administrator, I want to be able to download individual data infographics and statistics in the form of graphs, numerical stats and charts to provide key departmental information to C-Suite Executives.                     | Given an Administrator wants to download an individual infographic or statistic from the system, when the Administrator clicks download on the selected infographic or statistic, then the selected infographic or statistic is exported in either an image, CSV or Excel file format. |

### iv. System Feature 4

Manage Permissions

1.  **Description and Priority**

    Priority Level [High]

    Accessibility permissions must be implemented for security reasons. Each Administrator and C-Suite Executive have full access to everything by default. Additionally, they both have the power to assign and remove permissions as necessary from all other users excluding themselves. Each Manager should have their own set of default permissions, giving them full access to their department’s data.

    This feature is of high priority because without accurately managed permissions, the core usability and security of the system are compromised.

2.  **Functional Requirements**

    1.  **REQ-7**
        Each Administrator and C-Suite Executive must be able to manage permissions for every user and department.

        1. **Error Conditions / Invalid Inputs**

        - None

        2. **Backward Traceability**
           Second client meeting; notes in GitHub wiki.

        3. **Forward Traceability**
           Administrator or C-Suite Executive views a list of all departments and users in the system, then confirms its accuracy. Upon selecting a department or specific user, the Administrator or C-Suite Executive observes a list of enabled/disabled permissions and makes a change. An affected user confirms either gain or loss of access to that data element.
        4. **Acceptance test 7**
           Given that a user is an Administrator or C-Suite Executive, and they are viewing the permissions for a user, when they enable or disable a permission, then the systems displays a notification to indicate that it was successful, and the affected user recieves a notification about their change in permissions.
        4. **Acceptance test 8**
           Given that a user is an Administrator or C-Suite Executive, and they are viewing the permissions for a department, when they enable or disable a permission, then the systems displays a notification to indicate that it was successful, and all users in the affected department recieve a notification about their change in permissions.

    2.  **REQ-8**
        Each Administrator and C-Suite Executive must be able to add, delete, and merge departments.

        1. **Error Conditions / Invalid Inputs**

        - If a user tries to add a new department and department name is already in use, the system prompts the user to specify a different name.

        2. **Backward Traceability** 
           Outlined by the client team that these user classes should have the ability to manage permissions of all users which includes creation and deletion of departments.

        3. **Forward Traceability**
           Administrator or C-Suite Executive adds, deletes, or merges departments, then confirms the change was successful by viewing the updated list of departments in the system.
        4. **Acceptance test 9**
            Given that a user is an Administrator or C-Suite Executive, when the user selects either add, delete, or merge departments, then a success message will be displayed and all changes will be reflected in the system and to the user.
    3.  **REQ-9**
        If permissions are modified for a user or department, the system must notify all affected users and store the changes in an audit log.

        1. **Error Conditions / Invalid Inputs**

        - None

        2. **Backward Traceability** 
           Defined by our team in the process of actualizing this feature; never explicitly stated by client.

        3. **Forward Traceability**
           Administrator or C-Suite Executive modifies permissions for a department or individual user, then they check the audit log to see the record of the change. A user whose permissions were affected, logs in to the system and observes a notification informing them of a change to their permissions.
        4. **Acceptance test 10**
           Given that an Administrator or C-Suite Executive is viewing the permissions for a user or department, when they modify a permission, then the affected users recieve a notification, and the change is stored in the audit log.

    4.  **Use cases associated with the feature or functional requirement**

| ID and Name       | UC-4 Manage Permissions                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Primary Actor     | Administrator, C-Suite Executive                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Secondary Actor   | Manager                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Description       | Administrators and C-Suite Executives manage permissions by adding or removing permissions either at a departmental or individual user level. They can also manage organizational structure by adding, deleting, or merging departments.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Trigger           | A change in user or department responsibilities requires an update of permissions, or a new data category is introduced to the dashboard.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Preconditions     | PRE-1: Administrator or C-Suite Executive is logged into the system. <br>PRE-2: The user permission database is online and accessible.<br><br>PRE-3: System displays an up-to-date view of the permission settings for each user.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Postconditions    | POST-1: System accurately reflects the updated permissions for each user class. <br>POST-2: Affected users receive a notification of permission changes. <br>POST-3: Audit log records the changes made to permissions.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Normal Flow       | 4.0 Add or remove permissions<br><br>1. Administrator or C-Suite Executive navigates to permissions management section.<br> <br>2. Administrator or C-Suite Executive selects a user or department to manage permissions for, or adds a new department (see 4.1, 4.2, 4.3).<br> <br>3. Administrator or C-Suite Executive selects or deselects available permissions for the chosen user or department.<br> <br>4. System updates permission settings.<br> <br>5. System confirms changes to the Administrator or C-Suite Executive.<br> <br>6. System notifies affected users of permission changes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Alternative Flows | 4.1 Add a new department to the system<br><br>1. Administrator or C-Suite Executive navigates to the department creation page.<br> <br>2. System prompts the Administrator or C-Suite Executive for new department details, such as the name, assigned users, and default viewing/exporting permissions.<br> <br>3. Administrator or C-Suite Executive enters details and confirms creation of the new department (see 4.1.E1).<br> <br>4. System confirms changes to the Administrator or C-Suite Executive.<br> <br><br> <br><br>4.2 Remove an existing department<br><br>1. Administrator or C-Suite Executive navigates to the deletion section within the department management page.<br> <br><br>1. Administrator or C-Suite Executive selects the department to delete.<br> <br>2. System deletes the department and leaves all members of the department with their current permissions.<br> <br>3. System confirms changes to the Administrator or C-Suite Executive.<br> <br><br> <br><br>4.3 Merge two departments<br><br>1. Administrator or C-Suite Executive navigates to the merge section within the department management page.<br> <br>2. Administrator or C-Suite Executive chooses a second department to merge the selected department with.<br> <br>3. System combines permission settings and asks for a new department name.<br> <br>4. Administrator or C-Suite Executive inputs a new department name for the merged departments.<br> <br>5. System confirms changes to the Administrator or C-Suite Executive. |
| Exceptions        | 4.1.E1 Department name is already used<br><br>1. System displays message: Entered department name is already in use.<br> <br>2. System prompts the Administrator or C-Suite Executive to input a different department name (3a) or exit (4a).<br> <br>3. a) Administrator or C-Suite Executive chooses to input a different department name.<br> <br><br>           b) Return to alternative flow.<br><br>4. a) Administrator or C-Suite Executive chooses to exit department creation.<br> <br><br>           b) System terminates use case.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Priority          | High                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Frequency of Use  | Varies depending on addition of new data fields and organizational changes, but likely low.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Business Rules    | 1. Permissions are managed at the departmental or individual user level.<br><br>2. Administrators and C-Suite Executives have full access, while Managers have restricted access based on operations within their department.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Assumptions       | 1. Departments are distinct and well-defined.<br><br>2. System handles changes to permissions without disrupting user access.<br><br>3. Administrators and C-Suite Executives have full access and the ability to modify permissions.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |

## 6.0 Data Requirements

### i. Logical Data Model

1. **Entity-Relationship Diagram**

Refer to Appendix A figure 1.

2. **UML Class Diagram**

Refer to Appendix A figure 2.

### ii. Data Dictionary

| Data Element  | Description                                                                             | Composition or Data Type                                                             | Values                                                 |
| ------------- | --------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ | ------------------------------------------------------ |
| User Account  | One of the user classes creates an account on the system.                               | User ID and Password<br><br>- Verification code<br> <br>- Account recovery questions | Integers, letters                                      |
| Exported Data | Files or reports downloaded by an admin.                                                | File<br><br>- File identifier<br> <br>- File type                                    | Title, file type (for example, .csv, .pdf, .xsls, etc) |
| Imported Data | Either files uploaded by a user class or data imported from the database by the system. | File<br><br>- File identifier<br> <br>- File type                                    | Title, file type (for example, .csv, .pdf, .xsls, etc) |
| Permission    |                                                                                         |                                                                                      | Boolean                                                |
| User Role     | Role of a user to assign permissions.                                                   | Enumerator with 4 String options (Administrator, C-Suite Executive, Manager)         |                                                        |

### iii. Report Layout

In the first release, the system must have the capability of generating a simple report from each department dashboard containing statistical and numerical information, graphs, charts, and tables with a custom title. The department dashboards generate exhibits using data sourced from databases imported from third-party platforms.

The requirement specification is to bring all the virtual information from the web application to a PDF file. The design of the report is minimal and straightforward. The report must be customizable with the option of accommodating charts, graphs, numerical statistics, and tables along with a custom report title.

The report must contain these attributes if applicable:

- Date/Time
- Numeric Values in quantities and percentages
- Categorical Variables including titles, categories, and departments
- Textual descriptions
- Virtualization aids including charts and graphs
- Basic statistic values including mean, median, and mode

Example report entities:

- QuickBooks (Bookkeeping and Financial Statements) - Total Revenue, Net Profit, Operating Expenses Breakdown, Gross Profit Margins.
- Excel and Access Database (Inventory and Manufacturing) - Inventory Turnover Ratio, Manufacturing Process Time, and Production Lead Times.
- Jira and TeamSupport (Delivery and Installation Monitoring) - Project Completion Times, Delivery Status, and Installation Status.

### iv. Data Acquisition, Integrity, Retention, and Disposal

Data integrity is a critical specification emphasized by the client. The system must include a set of protocols to guarantee data integrity. These protocols must apply to all system activities, including data import, data virtualization, permission management, and data export processes.

The system must prioritize acquisition, retention, and disposal by validating incoming data and accepting files and data that are valid and error-free. Moreover, the system must accurately store imported data and precisely display data from the database without any data loss and distortion to the content. Upon any additions or deletions, the system must accurately add or dispose of data in the database and consistently update the dashboard to reflect the changes.

The system must ensure data integrity by implementing an authentication protocol allowing only authorized individuals to access, add, delete, and modify data. Administrators and C-Suites Executives must hold the authority to manage permissions for an authorized group. The permission levels must remain unchanged unless initiated by an Administrator.

## 7.0 External Interface Requirements

### i. User Interfaces

- The Administrators and C-Suite user class must have additional UI buttons and functions for user management. The user management should include a table listing all user profiles under an organization and buttons to perform CRUD actions on the user profiles. Additionally, The Administrator and C-Suite Executive user class must be able to view data from all departments, so an interactable filter must be located on the dashboard for the Administrator and C-Suite Executive user class.
- The Administrators must have additional UI buttons and menus for downloading data, creating report templates, and generating a report.
- The screen layout must be dynamic to support different screen sizes. A dynamic screen layout must include screen layout adjusting on web window resizing.
- Error popups must be displayed when an error from calling an API occurs. The error popup must attract the user’s attention and take up at least 15% of the user device’s screen.
- Each user must have a UI dashboard where they can see charts and statistics of data relevant to their permissions. A refresh button must be present on the dashboard to present new data retrieved from the database.
- Each user must have the ability to customize their dashboard from a selection of provided infographics and statistics
- The user will communicate with the system through UI components that call API endpoints.

### ii. Hardware Interfaces

Supported device types include devices with access to a web browser, but laptops and personal computers are the primary devices. Overall, this system does not have any other hardware interfaces as it is exclusively web-based. One assumption is that the system will leverage cloud infrastructure instead of relying on local physical servers. This choice is made to capitalize on the scalability and resource advantages offered by cloud computing options.

### iii. Software Interfaces

Data from the following software components is retrieved through API endpoints from outgoing requests from the system and stored in a database.

- Hubspot
- QuickBooks
- Excel
- Access Database
- Jira
- TeamSupport
- ServiceNow

Messages going into the system will consist of API requests to retrieve data stored in the system database housing all dashboard data. Data output from the system will be used to fill statistical charts and reports.

### iv. Communication Interfaces

- Communication between software components is conducted through HTTPS for the benefit of security, reliability, and industry standards.
- RESTful API interfaces are required for software components to have standardized and predictable means of communication with each other.
- A user must access the system through the web.

## 8.0 Software Quality Attributes (Non-Functional Requirements)

During the elicitation, the client communicated a set of software quality attributes both explicitly and implicitly. These following quality attributes are essential in ensuring that the system meets the desired standards and fulfills the business’s and user’s requirements.

### i. Interoperability 

REL-1: The system must retain the capability for real-time updates and synchronization with changes from the third-party platforms.

REL-2:  The system must provide an alternative method for manually updating data from third-party platforms through file upload.

### ii. Security

SEC-1: The system must protect against unauthorized access, addition, deletion, or modification of data.

SEC-2: The system must uphold the privilege level of each user unless an authorized individual initiates changes.

SEC-3: The system must grant control over permissions to an authorized group of individuals.

### iii. Integrity

INT-1: The system must reject uploaded files that are invalid or not error-free.

INT-2: The system must ensure precise and reliable updating of data in the database preserving the integrity of the original content imported into the system.

INT-3: The system must present real time data retrieved from the connected database on the dashboard.

### iv. Usability 

USE-1: The system must offer customizability allowing for the addition, deletion, and modification of information and graphical data interface in the virtualization dashboard.

USE-2: The system must facilitate the effortless summarization and generation of information reports in a single interaction.

USE-3: The system must facilitate an effortless and autonomous method for importing data from third-party platforms into the system's database and dashboard.

USE-4: The system must present clear textual and numerical data accompanied by visualization through graphs and charts

## 9.0 Analysis Models (Data Flow Diagrams)
### i. Data Flow Diagrams
See Appendix B:
- Figure 1: Data Flow Diagram Level 0
- Figure 2: Data Flow Diagram Level 1
- Figure 3: Data Flow Diagram Level 2 - Import
- Figure 4: Data Flow Diagram Level 2 - Manage Permissions

### ii. Swimlane Diagrams
See Appendix C:
- Figure 1 : Swimlane Diagram - Manage Permissions
- Figure 2 : Swimlane Diagram - Import

### iii. Sequence Diagrams
See Appendix D:
- Figure 1 : Sequence Diagram - Import
- Figure 2 : Sequence Digram - Manage Permissions


### iv. Dialog Maps
See Appendix E:
- Figure 1 : Dialog Map - Export
- Figure 2 : Dialog Map - Manage Permissions

### v. State Diagrams
See Appendix F:
- Figure 1 : State Diagram - Import
- Figure 2 : State Diagram - Export

### vi. Decision Trees & Decision Tables
See Appendix G:
- Figure 1 : Decision Tree & Decision Table - Import
- Figure 2 : Decision Tree & Decision Table - Export

### vii. Story Boards
See Appendix H:
- Figure 1 : Administrator/C-Suite Executive Story Boards
- Figure 2 : Department Manager Story Boards

### viii. Story Boards (Final)
See Appendix I:
- Figure 1: Finalized Storyboards


## 10.0 Appendices

### i. Appendix A - Logical Data Models

Figure 1: ERD diagram of the system.
![](https://lh7-us.googleusercontent.com/5dLSbCn_VWu3KEJN2Sz0qfnJTEoU9PQjRCs75eRFCZ5i28Y8c6jM1xJeJeZWJGciWpKVPlZOqrW1py39UbnKqMzFbW9L5P6vTzmRgaonxmuQby-g4mUrIRFF5j22Rq-trIVPTJcNleVPkNwy2_MzXFo)

In this Entity-Relationship Diagram (ERD), an arrow pointing away from an entity signifies that the entity is a key participant in the associated action. An arrow pointing away from an action towards an entity corresponds to the action creating or having some effect on the specified entity. This implementation allows a deeper understanding of the diagram.

Figure 2: UML class diagram of the system.
![](https://lh7-us.googleusercontent.com/wm8Dv5I7GgxrDFsrs4X1Ip5y2qPkRV_70vvOQ8JB1GRrYtS0L62PdJpcC-Hqo5pTVoRv4XFeGbSHAS7mbPnVtQlopd2c9sFi825xuGU6nlbPpqV3NglajkZ7GSCs06361Fp_D7vPNke1zzh1IrhtWXU)

### ii. Appendix B - Data Flow Diagrams

Figure 1 : Data Flow Diagram Level 0
![](/Wiki/Diagrams/data_flow_diagrams/dfd_level0.jpg)

In this data flow diagram, "Third-Party Platforms" refers to Hubspot, QuickBooks, Excel, Access Database, Jira, TeamSupport, and ServiceNow that the client uses to manage their deparment data.

Figure 2 : Data Flow Diagram Level 1
![](/Wiki/Diagrams/data_flow_diagrams/dfd_level1.jpg)

Figure 3 : Data Flow Diagram Level 2 - Import
![](/Wiki/Diagrams/data_flow_diagrams/dfd_level2_import.jpg)

Figure 4 : Data Flow Diagram Level 2 - Manage Permissions
![](/Wiki/Diagrams/data_flow_diagrams/dfd_level2_permissions.jpg)

### iii. Appendix C - Swimlane Diagrams

Figure 1 : Swimlane Diagram - Manage Permissions
![](/Wiki/Diagrams/data_flow_diagrams/swim_lane_permissions.jpg)

Figure 2 : Swimlane Diagram - Import
![](/Wiki/Diagrams/data_flow_diagrams/swimlane_import.jpg)

### iv. Appendix D - Sequence Diagrams

Figure 1 : Sequence Diagram - Import
![](/Wiki/Diagrams/data_flow_diagrams/sequence_import.jpg)

Figure 2 : Sequence Digram - Manage Permissions
![](/Wiki/Diagrams/data_flow_diagrams/sequence_permissions.jpg)

### v. Appendix E - Dialog Maps

Figure 1 : Dialog Map - Export
![](/Wiki/Diagrams/data_flow_diagrams/dialog_map_export.jpg)

Figure 2 : Dialog Map - Manage Permissions
![](/Wiki/Diagrams/data_flow_diagrams/dialog_map_permissions.jpg)

### vi. Appendix F - State Diagrams

Figure 1 : State Diagram - Import
![](/Wiki/Diagrams/data_flow_diagrams/state_export.jpg)

Figure 2 : State Diagram - Export
![](/Wiki/Diagrams/data_flow_diagrams/state_import.jpg)


### vii. Appendix G - Decision Trees & Decision Tables

Figure 1 : Decision Tree & Decision Table - Import
![](/Wiki/Diagrams/data_flow_diagrams/decision_tree_import.jpg)

Figure 2 : Decision Tree & Decision Table - Export
![](/Wiki/Diagrams/data_flow_diagrams/decision_tree_export.jpg)

### viii. Appendix H - Story Boards

Figure 1 : Administrator/C-Suite Executive Story Boards
![UI Prototypes_Story Boards Admin Executive](https://github.com/Uvic-SENG321Spring2024/team6-developer/assets/111109194/d8877a00-c293-4dd0-8ed0-cf75e1cffbef)

Figure 2 : Department Manager Story Boards
![UI Prototypes_Story Boards Manager](https://github.com/Uvic-SENG321Spring2024/team6-developer/assets/111109194/fde45410-cdcb-4453-b28c-dbe1b40aad03)

### ix. Appendix I - Story Boards (Final)
Figure 1: Finalized Storyboards
![UI Prototypes_Story Boards (2)](https://github.com/Uvic-SENG321Spring2024/team6-developer/assets/111109194/b3d4b667-eefd-4395-b238-92acd50f3dec)



