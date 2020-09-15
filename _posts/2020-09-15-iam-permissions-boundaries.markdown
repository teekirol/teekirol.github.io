
Without permission boundaries, an IAM user or role may create additional roles  with greater permissions than it has itself. 

With permission boundaries, this can be prevented. The end result is the roles that the principal may create are restricted to permissions that are the intersection of its own permissions and the permission boundary permissions.