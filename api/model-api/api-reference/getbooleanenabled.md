---
hidden: true
---

# getBooleanEnabled

#### getBooleanEnabled



Get whether the boolean calculation is currently active on a boolean operator.



#### Signature



```
getBooleanEnabled(objectNameOrId: string): Promise<boolean>
```



#### Parameters

<table><thead><tr><th width="182.1875">Parameter</th><th width="117.6640625">Type</th><th width="124.60546875">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>objectNameOrId</code></td><td><code>string</code></td><td>Yes</td><td>Name or ID of the boolean operator object</td></tr></tbody></table>



#### Returns



`Promise<boolean>` - `true` if the boolean calculation is active, `false` if disabled.



#### Examples

```js
const isEnabled = await api.getBooleanEnabled("Boolean 1");
console.log("Boolean active:", isEnabled); // true or false

// Works with object ID too
const isEnabled = await api.getBooleanEnabled("23a580bc-400a-49ca-9757-c2b54ab15b8d");
```
