---
hidden: true
---

# setBooleanChildOperation

#### setBooleanChildOperation



Change the boolean operation type applied to a specific child of a boolean operator.



#### Signature

```typescript
setBooleanChildOperation(
  booleanNameOrId: string,
  childNameOrId: string,
  operation: 'Subtract' | 'Intersection' | 'Union'
): Promise<void>
```



#### Parameters

<table><thead><tr><th width="154.19921875">Parameter</th><th width="343.3359375">Type</th><th width="70.40234375">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>booleanNameOrId</code></td><td><code>string</code></td><td>Yes</td><td>Name or ID of the parent boolean operator</td></tr><tr><td><code>childNameOrId</code></td><td><code>string</code></td><td>Yes</td><td>Name or ID of the child object</td></tr><tr><td><code>operation</code></td><td><code>'Subtract' | 'Intersection' | 'Union'</code></td><td>Yes</td><td>The operation to apply</td></tr></tbody></table>

#### Returns

`Promise<void>`



#### Examples

```javascript
// Set child to use subtraction
await api.setBooleanChildOperation("Boolean 1", "Sphere", "Subtract");

// Set child to intersection
await api.setBooleanChildOperation("Boolean 1", "Sphere", "Intersection");

// Set child to union
await api.setBooleanChildOperation("Boolean 1", "Sphere", "Union");
```



#### **Notes**



* The operation values use PascalCase here (`'Subtract'`, `'Intersection'`, `'Union'`). The corresponding getter `getBooleanChildOperation` returns uppercase internal values (`'A_MINUS_B'`, `'INTERSECTION'`, `'UNION'`).
