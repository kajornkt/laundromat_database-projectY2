# Laundromat Database Management System

## 📌 Project Overview

This project delivers a centralized relational database management system (DBMS) designed to optimize the business operations, transaction architectures, and analytics infrastructure of a multi-branch laundromat franchise.

Developed as part of the **Database System Concepts (06036112)** curriculum within the Program in Business Information Technology at the **School of Information Technology, King Mongkut's Institute of Technology Ladkrabang (KMITL)**.

### 📉 Problem Statement

Traditional laundromat administration websites often present limiting, unsummarized datasets—such as recording individual cash inputs every time a coin is dropped into a slot—without ever aggregating the total revenue per machine cycle. This layout makes it difficult to track specific temperature selections, extra time additions, or real-time consumer traffic variations required for critical forecasting.

Furthermore, scaling a growing brand into multi-branch ecosystems requires backend support for service expansions—such as app-integrated e-wallets, loyalty membership structures, ironing, and pick-up/drop-off courier logistics. This database model solves these core tracking limitations.

---

## 🚀 Core Objectives & Features

* **Aggregated Transaction Architecture:** Replaces raw coin-insertion tracking with unified order entries logging comprehensive cycle totals, custom user settings, and clear payment methods.


* **Omnichannel Service Bundling:** Natively links multi-layered orders (Washing, Drying, Ironing, and Pick-up/Drop-off Delivery logistics) directly to a single customer transaction profile.


* **Enterprise Multi-Branch Scaling:** Centralizes administrative authority to handle disparate regional branch metadata, regional staff placement, and distinct employee task states.


* **Tiered Loyalty Discount Matrix:** Tracks a dynamic customer database utilizing membership tiers (`Bronze`, `Silver`, `Gold`, `Diamond`) to calculate real-time savings margins dynamically.



---

## 🗺️ Database Architecture & Design

### Entity-Relationship Schema & Key Tables

The logical data model splits business operations into interconnected entity subsets:

1. **Organizational Infrastructure:** `BRANCHES`, `EMPLOYEES`, `ROLES`.

2. **Customer Ecosystem:** `CUSTOMERS`.

3. **Core Pipeline Operations:** `ORDERS`, `ORDERS_SERVICE`, `SERVICES`, `ORDERS_PAYMENT`.

4. **Physical Machinery & Telemetry:** `MACHINES`, `MACHINE_TRANSACTION`.

5. **Microservice Operations:** `ONLINE_WASHDRY`, `IRONING`, `DELIVERY`, `CLOTHES`.



### 📊 Normalization Principles

**First Normal Form (1NF):** Established atomic fields, verified unique rows, and eliminated repeating metadata attributes across all relational structures.


**Second Normal Form (2NF):** Extracted partial functional dependencies—such as creating an isolated `MEMBERSHIP_TIER` matrix table—to guarantee non-key elements are bound entirely to the primary identity key.


**Third Normal Form (3NF):** Eliminated structural redundancies by separating transitive layers within operational sub-tables (e.g., streamlining intermediate link fields like `Order_service_id` and optimizing transaction telemetry).



---

## 🛠️ Repository Directory & File Inventory

The repository is populated with optimized SQL script components that support step-by-step schema production, data injection, and query execution:

* **`table_data.sql`** — Master DDL schema. Contains structural logic defining entity tables, primary/foreign key relationships, internal constraints, and sequential counter tracking components (`CUST_ID_SEQ`, `ORDER_ID_SEQ`, etc.).


* **`data_customers.sql`** — Demographic input datasets populating individual customer details and foundational registration records.


* **`data_orders.sql`** / **`data_order_services.sql`** / **`data_services.sql`** — Transaction processing entries sorting state variations (`Pending`, `In Progress`, `Completed`, `Cancelled`).


* **`data_online_washdry.sql`** / **`data_ironing.sql`** / **`data_delivery.sql`** / **`data_clothes.sql`** — Domain inputs managing pricing definitions, item weights, volume, and courier records.


* **`data_orders_payment.sql`** — Mapping parameters verifying accounting details (e.g., `Prompt pay`, `Card`, `Cash`) along with corresponding settlement states.


* **`data_machine_transaction.sql`** — Low-level physical logs generated from manual hardware interactions.


* **`data_branches.sql`** / **`data_machines.sql`** — Core capital asset listings logging local physical franchise capacities.


* **`data_employees.sql`** — Complete human resource logs mapping staff assignments directly to targeted business nodes and responsibilities.



---

## 📊 SQL Query Implementation & Business Intent

All data analytics and operational scripts are organized cleanly inside the `/commands` directory, categorized by their execution complexity and strategic business utility:

### 📁 `/commands/beginner`

* **`beginner1.sql`**
* **Business Purpose:** Identifies veteran branch staff working over 1 year to evaluate retention stability and distribute senior training resources.




* **`beginner2.sql`**
* **Business Purpose:** Tallies and ranks historical garment counts to uncover customer garment preferences, optimizing inventory targets and tailoring pricing structures.




* **`beginner3.sql`**
* **Business Purpose:** Computes the average transaction size to track customer spending patterns and judge seasonal baseline performance.




* **`beginner4.sql`**
* **Business Purpose:** Returns customer order histories that successfully reached a completed status, useful for tracking fulfillment efficiency.




* **`beginner5.sql`**
* **Business Purpose:** Tracks historical hardware wear patterns to build preventive machine maintenance schedules and flag underutilized capacity.




* **`beginner6.sql`**
* **Business Purpose:** Ranks geographic locations by transaction frequency to guide resource adjustments and highlight underperforming markets.





### 📁 `/commands/middle`

* **`middle1.sql`**
* **Business Purpose:** Maps where registered members actively generate orders to evaluate localized engagement and steer targeted community marketing.




* **`middle2.sql`**
* **Business Purpose:** Aggregates gross revenue yields specifically across core online wash/dry categories to measure primary line profitability.




* **`middle3.sql`**
* **Business Purpose:** Pinpoints clients using both courier delivery and professional iron pipelines to isolate high-value convenience shoppers.




* **`middle4.sql`**
* **Business Purpose:** Calculates the concrete monetary discounts enjoyed by members to measure loyalty-tier value and verify profit margins.




* **`middle5.sql`**
* **Business Purpose:** Ranks individual shoppers by total active interactions across all services to guide VIP incentive distribution.




* **`middle6.sql`**
* **Business Purpose:** Pulls the elite top-tier spending accounts across completed orders for direct premium account stewardship.




* **`middle7.sql`**
* **Business Purpose:** Utilizes subqueries to find customers who outspend the typical user baseline, helping target specialized pilot campaigns.




* **`middle8.sql`**
* **Business Purpose:** Lists operational workers (delivery and ironing) alongside their local nodes to balance regional labor and handle shift planning.





### 📁 `/commands/high`

* **`high1.sql`**
* **Business Purpose:** Runs deep calculations pooling multi-microservice pipelines while incorporating individual discount variables to populate the ledger seamlessly.




* **`high2.sql`**
* **Business Purpose:** Generates total performance calculations broken down by explicit category divisions to isolate vertical growth.




* **`high3.sql`**
* **Business Purpose:** Breaks down local income daily across all service models to give management a granular view of branch health.




* **`high4.sql`**
* **Business Purpose:** Establishes reusable database views to analyze daily demand changes without running redundant operations.




* **`high5.sql`**
* **Business Purpose:** Packs transaction totals, ticket averages, and action counts into a single view for simplified business evaluation.




* **`high6.sql`**
* **Business Purpose:** Extracts premium regular accounts bundling primary cycles to drive dedicated long-term customer retention campaigns.





---

## 👥 Contributors (Development Team)

* **Chit Pont Pont Cherry** (66070327) 


* **Khokwan Tachaongart** (66070333) 


* **Nicha Wanaroj** (66070335) 



**Academic Mentor:** Asst. Prof. Dr. Pattanapong Chantamit-O-Pas
