# Modal Dialog JavaScript README

This README provides an overview of the JavaScript code that handles modal dialogs and overlays on a web page.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Usage](#usage)
- [Code Explanation](#code-explanation)
  - [Selecting Elements](#selecting-elements)
  - [Opening a Modal](#opening-a-modal)
  - [Closing a Modal](#closing-a-modal)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This JavaScript code is designed to manage the functionality of opening and closing modal dialogs and overlays on a web page. Modal dialogs are used to display content or interactions on top of the main page content.

## Features

- Clicking a button with the `data-modal-target` attribute opens the associated modal.
- Clicking the overlay closes all active modals.
- Clicking a button with the `data-close-button` attribute within a modal closes that specific modal.

## Usage

To use this JavaScript code, follow these steps:

1. Include the JavaScript file (`script.js`) in your HTML document.
2. Ensure that your HTML includes elements with the appropriate attributes:
   - Buttons with `data-modal-target` to open modals.
   - Buttons with `data-close-button` to close modals.
   - An overlay element with the `id` "overlay."
3. Customize the modals and their content as needed.
4. The JavaScript code handles the rest, including opening and closing modals and the overlay.

## Code Explanation

### Selecting Elements

- The code selects elements with `data-modal-target` and `data-close-button` attributes and stores them in variables.
- It also selects the overlay element by its `id` and stores it in a variable.

### Opening a Modal

- When a button with `data-modal-target` is clicked, it retrieves the corresponding modal element using `button.dataset.modalTarget` and passes it to the `openModal` function.
- The `openModal` function adds the "active" class to both the modal and the overlay, making them visible.

### Closing a Modal

- When the overlay is clicked, the code checks for all active modals (those with the "active" class) and closes them using the `closeModal` function.
- When a button with `data-close-button` is clicked, it finds the closest parent element with the class "modal" and passes it to the `closeModal` function to close the modal.
- The `closeModal` function removes the "active" class from both the modal and the overlay, hiding them.

## Contributing

Contributions to this code are welcome. If you have suggestions, improvements, or bug fixes, please submit a pull request.
