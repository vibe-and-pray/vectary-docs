---
hidden: true
---

# deselectObjects

#### deselectObjects



Remove objects from the selection, or clear the entire selection.



#### Signature



```typescript
deselectObjects(
  objectNamesOrIds?: string | string[]
): Promise<void>
```



#### Parameters

<table><thead><tr><th width="172.20703125">Parameter</th><th width="178.83203125">Type</th><th width="70.546875">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>objectNamesOrIds</code></td><td><code>string | string[]</code></td><td>No</td><td>Objects to deselect. If omitted, clears the entire selection.</td></tr></tbody></table>

#### Returns



`Promise<void>`



#### Examples



```javascript
// Clear all selection
await api.deselectObjects();

// Deselect a specific object
await api.deselectObjects("MyCube");

// Deselect multiple objects
await api.deselectObjects(["MyCube", "MySphere"]);
```
