# SWIFTCART
SwiftCart is a Nigerian e-commerce company, experiencing a significant increase in customer order cancellations. Customers are cancelling orders after placing them, resulting in Lost revenue, Increased refund processing, Poor customer experience, Increased workload for Customer Service, Wasted warehouse processing, Inefficient delivery operations and Reduced customer trust.<br>


**BUSINESS OBJECTIVES**<br>
Primary objective is to Reduce customer-initiated order cancellations by improving the order fulfillment experience.

**SUPPORTING OBJECTIVES**<br>
•	Identify the primary causes of customer cancellations.<br>
•	Improve inventory availability accuracy.<br>
•	Reduce unnecessary delays between order placement and fulfillment.<br>
•	Improve communication about order status and expected delivery.<br>
•	Give Customer Service better visibility into customer orders.<br>
•	Establish a measurable process for monitoring cancellation drivers.<br>

**PROJECT SCOPE**<br>
•	Customer order journey<br>
order placement > payment > inventory validation > order confirmation > warehouse fulfillment > dispatch > delivery > order tracking > cancellation > customer communication

•	Internal operations<br>
inventory management > warehouse processing > Customer Service > logistics coordination > order-status management

•	Technology<br>
order management > inventory integration > notifications > tracking > reporting

**OUT OF SCOPE**<br>
•	Changing SwiftCart's entire payment infrastructure<br>
•	Rebuilding the company's warehouse<br>
•	Changing external delivery companies<br>
•	Marketing campaigns<br>
•	Product pricing strategy<br>
•	Customer acquisition<br>
•	Redesigning the entire e-commerce website<br>

**PROJECT ASSUMPTIONS**<br>
•	Cancellation data is available.<br>
•	Order-level data can be linked to cancellation reasons.<br>
•	Inventory data is available from the existing inventory system.<br>
•	Customer Service records customer complaints.<br>
•	Delivery performance data can be obtained.<br>
•	Operations stakeholders are available for interviews.<br>

**CONSTRAINTS**<br>
•	The company has a limited transformation budget.<br>
•	Existing systems may not support real-time integration.<br>
•	Management wants measurable improvement within 2 months.<br>
•	Historical cancellation data may contain missing or inconsistent reasons.<br>
•	Delivery performance depends partly on third-party logistics companies.<br>

**RISKS**<br>
•	Poor historical data<br>
•	Stakeholder resistance<br>
•	Integration difficulty<br>
•	Delivery partner data unavailable<br>
•	Requirements change<br>
 
**SUCCESS CRITERIA**<br>
Cancellation rate: 12% → <7%<br>
Late delivery: 21% → <12%<br>
Inventory accuracy: 88% → ≥97%<br>
Customer Service order-resolution time: 15 minutes → <5 minutes<br>
Order tracking availability: 60% → ≥95%<br>

<br>
<br>

**ELICITATION & REQUIREMENTS GATHERING**<br>
**Elicitation plan**
| Method |	Participants/Evidence  |	Purpose |
| --------------- | -------------------------------------------- | --------------------------------------------------- |
| Interviews	| Operations, Inventory, Warehouse, CS, Logistics, Product, IT, Finance |	Understand needs, pain points and constraints |
| Observation	| Warehouse and CS workflows	| Identify actual process gaps|
| Document analysis	| Cancellation, inventory, delivery, refund and SOP documents, reports from stakeholders about their pain |	Validate existing rules and performance |
| Data analysis |	Orders, cancellations, inventory, delivery and complaints	| Quantify the problem and locate patterns |
| Customer research / survey	| Cancelled/recent customers	| Understand customer experience and cancellation triggers |

<br>
<br>


**GAP ANALYSIS**<br>
| Current State	| Desired State	| Gap |
| -------------------------------- | ----------------------------- | ----------------------------- |
| Delayed inventory updates | 	Near-real-time availability |	Integration gap |
| Manual fulfillment	| Integrated workflow	| Process/system  |
| Fragmented order information	| Central order view	| Visibility gap |
| Manual customer updates	| Automated notifications	| Communication gap |
| Manual delay detection	| SLA alerts	| Monitoring gap |
| Inconsistent cancellation reasons	| Standard reason codes	| Data-quality gap |

<br>
<br>


**BUSINESS REQUIREMENTS**<br>
| ID	| Requirement	| Priority |
| -------------------------------- | ----------------------------- | ----------------------------- |
| BR-001	| Reduce avoidable customer cancellations	| High |
| BR-002	| Improve inventory availability accuracy	| High |
| BR-003	| Improve order fulfillment visibility	| High |
| BR-004	| Provide timely customer order information	| High |
| BR-005	| Identify delayed orders before cancellations	| High |
| BR-006	| Give Customer Service a complete order view	| Medium |
| BR-007	| Provide management with reliable cancellation/fulfillment analytics	| Medium |

<br>
<br>


**FUNCTIONAL REQUIREMENTS**<br>
| ID	| Functional Requirement	| Business Link |
| -------------------------------- | ----------------------------- | ----------------------------- |
| FR-001	| Validate product availability before order confirmation	| BR-002 |
| FR-002	| Reserve available inventory after confirmation	| BR-002 |
| FR-003	| Maintain defined order lifecycle statuses	| BR-003 |
| FR-004	| Provide estimated delivery date	| BR-004 |
| FR-005	| Send notifications at defined order events	| BR-004 |
| FR-006	| Flag orders that exceed fulfillment thresholds	| BR-005 |
| FR-007	| Allow authorized CS users to search/view orders	| BR-006 |
| FR-008	| Require standardized cancellation reason codes	| BR-001 |
| FR-009	| Allow customers to view tracking information	| BR-003 |
| FR-010	| Provide a unified CS order view across payment, inventory, fulfillment and delivery	| BR-006 |

<br>
<br>


**NON-FUNCTIONAL REQUIREMENTS**
| ID	| Requirement	| Category |
| -------------------------------- | ----------------------------- | ----------------------------- |
| NFR-001	| Order-status information should meet an agreed response-time threshold.	| Performance |
| NFR-002	| Only authorized users may access customer/order information.	| Security |
| NFR-003	| Status changes must be timestamped and auditable.	| Auditability |
| NFR-004	| Inventory/order information must remain consistent across integrations.	| Reliability |
| NFR-005	| Solution should support increased order volume without unacceptable degradation.	| Scalability |

<br>
<br>


**BUSINESS RULES & MoSCoW**
| Type	| Item |
| -------------------------------- | ----------------------------- |
| Rule	| Inventory must be validated before confirmation. |
| Rule	| Confirmed orders reserve available stock. |
| Rule	| Orders exceeding SLA are flagged. |
| Rule	| Every cancellation requires a standard reason code. |
| Rule	| Refunds must follow the approved refund policy. |
| Must	| Inventory validation, reservation, order confirmation, order tracking, order status, customer notifications, cancellation reason capture |
| Should	| Delay alerts, CS dashboard, management analytics |
| Could	| Cancellation prediction, notification  |
| Won't	| AI chatbot, complete website redesign, recommendation engine |

<br>

**TO-BE PROCESS**

Customer → Select Product → Inventory Validation → Available? → Reserve Stock → Payment → Confirm Order → Automatic Warehouse Queue → Pick → Pack → Dispatch → Tracking Activated → Customer Notification → Delivery

If unavailable: Inform Customer → Alternative / Exit

<br>

**PROPOSED SOLUTION**
| Component	| Purpose	| Key Capabilities |
| -------------------------------- | ----------------------------- | ----------------------------- |
| Inventory Integration	| Improve stock accuracy	| Availability validation, reservation, exception monitoring |
| Order Management	| Centralize lifecycle	| Status management, order IDs, exception states |
| Customer Visibility	| Reduce uncertainty	| Tracking, ETA, status, delay information |
| Operations Monitoring	| Enable intervention	| SLA alerts, cancellation dashboard, inventory exceptions |


<br>
<br>


**USER STORIES AND ACCEPTANCE CRITERIA**

| ID 	| User Story | Acceptance Criteria |
| -------------------------------- | ----------------------------- | ----------------------------- |
| US-001 | As a customer, I want inventory validated before confirmation so I do not purchase an unavailable product. (inventory) |	Available stock is validated/reserved; unavailable stock prevents confirmation and shows an appropriate message.|
| US-002 | As a customer, I want to see my order status so I know where my order is. (Order tracking) |	Latest status, ETA and tracking number are displayed where available.|
| US-003 | As a customer, I want order updates so I know when my order progresses. (notification) |	Confirmation, dispatch, out-for-delivery, delivery and significant-delay notifications are triggered. |
| US-004 | As a CS agent, I want one order view so I can resolve customer issues quickly. (Customer service) |	Agent can retrieve order and see payment, inventory, fulfillment and delivery information, customer details, cancellation/refund. |
| US-005 | As an Operations Manager, I want delayed orders identified automatically so I can intervene before cancellation. (monitoring) |	SLA threshold is defined, orders monitored, flagged and visible to Operations. Escalation can occur |


<br>
<br>


**AGILE BACKLOG**
| Sprint	| Epic	| Stories	| Priority |
| -------------------------------- | ----------------------------- | ----------------------------- | ----------------------------- |
| Sprint 1	| Inventory & order processing	| US-001 + reservation + order confirmation	| Highest |
| Sprint 2	| Customer visibility	| US-002 + ETA + tracking	| High |
| Sprint 3	| Communication	| US-003 + confirmation/dispatch/delay notifications	| High |
| Sprint 4	| Operations control	| US-004 + US-005 + cancellation analytics	| High/Medium |

<br>
<br>


**UAT TEST CASES**
| ID	| Scenario	| Precondition	| Action	| Expected Result |
| ---------- | ----------------------------- | ----------------------------- |  ----------------------------- | ----------------------------- |
| UAT-001	| Available product	| Inventory available	| Order placed	| Inventory validated/reserved and order confirmed |
| UAT-002	| Unavailable product	| No available stock	| Customer attempts order	| Order blocked and customer informed |
| UAT-003	| Tracking	| Active order exists	| Customer opens tracking	| Status, ETA and tracking displayed |
| UAT-004	| Delay alert	| Order exceeds SLA	| SLA threshold reached	| Order flagged for Operations |
| UAT-005	| CS unified view	| Customer contacts support	| Agent searches order	| Complete order information displayed |

<br>
<br>


**REQUIREMENT TRACEABILITY MATRIX**
| Business Req.	| Functional Req.	| User Story	UAT |
| -------------------------------- | ----------------------------- | ----------------------------- |
| BR-001	| FR-001 / FR-008	US-001	| UAT-002 |
| BR-002	| FR-001 / FR-002	US-001	| UAT-001 / UAT-002 |
| BR-003	| FR-003 / FR-009	US-002	| UAT-003 |
| BR-004	| FR-004 / FR-005	US-003	| UAT-003 |
| BR-005	| FR-006	US-005	| UAT-004 |
| BR-006	| FR-007 / FR-010	US-004	| UAT-005 |







