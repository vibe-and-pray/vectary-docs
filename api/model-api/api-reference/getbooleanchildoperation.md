---
hidden: true
---

# getBooleanChildOperation

#### getBooleanChildOperation



Get the current boolean operation type applied to a specific child of a boolean operator.



#### Signature

```
getBooleanChildOperation(
  booleanNameOrId: string,
  childNameOrId: string
): Promise<string | null>
```



#### Parameters

<table><thead><tr><th width="193.125">Parameter</th><th width="118.6796875">Type</th><th width="110.26171875">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>booleanNameOrId</code></td><td><code>string</code></td><td>Yes</td><td>Name or ID of the parent boolean operator</td></tr><tr><td><code>childNameOrId</code></td><td><code>string</code></td><td>Yes</td><td>Name or ID of the child object</td></tr></tbody></table>

#### Returns



`Promise<string | null>` - the current operation as an uppercase string, or `null` if the child is not found in the operator.

| Return value     | Meaning                                  |
| ---------------- | ---------------------------------------- |
| `'UNION'`        | Objects are combined into one            |
| `'INTERSECTION'` | Only the overlapping volume remains      |
| `'A_MINUS_B'`    | Child is subtracted from the base object |
| `null`           | Child not found in this boolean operator |



#### **Note:** <br>

* the return values are uppercase internal identifiers. To set an operation, use the PascalCase values accepted by `setBooleanChildOperation`: `'Union'`, `'Intersection'`, `'Subtract'`.



#### Examples



```js
const op = await api.getBooleanChildOperation("Boolean 1", "Sphere");
console.log("Current operation:", op); // e.g., "A_MINUS_B"

// Returns null if child is not part of this boolean operator
const op = await api.getBooleanChildOperation("Boolean 1", "NonExistent");
console.log(op); // null
```
