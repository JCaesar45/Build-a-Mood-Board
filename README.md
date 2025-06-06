```
# Mood Board React App

## Overview

This project is a React application that builds a **Mood Board** — a visual collage of images and text that conveys ideas, goals, or feelings about a specific theme. The app uses reusable React components to create an interactive and styled mood board.

The CSS for styling the mood board is provided. Your task is to create functional React components that render the mood board content dynamically based on props.

---

## Features

* **Reusable `MoodBoardItem` component** that accepts `color`, `image`, and `description` props.
* Each `MoodBoardItem` displays:

  * A container with a background color from the `color` prop.
  * An image element sourced from the `image` prop.
  * A description rendered as a heading from the `description` prop.
* A parent `MoodBoard` component that:

  * Displays a heading titled **Destination Mood Board**.
  * Renders at least three `MoodBoardItem` components with different data.
* Fully responsive and styled according to provided CSS.

---

## Components

### `MoodBoardItem`

* Props:

  * `color` (string): Sets the background color of the item container.
  * `image` (string): URL of the image to display.
  * `description` (string): Text describing the mood board item.
* Structure:

  * Top-level `<div>` with class `mood-board-item` and inline background color.
  * `<img>` with class `mood-board-image` and `src` set to the image prop.
  * `<h3>` with class `mood-board-text` displaying the description.

### `MoodBoard`

* Structure:

  * Top-level `<div>`.
  * `<h1>` with class `mood-board-heading` displaying "Destination Mood Board".
  * A child `<div>` with class `mood-board` containing multiple `MoodBoardItem` components.
* Renders at least three `MoodBoardItem` components with unique props.

---

## Usage

1. Clone or download the repository.
2. Run the app using your React environment (e.g., `npm start`).
3. The mood board will display on the root element with the specified images and descriptions.

---

## Example

```jsx
// MoodBoardItem component
export function MoodBoardItem({ color, image, description }) {
  return (
    <div className="mood-board-item" style={{ backgroundColor: color }}>
      <img src={image} className="mood-board-image" alt={description} />
      <h3 className="mood-board-text">{description}</h3>
    </div>
  );
}

// MoodBoard component
export function MoodBoard() {
  return (
    <div>
      <h1 className="mood-board-heading">Destination Mood Board</h1>
      <div className="mood-board">
        <MoodBoardItem
          color="#FFDDC1"
          image="https://cdn.freecodecamp.org/curriculum/labs/santorini.jpg"
          description="Santorini"
        />
        <MoodBoardItem
          color="#C1E1DC"
          image="https://cdn.freecodecamp.org/curriculum/labs/ship.jpg"
          description="Ship Voyage"
        />
        <MoodBoardItem
          color="#F9E79F"
          image="https://cdn.freecodecamp.org/curriculum/labs/grass.jpg"
          description="Lush Grass"
        />
      </div>
    </div>
  );
}
``

---

## Additional Resources

* Images used in the mood board:

  * [Santorini](https://cdn.freecodecamp.org/curriculum/labs/santorini.jpg)
  * [Ship Voyage](https://cdn.freecodecamp.org/curriculum/labs/ship.jpg)
  * [Lush Grass](https://cdn.freecodecamp.org/curriculum/labs/grass.jpg)
  * [Pathway](https://cdn.freecodecamp.org/curriculum/labs/pathway.jpg)
  * [Shore](https://cdn.freecodecamp.org/curriculum/labs/shore.jpg)
  * [Pigeon](https://cdn.freecodecamp.org/curriculum/labs/pigeon.jpg)

---

## Testing

* The project includes tests that verify:

  * Export and rendering of `MoodBoardItem` and `MoodBoard` components.
  * Proper application of class names and inline styles.
  * Rendering of images and descriptions based on props.
  * Rendering at least three mood board items.
  * Correct mounting to the root DOM element.

---

## License

This project is open-source and available under the MIT License.
