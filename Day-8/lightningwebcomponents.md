# Lightning Web Components (LWC)

## HTML + JS + Meta XML

LWC components mainly contain:

### HTML File

* Creates the UI structure.
* Contains text, buttons, forms, etc.

### JavaScript File

* Handles logic and functionality.
* Used for variables and events.

### Meta XML File

* Controls component configuration.
* Defines where the component can be used.

Example Structure:

```plaintext id="w9kc5j"
helloWorld/
│── helloWorld.html
│── helloWorld.js
│── helloWorld.js-meta.xml
```

---

## Component Lifecycle

Lifecycle hooks are methods that run at different stages of a component.

### Important Hooks

* `constructor()` → Initializes component.
* `connectedCallback()` → Runs when component loads.
* `renderedCallback()` → Runs after rendering.
* `disconnectedCallback()` → Runs when component is removed.

Example:

```javascript id="t9br6t"
connectedCallback() {
   console.log('Component Loaded');
}
```

---

## Real Examples

### Greeting Component

```html id="dx1m6l"
<template>
   <h1>Hello User!</h1>
</template>
```

### Button Click Example

```html id="0pnkkw"
<template>
   <lightning-button 
      label="Click"
      onclick={handleClick}>
   </lightning-button>
</template>
```

```javascript id="ft7g9q"
handleClick() {
   alert('Button Clicked');
}
```

---

## Modern Salesforce UI

* LWC creates fast and responsive UI.
* Uses reusable components.
* Improves user experience and performance.
* Built using HTML, CSS, and JavaScript.
* Preferred framework for modern Salesforce development.
