# Hog Project - React Testing Suite
## Overview
This is a comprehensive testing suite for a Hog (Pig) Management Application built with React. The tests verify core functionality including displaying hog profiles, filtering, sorting, adding new hogs, and interactive UI features.

## Test Coverage
The test suite validates the following features:

*** 1. Initial Load Display ***
Renders a tile/card for each hog from the dataset

Verifies hog names and images are correctly displayed

*** 2. Hog Details Expansion ***
Clicking on a hog tile reveals additional details:

Specialty

Weight

Greased status

Highest medal achieved

*** 3. Filtering by Greased Status ***
Checkbox filter to show only greased pigs

Non-greased pigs are hidden when filter is active

*** 4. Sorting Functionality ***
Sort hogs alphabetically by name

Sort hogs numerically by weight

Dynamic re-rendering of hog list based on sort selection

*** 5. Hide/Remove Feature ***
Each hog card has a "Hide Me" button

Clicking hides that specific hog from the display

*** 6. Add New Hog via Form ***
Form inputs for:

Name

Weight

Specialty

Greased (checkbox)

Submitting the form adds the new hog to the grid

*** 7. UI Component Structure ***
Hog tiles use Semantic UI Card components

Each card has the classes: "ui" and "card"

Proper ARIA labeling for accessibility
### Technologies Used
Testing Library: React Testing Library

Test Runner: Jest (presumed)

UI Framework: Semantic UI React

Language: JavaScript/React

### File Structure
text
src/
├── components/
│   └── App.js          # Main application component
├── porkers_data.js      # Hog dataset
└── __tests__/
    └── App.test.js      # This test suite
### Running the Tests
bash
### Run all tests
npm test

### Run with watch mode
npm test -- --watch

### Run specific test file
npm test App.test.js
*** Expected Test Outcomes ***
All tests should pass when the React application correctly implements:

Hog data mapping to Semantic UI Cards

Toggle functionality for details view

Greased status filtering

Name/weight sorting logic

Hide/remove state management

Form submission handler

### Data Structure (hogs)
Each hog object in porkers_data.js should contain:

javascript
{
  name: string,
  image: string,
  specialty: string,
  weight: number,
  greased: boolean,
  "highest medal achieved": string
}
### Component Requirements
To pass these tests, your <App /> component must provide:

A filter checkbox with label "Greased Pigs Only?"

A sort dropdown with label "Sort by:" and options "name" and "weight"

A form with inputs labeled "Name:", "Weight:", "Specialty:", "Greased?"

Each hog card with:

A heading (level 3) containing the hog's name

An image with alt text "Photo of {hog name}"

A button labeled "Hide Me"

Additional details shown/hidden on click

ARIA label "hog card" on each card container

### Debugging Tips
If tests fail:

Check that Semantic UI CSS is properly imported

Verify event handlers are correctly attached

Ensure state updates trigger re-renders

Confirm unique keys are used for list items
