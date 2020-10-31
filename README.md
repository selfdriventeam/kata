# Farmacy Food Kata

selfdriventeam's architecture proposal for Farmacy Food

# The Customer
## Farmacy Food
**Let Food Be Thy Medicine.**

Farmacy Food creates tasty meals around your dietary needs, incorporating ingredients known to have beneficial properties to support your health and well-being.
Public repo for O'Reilly Kata Deliverables

# Our Vision

SelfDrivenTeam sees a scalable, extensible system running on a cloud provider where the system scales itself up and down dynamically based on load and response times.

SelfDrivenTeam's system provides secure, reliable functionality for Farmacy Food's customers, nutritionists, chefs, and delivery personel so they can focus on their areas of expertise while showcasing Farmacy Food's special sauce, the combination of the fresh, wholesome food, nutritionists, and a proprietary meal reccomendation engine to provide customers with fresh tasty, nutriutious, and low cost meals tailored to each customer's individual needs and preferences.

The system initally runs for the Detroit, Michigan area, but as service area and usage grows the system can easily scale out to handle multiple geographic areas **and** scale up within an area to handle increasing customer/POS density. The system includes all of the components needed to meet all of the current requirements and provides extensibility to add known and opportunistic future enhancements.

# Requirements from the customer
## Users
Dozens of automated fridges and representative run kiosks, thousands of customers.

## Requirements
1) Must integrate with 3rd party smart fridges to obtain inventory and purchase activity
1) Smart Fridges Produce item inventory levels and purchases. The smart fridges have a cloud based management system that handles communication with the Smart Fridge so obtaining this data would be through an API.
1) Must integrate with point of sale system at kiosks
1) The Kiosk is a sublet space inside another business where we will sell our product but have an employee handle the transactions through a point of sale. The same data should be accessible through the POS systems API’s.
1) Mobile and Web accessible
1) Support providing feedback on items of verified purchases and in app surveys
1) Accept coupons and promotional pricing
1) Send inventory updates to central kitchen

## Long term Goals
1) Long term would like to allow multiple vendors to offer items through points of sale
1) Wants to harvest data to provide personalized recommendations based on users health goals, purchase history, and item ratings

# Our Solution

*High level architecture diagram goes here*

Broken down into 8 major components in a micro-service based architecture, the system provides a **S.O.L.I.D.** foundation for the next steps (detailed design and implementation). The following diagrams, Architectural Decision Records, Personas, and intermediate artifacts provide more detail on the benefits of the system and why various trade-offs were made when defining the achitecture.

## Detailed Architectural Diagrams

| Index | Description |
|-------|-------------|
| A | High Level Architecture |
| B | Reccomendation Engine |
| C | Customer Domain |
| D | Order Domain |
| E | Billing Domain |
| F | Inventory Domain |
| G | Notification Engine |
| H | API Gateway |
| I | UI Conmponent |

## Architectural Decision Records

| Index | Description |
|-------|-------------|
| [ADR_001](doc/arc/adr_001.md) | Use actor/action to identify components |
| [ADR_002](doc/arc/adr_002.md) | No delivery component is needed for now |
| [ADR_003](doc/arc/adr_003.md) | Require stock monitoring and calibration |
| [ADR_004](doc/arc/adr_004.md) | Using a notification system |
| [ADR_006](doc/arc/adr_006.md) | Sharding/routing as per location |
| [ADR_007](doc/arc/adr_007.md) | Using External Identity Provider |
| [ADR_008](doc/arc/adr_008.md) | Data needs to be anonymized for PII |
| [ADR_009](doc/arc/adr_009.md) | 3rd party health hooks into the customer info |
| [ADR_010](doc/arc/adr_010.md) | Recommendation engine is a batch system |
| [ADR_011](doc/arc/adr_011.md) | Using microservices vs event driven |
| [ADR_012](doc/arc/adr_012.md) | Use mobile friendly web app |

## Personas

| Name | Role |
|------|------|
| [Alice](doc/personas/alice_(chef).md) | Chef |
| [Barbara](doc/personas/barbara_(kiosk_worker).md) | Kiosk Worker |
| [Edward](doc/personas/edward_(delivery_driver).md) | Delivery Driver |
| [Jennifer](doc/personas/jennifer_(subscriber).md) | Subscription Customer |
| [Mark](doc/personas/mark_(nutritionist).md) | Nutritionist |
| [Scott](doc/personas/scott_(eater).md) | Occasional Customer |

## Intermediate Artifacts

* Actors/Actions
