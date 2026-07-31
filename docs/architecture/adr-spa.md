--- 
status: accepted
date: 2026-07-30
decision-makers: [Ingrid Castillo, Full-Stack Development]
id: ADR-001
---

# Adopt Single-Page Application (SPA) Architecture

## Context
The project is an MVP web application for managing user appointments. Only clients can create, view, edit, or cancel their own appointments (the professional/admin panel is planned for a second version). 
It is being developed by a single developer. The application requires responsive user interactions, maintainable code, and does not require server-side rendering or search engine optimization. 

## Considered options
SPA
- fast client-side interactions
- reusable UI components
- larger initial JavaScript download
MPA
- server-rendered pages
- smaller initial JavaScript download
- full page reloads after each navigation

## Decision
Adopt a Single-Page Application (SPA) architecture. 

## Rationale
A SPA better supports the application's CRUD workflow by avoiding full page reloads during appointment managment. Since SEO is not a project requirement and the application is relatively small, the benefits of a SPA outweight its larger initial bundle size.

## Consequences/Trade-offs
Positive
- smoother user experience
- responsive interface
- easier separation between frontend and backend 
Negative
- larger initial JavaScript download
- dependence on client-side JavaScript