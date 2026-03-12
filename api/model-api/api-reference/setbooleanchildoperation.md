---
hidden: true
---

# setBooleanChildOperation

#### setBooleanChildOperation



Change the boolean operation type applied to a specific child of a boolean operator.



#### Signature

```
setBooleanChildOperation(
  booleanNameOrId: string,
  childNameOrId: string,
  operation: 'Union' | 'Subtract' | 'Intersection'
): Promise<void>
```



#### Parameters

<table><thead><tr><th width="151.375">Parameter</th><th width="340.03515625">Type</th><th width="73.15625">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>booleanNameOrId</code></td><td><code>string</code></td><td>Yes</td><td>Name or ID of the parent boolean operator</td></tr><tr><td><code>childNameOrId</code></td><td><code>string</code></td><td>Yes</td><td>Name or ID of the child object</td></tr><tr><td><code>operation</code></td><td><code>'Union' | 'Subtract' | 'Intersection'</code></td><td>Yes</td><td>The operation to apply</td></tr></tbody></table>

#### Returns



`Promise<void>`



#### Notes



* Operation values are **case-sensitive** - only `'Union'`, `'Subtract'`, and `'Intersection'` are accepted. Other casing (e.g. `'union'`, `'UNION'`) will not work.
* The getter `getBooleanChildOperation` returns different uppercase values: `'Union'` → `'UNION'`, `'Subtract'` → `'A_MINUS_B'`, `'Intersection'` → `'INTERSECTION'`.
* In a boolean operator, one object acts as the **base** (the shape being operated on). Changing the operation of the base object has no visual effect — only non-base children produce a visible result.



#### Examples

```js
// Subtract Sphere from the base object
await api.setBooleanChildOperation("Boolean 1", "Sphere", "Subtract");

// Keep only the overlapping volume with Tube
await api.setBooleanChildOperation("Boolean 1", "Tube", "Intersection");

// Combine Box into the base object
await api.setBooleanChildOperation("Boolean 1", "Box", "Union");

// Read back the result (returns uppercase internal value)
const op = await api.getBooleanChildOperation("Boolean 1", "Sphere");
console.log(op); // "A_MINUS_B"
```
