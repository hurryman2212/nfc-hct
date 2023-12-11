# NFC HCT(Host Capability Tester)

This is an Android application (compatible with APIs above Level 28) to test the NFC capability of the host device.
It shows whether the Android host system supports the following capabilities:
1. HCE-A/B or HCE-F capability (which includes NFC-A/B or NFC-F capability, duh)
2. eSE/microSD SE/SIM SE capability with the available reader(s)

## What is this for?

This is useful to determine whether your device "truly" doesn't support Korean(NFC-A/B SIM SE)/Japanese(Osaifu-Keitai - NFC-F eSE/SIM SE)/whatever local ecosystem based on any of NFC variants.

For example, currently (2019-01-21) Japanese Osaifu-Keitai payment (like Suica) requires FeliCa (NFC-F) with SIM SE support (or for some devices like Google Pixel series, HCE-F or FeliCa w/ eSE is enough).
Likewise, Korean payment systems like T-money or Cashbee require NFC-A/B with SIM SE but Railplus or JUSTOUCH require only HCE-A/B (which does not require any secure element medium).

For the information about HCE or NFC SE, please read [the following page](https://developer.android.com/guide/topics/connectivity/nfc/hce).

As of now (2023-12-12), [NFC-F support is (mostly) not limited by hardware factor](https://atadistance.net/2021/11/15/mobile-felica-evolution-for-2022/).
Even for global SKUs that are not possible to host Suica cards due to the software/firmware limitation, it is possible to host E-amusement passes that do not depend on the full Felica stack.
