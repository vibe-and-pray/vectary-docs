---
hidden: true
---

# configureGizmo



#### configureGizmo



Configure the interactive transform gizmo - translate, rotate, and scale handles shown in the viewport.



#### Signature

```
configureGizmo(options: GizmoOptions): Promise<GizmoState>
```



#### Parameters

<table><thead><tr><th width="177.44140625">Parameter</th><th>Type</th><th width="106.859375">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>options</code></td><td><code>GizmoOptions</code></td><td>Yes</td><td>Partial options to apply</td></tr></tbody></table>



#### GizmoOptions



```ts
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
  handles?: GizmoHandleOptions; // Per-handle visibility controls
};
```



#### GizmoHandleOptions



```ts
type AxisOptions = boolean | { x?: boolean; y?: boolean; z?: boolean };

type GizmoHandleOptions = {
  translate?: AxisOptions;      // Translate arrow handles (X, Y, Z)
  rotate?: AxisOptions;         // Rotate ring handles (RX, RY, RZ)
  scale?: AxisOptions;          // Scale cube handles (SX, SY, SZ)
  translatePlane?: AxisOptions; // Plane translate handles (TXY, TYZ, TZX) — requires advancedMode
  scalePlane?: AxisOptions;     // Plane scale handles (SXY, SYZ, SZX) — requires advancedMode
  center?: boolean;             // Center pivot handle
};
```

`AxisOptions` accepts:

* `true` / `false` — toggle all axes at once
* `{ x?: boolean, y?: boolean, z?: boolean }` — per-axis control

\
**Notes:**

* Plane handles (TXY, TYZ, TZX, SXY, SYZ, SZX) are automatically hidden if either of their constituent axes is disabled. For example, disabling translate X also hides TXY and TZX.
* Plane handles additionally require `advancedMode: true` to be visible.
* Omitted groups are left unchanged from their current state.



#### GizmoState



```ts
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
  handles: {
    translate: { x: boolean; y: boolean; z: boolean };
    rotate: { x: boolean; y: boolean; z: boolean };
    scale: { x: boolean; y: boolean; z: boolean };
    translatePlane: { x: boolean; y: boolean; z: boolean };
    scalePlane: { x: boolean; y: boolean; z: boolean };
    center: boolean;
  };
};
```



### Returns



`Promise<GizmoState>` - the full gizmo state after applying the options.



### Examples



```js
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

// Restrict to X/Y plane translation only (no rotation, scale, or Z axis)
await api.configureGizmo({
  enabled: true,
  handles: {
    translate: { x: true, y: true, z: false },
    rotate: false,
    scale: false,
    translatePlane: false,
    scalePlane: false,
    center: false,
  },
});

// Disable only the Z rotation handle
await api.configureGizmo({
  handles: { rotate: { z: false } },
});

// Re-enable all handles
await api.configureGizmo({
  handles: {
    translate: true,
    rotate: true,
    scale: true,
    translatePlane: true,
    scalePlane: true,
    center: true,
  },
});
```
