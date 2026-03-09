---
hidden: true
---

# setBooleanEnabled

#### setBooleanEnabled



Enable or disable the boolean calculation on a boolean operator. When disabled, the children render individually as if the boolean were not there.



#### Signature



```typescript
setBooleanEnabled(
  objectNameOrId: string,
  enabled: boolean
): Promise<void>
```



#### Parameters

<table><thead><tr><th width="178.51953125">Parameter</th><th width="117.83984375">Type</th><th width="106.703125">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>objectNameOrId</code></td><td><code>string</code></td><td>Yes</td><td>Name or ID of the boolean operator object</td></tr><tr><td><code>enabled</code></td><td><code>boolean</code></td><td>Yes</td><td><code>true</code> to enable calculation, <code>false</code> to disable</td></tr></tbody></table>

#### Returns



`Promise<void>`



#### Examples

```javascript
// Disable boolean — children render individually
await api.setBooleanEnabled("Boolean 1", false);

// Re-enable boolean calculation
await api.setBooleanEnabled("Boolean 1", true);
```
