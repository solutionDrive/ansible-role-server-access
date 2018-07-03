# solutiondrive.server-access

This role manages authorized keys for a specified user on the specified hosts

## Role Variables

- `sd_access_user`  user the keys will be deployed for
- `sd_access_authorized_keys`  the keys that will be deployed (default: all keys in the directory `files`)


## Example Playbook

Example that will provision all access keys included under `files` for user `ubuntu`

```
    - role: solutiondrive.server-access
      sd_access_user: "ubuntu"
```

Example for providing the access key from `user.pub`  for user `ubuntu`

```
    - role: solutiondrive.server-access
      sd_access_user: "ubuntu"
      sd_access_authorized_keys: ["user.pub"]
```

## Author Information

Role is writte by Patrick Jahns <jahns@solutiondrive.de>