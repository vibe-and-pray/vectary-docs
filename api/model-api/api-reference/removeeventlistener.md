---
hidden: true
---

# removeEventListener



#### removeEventListener



Removes a previously registered event listener.

<br>

#### **Signature**

```typescript
removeEventListener(eventName: string, callback?: (value: any) => void): Promise<void>
```



#### **Parameters**

<table><thead><tr><th width="155.0859375">Parameter</th><th width="136.0546875">Type</th><th width="117.73828125">Required</th><th>Description</th></tr></thead><tbody><tr><td>eventName</td><td>string</td><td>Yes</td><td>Name of the event</td></tr><tr><td>callback</td><td>function</td><td>No</td><td>The callback function to remove. If not provided, removes all listeners for this event name</td></tr></tbody></table>



#### **Returns**

`Promise<void>`



#### **Usage**

```javascript
// Define callback as a named function
const handleClick = (value) => {
  console.log("Clicked:", value);
};

// Add listener
await api.addEventListener("product_clicked", handleClick);

// Remove specific listener
await api.removeEventListener("product_clicked", handleClick);

// Or remove ALL listeners for this event
await api.removeEventListener("product_clicked");
```



#### **Notes**



* To remove a specific listener, pass the exact same function reference used in `addEventListener()`
* Anonymous functions cannot be removed individually — store the function in a variable first
* Call without callback to remove all listeners for the given event name<br>
