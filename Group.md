# **Group**

# **OpenStack group related command**

1. **List Groups:**
To list all groups in your OpenStack environment:
    
    ```bash
    openstack group list
    ```
    
2. **Show Group Details:** To display detailed information about a specific group:
    
    ```bash
    openstack group show <group-name-or-ID>
    ```
    
3. **Create a Group:** To create a new group:
    
    ```bash
    openstack group create --description "<description>" <group-name>
    ```
    
4. **Delete a Group:** To delete a specific group:
    
    ```bash
    openstack group delete <group-name-or-ID>
    ```
    
5. **Update a Group:** To update properties of a group:
    
    ```bash
    openstack group set --description "<new-description>" <group-name-or-ID>
    ```
    
6. **Add Users to a Group:** To add users to a specific group:
    
    ```bash
    openstack group add user <group-name-or-ID> <user-name-or-ID>
    ```
    
7. **Remove Users from a Group:** To remove users from a specific group:
    
    ```bash
    openstack group remove user <group-name-or-ID> <user-name-or-ID>
    ```
    
8. **List Users in a Group:** To list all users that belong to a specific group:
    
    ```bash
    openstack group show <group-name-or-ID> -f value -c users
    ```
    
9. **Assign Roles to a Group: T**o assign a role to a group in a specific project:
    
    ```bash
    openstack role add --group <group-name-or-ID> --project <project-name-or-ID> <role-name>
    ```
    
10. **Remove Roles from a Group:** To remove a role from a group:
    
    ```bash
    openstack role remove --group <group-name-or-ID> --project <project-name-or-ID> <role-name>
    
    ```
