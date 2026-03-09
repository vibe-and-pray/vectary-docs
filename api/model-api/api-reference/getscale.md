---
hidden: true
---

# getScale

#### getScale

Returns the scale of an object.



#### Signature

```typescript
getScale(objectName: string): Promise<Vector3>
```



#### Parameters

<table><thead><tr><th>Name</th><th>Type</th><th width="172.00390625">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>objectName</code></td><td><code>string</code></td><td>Yes</td><td>Object name</td></tr></tbody></table>

#### Returns

`Promise<Vector3>` - Object scale as `{x, y, z}`.\
See [Vector3](./#vector3) in Common Types.<br>

#### Usage

```javascript
const scale = await api.getScale("Chair");
console.log(scale); // { x: 1, y: 1, z: 1 }
```

#### Notes

* Default scale is `{ x: 1, y: 1, z: 1 }`
* Returns **local** scale (relative to parent)
* Only accepts string, not array
