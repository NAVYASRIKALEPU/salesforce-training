# Parent-Child Communication, Events, and Data Flow

## Parent-Child Communication

* In Lightning Web Components (LWC), components communicate with each other.
* A parent component can send data to a child component using `@api` properties.
* Child components can send information back to parent components using events.
* Communication improves component reusability and modular design.

### Parent to Child Communication

* Uses public properties with `@api` decorator.
* Parent passes values through HTML attributes.

### Example

#### Parent HTML

```html
<c-child message="Hello Child"></c-child>
```

#### Child JS

```javascript
import { LightningElement, api } from 'lwc';

export default class Child extends LightningElement {
    @api message;
}
```

---

# Events in LWC

* Events are used for communication from child to parent.
* LWC uses custom events for interaction.
* Events help components respond to user actions.

### Common Event Types

* Click Events
* Input Events
* Custom Events

### Example of Custom Event

#### Child JS

```javascript
handleClick() {
    const event = new CustomEvent('showmessage');
    this.dispatchEvent(event);
}
```

#### Parent HTML

```html
<c-child onshowmessage={handleMessage}></c-child>
```

---

# Data Flow

* Data flow means movement of data between components.
* Parent → Child uses properties.
* Child → Parent uses events.
* Proper data flow improves application performance and maintainability.
* LWC follows one-way data binding for better control.

---

# Advantages

* Improves component communication.
* Makes applications modular and reusable.
* Enhances user interaction.
* Supports clean and maintainable code.
* Helps build modern Salesforce UI applicatio
