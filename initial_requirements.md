# OrderBoard.xyz - Personal Online Order Tracker - Initial Requirements

## 1. Overview

This document outlines the initial requirements for a personal online order tracking application. The application provides users with a Kanban-style board interface to track the status of their online orders.

## 2. User Management

* **User Registration and Authentication:**

  * Users must be able to create an account.
  * Users must be able to sign in and out securely.

## 3. Board Structure

* **Single Board Per User:**

  * Each user has a single, persistent board.

* **Predefined Lists (Columns):**

  * The board contains four predefined lists:

    * Ordered
    * Received
    * Returned
    * Kept
  * These lists cannot be renamed or deleted by the user.

## 4. Cards (Order Items)

* **Card Creation:**

  * Users can add new cards to any list.
  * Each card must contain the following attributes:

    * Product (mandatory)
    * Seller (optional)
    * Value (mandatory, numeric)
    * Checkbox (indicates order is completed or irrelevant)
    * Comment (optional)

* **Card Behavior:**

  * Cards can be dragged and dropped between lists.
  * Drag-and-drop operation updates the card status.

* **Card Visibility and Lifecycle:**

  * Ticking the checkbox marks a card as inactive.
  * Inactive cards are removed from the board view.
  * Deletion is a separate operation from checkbox ticking.

## 5. Activity Tracking

* **Timestamps:**

  * System must record:

    * Date and time of card creation.
    * Date and time when a card changes list (status change).
    * Date and time when a card is marked with a checkbox.

## 6. Due Date Management

* **Return Deadline:**

  * When a card is moved to the "Returned" list, a default due date is set (14 days from the move date).
  * Cards in "Returned" turn red if not ticked within 14 days.

## 7. Totals and Metrics

* **List Totals:**

  * Each list displays the sum of values for active (visible) cards only.

* **Historical Totals:**

  * Users can view totals for any selected date via a calendar/date picker.

* **Kept Items Summary:**

  * Moving a card to "Kept" marks it as inactive.
  * The sum of values in "Kept" reflects the user's total spent.

* **Active Order Value:**

  * Sum of values for all active items not in "Kept" gives the user a view of frozen capital.

* **Checkbox Impact on Totals:**

  * Ticking a card in any list except "Kept" excludes its value from all totals.

## 8. Card Deletion

* Users can delete any card explicitly, independent of its checkbox state.

---

**Note:** All interactions must be intuitive and responsive, following best UI/UX practices for a Kanban-style interface. Detailed user stories and interface wireframes will follow based on this requirements document.
