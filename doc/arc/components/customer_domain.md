# [Customer Domain](../../../README.md)

![Customer Domain](../images/customer_domain.svg)

The Customer Domain consists of 3 major subsystems and 2 major databases. It manages and controls access to general PII and HIPAA data, providing anonymized/aggregated data to authorized users.

The **Customer Service** provides the interface and authorization based on presented ID. All requests to the customer domain **must** go through the **Customer Service**.

The **Anonymizer/Aggregator** is responsible for ensuring that any data returned from the Customer Domain for display, notification, recommendations, or future plans is properly filtered/massaged to prevent leakage of protected data.

The **Surveyor** is responsible for managing any customer surveys, handling scheduling, respondent selection, and compilation of results.

The **Customer Database** maintains the source of truth for the majority of data Farmacy Food maintains on its customers. This includes, but is not limited to, name, address, contact info, financial info, personal preferences, and subscription data.

The (optional) **HIPAA Database** will be be used in the future to maintain the source of truth for any secure personal medical information used by the [Recomendation Engine](/doc/arc/components/recommendation_engine.md)

## Communicates With:
* [Notification Engine](/doc/arc/components/notification_engine.md) for sending out survey information
* [Order Domain](/doc/arc/components/order_domain.md) to correlate orders with customers
* [Recomendation Engine](/doc/arc/components/recommendation_engine.md) via anonymized data
* [UI Component](/doc/arc/components/ui_component.md) for collecting/displaying customer data with the customer
