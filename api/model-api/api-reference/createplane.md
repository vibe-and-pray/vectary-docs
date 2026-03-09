---
hidden: true
---

# createPlane

#### createPlane



Creates a square plane primitive and adds it to the scene.



#### Signature



```typescript
createPlane(options?: CreatePrimitiveOptions): Promise<SceneObject>
```



#### Parameters

<table><thead><tr><th width="121.1171875">Parameter</th><th width="222.91796875">Type</th><th width="82.125">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>options</code></td><td><a href="./#createprimitiveoptions"><code>CreatePrimitiveOptions</code></a></td><td>No</td><td>Transform and primitive-specific settings</td></tr></tbody></table>

#### PrimitiveSquarePlaneSettings fields

<table><thead><tr><th width="258.16796875">Field</th><th width="131.72265625">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>width</code></td><td><code>number</code></td><td>Width</td></tr><tr><td><code>depth</code></td><td><code>number</code></td><td>Depth</td></tr><tr><td><code>widthSegments</code></td><td><code>number</code></td><td>Segments along width</td></tr><tr><td><code>depthSegments</code></td><td><code>number</code></td><td>Segments along depth</td></tr><tr><td><code>roundnessEnabled</code></td><td><code>boolean</code></td><td>Enable rounded corners</td></tr><tr><td><code>roundnessRadius</code></td><td><code>number</code></td><td>Roundness radius</td></tr><tr><td><code>roundnessRadiusSegments</code></td><td><code>number</code></td><td>Segments for roundness</td></tr><tr><td><code>computeNormals</code></td><td><code>boolean</code></td><td>Recompute normals</td></tr></tbody></table>

#### Returns

`Promise<SceneObject>` - the created object.



#### Examples

```javascript
const plane = await api.createPlane({
  primitiveSettings: { width: 4, depth: 4, widthSegments: 10, depthSegments: 10 },
});
```
