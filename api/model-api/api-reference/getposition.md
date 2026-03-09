---
hidden: true
---

# getPosition

#### getPosition



Returns the position of an object.

####

#### Signature

```typescript
getPosition(objectName: string): Promise<Vector3>
```

#### Parameters

<table><thead><tr><th>Name</th><th width="165.3203125">Type</th><th width="146.41015625">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>objectName</code></td><td><code>string</code></td><td>Yes</td><td>Object name</td></tr></tbody></table>

#### Returns

`Promise<Vector3>` - Object position as `{x, y, z}`.\
\
See [Vector3](./#vector3) in Common Types.

#### Usage

```javascript
const position = await api.getPosition("Chair");
console.log(position); // { x: 0, y: 100, z: 50 }
```

#### Notes

* Returns **local** coordinates (relative to parent), not world coordinates
* Coordinates use Z-up orientation
* Same value as `getObjects()[0].position`
* Only accepts string, not array
