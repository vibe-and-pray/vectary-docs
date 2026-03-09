---
hidden: true
---

# selectObjects

#### selectObjects



Select one or more objects in the scene by name or ID.



#### Signature



```typescript
selectObjects(
  objectNamesOrIds: string | string[],
  addToSelection?: boolean
): Promise<SceneObject[]>
```



#### Parameters

<table><thead><tr><th width="191.9765625">Parameter</th><th width="174.09375">Type</th><th width="77.6484375">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>objectNamesOrIds</code></td><td><code>string | string[]</code></td><td>Yes</td><td>Name(s) or ID(s) of objects to select</td></tr><tr><td><code>addToSelection</code></td><td><code>boolean</code></td><td>No</td><td>If <code>true</code>, adds to existing selection. If <code>false</code> or omitted, replaces current selection.</td></tr></tbody></table>



#### Returns



`Promise<SceneObject[]>` — the resulting selected objects. Each object includes full scene data: transform, materials, primitive settings, and children.



#### Examples



```javascript
// Select a single object (replaces current selection)
const selected = await api.selectObjects("MyCube");

// Select multiple objects
const selected = await api.selectObjects(["MyCube", "MySphere"]);

// Add to existing selection without clearing it
const selected = await api.selectObjects("AnotherObject", true);

// Select a child inside a boolean operator by ID
const selected = await api.selectObjects("a1b2c3d4-...");
```



#### **Notes:**



* Objects inside boolean operators are not directly clickable in the viewport. Use their ID to select them programmatically.
