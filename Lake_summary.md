

## 1. Disaster Recovery Overview
- **Definition:** Planning to recover application functionality after outages or failures.
- **Importance:** Ensures application availability and business continuity.
- **Criticality:** Determines allowable downtime and recovery strategy.
- **High-Level Approaches:** 
  - **Active-Active:** Immediate failover; expensive but no downtime.
  - **Active-Passive Approaches:**
    - **Cold Standby:** Secondary inactive, cost-effective but higher Recovery Time Objective (RTO).
    - **Pilot Light:** Secondary partially active; faster recovery, cost-effective.
    - **Warm Standby:** Secondary fully active but passive; quick failover but higher cost.
- **Key Terms:**
  - **RPO (Recovery Point Objective):** Acceptable data loss.
  - **RTO (Recovery Time Objective):** Maximum acceptable downtime.
- **Best Practices:** Choose strategies based on criticality, cost, and downtime tolerance.

---

## 2. Data Lakes Best Practices
- **Definition:** Centralized storage for structured, unstructured, and semi-structured data without schema enforcement.
- **Evolution:** Shift from batch-oriented, on-premises storage to cloud-based, real-time, multi-workload systems.
- **Best Practices:**
  1. Avoid becoming a "data swamp"; incrementally build with clear use-cases.
  2. Define a structured onboarding process; prioritize use-cases and consumer needs.
  3. Establish clear data integration patterns (batch, real-time, event-driven).
  3. Choose data processing methods (dedicated clusters, just-in-time clusters, serverless).
  4. Clearly define data consumption patterns (reporting, ad-hoc queries, exploratory analytics).
  5. Select technology based strictly on use-cases; avoid over-engineering.
  6. Ensure data quality upfront; implement a configurable data-quality rules engine.
  7. Implement strong data governance (lineage, auditing, metadata management).
  8. Ensure robust security (authentication, fine-grained authorization, encryption).
  9. Establish telemetry for proactive monitoring and rapid fixes.
  10. Continuously optimize cost (consider just-in-time resources, storage lifecycle policies, active-active vs active-passive setups).

---

## 2. Data Lake Essentials
- **Definition:** Central repository for all data types (structured, unstructured, semi-structured).
- **Schema Enforcement:** Schema-on-read approach, flexible data storage.
- **Modern Use-cases:** Cloud-based, real-time integration, analytics, reporting, ad-hoc queries, and exploratory analysis.
- **Integration Patterns:** Choose between batch processing, real-time ingestion (Kafka, Spark streaming), or event-driven triggers.
- **Data Processing:** Decide between dedicated, always-on clusters or just-in-time/elastic approaches for cost efficiency (e.g., AWS EMR, Azure Synapse).
- **Consumption Patterns:** Profile consumption needs to define appropriate data marts, query capabilities, and sandbox environments.
- **Technology Choices:** Prioritize simplicity, alignment with business needs, and avoiding unnecessary complexity.
- **Data Quality and Governance:** Essential to maintain data integrity, lineage tracking, auditing, and metadata management.
- **Security:** Implement comprehensive authentication, authorization, encryption, VPN, and comply with regulations.
- **Telemetry and Cost Optimization:** Proactively monitor environments, adopt serverless architectures, and optimize resources to control costs.

---

## 3. Snowflake Overview and Architecture
- **Definition:** SaaS-based cloud data warehouse for enterprise analytics.
- **Key Advantage:** No hardware setup/maintenance required; fully managed cloud service.
- **Architecture:** Hybrid of "Shared Disk" and "Shared Nothing":
  - **Shared Disk:** Simpler read-write operations, potential distributed-lock complexities.
  - **Shared Nothing:** Independent nodes (RAM, CPU, storage), data shuffling overhead.
- **Snowflake Layers:**
  1. **Storage Layer:** Decoupled, independent from compute.
  2. **Compute Layer (Virtual Warehouses):** Scale independently; spin-up/down as needed, optimizing cost and performance.
- **Virtual Warehouses:** Independent compute clusters based on user requirements, flexible scaling and cost-efficient.

---
