---
hidden: true
---

# moveObjects

Moves the specified objects within the scene’s hierarchy.

```tsx
moveObjects(
	objectNamesOrIds: string | string[];
	insertUnderId?: string;
	insertBeforeId?: string;
	keepGlobalPosition?: boolean;
): Promise<void}>
```

<table><thead><tr><th width="200.94140625">Parameters</th><th width="355.171875">Description</th><th>Type</th></tr></thead><tbody><tr><td>objectNamesOrIds</td><td>Name/s or id/s of the objects to duplicate.</td><td><code>string</code> | <code>string[]</code></td></tr><tr><td>insertUnderId</td><td>Specifies the group id to move the objects under.</td><td><code>string</code></td></tr><tr><td>insertBeforeId</td><td>Specifies the object id to move the objects before.</td><td><code>string</code></td></tr><tr><td>keepGlobalPosition</td><td>Specifies weather or not to keep the current global transformation of the object/s to move, or to apply the matrix transform of the new parents’ (defaults to <code>true</code>).</td><td><code>boolean</code></td></tr></tbody></table>



Usage:

```jsx
*const* group = (await modelApi.getObjects('Group'))[0];            
await modelApi.moveObjects('Plant Pot', group.id, null, false);
```
