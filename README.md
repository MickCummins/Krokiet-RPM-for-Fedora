# Krokiet RPM for Fedora

Prebuilt native RPM packages for **Krokiet** (the official Slint-based GUI frontend replacing Czkawka GTK) targeted for Fedora Linux.

---

## What is Krokiet?

[Krokiet](https://github.com/qarmin/czkawka) is the modern graphical frontend for the **Czkawka** duplicate cleaner engine. It helps you quickly find and remove:

* Duplicate files (by hash or size)
* Similar images and videos
* Same music files (by audio fingerprint/metadata)
* Empty files, directories, and broken symlinks
* Temporary, cache, and junk files

---

## Purpose of this Package

While Krokiet can be installed via Flatpak or compiled directly via Cargo, this RPM package provides a native, system-integrated installation for Fedora users:

* **Native Desktop Integration:** Installs the binary directly to `/usr/bin/krokiet` along with proper desktop launchers (`.desktop`) and application icons in `/usr/share/pixmaps`.
* **Automated Dependency Management:** Declares standard dependencies—such as `ffmpeg` for video duplicate detection—so DNF pulls them in automatically during installation.
* **Clean System Management:** Fully managed by DNF and RPM. You can check updates, verify file integrity, or remove it cleanly without stray binaries or user-space build artifacts.

---

## Installation

### 1. Enable RPM Fusion (Recommended for Full Codec Support)

For video comparison features, Krokiet relies on `ffmpeg`. If you do not have RPM Fusion enabled yet:

```bash
sudo dnf install -y \
  [https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm](https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm) -E %fedora).noarch.rpm \
  [https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm](https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm) -E %fedora).noarch.rpm
