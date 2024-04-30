# Alpine.js Table Demo

This repository provides a simple demonstration of how [Alpine.js](https://alpinejs.dev/) can be used to create interactive, dynamic tables with features like:

- **Search:** Filters table data based on user input.
- **Threshold Selection:** Allows users to control filtering using a customizable threshold.
- **Pagination:** Handles navigation through large datasets.
- **Data Fetching:** Simulates retrieving data from an external API.

## Key Alpine.js Concepts

- **x-data:** Declares the component's reactive data state.
- **x-model:** Creates two-way bindings for inputs (search field, select menu).
- **x-for:** Iterates over data to dynamically generate table rows.
- **@click:** Handles button clicks and calls functions.
- **x-text:** Dynamically updates text content within table cells.
- **x-if:** Conditionally displays elements (in this case, the table).
- **Conditional Classes:** (`class="[ ... ]"`) Enables the button's loading state styling.

## Setup

1. Clone this repository.
2. Open the `index.html` file in a web browser.

## Dependencies

- **Alpine.js** (included via CDN)
- **Bulma CSS** (included via CDN, for basic styling)

## Explanation

The JavaScript code (within the `<script>` tag) defines an Alpine.js component using the `getData()` function. Here's a breakdown of its properties and behavior:

- **options:** Provides values for the threshold dropdown.
- **searchValue:** Stores the text entered into the search field.
- **page, limit, total:** Manages pagination state.
- **events:** Stores the array of events fetched from the API.
- **isLoading:** Tracks loading state for the button.
- **previousPage, nextPage, lastPage:** Pagination variables.
- **fetchData():**
  - Fetches data from a mock API (`https://5d6516c05b26ae001489eb85.mockapi.io/api/v1/events`).
  - Updates the events array and pagination state based on the response.

## Notes

- The API call simulates fetching data from a real backend. In a production app you'd replace this with your actual data source.
- This example keeps the styling minimal (via [Bulma](https://bulma.io/)) to focus on the Alpine.js functionality.
