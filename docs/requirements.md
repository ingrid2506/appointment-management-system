## Functional requirements

| Requirement ID | FR-001 |
| -------------------- | -------------------- |
| Description | The application shall allow users to create an appointment |
| Priority | High |
| Acceptance Criteria | 1. The user can enter the required appointment information <br> 2. The user clicks the Save button <br> 3. A success message is displayed after the appointment is saved <br> 4. The new appointment appears in the appointment list |

| Requirement ID | FR-002 |
| -------------------- | -------------------- |
| Description | The application shall allow users to edit an appointment |
| Priority | High |
| Acceptance Criteria | 1. The user can click the Edit button <br> 2. The user can enter changes in required fields <br> 3. The user clicks the Save Changes button <br> 4. A success message is displayed after the appointment is updated <br> 5. The updated appointment appears in the appointment list |

| Requirement ID | FR-003 |
| -------------------- | -------------------- |
| Description | The application shall allow users to delete an appointment |
| Priority | High |
| Acceptance Criteria | 1. The user can click the Delete button <br> 2. A confirmation dialog is displayed before the appointment is deleted <br> 3. A success message is displayed after the appointment is deleted <br> 4. The deleted appointment no longer appears in the appointment list |

| Requirement ID | FR-004 |
| -------------------- | -------------------- |
| Description | The application shall validate appointment data before saving |
| Priority | High |
| Acceptance Criteria | 1. An error message is displayed if required fields are empty <br> 2. An error message is displayed if invalid data is entered |

## Non-functional requirements 

| Requirement ID | NFR-001 |
| -------------------- | -------------------- |
| Description | Validation feedback shall be displayed in under 1 second |
| Priority | High |
| Acceptance Criteria | 1. Validation feedback is displayed within 1 second after user input <br> 2. The response time remains under 1 second for all validation errors |

| Requirement ID | NFR-002 |
| -------------------- | -------------------- |
| Description | The interface shall follow basic accessibility practices |
| Priority | High |
| Acceptance Criteria | 1. Information must be presented in ways users can understand with their senses <br> 2. Navigation application and functions must be usable for everyone <br> 3. Content and operation must be clear <br> 4. Content must work reliably with different assistive tools |

| Requirement ID | NFR-003 |
| -------------------- | -------------------- |
| Description | The interface is usable on desktop and mobile devices |
| Priority | Middle |
| Acceptance Criteria | 1. The interface remains usable on screens from 320px to desktop widths <br> 2. The application is compatible with the latest versions of Chrome, Firefox, and Edge |