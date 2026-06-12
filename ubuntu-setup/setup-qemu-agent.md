# Ubuntu VM QEMU Guest Agent

## Enable QEMU Guest Agent in Proxmox

Shut down the Ubuntu VM.

In the Proxmox web UI, select the VM and go to the **Options** tab.

Double-click **QEMU Guest Agent**, check **Use QEMU Guest Agent**, then click OK.

Start the VM.

## Install qemu-guest-agent in Ubuntu

SSH into the VM or use the console in the Proxmox web UI.

Run the following commands:

```bash
sudo apt update && sudo apt install -y qemu-guest-agent
sudo systemctl enable --now qemu-guest-agent
```

## Verify

Once the agent is running, the VM's IP addresses will appear in the Proxmox **Summary** tab.

To verify from the Proxmox host shell:

```bash
qm agent <vmid> ping
```

A successful response confirms the agent is working.
