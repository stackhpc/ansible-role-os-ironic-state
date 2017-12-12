OpenStack Ironic Node State
===========================

This role can be used to set the provision state of ironic nodes.

Requirements
------------

The OpenStack keystone and ironic APIs should be accessible from the target
host.

Role Variables
--------------

`os_ironic_state_auth_type`: Authentication type as used by `os_*` modules'
`auth_type` argument.

`os_ironic_state_auth`: Authentication options as used by `os_*` modules'
`auth` argument.

`os_ironic_state_name`: Name of the ironic node.

`os_ironic_state_provision_state`: Desired provision state.

`os_ironic_state_delegate_to`: Host to delegate to.

`os_ironic_state_wait`: Whether to wait for the state transition to complete.
Default is `True`.

`os_ironic_state_timeout`: Time to wait for state transition to complete, if
`os_ironic_state_wait` is `True`. Default is 1200 seconds.

Dependencies
------------

The delegate host should have the python `shade` module installed.

Example Playbook
----------------

Author Information
------------------

- Mark Goddard (<mark@stackhpc.com>)
