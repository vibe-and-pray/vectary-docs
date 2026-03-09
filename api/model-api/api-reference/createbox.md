---
hidden: true
---

# createBox

#### createBox

Creates a box primitive and adds it to the scene.



#### Signature



```typescript
createBox(options?: CreatePrimitiveOptions): Promise<SceneObject>
```



#### Parameters

<table><thead><tr><th width="121.6875">Parameter</th><th width="226.94140625">Type</th><th width="84.25">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>options</code></td><td><a href="./#createprimitiveoptions"><mark style="color:blue;"><code>CreatePrimitiveOptions</code></mark></a></td><td>No</td><td>Transform and primitive-specific settings</td></tr></tbody></table>



#### PrimitiveBoxSettings fields



<table><thead><tr><th width="234.8203125">Field</th><th width="252.08984375">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>boxDimensions</code></td><td><code>{ x: number; y: number; z: number }</code></td><td>Box size on each axis</td></tr><tr><td><code>boxSegments</code></td><td><code>{ x: number; y: number; z: number }</code></td><td>Subdivision segments per axis</td></tr><tr><td><code>roundnessEnabled</code></td><td><code>boolean</code></td><td>Enable rounded corners</td></tr><tr><td><code>roundnessRadius</code></td><td><code>number</code></td><td>Corner radius</td></tr><tr><td><code>roundnessRadiusSegments</code></td><td><code>number</code></td><td>Segments for roundness curve</td></tr><tr><td><code>computeNormals</code></td><td><code>boolean</code></td><td>Recompute normals</td></tr></tbody></table>

#### Returns



`Promise<SceneObject>` - the created object.



#### Examples



```javascript
// Create with defaults
const box = await api.createBox();

// Create at a specific position with a name
const box = await api.createBox({
  name: "MyBox",
  position: { x: 0, y: 1, z: 0 },
});

// Create with custom dimensions and roundness
const box = await api.createBox({
  name: "RoundedBox",
  primitiveSettings: {
    boxDimensions: { x: 2, y: 1, z: 3 },
    roundnessEnabled: true,
    roundnessRadius: 0.1,
  },
});
```
