---
hidden: true
---

# setConfigurationState



Attempts to set an array with a [`ConfigurationState`](./#configurationstate) for present [`Variants`](../../../documentation/3d-configurator/floating-ui/variants-ui.md) and [`Materials`](../../../documentation/3d-configurator/floating-ui/materials-ui.md) in the model.

Returns an array with the final [`ConfigurationState`](./#configurationstate) that was set.

```typescript
setConfigurationState(
		state: Array<ConfigurationState>
): Promise<ConfigurationState[]>
```



<table><thead><tr><th width="230.69140625">Parameters</th><th>Description</th></tr></thead><tbody><tr><td>state</td><td><code>Array&#x3C;ConfigurationState></code><br><br>An array with different states for <a href="../../../documentation/3d-configurator/variants.md"><code>VariantSwitcherData</code></a> and <a href="../../../documentation/3d-configurator/floating-ui/materials-ui.md"><code>MaterialSwitcherData</code></a></td></tr></tbody></table>



Usage:

```javascript
await modelApi.setConfigurationState([
    {
        "variant": "Object Switcher",
        "active_object": "NUNO Stand"
    },
    {
        "object": "Adjustable Headband",
        "active_material": "White"
    }
]);
```

Return value:

```javascript
[
    {
        "switcher": "Object Switcher",
        "object": "NUNO Stand"
    },
    {
        "object": "Adjustable Headband",
        "material": "White"
    }
]
```
