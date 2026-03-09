---
hidden: true
---

# createTorus

#### createTorus



Creates a torus primitive and adds it to the scene.



#### Signature

```typescript
createTorus(options?: CreatePrimitiveOptions): Promise<SceneObject>
```



#### Parameters

<table><thead><tr><th width="122.1796875">Parameter</th><th width="218.5625">Type</th><th width="106.1875">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>options</code></td><td><a href="./#createprimitiveoptions"><code>CreatePrimitiveOptions</code></a></td><td>No</td><td>Transform and primitive-specific settings</td></tr></tbody></table>

#### PrimitiveTorusSettings fields

| Field               | Type      | Description                                |
| ------------------- | --------- | ------------------------------------------ |
| `torusRingRadius`   | `number`  | Radius of the ring (center to tube center) |
| `torusTubeRadius`   | `number`  | Radius of the tube                         |
| `torusRingSegments` | `number`  | Segments along the ring                    |
| `torusTubeSegments` | `number`  | Segments along the tube                    |
| `computeNormals`    | `boolean` | Recompute normals                          |

#### Returns



`Promise<SceneObject>` - the created object.



#### Examples

```javascript
const torus = await api.createTorus({
  primitiveSettings: {
    torusRingRadius: 2,
    torusTubeRadius: 0.5,
    torusRingSegments: 48,
    torusTubeSegments: 24,
  },
});
```
