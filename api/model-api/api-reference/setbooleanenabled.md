---
hidden: true
---

# setBooleanEnabled

#### setBooleanEnabled



Enable or disable the boolean calculation on a boolean operator. When disabled, the children render individually as regular objects, as if the boolean operator were not there.



#### Signature

```
setBooleanEnabled(
  objectNameOrId: string,
  enabled: boolean
): Promise<void>
```



#### Parameters

<table><thead><tr><th width="175.83203125">Parameter</th><th width="129.7734375">Type</th><th width="106.23046875">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>objectNameOrId</code></td><td><code>string</code></td><td>Yes</td><td>Name or ID of the boolean operator object</td></tr><tr><td><code>enabled</code></td><td><code>boolean</code></td><td>Yes</td><td><code>true</code> to enable boolean calculation, <code>false</code> to disable</td></tr></tbody></table>

#### Returns



`Promise<void>`



#### Examples



```js
// Disable boolean — children render individually as regular objects
await api.setBooleanEnabled("Boolean 1", false);

// Re-enable boolean calculation
await api.setBooleanEnabled("Boolean 1", true);

// Works with object ID too
await api.setBooleanEnabled("23a580bc-400a-49ca-9757-c2b54ab15b8d", false);
```
