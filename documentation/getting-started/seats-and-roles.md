---
description: Roles define what each workspace member can see and do.
---

# Seats and Roles



### Inviting members <a href="#block-0a23bb7ea7504d10a056b7a4d3cd266c" id="block-0a23bb7ea7504d10a056b7a4d3cd266c"></a>



Open workspace settings (gear icon) → **Workspace** tab to invite members.

<figure><img src="../../.gitbook/assets/image (560).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (562).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" icon="lock-keyhole" %}
Only the workspace **Owner** and **Manager** can access these settings. Other members can neither invite nor view the workspace member list.
{% endhint %}



Enter an email, pick a role, and send the invite:

<div align="left"><figure><img src="../../.gitbook/assets/image (565).png" alt="" width="375"><figcaption></figcaption></figure></div>

Role can be changed at any time from the same list:

<div align="left"><figure><img src="../../.gitbook/assets/image (566).png" alt="" width="375"><figcaption></figcaption></figure></div>



If the invited person doesn't have a Vectary account yet, they'll get an email invite to sign up. Your workspace will be added to the invited user's workspace list.

If the user already has an account, they don't need to do anything — no email confirmation is required, as the invite is accepted automatically.





## Roles: <a href="#owner" id="owner"></a>





### Owner <a href="#owner" id="owner"></a>



As the primary account holder, the Owner is responsible for managing the contract, creating the workspace, and overseeing billing. This role possesses managerial privileges, overseeing all features and functionalities within the workspace.



✅  full control over the workspace

***

### Manager <a href="#manager" id="manager"></a>



Managers hold a high-ranking role within a workspace, similar to the Owner, with the exception of not having access to billing information and not being able to delete a workspace. They oversee member access and permissions, and manage project editing and sharing. Managers can add, remove, and approve member requests, move projects between workspaces, and make projects public. They have full editing capabilities in the Studio, ensuring secure workspace management.



✅  possesses nearly the same rights as the Owner

❌  does not have access to billing information and cannot delete the workspace

***

### Editor <a href="#editor" id="editor"></a>



Editors primarily work with 3D data, import CAD files, and create interactions and animations. While they can create folders and move projects within their workspace, they cannot delete projects or move them outside the workspace. Editors can be internal team members or external professionals managed by workspace managers.



✅  ability to edit all projects within the workspace

❌  lacks permission to:

* manage workspace members
* delete workspaces, folders, projects, or comments
* export projects or change project sharing settings

***

### Collaborator <a href="#collaborator" id="collaborator"></a>



Collaborators have restricted access, with the ability to view or comment on projects, but not to edit them, which ensures project integrity. They can see all shared projects within the workspace but must be approved by a manager to join, ensuring a secure method for sharing sensitive data. This role offers more expansive viewing capabilities compared to the Viewer role.



✅  able to view all projects in the workspace and can perform all operations related to comments, except for deletion

❌  inherits the same restrictions as the **Editor**, with the additional inability to edit projects

***

### **Viewer** <a href="#viewer" id="viewer"></a>



Viewers have restricted access, limited to only seeing projects for which they have direct links. While they are technically part of the workspace, they cannot see the overall content or project lists. This role is particularly useful for sharing projects privately without allowing these users to comment or see existing comments.



✅  access only to view projects for which they possess a direct link

❌  inherits the same restrictions as a Collaborator, with the additional limitation of not being able to see projects within the workspace

***

### Permissions overview <a href="#permissions-overview" id="permissions-overview"></a>



<table><thead><tr><th width="237.9609375">Actions</th><th width="95.2421875" data-type="checkbox">Owner</th><th width="96.16796875" data-type="checkbox">Manager</th><th width="82.76953125" data-type="checkbox">Editor</th><th width="124.46484375" data-type="checkbox">Collaborator</th><th width="88.5390625" data-type="checkbox">Viewer</th></tr></thead><tbody><tr><td>Access to billing information</td><td>true</td><td>false</td><td>false</td><td>false</td><td>false</td></tr><tr><td>Managing workspace members</td><td>true</td><td>true</td><td>false</td><td>false</td><td>false</td></tr><tr><td>Deleting workspaces, folders, projects, comments</td><td>true</td><td>true</td><td>false</td><td>false</td><td>false</td></tr><tr><td>Exporting projects and changing project sharing settings</td><td>true</td><td>true</td><td>false</td><td>false</td><td>false</td></tr><tr><td>Project editing</td><td>true</td><td>true</td><td>true</td><td>false</td><td>false</td></tr><tr><td>Access to view all projects and comments in workspace</td><td>true</td><td>true</td><td>true</td><td>true</td><td>false</td></tr><tr><td>Read and add comments</td><td>true</td><td>true</td><td>true</td><td>true</td><td>false</td></tr><tr><td>Viewing projects via direct links</td><td>true</td><td>true</td><td>true</td><td>true</td><td>true</td></tr></tbody></table>

<br>
