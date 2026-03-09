---
hidden: true
---

# createPolyhedron

#### createPolyhedron



Creates an icosahedron (polyhedron) primitive and adds it to the scene.



#### Signature

```typescript
createPolyhedron(options?: CreatePrimitiveOptions): Promise<SceneObject>
```

#### Parameters

<table><thead><tr><th width="120.51171875">Parameter</th><th width="223.328125">Type</th><th width="75.67578125">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>options</code></td><td><a href="./#createprimitiveoptions"><mark style="color:blue;"><code>CreatePrimitiveOptions</code></mark></a></td><td>No</td><td>Transform and primitive-specific settings</td></tr></tbody></table>

#### PrimitivePolyhedronSettings fields

<table><thead><tr><th width="250.4375">Field</th><th width="127.578125">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>polyhedronRadius</code></td><td><code>number</code></td><td>Radius</td></tr><tr><td><code>polyhedronDetail</code></td><td><code>number</code></td><td>Subdivision level (0 = base icosahedron)</td></tr><tr><td><code>computeNormals</code></td><td><code>boolean</code></td><td>Recompute normals</td></tr></tbody></table>



#### Returns

`Promise<SceneObject>` - the created object.



#### Examples

```javascript
// Base icosahedron
const poly = await api.createPolyhedron({
  primitiveSettings: { polyhedronRadius: 1, polyhedronDetail: 0 },
});

// Subdivided (approaching sphere)
const poly = await api.createPolyhedron({
  primitiveSettings: { polyhedronRadius: 1, polyhedronDetail: 3 },
});
```
