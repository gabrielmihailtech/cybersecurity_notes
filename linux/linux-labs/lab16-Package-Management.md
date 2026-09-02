# Lab 16 - Package Management

Commands:

- apt update
- apt upgrade
- apt install
- apt remove
- apt search
- apt show
- dpkg -l

Learned:

- Linux software is managed through packages
- apt is used to install, update, search, and remove packages
- dpkg can display installed packages
- package information can be viewed before installation
- installed software can be identified during investigations

Examples:

Update package list:

```bash
sudo apt update
```

Purpose:

```text
Refresh package repository information.
```

View available upgrades:

```bash
apt list --upgradable
```

Install a package:

```bash
sudo apt install tree
```

Verify installation:

```bash
dpkg -l | grep tree
```

Observed Result:

```text
tree package installed
```

Use installed package:

```bash
tree ~/linux-lab
```

Purpose:

```text
Display directory structure in a tree format.
```

Display package information:

```bash
apt show tree
```

Information Available:

- package name
- version
- dependencies
- description
- maintainer

Search for packages:

```bash
apt search nmap
```

```bash
apt search wireshark
```

Purpose:

```text
Locate software available in repositories.
```

Display installed packages:

```bash
dpkg -l
```

Check specific package:

```bash
dpkg -l | grep tree
```

Remove package:

```bash
sudo apt remove tree
```

Important Concepts:

Package Manager:

```text
apt
```

Installed Package Database:

```text
dpkg
```

Common Commands:

```bash
sudo apt update
sudo apt upgrade
sudo apt install package
sudo apt remove package
apt search package
apt show package
dpkg -l
```

SOC Investigation Use Cases:

Check installed software:

```bash
dpkg -l
```

Verify presence of tools:

```bash
dpkg -l | grep nmap
```

Investigate installed applications:

```bash
apt show package
```

Identify unexpected software:

```bash
dpkg -l
```

Key Takeaways:

- apt manages software packages in Linux
- dpkg lists installed packages
- apt search finds available software
- apt show displays package details
- apt install adds software
- apt remove removes software
- Installed software can provide useful information during SOC and DFIR investigations
