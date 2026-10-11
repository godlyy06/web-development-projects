# 💻 Pricing Plans Layout Page

**Project:** FreeCodeCamp – Responsive Web Design  
**Topic:** CSS Flexbox  
**Goal:** Build a responsive pricing plans layout and pass all 27 tests.

---

## 📌 Project Overview

Create a pricing page containing three subscription plans:

| Plan | Price | Position |
|------|-------|----------|
| Basic | $9/month | First |
| Pro | $19/month | Second |
| Premium | $29/month | Third |

The layout must use CSS Flexbox.

**Important Requirements:**
- All three plans must be displayed as cards.
- Cards must use Flexbox for their internal layout.
- The container must support wrapping.
- The Pro plan must be able to grow more than the other plans.
- All 27 FreeCodeCamp tests must pass.

---

# 📁 1. Project Setup

Create the following project structure:

```text
pricing-plans/
│
├── index.html
└── styles.css
```

### Checklist

- [ ] Create `index.html`
- [ ] Create `styles.css`
- [ ] Add the basic HTML document structure
- [ ] Link `styles.css` inside the HTML `<head>`
- [ ] Set an appropriate page title

**Hint:** Use the `<link>` element to connect your CSS file.

---

# 🏗️ 2. HTML Structure

## Step 1: Main Heading

Create the main heading of your page.

### Requirements

- [ ] Use an `h1` element.
- [ ] The heading must contain exactly: `Pricing Plans`

### Tests Covered

- Test 1: An `h1` element exists.
- Test 2: The `h1` contains `Pricing Plans`.

---

## Step 2: Pricing Container

Below your main heading, create a container for the pricing cards.

### Requirements

- [ ] Create a `div` element below the `h1`.
- [ ] Assign the class `pricing-container`.

### Tests Covered

- Test 3: A `div` exists below the `h1`.
- Test 4: The `div` has the class `pricing-container`.

---

## Step 3: Pricing Cards

Inside the pricing container, create three pricing cards.

Each card must be a `div` element.

### Requirements

- [ ] Create three `div` elements.
- [ ] Assign the class `pricing-card` to each.
- [ ] Give the first plan the additional class `basic-plan`.
- [ ] Give the second plan the additional class `pro-plan`.
- [ ] Give the third plan the additional class `premium-plan`.

### Required Class Combinations

| Card | Required Classes |
|------|------------------|
| Basic | `pricing-card basic-plan` |
| Pro | `pricing-card pro-plan` |
| Premium | `pricing-card premium-plan` |

**Hint:** An HTML element can have multiple classes.

### Tests Covered

- Test 8: Three pricing cards exist inside the container.
- Test 9: One card has the class `basic-plan`.
- Test 10: One card has the class `premium-plan`.
- Test 11: One card has the class `pro-plan`.

---

## Step 4: Card Content

Add the required content to each pricing card.

### Basic Plan

- [ ] Add an `h2` element.
- [ ] Set its text to `Basic`.
- [ ] Add a `p` element.
- [ ] Set its text to `$9/month`.

### Pro Plan

- [ ] Add an `h2` element.
- [ ] Set its text to `Pro`.
- [ ] Add a `p` element.
- [ ] Set its text to `$19/month`.

### Premium Plan

- [ ] Add an `h2` element.
- [ ] Set its text to `Premium`.
- [ ] Add a `p` element.
- [ ] Set its text to `$29/month`.

### Tests Covered

- Test 19: Basic contains an `h2` with `Basic`.
- Test 20: Basic contains a `p` with `$9/month`.
- Test 21: Pro contains an `h2` with `Pro`.
- Test 22: Pro contains a `p` with `$19/month`.
- Test 25: Premium contains an `h2` with `Premium`.
- Test 26: Premium contains a `p` with `$29/month`.

---

# 🎨 3. CSS Styling

## Step 5: Pricing Container

Create a CSS selector for `.pricing-container`.

### Requirements

- [ ] Create the `.pricing-container` selector.
- [ ] Set `display` to `flex`.
- [ ] Set `flex-wrap` to `wrap`.

### What You Are Learning

**display: flex**

Activates Flexbox for the container.

Its direct child elements become flex items.

**flex-wrap: wrap**

Allows flex items to move onto another row when
there is not enough available horizontal space.

### Tests Covered

- Test 5: The `.pricing-container` selector exists.
- Test 6: `display` is set to `flex`.
- Test 7: `flex-wrap` is set to `wrap`.

---

## Step 6: Pricing Card Styling

Create a CSS selector for `.pricing-card`.

This selector should apply the same base styling
to all three pricing cards.

### Requirements

- [ ] Create the `.pricing-card` selector.
- [ ] Set `display` to `flex`.
- [ ] Set `flex-direction` to `column`.
- [ ] Set `justify-content` to `space-between`.
- [ ] Set `flex` to `0 0 200px`.
- [ ] Set `border` to `2px solid black`.

### What You Are Learning

**display: flex**

Makes each pricing card a flex container.

**flex-direction: column**

Stacks the content vertically instead of horizontally.

**justify-content: space-between**

Distributes available space between the child elements.

**flex: 0 0 200px**

This is shorthand for three Flexbox properties:

| Property | Value | Meaning |
|----------|-------|---------|
| flex-grow | 0 | Do not grow by default |
| flex-shrink | 0 | Do not shrink |
| flex-basis | 200px | Initial size |

**border: 2px solid black**

Creates a visible black border around each card.

### Tests Covered

- Test 12: The `.pricing-card` selector exists.
- Test 13: `display` is set to `flex`.
- Test 14: `flex-direction` is set to `column`.
- Test 15: `justify-content` is set to `space-between`.
- Test 16: `flex` is set to `0 0 200px`.
- Test 17: `border` is set to `2px solid black`.

---

# 🔢 4. Flexbox Ordering

## Step 7: Basic Plan

Create a CSS selector for `.basic-plan`.

### Requirements

- [ ] Create the `.basic-plan` selector.
- [ ] Set `order` to `0`.

### Explanation

The `order` property controls the visual position
of an element inside a flex container.

The Basic plan must appear first.

### Tests Covered

- Test 18: Basic has `order: 0`.

---

## Step 8: Pro Plan

Create a CSS selector for `.pro-plan`.

### Requirements

- [ ] Create the `.pro-plan` selector.
- [ ] Set `order` to `1`.
- [ ] Set `flex-grow` to `2`.

### Explanation

**order: 1**

Places the Pro plan after the Basic plan.

**flex-grow: 2**

Allows the Pro plan to expand when additional
space is available in its flex row.

The Basic and Premium plans do not grow by default.

**Important:**

The Pro card also inherits the properties from
`.pricing-card`.

Its `flex-grow: 2` overrides the `flex-grow: 0`
defined by the shorthand `flex: 0 0 200px`.

### Tests Covered

- Test 23: Pro has `order: 1`.
- Test 24: Pro has `flex-grow: 2`.

---

## Step 9: Premium Plan

Create a CSS selector for `.premium-plan`.

### Requirements

- [ ] Create the `.premium-plan` selector.
- [ ] Set `order` to `2`.

### Explanation

The Premium plan must appear last.

The expected visual order is:

```text
+-------------+------------------+-------------+
|    BASIC    |       PRO        |   PREMIUM   |
|             |                  |             |
|  $9/month   |    $19/month     |  $29/month  |
+-------------+------------------+-------------+
```

The Pro card can become wider because of
its `flex-grow` property.

### Tests Covered

- Test 27: Premium has `order: 2` and appears last.

---

# 🧪 5. Testing & Validation

## HTML Tests

- [ ] Test 1 – h1 element exists
- [ ] Test 2 – h1 contains Pricing Plans
- [ ] Test 3 – div exists below h1
- [ ] Test 4 – div has pricing-container class
- [ ] Test 8 – Three pricing-card elements exist
- [ ] Test 9 – Basic card class exists
- [ ] Test 10 – Premium card class exists
- [ ] Test 11 – Pro card class exists
- [ ] Test 19 – Basic h2 is correct
- [ ] Test 20 – Basic price is correct
- [ ] Test 21 – Pro h2 is correct
- [ ] Test 22 – Pro price is correct
- [ ] Test 25 – Premium h2 is correct
- [ ] Test 26 – Premium price is correct

## CSS Container Tests

- [ ] Test 5 – pricing-container selector exists
- [ ] Test 6 – display: flex
- [ ] Test 7 – flex-wrap: wrap

## CSS Card Tests

- [ ] Test 12 – pricing-card selector exists
- [ ] Test 13 – display: flex
- [ ] Test 14 – flex-direction: column
- [ ] Test 15 – justify-content: space-between
- [ ] Test 16 – flex: 0 0 200px
- [ ] Test 17 – border: 2px solid black

## CSS Ordering Tests

- [ ] Test 18 – Basic order: 0
- [ ] Test 23 – Pro order: 1
- [ ] Test 24 – Pro flex-grow: 2
- [ ] Test 27 – Premium order: 2

---

# 🚀 6. Final Verification

Before submitting the project:

- [ ] Check that the stylesheet is correctly linked.
- [ ] Verify that all three pricing cards are visible.
- [ ] Verify that the cards appear in the correct order.
- [ ] Verify that the Pro card grows when space is available.
- [ ] Resize the browser window to test flex wrapping.
- [ ] Run the FreeCodeCamp tests.
- [ ] Confirm that all 27 tests pass.

---

# ✨ 7. Optional Design Improvements

After passing all required tests, you can personalize
the design without changing the required structure.

### Possible Improvements

- [ ] Add a background color to the page.
- [ ] Add spacing between the pricing cards.
- [ ] Add padding inside each card.
- [ ] Add rounded corners.
- [ ] Change the font family.
- [ ] Highlight the Pro plan visually.
- [ ] Add hover effects.
- [ ] Improve the layout for smaller screens.

**Important:** Keep the CSS properties required by
FreeCodeCamp unchanged so the tests continue to pass.

---

# 🏁 Project Completion

**Project:** Pricing Plans Layout Page

**Technology:** HTML5 / CSS3 / Flexbox

**Required Tests:** 27

**Status:** Not completed

### Learning Outcomes

After completing this project, you should understand:

1. How Flexbox containers work.
2. How flex items are arranged.
3. How `flex-direction` changes the layout.
4. How `justify-content` distributes space.
5. How `flex-wrap` handles limited space.
6. How `flex-grow` controls expansion.
7. How `flex-basis` defines an initial size.
8. How `order` changes the visual arrangement.

---

*FreeCodeCamp – Responsive Web Design Practice*