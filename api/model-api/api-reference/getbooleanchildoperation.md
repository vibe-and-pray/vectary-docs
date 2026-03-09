---
hidden: true
---

# getBooleanChildOperation

#### getBooleanChildOperation



Get the current boolean operation type applied to a specific child of a boolean operator.



#### Signature

```typescript
getBooleanChildOperation(
  booleanNameOrId: string,
  childNameOrId: string
): Promise<string | null>
```



#### Parameters

<table><thead><tr><th width="173.54296875">Parameter</th><th width="117.0703125">Type</th><th width="106.20703125">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>booleanNameOrId</code></td><td><code>string</code></td><td>Yes</td><td>Name or ID of the parent boolean operator</td></tr><tr><td><code>childNameOrId</code></td><td><code>string</code></td><td>Yes</td><td>Name or ID of the child object</td></tr></tbody></table>



#### Returns



`Promise<string | null>` - one of `'UNION'`, `'INTERSECTION'`, `'A_MINUS_B'`, `'B_MINUS_A'`, or `null` if the child is not found in the operator.

<table><thead><tr><th width="262.87109375">Return value</th><th>Meaning</th></tr></thead><tbody><tr><td><code>'UNION'</code></td><td>Objects are combined</td></tr><tr><td><code>'INTERSECTION'</code></td><td>Only overlapping volume remains</td></tr><tr><td><code>'A_MINUS_B'</code></td><td>Child is subtracted from the parent</td></tr><tr><td><code>'B_MINUS_A'</code></td><td>Parent is subtracted from the child</td></tr><tr><td><code>null</code></td><td>Child not found in this boolean operator</td></tr></tbody></table>



#### Examples

```javascript
const op = await api.getBooleanChildOperation("Boolean 1", "Sphere");
console.log("Current operation:", op); // e.g., "A_MINUS_B"
```
