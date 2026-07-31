# Functional requirements

| Requirement ID | FR-001 |
| -------------------- | -------------------- |
| Description | The application shall allow users to create appointments |
| Priority | High |
| Acceptance Criteria | 1. The user can enter the required appointment information (title, date, time) <br> 2. The user submit the appointment form <br> 3. A success message is displayed after the appointment is submitted <br> 4. The new appointment appears in the appointment list |

| Requirement ID | FR-002 |
| -------------------- | -------------------- |
| Description | The application shall allow users to edit appointments |
| Priority | High |
| Acceptance Criteria | 1. The user can modify appointment information <br> 2. The user can submit changes <br> 3. A success message is displayed after the appointment is updated <br> 4. The updated appointment appears in the appointment list |

| Requirement ID | FR-003 |
| -------------------- | -------------------- |
| Description | The application shall allow users to delete appointments |
| Priority | High |
| Acceptance Criteria | 1. The user can delete appointments <br> 2. The user shall confirm the appointment deletion <br> 3. A success message is displayed after the appointment is deleted <br> 4. The deleted appointment no longer appears in the appointment list |

| Requirement ID | FR-004 |
| -------------------- | -------------------- |
| Description | The application shall validate appointment data before saving |
| Priority | High |
| Acceptance Criteria | 1. An error message is displayed if required fields are empty <br> 2. The application shall prevent submission of invalid data |

# Non-functional requirements 

| Requirement ID | NFR-001 |
| -------------------- | -------------------- |
| Description | Validation feedback shall be displayed in under 1 second |
| Priority | High |
| Acceptance Criteria | 1. Validation feedback is displayed within 1 second after user input <br> 2. The response time remains under 1 second for all validation errors |

| Requirement ID | NFR-002 |
| -------------------- | -------------------- |
| Description | The interface shall follow basic accessibility practices |
| Priority | High |
| Acceptance Criteria | 1. The images shall have alternative texts <br> 2. The text shall be high contrast <br> 3. The application can be navigated using only the keyboard |

| Requirement ID | NFR-003 |
| -------------------- | -------------------- |
| Description | The interface shall be usable on desktop and mobile devices |
| Priority | Medium |
| Acceptance Criteria | 1. The interface remains usable on screens from 320px to desktop widths <br> 2. The application is compatible with the latest versions of Chrome, Firefox, and Edge |

| Requirement ID | NFR-004 |
| -------------------- | -------------------- |
| Description | The application shall respond to user interactions in under 1 seconds. |
| Priority | High |
| Acceptance Criteria | 1. The application shall respond to user requests in less than 2 seconds |

| Requirement ID | NFR-005 |
| -------------------- | -------------------- |
| Description | The components shall be organized by feature |
| Priority | High |
| Acceptance Criteria | 1. Source code follows a modular folder structure <br> 2. Functions have a single responsibility <br> 3. Code follows a consistent naming convention |

| Requirement ID | NFR-006 |
| -------------------- | -------------------- |
| Description | Appointment data shall persist after the browser page is refreshed |
| Priority | High |
| Acceptance Criteria | 1. Appointment data remains avaible after refreshing the page, closing and reopening the browse, or restarting the device |