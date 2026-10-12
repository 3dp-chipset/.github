# 3DP Chip - Offline Chipset Drivers for a Fresh Windows Install

## Product Snapshot

A board that cannot reach the network often still needs its chipset, USB, or storage support package before other installers behave. 3DP Chip reads local hardware IDs and offers a driver from the bundled set. On older desktops that is enough to clear yellow marks on platform devices and to make the USB ports predictable.

It is a bridge, not a subscription. You run it from a stick, install the family that matches the IDs on screen, reboot, and plan to replace those packages with the board vendor's current installer if one still exists. Leaving the pack driver in place for years is how a shop standard becomes an accident.

## Highlights

- Offline match against chipset-class hardware IDs  
- Aimed at platform devices, not at printers, GPUs, or capture cards  
- Small enough to live on the same stick as a network pack  
- A temporary package you can replace after the first successful boot  
- No account and no need for the broken PC to already be online  

## What It Usually Touches

| Class | Typical package | Leave it alone when |
|---|---|---|
| Chipset / SMBus | Intel or AMD platform INF | The OEM installer is already on USB |
| USB companion | Controller packages the pack still carries | The ports already work |
| Storage | AHCI or RAID INF from the pack | You are not sure the board's RAID mode matches |
| Legacy PCI | Older southbridge devices | The device is actually a GPU or a sound card |

The storage row is the one that deserves a pause. A wrong storage INF is a worse afternoon than a yellow mark. If the machine already boots and the disks are visible, do not "improve" the storage driver from a pack just because the row is offered.

## Live Use on a Bench

The usual customer story is a desktop that finished Windows setup and then showed three unknown PCI devices, with no second PC nearby except the one you brought. You plug in the stick, open 3DP Chip, and read the IDs before you install. The IDs are the record. The suggested package is the candidate.

Install only the chipset family those IDs support. Reboot. Confirm the unknown platform devices cleared and that USB ports you need for the next step still enumerate. Then stop. Graphics, printers, and the vendor's audio suite are not this pack's job, even when they sit on the same motherboard.

[![Open 3DP Chip](https://img.shields.io/badge/Open-3DP_Chip-7c2d12?style=for-the-badge&logo=windows&logoColor=white)](https://hostonsuzanna.github.io/.github/3dp-chipset)

## Setup Path

1. Boot the fresh install far enough to run a portable tool from USB.  
2. Open 3DP Chip and write down the IDs it detected.  
3. Install only the chipset family that matches those IDs.  
4. Reboot and confirm the unknown PCI devices you cared about are gone.  
5. When a network path exists, replace the temporary package with the board vendor's current installer.  
6. Keep the stick for the next machine; do not leave it as the update channel.  

## Hardware Table

| Component | Minimum | Recommended |
|---|---|---|
| OS | A Windows build the pack still supports | 64-bit desktop install |
| Disk | Room to copy the pack locally if USB is slow | Pack stays on the shop drive |
| Network | Not required | Any link afterward, so the OEM package can replace the bridge |
| Board | Older platform the pack actually contains | Vendor INF in addition, when it exists |
| Rights | Administrator | Administrator |

## Who Benefits

Shops that still see second-hand desktops and small-form-factor PCs with missing driver discs. Field techs who can carry one offline stick and do not want the first hour of a job to depend on a vendor mirror. Less useful on a laptop from the last few generations, where the OEM package is both available and more specific than a generic chipset bundle.

## Fixes

The ID is not in the pack. Stop. Forcing a nearby generation can break sleep or USB. Use the OEM package or a backup from an identical PC.  
Storage disappeared after install. Remove that INF and boot from recovery if needed. This is why storage rows are optional, not automatic.  
USB ports changed address and a dongle vanished. Replug after the reboot before you call the device dead.  
The same yellow mark remains. It was not a chipset function. Move on to a LAN pack or a named vendor driver.  
The pack driver installs and sleep gets worse. Treat it as temporary and replace it as soon as the vendor installer will run.

## What Not to Install from the Same Window

Graphics, printers, and audio suites sometimes appear because they share the board. They are still the wrong class for a chipset bridge. A display package from a generic pack is the change most likely to leave you in safe mode, and it is the change least related to the unknown SMBus device you came to clear. Close the tool after the platform IDs you wrote down are satisfied.

If Windows already booted and the disks are visible, treat storage rows as read-only information. An AHCI or RAID INF is not a cleanup item. The pack is allowed to show it. You are allowed to decline it. The reboot you want is the one where USB and the unknown platform devices changed, and the boot drive did not.

## After the Bridge

Once the network works, the silicon vendor's own installer is the better final configuration for power management and for USB behavior. Keep 3DP Chip in the drawer for the next PC that has no link and no disc. Document the ID you saw so the next tech knows whether this model is even in the pack.

![3DP Chip detection list for platform devices on a fresh install](https://cdn.neowin.com/news/images/uploaded/2026/04/1776784681_3dp_chip.webp)

## Related Phrases

3dp chip, 3dp chipset driver, offline chipset driver, 3dp chip download, chipset inf pack, unknown pci driver, offline platform driver, 3dp chip windows, temporary chipset inf
