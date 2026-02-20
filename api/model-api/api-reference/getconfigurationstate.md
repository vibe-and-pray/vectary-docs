---
hidden: true
---

# getConfigurationState



#### getConfigurationState



Returns the current state of all variants and materials in the scene.



#### Signature

```typescript
getConfigurationState(): Promise<ConfigurationState[]>
```



#### Parameters

None.



#### Returns

`Promise<ConfigurationState[]>` — Array of variant and material states.

See [ConfigurationState](./#configurationstate) in Common Types.



#### Usage

```javascript
const state = await api.getConfigurationState();
console.log(state);
```



#### Example response

```javascript
[
  {
    variant: "Chair Type",
    variant_instanceId: "abc123",
    active_object: "Modern Chair",
    active_object_instanceId: "def456"
  },
  {
    object: "Table",
    object_instanceId: "ghi789",
    active_material: "Oak Wood",
    active_material_instanceId: "jkl012"
  }
]
```

