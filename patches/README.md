# patches needed to build a flashable ROM for xiaomi mione

* `xiaomi_mione_wifi.patch`: updates `hardware/libhardware_legacy` to select
  BCM4329/BCM4330 module arguments and firmware paths at runtime.
* `xiaomi_mione_wpa_supplicant.patch`: disables PMF/key management offload for
  the legacy Broadcom driver used by mione_plus.

apply patches
-------------

Just run script `./applypatch.sh`.
After patches applied, don't run this script again.


generate patches
----------------

run `repo diff -u project > output.patch` command.
_-u_ is required to inclued the project path
