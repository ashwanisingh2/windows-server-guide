# Windows Server Easy Guide

A beginner-friendly, static Windows Server field guide written in simple Hinglish. It is designed to feel like a cheat sheet: choose a task, follow short steps, validate the result, and open a detailed guide only when needed.

## What is included

- **Easy dashboard** — choose between learning, setup, and troubleshooting.
- **5-minute Quick Start** — the safest setup order for beginners.
- **Printable Cheat Sheet** — daily AD, DNS, DHCP, GPO, file-share, and time commands.
- **Click-by-click GUI guides** — lab setup, AD DS, DNS, DHCP, users, GPO, file services, backup, Hyper-V, and PKI.
- **Troubleshooting guide** — symptoms, diagnostic commands, fixes, and escalation triggers.

## Start locally

No build step or package installation is required.

### Option 1: Open directly

Open `public/index.html` in a modern web browser.

### Option 2: Run a local static server

```bash
cd public
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Recommended learning order

1. Build a VirtualBox lab and take a snapshot.
2. Prepare the server name, static IP, gateway, and updates.
3. Install AD DS and promote the first Domain Controller.
4. Validate DNS before configuring DHCP.
5. Create users, OUs, groups, and a pilot GPO.
6. Configure file shares and NTFS permissions.
7. Configure backup and perform a restore test.

## Project structure

```text
public/
├── index.html                 # Easy dashboard
├── quickstart.html            # Beginner setup path
├── cheatsheet.html            # Printable daily cheat sheet
├── gui-style.css              # Shared styles and responsive layout
├── gui-lab-setup.html         # VirtualBox practice lab
├── gui-setup.html             # AD DS and DHCP
├── gui-dns.html               # DNS configuration
├── gui-users-gpo.html         # Users, OUs, groups, and GPO
├── gui-fileserver.html        # Shares and NTFS permissions
└── gui-troubleshooting.html   # Diagnostic and recovery guide
```

## Writing standard

When adding or updating a procedure, use this order:

1. **Kya** — what the task changes.
2. **Kyu** — why it is required.
3. **Before you start** — permissions, backup, values, and prerequisites.
4. **Kaise** — numbered GUI steps or commands.
5. **Validate** — command and expected successful result.
6. **If it fails** — safe rollback or escalation trigger.

Use placeholders such as `<domain>`, `<server>`, `<user>`, and `<IP>` for environment-specific values. Define an abbreviation such as Domain Controller (DC) the first time it appears.

## Safety

This guide is educational. Test changes in a lab before production. Use an approved maintenance window, create a verified backup, document the rollback plan, and keep console/iLO access available before changing network, Active Directory, DNS, DHCP, or Group Policy settings.

## Contributing

- Keep instructions short and outcome-focused.
- Prefer numbered steps over long paragraphs.
- Include an expected result for every validation command.
- Mark read-only checks separately from configuration changes.
- Do not publish real passwords, private IP plans, domain names, or customer information.
- Check all relative links after changing file names or section IDs.
