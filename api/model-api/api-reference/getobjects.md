---
hidden: true
---

# getObjects



#### getObjects



Returns objects from the scene by name or ID, or all objects if no parameter is specified.



#### **Signature**

```typescript
getObjects(objectNamesOrIds?: string | string[]): Promise<Object[]>
```



#### **Parameters**

<table><thead><tr><th width="188.05859375">Parameter</th><th width="167.140625">Type</th><th width="114.07421875">Required</th><th>Description</th></tr></thead><tbody><tr><td>objectNamesOrIds</td><td>string | string[]</td><td>No</td><td>Object name/ID or array of names/IDs. If omitted, returns all objects.</td></tr></tbody></table>

#### **Returns**

`Promise<Object[]>` - Array of matching objects.

See [Object](./#object) in Common Types.



#### **Usage**

```javascript
// Get all objects
const allObjects = await api.getObjects();

// Get single object by name
const sphere = await api.getObjects("Sphere");

// Get multiple objects by names
const objects = await api.getObjects(["Sphere", "Box"]);
```



#### **Notes**

* Wildcard `"*"` does NOT work — returns empty array
* Both string and array parameters are accepted
* Returns empty array if no objects match
