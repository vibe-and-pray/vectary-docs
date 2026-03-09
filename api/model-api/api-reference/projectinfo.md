---
hidden: true
---

# projectInfo

#### projectInfo



Returns information about the current project.



#### Signature

```typescript
projectInfo(): Promise<ProjectInfo>
```

#### Parameters



None.



#### Returns

`Promise<ProjectInfo>` - Object containing project details:

```typescript
type ProjectInfo = {
  projectName: string;
  modelId: string;
  modelIdBase62: string;
  publishedId: string;
  workspaceId: string;
}
```

<table><thead><tr><th width="204.37890625">Property</th><th width="156.19140625">Type</th><th>Description</th></tr></thead><tbody><tr><td>projectName</td><td>string</td><td>Name of the project</td></tr><tr><td>modelId</td><td>string</td><td>Unique model identifier (UUID)</td></tr><tr><td>modelIdBase62</td><td>string</td><td>Model ID in Base62 format</td></tr><tr><td>publishedId</td><td>string</td><td>Published version identifier</td></tr><tr><td>workspaceId</td><td>string</td><td>Workspace identifier</td></tr></tbody></table>

#### Usage

```javascript
const info = await api.projectInfo();
console.log(info.projectName);
console.log(info.modelId);
```







