# Phase 02-installation

(Coming soon)


## 2.3 VM creation

Created via `VBoxManage` CLI rather than the GUI wizard, for reproducibility.

- **Name:** NPL-SAP-Trial
- **RAM:** 8192 MB
- **vCPUs:** 4 (host has 16 logical CPUs)
- **Disk:** 120 GB dynamically-allocated VDI, SATA controller
  - Adjusted down from the Phase 1 target of 130-150 GB: host only has one
    drive (C:) with 187 GB free. 120 GB still clears SAP's ~102 GB
    requirement (100 GB server + 2 GB client) while leaving ~65 GB free on
    the host drive after the VM disk is reserved.
- **Networking:** NAT with port forwarding (guest has no direct LAN presence):
  - 3200 -> SAP dispatcher (sapdp00, for SAP GUI)
  - 3300 -> SAP gateway (sapgw00, for RFC)
  - 8000 -> HTTP/ICM
  - 4237 -> SAPinst web installer GUI
  - 2222 -> SSH (host port 2222 to guest port 22)
- **Optical drive:** empty, ready for the openSUSE Leap 15.4 ISO

## 2.4 openSUSE Leap installation
*(pending)*

## 2.5 SAP AS ABAP install via install.sh
*(pending)*
