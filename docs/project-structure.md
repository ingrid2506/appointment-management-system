# Project Structure

The project follows a **Feature-Based MVC architecture**, where each feature groups its own models, views, and controllers. Shared resources are placed in a common directory to promote reuse and maintainability.

```text
src/
├── app/
│   ├── app.js
│   ├── router.js
│   └── routes.js
│
├── features/
│   └── appointments/
│       ├── controllers/
│       ├── models/
│       ├── views/
│       ├── components/
│       ├── styles/
│       └── index.js
│
├── shared/
│   ├── storage/
│   ├── utils/
│   ├── constants/
│   └── styles/
│
├── assets/
│   ├── icons/
│   └── images/
│
└── main.js
```

---

# Directory Description

## `src/`

Contains the application's source code.

---

## `src/app/`

Contains the application bootstrap and navigation logic.

| Directory/File | Purpose                                   |
| -------------- | ----------------------------------------- |
| `app.js`       | Initializes the application.              |
| `router.js`    | Implements the SPA routing mechanism.     |
| `routes.js`    | Defines the available application routes. |

---

## `src/features/`

Contains all application features.

Each feature is self-contained and includes its own MVC implementation.

---

## `src/features/appointments/`

Contains all files related to appointment management.

### `controllers/`

Coordinates communication between the views and models.

Responsibilities include:

* Handling user actions.
* Validating requests.
* Updating the model.
* Refreshing the user interface.

---

### `models/`

Contains the business logic and data management.

Typical responsibilities include:

* Representing appointment entities.
* Creating, updating, deleting, and retrieving appointments.
* Delegating persistence operations to the storage layer.

---

### `views/`

Responsible for rendering the user interface.

Responsibilities include:

* Displaying appointment information.
* Rendering forms and lists.
* Updating the DOM.

Views should not contain business logic.

---

### `components/`

Contains reusable UI elements shared within the feature.

Examples:

* Modal dialogs
* Toast notifications
* Buttons

---

### `styles/`

Contains styles specific to the appointments feature.

---

### `index.js`

Acts as the public entry point for the feature by exporting the modules required by the application.

---

## `src/shared/`

Contains reusable resources that are independent of any specific feature.

---

### `storage/`

Contains browser persistence utilities.

Current implementation:

* `localStorage`

Future implementations may replace this layer without affecting the rest of the application.

---

### `utils/`

Contains helper functions shared across the application.

Examples:

* Date formatting
* Form validation
* DOM utilities

---

### `constants/`

Contains application constants.

Examples:

* Storage keys
* Default configuration values

---

### `styles/`

Contains global styles shared by all features.

Typical files include:

* `reset.css`
* `variables.css`
* `base.css`
* `utilities.css`

---

## `src/assets/`

Contains static resources.

Examples:

* Images
* Icons

---

## `src/main.js`

Application entry point.

Responsibilities include:

* Starting the application.
* Initializing the router.
* Loading the initial view.

---

# Design Principles

The project structure follows these principles:

* **Feature-based organization** to keep related files together.
* **Model–View–Controller (MVC)** separation within each feature.
* **Shared resources** stored in a common directory to avoid duplication.
* **Separation of concerns**, where each module has a single responsibility.
* **Maintainability**, allowing new features to be added with minimal impact on existing code.

---

# Future Evolution

As the application grows, new features can be added following the same structure.

Example:

```text
features/
├── appointments/
├── profiles/
├── authentication/
└── settings/
```

Each feature should remain independent and encapsulate its own models, views, controllers, components, and styles whenever applicable.
