# Usage

Backuped from origin README.md

## Requirements
* zip
* unzip
* lzip
* tar

### Usage
```bash
  usage : ./convert-opengappss-to-magisk.sh <opengapps flashable zip file> <output directory>

    e.g : ./convert-opengappss-to-magisk.sh gapps.zip ./magisk-template/system
```
### Examples
```bash
./convert-opengappss-to-magisk.sh open_gapps-arm64-9.0-pico-20190920.zip ./magisk-template/system
```
Then you can look `./magisk-template`.It will have a system folder with android `/system` structures.You can zip it into a magisk module zip.

**In this case:**
```bash
cd ./magisk-template
zip -r ../Magisk-opengapps-arm64-9.0-20190920.zip *
```
Finally, you can push this zip file into your device and open `Magisk Manager` flash it.
### Blacklist
It provides a blacklist array in convert-opengappss-to-magisk.sh.
You can modify it to opt which you need.

**Recommend Blacklist:**
* googleonetimeinitializer-all 
* gmssetup-all 
* setupwizarddefault-all 
* setupwizardtablet-all 
* googlepartnersetup-all 
* packageinstallergoogle-all 
* carriersetup-all 
* backuprestore-all 
* googlebackuptransport-all

*This list can fix some devices cannot boot.*

**Full Optional Blacklist:**
* backuprestore-all
* carriersetup-all
* configupdater-all
* defaultetc-common
* defaultframework-common
* extservicesgoogle-all
* extsharedgoogle-all
* gmscore-arm64
* gmssetup-all
* googlebackuptransport-all
* googlecontactssync-all
* googlefeedback-all
* googleonetimeinitializer-all
* googlepartnersetup-all
* gsfcore-all
* setupwizarddefault-all
* setupwizardtablet-all
* soundpicker-all
* vending-arm
* calsync-all
* dialerframework-common
* googletts-arm64
* packageinstallergoogle-all


