# Availability Epic FDS

## GLOSSARY
- Exploitation Rights: Rights related to the use of content for various purposes such as broadcasting, streaming, etc.
- Sellable Rights: Rights that can be sold or licensed to third parties.
- Business Entity: An organizational unit within a company that manages specific business functions.
- Right Matrix: A structured representation of rights, including dimensions such as exploitation, merchandising, etc.
- Dimension Values: Specific attributes within a right matrix, such as territory, language, platform, etc.
- Exclusivity: A condition where rights are granted exclusively to one party, preventing others from using the same rights.
- Catalog Items: Individual pieces of content or groups of content managed within a catalog.
- Gantt View: A visual representation of availability periods using a timeline format.
- KPI (Key Performance Indicator): Metrics used to evaluate the success of specific activities or processes.
- Hiatus Rights: Temporary suspension of rights within a contract.
- Legal Block: Restrictions placed on content due to legal reasons.
- Composition: A collection of content items managed together.
- Edition: A specific version or release of a content item.
- Season: A collection of episodes within a series.
- Series: A collection of seasons or episodes.

--- 

## OVERVIEW

The “Availability” feature in AllRights by Fincons Group is designed to provide comprehensive management and optimization of digital rights availability. This feature enables users to search, view, and manage the availability of rights across various dimensions and periods.

The primary objective is to ensure that rights are utilized effectively, maximizing revenue while minimizing risks associated with rights violations. The feature supports detailed search criteria, multiple views for results, and performance optimizations to handle large datasets efficiently.

--- 

## PRODUCT PERSPECTIVE

### Problem Statement

The media and entertainment industry faces challenges in managing the availability of digital rights due to the complexity of rights matrices, varying business entities, and the need for precise control over rights usage. Traditional methods are often inefficient, leading to potential revenue loss and increased risk of rights violations. The “Availability” feature aims to address these issues by providing a robust, centralized platform for managing rights availability, ensuring full coverage and compliance with contractual obligations.

### Objectives
- Comprehensive Search: Enable detailed searches based on purpose, periods, rights, and catalogs.
- Flexible Views: Provide basic and advanced views for displaying search results, including Gantt and KPI views.
- Performance Optimization: Ensure fast response times for searches and result displays, even with large datasets.
- Exclusivity Management: Include checks for exclusivity to prevent rights conflicts.
- Detailed Reporting: Generate detailed reports and export options for further analysis.

---

### Constraints and Assumptions
- Technological Limits: The system must handle large datasets efficiently, with performance optimizations in place.
- Resource Availability: Development and testing resources must be allocated to ensure timely delivery.
- Time Constraints: The feature must be developed and deployed within the project timeline.
- Assumptions: Users have a basic understanding of rights management and the system’s interface.

---

## HIGH LEVEL PROCESS FLOWS

Search Criteria

1. Purpose:
- Separate availability categories for exploitation and sellable rights.
- Results vary by business entity for exploitation; unique availability for sellable rights.

2. Periods:
- Define the search period, which can be unlimited.
- Specify whether the period must be fully or partially covered.

3. Rights:
- Specify rights values to search.
- Define the right matrix and allow specific dimension values to be searched.
- Include exclusivity checks.

4. Catalogs:
- Search for specific catalog items or groups with specific attributes.
- Manage seasons and compositions/editions with rights based on KPIs from source items.

---

Results Views

1. Basic View:
- Display all found items with details on match criteria.
- Show available periods, rights match, exclusivity status, and details for seasons and compositions/editions.
- Actions include deep dives into seasons, compositions/editions, contracts, and a Gantt view of available periods.

2. Advanced View:
- Export detailed contract information for found items.
- Include all basic view data plus contract details, rights sets, dimension values, periods, and consumption metrics.
- Generate an Excel file for download.

---

Performance

1. Sizing:
- Based on a use case with approximately 135,000 items, including 12,000 seasons and compositions.
- Six dimensions for a single right matrix.

2. Exclusions:
- Timing related to backend service and client-side rendering logic.
- Concurrent queries.
- Catalog data partitioning.

3. Performance Results:
- First page results appear within 25 seconds (worst case) with a mean time of less than 8 seconds.
- Subsequent pages load within 3 seconds (worst case).

---

Filters

1. Mandatory Filter – Right Matrix Type:
- A new mandatory filter for “Right Matrix Type” is introduced, requiring each availability search to be performed on one right matrix type at a time.

2. License Period Filters:
- “Full Coverage” renamed to “Full license windows”.
- “Overlaps” renamed to “Not Full license windows”.
- “Begin with” and “End within” options.
- “Duration”: Aggregated license windows must have a contiguous period greater than a specified duration.

3. Right Combination Coverage:
- Standard search for “Not Full RC Coverage”.
- “Full RC Coverage” search.

4. Dimension Values:
- Filters on two dimensions applied with “AND” logic.
- Filters on the same dimension applied with intersecting logic.

---

Views

1. Basic View:
- Fields displayed by default: Poster, Title, Custom ID, Content Type, Record Type, Exclusivity, Availability Timeline, Availability Coverage, Residual Runs/Units.
- Additional fields: Catalog Parent, Genre, Category, Release Year.

2. Gantt View:
- Shows each timeslice on a row with different colors for full/partial coverage.

3. Advanced View:
- Fields displayed by default: Title, Custom ID, Content Type, Exclusivity, Contract Name, Contract Number, Rights Set Summary, Rights Type, Territory, Language, Platform, Channel, License Window Type, License Window, Contractual Runs, Residual Runs, Contractual Period, Residual Period.
- Additional fields: Record Type, Catalog Parent, Availability Timeline, Genre, Category, Release Year, Transmitted Runs, Scheduled Runs, Sold Runs, Transmitted Period, Scheduled Period, Sold Period.

4. New View Types:
- Net Right Combinations View: Shows results of the new algorithm with applied filters.
- Basic/Gantt View: Main attribute items and calculated fields.
- Enriched View: Basic view plus additional fields.
- Detailed View: Advanced view with contractual data.
- Export View: Information to be exported.
- KPI View: Aggregated results for Season, Series, Composition.

---

### Issues and Restrictions
- Views Priority: Prioritize developing the “RC Net view” as it contains main availability search information.
- Season and Series Views: Provide KPI view instead of detailed contract information.
- Ordering: Default ordering by item name due to performance issues.
- View Information in a Page: Users can switch views without waiting for long times.
- Catalog Parent Field: Part of enrichment on demand.
- Availability Timeline: Min (start date) and Max (end date) to show maximum interval.
- Exclusivity: Calculated similarly for Season, Composition, and Edition as for KPI on availability coverage.

---

Final Note

The “Availability” feature in AllRights is a comprehensive solution designed to address the complexities of digital rights management in the media and entertainment industry. By providing detailed search criteria, flexible views, and performance optimizations, this feature ensures that rights are managed effectively, maximizing revenue and minimizing risks. The inclusion of exclusivity checks, detailed reporting, and various view types further enhances the functionality, making it a robust tool for rights management.