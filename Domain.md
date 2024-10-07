# ***Domain***

# **OpenStack Domain Related Command**

Here are some commonly used OpenStack domain-related commands:

### **1. List Domains:** To list all the domains in OpenStack:

```bash
openstack domain list
```

### **2. Show Domain Details:** To show detailed information about a specific domain:

```bash
openstack domain show <domain-name-or-ID>
```

### **3. Create a Domain:** To create a new domain:

```bash
openstack domain create --description "<description>" <domain-name>
```

### **4. Delete a Domain:** To delete a specific domain:

```bash
openstack domain delete <domain-name-or-ID>
```

### **4. Update Domain:** To update a domain’s properties:

```bash
openstack domain set --name <new-domain-name> --description "<new-description>" <domain-name-or-ID>
```

### **5. Enable or Disable a Domain:** To enable or disable a domain:

```bash
openstack domain set --enable <domain-name-or-ID>
```

or

```bash
openstack domain set --disable <domain-name-or-ID>
```

# **Server**

# **OpenStack server related command**

### **1. List Servers:** To list all the servers (instances) in your OpenStack environment:

```bash
openstack server list
```

### **2. Show Server Details:** To display detailed information about a specific server:

```bash
openstack server show <server-name-or-ID>
```

### **3. Create a Server:** To create a new server:

```bash
openstack server create --flavor <flavor> --image <image> --network <network> <server-name>
```

Replace `<flavor>`, `<image>`, `<network>`, and `<server-name>` with your desired values.

### **4. Delete a Server:** To delete a specific server:

```bash
openstack server delete <server-name-or-ID>
```

### **5. Reboot a Server:** To reboot a server (hard or soft):

```bash
openstack server reboot --soft <server-name-or-ID>  # Soft reboot
```

or

```bash
openstack server reboot <server-name-or-ID>  # Hard reboot (default)
```

### **6. Resize a Server:** To resize a server to a different flavor:

```bash
openstack server resize <server-name-or-ID> --flavor <new-flavor>
```

### **7. Rebuild a Server:** To rebuild a server with a new image:

```bash
openstack server rebuild <server-name-or-ID> --image <new-image>
```

### **8. Change Server Status:** To set a server to active or paused:

```bash
openstack server pause <server-name-or-ID>  # Pause
```

or

```bash
openstack server unpause <server-name-or-ID>  # Unpause
```

### **9. List Server Volumes:** To list volumes attached to a server:

```bash
openstack server show <server-name-or-ID> -f value -c id
```

### **10. Attach a Volume to a Server:** To attach a volume to a server:

```bash
openstack server add volume <server-name-or-ID> <volume-name-or-ID>
```

### **11. Detach a Volume from a Server:** To detach a volume from a server:

```bash
openstack server remove volume <server-name-or-ID> <volume-name-or-ID>
```

# **Image**

# OpenStack image related command

### **1. List Images:** To list all images available in your OpenStack environment:

```bash
openstack image list
```

### **2. Show Image Details:** To display detailed information about a specific image:

```bash
openstack image show <image-name-or-ID>
```

### **3. Create an Image:** To create a new image from an existing server:

```bash
openstack image create --name <image-name> --source <server-name-or-ID>

```

Or, to create an image from a file:

```bash
openstack image create --name <image-name> --file <path-to-image-file> --disk-format <format>
```

### **4. Delete an Image:** To delete a specific image:

```bash
openstack image delete <image-name-or-ID>
```

### **5. Update an Image:** To update properties of an image:

```bash
openstack image set --name <new-image-name> <image-name-or-ID>
```

### **6. Download an Image:** To download an image file:

```bash
openstack image save --file <output-file-name> <image-name-or-ID>
```

### **7. Upload an Image:** To upload an image file to the OpenStack image service (Glance):

```bash
openstack image create --name <image-name> --file <path-to-image-file> --disk-format <format>
```

### **8. List Image Tags:** To list tags associated with an image:

```bash
openstack image show <image-name-or-ID> -f value -c tags
```

### **9. Add Tags to an Image:** To add tags to an image:

```bash
openstack image set --tag <tag1> --tag <tag2> <image-name-or-ID>
```

### **10. Remove Tags from an Image:** To remove a tag from an image:

```bash
openstack image unset --tag <tag> <image-name-or-ID>
```

# **Project**

# **OpenStack project related command**

### **1. List Projects:** To list all projects in your OpenStack environment:

```bash
openstack project list
```

### **2. Show Project Details:** To display detailed information about a specific project:

```bash
openstack project show <project-name-or-ID>
```

### **3. Create a Project:** To create a new project:

```bash
openstack project create --description "<description>" <project-name>
```

### **4. Delete a Project:** To delete a specific project:

```bash
openstack project delete <project-name-or-ID>
```

### **5. Update a Project** To update a project’s properties:

```bash
openstack project set --description "<new-description>" <project-name-or-ID>
```

### **6. List Users in a Project:** To list all users associated with a specific project:

```bash
openstack role assignment list --project <project-name-or-ID>
```

### **7. Add a User to a Project:** To add a user to a project with a specific role:

```bash
openstack role add --project <project-name-or-ID> --user <user-name-or-ID> <role-name>
```

### **8. Remove a User from a Project:** To remove a user from a project:

```bash
openstack role remove --project <project-name-or-ID> --user <user-name-or-ID> <role-name>
```

### **9. Set Quotas for a Project:** To set resource quotas for a project:

```bash
openstack quota set --ram <ram-limit> --cores <core-limit> --instances <instance-limit> <project-name-or-ID>
```

### **10. Show Quotas for a Project:** To display the current quotas for a specific project:

```bash
openstack quota show <project-name-or-ID>
```

# **User**

# **OpenStack user related command**

### **1. List Users:** To list all users in your OpenStack environment:

```bash
openstack user list
```

### **2. Show User Details:** To display detailed information about a specific user:

```bash
openstack user show <user-name-or-ID>
```

### **3. Create a User:** To create a new user:

```bash
openstack user create --password <password> --email <email> <user-name>
```

### **4. Delete a User:** To delete a specific user:

```bash
openstack user delete <user-name-or-ID>
```

### **5. Update a User:** To update properties of a user, such as the email address or password:

```bash
openstack user set --email <new-email> <user-name-or-ID>
```

Or to update the password:

```bash
openstack user set --password <new-password> <user-name-or-ID>
```

### **6. List User Roles:** To list all roles assigned to a specific user:

```bash
openstack role assignment list --user <user-name-or-ID>
```

### **7. Add a Role to a User:** To assign a role to a user in a specific project:

```bash
openstack role add --project <project-name-or-ID> --user <user-name-or-ID> <role-name>
```

### **8. Remove a Role from a User:** To remove a role from a user:

```bash
openstack role remove --project <project-name-or-ID> --user <user-name-or-ID> <role-name>
```

### **9. Enable a User:** To enable a user account:

```bash
openstack user set --enable <user-name-or-ID>
```

### **10. Disable a User:** To disable a user account:

```bash
openstack user set --disable <user-name-or-ID>
```


