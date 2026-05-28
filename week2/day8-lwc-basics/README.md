# 1. What is LWC?

LWC (Lightning Web Components) is a modern JavaScript framework used in Salesforce to build fast and reusable user interface components.

LWC is based on:
- HTML
- JavaScript
- CSS
- Web Standards

It helps developers create responsive and interactive Salesforce applications.

Examples:
- Login forms
- Product cards
- Dashboards
- Customer portals

---

# 2. Why Salesforce Uses LWC

Salesforce uses Lightning Web Components because they provide better performance and modern development capabilities.

Benefits of LWC:
- Faster rendering
- Reusable components
- Better performance
- Easy maintenance
- Uses modern JavaScript
- Improved user experience

LWC follows web standards, making development simpler and more efficient.

---

# 3. Your UI Screens

## Screens Created
- Bike Card Component
- Bike Selection App
- Product Detail View
- Interactive Selection Page

## Features
- Responsive layout
- Dynamic bike details
- Interactive buttons
- Image display
- Real-time UI updates

Add screenshots of:
- Bike Card page
- Selector component
- Product detail component
- Lightning App Builder page

---

# 4. Component Breakdown

## BikeCard Component
Displays:
- Bike name
- Description
- Price
- Image
- Category badges

Files:
- bikeCard.html
- bikeCard.js
- bikeCard.js-meta.xml

---

## Selector Component
Acts as the parent component that manages the application layout.

Responsibilities:
- Handles selected product
- Connects list and detail components

---

## List Component
Displays multiple bike tiles.

Responsibilities:
- Loops through bike data
- Renders tile components

---

## Tile Component
Displays a single bike item.

Responsibilities:
- Shows bike image and name
- Handles click events

---

## Detail Component
Displays detailed bike information.

Responsibilities:
- Shows selected bike details
- Updates dynamically based on user selection

---

# 5. Frontend vs Backend Logic

| Frontend Logic | Backend Logic |
|---|---|
| Handles user interface | Handles server-side processing |
| Uses HTML, CSS, JavaScript | Uses Apex and database operations |
| Displays data to users | Processes and stores data |
| Manages user interactions | Performs business logic |
| Example: Button click events | Example: Database updates |

In LWC:
- Frontend uses HTML and JavaScript
- Backend commonly uses Apex classes and Salesforce data services

---

# 6. Reflection

Lightning Web Components improve Salesforce application development by providing fast, reusable, and interactive UI components.

LWC development encourages:
- Modular design
- Reusability
- Better performance
- Cleaner code structure
- Improved user experience

Using separate frontend and backend logic helps developers build scalable and maintainable enterprise applications.
