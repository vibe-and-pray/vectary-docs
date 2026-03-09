---
hidden: true
---

# createSphere



#### createSphere



Creates a sphere primitive and adds it to the scene.



#### Signature



```typescript
createSphere(options?: CreatePrimitiveOptions): Promise<SceneObject>
```



#### Parameters

<table><thead><tr><th width="135.75">Parameter</th><th width="229.08984375">Type</th><th width="90.328125">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>options</code></td><td><a href="./#createprimitiveoptions"><mark style="color:blue;"><code>CreatePrimitiveOptions</code></mark></a></td><td>No</td><td>Transform and primitive-specific settings</td></tr></tbody></table>



#### PrimitiveSphereSettings fields

<table><thead><tr><th width="268.70703125">Field</th><th width="147.96484375">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>sphereRadius</code></td><td><code>number</code></td><td>Radius of the sphere</td></tr><tr><td><code>sphereWidthSegments</code></td><td><code>number</code></td><td>Horizontal segments (longitude)</td></tr><tr><td><code>sphereHeightSegments</code></td><td><code>number</code></td><td>Vertical segments (latitude)</td></tr><tr><td><code>computeNormals</code></td><td><code>boolean</code></td><td>Recompute normals</td></tr></tbody></table>

#### Returns



`Promise<SceneObject>` - the created object.



#### Examples



```javascript
// Create with custom radius
const sphere = await api.createSphere({
  primitiveSettings: { sphereRadius: 2.5 },
});

// Create low-poly sphere
const sphere = await api.createSphere({
  name: "LowPolySphere",
  primitiveSettings: {
    sphereRadius: 1,
    sphereWidthSegments: 8,
    sphereHeightSegments: 6,
  },
});
```
