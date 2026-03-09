---
hidden: true
---

# createCone



#### createCone



Creates a cone primitive and adds it to the scene.



#### Signature

```typescript
createCone(options?: CreatePrimitiveOptions): Promise<SceneObject>
```



#### Parameters

<table><thead><tr><th width="132.8828125">Parameter</th><th width="226.24609375">Type</th><th width="99.40234375">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>options</code></td><td><a href="./#createprimitiveoptions"><mark style="color:blue;"><code>CreatePrimitiveOptions</code></mark></a></td><td>No</td><td>Transform and primitive-specific settings</td></tr></tbody></table>



#### PrimitiveConeSettings fields

<table><thead><tr><th width="257.26953125">Field</th><th width="163.13671875">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>coneRadiusBottom</code></td><td><code>number</code></td><td>Radius at the base</td></tr><tr><td><code>coneHeight</code></td><td><code>number</code></td><td>Height of the cone</td></tr><tr><td><code>coneRadiusSegments</code></td><td><code>number</code></td><td>Radial segments</td></tr><tr><td><code>coneHeightSegments</code></td><td><code>number</code></td><td>Height segments</td></tr><tr><td><code>coneCloseEnds</code></td><td><code>boolean</code></td><td>Close the bottom cap</td></tr><tr><td><code>roundnessEnabled</code></td><td><code>boolean</code></td><td>Enable rounded base edge</td></tr><tr><td><code>roundnessRadius</code></td><td><code>number</code></td><td>Roundness radius</td></tr><tr><td><code>roundnessRadiusSegments</code></td><td><code>number</code></td><td>Segments for roundness curve</td></tr><tr><td><code>computeNormals</code></td><td><code>boolean</code></td><td>Recompute normals</td></tr></tbody></table>



#### Returns



`Promise<SceneObject>` - the created object.



#### Examples



```javascript
// Create cone with custom size and rotation
const cone = await api.createCone({
  rotation: { x: 0, y: 0, z: 90 },
  primitiveSettings: {
    coneRadiusBottom: 1.5,
    coneHeight: 3,
  },
});
```
