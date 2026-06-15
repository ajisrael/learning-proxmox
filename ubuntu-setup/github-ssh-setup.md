# GitHub SSH Key Setup

## Generate an SSH Key Pair

SSH into the VM or use the console in the Proxmox web UI.

```bash
ssh-keygen -t ed25519 -C "your-email@example.com"
```

Press Enter to accept the default location (`~/.ssh/id_ed25519`). Optionally set a passphrase.

## Add the Public Key to GitHub

Print the public key:

```bash
cat ~/.ssh/id_ed25519.pub
```

Copy the output. Then:

1. Go to **GitHub.com → Settings → SSH and GPG keys** (or directly to https://github.com/settings/keys)
2. Click **New SSH key**
3. Give it a title (e.g., the VM's hostname)
4. Paste the public key and click **Add SSH key**

## Clone a Private Repository

```bash
git clone git@github.com:username/repository.git
```

## Verify the Connection

```bash
ssh -T git@github.com
```

You should see: `Hi <username>! You've successfully authenticated, but GitHub does not provide shell access.`
