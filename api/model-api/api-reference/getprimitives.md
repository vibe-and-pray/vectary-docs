---
hidden: true
---

# getPrimitives

#### getPrimitives



Returns the settings of a primitive object (Box, Sphere, Cylinder, etc.).



#### Signature

```typescript
getPrimitives(name: string): Promise<PrimitiveNodeSettings | null>
```

#### Parameters

<table><thead><tr><th width="158.6640625">Name</th><th width="136.04296875">Type</th><th width="121.1875">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>name</code></td><td><code>string</code></td><td>Yes</td><td>Name of the primitive object</td></tr></tbody></table>

#### Returns



`Promise<PrimitiveNodeSettings | null>` - Settings specific to the primitive type, or `null` if object not found or not a primitive.

The returned type depends on the primitive:

```typescript
type PrimitiveNodeSettings =
  | PrimitiveBoxSettings
  | PrimitiveSphereSettings
  | PrimitiveCylinderSettings
  | PrimitiveConeSettings
  | PrimitiveTorusSettings
  | PrimitiveTubeSettings
  | PrimitivePolyhedronSettings
  | PrimitiveSquarePlaneSettings
  | PrimitiveInfinitePlaneSettings;
```



#### Usage

```javascript
// Get Box settings
const boxSettings = await api.getPrimitives("Box");
console.log(boxSettings.boxDimensions); // { x: "100", y: "100", z: "100" }

// Get Sphere settings
const sphereSettings = await api.getPrimitives("Sphere");
console.log(sphereSettings.sphereRadius); // "50"

// Check if object is a primitive
const settings = await api.getPrimitives("MyObject");
if (settings === null) {
  console.log("Not a primitive or doesn't exist");
}
```



#### Primitive Types



**PrimitiveBoxSettings:**

```typescript
{
  boxDimensions: { x: string; y: string; z: string };
  boxSegments: { x: number; y: number; z: number };
  roundnessEnabled: boolean;
  roundnessRadius: string;
  roundnessRadiusSegments: number;
  computeNormals: boolean;
}
```

**PrimitiveSphereSettings:**

```typescript
{
  sphereRadius: string;
  sphereWidthSegments: number;
  sphereHeightSegments: number;
  computeNormals: boolean;
}
```

#### Notes

* Returns `null` for non-existent objects or non-primitives (no error thrown)
* Dimension values are returned as **strings**, not numbers
* Also works with Backdrop object
