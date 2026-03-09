---
hidden: true
---

# getSelectedObjects

#### getSelectedObjects



Returns the currently selected objects.



#### Signature



```typescript
getSelectedObjects(): Promise<SceneObject[]>
```



#### Parameters



None.



### Returns



`Promise<SceneObject[]>` — currently selected objects. Each object includes full scene data: transform, materials, primitive settings, and children. Returns an empty array if nothing is selected.



### Examples



```javascript
const selected = await api.getSelectedObjects();
console.log(selected.map(obj => obj.name));
```
