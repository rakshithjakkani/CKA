# Authentication and Authorization in kubernetes
    * There are 3 mechanisms in kubernetes
        1. AllowAlways
        2. DenyAlways
        3. RBAC
    # AllowAlways: This can be configured at the api-server level. where we can allow the users to access all the objects in the cluster
    # DenyAlways: Its similar to the AllowAlways type. But the only difference is, It deny users to access kubernetes objects in the cluster
    # RBAC: The most used and famous authorization type in kubernetes. where we can give granular permission to the users using Role & RoleBinding, ClusterRole & ClusterRoleBinding. 
        
