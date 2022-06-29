# AudioCaffeine

A small Windows script to disable energy-saving sleep on sound cards, particularly annoying if you use a screen reader.

Note that this is an attempt, the result is not sure... in the worst case, simply nothing changes.

If you ran version 1.0 without success, try with version 2.0.


## How to use

1. Download .zip from [here (1.0),][v1] or [here (2.0)][v2]
2. extract .bat file;
3. from context menu, choose "Run as administrator";
4. follow the procedure, writing "yes" (in lowercase and without quotes) to confirm various steps.

##  Compatibility

Tested on Windows 10, but written to be compatible with Windows 11 too.

## How to work

It uses WMI/Powershell to get installed sound cards, their names and DeviceIDs. Then, it instructs Windows to avoid power saving for chosen device, adding in a specific registry location (DeviceId-dependent) three parameters (all set to 0): DeviceSelectiveSuspended, SelectiveSuspendEnabled, SelectiveSuspendSupported.


[v1]: https://github.com/ABuffEr/audioCaffeine/releases/download/v1.0/audioCaffeine-1.0.zip
[v2]: https://github.com/ABuffEr/audioCaffeine/releases/download/v2.0/audioCaffeine-2.0.zip
