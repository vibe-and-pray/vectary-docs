---
hidden: true
---

# createCylinder

#### createCylinder



Creates a cylinder primitive and adds it to the scene.



#### Signature



```typescript
createCylinder(options?: CreatePrimitiveOptions): Promise<SceneObject>
```



#### Parameters

<table><thead><tr><th width="143.3203125">Parameter</th><th width="219.96875">Type</th><th width="82.08984375">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>options</code></td><td><a href="./#createprimitiveoptions"><code>CreatePrimitiveOptions</code></a></td><td>No</td><td>Transform and primitive-specific settings</td></tr></tbody></table>



#### PrimitiveCylinderSettings fields

<table><thead><tr><th width="279.60546875">Field</th><th width="152.89453125">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>cylinderRadiusTop</code></td><td><code>number</code></td><td>Top radius</td></tr><tr><td><code>cylinderRadiusBottom</code></td><td><code>number</code></td><td>Bottom radius</td></tr><tr><td><code>cylinderHeight</code></td><td><code>number</code></td><td>Height</td></tr><tr><td><code>cylinderRadiusSegments</code></td><td><code>number</code></td><td>Radial segments</td></tr><tr><td><code>cylinderHeightSegments</code></td><td><code>number</code></td><td>Height segments</td></tr><tr><td><code>cylinderCapSegments</code></td><td><code>number</code></td><td>Cap segments</td></tr><tr><td><code>cylinderCloseEnds</code></td><td><code>boolean</code></td><td>Close top/bottom caps</td></tr><tr><td><code>roundnessEnabled</code></td><td><code>boolean</code></td><td>Enable edge roundness</td></tr><tr><td><code>roundnessRadius</code></td><td><code>number</code></td><td>Roundness radius</td></tr><tr><td><code>roundnessRadiusSegments</code></td><td><code>number</code></td><td>Segments for roundness</td></tr><tr><td><code>computeNormals</code></td><td><code>boolean</code></td><td>Recompute normals</td></tr></tbody></table>

#### Returns



`Promise<SceneObject>` - the created object.



#### Examples

```javascript
// High-detail cylinder
const cyl = await api.createCylinder({
  primitiveSettings: {
    cylinderRadius: 1,
    cylinderHeight: 4,
    cylinderRadiusSegments: 64,
  },
});

// Tapered cylinder (different top/bottom radius)
const tapered = await api.createCylinder({
  primitiveSettings: {
    cylinderRadiusTop: 0.5,
    cylinderRadiusBottom: 1.5,
    cylinderHeight: 2,
  },
});
```
