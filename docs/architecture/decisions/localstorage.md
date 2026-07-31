--- 
status: accepted
date: 2026-07-30
decision-makers: [Ingrid Castillo, Full-Stack Development]
id: ADR-002
---

# Use browser localStorage for appointment data persistence

## Context
The project is an MVP web application for managing user appointments. Only clients can create, view, edit, or cancel their own appointments (the professional/admin panel is planned for a second version). 
The current scope does not include autheticatio, multiple users, cloud synchronization, or a backend database. The application must persist appointment information after refreshing or reopening the browser while keeping the implementaion simple and maintainable for a single developer. 

## Considered options
### Browser localStorage
Advantages
- built into modern browsers without additional dependencies
- simple API sutable for small amounts of structured data
- data remains avaible after page refreshes and browser reopening
- reduces development complexity for an MVP

Disadvantages
- data is stored only on the user's device
- limited storage capacity
- no data synchronization between devices
- not suitable for sensitive or large amounts of data 

### Browser sessionStorage
Advantages
- simple browser API
- suitable for temporary data storage 

Disadvantages
- data is removed when the browser tab is closed 
- does not satisfy the persistence requirement 

### Backend database 
Advantages 
- persistent storage independent of the user's device
- enables multi-device acess 
- better foundation for future authentication and professional dashboards

Disadvantages
- requires backend develpoment, database management, and deployment
- increases project complexity
- not necessary for the current MVP scope

## Decision
Use browser localStorage as the persistence mechanism for appointment data.

## Rationale
The application is currently an MVP develped by a single developer and does not require user accounts, multi-device access, or centralized data management.
localStorage satisfies the current persistence requirement with minimal complexity, allowing the focus to remain on implementig appointment management functionality.
A backend database may be introduced in a future version if requirements evolve to support multiple users, authentication, or synchronization.

## Consequences/Trade-offs
Positive
- simple implementation with minimal setup
- no backend infrastructure required
- data persists after browser refresh and reopening
- faster development for the MVP
Negative
- data is limited to a single browser 
- users cannot access appointments from different devices
- data recovery and backup mechanisms are not available
- The solution is not suitable for production applications with multiple users