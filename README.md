# AudioCaffeine

A small Windows script to disable energy-saving sleep on sound cards, particularly annoying if you use a screen reader.

## How to use

1. Download .zip from [here;][release]
2. extract .bat file;
3. from context menu, choose "Run as administrator";
4. follow the procedure, writing "yes" (in lowercase and without quotes) to confirm various steps.

##  Compatibility

Tested on Windows 10, but written to be compatible with Windows 11 too.

## How to work

It uses WMI/Powershell to get installed sound cards, their names and DeviceIDs. Then, it instructs Windows to avoid power saving for chosen device, adding in a specific registry location (DeviceId-dependent) three parameters (all set to 0): DeviceSelectiveSuspended, SelectiveSuspendEnabled, SelectiveSuspendSupported.


[release]: https://github.com/ABuffEr/audioCaffeine/releases/download/v1.0/audioCaffeine-1.0.zip
