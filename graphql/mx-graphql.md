# MX Technologies — Conceptual GraphQL Schema

## Overview

MX Technologies does not publish a native GraphQL API. This schema is a conceptual
GraphQL representation derived from the MX Platform REST API
(https://docs.mx.com/api-reference/platform-api/overview/) and the published OpenAPI
specification (https://github.com/mxenabled/openapi).

The schema models the full surface of the MX Platform: account aggregation, open banking
connectivity, financial data enrichment, identity verification, budgets, goals, analytics,
hosted widgets, and OAuth/Connect flows.

**Schema file:** `mx-schema.graphql`

---

## Type Inventory (65 types)

### Core Financial Data

| Type | Description |
|------|-------------|
| `User` | An end-user on the MX platform with linked members, accounts, and financial data. |
| `Member` | A connection from a User to a financial Institution, tracking aggregation state and credentials. |
| `MemberStatus` | Real-time aggregation status and MFA challenges for a Member. |
| `MemberCredential` | A credential field value stored for a Member to authenticate with an Institution. |
| `Credential` | A generic credential field definition. |
| `InstitutionCredential` | A credential field required by a specific Institution. |
| `Institution` | A financial institution available for connection (16,000+). |
| `Account` | A financial account (checking, savings, credit card, investment, loan, etc.) belonging to a Member. |
| `AccountNumber` | Routing and account number details for an Account including ACH, IBAN, and SWIFT. |
| `AccountOwner` | Owner identity information attached to an Account. |
| `Balance` | A point-in-time balance record for an Account. |
| `Transaction` | A financial transaction on an Account with MX enrichment (category, merchant, flags). |
| `TransactionRule` | A user-defined rule to auto-categorize transactions matching a description pattern. |
| `TransactionCategory` | A hierarchical spending/income category used to classify transactions. |
| `Merchant` | An enriched merchant entity linked to transactions. |
| `MerchantLocation` | A physical location of a Merchant with geo-coordinates. |
| `Statement` | An account statement document linked to a Member and Account. |
| `StatementDownload` | Binary content for downloading a Statement PDF. |
| `TaxDocument` | A tax document (e.g., 1099, W-2) from a financial institution. |
| `TaxRecord` | A line-item record extracted from a TaxDocument. |
| `Holding` | An investment security or asset held in an Account. |
| `InvestmentHolding` | A Holding enriched with unrealized gain/loss context. |

### Identity & Verification

| Type | Description |
|------|-------------|
| `Identity` | Verified account owner identity data returned after an identify aggregation request. |
| `IdentityAddress` | A structured mailing address within an Identity. |
| `IdentityPhone` | A phone number entry within an Identity. |
| `VerificationStatus` | Aggregated account verification status for a Member including per-account results. |
| `AccountVerification` | Verification status and routing/account numbers for a single Account. |

### Microdeposits

| Type | Description |
|------|-------------|
| `Microdeposit` | A microdeposit verification initiation record for ACH account verification. |
| `MicrodepositTransaction` | An individual deposit transaction within a Microdeposit verification. |

### Budgets & Goals

| Type | Description |
|------|-------------|
| `Budget` | A spending budget for a TransactionCategory in a given period. |
| `BudgetCategory` | A category-level budget summary with spending totals. |
| `BudgetPeriod` | Monthly budget tracking data within a Budget. |
| `Goal` | A financial goal (savings, debt payoff, etc.) with progress tracking. |

### Analytics & Insights

| Type | Description |
|------|-------------|
| `MonthlyExpense` | Aggregated monthly spending totals broken down by category. |
| `MonthlyIncome` | Aggregated monthly income totals broken down by source. |
| `ExpenseCategory` | A single category's contribution to a MonthlyExpense. |
| `IncomeSource` | An individual income source in a MonthlyIncome summary. |
| `CashFlowProfile` | A user's cash flow profile including average income, expenses, and projections. |
| `NetWorthComponent` | A single asset or liability contributing to a user's net worth. |
| `SpendingAnalytics` | Detailed spending analysis over a date range by category and merchant. |
| `MerchantSpending` | Per-merchant spending totals within a SpendingAnalytics result. |
| `WeeklySpending` | Weekly spending buckets within a SpendingAnalytics result. |
| `DataPoint` | A typed numeric time-series data point for charting and trend analysis. |
| `Aggregation` | Metadata about an aggregation run including accounts and transactions processed. |
| `Analytics` | A composite analytics object grouping monthly, cash flow, and net worth data. |
| `Portfolio` | An investment portfolio view with asset allocation and aggregate performance. |
| `AssetAllocation` | Breakdown of portfolio value by HoldingType. |

### Loans & Real Assets

| Type | Description |
|------|-------------|
| `LoanDetail` | Detailed loan fields (rate, term, payoff) for a loan Account. |
| `Mortgage` | Mortgage-specific fields for a real estate loan Account. |
| `Vehicle` | Vehicle asset details associated with an Account. |
| `RealEstate` | Real estate property details associated with an Account. |

### Widgets

| Type | Description |
|------|-------------|
| `ConnectWidget` | A hosted MX Connect widget URL for account linking. |
| `SpendingWidget` | A hosted spending insights widget URL. |
| `NetWorthWidget` | A hosted net worth widget URL. |
| `CashFlowWidget` | A hosted cash flow widget URL. |
| `BillerWidget` | A hosted biller management widget URL. |
| `RewardWidget` | A hosted rewards widget URL. |
| `PulseWidget` | A hosted financial pulse widget URL. |
| `GoalWidget` | A hosted goals widget URL. |
| `WidgetUrl` | Generic widget URL response. |

### OAuth & Connect

| Type | Description |
|------|-------------|
| `MXConnect` | An MX Connect session for OAuth-based account linking. |
| `OAuthWindow` | An OAuth redirect window URI for an OAuth-enabled Institution. |
| `ConnectToken` | A short-lived token used to initialize the MX Connect widget. |
| `RefreshToken` | An OAuth access/refresh token pair. |

### Platform & Security

| Type | Description |
|------|-------------|
| `APIKey` | An API key credential for MX platform access. |
| `Pagination` | Cursor-style pagination metadata returned with list responses. |
| `DeleteResult` | Result envelope for delete mutations. |

### MFA

| Type | Description |
|------|-------------|
| `MFAChallenge` | An MFA challenge step requiring user input to continue aggregation. |
| `MFAImageOption` | An image-based MFA option with a data URI. |
| `CredentialOption` | A key-value option for select/multi-select credential fields. |

---

## Enums (16 enums)

| Enum | Values (count) |
|------|---------------|
| `ConnectionStatus` | 17 — full MX connection state machine |
| `AccountType` | 24 — checking through unknown |
| `AccountNumberType` | 4 |
| `TransactionType` | 2 — CREDIT / DEBIT |
| `TransactionStatus` | 2 — POSTED / PENDING |
| `CredentialFieldType` | 6 |
| `MFAChallengeType` | 6 |
| `HoldingType` | 10 |
| `GoalType` | 9 |
| `VerificationStatusValue` | 4 |
| `VerificationType` | 2 |
| `MicrodepositStatus` | 4 |
| `AggregationStatus` | 4 |
| `NetWorthComponentType` | 2 |
| `DataPointType` | 7 |
| `WidgetType` | 16 |

---

## Source References

- REST API Docs: https://docs.mx.com/api-reference/platform-api/overview/
- OpenAPI Spec: https://github.com/mxenabled/openapi/blob/master/openapi/mx_platform_api.yml
- GitHub Org: https://github.com/mxenabled
- Developer Portal: https://docs.mx.com/

---

## Notes

- MX has no publicly announced GraphQL endpoint as of June 2026.
- This schema is conceptual and intended for tooling, exploration, and API modeling purposes.
- All field names follow MX REST API conventions (snake_case translated to camelCase).
- The schema covers the Platform API (primary), Data Access API (FDX/OAuth), and Widget SSO surface.
- The Atrium legacy API is not separately modeled; its types overlap substantially with the Platform API types above.
