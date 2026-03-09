---
hidden: true
---

# configureGizmo

#### configureGizmo



Configure the interactive transform gizmo - translate, rotate, and scale handles shown in the viewport.



#### Signature



```typescript
configureGizmo(options: GizmoOptions): Promise<GizmoState>
```



#### Parameters

<table><thead><tr><th width="139.21875">Parameter</th><th width="171.54296875">Type</th><th width="109.12109375">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>options</code></td><td><code>GizmoOptions</code></td><td>Yes</td><td>Partial options to apply</td></tr></tbody></table>

#### GizmoOptions

```typescript
type GizmoOptions = {
  enabled?: boolean;       // Show/hide the gizmo
  advancedMode?: boolean;  // Show plane handles (TXY, TYZ, TZX, SXY, SYZ, SZX)
  localSpace?: boolean;    // Use local orientation instead of world
  snap?: {
    enabled?: boolean;       // Master snap toggle
    grid?: boolean;          // Grid snapping for translation
    angle?: boolean;         // Angle snapping for rotation
    gridResolution?: number; // Grid size in scene units (e.g., 0.5)
    angleParam?: number;     // Angle increment in degrees (e.g., 15)
    toFace?: boolean;        // Snap to faces of other objects
  };
};
```



#### GizmoState

```typescript
type GizmoState = {
  enabled: boolean;
  advancedMode: boolean;
  localSpace: boolean;
  snap: {
    enabled: boolean;
    grid: boolean;
    angle: boolean;
    gridResolution: number;
    angleParam: number;
    toFace: boolean;
  };
};
```



#### Returns



`Promise<GizmoState>` - the full gizmo state after applying the options.



#### Examples

```javascript
// Show the gizmo
await api.configureGizmo({ enabled: true });

// Hide the gizmo
await api.configureGizmo({ enabled: false });

// Enable advanced mode with local space orientation
await api.configureGizmo({ advancedMode: true, localSpace: true });

// Configure snapping
await api.configureGizmo({
  snap: {
    enabled: true,
    grid: true,
    gridResolution: 0.5,
    angle: true,
    angleParam: 15,
    toFace: true,
  },
});
```
