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



`Promise<SceneObject[]>` - array of currently selected objects. Returns an empty array if nothing is selected.



### Examples



```javascript
const selected = await api.getSelectedObjects();
console.log(selected.map(obj => obj.name));
```
