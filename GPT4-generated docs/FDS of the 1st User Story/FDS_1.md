# User story 1 - Search Availability by Exploitation Rights - FDS

## Glossary

- Exploitation Rights: Rights related to the use of content for various purposes such as broadcasting, streaming, etc.

- Rights Matrix: A structured representation of rights, including dimensions such as exploitation, merchandising, etc.
- Dimension Values: Specific attributes within a right matrix, such as territory, language, platform, etc.
- Catalog Items: Individual pieces of content or groups of content managed within a catalog.
- Exclusivity: A condition where rights are granted exclusively to one party, preventing others from using the same rights.
- Search API: An application programming interface that allows for querying and retrieving search results.
- User Interface (UI): The visual part of a computer application through which users interact with the software.
- Content Manager: A user role responsible for managing and distributing digital content.

## Executive summary

The primary objective of this user story is to implement a search functionality that allows users to search for content availability based on exploitation rights. This functionality will enable content managers to efficiently find available content for exploitation, ensuring they can maximize revenue opportunities by identifying available rights. The scope includes specifying periods and rights dimensions, integrating with the rights matrix and catalog data, and ensuring seamless interaction with the search API and user interface.

## Overview/Background

### Context
In the media and entertainment industry, managing the availability of digital rights is crucial for maximizing revenue and ensuring compliance with contractual obligations. Exploitation rights, which pertain to the use of content for various purposes such as broadcasting and streaming, are a key component of this management process. Traditional methods of searching for available exploitation rights are often inefficient and prone to errors, leading to potential revenue loss and increased risk of rights violations.

### Problem Statement

Content managers need a robust and efficient way to search for content availability based on exploitation rights. The current system lacks the necessary functionality to perform detailed searches, specify periods, and filter by rights dimensions. This limitation hinders the ability to identify and utilize available content for distribution, resulting in missed revenue opportunities and potential rights conflicts.

### Objectives
- Implement a search functionality for exploitation rights.
- Allow users to specify search periods and rights dimensions.
- Integrate with the rights matrix and catalog data.
- Ensure seamless interaction with the search API and user interface.
- Provide detailed search results, including match criteria, available periods, and exclusivity status.

## Scenarios

Scenario 1: Basic Search by Exploitation Rights
- Conditions: The user specifies exploitation rights and basic search criteria.
- User Interactions: The user enters search criteria in the UI and initiates the search.
- Expected Outcome: The system returns a list of available content matching the criteria.

Scenario 2: Advanced Search with Period Specification
- Conditions: The user specifies exploitation rights, search periods, and rights dimensions.
- User Interactions: The user enters detailed search criteria, including periods and dimensions, and initiates the search.
- Expected Outcome: The system returns a list of available content matching the detailed criteria.

Scenario 3: Search with Exclusivity Check
- Conditions: The user specifies exploitation rights and requests an exclusivity check.
- User Interactions: The user enters search criteria and selects the exclusivity check option.
- Expected Outcome: The system returns a list of available content, indicating exclusivity status for each result.

### Assumptions and dependencies

Assumptions
- The user has the necessary permissions to perform availability searches.
- The rights matrix for exploitation rights is predefined and accessible.
- Users have a basic understanding of rights management and the system’s interface.

Dependencies
- Integration with the rights matrix and catalog data.
- Interaction with the search API and user interface.
- Availability of development and testing resources.



## User requirements

Use cases & Scenarios
### Use Cases & Scenarios

### Use Cases & Scenarios

| **Use Case**                         | **Number** | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | **Linked Acceptance Criteria** |
|-------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| Basic Search by Exploitation Rights | 1          | 1. The user logs into the system.<br>2. The user navigates to the search functionality.<br>3. The user selects exploitation rights as the search criterion.<br>4. The user enters basic search criteria (e.g., content type, title).<br>5. The user initiates the search.<br>6. The system processes the search request.<br>7. The system returns a list of available content matching the criteria.<br>**Actors**: Content Manager<br>**Expected Outcome**: The system displays a list of available content based on exploitation rights. | AC1                           |
| Advanced Search with Period Specification | 2     | 1. The user logs into the system.<br>2. The user navigates to the search functionality.<br>3. The user selects exploitation rights as the search criterion.<br>4. The user enters detailed search criteria, including periods and rights dimensions.<br>5. The user initiates the search.<br>6. The system processes the search request.<br>7. The system returns a list of available content matching the detailed criteria.<br>**Actors**: Content Manager<br>**Expected Outcome**: The system displays a list of available content based on detailed search criteria. | AC1                           |
| Search with Exclusivity Check       | 3          | 1. The user logs into the system.<br>2. The user navigates to the search functionality.<br>3. The user selects exploitation rights as the search criterion.<br>4. The user enters search criteria and selects the exclusivity check option.<br>5. The user initiates the search.<br>6. The system processes the search request.<br>7. The system returns a list of available content, indicating exclusivity status for each result.<br>**Actors**: Content Manager<br>**Expected Outcome**: The system displays a list of available content with exclusivity status. | AC1                           |

### Business Rules
- BR 1: The system must only allow users with appropriate permissions to perform availability searches.
- BR 2: The rights matrix for exploitation rights must be predefined and accessible.
- BR 3: The system must integrate with the rights matrix and catalog data to retrieve accurate search results.
- BR 4: The system must provide an option for users to specify search periods and rights dimensions.
- BR 5: The system must include an exclusivity check option in the search functionality.

### User Journey

Use Case 1: Basic Search by Exploitation Rights
- Step 1: User logs into the system.
- Step 2: User navigates to the search functionality.
- Step 3: User selects exploitation rights as the search criterion.
- Step 4: User enters basic search criteria (e.g., content type, title).
- Step 5: User initiates the search.
- Step 6: System processes the search request.
- Step 7: System returns a list of available content matching the criteria.

Use Case 2: Advanced Search with Period Specification
- Step 1: User logs into the system.
- Step 2: User navigates to the search functionality.
- Step 3: User selects exploitation rights as the search criterion.
- Step 4: User enters detailed search criteria, including periods and rights dimensions.
- Step 5: User initiates the search.
- Step 6: System processes the search request.
- Step 7: System returns a list of available content matching the detailed criteria.

Use Case 3: Search with Exclusivity Check
- Step 1: User logs into the system.
- Step 2: User navigates to the search functionality.
- Step 3: User selects exploitation rights as the search criterion.
- Step 4: User enters search criteria and selects the exclusivity check option.
- Step 5: User initiates the search.
- Step 6: System processes the search request.
- Step 7: System returns a list of available content, indicating exclusivity status for each result.


## Framework Requirements

### Security

Permissions
- PR 1: Only users with the “Content Manager” role or higher should have access to the search functionality for exploitation rights.
- PR 2: Permissions should be managed through the system’s role-based access control (RBAC) mechanism.

Data Partitioning
- DP 1: Data partitioning should be implemented to ensure that users can only access data relevant to their business entity.
- DP 2: The system should segregate data based on user roles, data sensitivity, and other relevant factors to ensure data security and integrity.
