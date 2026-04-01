# === Milinate System FAQ ===
This GitHub repository will host documentation and index pages until the official website is launched. Below you will find answers to frequently asked questions about the Milinate System distribution.

## Q: What is Milinate System and who is it for?
- A: Milinate System is a Linux distribution built on one principle: respect for its users. You install the system, customize it to your liking, and then you can simply work.

## Q: Why did you reject systemd, Wayland, and GNU coreutils?
- A: 
  - systemd takes on too much and does it poorly: process parallelization is too crude, it uses its own journald format for logging, and it doesn't restart services if they fail.
  - Wayland performs poorly on older and mid-range NVIDIA graphics cards, which is why we chose X11, where everything works as expected.
  - GNU coreutils has issues with locales and vulnerabilities in text sorting commands (CVE-2013-0222, CVE-2024-0684, CVE-2024-0684) that can compromise the system through stack overflow, among other problems.

## Q: How is milcore different from milwf? Can they be installed separately?
- A: The entire Milinate System is composed of three large "brick" packages:
  - **milcore** (Milinate Core) – the base system.
  - **milwf** (Milinate WorkFlow) – the LXDE desktop environment.
  - **milwn** (MilWiNdow) – a targeted Windows OS emulation solution.
They can be installed separately, but they are interdependent. To get the most out of the system, installing all three is recommended.

## Q: What is the role of the mpc package manager, and how does it differ from apt/pacman?
- A: The role of any package manager is to manage packages. MPC differs by being more feature-packed while unifying features found in other package managers, all within a simplified framework without losing functionality. In many distributions with their own packaging system, the package building tool and the package management tool are separate. For example, Arch Linux uses `makepkg` and `pacman`. With MPC, everything is integrated: `mpc skel` and `mpc build` — two commands, and you have a working package that can be installed with `mpc install`.

## Q: What is the security situation? Is there package signing verification?
- A: All files within packages undergo SHA-256 hashing. MPC also checks scripts for dangerous commands (the list is at the beginning of the script).

## Q: What desktop environment will users get with milwf?
- A: A fully configured LXDE desktop environment.

## Q: Where can I download Milinate System and how do I install it?
- A: Currently, the installation ISO is not ready. However, you can request a test version of milcore from the developer ( t.me/cheesecake1337 ) and install it manually. All necessary tools are available for this.

## Q: How can the community help the project?
- A: By starring the repository on GitHub, financially, and by building packages for MPC.

---
