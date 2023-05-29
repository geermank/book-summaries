# A tale of two values

## Key points

- If we don't pay attention to architecture, systems can become practically imposible to change.
- Architecture is usually not considered as important as it is. The software development team must fight for architecture, giving it the priority it deserves over not important features.

## Summary

Every software system provides two different values to the stakeholders:
- Behaviour
- Structure

#### Behaviour
Refers to the functionality of the system. Implement functional requirements and fix bugs.

#### Architecture
Our systems must be easy to change. That's why the architecture matters; if they are not easy to change, costs can increase exponentially (due to time and number of developers needed to implement/modify different features).

However, which one provides greater value? Well, if we don't pay attention to architecture, the system may become practically imposible to change (the cost of change exceeds its benefit).

Afterwards, the author, based on the Eisenhour Matrix, categorizes behaviour as urgent but not always important and architecture as important but never particularly urgent. The problem comes when features that are urgent but not important are not separated from those that are truly urgent and important. This failure then leads to ignoring the important architecture of the system in favor of the unimportant features of the system. Therefore, it is the resposibility of the software developers to assert the importance of architecture over the urgency of features.




