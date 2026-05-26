# LWC Architecture, Component Structure, and Real Examples

## LWC Architecture

* Lightning Web Components (LWC) follows a component-based architecture.
* Each component is independent and reusable.
* Built using standard web technologies:

  * HTML
  * JavaScript
  * CSS
* LWC communicates with Salesforce backend using Apex.
* Uses one-way data binding and event-driven communication.
* Provides fast and secure UI development.

### Architecture Flow

User Interface → LWC Component → Apex Backend → Salesforce Database

---

# Component Structure

An LWC component contains multiple files.

### Main Files

1. **HTML File**

   * Defines UI structure.

2. **JavaScript File**

   * Handles logic and functionality.

3. **CSS File**

   * Adds styling.

4. **Meta XML File**

   * Controls component configuration and visibility.

### Example Structure

```plaintext id="u6b4rr"
helloComponent/
│── helloComponent.html
│── helloComponent.js
│── helloComponent.css
│── helloComponent.js-meta.xml
```

---

# Real Examples

## Example 1: Simple Greeting

### HTML

```html id="h8v0ya"
<template>
   <h1>Hello Salesforce</h1>
</template>
```

### JavaScript

```javascript id="7s2hcv"
import { LightningElement } from 'lwc';

export default class HelloComponent extends LightningElement {
}
```

---

## Example 2: Button Click Event

### HTML

```html id="r8u3fj"
<template>
   <lightning-button 
      label="Click Me"
      onclick={handleClick}>
   </lightning-button>
</template>
```

### JavaScript

```javascript id="otxgdf"
import { LightningElement } from 'lwc';

export default class ButtonDemo extends LightningElement {

   handleClick() {
      alert('Button Clicked');
   }
}
```

---

# Advantages of LWC

* Faster performance
* Reusable components
* Easy maintenance
* Modern UI development
* Better security and scalability
* Improved developer experience
