---
hidden: true
---

# createTube

#### createTube



Creates a tube (hollow cylinder) primitive and adds it to the scene.



#### Signature

```typescript
createTube(options?: CreatePrimitiveOptions): Promise<SceneObject>
```



#### Parameters

<table><thead><tr><th width="141.68359375">Parameter</th><th width="218.48828125">Type</th><th width="85.69140625">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>options</code></td><td><a href="./#createprimitiveoptions"><code>CreatePrimitiveOptions</code></a></td><td>No</td><td>Transform and primitive-specific settings</td></tr></tbody></table>



#### PrimitiveTubeSettings fields

<table><thead><tr><th width="258.2890625">Field</th><th width="143.0078125">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>tubeRadiusIn</code></td><td><code>number</code></td><td>Inner radius</td></tr><tr><td><code>tubeRadiusOut</code></td><td><code>number</code></td><td>Outer radius</td></tr><tr><td><code>tubeHeight</code></td><td><code>number</code></td><td>Height</td></tr><tr><td><code>tubeRadiusSegments</code></td><td><code>number</code></td><td>Radial segments</td></tr><tr><td><code>tubeHeightSegments</code></td><td><code>number</code></td><td>Height segments</td></tr><tr><td><code>tubeSideSegments</code></td><td><code>number</code></td><td>Side segments (wall thickness)</td></tr><tr><td><code>roundnessEnabled</code></td><td><code>boolean</code></td><td>Enable edge roundness</td></tr><tr><td><code>roundnessRadius</code></td><td><code>number</code></td><td>Roundness radius</td></tr><tr><td><code>roundnessRadiusSegments</code></td><td><code>number</code></td><td>Segments for roundness</td></tr><tr><td><code>computeNormals</code></td><td><code>boolean</code></td><td>Recompute normals</td></tr></tbody></table>

#### Returns



`Promise<SceneObject>` - the created object.



#### Examples



```javascript
const tube = await api.createTube({
  primitiveSettings: {
    tubeRadiusIn: 0.5,
    tubeRadiusOut: 1,
    tubeHeight: 3,
  },
});
```
