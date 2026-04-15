# chargeback-data-pipeline
An automated pipeline to normalise and deduplicate fragmented global chargeback data across Adyen, Stripe, and Ingenico.
# Global Chargeback Transformation Pipeline
**Business Value:** Recovered visibility on $242,214.87 in global risk exposure.

## Project Overview
This project addresses the manual data friction involved in managing chargebacks across three disparate merchant platforms: Adyen, Stripe, and Ingenico. The pipeline automates the ingestion of 9,400+ fragmented files to provide a single, deduplicated data source.

## Technical Features
- **Fuzzy Header Mapping:** Automatically identifies inconsistently labeled columns (e.g., 'Curr' vs 'Dispute Currency').
- **Structural Ingestion:** Handles both standard CSV/TXT lists and individual JSON record objects.
- **FX Fallback Algorithm:** Uses temporal proxy logic to handle 2025 transactions despite 2024 reference data gaps.
- **Automated Deduplication:** Cleans multi-currency "ghost" entries to ensure financial audit-readiness.

## Impact
- **Volume:** Processed 9,400+ files to identify 298 unique, valid disputes.
- **Integrity:** Identified and corrected a >$240k reporting bias caused by raw export duplicates.
