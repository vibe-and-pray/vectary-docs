---
hidden: true
---

# getRotation

### getRotation

Returns the rotation of an object.



#### Signature

```typescript
getRotation(objectName: string): Promise<Euler>
```

#### Parameters

<table><thead><tr><th>Name</th><th>Type</th><th width="172.76953125">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>objectName</code></td><td><code>string</code></td><td>Yes</td><td>Object name</td></tr></tbody></table>

#### Returns

`Promise<Euler>` — Object rotation as `{x, y, z, order}`.

* `x`, `y`, `z` — rotation angles in **degrees**
* `order` — rotation order (e.g., `"XYZ"`)

See [Euler](./#euler) in Common Types.\
<br>

#### Usage

```javascript
const rotation = await api.getRotation("Chair");
console.log(rotation); // { x: 0, y: 45, z: 0, order: "XYZ" }
```

#### Notes

* Values are in **degrees**, not radians
* Returns **local** rotation (relative to parent)
* Same value as `getObjects()[0].rotation`
* Only accepts string, not array

<br>
