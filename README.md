# ansible-role-udev-block-device-mode

###### Status: Unstable

(Persistently) set a block device's permissions to a given value using udev rules

## Example

```yaml
- name: Ensure cache block device allows RW from everyone
  ansible.builtin.include_role: mangadex.udev_block_device_mode
  vars:
    udev_rule_order: "50"
    udev_rule_device: "sdb"
    udev_rule_mode: "0666"
    udev_rule_comment: "Allow RW from docker container's non-root user"
```
