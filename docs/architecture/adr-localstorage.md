---
status: accepted
date: 2026-07-30
decision-makers: [Ingrid Castillo, Full-Stack Development]
id: ADR-002
---

# Use browser localStorage for appointment data persistence

## Context

The project is an MVP web application for managing appointments. Users can create, view, edit, and delete appointments.

The application is implemented as a client-side Single-Page Application (SPA) and stores all data in the user's browser. The current scope does not include user accounts, multiple users, or cloud synchronization.

Appointment data must remain available after refreshing or reopening the browser while keeping the implementation simple and maintainable for a single developer.

## Considered options

### Browser localStorage

**Advantages**

- Built into modern browsers without additional dependencies.
- Simple API suitable for storing small amounts of structured data.
- Data remains available after page refreshes and browser reopening.
- Satisfies the persistence requirement with minimal implementation effort.

**Disadvantages**

- Data is stored only on the user's device.
- Limited storage capacity.
- No synchronization between browsers or devices.
- Not suitable for sensitive or large amounts of data.

### Browser sessionStorage

**Advantages**

- Built into modern browsers.
- Simple API for temporary data storage.

**Disadvantages**

- Data is removed when the browser tab or window is closed.
- Does not satisfy the persistence requirement.

## Decision

Use browser localStorage as the persistence mechanism for appointment data.

## Rationale

The project is an MVP developed by a single developer and only requires local persistence within the user's browser.

localStorage satisfies the application's persistence requirement while keeping the implementation simple and avoiding unnecessary complexity.

If future requirements include multiple users or shared data, the persistence strategy will be re-evaluated.

## Consequences / Trade-offs

### Positive

- Simple implementation.
- No additional dependencies.
- Data persists after browser refresh and reopening.
- Faster development for the MVP.

### Negative

- Data is limited to a single browser on a single device.
- Users cannot access appointments from another browser or device.
- Data can be lost if the browser storage is cleared.
- Not suitable for applications requiring shared or centralized data.