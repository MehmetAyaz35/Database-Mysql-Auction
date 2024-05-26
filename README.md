# Auction Management System - Comprehensive Documentation

This repository contains all necessary SQL scripts, ER diagrams, and event handlers for managing an auction system. These components work together to support the functionality of creating, managing, and concluding auctions, including handling bids and maintaining customer and supplier data.

## Repository Content Overview

### SQL Scripts

#### Procedures
- **2302_G04_Procedure_SkapaAuktion(v4).sql**: Manages the creation of new auctions, setting initial parameters like start and end dates.
- **2302_G04_Procedure_VisaAvslutadeAuktioner(v4).sql**: Retrieves all completed auctions from the database.
- **2302_G04_Procedure_VisaBudHistorik(v4).sql**: Provides a detailed bidding history for auctions, essential for audit and transparency.
- **2302_G04_Procedure_RegisterProdukt(v4).sql**: Registers new products into the system, assigning them to suppliers and categories.

#### Triggers
- **2302_G04_Trigger_auktion_AFTER_DELETE(v4).sql**: Handles operations that need to be performed after an auction is deleted.
- **2302_G04_Trigger_auktionsbud_AFTER_INSERT(v4).sql**: Ensures that bids comply with business rules immediately after they are entered into the system.
- **2302_G04_Trigger_check_bud_limits(v4).sql**: Validates bid amounts to prevent underbidding or overbidding.

#### Views
- **2302_G04_View_kundlista_med_ordervarde(v4).sql**: Lists customers and the order value associated with each, useful for sales analysis.
- **2302_G04_View_pagaendeauktionersomlist(v4).sql**: Displays ongoing auctions, providing a real-time overview for users.
- **2302_G04_View_total_provisionen_per_manad(v4).sql**: Calculates total commissions per month, aiding in financial assessments.

#### Events
- **2302_G04_EVENT_delete_completed_auctions.sql**: Automatically cleans up completed auctions to maintain database efficiency.

#### Initial Setup and Data Entry
- **2302_G04_CREATE_Projektarbete(v4).sql**: Sets up the initial database schema required for the auction system.
- **2302_G04_INSERT_Leverantör_och_Kund(v4).sql**: Inserts initial data for suppliers and customers to kickstart the application.

### ER Diagrams and Design Files
- **2302_G04_ER_diagram.PNG**, **2302_G04_ER_diagram_projectarbete(v4).drawio**, **2302_G04_ERR_Diagram(v4).mwb**: These files provide detailed visual representations of the database structure, highlighting how different tables are interconnected.

## Usage Instructions
1. **Database Setup**: Begin by executing the `2302_G04_CREATE_Projektarbete(v4).sql` to establish the database schema.
2. **Data Initialization**: Populate initial data using `2302_G04_INSERT_Leverantör_och_Kund(v4).sql`.
3. **Operational Scripts**: Implement the procedures, triggers, and views to enable full functionality of the auction system.
4. **Maintenance and Cleanup**: Utilize the event script `2302_G04_EVENT_delete_completed_auctions.sql` to automate the maintenance of the database.

## Viewing ER Diagrams
- Use image viewers for `.PNG` files, diagrams.net for `.drawio` files, and MySQL Workbench for `.mwb` files to view and analyze the ER diagrams.

## Development Notes
- Regularly update scripts and diagrams as new business requirements emerge.
- Ensure rigorous testing in a development environment before deploying updates to production.

This comprehensive guide provides detailed insights into each component of the auction management system, supporting developers, database administrators, and system architects in the development, deployment, and ongoing maintenance of the system.
