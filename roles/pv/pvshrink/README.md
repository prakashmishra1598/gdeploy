pvshrink
=========
pvshrink shrinks PhysicalVolume which may already be in a volume group and have active logical volumes allocated on it.

Requirements
------------
Existing PhysicalVolume on the disk mentioned.

Role Variables
--------------
    disk- disk or partition on which the pv will be shrunk.
    setphysicalvolumesize (--setphysicalvolumesize)
    Overrides the automatically-detected size of the PV.  Use with care, or prior to reducing the physical size of the device.

Example Playbook to call the role
---------------------------------
    - hosts: servers
      roles:
         - ../pvshrink

Example of variable values that can be passed
---------------------------------------------
      action=resize
      disk=<disk>
      setphysicalvolumesize=1G
