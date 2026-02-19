# mapTextures \[new]

#### mapTextures

Overlays a texture on top of another. Useful for print-on-demand applications.

#### Signature

```typescript
mapTextures(
  baseTextureId: string, 
  overlayTextureId: string, 
  options?: MapOptions
): Promise<void>
```

#### Parameters

| Name               | Type         | Required | Description               |
| ------------------ | ------------ | -------- | ------------------------- |
| `baseTextureId`    | `string`     | Yes      | ID of the base texture    |
| `overlayTextureId` | `string`     | Yes      | ID of the overlay texture |
| `options`          | `MapOptions` | No       | Positioning options       |

```typescript
type MapOptions = {
 top?: number;    // Offset from top in pixels
 left?: number;   // Offset from left in pixels
 width?: number;  // Width in pixels
 height?: number; // Height in pixels
};
```

#### Returns

`Promise<void>`

#### Usage

```javascript
// Get base texture from material
const material = await api.getActiveMaterial("T-Shirt");
const baseId = material.baseColor.textureConfig.id;

// Add user's custom image
const overlayId = await api.addTexture(userFile);

// Map overlay onto base (full size)
await api.mapTextures(baseId, overlayId);

// Map with positioning
await api.mapTextures(baseId, overlayId, {
  top: 20,
  left: 30,
  width: 40
});
```

#### Notes



* Values are pixels relative to the base texture dimensions. For example, if the base texture is 512×512, passing `width: 512` will cover the full width.
* `width` has preference over `height` if both specified
* `top` and `left` default to 0
* The overlay is composited onto the base texture permanently
* Ideal for product customization (t-shirts, mugs, phone cases)
