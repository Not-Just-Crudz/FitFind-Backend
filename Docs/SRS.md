# FitFind Software Requirements Specification

## Linked contents

  - [Software Requirements Specification (SRS)](#software-requirements-specification-srs)
- [1. Introduction](#1-introduction)
  - [1.1 Purpose](#11-purpose)
  - [1.2 Product scope](#12-product-scope)
  - [1.3 Intended audience](#13-intended-audience)
  - [1.4 Document conventions](#14-document-conventions)
  - [1.5 Definitions and abbreviations](#15-definitions-and-abbreviations)
  - [1.6 References](#16-references)
- [2. Overall description](#2-overall-description)
  - [2.1 Product perspective](#21-product-perspective)
  - [2.2 Product objectives](#22-product-objectives)
  - [2.3 Product layers](#23-product-layers)
  - [2.4 User classes and actors](#24-user-classes-and-actors)
  - [2.5 Operating environment](#25-operating-environment)
  - [2.6 Assumptions and dependencies](#26-assumptions-and-dependencies)
  - [2.7 Product boundaries and constraints](#27-product-boundaries-and-constraints)
- [3. Product features and functional requirements](#3-product-features-and-functional-requirements)
  - [3.1 Customer experience](#31-customer-experience)
    - [`FR-CUS-001` — Browse without personalization](#fr-cus-001-browse-without-personalization)
    - [`FR-CUS-002` — Set or change preferences](#fr-cus-002-set-or-change-preferences)
    - [`FR-CUS-003` — Recommend products](#fr-cus-003-recommend-products)
    - [`FR-CUS-004` — Search across participating shops](#fr-cus-004-search-across-participating-shops)
    - [`FR-CUS-005` — Filter marketplace results](#fr-cus-005-filter-marketplace-results)
    - [`FR-CUS-006` — Use visual search](#fr-cus-006-use-visual-search)
    - [`FR-CUS-007` — Shop from a Store Profile](#fr-cus-007-shop-from-a-store-profile)
    - [`FR-CUS-008` — Complete shopping from either entry point](#fr-cus-008-complete-shopping-from-either-entry-point)
    - [`FR-CUS-009` — Show seller identity](#fr-cus-009-show-seller-identity)
    - [`FR-CUS-010` — View product details](#fr-cus-010-view-product-details)
    - [`FR-CUS-011` — Compare products](#fr-cus-011-compare-products)
    - [`FR-CUS-012` — Select variant and branch](#fr-cus-012-select-variant-and-branch)
    - [`FR-CUS-013` — Virtual try-on](#fr-cus-013-virtual-try-on)
    - [`FR-CUS-014` — Build cross-shop outfits](#fr-cus-014-build-cross-shop-outfits)
    - [`FR-CUS-015` — Save and revisit products](#fr-cus-015-save-and-revisit-products)
    - [`FR-CUS-016` — Follow shops and watch products](#fr-cus-016-follow-shops-and-watch-products)
    - [`FR-CUS-017` — Provide product updates](#fr-cus-017-provide-product-updates)
    - [`FR-CUS-018` — Ask product questions](#fr-cus-018-ask-product-questions)
  - [3.2 Shopping and fulfillment](#32-shopping-and-fulfillment)
    - [`FR-ORD-001` — Submit reservation request](#fr-ord-001-submit-reservation-request)
    - [`FR-ORD-002` — Require merchant reservation decision](#fr-ord-002-require-merchant-reservation-decision)
    - [`FR-ORD-003` — Record reservation statuses](#fr-ord-003-record-reservation-statuses)
    - [`FR-ORD-004` — Show reservation fee distinctly](#fr-ord-004-show-reservation-fee-distinctly)
    - [`FR-ORD-005` — Submit delivery order](#fr-ord-005-submit-delivery-order)
    - [`FR-ORD-006` — Show delivery fee only for delivery](#fr-ord-006-show-delivery-fee-only-for-delivery)
    - [`FR-ORD-007` — Keep product amount distinct](#fr-ord-007-keep-product-amount-distinct)
    - [`FR-ORD-008` — Support delivery order updates](#fr-ord-008-support-delivery-order-updates)
    - [`FR-ORD-009` — Receive and review return request](#fr-ord-009-receive-and-review-return-request)
    - [`FR-ORD-010` — Require actual purchase confirmation](#fr-ord-010-require-actual-purchase-confirmation)
    - [`FR-ORD-011` — Enable review only after verified purchase](#fr-ord-011-enable-review-only-after-verified-purchase)
  - [3.3 Merchant workspace](#33-merchant-workspace)
    - [`FR-MER-001` — Create free merchant account](#fr-mer-001-create-free-merchant-account)
    - [`FR-MER-002` — Use free capabilities with real business information](#fr-mer-002-use-free-capabilities-with-real-business-information)
    - [`FR-MER-003` — Identify paid capabilities](#fr-mer-003-identify-paid-capabilities)
    - [`FR-MER-004` — Upgrade merchant account](#fr-mer-004-upgrade-merchant-account)
    - [`FR-MER-005` — Unlock paid capabilities only after payment success](#fr-mer-005-unlock-paid-capabilities-only-after-payment-success)
    - [`FR-MER-006` — Maintain one Store Profile per business](#fr-mer-006-maintain-one-store-profile-per-business)
    - [`FR-MER-007` — Maintain multiple branches](#fr-mer-007-maintain-multiple-branches)
    - [`FR-MER-008` — Invite staff and assign access](#fr-mer-008-invite-staff-and-assign-access)
    - [`FR-MER-009` — Maintain one catalog per shop](#fr-mer-009-maintain-one-catalog-per-shop)
    - [`FR-MER-010` — Show same catalog listing in two locations](#fr-mer-010-show-same-catalog-listing-in-two-locations)
    - [`FR-MER-011` — Maintain product variants](#fr-mer-011-maintain-product-variants)
    - [`FR-MER-012` — Use AI listing assistance with retailer review](#fr-mer-012-use-ai-listing-assistance-with-retailer-review)
    - [`FR-MER-013` — Bulk upload products](#fr-mer-013-bulk-upload-products)
    - [`FR-MER-014` — Maintain branch inventory independently](#fr-mer-014-maintain-branch-inventory-independently)
    - [`FR-MER-015` — Maintain branch prices](#fr-mer-015-maintain-branch-prices)
    - [`FR-MER-016` — Create collections and announcements](#fr-mer-016-create-collections-and-announcements)
    - [`FR-MER-017` — Review and decide reservation](#fr-mer-017-review-and-decide-reservation)
    - [`FR-MER-018` — Prepare and update reservation status](#fr-mer-018-prepare-and-update-reservation-status)
    - [`FR-MER-019` — Process delivery orders](#fr-mer-019-process-delivery-orders)
    - [`FR-MER-020` — Respond to customer questions](#fr-mer-020-respond-to-customer-questions)
    - [`FR-MER-021` — Review merchant performance](#fr-mer-021-review-merchant-performance)
    - [`FR-MER-022` — Identify unmet demand](#fr-mer-022-identify-unmet-demand)
    - [`FR-MER-023` — Forecast demand](#fr-mer-023-forecast-demand)
    - [`FR-MER-024` — Notify merchant of operational events](#fr-mer-024-notify-merchant-of-operational-events)
  - [3.4 Supporting capabilities](#34-supporting-capabilities)
    - [`FR-SYS-001` — Keep listing information consistent](#fr-sys-001-keep-listing-information-consistent)
    - [`FR-SYS-002` — Support purchase-confirmation gate](#fr-sys-002-support-purchase-confirmation-gate)
    - [`FR-SYS-003` — Review support cases](#fr-sys-003-review-support-cases)
    - [`FR-SYS-004` — Support POS/ERP testing recommendation](#fr-sys-004-support-poserp-testing-recommendation)
- [4. External interface requirements](#4-external-interface-requirements)
- [5. Non-functional requirements](#5-non-functional-requirements)
- [6. Business rules](#6-business-rules)
- [7. Data requirements — business level](#7-data-requirements-business-level)
  - [7.1 Conceptual relationships](#71-conceptual-relationships)
- [8. Use cases](#8-use-cases)
  - [`UC-001` — Discover products in Global Marketplace](#uc-001-discover-products-in-global-marketplace)
  - [`UC-002` — Search using an image](#uc-002-search-using-an-image)
  - [`UC-003` — Shop directly from Store Profile](#uc-003-shop-directly-from-store-profile)
  - [`UC-004` — Review and select product](#uc-004-review-and-select-product)
  - [`UC-005` — Save and follow products/shops](#uc-005-save-and-follow-productsshops)
  - [`UC-006` — Ask and answer product question](#uc-006-ask-and-answer-product-question)
  - [`UC-007` — Request in-store reservation](#uc-007-request-in-store-reservation)
  - [`UC-008` — Review reservation as merchant](#uc-008-review-reservation-as-merchant)
  - [`UC-009` — Place delivery order](#uc-009-place-delivery-order)
  - [`UC-010` — Process delivery order](#uc-010-process-delivery-order)
  - [`UC-011` — Review return/support case](#uc-011-review-returnsupport-case)
  - [`UC-012` — Submit verified review](#uc-012-submit-verified-review)
  - [`UC-013` — Start free account and upgrade](#uc-013-start-free-account-and-upgrade)
  - [`UC-014` — Set up business and branches](#uc-014-set-up-business-and-branches)
  - [`UC-015` — Create and publish product](#uc-015-create-and-publish-product)
  - [`UC-016` — Bulk upload catalog](#uc-016-bulk-upload-catalog)
  - [`UC-017` — Update branch inventory and prices](#uc-017-update-branch-inventory-and-prices)
  - [`UC-018` — Review merchant insights](#uc-018-review-merchant-insights)
  - [`UC-019` — Handle operational notification](#uc-019-handle-operational-notification)
  - [`UC-020` — Validate POS/ERP assumptions](#uc-020-validate-poserp-assumptions)
- [9. Acceptance criteria](#9-acceptance-criteria)
  - [Customer](#customer)
  - [Shopping and fulfillment](#shopping-and-fulfillment)
  - [Merchant](#merchant)
  - [Supporting](#supporting)
- [10. Open questions and unresolved requirements](#10-open-questions-and-unresolved-requirements)
- [11. Requirements traceability matrix](#11-requirements-traceability-matrix)
- [12. Glossary and revision history](#12-glossary-and-revision-history)

### Software Requirements Specification (SRS)

Business-level functional and quality requirements translated from the revised FitFind Product Journey Notes. Structured in an IEEE/ISO-style format for clarity; this document does not claim formal certification.

> **Document control**  
> Version 1.0 \| Team review  \|  Source: FitFind Product Journey Notes Revised

## Contents

| Section | Coverage |
| --- | --- |
| 1. Introduction | Purpose, scope, audience, conventions, definitions and references |
| 2. Overall description | Perspective, objectives, layers, actors, assumptions and boundaries |
| 3. Functional requirements | Customer, fulfillment, merchant and supporting requirements |
| 4. External interfaces | User-facing expectations and external dependencies |
| 5. Non-functional requirements | Supported quality needs and unresolved targets |
| 6. Business rules | Rules with stable IDs and status |
| 7. Business-level data requirements | Entities and conceptual relationships |
| 8. Use cases | Major customer, merchant and supporting interactions |
| 9. Acceptance criteria | Given/When/Then criteria for each functional requirement |
| 10. Open questions | TBD decisions and affected requirements |
| 11. Traceability matrix | Source-to-workflow/requirement/rule/use-case/criterion mapping |
| 12. Glossary and revision history | Definitions and document control |

## 1. Introduction

### 1.1 Purpose

This SRS specifies business-level FitFind behavior from the revised Product Journey Notes. It provides a shared, testable reference for product, design, engineering, QA and stakeholders while preserving Agreed Direction, Proposed Features, Working Assumptions and TBD decisions.

### 1.2 Product scope

FitFind connects customers with local physical fashion shops. Its product vision includes a Global Marketplace, one Store Profile per business and a private Merchant Dashboard. Customers can shop from either customer-facing entry point and choose in-store reservation or delivery. Retailers can begin with a free live account and may pay to unlock paid capabilities; the free/paid split is TBD.

### 1.3 Intended audience

Product Manager, Business Analyst, UI/UX Designer, Software Developers, QA/Test Engineers and project stakeholders.

### 1.4 Document conventions

“Shall” denotes an Agreed Direction expressed as system behavior. “Should/may” denotes a Proposed Feature. Requirement status identifies Agreed Direction, Proposed, Assumption, TBD, or Proposed / source conflict. Unknown rules are marked TBD — To Be Decided. Status does not set launch priority.

| Status | Meaning |
| --- | --- |
| Agreed Direction | Established by source; detailed sub-rules can remain TBD. |
| Proposed | In the intended product vision; not automatically approved for launch. |
| Assumption | Working interpretation that needs confirmation if it affects a product promise. |
| TBD | No fixed behavior should be inferred until decided. |
| Proposed / source conflict | Requested in one place but inconsistent with another source statement; not mandatory until resolved. |

### 1.5 Definitions and abbreviations

| Term | Definition |
| --- | --- |
| Global Marketplace | Shared shopping space for products from participating shops; customers can proceed from it without opening a Store Profile. |
| Store Profile / Storefront | One business’s branded customer-facing shop page. |
| Merchant Dashboard | Private workspace for owner and permitted employees. |
| Branch | Physical location of a business, with its own operational and stock information. |
| Product variant | A product option such as size or color. |
| Inventory / stock | Quantity/availability a branch reports; it is not a guaranteed hold. |
| Reservation | Customer request for a shop to review and prepare/hold an item; not confirmed until accepted and not proof of purchase. |
| Reservation fee | Fee applying to both fulfillment paths; amount and collection/refund rules TBD. |
| Delivery fee | Fee for delivery path only; amount and handling TBD. |
| Delivery order | Request to purchase an item for delivery, subject to stock and delivery process. |
| Verified-purchase review | Review that requires actual purchase confirmation. |
| POS/ERP | External retailer sales, product or inventory system, referenced here for testing. |

### 1.6 References

| Reference | Use |
| --- | --- |
| FitFind Product Journey Notes Revised, 14 pages | Primary source for product behavior, journeys, rules and open decisions. Page references below point to this PDF. |
| Current Product Workflows & SRS brief | Requested document structure and capability topics; conflicts are identified, not silently resolved. |
| Earlier direct FitFind direction in this project conversation | Removed AI listing assistance; relevant to conflict OQ-021. |

## 2. Overall description

### 2.1 Product perspective

FitFind is a multi-sided local fashion marketplace. Customer discovery is shared across retailers, while each business maintains one branded Store Profile and a private Merchant Dashboard. The same shop product listing supports both customer-facing entry points. In-store reservation/purchase and delivery are complementary paths in the product vision; first-release scope is unresolved.

### 2.2 Product objectives

| Objective | Source-aligned outcome |
| --- | --- |
| Help customers find local fashion | Search across shops or enter one Store Profile directly. |
| Support informed choices | Show seller, product/variant, branch-specific reported availability and price. |
| Connect customer intent to shop action | Merchant decides reservations; Pending remains unconfirmed. |
| Support alternative fulfillment | In-store reservation and delivery have separate fees/operations. |
| Help retailers manage one presence | One Store Profile/catalog per business, multiple branches and branch-level inventory. |
| Support phased merchant access | Free live use first; successful payment unlocks paid capability; feature split TBD. |

### 2.3 Product layers

#### **Layer:** Global Marketplace
- **User:** Customer
- **Purpose:** Shared discovery, search, filters, comparison, details and direct fulfillment.

#### **Layer:** Store Profile / Storefront
- **User:** Customer
- **Purpose:** One branded storefront per business; full shopping can continue there.

#### **Layer:** Merchant Dashboard
- **User:** Owner/authorized staff
- **Purpose:** Manage business, branches, catalog, reservations, delivery orders, conversations and performance.

### 2.4 User classes and actors

| Actor | Goal / scope |
| --- | --- |
| Customer | Discover, compare, select variant/branch, reserve or order delivery, ask questions and seek support/review. |
| Business owner / retailer | Operate one business profile and its branches/catalog; decide fulfillment requests. |
| Authorized employee | Perform assigned merchant actions if staff roles are enabled; permission model TBD. |
| FitFind | Present and connect product/shop information, route requests and reflect known states. |
| FitFind Support | Review proposed support/return cases; authority and policy TBD. |
| Payment dependency | External service implied by subscriptions/fees; provider/interface TBD. |
| Delivery dependency | Potential external delivery service; no provider selected. |
| POS/ERP test service | Sandbox/mock test context only; no production integration selected. |

### 2.5 Operating environment

Customer and merchant device/platform scope has not been established. This specification describes business behavior, not deployment architecture.

### 2.6 Assumptions and dependencies

| Item | Status / effect |
| --- | --- |
| Free live account can use available free capabilities with real business information. | Agreed direction; required fields/verification TBD. |
| Payment success unlocks paid capabilities. | Agreed direction; feature split, plans and billing TBD. |
| Merchant checks actual stock before confirming. | Working interpretation consistent with deliberate merchant decision. |
| Payment, delivery, notification and purchase-evidence services. | Dependencies implied by workflows; providers/contracts TBD. |
| Interest/browsing data may inform recommendations. | Proposed; privacy and data-use rules TBD. |
| AI listing assistance. | Conflict; Proposed / source conflict only, not an agreed feature. |

### 2.7 Product boundaries and constraints

| Product vision | Boundary / decision |
| --- | --- |
| Local physical shops; Men, Women, Kids; clothing, shoes and accessories. | MVP features and delivery launch timing undecided. |
| Two complete shopping entry points. | Store Profile visit is never a prerequisite. |
| One business profile and catalog; multiple branches. | No duplicated product catalog or stock-transfer capability. |
| Branch-level reported availability and potential price differences. | Displayed quantity is not a hold. |
| Reservation and delivery are complementary. | Fees, payment timing, statuses, provider and return rules TBD. |
| POS/ERP tests can use sandbox or lightweight mock. | No production provider/integration confirmed. |
| Recommendations, unmet-demand signals and forecasts. | Proposed; no automatic MVP commitment. |

## 3. Product features and functional requirements

Every functional requirement has a unique ID, status and linked acceptance criterion in Section 9. Proposed items do not become mandatory MVP requirements by appearing here.

### 3.1 Customer experience

#### `FR-CUS-001` — Browse without personalization

Status: Agreed Direction  |  Source: PDF p.3, 1.1

The system shall allow a customer to begin browsing the Global Marketplace without completing preference setup.

#### `FR-CUS-002` — Set or change preferences

Status: Proposed  |  Source: PDF p.3, 1.2

The system should allow customers to select or change audience, style, color, budget and favorite shop/brand preferences.

#### `FR-CUS-003` — Recommend products

Status: Proposed  |  Source: PDF p.3, 1.3; p.13 AI data

The system should recommend products using customer interests, browsing activity and stated preferences. Recommendation policy, data use and launch priority are TBD.

#### `FR-CUS-004` — Search across participating shops

Status: Agreed Direction  |  Source: PDF p.2 product concept; p.3, 1.4

The system shall return marketplace product results from participating shops without requiring the customer to identify a seller first.

#### `FR-CUS-005` — Filter marketplace results

Status: Proposed  |  Source: PDF p.3, 1.4

The system should let customers filter results by relevant attributes such as size, color, price and style.

#### `FR-CUS-006` — Use visual search

Status: Proposed  |  Source: PDF p.3, 1.5

The system should accept an image for visual product discovery and describe results as visually similar rather than guaranteed exact matches.

#### `FR-CUS-007` — Shop from a Store Profile

Status: Agreed Direction  |  Source: PDF p.2-3, 1.6

The system shall allow a customer to enter a business Store Profile and browse its identity, catalog, branches, collections, offers and announcements.

#### `FR-CUS-008` — Complete shopping from either entry point

Status: Agreed Direction  |  Source: PDF p.2, 1.6, 1.12

The system shall allow customers to continue reservation or delivery shopping from the Global Marketplace or Store Profile without making Store Profile navigation mandatory.

#### `FR-CUS-009` — Show seller identity

Status: Agreed Direction  |  Source: PDF p.2 product concept

The system shall show the seller/shop identity on marketplace product listings or details.

#### `FR-CUS-010` — View product details

Status: Agreed Direction  |  Source: PDF p.4, 1.7-1.8

The system shall present available product images, description, options, seller identity, price and availability information.

#### `FR-CUS-011` — Compare products

Status: Proposed  |  Source: PDF p.4, 1.7; p.13

The system should allow comparison of exact matches and similar alternatives while distinguishing exact from similar results. Comparison attributes are TBD.

#### `FR-CUS-012` — Select variant and branch

Status: Agreed Direction  |  Source: PDF p.4, 1.8

The system shall let a customer select applicable product variant and physical branch and show reported branch availability and applicable price.

#### `FR-CUS-013` — Virtual try-on

Status: Proposed  |  Source: PDF p.4, 1.9

The system may provide AI-assisted virtual try-on; it shall not represent preview accuracy as guaranteed fit.

#### `FR-CUS-014` — Build cross-shop outfits

Status: Proposed  |  Source: PDF p.4, 1.9

The system may let customers combine items from multiple shops in an Outfit Builder while keeping each item separate and linked to its own listing and seller.

#### `FR-CUS-015` — Save and revisit products

Status: Proposed  |  Source: PDF p.4, 1.10; p.13

The system should support wishlist and recently viewed product access. Sign-in requirements are TBD.

#### `FR-CUS-016` — Follow shops and watch products

Status: Proposed  |  Source: PDF p.4, 1.10

The system should let customers follow shops and watch products or variants for relevant updates.

#### `FR-CUS-017` — Provide product updates

Status: Proposed  |  Source: PDF p.4, 1.10; p.13 Notifications

The system may notify customers about restocks, price changes, new collections and shop announcements according to preferences and rules still TBD.

#### `FR-CUS-018` — Ask product questions

Status: Proposed  |  Source: PDF p.4, 1.11

The system should allow customers to submit product questions and route them to shop staff or a controlled AI-assisted/hybrid process.

### 3.2 Shopping and fulfillment

#### `FR-ORD-001` — Submit reservation request

Status: Agreed Direction  |  Source: PDF p.5, Path A

The system shall allow a customer to submit a reservation for a selected product, variant, quantity and physical branch.

#### `FR-ORD-002` — Require merchant reservation decision

Status: Agreed Direction  |  Source: PDF p.5, p.8, 1.13

The system shall not treat a submitted reservation as confirmed until a merchant makes a decision.

#### `FR-ORD-003` — Record reservation statuses

Status: Agreed Direction  |  Source: PDF p.5-6, 1.13

The system shall support the documented reservation statuses Pending, Confirmed, Rejected, Ready, Expired, Cancelled and Completed, subject to detailed transition policy TBD.

#### `FR-ORD-004` — Show reservation fee distinctly

Status: Agreed Direction  |  Source: PDF p.5 fee table; p.13

The system shall distinguish the reservation fee from the product purchase amount for both fulfillment paths. Amount and collection timing are TBD.

#### `FR-ORD-005` — Submit delivery order

Status: Agreed Direction  |  Source: PDF p.5, Path B

The system shall allow a customer to choose delivery and submit a selected product/variant/quantity order from either shopping entry point.

#### `FR-ORD-006` — Show delivery fee only for delivery

Status: Agreed Direction  |  Source: PDF p.5 fee table; p.13

The system shall distinguish the delivery fee from product amount and apply delivery-fee presentation only to the delivery path. Amount and calculation are TBD.

#### `FR-ORD-007` — Keep product amount distinct

Status: Agreed Direction  |  Source: PDF p.5 fee table; p.13 Payments

The system shall present the product amount separately from reservation and delivery fees. Product payment timing for delivery is TBD.

#### `FR-ORD-008` — Support delivery order updates

Status: TBD  |  Source: PDF p.5-6, p.8, p.13

The system’s delivery updates and statuses shall follow an approved order lifecycle; no final status names are established.

#### `FR-ORD-009` — Receive and review return request

Status: Proposed  |  Source: PDF p.6, 1.14; p.13 Returns

The system should let a customer contact FitFind Support about a purchased product and allow case review under a policy to be defined.

#### `FR-ORD-010` — Require actual purchase confirmation

Status: Agreed Direction  |  Source: PDF p.6, 1.15; p.11

The system shall keep reservation status separate from actual purchase status for both in-store and delivery purchases.

#### `FR-ORD-011` — Enable review only after verified purchase

Status: Agreed Direction  |  Source: PDF p.6, p.11

The system shall make verified-purchase review eligibility dependent on reliable confirmation of actual in-store or delivery purchase.

### 3.3 Merchant workspace

#### `FR-MER-001` — Create free merchant account

Status: Agreed Direction  |  Source: PDF p.7, 2.1; p.12

The system shall allow a retailer to start with a free live merchant account. Account fields and verification rules are TBD.

#### `FR-MER-002` — Use free capabilities with real business information

Status: Agreed Direction  |  Source: PDF p.7, 2.1-2.3

The system shall make available free capabilities usable in the live workspace with the retailer’s real business information.

#### `FR-MER-003` — Identify paid capabilities

Status: TBD  |  Source: PDF p.7, 2.4; p.13 Retailer free access

The system shall identify which capabilities require payment once the free/paid feature split is decided.

#### `FR-MER-004` — Upgrade merchant account

Status: Agreed Direction  |  Source: PDF p.7, 2.5; p.13

The system shall support an optional upgrade/payment path from a live free account. Plans, prices and billing terms are TBD.

#### `FR-MER-005` — Unlock paid capabilities only after payment success

Status: Agreed Direction  |  Source: PDF p.7, 2.6; p.13

The system shall unlock paid capabilities only after successful payment is confirmed. Which features are paid is TBD; no specific AI feature is assumed paid.

#### `FR-MER-006` — Maintain one Store Profile per business

Status: Agreed Direction  |  Source: PDF p.2, p.8, 2.7

The system shall associate one Store Profile with each business.

#### `FR-MER-007` — Maintain multiple branches

Status: Agreed Direction  |  Source: PDF p.8, 2.8

The system shall allow one business to maintain multiple physical branches with location and operating information.

#### `FR-MER-008` — Invite staff and assign access

Status: Proposed  |  Source: PDF p.8, 2.9; p.13 Staff roles

The system should allow owners to invite employees and assign permissions; role definitions and permission matrix are TBD.

#### `FR-MER-009` — Maintain one catalog per shop

Status: Agreed Direction  |  Source: PDF p.2, p.8, 2.10

The system shall allow a shop to create and maintain each product listing once in its catalog.

#### `FR-MER-010` — Show same catalog listing in two locations

Status: Agreed Direction  |  Source: PDF p.2, p.8, p.11

The system shall use the same shop product listing in the Global Marketplace and its Store Profile.

#### `FR-MER-011` — Maintain product variants

Status: Agreed Direction  |  Source: PDF p.8, 2.10

The system shall associate product options such as size and color with the relevant product listing.

#### `FR-MER-012` — Use AI listing assistance with retailer review

Status: Proposed / conflict  |  Source: PDF p.2 residual boundary rule; current workflow brief §6 Catalog Management

If AI listing assistance is approved for the product, the system may suggest product titles/descriptions/details; retailer review and approval of generated claims is required before publishing. This feature conflicts with an earlier direct request to remove it and with its absence from the current journey steps.

#### `FR-MER-013` — Bulk upload products

Status: Proposed  |  Source: PDF p.9, 2.13; p.13 Bulk upload

The system should support spreadsheet upload, preview, row-level validation, corrections and merchant approval before applying valid changes.

#### `FR-MER-014` — Maintain branch inventory independently

Status: Agreed Direction  |  Source: PDF p.9, 2.14

The system shall allow stock and variant availability to be recorded independently for each branch.

#### `FR-MER-015` — Maintain branch prices

Status: Agreed Direction  |  Source: PDF p.9, 2.14; p.13 Branch prices

The system shall support branch-specific prices where applicable.

#### `FR-MER-016` — Create collections and announcements

Status: Proposed  |  Source: PDF p.9, 2.15; p.13 Promotions

The system should let a retailer create collections, promotions and announcements subject to content rules still TBD.

#### `FR-MER-017` — Review and decide reservation

Status: Agreed Direction  |  Source: PDF p.9, 2.16

The system shall route reservation requests to the shop/selected branch and allow a merchant decision to confirm, reject or request clarification.

#### `FR-MER-018` — Prepare and update reservation status

Status: Agreed Direction  |  Source: PDF p.9, 2.17

The system shall let a merchant mark an accepted item Ready when prepared and later close a reservation under policy TBD.

#### `FR-MER-019` — Process delivery orders

Status: Agreed Direction  |  Source: PDF p.9, 2.18

The system shall present submitted delivery orders to the merchant with product/variant, quantity, customer and relevant branch context, and support preparation/update under a TBD delivery process.

#### `FR-MER-020` — Respond to customer questions

Status: Proposed  |  Source: PDF p.10, 2.19; p.13 AI

The system should support manual responses and may support controlled AI/hybrid assistance using current shop information with escalation when uncertain.

#### `FR-MER-021` — Review merchant performance

Status: Proposed  |  Source: PDF p.10, 2.21

The system may show product views, saves, follows, questions, reservations, response times and confirmed outcomes, distinguishing activity from actual sales.

#### `FR-MER-022` — Identify unmet demand

Status: Proposed  |  Source: PDF p.8, 2.11

The system may identify products, sizes or categories customers search for but cannot find in available inventory.

#### `FR-MER-023` — Forecast demand

Status: Proposed  |  Source: PDF p.8, 2.12; p.13 AI data

The system may use historical customer activity and inventory or sales data where available to forecast future demand; forecast period and confidence behavior are TBD.

#### `FR-MER-024` — Notify merchant of operational events

Status: Proposed  |  Source: PDF p.10, 2.22; p.13 Notifications

The system should notify the appropriate owner/team about supported reservations, delivery orders, questions, stock changes, imports and staff actions under rules TBD.

### 3.4 Supporting capabilities

#### `FR-SYS-001` — Keep listing information consistent

Status: Agreed Direction  |  Source: PDF p.2; p.11 cross-functional

The system shall maintain consistent product, variant and relevant availability information across Global Marketplace and Store Profile views of the same listing.

#### `FR-SYS-002` — Support purchase-confirmation gate

Status: TBD  |  Source: PDF p.6, p.11, p.13 Purchase verification

The system shall use a reliable purchase-confirmation method for in-store and delivery purchases before marking a review as verified; the method is TBD.

#### `FR-SYS-003` — Review support cases

Status: Proposed  |  Source: PDF p.6, 1.14; p.11

The system should support FitFind Support review of customer return cases and any approved resolution under policy TBD.

#### `FR-SYS-004` — Support POS/ERP testing recommendation

Status: Proposed  |  Source: PDF p.11, section 3

Product validation may use provider sandboxes and should prefer a lightweight mock POS/ERP service for fashion variants and multiple branches; this is not a production integration commitment.

## 4. External interface requirements

Only interfaces supported or implied by the source are documented. No provider, endpoint, API contract or technical implementation is selected.

#### **Interface:** Customer interface
- **Business-level expectation:** Expose Marketplace, Store Profile, seller, product/variant/branch data, fulfillment choices, statuses and fee distinctions.
- **TBD dependency:** Platforms, sign-in, accessibility and layout.

#### **Interface:** Merchant interface
- **Business-level expectation:** Expose live free/paid workspace access, profile/branch/catalog operations and customer requests.
- **TBD dependency:** Web/mobile, role model, publication controls.

#### **Interface:** Payment dependency
- **Business-level expectation:** Confirm subscription payment before paid features unlock; customer fee paths remain unsettled.
- **TBD dependency:** Provider, plans, prices, timing, billing, refunds and failures.

#### **Interface:** Delivery dependency
- **Business-level expectation:** Support order handling and updates made available to customer and merchant.
- **TBD dependency:** Provider, coverage, status lifecycle, failed/refused orders.

#### **Interface:** POS/ERP testing
- **Business-level expectation:** Validate product/variant/branch/quantity/price behavior with sandbox or mock service.
- **TBD dependency:** Testing model only; production integration/provider TBD.

#### **Interface:** Notifications
- **Business-level expectation:** Present relevant customer or merchant updates under configured rules.
- **TBD dependency:** Channels, event list, preferences and delivery guarantees.

## 5. Non-functional requirements

No numeric quality targets are present in the source. The requirements below preserve supported needs and explicitly identify measurement decisions still needed.

#### **ID / Area:** `NFR-001` — Data consistency
- **Status:** Agreed Direction
- **Requirement:** The same product listing and approved information should be consistent in the Global Marketplace and Store Profile.
- **Target / decision needed:** No propagation latency target is specified; define acceptable update timing.

#### **ID / Area:** `NFR-002` — Inventory freshness
- **Status:** TBD
- **Requirement:** Availability should be clearly represented as reported information and must not imply a guaranteed hold.
- **Target / decision needed:** Refresh cadence, stale-data threshold and stale-state messaging need decisions.

#### **ID / Area:** `NFR-003` — Usability and clarity
- **Status:** Proposed
- **Requirement:** Customer fee types, reservation states and fulfillment choices should be understandable to non-technical users.
- **Target / decision needed:** Usability measures and validation approach TBD.

#### **ID / Area:** `NFR-004` — Privacy of customer signals
- **Status:** TBD
- **Requirement:** Use of interests and browsing activity for recommendations must follow privacy and data-use decisions.
- **Target / decision needed:** Consent, retention, access and applicable rules TBD.

#### **ID / Area:** `NFR-005` — Access control
- **Status:** Proposed
- **Requirement:** Merchant workspace actions should reflect owner/employee permissions when staff capability is enabled.
- **Target / decision needed:** Roles, authorization granularity and audit scope TBD.

#### **ID / Area:** `NFR-006` — Performance
- **Status:** TBD
- **Requirement:** Search, product detail and merchant workflows should respond within target times to be agreed.
- **Target / decision needed:** No numeric service target is present in source.

#### **ID / Area:** `NFR-007` — Availability and reliability
- **Status:** TBD
- **Requirement:** Marketplace and merchant operations should have availability and recovery expectations defined before launch.
- **Target / decision needed:** Service levels, support windows and recovery targets TBD.

#### **ID / Area:** `NFR-008` — Accessibility
- **Status:** TBD
- **Requirement:** Customer and merchant interfaces should be assessed for accessible use.
- **Target / decision needed:** Applicable standard and measurable conformance target not selected.

#### **ID / Area:** `NFR-009` — Scalability
- **Status:** TBD
- **Requirement:** The service should accommodate participating shops, products and branches as adoption grows.
- **Target / decision needed:** Volume forecast and capacity targets TBD.

#### **ID / Area:** `NFR-010` — AI insight transparency
- **Status:** Proposed
- **Requirement:** Recommendations and forecasts should be presented as suggestions/estimates, not guarantees; uncertainty/data limitations should be clear where enabled.
- **Target / decision needed:** Explanation detail, confidence treatment and quality measures TBD.

## 6. Business rules

#### **Rule / ID:** `BR-001` — Three connected layers
- **Status:** Agreed Direction
- **Rule:** FitFind includes the Global Marketplace, individual Store Profiles and Merchant Dashboard.

#### **Rule / ID:** `BR-002` — Two complete shopping entry points
- **Status:** Agreed Direction
- **Rule:** Customers may shop from Global Marketplace or Store Profile.

#### **Rule / ID:** `BR-003` — Store Profile visit is optional
- **Status:** Agreed Direction
- **Rule:** A customer need not visit a Store Profile before reservation or delivery order.

#### **Rule / ID:** `BR-004` — One Store Profile; multiple branches
- **Status:** Agreed Direction
- **Rule:** Each business has one Store Profile and may have multiple physical branches.

#### **Rule / ID:** `BR-005` — One catalog, one listing
- **Status:** Agreed Direction
- **Rule:** A shop creates each product listing once; same listing appears in Global Marketplace and Store Profile.

#### **Rule / ID:** `BR-006` — Branch independence
- **Status:** Agreed Direction
- **Rule:** A business may manage physical branches under one profile.

#### **Rule / ID:** `BR-007` — Branch stock/availability can differ
- **Status:** Agreed Direction
- **Rule:** Inventory and availability are managed separately by branch and variant.

#### **Rule / ID:** `BR-008` — Branch prices can differ
- **Status:** Agreed Direction
- **Rule:** Price may differ by branch.

#### **Rule / ID:** `BR-009` — Displayed stock is not a hold
- **Status:** Agreed Direction
- **Rule:** Displayed quantity does not guarantee that item is held for a customer.

#### **Rule / ID:** `BR-010` — Pending is undecided
- **Status:** Agreed Direction
- **Rule:** Pending reservation means the shop has not decided; it is not confirmed.

#### **Rule / ID:** `BR-011` — Merchant decision required
- **Status:** Agreed Direction
- **Rule:** Reservation request requires an actual shop decision.

#### **Rule / ID:** `BR-012` — Reservation is not purchase proof
- **Status:** Agreed Direction
- **Rule:** Reservation or reservation completion alone is not proof of purchase.

#### **Rule / ID:** `BR-013` — Verified review needs actual purchase
- **Status:** Agreed Direction
- **Rule:** Verified-purchase review requires actual in-store or delivery purchase confirmation.

#### **Rule / ID:** `BR-014` — Two fulfillment paths
- **Status:** Agreed Direction
- **Rule:** Product vision supports in-store reservation/purchase and delivery/shipping.

#### **Rule / ID:** `BR-015` — Reservation fee applies to both paths
- **Status:** Agreed Direction
- **Rule:** Reservation fee applies to in-store reservation and delivery order; amount and collection/refund rules are TBD.

#### **Rule / ID:** `BR-016` — Delivery fee applies only to delivery
- **Status:** Agreed Direction
- **Rule:** Delivery fee is associated with delivery path only; amount/calculation is TBD.

#### **Rule / ID:** `BR-017` — Fee amounts remain distinct
- **Status:** Agreed Direction
- **Rule:** Product purchase amount, reservation fee and applicable delivery fee are separate amounts.

#### **Rule / ID:** `BR-018` — Returns and fee refunds are not finalized
- **Status:** Proposed/TBD
- **Rule:** Support review is proposed; any full-fee refund may be approved under a future policy. No automatic refund is promised.

#### **Rule / ID:** `BR-019` — Free live merchant account and paid unlock
- **Status:** Agreed Direction
- **Rule:** Retailer may begin using free live capabilities with real shop information; successful payment unlocks paid capabilities. Feature split/plans/prices TBD.

#### **Rule / ID:** `BR-020` — Roles and operational notifications are unsettled
- **Status:** Proposed/TBD
- **Rule:** Staff permissions and notification behavior require decisions before becoming mandatory detailed behavior.

#### **Rule / ID:** `BR-021` — AI listing assistance source conflict
- **Status:** Proposed / conflict
- **Rule:** If adopted, AI-generated product claims require retailer review/approval. A prior direct request removed this feature; the current documentation brief asks to include it. Do not treat as agreed until reconciled.

#### **Rule / ID:** `BR-022` — No stock transfers
- **Status:** Agreed Direction
- **Rule:** Do not include any branch-to-branch stock movement capability. Branch stock is updated independently.

#### **Rule / ID:** `BR-023` — Delivery operations unspecified
- **Status:** TBD
- **Rule:** Provider, service area, order statuses and failed/refused delivery handling remain open.

#### **Rule / ID:** `BR-024` — AI recommendations/insights remain proposed
- **Status:** Proposed
- **Rule:** Recommendations, unmet-demand detection and demand forecasts support decision-making; scope, data and launch priority remain unsettled.

#### **Rule / ID:** `BR-025` — POS/ERP mock is testing recommendation
- **Status:** Proposed
- **Rule:** Lightweight mock inventory service is recommended for validation; sandbox alternatives may be used. Neither establishes a production provider integration.

## 7. Data requirements — business level

The following are business concepts and relationships, not database tables or implementation structures. Cardinality is stated only where established.

| Business entity | Meaning / relationships |
| --- | --- |
| Customer | Shopper; preference/follow/watch data may be associated, with account behavior TBD. |
| Business | Retailer identity; has one Store Profile and may have several physical Branches. |
| Store Profile | One branded customer-facing presence per business. |
| Branch | Physical business location with independent stock and possibly different prices. |
| Employee | Staff member invited by owner; role/permissions TBD. |
| Product Catalog | One catalog per shop/business. |
| Product | Created once in catalog and shown in both customer-facing locations. |
| Product Variant | Product option such as size or color. |
| Branch Inventory | Reported availability/quantity for variant and branch; not a guaranteed hold. |
| Price | Product amount, potentially branch-specific; default/override model TBD. |
| Reservation | Request linked to product, variant, quantity and branch; has merchant decision/status. |
| Delivery Order | Request for delivery; applicable branch and lifecycle TBD. |
| Payment / Fee | Product amount, reservation fee and delivery fee are distinct; collection/refunds TBD. |
| Subscription / Entitlement | Free account and paid access state; plan and feature mapping TBD. |
| Customer Question | Shop/product question and response; retention/status TBD. |
| Support Case | Proposed return/support case and relevant purchase/order context. |
| Review | Review with verified state only after actual purchase confirmation. |
| Collection / Promotion / Announcement | Merchant customer-facing content; rules and expiry TBD. |
| Notification | Customer/merchant event information; channels/preferences TBD. |
| Insight | Proposed recommendations, unmet-demand detection and demand forecast using permitted available data. |

### 7.1 Conceptual relationships

| Relationship | Established meaning / status |
| --- | --- |
| Business — Store Profile | One profile per business (Agreed). |
| Business — Branch | One business may have multiple branches (Agreed). |
| Business — Catalog | One catalog per shop (Agreed). |
| Catalog — Product — Variant | Product created once; variants belong to product (Agreed direction). |
| Product — Marketplace / Store Profile | Same listing in both entry points (Agreed). |
| Branch — Inventory — Variant | Availability can differ by branch (Agreed). |
| Branch — Price | Prices may differ; default/override TBD. |
| Reservation — Product/Variant/Branch | Selected context carried in request; multi-item rule TBD. |
| Delivery Order — Product/Variant/Branch | Selected item/variant and relevant branch as applicable; branch requirement TBD. |
| Purchase — Review | Actual confirmed purchase gates verified review; evidence method TBD. |
| Customer — Follow/Watch/Subscription | Account and retention behavior TBD. |
| Support Case — Purchase/Order | May use context for case review; exact relationships TBD. |

## 8. Use cases

Proposed behavior remains conditional on approval; TBD rules are not silently completed.

### `UC-001` — Discover products in Global Marketplace

| Use case field | Definition |
| --- | --- |
| Primary Actor | Customer |
| Goal | Find and shop across participating retailers without knowing the seller. |
| Preconditions | Marketplace is available; login need remains TBD. |
| Trigger | Customer opens Marketplace. |
| Main Success Scenario | Customer searches/browses; applies filters; sees products from multiple shops with seller identity; opens details; selects fulfillment without mandatory Store Profile visit. |
| Alternative Flows | Personalization can be skipped; optional filters can be changed; shop identity may open Store Profile. |
| Exception Flows | No results or service issue leads to search recovery. |
| Postconditions | Customer has a product selection or next discovery path. |
| Related Functional Requirements / Workflows | `FR-CUS-001`/003/004/005/008/009; `WF-CUS-001`/002 |
| Related Business Rules / Acceptance Criteria | `BR-002`/003/005; AC-CUS-001..005 |

### `UC-002` — Search using an image

| Use case field | Definition |
| --- | --- |
| Primary Actor | Customer |
| Goal | Find visually similar products. |
| Preconditions | Visual search is enabled; image can be supplied. |
| Trigger | Customer selects image search. |
| Main Success Scenario | Submit image; system presents visually similar marketplace results; customer opens a listing. |
| Alternative Flows | Use camera/upload where supported; refine through text filters. |
| Exception Flows | No result or image error offers ordinary search. |
| Postconditions | Customer can continue discovery without exact-match promise. |
| Related Functional Requirements / Workflows | `FR-CUS-006`; `WF-CUS-004` |
| Related Business Rules / Acceptance Criteria | `BR-024`; AC-CUS-006 |

### `UC-003` — Shop directly from Store Profile

| Use case field | Definition |
| --- | --- |
| Primary Actor | Customer |
| Goal | Browse and shop one retailer directly. |
| Preconditions | Store Profile exists. |
| Trigger | Customer opens Store Profile. |
| Main Success Scenario | Browse shop identity/catalog/branches; open product; select variant and branch; choose reservation/delivery. |
| Alternative Flows | Customer can return to marketplace but need not. |
| Exception Flows | Unavailable item can lead to other branch/product. |
| Postconditions | Customer shops within Store Profile entry. |
| Related Functional Requirements / Workflows | `FR-CUS-007`/008/009; `WF-CUS-003` |
| Related Business Rules / Acceptance Criteria | `BR-002`/003/004/005; AC-CUS-007/008 |

### `UC-004` — Review and select product

| Use case field | Definition |
| --- | --- |
| Primary Actor | Customer |
| Goal | Compare listing details and choose branch-specific variant. |
| Preconditions | Product details exist. |
| Trigger | Customer opens listing. |
| Main Success Scenario | Review seller/details; compare exact/similar; select variant and branch; view reported availability/price. |
| Alternative Flows | Use virtual try-on/outfit if enabled. |
| Exception Flows | Unavailable variant or stale stock leads to recovery. |
| Postconditions | Selected listing/variant/branch ready for fulfillment. |
| Related Functional Requirements / Workflows | `FR-CUS-010`/011/012/013/014; `WF-CUS-005`/006 |
| Related Business Rules / Acceptance Criteria | `BR-005`/007/008/009; AC-CUS-010..014 |

### `UC-005` — Save and follow products/shops

| Use case field | Definition |
| --- | --- |
| Primary Actor | Customer |
| Goal | Revisit choices and receive relevant updates. |
| Preconditions | Required account rules satisfied once decided. |
| Trigger | Customer saves/follows/watches. |
| Main Success Scenario | Save item; follow shop or watch variant; later revisit item/update. |
| Alternative Flows | Change preferences or remove saved relationship. |
| Exception Flows | No longer available item displays current state. |
| Postconditions | Saved/follow/watch state is current. |
| Related Functional Requirements / Workflows | `FR-CUS-015`/016/017; `WF-CUS-007` |
| Related Business Rules / Acceptance Criteria | `BR-005`/008; AC-CUS-015..017 |

### `UC-006` — Ask and answer product question

| Use case field | Definition |
| --- | --- |
| Primary Actor | Customer |
| Goal | Get shop-specific product information. |
| Preconditions | Question feature available. |
| Trigger | Customer submits question. |
| Main Success Scenario | Route to merchant; staff answers or controlled AI/hybrid process is used; response delivered. |
| Alternative Flows | Ask for clarification or escalate. |
| Exception Flows | Uncertain stock/product fact is not invented. |
| Postconditions | Customer has an answer or known unresolved question. |
| Related Functional Requirements / Workflows | `FR-CUS-018`, `FR-MER-020`; `WF-CUS-008`/`WF-MER-013` |
| Related Business Rules / Acceptance Criteria | `BR-007`/009; AC-CUS-018/AC-MER-020 |

### `UC-007` — Request in-store reservation

| Use case field | Definition |
| --- | --- |
| Primary Actor | Customer |
| Goal | Have a shop consider preparing an item for branch visit. |
| Preconditions | Product/variant/branch selected; fee process TBD. |
| Trigger | Customer submits request. |
| Main Success Scenario | Review separate fee; submit; record Pending; merchant decides; customer visits after acceptance and chooses purchase. |
| Alternative Flows | Clarification, rejection, other branch. |
| Exception Flows | Pending timeout/stock change handled under TBD policy. |
| Postconditions | Reservation result recorded, separate from purchase. |
| Related Functional Requirements / Workflows | `FR-ORD-001`/002/003/004; `WF-CUS-009`/010 |
| Related Business Rules / Acceptance Criteria | `BR-009`/010/011/012/015/017; AC-ORD-001..004 |

### `UC-008` — Review reservation as merchant

| Use case field | Definition |
| --- | --- |
| Primary Actor | Merchant |
| Goal | Decide whether branch can fulfill a request. |
| Preconditions | Pending request exists. |
| Trigger | Request routed to merchant. |
| Main Success Scenario | Check actual stock; confirm/reject/clarify; prepare/Ready; close later. |
| Alternative Flows | Clarification loop to customer. |
| Exception Flows | Unavailable stock leads to rejection or approved recovery. |
| Postconditions | Request status reflects actual merchant decision. |
| Related Functional Requirements / Workflows | `FR-ORD-002`/003, `FR-MER-017`/018; `WF-MER-010`/011 |
| Related Business Rules / Acceptance Criteria | `BR-009`/010/011/012; AC-ORD-002/003, AC-MER-017/018 |

### `UC-009` — Place delivery order

| Use case field | Definition |
| --- | --- |
| Primary Actor | Customer |
| Goal | Order item for delivery from either entry point. |
| Preconditions | Delivery available in chosen location; fee/payment rules TBD. |
| Trigger | Customer chooses delivery. |
| Main Success Scenario | Select item/variant/quantity; review product/reservation/delivery amounts; submit order to merchant. |
| Alternative Flows | Could return to in-store path before submission. |
| Exception Flows | Cannot fulfill/payment failure handled with policy TBD. |
| Postconditions | Order recorded for merchant review. |
| Related Functional Requirements / Workflows | `FR-ORD-005`/006/007; `WF-CUS-011` |
| Related Business Rules / Acceptance Criteria | `BR-014`/015/016/017; AC-ORD-005..007 |

### `UC-010` — Process delivery order

| Use case field | Definition |
| --- | --- |
| Primary Actor | Merchant |
| Goal | Check and prepare order and communicate progress. |
| Preconditions | Order submitted. |
| Trigger | Order reaches merchant. |
| Main Success Scenario | Review item/variant/branch; check availability; prepare; communicate available updates; delivery process completes. |
| Alternative Flows | Alternative when unavailable. |
| Exception Flows | Failed/refused delivery policy TBD. |
| Postconditions | Known outcome available; purchase confirmation separate. |
| Related Functional Requirements / Workflows | `FR-MER-019`, `FR-ORD-008`; `WF-MER-012`/`WF-CUS-012` |
| Related Business Rules / Acceptance Criteria | `BR-012`/014/016/023; AC-MER-019, AC-ORD-008 |

### `UC-011` — Review return/support case

| Use case field | Definition |
| --- | --- |
| Primary Actor | Customer; FitFind Support |
| Goal | Request a return/resolution for purchased item. |
| Preconditions | Purchase/order context available if possible; policy TBD. |
| Trigger | Customer contacts Support. |
| Main Success Scenario | Submit reason; Support reviews; requests merchant info if needed; determines and communicates resolution under policy. |
| Alternative Flows | Customer adds information. |
| Exception Flows | Policy/evidence missing keeps case unresolved. |
| Postconditions | Case outcome recorded; no refund promise invented. |
| Related Functional Requirements / Workflows | `FR-ORD-009`, `FR-SYS-003`; `WF-CUS-013`/`WF-SYS-003` |
| Related Business Rules / Acceptance Criteria | `BR-018`; AC-ORD-009, AC-SYS-003 |

### `UC-012` — Submit verified review

| Use case field | Definition |
| --- | --- |
| Primary Actor | Customer |
| Goal | Review product after actual purchase. |
| Preconditions | Actual purchase reliably confirmed; confirmation method TBD. |
| Trigger | Customer opens review action. |
| Main Success Scenario | System checks purchase; enables review only after confirmation; customer submits. |
| Alternative Flows | Wait/contact support if unconfirmed. |
| Exception Flows | Disputed/missing evidence blocks verified label. |
| Postconditions | Review eligibility reflects confirmed purchase. |
| Related Functional Requirements / Workflows | `FR-ORD-010`/011, `FR-SYS-002`; `WF-CUS-014` |
| Related Business Rules / Acceptance Criteria | `BR-012`/013; AC-ORD-010/011, AC-SYS-002 |

### `UC-013` — Start free account and upgrade

| Use case field | Definition |
| --- | --- |
| Primary Actor | Retailer / owner |
| Goal | Use free live capabilities and optionally pay to unlock paid ones. |
| Preconditions | Retailer can register; plan definitions TBD. |
| Trigger | Retailer creates account or chooses upgrade. |
| Main Success Scenario | Create live free account; use real business info/free functions; view paid limits; choose upgrade; successful payment unlocks paid features. |
| Alternative Flows | Keep free access; failed payment does not unlock paid access. |
| Exception Flows | Verification/entitlement status is communicated. |
| Postconditions | Current entitlements reflect payment confirmation. |
| Related Functional Requirements / Workflows | `FR-MER-001`..005; `WF-MER-001`/002 |
| Related Business Rules / Acceptance Criteria | `BR-019`; AC-MER-001..005 |

### `UC-014` — Set up business and branches

| Use case field | Definition |
| --- | --- |
| Primary Actor | Owner |
| Goal | Create one business Store Profile and branch records, then invite staff. |
| Preconditions | Free/live account. |
| Trigger | Owner begins setup. |
| Main Success Scenario | Enter business details; set Store Profile; add branches; invite staff/assign permissions if feature available. |
| Alternative Flows | Update profile or branch. |
| Exception Flows | Verification/publication/permission decisions remain TBD. |
| Postconditions | One profile and multiple branch records are maintained. |
| Related Functional Requirements / Workflows | `FR-MER-006`/007/008; `WF-MER-003`/004/005 |
| Related Business Rules / Acceptance Criteria | `BR-004`/006/020; AC-MER-006..008 |

### `UC-015` — Create and publish product

| Use case field | Definition |
| --- | --- |
| Primary Actor | Owner / authorized employee |
| Goal | Maintain one product listing and its variants. |
| Preconditions | Catalog workspace available. |
| Trigger | Merchant adds product. |
| Main Success Scenario | Enter product/variant details; publication handled under defined controls; same listing visible in two locations. Optional AI listing assistance if approved, with retailer approval. |
| Alternative Flows | Bulk upload; correct errors. |
| Exception Flows | Source conflict on AI assistance requires decision. |
| Postconditions | One catalog listing maintained. |
| Related Functional Requirements / Workflows | `FR-MER-009`/010/011/012; `FR-SYS-001`; `WF-MER-006`/`WF-SYS-001` |
| Related Business Rules / Acceptance Criteria | `BR-005`/021; AC-MER-009..012/AC-SYS-001 |

### `UC-016` — Bulk upload catalog

| Use case field | Definition |
| --- | --- |
| Primary Actor | Merchant |
| Goal | Add or update products in a batch with review. |
| Preconditions | Upload feature available; formats TBD. |
| Trigger | Merchant selects file. |
| Main Success Scenario | Upload; preview; correct errors; approve valid changes. |
| Alternative Flows | Partial row correction if rules permit. |
| Exception Flows | Unsupported/invalid file is not applied. |
| Postconditions | Approved products update one catalog. |
| Related Functional Requirements / Workflows | `FR-MER-013`; `WF-MER-007` |
| Related Business Rules / Acceptance Criteria | `BR-005`; AC-MER-013 |

### `UC-017` — Update branch inventory and prices

| Use case field | Definition |
| --- | --- |
| Primary Actor | Merchant |
| Goal | Keep branch-specific availability and price current. |
| Preconditions | Branch and product variants exist. |
| Trigger | Stock/price changes. |
| Main Success Scenario | Select branch/variant; update quantity and price; reflect in customer listings. |
| Alternative Flows | Manual updates or future approved source. |
| Exception Flows | Stale data messaging and refresh policy TBD. |
| Postconditions | Branch information updated independently. |
| Related Functional Requirements / Workflows | `FR-CUS-012`, `FR-MER-014`/015; `WF-MER-008` |
| Related Business Rules / Acceptance Criteria | `BR-006`/007/008/009; AC-CUS-012/AC-MER-014/015 |

### `UC-018` — Review merchant insights

| Use case field | Definition |
| --- | --- |
| Primary Actor | Owner / authorized employee |
| Goal | Understand activity and optional AI insight. |
| Preconditions | Metrics/data available; proposed feature enabled. |
| Trigger | Merchant opens insights. |
| Main Success Scenario | Review engagement, reservations and confirmed outcomes; optionally review unmet demand and forecast estimates. |
| Alternative Flows | Data-limited view states limitation. |
| Exception Flows | No actual sale is inferred from views/reservations. |
| Postconditions | Merchant sees status-labeled insights. |
| Related Functional Requirements / Workflows | `FR-MER-021`/022/023; `WF-MER-014` |
| Related Business Rules / Acceptance Criteria | `BR-012`/024; AC-MER-021..023 |

### `UC-019` — Handle operational notification

| Use case field | Definition |
| --- | --- |
| Primary Actor | Owner / authorized employee |
| Goal | Notice and respond to work event. |
| Preconditions | Notification capability and settings exist. |
| Trigger | Supported event occurs. |
| Main Success Scenario | Route/display notification; assigned merchant responds. |
| Alternative Flows | Adjust preferences if supported. |
| Exception Flows | Delivery channel issue falls back only as defined. |
| Postconditions | Task remains discoverable under decided rules. |
| Related Functional Requirements / Workflows | `FR-MER-024`; `WF-MER-015` |
| Related Business Rules / Acceptance Criteria | `BR-020`; AC-MER-024 |

### `UC-020` — Validate POS/ERP assumptions

| Use case field | Definition |
| --- | --- |
| Primary Actor | Product/testing team |
| Goal | Compare sandbox and mock inventory testing approaches. |
| Preconditions | Test scenario identified. |
| Trigger | Team plans integration validation. |
| Main Success Scenario | Consider sandbox; recommended mock service represents variants/branches/stock/prices; test sample change. |
| Alternative Flows | Use provider sandbox as complementary option. |
| Exception Flows | Provider data model gap is recorded. |
| Postconditions | Testing evidence informs later decision, not production provider choice. |
| Related Functional Requirements / Workflows | `FR-SYS-004`; `WF-SYS-004` |
| Related Business Rules / Acceptance Criteria | `BR-025`; AC-SYS-004 |

## 9. Acceptance criteria

Each functional requirement has a corresponding Given/When/Then criterion. For Proposed capabilities, this is a test only if the capability is approved/enabled. Conflict and TBD criteria wait on the named decision.

### Customer

| Acceptance ID / Requirement | Given / When / Then |
| --- | --- |
| AC-CUS-001 / `FR-CUS-001` — Browse without personalization | Given marketplace access is available, when the customer skips preference setup, then marketplace browsing remains available. |
| AC-CUS-002 / `FR-CUS-002` — Set or change preferences | Given preference setup is available, when a customer changes a preference, then subsequent recommendations may use the updated value while full browsing remains available. |
| AC-CUS-003 / `FR-CUS-003` — Recommend products | Given recommendation capability is enabled and relevant signals exist, when the customer opens the feed, then suggested products can reflect those signals; the system shall not restrict access to the full marketplace. |
| AC-CUS-004 / `FR-CUS-004` — Search across participating shops | Given matching listings exist at multiple shops, when the customer searches the Global Marketplace, then matching listings from those shops are shown together. |
| AC-CUS-005 / `FR-CUS-005` — Filter marketplace results | Given result filters are available, when the customer applies a filter, then results are narrowed to listings matching that filter. |
| AC-CUS-006 / `FR-CUS-006` — Use visual search | Given an image can be processed, when the customer searches with it, then similar marketplace listings are presented with seller identity. |
| AC-CUS-007 / `FR-CUS-007` — Shop from a Store Profile | Given a Store Profile is available, when the customer opens it, then the shop’s catalog and approved profile content are displayed. |
| AC-CUS-008 / `FR-CUS-008` — Complete shopping from either entry point | Given a customer selects a product in either location, when they choose a fulfillment path, then the system lets them continue from that path without a forced Store Profile visit. |
| AC-CUS-009 / `FR-CUS-009` — Show seller identity | Given a marketplace product is displayed, when the customer reviews its listing or details, then its associated shop is identifiable. |
| AC-CUS-010 / `FR-CUS-010` — View product details | Given a product listing is opened, when details are available, then the system presents available product and seller information. |
| AC-CUS-011 / `FR-CUS-011` — Compare products | Given comparison is available, when customer compares products, then each result is identified as an exact match or a similar alternative according to rules still to be defined. |
| AC-CUS-012 / `FR-CUS-012` — Select variant and branch | Given the product has branch/variant information, when the customer selects an option and location, then the system shows the corresponding reported availability and price. |
| AC-CUS-013 / `FR-CUS-013` — Virtual try-on | Given virtual try-on is enabled, when a customer requests a preview, then the system presents it as an aid and retains the product’s seller and listing context. |
| AC-CUS-014 / `FR-CUS-014` — Build cross-shop outfits | Given items from multiple shops are added to an outfit, when the outfit is displayed, then each item remains separately identifiable and does not become a combined order. |
| AC-CUS-015 / `FR-CUS-015` — Save and revisit products | Given save/recent-view capability is available, when the customer saves or opens products, then the saved/recent items can be revisited. |
| AC-CUS-016 / `FR-CUS-016` — Follow shops and watch products | Given follow/watch capability is enabled, when a customer follows a shop or watches a variant, then the association is retained for later access. |
| AC-CUS-017 / `FR-CUS-017` — Provide product updates | Given an eligible watched event occurs and notification rules allow it, when the event is processed, then a relevant update can be presented to the customer. |
| AC-CUS-018 / `FR-CUS-018` — Ask product questions | Given a customer submits a product question, when it is received, then it is associated with relevant shop/product context where available and routed for a response. |

### Shopping and fulfillment

| Acceptance ID / Requirement | Given / When / Then |
| --- | --- |
| AC-ORD-001 / `FR-ORD-001` — Submit reservation request | Given the customer selected product variant and branch, when they submit a reservation, then the system records the request as Pending until the merchant decides. |
| AC-ORD-002 / `FR-ORD-002` — Require merchant reservation decision | Given a reservation is submitted, when no merchant decision exists, then status remains Pending and is not represented as confirmed. |
| AC-ORD-003 / `FR-ORD-003` — Record reservation statuses | Given a valid merchant/customer action occurs, when status changes under the approved policy, then the resulting status is shown and retained. |
| AC-ORD-004 / `FR-ORD-004` — Show reservation fee distinctly | Given reservation fee information is available, when the customer reviews a fulfillment choice, then it is shown separately from product amount. |
| AC-ORD-005 / `FR-ORD-005` — Submit delivery order | Given a customer selects delivery and required information is available, when they submit, then a delivery order is routed to the shop. |
| AC-ORD-006 / `FR-ORD-006` — Show delivery fee only for delivery | Given the customer selects in-store reservation, when fees are shown, then no delivery fee is shown as applicable; for delivery, the delivery fee is separate. |
| AC-ORD-007 / `FR-ORD-007` — Keep product amount distinct | Given a fulfillment choice has fee information, when amounts are displayed, then product amount, reservation fee and applicable delivery fee are separately identifiable. |
| AC-ORD-008 / `FR-ORD-008` — Support delivery order updates | Given a delivery update is available, when the customer views the order, then only current supported information is shown; exact statuses await decision. |
| AC-ORD-009 / `FR-ORD-009` — Receive and review return request | Given a customer submits a return/support request, when support reviews it, then the case can be handled under the approved policy; no automatic eligibility or refund is implied. |
| AC-ORD-010 / `FR-ORD-010` — Require actual purchase confirmation | Given a reservation is Completed without purchase evidence, when review eligibility is checked, then no verified-purchase eligibility is granted. |
| AC-ORD-011 / `FR-ORD-011` — Enable review only after verified purchase | Given purchase completion is confirmed, when the customer submits a review, then it may qualify as verified; without confirmation it shall not be labeled verified. |

### Merchant

| Acceptance ID / Requirement | Given / When / Then |
| --- | --- |
| AC-MER-001 / `FR-MER-001` — Create free merchant account | Given a retailer begins registration, when required TBD account details are accepted, then a free live workspace can be created. |
| AC-MER-002 / `FR-MER-002` — Use free capabilities with real business information | Given a free account exists, when the retailer uses an available free capability, then the work is performed in the live business workspace. |
| AC-MER-003 / `FR-MER-003` — Identify paid capabilities | Given the feature split is configured, when the retailer views capabilities, then free access and payment-required access are distinguishable. |
| AC-MER-004 / `FR-MER-004` — Upgrade merchant account | Given a free merchant account exists and an upgrade is offered, when retailer completes a successful payment, then paid capabilities in the selected offer become available. |
| AC-MER-005 / `FR-MER-005` — Unlock paid capabilities only after payment success | Given payment has not succeeded, when paid access is checked, then paid capabilities remain locked; after success, included capabilities unlock. |
| AC-MER-006 / `FR-MER-006` — Maintain one Store Profile per business | Given a business profile is created, when its Store Profile is opened, then it represents that business as one profile. |
| AC-MER-007 / `FR-MER-007` — Maintain multiple branches | Given a business exists, when an authorized owner adds multiple locations, then each is represented as a branch of that business. |
| AC-MER-008 / `FR-MER-008` — Invite staff and assign access | Given staff access is enabled, when owner grants a permission, then employee actions are limited to assigned access. |
| AC-MER-009 / `FR-MER-009` — Maintain one catalog per shop | Given a product is created for a shop, when its customer-facing views are generated, then one catalog listing is used. |
| AC-MER-010 / `FR-MER-010` — Show same catalog listing in two locations | Given a published product exists, when the customer opens it through either entry point, then it refers to the same shop listing. |
| AC-MER-011 / `FR-MER-011` — Maintain product variants | Given a product has size/color options, when merchant updates the catalog, then options remain associated with that product. |
| AC-MER-012 / `FR-MER-012` — Use AI listing assistance with retailer review | Given the capability is approved and produces a suggestion, when the listing is prepared for publication, then retailer review/approval is required before any generated claim is published. |
| AC-MER-013 / `FR-MER-013` — Bulk upload products | Given a supported file is uploaded, when preview is shown, then row issues and proposed changes are visible before approval. |
| AC-MER-014 / `FR-MER-014` — Maintain branch inventory independently | Given a shop has two branches, when stock is changed for one branch, then the other branch value remains independently represented. |
| AC-MER-015 / `FR-MER-015` — Maintain branch prices | Given prices differ by branch, when customer selects a branch, then the corresponding reported price is shown. |
| AC-MER-016 / `FR-MER-016` — Create collections and announcements | Given merchant content is approved/publishable under defined rules, when published, then it can appear in the Store Profile or relevant discovery area. |
| AC-MER-017 / `FR-MER-017` — Review and decide reservation | Given a Pending request reaches the shop, when merchant confirms or rejects it, then status and customer-facing update reflect that decision. |
| AC-MER-018 / `FR-MER-018` — Prepare and update reservation status | Given an accepted reservation is prepared, when merchant marks Ready, then the customer can see Ready; closure does not by itself verify purchase. |
| AC-MER-019 / `FR-MER-019` — Process delivery orders | Given a delivery order is submitted, when merchant opens it, then requested item and available branch context are available for review. |
| AC-MER-020 / `FR-MER-020` — Respond to customer questions | Given a question is uncertain or current information is unavailable, when response is prepared, then it is escalated or marked unknown rather than inventing stock/product details. |
| AC-MER-021 / `FR-MER-021` — Review merchant performance | Given a reservation exists without purchase confirmation, when performance is displayed, then it is not counted as a confirmed sale. |
| AC-MER-022 / `FR-MER-022` — Identify unmet demand | Given relevant search and availability data exist and the feature is enabled, when merchant reviews insights, then unmet-demand signals are distinguishable from confirmed sales. |
| AC-MER-023 / `FR-MER-023` — Forecast demand | Given enough approved historical data exist and forecasting is enabled, when merchant opens the forecast, then it is presented as an estimate rather than a guarantee. |
| AC-MER-024 / `FR-MER-024` — Notify merchant of operational events | Given a supported event occurs and notification settings permit it, when the event is processed, then the relevant merchant can be notified. |

### Supporting

| Acceptance ID / Requirement | Given / When / Then |
| --- | --- |
| AC-SYS-001 / `FR-SYS-001` — Keep listing information consistent | Given merchant updates an approved listing, when customers use either entry point, then both refer to the same maintained listing. |
| AC-SYS-002 / `FR-SYS-002` — Support purchase-confirmation gate | Given a reservation is only completed, when eligibility is evaluated, then it is insufficient; only actual purchase confirmation can qualify. |
| AC-SYS-003 / `FR-SYS-003` — Review support cases | Given support receives a case, when policy details are available, then support can record and communicate the outcome; no automatic refund is assumed. |
| AC-SYS-004 / `FR-SYS-004` — Support POS/ERP testing recommendation | Given the team validates inventory behavior, when it selects a test approach, then the mock service can model products, variants, branches, quantity and price without implying production integration. |

## 10. Open questions and unresolved requirements

The questions below remain TBD. Dependent workflows and requirements are identified so the project can resolve decisions before committing related behavior.

#### **Question / topic:** OQ-001 — MVP scope
- **Decision still needed:** Which customer and merchant capabilities are essential for the first usable release? Is delivery in the first release or later?
- **Dependent items:** All launch-dependent workflows and Proposed requirements.

#### **Question / topic:** OQ-002 — Customer access
- **Decision still needed:** Can customers browse without an account? Which actions require sign-in?
- **Dependent items:** `WF-CUS-001`/007/009/011; `FR-CUS-001`/015/016.

#### **Question / topic:** OQ-003 — Preference options
- **Decision still needed:** What final audience/style/color/budget values and profile behavior are supported?
- **Dependent items:** `WF-CUS-001`; `FR-CUS-002`/003.

#### **Question / topic:** OQ-004 — Storefront/dashboard
- **Decision still needed:** Which Store Profile templates/customization controls exist? Is Merchant Dashboard web, mobile or both?
- **Dependent items:** `WF-CUS-003`; `WF-MER-003`; overall interface scope.

#### **Question / topic:** OQ-005 — Inventory updates
- **Decision still needed:** How is stock entered/refreshed, and how is stale availability shown?
- **Dependent items:** `WF-CUS-005`/015; `WF-MER-008`; `FR-MER-014`; `NFR-002`.

#### **Question / topic:** OQ-006 — Reservation stock handling
- **Decision still needed:** Are quantities deducted while Pending or only after confirmation?
- **Dependent items:** `WF-CUS-009`/010; `WF-MER-010`/011.

#### **Question / topic:** OQ-007 — Branch pricing
- **Decision still needed:** Shared default with branch overrides, or each branch sets price?
- **Dependent items:** `WF-CUS-005`; `WF-MER-008`; `FR-MER-015`.

#### **Question / topic:** OQ-008 — Reservation policy
- **Decision still needed:** Pending response duration, confirmed/Ready hold duration, multi-item requests, cancellation/expiry authority?
- **Dependent items:** `WF-CUS-009`/010/016; `WF-MER-010`/011.

#### **Question / topic:** OQ-009 — Reservation fee
- **Decision still needed:** Amount/fixed or variable; collection timing/method; reject/cancel/expire handling; refunds?
- **Dependent items:** `WF-CUS-009`; `WF-MER-010`; `FR-ORD-004`.

#### **Question / topic:** OQ-010 — Delivery/shipping
- **Decision still needed:** Coverage, provider, fee calculation/collection, failed/refused order handling and customer/merchant statuses?
- **Dependent items:** `WF-CUS-011`/012/017; `WF-MER-012`; `FR-ORD-008`/019.

#### **Question / topic:** OQ-011 — Product payments
- **Decision still needed:** When and how is product amount paid in each path? How are reservation/delivery fees collected?
- **Dependent items:** `WF-CUS-009`/011; `WF-MER-002`; `FR-ORD-004`/006/007.

#### **Question / topic:** OQ-012 — Returns/refunds
- **Decision still needed:** Return policy, eligibility, periods, refundable fees and support resolution authority?
- **Dependent items:** `WF-CUS-013`/017; `WF-SYS-003`; `FR-ORD-009`.

#### **Question / topic:** OQ-013 — Free/paid plan split
- **Decision still needed:** Which features are free vs paid, plans/prices, billing and in-place account upgrade behavior?
- **Dependent items:** `WF-MER-001`/002; `FR-MER-003`/004/005; `NFR-005`.

#### **Question / topic:** OQ-014 — Retailer verification/publication
- **Decision still needed:** What account information, business verification and publication approval are required, and when?
- **Dependent items:** `WF-MER-001`/003/006; `FR-MER-001`/006.

#### **Question / topic:** OQ-015 — Purchase verification
- **Decision still needed:** What reliably confirms in-store and delivery purchase completion?
- **Dependent items:** `WF-SYS-002`; `FR-ORD-010`/011.

#### **Question / topic:** OQ-016 — Notifications
- **Decision still needed:** Which events, channels, timing and preferences apply?
- **Dependent items:** `WF-CUS-007`; `WF-MER-015`; `FR-CUS-017`/024.

#### **Question / topic:** OQ-017 — AI and customer data
- **Decision still needed:** How may interest/browsing data be used? What privacy, retention, explanation and accuracy controls apply to recommendations, visual search, try-on, unmet demand and forecasts?
- **Dependent items:** `WF-CUS-004`/006/007; `WF-MER-014`; `FR-CUS-003`/006/013; `FR-MER-022`/023; `NFR-004`/010.

#### **Question / topic:** OQ-018 — Product comparison
- **Decision still needed:** How are exact matches distinguished from similar alternatives and which attributes are compared?
- **Dependent items:** `WF-CUS-005`; `FR-CUS-011`.

#### **Question / topic:** OQ-019 — Analytics/privacy
- **Decision still needed:** Which metrics and reporting levels are shown under what privacy safeguards?
- **Dependent items:** `WF-MER-014`; `FR-MER-021`/022/023; `NFR-004`.

#### **Question / topic:** OQ-020 — Promotions/bulk upload/staff
- **Decision still needed:** Which offer controls, file formats/image matching/error behavior and staff roles/permissions are supported?
- **Dependent items:** `WF-MER-005`/007/009; `FR-MER-008`/013/016.

#### **Question / topic:** OQ-021 — AI listing assistance conflict
- **Decision still needed:** Is AI listing assistance removed, retained as a Proposed feature, or reinstated? Which source controls? If retained, what retailer approval is required?
- **Dependent items:** `WF-MER-006`; `FR-MER-012`; `BR-021`; current journey PDF p.2 vs workflow brief §6/§9.

#### **Question / topic:** OQ-022 — Future phases
- **Decision still needed:** Which Proposed capabilities are in future phases after the first usable release?
- **Dependent items:** All Proposed workflows and requirements.

## 11. Requirements traceability matrix

Every functional requirement below maps to its source passage, workflow, business rule, use case, acceptance criterion and status.

| Requirement and source | Trace links and status |
| --- | --- |
| `FR-CUS-001` — Browse without personalization<br>Source: PDF p.3, 1.1 | Workflow: `WF-CUS-001`, `WF-CUS-002`<br>Rule: `BR-002`<br>Use case: `UC-001`<br>Acceptance: AC-CUS-001<br>Status: Agreed Direction |
| `FR-CUS-002` — Set or change preferences<br>Source: PDF p.3, 1.2 | Workflow: `WF-CUS-001`<br>Rule: `BR-002`<br>Use case: `UC-001`<br>Acceptance: AC-CUS-002<br>Status: Proposed |
| `FR-CUS-003` — Recommend products<br>Source: PDF p.3, 1.3; p.13 AI data | Workflow: `WF-CUS-001`, `WF-CUS-002`<br>Rule: `BR-002`<br>Use case: `UC-001`<br>Acceptance: AC-CUS-003<br>Status: Proposed |
| `FR-CUS-004` — Search across participating shops<br>Source: PDF p.2 product concept; p.3, 1.4 | Workflow: `WF-CUS-002`<br>Rule: `BR-002`, `BR-003`<br>Use case: `UC-001`<br>Acceptance: AC-CUS-004<br>Status: Agreed Direction |
| `FR-CUS-005` — Filter marketplace results<br>Source: PDF p.3, 1.4 | Workflow: `WF-CUS-002`<br>Rule: `BR-002`<br>Use case: `UC-001`<br>Acceptance: AC-CUS-005<br>Status: Proposed |
| `FR-CUS-006` — Use visual search<br>Source: PDF p.3, 1.5 | Workflow: `WF-CUS-004`<br>Rule: `BR-002`<br>Use case: `UC-002`<br>Acceptance: AC-CUS-006<br>Status: Proposed |
| `FR-CUS-007` — Shop from a Store Profile<br>Source: PDF p.2-3, 1.6 | Workflow: `WF-CUS-003`<br>Rule: `BR-002`, `BR-004`, `BR-005`<br>Use case: `UC-003`<br>Acceptance: AC-CUS-007<br>Status: Agreed Direction |
| `FR-CUS-008` — Complete shopping from either entry point<br>Source: PDF p.2, 1.6, 1.12 | Workflow: `WF-CUS-002`, `WF-CUS-003`<br>Rule: `BR-002`, `BR-003`<br>Use case: `UC-001`, `UC-003`<br>Acceptance: AC-CUS-008<br>Status: Agreed Direction |
| `FR-CUS-009` — Show seller identity<br>Source: PDF p.2 product concept | Workflow: `WF-CUS-002`, `WF-CUS-005`<br>Rule: `BR-002`, `BR-005`<br>Use case: `UC-001`<br>Acceptance: AC-CUS-009<br>Status: Agreed Direction |
| `FR-CUS-010` — View product details<br>Source: PDF p.4, 1.7-1.8 | Workflow: `WF-CUS-005`<br>Rule: `BR-005`, `BR-007`, `BR-008`<br>Use case: `UC-004`<br>Acceptance: AC-CUS-010<br>Status: Agreed Direction |
| `FR-CUS-011` — Compare products<br>Source: PDF p.4, 1.7; p.13 | Workflow: `WF-CUS-002`, `WF-CUS-005`<br>Rule: `BR-005`<br>Use case: `UC-004`<br>Acceptance: AC-CUS-011<br>Status: Proposed |
| `FR-CUS-012` — Select variant and branch<br>Source: PDF p.4, 1.8 | Workflow: `WF-CUS-005`<br>Rule: `BR-006`, `BR-007`, `BR-008`, `BR-009`<br>Use case: `UC-004`<br>Acceptance: AC-CUS-012<br>Status: Agreed Direction |
| `FR-CUS-013` — Virtual try-on<br>Source: PDF p.4, 1.9 | Workflow: `WF-CUS-006`<br>Rule: `BR-005`<br>Use case: `UC-004`<br>Acceptance: AC-CUS-013<br>Status: Proposed |
| `FR-CUS-014` — Build cross-shop outfits<br>Source: PDF p.4, 1.9 | Workflow: `WF-CUS-006`<br>Rule: `BR-005`<br>Use case: `UC-004`<br>Acceptance: AC-CUS-014<br>Status: Proposed |
| `FR-CUS-015` — Save and revisit products<br>Source: PDF p.4, 1.10; p.13 | Workflow: `WF-CUS-007`<br>Rule: `BR-005`<br>Use case: `UC-005`<br>Acceptance: AC-CUS-015<br>Status: Proposed |
| `FR-CUS-016` — Follow shops and watch products<br>Source: PDF p.4, 1.10 | Workflow: `WF-CUS-007`<br>Rule: `BR-005`, `BR-007`<br>Use case: `UC-005`<br>Acceptance: AC-CUS-016<br>Status: Proposed |
| `FR-CUS-017` — Provide product updates<br>Source: PDF p.4, 1.10; p.13 Notifications | Workflow: `WF-CUS-007`, `WF-MER-015`<br>Rule: `BR-008`<br>Use case: `UC-005`<br>Acceptance: AC-CUS-017<br>Status: Proposed |
| `FR-CUS-018` — Ask product questions<br>Source: PDF p.4, 1.11 | Workflow: `WF-CUS-008`, `WF-MER-013`<br>Rule: `BR-007`, `BR-009`<br>Use case: `UC-006`<br>Acceptance: AC-CUS-018<br>Status: Proposed |
| `FR-ORD-001` — Submit reservation request<br>Source: PDF p.5, Path A | Workflow: `WF-CUS-009`<br>Rule: `BR-009`, `BR-010`, `BR-011`<br>Use case: `UC-007`<br>Acceptance: AC-ORD-001<br>Status: Agreed Direction |
| `FR-ORD-002` — Require merchant reservation decision<br>Source: PDF p.5, p.8, 1.13 | Workflow: `WF-CUS-009`, `WF-MER-010`<br>Rule: `BR-010`, `BR-011`<br>Use case: `UC-008`<br>Acceptance: AC-ORD-002<br>Status: Agreed Direction |
| `FR-ORD-003` — Record reservation statuses<br>Source: PDF p.5-6, 1.13 | Workflow: `WF-CUS-010`, `WF-MER-010`, `WF-MER-011`<br>Rule: `BR-010`, `BR-011`, `BR-012`<br>Use case: `UC-008`<br>Acceptance: AC-ORD-003<br>Status: Agreed Direction |
| `FR-ORD-004` — Show reservation fee distinctly<br>Source: PDF p.5 fee table; p.13 | Workflow: `WF-CUS-009`, `WF-CUS-011`<br>Rule: `BR-015`, `BR-017`<br>Use case: `UC-007`, `UC-009`<br>Acceptance: AC-ORD-004<br>Status: Agreed Direction |
| `FR-ORD-005` — Submit delivery order<br>Source: PDF p.5, Path B | Workflow: `WF-CUS-011`<br>Rule: `BR-002`, `BR-014`<br>Use case: `UC-009`<br>Acceptance: AC-ORD-005<br>Status: Agreed Direction |
| `FR-ORD-006` — Show delivery fee only for delivery<br>Source: PDF p.5 fee table; p.13 | Workflow: `WF-CUS-011`<br>Rule: `BR-016`, `BR-017`<br>Use case: `UC-009`<br>Acceptance: AC-ORD-006<br>Status: Agreed Direction |
| `FR-ORD-007` — Keep product amount distinct<br>Source: PDF p.5 fee table; p.13 Payments | Workflow: `WF-CUS-009`, `WF-CUS-011`<br>Rule: `BR-017`<br>Use case: `UC-007`, `UC-009`<br>Acceptance: AC-ORD-007<br>Status: Agreed Direction |
| `FR-ORD-008` — Support delivery order updates<br>Source: PDF p.5-6, p.8, p.13 | Workflow: `WF-CUS-012`, `WF-MER-012`<br>Rule: `BR-014`, `BR-016`<br>Use case: `UC-010`<br>Acceptance: AC-ORD-008<br>Status: TBD |
| `FR-ORD-009` — Receive and review return request<br>Source: PDF p.6, 1.14; p.13 Returns | Workflow: `WF-CUS-013`, `WF-SYS-003`<br>Rule: `BR-018`<br>Use case: `UC-011`<br>Acceptance: AC-ORD-009<br>Status: Proposed |
| `FR-ORD-010` — Require actual purchase confirmation<br>Source: PDF p.6, 1.15; p.11 | Workflow: `WF-SYS-002`<br>Rule: `BR-012`, `BR-013`<br>Use case: `UC-012`<br>Acceptance: AC-ORD-010<br>Status: Agreed Direction |
| `FR-ORD-011` — Enable review only after verified purchase<br>Source: PDF p.6, p.11 | Workflow: `WF-CUS-014`, `WF-SYS-002`<br>Rule: `BR-013`<br>Use case: `UC-012`<br>Acceptance: AC-ORD-011<br>Status: Agreed Direction |
| `FR-MER-001` — Create free merchant account<br>Source: PDF p.7, 2.1; p.12 | Workflow: `WF-MER-001`<br>Rule: `BR-019`<br>Use case: `UC-013`<br>Acceptance: AC-MER-001<br>Status: Agreed Direction |
| `FR-MER-002` — Use free capabilities with real business information<br>Source: PDF p.7, 2.1-2.3 | Workflow: `WF-MER-001`<br>Rule: `BR-019`<br>Use case: `UC-013`<br>Acceptance: AC-MER-002<br>Status: Agreed Direction |
| `FR-MER-003` — Identify paid capabilities<br>Source: PDF p.7, 2.4; p.13 Retailer free access | Workflow: `WF-MER-001`, `WF-MER-002`<br>Rule: `BR-019`<br>Use case: `UC-013`<br>Acceptance: AC-MER-003<br>Status: TBD |
| `FR-MER-004` — Upgrade merchant account<br>Source: PDF p.7, 2.5; p.13 | Workflow: `WF-MER-002`<br>Rule: `BR-019`<br>Use case: `UC-013`<br>Acceptance: AC-MER-004<br>Status: Agreed Direction |
| `FR-MER-005` — Unlock paid capabilities only after payment success<br>Source: PDF p.7, 2.6; p.13 | Workflow: `WF-MER-002`<br>Rule: `BR-019`<br>Use case: `UC-013`<br>Acceptance: AC-MER-005<br>Status: Agreed Direction |
| `FR-MER-006` — Maintain one Store Profile per business<br>Source: PDF p.2, p.8, 2.7 | Workflow: `WF-MER-003`<br>Rule: `BR-004`<br>Use case: `UC-014`<br>Acceptance: AC-MER-006<br>Status: Agreed Direction |
| `FR-MER-007` — Maintain multiple branches<br>Source: PDF p.8, 2.8 | Workflow: `WF-MER-004`<br>Rule: `BR-004`, `BR-006`<br>Use case: `UC-014`<br>Acceptance: AC-MER-007<br>Status: Agreed Direction |
| `FR-MER-008` — Invite staff and assign access<br>Source: PDF p.8, 2.9; p.13 Staff roles | Workflow: `WF-MER-005`<br>Rule: `BR-020`<br>Use case: `UC-014`<br>Acceptance: AC-MER-008<br>Status: Proposed |
| `FR-MER-009` — Maintain one catalog per shop<br>Source: PDF p.2, p.8, 2.10 | Workflow: `WF-MER-006`<br>Rule: `BR-005`<br>Use case: `UC-015`<br>Acceptance: AC-MER-009<br>Status: Agreed Direction |
| `FR-MER-010` — Show same catalog listing in two locations<br>Source: PDF p.2, p.8, p.11 | Workflow: `WF-SYS-001`<br>Rule: `BR-002`, `BR-003`, `BR-005`<br>Use case: `UC-015`<br>Acceptance: AC-MER-010<br>Status: Agreed Direction |
| `FR-MER-011` — Maintain product variants<br>Source: PDF p.8, 2.10 | Workflow: `WF-MER-006`<br>Rule: `BR-005`, `BR-007`<br>Use case: `UC-015`<br>Acceptance: AC-MER-011<br>Status: Agreed Direction |
| `FR-MER-012` — Use AI listing assistance with retailer review<br>Source: PDF p.2 residual boundary rule; current workflow brief §6 Catalog Management | Workflow: `WF-MER-006`<br>Rule: `BR-021` (Proposed/conflict)<br>Use case: `UC-015`<br>Acceptance: AC-MER-012<br>Status: Proposed / conflict |
| `FR-MER-013` — Bulk upload products<br>Source: PDF p.9, 2.13; p.13 Bulk upload | Workflow: `WF-MER-007`<br>Rule: `BR-005`<br>Use case: `UC-016`<br>Acceptance: AC-MER-013<br>Status: Proposed |
| `FR-MER-014` — Maintain branch inventory independently<br>Source: PDF p.9, 2.14 | Workflow: `WF-MER-008`<br>Rule: `BR-006`, `BR-007`, `BR-009`<br>Use case: `UC-017`<br>Acceptance: AC-MER-014<br>Status: Agreed Direction |
| `FR-MER-015` — Maintain branch prices<br>Source: PDF p.9, 2.14; p.13 Branch prices | Workflow: `WF-MER-008`<br>Rule: `BR-008`<br>Use case: `UC-017`<br>Acceptance: AC-MER-015<br>Status: Agreed Direction |
| `FR-MER-016` — Create collections and announcements<br>Source: PDF p.9, 2.15; p.13 Promotions | Workflow: `WF-MER-009`<br>Rule: `BR-004`<br>Use case: `UC-014`<br>Acceptance: AC-MER-016<br>Status: Proposed |
| `FR-MER-017` — Review and decide reservation<br>Source: PDF p.9, 2.16 | Workflow: `WF-MER-010`<br>Rule: `BR-010`, `BR-011`<br>Use case: `UC-008`<br>Acceptance: AC-MER-017<br>Status: Agreed Direction |
| `FR-MER-018` — Prepare and update reservation status<br>Source: PDF p.9, 2.17 | Workflow: `WF-MER-011`<br>Rule: `BR-010`, `BR-012`<br>Use case: `UC-008`<br>Acceptance: AC-MER-018<br>Status: Agreed Direction |
| `FR-MER-019` — Process delivery orders<br>Source: PDF p.9, 2.18 | Workflow: `WF-MER-012`<br>Rule: `BR-014`, `BR-016`<br>Use case: `UC-010`<br>Acceptance: AC-MER-019<br>Status: Agreed Direction |
| `FR-MER-020` — Respond to customer questions<br>Source: PDF p.10, 2.19; p.13 AI | Workflow: `WF-MER-013`<br>Rule: `BR-007`, `BR-009`<br>Use case: `UC-006`<br>Acceptance: AC-MER-020<br>Status: Proposed |
| `FR-MER-021` — Review merchant performance<br>Source: PDF p.10, 2.21 | Workflow: `WF-MER-014`<br>Rule: `BR-012`<br>Use case: `UC-018`<br>Acceptance: AC-MER-021<br>Status: Proposed |
| `FR-MER-022` — Identify unmet demand<br>Source: PDF p.8, 2.11 | Workflow: `WF-MER-014`<br>Rule: `BR-024`<br>Use case: `UC-018`<br>Acceptance: AC-MER-022<br>Status: Proposed |
| `FR-MER-023` — Forecast demand<br>Source: PDF p.8, 2.12; p.13 AI data | Workflow: `WF-MER-014`<br>Rule: `BR-024`<br>Use case: `UC-018`<br>Acceptance: AC-MER-023<br>Status: Proposed |
| `FR-MER-024` — Notify merchant of operational events<br>Source: PDF p.10, 2.22; p.13 Notifications | Workflow: `WF-MER-015`<br>Rule: `BR-020`<br>Use case: `UC-019`<br>Acceptance: AC-MER-024<br>Status: Proposed |
| `FR-SYS-001` — Keep listing information consistent<br>Source: PDF p.2; p.11 cross-functional | Workflow: `WF-SYS-001`<br>Rule: `BR-005`, `BR-007`, `BR-008`<br>Use case: `UC-015`<br>Acceptance: AC-SYS-001<br>Status: Agreed Direction |
| `FR-SYS-002` — Support purchase-confirmation gate<br>Source: PDF p.6, p.11, p.13 Purchase verification | Workflow: `WF-SYS-002`<br>Rule: `BR-012`, `BR-013`<br>Use case: `UC-012`<br>Acceptance: AC-SYS-002<br>Status: TBD |
| `FR-SYS-003` — Review support cases<br>Source: PDF p.6, 1.14; p.11 | Workflow: `WF-SYS-003`<br>Rule: `BR-018`<br>Use case: `UC-011`<br>Acceptance: AC-SYS-003<br>Status: Proposed |
| `FR-SYS-004` — Support POS/ERP testing recommendation<br>Source: PDF p.11, section 3 | Workflow: `WF-SYS-004`<br>Rule: `BR-025`<br>Use case: `UC-020`<br>Acceptance: AC-SYS-004<br>Status: Proposed |

## 12. Glossary and revision history

| Term | Meaning |
| --- | --- |
| Global Marketplace | Shared shopping space for products from participating shops; customers can proceed from it without opening a Store Profile. |
| Store Profile / Storefront | One business’s branded customer-facing shop page. |
| Merchant Dashboard | Private workspace for owner and permitted employees. |
| Branch | Physical location of a business, with its own operational and stock information. |
| Product variant | A product option such as size or color. |
| Inventory / stock | Quantity/availability a branch reports; it is not a guaranteed hold. |
| Reservation | Customer request for a shop to review and prepare/hold an item; not confirmed until accepted and not proof of purchase. |
| Reservation fee | Fee applying to both fulfillment paths; amount and collection/refund rules TBD. |
| Delivery fee | Fee for delivery path only; amount and handling TBD. |
| Delivery order | Request to purchase an item for delivery, subject to stock and delivery process. |
| Verified-purchase review | Review that requires actual purchase confirmation. |
| POS/ERP | External retailer sales, product or inventory system, referenced here for testing. |

- **Version:** 1.0
- **Date:** 25 November 2026
- **Change:** Initial SRS based on revised journey source; open decisions and conflicts retained.
