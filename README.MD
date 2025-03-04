# Creates LDPlayer9 instances with independent system disk


### Tested against Windows 10 / Python 3.11 / Anaconda

### pip install ldplayer9newinstances


```python
# Install LDPlayer9 and VirtualBox 
# Create the main emulator and at least one instance of it and run all created instances 
from ldplayer9newinstances import create_independent_instance
import random

basic_configuration = {
    "propertySettings.phoneIMEI": "351542017956834",
    "propertySettings.phoneIMSI": "460003931985310",
    "propertySettings.phoneSimSerial": "89861050793589253274",
    "propertySettings.phoneAndroidId": "5da5e11ca1b514d6",
    "propertySettings.phoneModel": "ASUS_Z01QD",
    "propertySettings.phoneManufacturer": "asus",
    "propertySettings.macAddress": (
        "%02x%02x%02x%02x%02x%02x" % tuple(random.randint(0, 255) for v in range(6))
    ).upper(),
    "statusSettings.playerName": "",
    "basicSettings.verticalSync": False,
    "basicSettings.fsAutoSize": 1,
    "basicSettings.autoRun": False,
    "basicSettings.rootMode": True,
    "statusSettings.closeOption": 0,
    "basicSettings.heightFrameRate": False,
    "basicSettings.adbDebug": 1,
    "advancedSettings.resolution": {"width": 1280, "height": 720},
    "advancedSettings.resolutionDpi": 240,
    "advancedSettings.cpuCount": 4,
    "advancedSettings.memorySize": 4096,
    "propertySettings.phoneNumber": "",
    "basicSettings.autoRotate": False,
    "basicSettings.isForceLandscape": False,
    "basicSettings.standaloneSysVmdk": True,
    "basicSettings.lockWindow": False,
    "advancedSettings.micphoneName": "",
    "advancedSettings.speakerName": "",
    "networkSettings.networkEnable": True,
    "networkSettings.networkSwitching": False,
    "networkSettings.networkStatic": False,
    "networkSettings.networkAddress": "0.0.0.0",
    "networkSettings.networkGateway": "0.0.0.0",
    "networkSettings.networkSubnetMask": "255.255.255.0",
    "networkSettings.networkDNS1": "8.8.8.8",
    "networkSettings.networkDNS2": "8.8.4.4",
    "networkSettings.networkInterface": "",
    "basicSettings.disableMouseFastOpt": True,
    "basicSettings.cjztdisableMouseFastOpt_new": 0,
    "basicSettings.HDRQuality": 0,
    "basicSettings.qjcjdisableMouseFast": 1,
    "basicSettings.fps": 60,
    "basicSettings.astc": True,
    "hotkeySettings.backKey": {"modifiers": 0, "key": 27},
    "hotkeySettings.homeKey": {"modifiers": 0, "key": 112},
    "hotkeySettings.appSwitchKey": {"modifiers": 0, "key": 113},
    "hotkeySettings.menuKey": {"modifiers": 0, "key": 114},
    "hotkeySettings.zoomInKey": {"modifiers": 0, "key": 115},
    "hotkeySettings.zoomOutKey": {"modifiers": 0, "key": 116},
    "hotkeySettings.bossKey": {"modifiers": 2, "key": 81},
    "hotkeySettings.shakeKey": {"modifiers": 0, "key": 120},
    "hotkeySettings.operationRecordKey": {"modifiers": 0, "key": 121},
    "hotkeySettings.operationRecordPauseKey": {"modifiers": 0, "key": 0},
    "hotkeySettings.operationRecordShowFrame": {"modifiers": 2, "key": 56},
    "hotkeySettings.fullScreenKey": {"modifiers": 0, "key": 122},
    "hotkeySettings.showMappingKey": {"modifiers": 0, "key": 123},
    "hotkeySettings.videoRecordKey": {"modifiers": 0, "key": 119},
    "hotkeySettings.mappingRecordKey": {"modifiers": 0, "key": 117},
    "hotkeySettings.keyboardModelKey": {"modifiers": 2, "key": 70},
}
newfolder = create_independent_instance(
    basic_config=basic_configuration,
    vboxmanage_path=r"C:\Program Files\Oracle\VirtualBox\VBoxManage.exe",
    ldplayer_folder=r"C:\LDPlayer",
)
print(newfolder)

```
