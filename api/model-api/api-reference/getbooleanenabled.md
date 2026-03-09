---
hidden: true
---

# getBooleanEnabled

#### getBooleanEnabled



Check whether the boolean calculation is currently active on a boolean operator.



#### Signature

```typescript
getBooleanEnabled(objectNameOrId: string): Promise<boolean>
```



#### Parameters

<table><thead><tr><th width="167.81640625">Parameter</th><th width="116.51171875">Type</th><th width="107.5859375">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>objectNameOrId</code></td><td><code>string</code></td><td>Yes</td><td>Name or ID of the boolean operator object</td></tr></tbody></table>



#### Returns



`Promise<boolean>` - `true` if the boolean calculation is active.



#### Examples

```javascript
const isEnabled = await api.getBooleanEnabled("Boolean 1");
console.log("Boolean active:", isEnabled); // true or false
```
